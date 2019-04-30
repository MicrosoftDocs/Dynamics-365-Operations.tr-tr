---
title: Borç hesapları fatura eşleşmesi
description: Borç hesapları faturası eşleştirme, satıcı faturasını, satın alma siparişini ve ürün alındı bilgilerini eşleştirme işlemidir.
author: abruer
manager: AnnBe
ms.date: 02/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 27361
ms.assetid: 9f3dace7-05d8-4974-8f85-aca2e224876c
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a1f7e16064a954bb22dc233a77bf28747f7f11
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/25/2019
ms.locfileid: "896960"
---
# <a name="accounts-payable-invoice-matching"></a>Borç hesapları fatura eşleşmesi

[!include [banner](../includes/banner.md)]

Borç hesapları faturası eşleştirme, satıcı faturasını, satın alma siparişini ve ürün alındı bilgilerini eşleştirme işlemidir.

Belgeler eşleştirilirken, aralarındaki farklara eşleştirme uyuşmazlıkları denir. Eşleştirme uyuşmazlıkları, belirtilen toleranslarla karşılaştırılır. Bir eşleştirme uyuşmazlığı tolerans yüzdesini veya tutarını aşarsa, Satıcı faturası sayfasında ve Fatura geçmişi eşleştirme ayrıntıları sayfasında eşleşme farkı simgeleri görüntülenir. 

Örneğin, her birinin fiyatı 1,00 olan 1.000 pillik bir satır maddesiyle bir satınalma siparişi girdiğinizi varsayalım. Satınalma siparişi onaylanır ve satıcıya gönderilir. Satıcı 1000 pili sevk eder ve her birinin fiyatı 1,00 olan 1.000 pil için bir ürün girişi girersiniz. Pillerin stok maliyeti bu fiyatla güncelleştirilir. 

Her birinin fiyatı 1,10 olan 1000 pil için bir fatura gelir. Tüzel kişiliğiniz bu madde kategorisi tipi için yüzde 5 net birim fiyatı toleransına izin verir. 1,05 fiyatı kabul edilebilir, ancak 1,10 edilemez. Fatura bilgilerini girdiğinizde, bir fiyat uyuşmazlığı olduğu belirlenir ve faturayı bu uyuşmazlık çözümleninceye kadar kaydedebilirsiniz.

Borç hesapları fatura eşleştirmesi için aşağıdaki türleri kullanabilirsiniz:

-   Fatura toplamları eşleştirmesi – Satınalma siparişindeki toplam tutarları, fatura üzerindeki toplam tutarlara eşleştirin. Bu tür fatura eşleştirmesi fatura eşleştirme bilgileri gözden geçirmek ve denetimlerini ayarlamak için gerekli olan personel süresini en aza indirmek amacıyla bu seçeneği kullanabilmeniz için en az ayrıntı miktarını içerir.
-   İki yollu eşleştirme – Faturadaki fiyat bilgisini satınalma siparişindeki fiyat bilgisiyle eşleştirin.
-   Üç yollu eşleştirme – Faturadaki fiyat bilgisini satınalma siparişindeki fiyat bilgisiyle eşleştirir. Ayrıca, faturadaki miktar bilgisini, fatura için seçilen ürün girişleri üzerindeki miktar bilgisiyle eşleştirir.
-   Gider eşleştirme – Faturadaki gider bilgisini (tutarları) satınalma siparişi üzerindeki gider bilgisi (tutarlar) ile eşleştirir.

> [!NOTE]
> Diğer fatura doğrulama biçimleri, satıcı fatura ilkelerini kullanarak yapılabilir. 

