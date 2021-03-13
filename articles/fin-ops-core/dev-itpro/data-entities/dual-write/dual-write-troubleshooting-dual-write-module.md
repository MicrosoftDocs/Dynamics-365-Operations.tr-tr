---
title: Finance and Operations uygulamalarında çift yazma sorunlarını giderme
description: Bu konu, Finance and Operations uygulamalardaki çift-yazma modülüyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
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
ms.openlocfilehash: 3ffeb2de0acc1761bccf62a1a124852c504e2a3a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131257"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a><span data-ttu-id="b67fd-103">Finance and Operations uygulamalarında çift yazma sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="b67fd-103">Troubleshoot dual-write issues in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b67fd-104">Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="b67fd-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="b67fd-105">Bu konu, Finance and Operations uygulamalardaki **çift-yazma** modülüyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="b67fd-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b67fd-106">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="b67fd-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="b67fd-107">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b67fd-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="b67fd-108">Çift yazma modülü bir Finance and Operations uygulamaya yüklenemez</span><span class="sxs-lookup"><span data-stu-id="b67fd-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="b67fd-109">**Çift- yazılır** sayfayı, **veri yönetimi** çalışma alanında **ikili yazma** kutucuğunu seçerek açamazsınız, veri tümleştirme hizmeti büyük olasılıkla çalışmıyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="b67fd-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="b67fd-110">Veri tümleştirme hizmetinin yeniden başlatılmasını istemek için bir destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b67fd-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-table-map"></a><span data-ttu-id="b67fd-111">Yeni bir tablo eşlemesi oluşturmaya çalıştığınızda hata oluştu</span><span class="sxs-lookup"><span data-stu-id="b67fd-111">Error when you try to create a new table map</span></span>

<span data-ttu-id="b67fd-112">**Sorunu düzeltmek için gerekli kimlik bilgileri:** Çift yazma kurulumu yapan aynı kullanıcı.</span><span class="sxs-lookup"><span data-stu-id="b67fd-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="b67fd-113">Çift yazma için yeni bir tablo yapılandırmaya çalıştığınızda aşağıdaki hata iletisini alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b67fd-113">You might receive the following error message when you try to configure a new table for dual-write.</span></span> <span data-ttu-id="b67fd-114">Eşleme oluşturabilecek tek kullanıcı, çift yazma bağlantısını kuran kullanıcıdır.</span><span class="sxs-lookup"><span data-stu-id="b67fd-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="b67fd-115">*Yanıt durum kodu başarıyı göstermiyor: 401 (yetkisiz)*</span><span class="sxs-lookup"><span data-stu-id="b67fd-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="b67fd-116">İkili yazma Kullanıcı arabirimini açtığınızda hata oluştu</span><span class="sxs-lookup"><span data-stu-id="b67fd-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="b67fd-117">**Veri yönetimi** çalışma alanından çift-yazılabilir erişmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b67fd-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="b67fd-118">*login.microsoftonline.com bağlanmayı reddetti.*</span><span class="sxs-lookup"><span data-stu-id="b67fd-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="b67fd-119">Sorunu gidermek için, Microsoft Edge'de bir InPrivate pencere, Chromium'da bir gizli penceresi veya Google Chrome 'da bir gizli penceresi kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="b67fd-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="b67fd-120">Ayrıca, üçüncü taraf tanımlama bilgilerini engellemeyi veya temizlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b67fd-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a><span data-ttu-id="b67fd-121">Çift yazma için ortam bağladığınızda veya yeni bir tablo eşlemesi eklediğinizde hata oluştu</span><span class="sxs-lookup"><span data-stu-id="b67fd-121">Error when you link the environment for dual-write or add a new table mapping</span></span>

