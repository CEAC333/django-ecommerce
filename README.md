# django-ecommerce

## Getting Started

  ### Software

  #### Software
  - Python 3.6
  - Django 1.11.5
  - HTML + CSS
  - Bootstrap v4

  #### Recommended Projects

  - Python - 30 Days Of Python
  - Django - Try Django 1.11
  - HTML + CSS - Getting Started with HTML & CSS
  - Bootstrap v4 - eCommerce

  #### Add-on Software

  - jQuery/Javascript 
  - Angular 
  - Ionic 

  #### Recommended Projects

  - jQuery/Javascript - eCommerce
  - Angular - Try Angular v4
  - Ionic - eCommerce

  #### Resources:
  - https://www.codingforentrepreneurs.com/projects/
  - https://www.youtube.com/codingentrepreneurs
  
  ### System Setup
  
  #### Windows
  - Video - https://www.codingforentrepreneurs.com/projects/setup-windows/
  - Text Guide - https://www.codingforentrepreneurs.com/blog/install-python-django-on-windows/
  
  #### Mac
  - Video - https://www.codingforentrepreneurs.com/projects/get-with-mac/
  - Text Guide - https://www.codingforentrepreneurs.com/blog/install-django-on-mac-or-linux/
  
  #### Linux
  - Video - https://www.codingforentrepreneurs.com/projects/start-with-linux/
  - Text Guide - https://www.codingforentrepreneurs.com/blog/install-django-on-linux-ubuntu/
  
  ### Open Source
  - https://github.com/codingforentrepreneurs
  
## Hello World
  
### A Fresh Virtualenv

```
virtualenv -p python3 .
```

### Hello World

```
pip install Django==1.11.4
```

```
mkdir src && cd src
```

```
django-admin startproject ecommerce .
```

```
python manage.py runserver
```

### Render HTML

Inside `ecommerce/src/ecommerce` create the file `views.py`

```python
from django.http import HttpResponse
from django.shortcuts import render

def home_page(request):
  return HttpResponse("<h1>Hello World</h1>")
```

Inside `ecommerce/src/ecommerce` modify the file `urls.py`

```python
from django.conf.urls import url
from django.contrib import admin

from .views import home_page

urlpatterns = [
  url(r'^$', home_page),
  url(r'^admin/', admin.site.urls),
]
```

### Django Template

- Bootstrap - Starter Template - http://getbootstrap.com/docs/4.0/getting-started/introduction/#starter-template

Inside `ecommerce/src/ecommerce` create the file `views.py`

```python
from django.http import HttpResponse
from django.shortcuts import render

def home_page(request):

  html_ = """
          <!doctype html>
          <html lang="en">
            <head>
              <!-- Required meta tags -->
              <meta charset="utf-8">
              <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

              <!-- Bootstrap CSS -->
              <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">

              <title>Hello, world!</title>
            </head>
            <body>
              <div class='text-center'>
                <h1>Hello, world!</h1>
              </div>
              <!-- Optional JavaScript -->
              <!-- jQuery first, then Popper.js, then Bootstrap JS -->
              <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
              <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
              <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
            </body>
          </html>
          """

  return HttpResponse(html_)
```


Inside `ecommerce/src/ecommerce` modify the file `settings.py` line 57

Go to `TEMPLATES` list, the first dict has a key `DIRS`

```python
    'DIRS': [os.path.join(BASE_DIR, 'templates')]
```

Inside `ecommerce/src/` create the folder `templates`

Inside `ecommerce/src/templates` create the file `home_page.html`

```html
<!doctype html>
          <html lang="en">
            <head>
              <!-- Required meta tags -->
              <meta charset="utf-8">
              <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

              <!-- Bootstrap CSS -->
              <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">

              <title>Hello, world We're working!</title>
            </head>
            <body>
              <div class='text-center'>
                <h1>Hello, world!</h1>
              </div>
              <!-- Optional JavaScript -->
              <!-- jQuery first, then Popper.js, then Bootstrap JS -->
              <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
              <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
              <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
            </body>
          </html>
```


