---
title: Şirket içi dağıtımlar için SQL Server Reporting Services'ı yapılandırma
description: Bu makalede, bir şirket içi dağıtım için SQL Server Reporting Services (SSRS) yapılandırması hakkında bilgi sağlanmaktadır.
author: PeterRFriis
ms.date: 06/23/2017
ms.topic: article
ms.prod: dynamics-365
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.custom: 55651
ms.assetid: ''
ms.service: ''
ms.openlocfilehash: 9acb681ce07c3a7da82a630c7a87a4271a411b51
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275606"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>Şirket içi dağıtımlar için SQL Server Reporting Services'ı yapılandırma

[!include [banner](../includes/banner.md)]

Bu makaledeki adımları kullanarak SQL Server Reporting Services'ı (SSRS) Microsoft Dynamics 365 Finance + Operations (on-premises) dağıtımınız için yapılandırabilirsiniz.

1. Raporlama Servisleri Yapılandırma Yöneticisi uygulamasını açın.
2. Geçerli makinenin adı olması gereken varsayılan **Sunucu adı**'nı ve **Sunucu Örneğini Raporla**, **MSSQLSERVER** bırakın.
3. **Bağlan** üzerine tıklayın.

    [![Raporlama servisleri yapılandırma bağlantısı.](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. **Hizmet Hesabı** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.

    [![Servis hesabı sekmesi.](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. **Web Hizmet URL'si** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.

    [![Web hizmeti URL sekmesi.](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. **Veritabanı** sekmesine tıklayın ve **Veritabanı Adı** ve **Kimlik bilgisi ayarları**'nın aşağıdaki grafikle eşleştiğini doğrulayın.

    > [!NOTE]
    > Yeni bir veritabanı oluşturmanız gerekir. Bunu yapmak için **Veritabanıın Değiştir** üzerine tıklayın ve yeni veritabanı adının **DynamicsAxReportServer** olduğunu doğrulayın.

    [![veritabanı sekmesi.](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. **Web Portal URL'si** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.

    > [!NOTE]
    > Portalı oluşturmak ve düzgün biçimde yapılandırmak için **Uygula**'yı tıklamanız gerekir.

    [![web portal url sekmesi.](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    Portal yapılandırıldıktan sonra, **Web Portalı** sekmesi aşağıdaki grafikle eşleşecektir.

    [![web portal url sekmesi.](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. SQL Server Raporlama Servisleri web portalını görüntülemek için raporlar URL'sini tıklatın.
9. Portaldayken, **Dynamics** adlı yeni bir klasör oluşturun.

    [![dynamics klasörü.](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. **Raporlama Servisleri Yapılandırma Yöneticisi** içerisinde, **E-posta Ayarları** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.

    [![e-posta ayarları sekmesi.](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. **Yürütme Hesabı** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.

    [![yürütme hesabı sekmesi.](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    **Şifreleme Anahtarları** sekmesindeki varsayılan ayarları değiştirmeyin.

    [![şifreleme anahtarları sekmesi.](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. **Abonelik Ayarları** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.

    [![abonelik ayarları sekmesi.](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    **Dağıtımı Ölçeklendir** sekmesindeki varsayılan ayarları değiştirmeyin.

    [![dağıtımı ölçeklendir sekmesi.](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    **Power BI tümleştirmesi** sekmesindeki varsayılan ayarları değiştirmeyin.

    [![power bi tümleştirme sekmesi.](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. **Raporlama Servisleri Yapılandırma Yöneticisi**'ni kapatmak için **Çıkış**'a tıklayın.

    [![raporlama servisi yapılandırma yöneticisini kapatma.](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
