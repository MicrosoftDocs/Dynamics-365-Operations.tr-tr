---
title: Common Data Service'da kuruluş hiyerarşisi
description: Bu konu Finance and Operations uygulamaları ile Common Data Service arasında kuruluş verileri tümleştirmesini açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fbf7cc33d12fb54d2ff02acc46ba2e284b2a2b3f
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020058"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Common Data Service'da kuruluş hiyerarşisi

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Dynamics 365 Finance finansal bir sistem olduğundan, *kuruluş* temel bir kavramdır ve sistem kurulumu bir kuruluş hiyerarşisi yapılandırmasıyla başlar. İşletme mali öğeleri kuruluş düzeyinde ve ayrıca kuruluş hiyerarşisindeki herhangi bir düzeyde izlenebilir.

Common Data Service'da kuruluş hiyerarşisi kavramı bulunmasa da, toplam satış geliri gibi birkaç genel kavramlar bulunur. Common Data Service tümleştirmesinin bir parçası olarak, kuruluş hiyerarşisi veri yapısı Common Data Service'a eklenir.

## <a name="data-flow"></a>Veri akışı

Finance and Operations uygulamaları ve Common Data Service'dan olan işletme ekosistemi bir kuruluş hiyerarşisine sahip olmaya devam edecektir. Bu kuruluş hiyerarşisi Finance and Operations uygulamaları üzerinde oluşturulur ancak bilgi ve genişletilebilirlik amaçları Common Data Service'da kullanıma sunulur. Aşağıdaki örnekte Common Data Service'ta Finance and Operations uygulamalarından Common Data Service'a tek yönlü veri akışı olarak sunulan kuruluş hiyerarşisi bilgileri gösterilmektedir.

![Mimari resmi](media/dual-write-data-flow.png)

## <a name="templates"></a>Şablonlar

Kuruluş hiyerarşisi varlık eşlemeleri, Finance and Operations uygulamalarından Common Data Service'a tek yönlü veri eşitleme için kullanılabilir.

## <a name="templates"></a>Şablonlar

Ürün bilgileri, ürün boyutları veya izleme ve depolama boyutları gibi ürünle ve ürün tanımıyla ilgili tüm bilgileri içerir. Aşağıdaki tabloda gösterildiği gibi, ürün ve ilgili bilgileri eşitlemek için varlık haritaları koleksiyonu oluşturulur.

Finance and Operations | Diğer Dynamics 365 uygulamaları | Tanım
-----------------------|--------------------------------|---
Kuruluş hiyerarşisi amaçları | msdyn_internalorganizationhierarchypurposes | Bu şablon, Kuruluş Hiyerarşisi Amacı varlığının tek yönlü eşitlemesini sağlar.
Kuruluş hiyerarşisi türü | msdyn_internalorganizationhierarchytypes | Bu şablon, Kuruluş Hiyerarşisi Türü varlığının tek yönlü eşitlemesini sağlar.
Yayımlanan kuruluş hiyerarşisi | msdyn_internalorganizationhierarchies | Bu şablon, Yayımlanan Kuruluş Hiyerarşisi varlığının tek yönlü eşitlemesini sağlar.
Faaliyet birimi | msdyn_internalorganizations | 
Tüzel kişilikler | msdyn_internalorganizations | 
Tüzel kişilikler | cdm_companies | Tüzel kişilik (şirket) bilgilerinin iki yönlü eşitlemesini sağlar.


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Dahili Kuruluş

Common Data Service'daki dahili kuruluş bilgileri iki varlıktan gelir: **Faaliyet birimi** ve **Tüzel kişilikler**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
