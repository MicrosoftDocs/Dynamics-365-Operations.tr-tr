---
title: Kazanç geçerlilik bitiş tarihlerini yönetme
description: Bu yordam bir yararın süresini uzatmayı veya bitirmeyi, ve bu yarara kaydedilmiş çalışanların kayıt tarihlerini yönetmeyi gösterir.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefit, HcmMassBenefitExpiration, HcmMassBenefitExpirationResults, HcmWorker, HcmWorkerEnrollment, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 153982c926980236d13f09d2de0b9f1bb5038e42
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053045"
---
# <a name="manage-benefit-expiration-dates"></a><span data-ttu-id="f74cf-103">Kazanç geçerlilik bitiş tarihlerini yönetme</span><span class="sxs-lookup"><span data-stu-id="f74cf-103">Manage benefit expiration dates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f74cf-104">Bu yordam bir yararın süresini uzatmayı veya bitirmeyi, ve bu yarara kaydedilmiş çalışanların kayıt tarihlerini yönetmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="f74cf-104">This procedure shows how you can expire or extend a benefit, and manage the enrollment dates of workers that are enrolled in the benefit.</span></span> <span data-ttu-id="f74cf-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="f74cf-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="benefit-expiration-dates"></a><span data-ttu-id="f74cf-106">Kazanç geçerlilik bitiş tarihleri</span><span class="sxs-lookup"><span data-stu-id="f74cf-106">Benefit expiration dates</span></span>

1. <span data-ttu-id="f74cf-107">İnsan kaynakları > Kazançlar > Kazançlar seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="f74cf-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="f74cf-108">Kayıtlı çalışanlar bilgi kutusunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="f74cf-108">Expand the Enrolled workers FactBox.</span></span>
3. <span data-ttu-id="f74cf-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f74cf-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f74cf-110">Eylem Bölmesinde, Kazanç öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f74cf-110">On the Action Pane, click Benefit.</span></span>
5. <span data-ttu-id="f74cf-111">Kazançların geçerlilik süresini sonlandır veya uzat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f74cf-111">Click Expire or extend benefits.</span></span>
6. <span data-ttu-id="f74cf-112">Yeni kazanç bitiş tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="f74cf-112">In the New benefit expiration date field, enter a date and time.</span></span>
7. <span data-ttu-id="f74cf-113">Bitirme'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f74cf-113">Click Expire.</span></span>
8. <span data-ttu-id="f74cf-114">Eylem Bölmesinde, Kazanç öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f74cf-114">On the Action Pane, click Benefit.</span></span>
9. <span data-ttu-id="f74cf-115">Kazanç geçerlilik süresini bitirme ve uzatma sonuçları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f74cf-115">Click Benefit expiration and extension results.</span></span>
10. <span data-ttu-id="f74cf-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f74cf-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="f74cf-117">Listede, Etkilenen çalışanlar bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f74cf-117">In the list, click the Workers affected link.</span></span>
12. <span data-ttu-id="f74cf-118">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f74cf-118">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="f74cf-119">Personel numarası alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f74cf-119">Click to follow the link in the Personnel number field.</span></span>
14. <span data-ttu-id="f74cf-120">Kişisel bilgiler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="f74cf-120">Expand the Personal information section.</span></span>
15. <span data-ttu-id="f74cf-121">Kazançlar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f74cf-121">Click Benefits.</span></span>
16. <span data-ttu-id="f74cf-122">Listede, kazanç kaydını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f74cf-122">In the list, find the benefit and select the record.</span></span> <span data-ttu-id="f74cf-123">Yeni kapsam bitiş tarihi not edin.</span><span class="sxs-lookup"><span data-stu-id="f74cf-123">Note the new coverage end date.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]