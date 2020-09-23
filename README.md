# AWS-VPC
AWS VPC 

Go to the VPC console and select a region in the upper right corner from the region drop down.	Click on “Your VPCs” in the left menu.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/VPC1.png)

Click “Create VPC” in the upper left.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/create_vpc.png)

Create a Name tag. Choose an Ipv4 CIDR block.	Leave the rest as the default.	Click on Create.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/tag.png)

Now a new VPC is created.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/avail.png)

Click on “Subnets” on the left menu. Then click in “Create subnet” in the top left.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/subs.png)

Create a name tag. Choose the VPC you want. Availability Zone choose a selection in the N. Virginia region. Put 10.0.0.0/28 in the Ipv4 CIDR block. Click create.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/priv2.png)

Create any extra availability zones with different names and IPv4 CIDR blocks.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/sub3.png)

To create a route table,	click route tables on the left menu. Then click create route table on the top.	Add a name to the routing table you created.	Click create.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/route1.png)

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/route2.png)

Click create route table again to create a private route table.	Name it accordingly.	Choose the correct VPC. Click create.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/create4.png)

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/create5.png)

To create the association for private and public subnets, Select route tables on the left menu. Choose the Private routing table.	Click on subnet associations tab below.	Click edit.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/asso.png)

Choose the private subnets.	Click Save.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/save1.png)

Do the same for the public subnets. The route table page will display how many subnets are associated when finished.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/pub1.png)

To create an internet gateway and attach it to the VPC, Click on Internet Gateways in the left menu.	Click Create Internet Gateway near the top. Enter a name.	Click create.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/gate.png)

Select the gateway and then click the actions dropdown at the top.	Select Attach to VPC.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/attach.png)

Select the correct VPC.	Click Attach.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/attach3.png)

To add public destination routes, Select Route Table in the left menu. Select the appropriate route table. Click the Routes tab below.	Click Edit routes.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/edit.png)

Click add route.	Add 0.0.0.0/0 to the destination.	For the target click on internet gateway then select the correct one. Click Save.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/route4.png)

To create a NAT gateway and autogenerate an elastic IP,	Click NAT Gateways on the left menu. Click Create NAT Gateway near the top.	Select the correct subnet.	Click on Allocate Elastic IP address.	Click Create a NAT Gateway.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/createN.png)

Click Edit route tables.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/created.png)

Select the correct routing table.	Click the Routes tab below.	Click edit.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/twosub.png)

Click add route.	Add 0.0.0.0/0 as the destination.	Select NAT Gateway then choose the one that was created for routing table you’re working on.	Click Save Routes.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/destin.png)

To assign public IPs to instances launched in public subnets, Click Subnets on the left menu. Choose a public subnet. Click on the Actions dropdown near the top. Choose modify auto-assign IP settings.
 
![alt text](https://github.com/doyle199/AWS-VPC/blob/master/assign3.png)

Leave unchecked and click Save.	Repeat for any other needed subnets.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/mod.png)

Click Your VPCs on the left menu.	Select the correct VPC.	Click on the Actions dropdown near the top.	Click on Edit DNS Hostnames.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/edit2.png)

Click the enable box.	Click Save.

![alt text](https://github.com/doyle199/AWS-VPC/blob/master/id.png)