Inside `ecommerce/src/ecommerce` modify the file `views.py`

```python
from django.http import HttpResponse
from django.shortcuts import render

def home_page(request):
  return render(request, "home_page.html", {})
```

### Template Context

Inside `ecommerce/src/ecommerce` modify the file `views.py`

```python
from django.http import HttpResponse
from django.shortcuts import render

def home_page(request):
  context = {
    "title":"Hello World!",
    "content":"Welcome to the homepage."
  }
  return render(request, "home_page.html", context)
  
def about_page(request):
  context = {
    "title":"About Page",
    "content":"Welcome to the about page."
  }
  return render(request, "home_page.html", context)
  
def contact_page(request):
  context = {
    "title":"Contact",
    "content":"Welcome to the contact page."
  }
  return render(request, "home_page.html", context)
```

Inside `ecommerce/src/ecommerce` modify the file `urls.py`

```python
from django.conf.urls import url
from django.contrib import admin

from .views import home_page, about_page, contact_page

urlpatterns = [
  url(r'^$', home_page),
  url(r'^about/$', about_page),
  url(r'^contact/$', contact_page),
  url(r'^admin/', admin.site.urls),
]
```

Inside `ecommerce/src/templates` modify the file `home_page.html`

```html
<!doctype html>
          <html lang="en">
            <head>
              <!-- Required meta tags -->
              <meta charset="utf-8">
              <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

              <!-- Bootstrap CSS -->
              <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">

              <title>Hello, world We're working!</title>
            </head>
            <body>
              <div class='text-center'>
                <h1>Hello, world!</h1>
              </div>
              
              <div class='container'>
              <div class='row'>
                <div class='col'>
                  <p>{{ content }}</p>
                </div>
              </div>
              </div>
              <!-- Optional JavaScript -->
              <!-- jQuery first, then Popper.js, then Bootstrap JS -->
              <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
              <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
              <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
            </body>
          </html>
```

### HTML Form

Inside `ecommerce/src/ecommerce` modify the file `views.py`

```python
from django.http import HttpResponse
from django.shortcuts import render

def home_page(request):
  context = {
    "title":"Hello World!",
    "content":"Welcome to the homepage."
  }
  return render(request, "home_page.html", context)
  
def about_page(request):
  context = {
    "title":"About Page",
    "content":"Welcome to the about page."
  }
  return render(request, "home_page.html", context)
  
def contact_page(request):
  context = {
    "title":"Contact",
    "content":"Welcome to the contact page."
  }
  if request.method == "POST":
    # print(request.POST)
    print(request.POST.get('fullname'))
    print(request.POST.get('email'))
    print(request.POST.get('content'))
  return render(request, "contact/view.html", context)
```

Inside `ecommerce/src/templates` create the folder `contact`

Inside `ecommerce/src/templates/contact` create the file `view.html`


```html
<!doctype html>
          <html lang="en">
            <head>
              <!-- Required meta tags -->
              <meta charset="utf-8">
              <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

              <!-- Bootstrap CSS -->
              <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">

              <title>Hello, world We're working!</title>
            </head>
            <body>
              <div class='text-center'>
                <h1>Hello, world!</h1>
              </div>
              
              <div class='container'>
              <div class='row'>
                <div class='col'>
                  <p>{{ content }}</p>
                  <div class='col-sm-6 col-12'>
                  <form method='POST'> {% csrf_token %}
                    <input type='text' class='form-control' placeholder="Name" name='fullname'>
                    <input type='email' class='form-control' placeholder="Email" name='email'>
                    <textarea name='content' class='form-control' placeholder="Your content"></textarea>
                    <button type='submit' class='btn btn-default'>Submit</button>
                  </form>
                  </div>
                </div>
              </div>
              </div>
              <!-- Optional JavaScript -->
              <!-- jQuery first, then Popper.js, then Bootstrap JS -->
              <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
              <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
              <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
            </body>
          </html>
```

### Django Forms

