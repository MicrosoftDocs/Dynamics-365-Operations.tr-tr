---
title: Çalışma durdurulmaya devam edildi
description: Çalışma durdurulmaya devam edildi
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924142"
---
# <a name="work-remains-blocked"></a>Çalışma durdurulmaya devam edildi

Hata kodu: WHSWorkBlockingExecutingWaveReason_ErrorMessage

## <a name="symptoms"></a>Belirtiler

Sistem, aşağıdaki hata iletisini gösterir:

> İlgili %2 dalgasının durumu %3 olduğundan, %1 işi engellenmiş olarak kaldı.

## <a name="cause"></a>Nedeni

Aşağıdaki koşullardan biri tarafından gösterildiği gibi çalışma şu anda dalgada işleniyor ve durdurulamıyor:

- **Durdurma nedenleri** sekmesinde, bir veya daha fazla satır için **İş durdurma nedeni** alanı, *Dalga işleniyor* olarak ayarlı.
- Eylem Bölmesi sekmesinin **İlgili bilgiler** sekmesindeki **İlgili bilgiler** grubunda **Dalga**'yı seçtiğinizde, **Dalga durumu** *İşleniyor* olarak ayarlanır.

## <a name="resolution"></a>Çözünürlük

Eylem Bölmesinde **İlgili bilgiler** sekmesindeki **İlgili bilgiler** grubunda **Dalga**'yı seçin. Ardından, **Dalgalar** sayfasında, Eylem Bölmesinde, **Dalga** sekmesini açın ve **Dalga** grubundan **Dalga verisini temizle**'yi seçin.

## <a name="workaround"></a>Geçici çözüm

Önceki adımlar sorunu gidermezse, aşağıdaki adımları izleyerek işi iptal edebilirsiniz.

1. **Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.
1. **Çalışma kodu** alanında, iptal etmek istediğiniz şu anda **Çalışma durumu** değeri *Açık*, *Devam ediyor*, *İptal edildi*, *Birleştirilmiş* veya *Kapalı* olan çalışmanın kodunu belirtin.
1. **Tamam**'ı seçin.
1. Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.

Daha fazla bilgi için bkz. [Özel durum işleme için ambar işini iptal etme](../../warehousing/cancel-warehouse-work.md).
