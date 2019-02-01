---
title: "Kullanıcılar Core HR'a erişebilir ancak Onboard ve Attract uygulamasına erişemez"
description: "Bu konu, kullanıcının Microsoft Dynamics 365 for Talent Core HR'a erişebildiği ancak Attract veya Onboard'a erişemediği sorunu ortadan kaldırmayı anlatır."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: tr-tr
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>Kullanıcılar Core HR'a erişebilir ancak Onboard ve Attract uygulamasına erişemez

[!include [banner](includes/banner.md)]

**Ortam ayrıntıları**

- Microsoft Dynamics Lifecycle Services (LCS) dağıtımı kullanıcı A tarafından yapıldı.
- Kullanıcı A, kullanıcı B'yi Microsoft Dynamics 365 for Talent Core HR'a bir kullanıcı olarak ekledi.

**Stok çıkışı**

Kullanıcı B, Core HR'a erişebilmektedir ancak Talent: Attract veya Talent: Onboard uygulamasına erişememektedir. Kullanıcı **Deneyim uygulamalarına** gitmeyi denediğinde, deneme ortamına aktarılmaktadır.

**Çözüm**

Kullanıcı B, kullanıcı A'nın sağlama işlemi sırasında oluşturduğu Microsoft PowerApps ortamını görüntülemek için haklar atanmış olması gerekir.

Bilgi için, "Ortama erişim hakkı tanımak" bölümüne bkz. [Talent Sağlama](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

**Uzun vadeli çözüm**

Microsoft, Onboard ve Attract'a uygun hakları bir kullanıcı Core HR'a eklendiğinde otomatik olarak eklemeyi planlamaktadır.
