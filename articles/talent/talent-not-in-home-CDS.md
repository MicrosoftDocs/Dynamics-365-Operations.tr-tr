---
title: Talent Microsoft Dynamics 365 uygulamaları (Common Data Service 1.0) arasında görünmüyor
description: Bu konu, bir müşteri Microsoft Dynamics 365 uygulamaları arasında Microsoft Dynamics 365 for Talent'ı görmüyorsa ne yapılacağı açıklar.
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
ms.openlocfilehash: ad5add2b572ccb6bff175806b965f63b53986152
ms.sourcegitcommit: 45b79d1e587e03f5cde2766cdec4eaa7a2a897a3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2019
ms.locfileid: "949794"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talent Microsoft Dynamics 365 uygulamaları (Common Data Service 1.0) arasında görünmüyor

[!include [banner](includes/banner.md)]

**Çıkış**

Müşteri, Microsoft Dynamics 365 for Talent uygulamasını Microsoft Dynamics 365 uygulamaları arasında göremez.

**Çözünürlük**

Kullanıcı, Microsoft PowerApps içinde Ortam Oluşturucu rolüne eklenmiş olmalıdır.

1. PowerApps Plan 2 lisansına sahipi yönetici kullanıcı [PowerApps Yönetici portalını](https://preview.admin.powerapps.com/) açmalıdır.
2. **Ortamlar**'ı seçin ve Talent için doğru ortamı seçin.
3. **Güvenlik** sekmesinde, **Ortam rolleri** sekmesinde **Ortam Oluşturucu**'yu seçin.

    ![Ortam rolleri sekmesi](media/environment-roles.png)

4. **Kullanıcılar** sekmesinde, kullanıcıyı kuruluşunuza ekleyin.

    ![Kullanıcılar sekmesi](media/environment-maker.png)

5. **Kaydet**'i seçin.
6. Kullanıcının şimdi [Microsoft Dynamics 365'e oturum açması gerekir](https://home.dynamics.com/).
7. Kullanıcı uygulamalarını güncelleştirmek için **Eşitle**'yi seçin.

    ![Eşitleme düğmesi](media/get-more.png)

    Eşitleme tamamlandıktan sonra, Talent ana sayfada görüntülenir.
