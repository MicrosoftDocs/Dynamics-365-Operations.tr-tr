---
title: "POS içinde ürün ve müşteri arama"
description: "Bu konu Dynamics 365 for Retail içinde ürün ve müşteri arama özelliğinde yapılmış olan iyileştirmeler hakkında genel bakış sağlar."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 08/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: bd563610616fa72a610e0b134371765cc1edacc6
ms.contentlocale: tr-tr
ms.lasthandoff: 03/08/2018

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Satış noktası içinde ürün ve müşteri arama genel bakışı

[!include[banner](includes/banner.md)]

Modern Satış Noktası (MPOS) ve Bulut Satış Noktası (CPOS), kolay kullanımlı arama işlevi sağlar ve mağaza çalışanlarının ürün ve müşterileri hızlıca aramasına olanak sağlar. Arama çubuğu her zaman MPOS ve CPOS'un üstünde mevcuttur, böylece çalışanlar ürünleri ve müşterileri hızla bulabilir.

Çalışanlar ürünleri geçerli mağaza ile ilişkilendirilmiş sınıflamalar ve kataloglar ve şirketteki diğer herhangi bir mağaza ile ilişkilendirilmiş kataloglar ve sınıflandırmalar içerisinde arayabilirler. Bu nedenle, kasiyerler mağaza sınıflandırması dışındaki ürünleri satabilir ve iade alabilir. Benzer şekilde, çalışanlar geçerli mağaza veya şirketle ilişkili herhangi başka bir mağaza ile ilişkili müşterileri arayabilir. Ek olarak, çalışanlar, üst kuruluştaki başka bir şirketle ilişkilendirilmiş müşterileri arayabilirler.

## <a name="product-search"></a>Ürün arama 

Varsayılan olarak, ürün arama mağaza sınıflandırmasında yapılır. Bu arama türü *yerel ürün arama* olarak bilinir. Ancak, çalışanlar geçerli mağaza ile ilişkilendirilen herhangi bir kataloğa kolayca geçiş yapabilir veya farklı bir mağazada arama yapabilirler. Bu arama türü *uzak ürün arama* olarak bilinir. Kataloğu değiştirmek için sayfanın sol tarafındaki **Kategoriler** düğmesini seçin. Beliren bölmenin üstünde, **Kataloğu değiştir** düğmesini seçin ve sonra taramak için kullanılabilir kataloglardan birini seçin. Sistem ürünleri seçilen katalogda arar.

**Kataloğu değiştir** sayfasında, çalışanlar kolayca herhangi bir mağazayı seçebilir veya tüm mağazalar arasındaki ürünler arasından arama yapabilir.

![Kataloğu değiştirme](./media/Changecatalog.png "Kataloğu değiştirme")
 
Bir yerel ürün arama, aşağıdaki ürün özellikleri içerisinde arar:

- Ürün numarası
- Ürün adı
- Tanım
- Boyutlar
- Barkod
- Arama adı

### <a name="enhancements-to-local-product-searches"></a>Yerel ürün aramasındaki geliştirmeler

Yerel ürün arama deneyimi daha kullanıcı dostu yapılmıştır. Aşağıdaki geliştirmeler yapılmıştır:

- Ürün ve müşteri açılır menüleri arama çubuğuna eklenmiştir; böylece çalışanlar arama yapmadan önce **Ürün** veya **Müşteri** seçimini yapabilirler. Varsayılan olarak, **Ürün** seçilidir, aşağıdaki şekilde gösterildiği gibi.
- Çoklu anahtar sözcük aramaları için (yani, arama terimleri kullanan aramalar için) perakendeciler aramanın herhangi bir arama terimi ile mi eşleşen yoksa yalnızca tüm arama terimleriyle mi eşleşen sonuçları dahil edeceğini yapılandırabilir. Bu ayar, POS işlevi profilinde, **Ürün arama** olarak adlandırılan yeni bir grup altında kullanılabilir. Varsayılan ayar **Herhangi bir arama terimi ile eşleş**'tir. Bu ayar aynı zamanda önerilen ayardır. **Herhangi bir arama terimiyle eşleş** ayarı kullanıldığında, bir veya birden fazla arama terimi ile tümüyle veya kısmi olarak eşleşen tüm ürünler sonuç olarak getirilir ve sonuçlar, en fazla anahtar sözcük eşleşmesine (kısmi veya tam) sahip olan ürünler olarak otomatik sıralanır.

    **Tüm arama terimleriyle eşleş** ayarı, yalnızca tüm arama terimleriyle (kısmi veya tam) olarak eşleşen ürünleri döndürür. Bu ayar, ürün adları uzunsa ve çalışanlar arama sonuçlarında yalnızca sınırlı ürünleri görmek istiyorlarsa kullanışlıdır. Ancak, bu tür aramanın iki sınırlaması vardır:

    - Arama yalnızca tek tek ürün özellikleri üzerinde yapılır. Örneğin, en az bir ürün özelliğinde, yalnızca tüm aranan kelimeleri içeren ürünler döndürülür.
    - Boyutlar aranmaz.

