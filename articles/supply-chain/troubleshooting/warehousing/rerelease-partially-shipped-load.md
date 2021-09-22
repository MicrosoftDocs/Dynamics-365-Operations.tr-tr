---
title: Kısmen sevk edilen yük ambara yeniden serbest bırakılamıyor
description: Önceki sürümlerde, eksik rezervasyonlarla belirli işlevleri kullanırken kısmen sevk edilen bir yükü yeniden serbest bırakamazsınız. Bu sorun düzeltildi.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477865"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>Kısmen sevk edilen bir yük ambara yeniden serbest bırakılamıyor

## <a name="symptoms"></a>Belirtiler

Kısmen sevk edilen bir yükü ambara serbest bırakamazsınız. Ambara serbest bırakma işlemini gerçekleştirdiğinizde bir "İşlem tamamlandı" iletisi görüntülenir ancak hiçbir şey olmaz ve kalan miktar için hiçbir iş oluşturulmaz. Bu sorun, taşıma yükü işlevini kullandığınızda ve eksik bir ayırma varsa oluşur.

## <a name="resolution"></a>Çözüm

[KB sorunu 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Kısmen sevk edilen yükler yeniden dalgaya eklenebilir ve yeniden işlenebilir"), [sürüm 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15)'te düzeltilmiştir.
