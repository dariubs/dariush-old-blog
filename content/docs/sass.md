---
title: "آموزش  sass و scss"
date: 2018-01-12T20:01:20+03:30
authors: ["dariubs"]
draft: false
---

از زمانی شروع وب، استایل‌ها و نحوه‌ی نمایش المان‌ها در صفحات وبسایت‌ها یکی از جذابترین و البته چالشی‌ترین بخش‌های توسعه وب بوده است. زبان CSS از سال ۱۹۹۴ همراه وب بوده و در طول زمان تغییرات ساختاری اندک اما تغییرات بنیادی در پیاده سازی ها داشته است. تعداد زیادی از اتریبیوت‌های CSS معرفی و توسط مرورگرها پشتیبانی شده‌اند و از انیمیشن‌ها تا قالب‌بندی‌های پیچیده و بسیاری از بدیعیات توسط این ویژگی‌ها قابل پیاده سازی‌اند.

زبان CSS بسیار ساده است و ویژگی‌های ساختاری اندک آن، آن را به ساختاری ساده بدل کرده، اما همین ساختار ساده زمانی که در حجم بالای کدهای و تکرارهای زیاد کد و مشکلاتی ازین دست استفاده شود، کدی بزرگ و شلخته و با قابلیت کنترل پایین تولید میشود که شاید نگه‌داری و فهم آن بسیار دشوار و ملال آور باشد. ازین رو زبانهایی ایجاد شدند که ویژگی‌های مدرنی با خود دارند و امکانات زیادی را به دنیای CSS می‌آورند و البته به سادگی به CSS کامپایل می‌شوند. SASS یکی ازین زبانهاست و تقریبا پر استفاده‌ترین آنها.

## زبان SASS

زبان SASS یک زبان  برای تعریف استایل‌شیت‌های وب است که اولین بار در سال ۲۰۰۶ توسط همپتون کَتلین معرفی شد. این زبان ویژگی‌های زیادی را برای دنیای CSS قابل استفاده کرده است از جمله استفاده از متغیرها، ترکیب استایل‌ها، تکه تکه کردن کدها و ایمپورت، میکسین‌ها و استفاده از عملگرهای محاسباتی. 

برای استفاده از SASS نیاز دارید که ابتدا کامپایلر SASS را نصب کنید.


## نصب SASS

برای استفاده از زبان SASS دو راه پیش روی شماست، اول استفاده از اپلیکیشن‌های گرافیکی برای کامپایل SASS و راه دوم استفاده از برنامه خط فرمان SASS. کامپایلر زبان SASS به عنوان یک بسته‌ی نصبی روی روبی‌جمز قابل استفاده است. اما اگر قبلا تجربه کار با gemهای روبی را نداشته باشید ممکن است نصب این سیستم برای شما قدری چالشی باشد. 

### نصب اپ‌های کامپایل SASS

برای استفاده از یک محیط خط فرمان برای SASS میتوانید از برنامه‌های زیر استفاده کنید. بعضی ازین‌ها نسخه‌ی رایگان ندارند.

