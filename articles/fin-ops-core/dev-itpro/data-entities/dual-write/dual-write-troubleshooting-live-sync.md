---
title: Canlı eşitleme sorunlarını giderme
description: Bu konu,canlı eşitlemeyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 82bdcc71196c22689cc65601f98187aaa9e5e9d6
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997314"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="bf210-103">Canlı eşitleme sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="bf210-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="bf210-104">Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="bf210-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="bf210-105">Bu konu,canlı eşitlemeyle ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="bf210-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf210-106">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="bf210-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="bf210-107">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bf210-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="bf210-108">Bir Finance and Operations uygulamasında kayıt oluşturduğunuzda, canlı eşitleme 403 Yasak bir hata oluşturur</span><span class="sxs-lookup"><span data-stu-id="bf210-108">Live synchronization throws a 403 Forbidden error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="bf210-109">Finance and Operations uygulamasında bir kayıt oluşturduğunuzda aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="bf210-109">You might receive the following error message when you create a record in a Finance and Operations app:</span></span>

<span data-ttu-id="bf210-110">*\[{\\"hata\\":{\\"kod\\":\\"0x80072560\\",\\"mesaj\\":\\"Kullanıcı kurumun bir üyesi değil.\\"}}\], Uzak sunucu hata gönderdi: (403) Yasak."}}".*</span><span class="sxs-lookup"><span data-stu-id="bf210-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="bf210-111">Bu sorunu gidermek için, [sistem gereksinimleri ve önkoşulları](requirements-and-prerequisites.md) adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="bf210-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="bf210-112">Bu adımları tamamlamak için, Common Data Service'de oluşturulan ikili yazma uygulaması kullanıcılarının sistem yöneticisi rolüne sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="bf210-112">To complete those steps, the dual-write application users who are created in Common Data Service must have the system admin role.</span></span> <span data-ttu-id="bf210-113">Varsayılan sahip olan takımın sistem yöneticisi rolü de olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bf210-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="bf210-114">Bir Finance and Operations uygulamasında kayıt oluşturduğunuzda, her varlık için canlı eşitleme benzer bir hata gönderir</span><span class="sxs-lookup"><span data-stu-id="bf210-114">Live synchronization for any entity consistently throws a similar error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="bf210-115">**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="bf210-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="bf210-116">Bir Finance and Operations uygulamadaki varlık verilerini her kaydetmeye çalıştığınızda aşağıdakine benzer bir hata iletisi alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="bf210-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="bf210-117">*Değişiklikler veritabanına kaydedilemiyor. İş birimi, hareketi kaydedemiyor. Veriler varlık uyglarına yazılamıyor. UnitOfMeasureEntity yazma işlemi hata iletisiyle başarısız oldu varlık uoms ile eşitlenemiyor.*</span><span class="sxs-lookup"><span data-stu-id="bf210-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="bf210-118">Bu sorunu gidermek için, önkoşul başvuru verilerinin her iki Finance and Operations uygulamada ve Common Data Service'te bulunduğundan emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bf210-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Common Data Service.</span></span> <span data-ttu-id="bf210-119">Örneğin, Finance and Operations uygulamanızda olduğunuz müşteri belirli bir müşteri grubuna aitse, müşteri grubunun Common Data Service'te bulunduğundan emin olun .</span><span class="sxs-lookup"><span data-stu-id="bf210-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Common Data Service.</span></span>

<span data-ttu-id="bf210-120">Her iki tarafta da veri varsa ve sorunun veriyle ilgili olmadığını doğrulamamışsanız, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bf210-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="bf210-121">İlgili varlığı durdurun.</span><span class="sxs-lookup"><span data-stu-id="bf210-121">Stop the related entity.</span></span>
2. <span data-ttu-id="bf210-122">Finance and Operations uygulamada oturum açın ve başarısız olan varlığın kayıtlarının DualWriteProjectConfiguration ve DualWriteProjectFieldConfiguration tablolarında var olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="bf210-122">Sign in to the Finance and Operations app, and make sure that records for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="bf210-123">Örneğin, **müşteriler** varlığı başarısız olduğunda sorgu şöyle görünür.</span><span class="sxs-lookup"><span data-stu-id="bf210-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="bf210-124">Varlık eşlemesini durdurduktan sonra bile başarısız olan varlık için kayıt varsa, başarısız olan varlıkla ilişkili kayıtları silin.</span><span class="sxs-lookup"><span data-stu-id="bf210-124">If there are records for the failing entity even after you stop the entity mapping, delete the records that are related to the failing entity.</span></span> <span data-ttu-id="bf210-125">DualWriteProjectConfiguration tablosundaki **ProjeAdı** sütununu not edin ve kaydı silmek için proje adını kullanarak kaydı DualWriteProjectFieldConfiguration tablosunda getirin.</span><span class="sxs-lookup"><span data-stu-id="bf210-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the record.</span></span>
4. <span data-ttu-id="bf210-126">Varlık eşlemesini Başlat.</span><span class="sxs-lookup"><span data-stu-id="bf210-126">Start the entity mapping.</span></span> <span data-ttu-id="bf210-127">Verilerin herhangi bir sorun olmadan eşitlenip eşitlenmediğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="bf210-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="bf210-128">Bir Finance and Operations uygulamada veri oluşturduğunuzda okuma veya yazma ayrıcalık hatalarını işleme</span><span class="sxs-lookup"><span data-stu-id="bf210-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="bf210-129">Bir Finance and Operations uygulamada veri oluşturduğunuzda, aşağıdaki örneğe benzer bir "Hatalı istek" hata iletisi alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf210-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Hatalı istek hata iletisi örneği](media/error_record_id_source.png)

