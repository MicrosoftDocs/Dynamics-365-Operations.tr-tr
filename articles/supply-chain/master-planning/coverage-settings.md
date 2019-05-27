---
title: Kapsam ayarları
description: Bu konu, Master planlamanın madde gereksinimlerini hesaplamak için kullandığı kapsam ayarlarıyla ilgili bilgi sağlar.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538906"
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

## <a name="additional-resources"></a>Ek kaynaklar

[Master planlar](master-plans.md)
