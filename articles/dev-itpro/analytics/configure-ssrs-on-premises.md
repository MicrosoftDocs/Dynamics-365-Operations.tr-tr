---
title: "Şirket içi bir dağıtım için SQL Server Reporting Services'ı konfigüre etme"
description: "Bu konu, SQL Server Raporlama Servislerinin (SSRS) bir şirket içi dağıtım için yapılandırılması hakkında bilgi sağlar."
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a1f11641a2ec055cfaa0157ac9a40525daa4006
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a>Şirket içi bir dağıtım için SQL Server Reporting Services'ı konfigüre etme

Bu konudaki adımları, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (şirket içi) dağıtımınız için SQL Server Raporlama Servisleri'ni (SSRS) yapılandırmak için kullanın.

1. Raporlama Servisleri Yapılandırma Yöneticisi uygulamasını açın.
2. Geçerli makinenin adı olması gereken varsayılan **Sunucu adı**'nı ve **Sunucu Örneğini Raporla**, **MSSQLSERVER** bırakın. 
3. **Bağlan** üzerine tıklayın.
   
   [![Raporlama servisleri yapılandırma bağlantısı](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)
   
4. **Hizmet Hesabı** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.

    [![Servis hesabı sekmesi](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)
    
5. **Web Hizmet URL'si** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın. 

    [![Web hizmeti URL sekmesi](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png) 
    
6. **Veritabanı** sekmesine tıklayın ve **Veritabanı Adı** ve **Kimlik bilgisi ayarları**'nın aşağıdaki grafikle eşleştiğini doğrulayın. **Not:** Yeni bir veritabanı oluşturmanız gerekir. Bunu yapmak için **Veritabanıın Değiştir** üzerine tıklayın ve yeni veritabanı adının **DynamicsAxReportServer** olduğunu doğrulayın.

    [![veritabanı sekmesi](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)
    
7. **Web Portal URL'si** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın. **Not:** Portalı düzgün biçimde oluşturmak ve yapılandırmak için **Uygula**'yı tıklatın.

    [![web portal url sekmesi](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)
    
  Portal yapılandırıldıktan sonra, **Web Portalı** sekmesi aşağıdaki grafikle eşleşecektir.
    [![web portal url sekmesi](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)
    
8. SQL Server Raporlama Servisleri web portalını görüntülemek için raporlar URL'sini tıklatın. 
9.  Portaldayken, **Dynamics** adlı yeni bir klasör oluşturun.

    [![dynamics klasörü](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)
    
10. **Raporlama Servisleri Yapılandırma Yöneticisi** içerisinde, **E-posta Ayarları** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.

    [![e-posta ayarları sekmesi](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)
    
11. **Yürütme Hesabı** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.

    [![yürütme hesabı sekmesi](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)
    
  **Şifreleme Anahtarları** sekmesindeki varsayılan ayarları değiştirmeyin. [![şifreleme anahtarları sekmesi](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)
    
12. **Abonelik Ayarları** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.

    [![abonelik ayarları sekmesi](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)
    
  **Dağıtımı Ölçeklendir** sekmesindeki varsayılan ayarları değiştirmeyin. [![dağıtımı ölçeklendir sekmesi](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)
    
  **Power BI Tümleştirmesi** sekmesindeki varsayılan ayarları değiştirmeyin. [![power bi tümleştirme sekmesi](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png) 
    
13. **Raporlama Servisleri Yapılandırma Yöneticisi**'ni kapatmak için **Çıkış**'a tıklayın.

    [![raporlama servisi yapılandırma yöneticisini kapatın](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
    


