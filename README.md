# Ex02 Django ORM Web Application
## Date: 28/04/2024

## AIM
To develop a Django application to store and retrieve data from a Movies Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM



## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
admin.py
~~~
from django.contrib import admin
from .models import book,bookadmin
admin.site.register(book,bookadmin)
~~~
models.py
~~~
from django.db import models
from django.contrib import admin
class book(models.Model):
    Book_name=models.CharField(max_length=100)
    Author=models.CharField(max_length=100)
    Co_author=models.CharField(max_length=100)
    Book_code=models.IntegerField()
    Publisher=models.CharField(max_length=100)
    MRP=models.IntegerField()
class bookadmin(admin.ModelAdmin):
    list_display=("Book_name","Author","Co_author","Book_code","Publisher","MRP")
~~~
urls.pr
~~~

from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
]
~~~
## OUTPUT
![orm 1](https://github.com/user-attachments/assets/0ca72159-8716-4d89-9b2f-627853f0bcf4)
![orm 2](https://github.com/user-attachments/assets/b8a0e88b-95ef-485d-8d34-53b7893333e1)

![orm 3](https://github.com/user-attachments/assets/d3281e18-bae6-447f-b41b-946396cb9c6f)


## RESULT
Thus the program for creating movies database using ORM hass been executed successfully
