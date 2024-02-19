# EC2 with Elastic Load Balancer (ELB)

## Elastic Load Balancer

- Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple targets and virtual appliances in one or more availability zone (AZ)

    - `Application Load Balancer`
        - ALB operates at the application layer(layer 7) of the OSI model and is best sutied for ditributing HTTP/HTTPS, gRPC,Websockets.
   ![loadbalancer1](https://github.com/anupmaharzn/intro-to-aws/assets/34486226/b837b05b-cbdc-43d6-b5d9-1a924af605b9)
    - `Gateway Load Balancer`
        - GLB is designed fro routing traffic to third-party secrity appliances like firewalls and intrusion detection systems.
    - `Network Load Balancer`
        - NLB operates at the transport layer (layer 4) and is designed for handling TCP,UDP and TLS traffic.



## Application Load Balancer for EC2 instance

- To create a load balancer using the AWS Management Console, complete the following tasks.

 - Step 1: Configure a target group
 - Step 2: Register targets
 - Step 3: Configure a load balancer and a listener
 - Step 4: Test the load balancer

![loadbalancer2](https://github.com/anupmaharzn/intro-to-aws/assets/34486226/1e0b9e05-d0e7-4f01-9279-666f863894f3)


**Link for more detail**: - `https://docs.aws.amazon.com/elasticloadbalancing/latest/application/create-application-load-balancer.html`

- `Target Group`
    - Target groupos route request to individual registered targets, such as EC2 instanaces,using the protocol and port numbers that you specify.
    - Each target group is used to route requests to one or more registered targets.
- **`NOTE`**
    - ** when we create application load balancer we need to have default + another new security group for incomming traffice from http port 80 (allow http request) or any other internet access **


## EC2 with ALB

### Overview 

![applicationloadbalacer-practise](https://github.com/anupmaharzn/intro-to-aws/assets/34486226/d772154f-ca12-4582-9fdd-0ad766bd633f)


- first let's create `VPC`

#img1

- as we can see our `VPC` has been created.

#img2

- let's create `internet gateway` and attach it to our `VPC`

#img3

- now attach to `VPC`

#img4

- now let's create `2 public subnets`

#img5


- Create `Route Table` for our vpc so that each subnet in a vpc can associated with a route table,which contorls the traffic between subnets and defines the routes for traffic leaving the VPC.

- In an Amazon VPC, `each subnet` must be associated with `one and only one` `route table` at any given time.


#img6


- associate the subnets with this route table

#img7

- now adding `internet gateway` to the route table

#img8

- Let's create `two EC2 instance` ,assocaite `one instance for each subnet`

#img9

    - `similar for another instnace for different subnet`

- `now we have finished provisioning our EC2 instances`


- let create our `target group` and add our targets which is nothing but our ec2 insances

#img10-1

#img10-2

#img10-3

#img10-4

#img10-5


- Now create `Application Load Balancer`

    - in ALB we have to configure the security group to `allow inbound traffic` from `http protocal port 80` for our `ALB`

    #img11

- now `Create ALB`

#img12-1

#img12-2

#img12-3

#img12-4



**we have completed the EC2 with ALB**

- now we can see it's working

#img13

