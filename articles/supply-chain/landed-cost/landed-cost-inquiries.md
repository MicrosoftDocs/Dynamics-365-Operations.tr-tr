---
title: Varış yeri maliyeti sorguları
description: Bu konuda, varış yeri maliyeti modülü için kullanılabilen çeşitli sorgu türlerinin nasıl bulunacağı ve kullanılacağı açıklanmaktadır.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 22a2e76780adb43b053b6cf7fd08411a4a60aeac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823373"
---
# <a name="landed-cost-inquiries"></a>Varış yeri maliyeti sorguları

[!include [banner](../../includes/banner.md)]

## <a name="voyage-line-inquiries"></a>Seyahat satırı sorguları

**Seyahat satırları** sorgusu, stokla ilgili tüm seyahat satırlarını gösterir. Bu sorgu, bir maddeyi, satın alma siparişini veya diğer yararlı bilgi parçasını bulmanıza yardımcı olmak için filtre olarak kullanılabilir. Ayrıca, bir veya daha fazla seyahatte olabilecek bir maddenin beklenen teslimat tarihini tanımlamak için de kullanılabilir. Bu şekilde, beklenen stok teslim almayı yönetmenize yardımcı olabilir.

Bu sorguyu açmak için **Varış yeri maliyeti \> Sorgular \> Seyahat satırları**'na gidin.

### <a name="overview-tab"></a>Genel bakış sekmesi

**Seyahat satırları** sorgu sayfasının **Genel bakış** sekmesi, ilgili her seyahat satırına dair temel bilgileri gösteren bir kılavuz içerir. Aşağıdaki tabloda kılavuzdaki sütunlar açıklanmıştır.

| Sütun | Tanım |
|---|---|
| **Madde numarası** | Seyahat satırının maddesi. |
| **Referans** | Sipariş türü (satın alma siparişi veya transfer emri). |
| **Sayı** | Satın alma siparişi numarası veya transfer emri numarası. |
| **Folyo** | Seyahat satırı ile ilişkilendirilen folyo. |
| **Sevkiyat konteyneri** | Seyahat satırıyla ilişkilendirilen sevkiyat konteyneri. |
| **Seyahat** | Seyahat satırıyla ilişkilendirilen seyahat. |
| **Miktar** | Seyahat satırının madde miktarı. |
| (Diğer boyutlar) | Ek boyutlar için sütunları istediğiniz gibi gösterebilirsiniz. Bu boyutlar arasında toplu iş numarası, stok durumu ve ambar bulunur. Eylem bölmesinde, dahil edilecek boyutları seçebileceğiniz bir iletişim kutusu açmak için **Stok \> Boyutları görüntüle**'yi seçin. |

### <a name="general-tab"></a>Genel sekmesi

**Genel bakış** sekmesinde seçili olan satır hakkında daha fazla bilgi görüntülemek için **Genel** sekmesini seçin.

### <a name="dimensions-tab"></a>Boyutlar sekmesi

Bu sekmede göstermek üzere seçtiğiniz boyutlara bakılmaksızın, **Genel bakış** sekmesinde seçili olan satırın kullanılabilir tüm boyutlarının değerlerini görüntülemek için **Boyutlar** sekmesini seçin.

## <a name="cost-estimate-inquiries"></a>Maliyet tahmin sorguları

Her maliyet tahmini oluşturduğunuzda, tahmin **Maliyet tahminleri** sorgu sayfasına eklenir. Maliyet tahminlerini oluşturma, görüntüleme ve onlarla çalışma hakkında tam ayrıntılar için (sorgulama sayfasındaki tahminler dahil) bkz. [Varış yeri maliyetlerini tahmin etme ve yönetme](estimate-manage-landed-costs.md).

## <a name="item-tracking"></a>Madde izleme

Açık satın alma siparişi satırlarını ve geçerli durumlarını görüntülemek için **Madde izleme** sayfasını kullanın. Çizgilerin burada görünmesi için bir seyahatle ilişkilendirilmesine gerek yok. Ancak bir madde bir seyahatle ilişkiliyse madde izleme kayıt satırı, seyahat kimliğini gösterir.

Bu sayfayı açmak için **Varış yeri maliyeti \> Sorgular \> İzleme \> Madde izleme**'ye gidin.

