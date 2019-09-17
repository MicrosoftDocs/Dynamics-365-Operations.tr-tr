---
title: Talent içerisinde raporlama seçenekleri
description: Bu konu, bir müşteri Microsoft Dynamics 365 for Talent raporlarını özelleştirmek istediğinde veya yeni raporlar oluşturmak istediğinde ortaya çıkan sorunun nasıl çözüleceğini açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e7348a515b08523c15aa8f74d5616a3daf645b7
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741810"
---
# <a name="reporting-options-in-talent"></a>Talent'taki raporlama seçenekleri

[!include [banner](includes/banner.md)]

**Ortam ayrıntıları**

Bu sorun tüm ortamlar için geçerlidir.

**Belirti**

Müşteri, Microsoft Dynamics 365 for Talent raporlarını özelleştirmek veya yeni raporlar oluşturmak istiyor.

**Stok çıkışı**

Kullanıcı, katıştırılmış Microsoft Power BI raporlarını özelleştiremiyor.

**Çözüm**

- Common Data Service'a akan Core HR veriler, PowerApps Common Data Service bağlayıcısı aracılığıyla Power BI Desktop'a raporlanabilmektedir. Common Data Service'in, Core HR verisinin bir alt kümesini içerdiğini unutmayın. Power BI ve panolar hakkında daha fazla bilgi için bkz. [Power BI raporları ve panolarını PowerApps Common Data Service ile birlikte oluşturmak](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronik raporlama (ER), Talent içindeki bazı raporlar için kullanılabilir. Müşteri odaklı özelleştirmeler, ER yapılandırma seçenekleri aracılığıyla yapılabilir.
- Veri, Microsoft Excel veya Microsoft Word'e, Talent'ın Microsoft Office tümleştirmesi aracılığıyla sunduğu çeşitli veri varlıkları kullanılarak dışa aktarılabilir.

**Uzun vadeli çözüm**

Ek Power BI seçenekleri kullanılabilir olacaktır ve daha fazla veri ve varlık Common Data Service'in parçası olacaktır.
