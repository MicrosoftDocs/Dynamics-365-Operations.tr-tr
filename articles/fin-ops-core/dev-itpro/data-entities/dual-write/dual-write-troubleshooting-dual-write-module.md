---
title: Finance and Operations uygulamalarında çift yazma modülüyle ilgili sorunları giderme
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
ms.openlocfilehash: f99f3760e75ec1bbf2ccdea497cf2eec3e28e233
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997386"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="36742-103">Finance and Operations uygulamalarında çift yazma modülüyle ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="36742-103">Troubleshoot issues with the dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36742-104">Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="36742-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="36742-105">Bu konu, Finance and Operations uygulamalardaki **çift-yazma** modülüyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="36742-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36742-106">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="36742-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="36742-107">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="36742-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="36742-108">Çift yazma modülü bir Finance and Operations uygulamaya yüklenemez</span><span class="sxs-lookup"><span data-stu-id="36742-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="36742-109">**Çift- yazılır** sayfayı, **veri yönetimi** çalışma alanında **ikili yazma** kutucuğunu seçerek açamazsınız, veri tümleştirme hizmeti büyük olasılıkla çalışmıyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="36742-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="36742-110">Veri tümleştirme hizmetinin yeniden başlatılmasını istemek için bir destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="36742-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-map"></a><span data-ttu-id="36742-111">Yeni bir varlık eşlemesi oluşturmaya çalıştığınızda hata oluştu</span><span class="sxs-lookup"><span data-stu-id="36742-111">Error when you try to create a new entity map</span></span>

