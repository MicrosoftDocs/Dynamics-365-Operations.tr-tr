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
ms.openlocfilehash: a24f199484c7596189b19e4cddf344e9186c6044edd2906affca9b530de44168
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722211"
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
