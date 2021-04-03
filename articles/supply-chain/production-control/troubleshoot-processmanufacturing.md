---
title: Süreç üretimi ile ilgili sorunları giderme
description: Bu konuda, süreç üretimi ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71ff5eeb2065a67281393777937d50237ab78d5e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259734"
---
# <a name="troubleshoot-process-manufacturing"></a>Süreç üretimi ile ilgili sorunları giderme

Bu konuda, süreç üretimi ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>Bir üretim emrindeki son projedeki kısmi miktarı raporlamak için iş kartı cihazını kullandığımda, Devam ediyor durumundaki tüm önceki işler otomatik olarak sonlandırılıyor.

Bu davranış tasarımdan kaynaklanır. **Üretim emri Varsayılanları** sayfasında, **Tamamlandı olarak bildir** sekmesinde, **Rotaya bitiş işareti yerleştir** adlı bir seçenek vardır. Bu seçenek *Evet* olarak ayarlanırsa bir çalışan son işlemi bildirmek üzere iş kartı cihazını veya iş kartı terminalini kullandığında rota kartı günlüğü deftere nakledilir. Bu günlük tüm işlemleri tamamlandı olarak işaretler ve tüm üretim işlerini sonlandırır. **Rotaya bitiş işareti ekle** seçeneği *Evet* olarak ayarlandığında sistem, çalışanın son işlemi bildirdiğinde seçtiği iş durumunu dikkate almaz. Sistem aynı zamanda çalışanın tam mı yoksa kısmi bir miktar mı bildirdiğini de dikkate almaz.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>Stok kapanışı yapmaya çalıştığımda, aşağıdaki uyarı iletisini alıyorum: "Bir %1 tarihi eşleştirme dönemi sonuyla hiçbir geriye dönük maliyet hesaplama yürütmesi kaydedilmedi."

10.0.13 öncesi sürümlerde, stok kapatma sırasında aşağıdaki hatalı uyarı iletisini alırsınız:

> Bir stok kapanışını bir %1 tarihiyle yürütmek üzeresiniz. Bir %1 tarihi eşleştirme dönemi sonuyla hiçbir geriye dönük maliyet hesaplama yürütmesi kaydedilmedi. Bir %1 tarihi eşleştirme dönemi sonuyla bir geriye dönük maliyet hesaplaması yürütmeyi unutmayın. Stok değerlemesi, satılan malların maliyeti ve varyantlar, bu işlem yürütülünceye kadar Yardımcı Kayıt Defteri veya Genel Kayıt Defteri'nde doğru olmayabilir.

Bu sorun 10.0.13 ve sonraki sürümlerde giderilmiştir. Daha fazla bilgi için bkz. [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]