---
title: Hareket doğrulama işleminde kullanılan kuralları devre dışı bırakma
description: Bu konuda, Microsoft Dynamics 365 Commerce uygulamasındaki hareket doğrulama kurallarını devre dışı bırakma işlevi açıklanmaktadır.
author: analpert
ms.date: 12/11/2021
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
ms.openlocfilehash: cdaea51b4c84e6a62f0eb9412315ae77b4c11503
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919539"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Hareket doğrulama işleminde kullanılan kuralları devre dışı bırakma

[!include [banner](../includes/banner.md)]

Perakendecilerin, kendilerine özgü benzersiz iş senaryoları ve süreçleri olabilir. Bu nedenle, ticari hareket doğrulama işlemine eklenen tüm kurallar her perakendeci için geçerli değildir. Farklılıklara uyum sağlamak için Microsoft Dynamics 365 Commerce, geçerli olmayan kuralları devre dışı bırakmak üzere kullanılabileceğiniz bir işlev sunar.

Ortamınızdaki hareket doğrulama işleminde kullanılabilen kuralların listesini görüntülemek ve her bir kuralın durumunu görmek için **Retail ve Commerce \> Genel merkez ayarı \> Parametreler \> Commerce parametreleri** bölümüne gidin ve **Hareket doğrulaması** sekmesini seçin. Etkinleştirilen tüm kurallar, **Mağaza hareketlerini doğrula** işlemi sırasında hareketleri doğrulamak için kullanılır ve hareketlerin toplanıp bir hareket ekstresinde deftere nakledilmesi için geçirilmeleri gerekir.

Varsayılan olarak, her kuralın durumu **Etkin** olarak ayarlanır. Bu nedenle, tüm kurallar ticari hareket ekstrelerine çekilmeden önce hareketleri doğrulamak için kullanılır. Bir kuralı devre dışı bırakmak için durumunu **Devre Dışı** olarak değiştirin. **Mağaza hareketlerini doğrula** işlemi sırasında hareketler doğrulanırken devre dışı bırakılan kurallar dikkate alınmaz.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
