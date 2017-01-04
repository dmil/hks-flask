# hks-flask

#### Deploy
- Go to https://console.aws.amazon.com/console/home.
- Click on EC2 or go to https://console.aws.amazon.com/ec2/v2/home?region=us-east-1.
- Click Launch Instance.
- Choose this AMI (Amazon Machine Image):
  - Ubuntu Server 16.04 LTS (HVM), SSD Volume Type - ami-e13739f6
- Choose instance type: t2.micro.
- Click "Review and Launch".
- Click "Launch".
- Choose "Create New Key Pair".
  - Name it "hks"
  - Download Key Pair
  - Put it in a safe place!!
- Click "Launch Instance".
- Click View Instances.
- Name the instance "hks-flask-box".
- Click on the checkbox next to the instance and click "Connect".
- Run this:
  ```
  mkdir -p ~/Desktop/Credentials
  mv ~/Downloads/hks.pem ~/Desktop/Credentials
  chmod 600 ~/Desktop/Credentials/hks.pem
  cat ~/.ssh/id_rsa.pub | ssh -i ~/Desktop/Credentials/hks.pem ubuntu@52.90.42.210 "cat - >> ~/.ssh/authorized_keys"
  ssh ubuntu@52.90.42.210
  ```
