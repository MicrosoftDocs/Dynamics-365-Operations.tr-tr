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
ms.openlocfilehash: 6ee3556e033cf298bbd5102746d2b57884f5e6d0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898076"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="6f5cf-103">Görev kılavuzlarını LCS'ye kaydetme ve yeniden oynatma</span><span class="sxs-lookup"><span data-stu-id="6f5cf-103">Save task guides to LCS and replay them</span></span>

<span data-ttu-id="6f5cf-104">**Ortam ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="6f5cf-104">**Environment details**</span></span> 

<span data-ttu-id="6f5cf-105">Microsoft Dynamics Lifecycle Services (LCS) için dağıtılmış olan Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="6f5cf-105">Microsoft Dynamics 365 Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="6f5cf-106">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="6f5cf-106">**Issue**</span></span>

<span data-ttu-id="6f5cf-107">Müşteri, yeni görev kayıtlarını LCS projesine kaydetmek ve sonra kaydedilen görev kılavuzlarını yeniden oynatmak istiyor.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="6f5cf-108">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="6f5cf-108">**Resolution**</span></span>

<span data-ttu-id="6f5cf-109">Bir görev kaydını LCS'ye kaydetmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="6f5cf-110">LCS oturum açın ve projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="6f5cf-111">**İş süreci modelleyici** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="6f5cf-112">"Güncelleştirilmiş BPM deneyimi" içindeki sayfayı görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="6f5cf-113">Bir kütüphane seçin ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="6f5cf-114">İş süreci modelleyici (BPM) modeli için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="6f5cf-115">LCS'den Talent'a oturum açın.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="6f5cf-116">**Arama** alanına, **yardım** girin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="6f5cf-117">Lifecycle Services Yardım açılır.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="6f5cf-118">**Yenile** düğmesini Lifecycle Services Yardım yapılandırması için seçin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="6f5cf-119">Yeni BPM kütüphaneniz görünür ve etkin olacaktır.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="6f5cf-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-120">Close the page.</span></span>
10. <span data-ttu-id="6f5cf-121">Bir görev kaydı oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-121">Create a task recording.</span></span>
11. <span data-ttu-id="6f5cf-122">Tamamladığınızda **Lifecycle Services'a kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Lifecycle Services'a kaydet](media/task-guides.png)

12. <span data-ttu-id="6f5cf-124">Görev kaydının kaydedileceği düğümü ve BPM kütüphanesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="6f5cf-125">LCS'den bir görev kılavuzunu yeniden yürütmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="6f5cf-126">Görev kaydediciyi başlatın.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-126">Start Task recorder.</span></span>
2. <span data-ttu-id="6f5cf-127">**LCS'ten aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="6f5cf-128">Kaydedilmiş görev kılavuzuna sahip kütüphaneyi ve BPM düğümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="6f5cf-129">Görev kılavuzunu açın.</span><span class="sxs-lookup"><span data-stu-id="6f5cf-129">Open the task guide.</span></span>
