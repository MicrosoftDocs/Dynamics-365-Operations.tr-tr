--- 
title: "ISO20022 alacak transferi yapılandırmasını içe aktarma"
description: "Bu yordam, satıcı ödemesi elektronik raporlama yapılandırmasının nasıl içe aktarılacağını gösterir."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 71c0175178203006e297466c4a37cd3e6319b6ea
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="d448f-103">ISO20022 alacak transferi yapılandırmasını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="d448f-103">Import ISO20022 credit transfer configuration</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d448f-104">Bu yordam, satıcı ödemesi elektronik raporlama yapılandırmasının nasıl içe aktarılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d448f-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="d448f-105">Örnek olarak Alman ISO 20022 alacak transfer biçimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d448f-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="d448f-106">Bu yordam diğer mevcut elektronik raporlama biçimleri için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d448f-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="d448f-107">Bu görev, demo veri şirketi DEMF kullanılarak oluşturulmuştur ancak bu görevi tamamlamak için herhangi bir demo veri şirketini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d448f-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="d448f-108">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş görevin birincisidir.</span><span class="sxs-lookup"><span data-stu-id="d448f-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="d448f-109">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="d448f-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="d448f-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="d448f-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d448f-111">Kullanılabilir yapılandırma sağlayıcıları listesinden Microsoft'u seçin.</span><span class="sxs-lookup"><span data-stu-id="d448f-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="d448f-112">Etkin olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d448f-112">Click Set active.</span></span>
4. <span data-ttu-id="d448f-113">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d448f-113">Click Repositories.</span></span>
5. <span data-ttu-id="d448f-114">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d448f-114">Click Open.</span></span>
6. <span data-ttu-id="d448f-115">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d448f-115">Click Show filters.</span></span>
7. <span data-ttu-id="d448f-116">Şu filtreleri uygulayın: "ile başlar" filtre işlecini kullanarak "Yapılandırma adı" alanında "ISO20022 Alacak Transferi (DE)" için bir filtre değeri girin</span><span class="sxs-lookup"><span data-stu-id="d448f-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="d448f-117">Alternatif olarak listede yapılandırmayı bulup seçin ve ardından İçe Aktar görevine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="d448f-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="d448f-118">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d448f-118">Click Import.</span></span>
    * <span data-ttu-id="d448f-119">İçe Aktar düğmesi kullanılamıyorsa yapılandırma zaten içe aktarılmış demektir.</span><span class="sxs-lookup"><span data-stu-id="d448f-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="d448f-120">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d448f-120">Click Yes.</span></span>


