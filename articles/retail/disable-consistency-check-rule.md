---
title: Perakende hareketi tutarlılık denetleyicisinde kuralları devre dışı bırakma
description: Bu konuda, Microsoft Dynamics 365 Retail'deki perakende hareketi tutarlılık denetleyicisi kurallarını devre dışı bırakma işlevi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586309"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Perakende hareketi tutarlılık denetleyicisinde kuralları devre dışı bırakma 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Perakendecilerin, kendilerine özgü benzersiz iş senaryoları ve süreçleri olabilir. Bu nedenle, perakende hareketi tutarlılık denetleyicisine varsayılan olarak eklenen tüm kurallar tüm perakendeciler için geçerli değildir. Microsoft Dynamics 365 Retail, farklılıklara uyum sağlamak için geçerli olmayan kuralları devre dışı bırakmak üzere kullanılabilen bir işlev sunar.

Ortamınızdaki perakende hareketi tutarlılık denetleyicisinde bulunan kuralların listesini görüntülemek ve her kuralın durumunu görmek için **Perakende \> Genel merkez kurulumu \> Parametreler \> Perakende parametreleri**'ne gidin ve **Hareket doğrulama** sekmesini seçin.

Varsayılan olarak, her kuralın **Etkin**'dir. Bu nedenle, perakende hareketlerini perakende ekstrelerine eklenmeden önce doğrulamak için tüm kurallar kullanılır. Bir kuralı devre dışı bırakmak için durumunu **Devre dışı** olarak değiştirin. Ekstre hesaplama işlemi sırasında perakende hareketleri doğrulanırken devre dışı bırakılan kurallar dikkate alınmaz.

Tüm doğrulama sürecini atlamak için, etkinleştirilen kuralları dikkate almadan **Perakende \> Genel merkez kurulumu \> Parametreler \> Perakende parametreleri**'ne gidin ve sonra **Hareket doğrulama** sekmesinde **Perakende hareketleri için tutarlılık denetleyicisini devre dışı bırak** seçeneğini **Evet** olarak ayarlayın. Bu seçenek **Hayır** olarak ayarlandıktan sonra, kullanıcı arabiriminden (UI) tekrar **Evet** olarak değiştirilemez.
