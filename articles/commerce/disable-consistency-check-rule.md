---
title: Perakende hareketi tutarlılık denetleyicisinde kuralları devre dışı bırakma
description: Bu konuda, Microsoft Dynamics 365 Commerce'taki hareket tutarlılık denetleyicisi kurallarını devre dışı bırakma işlevi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5eb2af7e3090daabccd338d5d0bc6a6ebc4ea663
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982702"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Perakende hareketi tutarlılık denetleyicisinde kuralları devre dışı bırakma 

[!include [banner](../includes/banner.md)]

Perakendecilerin, kendilerine özgü benzersiz iş senaryoları ve süreçleri olabilir. Bu nedenle, ticari hareket tutarlılık denetleyicisine varsayılan olarak eklenen tüm kurallar tüm perakendeciler için geçerli değildir. Microsoft Dynamics 365 Commerce, farklılıklara uyum sağlamak için geçerli olmayan kuralları devre dışı bırakmak üzere kullanılabilen bir işlev sunar.

Ortamınızdaki ticari hareket tutarlılık denetleyicisinde bulunan kuralların listesini görüntülemek ve her kuralın durumunu görmek için **Retail ve Commerce \> Genel merkez kurulumu \> Parametreler \> Commerce parametreleri**'ne gidin ve **Hareket doğrulama** sekmesini seçin.

Varsayılan olarak, her kuralın durumu **Etkin** olarak ayarlanmıştır. Bu nedenle, ticari hareketleri ticari ekstrelere eklenmeden önce doğrulamak için tüm kurallar kullanılır. Bir kuralı devre dışı bırakmak için durumunu **Devre Dışı** olarak değiştirin. Ekstre hesaplama işlemi sırasında ticari hareketler doğrulanırken devre dışı bırakılan kurallar dikkate alınmaz.

Tüm doğrulama sürecini atlamak için, etkinleştirilen kuralları dikkate almadan **Retail ve Commerce \> Genel merkez kurulumu \> Parametreler \> Commerce parametreleri**'ne gidin ve sonra **Hareket doğrulama** sekmesinde **Commerce hareketleri için tutarlılık denetleyicisini devre dışı bırak** seçeneğini **Evet** olarak ayarlayın. Bu seçenek **Hayır** olarak ayarlandıktan sonra, kullanıcı arabiriminden (UI) tekrar **Evet** olarak değiştirilemez.


[!INCLUDE[footer-include](../includes/footer-banner.md)]