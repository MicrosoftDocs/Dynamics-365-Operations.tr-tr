---
title: Tamamlandı bildiriminin tersine çevrilmesi, beklenmedik bir açık hareket oluşturuyor
description: Tamamlandı bildiriminin tersine çevrilmesi, tersine çevrilmiş miktarın tersine çevrilmiş hareketle aynı stok boyutlarına sahip olduğu bir açık hareket oluşturur.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026995"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Tamamlandı bildiriminin tersine çevrilmesi, beklenmedik bir açık hareket oluşturuyor

KB numarası: 4612469

## <a name="symptoms"></a>Belirtiler

Tamamlandı bildirimini tersine çevirirseniz, sistem, tersine çevrilmiş miktarın tersine çevrilmiş hareketle aynı stok boyutlarına sahip olduğu bir açık hareket oluşturur.

## <a name="resolution"></a>Çözünürlük

Tamamlandı bildirimi işlemini tersine çevirdiğinizde, stok boyutu üretim günlüğünden başlatılır. Bu nedenle, toplu iş numarasını alır. İşaretleme nedeniyle, satış siparişi hareketleri toplu iş numarasını devralır.

Tamamlandı bildirimi deftere nakledildiğinde boyut sıfırlanabilir.