<span data-ttu-id="36742-112">**Sorunu düzeltmek için gerekli kimlik bilgileri:** Çift yazma kurulumu yapan aynı kullanıcı.</span><span class="sxs-lookup"><span data-stu-id="36742-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="36742-113">Çift yazma için yeni bir varlık yapılandırmaya çalıştığınızda aşağıdaki hata iletisini alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36742-113">You might receive the following error message when you try to configure a new entity for dual-write.</span></span> <span data-ttu-id="36742-114">Eşleme oluşturabilecek tek kullanıcı, çift yazma bağlantısını kuran kullanıcıdır.</span><span class="sxs-lookup"><span data-stu-id="36742-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="36742-115">*Yanıt durum kodu başarıyı göstermiyor: 401 (yetkisiz)*</span><span class="sxs-lookup"><span data-stu-id="36742-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="36742-116">İkili yazma Kullanıcı arabirimini açtığınızda hata oluştu</span><span class="sxs-lookup"><span data-stu-id="36742-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="36742-117">**Veri yönetimi** çalışma alanından çift-yazılabilir erişmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="36742-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="36742-118">*login.microsoftonline.com bağlanmayı reddetti.*</span><span class="sxs-lookup"><span data-stu-id="36742-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="36742-119">Sorunu gidermek için, Microsoft Edge'de bir InPrivate pencere, Chromium'da bir gizli penceresi veya Google Chrome 'da bir gizli penceresi kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="36742-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="36742-120">Ayrıca, üçüncü taraf tanımlama bilgilerini engellemeyi veya temizlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="36742-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="36742-121">Ortam ikili yazma için bağlantılandırma sırasında hata oluştu veya yeni bir varlık eşlemesi ekler</span><span class="sxs-lookup"><span data-stu-id="36742-121">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="36742-122">**Sorunu düzeltmek için gereken rol:** Hem Finance and Operations uygulamalarında hem de Common Data Service'ta sistem yöneticisi.</span><span class="sxs-lookup"><span data-stu-id="36742-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="36742-123">Haritaları bağlarken veya oluştururken aşağıdaki hata ile karşılaşabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="36742-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="36742-124">*Yanıt durum kodu başarı göstermiyor: 403 (tokenexchange).<br>Oturum kodu: \<your session id\><br> Kök etkinlik kimliği: \<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="36742-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="36742-125">Bu hata, Çift-yazılabilir veya haritalar oluşturmak için yeterli izniniz yoksa oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="36742-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="36742-126">Bu hata, Common Data Service ortamı çift yazma bağlantısını kaldırmadan sıfırlanırsa da oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="36742-126">This error can also occur if the Common Data Service environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="36742-127">Hem Finance and Operations uygulamaları hem de Common Data Service'ta sistem yöneticisi rolüne sahip herhangi bir kullanıcı ortamları bağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="36742-127">Any user with system administrator role in both Finance and Operations apps and Common Data Service can link the environments.</span></span> <span data-ttu-id="36742-128">Yalnızca çift yazma yazılır bağlantısını kuran kullanıcı yeni varlık eşlemeleri ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="36742-128">Only the user who setup the dual-write connection can add new entity maps.</span></span> <span data-ttu-id="36742-129">Kurulumdan sonra, sistem yöneticisi rolüne sahip tüm kullanıcılar durumu izleyebilir ve eşlemeleri düzenleyebilir.</span><span class="sxs-lookup"><span data-stu-id="36742-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="36742-130">Varlık eşlemesini durdurduğunuzda hata oluştu</span><span class="sxs-lookup"><span data-stu-id="36742-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="36742-131">Varlık eşlemelerini durdurmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="36742-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="36742-132">*\[Yasak\], \[{"durum": 403, "kaynak": "", "mesaj": "belirteç değiş tokuşu nedeniyle hata: kullanıcının dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]bağlantısına erişmesine izin verilmiyor uzak sunucu hata verdi: (403) yasak.*</span><span class="sxs-lookup"><span data-stu-id="36742-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="36742-133">Bu hata, bağlı Common Data Service ortam kullanılabilir olmadığında oluşur.</span><span class="sxs-lookup"><span data-stu-id="36742-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="36742-134">Bu sorunu gidermek için, veri tümleştirme ekibi için bir bilet oluşturun.</span><span class="sxs-lookup"><span data-stu-id="36742-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="36742-135">Veri tümleştirme ekibinin eşlemeleri arka uçta **çalışmıyor** olarak işaretlemesi için ağ izlemesini iliştirin.</span><span class="sxs-lookup"><span data-stu-id="36742-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-an-entity-mapping"></a><span data-ttu-id="36742-136">Bir varlık eşlemesi başlatılmaya çalışılırken hata</span><span class="sxs-lookup"><span data-stu-id="36742-136">Error while trying to start an entity mapping</span></span>

<span data-ttu-id="36742-137">Bir eşlemenin o durumunu **Çalıştırma** olarak ayarlamaya çalıştığınızda aşağıdakine benzer bir hata alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="36742-137">You might receive an error like the following when you try to set that state of a mapping to **Running** :</span></span>

<span data-ttu-id="36742-138">*İlk veri eşitlemesi tamamlanamıyor. Hata: Çift yazma hatası - eklenti kaydı başarısız oldu: Çift yazma arama meta verileri oluşturulamadı. Hata nesne başvurusu bir nesnenin örneğine ayarlanmadı.*</span><span class="sxs-lookup"><span data-stu-id="36742-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="36742-139">Bu hata için düzeltme hatanın nedenine bağlıdır:</span><span class="sxs-lookup"><span data-stu-id="36742-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="36742-140">Eşlemeye bağımlı eşlemeler varsa, bu varlık eşlemesinin bağımlı eşlemelerini etkinleştirdiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="36742-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this entity mapping.</span></span>
+ <span data-ttu-id="36742-141">Eşlemede kaynak veya hedef alanlar eksik olabilir.</span><span class="sxs-lookup"><span data-stu-id="36742-141">The mapping might be missing source or destination fields.</span></span> <span data-ttu-id="36742-142">Finance and Operations uygulamalarında bir alan eksikse, [Eşlemelerde eksik varlık alanları sorunu](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps) bölümlerindeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="36742-142">If a field in the Finance and Operations app is missing, then follow the steps in the section [Missing entity fields issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps).</span></span> <span data-ttu-id="36742-143">Common Data Service'taki bir alan eksikse, alanların otomatik olarak eşlemeye geri doldurulması için eşlemede **Varlıkları yenile** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36742-143">If a field in Common Data Service is missing, then click **Refresh entities** button on the mapping so that the fields are automatically populated back into the mapping.</span></span>
