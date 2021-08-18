# Vue.js & Restful API Workshop

### Chapter 1: Setup Environment
1.	ขั้นตอนการติดตั้ง Node.js ลงบนเครื่อง <br>
  1.1.	ทำการดาวน์โหลดไฟล์ติดตั้งโปรแกรมจากเว็บไซต์ https://nodejs.org/en/

  <!-- ![](images/node1.jpg) -->
  <img src="images/node1.jpg" width=800>

  1.2.  เมื่อได้ไฟล์ดาวน์โหลดมาแล้วให้ดับเบิลคลิก เพื่อทำการติดตั้ง <br>
  1.3.	click ปุ่ม Next เพื่อดำเนินการติดตั้ง <br>
  
  <img src="images/node2.jpg" width=500>

  1.4.	ยอมรับข้อตกลงในการติดตั้ง โดยเลือกช่องว่างหน้าข้อความ I accept the term in the License Agreement แล้ว click ปุ่ม Next
  
  <img src="images/node3.jpg" width=500>
 
  1.5.	เลือกโฟลเดอร์ปลายทางของโปรแกรมที่ต้องการติดตั้ง โดยปกติจะใช้ค่าเริ่มต้นที่กำหนดให้ จากนั้นคลิกปุ่ม Next
  
  <img src="images/node4.jpg" width=500>
  
  1.6.	ตัวเลือกในการติดตั้ง โดยปกติจะใช้การตั้งค่าเริ่มต้น แล้วคลิกปุ่ม Next
  
  <img src="images/node5.jpg" width=500>
  
  1.7.	เมื่อเราตั้งค่าการติดตั้งเรียบร้อยแล้ว ก็ถึงเวลาในการติดตั้ง ให้คลิก ปุ่ม Install เพื่อติดตั้ง Node.js
  
  <img src="images/node6.jpg" width=500>
  
  รอการติดตั้งสักครู่
  
  <img src="images/node7.jpg" width=500>
  
  1.8.	การติดตั้งเสร็จสมบูรณ์แล้วให้ click ปุ่ม Finish
  
  <img src="images/node9.jpg" width=500>
  
ตรวจสอบการใช้งาน Node. js
  1.	คลิกที่ปุ่มค้นหา (หาก Windows ต่ำกว่า Version 10 ให้ใช้ปุ่ม Start > Run) พิมพ์ว่า Command Prompt หรือ cmd จากนั้นเลือก Command Prompt 
  2.	ทดสอบพิมพ์คำว่า node -v (คำสั่งตรวจสอบเวอร์ชั่นของ Node.js) โปรแกรมบจะแสดงเวอร์ชั่น ดังภาพ
    
  <img src="images/node10.jpg" width=500>
  
  
### Setup Device
Run command in cmd
```
npm install -g @vue/cli 
```
Run command in PowerShell (Run as Administrator)
```
npm install --global --production windows-build-tools 
```

### Project setup 
```
npm install
```

### Compiles and reloads for development
```
npm run serve
```

### Vue Create Project and Add Plugin
```
vue create restapiproject  
cd restapiproject
```
Add Vuetify and Router
```
vue add vuetify
vue add router
```
Create .eslintignore files
```
/build/**
/coverage/**
/docs/**
/jsdoc/**
/templates/**
/tests/bench/**
/tests/fixtures/**
/tests/performance/**
/tmp/**
/tools/internal-rules/node_modules/**
/lib/rules/utils/unicode/is-combining-character.js
test.js
!.eslintrc.js
/src/**
```
Add Axios
```
vue add axios
```

### Create API
```
npm install --save json-server
npm run json:server
```

### Create db.json file
```
Create a db.json file with some data

{
  "posts": [
    { "id": 1, "title": "json-server", "author": "typicode" }
  ],
  "comments": [
    { "id": 1, "body": "some comment", "postId": 1 }
  ],
  "profile": { "name": "typicode" }
}
```
### Start JSON Server

```
json-server --watch db.json
```
Now if you go to http://localhost:3000/posts/1, you'll get
  { "id": 1, "title": "json-server", "author": "typicode" }
  
### Routes
Based on the previous db.json file, here are all the default routes. You can also add other routes using --routes.
```
GET    /posts
GET    /posts/1
POST   /posts
PUT    /posts/1
DELETE /posts/1
```
