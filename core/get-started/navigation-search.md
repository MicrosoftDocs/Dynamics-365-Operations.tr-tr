---
title: "Gezinti araması"
description: "Bu makalede, Microsoft Dynamics 365 işlemleri için sayfalara gitmek için arama işlevini kullanmak açıklar."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
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
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 87fed576f8cf358520d94f5cd5b326ff9801913a
ms.lasthandoff: 03/31/2017


---

# <a name="navigation-search"></a>Gezinti araması

Bu makalede, Microsoft Dynamics 365 işlemleri için sayfalara gitmek için arama işlevini kullanmak açıklar.

Dynamics 365 işlemleri için sektör ve verticals geniş bir yelpazede için işlevsellik sağlar. Uygulama alanları ve çeşitli görevleri gerçekleştirmenize yardımcı olmak için sayfaları içerir. Görevlerinizi tamamlamak için gerekli sayfaları hızlı bir şekilde bulmak için Gezinti arama özelliğini kullanın. Bu özelliği kullanmak için **Arama** simgesine tıklayarak **Arama** kutusunu görüntüleyin. Kutuya bir veya birden fazla sözcük yazabilirsiniz. Sistem, uygulamadaki ilgili sayfalarda, girdiğiniz sözcüklerle eşleşmeler arar. Örneğin, giriş olarak "satıcı faturası" yazdığınızda o girişle eşleşen sonuçları görüntüler. **Not:** **Arama** kutusu, sayfaları bulmanıza ve sayfalarda gezinmenize yardımcı olur. Belirli verileri veya eylemleri bulmanıza yardımcı olmaz. 

[![Arama kutusu](./media/search-box.png)](./media/search-box.png) Gezinti arama özelliği hızlı bir şekilde belirli bir sayfaya gitmek iyi bir yolu da görür. Örneğin, bir borç hesapları varsa memuru kim sık sık kullandığı **ödeme günlüğü** sayfası, arama kutusuna "ödeme günlüğü" girebilirsiniz. Giriş sayfası başlığı için tam bir eşleşme olduğu için sayfanın arama sonuçlarının üst kısmında listelenen ve için hızlı bir şekilde gidebilirsiniz. 

[![Arama-için-ödeme-günlük](./media/searching-for-payment-journal.png)](./media/searching-for-payment-journal.png) 

Arama sonuçları listesinde, sayfa başlığı gezinti yolunu görüntüler. Bu, sayfanın uygulamadaki konumunu bilmenize yardımcı olur. Ayrıca, sonuçlardaki iki veya daha fazla benzer sayfayı birbirlerinden ayırt etmenize yardımcı olur. Sayfa aradığınız zaman, girişiniz sayfa başlığıyla ve aynı zamanda gezinti yoluyla eşleştirilir. Örneğin, "alacak" girdiğiniz ** ** arama kutusunu göreceksiniz sonuç hesapları alanında--kullanılabilir sayfalar için sayfa başlıkları "alacak" sözcüğünü içermeyen olsa da 

[![Arama-için--word-alacak](./media/search-for-the-word-receivable.png)](./media/search-for-the-word-receivable.png) 

Bir yönetim ve güvenlik açısından, gezinti arama işlevselliği yalnızca yüzeyler:

-   Geçerli yapılandırmada (yapılandırma anahtarları aracılığıyla) etkinleştirilmiş sayfalar.
-   Kullanıcının rolüne göre erişebildiği sayfalar

Arama sonuçları listesi 10 öğeyle sınırlıdır. Aradığınızı sonuçlarda bulamazsanız, girişi daraltmayı veya güncelleştirmeyi denemelisiniz. Geliştirme açısından bakıldığında, gezinti araması, çok kolay yararlanılan bir işlevdir çünkü menü öğelerinin dağıtımı ve arama sonuçlarında görünmeleri arasında neredeyse hiç gecikme yoktur. Menü öğeleri gezinti bölmesinden veya panodan bağlantılı olduğu sürece, otomatik olarak aranabilir olacaktır. Gezinti araması işlevi, ileri düzeydeki kullanıcılar için çok istenen bir özellik içeriyor: teknik form adına göre bir sayfaya hızlı bir şekilde gidebilme. Birçok kullanıcı sistemi çalıştıkları form adlarını tam olarak biliyor. Bu kullanıcılardan biriyseniz aradığınız form adının önüne **form:** yazabilirsiniz. Örneğin **form: satıcıfatura** girerseniz, arama sonuçlarında form adının **satıcıfatura** ile başladığı tüm sayfalar gösterilir. 

[![Arama için form vendinvoice](./media/search-for-form-vendinvoice.png)](./media/search-for-form-vendinvoice.png)


