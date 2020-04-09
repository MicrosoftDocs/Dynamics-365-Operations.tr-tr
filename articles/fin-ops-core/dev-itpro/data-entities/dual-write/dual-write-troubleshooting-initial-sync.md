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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172726"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="cd217-103">Başlangıç eşitlemesi sırasında sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="cd217-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="cd217-104">Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="cd217-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="cd217-105">Bu konu, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="cd217-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="cd217-106">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="cd217-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="cd217-107">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="cd217-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="cd217-108">Finance and Operations uygulamadaki ilk eşitleme hatalarını denetle</span><span class="sxs-lookup"><span data-stu-id="cd217-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="cd217-109">Eşleme şablonları etkinleştirildikten sonra, haritaların durumu **çalışıyor** olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cd217-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="cd217-110">Durum **çalışmıyorsa**, ilk eşitleme sırasında hata meydana geldi.</span><span class="sxs-lookup"><span data-stu-id="cd217-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="cd217-111">Hataları görüntülemek için **çift-yazma** sayfasında **ilk eşitleme ayrıntıları** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cd217-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![İlk eşitleme Ayrıntıları sekmesi](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="cd217-113">İlk eşitlemeyi tamamlayamıyoruz: 400 Hatalı Istek</span><span class="sxs-lookup"><span data-stu-id="cd217-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="cd217-114">**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="cd217-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="cd217-115">Eşlemeyi ve ilk senkronizasyonu çalıştırmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="cd217-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="cd217-116">*Uzak sunucu hata verdi: (400) hatalı Istek.), AX dışarı aktarma bir hatayla karşılaştı*</span><span class="sxs-lookup"><span data-stu-id="cd217-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="cd217-117">Burada tam hata mesajı tablosu için bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="cd217-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="cd217-118">Bu hata sürekli olarak oluşuyorsa ve ilk eşitlemeyi tamamlayamıyorsa, sorunu düzeltmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="cd217-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="cd217-119">Finance and Operations uygulamanın sanal makinesine (VM) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="cd217-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="cd217-120">Microsoft Yönetim Konsolu 'Nu açın.</span><span class="sxs-lookup"><span data-stu-id="cd217-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="cd217-121">**Hizmetler** bölmesinde, Microsoft Dynamics 365 veri alma verme çerçevesi hizmetinin çalışmakta olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="cd217-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="cd217-122">Durdurulmuşsa, ilk eşitleme gerektirdiğinden yeniden Başlat.</span><span class="sxs-lookup"><span data-stu-id="cd217-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="cd217-123">İlk eşitleme hatası: 403 Yasak</span><span class="sxs-lookup"><span data-stu-id="cd217-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="cd217-124">İlk eşitlemede aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="cd217-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="cd217-125">*(\[Yasak\], Uzak sunucu hata verdi: (403) Yasak), AX dışarı aktarma bir hatayla karşılaştı*</span><span class="sxs-lookup"><span data-stu-id="cd217-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="cd217-126">Sorunu düzeltmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="cd217-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="cd217-127">Finance and Operations Uygulamaya oturum açın.</span><span class="sxs-lookup"><span data-stu-id="cd217-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="cd217-128">**Azure Active Directory uygulamalar** sayfasında **DtAppID** istemcisini silin ve sonra yeniden ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cd217-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD uygulamalar listesi](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="cd217-130">İlk eşitleme sırasında kendi kendine referans hataları</span><span class="sxs-lookup"><span data-stu-id="cd217-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="cd217-131">Eşlemelerinizin kendi kendine referansları varsa, aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="cd217-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="cd217-132">*Satıcılar sürüm 2'de aşağıdaki hata: kayıt kodu: yeni kayıt, ErrorMessage: alan için GUID çözülemedi: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Arama değeri bulunamadı: CN-001. Başvuru verilerinin var olup olmadığını denetlemek için bu URL 'yi deneyin: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber`  eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="cd217-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="cd217-133">Bu tür bir hata, kendi kendine referansları olan eşlemelerin ilk eşitlemesi sırasında oluşur.</span><span class="sxs-lookup"><span data-stu-id="cd217-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="cd217-134">Önceki örnekte, fatura hesabı alanı satıcı varlığına referans gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd217-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="cd217-135">Sorunu gidermek için, ilk eşitleme başarılı olmadan eşlemeyi iki kez çalıştırmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="cd217-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

