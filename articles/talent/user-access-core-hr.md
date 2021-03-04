---
title: Kullanıcı Human Resources'a erişebiliyor ancak Onboard veya Attract'a erişemiyor
description: Bu konu, kullanıcının Microsoft Dynamics 365 Talent - İnsan Kaynaklarına erişebildiği ancak Attract'e veya Onboard'a erişemediği sorunu ortadan kaldırmayı açıklamaktadır.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462811"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a>Kullanıcı Human Resources'a erişebiliyor ancak Onboard veya Attract'a erişemiyor

[!include [banner](includes/banner.md)]

**Ortam ayrıntıları**

- Microsoft Dynamics Lifecycle Services (LCS) dağıtımı kullanıcı A tarafından yapıldı.
- Kullanıcı A, kullanıcı B'yi Microsoft Dynamics 365 Human Resources'a bir kullanıcı olarak ekledi.

**Çıkış**

Kullanıcı B, İnsan Kaynakları'na erişebilmektedir ancak Talent: Attract veya Talent: Onboard uygulamasına erişememektedir. Kullanıcı **Deneyim uygulamalarına** gitmeyi denediğinde, deneme ortamına aktarılmaktadır.

**Çözüm**

Kullanıcı B, kullanıcı A'nın sağlama işlemi sırasında oluşturduğu Microsoft Power Apps ortamını görüntülemek için haklar atanmış olması gerekir.

Bilgi için, "Ortama erişim hakkı tanımak" bölümüne bkz. [Talent Sağlama](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Uzun vadeli çözüm**

Microsoft, Onboard ve Attract'e uygun hakları bir kullanıcı İnsan Kaynakları'na eklendiğinde otomatik olarak eklemeyi planlamaktadır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]