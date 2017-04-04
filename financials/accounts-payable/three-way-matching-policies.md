---
title: "Üç yönlü eşleştirme ilkeleri"
description: "Bu makalede üç yönlü eşleştirme örnekleri sağlanmıştır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2761
ms.assetid: 70f3cb1a-18b7-4474-95ec-28b2410dd8f8
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4e9ee51394ee7c1663de2396131fa36a3fa17f7d
ms.openlocfilehash: d9d105ea6a91c53c3d45feedb8ea3ba81983f926
ms.lasthandoff: 03/31/2017


---

# <a name="three-way-matching-policies"></a>Üç yönlü eşleştirme ilkeleri

Bu makalede üç yönlü eşleştirme örnekleri sağlanmıştır.

<a name="example-three-way-matching-for-items"></a>Örnek: Maddeler için üç yönlü eşleştirme
-------------------------------------

**Özet:** Ken, Fabrikam adındaki bir tüzel kişiliğin şirket genel merkezinde denetleyici olarak görev yapmaktadır. Ken, satınalma siparişlerini temel alan tüm satıcı faturalarının satınalma siparişi satırlarıyla eşleşmesi gerektiğinde karar verir (iki yönlü eşleştirme). Sabit kıymet olarak kullanılacak maddelerle ilgili satınalmalar için faturaların hem satınalma siparişi satırları hem de ürün giriş satırlarıyla eşleşmesi gerekmektedir (üç yönlü eşleştirme).

Fabrikam, birden çok tüzel kişilikle ve dünyanın tüm bölgelerindeki çalışanlarla çalışmaktadır. Hareketlerin hacmi arttıkça, girişler ile faturalar arasındaki uyuşmazlıklar da artmaktadır. Bu da varlıkların silinmesine yol açar. Satıcılardan gelen faturalar ödenir ancak işlem sipariş edilenden daha az madde alınması veya maddelerin hiç alınmaması gibi uyuşmazlıkların belirlenmesini kapsamaz. Çalışanlar işlerini yapmak için araç ve diğer malzemelere hala ihtiyaç duyduğundan harcama da artar. Ken, satıcıların sipariş edilen ürünleri sevk ettiklerinden ve maddelerin Fabrikam çalışanları tarafından alındığından emin olmak ister. Bu nedenle Ken, kuruluştaki tüm tüzel kişilikler iki yönlü ve üç yönlü eşleştirme talep eder. Fatura eşleştirme, kaybolan veya alınmayan maddelerle ilgili sorunların izlenmesi ve çözülmesine yardımcı olur. 

Bu örnekteki fatura eşleştirme ilkeleri aşağıdaki rollerde görev yapan kişilerin hedefleri karşılamasına yardımcı olur:

-   Ken, Fabrikam kurumunda denetleyicidir. Bu kuruluştaki kişilerin satıcılardan madde (mal veya hizmet) sipariş etme, alma ve ödeme yapmayla ilişkili sorunları belirlemesine ve düzeltmesine yardımcı olabilir.
-   Phyllis ve April Fabrikam'ın Amerika Birleşik Devletleri bölümündeki borç hesapları departmanında muhasebe yönetici olarak çalışmaktadır. Şirket ilkelerini uygulayarak faturalar için ödemelerin yalnızca faturalar satınalma siparişi ve uygun olduğunda mal ve hizmet girişleriyle eşleştirildikten sonra yapılmasını sağlayabilirler.
-   Tony, Fabrikam'ın Amerika Birleşik Devletleri bölümünde üretim müdürü olarak görev yapmaktadır. Kendisi ve diğer üretim personeli, ürünlerin satıcılardan sipariş edildiği şekilde alındığından ve muhasebeleştirildiğinden emin olarak personelin işlerini yapmak için gerekli olan araçlara sahip olmalarını sağlayabilirler.

### <a name="prerequisites"></a>Önkoşullar

