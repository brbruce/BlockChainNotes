# AWS Marketplace: Ethereum Development and Training Suit by Techlatest.net

---------------------------------------------------------------------

<http://www.techlatest.net/products/ethereum_development_and_traning_suit/>

<http://www.techlatest.net/support/ethereum_developer_kit/>

<https://aws.amazon.com/marketplace/library?ref_=header_user_your_software>

Login: bbawsjunk1 (user)

Region: N. Virginia

EC2 - 1 * t2.large

Cost: ~ $0.257 / hr = $67/month

---------------------------------------------------------------------

## Configuration

Go to <https://aws.amazon.com/marketplace/library?ref_=header_user_your_software> and click "Launch More Software".

Click "Continue to Launch" button in upper right corner.

Use the following settings:
- Launch From Website
- t2.large
- default vpc
- default subnet settings
- Create new Security group settings with ssh and rdp access from My IP only.
- Create new Key Pair and save the private key in a secure file system.

Launch, and view the instance in the EC2 console.

In the EC2 console, to get instructions for SSH, click the Connect button at the top of the Instances page.  You need to configure Putty with the private key file location, the username of "ubuntu" (Per the usage instructions below), and the public DNS address.

NOTE: To use Putty, you need to convert the pem private key file to ppk format using PuttyGen.  Just load the pem file, and save as Putty key ppk extension.  Then use that one.

    In gitbash shell:
    ssh -i "techlatest_ethereum.pem" ubuntu@ec2-34-239-148-211.compute-1.amazonaws.com

    In putty:
    techlatest_ethereum.ppk

Next, log in and change the ubuntu user's password:

    sudo passwd ubuntu

Next, start Remote Desktop Connection in Windows menu and enter userid ubuntu and new password.  Use module type "sesman-Xvnc".

Now you will see a desktop environment.

---------------------------------------------------------------------

Follow below instructions to enable remote desktop login (RDP) after starting the instance: 

1. Login to the instance using SSH via key based authentication. Use "ubuntu" as userid (refer https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/putty.html for details on how to connect using putty/ssh) 

2. Once connected using ssh/putty, run below command to set the password for "ubuntu" user on the terminal sudo passwd ubuntu 

3. Once the password is set for ubuntu user, from your local windows machine, goto start menu. 

4. On the start menu, search and select "remote desktop connection" . 

5. In the "remote desktop connection" wizard, provide public IP of your instance and click connect. 

6. In the displayed window, provide "ubuntu" as userid and password set in step 2 above. 

7. Now you are connected to the desktop environment of Ethereum devkit where you can access out of box environment for Ethereum development. 

To learn more on how to use Ethereum development kit, please visit http://techlatest.net/support/ethereum


