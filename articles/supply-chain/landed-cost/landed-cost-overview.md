---
title: Varış yeri maliyeti modülü
description: Varış yeri maliyeti modülü, kullanıcılara üreticiden ambara kadar ithal navlun üzerinde tam finansal ve lojistik kontrol sunarak işletmelerin gelen sevkiyat operasyonlarını kolaylaştırmasına yardımcı olur.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 524fcdbcf9ba607fe9bcec1f1e894beb45f265e6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823349"
---
# <a name="landed-cost-module"></a>Varış yeri maliyeti modülü

[!include [banner](../../includes/banner.md)]

**Varış yeri maliyeti** modülü, kullanıcılara üreticiden ambara kadar ithal navlun üzerinde tam finansal ve lojistik kontrol sunarak işletmelerin gelen sevkiyat operasyonlarını kolaylaştırmasına yardımcı olur. İthal mallar için ithalat maliyetleri, ithal edilen her maddenin toplam maliyetinin yüzde 40'ını veya daha fazlasını oluşturabilir. Bu nedenle, zorluk, varış yeri maliyetleri için doğru tahminler sağlamaktır.

İşletmeler, şu görevleri gerçekleştirmek için Varış yeri maliyetini kullanabilir:

- Yolculuk oluşturma anında varış yeri maliyetlerini tahmin etme.
- Varış yeri maliyetlerini tek bir yolculuktaki birden fazla maddeye veya transfer emrine paylaştırma.
- Varış yeri maliyetlerini tanıyarak malların fiziksel konumlar arasında transferini destekleyin.
- Transitteki mallar için tahakkuku onaylayın.

Varış yeri maliyeti, ek yüklü varış yeri maliyetleri için doğru ve zamanında maliyet tahminleri sağlar. Aynı zamanda, genişletilmiş tedarik zincirine yönelik daha fazla finansal ve lojistik görünürlük sunar. Maliyetlendirme ve maliyetlendirme hatalarının yönetimini azaltmaya yardımcı olur.

## <a name="highlights"></a>Öne çıkanlar

### <a name="voyages"></a>Seyahatler

Varış yeri maliyetinde, bir yolculuk, giden bir konumdan, belirli bir dönem boyunca belirli bir hedef kümesinden belirli bir gelen mal ambarı konumuna giden ayrı bir harekettir. Satın alma siparişleri ve sipariş satırları bir yolculuk için tek bir konteynere veya birden çok konteynere eklenebilir ve maliyetler madde satırına doğru şekilde geri tahsis edilir. Siparişler ve sipariş satırları, tek bir yolculuk için tüzel kişiliklere de eklenebilir.

### <a name="item-ownership"></a>Madde sahipliği

Microsoft Dynamics 365 Supply Chain Management'ta, mallar genellikle ambar hedefinde teslim alınır ve faturalanır. Bununla birlikte, çoğu uluslararası ticaret anlaşmasına göre, bir işletme malların mülkiyetini, mallar orijinal limandan ayrıldıkları anda, fiziksel olarak teslim edilmeden önce alır. Varış yeri maliyeti, işletmelerin malları fiziksel olarak teslim almadan önce faturalamasını sağlar. Bu kavram transitteki siparişteki mal olarak bilinir. Orijinal satın alma siparişi faturalandıktan sonra malların alımını yönetmek için yeni bir sipariş türü oluşturur.

### <a name="costs"></a>Maliyetler

Varış yeri maliyetinde bir yolculuk oluşturduğunuzda, maliyetler otomatik olarak eklenebilir. Bu maliyetler Varış yeri maliyeti olarak ayarlanır ve bunlar için çeşitli maliyet seçenekleri ve maliyet tabanları kullanılabilir. Her maliyet, bir yolculuğun farklı düzeyleri için ayarlanabilir ve miktar, hacim, ağırlık, tutar ve tanımlanmış hacimsel bölenleri destekleyen onay kuralları aracılığıyla madde düzeyine eklenebilir. Bu tahmini maliyetler, bir yolculuk için tüm maliyetlerin doğru bir tahminini sağlar.

Varış yeri maliyeti daha sonra, yolculuk oluşturma sırasında tahmini maliyetlerin doğru bir şekilde hesaplanmasını sağlamak için tahmini iniş maliyetlerinin bir ön deftere naklini/tahakkuk etmesini sağlar. Bu otomatik maliyetler faturalandıkça, tahmini maliyetler tersine çevrilir ve maliyet faturalarına göre gerçek maliyetlerle değiştirilir.

