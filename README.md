# 2-teir-app-demo
Example Application for 2 teir app



Test Connectivty to RDS from EC2 instance
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