---
title: Ürün reçetesinin etkin sürümü ve rota numaraları eklenemiyor
description: Seçili bir ürün için varsayılan tesis ve ambar önceden tanımlanmışsa ürün reçetesinin etkin sürümünü ve rota numaralarını eklemeniz istenmez.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477801"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>Yeni bir üretim emri oluşturulurken ürün reçetesi ve rota eklenemiyor

## <a name="symptoms"></a>Belirtiler

Yeni bir üretim emri oluşturduğunuzda, madde numarasını girdikten sonra **Tesis** ve **Ambar** alanları, otomatik olarak tamamlanan mallar için **Varsayılan sipariş ayarları** sayfasında tanımlanan varsayılan tesis ve ambara ayarlanır. Ayrıca etkin ürün reçetesi numarası ve rota numarası otomatik olarak girilir, böylece sizden şu değerleri isteyen aşağıdaki iletiyi almazsınız:

> Ürün reçetesi ve rotanın etkin sürümünü ekleyin?

## <a name="resolution"></a>Çözüm

**Varsayılan sipariş ayarları** sayfasında bir tesis ve ambarın önceden tanımlandığı bir ürün seçerseniz ürün reçetesi ve rota numaralarını eklemeniz istenmez. Yalnızca bu değerler seçili ürün için tanımlanmamışsa istenir.
