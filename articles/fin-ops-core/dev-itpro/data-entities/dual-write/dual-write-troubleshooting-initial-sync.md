---
title: Başlangıç eşitlemesi sırasında sorunları giderme
description: Bu konu, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8aa7d156d0f0dad921b5c0aceec941295950b308
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566849"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="f9d4e-103">Başlangıç eşitlemesi sırasında sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="f9d4e-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f9d4e-104">Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="f9d4e-105">Bu konu, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9d4e-106">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="f9d4e-107">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="f9d4e-108">Finance and Operations uygulamadaki ilk eşitleme hatalarını denetle</span><span class="sxs-lookup"><span data-stu-id="f9d4e-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="f9d4e-109">Eşleme şablonları etkinleştirildikten sonra, haritaların durumu **çalışıyor** olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="f9d4e-110">Durum **çalışmıyorsa**, ilk eşitleme sırasında hata meydana geldi.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="f9d4e-111">Hataları görüntülemek için **çift-yazma** sayfasında **ilk eşitleme ayrıntıları** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![İlk eşitleme ayrıntıları sekmesinde hata](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="f9d4e-113">İlk eşitlemeyi tamamlayamıyoruz: 400 Hatalı Istek</span><span class="sxs-lookup"><span data-stu-id="f9d4e-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="f9d4e-114">**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="f9d4e-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="f9d4e-115">Eşlemeyi ve ilk senkronizasyonu çalıştırmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="f9d4e-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="f9d4e-116">*(\[Hatalı İstek\], Uzak sunucu hata verdi: (400) Hatalı İstek.), AX dışarı aktarma işlemi bir hatayla karşılaştı*</span><span class="sxs-lookup"><span data-stu-id="f9d4e-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="f9d4e-117">Burada tam hata mesajı tablosu için bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="f9d4e-118">Bu hata sürekli olarak oluşuyorsa ve ilk eşitlemeyi tamamlayamıyorsa, sorunu düzeltmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="f9d4e-119">Finance and Operations uygulamanın sanal makinesine (VM) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="f9d4e-120">Microsoft Yönetim Konsolu 'Nu açın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="f9d4e-121">**Hizmetler** bölmesinde, Microsoft Dynamics 365 veri alma verme çerçevesi hizmetinin çalışmakta olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="f9d4e-122">Durdurulmuşsa, ilk eşitleme gerektirdiğinden yeniden Başlat.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="f9d4e-123">İlk eşitleme hatası: 403 Yasak</span><span class="sxs-lookup"><span data-stu-id="f9d4e-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="f9d4e-124">İlk eşitlemede aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="f9d4e-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="f9d4e-125">*(\[Yasak\], Uzak sunucu hata verdi: (403) Yasak), AX dışarı aktarma bir hatayla karşılaştı*</span><span class="sxs-lookup"><span data-stu-id="f9d4e-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="f9d4e-126">Sorunu düzeltmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="f9d4e-127">Finance and Operations Uygulamaya oturum açın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="f9d4e-128">**Azure Active Directory uygulamalar** sayfasında **DtAppID** istemcisini silin ve sonra yeniden ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD uygulamaları listesinde DtAppID istemcisi](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="f9d4e-130">İlk eşitleme sırasında kendi kendine referans veya döngüsel referans hataları</span><span class="sxs-lookup"><span data-stu-id="f9d4e-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="f9d4e-131">Eşlemelerinizin kendi kendine veya çevresel referansları varsa, aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="f9d4e-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="f9d4e-132">Hatalar aşağıdaki kategorilere ayrılır:</span><span class="sxs-lookup"><span data-stu-id="f9d4e-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="f9d4e-133">Vendors V2–to–msdyn_vendors tablo eşlemesinde hatalar</span><span class="sxs-lookup"><span data-stu-id="f9d4e-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="f9d4e-134">Customers V3–to–Accounts tablo eşlemesinde hatalar</span><span class="sxs-lookup"><span data-stu-id="f9d4e-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="f9d4e-135">Vendors V2–to–msdyn_vendors tablo eşlemesinde hataları çözümleme</span><span class="sxs-lookup"><span data-stu-id="f9d4e-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="f9d4e-136">Tabloların, **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** sütunlarında değerleri bulunan mevcut satırları varsa **Satıcılar V2** ile **msdyn\_vendors** eşlemesinde ilk eşitleme hatalarıyla karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns.</span></span> <span data-ttu-id="f9d4e-137">Bu hatalar **InvoiceVendorAccountNumber** kendi kendine başvuran bir sütun olduğundan ve **PrimaryContactPersonId**, satıcı eşlemede döngüsel bir başvuru olduğundan gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing column, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="f9d4e-138">Aldığınız hata iletileri aşağıdaki şekilde olacaktır.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="f9d4e-139">*Alan için GUID çözümlenemedi: \<field\>. Arama bulunamadı: \<value\>. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="f9d4e-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="f9d4e-140">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="f9d4e-140">Here are some examples:</span></span>

- <span data-ttu-id="f9d4e-141">*Alan için GUID çözümlenemedi: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Arama bulunamadı: 000056. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="f9d4e-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="f9d4e-142">*Alan için GUID çözümlenemedi: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Arama bulunamadı: V24-1. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="f9d4e-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="f9d4e-143">Satıcı tablosunda **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** sütunlarında değerleri bulunan satırlarınız varsa ilk eşitlemeyi tamamlamak için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-143">If any rows in the vendor table have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="f9d4e-144">Finance and Operations uygulamasında, eşlemeden **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** sütunlarını silin ve ardından eşlemeyi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="f9d4e-145">**Satıcılar V2 (msdyn\_vendors)** için çift yazma eşleme sayfasında, **Tablo eşlemeleri** sekmesinde, sol filtrede **Finance and Operations apps.Vendors V2**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="f9d4e-146">Sağ filtrede, **Sales.Vendor**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="f9d4e-147">**primarycontactperson** öğesini arayıp **PrimaryContactPersonId** kaynak sütununu bulun.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source column.</span></span>
    3. <span data-ttu-id="f9d4e-148">**Eylemler**'i ve sonra **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-148">Select **Actions**, and then select **Delete**.</span></span>

        ![PrimaryContactPersonId sütununu silme](media/vend_selfref3.png)

    4. <span data-ttu-id="f9d4e-150">**InvoiceVendorAccountNumber** sütununu silmek için bu adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** column.</span></span>

        ![InvoiceVendorAccountNumber sütununu silme](media/vend-selfref4.png)

    5. <span data-ttu-id="f9d4e-152">Değişikliklerinizi eşlemeye kaydedin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="f9d4e-153">**Satıcılar V2** tablosu için değişiklik izlemeyi kapatın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-153">Turn off change tracking for the **Vendors V2** table.</span></span>

    1. <span data-ttu-id="f9d4e-154">**Veri yönetimi** çalışma alanında **Veri tabloları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="f9d4e-155">**Satıcılar V2** tablosunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-155">Select the **Vendors V2** table.</span></span>
    3. <span data-ttu-id="f9d4e-156">Eylem Bölmesinde, **Seçenekler**'i ve sonra **Değişiklik izleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Değişiklik izleme seçeneğini belirleme](media/selfref_options.png)

    4. <span data-ttu-id="f9d4e-158">**Değişiklik izlemeyi devre dışı bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-158">Select **Disable Change Tracking**.</span></span>

        ![Değişiklik İzlemeyi Devre Dışı Bırak'ı seçme](media/selfref_tracking.png)

3. <span data-ttu-id="f9d4e-160">**Satıcı v2 (msdyn\_vendors)** eşlemesinin ilk eşitlemesini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="f9d4e-161">İlk eşitleme hatasız olarak çalışmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="f9d4e-162">**CDS İlgili Kişileri V2 (ilgili kişiler)** eşlemesi için başlangıç eşitlemesini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="f9d4e-163">İlk eşitlemenin ilgili kişi satırları için de yapılması gerektiğinden, satıcılar tablosundaki birincil ilgili kişi sütununu eşitlemek istiyorsanız bu eşlemeyi eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-163">You must sync this mapping if you want to sync the primary contact column on the vendors table, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="f9d4e-164">**PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** sütunlarını **Satıcılar v2 (msdyn\_vendors)** eşlemesine geri ekleyin ve eşlemeyi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** columns back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="f9d4e-165">**Satıcı v2 (msdyn\_vendors)** eşlemesinin ilk eşitlemesini yeniden çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="f9d4e-166">Değişiklik izleme devre dışı bırakıldığından tüm satırlar eşitlenecek.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="f9d4e-167">**Satıcılar V2** tablosu için değişiklik izlemeyi yeniden açın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-167">Turn change tracking back on for the **Vendors V2** table.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="f9d4e-168">Customers V3–to–Accounts tablo eşlemesinde hataları çözümleme</span><span class="sxs-lookup"><span data-stu-id="f9d4e-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="f9d4e-169">Tabloların, **ContactPersonID** ve **InvoiceAccount** sütunlarında değerleri bulunan mevcut satırları varsa **Müşteriler V3** ile **Hesaplar** eşlemesinde ilk eşitleme hatalarıyla karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** columns.</span></span> <span data-ttu-id="f9d4e-170">Bu hataların oluşma nedeni, **InvoiceAccount** sütununun kendine başvuruda bulunan bir sütun olması ve **ContactPersonID**'nin satıcı eşlemesinde döngüsel bir başvuru olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-170">These errors occur because **InvoiceAccount** is a self-referencing column, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="f9d4e-171">Aldığınız hata iletileri aşağıdaki şekilde olacaktır.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="f9d4e-172">*Alan için GUID çözümlenemedi: \<field\>. Arama bulunamadı: \<value\>. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="f9d4e-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="f9d4e-173">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="f9d4e-173">Here are some examples:</span></span>

- <span data-ttu-id="f9d4e-174">*Alan için GUID çözümlenemedi: primarycontactid.msdyn\_contactpersonid. Arama bulunamadı: 000056. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="f9d4e-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="f9d4e-175">*Alan için GUID çözümlenemedi: msdyn\_billingaccount.accountnumber. Arama bulunamadı: 1206-1. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="f9d4e-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="f9d4e-176">Müşteri tablosunda **ContactPersonID** ve **InvoiceAccount** sütunlarında değerler bulunan satırlar varsa ilk eşitlemeyi tamamlamak için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-176">If any rows in the customer table have values in the **ContactPersonID** and **InvoiceAccount** columns, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="f9d4e-177">Bu yaklaşımı, **Hesaplar** ve **İlgili kişiler** gibi kullanıma hazır tüm tablolar için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="f9d4e-178">Finance and Operations uygulamasında, **Müşteriler V3 (firmalar)** eşlemesinden **ContactPersonID** ve **InvoiceAccount** sütunlarını silin ve değişiklikleri kaydedin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** columns from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="f9d4e-179">**Müşteriler V3 (firmalar)** için çift yazma eşleme sayfasında, **Tablo eşlemeleri** sekmesinde, sol filtrede, **Finance and Operations app.Customers V3** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="f9d4e-180">Sağ filtrede, **Dataverse.Firma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="f9d4e-181">**contactperson** öğesini arayıp **ContactPersonID** kaynak sütununu bulun.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-181">Search for **contactperson** to find the **ContactPersonID** source column.</span></span>
    3. <span data-ttu-id="f9d4e-182">**Eylemler**'i ve sonra **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-182">Select **Actions**, and then select **Delete**.</span></span>

        ![ContactPersonID sütununu silme](media/cust_selfref3.png)

    4. <span data-ttu-id="f9d4e-184">**InvoiceAccount** sütununu silmek için bu adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-184">Repeat these steps to delete the **InvoiceAccount** column.</span></span>

        ![InvoiceAccount sütununu silme](media/cust_selfref4.png)

    5. <span data-ttu-id="f9d4e-186">Değişikliklerinizi eşlemeye kaydedin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="f9d4e-187">**Müşteriler V3** tablosu için değişiklik izlemeyi kapatın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-187">Turn off change tracking for the **Customers V3** table.</span></span>

    1. <span data-ttu-id="f9d4e-188">**Veri yönetimi** çalışma alanında **Veri tabloları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="f9d4e-189">**Müşteriler V3** tablosunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-189">Select the **Customers V3** table.</span></span>
    3. <span data-ttu-id="f9d4e-190">Eylem Bölmesinde, **Seçenekler**'i ve sonra **Değişiklik izleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Değişiklik izleme seçeneğini belirleme](media/selfref_options.png)

    4. <span data-ttu-id="f9d4e-192">**Değişiklik izlemeyi devre dışı bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-192">Select **Disable Change Tracking**.</span></span>

        ![Değişiklik İzlemeyi Devre Dışı Bırak'ı seçme](media/selfref_tracking.png)

3. <span data-ttu-id="f9d4e-194">**Müşteriler V3 (Hesaplar)** eşlemesi için başlangıç eşitlemesini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="f9d4e-195">İlk eşitleme hatasız olarak çalışmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="f9d4e-196">**CDS İlgili Kişileri V2 (ilgili kişiler)** eşlemesi için başlangıç eşitlemesini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9d4e-197">Aynı ada sahip iki eşleme var.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-197">There are two maps that have the same name.</span></span> <span data-ttu-id="f9d4e-198">**Ayrıntılar** sekmesinde şu açıklama bulunan eşlemeyi seçtiğinizden emin olun: **FO.CDS Satıcı İlgili Kişileri V2 ile CDS.İlgili Kişileri arasında eşitleme için çift yazma şablonu. \[Dynamics365SupplyChainExtended\] yeni paketini gerektirir.**</span><span class="sxs-lookup"><span data-stu-id="f9d4e-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="f9d4e-199">**Müşteriler V3 (Hesaplar)** eşlemesinden **InvoiceAccount** ve **ContactPersonId** sütunlarını silin ve değişiklikleri kaydedin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-199">Add the **InvoiceAccount** and **ContactPersonId** columns back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="f9d4e-200">Şimdi, hem **InvoiceAccount** sütunu hem de **ContactPersonId** sütunu yeniden canlı eşitleme modunun parçası olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-200">Both the **InvoiceAccount** column and the **ContactPersonId** column are now part of live synchronization mode again.</span></span> <span data-ttu-id="f9d4e-201">Sonraki adımda, bu sütunlar için başlangıç eşitlemesini tamamlayacaksınız.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-201">In the next step, you will do the initial synchronization for these columns.</span></span>
6. <span data-ttu-id="f9d4e-202">**Müşteriler V3 (Hesaplar)** eşlemesi için başlangıç eşitlemesini yeniden çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="f9d4e-203">Değişiklik izleme devre dışı bırakıldığından, **InvoiceAccount** ve **ContactPersonId** için veriler Finance and Operations uygulamasından Dataverse'e eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="f9d4e-204">**InvoiceAccount** ve **ContactPersonId** için verileri Dataverse'dan Finance and Operations uygulamasına eşitlemek için bir veri tümleştirme projesi kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="f9d4e-205">Power Apps içinde, **Sales.Account** ve **Finance and Operations apps.Customers V3** tabloları arasında veri tümleştirme projesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="f9d4e-206">Veri yönü, Dataverse'ten Finance and Operations uygulamasına olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="f9d4e-207">**InvoiceAccount** çift yazmada yeni bir öznitelik olduğundan, bunun için ilk eşitlemeyi atlamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="f9d4e-208">Daha fazla bilgi için bkz. [Dataverse'e veri entegre edin](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="f9d4e-208">For more information, see [Integrate data into Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="f9d4e-209">Aşağıdaki resimde **CustomerAccount** ve **ContactPersonId**'yi güncelleştiren bir proje gösterilmektedir .</span><span class="sxs-lookup"><span data-stu-id="f9d4e-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![CustomerAccount ve ContactPersonId alanını güncelleştirmek için veri tümleştirme projesi](media/cust_selfref6.png)

    2. <span data-ttu-id="f9d4e-211">Finance and Operations uygulamasında yalnızca filtre ölçütleriyle eşleşen satırların güncelleştirilmesi için şirket ölçütlerini Dataverse tarafında filtreye ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="f9d4e-212">Filtre eklemek için filtre düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="f9d4e-213">Ardından, **Sorguyu düzenle** iletişim kutusunda **\_msdyn\_company\_value eq '\<guid\>'** gibi bir filtre sorgusu ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="f9d4e-214">[NOT] Filtre düğmesi yoksa, veri tümleştirme ekibinin kiracınızda filtre yeteneğini etkinleştirmesini istemek için bir destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="f9d4e-215">**\_msdyn\_company\_value** için bir filtre sorgusu girmezseniz tüm satırlar eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![Filtre sorgusu ekleme](media/cust_selfref7.png)

    <span data-ttu-id="f9d4e-217">Satırların ilk eşitlenme işlemi şimdi tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="f9d4e-218">Finance and Operations uygulamasında, **Müşteriler V3** tablosu için değişiklik izlemeyi yeniden açın.</span><span class="sxs-lookup"><span data-stu-id="f9d4e-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** table.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]