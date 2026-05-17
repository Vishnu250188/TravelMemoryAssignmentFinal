# TravelMemoryAssignmentFinal
The Travel Memory application has been developed using the MERN stack.This will provide hands-on experience in deploying full-stack applications, working with cloud platforms, and ensuring scalable architecture. this project including provisioning cloud resources, configuring servers, setting up load balancing, enabling HTTPS, and running applications in production using best practices.
# Configurtion:
Configure EC2 and Security Group then open the Git Bash & provide the Permission to .PEM file
now Install Required software by using below commands
sudo apt update && sudo apt upgrade -y, sudo apt install git -y
# Install nodejs & nginx
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install nodejs -y, sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
Verify node -v, npm -v
<img width="594" height="357" alt="6_nginx_Success" src="https://github.com/user-attachments/assets/3b287972-3521-45d3-ac2e-92367bedbad9" />
<img width="583" height="375" alt="4_nginx" src="https://github.com/user-attachments/assets/af852c71-e703-4427-a860-78ba1fb3ace1" />
# Clone Repository
git clone https://github.com/UnpredictablePrashant/TravelMemory.git<img width="1335" height="667" alt="cloneTravelMemoryPransant" src="https://github.com/user-attachments/assets/b33b2a83-b089-46c3-bde2-97f327bdc035" />
# MongoDB Atlas Configuration
Create Cluster & Database user then Read & write permission to database
now get MongoDB URL like : mongodb+srv://traveluser:travel123@cluster.mongodb.net/travelmemory<img width="898" height="642" alt="3" src="https://github.com/user-attachments/assets/51042347-e66c-44d5-94cc-46b064a24d4c" />

# frondend and backend Comminication made successfully
<img width="614" height="386" alt="2" src="https://github.com/user-attachments/assets/3117dc39-4787-4161-b95c-366dcedf32d0" />
<img width="1323" height="455" alt="instances2" src="https://github.com/user-attachments/assets/3ac49372-3037-4676-bbf0-bc5bd2e63fd5" />

# Backend Configuration by using below commands
cd backend, npm install, nano .env, 
PORT=3000
MONGO_URI=mongodb+srv://traveluser:travel123@cluster.mongodb.net/travelmemory
# Now save the file and start the backend by below command
node index.js

# Configuration frontend 
open ssh terminal and connect to EC2, go to folder then install npm install, nano src/urls.js now replace url

# Configure Nginx Reverse Proxy: 
sudo nano /etc/nginx/sites-available/travelmemory<img width="594" height="357" alt="6_nginx_Success" src="https://github.com/user-attachments/assets/317f1971-98ac-4fd7-8f38-3ac3a399e7ae" />
#To Enable config : sudo ln -s /etc/nginx/sites-available/travelmemory /etc/nginx/sites-enabled/
Remove default config : sudo rm /etc/nginx/sites-enabled/default   then test nginx :sudo nginx -t
Restart nginx :sudo systemctl restart nginx<img width="898" height="642" alt="3" src="https://github.com/user-attachments/assets/396f208f-cb3f-4f03-8182-6cb06eda4b00" />
<img width="615" height="681" alt="1_Trips" src="https://github.com/user-attachments/assets/29b76551-d25e-429f-90c6-730b08577858" />

# Application Load Balancer setup : <img width="1345" height="645" alt="LoadBalancer" src="https://github.com/user-attachments/assets/50fd288a-aacd-4361-b387-5e1c45ea2793" />
# Application Load Balancer is pointing to Target group containing both backendServer01 and backendServer02 Security group : allowed only two port 80 and 443 for ALB Testing the load balancer:


# I have Designed a deployment architecture diagram using draw.io to visualize the flow and connections.
<img width="1133" height="305" alt="Architecure" src="https://github.com/user-attachments/assets/0d10535e-cd49-43b1-aa59-d09ed25698d5" />

