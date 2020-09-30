---
layout: post
date:   2020-09-30
title: "Tableau Row Level Security"
categories:
  - İş Zekası

image: /images/posts/tableau/cover.png
tags:
  - Tableau Desktop
  - Tableau Server
  - Row Level Security
---

### Tableau Row Level Security

<figure class="figure">
    <a href="/images/posts/tableau/row-level-security/cover.png"><img src="/images/posts/tableau/row-level-security/cover.png"></a>
    <figcaption>Row Level Security</figcaption>
</figure>

<strong> “Row Level Security” </strong>

Selamlar bu yazımda Tableau üzerinde Row Level Security nasıl yapılır özetle anlatmaya çalışacağım. 

Öncelikle işlemleri Tableau Desktop ve Tableau Server üzerinde gerçekleştireceğiz.
 Elimizde aşağıdaki gibi bir Dashboard olduğunu varsayalım. Bana ait olan iki farklı mail adresi üzerinden gideceğim.

 <a href="/images/posts/tableau/row-level-security/row-level-security-image1.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image1.png"></a>


Başlamadan önce Tableau Server üzerinde login oluyor ve bir site oluşturuyoruz.
<br/>
Owner User: Furkan Tolu (163…..@mersin.edu.tr)
"https://dub01.online.tableau.com/#/site/intelvod/"

Yapmak istediğimiz kullanıcı gruplarına ya da kullanıcılara göre görüntülenecek dataları filtreleme. 

Tableau Server üzerinde kullanıcı ve kullanıcı grubu oluşturuyoruz. Sol tarafta bulunan Groups menüsüne giderek işlemi gerçekleştiriyoruz.

 <a href="/images/posts/tableau/row-level-security/row-level-security-image2.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image2.png"></a>

Kullanıcı grubunu oluşturduk, şimdi kullanıcıları oluşturacağız. Bu işlemi iki farklı yol ile yapabilirsiniz. 

Kullanıcı mail adreslerini tek tek girerek ya da bir csv dosyasından alarak. 
<br/>Biz manuel şekilde mail adresi girerek oluşturacağız.

<a href="/images/posts/tableau/row-level-security/row-level-security-image3.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image3.png"></a>

<a href="/images/posts/tableau/row-level-security/row-level-security-image4.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image4.png"></a>

Kullanıcıları oluşturduk. Şimdi raporları publish edip yetkilendirme işlemleri gerçekleştireceğiz.
Tableau Desktop üzerinden Tableau Server’a sign in oluyoruz.

<a href="/images/posts/tableau/row-level-security/row-level-security-image5.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image5.png"></a>

Çalışmalarımızı publish ediyoruz.

<a href="/images/posts/tableau/row-level-security/row-level-security-image6.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image6.png"></a>

Permissions ayarlarını ister buradan özelleştirebilir, isterseniz Tableau Server üzerinden yapabiliriz.
Biz Tableau Server üzerinden devam edelim. Publish ediyorum.

<a href="/images/posts/tableau/row-level-security/row-level-security-image7.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image7.png"></a>

Explore menüsü üzerinde Proje, Dashboard, Sheet ya da Sütun bazlı izin ayarlamaları yapabiliyoruz.<br/>
<br/> Üç nokta daha sonra Permissions diyerek işlemlere devam ediyorum.

<a href="/images/posts/tableau/row-level-security/row-level-security-image8.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image8.png"></a>

Furkan Tolu(furkantolu70@gmail.com) user’ına görüntüleme izni verdik ve diğer özelleştirmeler için
onay vermedik.

Görüldüğü gibi user, sadece raporları görebiliyor.

<a href="/images/posts/tableau/row-level-security/row-level-security-image9.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image9.png"></a>

Şimdi ise CustomerD Dasboard’u, Day of Order Date sütununu için furkantolu70@gmail.com
kullanıcısına sadece ‘January’ ay bilgisini göstereceğiz. Diğer kullanıcı tüm ayları görebilecek.

<a href="/images/posts/tableau/row-level-security/row-level-security-image10.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image10.png"></a>

Order Date bazında kullanıcı için bir filtre oluşturuyoruz. Sol menüden kullanıcıyı, sağ menüden ise görmesini istediğimiz alanları seçerek devam ediyoruz.

<a href="/images/posts/tableau/row-level-security/row-level-security-image11.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image11.png"></a>

Şimdi her iki kullanıcı ile son duruma bakalım.

<a href="/images/posts/tableau/row-level-security/row-level-security-image12.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image12.png"></a>

<a href="/images/posts/tableau/row-level-security/row-level-security-image13.png"><img src="/images/posts/tableau/row-level-security/row-level-security-image13.png"></a>

Evet, bu yazıda Tableau ile Row Level Security düzenlemeleri yapmaya çalıştık. Elimden geldiği kadar açık ve özet bir anlatım yapmaya çalıştım.
Umarım sizler için faydalı bir yazı olmuştur.

Görüşmek üzere, esen kalın!

