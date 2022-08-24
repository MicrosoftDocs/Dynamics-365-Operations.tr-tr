---
title: E-ticaret kanallarında tutarlı teslimat şekli işlemeyi etkinleştirme
description: Bu makalede, Microsoft Dynamics 365 Commerce e-ticaret kanallarındaki ücretler akışlarıyla ilgili olası sorunları gidermek üzere tutarlı teslim modu işlemenin nasıl etkinleştirileceği açıklanmaktadır.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 43450c9d380bd57c234bb1c9acfbe296ab115f14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279663"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>E-ticaret kanallarında tutarlı teslimat şekli işlemeyi etkinleştirme 

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce e-ticaret kanallarındaki ücretler akışlarıyla ilgili olası sorunları gidermek üzere tutarlı teslim modu işlemenin nasıl etkinleştirileceği açıklanmaktadır.

Dynamics 365 Commerce'te, eşit şekilde olmayan başlık düzeyi ücretleri e-ticaret kanallarında varsayılan olarak uygulanmaz. Bu davranış, e-ticaret kanallarında aşağıdaki sorunlardan birine veya her ikisine neden olabilir:

- Eşit olarak alınmayan başlık düzeyi giderler görüntülenmiyor.
- Teslimat modları için ücretler, teslimat seçimi ile teslim alma siparişi özeti arasında tutarlı değil.

Bu sorunları gidermek için **Kanalda tutarlı mod işlemeyi etkinleştir** özelliğini açmanız gerekir. Bu özellik, e-ticaret kanallarında eşit olmayan başlık düzeyi ücretlerin görünmesini ve satış siparişi teslimat bilgilerinin aynı talep iş akışı tarafından tutarlı olarak işlenmesini sağlar.

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>Kanalda tutarlı teslimat şekli işlemeyi etkinleştirme özelliğini açma

Commerce genel merkezinde **Kanalda tutarlı teslimat şekli işlemeyi etkinleştirme** özelliğini etkinleştirmek için aşağıdaki adımları izleyin.

1. **Özellik yönetimi** çalışma alanını açın (**Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**).
1. Kullanılabilen özellikler listesinde, **Kanalda tutarlı teslimat yöntemi işlemeyi etkinleştir**'i arayıp seçin.
1. Sağdaki bölmeden **Şimdi etkinleştir**'i seçin.
