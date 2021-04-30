---
title: Power Apps Yönetim merkezinde ortam oluşturulamıyor
description: Bu oknu, bir yönetici Microsoft Power Apps Yönetim merkezinde bir ortam oluşturamıyorsa ne yapılacağını anlatmaktadır.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 26a228229a09e74809a048675a3ff90025f2a26c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892239"
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