---
title: Ortak ürünler için bir malzeme planı oluşturma
description: Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d910b89330865b0bcf3f6cd05b761506f339a45f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841683"
---
# <a name="create-a-material-plan-for-co-products"></a>Ortak ürünler için bir malzeme planı oluşturma

[!include [banner](../../includes/banner.md)]

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
1. Sayfayı kapatın.
2. Sayfayı kapatın.
3. Master planlama'ya tıklayın.
4. Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, seçili satırdaki bağlantıya tıklayın.
    * Örnek: MasterPlan  
6. Çalıştır öğesine tıklayın.
7. Eklenecek kayıtlar bölümünü genişletin veya daraltın.
8. Filtre'ye tıklayın.
9. Listede, Alan = Madde numarası alanını seçin.
10. Ölçütler alanına bir değer yazın.
    * Örnek: P6003  
11. Tamam'a tıklayın.
12. Tamam'a tıklayın.
13. Planlı siparişler'e tıklayın.
14. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Ürün numarası alanını 'P6000' değeriyle filtreleyin.
    * Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.  
15. Listede, seçili satırı işaretleyin.
    * Filtre tarafından geri getirilen satırlardan herhangi birini seçin.  
16. Listede, seçili satırdaki bağlantıya tıklayın.
17. İlişkilendirme bölümünü genişletin veya daraltın.
18. Listede, seçili satırdaki bağlantıya tıklayın.
    * Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.  
19. Sayfayı kapatın.

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
1. Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.
2. Listede, seçili satırdaki bağlantıya tıklayın.
    * Örnek: MasterPlan  
3. Çalıştır öğesine tıklayın.
4. Eklenecek kayıtlar bölümünü genişletin veya daraltın.
5. Filtre'ye tıklayın.
6. Listede, Alan = Madde numarası alanını seçin.
7. Ölçütler alanına bir değer yazın.
    * Örnek: P6003  
8. Tamam'a tıklayın.
9. Tamam'a tıklayın.
10. Planlı siparişler'e tıklayın.
11. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Ürün numarası alanını 'P6000' değeriyle filtreleyin.
    * Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.  
12. Listede, seçili satırı işaretleyin.
    * Filtre tarafından geri getirilen satırlardan herhangi birini seçin.  
13. Listede, seçili satırdaki bağlantıya tıklayın.
14. İlişkilendirme bölümünü genişletin veya daraltın.
15. Listede, seçili satırdaki bağlantıya tıklayın.
    * Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.  
16. Sayfayı kapatın.
17. Master planlama'ya tıklayın.
18. Master planlama > Kurulum > Master planlama parametreleri'ne gidin.
19. Tüm planlama işlemlerini devre dışı bırak alanında Hayır'ı işaretle.
20. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]