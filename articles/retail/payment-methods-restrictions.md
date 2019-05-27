---
title: İadeler için fişsiz ödeme yöntemlerini kısıtlama
description: Bu konu, çeşitli ödeme türlerinin, iadeler bir giriş olmadan yapıldığında bir iade için nasıl kısıtlanabileceğini açıklar.
author: rapraj
manager: AnnBe
ms.date: 013/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 6e2c32aae06ce7bbdde30809d7a197f43b856af1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564369"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>İadeler için fişsiz ödeme yöntemlerini kısıtlama


[!include [banner](includes/banner.md)]

Perakendecinin kabul edeceği ödeme türlerinin her biri, sistem ayarlandığında mutlaka yapılandırılmalıdır. Bu konu, çeşitli ödeme türlerinin, iadeler bir giriş olmadan yapıldığında bir iade için nasıl kısıtlanabileceğini açıklar.

## <a name="set-up-payment-methods"></a>Ödeme yöntemlerini ayarlama

Ödeme yöntemleri ayarlamak için, aşağıdaki görevlerin tamamlanması gerekir.
1. Tüm organizasyon tarafından kabul edilen ödeme yöntemleri oluşturun.
2. Organizasyon kapsamında kart tipleri ve kart numaraları oluşturma. Kredi kartları veya ATM kartları kabul ediliyorsa, kartlar için bir ödeme yöntemi oluşturmanız ve sonra organizasyon kapsamındaki kart tiplerini ve kart numaralarını oluşturmanız gerekir.
3. Mağaza ödeme yöntemlerini ayarlayın. Ödeme yöntemlerini her bir mağazayla ilişkilendirin ve ardından her bir ödeme yöntemi için mağazaya özel ayarları girin.
4. Mağazalar için kart ödeme yöntemleri ayarlayın. Mağazanın kabul ettiği tüm kart ödeme yöntemleri için kart kurulumunu tamamlayın.

![Perakende Mağaza Kurulumu](media/NoReceiptReturns1.png "Perakende Mağaza Kurulumu") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>İadeler için fişsiz ödeme yöntemlerini kısıtlama

Her bir mağaza ödeme yöntemi için **Perakende mağaza yönetimi** sayfasında, **Giriş olmayan iadeler** altında, **Giriş olmadan iadeleri kısıtla**'yı **Evet** olarak ayarlayın. 

Varsayılan değer **Hayır**'dır, bu da ödeme yönteminin iadeler için izin verilmesini sağlar. 

**Giriş olmadan iadeleri kısıtla**, **Evet** olarak ayarlanmışsa, seçilen ödeme yöntemine iadelerde izin verilmeyecektir. 

![Perakende Mağazası ödeme yöntemi](media/NoReceiptReturns3.png "Perakende Mağazası ödeme yöntemi") 

> [!NOTE]
> Bir kasiyer, giriş olmayan bir iade için kısıtlanmış bir ödem yöntemini seçerse, kabul edilebilir ödeme yöntemlerini gösteren bir mesaj görüntülenir.

![Kabul edilebilir ödeme yöntemleri](media/NoReceiptReturns4.png "Kabul edilebilir ödeme yöntemleri") 

Bir işlem hem girişli iade hem de giriş olmayan iade ise, kısıtlama koşulu zorlanmaz çünkü işlem, girişli bir iade iş akışı olacaktır. 

