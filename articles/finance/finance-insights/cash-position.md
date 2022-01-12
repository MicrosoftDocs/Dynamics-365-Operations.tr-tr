---
title: Nakit pozisyonu
description: Bu konuda, Nakit akışı tahmini özelliğinin belirli bir dönem için bir kuruluşun nakit pozisyonunu nasıl tahmin ettiği açıklanmaktadır. Ayrıca, farklı dönemlerin tahminlerini göstermek için kullanılabilen seçenekler de açıklanmıştır.
author: ShivamPandey-msft
ms.date: 12/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 6bb99084a2ffef067dd0d7158ecb5e57d6d97d75
ms.sourcegitcommit: c8dc60bb760553f166409c2e06dd2377f601c006
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/23/2021
ms.locfileid: "7945816"
---
# <a name="cash-position"></a>Nakit pozisyonu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nakit pozisyonu, yakın döneme yönelik bir tahmin olan nakit akışı tahminidir. Bu tahmin, ödeme bekleyen fatura ve siparişleri ödeyen müşterilerden gelen nakit tahsilatlarının tahminine ve satın alma faturaları ile siparişleri için satıcılara ödenen nakit ödemelerinin tahminine dayalıdır.

Sistem, müşteri ödemelerini tahmin ederken müşteri ödeme tahmini özelliğinden ödeme tahminlerini kullanır. Ödeme tahminleri olmaksızın, her müşteri için müşteri faturasını ödemeye dönüştürmek için gerekli ortalama süre kullanılarak ödeme tarihi hesaplanır. Açık müşteri siparişleri için sistem, faturalandırılacak müşteri başına sipariş satırları için ortalama gün sayısını kullanarak fatura tarihini hesaplar. Ardından, fatura tarihini ödeme tahmini işlevi için giriş olarak kullanır. Müşteri ödeme tahmin işlevi, her sipariş satırı için bir ödeme tarihi hesaplar. 

Bekleyen faturaların ödeme tarihi, tahmin edilen demet olasılıklarından elde edilen kümülatif dağılım işlevinin yüzde ellisine karşılık gelen bir tarih seçerek ödeme tahminlerinden hesaplanır.

Satıcılara yapılan ödemeleri tahmin etmek için benzer bir yaklaşım kullanılır. Sistem, her satıcıyla ilgili olarak bir satıcı faturasını ödemeye dönüştürmek için gereken ortalama süreyi hesaplar. Ardından bu gün sayısı, ödeme tarihini hesaplamak için kullanılır. Açık satıcı siparişleri için sistem, her satıcı için sipariş satırlarını faturaya dönüştürmek için gereken ortalama gün sayısını dikkate alarak fatura tarihini hesaplar. Ardından sistem, her satıcıyla ilgili olarak satıcı faturasını ödemeye dönüştürmek için gereken ortalama süreyi kullanarak ödeme tarihini hesaplar.

**Nakit pozisyonu** sekmesinin üst bölümünde nakit pozisyonu grafiği bulunur. Bu grafikte nakit girişleri, çıkışları ve bunların toplam likidite bakiyesine etkileri gösterilir. Nakit pozisyonu grafiğindeki ayrıntılar günlük, haftalık, aylık veya üç aylık dönemlerde görüntülenebilir. **Günlük** seçeneğini belirlediğinizde, sonraki 21 gün için tahminleri görüntüleyebilirsiniz. **Haftalık** seçeneğini belirlediğinizde, sonraki 20 hafta için tahminleri görüntüleyebilirsiniz. **Aylık** seçeneğini belirlediğinizde, sonraki 12 ay için tahminleri görüntüleyebilirsiniz. **Üç Aylık** seçeneğini belirlediğinizde, sonraki 12 üç ay için tahminleri görüntüleyebilirsiniz. **Nakit pozisyonu** sekmesindeki içeriği görüntülemek için ekranınızda ek alana gereksinim duyarsanız grafiği gizleyebilirsiniz.

**Nakit pozisyonu** sekmesinin alt bölümünde pozisyon, nakit akışı, öngörülen ödemeler ve banka hesabı ile ilgili ayrıntılar gösterilir.

- **Pozisyon ayrıntıları** ızgarasındaki bilgiler üç bölümde gösterilir: likidite hesaplarının listesi, nakit girişlerini oluşturan belgelerin listesi ve nakit çıkışlarını oluşturan belgelerin listesi. Izgara, nakit pozisyonu bakiyelerini de gösterir. Görüntülemekte olduğunuz ilk dönem için, likidite hesaplarının bakiyesi açılış bakiyesidir. Sonraki dönemlerde, likidite hesaplarının bakiyeleri nakit girişleri ekleme ve önceki dönemlere ait nakit çıkışlarını çıkarma işlemi temel alınarak hesaplanır. Bakiyeyi oluşturan hareketlerin ayrıntılarını görüntülemek için **Bakiye** bağlantısını seçin.
- **Nakit akışı** ızgarasında nakit girişleri, dönem başına toplanan nakit akışları ve bunların likidite hesabı bakiyelerine etkileri gösterilir. İlk dönem için, likidite hesaplarının bakiyesi açılış bakiyesidir. Sonraki dönemlerde, likidite hesaplarının bakiyeleri nakit girişleri ekleme ve önceki dönemlere ait nakit çıkışlarını çıkarma işlemi temel alınarak hesaplanır.
- **Öngörülen banka bakiyesi** ızgarasında beklenen nakit çıkışları ve bunların likidite hesaplarına etkileri gösterilir.
- **Banka hesabı** ızgarasında, beklenen nakit girişleri ve çıkışlarının banka bakiyesine etkisi gösterilir.

Nakit pozisyonunu kaydetmek ve düzenlemek için anlık görüntü oluşturun. Anlık görüntülerle nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Anlık görüntülere genel bakış](payment-snapshots.md).

## <a name="details-of-the-cash-position-capability"></a>Nakit pozisyonu özelliğinin ayrıntıları 

Nakit pozisyonu özelliği aşağıdaki işlevleri içerir. 

- Nakit pozisyonu özelliği, sistemdeki varolan belgelere dayalı nakit akışını ve harici sistemlerden içe aktarılan nakit giriş ve çıkış satırlarını gösterir.
- Harici sistemlerden gelen nakit akışı verilerini Dynamics 365 Finance'e tümleştirmeyi kolaylaştırır. Nakit pozisyonu, veri içe-dışa aktarma çerçevesini de kullanabilir. Bu çerçeve Excel OData ile tümleştirmeyi kolaylaştırır. Ayrıca, kapsamlı bir nakit pozisyonu çözümü oluşturmak için birden fazla kaynaktaki verileri birleştirebilirsiniz.
- Akıllı bir nakit pozisyonu sağlar. Nakit pozisyonu, şirketin hesaplarına nakit gelmesini bekleyebileceği zamanı tahmin etmek için müşterinin ödeme davranışına göre oluşturulur.
- Müşteri siparişleri ve faturaları için müşteri ödeme tahmini AI işlevi, bir sipariş veya fatura ödeneceği sırada müşterinin geçmiş ödeme davranışlarını belirlemek için kullanılır.
- Satıcı siparişleri ve faturalarında, bir satıcı siparişi veya faturasının ne zaman ödeneceğini belirleyerek nakit çıkışlarını daha doğru hale getirmek için satıcı başına sevkiyat ve fatura ile fatura ödeme arasında ortalama bir süre kullanırız.

Bu, haznedar için geçmiş ödeme davranışlarına dayalı olarak daha doğru bir nakit akışı görünümü oluşturur. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
