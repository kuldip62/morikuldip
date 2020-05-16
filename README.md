# morikuldip.github.io
hello Friends,

my this project main aim is host website and run on docker.
https://kuldip62.github.io/morikuldip/
this is my site url.

i run all th project in ubuntu os with install docker after perfome this all.
this link helps install docker in your ubuntu machine.
https://docs.docker.com/engine/install/ubuntu/   --- for ubuntu
https://docs.docker.com/engine/install/fedora/   --- for fedora
https://docs.docker.com/engine/install/centos/   --- for CentOS
https://docs.docker.com/engine/install/debian/   --- for debion

make sure you install properlly.
perfome this command and host website.i give here some command to help a perfome this prectical.

NOTE : i have get error when i not use sudo command make sure sudo is reqared or not !

1) update & upgrade your all system.
sudo apt-get update && upgrade -y
---------------------------------------------------------
2) create nginx container.
sudo docker -d -P --name web nginx 
---------------------------------------------------------
3) check port of web 
sudo docker web port
Note: after perfome this you have see somethink like   ip:portnumber
looks loke 0.0.0.0:32770
pest in your local browser.you get welcome page of nginx.

---------------------------------------------------------
4) i make 1 directory for my website
mkdir mysite
Note: mysite is my directory name you can give anythink you want.

---------------------------------------------------------
5) i go to my directory.
cd mysite
---------------------------------------------------------
6) make website to host 
echor " I am Kuldip Hiralal Mori" > index.html
Note: after perfome all opration given by here you can change index.html by your perpose.

--------------------------------------------------------
7) run website 
docker run -d -P -v $HOME/mysite:/usr/share/nginx/html \ ( PRESS ENTER & perfome command given by below )
--name mysite nginx

--------------------------------------------------------
8) check ip address for website 
sudo docker port mysite
Note: after perfome 8 number command youa get some like 80/tcp -> 0.0.0.0:32769 (May be you get diffrent number)
copy this all ip 0.0.0.0:32769 and pest in local browser 

--------------------------------------------------------

Done ! you complete here ! after perfoem 8 you can change your index.html

--------------------------------------------------------
after shutdown you laptop or computer may be you face some problem then run this command.


9) run your website once agine after shutdown machine.
sudo docker start af471e744f51
Note: here "af471e744f51" pest your CONTAINER ID

--------------------------------------------------------
your querys are welcome.
