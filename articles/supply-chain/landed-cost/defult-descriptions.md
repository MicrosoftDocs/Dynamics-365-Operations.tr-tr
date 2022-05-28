---
title: Genel muhasebe için varsayılan açıklamalar
description: Varsayılan açıklamalar, fiş deftere nakillerinde Açıklama alanını genel muhasebeye güncelleştirmek için kullanılabilir.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f95dff3a77a552d5788d813b3d13dc30579be715
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695721"
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
