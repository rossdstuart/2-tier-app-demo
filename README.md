# 2-tier-app-demo
Example Application for 2 tier app



Test Connectivity to RDS from EC2 instance
#install netcat if not already installed
sudo yum -y install nc
nc -zv <hostname> <port>

Valid output:
Ncat: Version 7.50 ( https://nmap.org/ncat )
Ncat: Connected to 10.201.2.117:3306.
Ncat: 0 bytes sent, 0 bytes received in 0.07 seconds.

Failed Connection:
Ncat: Connection timed out.


nslookup to test for public or private ELBs

## Deploy Code
```
aws cloudformation deploy --template-file 2-tier-app-stack.yaml \
    --stack-name StackName \
    --parameter-overrides VpcID="vpc-000000000" \
      PublicSubnet1="subnet-00000000" \
      PublicSubnet2="subnet-00000000" \
      PrivateSubnet1="subnet-00000000" \
      PrivateSubnet2="subnet-00000000" \
      SshKey="ssh-key-name" \
      DBSubnetGroup="Name of Private Subnet Group" \
      DBPassword="xxxxxx"
```
