---
title: RCS genel deposunda yapılandırmaları sona erdirme
description: Bu konuda, RCS genel deposundaki yapılandırmaların nasıl sona erdirileceği açıklanmaktadır.
author: JaneA07
manager: AnnBe
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 35d0af91161d898b09557a83913019609c71e836
ms.sourcegitcommit: e9d19f25e64cf4d1c1d07c8031a7081454a6f79e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/18/2021
ms.locfileid: "5474260"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="d4d16-103">RCS genel deposunda yapılandırmaları sona erdirme</span><span class="sxs-lookup"><span data-stu-id="d4d16-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4d16-104">Bu konuda, RCS genel deposundaki yapılandırmanın nasıl sona erdirileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d4d16-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="d4d16-105">Daha önce, gerekli olmayan yapılandırmalar yalnızca silinebiliyordu.</span><span class="sxs-lookup"><span data-stu-id="d4d16-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="d4d16-106">Ancak şimdi, sunulan bir yapılandırmayı RCS genel deposunda **Sona erdirildi** olarak işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4d16-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="d4d16-107">Bu işlevle şunları da yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d4d16-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="d4d16-108">Bir yapılandırmanın sona erdirilmesi planlanıyorsa ön bildirim sağlama.</span><span class="sxs-lookup"><span data-stu-id="d4d16-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="d4d16-109">Eskisiyle değiştirilen yapılandırmayla ilgili ayrıntılar ekleme.</span><span class="sxs-lookup"><span data-stu-id="d4d16-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="d4d16-110">Kullanıcıya, belirli bir yapılandırmanın ne zaman sona erdirileceğiyle ilgili bilgi vermek için bir **Son desteklenme tarihi** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d4d16-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="d4d16-111">Bir yapılandırma sürümünü sona erdirdiğinizde aşağıdaki isteğe bağlı bilgileri belirtebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d4d16-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="d4d16-112">**Yedek yapılandırma**</span><span class="sxs-lookup"><span data-stu-id="d4d16-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="d4d16-113">**Yedek yapılandırma sürümü**</span><span class="sxs-lookup"><span data-stu-id="d4d16-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="d4d16-114">**Serbest metin notu**: Belge bağlantıları veya referanslar sağlamak için bu alanı kullanın</span><span class="sxs-lookup"><span data-stu-id="d4d16-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="d4d16-115">**Son desteklenme tarihi**: Bu alan, geçerli yapılandırmanın/sürümün destekleneceği son tarihi sağlar.</span><span class="sxs-lookup"><span data-stu-id="d4d16-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="d4d16-116">Bu tarih el ile güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="d4d16-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="d4d16-117">Yapılandırmayı sona erdirmek için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="d4d16-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="d4d16-118">**Tüm sürümleri** **Evet**'e ayarlayarak aynı ayarlara sahip tüm sürümleri ya da tek bir sürümü tek bir işlemle sona erdirmek istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="d4d16-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="d4d16-119">**Sona erdir** parametresini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d4d16-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="d4d16-120">Yapılandırmaları sona erdirmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d4d16-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="d4d16-121">Değişiklikleri kaydettiğinizde, **Sona erdirilen tarih** alanı doldurulacaktır.</span><span class="sxs-lookup"><span data-stu-id="d4d16-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Yapılandırmayı sona erdirme bilgileri](media/Discontinue-details-2.png)
  
<span data-ttu-id="d4d16-123">Yapılandırmayı istediğiniz zaman **paylaşılan** olarak geri döndürebilir veya sona erdirme bilgilerini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4d16-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="d4d16-124">Bir yapılandırmayı paylaştırırsanız, ileride yapılacak sona erdirme için planlarınızı belirtecek şekilde **desteklendiği son tarih** ve sona erdirmeyle ilgili tüm diğer bilgileri belirtin.</span><span class="sxs-lookup"><span data-stu-id="d4d16-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="d4d16-125">Yapılandırmanın sona erdirilmesinden önce, planlı bir sona erdirme hakkında bilgi paylaşmak istiyorsanız, kullanıcı yedek yapılandırmayla ilgili tüm alanları önceden doldurabilir ancak **Sona erdir** parametresini **Hayır** olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d4d16-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="d4d16-126">Sona erdirme, yapılandırmayla yapılan işlemleri sınırlamaz.</span><span class="sxs-lookup"><span data-stu-id="d4d16-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="d4d16-127">Yapılandırmaları almaya, çalıştırmaya veya türetmeye devam edebilirsiniz; bu alanlar bilgi amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="d4d16-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="d4d16-128">Finance, 10.0.14 sürümünden itibaren bu bilgilerin görüntülenmesini destekler</span><span class="sxs-lookup"><span data-stu-id="d4d16-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="d4d16-129">Dynamics 365 Finance, 10.0.14 sürümünden itibaren sona erdirme bilgilerinin görüntülenmesini destekler.</span><span class="sxs-lookup"><span data-stu-id="d4d16-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="d4d16-130">**Genel depo** sayfasında, sona erdirmeyle ilgili güncel bilgileri görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4d16-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="d4d16-131">Varsayılan olarak, sona erdirilen yapılandırmalar filtrelenir.</span><span class="sxs-lookup"><span data-stu-id="d4d16-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="d4d16-132">**İçe aktarılan yapılandırmalar** (ERSolutionTable) sayfası, içe aktarıldıklarında zaten sona erdirilmiş olan yapılandırmaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="d4d16-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="d4d16-133">İçe aktarma işleminden sonra sona erdirilen yapılandırmalar için **içe aktarma yapılandırmaları güncelleştirmeleri** işi çalıştırılarak sona erdirme bilgileri eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="d4d16-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


