# aws-autoscaling-alb-lab
Modern cloud-based apps need to be able to scale up and be available all the time. Cloud-native load balancing lets us deploy faster, automate more, and be more flexible, which is ideal for workloads that change all the time. Moreover, we don't need to plan for the capacity or manage hardware and power resources.
 I did a hands-on lab that focused on setting up an Auto Scaling Group (ASG) behind an Application Load Balancer (ALB) to learn more about how AWS handles dynamic traffic and manages resources automatically.
Auto Scaling Group + Application Load Balancer for Building a Scalable Web Architecture. Scalability is no longer just a "good to have." It's a must-have for any modern cloud design. I recently finished a hands-on AWS lab where I set up an Auto Scaling Group (ASG) underneath an Application Load Balancer (ALB) to handle changing traffic in a smart way. This lab provided an way to learn how AWS services work together to provide high availability, fault tolerance, and flexibility. 

AWS-Autoscaling with Application The architecture included: 
• A custom VPC with several public subnets in different Availability Zones
• An Internet Gateway and route tables that were set up correctly 
• A secure Security Group that allowed controlled HTTP/HTTPS/SSH access 
• A reusable Launch Template (Amazon Linux + EC2 configuration) 
• An Application Load Balancer that balances incoming traffic.
• An Auto Scaling Group that automatically changes EC2 instances based on demand. 

This lab has made sure that traffic going to the ALB was spread out evenly among several EC2 instances instead of just one.️ How scaling and load balancing worked. The desired capacity was set to two instances. 
• The minimum capacity was 1 and the maximum capacity was 5.
• When demand went up, additional EC2 instances were immediately launched. 
• All instances were registered with the ALB target group. 
• The ALB DNS was used to test requests, and varied answers showed that load balancing was working.
 This got rid of the requirement for manual provisioning and showed how AWS can easily handle scale. 

During testing, requests that went through the ALB got answers from multiple servers. 
• The load balancing behaviour performed just like it was supposed to. 
• Auto Scaling made new instances on its own when it needed to. 
• ALB health checks that match how the application works
