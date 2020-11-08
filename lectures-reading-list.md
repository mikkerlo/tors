- [Why do we need distributed systems?](https://brooker.co.za/blog/2020/01/02/why-distributed.html)
- [Fallacies of Distributed Computing](https://en.wikipedia.org/wiki/Fallacies_of_distributed_computing)

# Лекции

## 1. Model / Time

- [Understanding GPS: Principles and Applications](http://d1.amobbs.com/bbs_upload782111/files_33/ourdev_584835O21W59.pdf)
- [Time, Clocks and GPS](http://www2.unb.ca/gge/Resources/gpsworld.nov-dec91.corr.pdf)
- [Relativistic Effects in the Global Positioning System](https://www.aapt.org/doorway/TGRU/articles/Ashbyarticle.pdf), [Why does GPS depend on relativity?](https://physics.stackexchange.com/a/128951), [GPS, Relativity, and pop-Science Mythology](http://www.alternativephysics.org/book/GPSmythology.htm)
- [Spanner, TrueTime and the CAP Theorem](https://ai.google/research/pubs/pub45855)

## 2. Consistency Models, Replicated R/W Register (ABD)

- [Consistency Models](https://jepsen.io/consistency), [Linearizability](https://jepsen.io/consistency/models/linearizable)
- [Cloud Spanner: TrueTime and External Consistency](https://cloud.google.com/spanner/docs/true-time-external-consistency)
- [Notes on Theory of Distributed Computing](http://www.cs.yale.edu/homes/aspnes/classes/465/notes.pdf), глава 16

## 3. Replication, Atomic Broadcast and Consensus

- [Unreliable Failure Detectors for Reliable Distributed Systems](https://www.cs.utexas.edu/~lorenzo/corsi/cs380d/papers/p225-chandra.pdf)
- [Sequential Consistency versus Linearizability](https://pdfs.semanticscholar.org/787c/d132b7c849863393a01ae8f0d92b6a3f8cb3.pdf)

## 4. Impossibility of Consensus

- [Impossibility of Distributed Consensus with One Faulty Process](https://groups.csail.mit.edu/tds/papers/Lynch/jacm85.pdf)
- [Notes on Theory of Distributed Computing](http://www.cs.yale.edu/homes/aspnes/classes/465/notes.pdf), глава 11
- [On the Minimal Synchronism Needed for Distributed Consensus](https://www.cs.huji.ac.il/~dolev/pubs/p77-dolev.pdf)
- [The Weakest Failure Detector for Solving Consensus](https://cs.nyu.edu/courses/fall18/CSCI-GA.3033-002/papers/cht.pdf)

## 5. Single Decree Paxos

- [Part-Time Parliament](https://lamport.azurewebsites.net/pubs/lamport-paxos.pdf)
- [Paxos Made Simple](https://lamport.azurewebsites.net/pubs/paxos-simple.pdf)
- Заметки Лесли Лампорта про [Part-Time Parliament](http://lamport.azurewebsites.net/pubs/pubs.html#lamport-paxos) и [Paxos Made Simple](http://lamport.azurewebsites.net/pubs/pubs.html#paxos-simple)
- [Notes on Theory of Distributed Computing](http://www.cs.yale.edu/homes/aspnes/classes/465/notes.pdf), глава 12
- [Псевдокод](https://pdos.csail.mit.edu/archive/6.824-2013/notes/paxos-code.html)
- [Неоднозначность](https://stackoverflow.com/questions/29880949/contradiction-in-lamports-paxos-made-simple-paper) в Paxos Made Simple, на которую ссылается Лэмпорт в своей [заметке](http://lamport.azurewebsites.net/pubs/pubs.html#paxos-simple)
- [Who are the legislators of Paxos](https://cs.stackexchange.com/questions/12401/who-are-the-legislators-of-paxos) 

## 6. State Machine Replication, MultiPaxos

- [I Heart Logs / Introduction](https://www.oreilly.com/library/view/i-heart-logs/9781491909379/ch01.html)
- [The Log: What every software engineer should know about real-time data's unifying abstraction](https://engineering.linkedin.com/distributed-systems/log-what-every-software-engineer-should-know-about-real-time-datas-unifying)

### Алгоритмы
- Multi-Paxos: [Paxos Made Moderately Complex](http://www.cs.cornell.edu/courses/cs7412/2011sp/paxos.pdf)
- Zookeeper Atomic Broadcast: [ZAB: High-performance broadcast for primary-backup systems](http://knowably-attachments.s3.amazonaws.com/u/55b69a1ce4b00ab397d67250/7c8734d3cf02154499a9b3161ef9f575/Zab_2011.pdf)
- RAFT: [In Search of an Understandable Consensus Algorithm](https://raft.github.io/raft.pdf)
- VR: [Viewstamped Replication Revisited](http://pmg.csail.mit.edu/papers/vr-revisited.pdf)
- [Vive La Difference: Paxos vs. Viewstamped Replication vs. Zab](https://arxiv.org/pdf/1309.5671.pdf)
- [Paxos vs Raft: Have we reached consensus on distributed consensus?](https://arxiv.org/abs/2004.05074)

### RAFT

- [RAFT Consensus Algorithm](https://raft.github.io/)
- [In Search of an Understandable Consensus Algorithm](https://raft.github.io/raft.pdf)
- [Consensus: Bridging Theory and Practice](https://github.com/ongardie/dissertation)
- [RAFT Lecture](https://www.youtube.com/watch?v=YbZ3zDzDnrw), [slides](https://raft.github.io/slides/raftuserstudy2013.pdf)
- [Why the "RAFT" name?](https://groups.google.com/forum/#!topic/raft-dev/95rZqptGpmU)
- [raft-dev Google Group](https://groups.google.com/forum/#!forum/raft-dev)

---

- MIT 6.824: [Part 1](https://pdos.csail.mit.edu/6.824/notes/l-raft.txt), [Part 2](https://pdos.csail.mit.edu/6.824/notes/l-raft2.txt)
- [Instructors' Guide to Raft](https://thesquareplanet.com/blog/instructors-guide-to-raft/)
- [Students' Guide to Raft](https://thesquareplanet.com/blog/students-guide-to-raft/)

---

- [ectd/raft](https://github.com/etcd-io/etcd/tree/master/raft)
- [LogCabin](https://github.com/logcabin/logcabin)

## 7. Paxos Made Live

- [Paxos Made Live - An Engineering Perspective](https://www.cs.utexas.edu/users/lorenzo/corsi/cs380d/papers/paper2-1.pdf)
- [Google SRE Book / Managing Critical State: Distributed Consensus for Reliability](https://landing.google.com/sre/book/chapters/managing-critical-state.html)
- [Consensus: Bridging Theory and Practice](https://github.com/ongardie/dissertation/blob/master/book.pdf?raw=true)
- [ZooKeeper Internals](https://www.oreilly.com/library/view/zookeeper/9781449361297/ch09.html)
- [Millions of Tiny Databases](https://www.usenix.org/conference/nsdi20/presentation/brooker)
- [Linearizable Quorum Reads in Paxos](https://www.usenix.org/conference/hotstorage19/presentation/charapko)

## 8. Distributed Transactions

- [How CockroachDB Does Distributed, Atomic Transactions](https://www.cockroachlabs.com/blog/how-cockroachdb-distributes-atomic-transactions/)
- [Transactions in Apache Kafka](https://www.confluent.io/blog/transactions-apache-kafka/)
- [Large-scale Incremental Processing Using Distributed Transactions and Notifications](https://research.google/pubs/pub36726/)
- [Spanner: Google’s Globally-Distributed Database](https://www.usenix.org/conference/osdi12/technical-sessions/presentation/corbett), [Cloud Spanner: Transactions](https://cloud.google.com/spanner/docs/transactions), [Spanner’s Concurrency Control](https://dahliamalkhi.files.wordpress.com/2016/08/spannerexplained-sigact2013b.pdf)
- [Calvin: Fast Distributed Transactions for Partitioned Database Systems](http://cs.yale.edu/homes/thomson/publications/calvin-sigmod12.pdf)
- [Spanner vs. Calvin: Distributed Consistency at Scale](https://fauna.com/blog/distributed-consistency-at-scale-spanner-vs-calvin), [Spanner vs. Calvin - Comparing consensus protocols in strongly consistent database systems](https://www.youtube.com/watch?v=5CKb8hmh9KU)
- [An Overview of Deterministic Database Systems](http://www.cs.umd.edu/~abadi/papers/abadi-cacm2018.pdf)
- [Comparing Distributed Transaction Architectures for the Cloud Era](https://www.youtube.com/watch?v=w_zYYF3-iSo) / Kyle Kingsbury

## 9. Formal Methods, TLA+

- [TLA+ Home Page](https://lamport.azurewebsites.net/tla/tla.html)
- [TLA+ Video Course](http://lamport.azurewebsites.net/video/videos.html)
- [If You’re Not Writing a Program, Don’t Use a Programming Language](http://bulletin.eatcs.org/index.php/beatcs/article/view/539/532)
- [Code Only Says What it Does](https://brooker.co.za/blog/2020/06/23/code.html)
- [What Good is Temporal Logic?](https://www.microsoft.com/en-us/research/uploads/prod/2016/12/What-Good-Is-Temporal-Logic.pdf)
- [TLA+ In Practice and Theory](https://pron.github.io/posts/tlaplus_part1)
- [Learn TLA+](https://learntla.com/introduction/)
- [Dr. TLA+ Series](https://github.com/tlaplus/DrTLAPlus)
- [TLA+ Google Group](https://groups.google.com/forum/#!forum/tlaplus)
- https://github.com/lemmy/BlockingQueue
- [Verdi: Formally Verifying Distributed Systems](http://verdi.uwplse.org/)

---

- [Use of Formal Methods at Amazon Web Services](https://lamport.azurewebsites.net/tla/formal-methods-amazon.pdf), [How Amazon Web Services Uses Formal Methods](https://www.cslab.pepperdine.edu/warford/math221/How-Amazon-Web-Services-Uses-Formal-Methods.pdf)
- [Experience of software engineers	using TLA+, PlusCal and TLC](http://tla2012.loria.fr/contributed/newcombe-slides.pdf)

### Примеры

- [Euclid](https://github.com/afronski/playground-courses/blob/master/tla-plus/euclid-algorithm-sample/Euclid.tla)
- [DieHard](https://github.com/jameshfisher/tlaplus/tree/master/examples/DieHard)
- [FPaxos](https://github.com/fpaxos/fpaxos-tlaplus/blob/master/FPaxos.tla)

### Спецификации

- [RAFT](https://github.com/ongardie/raft.tla/blob/master/raft.tla)
- [Flexible Paxos](https://github.com/fpaxos/fpaxos-tlaplus/blob/master/FPaxos.tla) – Single Decree Paxos with flexible quorums
- [Snapshot Isolation](https://github.com/will62794/snapshot-isolation-spec/blob/master/SnapshotIsolation.tla), [Serializable Snapshot Isolation](https://github.com/pron/amazon-snapshot-spec/blob/master/serializableSnapshotIsolation.tla) – алгоритмы изоляции транзакций
- [TLA+ in TiDB](https://github.com/pingcap/tla-plus)
- [TLA+ in CocroachDB](https://github.com/cockroachdb/cockroach/tree/master/docs/tla-plus), [Parallel Commits: An Atomic Commit Protocol For Globally Distributed Transactions](https://www.cockroachlabs.com/blog/parallel-commits/)
- [Kafka Replication Protocol](https://github.com/hachikuji/kafka-specification/blob/master/Kip101.tla), [доклад](https://www.confluent.io/kafka-summit-sf18/hardening-kafka-replication)
- [Consistency Models in CosmosDB](https://github.com/Azure/azure-cosmos-tla/blob/master/general-model/cosmos_client.tla), [доклад](https://www.youtube.com/watch?v=Ej6dlMBvUBI)
- [Ticket Lock](https://kernel.googlesource.com/pub/scm/linux/kernel/git/cmarinas/kernel-tla/+/master/ticketlock.tla) и [другие ядерные спеки](https://kernel.googlesource.com/pub/scm/linux/kernel/git/cmarinas/kernel-tla/+/master/), [доклад](https://linuxplumbersconf.org/event/2/contributions/60/)
- https://github.com/tlaplus/Examples

## 10. Byzantine Fault Tolerance, Ben-Or Randomized Algorithm

- [Randomized Protocols for Asynchronous Consensus](http://www.cs.yale.edu/homes/aspnes/papers/randomized-consensus-survey.pdf)

### Оригинальные статьи
- [Byzantine Generals Problem](https://people.eecs.berkeley.edu/~luca/cs174/byzantine.pdf)
- [Another Advantage of Free Choice](https://allquantor.at/blockchainbib/pdf/ben1983another.pdf)

## 11. Practical Byzantine Fault Tolerance (PBFT)

- [Paper](http://pmg.csail.mit.edu/papers/osdi99.pdf)
- [PhD thesis](https://www.microsoft.com/en-us/research/wp-content/uploads/2017/01/thesis-mcastro.pdf)
- [Talk by Miguel Castro](https://www.youtube.com/watch?v=Q0xYCN-rvUs), [Talk by Barbara Liskov](https://www.youtube.com/watch?v=Uj638eFIWg8)
- [From Viewstamped Replication to Byzantine Fault Tolerance](http://www.pmg.csail.mit.edu/papers/vr-to-bft.pdf)
- [Реализация PBFT из Hyperledger](https://github.com/hyperledger-archives/fabric/tree/master/consensus/pbft)
- [Subtle Details in PBFT](http://ug93tad.github.io/pbft/)
- [Zyzzyva](http://www.cs.cornell.edu/lorenzo/papers/kotla07Zyzzyva.pdf), [I Hate the Primary](https://twitter.com/heidiann360/status/1198966119555579907)
- [The Saddest Moment](https://scholar.harvard.edu/files/mickens/files/thesaddestmoment.pdf)

## 12-13. Bitcoin and cryptocurrencies

### Bitcoin

- [Bitcoin: A Peer-to-Peer Electronic Cash System](https://bitcoin.org/bitcoin.pdf)
- [Bitcoin and Cryptocurrency Technologies](http://bitcoinbook.cs.princeton.edu/)
- [Bitcoin's Academic Pedigree](https://queue.acm.org/detail.cfm?id=3136559)
- [Majority is not Enough: Bitcoin Mining is Vulnerable](https://www.cs.cornell.edu/~ie53/publications/btcProcFC.pdf)
- [Bitcoin Developer Guide](https://bitcoin.org/en/developer-guide)
- [Bitcoin Core](https://github.com/bitcoin/bitcoin)

---

- [Money in the modern economy: an introduction](https://www.bankofengland.co.uk/quarterly-bulletin/2014/q1/money-in-the-modern-economy-an-introduction)

### Ethereum

- [White Paper](https://github.com/ethereum/wiki/wiki/White-Paper)
- [Yellow Paper](https://ethereum.github.io/yellowpaper/paper.pdf)
- [A Proof of Stake Design Philosophy](https://medium.com/@VitalikButerin/a-proof-of-stake-design-philosophy-506585978d51)
- [Hard Problems of Cryptocurrency](https://github.com/ethereum/wiki/wiki/Problems)

### Анонимность

- [Zerocoin: Anonymous Distributed E-Cash from Bitcoin](http://zerocoin.org/media/pdf/ZerocoinOakland.pdf)
- [Zerocoin: making Bitcoin anonymous](https://blog.cryptographyengineering.com/2013/04/11/zerocoin-making-bitcoin-anonymous/)
- [Доклад про Zerocoin](https://www.youtube.com/watch?v=4uWlqPIb1zw)

## 14. HotStuff

- [HotStu: BFT Consensus in the Lens of Blockchain](https://arxiv.org/pdf/1803.05069.pdf)
- [State Machine Replication in the Libra Blockchain](https://developers.libra.org/docs/state-machine-replication-paper)