Gerçek maliyetler, her maliyet türü (örneğin, vergi, navlun ve sigorta) için ayarlanan kliring hesapları kullanılarak maliyet faturalama anında deftere nakledilen tahmini maliyetleri tersine çevirir. Bu deftere nakiller, belirli maddeyle ilişkili deftere nakil davranışını izler. Deftere nakil türünün ilk giren ilk çıkar (FIFO), son giren ilk çıkar (LIFO), hareketli ağırlıklı ortalama veya hareketli ortalama olmasına bakılmaksızın stok deftere naklini otomatik olarak güncelleştirirler. Tüm stok modeli grubu deftere nakil türleri desteklenir. Hareketli ortalama ve standart maliyet deftere nakli için tahmini maliyetler ile fiili maliyetler arasındaki farkları deftere nakletmek üzere satın alma fiyatı farkı hesapları kullanılabilir.

### <a name="item-and-order-tracking"></a>Madde ve sipariş izleme

Bir yolculuk, kaynak giden konumdan son hedef ambara geçerken, kullanıcılar yolculuğunun her adımını veya *durağını* gerektiği gibi güncelleştirebilir. Her durak için bir sağlama süresi ve bir sevkiyat durumu tanımlanır. Yolculuğun bir sonraki durağına hareket için onaylanmış teslimat tarihleri de tanımlanır. Bu teslimat tarihleri birlikte, malların gelen mal ambarına tahmini teslimat tarihini sağlar. Kullanıcılar bu teslim tarihlerini değiştirebilir. Bu durumda, malların tahmini teslimat tarihi, yolculuğun sağlama süreleri ve duraklarına göre otomatik olarak güncelleştirilir. Yolculuk ve gemi ile transit olarak taşınan mallara dair malların alınmasından önce konteyner başına görünürlük sunulur. Tarihler her satın alma siparişi satırında güncelleştirildiğından, işletmeler lojistik ve ambar planlaması üzerinde daha fazla denetime sahiptir.

## <a name="landed-cost-concepts"></a>Varış yeri maliyeti kavramları

Aşağıdaki tabloda, varış yeri maliyetinin bazı temel kavramları özetlenmiştir.

| Kavram | Tanım |
|---|---|
| Seyahat | Tipik olarak, bir yolculuk tek bir gemidir. Ancak uygulamalarınıza ve prosedürlerinize bağlı olarak bir satıcı veya bir satın alma siparişi olabilir. Bu kavramın kullanımında herhangi bir sınırlama yoktur. |
| Folyo | Folyo genellikle gümrük yönetmelikleri tarafından belirlenir. Sevkiyat başına bir tüzel kişilik/şirket için bir satıcının mallarından oluşabilir. Bir folyodaki mallar bir konteynerde olabilir veya birden fazla konteynere yayılabilir. |
| Sevkiyat konteyneri | Sevkiyat konteynerleri satın alma siparişi satırlarını depolar. Sevkiyat seviyesinin altındadırlar. Bunlar genellikle mallar için maliyetler konteynere göre paylaştırılırsa veya konteyner başına alım yapılırsa kullanılır. |
| Sevkiyat konteyneri türü | Sevkiyat konteyneri türleri, bir maliyet tipinin (örneğin, navlun) fiyatını belirleyebilir. Ayrıca yararlı nakliye bilgileri de sağlarlar. |
| Maliyet türü | Maliyet türleri; görev, navlun ve sigorta gibi ithalatla ilişkili maliyetleri tanımlar. |
| Otomatik maliyet | Otomatik maliyetler ticaret anlaşmaları gibi çalışır. Otomatik maliyet, yolculuk seviyesine bağlıdır. |
| Liman | Limanlar malların teslim alındığı ve transfer edildiği alanlardır. |
| Tekne | Araç, gemi veya uçak gibi malları taşımak için kullanılan ortamdır. |
| Transitteki mallar | Ayarlara bağlı olarak bir fatura güncelleştirildikten sonra mallar transit ambarına konur. |
| Faaliyet | Etkinlikler, yolculuğun iki liman arasındaki her önemli adımını saklamak için kullanılabilir. Tarihleri güncelleştirmek için kullanılabilirler. |
| Yolculuk şablonu | Yolculuk şablonları, malların iki liman arasında gittiği rotalardır. |

**Varış yeri maliyeti** ve **Taşıma yönetimi** (TMS) modüllerinin terminolojisinin ve özelliklerinin karşılaştırılması için bkz. [Varış yeri maliyeti ve Taşıma yönetimi](landed-cost-vs-tms.md).
