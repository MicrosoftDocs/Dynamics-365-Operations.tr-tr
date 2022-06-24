---
title: Alacak dekontlarında özgün faturalara referans verme (satıcı faturaları)
description: Bu makalede, alacak dekontu oluşturduğunuzda özgün faturaya nasıl referans oluşturabileceğiniz açıklanmaktadır.
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e05dddf056d86513d86ea925349f60ca25f191ca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901503"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Alacak dekontlarında özgün faturalara referans verme (satıcı faturaları)

[!include [banner](../includes/banner.md)]

Bu makalede, alacak dekontu oluşturduğunuzda özgün faturaya nasıl referans oluşturabileceğiniz açıklanmaktadır.

## <a name="prerequisites"></a>Önkoşullar

**Özellik yönetimi** çalışma alanında, **Satıcı faturalarında alacak faturalamayı etkinleştir** özelliğini etkinleştirin. Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Bu makalede açıklanan işlevsellik aşağıdaki iş belgeleri için geçerlidir.

**Borç hesapları:**

- Satın alma siparişi
- Fatura günlüğü
- Fatura defteri

**Genel muhasebe:**

- Yevmiye fişi

## <a name="define-a-reference-to-an-original-invoice"></a>Özgün faturaya referans tanımlama

Belirtilen iş belgesi türlerinde özgün faturaya bir referans tanımlamak için aşağıdaki yordamları kullanın.

### <a name="vendor-credit-note-purchase-order"></a>Satıcı alacak dekontu (satın alma siparişi)

1. **Borç hesapları** \> **Satın alma siparişleri** \> **Tüm satın alma siparişleri**'ne gidin.
2. Yeni bir satın alma siparişi oluşturun veya bir alacak dekontu oluşturmak için var olanı kullanın.
3. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Tanıt** grubunda **Alacak faturalaması**'nı seçin.
4. Düzeltme nedenini ve özgün faturaya olan referansı girin.

### <a name="vendor-credit-note-ledger-journals"></a>Satıcı alacak dekontu (genel muhasebe günlükleri)

1. Şu adımlardan birini izleyin:

    - **Borç hesapları** \> **Fatura günlükleri**'ne gidin.
    - **Borç hesapları** \> **Fatura defteri**'ne gidin.
    - **Genel muhasebe** \> **Yevmiye defteri girişleri** \> **Genel günlükler**'e gidin.

2. Yeni bir günlük ve yeni yevmiye defteri satırları oluşturun.
3. Eylem Bölmesi'nde, **İşlevler** \> **Alacak faturalama**'yı seçin.
4. Düzeltme nedenini ve özgün faturaya olan referansı girin.

> [!NOTE]
> **Hesap türü** alanı **Satıcı** olarak ayarlanmışsa **Alacak faturalama** komutu bir yevmiye defteri fişinde görünür.
