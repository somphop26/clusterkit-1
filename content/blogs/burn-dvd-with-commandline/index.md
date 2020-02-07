---
title: 'เขียนแผ่นดีวีดีด้วย command-line บนลีนุกซ์'
date: 2010-04-23T15:00:32+07:00
draft: false
---
อดีตเรานิยมใช้คำสั่ง cdrecord ในการเขียนแผ่นซีดีทั่วไป แต่ในระยะหลังเรามักจะพบปัญหาในการเขียนแผ่นดีวีดี ด้วยคำสั่งดังกล่าว วันนี้ ClusterKit  จะมาแนะนำท่านให้รู้จักกับอีกหนึ่งคำสั่งที่จะทำให้เราสามารถเขียนแผ่นดีวีดีจากไฟล์ ISO ได้ครับ

คำสั่ง growisofs เป็นคำสั่งที่ใช้สร้างและเขียนไฟล์ ISO โดยเฉพาะ สำหรับวิธีการเขียนกับแผ่นดีวีดีนั้น ก็เพียงแค่สั่งง่าย ๆ ในรูปแบบดังต่อไปนี้
   <table class="table table-bordered">
         <td>
            # growisofs -dvd-compat -Z /dev/dvd=dvd.iso
         </td>
   </table>

จากตัวอย่างข้างต้น ก็คือเราต้องการจะเขียนไฟล์ dvd.iso ลงแผ่นดีวีดี นั่นเองครับ  

เห็นไหมล่ะง่ายนิดเดียวเอง ลองดูนะครับแล้วได้ผลอย่างไรก็แจ้งกันมาบ้างนะครับ ^^