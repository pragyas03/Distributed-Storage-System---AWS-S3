# Distributed-Storage-System
## AWS-S3
Amazon Web Services (AWS) has an object-level distributed storage solution known as **Simple Storage Service**. We can store any kind of file in this cloud service. It gives unlimited storage and a maximum of 5TB single file upload. Amazon S3 provides a safe and secured storage facility over the cloud with a number of features like partitioning, replication, fault tolerance and elastic scalability. It offers pay for the storage that is actually used and gives flexibility of who can access the data with Identity and Access Management policies, access control list, bucket policies and query string authentication. It also helps to securely upload and download data with SSL encrypted end points and provides multiple options of encrypting data at rest.

## How to

### Setup AWS
1. Go to the link [AWS Command Line Interface (amazon.com)](https://aws.amazon.com/cli/).
2. Download and run the 64-bit Windows installer, for Windows operating system or MacOS PKG installer, for Mac operating system. Download, unzip, and then run the Linux installer for the Linux operating system.
3. For Mac OS, open the .pkg file. “Install AWS Command Line Interface” opens, then click on Continue. Enter the password and installation is a success. Similar is the process for other operating systems.
4. Open terminal and run the command: aws --version. If the output of the command is of the form “aws-cli/2.1.33 Python/3.8.8 Darwin/20.3.0 exe/x86_64 prompt/off”, then this confirms that AWS CLI is successfully installed on the machine and its version is 2.

Now, to start with the configuration process, it is required to download the access keys from AWS Console. 

The steps to download the access keys are:
1. Sign in to AWS Console. From the drop down next to the username go to “My Security Credentials”.
2. Click on “Access keys (access key ID and secret access key)”. If there is already an Access ID created and its password is known, then that can be used, otherwise, it is required to create a new access key.
3. Click on “Create New Access Keys”. View the Access Key ID and Secret Access Key and save or download these. 
It is important to note here that the Secret Access Key is visible only once and once the dialog box is closed the secret access keys cannot be viewed again. It should be saved or downloaded at this point itself. If the access keys are lost, then they can be deactivated and deleted and news ones can be created.

The steps to configure AWS CLI are:
1. Open the terminal and run the command: aws configure
2. The following values need to be entered one by one:
   - “AWS Access Key ID [None]” (Access Key ID)
   - “AWS Secret Access Key [None]” (Secret Access Key)
   - “Default region name [None]” (Region code e.g: us-east-1)
   - “Default output format [None]” (Desired format of the output - json, yaml, yaml-stream, text format)
After this the configuration is done and AWS CLI commands can be run successfully. A .aws folder is created on the machine after the configuration is complete. This folder consists of two files, “config” and “credentials”. The CLI automatically logs in with the default credentials using these two files and performs the actions of the commands that are run. A user can also create his or her own profile too.

Follow [here](https://github.com/pragyas03/Distributed-Storage-System---AWS-S3/blob/main/AWS%20S3%20CLI%20Command.mds.md) for AWS S3 CLI Commands

