--- 
title: "Üretim akışı sürümü için bir bitiş tarihi tanımlama"
description: "Üretim akışı sürümünün geçerliliğini ve işlenmesini verilen tarihte sona erdirmek için veya etkin sürümü yeni bir sürümle değiştirmeyi planlamak için, sürümde bitiş tarihini ayarlamanız gerekir."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6fabeb31720a60bf97d08dabf8ed87ac6af7cbf7
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="54cd1-103">Üretim akışı sürümü için bir bitiş tarihi tanımlama</span><span class="sxs-lookup"><span data-stu-id="54cd1-103">Define an expiry date for a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54cd1-104">Üretim akışı sürümünün geçerliliğini ve işlenmesini verilen tarihte sona erdirmek için veya etkin sürümü yeni bir sürümle değiştirmeyi planlamak için, sürümde bitiş tarihini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="54cd1-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="54cd1-105">Sürümü devre dışı bırakmak gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="54cd1-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="54cd1-106">Üretim akışı sürümünü sonlandırmak için bir bitiş tarihi ayarlama</span><span class="sxs-lookup"><span data-stu-id="54cd1-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="54cd1-107">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="54cd1-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="54cd1-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="54cd1-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="54cd1-109">Zaten tanımlanmış bir sürüme sahip bir üretim akışını seçin.</span><span class="sxs-lookup"><span data-stu-id="54cd1-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="54cd1-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54cd1-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="54cd1-111">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54cd1-111">Click Edit.</span></span>
5. <span data-ttu-id="54cd1-112">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="54cd1-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="54cd1-113">Bitiş tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="54cd1-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="54cd1-114">Bitiş tarihi için yeni bir sürüm başlamaz veya etkin hale gelmez.</span><span class="sxs-lookup"><span data-stu-id="54cd1-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="54cd1-115">Bu üretim akışı için görevleri oluşturmak veya başlatmak artık mümkün olmaz.</span><span class="sxs-lookup"><span data-stu-id="54cd1-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="54cd1-116">Başlatılan işleri, bitiş tarihinden sonra da tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="54cd1-116">You can still complete started jobs after the expiration date.</span></span>  


