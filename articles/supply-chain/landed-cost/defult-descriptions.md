---
title: Genel muhasebe için varsayılan açıklamalar
description: Varsayılan açıklamalar, fiş deftere nakillerinde Açıklama alanını genel muhasebeye güncelleştirmek için kullanılabilir.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: c68d0ae43ee2350225a0a0e32578f300b8faebe18aa575a5f737a49fd4c0c1a3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736731"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Genel muhasebe için varsayılan açıklamalar

[!include [banner](../../includes/banner.md)]

Varsayılan açıklamalar, fiş deftere nakillerinde **Açıklama** alanını genel muhasebeye güncelleştirmek için kullanılabilir. Bu işlevsellik, Varış yeri maliyetiyle çalışacak şekilde geliştirilmiştir.

Genel muhasebe deftere nakilleri için varsayılan açıklamaları ayarlamak üzere, **Kuruluş yönetimi \> Kurulum \> Varsayılan açıklamalar**'a gidin.

Aşağıdaki tabloda, Varış yeri maliyetini desteklemek için **Varsayılan açıklamalar** sayfasındaki **Açıklama** alanı için eklenen yeni değerler listelenmiştir.

| Açıklama türü | Notlar |
|---|---|
| İthalat maliyetlendirmesi - Maliyet tahakkuku | Bir satın alma siparişi faturası deftere nakledildiğinde, tahmini seyahat maliyetleri için bir maliyet tahakkuku işlenir. Açıklamaya yolculuk numarasını eklemek için varsayılan açıklamalar belirtilebilir. Sevkiyat numarası için *%4* kullanın. |
| İthalat maliyetlendirmesi - Transitteki mal siparişi | Transitteki mal işlemesi kullanıyorsanız satın alma siparişi faturası deftere nakledilir ve mallar transitteki mallar hesabına nakledilir. Açıklamaya transitteki mal sipariş numarasını eklemek için varsayılan açıklamalar belirtilebilir. Transitteki sipariş numarası için *%4* kullanın. |
| Stok – kapatma – ayarlama | Borç hesapları (AP) faturası, bir yolculuk maliyeti için işlendiğinde, yolculuk maliyetlerini tahmin etmek için bir stok ayarlaması işlenir. Açıklamaya yolculuk numarasını eklemek için varsayılan açıklamalar belirtilebilir. Sevkiyat numarası için *%4* kullanın. |

**Varsayılan açıklamalar** sayfasıyla çalışma hakkında daha fazla bilgi için, bkz. [Otomatik deftere nakil için varsayılan açıklamaları ayarlama](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).
