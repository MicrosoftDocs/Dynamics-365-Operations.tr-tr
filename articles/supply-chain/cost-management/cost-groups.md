---
title: Maliyet grupları
description: Maliyet grupları, üretilen bir maddenin malzeme, işçilik ve genel giderler için maliyet katkıları gibi hesaplanan maliyetindeki maliyet katkılarını segmentlere ayırmak ve analiz etmek için temel sağlar. Maliyet grubu segmentasyonu üretim ortamlarında maliyet dökümü, maliyet dağılımı veya maliyet sınıflandırması gibi birçok eşanlamlı ifadeye sahiptir.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCostGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dee8e40de43480cd010b5acc41a3d87611c2ab6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439441"
---
# <a name="cost-groups"></a>Maliyet grupları

[!include [banner](../includes/banner.md)]

Maliyet grupları, üretilen bir maddenin malzeme, işçilik ve genel giderler için maliyet katkıları gibi hesaplanan maliyetindeki maliyet katkılarını segmentlere ayırmak ve analiz etmek için temel sağlar. Maliyet grubu segmentasyonu üretim ortamlarında maliyet dökümü, maliyet dağılımı veya maliyet sınıflandırması gibi birçok eşanlamlı ifadeye sahiptir. 

Maliyet grubu segmentasyonu üretim ortamlarında maliyet dökümü, maliyet dağılımı veya maliyet sınıflandırması gibi birçok eşanlamlı ifadeye sahiptir. Maliyet grubu segmentasyonu birçok amaca hizmet edebilir. Burada bazı örnekler verilmiştir:

-   Maliyetleri, bir konserve ürünü için içindekiler ve ambalaj malzemesi gibi değişik malzeme tipleri için, maddelere atanan maliyet gruplarına dayanarak segmentlerine ayırabilir.
-   Maliyetleri, farklı işçilik veya makineler gibi değişik operasyon kaynağı türleri için, operasyon kaynakları ve rota operasyonlarına ilişkili maliyet kategorilerine atanan maliyet gruplarına dayanarak segmentlerine ayırabilir.
-   Maliyetleri rota operasyonlarındaki kurulum süresi ve çalışma süresi için, rota operasyonlarıyla ilgili maliyet kategorilerine atanan maliyet gruplarına dayanarak segmentlerine ayırabilir.
-   Maliyetleri, işçilikle ve makineyle ilişkili genel giderler gibi değişik genel gider tipleri için, maliyetlendirme tablosu kurulumunda dolaylı maliyetlere atanan maliyet gruplarına dayanarak segmentlerine ayırabilir.
-   Maliyetlendirme tablosu kurulumundaki çeşitli türde imalat genel giderlerini hesaplamak için temeli alınabilir. Bu genel giderler, operasyon kaynakları hakkındaki rota bilgileri ile ilişkili farklı türde genel giderleri veya kurulum süresi ve çalışma süresi hakkındaki bilgileri içerebilir. İmalat genel giderleri de bileşen malzemesinin maliyet katkılarıyla ilgili olabilir; bu, rota bilgileri gereksinimini ortadan kaldıran yalın bir imalat felsefesini yansıtır.

Maliyet grubu segmentasyonu, standart maliyetlere mi yoksa planlanan maliyetlere mi dayandığından bağımsız olarak, mamul maddenin hesaplanan maliyeti için geçerlidir. **Özet** sayfası, bu segmentasyonu maliyet grubuna, düzeye veya hem maliyet grubu hem de düzeye göre görüntüler. 

Maliyet grubu segmentasyonunu bir ürün yapısındaki birden fazla düzey boyunca koruma özelliği *bölme* olarak bilir. Bölme, yalnızca standart maliyet stok modeli kullanan mamul maddeler için geçerlidir. Bölme kullanılmıyorsa, mamul bir bileşene ait maliyet bir malzeme maliyeti katkısı olarak ele alınır. Yardımcı defter tarafından maliyet dökümüne yönelik stok parametresi, maliyet grubu segmentasyonunun standart maliyet hesaplamalarında birden çok düzey boyunca korunacağını gösterir. Bunun aksine, bir politika düzey içermiyorsa, maliyet grubu segmentasyonu yalnızca tek düzey hesaplama için geçerlidir. Örneğin, **Maliyet grubuna göre maliyet yukarı yuvarlaması** sayfası, standart maliyet maddeleri için birden fazla düzey boyunca maliyet grubu segmentasyonunu görüntüler. 

Maliyet grubu segmentasyonu aynı zamanda bir standart maliyet maddesine ait farklılıklar için de geçerlidir. İkinci bir stok parametresi, farklılıklar maliyet grubuna göre mi tanımlanacak yoksa sadece özetlenecek mi, belirler. 

Bir maliyet grubuna, bir maliyet grubu tipi ve tamamlayıcı segmentasyon amaçlı olarak bir davranış atanabilir.

-   **Maliyet grubu türü** − Maliyet grubunun doğrudan malzeme, doğrudan imalat veya doğrudan dış kaynak kullanımı için geçerli olduğunu göstermek veya onu dolaylı ya da tanımsız olarak atamak için her maliyet grubuna bir maliyet grubu türü atanmalıdır. Maddelere doğrudan malzeme olarak atanmış bir maliyet grubu atanabilir. Doğrudan üretim maliyet grubu maliyet kategorilerine atanabilir. Bir servis ürün türüne doğrudan bir dış kaynak maliyet grubu atanabilir, böylece servis satın alma ile ilişkili maliyetleri alt sözleşme etkinliklerine sınıflandırabilirsiniz. Dolaylı bir maliyet grubu ek talepler veya oranların dolaylı maliyetlerine atanabilir. Tanımsız olarak atanan bir maliyet grubu maddelere, maliyet kategorilerine veya dolaylı maliyetlere atanabilir. Bir maliyet grubu türünün ataması, sayısız amaca hizmet eder. İlk olarak, bir maliyet grubu atama ve geçerli maliyet gruplarının listesini görüntüleme özelliğini sınırlandırır. İkinci olarak, raporlama amaçlı olarak tamamlayıcı segmentasyon sağlar. Üçüncü olarak, farklılıklar için genel muhasebe hesapları atamakta kullanılabilir.
-   **Davranış** − Her bir maliyet grubuna, maliyet grubunun sabit maliyetler veya değişken maliyetler için geçerli olduğunu gösterecek şekilde isteğe bağlı olarak bir davranış atanabilir. Davranış için boş değere sahip bir maliyet grubu değişken bir maliyet olarak ele alınır. Bir davranış ataması yalnızca raporlama amaçlarına hizmet eder. Örneğin maliyetler, maliyetlendirme tablosundaki ve **Maliyet grubuna göre maliyet yukarı yuvarlaması** sayfasındaki sabit ve değişken maliyetlerin segmentasyonu ile birlikte görüntülenebilir. Her bir maliyet grubuna bir kar ayar yüzdesi atamanız halinde, ürün reçetesi hesaplaması, maliyet artı kar marjı yaklaşımına dayalı olarak önerilen bir satış fiyatı sağlar.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]