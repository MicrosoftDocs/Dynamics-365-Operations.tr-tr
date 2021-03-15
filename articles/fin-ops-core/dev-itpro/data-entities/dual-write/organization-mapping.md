---
title: Dataverse'da kuruluş hiyerarşisi
description: Bu konu Finance and Operations uygulamaları ile Dataverse arasında kuruluş verileri tümleştirmesini açıklar.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5132fd85fdf2c08ccded9db590328c394a2f984e
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744705"
---
# <a name="organization-hierarchy-in-dataverse"></a>Dataverse'da kuruluş hiyerarşisi

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Finance finansal bir sistem olduğundan, *kuruluş* temel bir kavramdır ve sistem kurulumu bir kuruluş hiyerarşisi yapılandırmasıyla başlar. İşletme mali öğeleri kuruluş düzeyinde ve ayrıca kuruluş hiyerarşisindeki herhangi bir düzeyde izlenebilir.

Dataverse'da kuruluş hiyerarşisi kavramı bulunmasa da, toplam satış geliri gibi birkaç genel kavramlar bulunur. Dataverse tümleştirmesinin bir parçası olarak, kuruluş hiyerarşisi veri yapısı Dataverse'a eklenir.

## <a name="data-flow"></a>Veri akışı

Finance and Operations uygulamaları ve Dataverse'dan olan işletme ekosistemi bir kuruluş hiyerarşisine sahip olmaya devam edecektir. Bu kuruluş hiyerarşisi Finance and Operations uygulamaları üzerinde oluşturulur ancak bilgi ve genişletilebilirlik amaçları Dataverse'da kullanıma sunulur. Aşağıdaki örnekte Dataverse'ta Finance and Operations uygulamalarından Dataverse'a tek yönlü veri akışı olarak sunulan kuruluş hiyerarşisi bilgileri gösterilmektedir.

![Mimari resmi](media/dual-write-data-flow.png)

Kuruluş hiyerarşisi tablo eşlemeleri, Finance and Operations uygulamalarından Dataverse'e tek yönlü veri eşitleme için kullanılabilir.

## <a name="templates"></a>Şablonlar

Ürün bilgileri, ürün boyutları veya izleme ve depolama boyutları gibi ürünle ve ürün tanımıyla ilgili tüm bilgileri içerir. Aşağıdaki tabloda gösterildiği gibi, ürün ve ilgili bilgileri eşitlemek için tablo haritaları koleksiyonu oluşturulur.

Finance and Operations uygulamaları | Diğer Dynamics 365 uygulamaları | Tanım
-----------------------|--------------------------------|---
Kuruluş hiyerarşisi amaçları | msdyn_internalorganizationhierarchypurposes | Bu şablon, Kuruluş Hiyerarşisi Amacı tablosunun tek yönlü eşitlemesini sağlar.
Kuruluş hiyerarşisi türü | msdyn_internalorganizationhierarchytypes | Bu şablon, Kuruluş Hiyerarşisi Türü tablosunun tek yönlü eşitlemesini sağlar.
Kuruluş hiyerarşisi - yayımlandı | msdyn_internalorganizationhierarchies | Bu şablon, Yayımlanan Kuruluş Hiyerarşisi tablosunun tek yönlü eşitlemesini sağlar.
Faaliyet birimi | msdyn_internalorganizations |
Tüzel kişilikler | msdyn_internalorganizations |
Tüzel kişilikler | cdm_companies | Tüzel kişilik (şirket) bilgilerinin iki yönlü eşitlemesini sağlar.

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Dahili Kuruluş

Dataverse'teki dahili kuruluş bilgileri iki tablodan gelir: **faaliyet birimi** ve **tüzel kişilikler**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]