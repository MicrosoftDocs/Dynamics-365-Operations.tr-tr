---
title: "Onarım yönetimi"
description: "Geçmişte başarılı olmuş önerilen çözümlerle yardım etmek üzere sorunları sistematik olarak gruplayın."
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 32202344f77352cd3f9c1a807d14192a9bf0d9e6
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="repair-management"></a><span data-ttu-id="0fb44-103">Onarım yönetimi</span><span class="sxs-lookup"><span data-stu-id="0fb44-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0fb44-104">Onarım yönetimi için sorunları sistematik olarak gruplandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0fb44-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="0fb44-105">Bu, geçmişte başarılı olmuş önerilen çözümlerle yardımcı olunmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="0fb44-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="0fb44-106">Belirtileri, tanıları ve çözüm ayarlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="0fb44-107">Onarım için benzer bir madde aldığınızda, bunların tümü daha sonra uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="0fb44-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="0fb44-108">Bir onarım sorununun ilerlemesini takip edebilmek için onarım aşamaları da ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0fb44-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="0fb44-109">Onarım yönetimi ayarlama</span><span class="sxs-lookup"><span data-stu-id="0fb44-109">Setting up repair management</span></span>

<span data-ttu-id="0fb44-110">Belirtileri, tanıları ve onarım çözümünü belirtmek için kullanılacak bilgileri girmek için aşağıdaki ayar formlarını kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0fb44-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

1.  <span data-ttu-id="0fb44-111">**Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Durumlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-111">Click **Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>

2.  <span data-ttu-id="0fb44-112">**Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Belirti alanları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-112">Click **Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>

3.  <span data-ttu-id="0fb44-113">**Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Tanı alanları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-113">Click **Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>

4.  <span data-ttu-id="0fb44-114">**Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Çözümler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-114">Click **Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>

5.  <span data-ttu-id="0fb44-115">**Servis yönetimi** \> **Kurulum** \> **Onarım** \> **Onarım aşamaları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-115">Click **Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="0fb44-116">Belirtiler ve durumlar</span><span class="sxs-lookup"><span data-stu-id="0fb44-116">Symptoms and conditions</span></span>

<span data-ttu-id="0fb44-117">Belirtiler, müşterinin sorunu nasıl tanımladığıdır.</span><span class="sxs-lookup"><span data-stu-id="0fb44-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="0fb44-118">Belirtiler onarım gerektiğini gösteren müşteri gözlemlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="0fb44-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="0fb44-119">Belirti alanları, belirti kodları ve koşulları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0fb44-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="0fb44-120">Belirti alanı arıza alanını kapsar ve belirti kodu da arıza belirtisini kapsar.</span><span class="sxs-lookup"><span data-stu-id="0fb44-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="0fb44-121">Durum, sorun oluştuğundaki durumu veya ortamı açıklar.</span><span class="sxs-lookup"><span data-stu-id="0fb44-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="0fb44-122">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="0fb44-122">**Example**</span></span>

<span data-ttu-id="0fb44-123">Bir bilgisayar, uzun süreli kullanımdan sonra sabit disk arızalandığı için onarıma alınır.</span><span class="sxs-lookup"><span data-stu-id="0fb44-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="0fb44-124">Sabit disk arızası bir mavi ekran hatasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="0fb44-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="0fb44-125">Bilgisayarı alan teknisyen aşağıdaki belirtileri ve durumları girer:</span><span class="sxs-lookup"><span data-stu-id="0fb44-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="0fb44-126">Belirti alanı sabit disktir</span><span class="sxs-lookup"><span data-stu-id="0fb44-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="0fb44-127">Belirti kodu mavi ekran hatasıdır</span><span class="sxs-lookup"><span data-stu-id="0fb44-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="0fb44-128">Durum sabit diskin uzun süreli kullanımı sonrasında arızalanmasıdır</span><span class="sxs-lookup"><span data-stu-id="0fb44-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="0fb44-129">Tanı ve çözümler</span><span class="sxs-lookup"><span data-stu-id="0fb44-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="0fb44-130">Tanı ve çözüm alanları onarım açısından olan ifadelerdir.</span><span class="sxs-lookup"><span data-stu-id="0fb44-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="0fb44-131">Bunlar, bir teknisyenin sorunu incelemek için takip ettiği adımlardır.</span><span class="sxs-lookup"><span data-stu-id="0fb44-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="0fb44-132">Tanı alanı, sorunu çözmek için oluşması gereken operasyonu kapsar.</span><span class="sxs-lookup"><span data-stu-id="0fb44-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="0fb44-133">Tanı kodu sorunun nasıl ele alındığını ifade eder ve çözüm maddenin onarılması, değiştirilmesi veya siparişin müşteri tarafından iptal edilmesi şeklinde olabilir.</span><span class="sxs-lookup"><span data-stu-id="0fb44-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="0fb44-134">Örneğin, bilgisayar onarılmışsa, tanı alanı "arızalı parça", tanı kodu "takılan yeni video kartı" ve çözüm "değiştirildi" olabilir.</span><span class="sxs-lookup"><span data-stu-id="0fb44-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="0fb44-135">Onarım aşamaları</span><span class="sxs-lookup"><span data-stu-id="0fb44-135">Repair stages</span></span>

