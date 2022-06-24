---
title: İnsan Kaynakları Microsoft Dynamics 365 uygulamalarında görünmez
description: Bu makalede, Microsoft Dynamics 365 Human Resources Microsoft Dynamics 365 uygulamaları arasında listelenmemişse ne yapılması gerektiği açıklanmaktadır.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d520ac06bcc0990714929c0fdd622516eda5f30
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872253"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources uygulaması Microsoft Dynamics 365 uygulamalarında görünmüyor


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Sorun**

Müşteri, Dynamics 365 Human Resources'ı Microsoft Dynamics 365 uygulamaları arasında görünmüyor.

**Çözünürlük**

Kullanıcı, Microsoft Power Apps içinde Ortam Oluşturucu rolüne eklenmiş olmalıdır.

1. [Power Apps Yönetim portalını](https://preview.admin.powerapps.com/) Power Apps Plan 2 lisansına sahip yönetici kullanıcı açmalıdır.

2. **Ortamlar**'ı seçin ve İnsan Kaynakları için doğru ortamı seçin.

3. **Güvenlik** sekmesinde, **Ortam rolleri** sekmesinde **Ortam Oluşturucu**'yu seçin.

    ![Ortam rolleri sekmesi.](media/environment-roles.png)

4. **Kullanıcılar** sekmesinde, kullanıcıyı kuruluşunuza ekleyin.

    ![Kullanıcılar sekmesi.](media/environment-maker.png)

5. **Kaydet**'i seçin.

6. Kullanıcının şimdi [Microsoft Dynamics 365'e oturum açması gerekir](https://home.dynamics.com/).

7. Kullanıcı uygulamalarını güncelleştirmek için **Eşitle**'yi seçin.

    ![Eşitleme düğmesi.](media/get-more.png)

    Eşitleme tamamlandıktan sonra, İnsan Kaynakları ana sayfada görüntülenir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
