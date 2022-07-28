# Django Forms

## Django Form class

model class’s fields map to database fields, a form class’s fields map to HTML form <input> elements. (A ModelForm maps a model class’s fields to HTML form <input> elements via a Form; this is what the Django admin is based upon.)

A form’s fields are themselves classes; they manage form data and perform validation when a form is submitted. A DateField and a FileField handle very different kinds of data and have to do different things with it.



## Building a form 

first we need html form  in the template:

```
<form action="/your-name/" method="post">
    <label for="your_name">Your name: </label>
    <input id="your_name" type="text" name="your_name" value="{{ current_name }}">
    <input type="submit" value="OK">
</form>
```

This tells the browser to return the form data to the URL /your-name/, using the POST method. It will display a text field, labeled “Your name:”, and a button marked “OK”. If the template context contains a current_name variable, that will be used to pre-fill the your_name field.

You’ll need a view that renders the template containing the HTML form, and that can supply the current_name field as appropriate.

When the form is submitted, the POST request which is sent to the server will contain the form data.


## Building a form in Django

```
from django import forms

class NameForm(forms.Form):
    your_name = forms.CharField(label='Your name', max_length=100)
```