İki yönlü eşleştirme ve üç yönlü eşleştirme her zaman fiyat bilgilerini birim fiyata göre eşleştirir. Bu eşleştirme ilkelerini fiyat bilgisini, fiyat toplamına eşleştirmek üzere de yapılandırabilirsiniz.
-   NET birim fiyatı eşleştirme – İki yönlü eşleştirme ve üç yönlü eşleştirme için fiyat bilgisini, faturanın üzerindeki her bir satır için net birim fiyatı, satınalma siparişi üzerinde karşılık gelen net birim fiyatı ile eşleştirerek gerçekleştirin. Net birim fiyat aşağıdaki formül kullanılarak belirlenir: Satırın net tutarı / Satırın miktarı
-   Fiyat toplamları eşleştirme – İki yönlü eşleştirme ve üç yönlü eşleştirme için fiyat bilgisini, faturanın üzerindeki her bir satır için net tutarı (fiyat toplamı), satınalma siparişi üzerinde karşılık gelen net tutar ile eşleştirerek gerçekleştirin. Net tutar aşağıdaki formül kullanılarak belirlenir: *(Birim fiyat \* Satır miktarı) + Satır giderleri - Satır indirimleri*. Fiyat toplamlarını yüzde ile eşleştirirken, sistem değerleri hareketin para birimini kullanarak karşılaştırır. Fiyat toplamlarını tutara göre eşleştirirken, sistem değerleri muhasebe para birimini kullanarak karşılaştırır.

Genellikle, satıcı fatura sayfasındaki satıcı faturalarını düzenlerken fatura eşleştirme hesaplamaları otomatik olarak gerçekleştirilir. Alternatif olarak, fatura eşleştirmesi, gerektiği takdirde isteğe bağlı gerçekleştirilebilir. Tüzel kişilik için İsteğe bağlı fatura eşleştirme, Borç hesapları parametreleri sayfasındaki Fatura Doğrulama sekmesindeki Fatura başlığı durumunu otomatik olarak güncelleştirmenin hedefine göre denetlenir. Fatura eşleştirme ayrıca fatura inceleme işleminin bir parçası olarak da gerçekleştirilebilir. Fatura eşleştirmenin sonuçlarını satıcı fatura sayfasında ve ilgili fatura eşleştirme sayfalarında da görüntüleyebilirsiniz.

## <a name="invoice-totals-matching"></a> Fatura toplamları eşleştirme
Fatura toplamları eşleştirmesini, toplam fatura tutarlarının beklenen tutarlar ile aralarındaki farkın kabul edilebilir bir düzeyden fazla olmadığından emin olmak için kullanabilirsiniz. Aşağıdaki tabloda gösterildiği gibi, altı toplam Fatura toplamları eşleştirme detayları sayfasında karşılaştırılır. Fatura toplamları için izin verilebilir tolerans %20 ise, toplam iskonto tutarı yüzdesindeki %100'lük fark bir eşleştirme tutarsızlığı olarak kabul edilir.

| Toplam alanı    | Gerçek fatura toplamı | Beklenen fatura toplamı | Fark yüzdesi | Eşleştirme durumu |
|----------------|----------------------|------------------------|---------------------|--------------|
| Kalan        | 495,00               | 495,00                 | %0                  | Başarılı       |
| Toplam iskonto | 0,00                 | 9,90                   | %100                | Basarisiz       |
| Masraflar        | 64,90                | 64,90                  | %0                  | Başarılı       |
| Satış vergisi      | 139,98               | 137,50                 | %2                  | Başarılı       |
| Yuvarlama      | 0,00                 | 0,00                   | %0                  | Başarılı       |
| Fatura tutarı | 699,88               | 687,50                 | %2                  | Başarılı       |

Tüzel kişilik için fatura toplamları eşleştirmesi, Borç hesapları parametreleri sayfasındaki Fatura toplamlarını eşleştir tuşu tarafından denetlenir. Eşleştirme beklenen fatura toplamları ve gerçek fatura toplamlarının üzerinde gerçekleştirilir. Beklenen fatura toplamları; fiyatlar, giderler ve satınalma siparişindeki satış vergisi bilgilerini ve faturadaki miktarlar kullanarak hesaplanır.

## <a name="two-way-price-totals-matching"></a> İki yönlü, fiyat toplamları eşleşirmesi
Çift yönlü eşleştirmeyi satınalma siparişi ve fatura üzerindeki fiyat bilgilerinin arasındaki farkın kabul edilebilir tolerans içinde olduğundan emin olmak kullanın. Faturadaki her bir satırın net tutarıyla ilgili fiyat bilgilerini ve tüm bekleyen ve önceden nakledilmiş fatura satırlarını, karşılık gelen satınalma siparişi satırının net tutarıyla karşılaştırabilirsiniz. Buna fiyatı toplamları eşleştirmesi denir. 

