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
ms.openlocfilehash: 1a1a32495b63a5a67a49bf3b02710aba63c1e2f0
ms.sourcegitcommit: bfd6142569196a060e3f37893c78f00c40a2a18c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946202"
---
# <a name="wave-step-codes"></a><span data-ttu-id="ac2aa-103">Dalga adım kodları</span><span class="sxs-lookup"><span data-stu-id="ac2aa-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac2aa-104">Dalga adımı kodları, kullanıcıların, dalga yöntemlerinin belirli örneklerini ilgili bir şablona bağlamak için ayarlayıp kullanabileceği kodlardır.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="ac2aa-105">Şablonlar, stok yenileme, konteyner kullanımı, etiket yazdırma, yük oluşturma ve sıralama şablonlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="ac2aa-106">Dalga adımı kodları kullanılmadığı zaman, kullanıcıların dalga yöntemi örneğinden belirli bir şablona başvuruda bulunmak için serbest metin girmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="ac2aa-107">Serbest metin hataya açıktır çünkü kullanıcılar bir dalga şablonunda belirli bir dalga adımı yöntemi için ekledikleri dalga adımı metninin, hedef şablondaki dalga adımı metniyle tam olarak eşleştiğinden emin olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="ac2aa-108">Belirli bir dalga adımı türü için dalga adımı kodları ayrı bir sayfada ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="ac2aa-109">Dalga adımı kodu gerektiren bir dalga şablonunda bulunan her bir dalga adımı yöntemi örneği için, dalga adımı kodunun açılan listede seçilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="ac2aa-110">Açılır listedeki seçim serbest metin girişinin yerini alır ve insan hatası riskini ve etkisini azaltmaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="ac2aa-111">Kurulum kodları, bir dalga şablonundaki dalga adımı yöntemini yöntem için hedef şablona bağlamak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="ac2aa-112">Dalga adım kodları özelliğinin kullanılması isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="ac2aa-113">Tüm yasal varlıklar için Organizasyon genelinde etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="ac2aa-114">Kurulum demosu</span><span class="sxs-lookup"><span data-stu-id="ac2aa-114">Setup demo</span></span> 

<span data-ttu-id="ac2aa-115">Bu demo için, demo verilerinin yüklenmiş olması ve **USMF** demo veri şirketini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="ac2aa-116">Dalga adım kodlarını etkinleştir</span><span class="sxs-lookup"><span data-stu-id="ac2aa-116">Enable wave step codes</span></span>

<span data-ttu-id="ac2aa-117">Dalga adımı kodları özelliğini açmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="ac2aa-118">**Özellik yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="ac2aa-119">**Organizasyon çapında dalga adım kodu** adı verilen özelliği etkinleştirmek için seçin.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="ac2aa-120">Tüm yasal varlıklarda varolan tüm dalga adımı serbest metinleri yeni yapıya yükseltilir.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="ac2aa-121">Tüm yasal varlıklar için bu yükseltme tamamlandıktan sonra, özellik etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="ac2aa-122">Özellik bir veya daha fazla tüzel kişilikler için etkinleştirilemez, geçerli varlıklar için özellik etkinleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="ac2aa-123">Etkinleştirme sırasında, veri yükseltme sırasında doğrulama yapılır.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="ac2aa-124">Yükseltme başarısız olursa, bir hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="ac2aa-125">Bir yükseltme aşağıdaki çakışmalar nedeniyle başarısız olabilir:</span><span class="sxs-lookup"><span data-stu-id="ac2aa-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="ac2aa-126">Tekrarlanan dalga adımı serbest metinleri vardır.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="ac2aa-127">Özelleştirmeler vardır.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-127">Customizations exist.</span></span>
- <span data-ttu-id="ac2aa-128">Bir dalga adımı yöntemi örneğiyle ilişkilendirilmiş dalga adımı serbest metni, beklenen şablon türüyle eşleşmiyordur.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="ac2aa-129">Doğrulamalar sırasında tanımlanan çakışmaları çözümledikten sonra özelliği etkinleştirmeyi yeniden deneyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="ac2aa-130">Özellik etkinleştirilirse **Dalga adımı kodları** sayfası (**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga adımı kodları**) kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="ac2aa-131">Kurum Genelinde Dalga Adımı Kodu özelliği etkinse, bu sayfada, yükseltilmiş dalga adımı kodları listelenir.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="ac2aa-132">Yeni dalga adımı kodları oluşturma</span><span class="sxs-lookup"><span data-stu-id="ac2aa-132">Create new wave step codes</span></span>

