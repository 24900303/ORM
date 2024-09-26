# Ex02 Django ORM Web Application
## Date: 26-09-2024

## AIM
To develop a Django application to store and retrieve data from a Bank database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![image](https://github.com/user-attachments/assets/785aa437-3397-4037-82fe-802055a301d9)


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

# Register your models here.
from .models import bankloan,bankloanAdmin
admin.site.register(bankloan,bankloanAdmin)
```

models.py
```
from django.db import models

# Create your models here.
from django.contrib import admin
class bankloan(models.Model):
    accno=models.IntegerField(primary_key=True);
    name=models.CharField(max_length=100);
    loanamt=models.IntegerField();
    loanlimit=models.IntegerField();
    phoneno=models.IntegerField();

class bankloanAdmin(admin.ModelAdmin):
    list_display=('accno','name','loanamt','loanlimit','phoneno')

## OUTPUT

![Screenshot 2024-09-26 114622](https://github.com/user-attachments/assets/f365d00b-fe85-425e-86b2-5dc9ca1dfd66)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
