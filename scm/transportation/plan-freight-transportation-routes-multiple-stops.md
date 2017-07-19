---
title: "Birden fazla duraklı navlun taşıma rotaları planlama"
description: "Bu makalede Dynamics 365 for Finance and Operations uygulamasında ulaşım yolları planlamak için kullandığınız çeşitli öğeler açıklanmaktadır."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: e7965c094f91bcbcad21ecfa599f133a6e84f4f7
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>Birden fazla duraklı navlun taşıma rotaları planlama

[!include[banner](../includes/banner.md)]


Bu makalede Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümünde ulaşım yolları planlamak için kullandığınız çeşitli öğeler açıklanmaktadır.

Birden fazla durakları olan karmaşık ulaşım yolları için rota planları ve rota kılavuzlarını kullanabilirsiniz. Aynı yol düzenli olarak kullanılacaksa, zamanlanmış bir rota ayarlayabilirsiniz.

## <a name="route-plans"></a>Rota planları
Rota planı yol üzerinde ziyaret edilen duraklar ve her segment için kullanılan taşıyıcılar hakkında bilgiler sağlayan rota segmentleri içerir. Rota üzerindeki durakları hub olarak tanımlamanız gerekir. Hub bir satıcı, ambar, müşteri veya taşıyıcı değiştirdiğiniz bir yeniden yükleme alanı olabilir. Her segment için çeşitli ücretlerle "nokta oranları" tanımlayabilirsiniz. Burada bazı örnekler verilmiştir:

-   Verilen kesimlere seyahat giderleri
-   Ürünleri çekme giderleri
-   Ürünleri bırakma giderleri

Her rota planı bir rota kılavuzu ile ilişkilendirilmiş olmalıdır.

## <a name="route-guides"></a>Rota kılavuzları
Rota kılavuzu belirli bir rota planıyla bir yükü eşleştirme ölçütlerini tanımlar. Örneğin bir kaynak hub ve hedef hub, konteyner hacmi veya ağırlığı için sınırlar ve bir sevkiyat taşıyıcısı, hizmeti veya grubu belirleyebilirsiniz. Rota kılavuzları yüklerin rotalarla el ile veya otomatik olarak eşleştirilebileceği **Rota çalışma ekranı oranı** sayfasında bulunmaktadır. Rota kılavuzu planlanmış bir rota içinse, **Yük oluşturma çalışma ekranı** sayfasında da bulunabilir.

## <a name="scheduled-routes"></a>Planlanan rotalar
Planlanan bir rota sevkiyat tarihleri için bir planı olan, önceden tanımlanmış bir rota planıdır. Planlanan rotalar ve planlanmayan rotalar bunlara atanan yükler açısından farklılık gösterir. Planlanmayan bir rotayı Rota çalışma ekranı oranı kullanarak atadığınızda yalnızca yük ve rota kılavuzu doğrulanır. Planlanan bir rota atadığınızda, siparişlerden ve hublardan alınan tarihler ve adresler, rota planındaki tarih gibi tüm bilgiler ele alınır. Yükleri planlanan bir rotaya el ile atamak için Rota çalışma ekranı oranı sayfasını kullanmanız gerekmez. Bunun yerine, yüklerin verilen bir planlana rotaya ilişkin satış siparişinden alınan müşteri adresleri ve teslimat tarihlerine göre oluşturulacağını gösteren Yük oluşturma çalışma ekranını kullanabilirsiniz. Planlanan rotalarda rota planının kaynak ve hedef hub'ları sabittir. Genellikle sevkiyat taşıyıcısı ve hizmeti tüm segmentlerde aynıdır ancak farklı da olabilir. Hedef hub'lar rota üzerinde ziyaret edilen müşterilerin posta kodları kullanılarak oluşturulur. Bir rota planı için birkaç rota zaman çizelgesi tanımlanabilir. Rota planı bir rota kılavuzu ile ilişkilendirilmiş olmalıdır. Ancak planlanan rotalarda plan yalnızca tek bir rota kılavuzu ile ilişkilendirilebilir. Rota zaman çizelgesi yalnızca **Rota zaman çizelgesi** sayfasında gerçek rotalar oluşturmak için kullanılır. Yük oluşturma çalışma ekranında yük önerirken varsayılan yük şablonunu kullanabilirsiniz.

## <a name="load-building-workbench"></a>Yük oluşturma çalışma ekranı
Yük oluşturma çalışma ekranı yük önermek için, satış siparişlerinden alınan müşteri adreslerini ve teslimat tarihleri ile kullanılabilen planlanan rotaları kullanır. Varsayılan olarak rotanın değerleri çalışma ekranına girilir. Ancak rotadaki "başlangıç" tarihinden önceki bir "başlangıç" tarihi seçebilirsiniz. Yük önerildiğinde tüm açık satış siparişlerinin teslimat adresi ve teslimat tarihi denetlenir. Teslimat adresinin posta kodu rota planındaki bir hub'ın posta kodu ile eşleşirse ve teslimat tarihi ölçütlerde seçilen aralığın içindeyse satış siparişi yük için önerilir. Yük şablonunun kapasitesi de dikkate alınır. Bir defada yalnızca bir yük önerilir. Dahil edilmeyen bir satış siparişiniz varsa, farklı bir yük şablonu kullanmanız (örneğin daha büyük bir kamyon veya konteyner için bir yük şablonu) veya ek teslimat planlamanız gerekebilir.




