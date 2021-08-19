---
title: Üretim çıkış yeri
description: Bu konu, üretim çıkış konumunun kimliğini belirlemekte kullanılacak hiyerarşiyi açıklar.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f4c8086e9179ff51f62ce77620af96360c6123060372dfd1c0e06dad79998b75
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720288"
---
# <a name="production-output-location"></a>Üretim çıkış yeri

[!include [banner](../includes/banner.md)]

Bu konu, üretim çıkış konumunun kimliğini belirlemekte kullanılacak hiyerarşiyi açıklar.

Üretim çıkış konumu, tamamlanmış malın üretildikten sonra ilk depolandığı konumdur. Bu, konum genellikle, tamamlanmış ürünü üreten üretim merkezine yakındır. Üretim çıkış konumu, malzemenin sevkiyat alanına, bir depolama konumuna, üretime devam etme işlemi için bir üretim giriş konumuna ve benzerlerine taşınmadan önceki bir ara depolamadır. 

Bir varsayılan üretim çıkış konumu, tamamlanmış mallar bir üretim siparişi veya toplu iş siparişinde raporlandığında ayarlanır. Aşağıdaki hiyerarşi bu çıkış konumunu tanımlamakta kullanılır:

1. Üretim emri veya toplu iş siparişi başlığında tanımlanan çıkış konumunu kullan.
2. Burada konum bulunamıyorsa, kaynak üzerinde üretim rotasında tanımlanmış son operasyonda tanımlanmış olan çıkış konumunu kullan.
3. Burada konum bulunamıyorsa, kaynak grubu üzerinde üretim rotasında tanımlanmış son operasyon için tanımlanmış olan çıkış konumunu kullan.
4. Burada konum bulunmazsa, üretim emri için tanımlanmış ambardaki çıkış konumunu kullan.

Bir varsayılan üretim çıkış konumu, yalnızca gelişmiş ambar işlemleri kullanan ürünler için ayarlanmıştır. Bu türde bir madde tamamlanmış olarak raporlandığında, **Tamamlanmış mal koyma** veya **Ortak ürün ve yan ürün koyma** türünde bir ambar işi oluşturulur. Bu türde iş, üretim çıkış konumunu çekme konumu olarak kullanır. Yerine koyma konumu, konum yönergeleri tarafından belirlenir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]