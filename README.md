hello Friends,
my this project's main aim is to host a website and run on docker. 
https://kuldip62.github.io/morikuldip/ this is my site URL.

I run all the projects in ubuntu os with install docker after performing this all.
This link helps install docker in your ubuntu machine.
https://docs.docker.com/engine/install/ubuntu/ --- for ubuntu 
https://docs.docker.com/engine/install/fedora/ --- for fedora 
https://docs.docker.com/engine/install/centos/ --- for CentOS 
https://docs.docker.com/engine/install/debian/ --- for Debian

Make sure you install properly. perform this command and host website. i give here some command to help a perform this practice.

NOTE: I have got an error when I do not use sudo command to make sure sudo is required or not!

update & upgrade your all system. 
sudo apt-get update && upgrade -y
-----------------------------------------------------------------------------------------------------------------------------
create an Nginx container. 
sudo docker -d -P --name web nginx
-----------------------------------------------------------------------------------------------------------------------------
check port of web.
sudo docker web port 
Note: after performing this you have to see something like IP: port number looks like 0.0.0.0:32770 pest in your local browser. you get a welcome page of nginx.
-----------------------------------------------------------------------------------------------------------------------------
I make 1 directory for my website
mkdir mysite 
Note: my site is my directory name you can give anything you want.
-----------------------------------------------------------------------------------------------------------------------------
I go to my directory. 
cd mysite
-----------------------------------------------------------------------------------------------------------------------------
make a website to host 
echo " I am Kuldip Hiralal Mori" > index.html 
Note: after performing all operation given by here you can change index.html by your purpose.
-----------------------------------------------------------------------------------------------------------------------------
run website
sudo docker run -d -P -v $HOME/mysite:/usr/share/nginx/html \ 
( PRESS ENTER & perform command given by below ) --name mysite nginx
check IP address for website sudo docker port mysite 
Note: after perform 8 number command you get some like 80/tcp -> 0.0.0.0:32769 (Maybe you get different number) copy this all IP 0.0.0.0:32769 and pest in local browser
-----------------------------------------------------------------------------------------------------------------------------
Done ! you complete here! after performing 8 you can change your index.html
-----------------------------------------------------------------------------------------------------------------------------
after shutting down your laptop or computer maybe you face some problem then run this command
run your website once again after shutdown machine. 
sudo docker start af471e744f51 
Note: here "af471e744f51" pest your CONTAINER ID
-----------------------------------------------------------------------------------------------------------------------------
Your querys are welcome.