- https://docs.djangoproject.com/en/1.11/ref/forms/fields/#built-in-field-classes
- https://docs.djangoproject.com/en/1.11/ref/forms/widgets/#customizing-widget-instances

Inside `ecommerce/src/ecommerce` create the file `forms.py`

```python
from django import forms

class ContactForm(forms.Form):
  fullname = forms.CharField(
              widget=forms.TextInput(
                attrs={
                  "class": "form-control",
                  "placeholder": "Your full name"
                  }
                )
              )
  email = forms.EmailField(
              widget=forms.EmailInput(
                attrs={
                  "class": "form-control",
                  "placeholder": "Your email"
                  }
                )
              )
  content = forms.CharField(
              widget=forms.Textarea(
                attrs={
                  "class": "form-control",
                  "placeholder": "Your message"
                  }
                )
              )
              
  def clean_email(self):
    email = self.cleaned_data.get("email")
    if not "gmail.com" in email:
      raise forms.ValidationError("Email has to be gmail.com")
    return email

```

Inside `ecommerce/src/ecommerce` modify the file `views.py`

```python
from django.http import HttpResponse
from django.shortcuts import render

from .forms import ContactForm

def home_page(request):
  context = {
    "title":"Hello World!",
    "content":"Welcome to the homepage."
  }
  return render(request, "home_page.html", context)
  
def about_page(request):
  context = {
    "title":"About Page",
    "content":"Welcome to the about page."
  }
  return render(request, "home_page.html", context)
  
def contact_page(request):
  contact_form = ContactForm(request.POST or None)
  context = {
    "title":"Contact",
    "content":"Welcome to the contact page."
    "form":contact_form
  }
  if contact_form.is_valid():
    print(contact_form.cleaned_data)
  return render(request, "contact/view.html", context)
```


Inside `ecommerce/src/templates/contact` modify the file `view.html`


```html
<!doctype html>
          <html lang="en">
            <head>
              <!-- Required meta tags -->
              <meta charset="utf-8">
              <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

              <!-- Bootstrap CSS -->
              <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">

              <title>Hello, world We're working!</title>
            </head>
            <body>
              <div class='text-center'>
                <h1>Hello, world!</h1>
              </div>
              
              <div class='container'>
              <div class='row'>
                <div class='col'>
                  <p>{{ content }}</p>
                  <div class='col-sm-6 col-12'>
                  <form method='POST'> {% csrf_token %}
                    {{ form }}
                    <button type='submit' class='btn btn-default'>Submit</button>
                  </form>
                  </div>
                </div>
              </div>
              </div>
              <!-- Optional JavaScript -->
              <!-- jQuery first, then Popper.js, then Bootstrap JS -->
              <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
              <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
              <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
            </body>
          </html>
```

### User Login

- https://docs.djangoproject.com/en/1.11/topics/auth/default/#how-to-log-a-user-in


Inside `ecommerce/src/ecommerce` modify the file `views.py`

```python
rom django.contrib.auth import authenticate, login
from django.http import HttpResponse
from django.shortcuts import render, redirect

from .forms import ContactForm, LoginForm

def home_page(request):
  context = {
    "title":"Hello World!",
    "content":"Welcome to the homepage."
  }
  return render(request, "home_page.html", context)
  
def about_page(request):
  context = {
    "title":"About Page",
    "content":"Welcome to the about page."
  }
  return render(request, "home_page.html", context)
  
def contact_page(request):
  contact_form = ContactForm(request.POST or None)
  context = {
    "title":"Contact",
    "content":"Welcome to the contact page."
    "form":contact_form
  }
  if contact_form.is_valid():
    print(contact_form.cleaned_data)
  return render(request, "contact/view.html", context)
  
def login_page(request):
  form = LoginForm(request.POST or None)
  context = {
    "form": form
  }
  print("User logged in")
  #print(request.user.is_authenticated())
  if form.is_valid():
    print(form.cleaned_data)
    username = form.cleaned_data.get("username")
    password = form.cleaned_data.get("password")
    user = authenticate(request, username=username, password=password)
    print(user)
    #print(request.user.is_authenticated())
    if user is not None:
      #print(request.user.is_authenticated())
      login(request, user)
      # Redirect to a success page.
      #context['form'] = LoginForm()
      return redirect("/login")
    else:
      # Return an 'invalid login' error message.
      print("Error")
    
  return render(request, "auth/login.html", context)
  
def register_page(request):
  form = LoginForm(request.POST or None)
  if form.is_valid():
    print(form.cleaned_data)
  return render(request, "auth/register.html", {})
```

