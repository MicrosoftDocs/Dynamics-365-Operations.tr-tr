---
title: Bakım talepleri oluştur
description: Bu konuda Kıymet Yönetimi'nde bakım talepleri oluşturma işlemi açıklanmaktadır.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: af67d320f14fc6c3d28eec47de402ba645eea06d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836794"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="9d3ff-103">Bakım talepleri oluştur</span><span class="sxs-lookup"><span data-stu-id="9d3ff-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9d3ff-104">Bakım görevlileri veya üretim çalışanları, ekipmanların onarımını gerektiğini keşfeder ancak onarım işi hemen yapılamazsa bakım talepleri kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="9d3ff-105">**Örnek:** Bir bakım görevlisi bir onarım yaparken, aynı bölgedeki başka bir varlığa hizmet verilmesi gerektiğini keşfeder.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="9d3ff-106">Ancak, bakım görevlisinin onarım işini yapmak için zamanı veya gerekli yedek parçaları yoktur.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="9d3ff-107">Bu nedenle, o varlık üzerinde bir bakım talebi oluşturur ve sorunun kısa bir açıklamasını girer.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="9d3ff-108">**Tüm varlıklar** ya da **Etkin varlıklar** sayfasının sağ tarafındaki **İlgili bilgiler** panelinin **Etkin bakım talepleri** bölümünde (**Varlık yönetimi** \> **Ortak** \> **Varlıklar** \> **Tüm varlıklar** veya **Etkin varlıklar**) seçili varlığa iliştirilmiş etkin bakım taleplerinin gösterir.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="9d3ff-109">**Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Tüm bakım talepleri** ya da **Etkin bakım talepleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="9d3ff-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-110">Select **New**.</span></span>
3. <span data-ttu-id="9d3ff-111">**İstek oluştur** iletişim kutusunda **Bakım talebi türü** alanında bakım talebi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="9d3ff-112">Varsayılan tür önerilir.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-112">A default type is suggested.</span></span>
4. <span data-ttu-id="9d3ff-113">**Açıklama** alanına, bakım talebini kısaca açıklayan bir ad veya başlık girin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="9d3ff-114">**İşlem yapılacak yerleşim** ve **Varlık** alanlarında, gerektiği gibi işlem yapılacak yerleşim ya da bir varlık veya işlem yapılacak yerleşim ve bir varlığın birleşimini seçin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="9d3ff-115">Bir varlık seçmeden bir bakım talebi oluşturabilir ve varlık, bakım talebine daha sonra eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="9d3ff-116">Oturum açan bir bakım görevlisi bir varlıkla ilgili bir kaynakla ilişkiliyse **Varlık** alanı otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-116">If the maintenance worker who is signed in is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="9d3ff-117">Bir bakım talebi zaten seçili varlığa bağlıysa varolan bakım isteğinin kimliği hakkında sizi bilgilerindirmek için **İstek oluştur** iletişim kutusunun üst kısmında bir ileti çubuğu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="9d3ff-118">Bir mesaj çubuğu, varlık bir garanti sözleşmesi ile kapsamında ise size bildirir.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="9d3ff-119">**Hizmet düzeyi** alanında, isteğin aciliyetini belirten bir hizmet düzeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="9d3ff-120">5. adımda bir valık seçtiyseniz **Hata belirtisi**, **Hata alanı** ve **Hata türü** alanılarını kullanarak bir arıza kaydı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="9d3ff-121">Bakım taleb, bakım kesintisi süresine neden olursa kesinti süresinin başlangıç tarihi ve saatini girin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="9d3ff-122">**Başlatan** alanı otomatik olarak adınıza ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="9d3ff-123">**Fiili başlangıç** alanı otomatik olarak mevcut tarih ve saat olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="9d3ff-124">Ancak, değerleri istediğiniz gibi değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="9d3ff-125">**Notlar** alanında, gerekli olan ek notları girin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="9d3ff-126">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-126">Select **OK**.</span></span>

![Bakım talebi oluştur](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="9d3ff-128">Bakım taleplerinin sonraki işlemesi</span><span class="sxs-lookup"><span data-stu-id="9d3ff-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="9d3ff-129">Bir bakım talebi oluşturulduktan sonra ancak bir iş emrine dönüştürülmeden önce üzerinde çeşitli bilgiler güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="9d3ff-130">Genellikle, bir planlayıcı veya başka bir yönetici personel bu görevi tamamlar.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="9d3ff-131">**Tüm bakım talepleri** veya **Etkin bakım talepleri** sayfasında çalışılacak isteği seçin ve **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="9d3ff-132">Ayrıntılar görünümünde, çeşitli bilgileri güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-132">In the details view, you can update various information.</span></span> <span data-ttu-id="9d3ff-133">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="9d3ff-133">Here are some examples:</span></span>

- <span data-ttu-id="9d3ff-134">Varlığı seçin ve doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-134">Select and verify the asset.</span></span> <span data-ttu-id="9d3ff-135">Daha sonra farklı bir varlık seçmeniz gerekiyorsa **Varlık doğrulandı** seçeneğini **Hayır** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="9d3ff-136">Sorumlu bir bakım görevlisi grubu ve/veya sorumlu bir bakım görevlisini seçin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="9d3ff-137">Gerekli kurulum hakkında daha fazla bilgi için bkz: [Sorumlu bakım görevlileri](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="9d3ff-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="9d3ff-138">Bir bakım işi türü seçin ve bu bilgiler alakalı ise ilgili bakım iş çeşidi ve bir zanaat seçin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="9d3ff-139">**Enlem** ve **Boylam** alanlarında coğrafi koordinatları girin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="9d3ff-140">Bir bakım talebine eklenen koordinatlar otomatik olarak ilgili iş emri için aktarılır.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![Bakım talebini güncelleştirme](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="9d3ff-142">Bir bakım talebi oluşturduğunuzda bir varlık seçerseniz varlığa bir hata ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="9d3ff-143">Bakım talebi oluşturulduktan sonra ihtiyacınız olursa daha fazla hata ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="9d3ff-144">Hata eklemek için **Tüm bakım talepleri** sayfasından **Varlık hatası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="9d3ff-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]