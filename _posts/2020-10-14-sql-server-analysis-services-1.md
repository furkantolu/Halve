---
layout: post
date:   2020-09-30
title: "SSAS (SQL Server Analysis Services) #1"
categories:
  - İş Zekası

image: /images/posts/SSAS/cover.png
tags:
  - SSAS(SQL Server Analysis Services)
  - Tabular Model
  - Data Mining
---

### SSAS (SQL Server Analysis Services) #1

<figure class="figure">
    <a href="/images/posts/SSAS/chapter1/ssas-1.png"><img src="/images/posts/SSAS/chapter1/ssas-1.png"></a>
    <figcaption>SSAS</figcaption>
</figure>

Merhabalar,  

Bu yazımda yeni tanıştığım MSBI SSAS üzerinde konuşacağız.

SQL Server Analysis Services(SSAS), Microsoft SQL Server'da bir çevrimiçi analitik işleme ve veri madenciliği aracıdır. SSAS, kuruluşlar tarafından muhtemelen birden çok veritabanına veya farklı tablolara veya dosyalara yayılmış bilgileri analiz etmek ve anlamlandırmak için bir araç olarak kullanılır.  

Özetle DW veya DM verisini çok boyutlu olarak analiz edilmeye hazır hale getirmek için kullanılır. 

SSAS içerisinde Multidimensional and Data Mining Mode, Tabular Mode ve PowerPivot Mode olmak üzere 3 mod bulunmaktadır.

 <a href="/images/posts/SSAS/chapter1/image1.png"><img src="/images/posts/SSAS/chapter1/image1.png"></a>

<strong>
  Multidimensional and Data Mining Mode 
</strong><br/>
Bu çok boyutlu model ile Visual Studio üzerinde Multidimensional projeler yapılır, veri küpleri oluşturulur ve Analysis Services üzerinden kullanıcılara sunulur. Küpler üzerinde analiz yapan kullanıcı sayısı çoksa ve küplere ilişkin gelişmiş özellikler isteniyorsa iyi bir yöntemdir. Diğer modellere göre development daha zahmetlidir. 

<strong>
  Tabular(Semantic) Mode 
</strong><br/>
MS SQL Server 2012 ile gelmiştir. Bu model ile birlikte Tabular projeler yapılır, veriler excelde pivot tablolarla analiz edilmeye hazır hale getirilir. Multidimensional modele göre daha basit bir yapısı vardır. Power Pivotta yapılmış veri yapısı kolaylıkla import edilebilir. 

<strong>
  Power Pivot Mode 
</strong><br/>
Bazı işletmelerde az sayıda kullanıcının kullanacağı bir yapı yeterli olabilir. Bu tip durumlarda küplerle uğraşmak gerekmez. Bu ihtiyacı gidermek amacıyla excel eklentisi olarak Power Pivot getirilmiştir. Excel içerisindeki standart pivot table işleyebileceği satır sayısı ve işlem hızı açısından ciddi bir veri analizi yapmak için eksik kalmaktadır. Bu ihtiyacı Power Pivot karşılamaktadır. 

Bir sonraki yazımda SSAS Tabular Model hakkında yazacağım, görüşmek üzere. Hoşçakalın!