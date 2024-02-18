# VPC 

## Amazon VPC

- Enables you to provision a `logically isolated` section of the AWS Cloud where you can launch AWS resoruces in a virtual network that you define.
- Gives you `control over your virtual networking ` resources including:
    - selection of ip address range
    - creation of subnets
    - configuration of route tables and network gateways
- Enables you to `customize the network configuration` for you VPC
- enables you to use `multiple layer of security`
- 
![vpc1](https://github.com/anupmaharzn/intro-to-aws/assets/34486226/99300dbd-4be9-4e48-a342-7f74aede914f)


## Lab Task Overview

#img1

- Create VPC

#img2

- As we can see VPC is Created

#img3

- Creating Public and Private Subnet

#img4

- Here both of our subnet is ready

#img5

- Create Internet Gateway

#img6

- Now attach it to our vpc

#img7


- Creating `Route table` for `public subnet`

#imgofpubliroutetable8

- after creating public route table attach the `internet gateway in it`

#imgofattaching9

- now associate our `public subnet` also in `route table`.

#imgofassocatie10


- creating `Route table` for `private subnet`

#img11

- after create  route table associate the `private subnet` with it

#img12


- now creating `NAT Gateway` assocaiated with our `public subnet` because public subnet has the `internet gateway`.

#img13


- now update the route table of `private subnet` and add the `nat gateway` to private route table

#img14




- so in this lab we have 
    - created the `vpc`
    - configure the `subnets`(public & private)
    - created the `route table` (public & private)

    - also created internet gateway and attached to our VPC and in `public subnet route table`

    - create the` Nat gateway` associated with our public subnet and added the `private subnet route table` thru which it will access the internet.