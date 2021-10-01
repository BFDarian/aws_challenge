# Trio-task

## MVP

- I first created a custom VPC 
- I then mad an internet gateway so inbound and outbound traffic can pass through
- I then made a public and two private subnets.
- I added a NAT Gateway to the public subnet
- I then made a route table for the public subnet and added the igw (internet gateway) as a route.
- I made the route table for one of the private subnets and added the NAT Gateway as a route.
- Next, I created an EC2 in the public subnet where the web app would be installed. I also set up the security group for the EC2.
- Finally, I created the RDS database in the private subnet with teh same security group as the EC2 so they could communicate with each other so the databse could be accessed and manipulated.

## Future Improvements

- Due to time constraints I was unable to get the app working in docker due to an unresolved issue. So with a bit more time I hope to solve the issue.

- I would like to add IAM policies to restrict who could access the web server and what people could do to the app.

- Use of a YAML file to speed up the set up of aws resources.

- Use of CloudTrail to monitor the event history of the VPC and use of CloudWatch to provide alerts when a change has been made that has negatively affected the app or if the app is having issues such as if the CPU utilisation is high and could cause the web app to crash.
