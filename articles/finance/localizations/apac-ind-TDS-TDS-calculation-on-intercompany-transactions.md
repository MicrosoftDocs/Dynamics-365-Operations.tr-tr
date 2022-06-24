---
title: Şirketlerarası hareketlerde TDS hesaplaması
description: Bu makalede, şirketlerarası hareketlerde Kaynakta Kesilen Vergiyi (TDS) hesaplamak için kullanılan işlem aşamalı olarak açıklanmaktadır.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: c27bea997804f2c5eff6be2b20064b272ccd062f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888987"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>Şirketlerarası hareketlerde TDS hesaplaması

[!include [banner](../includes/banner.md)]

Bu makalede, şirketlerarası hareketlerde Kaynakta Kesilen Vergiyi (TDS) hesaplamak için kullanılan işlem aşamalı olarak açıklanmaktadır.

Bir şirketlerarası satınalma siparişi veya satış siparişi oluşturulduğunda, TDS tutarını hesaplamak için müşteri veya satıcı için tanımlanan varsayılan TDS grubu kullanılır. TDS tutarı, fatura deftere nakledildikten sonra kurtarılabilir veya borç hesaplarına nakledilir.

Orijinal satınalma siparişi veya satış siparişi için otomatik olarak bir şirketlerarası satış siparişi veya satınalma siparişi oluşturulur. Varsayılan TDS grubu şirketlerarası siparişte görüntülenir, böylece TDS hesaplanabilir. TDS grubunu değiştirebilirsiniz. Fatura, yalnızca otomatik olarak oluşturulan şirketlerarası siparişte bulunan net fatura tutarı orijinal siparişteki net fatura tutarıyla eşleşiyorsa deftere nakledilebilir. (Net tutar, TDS kesildikten sonraki fatura miktarıdır).

Örneğin, 50.000 değeri için bir satış faturası oluşturulur ve buna **%10** TDS grubu iliştirilir. Deftere nakledilen fatura tutarı 45.000'dir, satış faturası için deftere nakledilen TDS tutarı 5.000'dir. Şirketlerarası satış siparişi için otomatik olarak bir satınalma siparişi oluşturulur ve buna **%10** TDS grubu iliştirilir. TDS grubunu **%15** olarak değiştirirseniz, otomatik olarak oluşturulan şirketlerarası satış siparişinin net faturası tutarı orijinal satış siparişinin net fatura tutarıyla eşleşmediğinden, faturayı deftere nakledemezsiniz.

Şirketlerarası bir fatura için oluşturulan ödeme günlükleri otomatik olarak deftere nakledilir. Ödeme günlüğü yalnızca, bu satırdaki net ödeme tutarı orijinal ödeme günlüğündeki net ödeme tutarıyla eşleşiyorsa nakledilebilir.
