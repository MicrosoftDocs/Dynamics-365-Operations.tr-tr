---
title: Dalga, temizlik için uygun değil
description: Dalga, temizlik için uygun değil
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 99d76b6a90045be7630785769b11e43abaf4b789b1c4a134050b6ee396c71199
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778518"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>Dalga, temizlik için uygun değil

Hata kodu: WaveNotEligibleForCleanup

## <a name="symptoms"></a>Belirtiler

Sistem, aşağıdaki hata iletisini gösterir:

> %1 dalgası temizleme işlemi için uygun değil.

Dalga verileri temizlenemiyor.  

## <a name="cause"></a>Nedeni

Aşağıdaki koşullardan biri tarafından gösterildiği gibi dalga şu anda işlenmektedir:

- **Dalga durumu** alanının ayarı *Yürütülüyor* olarak ayarlanmış.
- Eylem bölmesinin **Dalga** sekmesindeki **Dalga** grubunda **Toplu iş**'i seçtiğinizde, **Durum** alanı *Sonlandırıldı*, *Hata* veya *İptal edildi* olarak ayarlanmaz. Bu nedenle, bir toplu iş şu anda çalışıyor.

## <a name="resolution"></a>Çözünürlük

Eylem bölmesinde, **Dalga** sekmesinde, **Dalga** grubunda, **Toplu iş**'i seçin ve aşağıdaki adımlardan birini izleyin:

- **Durum** alanı *Yürütülüyor* olarak ayarlanmışsa: Eylem bölmesinde, **Toplu iş** sekmesinde, **Toplu iş** grubunda, **Görevleri görüntüle**'yi seçin. İlerlemeyi **Toplu iş görevleri** sayfasını yenileyerek izleyebilirsiniz.
- **Durum** alanı *Yürütülüyor* olarak ayarlanmamışsa: Eylem bölmesinde, **Toplu iş** sekmesinde, **İşlevler** grubunda, **Durumu değiştir**'i seçin. **Yeni durum seç** alanında, *Bekliyor*'u seçin. Daha sonra **Tamam**'ı seçin.