<span data-ttu-id="b67fd-122">**Sorunu düzeltmek için gereken rol:** Hem Finance and Operations uygulamalarında hem de Dataverse'ta sistem yöneticisi.</span><span class="sxs-lookup"><span data-stu-id="b67fd-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="b67fd-123">Haritaları bağlarken veya oluştururken aşağıdaki hata ile karşılaşabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b67fd-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="b67fd-124">*Yanıt durum kodu başarı göstermiyor: 403 (tokenexchange).<br>Oturum kodu: \<your session id\><br> Kök etkinlik kimliği: \<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="b67fd-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="b67fd-125">Bu hata, Çift-yazılabilir veya haritalar oluşturmak için yeterli izniniz yoksa oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="b67fd-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="b67fd-126">Bu hata, Dataverse ortamı çift yazma bağlantısını kaldırmadan sıfırlanırsa da oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="b67fd-126">This error can also occur if the Dataverse environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="b67fd-127">Hem Finance and Operations uygulamaları hem de Dataverse'ta sistem yöneticisi rolüne sahip herhangi bir kullanıcı ortamları bağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="b67fd-127">Any user with system administrator role in both Finance and Operations apps and Dataverse can link the environments.</span></span> <span data-ttu-id="b67fd-128">Yalnızca çift yazma bağlantısını kuran kullanıcı yeni tablo eşlemeleri ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="b67fd-128">Only the user who setup the dual-write connection can add new table maps.</span></span> <span data-ttu-id="b67fd-129">Kurulumdan sonra, sistem yöneticisi rolüne sahip tüm kullanıcılar durumu izleyebilir ve eşlemeleri düzenleyebilir.</span><span class="sxs-lookup"><span data-stu-id="b67fd-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-table-mapping"></a><span data-ttu-id="b67fd-130">Tablo eşlemesini durdurduğunuzda hata oluştu</span><span class="sxs-lookup"><span data-stu-id="b67fd-130">Error when you stop the table mapping</span></span>

<span data-ttu-id="b67fd-131">Tablo eşlemelerini durdurmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b67fd-131">You might receive the following error message when you try to stop the table mappings:</span></span>

<span data-ttu-id="b67fd-132">*\[Yasak\], \[{"durum": 403, "kaynak": "", "mesaj": "belirteç değiş tokuşu nedeniyle hata: kullanıcının dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]bağlantısına erişmesine izin verilmiyor uzak sunucu hata verdi: (403) yasak.*</span><span class="sxs-lookup"><span data-stu-id="b67fd-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="b67fd-133">Bu hata, bağlı Dataverse ortam kullanılabilir olmadığında oluşur.</span><span class="sxs-lookup"><span data-stu-id="b67fd-133">This error occurs when the linked Dataverse environment isn't available.</span></span>

<span data-ttu-id="b67fd-134">Bu sorunu gidermek için, veri tümleştirme ekibi için bir bilet oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b67fd-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="b67fd-135">Veri tümleştirme ekibinin eşlemeleri arka uçta **çalışmıyor** olarak işaretlemesi için ağ izlemesini iliştirin.</span><span class="sxs-lookup"><span data-stu-id="b67fd-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-a-table-mapping"></a><span data-ttu-id="b67fd-136">Bir tablo eşlemesi başlatılmaya çalışılırken hata oluştu</span><span class="sxs-lookup"><span data-stu-id="b67fd-136">Error while trying to start a table mapping</span></span>

<span data-ttu-id="b67fd-137">Bir eşlemenin o durumunu **Çalıştırma** olarak ayarlamaya çalıştığınızda aşağıdakine benzer bir hata alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b67fd-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="b67fd-138">*İlk veri eşitlemesi tamamlanamıyor. Hata: Çift yazma hatası - eklenti kaydı başarısız oldu: Çift yazma arama meta verileri oluşturulamadı. Hata nesne başvurusu bir nesnenin örneğine ayarlanmadı.*</span><span class="sxs-lookup"><span data-stu-id="b67fd-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="b67fd-139">Bu hata için düzeltme hatanın nedenine bağlıdır:</span><span class="sxs-lookup"><span data-stu-id="b67fd-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="b67fd-140">Eşlemeye bağımlı eşlemeler varsa bu tablo eşlemesinin bağımlı eşlemelerini etkinleştirdiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="b67fd-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this table mapping.</span></span>
+ <span data-ttu-id="b67fd-141">Eşlemede kaynak veya hedef sütunlar eksik olabilir.</span><span class="sxs-lookup"><span data-stu-id="b67fd-141">The mapping might be missing source or destination columns.</span></span> <span data-ttu-id="b67fd-142">Finance and Operations uygulamalarında bir sütun eksikse, [Eşlemelerde eksik tablo sütunları sorunu](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b67fd-142">If a column in the Finance and Operations app is missing, then follow the steps in the section [Missing table columns issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps).</span></span> <span data-ttu-id="b67fd-143">Dataverse'teki bir sütun eksikse sütunların otomatik olarak eşlemede geri doldurulması için eşlemede **Tabloları yenile** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b67fd-143">If a column in Dataverse is missing, then click **Refresh tables** button on the mapping so that the columns are automatically populated back into the mapping.</span></span>