<span data-ttu-id="bf210-131">Sorunu gidermek için, eksik ayrıcalığını etkinleştirmek amacıyla eşlenen Dynamics 365 Sales veya Dynamics 365 Customer Service departmanı ekibine doğru güvenlik rolünü atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bf210-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="bf210-132">Finance and Operations uygulamada, veri tümleştirme bağlantısı kümesinde eşlenen iş birimini bulun.</span><span class="sxs-lookup"><span data-stu-id="bf210-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organizasyon eşleme](media/mapped_business_unit.png)

2. <span data-ttu-id="bf210-134">Dynamics 365 model kullanan uygulamadaki ortama oturum açın, **Ayar \> Güvenlik** gidin ve eşlenen departmanın ekibini bulun.</span><span class="sxs-lookup"><span data-stu-id="bf210-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security** , and find the team of the mapped business unit.</span></span>

    ![Eşlenen departmanın ekibi](media/setting_security_page.png)

3. <span data-ttu-id="bf210-136">Düzenleme için takıma ait sayfayı açın ve sonra **takım rollerini Yönet** iletişim kutusunu açmak için **rolleri Yönet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bf210-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Rolleri Yönet düğmesi](media/manage_team_roles.png)

4. <span data-ttu-id="bf210-138">İlgili varlıklar için okuma/yazma ayrıcalığına sahip rolü atayın ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bf210-138">Assign the role that has the read/write privilege for the relevant entities, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a><span data-ttu-id="bf210-139">En son değiştirilen Common Data Service ortamı olan ortamlarda eşitleme sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="bf210-139">Fix synchronization issues in an environment that has a recently changed Common Data Service environment</span></span>

<span data-ttu-id="bf210-140">**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="bf210-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="bf210-141">Finance and Operations uygulamasında bir veri oluşturduğunuzda aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="bf210-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="bf210-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":" **CustCustomerV3Entity varlığı için yük oluşturulamıyor** ","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Geçersiz URI hatasıyla yük oluşturma başarısız oldu: URI boş."}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="bf210-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":" **Unable to generate payload for entity CustCustomerV3Entity** ","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="bf210-143">Burada, Dynamics 365'deki model kullanımlı uygulamasında hatanın nasıl göründüğü açıklanmaktadır:</span><span class="sxs-lookup"><span data-stu-id="bf210-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="bf210-144">*ISV kodundan beklenmeyen bir hata oluştu. (ErrorType = ClientError) Eklentiden beklenmeyen özel durum (Yürüt):  Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: varlık hesabı işlenemedi - (Bağlanılan taraf bir süre içinde doğru şekilde yanıt vermediğinden bir bağlantı girişimi başarısız oldu veya bağlanılan ana bilgisayar yanıt vermediğinden bağlantı kurulamadı*</span><span class="sxs-lookup"><span data-stu-id="bf210-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="bf210-145">Bu hata, Finance and Operations uygulamada veri oluşturmaya çalıştığınız sırada Common Data Service ortam yanlış sıfırlandığında oluşur.</span><span class="sxs-lookup"><span data-stu-id="bf210-145">This error occurs when the Common Data Service environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="bf210-146">Sorunu düzeltmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bf210-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="bf210-147">Finance and Operations sanal makinede (VM) oturum açın, SQL Server Management Studio'yu açın ( SSMS) ve DUALWRITEPROJECTCONFIGURATIONENTITY tablosundaki **internalentityname** , **Müşteriler V3** ve **externalentityname** **hesaplara** eşit olup olmadığına bakın.</span><span class="sxs-lookup"><span data-stu-id="bf210-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for records in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="bf210-148">Sorgu şöyle görünür.</span><span class="sxs-lookup"><span data-stu-id="bf210-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="bf210-149">Aşağıdaki sorguyu çalıştırmak için önceki sorgunun sonuçlarından proje adını kullanın.</span><span class="sxs-lookup"><span data-stu-id="bf210-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="bf210-150">**Externalenvironmenturl** sütununda doğru Common Data Service veya uygulama URL 'sinin bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="bf210-150">Make sure that the **externalenvironmentURL** column has the correct Common Data Service or app URL.</span></span> <span data-ttu-id="bf210-151">Yanlış Common Data Service URL 'yi işaret eden tüm yinelenen kayıtları silin.</span><span class="sxs-lookup"><span data-stu-id="bf210-151">Delete any duplicate records that point to the wrong Common Data Service URL.</span></span> <span data-ttu-id="bf210-152">Karşılık gelen DUALWRITEPROJECTFIELDCONFIGURATION ve DUALWRITEPROJECTCONFIGURATION tablolarını silin.</span><span class="sxs-lookup"><span data-stu-id="bf210-152">Delete the corresponding records in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="bf210-153">Varlık eşlemesini durdurun ve yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="bf210-153">Stop the entity mapping, and then restart it</span></span>
