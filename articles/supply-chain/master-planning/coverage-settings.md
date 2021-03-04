---
title: Kapsam ayarları
description: Bu konu, Master planlamanın madde gereksinimlerini hesaplamak için kullandığı kapsam ayarlarıyla ilgili bilgi sağlar.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1134f734f1025151a56b2a72266a6baa5763ba4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439544"
---
# <a name="coverage-settings"></a>Kapsam ayarları

[!include [banner](../includes/banner.md)]

Master planlama, madde gereksinimlerini hesaplamak için karşılama ayarlarını kullanır.

Karşılama ayarlarını birkaç şekilde belirtebilirsiniz:

- Bir kapsam grubuna yönelik kapsam ayarlarını belirtin.

    Kapsam grubuyla bağlantılı tüm ürünlere yönelik ayarları içeren bir kapsam grubu oluşturabilirsiniz. Bir kapsam grubu oluşturmak için **Master planlama &gt; Kurulum &gt; Kapsam &gt; Kapsam grupları**'na gidin. Ürüne bir kapsam grubu bağlayabilirsiniz. Bağlantı belirli bir siteye, ambara veya ürün boyutuna ise, **Madde kapsamı** sayfasındaki **Kapsam grubu** alanını kullanın. Bağlantı genel ise, ürün boyutlarından bağımsız olarak **Ürün ayrıntıları** sayfasındaki **Plan** hızlı sekmesinde yer alan **Kapsam grubu** alanını kullanın. Varsayılan olarak, bir kapsam grubunu bir ürüne bağlamazsanız, master planlama **Master planlama parametreleri** sayfasında belirtilen genel kapsam grubunu kullanır.

- Bir ürün için kapsam ayarları belirtin.

    Özel bir ürün için kapsam ayarları oluşturabilirsiniz. **Ürün bilgi yönetimi &gt; Ürünler &gt; Serbest bırakılmış ürünler**'e gidin. Ürünü seçin ardından Eylem Bölmesi'nde, **Plan** sekmesinde, **Kapsam** grubunda **Madde kapsamı**'nı seçerek **Madde kapsamı** sayfasını açın. Ürün bir kapsam grubuna zaten bağlanmışsa, **Üstüne yazdır** alanını kullanarak kapsam grubu ayarlarının üstüne yazdırabilirsiniz. **Madde kapsamı** sayfasındaki kapsam ayarları, **Kapsam grubu** sayfasındaki ayarlardan önceliklidir.

- Sihirbaz kullanarak bir ürüne yönelik kapsam ayarlarını belirleyin.

    Sihirbaz, birincil madde kapsamı parametrelerini ayarlama sürecinde size adım adım yol gösterir. **Madde kapsamı** sayfasında, Eylem Bölmesinde **Sihirbaz**'ı seçerek **Madde Kapsamı Sihirbazı**'nı açın.

- Boyut grubu için kapsam ayarları belirtin.

    **Ürün bilgi yönetimi &gt; Ürünler &gt; Serbest bırakılmış ürünler**'e gidin. **Serbest bırakılan ürün ayrıntıları** sayfasında, **Genel** hızlı sekmesinde, **Yönetim** bölümünde, **Depolama boyut grubu** alanındaki bağlantıya tıklayın. **Depolama boyut grupları** sayfasında **Boyuta göre kapsam planı** onay kutusunu seçerek depolama boyut grubundaki bir boyut için kapsam ayarları oluşturabilirsiniz. Yapılandırma, renk, boyut, stil gibi tüm ürün boyutları için **Boyuta göre kapsam planı** alanı seçilmiş olmalıdır.


## <a name="coverage-codes"></a>Karşılama kodları

Master planlama farklı stok yenileme yöntemleri kullanacak şekilde yapılandırılabilir. Stok yenileme yöntemleri veya lot boyutlandırma yöntemleri, sistem tarafından satın alınan veya üretilen maddelerin toplu iş boyutunu belirlemek için kullanılan tekniklerdir. 

Her stok yenileme yöntemine aşağıdaki karşılama kodlarından biri atanır:

- **El ile** : Sistemin madde için satın alınan, transfer veya üretim emirlerini önermediği lot boyutlandırma yöntemi. Maddenin planlayıcısı, maddenin stok yenileme işlemi için gerekli siparişlerin oluşturulmasından sorumlu olacaktır.
- **Gereksinim başına**: Sistemin madde için her gereksinim başına bir planlı satınalma, transfer veya üretim emri oluşturduğu lot boyutlandırma yöntemidir. Bu genellikle, aralıklı talep bulunan pahalı maddeler için kullanılır.  
- **Dönem başına**: Madde için bir döneme ait tüm talepleri tek bir siparişte olacak şekilde birleştiren lot boyutlandırma yöntemi. Sipariş dönemin ilk günü için planlanacaktır ve miktarı ayarlanan dönem içindeki net gereksinimleri karşılayacaktır. Dönem, maddeye yapılan ilk taleple başlar ve tanımlanan süreyi olduğu gibi kapsar. Sonraki dönem, maddenin sonraki gereksinimleri itibarıyla başlar.
- **Minimum/Maksimum**: Tahmini eldeki değeri bir eşiğin altında olduğunda, belirli bir düzeye kadar stok stok yenilemesini içeren lot boyutlandırma yöntemi. Stok yenileme miktarı maksimum düzey ve eldeki tahmini düzey arasındaki fark olur.


## <a name="additional-resources"></a>Ek kaynaklar

[Master planlara genel bakış](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]