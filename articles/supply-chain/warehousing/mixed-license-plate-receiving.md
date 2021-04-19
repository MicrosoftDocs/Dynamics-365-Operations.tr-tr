---
title: Karma plaka alımı
description: Bu konu, bir mobil cihaz ile çoklu öğe için iş oluşturma ve kaydetme amacıyla karma plaka alma kullanmayı açıklar.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b17b3a4d704c5bfd051426e708d39022e59cc67a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810474"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]