---
title: "Bir mobil cihazda ambar içindeki eski toplu işleri görüntülemeyi konfigüre etme"
description: "Bu konu, bir iş satırının geçerli konumundan daha eski toplu işlere sahip konumların bir listesini görüntüleme için bir mobil cihazı ayarlamayı açıklar."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations, Core
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cd0a9c2e9fbfea987b045e301fb73a505a0f2a4e
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Bir mobil cihazda ambar içindeki eski toplu işleri görüntülemeyi konfigüre etme

[!include[banner](../includes/banner.md)]

**Bu ambar içerisindeki daha eski toplu işleri görüntüle** yapılandırması, iş satırının geçerli konumundakinden eski toplu işlere sahip konumları listelemenizi sağlar. Görüntülenen konumların listesi konumdaki eski toplu işler hakkında bilgiyi, her bir toplu işin bitiş tarihi ve fiziksel stokunu içerir. Yeni bir konumdan çekmeyi veya geçerli konumdan çekmeye devam etmeyi seçebilirsiniz. 
- Yeni bir konumdan çek - Çekmek için yeni bir konum seçerseniz, geçerli iş satırı yeni konumu kullanmak üzere güncelleştirilir ve iş, yeni konumda her zaman olduğu gibi devam eder. Yeni konumun geçerli olması için tüm iş satırı için yeterli kullanılabilir miktara sahip olması gerekir. Gerekli miktar kullanılabilir durumda değilse, iş satıcı güncelleştirilmez ve liste görüntülenir. 
- Geçerli konumdan çekmeye devam et - Geçerli iş satırı konumuyla devam ederseniz, iş satırı için miktarlar orijinal konumdan çekilmeye devam eder.

## <a name="where-it-applies"></a>Uygulandığı yerler
Ambar içindeki eski toplu işleri görüntüle mobil cihaz menü öğelerinde yapılandırılır ve aşağıdaki toplu iş maddeleri için seçimi etkiler.

## <a name="set-up-display-older-batches-within-warehouse"></a>Bu ambar içindeki eski toplu işleri görüntülemeyi ayarlama
**Bu ambar içindeki eski toplu işleri görüntüle** yapılandırması mobil cihaz menü öğelerinde **En eski toplu işi çek** seçeneği **Uyar** olarak ayarlanmışsa kullanılabilir.

- **Ambar yönetimi** > **Kurulum** > **Mobil cihaz** > **Mobil cihaz menü öğeleri** altında, **Mevcut işi kullan**'ı menü öğesi için **Evet** olarak ayarlayın ve **En eksiyi çek** altında **Uyar**'ı seçin. 