-   Ken, eşleştirme ilkesini tüzel kişilik düzeyinde Üç yönlü eşleştirme olarak ayarlar.
-   Ken, tüzel kişilikte Başlık eşleştirme durumu geçişini otomatik olarak güncelleştir seçeneğini Evet olarak ayarlar.
-   Ken, tüzel kişilik için Fiyat toplamları alanını eşleştir bölümünü Yüzde olarak ayarlar ve tolerans değeri olarak %15 girer.
-   Ken, madde 1500 - CNC Milicron Makine için madde düzeyinde eşleştirme ilkesini Üç yönlü eşleştirme olarak ayarlar. Bu madde, Fabrikam'de üretim için kullanılan bir varlık maddesidir. Bu maddeye ilişkin faturalar fiyatlar için satınalma siparişi satırlarıyla ve miktarlar için ürün girişleriyle eşleştirilir.
-   Tony, beş adet CNC Milicron Makine için bir talep girer. Fabrikam'da satınalma siparişi görevlisi olan Alicia, maddeleri tedarik etmek için Contoso adlı bir tüzel kişiliğe bir satınalma siparişi düzenler.

    | Madde kodu                 | Miktar | Birim fiyat | Net tutar | Masraf kodu        | Masraf değeri |
    |-----------------------------|----------|------------|------------|---------------------|---------------|
    | 1500 – CNC Milicron Makine | 5        | 8.000,00   | 40.000,00  | Sevkiyat ve ambalaj | 3.000,00      |

-   Contoso'da alacak hesapları görevlisi olan Arnie o haftayla ilgili sevkiyatları inceler. Arnie, CNC Milicron Makinelerinin teslimatı için Fabrikam'a faturalanacak sevkiyat hareketlerini seçer. Tamer, sevkiyat ve ambalaj için de bir ücret ekler. Fabrikam, bu gideri kıymet maliyetinin bir parçası olarak değerlendirecektir.

### <a name="scenario"></a>Senaryo

1.  Fabrikam'da alım departmanındaki bir çalışan olan Sammy, Contoso tarafından sevk edilen makinelerin toplam miktarını alır. Ürün girişine miktar olarak 5 girer. Satınalma siparişi tam olarak alındığından, satınalma siparişinin durumu Alındı olarak değişir.
2.  Fabrikam'da borç hesapları koordinatörü olan April, Contoso tarafından gönderilen faturayı girer ve doğrular. April aşağıdaki bilgileri doğrular:
    -   Üç yönlü eşleştirme gerektiren maddeler için fatura satırındaki miktarın alınan miktarla eşleştiğini. Ürün girişinde belirtilen alınan miktarın faturayla eşleştiğini.
    -   Çift yönlü veya üç yollu eşleşen gerektiren maddeler için Operations.This fiyat eşleştirme aşağıdaki türleri içerir, Microsoft Dynamics 365 içinde tanımlanan tolerans içinde faturada fiyatları şunlardır:
        -   Net birim fiyatı eşleştirme – Fatura satırındaki net birim fiyatı, satınalma siparişi satırındaki net birim fiyatla, tolerans yüzdesi aralığında eşleşir. Bu örnekte, net birim fiyat toleransı +%8'dir.
        -   Fiyat toplamları eşleştirme – Fatura satırlarındaki net tutar, tolerans yüzdesi, tutarı veya yüzde ve tutarı kapsamında satınalma siparişi satırındaki net tutarla eşleşir. Bu örnekte, fiyat toplamları eşleştirme toleransı +%15'dir.

Contoso'nun gönderdiği basılı fatura aşağıdaki bilgileri içerir.

| Madde                        | Miktar | Birim fiyat | Net tutar |
|-----------------------------|----------|------------|------------|
| 1500 – CNC Milicron Makine | 5        | 8.100,00   | 40.500,00  |
| Sevkiyat ve ambalaj       |          |            | 4.000,00   |
| Vergi                         |          |            | 0,00       |
| Toplam                       |          |            | 44.500,00  |

İşlemler için Microsoft Dynamics 365 fatura satırının aşağıdaki bilgileri içerir.

| Madde kodu                 | Miktar | Birim fiyat | Satır net tutarı | Eşleme ilkesi    | Ürün girişi miktar eşleşmesi | Fiyat eşleme | Fiyat toplamı eşleştirme |
|-----------------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| 1500 – CNC Milicron Makine | 5        | 8.100,00   | 40.500,00       | Üç yönlü eşleştirme | Başarılı                         | Başarılı      | Başarılı            |

Bu satır fatura eşleştirme işlemini geçtiğinden, fatura deftere nakledilebilir.

