---
title: Raporlama seçenekleri
description: Bu konu, bir müşteri Microsoft Dynamics 365 Human Resources raporlarını özelleştirmek istediğinde veya yeni raporlar oluşturmak istediğinde ortaya çıkan sorunun nasıl çözüleceğini açıklar.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64a03724d81745373d028d76a8cc64aab66efdbb
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053311"
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