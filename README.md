### aws_project_LAMP_stack

![download](https://user-images.githubusercontent.com/85028974/230502329-80f351e8-6fd4-44e8-8293-f431190f9f41.png)


# LAMP stack - is a bundle of four different software technologies that developers use to build websites and web applications. 
## LAMP is an acronym for the operating system : [Linux](https://www.linux.org/), the web server: [Apache](https://www.apache.org/), the database server : [MySQL](https://dev.mysql.com/doc/mysql-port-reference/en/mysql-ports-reference-tables.html) and the programming language : [PHP](https://www.php.net/).

### * Task :
- [ ] In us-east-1 region, create VPC - 2 public, 2 private subnets, choose us-east-1a and us-east-1b AZs

- [ ] Launch two amazon linux instances in each public subnets and one RDS (latest MySQL 5.7) in a private subnets. (*Note: 1 ec2 per public subnet!*)

- [ ] Restrict RDS access to only public subnets ( on RDS security group open port 3306 for public-1a and open port 3306 for public-1b )

- [ ] Configure LAMP/Wordpress on EC2 instances and connect it to MySQL database. Refer to Setup Wordpress/LAMP stack on AWS  

Create ALB and put EC2 instances behind it

On ALB, open port 80/443 to the world. On EC2s, limit port 80 to ALB

Install SSL on ALB

Create Route 53 CNAME record and from your browser check if you can visit your page.

Once LAMP/WordPress is built, create an AMI from one of your EC2 instances

Setup Autoscaling using the AMI. Minimum, desired = 1, maximum = 2

Test your autoscaling group

Stream apache error and access logs to cloudwatch from both EC2 instances
