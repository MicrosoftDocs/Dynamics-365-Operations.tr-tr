---
title: Satış siparişinden satınalma siparişi oluşturma
description: Bu yordam, bir satış siparişine göre nasıl satınalma siparişi oluşturulacağını gösterir.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7991476b86ace92cda513ae8906c62ba7fbbe915
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547441"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Satış siparişinden satınalma siparişi oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir satış siparişine göre nasıl satınalma siparişi oluşturulacağını gösterir. Satınalma siparişindeki ürün miktarları kaynak satış siparişinin talebini karşılayacak şekilde belirlenir. Satış talebinin bu şekilde karşılanması, daha kapsamlı ve iyi bir Dağıtım Gereksinimleri Planlaması yöntemi için alternatiftir. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Satış siparişinden satınalma siparişi oluşturma
1. Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.
4. Listede, istenen kaydı bulun ve seçin.
5. Tamam'ı tıklatın.
6. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
7. Listede, istenen kaydı bulun ve seçin.
    * USMF kullanıyorsanız, D0001 öğesini seçebilirsiniz.  
8. Miktar alanına bir sayı girin.
9. Satır ekle'ye tıklayın.
10. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
11. Listede, istenen kaydı bulun ve seçin.
    * USMF kullanıyorsanız, T0020 öğesini seçebilirsiniz.  
12. Listede, seçili satırdaki bağlantıya tıklayın.
13. Miktar alanına bir sayı girin.
14. Kaydet'i tıklatın.
15. Eylem Bölmesinde, Satış siparişi öğesine tıklayın.
16. Satın alma siparişini tıklatın.
    * Satınalma siparişi oluştur sayfası, satış siparişinden kopyalanmış tüm açık satış siparişi satırlarını listeler. Sipariş ayrıntılarını gözden geçirebilir ve gerekiyorsa satınalma oluşturmadan önce satınalma miktarı ve fiyatlandırma koşulları gibi seçilen ayrıntıları değiştirebilirsiniz.  
17. Tümünü dahil et seçeneğini belirleyin.
    * Satış siparişi satırlarının yalnızca bir alt kümesi için satınalma siparişleri oluşturmak istiyorsanız, bunları tek tek seçin.  
    * Satıcı hesabı alanı bir satıcı numarası ile önceden doldurulmuş olabilir. Varsayılan satıcı ürün için (ilişkili ürün kapsamında) ayarlanmışsa, bu satıcı satıra kopyalanır. Aksi takdirde, manüel olarak bir satıcı girmeniz gerekir.  Bu kılavuzda, Satıcı hesabı alanının önceden bir değer içerip içermediğine bakılmaksızın, aşağıdaki adımlar sizi her satır için farklı olan yeni bir satıcı seçmeniz için yönlendirir.  
18. Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
19. Listede, istenen kaydı bulun ve seçin.
20. Listede, seçili satırdaki bağlantıya tıklayın.
21. İkincil sipariş satırını seçin.
22. Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
23. Listede, istenen kaydı bulun ve seçin.
24. Listede, seçili satırdaki bağlantıya tıklayın.
25. Doğrula'ya tıklayın.
26. Tamam'a tıklayın.
    * İleti, bir veya daha fazla satınalma siparişinin oluşturulduğunu bildirir. Sistem, satış siparişi satırları için belirlenmiş her satıcıya ait ayrı bir satınalma siparişi oluşturur. Başka bir deyişle, aynı satıcı tarafından birden fazla satış siparişi satırı sağlanırsa, birden fazla satıra sahip tek bir satınalma siparişi oluşturulur.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Satış siparişlerinden oluşturulan satınalma siparişlerini gözden geçirin.
1. Eylem Bölmesinde, Genel öğesine tıklayın.
2. İlgili siparişleri tıklatın.
    * İlgili siparişler sayfası, satış siparişinden oluşturulan tüm siparişleri listeler. Bu örnekte, sırasıyla iki farklı satıcı için oluşturulan iki satınalma siparişi vardır.  
3. Satınalma siparişi alanındaki bağlantıyı izlemek için tıklayın.
    * Her satınalma siparişi satırı, satın almaya yol açan satış siparişi satırıyla ilişkilendirilmiştir. Satış siparişinin ilişkisi Satır ayrıntıları FastTab'inde Ürün sekmesinde, Referans türü, Referans numarası ve Referans lotu alanlarında belirtilir.  
4. Satır ayrıntıları bölümünü genişletin veya daraltın.
5. Ürün sekmesine tıklayın.
    * Referans lotu, geçerli satınalmadan kaynaklanan maliyetlerin eklenmiş satış siparişine uygulanacağını garanti eder.  
    * Başvuru numarası alanındaki bağlantıyı açarak kaynak satış siparişine gidebilirsiniz.  

