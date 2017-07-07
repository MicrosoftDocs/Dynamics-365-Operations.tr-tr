---
title: "Satıcı çekleri örnek elektronik raporlama"
description: "Bu konu, Elektronik raporlama örnek çek biçimlerinin nasıl kullanılacağı hakkında genel bilgi sağlar."
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.dyn365.intro: 2017-06-30
ms.dyn365.version: Enterprise edition, July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 6cb473962f40ed9ef2f5f807f089098764f47009
ms.openlocfilehash: 8228690ee5ab7839ec19c307c23f9b6150006371
ms.contentlocale: tr-tr
ms.lasthandoff: 06/14/2017


---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a>Elektronik raporlama örnek çek biçimleri

Satıcı çeklerinizi biçimlendirmek için Elektronik raporlama (ER) kullanabilirsiniz. Pek çok bankaya özel çek sağlayıcısı–özel çek biçimi piyasada mevcuttur. Örnek çek biçimleri, ER araç havuzundaki Ödeme çeki modeline eklenmiştir. Bu örnek çekler **Ortadaki çek (ABD)** ve **Altına üst denetleme çeki (ABD)** olarak etiketlenmiştir.

## <a name="what-check-formats-are-currently-supported"></a>Hangi çek biçimleri şu anda desteklenmektedir?

Sürekli olarak Microsoft Dynamics Lifecycle Services'daki (LCS) Paylaşılan varlık kitaplığına gidip varlık türü **GER yapılandırması** olan mevcut dosyaların geçerli listesini görüntülemeniz gerekir. Sonraki "Neyi ayarlamam gerekiyor?" bölümünde, mevcut yapılandırmaları incelemek ve seçili yapılandırmaları içe aktarmak için bir LCS havuzunun nasıl oluşturulacağının açıklandığını açıklayan konuya bağlantı verilmektedir.

Microsoft Dynamics 365 for Finance and Operations, Enterprise edition çekin üstte bulunduğu ve iki havale bölümü tarafından izlenen bir örnek biçimi içermektedir. Ayrıca, çekin ortada, iki havale bölümü arasında bulunduğu bir örnek biçim de içermektedir. Bu örnek biçimleri, Deluxe iş çek biçimlerine karşılık gelir.

## <a name="what-do-i-have-to-set-up"></a>Neyi ayarlamam gerekiyor?

- ER kullanarak çek yazdırmadan önce, en az bir etkin çek yapılandırmasının ER yapılandırmanıza aktarılmış olması gerekir. Yönergeler için bkz. [Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle](/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
- Banka hesabı için Nakit ve banka yönetimini çeklerini yapılandırırken, **Genel elektronik Dışa aktarma biçimi** onay kutusunu seçin ve sonra uygun dışa aktarma biçim yapılandırmasını çek biçimi olarak seçin.
- Ayrıca, havale üzerine yazdırılacak makbuz satırlarının sayısını da belirtmeniz gerekir. Bu sayıyı hesaplarken başlık satırlarını eklediğinizden emin olun. İki örnek çek biçimi için, önerilen irsaliye satırı sayısı 17'dir. Bununla birlikte, bu sayı, çek stokunuz ve yazıcı sürücülerinize göre farklılık gösterecektir.
- Çek biçimini doğrulamak için bir test çeki yazdırmanızı öneririz. Bir test çeki yazdırmak için **Yazdırma testi** seçeneğini işaretleyin. Örnek çek biçimleri, Microsoft Excel için gelişmiş yazdırma özellikleri içinde **Kenar boşlukları** **Yok** olarak ayarlandığında en iyi çalışır. Test çeki oluşturulduktan sonra, Excel çıktısının düzenlenmesini etkinleştirin ve sayfa düzenini, tüm kenar boşlukları **0** (sıfır) olacak şekilde yapılandırın. Çeklerin test kopyasını, çek stokunuzla kıyaslayın ve hizalamadan tatmin olana kadar ayar yapın.
- Ödeme günlüğünde yapılandırılmış banka hesabı için ödemeler oluşturduğunuzda, çekler belirtilen biçim kullanılarak yazdırılır.

Daha fazla bilgi için [Bir Elektronik raporlamada biçimini değiştir](/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md) konusuna bakın.

