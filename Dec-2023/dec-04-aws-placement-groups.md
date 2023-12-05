# AWS Placement Groups

Placement groups are a way we can set up our EC2 instances in a way that suites our computation and risk needs. There are three major ways a placement group is configured: Cluster, Spread, and Partition. 

A cluster configuration makes the latency between EC2 instances incredibly fast and reliable (around 10Gbps!). This way, big data can be computed and analyzed with speed. However, this option can be risky, as all the EC2 instances are on the same 'rack' of servers. If the rack or data center is compromised and fails, then the EC2 instances all fail with it. This may happen rarely, and is more of a warning in legal terms than practical terms. Although, I have to acknowledge that a power outage or unethical hack is always a looming threat, even if rare or small. 

A spread configuration does the opposite of cluster. The spread option separates EC2 instances in their own data centers and or racks of servers. This allows for the most risk-resistant option, but of course has drawbacks. The latency can be quite high, thus the communication is limited. However, this separation of instances allow for a more trustworthy computation workflow. This option is great for mission-critical work.

A partition is a relatively new way of configuring a placement group: do both! A partition is a set of EC2 instances (max 7 at a time) in a rack of servers, or at least in the same availability zone. We can create multiple partitions in several availability zones and multiple in the same region. This allows a balance between risk and latency, but only if you want it to be a perfect balance. It can sway towards either more instances in a zone or more partitions. 

So, as a developer and not an IT support guy, how does this matter to me? Well, I am at least aware of the details of how an application's computation should be organized on VM's in AWS. At the very least, I can help in these matters should a position ask of me, but I can also use this knowledge for a startup software application I might have in the future. 
