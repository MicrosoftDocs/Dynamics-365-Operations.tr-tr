---
title: Hiçbir değişiklik yapmamış olsanız bile madde karşılama ayarlarını kaydetmeniz istenir
description: Hiçbir değişiklik yapmamış olsanız bile madde karşılama ayarlarını kaydetmeniz istenir.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049494"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>Hiçbir değişiklik yapmamış olsanız bile madde karşılama ayarlarını kaydetmeniz istenir

KB numarası: 4615588

## <a name="symptoms"></a>Belirtiler

Bazı senaryolarda, **Madde kapsamı V2** varlığı üzerinden öğeleri aldıktan sonra *Madde kapsamı* sayfasını açtığınızda aşağıdaki iletiyi alabilirsiniz:

> Kapatmadan önce değişikliklerinizi kaydetmek istiyor musunuz?

Herhangi bir değişiklik yapmamış olsanız bile bu iletiyi alırsınız.

## <a name="resolution"></a>Çözüm

**Madde kapsamı** sayfası, varlık alma gibi veritabanında son zamanlarda doğrudan değişiklikler yapıldıktan sonra iletinin gösterilmesine neden olabilecek karmaşık varsayılan mantık içerir. Örneğin, `AREGENERALSETTINGSOVERRIDDEN` varlık alanı *Hayır* olarak ayarlanır, ancak `PRODUCTCOVERAGEGROUPID` ve/veya `VENDORACCOUNTNUMBER` gibi alanlar için yeni veya değiştirilmiş değerler sağlayan bir dosya alırsınız. Bu durumda, `AREGENERALSETTINGSOVERRIDDEN` alanı *Hayır* olarak ayarlandığından, **madde kapsamı** sayfasını içe aktarma işleminden sonra ilk kez açtığınızda değerler alanlardan otomatik olarak temizlenir. Değişiklikleri ileti kutusu istemiyle kaydederseniz, bunlar veritabanında depolanır. Aksi takdirde, sayfayı bir sonraki açışınızda aynı iletiyi alırsınız.

Bu davranışı önlemek, ancak varlık içer aktarm üzerinden `PRODUCTCOVERAGEGROUPID` gibi alanların değerlerini de eklemek için, `AREGENERALSETTINGSOVERRIDDEN` alanını içe aktardığınızda *Evet* olarak ayarlayın.
