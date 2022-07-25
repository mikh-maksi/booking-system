# Конфірматор
Запит:
(відбувається за внутрішнім часом серверу на бек-енді)
/current_confirmation

Відповідь:
(генерується із таблиць slots та appointment за зв'язком по slot_id в таблиці appointments, де у полі work_status_id = 3 :заплановано, але не підтверджено)
{week_id:1,
day:0,
half:1,
appointments:[
    {appointment_id:121;hour:11;course:Minecraft;manager_name:Марія;phone:+380631234567;status:3;},
    {appointment_id:122;hour:11;course:FrontEnd;manager_name:Артем;phone:+380631234567;status:2;},
    {appointment_id:123;hour:11;course:GameDev;manager_name:Олена;phone:+380631234567;status:1;},
]
}

Запит:
/get_confirmation :week_id :day :half


Відповідь:
(повертаємо тільки ті заявки, які ще не підтверджено: зі статусом 3)
{week_id:1,
day:2,
half:1,
appointments:[
    {appointment_id:111;hour:11;course:Minecraft;manager_name:Марія;phone:+380631234567;slot_id:111;status:3;},
    {appointment_id:112;hour:11;course:FrontEnd;manager_name:Артем;phone:+380631234567;slot_id:113;status:3;},
    {appointment_id:113;hour:11;course:GameDev;manager_name:Олена;phone:+380631234567;slot_id:114;status:3;},
    {appointment_id:114;hour:12;course:GameDev;manager_name:Марія;phone:+380631234567;slot_id:116;status:3;},
]
}

/get_confirmation week_id:1 day:0 half:2


{week_id:1,
day:0,
half:2,
appointments:[
    {appointment_id:131;hour:15;course:Minecraft;manager_name:Марія;phone:+380631234567;slot_id:111;status:3;},
    {appointment_id:132;hour:16;course:FrontEnd;manager_name:Артем;phone:+380631234567;slot_id:113;status:2;},
    {appointment_id:133;hour:17;course:GameDev;manager_name:Олена;phone:+380631234567;slot_id:114;status:1;},
]
}

Запит:
/set_confirmation :slot_id :status :message
/set_confirmation slot_id:111 status:4 message: "раніше грав в Roblox"

(змінюється поле work_status_id на 4 (заплановано та підтверджено) в таблиці slots за ключем slot_id)

Відповідь:
{"Підвержено"}

/set_cancel_confirmation :slot_id :cancel_type :message
/set_cancel_confirmation slot_id:111 cancel_type:1 message:"вже обрали іншу школу"

Відповідь:
{"Відмінено"}

/set_postpone_confirmation :slot_id :appointment_id
(для запису в таблиці appointments за ключем :appointment_id змінити поле slot_id на значення отримане в полі :slot_id )
Відповідь:
{"Перенесено"}

