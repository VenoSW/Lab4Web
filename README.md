# Praktikum 4 - Pemrograman Web
```
Veno Setyoaji Wiratama
311910363
TI.19.A.2
Universitas Pelita Bangsa
```

## LANGKAH 1
### Membuat dokumen HTML dengan nama file lab4_box.html. Setelah itu buat struktur dasar HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Box Element</title>
</head>
<body>
  <header>
    <h1>Box Element</h1>
  </header>
</body>
</html>
```
![LANGKAH 1 membuat dokumen](https://user-images.githubusercontent.com/22215113/115274283-b0d0a080-a16a-11eb-9332-c3248a7e61a0.png)

## LANGKAH 2
### Membuat box element dengan tag div
```
<section>
  <div class="div1">Div 1</div>
  <div class="div2">Div 2</div>
  <div class="div3">Div 3</div>
</section>
```
![LANGKAH 2 membuat box element](https://user-images.githubusercontent.com/22215113/115274297-b3cb9100-a16a-11eb-8d7d-4a8bfacc2adf.png)

## LANGKAH 3
### Tambahkan deklarasi CSS pada head untuk membuat float element
```
<style>
        div {
            float:left;
            padding: 10px;
        }
        .div1 {
            background: red;
        }
        .div2 {
            background: yellow;
        }
        .div3 {
            background: green;
        }
        .div4 {
            background-color: blue;
            clear: left;
            float: none;
        }
</style>
```
![LANGKAH 3 tambahkan deklarasi CSS pada head untuk membuat float element](https://user-images.githubusercontent.com/22215113/115274318-b7f7ae80-a16a-11eb-9e60-be68202d0c0a.png)

## LANGKAH 4
### Mengatur Clearfix Element. Clearfix digunakan untuk mengatur element setelah float element
* Tambahkan element div lainnya seteleah div3
```
<section>
  <div class="div1">Div 1</div>
  <div class="div2">Div 2</div>
  <div class="div3">Div 3</div>
  <div class="div4">Div 4</div>
</section>

```
* Kemudian atur property clear pada CSS
```
.div4 {
  background-color: blue;
  clear: left;
  float: none;
}
```
![LANGKAH 4 Mengatur Clearfix Element](https://user-images.githubusercontent.com/22215113/115274344-be862600-a16a-11eb-96c3-0b47bee7ab05.png)

# Membuat Layout Sederhana
## LANGKAH 1
* Buat folder baru dengan nama `lab4_layout`, kemudian buatlah file baru didalamnya dengan nama `home.html`, dan file css dengan nama `style.css`.
![folder layout sederhana](https://user-images.githubusercontent.com/22215113/115270566-a14f5880-a166-11eb-83e1-ddcf381f2390.png)

* Kemudian coding `home.html`
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Layout Sederhana</h1>
        </header>
        <nav>
            <a href="home.html" class="active">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>
        <section id="hero"></section>
        <section id="wrapper">
            <section id="main"></section>
            <aside id="sidebar"></aside>
        </section>
        <footer>
            <p>&copy; 2021 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```

