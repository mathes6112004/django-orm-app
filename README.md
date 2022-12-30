# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here
### Creating django-orm-app

create django orm app

### Step 1:
then clone it.create my app

### Step 2:
then run the webserver,create the super user,after that create the 10 employee id


### Step 3:
then add the screenshot of employee id in output



## PROGRAM

#setting.py

Database
 https://docs.djangoproject.com/en/3.1/ref/settings/#databases

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}

#models.py

from django.db import models
from django.contrib import admin

class employee (models.Model):
    EMP_ID=models.CharField(primary_key=True,max_length=20,help_text="EMP_ID")
    ENAME=models.CharField(max_length=100)
    POST=models.CharField(max_length=20)
    SALARY=models.IntegerField()

class employeeAdmin(admin.ModelAdmin):
      list_display=('EMP_ID','ENAME','POST','SALARY')

admin.py

from django.contrib import admin
from .models import employee,employeeAdmin

admin.site.register(employee,employeeAdmin)

## OUTPUT:

Include the screenshot of your admin page.
### Employee Id:

![Employee_id](./img2/10employeeid.jpeg)

### Primary Key error:

![Employee_id](./img2/primarykey.jpeg)



## RESULT
Django application to store and retrieve data from a database using Object Relational Mapping(ORM) is developed.