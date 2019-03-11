---
title: Talent, Microsoft Dynamics 365 uygulamaları (CDS1.0) arasında görünmüyor
description: Bu konu, bir müşteri Microsoft Dynamics 365 uygulamaları arasında Microsoft Dynamics 365 for Talent'ı görmüyorsa ne yapılacağı açıklar.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "306613"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>Talent, Microsoft Dynamics 365 uygulamaları (CDS1.0) arasında görünmüyor

[!include [banner](includes/banner.md)]

**Stok çıkışı**

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
