---
title: Görev kılavuzlarını LCS'ye kaydetme ve yeniden oynatma
description: Bu konu, görev kılavuzlarını Microsoft Dynamics Lifecycle Services'ye (LCS) kaydetmeyi ve sonra bunları yeniden yürütmeyi açıklar.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c81c345932e0e3dce4b13104222ed9f668a3c460
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114658"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="c1fd1-103">Görev kılavuzlarını LCS'ye kaydetme ve yeniden oynatma</span><span class="sxs-lookup"><span data-stu-id="c1fd1-103">Save task guides to LCS and replay them</span></span>

<span data-ttu-id="c1fd1-104">**Ortam ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="c1fd1-104">**Environment details**</span></span> 

<span data-ttu-id="c1fd1-105">Microsoft Dynamics Lifecycle Services (LCS) için dağıtılmış olan Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="c1fd1-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="c1fd1-106">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="c1fd1-106">**Issue**</span></span>

<span data-ttu-id="c1fd1-107">Müşteri, yeni görev kayıtlarını LCS projesine kaydetmek ve sonra kaydedilen görev kılavuzlarını yeniden oynatmak istiyor.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="c1fd1-108">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="c1fd1-108">**Resolution**</span></span>

<span data-ttu-id="c1fd1-109">Bir görev kaydını LCS'ye kaydetmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="c1fd1-110">LCS oturum açın ve projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="c1fd1-111">**İş süreci modelleyici** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="c1fd1-112">"Güncelleştirilmiş BPM deneyimi" içindeki sayfayı görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="c1fd1-113">Bir kütüphane seçin ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="c1fd1-114">İş süreci modelleyici (BPM) modeli için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="c1fd1-115">LCS'den İnsan Kaynakları oturum açın.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="c1fd1-116">**Arama** alanına, **yardım** girin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="c1fd1-117">Lifecycle Services Yardım açılır.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="c1fd1-118">**Yenile** düğmesini Lifecycle Services Yardım yapılandırması için seçin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="c1fd1-119">Yeni BPM kütüphaneniz görünür ve etkin olacaktır.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="c1fd1-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-120">Close the page.</span></span>
10. <span data-ttu-id="c1fd1-121">Bir görev kaydı oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-121">Create a task recording.</span></span>
11. <span data-ttu-id="c1fd1-122">Tamamladığınızda **Lifecycle Services'a kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Lifecycle Services'a kaydet](media/task-guides.png)

12. <span data-ttu-id="c1fd1-124">Görev kaydının kaydedileceği düğümü ve BPM kütüphanesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="c1fd1-125">LCS'den bir görev kılavuzunu yeniden yürütmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="c1fd1-126">Görev kaydediciyi başlatın.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-126">Start Task recorder.</span></span>
2. <span data-ttu-id="c1fd1-127">**LCS'ten aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="c1fd1-128">Kaydedilmiş görev kılavuzuna sahip kütüphaneyi ve BPM düğümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="c1fd1-129">Görev kılavuzunu açın.</span><span class="sxs-lookup"><span data-stu-id="c1fd1-129">Open the task guide.</span></span>
