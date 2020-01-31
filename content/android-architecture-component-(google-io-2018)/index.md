---
title: "มีอะไรใหม่ใน Android Architecture Component (Google I/O 2018)"
description: "หลังจากปีที่แล้ว Google ได้ประกาศ Architecture Component ออกมาเพื่อให้เหล่า Android Developer มีตัวช่วยในการเขียน Android App ได้ง่ายขึ้น…"
date: "2020-01-31T17:17:48.331Z"
categories: []
published: false
---

หลังจากปีที่แล้ว Google ได้ประกาศ Architecture Component ออกมาเพื่อให้เหล่า Android Developer มีตัวช่วยในการเขียน Android App ได้ง่ายขึ้น _ใครยังไม่รู้ว่า Architecture Component คืออะไร ดูได้จากบล็อคด้านล่างเลยจ้า_

[**รู้จัก Architecture Component ของใหม่จาก Google ที่จะมาช่วยจัดการ project ของคุณ**  
_ท่ามกลางกระแสชื่นชมที่ Kotlin ได้ถูกบรรจุเป็นภาษาทางการของ Android มีอีกเรื่องหนึ่งที่น่าสนใจไม่แพ้กันนั่นก็คือ…_medium.com](https://medium.com/@leelorz6/%E0%B8%A3%E0%B8%B9%E0%B9%89%E0%B8%88%E0%B8%B1%E0%B8%81-architecture-component-%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B9%83%E0%B8%AB%E0%B8%A1%E0%B9%88%E0%B8%88%E0%B8%B2%E0%B8%81-google-%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%88%E0%B8%B0%E0%B8%A1%E0%B8%B2%E0%B8%8A%E0%B9%88%E0%B8%A7%E0%B8%A2%E0%B8%88%E0%B8%B1%E0%B8%94%E0%B8%81%E0%B8%B2%E0%B8%A3-project-%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%84%E0%B8%B8%E0%B8%93-85e48a6b8ff8 "https://medium.com/@leelorz6/%E0%B8%A3%E0%B8%B9%E0%B9%89%E0%B8%88%E0%B8%B1%E0%B8%81-architecture-component-%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B9%83%E0%B8%AB%E0%B8%A1%E0%B9%88%E0%B8%88%E0%B8%B2%E0%B8%81-google-%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%88%E0%B8%B0%E0%B8%A1%E0%B8%B2%E0%B8%8A%E0%B9%88%E0%B8%A7%E0%B8%A2%E0%B8%88%E0%B8%B1%E0%B8%94%E0%B8%81%E0%B8%B2%E0%B8%A3-project-%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%84%E0%B8%B8%E0%B8%93-85e48a6b8ff8")[](https://medium.com/@leelorz6/%E0%B8%A3%E0%B8%B9%E0%B9%89%E0%B8%88%E0%B8%B1%E0%B8%81-architecture-component-%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B9%83%E0%B8%AB%E0%B8%A1%E0%B9%88%E0%B8%88%E0%B8%B2%E0%B8%81-google-%E0%B8%97%E0%B8%B5%E0%B9%88%E0%B8%88%E0%B8%B0%E0%B8%A1%E0%B8%B2%E0%B8%8A%E0%B9%88%E0%B8%A7%E0%B8%A2%E0%B8%88%E0%B8%B1%E0%B8%94%E0%B8%81%E0%B8%B2%E0%B8%A3-project-%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%84%E0%B8%B8%E0%B8%93-85e48a6b8ff8)

ในปีนี้ Google Architecture Component ถูกรวมไปใน Jetpack เรียบร้อยแล้ว (_Jetpack คืออะไรอ่านได้จาก_[_บล็อคนี้_](https://nuuneoi.com/blog/blog.php?read_id=940)) โดย Architecture Component มาพร้อม Component ใหม่ๆ ที่จะเข้ามาเสริมทัพ Architecture Component ที่มีอยู่แล้วให้ดียิ่งขึ้นไปอีก มาดูกันดีกว่าว่ามี Component อะไรเข้ามาใหม่บ้าง

### อ้างอิง
