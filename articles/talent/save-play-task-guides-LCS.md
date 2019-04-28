---
title: Görev kılavuzlarını LCS'ye kaydetme ve yeniden oynatma
description: Bu konu, görev kılavuzlarını Microsoft Dynamics Lifecycle Services'ye (LCS) kaydetmeyi ve sonra bunları yeniden yürütmeyi açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1128a1d9b54935e44be76bf93549c0cae82e1d38
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "857904"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="c97ff-103">Görev kılavuzlarını LCS'ye kaydetme ve yeniden oynatma</span><span class="sxs-lookup"><span data-stu-id="c97ff-103">Save task guides to LCS and replay them</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c97ff-104">**Ortam ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="c97ff-104">**Environment details**</span></span> 

<span data-ttu-id="c97ff-105">Microsoft Dynamics Lifecycle Services (LCS) için dağıtılmış olan Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="c97ff-105">Microsoft Dynamics 365 for Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="c97ff-106">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="c97ff-106">**Issue**</span></span>

<span data-ttu-id="c97ff-107">Müşteri, yeni görev kayıtlarını LCS projesine kaydetmek ve sonra kaydedilen görev kılavuzlarını yeniden oynatmak istiyor.</span><span class="sxs-lookup"><span data-stu-id="c97ff-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="c97ff-108">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="c97ff-108">**Resolution**</span></span>

<span data-ttu-id="c97ff-109">Bir görev kaydını LCS'ye kaydetmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="c97ff-110">LCS oturum açın ve projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="c97ff-111">**İş süreci modelleyici** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="c97ff-112">"Güncelleştirilmiş BPM deneyimi" içindeki sayfayı görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="c97ff-113">Bir kütüphane seçin ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="c97ff-114">İş süreci modelleyici (BPM) modeli için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="c97ff-115">LCS'den Talent'a oturum açın.</span><span class="sxs-lookup"><span data-stu-id="c97ff-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="c97ff-116">**Arama** alanına, **yardım** girin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="c97ff-117">Lifecycle Services Yardım açılır.</span><span class="sxs-lookup"><span data-stu-id="c97ff-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="c97ff-118">**Yenile** düğmesini Lifecycle Services Yardım yapılandırması için seçin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="c97ff-119">Yeni BPM kütüphaneniz görünür ve etkin olacaktır.</span><span class="sxs-lookup"><span data-stu-id="c97ff-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="c97ff-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c97ff-120">Close the page.</span></span>
10. <span data-ttu-id="c97ff-121">Bir görev kaydı oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="c97ff-121">Create a task recording.</span></span>
11. <span data-ttu-id="c97ff-122">Tamamladığınızda **Lifecycle Services'a kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Lifecycle Services'a kaydet](media/task-guides.png)

12. <span data-ttu-id="c97ff-124">Görev kaydının kaydedileceği düğümü ve BPM kütüphanesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="c97ff-125">LCS'den bir görev kılavuzunu yeniden yürütmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="c97ff-126">Görev kaydediciyi başlatın.</span><span class="sxs-lookup"><span data-stu-id="c97ff-126">Start Task recorder.</span></span>
2. <span data-ttu-id="c97ff-127">**LCS'ten aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="c97ff-128">Kaydedilmiş görev kılavuzuna sahip kütüphaneyi ve BPM düğümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="c97ff-129">Görev kılavuzunu açın.</span><span class="sxs-lookup"><span data-stu-id="c97ff-129">Open the task guide.</span></span>
