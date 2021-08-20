---
title: Tek bir girişte birden fazla çalışma başlığı için yalnızca bir etiket yazdırılıyor
description: Tek bir girişte birden fazla çalışma başlığı için yalnızca bir etiket yazdırılıyor.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: cf307964a07c2b69eb5e4ef2cf9dc094482736d0970e333e84f674c9be6331c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740539"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Tek bir girişte birden fazla çalışma başlığı için yalnızca bir etiket yazdırılıyor

KB numarası: 4614667

## <a name="symptoms"></a>Belirtiler

Tek bir ambar uygulaması alma olayının parçası olarak aynı hedef plaka için birden fazla iş üstbilgisi oluşturulur. Ancak, ürün alındığında yalnızca bir plaka etiketi yazdırılır.

## <a name="resolution"></a>Çözünürlük

Sistem, beklendiği şekilde davranıyordur.

Geçerli tasarımda, varolan çalışma başlığı ve iş satırı birleşimlerinin sayısına bakmaksızın, her zaman tek bir plaka etiketi oluşturulur. Oluşturulan etiket, yalnızca bir birleşimin bilgilerini içerir.

Bu soruna geçici bir çözüm olarak, iş üstbilgi oluşturmanın her zaman tek bir hedef plakaya eşlendiğinden emin olun.
