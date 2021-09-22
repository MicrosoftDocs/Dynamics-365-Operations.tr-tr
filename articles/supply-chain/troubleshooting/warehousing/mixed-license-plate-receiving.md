---
title: Karma plaka alma işlemi tüm değerlendirme kodları için çalışmıyor
description: Değerlendirme kodunun Eylem alanı Alacak veya Hurda olarak ayarlandığında , iade edilen maddeleri işlemek için yalnızca Karma plaka alma işlemi menü öğesini kullanabilirsiniz.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b762255bc5ef6a1e15688a9c635940e92e67db3c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477873"
---
# <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-but-credit"></a>Karma plaka alma işlemi Alacak dışındaki herhangi bir değerlendirme kodu için çalışmıyor

## <a name="symptoms"></a>Belirtiler

Değerlendirme kodunun **Eylem** alanı *Alacak* veya *Hurda* olarak ayarlandığında , iade edilen maddeleri işlemek için yalnızca [Karma plaka alma işlemi](/dynamics365/supply-chain/warehousing/mixed-license-plate-receiving) menü öğesini kullanabilirsiniz.

## <a name="resolution"></a>Çözüm

Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir. Şu anda, karma plaka alma işlemi için yalnızca **Eylem** alanı *Alacak* veya *Hurda* olarak ayarlanan [değerlendirme kodları](/dynamics365/supply-chain/service-management/set-up-disposition-codes) desteklenmektedir.
