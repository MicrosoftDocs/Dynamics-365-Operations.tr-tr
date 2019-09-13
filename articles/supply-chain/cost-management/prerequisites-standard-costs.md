---
title: Standart maliyetler için ön koşullara genel bakış
description: Bu konu, standart maliyetleri kullanmak için temel adımları açıklar.
author: AndersGirke
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d5fd28f2605c6382a5901b7d52389b07c54d037
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865508"
---
# <a name="prerequisites-for-standard-costs-overview"></a>Standart maliyetler için ön koşullara genel bakış

[!include [banner](../includes/banner.md)]

Bu konu, standart maliyetleri kullanmak için temel adımları açıklar. Sonraki adımlar şirketin işlemlerine bağlıdır. Örneğin, adımlar üretim yapılmayan bir ortam, rotaları kullanmayan bir üretim ortamı ve rotaları kullanan üretim ortamı için farklıdır. 

Standart maliyetleri ayarlamak için aşağıdaki adımları takip edin.

**1. Standart maliyetler için bir madde modeli grubu oluşturun.**

Standart maliyetler için yeni bir grup oluşturmak ve **Standart maliyet** stok modeli atamak için **Madde modeli grupları** sayfasını kullanın. Madde modeli grubu tanımlayıcısının **Std Cost** gibi anlamlı olması gerekir. Grubun mali negatif stoka izin vermesi ve fiziksel stok ile mali stoğu nakletmesi gerektiğini belirtmek için onay kutularını işaretleyin. Bu standart maliyet grubu maddelere atanır.

**2. Standart maliyet farklarıyla ilişkili genel muhasebe hesapları tanımlayın.** 

Standart maliyet farklarıyla ilişkili genel muhasebe hesapları tanımlamak için **Hesap planı** formunu kullanın. Bu genel muhasebe hesaplarının **Deftere nakil** sayfasında atanabilmeleri için önce tanımlanmaları gerekir. Genel muhasebe hesapları madde gruplarını ve maliyet gruplarını yansıtabilir.

**3. Madde nakillerine, standart maliyet farklarıyla ilişkili genel muhasebe hesapları atayın.** 

Standart maliyet farklarıyla ilişkili genel muhasebe hesapları atamak için **Deftere nakil** sayfasını kullanın. Bir farklılığın genel muhasebe hesabını maddeye (veya madde grubuna) göre belirtme veya genel muhasebe hesabının tüm madde ve maliyet gruplarına uygulanacağını belirtme seçeneklerinden birini tercih edebilirsiniz. Bu seçenekler tablolar, gruplar ve tümü için maliyet ilişkilerine karşılık gelir. 

Madde deftere nakil kuralları tanımlamadan önce maliyet ilişkilerini (tablolar, gruplar ve tümü için) etkinleştirmek için **Hareket birleşimleri** sayfasını kullanın.

**4. Standart maliyetlerle ilişkili stok parametreleri tanımlayın.** 

-  Standart maliyetlerle ilişkili iki maliyet denetimi parametresi tanımlamak için **Stok muhasebesi politikaları kurulumu > Parametreler** sayfasındaki **Stok muhasebesi** sekmesini kullanın.

    -  **Maliyet dökümü** alanında **Hiçbiri** veya **Yardımcı muhasebe**'yi seçin. **Yardımcı defter**'i seçmeniz durumunda, maliyet dökümü *etkin* bir maliyet dökümü olur. Etkin maliyet dökümü, standart maliyet maddeleri için çok düzeyli bir ürün yapısı üzerinde maliyet grubu segmentasyonunun hesaplanması, sürdürülmesi ve görüntülenmesi için önemlidir. Maliyet dökümü etkin olduğunda, tek düzeyli, çok düzeyli veya toplam biçiminde her maliyet grubu için stok, süren iş ve satılan malların maliyet tutarını rapor edebilir ve analiz edebilirsiniz. Maliyet dökümü etkin olduğunda, üretilen bir öğenin maliyetini etkinleştirmeniz halinde, maliyet grubu segmentleri maddenin maliyet kaydında saklanır. 

    -  **Hiçbiri** öğesini seçerseniz, maliyet grubu segmentleri standart maliyet maddeleri için tutulmaz. Başka bir deyişle, üretilmiş bir maddenin standart maliyeti hesaplanır ve maliyet grubu segmentleri olmadan tek bir tutar olarak tutulur. Üretilmiş bileşenlerin maliyet katkıları tek bir tutarda toplanır.

-  **Standarttan farkılıklar** alanında **Özetlenmiş** veya **Maliyet grubu başına** seçeneğini seçin. **Maliyet grubu başına** seçeneğini belirlerseniz, satınalma fiyatı farklarını ve üretim farklarını maliyet grubuna göre tanımlayabilirsiniz. Ayrıca dört tip üretim farkı tanımlayabilirsiniz: lot boyutu, miktar, fiyat ve değer değiştirme farkları. **Özetlenmiş** öğesini seçerseniz, farkları maliyet grubuna göre belirleyemez ve dört üretim farkı tipini belirleyemezsiniz. Yalnızca özetlenmiş bir üretim farkı görüntüleyebilirsiniz.

-  Standarttan fark ilkesi, maliyet dökümü ilkesinden bağımsız çalışır. Başka bir deyişle, maliyet grubuna göre üretim farklarının yakalanmaya devam edilebilmesi için maliyet dökümü ilkesi olarak **Hiçbiri** seçeneğini seçebilir ve maliyet grubu başına farkları belirleyebilirsiniz.

**5. Standart maliyetler için maliyetlendirme sürümleri oluşturun.** 

Standart maliyetler için bir veya daha fazla maliyetlendirme sürümü oluşturmak için **Maliyet sürümü kurulumu** sayfasını kullanın. Her maliyetlendirme sürümünün **Standart maliyetler** maliyetlendirme türü ile atanması ve içeriğin maliyet verilerini dahil etmesine izin vermesi gerekir.

**6. Standart maliyetleri kullanmak için varolan bir müşteri hazırlayın.** 

Varolan maddelerini standart bir maliyet stok modeline değiştirmek isteyen müşterilerin **Standart maliyet dönüştürmeleri** sayfasını kullanması gerekir.


<a name="related-topics"></a>İlgili konular
--------

[Standart maliyet dönüştürmeye genel bakış](standard-cost-conversion-overview.md)

### <a name="blogs"></a>Bloglar

#### <a name="community-blogs"></a>Topluluk blogları

- [Dynamics 365 for Finance and Operations içindeki doğrudan malzemeler için standart maliyetleri ayarlamak](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [Dynamics 365 for Finance and Operations içinde standart işgücü maliyetleri](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)