Inside `ecommerce/src/ecommerce` modify the file `forms.py`

```python
from django import forms

class ContactForm(forms.Form):
  fullname = forms.CharField(
              widget=forms.TextInput(
                attrs={
                  "class": "form-control",
                  "placeholder": "Your full name"
                  }
                )
              )
  email = forms.EmailField(
              widget=forms.EmailInput(
                attrs={
                  "class": "form-control",
                  "placeholder": "Your email"
                  }
                )
              )
  content = forms.CharField(
              widget=forms.Textarea(
                attrs={
                  "class": "form-control",
                  "placeholder": "Your message"
                  }
                )
              )
              
  def clean_email(self):
    email = self.cleaned_data.get("email")
    if not "gmail.com" in email:
      raise forms.ValidationError("Email has to be gmail.com")
    return email
    
class LoginForm(forms.Form):
  username = forms.CharField()
  password = forms.CharField(
              widget=forms.PasswordInput
              )

```

### User Register

- https://docs.djangoproject.com/en/1.11/topics/auth/default/#user-objects

Inside `ecommerce/src/ecommerce` modify the file `views.py`

```python
rom django.contrib.auth import authenticate, login, get_user_model
from django.http import HttpResponse
from django.shortcuts import render, redirect

from .forms import ContactForm, LoginForm, RegisterForm

def home_page(request):
  context = {
    "title":"Hello World!",
    "content":"Welcome to the homepage.",
    
  }
  if request.user.is_authenticated():
    context["premium_content"] = "YEAHHHHHH"
  return render(request, "home_page.html", context)
  
def about_page(request):
  context = {
    "title":"About Page",
    "content":"Welcome to the about page."
  }
  return render(request, "home_page.html", context)
  
def contact_page(request):
  contact_form = ContactForm(request.POST or None)
  context = {
    "title":"Contact",
    "content":"Welcome to the contact page."
    "form":contact_form
  }
  if contact_form.is_valid():
    print(contact_form.cleaned_data)
  return render(request, "contact/view.html", context)
  
def login_page(request):
  form = LoginForm(request.POST or None)
  context = {
    "form": form
  }
  print("User logged in")
  #print(request.user.is_authenticated())
  if form.is_valid():
    print(form.cleaned_data)
    username = form.cleaned_data.get("username")
    password = form.cleaned_data.get("password")
    user = authenticate(request, username=username, password=password)
    print(user)
    #print(request.user.is_authenticated())
    if user is not None:
      #print(request.user.is_authenticated())
      login(request, user)
      # Redirect to a success page.
      #context['form'] = LoginForm()
      return redirect("/")
    else:
      # Return an 'invalid login' error message.
      print("Error")
    
  return render(request, "auth/login.html", context)
  
User = get_user_model()
def register_page(request):
  form = RegisterForm(request.POST or None)
  context = {
    "form": form
  }
  if form.is_valid():
    print(form.cleaned_data)
    username = form.cleaned_data.get("username")
    email = form.cleaned_data.get("email")
    password = form.cleaned_data.get("password")
    new_user = User.objects.create_user(username, email, password)
    print(new_user)
  return render(request, "auth/register.html", context)
```


Inside `ecommerce/src/templates` modify the file `home_page.html`

