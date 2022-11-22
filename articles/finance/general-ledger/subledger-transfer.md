---
title: Yardımcı defterden genel muhasebeye transfer
description: Bu makale, genel muhasebedeki yardımcı defter aktarma işlemiyle ilgili olan özellikleri açıklar.
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7ef93b81ce37128f7ff400eb4034ffea01756038
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779866"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Yardımcı defterden genel muhasebeye transfer

[!include [banner](../includes/banner.md)]

Bu makalede, yardımcı defter günlük girişleri toplu işleri aktarma kurallarıyla ilişkili özellikler açıklanmaktadır.

Sürüm 8.1'de kuralların aktarılmasına izin vermek için değişiklikler yapıldı ve **Zaman Uyumlu** seçeneği kullanım dışı bırakıldı. Daha fazla bilgi için bkz. [Finans ve operasyon uygulamaları için kaldırılan veya kullanımına son verilen özellikler](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Alt genel muhasebe toplu işlemlerine transfer için aşağıdaki seçenekler kullanılabilir:

- **Zaman uyumsuz**: Yardımcı defter muhasebe girişlerinin genel muhasebeye transferi hemen zamanlanır. Kaynaklar bu isteği sunucuda işlemek için kullanılabilir olur olmaz Genel muhasebe fişi kaydedilecektir.
- **Zamanlanmış toplu iş**: Transfer edilmesi gereken yardımcı defter muhasebe girişleri Genel muhasebedeki işleme kuyruğuna eklenir. Kuyruktaki girişler alındıkları sırada işlenir. Kaynaklar toplu işi sunucuda işlemek için kullanılabilir durumdaysa, her Genel muhasebe fişi hesapları planlanan zamanda güncelleştirir.

**Zaman uyumsuz** seçeneğinin performansını artırmak için iyileştirmeler yapılmıştır. Bu özellik, performansın en iyi duruma getirilmesi **Genel muhasebe Özellik adı alt genel muhasebe aktarımı** altında etkinleştirilir.

Yardımcı defter toplu işlerinin zaman uyumsuz aktarımı işlevi, yardımcı defterden genel muhasebeye veri aktarımını iyileştirmeye yardımcı olur. İşlev, daha küçük hareket kümelerini gruplayarak ve hareketleri gruplar halinde aktararak hareketleri daha verimli bir şekilde işler. Hareketler gruplandığında, toplu iş sunucusunun kaynakları daha verimli kullanılır.

Alt genel muhasebe toplu işlemlerine ilişkin zaman uyumsuz aktarım toplu iş görevleri, toplu iş sunucusunda hemen yürütülmek üzere oluşturulduğundan, bu işlem sunucusunun ayarlanmasını, çevrimiçi olmasını ve çalışmasını gerektirir. **Genel muhasebeye alt muhasebe aktarımı performansını iyileştirme** özelliği etkinken, **Süreç otomasyonu yoklama sistem işi** adlı **Süreç otomasyonu** sistem toplu işi de etkinleştirilmelidir. Daha fazla bilgi için bkz. [İşlem otomasyonu](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

Toplu iş düzeyindeki verimlilik değişikliği, sistemdeki tüm tüzel kişilikler için yinelenen tek bir toplu işlem kullanır. Çalışma zamanında, henüz transfer edilmemiş gerekli kayıtları işlemek için yeni bir toplu işlem oluşturulur. Sistem yönetimindeki **İşlem otomasyonu** sayfasından daha fazla ayar kontrol edilebilir. Bu sayfada, arka plan işlemini değiştirebilir, sıklığı değiştirebilir ve bir uyku süresi tanımlayabilirsiniz.

İşlem otomasyonu kurulumu hakkında daha fazla bilgi için bkz. [İşlem otomasyonu](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

