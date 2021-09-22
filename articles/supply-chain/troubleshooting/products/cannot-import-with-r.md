---
title: Serbest bırakılmış ürünler V2 varlığını kullanarak bir maddeyi içe aktaramazsınız
description: Serbest bırakılmış ürünler V2 varlığını kullanarak bir maddeyi içe aktaramazsınız.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: bf6eb0eb755de3f2842c235946bfd7ccad04ccf7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474736"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Serbest bırakılmış ürünler V2 varlığını kullanarak bir maddeyi içe aktaramazsınız

KB numarası: 4611825

## <a name="symptoms"></a>Belirtiler

*Serbest bırakılmış ürünler V2* varlığını kullanarak bir maddeyi içe aktarmaya çalıştığınızda, aşağıdaki örneğe benzer bir hata iletisi alırsınız:

> Maddeler - izleme boyutu gruplarında bir kayıt oluşturulamıyor (EcoResTrackingDimensionGroupItem). Madde Numarası: 2040663, Toplu iş. Kayıt zaten var.

## <a name="resolution"></a>Çözünürlük

Yeni serbest bırakılan ürünleri içe aktarmak için, *Serbest bırakılan ürünler V2* varlığı yerine *Serbest bırakılmış ürün oluşturma V2* varlığını kullanmalısınız.
