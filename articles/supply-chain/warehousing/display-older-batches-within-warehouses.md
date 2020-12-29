---
title: Bir mobil cihazda ambar içindeki eski toplu işleri görüntülemeyi konfigüre etme
description: Bu konu, bir iş satırının geçerli konumundan daha eski toplu işlere sahip konumların bir listesini görüntüleme için bir mobil cihazı ayarlamayı açıklar.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b1c9452a811d662976a25993264be0617ac67fe
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439281"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Bir mobil cihazda ambar içindeki eski toplu işleri görüntülemeyi konfigüre etme

[!include [banner](../includes/banner.md)]

**Bu ambar içerisindeki daha eski toplu işleri görüntüle** yapılandırması, iş satırının geçerli konumundakinden eski toplu işlere sahip konumları listelemenizi sağlar. Görüntülenen konumların listesi konumdaki eski toplu işler hakkında bilgiyi, her bir toplu işin bitiş tarihi ve fiziksel stokunu içerir. Yeni bir konumdan çekmeyi veya geçerli konumdan çekmeye devam etmeyi seçebilirsiniz. 
- Yeni bir konumdan çek - Çekmek için yeni bir konum seçerseniz, geçerli iş satırı yeni konumu kullanmak üzere güncelleştirilir ve iş, yeni konumda her zaman olduğu gibi devam eder. Yeni konumun geçerli olması için tüm iş satırı için yeterli kullanılabilir miktara sahip olması gerekir. Gerekli miktar kullanılabilir durumda değilse, iş satıcı güncelleştirilmez ve liste görüntülenir. 
- Geçerli konumdan çekmeye devam et - Geçerli iş satırı konumuyla devam ederseniz, iş satırı için miktarlar orijinal konumdan çekilmeye devam eder.

## <a name="where-it-applies"></a>Uygulandığı yerler
Ambar içindeki eski toplu işleri görüntüle mobil cihaz menü öğelerinde yapılandırılır ve aşağıdaki toplu iş maddeleri için seçimi etkiler.

## <a name="set-up-display-older-batches-within-warehouse"></a>Bu ambar içindeki eski toplu işleri görüntülemeyi ayarlama
**Bu ambar içindeki eski toplu işleri görüntüle** yapılandırması mobil cihaz menü öğelerinde **En eski toplu işi çek** seçeneği **Uyar** olarak ayarlanmışsa kullanılabilir.

- **Ambar yönetimi** > **Kurulum** > **Mobil cihaz** > **Mobil cihaz menü öğeleri** altında, **Mevcut işi kullan**'ı menü öğesi için **Evet** olarak ayarlayın ve **En eksiyi çek** altında **Uyar**'ı seçin. 

