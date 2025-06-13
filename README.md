## 📁 Project Structure
aws-cli-s3-setup/
- screenshots/              # All AWS CLI operation screenshots
  - aws-version.png         # aws --version output
  - aws-configure.png       # aws configure setup
  - bucket-create.png       # Bucket creation proof
  - ...                     # Other screenshots
- README.md                 # This documentation

# 🚀 AWS CLI & S3 Bucket Guide

![AWS CLI Demo](https://img.icons8.com/color/96/000000/amazon-web-services.png)  
*A step-by-step guide to mastering AWS CLI for S3 operations*

## 🔧 Setup AWS CLI

### 1. Install AWS CLI
```bash
# For Windows (download .msi):
https://aws.amazon.com/cli/

# For Mac/Linux:
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

### 2. Verify Installation
```bash
aws --version
```
![Version Check](https://github.com/Sabin-Rana/aws-cli-s3-setup/blob/main/Screenshots/AWS%20CLI%20Version.PNG)

## 🔐 Configure AWS

### 3. Set Up Credentials
```bash
aws configure
```
Enter:
- Your AWS Access Key ID
- Your AWS Secret Access Key
- Default region (e.g. `us-east-1`)
- Default output format (`json`)

![AWS Configuration](https://github.com/Sabin-Rana/aws-cli-s3-setup/blob/main/Screenshots/aws-configure.PNG)

## 📦 S3 Bucket Operations

### 4. Create Bucket
```bash
aws s3 mb s3://epicreads-aws-cli-bucket
```
![Bucket Created](https://github.com/Sabin-Rana/aws-cli-s3-setup/blob/main/Screenshots/bucket-create.PNG)

### 5. Upload File
```bash
aws s3 cp "C:\Users\Acer\Pictures\Wallpaper" s3://epicreads-aws-cli-bucket/wallpapers/ --recursive
```
![File Uploaded](https://github.com/Sabin-Rana/aws-cli-s3-setup/blob/main/Screenshots/file-upload.PNG)

### 6. List Files
To confirm that the files have been successfully uploaded, you can view them in the AWS Management Console. Below is a screenshot showing the uploaded files in the S3 bucket.
![File Listing](https://github.com/Sabin-Rana/aws-cli-s3-setup/blob/main/Screenshots/list-files.png)

### 7. Clean Up
1. To delete the S3 bucket and its contents, follow these steps:
First, remove all objects in the bucket with the following command:
```bash
aws s3 rm s3://epicreads-aws-cli-bucket --recursive
```
2. Remove the bucket itself using the following command:
```bash
aws s3 rm s3://epicreads-aws-cli-bucket --recursive=
```
3. Verify the bucket deletion by listing all your buckets. If the bucket is successfully deleted, you will see no result:
```bash
aws s3 ls

```
The following screenshot shows the successful deletion of the epicreads-aws-cli-bucket in the AWS Console:
![Bucket Deleted](https://github.com/Sabin-Rana/aws-cli-s3-setup/blob/main/Screenshots/bucket-delete.PNG)

## 🎉 Congratulations!
You've successfully:
- Installed AWS CLI
- Configured credentials
- Created/managed an S3 bucket
- Uploaded/deleted files

---

💡 **Pro Tip**: Add these badges to your README by pasting this at the top:
```markdown
[![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?logo=amazon-aws&logoColor=white)](https://aws.amazon.com)
[![CLI](https://img.shields.io/badge/CLI-Expert-green)](https://aws.amazon.com/cli/)
```
