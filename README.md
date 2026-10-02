<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>موقعي</title>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #eef1f5;
  color: #222;
}

/* العنوان */
header {
  background: #17324d;
  color: white;
  text-align: center;
  padding: 25px;
}

/* التبويبات */
nav {
  background: white;
  padding: 12px;
  display: flex;
  gap: 8px;
  justify-content: center;
  flex-wrap: wrap;
  position: sticky;
  top: 0;
  z-index: 10;
  box-shadow: 0 2px 8px #0002;
}

nav button {
  border: 0;
  padding: 12px 17px;
  border-radius: 8px;
  background: #e4e8ed;
  cursor: pointer;
  font-size: 15px;
}

nav button:hover,
nav button.active {
  background: #17324d;
  color: white;
}

/* الأقسام */
section {
  display: none;
  max-width: 1200px;
  margin: auto;
  padding: 30px 20px;
}

section.active {
  display: block;
}

/* معرض الصور */
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 18px;
}

.gallery img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  border-radius: 12px;
  cursor: pointer;
  transition: 0.2s;
}

.gallery img:hover {
  transform: scale(1.03);
}

/* البث */
.live {
  background: white;
  padding: 60px 20px;
  text-align: center;
  border-radius: 15px;
}

/* تكبير الصورة */
#viewer {
  display: none;
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,.9);
  z-index: 100;
  align-items: center;
  justify-content: center;
}

#viewer img {
  max-width: 95%;
  max-height: 90%;
  border-radius: 10px;
}

#close {
  position: absolute;
  top: 15px;
  right: 25px;
  color: white;
  font-size: 45px;
  cursor: pointer;
}

/* الموبايل */
@media(max-width:600px) {

  nav {
    justify-content: flex-start;
    overflow-x: auto;
    flex-wrap: nowrap;
  }

  nav button {
    white-space: nowrap;
  }

  .gallery {
    grid-template-columns: 1fr 1fr;
  }

  .gallery img {
    height: 160px;
  }
}
</style>
</head>

<body>

<header>
  <h1>معرض الصور</h1>
</header>

<nav>

<button class="active" onclick="showTab('home',this)">
الرئيسية
</button>

<button onclick="showTab('nature',this)">
صور طبيعة
</button>

<button onclick="showTab('wallpapers',this)">
صور خلفيات
</button>

<button onclick="showTab('cities',this)">
صور مدن
</button>

<button onclick="showTab('sunrise',this)">
غروب وشروق
</button>

<button onclick="showTab('night',this)">
صور ليلية
</button>

<button onclick="showTab('misc',this)">
صور متنوعة
</button>

<button onclick="showTab('live',this)">
البث المباشر
</button>

</nav>

<section id="home" class="active">

<h2>أهلاً وسهلاً 👋</h2>

<p>
مرحباً بك في موقعي الخاص بالصور والبث المباشر.
</p>

</section>


<section id="nature">

<h2>🌳 صور الطبيعة</h2>

<div class="gallery">

<img src="https://picsum.photos/600/400?random=1">
<img src="https://picsum.photos/600/400?random=2">
<img src="https://picsum.photos/600/400?random=3">
<img src="https://picsum.photos/600/400?random=4">

</div>

</section>


<section id="wallpapers">

<h2>🖼️ صور خلفيات</h2>

<div class="gallery">

<img src="https://picsum.photos/600/400?random=5">
<img src="https://picsum.photos/600/400?random=6">
<img src="https://picsum.photos/600/400?random=7">
<img src="https://picsum.photos/600/400?random=8">

</div>

</section>


<section id="cities">

<h2>🏙️ صور المدن</h2>

<div class="gallery">

<img src="https://picsum.photos/600/400?random=9">
<img src="https://picsum.photos/600/400?random=10">
<img src="https://picsum.photos/600
