---
title: Gezinti araması
description: Bu konuda, sayfalarda gezinmek için arama işlevinin nasıl kullanılacağı açıklanmaktadır.
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6b99c677af0d20ea04f65f5b17cf07a2a45cf99
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565397"
---
# <a name="navigation-search"></a>Gezinti araması

[!include [banner](../includes/banner.md)]

Bu konuda, sayfalarda gezinmek için arama işlevinin nasıl kullanılacağı açıklanmaktadır.

Uygulama, çeşitli görevleri gerçekleştirmenize yardımcı olmak için çok sayıda alan ve sayfa içerir. Görevlerinizi tamamlamak için ihtiyaç duyduğunuz sayfaları hızlı bir şekilde bulmak için gezinti araması özelliğini kullanın.

Bu özelliği kullanmak için **Arama** simgesine tıklayarak **Arama** kutusunu görüntüleyin. Kutuya bir veya birden fazla sözcük yazabilirsiniz. Sistem, uygulamadaki ilgili sayfalarda, girmiş olduğunuz sözcüklerle eşleşmeler arar. Örneğin, giriş olarak "satıcı faturası" yazdığınızda o girişle eşleşen sonuçları görüntüler.

> [!NOTE]
> **Arama** kutusu, sayfaları bulmanıza ve sayfalarda gezinmenize yardımcı olur. Belirli verileri veya eylemleri bulmanıza yardımcı olmaz.

[![search-box](media/navigation-search.png "Arama kutusu")

## <a name="quickly-navigate-to-a-particular-page"></a>Belirli bir sayfaya hızlı bir şekilde gitmek

Gezinti araması özelliği, belirli bir sayfayı hızla bulmak için de harika bir araç işlevi görür. Örneğin, **Ödeme günlüğü** sayfasını sık kullanan bir borç hesapları memuruysanız, **Arama** kutusuna "ödeme günlüğü" girebilirsiniz. Giriş sayfa başlığı için tam bir eşleşme olduğundan, sayfa arama sonuçlarının üst kısmında listelenir ve sayfaya hızlı bir şekilde gidebilirsiniz.

Arama sonuçları listesinde sayfa başlığının yanı sıra gezinti yolu da görüntülenir. Bu, sayfanın uygulamadaki yerini gösterir. Ayrıca, sonuçlardaki iki veya daha fazla benzer sayfayı birbirlerinden ayırt etmenize yardımcı olur.

Sayfa aradığınız zaman, girişiniz sayfa başlığıyla ve aynı zamanda gezinti yoluyla eşleştirilir. Örneğin **Arama** kutusuna "alacak" girerseniz, sayfa başlıklarında "alacak" sözcüğü yer almasa bile, Alacak Hesapları alanında kullanımınıza sunulan sayfalar için sonuçları görürsünüz.

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Teknik form adını temel alarak bir sayfaya hızlı bir şekilde gitmek

Gezinti araması işlevi, ileri düzeydeki kullanıcılar için çok istenen bir özellik içeriyor: teknik form adına göre bir sayfaya hızlı bir şekilde gidebilme. Birçok kullanıcı sistemi çalıştıkları form adlarını tam olarak biliyor. Bu kullanıcılardan biriyseniz aradığınız form adının önüne **form:** yazabilirsiniz. Örneğin **form: satıcıfatura** girerseniz, arama sonuçlarında form adının **satıcıfatura** ile başladığı tüm sayfalar gösterilir.

## <a name="administration-and-security"></a>Yönetim ve güvenlik

Yönetim ve güvenlik açısından bakıldığında, gezinti araması işlevi şuralarda yalnızca iki türde sonuç ortaya çıkartır:

- Geçerli yapılandırmada (yapılandırma anahtarları aracılığıyla) etkinleştirilmiş sayfalar.
- Kullanıcının, rolüne göre erişimin olduğu sayfalar.

Arama sonuçları listesi 10 öğeyle sınırlıdır. Aradığınızı sonuçlarda bulamazsanız, girişi daraltmayı veya güncelleştirmeyi denemelisiniz.

## <a name="development"></a>Geliştirme

Geliştirme açısından bakıldığında, gezinti araması, kolay yararlanılan bir işlevdir çünkü menü öğelerinin dağıtımı ve arama sonuçlarında görünmeleri arasında neredeyse hiç gecikme yoktur. Menü öğeleri gezinti bölmesinden veya panodan bağlantılı olduğu sürece, otomatik olarak aranabilir olacaktır.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]