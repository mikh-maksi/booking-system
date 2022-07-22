# Конфірматор
Запит:
/current_confirmation
Відповідь:
{week_id:1,
day:0,
half:1,
appointments:[
    {appointmentt_id:121;hour:11;course:Minecraft;manager_name:Марія;phone:+380631234567;status:3;},
    {appointmentt_id:122;hour:11;course:FrontEnd;manager_name:Артем;phone:+380631234567;status:2;},
    {appointmentt_id:123;hour:11;course:GameDev;manager_name:Олена;phone:+380631234567;status:1;},
    
]
}

Запит:
/get_confirmation :week_id :day :half

/get_confirmation week_id:1 day:0 half:2

{week_id:1,
day:0,
half:2,
appointments:[
    {appointmentt_id:131;hour:15;course:Minecraft;manager_name:Марія;phone:+380631234567;status:3;},
    {appointmentt_id:132;hour:16;course:FrontEnd;manager_name:Артем;phone:+380631234567;status:2;},
    {appointmentt_id:133;hour:17;course:GameDev;manager_name:Олена;phone:+380631234567;status:1;},
]
}

Запит:
/change_appointment appointmentt_id:131;status:2;

/change_appointment appointmentt_id:133;week:2;day:3,hour;13;status:0;