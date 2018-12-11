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

```
from django.http import HttpResponse
from django.shortcuts import render

def home_page(request):
  return HttpResponse("<h1>Hello World</h1>")
```

Inside `ecommerce/src/ecommerce` modify the file `urls.py`

```
from django.conf.urls import url
from django.contrib import admin

from .views import home_page

urlpatterns = [
  url(r'^$', home_page),
  url(r'^admin/', admin.site.urls),
]
```

### Django Template

### Template Context

### HTML Form

### Django Forms

### User Login

### User Register

### Setup & Serve Local Static & Media Files
  
## Products Component

  ### Intro
  
  ### Your First App Module
  
  ### Understanding CRUD
  
  ### Product Model
  
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
