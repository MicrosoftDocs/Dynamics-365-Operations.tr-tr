---
title: Finance and Operations uygulamalarında Çift yazma modülüyle ilgili sorunları giderme
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172772"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="280ae-103">Finance and Operations uygulamalarında Çift yazma modülüyle ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="280ae-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="280ae-104">Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="280ae-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="280ae-105">Bu konu, Finance and Operations uygulamalardaki **çift-yazma** modülüyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="280ae-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="280ae-106">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="280ae-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="280ae-107">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="280ae-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="280ae-108">Çift-yazılır modülü bir Finance and Operations uygulamaya yüklenemez</span><span class="sxs-lookup"><span data-stu-id="280ae-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="280ae-109">**Çift- yazılır** sayfayı, **veri yönetimi** çalışma alanında **ikili yazma** kutucuğunu seçerek açamazsınız, veri tümleştirme hizmeti büyük olasılıkla çalışmıyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="280ae-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="280ae-110">Veri tümleştirme hizmetinin yeniden başlatılmasını istemek için bir destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="280ae-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="280ae-111">Yeni bir varlık eşlemesi oluşturmaya çalıştığınızda hata oluştu</span><span class="sxs-lookup"><span data-stu-id="280ae-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="280ae-112">**Sorunun düzeltilmesi için gerekli olan kimlik bilgileri:** Azure AD Kiracı Yönetimi</span><span class="sxs-lookup"><span data-stu-id="280ae-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="280ae-113">Çift-yazılır için yeni bir varlık yapılandırmaya çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="280ae-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="280ae-114">*Yanıt durum kodu başarıyı göstermiyor: 401 (yetkisiz)*</span><span class="sxs-lookup"><span data-stu-id="280ae-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="280ae-115">Bu hata, yalnızca bir Azure AD kiracı yöneticisinin yeni bir varlık eşlemesi ekleyebilmesi nedeniyle oluşur.</span><span class="sxs-lookup"><span data-stu-id="280ae-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="280ae-116">Bu sorunu gidermek için, Finance and Operations uygulamaya Azure AD yönetici kiracısı olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="280ae-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="280ae-117">Ayrıca Web.PowerApps.com'e gitmelisiniz ve bağlantınızı yeniden doğrular.</span><span class="sxs-lookup"><span data-stu-id="280ae-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="280ae-118">İkili yazma Kullanıcı arabirimini açtığınızda hata oluştu</span><span class="sxs-lookup"><span data-stu-id="280ae-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="280ae-119">**Veri yönetimi** çalışma alanından çift-yazılabilir erişmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="280ae-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="280ae-120">*login.microsoftonline.com bağlanmayı reddetti.*</span><span class="sxs-lookup"><span data-stu-id="280ae-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="280ae-121">Sorunu gidermek için, Microsoft Edge'de bir InPrivate pencere, Chromium'da bir gizli penceresi veya Google Chrome 'da bir gizli penceresi kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="280ae-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="280ae-122">Ayrıca, üçüncü taraf tanımlama bilgilerini engellemeyi veya temizlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="280ae-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="280ae-123">Ortam ikili yazma için bağlantılandırma sırasında hata oluştu veya yeni bir varlık eşlemesi ekler</span><span class="sxs-lookup"><span data-stu-id="280ae-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="280ae-124">**Sorunun düzeltilmesi için gerekli olan kimlik bilgileri:** Azure AD Kiracı Yönetimi</span><span class="sxs-lookup"><span data-stu-id="280ae-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="280ae-125">Haritaları bağlarken veya oluştururken aşağıdaki hata ile karşılaşabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="280ae-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="280ae-126">*Yanıt durum kodu başarı göstermiyor: 403 (tokenexchange). <br>Oturum kodu: \<oturum kimliği\><br> kök etkinlik kimliği: \<kök etkinlik kimliğiniz\>*</span><span class="sxs-lookup"><span data-stu-id="280ae-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="280ae-127">Bu hata, Çift-yazılabilir veya haritalar oluşturmak için yeterli izniniz yoksa oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="280ae-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="280ae-128">Ortamları bağlamak ve yeni Azure AD varlık eşlemeleri eklemek için kiracı yöneticisi hesabı kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="280ae-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="280ae-129">Ancak, kurulumdan sonra, durumu izlemek ve eşlemeleri düzenlemek için yönetici olmayan bir hesabı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="280ae-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="280ae-130">Varlık eşlemesini durdurduğunuzda hata oluştu</span><span class="sxs-lookup"><span data-stu-id="280ae-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="280ae-131">Varlık eşlemelerini durdurmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="280ae-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="280ae-132">*\[Yasak\], \[{"durum": 403, "kaynak": "", "mesaj": "belirteç değiş tokuşu nedeniyle hata: kullanıcının dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]bağlantısına erişmesine izin verilmiyor uzak sunucu hata verdi: (403) yasak.*</span><span class="sxs-lookup"><span data-stu-id="280ae-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="280ae-133">Bu hata, bağlı Common Data Service ortam kullanılabilir olmadığında oluşur.</span><span class="sxs-lookup"><span data-stu-id="280ae-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="280ae-134">Bu sorunu gidermek için, veri tümleştirme ekibi için bir bilet oluşturun.</span><span class="sxs-lookup"><span data-stu-id="280ae-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="280ae-135">Veri tümleştirme ekibinin eşlemeleri arka uçta **çalışmıyor** olarak işaretlemesi için ağ izlemesini iliştirin.</span><span class="sxs-lookup"><span data-stu-id="280ae-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
