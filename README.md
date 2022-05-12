# aws

static website host = S3 buckte

AUTOSCALING = create AMI (create image) -> launch configration -> Auto scalaing conf..

LOAD BALANCER = create 2 instance -> target group -> Load balancer 
# target group which instance you want attach load balancer(http for appliaction  and TCP for network

VPC CREATE = vpc create -> subnet -> internet getway(attach vpc) -> route table
# subnet =range of ip
# internet getway = it is connect you with internet
# route table = connect subnet with inetrnet getway mainly it is used for route
ROUTE EDIT ROUTES AND SUBNET ASSOCIATIONS

PAIRING VPC = create peering connection -> rote table
# edit route table first vpc1 and second vpc2 add in both subnetip range and peering connection

NAT GATEWAY = create vp -> create two subnet(public and private subnet)-> inetnet getway(attach vpc) -> route table(create public and private table )->
-> -> create netgateway
# natway gateway = it is help to used private instance used internet without public ip
# public route table = route add ineternet getway and subnet association add only public subnet 
# pivate route table = route add ip(0.0.0.0/0) NATGETWAY add subnet association add only private subnet(first create netgateway)
# netgateway = add pubic subnet and add ELASTIC IP
# ELASTIC IP = one ip give all private instace

RDS = create database -> go inside scecurity gp
# rds = it used to create data base
# security gp = inbound rule add rule ssh , both anywhere 
# connect rds with instance = login instance install first data base like mysql and mysql -h endpoint data base -u username -p database_name
( endpoint in you can see in rds down detail) this for linux

S3 BUCKET = create bucket -> upload data
# it is used for stored data
# Version Enable = recover your old data (meaning pervious version data)
version = go on click data -> version
#Crossregion Repliaction = It is used for create backup data(it create copy data on differnet region automatic)

AWS CLOUDFRONT = bucket create -> create cloufront
# it is used for fast client go on wbebsite(it reduced your time client to serverand it reduced latency) and its global service
#it create edge(virtual data store) location on your region(server - edge - client), 
# orgin= main server, edge=where virtual data store, regional edge location= long time edge data store here

ELASTIC BEANSTALK = create application -> upload and deploy ->
# you can go Elastic blanstalk click on change configration (if you want edit setting instance,load balanced, autoscaling, notification,Database etc then change configration )
# upload file only when file is zip
# It is used for deploying and scaling web appliation and load balancing , auto sclaing and health monitoring is automatically handle
create appliaction - upload version - launch Environment - Manage Environment (workflow Elatic beanstalk
crossregion repliaction = first create two bucket different region -> go main bucket click on -> Management -> replication rule
#Lifecycle Ploicy = automatically data go on less price storage
go bucket click on -> Management -> 

EFS = cretate ec2 instance -> create efs -> login ec2 instance ->run command(yum install -y amazon-efs-utils) -> go efs open attach(run command on instance)
#EFS(Elastic File system) it is used one storage on differnet ec2 instance in same region( it is ony use in linux not in window)
