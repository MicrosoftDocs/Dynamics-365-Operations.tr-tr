---
title: İade edilen maddeleri inceleme yoluyla alma
description: İade edilen maddeleri inceleme yoluyla alın.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d782e9bf4793e2c6d1ef8b334d3bfc3bb729ad31
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824353"
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

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]