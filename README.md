<div dir="rtl">

## تغيير الوان الموقع او اي خاصية كانت 

الطريقة جدا مميزة وسهله 

### الخطوات

انشاء متغيرات css داخل عنصر ``` root: ``` <br>

</div>

```css
:root {
    --primary: #8b5cf6; 
}

```
<div dir="rtl">
بعد ذالك ننشى input من نوع color
</div>

```html
<input type="color" id="primary-color" name="change-color" value="#8B5CF6"/>
```
<div dir="rtl">
طبعا اللون الاساسي في المثال هو

#8B5CF6

الان بعد هذا لنستخدم javascript لتغيير القيمة عند تغيير اللون في input
</div>

```javascript

document.querySelector('input[name="change-color"]')
.addEventListener('input', function(){
    let root = document.querySelector(":root");
    root.style.setProperty("--primary", this.value);
})

```

<div dir="rtl">
اول سطر هو لتحديد العنصر لقد حددناه عن طريق اسم الinput 

السطر الثاني عند تغيير لون input سوف ننفذ الكود في function closure

السطر الثالث واضح وهو تحديد root في css اللي خزنا داخله المتغيرات 
</div>


```javascript
let root = document.querySelector(":root");
```

<div dir="rtl">
واخر سطر غيرنا قيمة متغير primary الى القيمة الخاصة بـ input

طبعا الطريقة تنفع لكثير من خصائص الموقع



وبس والله. ✋
</div>
