---
title: İade edilen maddeleri inceleme yoluyla alma
description: İade edilen maddeleri inceleme yoluyla alın.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53cb727cc0f001a6ac344d37f25273999f992d8a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974097"
---
# <a name="take-returned-items-through-inspection"></a>İade edilen maddeleri inceleme yoluyla alma 

[!include [banner](../includes/banner.md)]


1.  **Stok yönetimi** \> **Periyodik** \> **Kalite yönetimi** \> **Karantina emirleri**'ne tıklayın.

2.  Denetlediğiniz iade maddesine karşılık gelen sipariş satırının yerini belirleyin.

    > [!NOTE]
    > <P>Bir karantina emri yalnızca tek bir madde numarasıyla ilişkilendirilebilir. Farklı madde numaralarına sahip 10 maddenin tek bir sevkiyatta iade edilmesi ve karantinaya gönderilmesi durumunda, ayrı ayrı 10 karantina emri oluşturulacaktır.</P>

3.  Maddeyi inceledikten sonra, maddeye ne yapılması gerektiğini ve ilişkili mali hareketin ne şekilde ele alınacağını belirtmek üzere **Elden çıkarma kodu** alanında bir seçim yapın. Örnekler arasında maddenin stoka geri gönderilmesi ve müşteriye para iadesi yapılması, maddenin ıskartaya çıkarılması ve müşteriye yenisinin gönderilmesi ya da maddenin alacak kaydedilmeksizin müşteriye geri gönderilmesi yer alır.
    
    > [!NOTE]
    > <P>Tek bir madde numarası toplu işindeki birden çok iade maddesine aynı elden çıkarma kodunun atanamaması durumunda, her alt toplu işe farklı bir çıkarma kodu atamak için karantina emrini bölmeniz gerekir (<STRONG>İşlevler</STRONG> &gt; <STRONG>Böl</STRONG>).</P>


4.  Denetim tamamlandıktan sonra, iade edilen maddeleri serbest bırakmak ve bir madde varış günlük girişi oluşturmak için **Bitti olarak bildir**'e tıklayın. Daha sonra maddeleri alan kişi veya departman, stoğa iade edilecek maddeler için günlüğü işler.
    
    veya
    
    Karantina emrini sona erdirin ve doğrudan **Stok** işlevlerinden birini kullanarak maddeleri tekrar stoğa taşıyın.

5.  Değişikliklerinizi kaydetmek için formu kapatın.

## <a name="see-also"></a>Ayrıca bkz.

[İade edilen maddelerin nasıl elden çıkarılacağını belirtme](specify-how-to-dispose-of-returned-items.md)

  


