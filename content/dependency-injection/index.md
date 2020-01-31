---
title: "Dependency Injection คืออะไร"
description: "ตอนผมเขียนโปรแกรมใหม่ๆ เจอศัพท์คำว่า Dependency Injection แล้วค่อนข้างงงกับคำๆนี้ เลยจะลองเขียนสรุปง่ายๆตามที่เข้าใจดูละกัน"
date: "2017-03-12T15:58:05.369Z"
categories: []
published: true
canonical_link: https://medium.com/@leelorz6/dependency-injection-%E0%B8%84%E0%B8%B7%E0%B8%AD%E0%B8%AD%E0%B8%B0%E0%B9%84%E0%B8%A3-6a1a8a2996be
redirect_from:
  - /dependency-injection-คืออะไร-6a1a8a2996be
---

ตอนผมเขียนโปรแกรมใหม่ๆ เจอศัพท์คำว่า Dependency Injection แล้วค่อนข้างงงกับคำๆนี้ เลยจะลองเขียนสรุปง่ายๆตามที่เข้าใจดูละกัน

---

ก่อนจะมารู้จักกับ Dependency Injection เรามาแปลคำศัพท์ทีละคำกันก่อนดีกว่าครับ

> Dependency — something that is dependent on something else

คำว่า dependency หมายถึงสิ่งที่ขึ้นอยู่กับ(dependent)สิ่งอื่น โดยในทาง programming แล้ว object ที่เป็น dependency นั้น จะขึ้นอยู่กับ class อื่นๆ ซึ่งไม่ใช่ class ที่เราสนใจอยู่ เช่น dependency ของ service ที่ใช้ติดต่อ API ก็จะขึ้นอยู่กับ service ที่ใช้ติดต่อ API

```
class Login {
     
    String username;
    String password;

    // dependency
    AuthenService authenService = new AuthenService(username, password);

    ...

}
```

> Injection — the action of injecting

> Inject — introduce (a new or different element) into something

ส่วนคำว่า injection นั้นเป็น noun ของคำว่า inject ซึ่งแปลได้ว่า ฉีด(ยา) หรืออีกความหมายหนึ่งก็คือการนำบางอย่างเข้าสู่บางสิ่ง ซึ่งแปลง่ายๆได้ว่า การส่งต่อนั้นเอง

#### **ดังนั้น Dependency Injection ก็คือเทคนิคหนึ่งในการเขียนโปรแกรม โดยจะใช้การส่งต่อ (inject) ตัว dependency แทนการสร้าง dependency ขึ้นมาใหม่**

---

ลองมาดูตัวอย่าง code กันครับ

**แบบที่ไม่ใช้ Dependency Injection**

```
class WithOutDependencyInjection {
    
     Dependency dependency;

     WithOutDependencyInjection() {
         dependency = new Dependency();
     }
}
```

จะเห็นว่าเราจะสร้าง dependency ใหม่ขึ้นมาด้วยการ new object เลย

**แบบที่ใช้ Dependency Injection**

```
class WithDependencyInjection {

     Dependency dependency;

     WithDependencyInjection(Dependency dependency) {
         this.dependency = dependency;
     }
}
```

แบบนี้เราจะส่ง(inject) dependency ผ่าน constructor ของ class ซึ่งตัว class จะไม่ได้สร้าง dependency ด้วยตัวเอง

สำหรับการ inject นั้นมีหลายแบบ ตัวอย่างข้างบนใช้การ inject ผ่าน constructor นอกจากนั้นแล้วยังมีการ inject ผ่านทาง setter หรือทาง interface

---

### **ประโยชน์ของ Dependency Injection**

1.  **ลดการ couple(ผูกมัด) ของ code**

ถ้าเราใช้เทคนิค dependency injection แล้ว code ในส่วนของ dependency ก็จะไม่ผูกหรือขึ้นอยู่กับ class ของเรา ทำให้นำไปสู่ข้อต่อไป

2\. **ง่ายต่อการ test**

เมื่อ code ผูกมัดกัน(couple)น้อยลงแล้ว ทำให้เวลาเรา test สามารถ mock(จำลอง) ส่วนของ dependency ได้ จึงทำให้ง่ายต่อการเขียน test ครับ

---

_สำหรับบทความนี้ก็เป็นบทความแรกของผมนะครับ มีอะไรสามารถติชมได้นะครับ ขอบคุณครับ_

_Reference :_ [_Wikipedia_](https://en.wikipedia.org/wiki/Dependency_injection)