**برنامه [Codekit](https://codekitapp.com/index.html)**

سیستم‌عامل : macOS


**برنامه [Koala](http://koala-app.com/)**

سیستم‌عامل : لینوکس، ویندوز و مک


**برنامه [ScoutApp](http://scout-app.io/)**

سیستم‌عامل : لینوکس، ویندوز و مک


**برنامه [Compass.app](http://compass.kkbox.com/)**

سیستم‌عامل : لینوکس، ویندوز و مک


**برنامه [Ghostlab](http://www.vanamco.com/ghostlab/)**

سیستم‌عامل : ویندوز و مک


**برنامه [Hammer](https://hammerformac.com)**

سیستم‌عامل : مک


**برنامه [LiveReload](http://livereload.com)**

سیستم‌عامل : لینوکس، ویندوز و مک


## نصب واسط خط فرمان SASS از روی پکیج منیجر روبی

### نصب روبی روی لینوکس

اگر از یک توزیع لینوکس استفاده میکنید، ابتدا لازم است روبی را نصب کنید. شما میتوانید روبی را از روی APT، rvm یا rbenv نصب کنید. شما همچنین به بسته‌ی  build-essential نیاز دارید. پس از آن از روی پکیج منیجر ruby gems برنامه sass را با دستور زیر نصب کنید :


```bash
sudo gem install sass --no-user-install
```

### نصب روبی روی ویندوز

قبل ازینکه بخواهید SASS را نصب کنید باید روبی را نصب کرده باشید. سریعترین راه برای نصب روبی روی ویندوز استفاده از [Ruby Installer](http://rubyinstaller.org/) است. روبی اینستالر یک برنامه ساده است که با چند کلیک به سبک برنامه های ویندوز نصب می‌شود. بعد از نصب از طریق Powershell میتوانید به دستورات روبی دسترسی داشته باشید.

### نصب روبی روی مک

روی سیستم عامل macOS بصورت پیشفرض زبان روبی نصب شده است و نیاز به  نصب ندارد.

### نصب SASS روی واسط خط فرمان

برای نصب SASS از طریق ترمینال،  یک برنامه ترمینال باز کنید و دستور زیر را در آن اجرا کنید :

```bash
gem install sass

```

روی لینوکس اگر از طریق مدیر بسته ی سیستم عامل نصب کرده باشید ممکن است نیاز به استفاده از دستور `sudo` باشد.

برای بررسی صحت نصب هم دستور زیر را اجرا کنید :

```bash
sass -v
```

که در صورت نصب صحیح برنامه، ورژن SASS ایی که نصب کرده‌اید در صفحه پرینت می‌شود.

## ساختار زبان  SASS و تفاوت  Sass و SCSS

زبان CSS امکانات فراخی برای توسعه‌دهندگان ندارن و ساختاری ساده دارد. زبانهایی مانند SASS برای افزودن امکانات بیشتر برای توسعه دهندگان ایجاد شده اند. این زبانها امکاناتی برای تفاوت در خروجی ندارند و در نهایت به CSS کامپایل میشود و صرفا امکاناتی برای توسعه بهتر و سریعتر در اختیار کاربران خود قرار میدهند. مرورگرها صرفا CSS را درک و پشتیبانی و پردازش میکنند، پس برای استفاده از SASS خروجی این زبان باید قبل از استفاده به کد CSS تبدیل شوند. این همان کاریست که کامپایلر زبان SASS انجام میدهد : تبدیل SASS به  CSS.


استایل‌شیت‌های SASS به دو نوع ساختار ممکن است نوشته :

- ساختار Sass که در فایل‌هایی با پسوند `.sass` ذخیره می‌شوند
- ساختار SCSS که در فایل‌هایی با پسوند `.scss` ذخیره می‌شوند

در ادامه به توضیح مدل استفاده از هردوی اینها میپردازیم.

زبان CSS ساختار ساده ای دارد. نام سلکتور + { + تعریف ساختار در قالب یک کلید و یک مقدار مختومه به سمی کولن + } . مانند تصویر زیر : 

![CSS Selector](/img/guide/sass/selector.gif)

مثال زیر نمونه یک تکه کد CSS است :

```css
h1 {
    font-size: 2em;
}

.title {
    border: 2px solid black;
    font-family: iransans;
}
```

همانطور که میدانید، در ساختار CSS فضاهای خالی، رفتن به خط بعدی و رعایت کردن یا نکردنه ایندنت‌ها در تعریف مقادیر داخل سلکتور مساله‌ی خاصی ندارد. برای مثال کد بالا را میتوانیم به صورت زیر هم بنویسیم :

```css
h1{font-size: 2em;}

.title {border: 2px solid black;font-family: iransans;}
```

در بین دو ساختار **Sass** و **SCSS**، ساختار **SCSS** هم سینتکسی مشابه CSS دارد اما ساختار Sass قدری **متفاوت** است. در ساختار Sass بجای بلاک‌های محصور شده با دو علامت براکت، از تب و فضای خالی استفاده می‌شود. نمونه کد بالا در ساختار Sass بصورت زیر نوشته می‌شود :

```
h1
    font-size: 2em

.title
    border: 2px solid black
    font-family: iransans
 
```

در این ساختار نیاز به استفاده از سمی‌کولن (;) و براکت‌ها ( علامت } و { ) نیست و بجای آن تعریف هر مقدار برای سلکتور در یک خط جداگانه و البته با فاصله از سطح سلکتور به تعداد معینی تب یا اسپیس صورت میگیرد.

### استفاده عمده

در بین توسعه‌دهندگان نرم افزار و طراحان وب، ساختار SCSS ساختار جا افتاده‌ و پرکاربردیست و پروژه های بزرگی همچون گیتهاب از آن استفاده می‌کنند و عمدتا وقتی صحبت از زبان SASS میشود منظور ساختار SCSS آن است.


## ویژگی‌های SASS

زبان SASS ساده‌نویسی و قابلیت نگه‌داری و توسعه در آینده‌ی استایل‌شیت های پروژه ها را بالا میبرد و با استفاده از ویژگی‌های آن کدهایی ساختارمند و منظم‌تر میتوان نوشت. برخی از مهمترین ویژگی‌های SASS عبارتند از :

### قابلیت تعریف متغیر‌ها

همانند زبان‌های برنامه‌نویسی، در زبان SASS میتوانید متغیرهایی را تعریف کنید. اما چه کاربردی میتواند داشته باشد؟ فرض کنید شما یک رنگ سازمانی دارید یا یک رنگ موقت را برای پروژه‌تان انتخاب کرده اید و در جاهای مختلف در برنامه میخواهید آن را استفاده کنید، دو راه دارید : میتوانید در هر بخش یکبار کد آن رنگ را پیست کنید، یا میتوانید یک متغیر تعریف کنید و یک بار آن را مقدار دهی کنید و هرکجا که میخواهید آن را استفاده کنید. با این کار اگر نیاز به تغییر آن مقدار داشتید به سادگی میتوانید در آینده با تنها تغییر دادن مقدار اولیه آن را در تمام پروژه و بدون کار اضافه تغییر دهید. 

نام متغیرها با علامت $ شروع می‌شود و معمولا در بیرون بلاک‌های سلکتورهای پروژه تعریف میشوند. مانند تکه کد زیر :


```scss
$bg-color: #fff;
$primary-color: #333;

body {
  background-color: $bg-color;
  color: $primary-color;
}
```

### بلاک‌های تو در تو

در HTML دیده‌اید که تگ‌ها میتوانند بصورت تودرتو باشند. مثلا درون تگ h1 میتوانیم یک تگ a گذاریم و هر تگ دیگری هم همینطور. این ویژگی اما در CSS موجود نیست و برای نوشتن استایل‌های هر سلکتور باید یک بلاک جداگانه و بیرون از همه بلاکهای دیگر ایجاد و کدهایمان را درون آن بنویسیم. با SASS میتوانید درون استایل‌شیت‌هایتان هم بلاک‌های تو در تو داشته باشید :

```scss
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}

```

کد بالا اگر قرار بود در CSS پیاده شود بصورت زیر می‌شد :

```css
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

nav li {
  display: inline-block;
}

nav a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}
```

### ایمپورت کردن کدها

میتوانید استایل‌های تان را در قالب فایل‌های کوچک و ساده قرار دهید و با دستور import آنها را در استایل اصلی خود وارد کنید. این ویژگی قابلیت ماژولار کردن کدهایتان را به شما میدهد و میتوانید هرطور که تمایل دارید کدهایتان را مدیریت و دسته بندی کنید. 

**...ادامه دارد...**


