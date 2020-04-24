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
ms.search.form: BenefitFutureLifeEvents
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 134152bb8ae2b9f42b59cc9202e244435a607eba
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230097"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="eee4a-103">Gelecekteki ömür olaylarını konfigüre et</span><span class="sxs-lookup"><span data-stu-id="eee4a-103">Configure future life events</span></span>

<span data-ttu-id="eee4a-104">Gelecekteki ömür olaylarını Dynamics 365 Human Resources'da zamanlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eee4a-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="eee4a-105">**Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **gelecekteki ömür olayları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="eee4a-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="eee4a-106">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="eee4a-106">Select **New**.</span></span>

3. <span data-ttu-id="eee4a-107">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="eee4a-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="eee4a-108">Alan</span><span class="sxs-lookup"><span data-stu-id="eee4a-108">Field</span></span> | <span data-ttu-id="eee4a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="eee4a-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="eee4a-110">Yaşam olayı tarihi</span><span class="sxs-lookup"><span data-stu-id="eee4a-110">Life event date</span></span> | <span data-ttu-id="eee4a-111">Sistem, kayıt süresi boyunca bu tarihe kadar olan tüm olayları işler.</span><span class="sxs-lookup"><span data-stu-id="eee4a-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="eee4a-112">Yaşam olayı günlüğe kaydedildi</span><span class="sxs-lookup"><span data-stu-id="eee4a-112">Life event logged</span></span> | <span data-ttu-id="eee4a-113">Olayın günlüğe girildiği tarih ve saat.</span><span class="sxs-lookup"><span data-stu-id="eee4a-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="eee4a-114">Günlükleri türü</span><span class="sxs-lookup"><span data-stu-id="eee4a-114">Log type</span></span> | <span data-ttu-id="eee4a-115">Eylemin aşağıdakilerden biri olup olmayacağını gösterir:</span><span class="sxs-lookup"><span data-stu-id="eee4a-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="eee4a-116">- **Güncelleştirme** – geçerlilik olaylarını izleyen varolan bir kayıtta yapılan değişiklik</span><span class="sxs-lookup"><span data-stu-id="eee4a-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="eee4a-117">- **Ekle** – yeni bir ömür olayı kaydı oluşturma</span><span class="sxs-lookup"><span data-stu-id="eee4a-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="eee4a-118">Yaşam olayı tür kodu</span><span class="sxs-lookup"><span data-stu-id="eee4a-118">Life event type ID</span></span> | <span data-ttu-id="eee4a-119">Ömür olayı türü benzersiz tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="eee4a-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="eee4a-120">Yaşam olayı türü</span><span class="sxs-lookup"><span data-stu-id="eee4a-120">Life event type</span></span> | <span data-ttu-id="eee4a-121">Bir çalışanın sosyal haklar kaydını güncelleştirmek için bir Catalyst.</span><span class="sxs-lookup"><span data-stu-id="eee4a-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="eee4a-122">Daha fazla ayrıntı için, ömür olayı Tetikleyicileri bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="eee4a-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="eee4a-123">Durum</span><span class="sxs-lookup"><span data-stu-id="eee4a-123">Status</span></span> | <span data-ttu-id="eee4a-124">Ömür olayının işlenip işlenmediği.</span><span class="sxs-lookup"><span data-stu-id="eee4a-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="eee4a-125">Satır</span><span class="sxs-lookup"><span data-stu-id="eee4a-125">Line</span></span> | <span data-ttu-id="eee4a-126">Gelecek ömür olayı satır numarası.</span><span class="sxs-lookup"><span data-stu-id="eee4a-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="eee4a-127">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="eee4a-127">Select **Save**.</span></span> 