Fiyatı toplamları eşleştirmesi bir yüzdeye, bir tutara veya yüzde ve tutara dayanabilir. 

Bir satınalma fiyatı toplamı yüzdesi belirtilmişse, aşağıdaki tabloda gösterildiği gibi beş alan karşılaştırılır. Satınalma fiyat toplam tolerans yüzdesi %10 olduğu için %50 fiyat toplamı farkı yüzdesi bir eşleştirme tutarsızlığını temsil eder.

| Eşleştirme durumu | Fatura net tutarı | Beklenen net tutar | Eşleşmeyen satınalma fiyatı toplamı (fark tutarı) | Eşleşmeyen satınalma fiyatı toplamı yüzdesi (fark yüzdesi) | Satınalma fiyatı toplam tolerans yüzdesi |
|--------------|--------------------|---------------------|--------------------------------------------------|-----------------------------------------------------------------|----------------------------------------|
| Başarılı       | 105,00             | 100,00              | 5,00                                             | %5                                                              | %10                                    |
| Basarisiz       | 150,00             | 100,00              | 50,00                                            | %50                                                             | %10                                    |

Bir satınalma fiyatı toplamı toplamı belirtilmişse, aşağıdaki tabloda gösterildiği gibi beş alan karşılaştırılır. Satınalma fiyat toplam tolerans tutarı 100,00 olduğu için 105,00 fiyat toplamı farkı tutarı bir eşleştirme tutarsızlığını temsil eder.

| Eşleştirme durumu | Fatura net tutarı | Beklenen net tutar | Eşleşmeyen satınalma fiyatı toplamı (fark tutarı) | Muhasebe para birimi cinsinden eşleşmeyen satınalma fiyatı toplamı (fark tutarı) | Satınalma toplam fiyatı toleransı |
|--------------|--------------------|---------------------|--------------------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Başarılı       | 150,00             | 100,00              | 50,00                                            | 50,00                                                                   | 100,00                         |
| Basarisiz       | 205,00             | 100,00              | 105,00                                           | 105,00                                                                  | 100,00                         |

Eğer fiyat toplamları eşleştirmesi, bazen aşılmaması gereken tutar olarak da adlandırılan, bir yüzde toleransı ve tolerans miktarı ile ayarlandıysa, bir satırın eşleştirme tutarsızlığına sahip olup olmadığı değerlendirilirken her iki tolerans da dikkate alınır. Eğer yüzde ya toplam belirlenen toleransı aşarsa, aşağıdaki tablonun 150,00 ve 205,00 satırlarında gösterildiği gibi, satırın eşleştirme tutarsızlığı vardır.

| Eşleştirme durumu | Fatura net tutarı | Beklenen net tutar | Eşleşmeyen satınalma fiyatı toplamı yüzdesi (fark yüzdesi) | Satınalma fiyatı toplam tolerans yüzdesi | Muhasebe para birimi cinsinden eşleşmeyen satınalma fiyatı toplamı (fark tutarı) | Satınalma toplam fiyatı toleransı |
|--------------|--------------------|---------------------|-----------------------------------------------------------------|----------------------------------------|-------------------------------------------------------------------------|--------------------------------|
| Başarılı       | 105,00             | 100,00              | %5                                                              | %10                                    | 5,00                                                                    | 100,00                         |
| Basarisiz       | 150,00             | 100,00              | %50                                                             | %10                                    | 50,00                                                                   | 100,00                         |
| Basarisiz       | 205,00             | 100,00              | %105                                                            | %10                                    | 105,00                                                                  | 100,00                         |

Tüzel kişilik için iki yönlü eşleştirme, Borç hesapları parametreleri sayfasındaki Satır eşleştirme ilkesi alanı tarafından denetlenir. Eşleştirme ilkesi geçersiz kılmaya izin ver alanındaki seçime göre, Eşleştirme ilkesi sayfasındaki belirli bir satıcı, madde veya madde ve satıcı kombinasyonu için ve Satınalma siparişi sayfasındaki belirli bir satınalma siparişi için iki yönlü eşleştirme seçilebilir.

