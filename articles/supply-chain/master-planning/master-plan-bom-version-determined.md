---
title: Ürün reçetesi sürümünü belirleme
description: Bir talep açılımı sırasında bir maddenin varsayılan bir Üretim emri varsa, planlama altyapısı tesise göre geçerli bir ürün reçetesi sürümü bulur.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4fd5f28d0ee85c267ea6a86a1452fbacc824620
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833629"
---
# <a name="determine-the-bom-version"></a>Ürün reçetesi sürümünü belirleme

[!include [banner](../includes/banner.md)]

Bir talep açılımı sırasında bir maddenin varsayılan bir Üretim emri varsa, planlama altyapısı tesise göre geçerli bir ürün reçetesi sürümü bulur. 

Tesis boyutu her zaman bilinir ve talep hareketinde belirtilir. Sıradaki süreç kullanılacak ürün reçetesi sürümünü belirlemek için kullanılır:

-   Talep tesisindeki madde için tanımlanmış bir ürün reçetesi sürümü varsa, bu tesise özgü ürün reçetesi kullanılır.
-   Talep tesisindeki madde için tanımlanmış belirli bir ürün reçetesi sürümü yoksa, genel bir ürün reçetesi kullanılır. Genel ürün reçetesinde tesis belirtilmez ve birden çok tesis için geçerlidir. Genel bir ürün reçetesi varsa, o kullanılır.
-   Kullanılacak bir genel ürün reçetesi yoksa, talep açılımı bu noktada durur.

Geçerli bir ürün reçetesi sürümü, ister tesise özgü ister genel bir ürün reçetesi olsun, tarih ve miktar ölçütlerini karşılamalıdır.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]