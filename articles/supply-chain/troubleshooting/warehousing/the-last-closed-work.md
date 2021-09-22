---
title: Kapatılan son iş satırı, yerine koy olmalıdır
description: Kapatılan son iş satırı, yerine koy olmalıdır
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 221c64c89d0e8addbf44acab8e7561e5f3a27239
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474760"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>Kapatılan son iş satırı, yerine koy olmalıdır

Hata kodu: WAX1285

## <a name="symptoms"></a>Belirtiler

Sistem, aşağıdaki hata iletisini gösterir:

> Kapatılan son iş satırı, yerine koy olmalıdır.

## <a name="cause"></a>Nedeni

İş, geçerli durumunda iptal edilemez.

Son iş satırında, **İş durumu** alanı *Kapalı* olarak ayarlı ancak **İş türü** alanı *Yerine koy* olarak ayarlanmamış.

## <a name="resolution"></a>Çözünürlük

İşi iptal etmek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.
1. **İş kimliği** alanında, iptal etmek istediğiniz iş kaydının kodunu belirtin.
1. **Tamam**'ı seçin.
1. Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.

Daha fazla bilgi için bkz. [Özel durum işleme için ambar işini iptal etme](../../warehousing/cancel-warehouse-work.md).
