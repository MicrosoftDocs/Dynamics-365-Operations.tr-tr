---
title: İadeler için fişsiz ödeme yöntemlerini kısıtlama
description: Bu makale, çeşitli ödeme türlerinin, iadeler bir giriş olmadan yapıldığında bir iade için nasıl kısıtlanabileceğini açıklar.
author: rapraj
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 091d39ea9fe41d78b7f34f85ecd1894047e022d6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896965"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>İadeler için fişsiz ödeme yöntemlerini kısıtlama


[!include [banner](includes/banner.md)]

Perakendecinin kabul edeceği ödeme türlerinin her biri, sistem ayarlandığında mutlaka yapılandırılmalıdır. Bu makale, çeşitli ödeme türlerinin, iadeler bir giriş olmadan yapıldığında bir iade için nasıl kısıtlanabileceğini açıklar.

## <a name="set-up-payment-methods"></a>Ödeme yöntemlerini ayarlama

Ödeme yöntemleri ayarlamak için, aşağıdaki görevlerin tamamlanması gerekir.
1. Tüm organizasyon tarafından kabul edilen ödeme yöntemleri oluşturun.
2. Organizasyon kapsamında kart tipleri ve kart numaraları oluşturma. Kredi kartları veya ATM kartları kabul ediliyorsa, kartlar için bir ödeme yöntemi oluşturmanız ve sonra organizasyon kapsamındaki kart tiplerini ve kart numaralarını oluşturmanız gerekir.
3. Mağaza ödeme yöntemlerini ayarlayın. Ödeme yöntemlerini her bir mağazayla ilişkilendirin ve ardından her bir ödeme yöntemi için mağazaya özel ayarları girin.
4. Mağazalar için kart ödeme yöntemleri ayarlayın. Mağazanın kabul ettiği tüm kart ödeme yöntemleri için kart kurulumunu tamamlayın.

![Mağaza Kurulumu.](media/NoReceiptReturns1.png "Mağazada Retail kurulumu") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>İadeler için fişsiz ödeme yöntemlerini kısıtlama

Her bir mağaza ödeme yöntemi için **Mağaza yönetimi** sayfasında, **Giriş olmayan iadeler** altında, **Giriş olmadan iadeleri kısıtla**'yı **Evet** olarak ayarlayın. 

Varsayılan değer **Hayır**'dır, bu da ödeme yönteminin iadeler için izin verilmesini sağlar. 

**Giriş olmadan iadeleri kısıtla**, **Evet** olarak ayarlanmışsa, seçilen ödeme yöntemine iadelerde izin verilmeyecektir. 

![Mağaza ödeme yöntemi.](media/NoReceiptReturns3.png "Perakende Mağaza Ödeme Yöntemi") 

> [!NOTE]
> Bir kasiyer, giriş olmayan bir iade için kısıtlanmış bir ödem yöntemini seçerse, kabul edilebilir ödeme yöntemlerini gösteren bir mesaj görüntülenir.

![Kabul edilebilir ödeme yöntemleri.](media/NoReceiptReturns4.png "Kabul edilebilir ödeme yöntemleri") 

Bir işlem hem girişli iade hem de giriş olmayan iade ise, kısıtlama koşulu zorlanmaz çünkü işlem, girişli bir iade iş akışı olacaktır. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]