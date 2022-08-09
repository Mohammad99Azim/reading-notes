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




## Django REST Framework

Django REST framework is a powerful and flexible toolkit for building Web APIs.

Django REST framework (DRF) is a open source, mature and well supported Python/Django library that aims at building sophisticated web APIs. It is flexible and fully-featured toolkit with modular and customizable architecture that makes possible development of both simple, turn-key API endpoints and complicated REST constructs.
The only REST framework’s dependencies are Python (2.6.5+) and Django (1.30+). All other packages are optional, e.g. for filtering and OAuth support, or Markdown, PyYAML, defusedxml for Markdown, YAML, XML content types support.



#### why i need it?

Django REST framework contains wide set of out of the box features, but the core view class is very simple and framework in general is easy to use. The main idea behind the DRF is to clearly divide a model, the generalized wire representation (e.g. JSON, XML, etc.), and set of generic Class-Based-Views that can be customized to satisfy the specific API endpoint using Serializer that describes the mapping between them.



#### differences between DRF and other frameworks

One of the main differences between DRF and other frameworks is that it allows developer to define URL structure and not rely on an auto-generated one, while others automate much of the conversion from Django models to REST endpoints, thus are less flexible. Moreover, Django REST Framework includes built-in API browser for testing out newly developed API.



#### Main advantages of Django REST framework:

- Simplicity, flexibility, quality, and test coverage of source code.
- Powerful serialization engine compatible with both ORM and non-ORM data sources.
- Pluggable and easy to customise emitters, parsers, validators and authenticators.
- Generic classes for CRUD operations.
- Clean, simple, views for Resources, using Django's new class based views.
- Support for ModelResources with out-of-the-box default implementations and input validation (optional support for forms as input validation).
- HTTP response handling, content type negotiation using HTTP Accept headers.
- Pagination simplifies the process of returning paginated data in a way that can then be rendered to arbitrary media types.
- Publishing of metadata along with querysets.
- Permission classes and throttling management (API may feature a RESTrictive throttle for unauthenticated requests, a less RESTrictive throttle for authenticated requests, etc.).







