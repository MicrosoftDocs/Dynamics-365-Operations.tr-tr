---
title: Sipariş tutmaları yönetme
description: Bu yordam, müşteri satış siparişlerinin nasıl beklemeye alınacağını, sipariş bekletmeleri kullanıma almayla nasıl çalışılacağını ve sipariş bekletmelerinin nasıl kaldırılacağını gösterir.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7168d13ef0b24d06aa28fbbc22bbb4e6093df24
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/11/2019
ms.locfileid: "1994922"
---
# <a name="manage-order-holds"></a>Sipariş tutmaları yönetme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, müşteri satış siparişlerinin nasıl beklemeye alınacağını, sipariş bekletmeleri kullanıma almayla nasıl çalışılacağını ve sipariş bekletmelerinin nasıl kaldırılacağını gösterir. Sipariş, çeşitli nedenlerle beklemeye alınabilir. Örneğin, müşteri adresi veya ödeme yöntemi doğrulanıncaya kadar veya yönetici, müşterinin kredi limitini gözden geçirene kadar siparişi beklemeye alabilirsiniz. Sipariş beklemedeyken sevkiyat için ambar tarafından işlenemez. 

Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.


## <a name="set-up-order-holds"></a>Sipariş bekletmelerini ayarlama
1. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Ayarla > Satış siparişleri > Sipariş bekletme kodları**'na gidin.
2. **Yeni**'ye tıklayın.
3. **Bekletme kodu** alanına bir değer yazın. Örneğin, "Geri çağırma" yazın.  
4. **Tanım** alanına bir değer girin.
    - Örneğin, Sipariş müşteri geri araması için bekletiliyor.  
    - İsteğe bağlı olarak, bu sipariş bekletme kodu eklendiğinde tüm fiziksel rezervasyonları kaldırmak için **Rezervasyonları kaldır** onay kutusunu işaretleyin.  
5. **Kaydet**'e tıklayın.

## <a name="place-order-on-hold"></a>Siparişi beklemeye alma
1. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Satış siperişler > Tüm satış siparişleri**'ne gidin.
2. **Yeni**'ye tıklayın.
3. **Müşteri hesabı** alanında bir değer girin veya seçin.
4. **Tamam**'a tıklayın.
5. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.
6. **Miktar** alanına bir sayı girin.
7. **Eylem Bölmesinde** **Satış siparişi** öğesine tıklayın.
8. **Sipariş bekletmeleri**'ne tıklayın.
9. **Yeni**'ye tıklayın.
10. **Bekletme kodu** alanında, önceki alt görevde oluşturduğunuz kodu seçin.
11. **Kaydet**'e tıklayın.
12. Sayfayı kapatın.
13. **Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri**'ne gidin.
14. Listede, seçili satırı işaretleyin. Şu anda beklemede olan siparişlerde "İşleme" ve "Durduruldu" alanları işaretledir.
15. Eylem Bölmesi'nde **Çek ve paketle**'ye tıklayın.

## <a name="manage-order-holds"></a>Sipariş tutmaları yönetme
1. **Satış ve pazarlama > Satış siparişleri > Açık siparişler > Sipariş bekletmeleri**'ni seçin. **Sipariş bekletmeleri** sayfası, bir çalışma ekranı işlevi görür. Burada mevcut ve işlenmiş tüm bekletmelerin bir özetini görebilir, bunları ve ilişkilendirilmiş satış siparişlerini işleyebilirsiniz.     
2. Listede, seçili satırı işaretleyin.
3. **Eylem Bölmesi**'nde **Ödemeyi beklet**'e tıklayın.
4. **Öde**'ye tıklayın.
5. Listede, seçili satırın işaretini kaldırın. **Ödemeyi yapan kişi** alanında artık sizin kullanıcı kimliğiniz gösterilir.   
6. **Ödemeyi sil**'e tıklayın.
7. **Eylem Bölmesi**'nde **Bekletmeyi sil**'e tıklayın.
    - Bekletmeyi kaldırmaya ve siparişin sonraki tamamlanma adımına ilerlemesine izin vermeye hazır olduğunuzda bekletmeyi temizlemeniz gerekir. Sipariş hiçbir değişiklik gerektirmiyorsa Tutmaları temizle eylemini çalıştırabilirsiniz. Ancak bir bekletmeyi temizlerken siparişin güncelleştirilmesi gerekirse Temizle ve değiştir eylemini kullanabilirsiniz.      
    - **Sil ve gönder** eylemi, yalnızca Çağrı merkezi işlevini kullandığınızda geçerlidir.  
8. **Bekletmeleri sil**'e tıklayın. Bekletme artık siparişten temizlenmiş ve Etkin bekletmeler listesinden kaldırılmıştır. Tüm bekletmeleri veya bunların alt kümesini belirli bir duruma göre görmek için Göster alanındaki değeri değiştirin.     

