---
title: Global Stok Muhasebesi tarafından desteklenen iş belgeleri
description: Bu makalede, Global Stok Muhasebesi tarafından desteklenen iş belgeleri listelenmektedir. Ayrıca, satınalma siparişi belgeleri için ayrıntılı bir örnek sağlar.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0dee558de2defa7baae4bc4097c750e974c12a14
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135704"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a>Global Stok Muhasebesi tarafından desteklenen iş belgeleri

[!include [banner](../includes/banner.md)]

Global Stok Muhasebesi Eklentisi tam olarak ayarlandıktan sonra, Microsoft Dynamics 365 Supply Chain Management'a girilen stokla ilgili belgeleri işlemeye hazırdır.

## <a name="supported-business-documents"></a>Desteklenen iş belgeleri

İki türde iş belgesi vardır:

- **Günlüğü olan belgeler**: Bu belgeler ürün girişi, satınalma faturası, sevk irsaliyesi ve satış faturası belgelerini içerir.
- **Günlüğü olmayan belgeler**: Bu belgeler sayım, taşıma ve stok ayarlama belgelerini içerir.

Bu makalenin ilerleyen bölümlerinde, satınalma siparişleri işlemi göstermek için örnek olarak kullanılacaktır.

Aşağıdaki tabloda, geçerli sürümün desteklediği belgeler listelenir.

| Belge türü      | Belge        |
|--------------------|-----------------|
| Satın Alma Siparişi     | Ürün Girişi |
| Satın Alma Siparişi     | Fatura         |
| Satış Siparişi        | Sevk irsaliyesi    |
| Satış Siparişi        | Fatura         |
| Stok Günlükleri | Hareket        |
| Stok Günlükleri | Düzeltme      |
| Stok Günlükleri | Sayım        |
| Stok Günlükleri | Transfer        |
| Transfer Emri     | Sevkiyat        |
| Transfer Emri     | Al         |

> [!IMPORTANT]
> Global Stok Muhasebesi, Supply Chain Management'a girilen belgeleri zaman uyumsuz olarak işler. Sorunlu belgeler için hata iletisi gösterilmez.

## <a name="example-purchase-order"></a>Örnek: Satın alma siparişi

### <a name="product-receipt"></a>Ürün girişi

Ürün girişlerini her zamanki gibi deftere nakledin. **Tüm satınalma siparişleri** sayfasında bir satınalma siparişi seçin ve ardından Eylem Bölmesi'nde, **Al** sekmesinde **Ürün girişi günlüğü** sayfasını açmak için **Ürün girişi**'ni seçin. Her satır için bir operasyon olayı ve bir Global Stok Muhasebesi olayı oluşturulur. Bu nedenle, **Satırlar** sekmesini seçin ve ardından **Stok \> Olaylar ve ölçümler**'i seçerek **Olaylar ve ölçümler** sayfasını açın.

Global Stok Muhasebesi, olaylara ve ölçümlere dayanan bir muhasebe sistemidir. **Olaylar ve ölçümler** sayfasındaki ölçüm satırı ızgarası, ölçümlerin bir listesini gösterir. Her ölçümün bir boyut listesi vardır.

Her işlem olayı için iki tür ölçüm vardır:

- **Operasyon ölçümleri**: Bu ölçümler iş belgelerini genel terimlerle açıklar. Bir ölçüm, belgede kullanılan ölçü birimini kullanan ürün miktarıdır. Genişletilmiş fiyat, iskonto, iskonto yüzdesi ve satır masrafı gibi stok değerini etkileyen ölçümler de vardır.
- **Kaynak muhasebesi ölçümleri**: Bu ölçümler stok kaydı açısındandır. Belgenin stok ölçü birimindeki stok üzerindeki etkisini açıklarlar. Birden çok stok kaydı varsa, birden çok kaynak muhasebesi ölçümü satırı vardır.

Boyutlar aşağıdaki şekilde düzenlenir:

- **İkili**: İkili, ekonomik olaylara katılan unsurları tanımlar. Harici iş belgeleri için, birincil boyutlar belgenin girildiği tüzel kişiliği açıklarken, ikili boyutları satıcıyı, müşteriyi vb. açıklar. Dahili iş belgeleri (örneğin, transfer emirleri) için, ikili boyutlar karşı taraf ambarını açıklar.
- **Boyut türü**: Boyut türleri boyutları kategorilere ayırır.
- **Boyut**: Boyutun adı.
- **Boyut değeri**: Boyutun değeri.

### <a name="global-inventory-accounting-event"></a>Global Stok Muhasebesi olayı

Global Stok Muhasebesi, operasyonel olayları ve ölçümleri giriş olarak alır. Daha sonra, iliştirilmiş para birimine ve kurala göre ilgili her genel kayut defteri için uygun muhasebeyi uygular. Global Stok Muhasebesi olayını görüntülemek için **Global stok muhasebesi olayları ve ölçümleri**'ni seçebilirsiniz. Global Stok Muhasebesi olayı, operasyon olaylarıyla aynı metodolojiyi izler, ancak farklı ölçümler kullanır. Üç ana ölçüm türü vardır: ürün maliyeti miktarı, ürün maliyeti ve fark.

Yardımcı defter hesapları ölçümleri daha fazla sınıflandırmak için kullanılır. Birden fazla genel defter olabilir. Bu genel defterler, belgenin girildiği tüzel kişiliğe bağlıdır. **Genel Defter** alanının değerini değiştirerek her genel muhasebe defteri için olayları ve ölçümleri görüntüleyebilirsiniz.

### <a name="cost-element"></a>Maliyet öğesi

Genel muhasebe defterine iliştirilen maliyet öğesi ilkesini temel alan sistem, stok maliyetini etkileyen her muhasebeleştirilmiş operasyon olayı ölçümüne bir maliyet öğesi atar. Bu ölçümler arasında genişletilmiş fiyat, iskonto, iskonto yüzdesi ve satır gideri bulunur.

### <a name="measurement-line-details"></a>Ölçüm satırı ayrıntıları

**Genel Bakış** sekmesi, ekli ilkelerin ayrıntılarını gösterir. Maliyet nesnesi boyutları, maliyet nesnesi ilkesini temel alarak maliyet nesnesini gösterir. Maliyet akışı varsayımı *Belirli – Toplu İş* ise, belirli tanımlama boyutları toplu iş numarasını gösterir.

### <a name="purchase-invoice"></a>Satınalma faturası

Faturayı her zamanki gibi deftere nakledin. Ardından, Eylem Bölmesi'nde, **Fatura** sekmesinin **Günlükler** grubunda fatura günlüğünü açmak için **Fatura**'yı seçin. Her satır için bir operasyon olayı ve bir Global Stok Muhasebesi olayı oluşturulur. Bu nedenle, **Satırlar** sekmesini seçin ve ardından **Stok \> Olaylar ve ölçümler**'i seçerek **Olaylar ve ölçümler** sayfasını açın. **Olaylar ve ölçümler** sayfası aynı ölçüm türünü gösterir. Ancak, sayfa farklı bir ölçü rolü ve ölçü değiştirici gösterdiğinden, aracı (tüzel kişilik) üzerindeki etkisi farklıdır.

Global Stok Muhasebesi olayını görüntülemek için **Global stok muhasebesi olayları ve ölçümleri**'ni seçin. Stok miktarı ve maliyeti artık *Alınan ve faturalanmayan mallar stoğu* yardımcı defteri hesabından *Satın alınan malların maliyeti* yardımcı defter hesabına akar.
