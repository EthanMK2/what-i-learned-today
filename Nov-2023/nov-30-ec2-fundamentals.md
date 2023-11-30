# Learning AWS EC2 fundamentals

With EC2, we can rent virtual machines from AWS for any kind of workload we might have. We can have any workload for AWS to handle, from data analysis and machine learning, to gaming servers and high performance computing. There are many types of ec2 instances that we can work with to maximize saving, computation, memory, or storage.

On-demand is for short workloads that need to be predictably priced and computed. This is the easiest to set up, but can be one of the pricier options.

Reserved instances are for longer workloads with predictable computation and/or timeframes of when to run your computations. The convertible type has a lots of flexible instances that can meet many specific needs.

Savings Plans rents VMs for 1 OR 3 years. You commit to a amount of usage, and is good for long workloads for the best savings and consistency. 

Spot instances are the cheapest option, but there's a catch, and a lot of configuration that may need to happen. We can use spot fleets to optimize the best bang-for-buck, and reestablish instances if they are 'lost'. How do they get lost? Well, you have to set up a 'bid price' for how much you are willing to pay for a VM instance. If the demand/price of the instance goes above your max price you want, your instances are forced to terminate. These spot instances are thus prone to termination, so only flexible and non-critical workloads are recommended.

Dedicated hosts are a service that allows you to reserve an entire physical server, and control the instance placement and other low-level configurations. This is the MOST expensive option, so it is recommended for businesses that must comply with regulation and/or software license restrictions.

Capacity Reservations reserve capacity in a specific Availability Zone for any duration. However, you pay for the reservation even if you do not use it. 
