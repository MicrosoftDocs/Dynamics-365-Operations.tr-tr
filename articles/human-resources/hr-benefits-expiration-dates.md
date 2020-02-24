---
title: Kazanç geçerlilik bitiş tarihlerini yönetme
description: Bu yordam bir yararın süresini uzatmayı veya bitirmeyi, ve bu yarara kaydedilmiş çalışanların kayıt tarihlerini yönetmeyi gösterir.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefit, HcmMassBenefitExpiration, HcmMassBenefitExpirationResults, HcmWorker, HcmWorkerEnrollment
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 9a1e815e51b4dc232b546294d66337f80dbc30bc
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010928"
---
# <a name="manage-benefit-expiration-dates"></a><span data-ttu-id="cfa26-103">Kazanç geçerlilik bitiş tarihlerini yönetme</span><span class="sxs-lookup"><span data-stu-id="cfa26-103">Manage benefit expiration dates</span></span>

<span data-ttu-id="cfa26-104">Bu yordam bir yararın süresini uzatmayı veya bitirmeyi, ve bu yarara kaydedilmiş çalışanların kayıt tarihlerini yönetmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="cfa26-104">This procedure shows how you can expire or extend a benefit, and manage the enrollment dates of workers that are enrolled in the benefit.</span></span> <span data-ttu-id="cfa26-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="cfa26-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="benefit-expiration-dates"></a><span data-ttu-id="cfa26-106">Kazanç geçerlilik bitiş tarihleri</span><span class="sxs-lookup"><span data-stu-id="cfa26-106">Benefit expiration dates</span></span>

1. <span data-ttu-id="cfa26-107">İnsan kaynakları > Kazançlar > Kazançlar seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="cfa26-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="cfa26-108">Kayıtlı çalışanlar bilgi kutusunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="cfa26-108">Expand the Enrolled workers FactBox.</span></span>
3. <span data-ttu-id="cfa26-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cfa26-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cfa26-110">Eylem Bölmesinde, Kazanç öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfa26-110">On the Action Pane, click Benefit.</span></span>
5. <span data-ttu-id="cfa26-111">Kazançların geçerlilik süresini sonlandır veya uzat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfa26-111">Click Expire or extend benefits.</span></span>
6. <span data-ttu-id="cfa26-112">Yeni kazanç bitiş tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="cfa26-112">In the New benefit expiration date field, enter a date and time.</span></span>
7. <span data-ttu-id="cfa26-113">Bitirme'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cfa26-113">Click Expire.</span></span>
8. <span data-ttu-id="cfa26-114">Eylem Bölmesinde, Kazanç öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfa26-114">On the Action Pane, click Benefit.</span></span>
9. <span data-ttu-id="cfa26-115">Kazanç geçerlilik süresini bitirme ve uzatma sonuçları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfa26-115">Click Benefit expiration and extension results.</span></span>
10. <span data-ttu-id="cfa26-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="cfa26-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="cfa26-117">Listede, Etkilenen çalışanlar bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfa26-117">In the list, click the Workers affected link.</span></span>
12. <span data-ttu-id="cfa26-118">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cfa26-118">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="cfa26-119">Personel numarası alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfa26-119">Click to follow the link in the Personnel number field.</span></span>
14. <span data-ttu-id="cfa26-120">Kişisel bilgiler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="cfa26-120">Expand the Personal information section.</span></span>
15. <span data-ttu-id="cfa26-121">Kazançlar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cfa26-121">Click Benefits.</span></span>
16. <span data-ttu-id="cfa26-122">Listede, kazanç kaydını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cfa26-122">In the list, find the benefit and select the record.</span></span> <span data-ttu-id="cfa26-123">Yeni kapsam bitiş tarihi not edin.</span><span class="sxs-lookup"><span data-stu-id="cfa26-123">Note the new coverage end date.</span></span>

