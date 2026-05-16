🚀 What is KRaft?
===================
KRaft stands for Kafka Raft Metadata mode.
It’s a new way for Kafka to manage its cluster without ZooKeeper. 
Instead of relying on ZooKeeper, Kafka brokers themselves use the Raft consensus algorithm to agree on metadata and leadership.


🧩 Why KRaft Was Introduced
=============================
- Simpler architecture → No need to set up and maintain a separate ZooKeeper cluster.
- Better scalability → Kafka can handle larger clusters more efficiently.
- Unified system → Metadata and data are managed in one place.
- Future direction → ZooKeeper is being phased out; KRaft is the default in newer Kafka versions.


🎯 Simple Analogy
==================
Imagine a sports team:
- In the old system (ZooKeeper), there was a coach outside the team who decided who the captain was and kept track of players.
- In the new system (KRaft), the players themselves vote and agree on who the captain is, using a fair rule (Raft algorithm).
So now, the team doesn’t need an external coach — they self-organize.


🔑 How KRaft Works
====================
- Raft consensus → A group of brokers (called the quorum) agree on metadata changes.
- Metadata quorum → A small set of brokers store and replicate metadata.
- Leader broker → One broker acts as the leader, and others follow. If the leader fails, a new one is elected automatically.


👉 In short:
==============
KRaft makes Kafka self-sufficient. It’s like Kafka growing up and no longer needing ZooKeeper to babysit it.

