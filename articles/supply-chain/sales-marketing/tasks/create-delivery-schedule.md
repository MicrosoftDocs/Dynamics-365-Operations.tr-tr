---
title: Teslimat planı oluşturun
description: Bu prosedür, satış siparişi için teslimat oluşturmayı göstermektedir.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dccc90321977382c7625ca1785427a6d26a14f27
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835655"
---
# <a name="create-delivery-schedule"></a>Teslimat planı oluşturun

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, satış siparişi için teslimat oluşturmayı göstermektedir. Teslimat planı, bir siparişteki veya teklifteki miktarın birden fazla sevkiyatlar halinde teslim edilmesi istendiği zaman kullanılır. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.


## <a name="create-delivery-schedule"></a>Teslimat planı oluşturun
1. Tüm satış siparişleri'ne gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında bir değer girin veya seçin.
4. Tamam'a tıklayın.
5. Madde numarası alanında bir değer girin veya seçin.
6. Miktar alanına 1'den büyük bir sayı girin.
7. Satış siparişi satırına tıklayın.
8. Teslimat planı öğesine tıklayın.
    * Teslimat planı sayfası, sipariş satırı toplam miktarının müşteriye teslim edileceği sevkiyat sayısını belirtebildiğiniz yerdir.    
    * Varsayılan olarak, sistem orijinal satış satırının toplam miktarını ve diğer teslimat ayrıntılarını ilk teslimat planı satırına kopyalar. Bu örnekte iki sevkiyat planı oluşturacağız ve ikinci sevkiyatın tarihi, ilkinden bir hafta sonra olacak.  
9. Miktar alanına toplam miktarın bir kısmı olan bir sayı girin.
10. Yeni'yi tıklatın.
11. Miktar alanına, kalan miktarı girin.
12. Talep edilen sevk tarihi alanına, ilk teslimat satırı tarihinden bir hafta sonrasına denk gelen tarihi girin.
    * Masraf dönüştürme hızlı sekmesindeki iki seçenek, masrafların, orijinal sipariş satırına atandıktan sonra teslimat planı satırlarına nasıl dağıtılmasını istediğinizi belirler. Brüt tutarları kopyala'yı seçerseniz, her satıra aynı masraf tutarı kopyalanır. Teslimat satırlarına tahsis et seçeneği, masrafı teslimat satırlarına eşit olarak böler.  
    * Yalnızca sabit masraflar bölünebilir, ancak değişken masraflar satırlara kopyalanmaya devam eder.  
13. İmleci ikinci teslimat satırından uzaklaştırarak sayfayı güncelleştirin.
    * Toplam ve Kalan alanlarına bakarak, teslimat planı satırlarına tahsis edilen toplam miktarı izleyebilirsiniz. Kalan miktar sıfır olduğunda, orijinal satırdan alınan tüm miktar plana tahsis edilmiştir.   
14. Tamam'a tıklayın.
    * Teslimat planı artık diğer sipariş satırlarına kopyalandı.   
    * Ticari satırı olarak anılan orijinal sipariş satırı, birden fazla teslimatlı bir Siparişe dönüştürülmüştür. Farklı bir simgeyle işaretlenir ve teslimat satırlar için üst bilgi işlevi görür.  
    * Teslimat satırları olarak başvurulan iki yeni satır bir teslimat planı oluşturur. Sipariş orijinal satıra göre değil, bu satırlara göre işlenir. Onay makbuzu, malzeme çekme listesi, sevk irsaliyesi, fatura gibi belgeler yazdırılırken yalnızca teslimat satırları gösterilir.   
    * Teslimat satırları farklı teslim tarihleri; miktarları; teslimat şekilleri; tesis ve ambar gibi depolama boyutları içerebilir. Ancak, ürün boyutları mutlaka ticari satırındaki boyutlarla eşleşmek zorundadır ve değiştirilemez.  
15. Miktar alanına, mevcut sayıdan daha büyük bir sayı girin.
16. Miktarın yeniden hesaplanmasının etkisini görmek için ticari satırını seçin.
17. Eylem Bölmesinde, Çek ve paketle öğesine tıklayın.
18. Sevk irsaliyesini deftere naklet'e tıklayın.
19. Parametreler bölümünü genişletin.
20. Miktar alanında, 'Tümü' öğesini seçin.
    * Sevk irsaliyesinin orijinal sipariş satırı için değil, bu iki teslimat planı satırı için oluşturulacağını unutmayın.  
21. Sevk irsaliyesi yazdır alanında Evet'i seçin.
22. Tamam'a tıklayın.
23. Evet'i tıklatın.
24. Sayfayı kapatın.

