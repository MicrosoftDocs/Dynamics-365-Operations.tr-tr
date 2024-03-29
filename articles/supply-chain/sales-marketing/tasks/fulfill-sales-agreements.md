---
title: Satış sözleşmelerini karşılama
description: Bu yordam, bir satış anlaşmasının satış siparişleri ile ilişkilendirerek nasıl yerine getirileceğini gösterir.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe26d528e42da61d47fd2448e071bf9025c08f5d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573405"
---
# <a name="fulfill-sales-agreements"></a>Satış sözleşmelerini karşılama

[!include [banner](../../includes/banner.md)]

Bu yordam, bir satış anlaşmasının satış siparişleri ile ilişkilendirerek nasıl yerine getirileceğini gösterir. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Bu kılavuzu başlatmadan önce, "Ürün değeri taahhüdü" türünde etkin bir satış anlaşmanız olduğundan emin olun. Alternatif olarak, "Satış anlaşmaları oluşturma" adı verilen görev kılavuzunu çalıştırabilirsiniz.  




## <a name="release-a-sales-order-from-the-agreement"></a>Anlaşmadaki bir satış siparişini sevk etme
1. Sales and marketing > Sales agreements > Sales agreements (Satış ve pazarlama > Satış anlaşmaları > Satış anlaşmaları) menüsüne gidin
2. Listede, siparişini sevk etmek istediğiniz anlaşmayı açın.
3. Eylem Bölmesinde, Satış anlaşması'nı tıklatın.
4. Sevk emri'ni tıklatın.
    * Sevk emrini oluştur sayfasının üstündeki metinde gösterildiği üzere, satış siparişi satırları için gerekli ayrıntılar anlaşmanın miktar mı yoksa değer esaslı mı olduğuna bağlı olarak farklılık gösterir.  
    * Bu kılavuzdaki anlaşma "Ürün değeri taahhüdü" türündedir. Bu nedenle, bu sayfanın Satırlar bölümü boştur. Taahhüt miktarı esas alıyorsa, satır bilgilerinin sözleşmeden kopyalanması gerekir.  
5. Oluştur'a tıklayın.
    * İleti, bir satış siparişinin oluşturulduğunu bildirir. Sipariş hiçbir satır içermediğinden, serbest bırakma işlemini tamamlamak için sipariş satırı ayrıntılarını eklemeniz gerekir.   
6. Sayfayı kapatın.
7. Sayfayı kapatın.
8. Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.
9. Listede, önceki görevde sevk edilen siparişin sonucunda oluşturulan siparişi bulun ve açın.
10. Satır ekle'ye tıklayın.
11. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
12. Ürün numarası alanında, ilişkili satış anlaşmasında belirtilen ürünü bulun ve seçin.
13. Miktar alanına bir sayı girin.
    * İlişkili satış anlaşmasının değeri altındaki Net tutarı getiren bir miktar girdiğinizden emin olun.  
    * Satış siparişi anlaşmaya bağlı olduğundan, üzerinde anlaşılan iskonto yüzdesinin sipariş satırına uygulanacağını unutmayın.  
14. Satırı güncelleştir öğesine tıklayın.
15. İlişik öğesine tıklayın.
    * İlişik anlaşma sayfası, satırın serbest bırakıldığı anlaşmanın kodunu ve şartlarını gösterir.  
16. Sayfayı kapatın.
17. Eylem Bölmesinde, Genel öğesine tıklayın.
18. İlişik satış anlaşması'nı tıklatın.
19. Satır ayrıntıları bölümünü genişletin.
20. Karşılama sekmesini tıklatın.
    * Karşılama sekmesi, bu taahhüt ile ilişkilendirilmiş tüm satış siparişlerinin bir özetinin ve karşılama durumlarının yanı sıra henüz sevk edilmemiş tutarı veya miktarı gösterir.   
21. Sayfayı kapatın.
22. Sayfayı kapatın.
23. Sayfayı kapatın.

## <a name="apply-sales-agreement-in-the-order-process"></a>Sipariş işleminde satış anlaşmasını uygulama
1. Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.
4. Listede, satış anlaşmasında belirtilen müşteriyi bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Genel bölümünü genişletin.
7. Satış anlaşması kodu alanında, aramayı açmak için açılır menü düğmesini tıklatın.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Evet'i tıklatın.
10. Tamam'a tıklayın.
11. Listede, seçili satırı işaretleyin.
12. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
13. Ürün numarası alanında, ilişkili satış anlaşmasında belirtilen ürünü bulun ve seçin.
14. Listede, seçili satırdaki bağlantıya tıklayın.
15. Kaydet'i tıklatın.
16. Eylem Bölmesinde, Çek ve paketle öğesine tıklayın.
17. Sevk irsaliyesini deftere naklet öğesine tıklayın.
18. Parametreler bölümünü genişletin.
19. Deftere nakil alanında 'Evet'i seçin.
20. Tamam'a tıklayın.
21. Tamam'a tıklayın.
22. Eylem Bölmesinde, Genel öğesine tıklayın.
23. İlişik satış anlaşması'nı tıklatın.
24. Karşılama sekmesini tıklatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]