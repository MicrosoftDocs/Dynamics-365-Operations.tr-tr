---
title: Taşıma yönetimine genel bakış
description: Bu konuda, Supply Chain Management'taki taşıma yönetimi işlevine genel bir bakış sunulmaktadır.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench, TMSLoadBuildTemplateApply, WHSLoadTemplate, TMSTransportationStatus, TMSLoadSeal, TMSLoadBuildProposal, TMSLoadBuildWorkbench, TMSLoadBuildStrategy, TMSLoadBuildStrategyAttributeValue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4affc5846ee329a4571d6fb3e0c42873387241ad
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439666"
---
# <a name="transportation-management-overview"></a>Taşıma yönetimine genel bakış

[!include [banner](../includes/banner.md)]

Bu konuda, Supply Chain Management'taki taşıma yönetimi işlevine genel bir bakış sunulmaktadır.

Taşıma yönetimi, şirketinizin taşımalarını kullanmanıza olanak tanır ve satıcı ile gelen ve giden siparişler için yönlendirme çözümlerini belirlemenizi sağlar. Örneğin bir sevkiyat için en hızlı yolu veya en ucuz oranı tanımlayabilirsiniz. Aşağıdaki tabloda, Taşıma yönetiminin kullanılmasına ilişkin ana senaryolar açıklanmaktadır.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Senaryo</th>
<th>Taşıma yönetimi nasıl yardımcı olur?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Taşıma faaliyetleri için dış lojistik sağlayıcılarını kullanın.</td>
<td>Gelen ve/veya giden taşıma için Taşıma yönetimini kullanın.</td>
</tr>
<tr class="even">
<td>Şirketin teslimat/mal alımı için kullandığı kendi filosu vardır ve teslimat giderleri müşterilere aktarılır.</td>
<td>Giden işlemleri için, taşıma giderlerini belirlemek ve bunları müşterilere aktarmak için Taşıma yönetimini kullanabilirsiniz. Ancak, taşıyıcı fatura mutabakat işlemi gerekli değildir.</td>
</tr>
<tr class="odd">
<td>Teslimat/mal alımı için şirketin kendi filosu vardır ancak ürün fiyatı nakliyeyi içerdiğinden teslimat giderleri müşterilere aktarılmaz.</td>
<td>Çok sayıda Taşıma yönetimi işlevi gerekli değildir. Bununla birlikte, taşıma fiyatlarını belirlemek ve satış fiyatını buna göre ayarlamak için Taşıma yönetimini kullanabilirsiniz.</td>
</tr>
<tr class="even">
<td>Lojistik hizmeti aynı şirketteki başka bir tüzel kişilik tarafından sağlanır.</td>
<td><ul>
<li>Başka bir tüzel kişiliği herhangi bir sevkiyat yüklenicisi olarak kullanmak için Taşıma yönetimini kullanabilirsiniz. Tüzel kişilikler arasındaki ekonomik hareketleri otomatik hale getiremezsiniz. Bu nedenle, bu hareketleri el ile işlemeniz gerekir (örneğin, bir satınalma siparişi oluşturarak).</li>
<li>Lojistik hizmetler sunan tüzel kişilikte, Taşıma yönetimi taşıma ücretlerini belirlemek için kullanılabilir.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-supply-chain-management"></a>Supply Chain Management'ta taşımayı planlama
Taşıma yönetiminde , taşıma planlaması için siparişler veya bu siparişlere göre oluşturulan sevkiyatlar temel alınır. Sevkiyatlar daima zaman içinde bir noktada bulunmaktadır ancak taşıma planlaması için gerekli değildir. Transfer emirleri giden senaryosunun bir parçasıdır ve satış siparişleriyle birlikte planlanabilir. 

![Yük çekme](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Gelen taşıma
Bir satıcıya madde siparişi verdiğiniz zaman ve bu maddelerin sizin ambarınıza teslim edilmesi gerektiğinde maddeleri taşımayı kendiniz düzenlemek isteyebilirsiniz. Gelen yükün taşıma ve girişini planlamak için Supply Chain Management kullanabilirsiniz. Aşağıdaki şekilde, gelen yük için taşıma planlamasına ilişkin iş süreci akışı gösterilmektedir. 

![Gelen yükün taşınmasına ilişkin iş süreci akışı](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Giden taşıma
Belirli maddeleri şirketin ambarından müşteriye sevk etmek için giden yük planlaması yapabilir ve işleme koyabilirsiniz. Giden yükün taşıma ve sevkiyatını planlamak için Supply Chain Management kullanabilirsiniz. Aşağıdaki şekilde, giden yükün sevkiyat için planlaması ve işleme konmasına ilişkin iş süreci akışı gösterilmektedir. 

![Giden yükleri planlama ve işleme](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Yapıyı yükle
Supply Chain Management, Hacim tabanlı yük oluşturma stratejisi olarak adlandırılan bir yük oluşturma stratejisi sunar. Bu strateji, yük şablonunda yükseklik ve ağırlık için belirtilen maksimum değerleri kullanmanıza olanak tanır; veya yeni değerler girerek ayarları geçersiz kılabilirsiniz. Kullanmak için **Yük oluşturma workbench'i** sayfasında bulunan **Ayar** Hızlı sekmesindeki **Yük oluşturma stratejisi** alanından bu stratejiyi seçebilirsiniz. Ayrıca, Uygulama Nesne Ağacı'nda (AOT) yeni bir sınıf oluşturarak kendi yük oluşturma stratejinizi ekleyebilirsiniz.