```html
<!doctype html>
          <html lang="en">
            <head>
              <!-- Required meta tags -->
              <meta charset="utf-8">
              <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

              <!-- Bootstrap CSS -->
              <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">

              
            </head>
            <body>
              <div class='text-center'>
                <h1>{{ title }}</h1>
                <h1>Hello, world we're working!</h1>
              </div>
              
              <div class='container'>
                <div class='row'>
                  <div class='col'>
                    <p>{{ content }}</p>
                  </div>
                </div>
                {% if request.user.is_authenticated %}
                <div class='row'>
                  <div class='col'>
                  <h1>Premium</h1>
                  {{ premium_content }}
                  </div>
                </div>
                {% endif %}
              </div>
              <!-- Optional JavaScript -->
              <!-- jQuery first, then Popper.js, then Bootstrap JS -->
              <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
              <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
              <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
            </body>
          </html>
```

Inside `ecommerce/src/ecommerce` modify the file `forms.py`

```python
from django import forms
from django.contrib.auth import get_user_model

User = get_user_model()

class ContactForm(forms.Form):
  fullname = forms.CharField(
              widget=forms.TextInput(
                attrs={
                  "class": "form-control",
                  "placeholder": "Your full name"
                  }
                )
              )
  email = forms.EmailField(
              widget=forms.EmailInput(
                attrs={
                  "class": "form-control",
                  "placeholder": "Your email"
                  }
                )
              )
  content = forms.CharField(
              widget=forms.Textarea(
                attrs={
                  "class": "form-control",
                  "placeholder": "Your message"
                  }
                )
              )
              
  def clean_email(self):
    email = self.cleaned_data.get("email")
    if not "gmail.com" in email:
      raise forms.ValidationError("Email has to be gmail.com")
    return email
    
class LoginForm(forms.Form):
  username = forms.CharField()
  password = forms.CharField(
              widget=forms.PasswordInput
              )
              
class RegisterForm(forms.Form):
  username = forms.CharField()
  email = forms.EmailField()
  password = forms.CharField(
                widget=forms.PasswordInput
              )
  password2 = forms.CharField(
                label='Confirm password'          
                widget=forms.PasswordInput
              )
              
  def clean_username(self):
    username = self.cleaned_data.get('username')
    qs = User.objects.filter(username=username)
    if qs.exists():
      raise forms.ValidationError("Username is taken")
    return username
    
  def clean_email(self):
    email = self.cleaned_data.get('email')
    qs = User.objects.filter(email=email)
    if qs.exists():
      raise forms.ValidationError("email is taken")
    return email
  
  def clean(self):
    data = self.cleaned_data
    password = self.cleaned_data.get('password')
    password2 = self.cleaned_data.get('password2')
    if password2 != password:
      raise forms.ValidationError("Passwords must match.")
    return data

```

Inside `ecommerce/src/templates/auth` create the file `register.html`

```html
<form method='POST'> {% csrf_token %}
  {{ form }}
  <button type='submit' class='btn btn-default'>Submit</button>
</form>
```

Inside `ecommerce/src/ecommerce` modify the file `urls.py`

```python
from django.conf import settings
from django.conf.urls.static import static

from django.conf.urls import url
from django.contrib import admin


from .views import home_page, about_page, contact_page, login_page, register_page

urlpatterns = [
  url(r'^$', home_page),
  url(r'^about/$', about_page),
  url(r'^contact/$', contact_page),
  url(r'^login/$', login_page),
  url(r'^register/$', register_page),
  url(r'^admin/', admin.site.urls),
]

if settings.DEBUG:
  urlpatterns = urlpatterns + static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)
```

### Setup & Serve Local Static & Media Files

- http://getbootstrap.com/
- https://docs.djangoproject.com/en/1.11/howto/static-files/

Inside `ecommerce` create the folder `static_cdn`

Inside `ecommerce/src/ecommerce` modify the file `setting.py`, add this at the end of the file

```python
STATICFILES_DIRS = [
    os.path.join(BASE_DIR, "static_my_proj"),
]

STATIC_ROOT = os.path.join(os.path.dirname(BASE_DIR), "static_cdn", "static_root")

MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(os.path.dirname(BASE_DIR), "static_cdn", "media_root")
```

