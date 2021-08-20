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
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764704"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Serbest bırakılmış ürünler V2 varlığını kullanarak bir maddeyi içe aktaramazsınız

KB numarası: 4611825

## <a name="symptoms"></a>Belirtiler

*Serbest bırakılmış ürünler V2* varlığını kullanarak bir maddeyi içe aktarmaya çalıştığınızda, aşağıdaki örneğe benzer bir hata iletisi alırsınız:

> Maddeler - izleme boyutu gruplarında bir kayıt oluşturulamıyor (EcoResTrackingDimensionGroupItem). Madde Numarası: 2040663, Toplu iş. Kayıt zaten var.

## <a name="resolution"></a>Çözünürlük

Yeni serbest bırakılan ürünleri içe aktarmak için, *Serbest bırakılan ürünler V2* varlığı yerine *Serbest bırakılmış ürün oluşturma V2* varlığını kullanmalısınız.
