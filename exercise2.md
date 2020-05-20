---
layout: default
title: JASP Practice Statistics
category : [relationship, testing]
subcategory: [correlation, JASP, Statistics]
---
### [<BACK](/index.md)

    python
    from .models import ToDoList, Item
# from forms import CreateNewList


# Create your views here.


def index(response, id):
    ls = ToDoList.objects.get(id=id)
    return render(response, "main/list.html", {"ls": ls})


def home(response):
    return render(response, "main/home.html", {}
    
    





### [NEXT>](/_posts/2020-05-20-post1.md)
