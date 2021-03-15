---
title: Power Apps Yönetim merkezinde ortam oluşturulamıyor
description: Bu oknu, bir yönetici Microsoft Power Apps Yönetim merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.
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
ms.openlocfilehash: 664c644c9b34e3489b4134040e165d26202dbd38
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114593"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Power Apps Yönetim merkezinde ortam oluşturulamıyor

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
2. [İnsan Kaynakları sağlama](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) içindeki talimatları izleyerek ortamlar oluşturun.


[!INCLUDE[footer-include](../includes/footer-banner.md)]