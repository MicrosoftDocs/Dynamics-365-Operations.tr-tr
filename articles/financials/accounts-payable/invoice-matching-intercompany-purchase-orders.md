---
title: "Fatura eşleştirme ve şirketlerarası satınalma siparişleri"
description: "Bir şirketlerarası ticaret hareketinde yer alan satın alma tüzel kişiliği, borç hesapları fatura eşleştirmesini kullanacak şekilde ayarlanabilir. Bu durumda, şirketlerarası satıcı faturalarının deftere nakledilebilmesi için, hem şirketlerarası ticaret için, hem de borç hesapları fatura eşleştirmesi için deftere nakil gereksinimleri karşılanmalıdır."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3d0eb5c19c07313f4d4c0bac1b9c48375446afd9
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="invoice-matching-and-intercompany-purchase-orders"></a>Fatura eşleştirme ve şirketlerarası satınalma siparişleri

[!INCLUDE [banner](../includes/banner.md)]

Bir şirketlerarası ticaret hareketinde yer alan satın alma tüzel kişiliği, borç hesapları fatura eşleştirmesini kullanacak şekilde ayarlanabilir. Bu durumda, şirketlerarası satıcı faturalarının deftere nakledilebilmesi için, hem şirketlerarası ticaret için, hem de borç hesapları fatura eşleştirmesi için deftere nakil gereksinimleri karşılanmalıdır.

Bu başlıktaki örnekler aşağıdaki şirketlerarası ticaret ayarlarını kullanır:
-   Fabrikam Satınalma, satınalma yapan yasal varlıktır.
-   Fabrikam Satış, satış yapan yasal varlıktır.
-   Müşteri 4020, Fabrikam Satışlar içinde yer alır.
-   Satıcı 3024, Fabrikam Satınalma içinde yer alır.
-   Fabrikam Satınalma, satıcı 3024 için şirketlerarası bilgiler belirtilir. Fabrikam Satışlar, müşteri şirketi olarak belirtilir ve müşteri 4020, Fabrikam Satınalma tüzel varlığa karşılık gelen müşteri hesabı olarak belirtilir.
-   Fabrikam Satış, müşteri 4020 için şirketlerarası bilgiler belirtilir. Fabrikam Satınalma, satıcı şirketi olarak belirtilir ve satıcı 3024, Fabrikam Satınalma tüzel varlığa karşılık gelen satıcı hesabı olarak belirtilir.

Örnekler Fabrikam Satınalma için aşağıdaki borçlar hesabı fatura eşleştirme ayarlarını kullanır:
-   Borç hesapları parametreleri sayfasında, fatura eşleşmesi doğrulama seçeneğini etkinleştirin.
-   Borç hesapları parametreleri sayfasında, Uyuşmazlıkları olan faturayı deftere naklet alanı Onay gerektiriyor seçeneğine ayarlanır.
-   Tüzel kişilik için fiyat tolerans oranı yüzde 2'dir.