Inside `ecommerce/src` create the folder `static_my_proj`


Inside `ecommerce/src/ecommerce` modify the file `settings.py`, line 26

```python
DEBUG = False
```

Inside the terminal with the env activated, run the commd to move static files:

```
python manage.py collectstatic
```

```
python manage.py runserver
```

Inside `ecommerce/src/static_cdn` the folder `admin` was created, delete it

Inside `ecommerce/src/ecommerce` modify the file `urls.py`

```python
from django.conf import settings
from django.conf.urls.static import static

from django.conf.urls import url
from django.contrib import admin


from .views import home_page, about_page, contact_page, login_page, register_page

urlpatterns = [
  url(r'^$', home_page),
  url(r'^about/$', about_page),
  url(r'^contact/$', contact_page),
  url(r'^login/$', login_page),
  url(r'^register/$', register_page),
  url(r'^admin/', admin.site.urls),
]

if settings.DEBUG:
  urlpatterns = urlpatterns + static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)
  urlpatterns = urlpatterns + static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
```

Inside `ecommerce/src/static_cdn` create the folder `media_root` 

Inside `ecommerce/src/ecommerce/static_my_proj` create the folder `css` 

Inside `ecommerce/src/ecommerce/static_my_proj/css` create the file `main.css` 

```css
body {
  color: #ccc;
}
```

Inside the terminal with the env activated, run the commd to move static files to `static_cdn`:

```
python manage.py collectstatic
```

```
python manage.py runserver
```

Inside `ecommerce/src/static_my_proj/css/img` download an image `img.jpg` 

Inside the terminal with the env activated, run the commd to move static files to `static_cdn`:

```
python manage.py collectstatic
```

```
python manage.py runserver
```

Inside `ecommerce/src/templates` modify the file `home_page.html`

```html
<!doctype html>
          <html lang="en">
            <head>
              <!-- Required meta tags -->
              <meta charset="utf-8">
              <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

              <!-- Bootstrap CSS -->
              <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
              <link rel='stylesheet' href='{ static "css/main.css" %}' >
              
            </head>
            <body>
              <div class='text-center'>
                <h1>{{ title }}</h1>
                <h1>Hello, world we're working!</h1>
              </div>
              
              <div class='container'>
                <div class='row'>
                  <div class='col'>
                    <img src="{% static 'img/img.jpg' %}" class='img-fluid' />
                    <p>{{ content }}</p>
                  </div>
                </div>
                {% if request.user.is_authenticated %}
                <div class='row'>
                  <div class='col'>
                  <h1>Premium</h1>
                  {{ premium_content }}
                  </div>
                </div>
                {% endif %}
              </div>
              <!-- Optional JavaScript -->
              <!-- jQuery first, then Popper.js, then Bootstrap JS -->
              <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
              <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
              <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
            </body>
          </html>
```
  
## Products Component

### Your First App Module

```
cd ecommerce
source bin/activate
cd src
python manage.py startapp products
```

This will create the folder `products` inside `ecommerce/src`


### Understanding CRUD

- Create -- POST
- Retrieve / List / Search --GET
- Update -- PUT / Patch / POST
- Delete -- Delete

```
python manage.py createsuperuser
```

```
python manage.py runserver
```

Go to

```
localhost:8000/admin
```

### Product Model

- https://docs.djangoproject.com/en/1.11/ref/models/fields/

Inside `ecommerce/src/products` modify the file `models.py` 

```python
from django.db import models

# Create your models here.
class Product(models.Model):
  title       = models.CharField(max_length=120)
  description = models.TextField()
  price       = models.DecimalField(decimal_places=2, max_digits=20, default=39.99) 
```

Inside `ecommerce/src/ecommerce` modify the file `settings.py`, line 33

```python
INSTALLED_APPS = [
  'django.contrib.admin',
  'django.contrib.auth',
  'django.contrib.contenttypes',
  'django.contrib.sessions',
  'django.contrib.messages',
  'django.contrib.staticfiles',
  
  # our apps
  'products'
]
```