Tüzel kişilik için Fiyat toplamları eşleştirmesi, Borç hesapları parametreleri sayfasındaki Fiyat toplamlarını eşleştir alanı tarafından denetlenir. Satınalma fiyatı toplam tolerans yüzdesi ve tolerans tutarı (aşılmaması gereken tutar) da bu sayfada belirtilir.

## <a name="two-way-net-unit-price-matching"></a> İki yönlü, net birim fiyatı eşleştirmesi
Çift yönlü eşleştirmeyi satınalma siparişi ve fatura üzerindeki fiyat bilgilerinin arasındaki farkın kabul edilebilir tolerans içinde olduğundan emin olmak kullanın. Faturanın üzerindeki her madde için net birim fiyatının fiyat bilgisini karşılaştırabilirsiniz. Buna net birim fiyatı eşleştirmesi denir. 

Aşağıdaki tabloda gösterildiği gibi, dokuz satır tutarı Fatura eşleştirme detayları sayfasında karşılaştırılır. Net birim fiyatı eşleştirmesi için izin verilebilir fiyat toleransı %10 ise, net birim fiyatındaki %22,61'lik fark bir eşleştirme tutarsızlığı olarak kabul edilir.

| Satır alanı                    | Fatura değeri | Satınalma siparişi değeri | Fark yüzdesi | Eşleştirme durumu |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Birim fiyat                    | 55,40         | 55,38                | %0                  | Başarılı       |
| Fiyat birimi                    | 1,00          | 1,00                 | %0                  | Başarılı       |
| Satınalmadaki masraflar          | 50,00         | 0,00                 | %100                | Basarisiz       |
| İskonto                      | 0,00          | 0,00                 | %0                  | Başarılı       |
| İskonto yüzdesi              | 0,00          | 0,00                 | %0                  | Başarılı       |
| Çok satırlı iskonto            | 0,00          | 0,00                 | %0                  | Başarılı       |
| Çok satırlı iskonto yüzdesi | 0,00          | 0,00                 | %0                  | Başarılı       |
| Net tutar                    | 271,60        | 221,52               | %22,61              | Basarisiz       |
| Net birim fiyatı                | 67,9000       | 55,3800              | %22,61              | Basarisiz       |

Tüzel kişilik için iki yönlü eşleştirme, Borç hesapları parametreleri sayfasındaki Satır eşleştirme ilkesi alanı tarafından denetlenir. Eşleştirme ilkesi geçersiz kılmaya izin ver alanındaki seçime göre, Eşleştirme ilkesi sayfasındaki belirli bir satıcı, madde veya madde ve satıcı kombinasyonu için ve Satınalma siparişi sayfasındaki belirli bir satınalma siparişi için iki yönlü eşleştirme seçilebilir. 

Tüzel kişilik için net birim fiyatı eşleştirmesi, Borç hesapları parametreleri sayfasındaki Fatura eşleştirme doğrulamasını etkinleştir alanı tarafından denetlenir. Net Birim Fiyat tolerans yüzdeleri; maddeler, madde grupları, satıcılar, satıcı grupları, madde ve satıcı birleşimleri veya tüzel kişilik için Fiyat toleransları sayfasını kullanarak yapılandırılabilir.

## <a name="two-way-price-totals-matching-and-net-unit-price-matching"></a> Çift yönlü fiyat toplamları eşleştirmesi ve net birim fiyatı eşleştirmesi
Çift yönlü fiyat toplamları eşleştirmesi ve net birim fiyatı eşleştirmesini birlikte kullanabilirsiniz. Bu örnek, aşağıdaki yapılandırmayı varsayar:

-   USB sürücü öğesi için net birim fiyat toleransı %10'dur.
-   Tüzel kişilik için fiyat eşleştirme tolerans toplamı %15 veya 500,00'dür.

Satınalma siparişi aşağıdaki satırı içerir.

| Madde kodu | Miktar | Birim fiyat | Net tutar |
|-------------|----------|------------|------------|
| USB Sürücü   | 1.000    | 10,00      | 10.000,00  |