<span data-ttu-id="ac2aa-133">Dalga adımı kodları oluşturmak ve silmek için **Dalga adımı kodları** sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="ac2aa-134">Her yeni dalga adımı kodu ve ilişkili kodu, tüm dalga adımı türleri arasında benzersiz olmalıdır ve belirli bir dalga adımı türü için tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="ac2aa-135">Dalga adımı kodlarını uygulama</span><span class="sxs-lookup"><span data-stu-id="ac2aa-135">Apply wave step codes</span></span>

<span data-ttu-id="ac2aa-136">Siz uygun dalga adımı kodlarını tanımladıktan sonra bu kodlar dalga işlemi yöntemlerine uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="ac2aa-137">Dalga adımı kodlarını uygulamak için uygun hedef şablonuna gidin.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="ac2aa-138">Dalga adımı kodlarının işaret etmek üzere belirlenmiş olduğu hedef şablonlar:</span><span class="sxs-lookup"><span data-stu-id="ac2aa-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="ac2aa-139">**Stok yenileme şablonları:** Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları</span><span class="sxs-lookup"><span data-stu-id="ac2aa-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="ac2aa-140">**Yük oluşturma şablonları:** Ambar yönetimi \> Kurulum \> Yük \> Yük oluşturma şablonları</span><span class="sxs-lookup"><span data-stu-id="ac2aa-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="ac2aa-141">**Sıralama şablonları:** Ambar yönetimi \> Kurulum \> Ambalaj \> Giden sıralama şablonları</span><span class="sxs-lookup"><span data-stu-id="ac2aa-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="ac2aa-142">**Konteyner kullanımı şablonları:** Ambar yönetimi \> Kurulum \> Konteynerler \> Konteyner yapı şablonları</span><span class="sxs-lookup"><span data-stu-id="ac2aa-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="ac2aa-143">**Etiket yazdırma şablonları:** Ambar yönetimi \> Kurulum \> Belge rotası \> Dalga etiketi şablonları</span><span class="sxs-lookup"><span data-stu-id="ac2aa-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="ac2aa-144">Bu listedeki şablonlar, bir dalga şablonunda seçilen bir dalga işlemi yönteminden başvurulduğunda uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="ac2aa-145">Bir dalga şablonunda dalga işleme yöntemindeki dalga adımı kodu, şablon türlerinden birindeki dalga adım koduyla eşleştiğinde şablon uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="ac2aa-146">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="ac2aa-146">Sample scenario</span></span>

<span data-ttu-id="ac2aa-147">Aşağıdaki yordam, oluşturduğunuz stok yenileme şablonunun dalga şablonu için uygulanmasını garantilemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="ac2aa-148">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga adımı kodları**'na gidin ve **Stok yenileme** türü için bir dalga adımı kodu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="ac2aa-149">**Ambar yönetimi \> Kurulum \> Stok yenileme \> Stok yenileme şablonları**'na gidin ve bir stok yenileme şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="ac2aa-150">Stok yenileme şablonunda, **Stok yenileme** türü için oluşturduğunuz dalga adımı kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="ac2aa-151">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin ve kullanmayı düşündüğünüz dalga şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="ac2aa-152">Şablonda, **Yöntemler** hızlı sekmesinde **Stok yenileme** yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="ac2aa-153">**Dalga adımı kodu** alanında, stok yenileme şablonunda seçtiğiniz dalga adımı kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="ac2aa-154">Her yasal varlık için bu adımları gerçekleştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-154">You perform these steps for each legal entity.</span></span>
