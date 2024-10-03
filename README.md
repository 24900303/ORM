# Ex02 Django ORM Web Application
## Date: 03.10.2024

## AIM
To develop a Django application to store and retrieve data from a Bank database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![image](https://github.com/user-attachments/assets/1a68f74b-0c7f-4e4c-8fb8-009da0f016dc)

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 customers.

## PROGRAM
admin.py
```
from django.contrib import admin
from .models import Bankloan, BankloanAdmin  
admin.site.register(Bankloan, BankloanAdmin)
```
model.py
```
from django.db import models
from django.contrib import admin
from django.db import models
from django.contrib import admin

class Bankloan(models.Model):
    customerid= models.IntegerField(primary_key=True)
    customerrate = models.IntegerField()
    age = models.IntegerField()  
    cust_no = models.IntegerField()
    customerloan_purpose =models.CharField(max_length=500)

class BankloanAdmin(admin.ModelAdmin):
    list_display = ('customerid', 'customerrate', 'age', 'cust_no', 'customerloan_purpose')
```

## OUTPUT
![Screenshot 2024-10-03 112541](https://github.com/user-attachments/assets/753261a8-1f3b-4ac0-b42d-a135365b2438)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully


