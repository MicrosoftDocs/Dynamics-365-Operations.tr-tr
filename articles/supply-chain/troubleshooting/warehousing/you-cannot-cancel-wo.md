---
title: Bir kullanıcıdaki çalışmayı iptal edemezsiniz
description: Bir kullanıcıdaki çalışmayı iptal edemezsiniz
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
ms.openlocfilehash: 1d7b0140d0c2724234a549ca4dfb23109012654abe0e60fcea1f98e8f17c153a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748703"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>Bir kullanıcıdaki çalışmayı iptal edemezsiniz

Hata kodu: WAX708

## <a name="symptoms"></a>Belirtiler

Sistem, aşağıdaki hata iletisini gösterir:

> Kullanıcı üzerindeki bir işi iptal edemezsiniz.

## <a name="cause"></a>Nedeni

İş, bir kullanıcı tarafından kilitlenmiş ve iptal edilemiyor. Bunu onaylamak için, iş kodunu açın ve **Genel** sekmesini açın. İş kilitliyse, **İş durumu** alanı *Devam ediyor* olarak ayarlıdır ve **Kilitleyen** alanında bir kullanıcı kimliği bulunur.

## <a name="resolution"></a>Çözünürlük

İşi iptal etmek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.
1. **İş kimliği** alanında, iptal etmek istediğiniz iş kaydının kodunu belirtin.
1. **Tamam**'ı seçin.
1. Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.

Daha fazla bilgi için bkz. [Özel durum işleme için ambar işini iptal etme](../../warehousing/cancel-warehouse-work.md).
