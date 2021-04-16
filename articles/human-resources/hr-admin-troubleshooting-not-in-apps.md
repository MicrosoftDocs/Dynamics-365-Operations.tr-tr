---
title: İnsan Kaynakları Microsoft Dynamics 365 uygulamalarında görünmez
description: Bu konu, bir müşteri Microsoft Dynamics 365 uygulamaları arasında Microsoft Dynamics 365 Human Resources'ı görmüyorsa ne yapılacağı açıklar.
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
ms.openlocfilehash: 658c6a4f17c022c3d0e3e49d16eb89624c4be27c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803981"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>İnsan Kaynakları Microsoft Dynamics 365 uygulamalarında görünmez

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Çıkış**

Müşteri, Dynamics 365 Human Resources'ı Microsoft Dynamics 365 uygulamaları arasında görünmüyor.

**Çözünürlük**

Kullanıcı, Microsoft Power Apps içinde Ortam Oluşturucu rolüne eklenmiş olmalıdır.

1. [Power Apps Yönetim portalını](https://preview.admin.powerapps.com/) Power Apps Plan 2 lisansına sahip yönetici kullanıcı açmalıdır.

2. **Ortamlar**'ı seçin ve İnsan Kaynakları için doğru ortamı seçin.

3. **Güvenlik** sekmesinde, **Ortam rolleri** sekmesinde **Ortam Oluşturucu**'yu seçin.

    ![Ortam rolleri sekmesi](media/environment-roles.png)

4. **Kullanıcılar** sekmesinde, kullanıcıyı kuruluşunuza ekleyin.

    ![Kullanıcılar sekmesi](media/environment-maker.png)

5. **Kaydet**'i seçin.

6. Kullanıcının şimdi [Microsoft Dynamics 365'e oturum açması gerekir](https://home.dynamics.com/).

7. Kullanıcı uygulamalarını güncelleştirmek için **Eşitle**'yi seçin.

    ![Eşitleme düğmesi](media/get-more.png)

    Eşitleme tamamlandıktan sonra, İnsan Kaynakları ana sayfada görüntülenir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]