In the terminal

```
python manage.py makemigrations
```

```
python manage.py migrate
```

### Django Admin

### List View

### Detail View

### ImageField & FileField

### Understanding Lookups

### Custom Model Managers

### Featured & Custom QuerySets

### SlugField & Signals

### Product URLs
  
## Templates

  ### Intro
  
  ### Base Template
  
  ### Include Tag
  
  ### Pass Arguments with Include
  
  ### Reusable List View Snippets
  
  ### Reverse for URLs
  
  ### NavBar
  
  ### Template Filters
  
  ### ForLoop Counter & Cycle
  
## Bootstrap Framework

  ### Intro
  
  ### Adding Bootstrap
  
  ### Container vs Container-Fluid
  
  ### Rows and Columns
  
  ### Column Sizing
  
  ### Offset & Ordering
  
  ### Designing for Different Browser Sizes with Breakpoints
  
  ### Spacing with Margin & Padding
  
  ### Navbar
  
  ### Prepare for Integration
  
  ### Integrate to Django
  
## Search Component

  ### Intro
  
  ### A Basic Search View
  
  ### Display the Query to the User
  
  ### Creating the Search Form
  
  ### Better Lookups with Q
  
  ### Tag Component
  
  ### Shell Commands for a Brief Intro to Foreign Keys
  
  ### Search by Related Model
  
## Cart Component

  ### Intro
  
  ### Cart App
  
  ### Django Sessions
  
  ### Cart Model
  
  ### Create a Cart in the View
  
  ### Cart Model Manager Part 1
  
  ### Cart Model Manager Part 2
  
  ### M2M Changed Signal to Calculate Cart Total
  
  ### Cart Update View
  
  ### Add to Cart Form
  
  ### Display Cart
  
  ### Remove Items from the Cart
  
  ### Cart Icon & Font Awesome
  
## Checkout Process

  ### Intro
  
  ### The Roadmap for the Checkout Process
  
  ### The Order Component
  
  ### Generate the Order ID
  
  ### Calculate the Order Total
  
  ### Checkout View
  
  ### Math with Decimals and Floats in Python
  
  ### Upgrading Auth to Prep for Checkout
  
  ### Billing Profile Model
  
  ### Billing Profile in the Checkout View
  
  ### Guest Checkout Profile
  
  ### Associate Billing Profile to Order
  
  ### Order Manager
  
  ### Billing Profile Manager
  
  ### Addresses App
  
  ### Addresses App Part 2
  
  ### Associate Addresses to Order
  
  ### Finalize Checkout
  
  ### Reuse Addresses for Checkout
  
  ### Checkout Success
  
## Fast Track to jQuery

  ### Intro
  
  ### Getting Started
  
  ### A Basic Selector
  
  ### Selectors Part 2
  
  ### Content Overflow Part 1
  
  ### Data Types, Iteration and Conditionals
  
  ### Content Overflow Part 2
  
  ### Click Events
  
  ### Handling form data in jQuery
  
## Products & Async

  ### Intro
  
  ### Sync vs Async
  
  ### Ajax-ify a Form
  
  ### Handle Ajax in Django with JsonResponse
  
  ### Cart Item Count
  
  ### Refresh Cart Ajax
  
  ### Refresh Cart Ajax 2
  
  ### Refresh Cart Ajax 3
  
  ### Finalize Cart Updating with Ajax
  
  ### Auto Search
  
  ### Display Errors with jQuery Confirm
  
  ### Ajaxify the Contract Form Part 1
  
  ### Ajaxify the Contract Form Part 2
  
  ### Custom eCommerce JS
  
  ### Ajax CSRF Security for Django
  
## Custom User Model

  ### Intro
  
  ### Before we get started
  
  ### Create the Abstract Base User
  
  ### Create the User Model Manager
  
  ### Change Default Auth User Model to our Custom Model
  
  ### Reload the Database with Fixtures
  
  ### Forms & Admin for our Custom User
  
  ### Add a Required Field to the User Model
  
  ### Update Login & Register Forms
  
  ### Login & Register Views
  
