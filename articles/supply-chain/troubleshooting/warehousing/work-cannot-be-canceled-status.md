---
title: İş, durumu nedeniyle iptal edilemiyor
description: İş, durumu nedeniyle iptal edilemiyor
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
ms.openlocfilehash: f983501b490c5516525b4d5904603ed62e8799f9e6124e5672b36a12804ecb0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755990"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>İş, durumu nedeniyle iptal edilemiyor

Hata kodu: WAX2190

## <a name="symptoms"></a>Belirtiler

Sistem, aşağıdaki hata iletisini gösterir:

> İş %1 %2 durumunda olduğu için, iptal edemezsiniz.

## <a name="cause"></a>Nedeni

İş, geçerli durumunda iptal edilemez.

İş başlığı veya iş satırları, beklenen **İş durumu** değerine sahip değil. İş başlığındaki **İş durumu** alanı *Açık* veya *Devam ediyor* olarak ayarlı değil.

## <a name="resolution"></a>Çözünürlük

İşi iptal etmek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.
1. **İş kimliği** alanında, iptal etmek istediğiniz iş kaydının kodunu belirtin.
1. **Tamam**'ı seçin.
1. Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.

Daha fazla bilgi için bkz. [Özel durum işleme için ambar işini iptal etme](../../warehousing/cancel-warehouse-work.md).