Aşağıdaki tabloda gösterildiği şekilde üç fatura girilir. Fatura 3 için bir fatura eşleştirme tutarsızlığı vardır çünkü 1.880,00 miktarındaki bir fark, satınalma fiyatı toplam toleransı olan 500,00'ü aşmaktadır. Fiyat toplamları eşleştirmesi için, fatura net tutarı daha önce nakledilen tüm faturaları, üzerinde çalışmakta olduğunu faturaya ekler.

| Madde kodu          | Miktar | Birim fiyat | Net tutar | Fiyat eşleme | Fiyat toplamı eşleştirme |
|----------------------|----------|------------|------------|-------------|-------------------|
| Fatura 1: USB Sürücü | 800      | 10,80      | 8.640,00   | Başarılı      | Başarılı            |
| Fatura 2: USB Sürücü | 100      | 10,80      | 1.080,00   | Başarılı      | Başarılı            |
| Fatura 3: USB Sürücü | 200      | 10,80      | 2.160,00   | Başarılı      | Basarisiz            |
| Toplam                |          |            | 11.880,00  |             |                   |

## <a name="three-way-matching"></a>Üç yönlü eşleştirme

Satınalma siparişi ve fatura üzerindeki fiyat bilgisinin arasındaki farkın kabul edilebilir tolerans içinde olduğundan ve faturadaki miktarın, buna karşı gelen ürün girişindekiyle eşleştiğinden emin olmak için üç yönlü eşleşmeyi kullanın

Fatura eşleştirme detayları sayfasında, iki yönlü eşleştirmede kullanılan aynı satır tutarları karşılaştırılır. Ayrıca, faturadaki miktar, alınan ürününün alış irsaliyesindeki miktarlar ile eşleştirilir. Eğer fatura miktarı, eşleştirilen ürün girişi miktarından farklılık gösterirse, bir miktar eşleştirme hatası vardır.

| Satır alanı                    | Fatura değeri | Satınalma siparişi değeri | Fark yüzdesi | Eşleştirme durumu |
|-------------------------------|---------------|----------------------|---------------------|--------------|
| Birim fiyat                    | 55,40         | 55,38                | %0                  | Başarılı       |
| Fiyat birimi                    | 1,00          | 1,00                 | %0                  | Başarılı       |
| Satınalmadaki masraflar          | 50,00         | 0,00                 | %100                | Basarisiz       |
| İskonto                      | 0,00          | 0,00                 | %0                  | Başarılı       |
| İskonto yüzdesi              | 0,00          | 0,00                 | %0                  | Başarılı       |
| Çok satırlı iskonto            | 0,00          | 0,00                 | %0                  | Başarılı       |
| Çok satırlı iskonto yüzdesi | 0,00          | 0,00                 | %0                  | Başarılı       |
| Net tutar                    | 271,60        | 221,52               | %22,61              | Basarisiz       |
| Net birim fiyatı                | 67,9000       | 55,3800              | %22,61              | Basarisiz       |

| Satır alanı                     | Fatura değeri | Eşleştirme durumu |
|--------------------------------|---------------|--------------|
| Fatura miktarı               | 4,00          |              |
| Eşleşen toplam ürün girişi | 0,00          | Basarisiz       |

Tüzel kişilik için üç yönlü eşleştirme, Borç hesapları parametreleri sayfasındaki Satır eşleştirme ilkesi alanı tarafından denetlenir. Eşleştirme ilkesi geçersiz kılmaya izin ver alanındaki seçime göre, Eşleştirme ilkesi sayfasındaki belirli bir satıcı, madde veya madde ve satıcı kombinasyonu için ve Satınalma siparişi sayfasındaki belirli bir satınalma siparişi için üç yönlü eşleştirme seçilebilir.

## <a name="charges-matching"></a> Gider eşleştirme
Gider eşleştirmesini, gider tutarlarının beklenen tutarlar ile aralarındaki farkın kabul edilebilir bir yüzdeden fazla olmadığından emin olmak için kullanabilirsiniz. Faturaya ve satınalma siparişine uygulanan her bir gider kodu için toplam tutarlar, Gider değerlerini karşılaştır - Fatura: sayfasında, aşağıdaki tabloda gösterildiği gibi karşılaştırılır. Gider kodu için izin verilebilir tolerans %25 ise, Lisans giderleri kodu yüzdesindeki %99,999,999,999.99'lük fark bir eşleştirme tutarsızlığı olarak kabul edilir.

