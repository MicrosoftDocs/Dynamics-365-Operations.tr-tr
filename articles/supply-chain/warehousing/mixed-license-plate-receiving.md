---
title: Karma plaka alımı
description: Bu konu, bir mobil cihaz ile çoklu öğe için iş oluşturma ve kaydetme amacıyla karma plaka alma kullanmayı açıklar.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15c058887da33b522c5d9a1a8d2c45a5d1566a5d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215781"
---
# <a name="mixed-license-plate-receiving"></a>Karma plaka alımı

[!include [banner](../includes/banner.md)]

Karma plaka almak, yerine koyma işlemi oluşturmadan önce çoklu öğelerden oluşan bir plaka oluşturmanıza izin verir. 

Birden fazla öğeden oluşan bir plakanın, sizin her bir öğeyi kaydetmeniz için teslim alma noktasında bölünmesi gerekmez. 

Belge satırlarının kaynağını belirlemek için maddeye bağlı akış kullanırken, madde denetimi üzerindeki barkodları taratabilirsiniz. Barkodun üzerinde miktar ve bir ölçüm birimi (UOM) yapılandırılmışsa, madde ve miktar otomatik olarak karma plaka eklenir ve başka bir madde taramak için ekrana döndürülürsünüz. Bu da tüm maddeleri, her adımda bir onay vermek zorunda kalmadan hızlıca taramanıza olanak sağlar. 

Karma plaka alma akışı içerisinde, plakaya taranmış olan maddelerin listesini görüntüleyebilir ve buradan bir maddeyi değiştirebilir veya miktarını düzeltebilirsiniz.

## <a name="where-it-applies"></a>Uygulandığı yerler

Karma plaka alma, çoklu satır/madde için aynı anda kayıt ve iş oluşturma sağlayan bir mobil cihaz alma akışıdır. Bu, birden çok öğe içeren gelen plakalar alıyorsanız yararlıdır. 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a>Karma plaka almanın ayarlanması
Karma plaka alma, bir mobil cihaz menü öğesi olarak ayarlanır.

Mevcut işi kullanmayan ve aşağıdaki yöntemlerden birini kullanan, iş moduna sahip yeni bir menü öğesi oluşturmanız gerekir:

- Karma plaka alımı
- Karma plaka alımı ve yerine koyma işlemi

Kaynak belge satırlarını belirlemek için seçenekler şunlardır: satınalma siparişi maddesi, satınalma siparişi satırı, iade siparişi, transfer sipariş maddesi ve transfer emri satırı. Bu seçenekler, tek bir plaka üzerindeki alma sırasını değiştirebilir. Son seçenek yük maddesine göredir. Birden fazla maddeyi bir plakaya ekleyebilirsiniz ancak çoklu yükler arasında geçiş yapamazsınız.
