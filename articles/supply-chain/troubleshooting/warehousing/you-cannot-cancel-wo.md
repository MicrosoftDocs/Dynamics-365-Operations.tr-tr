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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924413"
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
