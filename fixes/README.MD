# Правки.
## Freemanagers
<img src = "img/fix02.jpg">
<img src = "img/fix01.jpg">

Всі хто вільний на даний час на тижні. А також можна обирати тих МІКів, які відображаються.  
Бек-енд:  
<a href = "https://goiteens-booking-system.herokuapp.com/avaliable_managers_list/14/6">https://goiteens-booking-system.herokuapp.com/avaliable_managers_list/14/6</a> 

## ManagersPostpone
<img src = "img/fix03.jpg">
Додати кнопку "Перенести" (Postpone) до форми інформації про консуьлтацію.  

Функціонал - аналогічний переносу у конфірматора.  

PUT /set_postpone_confirmation/{int:slot_id}/{int:appointment_id}  

<img src = "img/Letter - 3.png" width = 500>

## Cancelation

/set_cancel_confirmation/<int:slot_id>/<int:cancel_type>/<string:message>/

## NoList
<img src = "img/fix04.jpg">  
Прибрати перелік вибору менеджеру.

## Information
<img src = "img/fix05.jpg">  
При фіксації підтвердження, переносу, відміни - вспливає інформаційне вікно.

## Confirmed

<img src = "img/fix06.jpg">  
/get_confirmed/<int:week_id>/<int:day>/<int:half>/

Додати пункт меню "Підтверджені", які відображають перелік всіх підтверджених консультацій.