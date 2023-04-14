# Launching nginx via aws 
Launch instance as done before, and assign a name, then we explore the AMI and go through the catalogue, we selected ubuntu 20.4
<img width="1232" alt="Screenshot 2023-04-14 at 14 13 17" src="https://user-images.githubusercontent.com/129948378/232090127-19474ed7-4c09-44a7-b6d7-63e908e3739c.png">
After sorting out our AMIs, we change our security group, you can use a new one, but we decide to use an existing one as seen below.
<img width="1232" alt="Screenshot 2023-04-14 at 14 13 26" src="https://user-images.githubusercontent.com/129948378/232091480-5f2136f4-fe00-45c5-ab1e-1f4e4bb04359.png">
Under the advanced tab, we go under user data and enter our scripting commands as seen below.
#!/bin/bash 
sudo apt update -y 
sudo apt upgrade -y 
sudo apt install nginx -y 
sudo systemctl restart nginx 
sudo systemctl enable nginx
<img width="1232" alt="Screenshot 2023-04-14 at 14 16 24" src="https://user-images.githubusercontent.com/129948378/232092298-838faabb-c82b-430f-b05f-0ce3b89e9d1b.png">
Press on the public adress in your instances 
<img width="1277" alt="Screenshot 2023-04-14 at 18 11 49" src="https://user-images.githubusercontent.com/129948378/232112328-b6eeafff-93f7-48c1-b542-933fdd07cc52.png">

We then navigate to our instance details and find our public ip address, which we will then paste into our browser to see if nginx has in fact been installed.
<img width="891" alt="Screenshot 2023-04-14 at 16 49 55" src="https://user-images.githubusercontent.com/129948378/232092804-03bfed9d-04b6-4037-be18-9c9df7cd76c9.png">
