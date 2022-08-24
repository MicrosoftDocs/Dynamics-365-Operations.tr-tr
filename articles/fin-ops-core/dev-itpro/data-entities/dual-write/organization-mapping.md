---
title: Dataverse'da kuruluş hiyerarşisi
description: Bu makalede, finans ve operasyon uygulamaları ile Dataverse arasında kuruluş verileri tümleştirmesi açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 48533dd104f62080d0ebd47389a4a829c772db13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289061"
---
# <a name="organization-hierarchy-in-dataverse"></a>Dataverse'da kuruluş hiyerarşisi

[!include [banner](../../includes/banner.md)]



Dynamics 365 Finance finansal bir sistem olduğundan, *kuruluş* temel bir kavramdır ve sistem kurulumu bir kuruluş hiyerarşisi yapılandırmasıyla başlar. İşletme mali öğeleri kuruluş düzeyinde ve ayrıca kuruluş hiyerarşisindeki herhangi bir düzeyde izlenebilir.

Dataverse'da kuruluş hiyerarşisi kavramı bulunmasa da, toplam satış geliri gibi birkaç genel kavramlar bulunur. Dataverse tümleştirmesinin bir parçası olarak, kuruluş hiyerarşisi veri yapısı Dataverse'a eklenir.

## <a name="data-flow"></a>Veri akışı

Finans ve operasyon uygulamaları ve Dataverse'ten olan işletme ekosistemi bir kuruluş hiyerarşisine sahip olmaya devam edecektir. Bu kuruluş hiyerarşisi finans ve operasyon uygulamaları üzerinde oluşturulur ancak bilgi ve genişletilebilirlik amaçları Dataverse'te kullanıma sunulur. Aşağıdaki örnekte Dataverse'te finans ve operasyon uygulamalarından Dataverse'e tek yönlü veri akışı olarak sunulan kuruluş hiyerarşisi bilgileri gösterilmektedir.

![Mimari resmi.](media/dual-write-data-flow.png)

Kuruluş hiyerarşisi tablo eşlemeleri, finans ve operasyon uygulamalarından Dataverse'e tek yönlü veri eşitleme için kullanılabilir.

## <a name="templates"></a>Şablonlar

Bir organizasyon, bir iş sürecini gerçekleştirmek veya bir hedefe ulaşmak için birlikte çalışan bir grup insandır. Organizasyonel hiyerarşiler, işinizi meydana getiren organizasyonlar arasındaki ilişkileri temsil eder. Tüzel kişilikler, işletme birimleri ve ekipler gibi dahili kuruluş türlerini tanımlayabilirsiniz. Aşağıdaki tabloda gösterildiği gibi, yasal varlıkları, çalışma birimlerini, ve ilgili kuruluş hiyerarşi bilgilerini eşitlemek için bir tablo haritaları koleksiyonu oluşturulur.

Finans ve Operasyon uygulamaları | Müşteri etkileşimi uygulamaları     | Açıklama
-----------------------|--------------------------------|---
[Tüzel kişilikler](mapping-reference.md#102) | cdm_companies | 
[Tüzel kişilikler](mapping-reference.md#142) | msdyn_internalorganizations |
[Faaliyet birimi](mapping-reference.md#143) | msdyn_internalorganizations |
[Kuruluş hiyerarşisi - yayımlandı](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Bu şablon, Yayımlanan Kuruluş Hiyerarşisi tablosunun tek yönlü eşitlemesini sağlar.
[Kuruluş hiyerarşisi amaçları](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Bu şablon, Kuruluş Hiyerarşisi Amacı tablosunun tek yönlü eşitlemesini sağlar.
[Kuruluş hiyerarşisi türü](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Bu şablon, Kuruluş Hiyerarşisi Türü tablosunun tek yönlü eşitlemesini sağlar.

## <a name="internal-organization"></a>Dahili Kuruluş

Dataverse'teki dahili kuruluş bilgileri, **Faaliyet birimi** ve **Tüzel kişilikler** olmak üzere iki tablodan gelir.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

