---
title: Üretim emirleri İşaretleme sayfasında gösterilmiyor
description: Bazı üretim emirleri İşaretleme sayfasında gösterilmez. Bu konuda, işaretleme için kullanılabilir olmayan üç ürün yapılandırması açıklanmaktadır.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477794"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>Üretim emirleri İşaretleme sayfasında gösterilmiyor

## <a name="symptoms"></a>Belirtiler

Parçalı üretimle çalışırken bazı üretim emirleri **İşaretleme** sayfasında gösterilmez.

## <a name="resolution"></a>Çözüm

Aşağıdaki yapılandırmalara sahip ürünler işaretleme için kullanılamaz. Bu nedenle, **İşaretleme** sayfasında gösterilmez:

- Ürünler, *fiili ağırlık* tipi ürünler olarak tanımlanır.
- Bunlar gelişmiş ambar işlemleri için etkinleştirilir.
- *Standart maliyet* ilkesi tarafından denetlenecek şekilde yapılandırılırlar.
