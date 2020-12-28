---
title: Şirket içi dağıtımlar için SQL Server Reporting Services'ı yapılandırma
description: Bu konu, SQL Server Raporlama Servislerinin (SSRS) bir şirket içi dağıtım için yapılandırılması hakkında bilgi sağlar.
author: PeterRFriis
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: perahlff
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 2577705b04beef1f8b03f83ed8536be2e6ab6e83
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683933"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a><span data-ttu-id="d2459-103">Şirket içi dağıtımlar için SQL Server Reporting Services'ı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d2459-103">Configure SQL Server Reporting Services for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2459-104">Bu konudaki adımları kullanarak SQL Server Reporting Services (SSRS) Microsoft Dynamics 365 Finance+ Operations (şirket içi) dağıtımınız için yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2459-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 Finance + Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="d2459-105">Raporlama Servisleri Yapılandırma Yöneticisi uygulamasını açın.</span><span class="sxs-lookup"><span data-stu-id="d2459-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="d2459-106">Geçerli makinenin adı olması gereken varsayılan **Sunucu adı**'nı ve **Sunucu Örneğini Raporla**, **MSSQLSERVER** bırakın.</span><span class="sxs-lookup"><span data-stu-id="d2459-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span>
3. <span data-ttu-id="d2459-107">**Bağlan** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d2459-107">Click **Connect**.</span></span>

    <span data-ttu-id="d2459-108">[![Raporlama servisleri yapılandırma bağlantısı](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>

4. <span data-ttu-id="d2459-109">**Hizmet Hesabı** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d2459-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="d2459-110">[![Servis hesabı sekmesi](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>

5. <span data-ttu-id="d2459-111">**Web Hizmet URL'si** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d2459-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="d2459-112">[![Web hizmeti URL sekmesi](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span>

6. <span data-ttu-id="d2459-113">**Veritabanı** sekmesine tıklayın ve **Veritabanı Adı** ve **Kimlik bilgisi ayarları**'nın aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d2459-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2459-114">Yeni bir veritabanı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d2459-114">You will need to create a new database.</span></span> <span data-ttu-id="d2459-115">Bunu yapmak için **Veritabanıın Değiştir** üzerine tıklayın ve yeni veritabanı adının **DynamicsAxReportServer** olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d2459-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="d2459-116">[![veritabanı sekmesi](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>

7. <span data-ttu-id="d2459-117">**Web Portal URL'si** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d2459-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2459-118">Portalı oluşturmak ve düzgün biçimde yapılandırmak için **Uygula**'yı tıklamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d2459-118">You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="d2459-119">[![web portal url sekmesi](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>

    <span data-ttu-id="d2459-120">Portal yapılandırıldıktan sonra, **Web Portalı** sekmesi aşağıdaki grafikle eşleşecektir.</span><span class="sxs-lookup"><span data-stu-id="d2459-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>

    <span data-ttu-id="d2459-121">[![web portal url sekmesi](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>

8. <span data-ttu-id="d2459-122">SQL Server Raporlama Servisleri web portalını görüntülemek için raporlar URL'sini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d2459-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span>
9. <span data-ttu-id="d2459-123">Portaldayken, **Dynamics** adlı yeni bir klasör oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d2459-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="d2459-124">[![dynamics klasörü](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>

10. <span data-ttu-id="d2459-125">**Raporlama Servisleri Yapılandırma Yöneticisi** içerisinde, **E-posta Ayarları** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d2459-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="d2459-126">[![e-posta ayarları sekmesi](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>

11. <span data-ttu-id="d2459-127">**Yürütme Hesabı** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d2459-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="d2459-128">[![yürütme hesabı sekmesi](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>

    <span data-ttu-id="d2459-129">**Şifreleme Anahtarları** sekmesindeki varsayılan ayarları değiştirmeyin.</span><span class="sxs-lookup"><span data-stu-id="d2459-129">Don't change the default settings on the **Encryption Keys** tab.</span></span>

    <span data-ttu-id="d2459-130">[![şifreleme anahtarları sekmesi](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-130">[![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>

12. <span data-ttu-id="d2459-131">**Abonelik Ayarları** sekmesine tıklayın ve ayarların aşağıdaki grafikle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d2459-131">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="d2459-132">[![abonelik ayarları sekmesi](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-132">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>

    <span data-ttu-id="d2459-133">**Dağıtımı Ölçeklendir** sekmesindeki varsayılan ayarları değiştirmeyin.</span><span class="sxs-lookup"><span data-stu-id="d2459-133">Don't change the default settings on the **Scale-out Deployment** tab.</span></span>

    <span data-ttu-id="d2459-134">[![dağıtımı ölçeklendir sekmesi](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-134">[![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>

    <span data-ttu-id="d2459-135">**Power BI tümleştirmesi** sekmesindeki varsayılan ayarları değiştirmeyin.</span><span class="sxs-lookup"><span data-stu-id="d2459-135">Don't change the default settings on the **Power BI Integration** tab.</span></span>

    <span data-ttu-id="d2459-136">[![power bi tümleştirme sekmesi](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-136">[![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span>

13. <span data-ttu-id="d2459-137">**Raporlama Servisleri Yapılandırma Yöneticisi**'ni kapatmak için **Çıkış**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d2459-137">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="d2459-138">[![raporlama servisi yapılandırma yöneticisini kapatın](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="d2459-138">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
