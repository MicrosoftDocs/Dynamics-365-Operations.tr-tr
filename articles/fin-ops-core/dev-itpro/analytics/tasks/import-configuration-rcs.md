---
title: (ER) Yapılandırmaları RCS'den içe aktarma
description: Bu konu, bir kullanıcının bir ER yapılandırmasının yeni sürümünü RCS'den nasıl içe aktarılacağı hakkında bilgi sağlar.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32c9c17d8b63e4c0806559c2dcc2e11ae9825a53
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184635"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="5effa-103">(ER) Yapılandırmaları RCS'den içe aktarma</span><span class="sxs-lookup"><span data-stu-id="5effa-103">(ER) Import configurations from RCS</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5effa-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Regulatory Configuration Services (RCS)'den içe aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="5effa-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="5effa-105">Bu örnekte, bir RCS örneğinde yapılandırılan ER yapılandırmasının sürümünü seçersiniz ve bunu örnek şirket, Litw, Inc. için geçerli örneğe aktarmanız gerekir. Bu adımlar herhangi bir şirket içinde gerçekleştirilerek, ER yapılandırmaları şirketler arasında paylaşıldığından gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="5effa-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="5effa-106">Bu adımları tamamlamak için öncelikle [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md). adımlarını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5effa-106">To complete these steps, you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="5effa-107">Bu adımları tamamlamak için **Tamamlanmış** veya **Paylaşılan** durumda en az bir er yapılandırması içeren bir RCS örneğine de erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5effa-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="5effa-108">**Organizasyon yönetimi** > **Çalışma alanları** > **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="5effa-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="5effa-109">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5effa-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="5effa-110">Bu konudaki yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) prosedüründeki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="5effa-110">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="5effa-111">Şirketiniz için sağlanmış bir RCS ortamınız yoksa **Regulatory services - Yapılandırma** dış bağlantısını tıklatın ve RCS ortamını sağlamak için yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="5effa-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="5effa-112">**Elektronik raporlama parametreleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5effa-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="5effa-113">**RCS** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5effa-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="5effa-114">Şirketiniz için RCS ortamı zaten sağlanmış ise ona erişmek için sayfa URL'lerinde sunulanları kullanın.</span><span class="sxs-lookup"><span data-stu-id="5effa-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="5effa-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5effa-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="5effa-116">Yeni bir ER havuzu kaydedin.</span><span class="sxs-lookup"><span data-stu-id="5effa-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="5effa-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="5effa-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="5effa-118">Litware, Inc. sağlayıcısı seçin.</span><span class="sxs-lookup"><span data-stu-id="5effa-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="5effa-119">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5effa-119">Click Repositories.</span></span> 
4. <span data-ttu-id="5effa-120">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5effa-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="5effa-121">Yapılandırma havuz türü alanında RCS'yi girin.</span><span class="sxs-lookup"><span data-stu-id="5effa-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="5effa-122">Havuz oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5effa-122">Click Create repository.</span></span> 
7. <span data-ttu-id="5effa-123">RCS ortamı görüntüleme adı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="5effa-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="5effa-124">İstenilen RCS örneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="5effa-124">Select the desired RCS instance.</span></span> <span data-ttu-id="5effa-125">Bunlardan birkaç tane olabilir.</span><span class="sxs-lookup"><span data-stu-id="5effa-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="5effa-126">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5effa-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="5effa-127">RCS tabanlı depodan ER yapılandırmalarını içe aktarın</span><span class="sxs-lookup"><span data-stu-id="5effa-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="5effa-128">**Filtreleri göster**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5effa-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="5effa-129">**Name** alanındaki "RCS" değeri filtresine **ile başlar** filtre işlecini kullanarak bir filtre girin.</span><span class="sxs-lookup"><span data-stu-id="5effa-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="5effa-130">Seçili havuzu açtığınızda, **Regulatory Configuration Services'a bağlan** sayfasında,**Regulatory Configuration Services'e bağlanmak için buraya tıklayın** bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5effa-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="5effa-131">**Aç**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5effa-131">Click **Open**.</span></span> 
5. <span data-ttu-id="5effa-132">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5effa-132">Click **Close**.</span></span> 
6. <span data-ttu-id="5effa-133">İstenen ER yapılandırması sürümünü seçin ve bunu geçerli örneğine getirmek için **İçe aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5effa-133">Select the desired version of ER configuration and click **Import** to bring it in the current instance.</span></span>

