---
title: Kullanıcı Core HR'a erişebiliyor ancak Onboard'a veya Attract'e erişemiyor
description: Bu konu, kullanıcının Microsoft Dynamics 365 Talent - Core HR'a erişebildiği ancak Attract'e veya Onboard'a erişemediği sorunu ortadan kaldırmayı açıklamaktadır.
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
ms.openlocfilehash: 1a86936d756d8375761ce50c9d9bf33dc638dfad
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772931"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a>Kullanıcı Core HR'a erişebiliyor ancak Onboard'a veya Attract'e erişemiyor

[!include [banner](includes/banner.md)]

**Ortam ayrıntıları**

- Microsoft Dynamics Lifecycle Services (LCS) dağıtımı kullanıcı A tarafından yapıldı.
- Kullanıcı A, kullanıcı B'yi Microsoft Dynamics 365 Talent: Core HR'a bir kullanıcı olarak ekledi.

**Çıkış**

Kullanıcı B, Core HR'a erişebilmektedir ancak Talent: Attract veya Talent: Onboard uygulamasına erişememektedir. Kullanıcı **Deneyim uygulamalarına** gitmeyi denediğinde, deneme ortamına aktarılmaktadır.

**Çözüm**

Kullanıcı B, kullanıcı A'nın sağlama işlemi sırasında oluşturduğu Microsoft Power Apps ortamını görüntülemek için haklar atanmış olması gerekir.

Bilgi için, "Ortama erişim hakkı tanımak" bölümüne bkz. [Talent Sağlama](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Uzun vadeli çözüm**

Microsoft, Onboard ve Attract'e uygun hakları bir kullanıcı Core HR'a eklendiğinde otomatik olarak eklemeyi planlamaktadır.
