---
title: Üretim planlamasında emniyet marjları dikkate alınmıyor
description: Üretim planlaması, ilişkilendirilmiş arz için madde karşılamasının ayarlandığı emniyet marjlarını dikkate almıyor
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477827"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>Üretim planlamasında emniyet marjları dikkate alınmıyor

## <a name="symptoms"></a>Belirtiler

Master planlama emniyet marjlarını dikkate alır. Ancak planlanan üretim emirleri planlandığında emniyet marjları yoksayılır.

## <a name="resolution"></a>Çözüm

Marjlar yalnızca master planlama sırasında değerlendirilir, el ile zamanlama sırasında değil. Marjlar planlama aşamasında, gerçek işleme "marj" vermek için bir tampon olarak çalışacak şekilde tasarlanmıştır.

İstenen sonuca ulaşmak için marjı kaldırabilirsiniz. Rotanın istenen saati (örneğin, kuyruk süresi olarak) içermesi için güncelleştirilmesi gerekir. Hem master planlama hem de el ile programlamanın aynı sonucu üretmesi gerekir.
