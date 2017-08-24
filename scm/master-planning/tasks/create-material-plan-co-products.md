--- 
title: "Ortak ürünler için malzeme planı oluşturma"
description: "Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4eb36b0de53f40f882950628d55d6ac08ac5fdde
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-material-plan-for-co-products"></a>Ortak ürünler için malzeme planı oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar. Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USP2'dir.


## <a name="create-requirement-for-a-co-product"></a>Ortak bir ürün için gereksinim oluşturun
1. Varsayılan panoya gidin.
2. Satış siparişi işleme ve sorgulama'ya tıklayın.
3. Yeni'yi tıklatın.
4. Satış siparişi'ne tıklayın.
5. Müşteri hesabı alanına bir değer girin.
    * Örnek: US-001  
6. Tamam'a tıklayın.
7. Madde numarası alanına bir değer girin.
    * Örnek: P6003  
8. Miktar alanına bir sayı girin.
    * Örnek: 50000  
9. Kaydet'e tıklayın.

## <a name="create-a-material-plan-for-co-products"></a>Ortak ürünler için malzeme planı oluşturma
1. Master planlama'ya tıklayın.
2. Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * Örnek: MasterPlan  
4. Çalıştır öğesine tıklayın.
5. Eklenecek kayıtlar bölümünü genişletin veya daraltın.
6. Filtre'ye tıklayın.
7. Listede, Alan = Madde numarası alanını seçin.
8. Ölçütler alanına bir değer yazın.
    * Örnek: P6003  
9. Tamam'a tıklayın.
10. Tamam'a tıklayın.
11. Planlı siparişler'e tıklayın.
12. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Ürün numarası alanını 'P6000' değeriyle filtreleyin.
    * Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.  
13. Listede, seçili satırı işaretleyin.
    * Filtre tarafından geri getirilen satırlardan herhangi birini seçin.  
14. Listede, seçili satırdaki bağlantıya tıklayın.
15. İlişkilendirme bölümünü genişletin veya daraltın.
16. Listede, seçili satırdaki bağlantıya tıklayın.
    * Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.  
17. Sayfayı kapatın.


