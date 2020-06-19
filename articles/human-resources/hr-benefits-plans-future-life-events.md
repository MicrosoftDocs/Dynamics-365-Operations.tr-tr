---
title: Gelecekteki ömür olaylarını konfigüre et
description: Gelecekteki ömür olaylarını Dynamics 365 Human Resources'da zamanlayabilirsiniz.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78c65faa4ae0f428184700a912998e9dded026c5
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429417"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="ab2d1-103">Gelecekteki ömür olaylarını konfigüre et</span><span class="sxs-lookup"><span data-stu-id="ab2d1-103">Configure future life events</span></span>

<span data-ttu-id="ab2d1-104">Gelecekteki ömür olaylarını Dynamics 365 Human Resources'da zamanlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab2d1-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="ab2d1-105">**Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **gelecekteki ömür olayları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="ab2d1-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="ab2d1-106">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ab2d1-106">Select **New**.</span></span>

3. <span data-ttu-id="ab2d1-107">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="ab2d1-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ab2d1-108">Alan</span><span class="sxs-lookup"><span data-stu-id="ab2d1-108">Field</span></span> | <span data-ttu-id="ab2d1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab2d1-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ab2d1-110">Yaşam olayı tarihi</span><span class="sxs-lookup"><span data-stu-id="ab2d1-110">Life event date</span></span> | <span data-ttu-id="ab2d1-111">Sistem, kayıt süresi boyunca bu tarihe kadar olan tüm olayları işler.</span><span class="sxs-lookup"><span data-stu-id="ab2d1-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="ab2d1-112">Yaşam olayı günlüğe kaydedildi</span><span class="sxs-lookup"><span data-stu-id="ab2d1-112">Life event logged</span></span> | <span data-ttu-id="ab2d1-113">Olayın günlüğe girildiği tarih ve saat.</span><span class="sxs-lookup"><span data-stu-id="ab2d1-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="ab2d1-114">Günlükleri türü</span><span class="sxs-lookup"><span data-stu-id="ab2d1-114">Log type</span></span> | <span data-ttu-id="ab2d1-115">Eylemin aşağıdakilerden biri olup olmayacağını gösterir:</span><span class="sxs-lookup"><span data-stu-id="ab2d1-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="ab2d1-116">- **Güncelleştirme** – geçerlilik olaylarını izleyen varolan bir kayıtta yapılan değişiklik</span><span class="sxs-lookup"><span data-stu-id="ab2d1-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="ab2d1-117">- **Ekle** – yeni bir ömür olayı kaydı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ab2d1-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="ab2d1-118">Yaşam olayı tür kodu</span><span class="sxs-lookup"><span data-stu-id="ab2d1-118">Life event type ID</span></span> | <span data-ttu-id="ab2d1-119">Ömür olayı türü benzersiz tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ab2d1-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="ab2d1-120">Yaşam olayı türü</span><span class="sxs-lookup"><span data-stu-id="ab2d1-120">Life event type</span></span> | <span data-ttu-id="ab2d1-121">Bir çalışanın sosyal haklar kaydını güncelleştirmek için bir Catalyst.</span><span class="sxs-lookup"><span data-stu-id="ab2d1-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="ab2d1-122">Daha fazla ayrıntı için, ömür olayı Tetikleyicileri bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="ab2d1-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="ab2d1-123">Durum</span><span class="sxs-lookup"><span data-stu-id="ab2d1-123">Status</span></span> | <span data-ttu-id="ab2d1-124">Ömür olayının işlenip işlenmediği.</span><span class="sxs-lookup"><span data-stu-id="ab2d1-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="ab2d1-125">Satır</span><span class="sxs-lookup"><span data-stu-id="ab2d1-125">Line</span></span> | <span data-ttu-id="ab2d1-126">Gelecek ömür olayı satır numarası.</span><span class="sxs-lookup"><span data-stu-id="ab2d1-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="ab2d1-127">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ab2d1-127">Select **Save**.</span></span> 
