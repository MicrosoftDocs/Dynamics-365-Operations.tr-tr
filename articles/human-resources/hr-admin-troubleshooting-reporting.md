---
title: Raporlama seçenekleri
description: Bu konu, bir müşteri Microsoft Dynamics 365 Human Resources raporlarını özelleştirmek istediğinde veya yeni raporlar oluşturmak istediğinde ortaya çıkan sorunun nasıl çözüleceğini açıklar.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66581331dceacc1c0fa1816bf336339693db5339
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463298"
---
# <a name="reporting-options"></a>Raporlama seçenekleri

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Ortam ayrıntıları**

Bu sorun tüm ortamlar için geçerlidir.

**Belirti**

Müşteri, Microsoft Dynamics 365 Human Resources raporlarını özelleştirmek veya yeni raporlar oluşturmak istiyor.

**Stok çıkışı**

Kullanıcı, katıştırılmış Microsoft Power BI raporlarını özelleştiremiyor.

**Çözüm**

- Dataverse'e akan İnsan Kaynakları verileri, Power Apps Dataverse bağlayıcısı aracılığıyla Power BI Desktop'a raporlanabilir. Dataverse'in, İnsan Kaynakları verisinin bir alt kümesini içerdiğini unutmayın. Power BI ve panolar hakkında daha fazla bilgi için bkz. [Power BI raporlarını ve panolarını Power Apps Common Data Service ile oluşturma](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronik raporlama (ER), İnsan Kaynakları içindeki bazı raporlar için kullanılabilir. Müşteri odaklı özelleştirmeler, ER yapılandırma seçenekleri aracılığıyla yapılabilir.
- Veri, Microsoft Excel veya Microsoft Word'e, İnsan Kaynakları'nın Microsoft Office tümleştirmesi aracılığıyla sunduğu çeşitli veri varlıkları kullanılarak dışa aktarılabilir.

**Uzun vadeli çözüm**

Ek Power BI seçenekleri kullanılabilir olacaktır ve daha fazla veri ve varlık Dataverse'in parçası olacaktır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]