## <a name="example-price-matching-and-intercompany-trade"></a> Örnek: Fiyat eşleme ve şirketlerarası ticaret
Şirketlerarası satıcısı faturası ve şirketlerarası müşteri siparişi faturasının net tutarları eşit olmalıdır. Bu zorunluluk, uygulanan tüm fatura eşleştirme onaylarını veya fiyat toleransı yüzdelerini geçersiz kılar. Örneğin, aşağıdaki adımları izleyin.
1.  Fabrikam Satınalma'da müşteri 4020 için SO888 satış siparişini oluşturun. Şirketlerarası satınalma siparişi ICPO222, satıcı 3024 için Fabrikam Satınalma'da otomatik olarak oluşturulur ve satış siparişi ICSO888 Fabrikam Satışlar'da otomatik olarak oluşturulur.
2.  Maddelerin alındığını Fabrikam Satışlar'da kaydedin ve bir sevk irsaliyesini deftere nakledin. ICSO888'in durumu Teslim Edildi olarak değişir. ICPO222'nin durumu Alındı olarak değişir.
3.  Fabrikam Satışlar'da ICSO888 için bir fatura güncelleştirmesi gerçekleştirin. Birim fiyat 0,45 olur ve 100 madde güncelleştirilir.
4.  Fabrikam Satınalma'da ICPO222 için bir fatura oluşturun. Net fiyatı yanlışlıkla 45,00'ten 54,00'e değiştirin. Fiyatın, izin verilen yüzde 2'lik fiyat toleransını aştığını belirtmek üzere bir simge görüntülenir.
5.  Fatura eşleme ayrıntıları sayfasında, farklılıklarıyla deftere nakletmeye izin verecek seçeneği işaretleyin. Satıcı fatura sayfasında Tamam'ı tıklatın. Eğer satıcı faturası şirketlerarası satıcı faturası değilse, nakletme başarılı olur. Ancak, bir şirketlerarası satıcı faturası ile çalıştığınız için, deftere nakil başarısız olur. Şirketlerarası ticaret için şirketlerarası satış siparişindeki fatura toplamları ilgili şirketlerarası satınalma siparişi fatura toplamları ile eşit miktarda olmalıdır. Bu sorunu gidermek için faturadaki net fiyatı, tekrar varsayılan tutar olan 45,00'e değiştirmeniz gerekir.

## <a name="example-quantity-matching-with-intercompany-trade"></a> Örnek: Şirketlerarası ticaretle miktar eşleştirme
Şirketlerarası satınalma siparişi ve şirketlerarası satış siparişi üzerindeki miktarlar eşit olmalıdır. Bu zorunluluk, tüm uygulanan fatura eşleştirme onaylarını geçersiz kılar. Bu örnek şirketlerarası ticaret için aşağıdaki ek ayarı kullanır:
-   Fabrikam Satınalma'da, satıcı 3024 için satınalma siparişi eylem ilkesi, hem müşteri faturasını hem de şirketlerarası satıcı faturasını otomatik olarak deftere nakledecek şekilde ayarlanır.

Bu örnek Fabrikam Satınalma borç hesapları fatura eşleştirme için aşağıdaki ek ayarları kullanır:
-   Madde B-R14 tarafından kullanılan model grubu için madde model grupları sayfasında Alım gereksinimleri seçeneği işaretlidir.
-   Madde B-R14 için eldeki miktar 0'dır (sıfır).

Örneğin, aşağıdaki adımları izleyin.
1.  Fabrikam Satınalma'da müşteri 4020 için SO999 satış siparişini oluşturun. Sipariş bir satır öğesi içerir: birim fiyatı her biri için 1,00 olan, 100 pil (madde B-R14). Şirketlerarası satınalma siparişi ICPO333, satıcı 3024 için Fabrikam Satınalma'da otomatik olarak oluşturulur ve satış siparişi ICSO999 Fabrikam Satışlar'da otomatik olarak oluşturulur.
2.  Fabrikam Satışlar'da ICSO999 için bir fatura güncelleştirmesi gerçekleştirin. Madde stokta olmadığı ve henüz alınmadığı için deftere nakil başarısız olur. Bu nedenle, mali bilgileri güncelleştirilemez.
3.  Maddelerin alındığını Fabrikam Satışlar'da kaydedin ve ICSO999 için bir sevk irsaliyesini deftere nakledin. Fabrikam Satınalma'da ICPO333 için bir ürün girişi otomatik olarak deftere nakledilir. Fabrikam Satınalma'da B-R14 maddesi için alınan miktar 100 olarak değişir.
4.  Fabrikam Satışlar'da ICSO999 için bir fatura güncelleştirmesi gerçekleştirin. Deftere nakil her iki düzel kişilikte de başarılı olur. Fabrikam Satınalma'da B-R14 maddesi için satın alınan miktar 100 olarak değişir. 






