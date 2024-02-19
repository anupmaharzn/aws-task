# EC2 with Auto Scaling Group


## AWS EC2 Auto Scaling
    
- `Auto Scaling Groups`

- Amazon EC2 auto scaling helps you maintain application availability and allows you to `dynamically adjust `the `capacity` of your Amazon EC2 instances based on the demand for your applications.

- commonly used for following secnarios:
    - maintaining application availability
    - cost optimization
    - fault tolerance
    - elasticity: scale seamlessly 

![autoscaling1](https://github.com/anupmaharzn/intro-to-aws/assets/34486226/b7bbf81d-fcb4-4d23-a378-4be7ca3dc3de)


- **For More Detail**
    - `https://docs.aws.amazon.com/autoscaling/ec2/userguide/get-started-with-ec2-auto-scaling.html`


- `NOTE`
    - Instances of EC2 are typically created and managed using `Auto Scaling Policies`
    - The Purpose of Amazon EC2 auto scaling is to autmatically adjust the number of instances in an `auto scaling group `based on `changes in demand `or other specified condition.
- `While create the instance from autoscaling group we need **Lauch Template**`
- `Amazon EC2 Launch Templates` provide a way to specify the configuration of an EC2 instance in a resuable format.
    - A lauch template includes settings such as the
        - `AMI`
        - `instance type`
        - `key pair`
        - `security groups`
        - `other launch configuration parameters`

- `we just have to create one lauch template and auto scaling will automatically scale that instance into multiple instance`

## Lab

### overview architecture

![autoscaling2-practise](https://github.com/anupmaharzn/intro-to-aws/assets/34486226/a4315695-aa5f-4456-b7db-115ce5b5b22c)


**Let's Start**

- Lets first Create our `VPC`
    - as we can see our `test-asg-vp` VPC `is created`

    #img1

- Now let's create our `internet gateway`
    - as we can see our `test-asg-igw` internet gateway is created.

    #img2

    - now attach it to vpc.

    #img3

- `note in overview we have mentioned only one subnet` but we are creating two subnets

#img4

#img5

- now create `route table` add `internet gateway` in route and also associate the subnets that we created.
- added `igw`
#img6
- associated `subnets`
#img7

- now lets create `target group`,responsible for pointing to `EC2 instances`

#img8

- as we can see, we are just creating blank `tg`.
#img9


- now create `Application Load Balancer`

    - we also have to create security group from inbound http traffic
    #img10

- now,create `ALB`
#img11

- after that, it's time to create `Auto Scaling Group`

#img12

- lets create `Lauch template`

#img13

- now assign this lauch template and create auto scaling group

#img14

#img15

#img16

- now click on create auto scaling group.

#img17


- **once you create auto scaling group it automatically start creating EC2 instances.**