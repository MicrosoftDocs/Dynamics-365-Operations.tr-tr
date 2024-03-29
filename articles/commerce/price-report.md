---
title: Perakende fiyatı raporları
description: Bu makale, çeşitli ürünler için gelecekteki fiyat değişiklikleri görmek için kullanılan fiyat raporlama özelliğine bir genel bakış sağlar.
author: ShalabhjainMSFT
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 09350d15660978126d36199a3b4e93f6be5fe157
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269040"
---
# <a name="retail-price-reports"></a>Perakende satış fiyatı raporları

[!include [banner](includes/banner.md)]


Müşterilerine rekabetçi fiyatlar sunabilmek için perakendeciler ürünlerinin fiyatını sıklıkla değiştirir. Mağaza yöneticileri, geçmişte veya gelecekteki fiyat değişikliklerine hızlı erişime sahip olmak isterler, bu sayede mağaza raflarında gösterilen fiyat etiketlerini güncelleştirmek için gerekli kaynakları planlayabilirler. Retail 10.0 sürümünün yayınlanmasıyla, bir mağaza yöneticisi **Fiyat** raporunu **Tüm perakende mağazaları \> Mağaza \> Fiyat raporu**'na giderek ve mağaza ile ilişkilendirilmiş ürünlerin fiyatlarını görüntülemek ve güncelleştirmek için açabilirler. 

Fiyat raporunu etkinleştirmek için **Mağaza için fiyat raporunu etkinleştir** parametresinin açık olması gerekir. Bu parametre **Ticaret parametreleri \> İskontolar \> Çeşitli** sekmesinde bulunur. **Fiyat raporu** sayfasını açmak, çeşitli yapılandırmaları içeren bir iletişim kutusunu görüntüler. Kullanılabilir yapılandırmalar aşağıda listelenmiştir.

| Konfigürasyon | Açıklama |
|---|---|
| Başlangıç tarihi / Bitiş tarihi| Fiyat raporunun oluşturulacağı veri aralığı. Güncel süre sınırı 7 gündür. |
| Kanal| Fiyat raporunun oluşturulacağı mağazası. |
| Ürünleri kullanılabilir stokla birlikte görüntüle| Bunu **Evet** olarak ayarlamak, mağazada yalnızca fiziksel stoku bulunan ürünler için fiyatları listeler. |
| Çeşitler için fiyatları görüntüle | Bunu **Evet** olarak ayarlamak, ana ürünlerle birlikte ürün çeşitlerinin de fiyatlarını görüntüler. Bu yalnızca çeşide özel fiyatlarınız varsa **Açık** olarak seçilmelidir, çünkü satırların sayısı çok artar. Gelecekteki sürümlerde, boyuta bağlı fiyatları etkileştireceğiz ve böylece mağaza yöneticisi, fiyatların görüntülenmesi istediği boyutları seçebilecek. |
| Ürünleri fiyat değişiklikleriyle birlikte görüntüle | Bu ayarı **Evet** olarak işaretlemek, yalnızca fiyatların değiştiği tarihlerdeki fiyatları görüntüler. *Bir önceki gün* fiyatı için seçilen **Başlangıç tarihi** her zaman görüntülenecektir, böylece mağaza yöneticisi seçilen sürenin tamamında fiyatları değişmemiş ürünleri kolayca tespit edebilir ve geçerli fiyatı da görüntüleyebilir. |

Rapor oluşturulduktan sonra Excel dosyası ek filtreleme ihtiyaçlarını gidermek için indirilebilir. Fiyat raporu, geçmiş tarihlerdeki ürünlerin eski fiyatlarını denetlemek için de kullanılabilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
