--- 
title: "Üretim akışı sürümünü devre dışı bırakma"
description: "Etkin bir üretim akışı sürümüne artık ihtiyaç duyulmuyorsa devre dışı bırakılabilir."
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4a7eee6617e12d59a3d06207f5f6b58c93e28240
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="1d892-103">Üretim akışı sürümünü devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="1d892-103">Deactivate a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d892-104">Etkin bir üretim akışı sürümüne artık ihtiyaç duyulmuyorsa devre dışı bırakılabilir.</span><span class="sxs-lookup"><span data-stu-id="1d892-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="1d892-105">Bu seçeneği yalnızca tüm kanban kuralları ve etkinlikler sonlandırmışsa ve yeniden etkinleştirilmeyecekse kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="1d892-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="1d892-106">Bu üretim akışı sürümüyle ilgili tüm kanban kurallarının bitiş tarihinin geçerli tarih ve saat ile güncelleştirileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1d892-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="1d892-107">Etkin bir üretim akışı sürümünü değiştirmek için etkin sürümün bitiş tarihini ayarlamayı düşünün ve yeni bir sürüm oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1d892-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="1d892-108">Bu, yeni sürümü ve ilgili kanban kurallarını hazırlarken üretim operasyonlarınıza devam etmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="1d892-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="1d892-109">Etkin bir üretim akışı sürümünün geçerliliğini sona erdirmek için bitiş tarihini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d892-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="1d892-110">Bu anlamda devre dışı bırakma bir kuraldan çok bir istisnadır.</span><span class="sxs-lookup"><span data-stu-id="1d892-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="1d892-111">Bu yordam için devre dışı bırakılabilir bir sürüme sahip bir üretim akışı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1d892-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="1d892-112">Sürümün tamamen geçersiz olduğundan %100 emin olmadan bunu üretim ortamında denemeyin.</span><span class="sxs-lookup"><span data-stu-id="1d892-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="1d892-113">Üretim akışı sürümünü devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="1d892-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="1d892-114">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="1d892-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="1d892-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1d892-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1d892-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d892-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1d892-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1d892-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="1d892-118">Devre Dışı Bırak'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d892-118">Click Deactivate.</span></span>
    * <span data-ttu-id="1d892-119">Bu üretim akışı sürümünün geçersiz olduğundan %100 emin değilseniz devam etmeyin.</span><span class="sxs-lookup"><span data-stu-id="1d892-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="1d892-120">Tamam'a tıklamak tüm kanban kurallarını sona erdirir ve bu üretim akışı sürümünün tüm üretim ve stok yenileme faaliyetlerini anında durdurur.</span><span class="sxs-lookup"><span data-stu-id="1d892-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="1d892-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d892-121">Click OK.</span></span>

