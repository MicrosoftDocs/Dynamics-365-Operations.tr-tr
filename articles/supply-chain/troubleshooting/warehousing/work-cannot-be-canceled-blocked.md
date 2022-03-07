---
title: İş, durdurulduğu için iptal edilemiyor
description: İş, durdurulduğu için iptal edilemiyor
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924291"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>İş, durdurulduğu için iptal edilemiyor

Hata kodu: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>Belirtiler

Sistem, aşağıdaki hata iletisini gösterir:

> %1 işi, neden türü %2 tarafından engellendiğinden iptal edilemiyor. İşin iptal edilebilmesi için öncelikle durdurmanın kaldırılması gerekiyor.

## <a name="cause"></a>Nedeni

İş durdurulmuş ve iptal edilemiyor.

**Çalışma** sayfasında, **Genel** sekmesinde, **Durdurulmuş** seçeneği *Evet* olarak ayarlı. Bu ayar, çalışmanın durdurulduğunu belirtir. **Durdurma nedenleri** sekmesi, çalışmanın neden durdurulduğunu gösterir.

## <a name="resolution"></a>Çözünürlük

Çalışmanın durdurmasını kaldırmak için, **Durdurma nedenleri** sekmesini seçin ve aşağıdaki adımlardan birini izleyin:

- **Çalışma durdurma nedeni** alanı *Tanımsız neden* olarak ayarlanmışsa: Eylem Bölmesinde, **Çalışma** sekmesinde, **Çalışma** grubunda, **Çalışma engelini kaldır**'ı seçin.
- **Çalışma durdurma nedeni** alanı, *Dalga işleniyor* olarak ayarlanmışsa : Eylem Bölmesinde, **İlgili bilgiler** sekmesinde, **İlgili bilgiler** grubunda **Dalga** seçeneğini belirleyin. Ardından, **Dalgalar** sayfasında, Eylem Bölmesinde, **Dalga** sekmesini açın ve **Dalga** grubundan **Dalga verisini temizle**'yi seçin.

## <a name="workaround"></a>Geçici çözüm

Önceki adımlar sorunu gidermezse, aşağıdaki adımları izleyerek işi iptal edebilirsiniz.

1. **Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.
1. **Çalışma kodu** alanında, iptal etmek istediğiniz şu anda **Çalışma durumu** değeri *Açık*, *Devam ediyor*, *İptal edildi*, *Birleştirilmiş* veya *Kapalı* olan çalışmanın kodunu belirtin.
1. **Tamam**'ı seçin.
1. Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.

Daha fazla bilgi için bkz. [Özel durum işleme için ambar işini iptal etme](../../warehousing/cancel-warehouse-work.md).
