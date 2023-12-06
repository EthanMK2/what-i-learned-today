# AWS Instance Storage Features

There are three main storage types in AWS, each of which have their use case and ways to work with EC2 instances and the services they might provide. 

The first is Elastic Block Store, or EBS, which is a network drive that stores the EC2 instance files and workload. On default, if the instance is terminated, the root EBS volume is deleted, and the data is lost. This can be disabled, and for any subsequent volumes added to an instance, the option to delete on terminate is set to disabled. EBS has many types that allow connecting to multiple instances and allow customization for input/output and storage needs. 

The second type is the Elastic File System, or EFS, which is a way to connect multiple instances together and share the same files for use cases such as websites, content management, and Wordpress. This allows us to share data quickly between instances, without having to copy and transfer EBSs. EFS can also allow preconfigured security groups and user scripts, allowing for an incredibly fast boot time for new instances. EFS allows for pay-per-use, and it scales to what you need, but it is usually three times more expensive than a gp2 EBS storage type. 

The third type is Instance Store, which is an actual physical drive connected to the EC2 instance server. This is incredibly fast and durable, yet it will be lost if the server goes down. This is a great option for big data operations without a fear of losing data due to backups on hand. 
  
