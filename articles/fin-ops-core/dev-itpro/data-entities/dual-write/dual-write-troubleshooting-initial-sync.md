---
title: Başlangıç eşitlemesi sırasında sorunları giderme
description: Bu konu, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410093"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="049a8-103">Başlangıç eşitlemesi sırasında sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="049a8-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="049a8-104">Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="049a8-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="049a8-105">Bu konu, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="049a8-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="049a8-106">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="049a8-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="049a8-107">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="049a8-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="049a8-108">Finance and Operations uygulamadaki ilk eşitleme hatalarını denetle</span><span class="sxs-lookup"><span data-stu-id="049a8-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="049a8-109">Eşleme şablonları etkinleştirildikten sonra, haritaların durumu **çalışıyor** olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="049a8-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="049a8-110">Durum **çalışmıyorsa**, ilk eşitleme sırasında hata meydana geldi.</span><span class="sxs-lookup"><span data-stu-id="049a8-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="049a8-111">Hataları görüntülemek için **çift-yazma** sayfasında **ilk eşitleme ayrıntıları** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="049a8-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![İlk eşitleme Ayrıntıları sekmesi](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="049a8-113">İlk eşitlemeyi tamamlayamıyoruz: 400 Hatalı Istek</span><span class="sxs-lookup"><span data-stu-id="049a8-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="049a8-114">**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="049a8-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="049a8-115">Eşlemeyi ve ilk senkronizasyonu çalıştırmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="049a8-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="049a8-116">*Uzak sunucu hata verdi: (400) hatalı Istek.), AX dışarı aktarma bir hatayla karşılaştı*</span><span class="sxs-lookup"><span data-stu-id="049a8-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="049a8-117">Burada tam hata mesajı tablosu için bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="049a8-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="049a8-118">Bu hata sürekli olarak oluşuyorsa ve ilk eşitlemeyi tamamlayamıyorsa, sorunu düzeltmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="049a8-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="049a8-119">Finance and Operations uygulamanın sanal makinesine (VM) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="049a8-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="049a8-120">Microsoft Yönetim Konsolu 'Nu açın.</span><span class="sxs-lookup"><span data-stu-id="049a8-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="049a8-121">**Hizmetler** bölmesinde, Microsoft Dynamics 365 veri alma verme çerçevesi hizmetinin çalışmakta olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="049a8-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="049a8-122">Durdurulmuşsa, ilk eşitleme gerektirdiğinden yeniden Başlat.</span><span class="sxs-lookup"><span data-stu-id="049a8-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="049a8-123">İlk eşitleme hatası: 403 Yasak</span><span class="sxs-lookup"><span data-stu-id="049a8-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="049a8-124">İlk eşitlemede aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="049a8-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="049a8-125">*(\[Yasak\], Uzak sunucu hata verdi: (403) Yasak), AX dışarı aktarma bir hatayla karşılaştı*</span><span class="sxs-lookup"><span data-stu-id="049a8-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="049a8-126">Sorunu düzeltmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="049a8-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="049a8-127">Finance and Operations Uygulamaya oturum açın.</span><span class="sxs-lookup"><span data-stu-id="049a8-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="049a8-128">**Azure Active Directory uygulamalar** sayfasında **DtAppID** istemcisini silin ve sonra yeniden ekleyin.</span><span class="sxs-lookup"><span data-stu-id="049a8-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD uygulamalar listesi](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="049a8-130">İlk eşitleme sırasında kendi kendine referans veya döngüsel referans hataları</span><span class="sxs-lookup"><span data-stu-id="049a8-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="049a8-131">Eşlemelerinizin kendi kendine veya çevresel referansları varsa, aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="049a8-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="049a8-132">Hatalar aşağıdaki kategorilere ayrılır:</span><span class="sxs-lookup"><span data-stu-id="049a8-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="049a8-133">Satıcılar V2 ve msdyn_vendors varlık eşlemesi</span><span class="sxs-lookup"><span data-stu-id="049a8-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="049a8-134">Müşteriler V3 ile Firmalar varlık eşlemesi</span><span class="sxs-lookup"><span data-stu-id="049a8-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="049a8-135">Varlık eşleştirmesini msdyn_vendors üzere Satıcılar V2'deki bir hatayı giderme</span><span class="sxs-lookup"><span data-stu-id="049a8-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="049a8-136">Varlıkların, **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** alanlarında değerleri bulunan mevcut kayıtları varsa **msdyn_vendors** eşlemeyi yapmak için **satıcı v2** üzerinde aşağıdaki ilk eşitleme hatalarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="049a8-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="049a8-137">Bu **InvoiceVendorAccountNumber**, kendine referans bir alan olduğundan ve **PrimaryContactPersonId** satıcı eşlemesindeki bir döngüsel başvurudur.</span><span class="sxs-lookup"><span data-stu-id="049a8-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="049a8-138">*Alan için GUID çözümlenemedi:<field>. Arama bulunamadı: <value>Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="049a8-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="049a8-139">İşte birkaç örnek:</span><span class="sxs-lookup"><span data-stu-id="049a8-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="049a8-140">*Şu alan için GUID çözülemedi: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Arama bulunamadı: 000056. Başvuru verilerinin var olup olmadığını denetlemek için bu URL 'yi deneyin: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="049a8-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="049a8-141">*Şu alan için GUID çözülemedi: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Arama bulunamadı: V24-1. Başvuru verilerinin var olup olmadığını denetlemek için bu URL 'yi deneyin: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span><span class="sxs-lookup"><span data-stu-id="049a8-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="049a8-142">Satıcı varlığındaki bu alanlardaki değerleri bulunan kayıtlarınız varsa, ilk eşitlemeyi başarıyla tamamlamak için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="049a8-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="049a8-143">Finance and Operations uygulamada, eşlemeden önce **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** alanlarını silin ve değişiklikleri kaydedin.</span><span class="sxs-lookup"><span data-stu-id="049a8-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="049a8-144">Satıcılar v2 (msdyn_vendors) için ikili yazma eşleme sayfasına gidin **Vendors V2 (msdyn_vendors)** ve **varlık eşleştirmeleri** sekmesini seçin. Sol filtrede, **Finance and Operations uygulamaları. Satıcıları sürüm 2** seçin.</span><span class="sxs-lookup"><span data-stu-id="049a8-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="049a8-145">Sağ filtrede, **Sales.Vendor**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="049a8-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="049a8-146">**primarycontactperson**'ı arayıp **PrimaryContactPersonId** kaynak alanını bulur .</span><span class="sxs-lookup"><span data-stu-id="049a8-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="049a8-147">**Eylemler** düğmesine tıklayın ve **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="049a8-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![kendinden veya dairesel referans 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="049a8-149">**InvoiceVendorAccountNumber** alanını silmek için tekrarlayın .</span><span class="sxs-lookup"><span data-stu-id="049a8-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![kendinden veya dairesel referans 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="049a8-151">Eşleme değişikliklerini kaydedin.</span><span class="sxs-lookup"><span data-stu-id="049a8-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="049a8-152">**Vendors V2** varlığı için değişiklik izlemeyi devre dışı bırakın .</span><span class="sxs-lookup"><span data-stu-id="049a8-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="049a8-153">**Veri yönetimi \> veri varlıklarına** gidin .</span><span class="sxs-lookup"><span data-stu-id="049a8-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="049a8-154">**Satıcılar V2** tüzel kişiliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="049a8-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="049a8-155">Menü çubuğundan **seçenekler**'i tıklatın ve sonra **izlemeyi değiştirin**.</span><span class="sxs-lookup"><span data-stu-id="049a8-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![kendinden veya dairesel referans 5](media/selfref_options.png)
    
    4. <span data-ttu-id="049a8-157">**Değişiklik izlemeyi devre dışı bırak**'ı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049a8-157">Click **Disable Change Tracking**.</span></span>
    
        ![kendinden veya dairesel referans 6](media/selfref_tracking.png)

3. <span data-ttu-id="049a8-159">**Satıcı v2 (msdyn_vendors)** eşlemesinin ilk eşitlemesini çalıştırın .</span><span class="sxs-lookup"><span data-stu-id="049a8-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="049a8-160">İlk eşitleme hatasız olarak çalışmalıdır.</span><span class="sxs-lookup"><span data-stu-id="049a8-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="049a8-161">**CD kişilerinin v2 (kişiler)** eşlemesi için başlangıç eşitlemesini çalıştırın .</span><span class="sxs-lookup"><span data-stu-id="049a8-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="049a8-162">İlgili kişi kayıtlarının de ilk eşitlenmesi gerektiğinde, satıcı varlığındaki birincil ilgili kişi alanını eşitlemek istiyorsanız bu eşlemeyi eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="049a8-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="049a8-163">**PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** alanlarını **satıcı v2 (msdyn_vendors)** eşleme alanlarına geri ekleyin ve eşlemeyi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="049a8-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="049a8-164">**Satıcı v2 (msdyn_vendors)** eşlemesinin ilk eşitlemesini çalıştırın .</span><span class="sxs-lookup"><span data-stu-id="049a8-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="049a8-165">Değişiklik izleme devre dışı bırakıldığından tüm kayıtlar eşitlenecek.</span><span class="sxs-lookup"><span data-stu-id="049a8-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="049a8-166">**Vendors V2** varlığı için değişiklik izlemeyi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="049a8-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="049a8-167">Müşteriler V3 ile Firmalar varlık eşleme müşterilerine hata giderme</span><span class="sxs-lookup"><span data-stu-id="049a8-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="049a8-168">Varlıkların, **ContactPersonID** ve **InvoiceAccount** alanlarında değerleri bulunan mevcut kayıtları varsa **Firmalar** eşlemeyi yapmak için **Müşteriler v3** üzerinde aşağıdaki ilk eşitleme hatalarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="049a8-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="049a8-169">Bu **InvoiceAccount**, kendine referans bir alan olduğundan ve **ContactPersonID** satıcı eşlemesindeki bir döngüsel başvurudur.</span><span class="sxs-lookup"><span data-stu-id="049a8-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="049a8-170">*Alan için GUID çözümlenemedi:<field>. Arama bulunamadı: <value>Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="049a8-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="049a8-171">*Şu alan için GUID çözülemedi: primarycontactid.msdyn_contactpersonid. Arama bulunamadı: 000056. Başvuru verilerinin var olup olmadığını denetlemek için bu URL 'yi deneyin: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="049a8-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="049a8-172">*Şu alan için GUID çözülemedi: msdyn_billingaccount.accountnumber. Arama bulunamadı: 1206-1. Başvuru verilerinin var olup olmadığını denetlemek için bu URL 'yi deneyin: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span><span class="sxs-lookup"><span data-stu-id="049a8-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="049a8-173">Müşteri varlığındaki bu alanlardaki değerleri bulunan kayıtlarınız varsa, ilk eşitlemeyi başarıyla tamamlamak için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="049a8-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="049a8-174">Bu yaklaşımı, firma ve Ilgili kişiler gibi, kutudan çıkan herhangi bir varlık için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="049a8-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="049a8-175">Finance and Operations uygulamada, **Müşteriler V3 (firmalar)** eşlemesinden önce **ContactPersonID** ve **InvoiceAccount** alanlarını silin ve değişiklikleri kaydedin.</span><span class="sxs-lookup"><span data-stu-id="049a8-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="049a8-176">**Müşteriler V3 (firmalar)** için ikili yazma eşleme sayfasına gidin, **varlık eşleştirmeleri** sekmesini seçin. Sol filtrede, **Finance and Operations uygulamaları.Müşteriler sürüm 2** seçin.</span><span class="sxs-lookup"><span data-stu-id="049a8-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="049a8-177">Sağ filtrede, **Common Data Service.Firma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="049a8-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="049a8-178">**contactperson**'ı arayıp **ContactPersonID** kaynak alanını bulur .</span><span class="sxs-lookup"><span data-stu-id="049a8-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="049a8-179">**Eylemler** düğmesine tıklayın ve **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="049a8-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![kendinden veya dairesel referans 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="049a8-181">**InvoiceAccount** alanını silmek için tekrarlayın .</span><span class="sxs-lookup"><span data-stu-id="049a8-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![kendinden veya dairesel referans](media/cust_selfref4.png)
    
    5. <span data-ttu-id="049a8-183">Eşleme değişikliklerini kaydedin.</span><span class="sxs-lookup"><span data-stu-id="049a8-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="049a8-184">**Müşteriler V3** varlığı için değişiklik izlemeyi devre dışı bırakın .</span><span class="sxs-lookup"><span data-stu-id="049a8-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="049a8-185">**Veri yönetimi \> veri varlıklarına** gidin .</span><span class="sxs-lookup"><span data-stu-id="049a8-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="049a8-186">**Müşteriler V3** tüzel kişiliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="049a8-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="049a8-187">Menü çubuğundan **seçenekler**'i tıklatın ve sonra **izlemeyi değiştirin**.</span><span class="sxs-lookup"><span data-stu-id="049a8-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![kendinden veya dairesel referans 5](media/selfref_options.png)
    
    4. <span data-ttu-id="049a8-189">**Değişiklik izlemeyi devre dışı bırak**'ı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="049a8-189">Click **Disable Change Tracking**.</span></span>
    
        ![kendinden veya dairesel referans 6](media/selfref_tracking.png)

3. <span data-ttu-id="049a8-191">**Müşteriler V3 (Firmalar)** eşlemesi için başlangıç eşitlemesini çalıştırın .</span><span class="sxs-lookup"><span data-stu-id="049a8-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="049a8-192">İlk eşitleme hatasız olarak çalışmalıdır.</span><span class="sxs-lookup"><span data-stu-id="049a8-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="049a8-193">**CD kişilerinin v2 (kişiler)** eşlemesi için başlangıç eşitlemesini çalıştırın .</span><span class="sxs-lookup"><span data-stu-id="049a8-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="049a8-194">Aynı adda 2 eşleme var.</span><span class="sxs-lookup"><span data-stu-id="049a8-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="049a8-195">**FO.CDS Vendor Contacts V2 ve CDS.Contacts arasında eşitleme için çift yazma şablonu. yeni paket gerekli \[Dynamics365SupplyChainExtended\].** açıklaması olanı seçin.</span><span class="sxs-lookup"><span data-stu-id="049a8-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="049a8-196">Haritanın **Ayrıntılar** sekmesinde yapın.</span><span class="sxs-lookup"><span data-stu-id="049a8-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="049a8-197">**Müşteriler V3 (firmalar)** eşlemesinden önce **ContactPersonID** ve **InvoiceAccount** alanlarını silin ve değişiklikleri kaydedin.</span><span class="sxs-lookup"><span data-stu-id="049a8-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="049a8-198">Şimdi, hem **InvoiceAccount** alanını hem de **ContactPersonId** alanı canlı eşitleme modunun parçası olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="049a8-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="049a8-199">Sonraki adımda, bu alanlar için başlangıç eşitlemesini tamamdınız.</span><span class="sxs-lookup"><span data-stu-id="049a8-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="049a8-200">**Müşteriler V3 (Firmalar)** eşlemesi için başlangıç eşitlemesini çalıştırın .</span><span class="sxs-lookup"><span data-stu-id="049a8-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="049a8-201">Değişiklik izleme devre dışı bırakıldığından, Finance and Operations uygulamasından Common Data Service'e eşitleme çalıştırmak **InvoiceAccount** ve **ContactPersonId** verilerini uygulamadan eşitler.</span><span class="sxs-lookup"><span data-stu-id="049a8-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="049a8-202">**InvoiceAccount** ve **ContactPersonId** için verileri Common Data Service'dan Finance and Operations'a eşitlemek için bir veri tümleştirme projesi kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="049a8-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="049a8-203">Power Apps içinde , **Satış. firma** ve **Finance and Operations uygulamalar.Müşteriler V3** varlıkları arasında veri entegrasyonu projesi oluşturunuygulamalar arasında bir veri tümleştirme projesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="049a8-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="049a8-204">Veri yönü, Common Data Service'ten Finance and Operations uygulamasına olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="049a8-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="049a8-205">**InvoiceAccount** çift-yazılabilir olarak yeni bir öznitelik olduğundan, bu öznitelik için ilk eşitlemeyi atlamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="049a8-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="049a8-206">Daha fazla bilgi için bkz. [Common Data Service'e veri entegre edin](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="049a8-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="049a8-207">Aşağıdaki resimde **CustomerAccount** ve **ContactPersonId**'yi güncelleştiren bir proje gösterilmektedir .</span><span class="sxs-lookup"><span data-stu-id="049a8-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![kendinden veya dairesel referans](media/cust_selfref6.png)

    2. <span data-ttu-id="049a8-209">Finance and Operations Uygulamasında, filtre ölçütleriyle eşleşen kayıtlar güncelleştirilecek şekilde şirket ölçütlerini Common Data Service kenarına ekleyin.</span><span class="sxs-lookup"><span data-stu-id="049a8-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="049a8-210">Filtre eklemek için filtre simgesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="049a8-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="049a8-211">**Sorgu düzenle** iletişim kutusunda, **_msdyn_company_value eq '\<guid\>** gibi bir filtre sorgusu ekleyebilirsiniz .</span><span class="sxs-lookup"><span data-stu-id="049a8-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="049a8-212">Filtre simgesi yoksa, veri tümleştirme ekibinin kiracınızda filtre yeteneğini etkinleştirmesini istemek için bir destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="049a8-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="049a8-213">**_Msdyn_company_value** için bir filtre sorgusu girmezseniz , tüm kayıtlar eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="049a8-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![kendinden veya dairesel referans](media/cust_selfref7.png)

        <span data-ttu-id="049a8-215">Böylece, kayıtların ilk eşitlenmesi tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="049a8-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="049a8-216">Finance and Operations uygulamasında **Müşteriler V3** varlığı için değişiklik izlemeyi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="049a8-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