## <a name="example-three-way-matching-for-item-and-vendor-combinations"></a> Örnek: Madde ve satıcı birleşimleri için üç yönlü eşleştirme
Özet: Ken, Fabrikam adındaki bir tüzel kişiliğin şirket genel merkezinde denetleyici olarak görev yapmaktadır. Ken, satınalma siparişlerini temel alan tüm faturaların satınalma siparişi satırlarıyla eşleşmesi gerektiğinde karar verir (iki yönlü eşleştirme). Cassie, Fabrikam Malezya bölümünde sayman olarak görev yapmaktadır. Malezya'daki belirli satıcılardan sipariş edilen seçili maddelerin hem satınalma siparişi satırları hem de ürün giriş satırları ile eşleşmesi (üç yönlü eşleştirme) gerektiğini belirtir. Ayrıca, belirli satınalma siparişleri için eşleştirme ilkesini geçersiz kılarak daha üst düzey bir eşleştirme belirtebilir. 

Hacim ve tutarlar küçüktür ve Malezya'daki bazı satıcıların yaptıkları teslimatlarda sorunlar olmuştur. Bu nedenlerle Cassie, Malezya'da tedarik sağlayan belirli madde ve satıcı bileşenleri için denetim düzeyini üç yönlü eşleştirme olarak ayarlar. 

Bu örnekteki fatura eşleştirme ilkeleri aşağıdaki rollerde görev yapan kişilerin hedefleri karşılamasına yardımcı olur:
-   Ken, Fabrikam kurumunda denetleyicidir. Bu kuruluştaki kişilerin satıcılardan madde (mal veya hizmet) sipariş etme, alma ve ödeme yapmayla ilişkili sorunları belirlemesine ve düzeltmesine yardımcı olabilir.
-   Cassie, Fabrikam Malezya bölümünde sayman olarak görev yapmaktadır. Şirket ilkelerini uygulayarak faturalar için ödemelerin yalnızca faturalar satınalma siparişi satırları ve mal ve hizmet alımını gösteren ürün girişleriyle eşleştirildikten sonra yapılmasını sağlayabilir. Ayrıca, operasyon maliyetlerini denetlemek amacıyla belirli maddeler için denetim düzeyini üç yönlü eşleştirmeye yükseltebilir.

### <a name="prerequisites"></a>Önkoşullar

-   Ken, eşleştirme ilkesini tüzel kişilik düzeyinde İki yönlü eşleştirme olarak ayarlar.
-   Ken, tüzel kişilik için Fiyat toplamları alanını eşleştir bölümünü Yüzde olarak ayarlar ve tolerans değeri olarak %10 girer.
-   Ken tüm maddeler için birim fiyat toleransını %2 olarak ayarlar.
-   Cassie PH2500 - Bilgisayar maddesi ve Contoso satıcısı için madde ve satıcı bileşimi düzeyinde eşleştirme ilkesini Üç yönlü eşleştirme olarak ayarlar.
-   Fabrikam'n Malezya bölümünde satınalma görevlisi olan Alicia, aşağıdaki tabloda gösterildiği şekilde üç madde tedarik etmek için Contoso'ya satınalma siparişleri düzenler. Satınalma siparişini oluştururken, kablosuz fare için eşleştirme ilkesinin iki yönlü eşleştirme değil üç yönlü eşleştirme olmasını seçer.

    | Madde kodu           | Miktar | Birim fiyat | Net tutar | Eşleştirme ilkesi (varsayılan giriş) | Eşleştirme ilkesi (satınalma siparişi satırında) |
    |-----------------------|----------|------------|------------|---------------------------------|----------------------------------------------|
    | PH2500 – Bilgisayar     | 2        | 2.500,00   | 5.000,00   | Üç yönlü eşleştirme              | Üç yönlü eşleştirme                           |
    | MM01 – Kablosuz Fare | 2        | 40,00      | 80,00      | İki yönlü eşleştirme                | Üç yönlü eşleştirme                           |
    | USB Sürücü             | 200      | 10,00      | 2.000,00   | İki yönlü eşleştirme                | İki yönlü eşleştirme                             |

### <a name="scenario"></a>Senaryo

