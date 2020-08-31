# Семинары

## Network / Faults
* [Primer on Latency and Bandwidth](https://hpbn.co/primer-on-latency-and-bandwidth/)
* [The Network is Reliable](https://blog.acolyer.org/2014/12/18/the-network-is-reliable/)
* [Inside a Google data center](https://www.youtube.com/watch?v=XZmGGAbHqa0), [Google Data Center 360° Tour](https://www.youtube.com/watch?v=zDAYZU4A3w0)
* [Google Cloud Infrastructure](https://cloud.withgoogle.com/infrastructure)
* [Inside Google Network](https://www.youtube.com/watch?v=hMUHwMg2pow)
* [Submarine Cable Map](https://www.submarinecablemap.com/)
---
* [What Can We Learn from Four Years of Data Center Hardware Failures?](https://pdfs.semanticscholar.org/e1ff/9a9441726e731d2fd8d5f8316f3a5da1ac68.pdf)

## TCP
* [Building Blocks of TCP](https://hpbn.co/building-blocks-of-tcp/)
* [TCP Puzzlers](https://www.joyent.com/blog/tcp-puzzlers)
* [Network Protocols for anyone who knows programming language](https://www.destroyallsoftware.com/compendium/network-protocols?share_key=97d3ba4c24d21147)
* [Introduction to Computer Networks / TCP Transport](http://intronetworks.cs.luc.edu/current/html/tcp.html)

## Local Storage
* [Algoritms Behind Modern Storage Systems](https://queue.acm.org/detail.cfm?id=3220266)
* [Database Internals Series on Disk I/O](https://medium.com/databasss/on-disk-io-part-1-flavours-of-io-8e1ace1de017])
* [TiKV Internals: B-Tree vs Log-Structured Merge-Tree](https://tikv.github.io/deep-dive-tikv/key-value-engine/B-Tree-vs-Log-Structured-Merge-Tree.html)
* [LevelDB](https://github.com/google/leveldb), [RocksDB](https://github.com/facebook/rocksdb/wiki)
* [RUM Conjecture](http://daslab.seas.harvard.edu/rum-conjecture/)
* [SSDs and Distributed Data Systems](https://blog.empathybox.com/post/24415262152/ssds-and-distributed-data-systems) 
* [A Brief History of Log Structured Merge Trees](https://ristret.com/s/gnd4yr/brief_history_log_structured_merge_trees)
* [Why we built CockroachDB on top of RocksDB](https://www.cockroachlabs.com/blog/cockroachdb-on-rocksd/)

## Distributed File System
* [The Google File System](https://ai.google/research/pubs/pub51)
* [GFS: Evolution on Fast-forward](https://queue.acm.org/detail.cfm?id=1594206)
* [Cluster-Level Storage @ Google](http://www.pdsw.org/pdsw-discs17/slides/PDSW-DISCS-Google-Keynote.pdf)
* MIT 6.824 [notes](https://pdos.csail.mit.edu/6.824/notes/l-gfs-short.txt), [faq](https://pdos.csail.mit.edu/6.824/papers/gfs-faq.txt)
* [HDFS Architecture](https://hadoop.apache.org/docs/stable/hadoop-project-dist/hadoop-hdfs/HdfsDesign.html) 
* [Лекция про HDFS](https://www.youtube.com/watch?v=IHVIFVZeXcA)

## Asynchrony 
* [epoll - I/O event notification facility](http://man7.org/linux/man-pages/man7/epoll.7.html)
* [Реактивный эхо-сервер на libuv](https://github.com/libuv/libuv/blob/v1.x/docs/code/tcp-echo-server/main.c)
* [Thinking Asynchronously: Designing Applications with Boost.Asio](https://www.youtube.com/watch?v=D-lTwGJRx0o), [slides](http://cpp.mimuw.edu.pl/files/boost_vs_qt/asio/thinking_asynchronously.pdf)
* [Your Server as a Function](https://monkey.org/~marius/funsrv.pdf)
* [Futures for C++11 at Facebook](https://engineering.fb.com/developer-tools/futures-for-c-11-at-facebook/), [Documentation](https://github.com/facebook/folly/blob/master/folly/docs/Futures.md)
* [Асинхронность в программировании](https://habr.com/ru/company/jugru/blog/446562/)
* [Реализация async/await в Kotlin](https://github.com/Kotlin/KEEP/blob/master/proposals/coroutines.md#state-machines)
* [C++ Coroutines: A Negative Overhead Abstraction](https://github.com/GorNishanov/await/blob/master/2015_CppCon/C%2B%2B%20Coroutines%20-%20Gor%20Nishanov%20-%20CppCon%202015.pdf)
* Rust: [Async/Await Proposal](https://github.com/rust-lang/rfcs/blob/master/text/2394-async_await.md), [Propagating Errors](https://doc.rust-lang.org/book/ch09-02-recoverable-errors-with-result.html#propagating-errors), [Await Syntax Write Up](https://paper.dropbox.com/doc/Await-Syntax-Write-Up-t9NlOSeI4RQ8AINsaSSyJ), [A final proposal for await syntax](https://boats.gitlab.io/blog/post/await-decision/)
* C++: [Better keywords for the Coroutines](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2019/p1485r1.html)
* [What Color is Your Function?](https://journal.stuffwithstuff.com/2015/02/01/what-color-is-your-function/)
* [C++ Coroutines: Understanding operator co_await](https://lewissbaker.github.io/2017/11/17/understanding-operator-co-await), 
* [Cactus](https://gitlab.com/levysotsky/shad-cpp-cactus/tree/master/cactus) – учебная библиотека для сетевого IO на файберах
* [Асинхронность: назад в будущее](https://habr.com/ru/post/201826/)
* [Echo server in Go](https://github.com/golergka/go-tcp-echo/blob/master/go-tcp-echo.go)

## Erasure Codes
* [Erasure Coding in Windows Azure Storage](https://www.usenix.org/conference/atc12/technical-sessions/presentation/huang)
* [Коды избыточности в Яндекс](https://habr.com/ru/company/yandex/blog/311806/)

## RAFT
* https://raft.github.io/
* [RAFT Lecture](http://youtu.be/YbZ3zDzDnrw), [Slides](https://ongardie.net/static/raft/userstudy/raft.pdf)
* https://github.com/etcd-io/etcd/tree/master/raft
* https://github.com/pingcap/raft-rs

## Crash Recovery, File Systems
* [xv6 Book](https://pdos.csail.mit.edu/6.828/2018/xv6/book-rev11.pdf), chapter 6
* [All File Systems Are Not Created Equal: On the Complexity of Crafting Crash-Consistent Applications](https://www.usenix.org/node/186195)
* [Files are hard](https://danluu.com/file-consistency/)
* [Protocol-Aware Recovery for Consensus-Based Storage](https://www.usenix.org/conference/fast18/presentation/alagappan)
* [Can Applications Recover from fsync Failures?](https://www.usenix.org/conference/atc20/presentation/rebello)

## Consensus as a Service – ZooKeeper
* [The Chubby lock service for loosely-coupled distributed systems](https://ai.google/research/pubs/pub27897)
* [ZooKeeper: Wait-free coordination for Internet-scale systems](https://www.usenix.org/legacy/event/usenix10/tech/full_papers/Hunt.pdf)
* [ZK docs](https://zookeeper.apache.org/doc/current/index.html), [API](https://zookeeper.apache.org/doc/r3.4.6/api/org/apache/zookeeper/ZooKeeper.html) 
* [ZooKeeper Internals](https://www.oreilly.com/library/view/zookeeper/9781449361297/ch09.html)
* [Distributed Consensus Reloaded: Apache ZooKeeper and Replication in Apache Kafka](https://www.confluent.io/blog/distributed-consensus-reloaded-apache-zookeeper-and-replication-in-kafka/)
* [Hardening Kafka Replication](https://yadi.sk/i/z0-7DDv4P4wSKw) 

## Actor model
* [Actor Model](https://www.youtube.com/watch?v=7erJ1DV_Tlo)
* [Message Passing and Actor Model](http://dist-prog-book.com/chapter/3/message-passing.html)
* [Akka](https://akka.io/)
* [Joe Armstrong – Making reliable distributed systems in the presence of sodware errors](http://erlang.org/download/armstrong_thesis_2003.pdf)
* [Orleans: Distributed Virtual Actors for Programmability and Scalability](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/Orleans-MSR-TR-2014-41.pdf)
* [Pony Programming Language](https://www.ponylang.io/)

## Gossiping
* [Randomized Gossip Methods](https://www.youtube.com/watch?v=Gxf5glthqrk)
* [SWIM: Scalable Weakly-consistent Infection-style Process Group Membership Protocol](https://www.cs.cornell.edu/~asdas/research/dsn02-swim.pdf)
* [SWIM Protocol explained](https://asafdav2.github.io/2017/swim-protocol/)

## Failure Detectors
* [Phi Accural Failure Detector](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.80.7427&rep=rep1&type=pdf)
* [Realization of φ accrual failure detector](https://github.com/atomix/atomix/issues/405)
* [Cassandra – Failure Detection and Recovery](https://docs.datastax.com/en/archived/cassandra/3.0/cassandra/architecture/archDataDistributeFailDetect.html)
* [Akka – Failure Detector](https://doc.akka.io/docs/akka/2.5.6/scala/cluster-usage.html#failure-detector)

## SRE Book
* https://landing.google.com/sre/sre-book/toc/index.html
* https://danluu.com/google-sre-book/ 

## Testing / Verification
* [Testing Distributed Systems with Deterministic Simulation](https://www.youtube.com/watch?v=4fFDFbi3toc)
* https://github.com/asatarin/testing-distributed-systems
* Jepsen / Fault injection
* Linearizability testing, https://github.com/rystsov/fast-jepsen
* Fuzzing

## Formal Methods
* PlusCal, трансляция в TLA+, тестирование аллокатора
* [Hardening Kafka Replication](https://www.confluent.io/kafka-summit-sf18/hardening-kafka-replication)

## CRDT
* [A comprehensive study of Convergent and Commutative Replicated Data Types](https://hal.inria.fr/inria-00555588/document)

## Cryptography
* Cryptographic Hash Functions
* Digital Signatures / [Elliptic Curves](https://andrea.corbellini.name/2015/05/17/elliptic-curve-cryptography-a-gentle-introduction/)
* Certificates
* [TLS](https://hpbn.co/transport-layer-security-tls/), Diffie-Hellman



## Misc
* [A List of Post-mortems!](https://github.com/danluu/post-mortems), https://danluu.com/postmortem-lessons/
* [Exponential Backoff and Jitter](https://aws.amazon.com/blogs/architecture/exponential-backoff-and-jitter/)
* [Queueing Theory in Practice: Performance Modeling for the Working Engineer](https://www.usenix.org/conference/lisa17/conference-program/presentation/freeman)