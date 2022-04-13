---
title: Ortak ürünler için bir malzeme planı oluşturma
description: Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27bba54db915b7ccc31fda43a00a8c9435493e07
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469547"
---
# <a name="create-a-material-plan-for-co-products"></a>Ortak ürünler için bir malzeme planı oluşturma

[!include [banner](../../includes/banner.md)]

Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar. Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USP2'dir.

## <a name="create-requirement-for-a-co-product"></a>Ortak bir ürün için gereksinim oluşturun

1. **Satış ve pazarlama \> Çalışma alanları \> Satış siparişi işleme ve sorgulama**'ya gidin.
1. **Yeni**'yi seçin.
1. **Satış siparişi**'ni seçin.
1. **Müşteri hesabı** alanına bir değer girin.
    * Örnek: US-001  
1. **Tamam**'ı seçin.
1. **Madde numarası** alanına bir değer girin.
    * Örnek: P6003  
1. **Miktar** alanına bir sayı girin.
    * Örnek: 50000  
1. **Kaydet**'i seçin.

## <a name="create-a-material-plan-for-co-products"></a>Ortak ürünler için malzeme planı oluşturma

1. Sayfayı kapatın.
1. Sayfayı kapatın.
1. **Master planlama**'yı seçin.
1. **Plan** alanında, aramayı açmak için açılır menü düğmesini seçin.
1. Listeden, seçilen satırdaki bağlantıyı seçin.
    * Örnek: MasterPlan  
1. **Çalıştır**'ı seçin.
1. **Eklenecek kayıtlar** bölümünü genişletin veya daraltın.
1. **Filtre**'yi seç.
1. Listede, **Alan** =  *Madde numarası* satırını seçin.
1. **Ölçütler** alanına bir değer yazın.
    * Örnek: P6003  
1. **Tamam**'ı seçin.
1. **Tamam**'ı seçin.
1. **Planlı siparişler**'i seçin.
1. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, **Öğe numarası** alanını 'P6000' değeriyle filtreleyin.
    * Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.  
1. Listede, seçili satırı işaretleyin.
    * Filtre tarafından geri getirilen satırlardan herhangi birini seçin.  
1. Listeden, seçilen satırdaki bağlantıyı seçin.
1. **İlişkilendirme** bölümünü genişletin.
1. Listeden, seçilen satırdaki bağlantıyı seçin.
    * Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.  
1. Sayfayı kapatın.

## <a name="create-a-second-requirement-for-a-co-product"></a>Ortak bir ürün için ikinci bir gereksinim oluşturma

1. **Satış ve pazarlama \> Çalışma alanları \> Satış siparişi işleme ve sorgulama**'ya gidin.
1. **Yeni**'yi seçin.
1. **Satış siparişi**'ni seçin.
1. **Müşteri hesabı** alanına bir değer girin.
    * Örnek: US-001  
1. **Tamam**'ı seçin.
1. **Madde numarası** alanına bir değer girin.
    * Örnek: P6003  
1. **Miktar** alanına bir sayı girin.
    * Örnek: 50000  
1. **Kaydet**'i seçin.

## <a name="create-a-second-material-plan-for-co-products"></a>Ortak ürünler için ikinci bir malzeme planı oluşturma

1. **Plan** alanında, aramayı açmak için açılır menü düğmesini seçin.
2. Listeden, seçilen satırdaki bağlantıyı seçin.
    * Örnek: MasterPlan  
3. **Çalıştır**'ı seçin.
4. **Eklenecek kayıtlar** bölümünü genişletin veya daraltın.
5. **Filtre**'yi seç.
6. Listede, **Alan** =  *Madde numarası* satırını seçin.
7. *Ölçütler* alanına bir değer yazın.
    * Örnek: P6003  
8. **Tamam**'ı seçin.
9. **Tamam**'ı seçin.
10. **Planlı siparişler**'i seçin.
11. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, **Öğe numarası** alanını 'P6000' değeriyle filtreleyin.
    * Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.  
12. Listede, seçili satırı işaretleyin.
    * Filtre tarafından geri getirilen satırlardan herhangi birini seçin.  
13. Listeden, seçilen satırdaki bağlantıyı seçin.
14. **İlişkilendirme** bölümünü genişletin veya daraltın.
15. Listeden, seçilen satırdaki bağlantıyı seçin.
    * Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.  
16. Sayfayı kapatın.
17. **Master planlama**'yı seçin.
18. **Master planlama \> Kurulum \> Master planlama parametreleri**'ne gidin.
19. **Tüm planlama işlemlerini devre dışı bırak** alanında *Hayır*'ı işaretleyin.
20. Sayfayı kapatın.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]