--- 
title: " Çalışanı yapılandırma"
description: "Bu yordam bir perakende çalışanını POS'ta satışlar üzerinden komisyon için uygun bir satış temsilcisi olarak yapılandırmayı gösterir."
author: jblucher
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: f241899df89377e3c08c94663b90ee9d0ce750dc
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="configure-a-worker"></a> Çalışanı yapılandırma

[!include[task guide banner](../includes/task-guide-banner.md)]

Bu yordam bir perakende çalışanını POS'ta satışlar üzerinden komisyon için uygun bir satış temsilcisi olarak yapılandırmayı gösterir. Bu yordam, USRT demo veri şirketini kullanır.


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
1. Retail and commerce > Employees > Workers (Perakende ve ticaret > Personel > Çalışanlar) menüsüne gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Perakende sekmesini tıklatın.
    * Çalışan varsayılan bir satış grubuna atanabilir. Mağazanın işlevsellik profilinde seçenek etkinleştirilmişse varsayılan satış grubu POS'ta satış satırlarına otomatik olarak eklenir.  
5. Düzenle öğesine tıklayın.
6. Varsayılan grup alanına bir değer girin veya bir değer seçin.
7. Kaydet'e tıklayın.

