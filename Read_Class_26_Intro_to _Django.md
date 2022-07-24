## What is Django?
Django is a high-level Python web framework that enables rapid development of secure and maintainable websites

## Intro to Django

### Models

in Django you can control the data  base with python command see the example:

```
from django.db import models

class Person(models.Model):
    first_name = models.CharField(max_length=30)
    last_name = models.CharField(max_length=30)
    
```
The above Person model would create a database table like this:
```
CREATE TABLE myapp_person (
    "id" serial NOT NULL PRIMARY KEY,
    "first_name" varchar(30) NOT NULL,
    "last_name" varchar(30) NOT NULL
);
```

so you create a table in the database 


### Templates

Django’s template language is designed to strike a balance between power and ease.

It’s designed to feel comfortable and easy-to-learn to those used to working with HTML

```
<html>
  <head>
    <title>Band Listing</title>
  </head>
  <body>
    <h1>All Bands</h1>
    <ul>
    {% for band in bands %}
      <li>
        <h2><a href="{{ band.get_absolute_url }}">{{ band.name }}</a></h2>
        {% if band.can_rock %}<p>This band can rock!</p>{% endif %}
      </li>
    {% endfor %}
    </ul>
  </body>
</html>
```
in the above we used some py code in the html


### Forms

Django provides a powerful form library that handles rendering forms as HTML, validating user-submitted data, and converting that data to native Python types. 

Django also provides a way to generate forms from your existing models and use those forms to create and update data.

```
from django import forms

class BandContactForm(forms.Form):
    subject = forms.CharField(max_length=100)
    message = forms.CharField()
    sender = forms.EmailField()
    cc_myself = forms.BooleanField(required=False)
```

in the above the subject have a max length restriction it should not be more than 100

also the cc_myself as we se it's not required and it can be change to the requered 



### Authentication

Django comes with a full-featured and secure authentication system. It handles user accounts, groups, permissions and cookie-based user sessions.

This lets you easily build sites that allow users to create accounts and safely log in/out.

```
from django.contrib.auth.decorators import login_required
from django.shortcuts import render

@login_required
def my_protected_view(request):
    """A view that can only be accessed by logged-in users"""
    return render(request, 'protected.html', {'current_user': request.user})
    
```

The code above will only allow view to the logged in uers only.

There is a lot you can do in the Authentication like handles user accounts, groups, permissions, admins etc...



