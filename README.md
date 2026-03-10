# multi-cloud-architecture
Task 3

COMPANY: CLOUDTECH IT SOLUTIONS

NAME: NEHA SATPUTE

INTERN ID: CTIS5002

DOMAIN: CLOUD COMPUTING

DURATION: 4 WEEKS

MENTOR: NEELA SANTOSH

Multi-Cloud Architecture Implementation

In this task, I designed and implemented a simple multi-cloud architecture where services are distributed across two different cloud platforms. The purpose of this task was to understand how multiple cloud providers can work together in a single architecture. Multi-cloud architecture is commonly used in modern applications to improve reliability, scalability, and flexibility while avoiding dependency on a single cloud provider.

For this implementation, I used Amazon Web Services (AWS) and Cloudflare. AWS was used to host the application server, while Cloudflare was used for DNS management and request routing. By combining these two platforms, I was able to demonstrate how different cloud services can integrate and work together efficiently.

The first step in the implementation was creating and configuring a virtual server on AWS using the EC2 service. I launched an Ubuntu based EC2 instance and configured the necessary security group settings to allow SSH and HTTP traffic. After the instance was successfully launched, I connected to the server using SSH and updated the system packages to ensure that the environment was properly prepared for deployment.

Next, I installed the Apache web server on the EC2 instance. Apache allows the server to host and deliver web content to users through a web browser. After installing Apache, I started the service and enabled it to run automatically whenever the server starts. I then created a simple HTML webpage and placed it in the Apache web server directory. This webpage was created to demonstrate that the server was working correctly and that users could access the hosted application through the internet.
Once the AWS server was configured and the website was running successfully, the next step was to integrate Cloudflare. I created a Cloudflare account and added my domain to the Cloudflare dashboard. After adding the domain, I configured a DNS record that pointed the domain name to the public IP address of my AWS EC2 instance. This configuration allows user requests to first pass through Cloudflare before reaching the AWS server.

Cloudflare acts as an intermediary layer between users and the server. It provides DNS management, improved performance through caching, and additional security features such as protection from malicious traffic. Because the application server is hosted on AWS and the DNS and request routing are handled by Cloudflare, the architecture uses services from two different cloud providers, making it a multi-cloud setup.

Finally, I tested the implementation by accessing the website through the configured domain. The request was routed through Cloudflare and successfully delivered to the AWS EC2 server hosting the web application. This confirmed that the multi-cloud architecture was functioning correctly.

Through this task, I learned how different cloud platforms can be integrated to build a more flexible and reliable infrastructure. This experience also helped me understand the practical benefits of multi-cloud architecture in real-world cloud computing environments.

#commands
sudo apt update
sudo apt install apache2 -y
sudo systemctl start apache2
sudo systemctl enable apache2
