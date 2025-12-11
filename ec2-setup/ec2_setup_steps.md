 EC2 Setup Steps (Amazon Linux 2023)

## 1. Launch EC2 Instance
- Image: Amazon Linux 2023 AMI
- Type: t2.micro (Free Tier)
- Storage: 8GB
- Security group inbound rules:
  - HTTP (80)
  - HTTPS (443)
  - SSH (22)

## 2. Attach Two IAM Roles
Role 1: SSM Access → AmazonSSMManagedInstanceCore  
Role 2: CloudWatch Agent → CloudWatchAgentServerPolicy

## 3. Install Apache
sudo dnf install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd

## 4. Install PHP
sudo dnf install php php-mysqlnd php-fpm -y

## 5. Check Apache
Go to browser:
http://your-public-ip/
