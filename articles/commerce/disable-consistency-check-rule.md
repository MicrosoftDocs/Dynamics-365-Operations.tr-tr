---
title: Perakende hareketi tutarlılık denetleyicisinde kuralları devre dışı bırakma
description: Bu konuda, Microsoft Dynamics 365 Commerce'taki hareket tutarlılık denetleyicisi kurallarını devre dışı bırakma işlevi açıklanmaktadır.
author: josaw1
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: 381bc8534d4b0a06a50c8c18b3f78aba9d43a1f497bfd271361216ed1dee9197
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746673"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Perakende hareketi tutarlılık denetleyicisinde kuralları devre dışı bırakma 

[!include [banner](../includes/banner.md)]

Perakendecilerin, kendilerine özgü benzersiz iş senaryoları ve süreçleri olabilir. Bu nedenle, ticari hareket tutarlılık denetleyicisine varsayılan olarak eklenen tüm kurallar tüm perakendeciler için geçerli değildir. Microsoft Dynamics 365 Commerce, farklılıklara uyum sağlamak için geçerli olmayan kuralları devre dışı bırakmak üzere kullanılabileceğiniz bir işlev sunar.

Ortamınızdaki ticari hareket tutarlılık denetleyicisinde bulunan kuralların listesini görüntülemek ve her kuralın durumunu görmek için **Retail ve Commerce \> Genel merkez kurulumu \> Parametreler \> Commerce parametreleri**'ne gidin ve **Hareket doğrulama** sekmesini seçin.

Varsayılan olarak, her kuralın durumu **Etkin** olarak ayarlanmıştır. Bu nedenle, ticari hareketleri ticari ekstrelere eklenmeden önce doğrulamak için tüm kurallar kullanılır. Bir kuralı devre dışı bırakmak için durumunu **Devre Dışı** olarak değiştirin. Ekstre hesaplama işlemi sırasında ticari hareketler doğrulanırken devre dışı bırakılan kurallar dikkate alınmaz.

Tüm doğrulama sürecini atlamak için, etkinleştirilen kuralları dikkate almadan **Retail ve Commerce \> Genel merkez kurulumu \> Parametreler \> Commerce parametreleri**'ne gidin ve sonra **Hareket doğrulama** sekmesinde **Commerce hareketleri için tutarlılık denetleyicisini devre dışı bırak** seçeneğini **Evet** olarak ayarlayın. Bu seçenek **Hayır** olarak ayarlandıktan sonra, kullanıcı arabiriminden (UI) tekrar **Evet** olarak değiştirilemez.


[!INCLUDE[footer-include](../includes/footer-banner.md)]