# 武汉大学计算机学院本科生实验报告

### 计算机网络第二次课后作业



专业名称：软件工程

课程名称：计算机网络

指导老师：胡继承

学生学号：2020302111389

学生姓名：王楚

时间：2022年2月28日



### 1.

> Consider an application that transmits data at a steady rate (for example, the  sender generates an N-bit unit of data every k time units, where k is small  and fixed). Also, when such an application starts, it will continue running  for a relatively long period of time. Answer the following questions, briefly  justifying your answer: 
>
> a. Would a packet-switched network or a circuit-switched network be more  appropriate for this application? Why?
>
>  b. Suppose that a packet-switched network is used and the only traffic in this network comes from such applications as described above. Furthermore, assume that the sum of the application data rates is less than the  capacities of each and every link. Is some form of congestion control  needed? Why?

a. packet-switched network. packet-switched network will  make better use of Internet resources, and make data more secure.

b. no, there will not be congestion

### 2

> Metcalfe’s law states the value of a computer network is proportional to  the square of the number of connected users of the system. Let n denote the  number of users in a computer network. Assuming each user sends one message to each of the other users, how many messages will be sent? Does your  answer support Metcalfe’s law?

n*(n-1), yes

### 3

> Let a denote the rate of packets arriving at a link in packets/sec, and let µ denote the link’s transmission rate in packets/sec. Based on the formula for  the total delay (i.e., the queuing delay plus the transmission delay) derived  in the previous problem, derive a formula for the total delay in terms of a and µ.

queuing delay: a/µ 

transmission delay: 1/µ

total delay: a/µ+1/µ
