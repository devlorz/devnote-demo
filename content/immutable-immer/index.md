---
title: "Immutable ง่ายๆ ด้วย immer"
description: "Immutable ถือว่าเป็นหลักการสำคัญ โดยเฉพาะเวลาการอัพเดท State ใน Redux ในวันนี้จะมาแนะนำ Library ตัวใหม่ที่ชื่อว่า immer…"
date: "2020-01-31T17:16:26.507Z"
categories: []
published: false
---

Immutable ถือว่าเป็นหลักการสำคัญ โดยเฉพาะเวลาการอัพเดท State ใน Redux ในวันนี้จะมาแนะนำ Library ตัวใหม่ที่ชื่อว่า immer ซึ่งจะมาช่วยให้เราทำ Immutable ง่ายขึ้นครับ

### สารบัญ

-   Immutable คืออะไร
-   แนะนำ immer
-   ตัวอย่างการใช้งาน immer
-   สรุป

### Immutable คืออะไร

Immutable มาจากคำว่า Im(ไม่) + mutable(เปลี่ยนแปลง) รวมกันจึงแปลว่าไม่เปลี่ยนแปลงนั่นเอง แต่ว่าอะไรล่ะที่ไม่เปลี่ยนแปลง คำตอบก็คือ Object ครับ จาก Wikipedia ให้นิยามคำว่า Immutable Object ไว้ดังนี้

> an immutable object (unchangeable object) is an object whose state cannot be modified after it is created. This is in contrast to a mutable object (changeable object), which can be modified after it is created.

แปลเป็นไทยง่ายๆก็คือ Immutable Object หลังจากถูกสร้างแล้ว State ของ Object จะไม่มีการเปลี่ยนแปลง ซึ่งตรงข้ามกับ Mutable Object ซึ่งจะมีการเปลี่ยนแปลงของ State ของ Object หลังจากที่สร้างแล้วครับ อธิบายแบบนี้อาจจะงงไปดูตัวอย่างกันดีกว่า

จากตัวอย่างด้านบนจะเห็นว่าเราสร้างตัวแปรที่ชื่อว่า hero จากนั้นสร้างตัวแปรใหม่ที่มีชื่อว่า anotherHero แล้วทำการเปลี่ยนค่า จะเห็นว่าการเปลี่ยนค่าตัวแปร anotherHero ส่งผลให้ตัวแปร hero เปลี่ยนแปลงตาม 

จะเห็นว่าจากด้านบนถ้าเรา Mutate State ตรงๆอาจส่งผลให้เกิด Bug ขึ้นได้ ถ้าเราไม่อยากให้เกิดเหตุการณ์แบบด้านบนต้องทำยังไง คำตอบคือต้องใช้วิธี Immutable ครับ

จากโค้ดด้านบน แทนที่เราจะทำการ Mutate State ตรงๆ เราก็ใช้ Spread Syntax เพื่อสร้าง Object ขึ้นมาใหม่แทน ด้วยวิธีนี้จะทำให้ Object hero ไม่โดนเปลี่ยนค่า (Mutate) แน่นอนครับ

ส่วนตัวแปรประเภท Array ใน JavaScript นั้นมี Method ที่เป็น Immutable (Return เป็น Array ใหม่แทนที่จะ Mutate Array ตัวเก่า) ได้แก่ `map` , `filter` เป็นต้น

สำหรับการใช้งาน Immutable นั้นที่เห็นใช้กันบ่อยก็น่าจะเป็นใน Reducer ของ Redux ครับ

### แนะนำ immer

  

### ตัวอย่างการใช้งาน immer

#### Redux

#### NGRX

#### NGXS

#### AKITA

### สรุป

### อ้างอิง

[**Introducing Immer: Immutability the easy way**  
_Immutable, structurally shared data structures are a great paradigm for storing state. Especially when combined with an…_hackernoon.com](https://hackernoon.com/introducing-immer-immutability-the-easy-way-9d73d8f71cb3 "https://hackernoon.com/introducing-immer-immutability-the-easy-way-9d73d8f71cb3")[](https://hackernoon.com/introducing-immer-immutability-the-easy-way-9d73d8f71cb3)

[**mweststrate/immer**  
_Create the next immutable state by mutating the current one - mweststrate/immer_github.com](https://github.com/mweststrate/immer "https://github.com/mweststrate/immer")[](https://github.com/mweststrate/immer)

[**Immutability in React and Redux: The Complete Guide**  
_Immutability can be a confusing topic, and it pops up all over the place in React, Redux, and JavaScript in general…_daveceddia.com](https://daveceddia.com/react-redux-immutability-guide/ "https://daveceddia.com/react-redux-immutability-guide/")[](https://daveceddia.com/react-redux-immutability-guide/)

[**Immutable Data with Immer and React setState**  
_In this lesson we'll show the traditional method of updating state with a spread operator and then transform it into…_codedaily.io](https://codedaily.io/tutorials/58/Immutable-Data-with-Immer-and-React-setState "https://codedaily.io/tutorials/58/Immutable-Data-with-Immer-and-React-setState")[](https://codedaily.io/tutorials/58/Immutable-Data-with-Immer-and-React-setState)

[**Clean NgRx reducers using Immer**  
_Declutter your reducers with Immer_blog.angularindepth.com](https://blog.angularindepth.com/clean-ngrx-reducers-using-immer-7fe4a0d43508 "https://blog.angularindepth.com/clean-ngrx-reducers-using-immer-7fe4a0d43508")[](https://blog.angularindepth.com/clean-ngrx-reducers-using-immer-7fe4a0d43508)
