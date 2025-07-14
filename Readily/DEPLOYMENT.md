# Deployment Instructions for AWS EC2

1. **Build and Test Locally**
   - In your project root (`Readily`), run:
     ```sh
     docker-compose build
     docker-compose up
     ```
   - Visit http://localhost:5000 to verify the app works.

2. **Push Code to EC2**
   - Copy your project folder to your EC2 instance (e.g., using `scp` or `git`).

3. **Install Docker & Docker Compose on EC2**
   - SSH into your EC2 instance:
     ```sh
     ssh ec2-user@<your-ec2-public-ip>
     ```
   - Install Docker:
     ```sh
     sudo yum update -y
     sudo yum install docker -y
     sudo service docker start
     sudo usermod -a -G docker ec2-user
     ```
   - Install Docker Compose:
     ```sh
     sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
     sudo chmod +x /usr/local/bin/docker-compose
     ```
   - Log out and back in to refresh group membership.

4. **Run the App on EC2**
   - In your project directory on EC2:
     ```sh
     docker-compose up -d
     ```
   - The app will be running on port 5000.

5. **Open Port 5000 in AWS Security Group**
   - In the AWS Console, edit your EC2 instance's security group to allow inbound TCP traffic on port 5000.

6. **Access Your App**
   - Visit: `http://<your-ec2-public-ip>:5000`

---

**For production, consider using a reverse proxy (like Nginx) and HTTPS.**
