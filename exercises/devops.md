# Devops

The following questions are relevant if you have experience in devops or systems administration – they're in no way
required for our software engineering positions. Feel free to answer in French if needed.


## Standalone Django App Deployment

Describe a minimal setup to deploy a very simple, standalone Django application in production. We want to minimize
hosting costs and maintenance cost. Deployment will be independent from our existing infrastructure as this will be an
MVP test.

to start : 
install python , install pip , install django with pip, 
create project command :  $ django-admin startproject myApplication .

Run the Server  : 
$ python manage.py runserver ,  we will have a specific port  , for exemple : "Starting development server at http://127.0.0.1:8000/" so the port is 8000 (check if you don't have another server runing in this port)

now we can see our application 


in order to publish a django web application, we have several choices:

1- rent a small server at a distance (low cost)
2- open the server locally (which will be accessible via the internal network of the company) with adress ip local of the machine (who has django server) -> contact this machine with another machine (of the same netwoork) https://adressLocalMachineDjango:portUsed

3- if you still want to publish the application in internet (for free), we can use the port redirections in the server of the company (NAT: Network address translation), with this solution the application django will be accessible even from the outside network  : (https: // ipPublicOfServer: portUsed) -> I often use this method with my internet box

## Code Deployment

What are the main challenges to overcome to perform clean and reliable production updates of the code of a Django+MySQL
application on a Linux+Apache+mod_wsgi stack? What would be the first component you'd add or replace in this stack?

we can use pip for updates pythons package or to install a new package 
don't upgrade all package of the application django, if we upgrade all we can fall in problems of libraries adaptation

in the best case, we use a file json or gives the libraries and the dependencies which one uses in the application but also the versions not to exceed (even if there are updates available), then one has a dependency manager (pip) that does the rest of the work

we can remove apache, since Django already offers a web server

## Security

What are the main security measures that would seem important for a startup our size and in our industry to take?

here are some security methods :
    for the code : 
        use good frameworks (especially in web), there are frameworks that provide security by using good template engine (faills XSS, SQL injection ...)
        use new technologies to facilitate work and be faster (use of libraries and ORM to manage databases for example)

    for the infrastructure:
        work with Git (keep the code clean)
        use backups, firewalls to manage network flow (blocking and authorization)
        encrypting data by installing software that touches the lower layers of the network (software installation and VPN ...)
        manage the server users well

there are other ways of security of course
