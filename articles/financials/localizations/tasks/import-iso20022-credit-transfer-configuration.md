---
title: ISO20022 alacak transferi yapılandırmasını içe aktarma
description: Bu yordam, satıcı ödemesi elektronik raporlama yapılandırmasının nasıl içe aktarılacağını gösterir.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee7e69611d31d2577ebafdfc059b0936aef0520b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848803"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="12a77-103">ISO20022 alacak transferi yapılandırmasını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="12a77-103">Import ISO20022 credit transfer configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12a77-104">Bu yordam, satıcı ödemesi elektronik raporlama yapılandırmasının nasıl içe aktarılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12a77-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="12a77-105">Örnek olarak Alman ISO 20022 alacak transfer biçimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="12a77-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="12a77-106">Bu yordam diğer mevcut elektronik raporlama biçimleri için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="12a77-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="12a77-107">Bu görev, demo veri şirketi DEMF kullanılarak oluşturulmuştur ancak bu görevi tamamlamak için herhangi bir demo veri şirketini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12a77-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="12a77-108">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş görevin birincisidir.</span><span class="sxs-lookup"><span data-stu-id="12a77-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="12a77-109">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="12a77-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="12a77-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="12a77-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="12a77-111">Kullanılabilir yapılandırma sağlayıcıları listesinden Microsoft'u seçin.</span><span class="sxs-lookup"><span data-stu-id="12a77-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="12a77-112">Etkin olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12a77-112">Click Set active.</span></span>
4. <span data-ttu-id="12a77-113">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12a77-113">Click Repositories.</span></span>
5. <span data-ttu-id="12a77-114">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12a77-114">Click Open.</span></span>
6. <span data-ttu-id="12a77-115">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12a77-115">Click Show filters.</span></span>
7. <span data-ttu-id="12a77-116">Şu filtreleri uygulayın: "ile başlar" filtre işlecini kullanarak "Yapılandırma adı" alanında "ISO20022 Alacak Transferi (DE)" için bir filtre değeri girin</span><span class="sxs-lookup"><span data-stu-id="12a77-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="12a77-117">Alternatif olarak listede yapılandırmayı bulup seçin ve ardından İçe Aktar görevine taşıyın.</span><span class="sxs-lookup"><span data-stu-id="12a77-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="12a77-118">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="12a77-118">Click Import.</span></span>
    * <span data-ttu-id="12a77-119">İçe Aktar düğmesi kullanılamıyorsa yapılandırma zaten içe aktarılmış demektir.</span><span class="sxs-lookup"><span data-stu-id="12a77-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="12a77-120">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="12a77-120">Click Yes.</span></span>

