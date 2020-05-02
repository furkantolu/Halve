---
layout: post
date:   2020-05-01
title: "Power BI ve R ile 10 Günlük Covid-19 Forecast"
categories:
  - Power BI

image: /images/posts/powerbi/cover2.png
tags:
  - Power BI
  - R Language
  - Forecast
  - Covid-19
---

### 10 günlük Covid-19 Artış Oranı Forecast

<figure class="figure">
    <a href="/images/posts/powerbi/cover.png"><img src="/images/posts/powerbi/cover.png"></a>
    <figcaption>Forecast</figcaption>
</figure>

<strong> “Covid-19 ” </strong>

Selamlar bu yazımda 10 günlük basit bir artış oranı tahmini nasıl yapılır onu anlatmaya çalışacağım. Elimizde “worldwide-aggregate.csv” adında bir datasetimiz bulunmaktadır. Bu datasetin içinde "Date-Confirmed-Recovered-Deaths-Increase Rate" sütunları bulunmaktadır. Bizim ihtiyacımız olan tarih ve artış oranları olacaktır.

 <a href="/images/posts/powerbi/p1.png"><img src="/images/posts/powerbi/p1.png"></a>

Başlamadan <a href="https://mran.microsoft.com/download" link="https://mran.microsoft.com/download">Microsoft R Open</a> kurulumu yapınız.

Kodlarınızı <a href="https://rstudio.com/" link="https://rstudio.com/">R Studio</a> içerisinde yazıp daha sonra Power BI içerisine alabilirsiniz.

Power BI içerisinde "Get Data" seçeneği ile csv dosyamızı içeri alıyoruz.

 <a href="/images/posts/powerbi/p2.png"><img src="/images/posts/powerbi/p2.png"></a>

Başlamadan `null` olan verileri `0` ile yenileyeceğiz. "Transform Data" seçeneği ile Power Query Editor’e gidiyoruz.

 <a href="/images/posts/powerbi/p3.png"><img src="/images/posts/powerbi/p3.png"></a>

 "Replace Values" seçeneğine tıklayarak `Null` olan değerleri `0` ile değiştireceğiz.

 <a href="/images/posts/powerbi/p4.png"><img src="/images/posts/powerbi/p4.png"></a>

 İşlemi gerçekleştirdikten sonra "Close&Apply" seçeneği ile Power BI arayüzümüzü açıyoruz.
 Verilerimiz bu şekilde;

<a href="/images/posts/powerbi/p5.png"><img src="/images/posts/powerbi/p5.png"></a>

Yeni bir R Script Visual ekleyelim, "Date" ve "Increase rate" alanlarını ekleyerek devam edelim.

<a href="/images/posts/powerbi/p6.png"><img src="/images/posts/powerbi/p6.png"></a>

R scriptlerimizi yazmaya başlayacağız bu işlemi R Studio üzerinde ya da Power BI üzerinde gerçekleştirebilirsiniz. Ben Power BI üzerinde yapacağım.
Açılan R script editor penceresinde yazmaya başlayalım.
Eğer daha önce kurulum yapmadıysanız

-`install.packages("forecast")`

-`install.packages("tseries")`

paketlerinizi yüklemeniz gerekecektir. Kodlarımız aşağıdaki gibi olacaktır.

<a href="/images/posts/powerbi/p7.png"><img src="/images/posts/powerbi/p7.png"></a>

`Library(“”)` fonksiyonu ile kullanacağımız kütüphaneleri çağırdık.

`myTimeSeries <- dataset` komutu ile datasetimizi myTimeSeries vektörüne atadık.

`as.ts` ile bir seriyi zaman serisine dönüştürüyoruz. Argüman olarak X’in 2. Sütununu verdik. Bu işlemi `myX` vektörüne verdik.

`myForecast <- forecast(holt(myX), h = 10)` burada ise 10 günlük bir tahmin alıyor ve myForecast vektörüne atıyoruz.
`Forecast` fonksiyonu gelecekteki verileri tahmin etmek için kullanılıyor.

`plot(myForecast, main = "10-day increase rate forecast", ylab="Level", xlab="Day" )`
`plot` fonksiyonu ise çizim yapmak için kullanılır. `myForeCast` içerisinde bulunan verileri `plot` ile grafik haline getirdik.

<a href="/images/posts/powerbi/p8.png"><img src="/images/posts/powerbi/p8.png"></a>

Ortaya çıkan tahminimiz bu şekildedir. Grafik, yapacağınız özelleştirmeler ile geliştirilebilir.

Okuduğunuz için teşekkürler..