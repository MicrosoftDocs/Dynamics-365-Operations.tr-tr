---
title: Satıcı çekleri için elektronik raporlama örneği
description: Bu makalede, Elektronik raporlama örnek çek biçimlerinin nasıl kullanılacağı hakkında genel bilgiler sağlanmaktadır.
author: mrolecki
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6863acaa264cfb8f15c34e85811a94afc67bec5e
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715275"
---
# <a name="electronic-reporting-sample-vendor-checks"></a>Satıcı çekleri örnek elektronik raporlama

[!include [banner](../includes/banner.md)]

Satıcı çeklerinizi biçimlendirmek için Elektronik raporlama (ER) kullanabilirsiniz. Pek çok bankaya özel çek sağlayıcısı–özel çek biçimi piyasada mevcuttur. Örnek çek biçimleri, ER araç havuzundaki Ödeme çeki modeline eklenmiştir. Bu örnek çekler **Ortadaki çek (ABD)** ve **Altına üst denetleme çeki (ABD)** olarak etiketlenmiştir.

## <a name="what-check-formats-are-currently-supported"></a>Hangi çek biçimleri şu anda desteklenmektedir?

Sürekli olarak Microsoft Dynamics Lifecycle Services'daki (LCS) Paylaşılan varlık kitaplığına gidip varlık türü **GER yapılandırması** olan mevcut dosyaların geçerli listesini görüntülemeniz gerekir. Sonraki "Neyi ayarlamam gerekiyor?" bölümünde, mevcut yapılandırmaları incelemek ve seçili yapılandırmaları içeri aktarmak için bir LCS deposunun nasıl oluşturulacağını açıklayan makalenin bağlantısı verilmektedir.

 Microsoft Dynamics 365 Finance ayrıca, çekin üstte olduğu ve bunu iki havale bölümünün izlediği örnek bir biçim içermektedir. Ayrıca, çekin ortada, iki havale bölümü arasında bulunduğu bir örnek biçim de içermektedir. Bu örnek biçimleri, Deluxe iş çek biçimlerine karşılık gelir.

## <a name="what-do-i-have-to-set-up"></a>Neyi ayarlamam gerekiyor?

- ER kullanarak çek yazdırmadan önce, en az bir etkin çek yapılandırmasının ER yapılandırmanıza aktarılmış olması gerekir. Yönergeler için bkz. [Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
- Banka hesabı için Nakit ve banka yönetimini çeklerini yapılandırırken, **Genel elektronik Dışa aktarma biçimi** onay kutusunu seçin ve sonra uygun dışa aktarma biçim yapılandırmasını çek biçimi olarak seçin.
- Ayrıca, havale üzerine yazdırılacak makbuz satırlarının sayısını da belirtmeniz gerekir. Bu sayıyı hesaplarken başlık satırlarını eklediğinizden emin olun. İki örnek çek biçimi için, önerilen irsaliye satırı sayısı 17'dir. Bununla birlikte, bu sayı, çek stokunuz ve yazıcı sürücülerinize göre farklılık gösterecektir.
- Çek biçimini doğrulamak için bir test çeki yazdırmanızı öneririz. Bir test çeki yazdırmak için **Yazdırma testi** seçeneğini işaretleyin. Örnek çek biçimleri, Microsoft Excel için gelişmiş yazdırma özellikleri içinde **Kenar boşlukları** **Yok** olarak ayarlandığında en iyi çalışır. Test çeki oluşturulduktan sonra, Excel çıktısının düzenlenmesini etkinleştirin ve sayfa düzenini, tüm kenar boşlukları **0** (sıfır) olacak şekilde yapılandırın. Çeklerin test kopyasını, çek stokunuzla kıyaslayın ve hizalamadan tatmin olana kadar ayar yapın.
- Ödeme günlüğünde yapılandırılmış banka hesabı için ödemeler oluşturduğunuzda, çekler belirtilen biçim kullanılarak yazdırılır.

Daha fazla bilgi için [Bir Elektronik raporlamada biçimini değiştir](../../fin-ops-core/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md) konusuna bakın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
