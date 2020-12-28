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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b591df3d384e8dc59646ebb9d0205001db040a55
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684199"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="efaf8-103">(ER) Yapılandırmaları RCS'den içe aktarma</span><span class="sxs-lookup"><span data-stu-id="efaf8-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="efaf8-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Regulatory Configuration Services (RCS)'den içe aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="efaf8-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="efaf8-105">Bu örnekte, bir RCS örneğinde yapılandırılan ER yapılandırmasının sürümünü seçersiniz ve bunu örnek şirket, Litw, Inc. için geçerli örneğe aktarmanız gerekir. Bu adımlar herhangi bir şirket içinde gerçekleştirilerek, ER yapılandırmaları şirketler arasında paylaşıldığından gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="efaf8-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="efaf8-106">Bu adımları tamamlamak için öncelikle [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md). adımlarını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="efaf8-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="efaf8-107">Bu adımları tamamlamak için **Tamamlanmış** veya **Paylaşılan** durumda en az bir er yapılandırması içeren bir RCS örneğine de erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="efaf8-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="efaf8-108">**Organizasyon yönetimi** > **Çalışma alanları** > **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="efaf8-109">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="efaf8-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="efaf8-110">Bu yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="efaf8-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="efaf8-111">Şirketiniz için sağlanmış bir RCS ortamınız yoksa **Regulatory services - Yapılandırma** dış bağlantısını seçin ve RCS ortamını sağlamak için yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-111">If you have no RCS environment provisioned to your company, select **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="efaf8-112">**Elektronik raporlama parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-112">Select **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="efaf8-113">**RCS** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-113">Select the **RCS** tab.</span></span> 
6. <span data-ttu-id="efaf8-114">Şirketiniz için RCS ortamı zaten sağlanmış ise ona erişmek için sayfa URL'lerinde sunulanları kullanın.</span><span class="sxs-lookup"><span data-stu-id="efaf8-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="efaf8-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="efaf8-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="efaf8-116">Yeni bir ER havuzu kaydedin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="efaf8-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="efaf8-118">Litware, Inc. sağlayıcısı seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="efaf8-119">Depolar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-119">Select Repositories.</span></span> 
4. <span data-ttu-id="efaf8-120">Açılır iletişim kutusunu açmak için Ekle öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-120">Select Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="efaf8-121">Yapılandırma havuz türü alanında RCS'yi girin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="efaf8-122">Depo oluştur'u seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-122">Select Create repository.</span></span> 
7. <span data-ttu-id="efaf8-123">RCS ortamı görüntüleme adı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="efaf8-124">İstenilen RCS örneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-124">Select the desired RCS instance.</span></span> <span data-ttu-id="efaf8-125">Bunlardan birkaç tanesine sahip olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="efaf8-125">You can have several of them.</span></span> 
9. <span data-ttu-id="efaf8-126">Tamam'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-126">Select OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="efaf8-127">RCS tabanlı depodan ER yapılandırmalarını içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="efaf8-127">Import ER configurations from RCS-based repository</span></span>
1. <span data-ttu-id="efaf8-128">**Filtreleri göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-128">Select **Show filters**.</span></span> 
2. <span data-ttu-id="efaf8-129">**Name** alanındaki "RCS" değeri filtresine **ile başlar** filtre işlecini kullanarak bir filtre girin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="efaf8-130">Seçili depoyu açtığınızda, **Regulatory Configuration Services'a bağlan** sayfasında,**Regulatory Configuration Services'a bağlanmak için burayı seçin** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, select **Select here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="efaf8-131">**Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-131">Select **Open**.</span></span> 
5. <span data-ttu-id="efaf8-132">**Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-132">Select **Close**.</span></span> 
6. <span data-ttu-id="efaf8-133">İstenen ER yapılandırması sürümünü seçin ve bunu geçerli kuruluma getirmek için **İçeri aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="efaf8-133">Select the desired version of ER configuration and select **Import** to bring it in the current instance.</span></span>