- Perakendeciler şimdi ürün aramayı, kullanıcılar ürün adlarını yazarken arama sonuçlarını gösterecek şekilde yapılandırabilir. Bu işlev için yeni bir ayar, POS işlevi profilinde, **Ürün arama** olarak adlandırılan bir grup altında kullanılabilir. Bu ayarın adı **Yazarken arama önerilerini göster**'dir. Bu işlev, çalışanların aradıkları ürünü hızlıca bulmalarına yardımcı olabilir çünkü tam adını yazmalarına gerek kalmaz.
- Ürün arama algoritması şimdi ayrıca aranan terimleri ürünün **Arama adı** özelliğinde de arar.

![Ürün önerileri](./media/Productsuggestions.png "Ürün önerileri")

## <a name="customer-search"></a>Müşteri arama

Müşteri arama, çeşitli amaçlarla müşterileri bulmak için kullanılır. Örneğin, kasiyer bir müşterinin istek listesini veya satın alma geçmişini görüntülemek veya müşteriyi bir harekete eklemek isteyebilir. Çoklu anahtar sözcük aramalarında, müşteri arama algoritması aranan sözcüklerden herhangi biriyle eşleşen tüm müşterileri döndürür. Ancak, daha fazla anahtar kelime ile eşleşen müşteriler sonuçların üst kısmında görüntülenir. Bu davranış, diğer arama motorlarının sonuçları gösterme şekline benzer. Önce aranan terimlerin en fazlası ile eşleşen sonucu gösterirler ve sonra arama sözcükleri ile kısmen eşleşen sonuçları gösterirler. Bu davranış, aramalarında birden fazla anahtar sözcük kullandıkları, ancak sözcüklerden birinin yazım hatası içerdiği durumlarda kasiyerlere yardımcı olur.

Varsayılan olarak, müşteri arama mağazayla ilişkilendirilmiş olan müşteri adres defterleri üzerinden yapılır. Bu arama türü *yerel müşteri arama* olarak bilinir. Bununla birlikte, çalışanlar müşteriler için genel arama da yapabilir. Başka bir deyişle, şirketin mağazaları ve tüm diğer tüzel kişiler arasında arama yapabilirler. Bu arama türü *uzak müşteri arama* olarak bilinir.

Genel olarak aramak için, çalışanlar sayfanın altında bulunan **Sonuçları filtrele** düğmesini seçebilir ve sonra **Tüm mağazaları ara** seçeneğini, aşağıdaki şekilde gösterildiği gibi işaretleyebilir. Bu durumda, yalnızca müşteriler döndürülmez. Merkezdeki herhangi bir adres defterinin parçası olan tüm taraflar da döndürülür. Bu taraflar arasında çalışanlar, satıcılar, ilgili kişiler ve rakipler de vardır.

> [!NOTE]
> Bir uzak müşteri aramasının sonuç döndürmesi için en az dört karakter girilmesi gerekir.

Bir uzak müşteri aramasında, diğer tüzel varlıklardaki müşteriler için müşteri kimliği gösterilmez, çünkü geçerli şirkette bu müşteriler için bir müşteri kimliği oluşturulmamıştır. Ancak, bir çalışan müşteri ayrıntıları sayfasını açarsa, sistem otomatik olarak bu taraf için bir müşteri kimliği oluşturur ve mağazanın müşteri adres defterini müşteri ile ilişkilendirir. Bu nedenle, müşteri daha sonra yapılan yerel mağaza aramalarında da görünür.

![Genel müşteri arama](./media/Globalcustomersearch.png "Genel müşteri arama")

### <a name="enhancements-to-local-customer-searches"></a>Yerel müşteri aramasındaki geliştirmeler

Yerel müşteri aramaları, çalışanların müşterileri telefon numarasına göre hızlıca bulmasına yardımcı olur. Çalışanların, köşeli parantez, tire veya boşluk gibi bir müşterinin telefon numarasını eklenmiş olan özel karakterleri eklemesi gerekmez. Kasiyerlerin telefon numaralarını herhangi bir şekilde saklayabilmelerine rağmen (örneğin köşeli parantez, tire, simgeler ve benzeri içerebilirler), müşterileri telefon numarasının bir kısmını yazarak arayabilirler. Bir kasiyer telefon numarasını girdiğinde bir özel karakter dahil etmişse, diğer kasiyerler müşteriyi, özel karakterden sonra beliren numaraları girerek bulabilirler. Örneğin, bir müşterinin telefon numarası **123-456-7890** olarak girilmişse, bir kasiyer müşteriyi **123**, **456**, **7890** veya **1234567890** arayarak veya telefon numarasının ilk birkaç rakamını kısmen girerek arayabilir.

