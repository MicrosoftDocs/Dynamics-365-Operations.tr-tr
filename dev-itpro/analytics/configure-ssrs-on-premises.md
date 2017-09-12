---
title: "Şirket içi bir dağıtım için SQL Server Reporting Services'ı konfigüre etme"
description: "Bu konu, SQL Server Raporlama Servislerinin (SSRS) bir şirket içi dağıtım için yapılandırılması hakkında bilgi sağlar."
author: kfend
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, UnifiedOperations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanisathish
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: b0bfaadabe960f31d7609512b7ad6eaf848afddc
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a><span data-ttu-id="3f7d1-103">Şirket içi bir dağıtım için SQL Server Reporting Services'ı konfigüre etme</span><span class="sxs-lookup"><span data-stu-id="3f7d1-103">Configure SQL Server Reporting Services for an on-premises deployment</span></span>

<span data-ttu-id="3f7d1-104">Bu konudaki adımları, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (şirket içi) dağıtımınız için SQL Server Raporlama Servisleri'ni (SSRS) yapılandırmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises) deployment.</span></span>

1. <span data-ttu-id="3f7d1-105">Raporlama Servisleri Yapılandırma Yöneticisi uygulamasını açın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="3f7d1-106">Geçerli makinenin adı olması gereken varsayılan **Sunucu adı**'nı ve **Sunucu Örneğini Raporla**, **MSSQLSERVER** bırakın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span> 
3. <span data-ttu-id="3f7d1-107">**Bağlan** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-107">Click **Connect**.</span></span>
   
   <span data-ttu-id="3f7d1-108">[![Raporlama servisleri yapılandırma bağlantısı](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>
   
4. <span data-ttu-id="3f7d1-109">**Hizmet Hesabı** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="3f7d1-110">[![Servis hesabı sekmesi](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>
    
5. <span data-ttu-id="3f7d1-111">**Web Hizmet URL'si** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span> 

    <span data-ttu-id="3f7d1-112">[![Web hizmeti URL sekmesi](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span> 
    
6. <span data-ttu-id="3f7d1-113">**Veritabanı** sekmesine tıklayın ve **Veritabanı Adı** ve **Kimlik bilgisi ayarları**'nın aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span> <span data-ttu-id="3f7d1-114">**Not:** Yeni bir veritabanı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-114">**Note:** You will need to create a new database.</span></span> <span data-ttu-id="3f7d1-115">Bunu yapmak için **Veritabanıın Değiştir** üzerine tıklayın ve yeni veritabanı adının **DynamicsAxReportServer** olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="3f7d1-116">[![veritabanı sekmesi](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>
    
7. <span data-ttu-id="3f7d1-117">**Web Portal URL'si** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span> <span data-ttu-id="3f7d1-118">**Not:** Portalı düzgün biçimde oluşturmak ve yapılandırmak için **Uygula**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-118">**Note:** You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="3f7d1-119">[![web portal url sekmesi](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>
    
  <span data-ttu-id="3f7d1-120">Portal yapılandırıldıktan sonra, **Web Portalı** sekmesi aşağıdaki grafikle eşleşecektir.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>
    <span data-ttu-id="3f7d1-121">[![web portal url sekmesi](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>
    
8. <span data-ttu-id="3f7d1-122">SQL Server Raporlama Servisleri web portalını görüntülemek için raporlar URL'sini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span> 
9.  <span data-ttu-id="3f7d1-123">Portaldayken, **Dynamics** adlı yeni bir klasör oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="3f7d1-124">[![dynamics klasörü](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>
    
10. <span data-ttu-id="3f7d1-125">**Raporlama Servisleri Yapılandırma Yöneticisi** içerisinde, **E-posta Ayarları** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="3f7d1-126">[![e-posta ayarları sekmesi](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>
    
11. <span data-ttu-id="3f7d1-127">**Yürütme Hesabı** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="3f7d1-128">[![yürütme hesabı sekmesi](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>
    
  <span data-ttu-id="3f7d1-129">**Şifreleme Anahtarları** sekmesindeki varsayılan ayarları değiştirmeyin.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-129">Don’t change the default settings on the **Encryption Keys** tab.</span></span>
    <span data-ttu-id="3f7d1-130">[![şifreleme anahtarları sekmesi](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-130">[![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>
    
12. <span data-ttu-id="3f7d1-131">**Abonelik Ayarları** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-131">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="3f7d1-132">[![abonelik ayarları sekmesi](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-132">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>
    
  <span data-ttu-id="3f7d1-133">**Dağıtımı Ölçeklendir** sekmesindeki varsayılan ayarları değiştirmeyin.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-133">Don’t change the default settings on the **Scale-out Deployment** tab.</span></span>
    <span data-ttu-id="3f7d1-134">[![dağıtımı ölçeklendir sekmesi](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-134">[![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>
    
  <span data-ttu-id="3f7d1-135">**Power BI Tümleştirmesi** sekmesindeki varsayılan ayarları değiştirmeyin.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-135">Don’t change the default settings on the **Power BI Integration** tab.</span></span>
    <span data-ttu-id="3f7d1-136">[![power bi tümleştirme sekmesi](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-136">[![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span> 
    
13. <span data-ttu-id="3f7d1-137">**Raporlama Servisleri Yapılandırma Yöneticisi**'ni kapatmak için **Çıkış**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3f7d1-137">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="3f7d1-138">[![raporlama servisi yapılandırma yöneticisini kapatın](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="3f7d1-138">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
    


