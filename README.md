# Distributed Search System

Built a dynamic, fault-tolerant, and highly scalable document search system by adopting parallel TF-IDF algorithm, Apache Zookeeper, and leader election algorithm.

## Display of Distributed System (Leader Election)

1.Start server 1(left-top), server 2(right-top), server 3(left-bottom), and server 4(right-bottom) sequentially.
<img width="1440" alt="image" src="https://user-images.githubusercontent.com/70275050/178123953-fffb414a-521a-452d-888d-a669f10aca46.png">

2.Server 1 is the leader, server 2 to 4 are workers.
<img width="1438" alt="image" src="https://user-images.githubusercontent.com/70275050/178123965-99945960-d5b6-4875-a417-8fd80749a4f6.png">

3.As the leader, server 1 distributes calculation tasks and collects results from worker servers 2 to 4.
<img width="1440" alt="image" src="https://user-images.githubusercontent.com/70275050/178124069-15fb5428-49e0-4677-a5b4-8312b385e312.png">

4.If one of the workers went down accidentally, the system would still work.
<img width="1440" alt="image" src="https://user-images.githubusercontent.com/70275050/178124121-94c7b9e6-5318-436d-a5c5-b5fe8e9e3a4c.png">

5.If leader server went down, the system would reelect a new leader (server 2) from workers and the system would still work.
<img width="1440" alt="image" src="https://user-images.githubusercontent.com/70275050/178124144-ffb229b4-c49e-470e-9d5a-84841aec660a.png">

6.After the broken server recovered, it will join the workers and listen to the new leader.
<img width="1440" alt="image" src="https://user-images.githubusercontent.com/70275050/178124155-08f263b7-b4cf-41dc-830c-454682bb3298.png">


## Frontend Display
<img width="1432" alt="image" src="https://user-images.githubusercontent.com/70275050/178124096-af154601-d48f-49d9-958e-76a7ce28ca73.png">
<img width="1429" alt="image" src="https://user-images.githubusercontent.com/70275050/178123821-df5b8580-2fbc-458f-baca-7c694bf7ac5e.png">
