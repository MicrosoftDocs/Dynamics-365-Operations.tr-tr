---
title: "Gezinti araması"
description: "Bu konuda, Microsoft Dynamics 365 for Operations sayfalarında gezinmek için arama işlevinin nasıl kullanılacağı açıklanmaktadır."
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 650c8b60ba8204e8990cf607c1c9901b8f0bb762
ms.openlocfilehash: 9f2cbafa3e21006f458067baf99ea5abaef8bb86
ms.contentlocale: tr-tr
ms.lasthandoff: 04/28/2017


---

# <a name="navigation-search"></a>Gezinti araması

[!include[banner](../includes/banner.md)]


Bu konuda, Microsoft Dynamics 365 for Operations sayfalarında gezinmek için arama işlevinin nasıl kullanılacağı açıklanmaktadır.

Dynamics 365 for Operations geniş bir sektör ve faaliyet alanı yelpazesi için işlevler sağlar. Uygulama, çeşitli görevleri gerçekleştirmenize yardımcı olmak için çok sayıda alan ve sayfa içerir. Görevlerinizi tamamlamak için ihtiyaç duyduğunuz sayfaları hızlı bir şekilde bulmak için gezinti araması özelliğini kullanın. 

Bu özelliği kullanmak için **Arama** simgesine tıklayarak **Arama** kutusunu görüntüleyin. Kutuya bir veya birden fazla sözcük yazabilirsiniz. Sistem, uygulamadaki ilgili sayfalarda, girmiş olduğunuz sözcüklerle eşleşmeler arar. Örneğin, giriş olarak "satıcı faturası" yazdığınızda o girişle eşleşen sonuçları görüntüler. 

**Not:** **Arama** kutusu, sayfaları bulmanıza ve sayfalarda gezinmenize yardımcı olur. Belirli verileri veya eylemleri bulmanıza yardımcı olmaz. 

[![arama-kutusu](media/navigation-search.png "Arama kutusu") 

## <a name="quickly-navigate-to-a-particular-page"></a>Belirli bir sayfaya hızlı bir şekilde gitmek
Gezinti araması özelliği, belirli bir sayfayı hızla bulmak için de harika bir araç işlevi görür. Örneğin, **Ödeme günlüğü** sayfasını sık kullanan bir borç hesapları memuruysanız, **Arama** kutusuna "ödeme günlüğü" girebilirsiniz. Giriş sayfa başlığı için tam bir eşleşme olduğundan, sayfa arama sonuçlarının üst kısmında listelenir ve sayfaya hızlı bir şekilde gidebilirsiniz. 

Arama sonuçları listesinde sayfa başlığının yanı sıra gezinti yolu da görüntülenir. Bu, sayfanın uygulamadaki yerini gösterir. Ayrıca, sonuçlardaki iki veya daha fazla benzer sayfayı birbirlerinden ayırt etmenize yardımcı olur. 

Sayfa aradığınız zaman, girişiniz sayfa başlığıyla ve aynı zamanda gezinti yoluyla eşleştirilir. Örneğin **Arama** kutusuna "alacak" girerseniz, sayfa başlıklarında "alacak" sözcüğü yer almasa bile, Alacak hesapları alanında kullanımınıza sunulan sayfalar için sonuçları görürsünüz. 

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Teknik form adını temel alarak bir sayfaya hızlı bir şekilde gitmek
Gezinti araması işlevi, ileri düzeydeki kullanıcılar için çok istenen bir özellik içeriyor: teknik form adına göre bir sayfaya hızlı bir şekilde gidebilme. Birçok kullanıcı sistemi çalıştıkları form adlarını tam olarak biliyor. Bu kullanıcılardan biriyseniz aradığınız form adının önüne **form:** yazabilirsiniz. Örneğin **form: satıcıfatura** girerseniz, arama sonuçlarında form adının **satıcıfatura** ile başladığı tüm sayfalar gösterilir. 

## <a name="administration-and-security"></a>Yönetim ve güvenlik
Yönetim ve güvenlik açısından bakıldığında, gezinti araması işlevi şuralarda yalnızca iki türde sonuç ortaya çıkartır:

-   Geçerli yapılandırmada (yapılandırma anahtarları aracılığıyla) etkinleştirilmiş sayfalar.
-   Kullanıcının, rolüne göre erişimin olduğu sayfalar.

Arama sonuçları listesi 10 öğeyle sınırlıdır. Aradığınızı sonuçlarda bulamazsanız, girişi daraltmayı veya güncelleştirmeyi denemelisiniz. 

## <a name="development"></a>Geliştirme 
Geliştirme açısından bakıldığında, gezinti araması, kolay yararlanılan bir işlevdir çünkü menü öğelerinin dağıtımı ve arama sonuçlarında görünmeleri arasında neredeyse hiç gecikme yoktur. Menü öğeleri gezinti bölmesinden veya panodan bağlantılı olduğu sürece, otomatik olarak aranabilir olacaktır. 

