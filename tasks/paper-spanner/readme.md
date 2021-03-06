# Google Spanner

## Список для чтения
* [Spanner: Google's Globally-Distributed Database](https://www.usenix.org/system/files/conference/osdi12/osdi12-final-16.pdf)
* [Spanner, TrueTime and the CAP Theorem](https://ai.google/research/pubs/pub45855)

### Spanner Txns Documentation
* [Transactions](https://cloud.google.com/spanner/docs/transactions)
* [Life of Cloud Spanner Reads & Writes](https://cloud.google.com/spanner/docs/whitepapers/life-of-reads-and-writes)

### Дополнительно
* [Beyond TrueTime: Using AugmentedTime for Improving Spanner](https://cse.buffalo.edu/~demirbas/publications/augmentedTime.pdf)
* [Two-Phase Locking](http://www.mathcs.emory.edu/~cheung/Courses/554/Syllabus/7-serializability/2PL.html)

## Вопросы

Все вопросы про 2PL или 2PC касаются не общего алгоритма, а его реализации в Google Spanner.

* Как _commit wait_ позволяет получить согласованные _snapshot reads_ без блокировок? Подумайте, как связаны снапшоты и порядок сериализации транзакций в 2PL.

---

* Зачем разделять транзакции на несколько классов?
* Классический алгоритм 2PL не оперирует версиями записей, а перезаписывает их. Снапшоты появлялись в алгоритме Snapshot Isolation, который правда не гарантировал сериализуемости. Зачем Spanner смешивает два этих подхода?
* В системе есть _standalone_ чтения и записи наравне с транзакциями. Как описать их семантику при конкуренции с транзакциями?
* В статье используется термин _external consistency_ для обозначения модели согласованности, которую предоставляет система. Найдите эту модель на [диаграмме](https://jepsen.io/consistency).
* Что может стать причиной отката (_abort_) транзакции?
* Механизм _leader leases_ означает, что после смерти лидера в Paxos новый лидер не будет выбран до тех пор, пока не протухнет таймер лизы на большинстве реплик. Означает ли это, что в случае смерти лидера шарда этот шард становится на некоторое время недоступным и на чтение, и на запись?
* Делается ли в описанном в статье механизме _leader leases_ поправка на дрейф физических часов?
* Как транзакции назначается временная метка коммита? 
* RW-транзакции используют 2PL, т.е. берут блокировки на диапазоны строк. Что происходит с этими блокировками, если клиент умирает?
* Как система обходит дэдлоки в 2PL?
* Где хранятся блокировки, которые берет транзакция в 2PL? Что если лидер умрет 1) до коммита 2) во время коммита?
* Что происходит в системе на стадии _prepare_ двухфазного коммита?
* Как система гарантирует, что RO-транзакция не может увидеть только часть записей другой RW-транзакции в процессе коммита последней? Иначе говоря, как достигается атомарность нескольких записей в один шард?
* Система позволяет клиенту читать данные не только с лидера шарда, а с любой из реплик. Может ли клиент в этом случае не увидить некоторых записей, потому что они еще не доехали на реплику?
* Зачем каждому шарду поддерживать нижнюю локальную оценку $`s_{i,g}^{prepare}`$ на временную метку коммита транзакции? Подумайте в сторону $`t_{safe}`$.
* Приведите пример _paxos write_, которая не является клиентской записью. В чем смысл $`t_{safe}^{paxos}`$?
* Как механизм _leader leases_ помогает поддерживать $`t_{safe}^{paxos}`$?
* Как дождаться $`t > t_{safe}_^{paxos}`$ на реплике в случае, когда в систему никто ничего не пишет?
* Кто координирует выполнение распределенной транзакции?
* В каком случае транзакция проходит через протокол 2PL, но не проходит через 2PC?
* Какая дополнительная статья расхода появляется в случае транзакции, которая задевает несколько шардов?
* Кто такие _armageddon masters_?
* Какую неопределенность достигает TrueTime? Какой дрейф локальных часов при этом закладывается (в пересчете на сутки)?
* Зачем в TrueTime одновременно использовать и GPS, и атомные часы?
* Как дизайн системы вокруг TrueTime связан с ее геораспределенностью? Нужен ли вам TrueTime, если вы живете в пределах одного ДЦ?
