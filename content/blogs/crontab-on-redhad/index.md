---
title: 'การเขียน crontab บน Linux Redhat'
date: 2010-04-26T11:36:22+07:00
draft: false
---
Cron เป็นการสั่งคำสั่งเพื่อให้ server ของเรานั้นทำงานโดยอัตโนมัติตามเวลาที่เราเขียนไฟล์ตั้งเวลาไว้ หรือพูดง่าย ๆ ว่าเป็นการรันสคริปต์ตามเวลาที่เราตั้งไว้นั่นเอง ซึ่งส่วนใหญ่จะเป็นงานซ้ำ ๆ ที่ต้องสั่งเหมือนกัน ทุก ๆ วัน หรือทุก ๆ สัปดาห์  cron ก็จะมาช่วยอำนวยความสะดวกให้เราได้ ซึ่งถ้าเราต้องการตั้งเวลาทำงานอัตโนมัตินั้น เราจะไประบุได้ที่ไฟล์ /etc/crontab ซึ่งจะเป็นไฟล์ที่เก็บคำสั่งและเวลาที่ต้องการให้คำสั่งทำงาน ซึ่งจะเป็นรูปแบบ
<table class="table table-bordered">
         <td>
            # * * * * *   < user >    < command >  // ซึ่งตัว * แต่ละหลักจะมีความหมายดังนี้ 
         </td>
</table>

- นาที ( 0-59 )  
- ชั่วโมง ( 0-23 )  
- วันในรอบเดือน ( 1-31 )  
- เดือน (1-12)  
- วันในสัปดาห์ (0-6   Sunday =0 )  
ซึ่งถ้าหลักใหนใช้เป็น * จะแปลว่าไม่สนใจในหลักนั้น

ตัวอย่าง เช่นถ้าต้องการรันคำสั่งทุก ๆ วันจันทร์ เวลา 02.30 จะตั้งเป็น  
<table class="table table-bordered">
         <td>
            # 30 02 * * 1   root  tar zcvf /var/log/messege
         </td>
</table>

ต้องการรันคำสั่งทุก ๆ วันที่ 12 ของเดือน เวลา 12.12 จะตั้งเป็น  
<table class="table table-bordered">
         <td>
            # 12 12 12 * *   root   tar jcvf  /home
         </td>
</table>

ซึ่งรูปแบบข้างต้นนั้นจะเป็นการเพิ่มเข้าไปใน crontab โดยตรง ซึ่งจริง ๆ แล้วนั้น cron นั้นได้เตรียม script ที่จะรัน cron พื้นฐานไว้ให้แล้ว เช่น cron.daily , cron.monthly , cron.hourly  ซึ่งจะอยู่ใน /etc ซึ่งเราสามารถเขียนไฟล์สคริปต์คำสั่งไปวางใน directory เหล่านี้เพื่อให้รันอัตโนมัติตามที่ตั้งเวลาไว้   แต่ถ้าต้องการตั้งเวลาในการรันอัตโนมัติเองนั้น หรือถ้าเป็น normal user ต้องการใช้งาน cron เราสามารถใช้งานได้โดยใช้คำสั่ง crontab -e ซึ่งการเขียน cron จะต่างกับการเขียนลง crontab โดยตรงเล็กน้อยคือ ไม่ต้องระบุชื่อ user ที่รัน ส่วนอื่น ๆ จะเหมือนกัน
<table class="table table-bordered">
         <td>
            # * * * * *     < command >
         </td>
</table>

ตัวอย่าง เช่น
ถ้าต้องการรันคำสั่งทุก ๆ วันจันทร์ เวลา 02.30 จะตั้งเป็น  
<table class="table table-bordered">
         <td>
            # 30 02 * * 1    tar zcvf /var/log/messege 
         </td>
</table>
