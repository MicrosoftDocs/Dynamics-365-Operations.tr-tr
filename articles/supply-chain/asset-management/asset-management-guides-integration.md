---
title: Dynamics 365 Supply Chain Management'ı (Varlık yönetimi) Dynamics 365 Guides ile tümleştirme
description: Bu konu, günlük servis ve bakım iş akışlarınızda karma gerçeklik kılavuzlarından yararlanmak için Microsoft Dynamics 365 Supply Chain Management'taki Varlık yönetimi modülünün Dynamics 365 Guides ile nasıl tümleştirileceğini açıklar.
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: ae26012d236a44bfa0c8453bdc660671ddee82a4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000296"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="07918-103">Dynamics 365 Supply Chain Management'ı (Varlık yönetimi) Dynamics 365 Guides ile tümleştirme</span><span class="sxs-lookup"><span data-stu-id="07918-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="07918-104">Günlük servis ve bakım iş akışlarınızda karma gerçeklik kılavuzlarından yararlanmak için Microsoft Dynamics 365 Supply Chain Management'taki **Varlık yönetimi** modülünü Dynamics 365 Guides ile tümleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="07918-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="07918-105">Bir kılavuz Varlık yönetimi iş emriyle ilişkilendirilmişse, Supply Chain Management (Dynamics 365) mobil uygulamasında iş emrinin bakım denetim listesini açan bir çalışan bir kılavuzun kullanılabilir olduğunu görür.</span><span class="sxs-lookup"><span data-stu-id="07918-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="07918-106">Çalışan daha sonra kılavuzu Dynamics 365 Guides HoloLens uygulamasında bulabilir ve açabilir.</span><span class="sxs-lookup"><span data-stu-id="07918-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="07918-107">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="07918-107">Prerequisites</span></span>

