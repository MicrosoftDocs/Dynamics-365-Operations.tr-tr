---
title: Dalga adım kodları
description: Bu konu altında, dalga adımı kodları hakkında genel bilgi ve bu kodların nasıl kullanıldığı açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992369"
---
# <a name="wave-step-codes"></a><span data-ttu-id="d3ef8-103">Dalga adım kodları</span><span class="sxs-lookup"><span data-stu-id="d3ef8-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="d3ef8-104">Dalga adımı kodları hakkında</span><span class="sxs-lookup"><span data-stu-id="d3ef8-104">About wave step codes</span></span>

<span data-ttu-id="d3ef8-105">Dalga adımı kodları, kullanıcıların, dalga yöntemlerinin belirli örneklerini ilgili bir şablona bağlamak için ayarlayıp kullanabileceği kodlardır.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="d3ef8-106">Şablonlar, stok yenileme, konteyner kullanımı, etiket yazdırma, yük oluşturma ve sıralama şablonlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="d3ef8-107">Dalga adımı kodları kullanılmadığı zaman, kullanıcıların dalga yöntemi örneğinden belirli bir şablona başvuruda bulunmak için serbest metin girmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="d3ef8-108">Serbest metin hataya açıktır çünkü kullanıcılar bir dalga şablonunda belirli bir dalga adımı yöntemi için ekledikleri dalga adımı metninin, hedef şablondaki dalga adımı metniyle tam olarak eşleştiğinden emin olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="d3ef8-109">Belirli bir dalga adımı türü için dalga adımı kodları ayrı bir sayfada ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="d3ef8-110">Dalga adımı kodu gerektiren bir dalga şablonunda bulunan her bir dalga adımı yöntemi örneği için, dalga adımı kodunun açılan listede seçilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="d3ef8-111">Açılır listedeki seçim serbest metin girişinin yerini alır ve insan hatası riskini ve etkisini azaltmaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="d3ef8-112">Kurulum kodları, bir dalga şablonundaki dalga adımı yöntemini yöntem için hedef şablona bağlamak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="d3ef8-113">Dalga adımı kodları özelliğinin kullanımı isteğe bağlıdır ve tüzel kişilik için yükseltme yapılır.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="d3ef8-114">Bu nedenle, belirli bir tüzel kişilik bu özelliği kullanıyorsa, o tüzel kişilikteki tüm varolan dalga adımı kodları yeni yapıya yükseltilir.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="d3ef8-115">Kurulum demosu</span><span class="sxs-lookup"><span data-stu-id="d3ef8-115">Setup demo</span></span> 

<span data-ttu-id="d3ef8-116">Bu demo için, demo verilerinin yüklenmiş olması ve **USMF** demo veri şirketini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="d3ef8-117">Dalga adım kodlarını etkinleştir</span><span class="sxs-lookup"><span data-stu-id="d3ef8-117">Enable wave step codes</span></span>

<span data-ttu-id="d3ef8-118">Dalga adımı kodları özelliğini açmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="d3ef8-119">**Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="d3ef8-120">**Genel** sekmesinde **Dalga işleme** hızlı sekmesindeki **Dalga adımı kodlarını etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="d3ef8-121">Varolan tüm dalga adımı serbest metinleri yeni yapıya yükseltilir.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="d3ef8-122">Bir tüzel kişilik için bu yükseltme işlemi tamamlandıktan sonra, **Ambar yönetimi parametreleri** sayfasında **Dalga adımı kodlarını etkinleştir** seçeneği artık kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="d3ef8-123">Yükseltme sırasında doğrulamalar yapılır ve yükseltme başarısız olursa bir hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="d3ef8-124">Bir yükseltme aşağıdaki çakışmalar nedeniyle başarısız olabilir:</span><span class="sxs-lookup"><span data-stu-id="d3ef8-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="d3ef8-125">Tekrarlanan dalga adımı serbest metinleri vardır.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="d3ef8-126">Özelleştirmeler vardır.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-126">Customizations exist.</span></span>
- <span data-ttu-id="d3ef8-127">Bir dalga adımı yöntemi örneğiyle ilişkilendirilmiş dalga adımı serbest metni, beklenen şablon türüyle eşleşmiyordur.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="d3ef8-128">Doğrulamalar sırasında tanımlanan çakışmaları çözümledikten sonra yükseltme işlemini yeniden çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="d3ef8-129">Yükseltme başarılı olursa **Dalga adımı kodları** sayfası (**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga adımı kodları**) kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="d3ef8-130">Dalga adımı kodları özelliği açıksa, bu sayfada, yükseltilmiş dalga adımı kodları listelenir.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="d3ef8-131">Yeni dalga adımı kodları oluşturma</span><span class="sxs-lookup"><span data-stu-id="d3ef8-131">Create new wave step codes</span></span>

