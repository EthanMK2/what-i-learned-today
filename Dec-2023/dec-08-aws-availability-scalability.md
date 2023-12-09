# AWS Load Balancers and Auto Scaling Groups

AWS has 3 main types of load balancers, Application load balancer, Network load balancer, and Gateway load balancer. The ALB is a load balancer that works for most applications like websites where it balances the load of web traffic evenly across EC2 instances. The ALB can even auto balance across availability zones, called cross-zone load balancing. This is enabled by default, and so the load balancer works nicely for maximizing availability of websites. The ALB has to have instances registered to it in order for it to work, same with the other load balancers (for EC2 instances). 

A Network load balancer is for maximum performance and speed, with the ability to handle millions of requests per second! This is fantastic for heavy workloads or busy applications with lots of traffic. The NLB has cross-zone load balancing off by default, so it must be enabled. NLBs are also great for having one IP to work with for itself. The NLB of course needs to have EC2 instances registered to it.

A Gateway load balancer is a relatively new LB that enables the ability to run requests through third-party security virtual appliances. This allows us to use other security services to monitor/filter requests in a way that AWS cannot. The Gateway load balancer also allows for special features like using the GENEVE protocol. 

So how does this all scale? Well, we use a Auto Scaling Group. This group has a template that we design in order to get the results we want. We can set EVERYTHING about an EC2 instance launch in this template, such as the type of instance, the size, the security groups, the AMI, and other things. This is what allows us to register the instances automatically to load balancers, enabling our app to remain behind a load balancer layer! The Auto Scaling Group has some more customization, but the big idea is that we can track activity and make adjustments to the template and settings. Primarily, we would want to make sure we are aware of how many instances we want, the minimum we need, and the maximum we can afford. 