<span data-ttu-id="07918-108">Kılavuzları Varlık yönetimi iş emirlerine ekleyebilmeniz için önce aşağıdaki önkoşulları tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="07918-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="07918-109">[Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) sürüm 10.0.9 veya üstünü kurun.</span><span class="sxs-lookup"><span data-stu-id="07918-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="07918-110">[Supply Chain Management uygulamaları için çift yazmayı açın](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="07918-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="07918-111">**MRGuidesFeature** özelliği için [sınırlı dağıtımı açın](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features).</span><span class="sxs-lookup"><span data-stu-id="07918-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="07918-112">(Üretim ortamları için, kiracınızın sınırlı dağırım grubuna eklenmesini sağlamak için öncelikle bir destek bileti göndermeniz gerekir.)</span><span class="sxs-lookup"><span data-stu-id="07918-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="07918-113">**Lisans yapılandırması** sayfasında [aşağıdaki yapılandırma anahtarlarını açın](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) :</span><span class="sxs-lookup"><span data-stu-id="07918-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="07918-114">Varlık yönetimi \>Varlık yönetimi karma gerçeklik</span><span class="sxs-lookup"><span data-stu-id="07918-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="07918-115">Karma gerçeklik \> Karma gerçeklik kılavuzu</span><span class="sxs-lookup"><span data-stu-id="07918-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="07918-116">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) sürüm 200.0.0.96 veya üstünü kurun.</span><span class="sxs-lookup"><span data-stu-id="07918-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="07918-117">Dynamics 365 Guides'ı Varlık yönetimi ile kullanma</span><span class="sxs-lookup"><span data-stu-id="07918-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="07918-118">Bir kılavuzu ilişkilendirmek için, Varlık yönetimindeki bir bakım denetim listesi satırını kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="07918-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="07918-119">İlişkilendirmeyi bakım denetim listesi şablonu, bakım iş türü veya iş emri aracılığıyla oluşturabilirsiniz, çünkü her üçü de bakım denetim listesi satırları içerir.</span><span class="sxs-lookup"><span data-stu-id="07918-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="07918-120">Bir şablon onu kullanan tüm bakım işi türleriyle ilişkilendirilebileceğinden bir şablon kullanarak zamandan tasarruf edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="07918-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="07918-121">Örneğin, bir bakım işi türü ile ilişkilendirilmiş bir kılavuz, iş türünü belirten tüm iş emirleriyle otomatik olarak ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="07918-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="07918-122">Diğer taraftan, bir iş emriyle doğrudan ilişkilendirilmiş olan bir kılavuz yalnızca o iş emri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="07918-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="07918-123">Kılavuzu bakım denetim listesi şablonuyla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="07918-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="07918-124">Kılavuzu bakım denetim listesi şablonuyla ilişkilendirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="07918-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="07918-125">Dynamics 365 Guides PC ve HoloLens uygulamalarını kullanarak bir kılavuz oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07918-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="07918-126">Kılavuz oluşturma hakkında daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="07918-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="07918-127">Kılavuz oluşturmak için PC uygulaması kullanma</span><span class="sxs-lookup"><span data-stu-id="07918-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="07918-128">Hologramlarınızı yerleştirmek için HoloLens uygulaması kullanma</span><span class="sxs-lookup"><span data-stu-id="07918-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="07918-129">Supply Chain Management'ta [bir bakım denetim listesi şablonu oluşturun](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span><span class="sxs-lookup"><span data-stu-id="07918-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="07918-130">Oluşturduğunuz kılavuzu yeni bakım denetim listesi şablonundaki bir bakım denetim listesi satırı ile ilişkilendirin:</span><span class="sxs-lookup"><span data-stu-id="07918-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="07918-131">**Bakım denetim listesi satırları** hızlı sekmesinde, kılavuzu ilişkilendirmek istediğiniz satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="07918-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="07918-132">**İlişkili kılavuzlar** hızlı sekmesinde, **Kılavuz Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="07918-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="07918-133">![Kılavuzu bakım denetim listesi satırıyla ilişkilendirme](media/am-guides-integration-add-guide.png "Kılavuzu bakım denetim listesi satırıyla ilişkilendirme")</span><span class="sxs-lookup"><span data-stu-id="07918-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="07918-134">**Ad** alanında bir kılavuz seçin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="07918-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="07918-135">![Ad alanında bir kılavuz seçme](media/am-guides-integration-select-guide.png "Ad alanında bir kılavuz seçme")</span><span class="sxs-lookup"><span data-stu-id="07918-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="07918-136">Bakım denetim listesi şablonunu bir iş türüyle ilişkilendirme:</span><span class="sxs-lookup"><span data-stu-id="07918-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="07918-137">[Bir bakım işi türü oluşturun](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) veya varolan bir bakım işi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="07918-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="07918-138">Eylem Bölmesinde **Bakım işi türü varsayılanları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="07918-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="07918-139">![Bakım işi türü varsayılanları düğmesi](media/am-guides-integration-job-defaults.png "Bakım işi türü varsayılanları düğmesi")</span><span class="sxs-lookup"><span data-stu-id="07918-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="07918-140">Bir satır oluşturun ve **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="07918-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="07918-141">![Satır oluşturma](media/am-guides-integration-add-line.png "Satır oluşturma")</span><span class="sxs-lookup"><span data-stu-id="07918-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="07918-142">Eylem Bölmesinde, **Bakım denetim listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="07918-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="07918-143">![Bakım denetim listesi düğmesi](media/am-guides-integration-maintenance-checklist.png "Bakım denetim listesi düğmesi")</span><span class="sxs-lookup"><span data-stu-id="07918-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="07918-144">**Bakım denetim listesi satırları** hızlı sekmesinde, bir satır ekleyin ve sonra **Tür** alanının değerini **Şablon** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="07918-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="07918-145">![Tür değerini değiştirme](media/am-guides-integration-checklist-lines.png "Tür değerini değiştirme")</span><span class="sxs-lookup"><span data-stu-id="07918-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="07918-146">**Satır ayrıntıları** hızlı sekmesinde, **Şablon** alanında, kılavuzla ilişkilendirdiğiniz şablonu ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="07918-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="07918-147">![Şablon seçme](media/am-guides-integration-checklist-line-details.png "Şablon seçme")</span><span class="sxs-lookup"><span data-stu-id="07918-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="07918-148">[Bir iş emri oluşturun ](work-orders/manually-created-workorders.md#create-work-order) ve ardından kılavuzla ilişkilendirdiğiniz bakım denetim listesi şablonunu kullanan bakım işi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="07918-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="07918-149">Kılavuz, iş emriyle otomatik olarak ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="07918-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="07918-150">![Bakım işi türü seçme](media/am-guides-integration-create-work-order.png "Bakım işi türü seçme")</span><span class="sxs-lookup"><span data-stu-id="07918-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="07918-151">İş emri ve çalışanlar ile ilişkilendirilmiş kılavuzu görüntüleyin:</span><span class="sxs-lookup"><span data-stu-id="07918-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="07918-152">İş emrine erişmek için [Varlık yönetimi mobil çalışma alanını](asset-management-mobile-workspace.md) açın.</span><span class="sxs-lookup"><span data-stu-id="07918-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="07918-153">İş emri için [bakım denetim listesini açın](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job).</span><span class="sxs-lookup"><span data-stu-id="07918-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="07918-154">İlişkili kılavuzu görmek için bir denetim listesi satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="07918-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="07918-155">![Denetim listesi satırıyla ilişkilendirilmiş kılavuz](media/am-guides-integration-show-guide.png "Denetim listesi satırıyla ilişkilendirilmiş kılavuz")</span><span class="sxs-lookup"><span data-stu-id="07918-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="07918-156">Kılavuzu HoloLens'te açın.</span><span class="sxs-lookup"><span data-stu-id="07918-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="07918-157">![Kılavuzu HoloLens'te açın](media/am-guides-integration-hololens-select.png "Kılavuzu HoloLens'te açma")</span><span class="sxs-lookup"><span data-stu-id="07918-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="07918-158">Ayrıca, bir kılavuzu doğrudan bir iş emrinin veya iş türünün bakım denetim listesinde ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="07918-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07918-159">Bir bakım denetim listesi şablonunu varsayılan bir bakım işi türü ile ilişkilendirdiğinizde, şablonla bağlantılı olan kılavuzun **Bakım işi türü varsayılanları** sayfasındaki **İlişkilendirilmiş kılavuzlar** hızlı sekmesinde görünmediğiyle ilgili bilinen bir sorun vardır.</span><span class="sxs-lookup"><span data-stu-id="07918-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="07918-160">Ancak, bu iş türü **İlişkilendirilmiş kılavuzlar** hızlı sekmesindeki bir iş emrine uygulandıktan sonra kılavuz görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="07918-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="07918-161">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="07918-161">See also</span></span>

- [<span data-ttu-id="07918-162">Çift yazmaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="07918-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="07918-163">Varlık yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="07918-163">Asset management overview</span></span>](index.md)
