---
title: Attract kullanıcıları kariyer portalından iş başvurusunda bulunamıyor
description: Bu konu, kullanıcıların kariyer portalı 'ndan iş için uygulayabileceği bir sorunun nasıl giderileceğini açıklamaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462794"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Attract kullanıcıları kariyer portalından iş başvurusunda bulunamıyor

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Çıkış

Attract kullanıcıları kariyer portalından iş başvurusunda bulunamıyor. Dynamics 365 Talent: Attract'De oluşturulan bir iş için uygulamaya çalıştıklarında , tarayıcı sayfayı devamlı olarak yükler ve eylemi tamammaz.

## <a name="cause"></a>Nedeni

Bu sorun, Talent Relationship Ekibinin Talent kullanıcı rolü yoksa oluşur.

## <a name="resolution"></a>Çözünürlük

Talent Relationship Ekibine Talent kullanıcı atayın.

1. [Power Platform Yönetim Merkezi'nde](https://admin.powerplatform.microsoft.com) aşağıdaki yönetici kimlik bilgileriyle oturum açın:

   - Dynamics 365 Yöneticisi
   - Genel Yönetim
   - Power Platform yöneticisi

2. Gezinti bölmesinde, **ortamlar** 'ı seçin ve sonra taödünç verilen ilişki ekibine, Talent kullanıcı rolünün atanacağı ortamı seçin.

   ![Ortam Seç](./media/attract-troubleshoot-career-portal-select-environment.png)

3. **Ortamlar** bölmesinde, **ortam URL**'sini seçin ve ortamın yönetim portalında oturum açın (örneğin, https:<orgname>.crm.dynamics.com).

4. **Ayarlar**'ı seçin, **sistem**'i seçin ve sonra **güvenlik**'i seçin.

   ![Güvenliğe git](./media/attract-troubleshoot-career-portal-security.png)

5. **Takımları** seçin .

   ![Takımları seçin](./media/attract-troubleshoot-career-portal-security-teams.png)

6. Arama kutusunda **Talent Relationship ekibini** arayın ve sonra arama sonuçlarından takımı seçin.

7. Şeritten **ROLLERİ YÖNET** seçin.

8. **Takım Rollerini Yönet** iletişim kutusunda, kullanılabilir roller listesinden **Talent kullanıcısı**' yı seçin ve sonra rolü uygulamak için **Tamam**'ı seçin.

   ![Rolü Uygula](./media/attract-troubleshoot-career-portal-apply-role.png)

9. Değişikliklerinizi test edin:

   1. Yeni bir tarayıcı penceresinden kariyer portalı 'nda oturum açın.
   2. Kariyer portalından iş için geçerlidir. 