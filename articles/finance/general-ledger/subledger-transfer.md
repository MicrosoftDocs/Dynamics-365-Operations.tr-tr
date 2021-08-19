---
title: Yardımcı defterden genel muhasebeye transfer
description: Bu konu, genel muhasebedeki alt defter transfer işlemiyle ilgili olan özellikleri açıklar.
author: rcarlson
ms.date: 07/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 03c04a5eb8b544b582019ddd204382900b162d952842c901f69ed4a853bd8183
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716657"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Yardımcı defterden genel muhasebeye transfer

[!include [banner](../includes/banner.md)]

Bu konuda, yardımcı defter günlük girişleri toplu işleri aktarma kurallarıyla ilişkili özellikleri açıklanmaktadır.

Sürüm 8.1'de kuralların aktarılmasına izin vermek için değişiklikler yapıldı ve **Zaman Uyumlu** seçeneği kullanım dışı bırakıldı. Daha fazla bilgi için bkz. [Finance and Operations için kaldırılan veya artık kullanılmayan özellikler](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Alt genel muhasebe toplu işlemlerine transfer için aşağıdaki seçenekler kullanılabilir:

- **Zaman uyumsuz**: Yardımcı defter muhasebe girişlerinin genel muhasebeye transferi hemen zamanlanır. Kaynaklar bu isteği sunucuda işlemek için kullanılabilir olur olmaz Genel muhasebe fişi kaydedilecektir.
- **Zamanlanmış toplu iş**: Transfer edilmesi gereken yardımcı defter muhasebe girişleri Genel muhasebedeki işleme kuyruğuna eklenir. Kuyruktaki girişler alındıkları sırada işlenir. Kaynaklar toplu işi sunucuda işlemek için kullanılabilir durumdaysa, her Genel muhasebe fişi hesapları planlanan zamanda güncelleştirir.

Sürüm 10.0.8'de **Zaman uyumsuz** seçeneğinin performansını artırmak için iyileştirmeler yapılmıştır. Bu özellik, performansın en iyi duruma getirilmesi **Genel muhasebe Özellik adı alt genel muhasebe aktarımı** altında etkinleştirilir.

Yardımcı defter toplu işlerinin zaman uyumsuz aktarımı işlevi, yardımcı defterden genel muhasebeye veri aktarımını iyileştirmeye yardımcı olur. İşlev, daha küçük hareket kümelerini gruplayarak ve hareketleri gruplar halinde aktararak hareketleri daha verimli bir şekilde işler. Hareketler gruplandığında, toplu iş sunucusunun kaynakları daha verimli kullanılır.

Yardımcı defter toplu işlerinin zaman uyumsuz aktarımı, toplu iş sunucusunun kurulmuş, çevrimiçi ve çalışır olmasını gerektirir. Aksi takdirde, **Zaman Uyumsuz** aktarım seçeneği çalışmaz.

Toplu iş düzeyindeki verimlilik değişikliği, sistemdeki tüm tüzel kişilikler için yinelenen tek bir toplu işlem kullanır. Çalışma zamanında, henüz transfer edilmemiş gerekli kayıtları işlemek için yeni bir toplu işlem oluşturulur. Sistem yönetimindeki **İşlem otomasyonu** sayfasından daha fazla ayar kontrol edilebilir. Bu sayfada, arka plan işlemini değiştirebilir, sıklığı değiştirebilir ve bir uyku süresi tanımlayabilirsiniz.

İşlem otomasyonu kurulumu hakkında daha fazla bilgi için bkz. [İşlem otomasyonu](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
