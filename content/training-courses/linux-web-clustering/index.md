---
title: 'Linux Web Clustering'
subID: '28'
date: 2019-06-23T10:06:54+07:00
draft: false
totalHours: 18
totalDays: 3
price: 10700
pdfURL: 'http://www.clusterkit.co.th/training/pdf/Linux%20Web%20Clustering.pdf'
---

## รายละเอียดของหลักสูตร

หลักสูตรนี้ กล่าวถึงหลักการทำงานของระบบเว็บคลัสเตอร์ ที่ใช้ในงานให้บริการเว็บไซต์สำหรับเว็บขนาดใหญ่เพื่อรองรับผู้ใช้งานจำนวนมาก เป็นหลักสูตรที่เน้นการปฎิบัติใช้งานจริง โดยเนื้อหาครอบคลุมตั้งแต่กระบวนการออกแบบ การติดตั้ง การสร้างระบบคงอยู่สูง (High Availability - HA) ทฤษฎีกระจายภาระงาน (Load balancing) ด้วย Linux Virtual Server (LVS) และ HAProxy การใช้ memcache ในการจัดการ session ข้ามเครื่อง การติดตั้งระบบไฟล์แบบกระจาย GlustreFS เพื่อให้ปรับปรุงไฟล์ทีเดียวแล้วกระจายสำเนาไปยังเว็บเซิร์ฟเวอร์ทุกเครื่อง การปรับแต่งความปลอดภัยของระบบ และมีการปรับพื้นฐานทฤษฎีระบบเครือข่ายในส่วนที่เกี่ยวข้องกับเว็บคลัสเตอร์ เช่น Mac Address, ARP Protocol, Public และ Private Network เป็นต้น

## หลักสูตรนี้เหมาะสำหรับ

ผู้ดูแลระบบเว็บ องค์กรที่ให้บริการเว็บ และผู้ที่สนใจ

## วัตถุประสงค์

1. เพื่อให้ผู้เข้าอบรมมีความรู้ความเข้าใจในหลักการออกแบบเว็บคลัสเตอร์
2. เพื่อให้ผู้เข้าอบรมทราบถึงความแตกต่างของวิธีการกระจายภาระงานในแบบต่าง ๆ
3. เพื่อให้ผู้เข้าอบรมสามารถนำไปประยุกต์ใช้งานได้จริง

## ความรู้พื้นฐาน

ผู้เข้าอบรมต้องมีความรู้ความสามารถในการติดตั้ง Linux Server หรือผ่านหลักสูตร Linux Administration มาก่อน และควรมีความเข้าใจเรื่องระบบเครือข่ายพื้นฐาน

## รูปแบบการสอน

บรรยายและปฏิบัติการ โดยใช้ระบบคอมพิวเตอร์แบบเสมือน (Virtual Machine) เพื่อต่อเป็นระบบคลัสเตอร์

## ซอฟต์แวร์ที่ใช้สอน

1. ระบบปฏิบัติการลีนุกซ์ CentOS-7

## เนื้อหาหลักสูตร

### วันที่ 1

#### เช้า

- รู้จักกับระบบเว็บคลัสเตอร์
- เว็บคลัสเตอร์คืออะไร
- รูปแบบการกระจายภาระงานของเว็บ (Web Load Balancing)
- DNS Round Robin
- Scale out
- Hardware Load Balancing
- Software Load Balancing
- สถาปัตยกรรมและหลักการออกแบบเว็บคลัสเตอร์
- ขั้นตอนการติดตั้งระบบปฏิบัติการ Linux
- **Workshop 1:** ประกอบคลัสเตอร์และติดตั้งระบบปฏิบัติการ Linux
- การตั้งค่า SSH ให้ทำงานแบบ Single Sign On with Public key Infrastructure (PKI)
- **Workshop 2:** ปรับแต่งการเชื่อมต่อภายในระบบคลัสเตอร์และทบทวนคำสั่งที่เกี่ยวข้อง

