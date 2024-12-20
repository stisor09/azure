# microsoft azure thing
the barnyard movie or flushed away, pick your poison

!!NOTE!!
From modules/vm/main.tf, lines 37-48, linux commands for the mySQL vm's must be used manually since my stupid ass cant get it to work automatically upon startup
!!NOTE!!
From modules/vm/main.tf, lines 74-118, change directories to match your own choices
!!NOTE!!

Download the terraform files.zip file

Preferably keep the majority of files inside this directory > C:\Users\YourNameHere\Documents\Terraform

The WEBSERVER_SCRIPTS folder should be in your downloads, but if you want them elsewhere, you must specify directories in the .tf file.

The contents are Terraform files, modules and variables that automatically sets up infrastructure in Azure:

A network

2 subnets

2 Load balancers, although 1 unused

1 Website VM w/ NIC w/ public IP

1 availability set for MySQL VMs

2 MySQL Database VMs w/ NIC w/ internal IP's

2 NSG's, one for each subnet

1 unsuccessful attempt at creating a functional NAT-gateway

The Webserver_scripts and its contents is necessary for the website VM to work.

Delete the existing NAT-gateway and its public IP, and create new pub IP's for the NIC's to SSH into the MySQL VMs to run the commands

If you paste the web-vm public IP into your browser, it should display database content 

You will get a 502 error if things are not setup properly, or MySQL errors if things are misconfigured in MySQL
