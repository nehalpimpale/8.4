# 8.4


1.Explain the difference between FIFO and Capacity scheduler

2.Explain the difference between FIFO and Fair scheduler

3.Explain the difference between Capacity and Fair scheduler

4.What are the limitations of hadoop 1.x and how they were overcome in hadoop 2.x


Q1. Explain the difference between FIFO and Capacity scheduler

1.FIFO Scheduler 


• The FIFO Scheduler places applications in a queue and runs them in the order of
submission (first in, first out).
• Requests for the first application in the queue are allocated first; once its
requests have been satisfied, the next application in the queue is served, and so
on.
• The FIFO Scheduler has the merit of being simple to understand and not needing
any configuration, but it’s not suitable for shared clusters.
• Large applications will use all the resources in a cluster, so each application has
to wait its turn. On a shared cluster, it is better to use the Capacity Scheduler or
the Fair Scheduler. 

2.Capacity Scheduler


• With the Capacity Scheduler, a separate dedicated queue allows the small job to
start as soon as it is submitted.
• This is at the cost of overall cluster utilization since the queue capacity is
reserved for jobs in that queue.
• If queues are not designed or used properly, some queues may be overloaded
while some may be underutilised.
• Large job finishes late when compared with using the FIFO Scheduler.

Q2. Explain the difference between FIFO and Fair scheduler

1.FIFO Scheduler 


• The FIFO Scheduler places applications in a queue and runs them in the order of
submission (first in, first out).
• Requests for the first application in the queue are allocated first; once its
requests have been satisfied, the next application in the queue is served, and so
on.
• The FIFO Scheduler has the merit of being simple to understand and not needing
any configuration, but it’s not suitable for shared clusters.
• Large applications will use all the resources in a cluster, so each application has
to wait its turn. On a shared cluster, it is better to use the Capacity Scheduler or
the Fair Scheduler. 

2.Fair Scheduler

• With the Fair Scheduler, there is no need to reserve a set amount of capacity,
since it will dynamically balance resources between all running jobs.
• Just after the first (large) job starts, it is the only job running, so it gets all the
resources in the cluster.
• When the second (small) job starts, it is allocated half of the cluster resources,
so that each job is using its fair share of resources.
• After the small job completes and no longer requires resources, the large job
goes back to using the full cluster capacity again.
• The overall effect is both high cluster utilization and timely small job completion.


Q3. Explain the difference between Capacity and Fair scheduler

1.Capacity Scheduler


• With the Capacity Scheduler, a separate dedicated queue allows the small job to
start as soon as it is submitted.
• This is at the cost of overall cluster utilization since the queue capacity is
reserved for jobs in that queue.
• If queues are not designed or used properly, some queues may be overloaded
while some may be underutilised.
• Large job finishes late when compared with using the FIFO Scheduler.

2.Fair Scheduler

• With the Fair Scheduler, there is no need to reserve a set amount of capacity,
since it will dynamically balance resources between all running jobs.
• Just after the first (large) job starts, it is the only job running, so it gets all the
resources in the cluster.
• When the second (small) job starts, it is allocated half of the cluster resources,
so that each job is using its fair share of resources.
• After the small job completes and no longer requires resources, the large job
goes back to using the full cluster capacity again.
• The overall effect is both high cluster utilization and timely small job completion.

Q4. What are the limitations of hadoop 1.x and how they were overcome in hadoop 2.x

Hadoop 1.x has many limitations or drawbacks. Main drawback of Hadoop 1.x is that MapReduce Component in it’s Architecture. That means it supports only MapReduce-based Batch/Data Processing Applications.

Hadoop 1.x has the following Limitations/Drawbacks:

1.It is only suitable for Batch Processing of Huge amount of Data, which is already in Hadoop System.

2.It is not suitable for Real-time Data Processing.

3.It is not suitable for Data Streaming.

4.It supports upto 4000 Nodes per Cluster.

5.It has a single component : JobTracker to perform many activities like Resource Management, Job Scheduling, Job Monitoring, Re-scheduling Jobs etc.

6.JobTracker is the single point of failure.

7.It does not support Multi-tenancy Support.

8.It supports only one Name Node and One Namespace per Cluster.

9.It does not support Horizontal Scalability.

10.It runs only Map/Reduce jobs.

11.It follows Slots concept in HDFS to allocate Resources (Memory, RAM, CPU). It has static Map and Reduce Slots. That means once it assigns resources to Map/Reduce jobs, it cannot re-use them even though some slots are idle.


Hadoop 2.x solves Hadoop 1.x Limitations


Hadoop 2.x has resolved most of the Hadoop 1.x limitations by using new architecture.

1.By decoupling MapReduce component responsibilities into different components.

2.By Introducing new YARN component for Resource management.

3.By decoupling component’s responsibilities, it supports multiple namespace, Multi-tenancy, Higher Availability and Higher Scalability.
Hadoop 2.x YARN Benefits


Hadoop 2.x YARN has the following benefits.

1.Highly Scalability

2.Highly Availability

3.Supports Multiple Programming Models

4.Supports Multi-Tenancy

5.Supports Multiple Namespaces

6.Improved Cluster Utilization

7.Supports Horizontal Scalability
