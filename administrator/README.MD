# Адміністратор
**Адміністратор** - це керівник відділу індивідуальних консультацій чи тім лід команди менеджерів індивідуальних консультацій.  

**Адміністратор** - має власний інтерфейс, на який заходить за адресою /administrator/:id , де :id ідентифікатор адмінітратора в базі даних.

У Адміністратора є основні функції: створення та редагування користувачів, управління курсами, управління групаи по курсах, контроль та корегування дій всіх спеціалістів.

<img src = "img/admin_01.png">  

<img src = "img/admin_02.png">  

<img src = "img/admin_03.png">  

  POST /register_manager

<img src = "img/admin_04.png">  

## CRUD курсів.

<img src = "img/admin_05.png">  

<img src = "img/admin_06.png">  

<img src = "img/admin_07.png">  


GET /courses

POST /register_course

DELETE /remove_course/{int:element_id}

PUT /update_course/{int:element_id}

## CRUD Груп курсів.