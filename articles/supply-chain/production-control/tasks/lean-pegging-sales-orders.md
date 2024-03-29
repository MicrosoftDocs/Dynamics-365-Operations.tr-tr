---
title: Satış siparişlerinden yalın ilişkilendirme
description: Bu yordam, satış satırındaki maddenin kanbanlar ile üretildiği bir pegging ağacını onaylamaya odaklanır.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8eca21f8bd988ca352c07e839295b3edd9669929
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580636"
---
# <a name="lean-pegging-from-sales-orders"></a>Satış siparişlerinden yalın ilişkilendirme

[!include [banner](../../includes/banner.md)]

Bu yordam, satış satırındaki maddenin kanbanlar ile üretildiği bir pegging ağacını onaylamaya odaklanır. Pegging ağacı doğrulandıktan sonra tüm kanban işleri planlanmaktadır. Bu durum sipariş alan kişinin üretimin hemen başlayabildiğinden emin olmasının gerektiği senaryolar için faydalıdır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam, yalın bir şirkette çalışan gelişmiş siparişi alıcı içindir.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>Kanban kontrollü madde için bir satış siparişi oluşturun
1. Tüm satış siparişleri'ne gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında bir değer girin veya seçin.
    * Kullanım ABD-001.  
4. Tamam'a tıklayın.
5. Madde numarası alanına 'L0001' girin.
6. Miktarı '30' olarak ayarlayın.
    * Olay kanban kuralını tetiklemek için miktarın 24'ten daha yüksek olması önemlidir.  

## <a name="open-a-pegging-tree"></a>Bir ilişkilendirme ağacı açmak 
1. Ürün ve tedarik seçeneğine tıklayın.
2. İlişkilendirme ağacını görüntüle'yi tıklatın.
    * Pegging ağacının satış emri satırındaki gerekli tüm pegginglerin seviyelerini gösterdiğine dikkat edin. Bu durumda, iki düzeyde kanban mevcuttur ve hepsi gerekli bileşenlerdir.  

## <a name="plan-the-pegging-tree"></a>İlişkilendirme ağacını planla
1. Ağaçta 'Satış satırı 000832\Kanban 000558' seçin.
2. Kanban işleri bölümünü genişletin.
    * Kanban işi için iş durumunun planlanmadı olduğuna dikkat edin.  
3. Tüm ilişkilendirme ağacını planla'ya tıkla.
    * Bu, iş değiştirme ilişkilendirme ağacındaki tüm kanban işlerinin iş durumunu planlanmadı'dan planlandı'ya değiştirecektir.  
4. Sayfayı yenileyin.
    * Kanban iş durumunun planlanmadı'dan planlandı'ya dönüştüğüne dikkat edin.  
5. Ağaçta, 'Satış 000832\Kanban 000558\Issue L0001\Kanban 000559 için satır' seçin.
    * İkinci kanban için de iş planlanmıştır çünkü tüm pegging ağacı planlıdır. Kanban iş durumunun planlanmadı'dan planlandı'ya dönüştüğüne dikkat edin.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]