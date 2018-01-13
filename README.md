# Jenkin
How to work with Jenkins

Installation of Jenkins in AWS ?
Go through the beloe steps:
1. open AWS Console in browser
2. Go to EC2 service
3. Launch t2 Instance using AWS AMI
4. SSH into ec2 instance
  ``` ssh -i "mann_cloud_aws.pem" ec2-user@ec2-34-209-90-176.us-west-2.compute.amazonaws.com ```
5. Set the repo get the files:
  ``` sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat/jenkins.repo
  sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io.key ```
  
6. install the jenkins
  ``` sudo yum install jenkins ```
  
7. start the jenkin service :
    ``` service jenkins start```
8. Service start jenkins if it is asking for java 8 install the java 8 using below commands
    ``` cd /opt/
      wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-  securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u151-b12/e758a0de34e24606bca991d704f6dcbf/jdk-8u151-linux-x64.tar.gz"
      tar xzf jdk-8u151-linux-x64.tar.gz 
      cd /opt/jdk1.8.0_151/ 
      alternatives --install /usr/bin/java java /opt/jdk1.8.0_151/bin/java 2
      alternatives --config java
      alternatives --install /usr/bin/jar jar /opt/jdk1.8.0_151/bin/jar 2
      alternatives --install /usr/bin/javac javac /opt/jdk1.8.0_151/bin/javac 2
      alternatives --set jar /opt/jdk1.8.0_151/bin/jar
      alternatives --set javac /opt/jdk1.8.0_151/bin/javac ```

8. Start the Jenkins service now
9. Open the browser and open your public dns with port 8080
10. Install the recommended or custom plugins