Sisteminiz büyük olasılıkla çok sayıda satın alma siparişi satırı içerdiğinden **Madde izleme** sayfasında başlangıçta kayıt olmaz. Aradığınız satın alma siparişi satırları kümesini tanımlamak için sayfanın üst kısmındaki filtre alanlarını kullanarak başlayın. Ardından, listeyi oluşturmak için eylem bölmesinden **Güncelleştir**'i seçin. Filtre alanlarının tümünde joker karakter olarak yıldız (\*) kullanabilirsiniz. Örneğin, adlarında "DVD" sözcüğünü içeren maddelerin tüm satın alma siparişi satırlarını bulmak için **Tür** alanını **Ürün adı** olarak ayarlayın ve **Alan değeri** alanına *\*DVD\** girin.

> [!NOTE]
> Şu anda, karşılanmayan siparişler yalnızca satış siparişlerini içerir. Satış teklifleri gösterilmez veya karşılanmayan sipariş olarak kabul edilmez.

Aşağıdaki tabloda **Madde izleme** sayfasındaki kılavuzdaki sütunlar açıklanmıştır.

| Sütun | Tanım |
|---|---|
| **Varış limanı** | Son varış noktası. |
| **Onaylı** | Satın alma siparişi satırının onaylanma tarihi. |
| **Teslimat Tarihi** | Satın alma siparişi satırının teslimat tarihi. |
| **Seyahat** | Satır bir seyahatle ilişkiliyse seyahat kimliği. |
| **Sevkiyat Konteyneri** | Satır bir sevkiyat konteynerine bağlıysa konteyner kimliği. |
| **Sevkiyat limanı** | Satın alma siparişi satırıyla ilişkili sevkiyat konteyneri için gerçek bir tarih ayarlanmamışsa izleme formundaki ilk durağı temel alan geçerli liman. |
| **Faaliyet** | Satın alma siparişi satırıyla ilişkili sevkiyat konteyneri için gerçek bir tarih ayarlanmamışsa izleme formundaki ilk durağı temel alan geçerli faaliyet. |
| **Tahmini bitiş tarihi** | Seyahatin varış ambarı tarafından teslim alınmasının beklendiği tarih. |
| **Kuruluş adı** | Satıcının adı. |
| **Seyahat Durumu** | Satın alma siparişi satırına eklenen sevkiyatın durumu. |
| **Madde numarası** | Satın alma siparişi satırının madde numarası. |
| **Harici** | Satıcının madde adı. |
| **Ürün Adı** | Satın alma siparişi satırı için madde adı. |
| **Miktar** | Satın alma siparişi satırı için satın alma siparişi satırı miktarı. |
| **Birim** | Satın alma siparişi satırının ölçü birimi. |
| **Referans** | Sipariş türü (satın alma siparişi veya transfer emri) |
| **Referans numarası** | Satın alma siparişi numarası veya transfer emri numarası. |
| **Karşılanamayan sipariş** | Bir sembol, madde için karşılanmayan satış siparişi olduğunu gösterir. |
| (Diğer boyutlar) | Ek boyutlar için sütunları istediğiniz gibi gösterebilirsiniz. Bu boyutlar arasında toplu iş numarası, stok durumu ve ambar bulunur. Eylem bölmesinde, dahil edilecek boyutları seçebileceğiniz bir iletişim kutusu açmak için **Boyutları görüntüle**'yi seçin. |

### <a name="related-information-about-backorders"></a>Karşılanmayan siparişlerle ilgili bilgiler

Karşılanmayan siparişlerle ilgili daha fazla bilgi görüntülemek için sayfanın sağ tarafındaki **İlgili bilgiler** sekmesini ve ardından **Karşılanmayan Siparişler**'i seçin. Belirli bir karşılanmayan sipariş hakkında daha fazla bilgi görüntülemek için bunun satırını seçin ve ardından **Diğer** bağlantısını seçin.

## <a name="individual-shipping-container-tracking"></a>Ayrı sevkiyat konteyneri izleme

**Ayrı sevkiyat konteyneri izleme** sorgusu, bir sevkiyat konteynerini bulmanıza ve ardından bu konteynerdeki tüm seyahat satırlarını tanımlamanıza olanak sağlayan bir filtre sağlar.

Bu sorguyu açmak için **Varış yeri maliyeti \> Sorgular \> İzleme \> Ayrı sevkiyat konteyneri izleme**'ye gidin.

## <a name="multiple-shipping-container-tracking"></a>Çoklu sevkiyat konteyneri izleme

**Çoklu sevkiyat konteyneri izleme** sorgusu, bir sevkiyat konteyneri koleksiyonunu bulmanıza ve ardından bu konteynerlerdeki tüm seyahat satırlarını tanımlamanıza olanak tanıyan bir filtre sağlar.

Bu sorguyu açmak için **Varış yeri maliyeti \> Sorgular \> İzleme \> Çoklu sevkiyat konteyneri izleme**'ye gidin.
