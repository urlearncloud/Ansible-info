HOW TO SET-UP ANSIBLE CONTROLL AND MANAGED NODE
=================================================



### 1. Create 1 EC2 instance & Declare as controll node(master)
-----------------------------------------------------------------

ami -> ubuntu-22
instance types -> t2.micro
key pair -> mykey.pem
vpc -> default vpc
az -> 1a
sg -> ubuntu-SG (ssh,http,https,all traffic = ANYWHERE)

### 2. Connect EC2 instance and install ansible on master
------------------------------------------------------------------

go to your terminal
cd downloads
ls
ssh -i "mykey.pem" ubuntu@ec2-3-6-89-52.ap-south-1.compute.amazonaws.com
sudo apt-add-repository ppa:ansible/ansible
sudo apt update
sudo apt install ansible -y
ansible --version
