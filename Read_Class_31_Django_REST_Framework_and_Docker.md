# Django REST Framework & Docker

## Docker

#### What is Docker?

Docker is an open source platform for building, deploying, and managing containerized applications. 


#### How Docker works


Docker packages, provisions and runs containers. Container technology is available through the operating system: A container packages the application service or function 
with all of the libraries, configuration files, dependencies and other necessary parts and parameters to operate. Each container shares the services of one underlying 
operating system. Docker images contain all the dependencies needed to execute code inside a container, so containers that move between Docker environments with the same 
OS work with no changes.


#### Linux Containers
Docker is really just Linux containers which are a type of virtualization.

Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm. How could multiple programmers use the same single machine? The answer was virtualization and specifically virtual machines which are complete copies of a computer system from the operating system on up.


#### What’s the downside to a virtual machine? 

Size and speed. A typical guest operating system can easily take up 700MB of size. So if one physical server supports three virtual machines, that’s at least 2.1GB of 
disk space taken up along with separate needs for CPU and memory resources.




#### Containers vs Virtual Environments

Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.

But…virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper version. So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment.

Also we can’t run a production database or other services within virtual environments so compared to Docker containers they are far more limited.






