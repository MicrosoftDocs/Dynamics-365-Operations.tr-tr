---
title: Power Apps Yönetim merkezinde ortam oluşturulamıyor
description: Bu oknu, bir yönetici Microsoft Power Apps Yönetim merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 50a5aac71ec8ed850cfad32bdb1b8d589eb2885a
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413573"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Power Apps Yönetim merkezinde ortam oluşturulamıyor

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Çıkış**

- Kiracı/ortam yöneticisi, Microsoft Power Apps Yönetici merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.
- Kullanıcının, ortam oluşturma hakkı veren bir lisansı yok.

**Çözüm**

Kiracı yöneticisinin, ortamı oluşturan kullanıcıya geçerli bir Power Apps P2 lisansı atadığından emin olun. Aşağıdaki Microsoft Dynamics hizmet planları ortam oluşturma izni sağlar:

| Tüm ürün stok tutma birimi (SKU)       | Power Apps P2 servis planı  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps for Dynamics 365 |

Çeşitli Microsoft Office SKU'larının da bu hakkı, tek başına Power Apps Plan 2 SKU'larıyla birlikte tanıdığına dikkat edin. Buradaki önemli nokta bu SKU'lardan birinin mevcut olması zorunluluğudur.

1. [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments) gidin.
2. [İnsan Kaynakları sağlama](/dynamics365/unified-operations/talent/provisioning-talent) içindeki talimatları izleyerek ortamlar oluşturun.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
