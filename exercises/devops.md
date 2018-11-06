# Devops

The following questions are relevant if you have experience in devops or systems administration – they're in no way
required for our software engineering positions. Feel free to answer in French if needed.


## Standalone Django App Deployment

Describe a minimal setup to deploy a very simple, standalone Django application in production. We want to minimize
hosting costs and maintenance cost. Deployment will be independent from our existing infrastructure as this will be an
MVP test.


## Code Deployment

What are the main challenges to overcome to perform clean and reliable production updates of the code of a Django+MySQL
application on a Linux+Apache+mod_wsgi stack? What would be the first component you'd add or replace in this stack?


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