> [!NOTE] 
> %99,999,999,999.99'lük bir varyans yüzdesi farkı, satınalma siparişine göre beklenen tutarın sıfır olduğunu ve faturadaki gerçek tutarın pozitif bir değer olduğu anlamına gelir. 

| Giderler eşleştirme durumu | Fatura masrafları kodu | Gerçek toplam hesaplanan değer | Beklenen toplam hesaplanan değer | Değişken tutar | Fark yüzdesi | Tolerans yüzdesi |
|----------------------|----------------------|-------------------------------|---------------------------------|-----------------|---------------------|----------------------|
| Basarisiz               | Lisans              | 25                            | 0                               | 25              | %99,999,999,999.99  | %25                  |
| Başarılı               | Navlun              | 200                           | 200                             | 0               | %0                  | %25                  |
| Basarisiz               | Hızlandır             | 4                             | 2                               | 2               | %100                | %25                  |

Tüzel kişilik için Giderler eşleştirmesi, Borç hesapları parametreleri sayfasındaki giderleri eşleştir tuşu tarafından denetlenir. Gider toleransları sayfasında giderler için fark tolerans yüzdeleri ayarlayabilirsiniz.

> [!NOTE]
> Gider eşleştirme sadece Gider kodları sayfası üzerinde Satınalma siparişi ve fatura değerlerini karşılaştır seçeneğinin işaretli olduğu gider kodları üzerinde gerçekleştirilir.

## <a name="related-functionality"></a> İlgili işlevsellik
Satıcı faturaları, genellikle satınalma siparişlerine göre değil gerçek sevkiyatları gösteren ürün girişlerine göre oluşturulur. Bazen faturalanan tutarlar satınalma siparişi tutarlarıyla eşleşmez ve bazen sevk edilen miktarlar faturalanan miktarlarla eşleşmez. Bu bilgileri aşağıdaki yollarla yönetmeye yardımcı olabilirsiniz:
-   Ürün girişlerine dayalı satıcı faturası oluşturma. Ürün alış irsaliyeleri faturalar için otomatik olarak önerilir ve hangi ürün girişlerinin kullanılacağını seçebilirsiniz. Gerekirse birden çok satınalma siparişinden belirli ürün girişi satırlarını da seçebilirsiniz.
-   Fatura üzerindeki Faturalanan Miktar ve ürün girişindeki teslim alınan miktar arasındaki farkları onaylayın ve görüntüleyin. Eğer arada fark varsa, faturayı kaydedebilir ve daha sonra farklı ürün alış irsaliyesine eşleyebilir veya faturalanan miktarı alınan miktar ile eşleşecek şekilde değiştirebilirsiniz.
-   Satıcıdan alınan fatura fatura bilgileri ile eşleşen orijinal satınalma siparişine dahil edilmeyen fatura tutarlarını girin. Satınalma siparişleri için giderleri, faturalar için giderlerle karşılaştırabilirsiniz. Gerekirse, faturalara giderler ekleyebilir ve bunları fatura satırlarına tahsis edebilirsiniz.
-   Fatura net birim fiyatı ve satınalma siparişi net birim fiyatı arasındaki fiyat eşleşme tutarsızlıklarını görüntüleyin ve onaylayın. Tüzel kişiliğiniz, maddeler, satıcılarınız için fiyat toleransı yüzdeleri ayarlayabilirsiniz. Satıcı faturası satır fiyatı kabul edilebilir fiyat tolerans içinde değilse, faturayı deftere nakil işleminde onaylanana kadar veya düzeltmeyi satıcıdan alana kadar kaydedebilirsiniz.

Daha fazla bilgi için bkz. [Üç yönlü faturaları eşleştirmek](three-way-matching-policies.md) ve [Borç hesapları fatura eşleştirme doğrulaması](tasks/set-up-accounts-payable-invoice-matching-validation.md). 




