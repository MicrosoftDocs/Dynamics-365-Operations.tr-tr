--- 
title: "Sipariş tutmaları yönetme"
description: "Bu yordam, müşteri satış siparişlerinin nasıl beklemeye alınacağını, sipariş bekletmeleri kullanıma almayla nasıl çalışılacağını ve sipariş bekletmelerinin nasıl kaldırılacağını gösterir."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 3edb8d2fe0fda6634bc2edb8e3bafc5a60344b7a
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="manage-order-holds"></a>Sipariş tutmaları yönetme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, müşteri satış siparişlerinin nasıl beklemeye alınacağını, sipariş bekletmeleri kullanıma almayla nasıl çalışılacağını ve sipariş bekletmelerinin nasıl kaldırılacağını gösterir. Sipariş, çeşitli nedenlerle beklemeye alınabilir. Örneğin, müşteri adresi veya ödeme yöntemi doğrulanıncaya kadar veya yönetici, müşterinin kredi limitini gözden geçirene kadar siparişi beklemeye alabilirsiniz. Sipariş beklemedeyken sevkiyat için ambar tarafından işlenemez. 

Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.


## <a name="set-up-order-holds"></a>Sipariş bekletmelerini ayarlama
1. Satış ve pazarlama > Kurulum > Satış siparişleri > Sipariş tutma kodları'na gidin.
2. Yeni'ye tıklayın.
3. Tutma kodu alanına bir değer yazın.
    * Örneğin, Geri arama yazın.  
4. Açıklama alanına bir değer girin.
    * Örneğin, Sipariş müşteri geri araması için bekletiliyor.  
    * İsteğe bağlı olarak, bu sipariş bekletme kodu eklendiğinde tüm fiziksel rezervasyonları kaldırmak için Rezervasyonları kaldır onay kutusunu işaretleyin.  
5. Kaydet'e tıklayın.

## <a name="place-order-on-hold"></a>Siparişi beklemeye alma
1. Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında bir değer girin veya seçin.
4. Tamam'a tıklayın.
5. Madde numarası alanında bir değer girin veya seçin.
6. Miktar alanına bir sayı girin.
7. Eylem Bölmesinde, Satış siparişi öğesine tıklayın.
8. Sipariş tutmaları'na tıklayın.
9. Yeni'ye tıklayın.
10. Tutma kodu alanında, önceki alt görevde oluşturduğunuz kodu seçin.
11. Kaydet'e tıklayın.
12. Sayfayı kapatın.
13. Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.
14. Listede, seçili satırı işaretleyin.
    * Şu anda beklemede olan siparişlerde "İşleme" ve "Durduruldu" alanları işaretledir.    
15. Eylem Bölmesinde, Çek ve paketle öğesine tıklayın.

## <a name="manage-order-holds"></a>Sipariş tutmaları yönetme
1. Satış ve pazarlama > Satış siparişleri > Açık siparişler > Sipariş tutmaları öğesini seçin.
    * Sipariş bekletme sayfası bir çalışma ekranı işlevi görür. Burada mevcut ve işlenmiş tüm bekletmelerin bir özetini görebilir, bunları ve ilişkilendirilmiş satış siparişlerini işleyebilirsiniz.      
2. Listede, seçili satırı işaretleyin.
3. Eylem Bölmesi'nde, Kullanıma almayı askıya al'a tıklayın.
4. Kullanıma alma öğesine tıklayın.
5. Listede, seçili satırın işaretini kaldırın.
    * Teslim alan alanında artık sizin kullanıcı kimliğiniz gösterilir.   
6. Kullanıma almayı temizle öğesine tıklayın.
7. Eylem Bölmesi'nde, Beklemeyi sil öğesine tıklayın.
    * Bekletmeyi kaldırmaya ve siparişin sonraki tamamlanma adımına ilerlemesine izin vermeye hazır olduğunuzda bekletmeyi temizlemeniz gerekir. Sipariş hiçbir değişiklik gerektirmiyorsa Tutmaları temizle eylemini çalıştırabilirsiniz. Ancak bir bekletmeyi temizlerken siparişin güncelleştirilmesi gerekirse Temizle ve değiştir eylemini kullanabilirsiniz.      
    * Temizle ve gönder eylemi yalnızca Çağrı merkezi işlevini kullandığınızda geçerlidir.  
8. Tutmaları temizle öğesine tıklayın.
    * Bekletme artık siparişten temizlenmiş ve Etkin bekletmeler listesinden kaldırılmıştır. Tüm bekletmeleri veya bunların alt kümesini belirli bir duruma göre görmek için Göster alanındaki değeri değiştirin.     


