---
title: Alacak dekontlarında özgün faturalara referans verme (satıcı faturaları)
description: Bu konuda, alacak dekontu oluşturduğunuzda özgün faturaya nasıl referans oluşturabileceğiniz açıklanmaktadır.
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6114ffb4d3b9e942887cbfa10c6039b0d73af7e1
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562238"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Alacak dekontlarında özgün faturalara referans verme (satıcı faturaları)

[!include [banner](../includes/banner.md)]

Bu konuda, alacak dekontu oluşturduğunuzda özgün faturaya nasıl referans oluşturabileceğiniz açıklanmaktadır.

## <a name="prerequisites"></a>Önkoşullar

**Özellik yönetimi** çalışma alanında, **Satıcı faturalarında alacak faturalamayı etkinleştir** özelliğini etkinleştirin. Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Bu konuda açıklanan işlevsellik aşağıdaki iş belgeleri için geçerlidir.

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
