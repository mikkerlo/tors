# Репликация регистра

Напишите спецификации для двух алгоритмов репликации регистра для случая 1 писателя:

## I. Наивные кворумные операции

Пусть с регистром работает только один писатель. 

Пусть операции `Get` и `Set` – однофазные:

- `Set` – кворумная запись – писатель увеличивает временную метку и отправляет команду $`\texttt{Write}(v, ts)`$ на реплики. Операция `Set` завершается, когда писатель получил подтверждение от большинства реплик (собрал _кворум_).

- `Get` – кворумное чтение – читатель в операции отправляет запрос на чтение $`\texttt{Read}()`$ на реплики и дожидается ответа от большинства (кворума), каждый ответ – пара $`(v, ts)`$. После этого он выбирает значение с наибольшей временной меткой и завершает чтение.

Напишите спецификацию `Quorum1WRegister.tla` и с помощью TLC убедитесь, что алгоритм нарушает линеаризуемость даже в случае 1 писателя. Получите с помощью TLC сценарий нарушения линеаризуемости.

## II. Двухфазное чтение

Пусть писатель по-прежнему один.

В отличие от предыдущего варианта, операция `Get` будет двухфазной:
- На первой фазе (назовем ее $`\texttt{Read}`$) читатель выполняет кворумное чтение: собирает с кворума реплик версии значения регистра и выбирает их них самое свежее.
- На второй фазе ($`\texttt{Write}`$) читатель пишет выбранное значение на большинство реплик.

Операция `Get` завершается и возвращает значение читателю только после завершения второй фазы, т.е. только после того, как перезапишет на кворум прочитанное значение.

Вторая фаза гарантирует, что после завершения операции `Get` никакой последующий `Get` не может прочитать более старое значение.

Напишите спецификацию `Linearizable1WRegister.tla` и с помощью TLC убедитесь в его корректности.

## Кворумы

- Вместо порогов для определения большинства используйте явную систему кворумов, с ее помощью можно будет легко устроить sanity check линеаризуемой версии алгоритма: достаточно задать систему подмножеств, где есть пара с пустым пересечением, после чего TLC должен найти нелинеаризуемое исполнение.

## Операции и истории

В алгоритме репликации регистра есть понятия _операции_ и _истории_. Посмотрите, устроена работа с этими понятиями в спеках алгоритмов изоляции транзакций:

- [Snapshot Isolation](https://github.com/will62794/snapshot-isolation-spec/blob/master/SnapshotIsolation.tla#L309)
- [Serializable Snapshot Isolation](https://github.com/pron/amazon-snapshot-spec/blob/master/serializableSnapshotIsolation.tla#L971)

## Линеаризуемость

- [Reading the Herlihy & Wing Linearizability paper with TLA+](https://github.com/lorin/tla-linearizability)

## Полезные техники

- Используйте [инвариант для проверки типов](https://github.com/pron/amazon-snapshot-spec/blob/master/serializableSnapshotIsolation.tla#L204) для отладки вашей спецификации. После отладки его стоит отключить для ускорения проверки модели.
- Обязательно используйте [symmetry sets](https://tla.msr-inria.inria.fr/tlatoolbox/doc/model/model-values.html) для ускорения проверки модели
- Пишите [юнит-тесты](https://github.com/pron/amazon-snapshot-spec/blob/master/serializableSnapshotIsolation.tla#L1062) для сложных операторов
- Убедитесь, что ваша спецификация порождает [нетривиальные исполнения](https://github.com/pron/amazon-snapshot-spec/blob/master/serializableSnapshotIsolation.tla#L1560)
- Убедитесь, что в любом исполнении вашей модели [все операции чтения и записи завершаются](https://github.com/pron/amazon-snapshot-spec/blob/master/serializableSnapshotIsolation.tla#L1022)
- Добавьте [заикание](https://github.com/pron/amazon-snapshot-spec/blob/master/serializableSnapshotIsolation.tla#L984) в предикат _Next_, чтобы чекер не ругался на дедлоки после завершения всех операций

Образец для подражания: https://github.com/pron/amazon-snapshot-spec/blob/master/serializableSnapshotIsolation.tla

# TLA

## Первые шаги

1. Установите [TLA Toolbox](https://lamport.azurewebsites.net/tla/toolbox.html)
2. Посмотрите уроки от Лесли Лампорта: [Resources and Tools](http://lamport.azurewebsites.net/video/video3.html) и [Die Hard](http://lamport.azurewebsites.net/video/video4.html)
2. Пропустите спеку [DieHard](https://github.com/tlaplus/Examples/tree/master/specifications/DieHard) через TLC, получите трассу с решением / нарушением инварианта

## Работа с TLA Toolbox

- [TLA+ Toolbox](https://lamport.azurewebsites.net/tla/toolbox.html)
- [Resources and Tools](https://lamport.azurewebsites.net/video/video3.html)
- [Using the Toolbox](https://learntla.com/pluscal/toolbox/)
- [Introduction to TLA+ Model Checking in the Command Line](https://medium.com/@bellmar/introduction-to-tla-model-checking-in-the-command-line-c6871700a6a2)

## Справочные материалы по TLA+/+Cal

- [Learn TLA+](https://learntla.com/introduction/) с акцентом на главу [Concurrency](https://learntla.com/concurrency/)
- [The TLA+ Video Course](https://lamport.azurewebsites.net/video/videos.html) – вводный курс от Лэсли Лампорта