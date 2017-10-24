--- 
title: " Çağrı merkezi siparişleri oluşturma"
description: "Bu yordam bir müşteri arama, yeni bir sipariş oluşturma, bir ürün arama ve müşteriden ödeme tahsil etme için kılavuzluk sağlar."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f702690f72b3e299f6c2744da326a23d5753eb5d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

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


