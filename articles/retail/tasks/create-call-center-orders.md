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
ms.openlocfilehash: 4867ad67dc570ab42420ba12fc7dc2da6b5ba503
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "334324"
---
# <a name="create-call-center-orders"></a> Çağrı merkezi siparişleri oluşturma

[!include[task guide banner](../includes/task-guide-banner.md)]

Bu yordam bir müşteri arama, yeni bir sipariş oluşturma, bir ürün arama ve müşteriden ödeme tahsil etme için kılavuzluk sağlar. Bu yordam, USRT demo veri şirketini kullanır ve Satış Siparişi Memurlarına yöneliktir. Ön koşullar: Yordamı tamamlayan kullanıcı Çağrı merkezi kullanıcısı olarak ayarlanır ve en az bir Kaynak kodla Fabrikam Yarı Yıllık Kataloğu yayınlanır.

1. Perakende ve ticaret > Müşterileri > Müşteri hizmetlerine gidin.
2. SearchText alanında müşteri aramak için arama ölçütü girin.
    * Bu örnek yordam için 'karen' yazın ve sekme tuşuna basın.  
3. Ara'ya tıklayın.
    * Demo veride Karen adında tek bir müşteri olduğundan otomatik olarak seçililer.  
4. Yeni satış siparişine tıklayın.
5. Satış siparişi başlığı bölümünü genişletin veya daraltın.
6. Katalog için kaynak kodu seçin.
    * Hiçbir etkin Kaynak kodu yoksa, Kaynak alanını kapatıp bu adımı atlayabilirsiniz.  
7. Satır ekle'ye tıklayın.
8. Madde numarası alanına madde arama terimini girin.
    * Bu örnek yordamda "8111" kısmi madde numarasını girin ve sekme tuşuna basın. Bu madde arama penceresinin açılmasını sağlar.  
9. Satış siparişine eklenecek ürünü seçin
10. Satış miktarını girin.
11. Oluştur'a tıklayın.
12. Müşteri ödemesi yakalamayı tamamla'ya tıklayın.
13. Ekle öğesini tıklatın.
    * Ekle bağlantısı Ödemeler sekmesinde bulunur. Daraltılmışsa Ödemeler sekmesini genişletin.  
14. Ödeme yöntemini seçin.
    * Bu yordam için nakit ödeme yöntemini seçin.  
15. Sayfayı kapatın.
16. Tutarı girin.
    * Bu yordam için, tutar alanının sol tarafındaki Satış siparişi özet sayfasında görebileceğiniz sipariş bakiyesine eşit bir tutar girin. Siparişi tamamen ödenmiş olarak tamamlamanızı sağlar.  
17. Tamam'a tıklayın.
18. Gönder'i tıklatın.