#### บ่าย

- ทบทวนความรู้ทฤษฎีระบบเครือข่ายในส่วนที่เกี่ยวข้องกับระบบเว็บคลัสเตอร์
- MAC Address
- ARP Protocol
- Public และ Private Network
- ทบทวนเรื่อง Web Server
- การทำงานของ Web Server
- Configuration ที่สำคัญของ Web Server
- การกระจายภาระงานด้วย Linux Virtual Server (LVS)
- รู้จักกับ Linux Virtual Server
- รู้จักกับ LVS Scheduling Algorithm ประเภทต่าง ๆ
- ทฤษฎีการกระจายภาระงาน (Load Balancing) เบื้องต้น
- การปรับแต่งเว็บคลัสเตอร์แบบ NAT
- การปรับแต่งเว็บคลัสเตอร์แบบ Direct Route
- หลักการของ Virtual IP
- MAC Spoofing
- การติดตั้งและใช้งาน arptable_jf เพื่อจัดการกับปัญหา MAC Address ในการทำงานของระบบเว็บคลัสเตอร์
- Piranha configuration tool
- **Workshop 3:** สร้างเว็บคลัสเตอร์แบบ NAT ด้วย Piranha GUI พร้อมทดสอบวิธีการกระจายแบบต่าง ๆ
- **Workshop 4:** สร้างเว็บคลัสเตอร์แบบ Direct Route ด้วย Piranha GUI พร้อมทดสอบวิธีการกระจายแบบต่าง ๆ

### วันที่ 2

#### เช้า

- การกระจายภาระงานด้วยซอฟต์แวร์ HAProxy
- **Workshop 5:** การติดตั้งใช้งาน HAProxy
- เปรียบเทียบการทำงานระหว่า HAProxy และ LVS
- การทำระบบภาวะทนต่อความผิดพร่องสูง
- หลักการทำงานแบบ High Availability (HA) ของ Load Balancer
- การสร้างระบบ High Availability สำหรับระบบ Web Cluster
- **Workshop 6:** สร้างระบบ High Availability สำหรับระบบเว็บคลัสเตอร์ พร้อมทดสอบการทำงาน

#### บ่าย

- วิธีการจัดการไฟล์เว็บในรูปแบบต่าง ๆ เพื่อความสะดวกในการ Update ข้อมูลที่เดียว
- ความแตกต่างระหว่าง Share Disk และ Share Storage
- Network File System (NFS), ISCSI, GlusterFS (60 min)
- ISCSI รูปแบบใช้ เพื่อให้ทุกเครื่องเห็นที่เดียวกัน
- **Workshop 7:** การสร้าง Share Directory บน NFS และการทำ Auto mount
- รู้จักกับ GlusterFS
- การทำงานของ GlusterFS ในรูปแบบต่าง ๆ
- องค์ประกอบของเครื่องในระบบ
- **Workshop 8:** การติดตั้งและใช้งาน GlusterFS แบบ Replication (3 เครื่อง)การรักษาความปลอดภัยของระบบ (100 min)

### วันที่ 3

#### เช้า

- รู้จักกับ Memcache
- **Workshop 9:** การใช้งาน Memcache ในการจัดการ session ภายในคลัสเตอร์
- แนะนำ Ganglia ระบบ Web Monitoring tools
- **Workshop 10:** ติดตั้งระบบ Web Monitoring
- การปรับแต่งประสิทธิภาพ
- การทดลองยิงโหลดด้วย awk
- วางแผนการรับโหลด

#### บ่าย

- การปรับแต่งประสิทธิภาพ(ต่อ)
- การปรับแต่ระบบปฏิบัติการเพื่อรองรับภาระงานที่เพิ่มขึ้น
- การใช้งาน MySQLTuner เพื่อปรับแต่งประสิทธิภาพให้ MySQL
- แนะนำระบบฐานข้อมูลแบบกระจายในแบบต่าง ๆ เช่น MarieDB Galera Cluster, MySQL Cluster