<span data-ttu-id="0fb44-136">Onarım aşamaları onarım sürecinin ilerlemesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0fb44-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="0fb44-137">Onarım aşaması, onarım satırının tamamlandığını ve tamamlanma tarihi ve saatinin kaydedildiğini gösteren bir **Bitti** kapatma parametresi taşır.</span><span class="sxs-lookup"><span data-stu-id="0fb44-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="0fb44-138">Onarım yönetimini ayarlama</span><span class="sxs-lookup"><span data-stu-id="0fb44-138">Applying repair management</span></span>

<span data-ttu-id="0fb44-139">Bir maddeye onarım yönetim uygulamak için maddenin bir servis siparişinde bir servis kapsamındaki parça ilişkisiyle ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0fb44-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="0fb44-140">Ardından servis siparişinden, geçerli sorun hakkındaki bilgiler içeren bir onarım satırı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0fb44-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="0fb44-141">Onarım satırında, onarımda olan servis kapsamındaki parçayı ve sistem, tanı ve uygulama hakkındaki bilgileri tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="0fb44-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="0fb44-142">Ayrıca onarım satırı için bir not da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0fb44-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="0fb44-143">Onarım işlemindeki her adım için onarım satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0fb44-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="0fb44-144">Bir servis siparişinde onarım satırı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0fb44-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="0fb44-145">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-145">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="0fb44-146">Onarım gerektiren servis kapsamındaki parça içeren servis siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="0fb44-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="0fb44-147">**Onarım** \> **Onarım satırları**'nı tıklayarak **Onarım satırları** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-147">Click **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="0fb44-148">Yeni bir satır oluşturmak için Ctrl+N tuşlarına basın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-148">Press CTRL+N to create a new line.</span></span>

5.  <span data-ttu-id="0fb44-149">Bir servis kapsamında parça seçin.</span><span class="sxs-lookup"><span data-stu-id="0fb44-149">Select a service object.</span></span> <span data-ttu-id="0fb44-150">Servis siparişinde bir parça ilişkisiyle ayarlanmış her türlü servis kapsamındaki parçayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0fb44-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="0fb44-151">Onarım satırında ilişkili olan önayarlı belirti, tanı ve uygulama değerlerinden birini seçin ve gerekirse onarım satırında bir not oluşturmak için **Not** sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then click the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="0fb44-152">Yeni onarım satırını kaydetmek için CTRL+S tuşlarına basın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-152">Press CTRL+S to save the new repair line.</span></span> <span data-ttu-id="0fb44-153">**Onarım satırları** formunun **Genel** sekmesindeki **Oluşturma tarihi ve saati** alanı formun kaydedildiği saatle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="0fb44-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="0fb44-154">İlerlemeyi izleme ve bir onarım sorununu çözümleme</span><span class="sxs-lookup"><span data-stu-id="0fb44-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="0fb44-155">Onarımın ilerlemesini izlemek için bir onarım satırının onarım aşamalarını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0fb44-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="0fb44-156">Bir onarım sorunu giderildiğinde, onarım satırını kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0fb44-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="0fb44-157">Onarım aşamasını **Bitti** özelliği etkinleştirilmiş bir aşamaya ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="0fb44-158">Geçerli tarih ve saat, satırdaki tamamlanma zamanı olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="0fb44-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="0fb44-159">Çözülen bir sorunun onarım satırını kapatma</span><span class="sxs-lookup"><span data-stu-id="0fb44-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="0fb44-160">**Onarım satırları** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="0fb44-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="0fb44-161">Bu konunun başlarında bir onarım satırı oluşturmak için verilen yordamı takip edin.</span><span class="sxs-lookup"><span data-stu-id="0fb44-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="0fb44-162">Kapatmak istediğiniz onarım sorununu içeren onarım satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="0fb44-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="0fb44-163">**Onarım aşaması** alanından, **Bitti** özelliği etkinleştirilmiş bir aşama seçin.</span><span class="sxs-lookup"><span data-stu-id="0fb44-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  



