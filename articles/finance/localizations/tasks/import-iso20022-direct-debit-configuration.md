---
title: ISO20022 hesaptan ödeme yapılandırmasını içe aktarma
description: Bu yordam, müşteri ödemesi elektronik raporlama yapılandırmasının nasıl içe aktarılacağını gösterir.
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
ms.openlocfilehash: 7eee00021f49ac0110d7bde07faba8095348e1b4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185762"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="1d895-103">ISO20022 hesaptan ödeme yapılandırmasını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="1d895-103">Import ISO20022 direct debit configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d895-104">Bu yordam, müşteri ödemesi elektronik raporlama yapılandırmasının nasıl içe aktarılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d895-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="1d895-105">Bu yordam örnek olarak ISO 20022 hesaptan ödeme biçimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1d895-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="1d895-106">Bu yordam, demo veri şirketi DEMF kullanılarak oluşturulmuştur ancak bu amaç için herhangi bir demo veri şirketini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d895-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="1d895-107">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak müşteri ödemesi işlemini gösteren beş yordamın birincisidir.</span><span class="sxs-lookup"><span data-stu-id="1d895-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="1d895-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="1d895-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1d895-109">Kullanılabilir yapılandırma sağlayıcıları listesinden Microsoft'u seçin.</span><span class="sxs-lookup"><span data-stu-id="1d895-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="1d895-110">Etkin olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d895-110">Click Set active.</span></span>
4. <span data-ttu-id="1d895-111">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d895-111">Click Repositories.</span></span>
5. <span data-ttu-id="1d895-112">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d895-112">Click Open.</span></span>
6. <span data-ttu-id="1d895-113">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d895-113">Click Show filters.</span></span>
7. <span data-ttu-id="1d895-114">Şu filtreleri uygulayın: "ile başlar" filtre işlecini kullanarak "Yapılandırma adı" alanında "ISO20022 Hesaptan ödeme (DE)" için bir filtre değeri girin</span><span class="sxs-lookup"><span data-stu-id="1d895-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="1d895-115">İsteğe bağlı olarak, listede yapılandırmayı bulabilir, seçebilir ve bu adımı atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d895-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="1d895-116">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1d895-116">Click Import.</span></span>
    * <span data-ttu-id="1d895-117">İçe aktar düğmesi kullanılamıyorsa yapılandırma zaten içe aktarılmış demektir.</span><span class="sxs-lookup"><span data-stu-id="1d895-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="1d895-118">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1d895-118">Click Yes.</span></span>