<span data-ttu-id="d3ef8-132">Dalga adımı kodları oluşturmak ve silmek için **Dalga adımı kodları** sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="d3ef8-133">Her yeni dalga adımı kodu ve ilişkili kodu, tüm dalga adımı türleri arasında benzersiz olmalıdır ve belirli bir dalga adımı türü için tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="d3ef8-134">Dalga adımı kodlarını uygulama</span><span class="sxs-lookup"><span data-stu-id="d3ef8-134">Apply wave step codes</span></span>

<span data-ttu-id="d3ef8-135">Siz uygun dalga adımı kodlarını tanımladıktan sonra bu kodlar dalga işlemi yöntemlerine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="d3ef8-136">Dalga adımı kodlarını uygulamak için uygun hedef şablonuna gidin.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="d3ef8-137">Dalga adımı kodlarının işaret etmek üzere belirlenmiş olduğu hedef şablonlar:</span><span class="sxs-lookup"><span data-stu-id="d3ef8-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="d3ef8-138">**Stok yenileme şablonları:** Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları</span><span class="sxs-lookup"><span data-stu-id="d3ef8-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="d3ef8-139">**Yük oluşturma şablonları:** Ambar yönetimi \> Kurulum \> Yük \> Yük oluşturma şablonları</span><span class="sxs-lookup"><span data-stu-id="d3ef8-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="d3ef8-140">**Sıralama şablonları:** Ambar yönetimi \> Kurulum \> Ambalaj \> Giden sıralama şablonları</span><span class="sxs-lookup"><span data-stu-id="d3ef8-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="d3ef8-141">**Konteyner kullanımı şablonları:** Ambar yönetimi \> Kurulum \> Konteynerler \> Konteyner yapı şablonları</span><span class="sxs-lookup"><span data-stu-id="d3ef8-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="d3ef8-142">**Etiket yazdırma şablonları:** Ambar yönetimi \> Kurulum \> Belge rotası \> Dalga etiketi şablonları</span><span class="sxs-lookup"><span data-stu-id="d3ef8-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="d3ef8-143">Bu listedeki şablonlar, bir dalga şablonunda seçilen bir dalga işlemi yönteminden başvurulduğunda uygulanır.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="d3ef8-144">Bir dalga şablonunda dalga işleme yöntemindeki dalga adımı kodu, şablon türlerinden birindeki dalga adım koduyla eşleştiğinde şablon uygulanır.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="d3ef8-145">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="d3ef8-145">Sample scenario</span></span>

<span data-ttu-id="d3ef8-146">Aşağıdaki yordam, oluşturduğunuz stok yenileme şablonunun dalga şablonu için uygulanmasını garantilemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="d3ef8-147">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga adımı kodları**'na gidin ve **Stok yenileme** türü için bir dalga adımı kodu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="d3ef8-148">**Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları**'na gidin ve bir stok yenileme şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="d3ef8-149">Stok yenileme şablonunda, **Stok yenileme** türü için oluşturduğunuz dalga adımı kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="d3ef8-150">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin ve kullanmayı düşündüğünüz dalga şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="d3ef8-151">Şablonda, **Yöntemler** hızlı sekmesinde **Stok yenileme** yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="d3ef8-152">**Dalga adımı kodu** alanında, stok yenileme şablonunda seçtiğiniz dalga adımı kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d3ef8-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>
