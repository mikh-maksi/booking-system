# Super Administrator

## Users
* CREATE 
  * POST users name, telegram, login, password, role_id
* READ
  * GET users?role=2 (managers)
  * GET users?role=3 (callers)
  * GET users?role=4 (confirmators)
* UPDATE

* DELETE
  * remove_user id



## Avaliable Managers
/avaliable_managers :date :half  

{date:11.09.22,half:1,avaliable_managers:[{time:8,managers:['Марія', 'Артем', 'Роман', 'Слава', 'Марина']},{time:9,managers:['Марія', 'Артем', 'Роман', 'Слава', 'Марина']},{time:10,managers:['Марія', 'Артем', 'Роман', 'Слава', 'Марина']},{timd:11,managers:['Марія', 'Артем', 'Роман', 'Слава', 'Марина']},{timd:12,managers:['Марія', 'Артем', 'Роман', 'Слава', 'Марина']},{timd:13,managers:['Марія', 'Артем', 'Роман', 'Слава', 'Марина']},{timd:14,managers:['Марія', 'Артем', 'Роман', 'Слава', 'Марина']}]


## Search
**/search** :crm_link

Відповідь:
{  
    appointment_id:1234
    week_id:1,  
    day_id:0,  
    day:11.09,  
    weekday:'Пн',
    hour:11,  
    slot_id:121,  
    course_id:1,
    course:'Python'.
    crm_link:"http://zoho.com/1244",  
    phone:"+380631234567",  
    age:10,  
    manager_id:111,
    manager_name:'Марія'    
}
  


**/update_appointment** :appointment_id :week_id :day_id :hour :course_id :crm_link :phone :age :manager_id 

{  
    appointment_id:1234
    week_id:1,  
    day_id:0,  
    day:11.09,  
    weekday:'Пн',
    hour:11,  
    slot_id:121,  
    course_id:1,
    course:'Python'.
    crm_link:"http://zoho.com/1244",  
    phone:"+380631234567",  
    age:10,  
    manager_id:111,
    manager_name:'Марія'    
}