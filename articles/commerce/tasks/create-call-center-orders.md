---
title: " Çağrı merkezi siparişleri oluşturma"
description: Bu yordam bir müşteri arama, yeni bir sipariş oluşturma, bir ürün arama ve müşteriden ödeme tahsil etme için kılavuzluk sağlar.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c875eaa85d9da997b75b296ad9ace99ae1e91798
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594248"
---
# <a name="create-call-center-orders"></a> Çağrı merkezi siparişleri oluşturma

[!include [banner](../includes/banner.md)]

Bu yordam bir müşteri arama, yeni bir sipariş oluşturma, bir ürün arama ve müşteriden ödeme tahsil etme için kılavuzluk sağlar. Bu yordam, USRT demo veri şirketini kullanır ve Satış Siparişi Memurlarına yöneliktir. Ön koşullar: Yordamı tamamlayan kullanıcı Çağrı merkezi kullanıcısı olarak ayarlanır ve en az bir Kaynak kodla Fabrikam Yarı Yıllık Kataloğu yayınlanır.

1. **Perakende ve Ticaret \> Müşteriler \> Müşteri hizmetlerine gidin**.
2. **SearchText** alanında müşteri aramak için arama ölçütü girin.
    * Bu örnek yordam için "Karen" yazın ve **Sekme**'yi seçin.  
3. Ara'yı seçin.
    * Demo veride "Karen" adında tek bir müşteri olduğundan sonuç otomatik olarak seçilir.  
4. **Yeni satış siparişi**'ni seçin.
5. **Satış siparişi** başlığı bölümünü genişletin veya daraltın.
6. Katalog için kaynak kodu seçin.
    * Hiçbir etkin kaynak kodu yoksa bu adımı atlayabilirsiniz.  
7. **Satır ekle**'yi seçin.
8. **Madde numarası** alanına madde arama terimini girin.
    * Bu örnek yordamda '8111' kısmi madde numarasını girin ve Tab tuşuna basın. Bu eylem arama penceresinin açılmasını sağlar.  
9. Satış siparişine eklenecek ürünü seçin.
10. Satış miktarını girin.
11. **Oluştur**'u seçin.
12. Müşteri ödemesini yakalamak için **Tamamla**'yı seçin.
13. **Ekle**'yi seçin.
    * Ekle bağlantısı Ödemeler sekmesinde bulunur. Daraltılmışsa Ödemeler sekmesini genişletin.  
14. Ödeme yöntemini seçin.
    * Bu yordam için nakit ödeme yöntemini seçin.  
15. Sayfayı kapatın.
16. Tutarı girin.
    * Bu yordam için, tutar alanının sol tarafındaki Satış siparişi özet sayfasında görebileceğiniz sipariş bakiyesine eşit bir tutar girin. Bu eylem siparişi tamamen ödenmiş olarak tamamlamanızı sağlar.  
17. **Tamam**'ı seçin.
18. **Gönder**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Teslimat şekline göre işlem tabanlı e-postaları özelleştirme](../customize-email-delivery-mode.md)

[Satış noktasında teslimat şeklini değiştirme](../pos-change-delivery-mode.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]