* dan coding pada `style.css`
```
/* import google font */
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');

/* Reset CSS */
* {
    margin: 0;
    padding: 0;
}
body {
    line-height:1;
    font-size:100%;
    font-family:'Open Sans', sans-serif;
    color:#5a5a5a;
}
#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #cccccc;
}

/* header */
header {
    padding: 20px;
}
header h1 {
    margin: 20px 10px;
    color: #b5b5b5;
}
```
![LANGKAH 5 membuat html dan css baru untuk layout (coding)](https://user-images.githubusercontent.com/22215113/115271004-17ec5600-a167-11eb-9e41-76c7805138dc.png)
* Buka file `home.html` pada web browser
![LANGKAH 5 membuat html dan css baru untuk layout](https://user-images.githubusercontent.com/22215113/115271087-29356280-a167-11eb-9767-81f71710cb6a.png)

## LANGKAH 2
## Mengatur Navigasi pada CSS
```
/* navigasi */
nav {
    display: block;
    background-color: #1f5faa;
}
nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    font-size: 14px;
    text-decoration: none;
    font-weight: bold;
}
nav a.active,
nav a:hover {
    background-color: #2b83ea;
}
```
![LANGKAH 6 membuat navigasi](https://user-images.githubusercontent.com/22215113/115271614-b5e02080-a167-11eb-982b-1f5f950965f3.png)

## LANGKAH 2
## Membuat Hero Panel
* Tambahkan Coding pada `home.html`
```
<section id="hero">
    <h1>Hello World!</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
    <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
```

* Tambahkan Coding pada `style.css`
```
/* Hero Panel */
#hero {
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
}
#hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
}
#hero p {
    margin-bottom: 20px;
    font-size: 18px;
    line-height: 25px;
}
```
![LANGKAH 7 membuat hero panel (coding)](https://user-images.githubusercontent.com/22215113/115271921-0b1c3200-a168-11eb-8e94-7acf6574d38b.png)
* Hasilnya
![LANGKAH 7 membuat hero panel](https://user-images.githubusercontent.com/22215113/115271866-fc357f80-a167-11eb-8bd8-9d6c2016df07.png)

## LANGKAH 3
## Mengatur Layout Main dan Sidebar
* Tambahkan coding pada `style.css`
```
/* main content */
#wrapper {
    margin: 0;
}
#main {
    float: left;
    width: 640px;
    padding: 20px;
}

/* sidebar area */
#sidebar {
    float: left;
    width: 260px;
    padding: 20px;
}
```
![LANGKAH 8 mengatur main layout dan sidebar](https://user-images.githubusercontent.com/22215113/115272131-43237500-a168-11eb-9adc-6e9492b36602.png)

## LANGKAH 4
## Membuat Sidebar Widget
* Tambahkan Coding pada `home.html`
```
<aside id="sidebar">
    <div class="widget-box">
        <h3 class="title">Widget Header</h3>
        <ul>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
       </ul>
    </div>
    <div class="widget-box">
       <h3 class="title">Widget Text</h3>
       <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
pharetra est nunc, nec pretium nunc pretium ac.</p>
   </div>
</aside>
```

* Tambahkan Coding pada `style.css`
```
/* widget */
.widget-box {
    border:1px solid #eee;
    margin-bottom:20px;
}
.widget-box .title {
    padding:10px 16px;
    background-color:#428bca;
    color:#fff;
}
.widget-box ul {
    list-style-type:none;
}
.widget-box li {
    border-bottom:1px solid #eee;
}
.widget-box li a {
    padding:10px 16px;
    color:#333;
    display:block;
    text-decoration:none;
}
.widget-box li:hover a {
    background-color:#eee;
}
.widget-box p {
    padding:15px;
    line-height:25px;
}
```
![LANGKAH 9 membuat sidebar widget (coding)](https://user-images.githubusercontent.com/22215113/115272508-aca38380-a168-11eb-81df-4fe2834f1933.png)
* Hasilnya
![LANGKAH 9 membuat sidebar widget](https://user-images.githubusercontent.com/22215113/115272539-b4632800-a168-11eb-8cd5-58a5a506089b.png)

## LANGKAH 5
## Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer
```
/* footer */
footer {
    clear:both;
    background-color:#1d1d1d;
    padding:20px;
    color:#eee;
}
```
![LANGKAH 10 mengatur footer](https://user-images.githubusercontent.com/22215113/115272643-d6f54100-a168-11eb-8885-ce8a1735cb96.png)

## LANGKAH 6
## Menambahkan Elemen lainnya pada Main Content
* Tambahkan Coding pada `home.html`
```
<section id="main">
    <div class="row">
        <div class="box">
            <img src="https://dummyimage.com/120/db7d25/fff.png" alt=""
class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
euismod.</p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
        <div class="box">
            <img src="https://dummyimage.com/120/3e73e6/fff.png" alt=""
class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
euismod.</p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
        <div class="box">
            <img src="https://dummyimage.com/120/71e6d4/fff.png" alt=""
class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
euismod.</p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
    </div>
</section>
```

* Tambahkan Coding pada `style.css`
```
/* box */
.box {
    display:block;
    float:left;
    width:33.333333%;
    box-sizing:border-box;
    -moz-box-sizing:border-box;
    -webkit-box-sizing:border-box;
    padding:0 10px;
    text-align:center;
}
.box h3 {
    margin: 15px 0;
}
.box p {
    line-height: 20px;
    font-size: 14px;
    margin-bottom: 15px;
}
box img {
    border: 0;
    vertical-align: middle;
}
.image-circle {
    border-radius: 50%;
}
.row {
    margin: 0 -10px;
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
}
.row:after, .row:before,
.entry:after, .entry:before {
    content:'';
    display:table;
}
.row:after,
.entry:after {
    clear:both;
}
```
![LANGKAH 11 Menambahkan Elemen lainnya pada Main Content (coding)](https://user-images.githubusercontent.com/22215113/115273030-3f442280-a169-11eb-9cf1-d3c392fdc2c0.png)
* Hasilnya
![LANGKAH 11 Menambahkan Elemen lainnya pada Main Content](https://user-images.githubusercontent.com/22215113/115273125-5edb4b00-a169-11eb-99ef-f830b673b08f.png)

## LANGKAH 7
## Selanjutnya membuat content artikel
* Tambahkan Coding pada `home.html`
```
<hr class="divider" />
<article class="entry">
    <h2>First featurette heading.</h2>
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
</article>
<hr class="divider" />
<article class="entry">
    <h2>First featurette heading.</h2>
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt=""
class="right-img">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
</article>

```
* Tambahkan Coding pada `style.css`
```
.divider {
    border:0;
    border-top:1px solid #eeeeee;
    margin:40px 0;
}
/* entry */
   .entry {
    margin: 15px 0;
}
   .entry h2 {
    margin-bottom: 20px;
}
.entry p {
    line-height: 25px;
}
.entry img {
    float: left;
    border-radius: 5px;
    margin-right: 15px;
}
.entry .right-img {
    float: right;
}
```
![LANGKAH 12 Menambahkan Content Artikel (coding)](https://user-images.githubusercontent.com/22215113/115273318-9813bb00-a169-11eb-92c7-d3b72b3c13dc.png)
* Hasilnya
![LANGKAH 12 Menambahkan Content Artikel](https://user-images.githubusercontent.com/22215113/115273353-a19d2300-a169-11eb-9b0d-c59da4fa950c.png)

## TUGAS
### 1. Tambahkan Layout untuk menu About

* Buat file HTML baru dengan nama `about.html`, dan buat single layout yang berisi deskripsi, portfolio, dll
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Me</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>About Me</h1>
        </header>
        <nav>
            <a href="home.html" class="active">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>
        <section id="about">
            <div class="row">
                <img src="venosw.JPG" title="Veno Setyoaji Wiratama" alt="Veno Setyoaji Wiratama" class="image-circle" width="200" style="float: left; border: 2px solid black;">
                <h1>Veno Setyoaji Wiratama</h1>
                <p>Nama saya Veno Setoaji Wiratama, Saya adalah seorang mahasiswa Universitas Pelita Bangsa Jurusan Teknik Informatika. Saya lahir di Pemalang, 8 April 2001.
                </p>
            </div>
        </section>
    </div>
</body>
</html>
```

* Tambahkan Coding pada `style.css`
```
/* About Panel */
#about{
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
}
#about h1 {
    margin-bottom: 10px;
    font-size: 35px;
    position: relative;
    left: 15px;
}
#about p {
    margin-bottom: 20px;
    font-size: 18px;
    padding: 30px;
    line-height: 25px;
    position: relative;
    left: 15px;
}
```
![About (coding)](https://user-images.githubusercontent.com/22215113/115273738-1f612e80-a16a-11eb-9bb3-3a7c0c2ef05c.png)

* Hasilnya
![About](https://user-images.githubusercontent.com/22215113/115273777-29832d00-a16a-11eb-8cec-e5c4d1d4da61.png)

### 2. Tambahkan layout untuk menu Contact

* Buat file HTML baru dengan nama `kontak.html`, dan buat form yang berisi: nama, email, message, dll
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Contact Me</h1>
        </header>
        <nav>
            <a href="home.html" class="active">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>
        <section id="kontak">
            <div class="login">
                <input type="text" placeholder="Your Name" class="input">
                <input type="text" placeholder="Your Email Address" class="input">
            </div>

            <div class="subject">
                <input type="text" placeholder="Subject" class="input">
            </div>

            <div class="msg">
                <textarea cols="35" rows="10" class="area" placeholder="Your Message" class="input"></textarea>
            </div>

            <button type="submit"> Send </button>

        </section>
    </div>
</body>
</html>
```

* Tambahkan Coding pada `style.css`
```
/* Kontak Panel */
#kontak{
    background-color: #e4e4e5;
    padding: 20px 20px;
    margin-bottom: 20px;
}
.input,
.msg, .area{
    width: 100%;
    padding: 10px;
    border: 2px solid white;
    box-sizing: border-box;
    font-size: 15px;
    margin-bottom: 20px;
}
button{
    font-size: 14px;
    background-color: #3f3f3f;
    color: white;
    border-radius: 5px;
    padding: 10px 20px;
    margin-top: 8x;
}
button :hover{
    opacity: 0,9;
}
```
![Kontak (coding)](https://user-images.githubusercontent.com/22215113/115274176-9a2a4980-a16a-11eb-970f-ca2d6fe6d1ad.png)

* Hasilnya
![Kontak](https://user-images.githubusercontent.com/22215113/115274198-a0b8c100-a16a-11eb-85ef-dfbef7a5be01.png)
