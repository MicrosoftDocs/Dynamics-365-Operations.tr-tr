---
title: B2B web sitesi siparişlerini hızla verme
description: Bu konu, işletmeler arası (B2B) site kullanıcılarının toplu ve yinelenen siparişleri hızla verebilmesine olanak tanıyan Microsoft Dynamics 365 Commerce özelliklerini açıklamaktadır.
author: shajain
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 4909056435425f251efb45f5a4355f103a420ba8
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/16/2022
ms.locfileid: "8312598"
---
# <a name="place-b2b-website-orders-quickly"></a>B2B web sitesi siparişlerini hızla verme

[!include [banner](../../includes/banner.md)]

Bu konu, işletmeler arası (B2B) site kullanıcılarının toplu ve yinelenen siparişleri hızla verebilmesine olanak tanıyan Microsoft Dynamics 365 Commerce özelliklerini açıklamaktadır.

Dynamics 365 Commerce B2B e-ticaret web siteleri, kullanıcıların arama ve gözatma yoluyla yeni ürünleri keşfetmek, ürün ayrıntılarını görüntülemek, sepete öğeler eklemek ve satın almak gibi standart işlemleri gerçekleştirmesini sağlar. Ancak, işletmeler arası (B2C) sitelerinin müşterileri genel olarak küçük miktarlarda ürün sipariş eder ve bunları yalnızca bir kez sipariş ederken B2B müşterileribüyük miktarlarda sipariş verir ve bunları birden çok kere sipariş eder. Bu müşteriler genellikle satın almak istedikleri ürünleri tam olarak bildiklerinden genellikle ürün bulma aşamasını atlar ve doğrudan sipariş vermeye geçer. Commerce B2B e-ticaret web siteleri, bu müşterilerin ihtiyaçlarını karşılamak için siparişleri hızlı bir şekilde vermenize yardımcı olan çeşitli yetenekler sağlar.

## <a name="bulk-order-by-item-number"></a>Madde numarasına göre toplu sipariş

Commerce B2B e-ticaret web siteleri, site kullanıcılarının istenen miktarla birlikte ürün madde numaralarını girerek alışveriş sepetine madde eklemesine olanak tanır.

Aşağıdaki şekilde ürün madde numarasına göre sipariş girişi örneği gösterilmektedir.

![Ürün madde numarasına göre hızlı sipariş girişi.](../media/QuickAddByItem.png)

## <a name="bulk-order-by-variant"></a>Ürün çeşidine göre toplu sipariş

Commerce B2B e-ticaret web siteleri, site kullanıcılarının stok kullanılabilirliğini boyut, renk ve stile göre gösteren tek bir görünümde hızla aynı ürünün farklı çeşitlerini eklemesine olanak tanır. Ayrıca, site kullanıcıları **Tüm miktarları gir**'i seçerek stoktaki tüm ürünler için kolaylıkla aynı miktarı girebilirler.

Aşağıdaki örnekte, "tüm miktarları gir" işlevi kullanılan bir hızlı sipariş girişi örneği gösterilmektedir.

!["Tüm miktarları gir" işlevini kullanan hızlı sipariş girişi.](../media/MatrixView.png)

## <a name="use-order-templates-for-quick-order-entry"></a>Hızlı sipariş girişi için sipariş şablonlarını kullanma

B2B web sitelerindeki alıcılar genellikle belirli maddeleri bir arada sipariş eder. Örneğin, bir inşaat tesisi için siparişler veriyorsanız gömlek, ceket, pantolon, ayakkabı ve şapkaları birlikte sipariş vermek isteyebilirsiniz. Doktor, hemşire ve temizlik çalışanlarının farklı üniformlar kullandığı bir hastane için siparişler veriyorsanız daha kolay sipariş vermek için her bir üniforma türünü birlikte gruplamak isteyebilirsiniz. Bu tür senaryolar için Commerce B2B siteleri sipariş şablonlarının oluşturulmasına olanak tanır. Site kullanıcıları istedikleri sayıda özel şablon oluşturabilir ve sonra bu şablonlardaki maddelerin tümünü veya bir kısmını gereksinim duydukları şekilde sipariş edebilir.

Aşağıdaki örnekte, sipariş şablonu örneği gösterilmektedir.

![Sipariş şablonu örneği.](../media/OrderTemplateHeader.png)

Aşağıdaki örnekte, sipariş şablonu ayrıntılı görünümünün bir örneği gösterilmektedir.

![Sipariş şablonunun ayrıntılar görünümü örneği.](../media/OrderTemplateLines.png)

## <a name="reorder-from-order-history"></a>Sipariş geçmişinden yeniden sipariş verme

Commerce B2B e-ticaret web siteleri, site kullanıcılarının maddeleri sipariş geçmişlerinden hızlıca yeniden oluşturmasını sağlar. Site kullanıcıları, seçili maddeleri kendi sipariş geçmişlerinden satın alabilir veya alışveriş sepetine daha önce satın alınan tüm maddeleri ekleyebilir.

Aşağıdaki örnekte kullanıcının sipariş geçmişi ve sipariş geçmişinden maddeleri yeniden sipariş vermek seçeneklerine ilişkin bir örnek gösterilmektedir.

![Sipariş geçmişinden yeniden sipariş verme.](../media/Reorder.png)

Bu konuda, Commerce B2B sitelerinin kullanıcıların istedikleri ürünleri kolayca bulmasına, sipariş vermesine ve yeniden sipariş vermesine yardımcı olma yollarından bazıları açıklanmıştır. Toplu siparişler yakalama sürecini daha da basitleştirmek için daha fazla özellik geliştirilme aşamasındadır.