## Custom Analytics

  ### Intro
  
  ### Getting Started
  
  ### Craft the Object Viewed Model
  
  ### Get Client IP Address
  
  ### A Custom Signal
  
  ### Object Viewed Mixin
  
  ### Handle the Object Viewed Signal
  
  ### Handling and Endling User Sessions
  
## Stripe Integration

  ### Intro
  
  ### Getting Started
  
  ### Create Stripe Customer
  
  ### Payment Method View & Stripe JS
  
  ### Improving Payment Method Form 
  
  ### Improving Payment Method Form Part 2
  
  ### Reusable Stripe Module
  
  ### Add Card to Customer with Stripe
  
  ### Save Card in Django
  
  ### Charge the Customer
  
  ### Putting it All Together
  
  ### Guest Card Checkout 
  
  ### Changing Payment Methods
  
  ### Improving Card UI Part 1
  
  ### Improving Card UI Part 2

  
## Mailchimp Integration

  ### Intro
  
  ### The Value of Email
  
  ### Marketing vs Transactional Email
  
  ### Setup API Keys
  
  ### Marketing App
  
  ### Mailchimp Class Part 1
  
  ### Mailchimp Class Part 2
  
  ### Mailchimp Class Part 3
  
  ### Django & Mailchimp
  
  ### User Email Marketing Preference View
  
  ### Mailchimp Webhook Handler
  
## Go Live

  ### Local vs Production Environments
  
  ### New Settings Module
  
  ### Multiple Settings Modules
  
  ### Prepare for HTTPs
  
  ### The gitignore File
  
  ### Requirements File
  
  ### Setup Git Version Control
  
  ### Deploy to Heroku
  
  ### AWS S3 for Static Files
  
  ### Add Custom Domain & HTTPs on Heroku
  
  ### Live Environment Variables
  
  ### Error Views and Templates
  
  ### Setup Email to Help Solve Server Errors
  
  ### Using Heroku Locally
  
## Account & Settings

  ### User Account Home
  
  ### Naming & Dropdown
  
  ### Account Bootstrap Cards
  
  ### Link Account Bootstrap Cards
  
  ### Password Reset and Change
  
  ### send_email and get_template
  
  ### Email Activation
  
  ### Custom QuerySet for Confirmable Activations
  
  ### Email Activation View
  
  ### Email Reactivation
  
  ### Improved Login Form & View
  
  ### Login Form for Confirmation Email
  
  ### Upgrading the Guest Checkout Form
  
  ### Edit Account Details
  
  ### User Product History View
  
  ### Orders & Order Detail
  
## Selling Digital Items

  ### Digital Products & Cart
  
  ### Shipping-less Checkout
  
  ### Product Purchases
  
  ### Handling Products Being Purchased
  
  ### Display of Refunded Items
  
  ### library View
  
  ### Library View for Products Only
  
  ### Product File Model
  
  ### Changing File Field Storage to Protected Location
  
  ### Download Product File Part 1
  
  ### Download Product File Part 2
  
  ### Perform the File Download
  
  ### Checking Download Permissions
  
  ### In Library Display Part 1
  
  ### In Library Display Part 2 with Ajax
  
  ### AWS S3 File Upload
  
  ### Fixing the Upload Path
  
  ### Creating the AWS Download Class
  
  ### Using the AWS Download Client
  
  ### A Custom Filename
  
## Graphs and Sales

  ### Setup the View
  
  ### Add Context for the Order Data
  
  ### Intuitive Recent Order Total
  
  ### Aggregate & Annotate
  
  ### Get Data by Custom QuerySet
  
  ### Intro to Datetime Module
  
  ### Filter by Range of Time
  
  ### Chart-js Intro
  
  ### Using Ajax to Render Charts
  
  ### Display True Data
  
  ### Cleanup
  
  ### Inline Js to External
  
  
  

## References:
- https://www.udemy.com/python-ecommerce-build-a-django-ecommerce-web-application
