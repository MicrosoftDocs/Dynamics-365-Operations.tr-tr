---
title: "Maliyet nesnesi boyutları"
description: "Maliyetleri analiz ettiğinizde maliyetlerin nereye aktığını belirlemek için maliyet öğesi boyutlarını kullanın. Maliyetleri nereye atamanız gerektiğini belirlemek için maliyet nesnesi boyutlarını kullanın. Bu konu, maliyet nesnesi boyutları hakkında bilgiler sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d38f0aa1c3272d5361e6fcca57d693cfa0042f3c
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="cost-object-dimensions"></a>Maliyet nesnesi boyutları

[!include[banner](../includes/banner.md)]


Maliyetleri analiz ettiğinizde maliyetlerin nereye aktığını belirlemek için maliyet öğesi boyutlarını kullanın. Maliyetleri nereye atamanız gerektiğini belirlemek için maliyet nesnesi boyutlarını kullanın. Bu konu, maliyet nesnesi boyutları hakkında bilgiler sağlar.

Maliyet nesnesi tahmin etmek, maliyetleri tahsis etmek veya doğrudan ölçmek istediğiniz herhangi bir tür nesne olabilir. Maliyet nesneleri genellikle ürünleri, projeleri, kaynakları, departmanları, maliyet merkezlerini ve coğrafi bölgeleri içerir. Yönetim, maliyetlerini sayısallaştırmak ve ayrıca karlılık analizini sürdürmek için maliyet nesnelerini kullanır.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Maliyet nesnesi boyutları ve maliyet nesnesi boyut üyeleri
Maliyet nesneleri *maliyet nesnesi boyutları* olarak da bilinir. Maliyet nesnesi boyutunun hangi varlığa başvuracağına karar vermenizden sonra tek tek boyut değerlerini belirlemeniz veya diğer kaynak sistemlerden Maliyet muhasebesine aktarmanız gerekir. Bu tek tek boyut değerleri *maliyet nesnesi boyut üyeleri* olarak bilinir. Örneğin, maliyet nesnesi boyutu olarak Maliyet merkezi adlandırılan mali boyutu kullanmak istiyorsunuz. Maliyetlerin tek tek maliyet merkezlerine nasıl dağıldığını görmek için maliyet nesnesi boyut üyelerini içe aktarmanız gerekir. Bu durumda maliyet nesnesi boyut üyeleri Satış, Üretim, Yönetim ve Coğrafi konumlar gibi fiili maliyet merkezleridir. Aşağıdaki ekran görüntüsü, maliyet nesnesi boyutu olarak Maliyet Merkezlerini maliyet nesnesi boyut üyesi olarak fiili maliyet hesaplarıyla gösterir. 

[![maliyet-nesnesi-boyutlari](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Veri bağlayıcıları üzerinden maliyet nesnesi boyut üyelerini içe aktarma
Maliyet nesnesi boyut üyelerini içe aktarmayı daha kolay hale getirmek için maliyet nesne boyutu olarak kullanmak istediğiniz varlıklardan değerleri almak için veri bağlayıcıları kullanın. Önceden oluşturulmuş veri bağlayıcılarını veya oluşturduğunuz özel veri bağlayıcıları kullanabilirsiniz.



