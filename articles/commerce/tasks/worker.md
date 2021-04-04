---
title: " Çalışanı yapılandırma"
description: Bu yordam bir çalışanını POS'ta satışlar üzerinden komisyon için uygun bir satış temsilcisi olarak yapılandırmayı gösterir.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 120705200f223e31c72290059e8634e7db6f9fdd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232629"
---
# <a name="configure-a-worker"></a> Çalışanı yapılandırma

[!include [banner](../includes/banner.md)]

Bu yordam bir çalışanını POS'ta satışlar üzerinden komisyon için uygun bir satış temsilcisi olarak yapılandırmayı gösterir. Bu yordam, USRT demo veri şirketini kullanır.


## <a name="create-a-commission-sales-group-for-the-worker"></a>Çalışan için komisyon satış grubu oluşturma
1. Satış ve pazarlama > Komisyonlar > Satış grupları'na gidin.
    * Çalışanlar bir veya daha fazla satış grubuna atanabilir. POS'ta, mağazanın adres defterinden çalışanları içeren herhangi bir satış grubunu seçebilirsiniz.  
2. Yeni'ye tıklayın.
3. Grup alanında bir değer girin.
4. İsim alanına bir değer yazın.
5. Kaydet'e tıklayın.
6. Eylem Bölmesinde, Genel öğesine tıklayın.
7. Satış temsilcisi'ne tıklayın.
    * Satış grubu birden fazla çalışan içerebilir. Komisyonlar, komisyon hissesini nasıl tanımladığınıza bağlı olarak çalışanlar arasında bölünebilir.  
8. Ad alanına bir değer girin veya buradan bir değer seçin.
9. Komisyon hissesi alanına bir sayı girin.
10. Kaydet'e tıklayın.
11. Sayfayı kapatın.
12. Sayfayı kapatın.

## <a name="assign-the-workers-default-sales-group"></a>Çalışanlar varsayılan satış grubunu atama
1. Retail ve Commerce > Personel > Çalışanlar menüsüne gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Commerce sekmesine tıklayın.
    * Çalışan varsayılan bir satış grubuna atanabilir. Mağazanın işlevsellik profilinde seçenek etkinleştirilmişse varsayılan satış grubu POS'ta satış satırlarına otomatik olarak eklenir.  
5. Düzenle öğesine tıklayın.
6. Varsayılan grup alanına bir değer girin veya bir değer seçin.
7. Kaydet'e tıklayın.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]