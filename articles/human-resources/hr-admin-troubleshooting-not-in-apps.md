---
title: İnsan Kaynakları Microsoft Dynamics 365 uygulamalarında görünmez
description: Bu konuda, Microsoft Dynamics 365 Human Resources uygulaması Microsoft Dynamics 365 uygulamaları arasında listelenmemişse ne yapılması gerektiği açıklanmaktadır.
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
ms.openlocfilehash: dfed82463eece882bed66c7b2dac1dd30e04720e
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413413"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources uygulaması Microsoft Dynamics 365 uygulamalarında görünmüyor

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
