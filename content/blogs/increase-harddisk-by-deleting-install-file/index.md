---
title: 'เพิ่มพื้นที่ฮาร์ดดิสก์ด้วยการลบไฟล์ติดตั้งทิ้ง'
date: 2010-08-30T14:59:02+07:00
draft: false
---
ช่วงนี้ผมประสบปัญหาฮาร์ดดิสก์ใกล้จะเต็ม จนมีข้อความเตือนขึ้นมาบ่อยครั้ง เพราะพาร์ทิชั่นที่ผมแบ่งไว้สำหรับรูท / เริ่มไม่พอต่อการใช้งาน (ผมแบ่งไว้ 6GB) จนทำให้ต้องหาวิธีลบไฟล์ที่ไม่จำเป็นออก หนึ่งในนั้นคือไฟล์ .deb ที่อูบันตูโหลดมาวางไว้เวลาที่เราติดตั้งโปรแกรมเพิ่มเติมผ่าน apt-get นั่นแหละ
ตำแหน่งของไฟล์ที่ถูกโหลดมาวางไว้ก่อนจะติดตั้งอยู่ที่ /var/cache/apt/archives ลองเข้าไปดู ท่านจะพบไฟล์ .deb อยู่หลายไฟล์ ถ้าคนไหนอัพเกรดบ่อย ลงโปรแกรมเพิ่มเยอะ เข้าใจว่าจะมีไฟล์วางอยู่ในไดเรกทอรีนี้เยอะตาม ซึ่งอาจจะกินพื้นที่ไปหลายเมกะไบต์หรืออาจจะเป็นกิ๊กกะไบต์กันเลยทีเดียว <br>
วิธีการลบไฟล์ในไดเรกทอรีนี้นั้น ท่านไม่ควรใช้คำสั่งลบไฟล์ตรง ๆ  แต่ควรจะใช้คำสั่งดังต่อไปนี้
<table class="table table-bordered">
      <td>
        $ sudo apt-get clean
      </td>
</table>
เพียงเท่านี้ เราก็จะได้พื้นที่ว่างอีกส่วนหนึ่งคืนกลับมาแล้วครับ