1.  Maddeler gelir. Fabrikam Malezya bölümünde alım departmanında çalışan Sammy işe ara vermiştir ve ürün girişini hemen deftere nakletmez.
2.  Fabrikam'da borç hesapları koordinatörü olan April, Contoso tarafından gönderilen faturayı girer ve doğrular. April aşağıdaki bilgileri doğrular:
    -   Üç yönlü eşleştirme gerektiren maddeler için fatura satırındaki miktarın alınan miktarla eşleştiğini. Ürün girişinde belirtilen alınan miktarın faturayla eşleştiğini.
    -   Çift yönlü veya üç yollu eşleşen gerektiren öğeler fiyatları fatura satırındaki Microsoft Dynamics 365 işlemleri için tanımlanan tolerans içinde olan. Bu fiyat eşleştirme aşağıdaki türleri içerir:
        -   Net birim fiyatı eşleştirme – Fatura satırındaki net birim fiyatı, satınalma siparişi satırındaki net birim fiyatla, tolerans yüzdesi aralığında eşleşir. Bu örnekte, net birim fiyat toleransı +%2'dir.
        -   Fiyat toplamları eşleştirme – Fatura satırlarındaki net tutar, tolerans yüzdesi, tutarı veya yüzde ve tutarı kapsamında satınalma siparişi satırındaki net tutarla eşleşir. Bu örnekte, fiyat toplamları eşleştirme toleransı +%10'dir.

Contoso'nun gönderdiği basılı fatura aşağıdaki bilgileri içerir.

| Madde                  | Miktar | Birim fiyat | Net tutar |
|-----------------------|----------|------------|------------|
| PH2500 – Bilgisayar     | 2        | 2,500,00   | 5.000,00   |
| MM01 – Kablosuz Fare | 2        | 41,00      | 82,00      |
| USB Sürücü             | 200      | 10,05      | 2.010,00   |
| Toplam fatura         |          |            | 7.092,00   |

İşlemler için Microsoft Dynamics 365 fatura satırının aşağıdaki bilgileri içerir.

| Madde kodu           | Miktar | Birim fiyat | Satır net tutarı | Eşleme ilkesi    | Ürün girişi miktar eşleşmesi | Fiyat eşleme | Fiyat toplamı eşleştirme |
|-----------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| PH2500 – Bilgisayar     | 2        | 2.500,00   | 5.000,00        | Üç yönlü eşleştirme | Basarisiz                         | Başarılı      | Başarılı            |
| MM01 – Kablosuz Fare | 2        | 41,00      | 82,00           | Üç yönlü eşleştirme | Basarisiz                         | Basarisiz      | Başarılı            |
| USB Sürücü             | 200      | 10,05      | 2010,00         | İki yönlü eşleştirme   |                                | Başarılı      | Başarılı            |

Aşağıdaki öğeleri not alın:
-   PH2500 – Bilgisayar satırı için, Ürün giriş miktarı eşleştirme sütununda, fatura satırı bir ürün girişiyle eşleşmediğinden bir uyarı simgesi bulunur.
-   MM01 – Kablosuz Fare satırı için, Ürün girişi miktarı eşleştirme sütununda, fatura satırı bir ürün girişiyle eşleşmediğinden bir uyarı simgesi bulunur. %2 net birim fiyat toleransı aşıldığından Birim fiyat eşleştirme sütununda bir uyarı simgesi bulunur.
-   USB Sürücü satırı için, iki yönlü eşleştirme fatura satırı ile ürün giriş satırı miktarlarını eşleştirmediğinden, ürün giriş miktarı eşleştirme sütunu boş bırakılır.

Deftere fatura eşleştirme uyuşmazlıklarıyla nakledilecek faturalar için onay gerekiyorsa, faturanın fiyat eşleştirme hataları ve miktar eşleştirme hatalarıyla nakledilebilmesi için Fatura eşleştirme ayrıntıları sayfasındaki Eşleştirme uyuşmazlıklarıyla deftere nakli onayla seçeneğinin seçilmesi gerekir. Onay gerekli değilse, başka bir deftere nakil hatası olmaması durumunda fatura işleme devam edebilir.


Daha fazla bilgi için bkz: [hesapları eşleştirme borçları fatura](accounts-payable-invoice-matching.md).


