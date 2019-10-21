---
title: Talent Microsoft Dynamics 365 uygulamaları (Common Data Service 1.0) arasında görünmüyor
description: Bu konu, bir müşteri Microsoft Dynamics 365 uygulamaları arasında Microsoft Dynamics 365 Talent'ı görmüyorsa ne yapılacağı açıklar.
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
ms.openlocfilehash: 956af80a8ab2f454d9f523d3c74dda754ef0f793
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009391"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talent Microsoft Dynamics 365 uygulamaları (Common Data Service 1.0) arasında görünmüyor

[!include [banner](includes/banner.md)]

**Çıkış**

Müşteri, Microsoft Dynamics 365 Talent uygulamasını Microsoft Dynamics 365 uygulamaları arasında göremez.

**Çözünürlük**

Kullanıcı, Microsoft PowerApps içinde Ortam Oluşturucu rolüne eklenmiş olmalıdır.

1. [PowerApps Yönetim portalını](https://preview.admin.powerapps.com/) PowerApps Plan 2 lisansına sahip yönetici kullanıcı açmalıdır.
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
