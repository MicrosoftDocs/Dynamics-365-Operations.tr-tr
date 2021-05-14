---
title: Kalite yönetimi testleri
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle kullanılabilmesi için, testlerin nasıl oluşturulacağını açıklar.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b88011f486b6582db4727b85d021868899c6abe1
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956863"
---
# <a name="quality-management-tests"></a><span data-ttu-id="ad321-103">Kalite yönetimi testleri</span><span class="sxs-lookup"><span data-stu-id="ad321-103">Quality management tests</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad321-104">Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle kullanılabilmesi için, testlerin nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="ad321-104">This topic describes how to create tests that can be used for quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="ad321-105">Ürünlerinizin kalite belirtimlerini sağlayıp sağlamadığını belirleyen tek tek testler tanımlamak ve görüntülemek için **Testler** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ad321-105">You use the **Tests** page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="ad321-106">Bir veya daha çok bireysel testleri bir test grubuna atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad321-106">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="ad321-107">Bu durumda, kabul edilebilir ölçüm değerleri gibi teste özgü bilgileri de belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad321-107">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="ad321-108">Ölçüm değerleri, niceliksel testler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ad321-108">Measurement values are used for quantitative tests.</span></span> <span data-ttu-id="ad321-109">Niteleyici testler için test değişkenleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ad321-109">For qualitative tests, test variables are used.</span></span>

- <span data-ttu-id="ad321-110">Niceliksel testler için, **Tür** alanını *Tamsayı* veya *Kesir* olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ad321-110">For quantitative tests, the **Type** field is set to *Integer* or *Fraction*.</span></span> <span data-ttu-id="ad321-111">Bir ölçü birimi belirlenir.</span><span class="sxs-lookup"><span data-stu-id="ad321-111">A unit of measure is also specified.</span></span> <span data-ttu-id="ad321-112">Kalite belirtimleri ve test sonuçları sayı olarak ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="ad321-112">Quality specifications and test results are expressed as numbers.</span></span>
- <span data-ttu-id="ad321-113">Niteliksel testler için, **Tür** alanı *Seçenek* olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ad321-113">For qualitative tests, the **Type** field is set to *Option*.</span></span> <span data-ttu-id="ad321-114">Kalite testleri, ölçülmekte olan değişken ve onun numaralandırılmış seçenekleri hakkında ek bilgi gerektirirler.</span><span class="sxs-lookup"><span data-stu-id="ad321-114">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="ad321-115">Kalite belirtimleri ve test sonuçları bir sonuca göre ifade edilirler.</span><span class="sxs-lookup"><span data-stu-id="ad321-115">Quality specifications and test results are expressed according to an outcome.</span></span>

<span data-ttu-id="ad321-116">İsteğe bağlı olarak test aracını bir teste de atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad321-116">You can optionally assign a test instrument to a test.</span></span> <span data-ttu-id="ad321-117">Ancak, test araçları, testleri kalite emirleri ile oluşturmak ve kullanmak için gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="ad321-117">However, test instruments aren't required to create and use tests with quality orders.</span></span> <span data-ttu-id="ad321-118">Daha fazla bilgi için bkz. [Kalite yönetimi test araçları](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="ad321-118">For more information, see [Quality management test instruments](quality-test-instruments.md).</span></span>

<span data-ttu-id="ad321-119">Test sonuçlarının kaydedildiği ölçü birimini belirtmek için isteğe bağlı olarak test için bir birim de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad321-119">You can also optionally specify a unit for a test, to indicate the unit of measure that test results are recorded in.</span></span> <span data-ttu-id="ad321-120">Örneğin, sıcaklık testine Fahrenhayt veya Santigrat derece birimini ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad321-120">For example, a test for temperature might include a unit of either degrees Fahrenheit or degrees Celsius.</span></span>

## <a name="example-of-a-test"></a><span data-ttu-id="ad321-121">Test örneği</span><span class="sxs-lookup"><span data-stu-id="ad321-121">Example of a test</span></span>

<span data-ttu-id="ad321-122">Bir üretim şirketi satın alınan malzeme üzerinde, malzeme kalitesi hakkında bir sayısal test ile ambalaj hasarı üzerine bir kalite testi dahil olmak üzere iki test gerçekleştiriyor.</span><span class="sxs-lookup"><span data-stu-id="ad321-122">A manufacturing company performs two tests on purchased material: a quantitative test for material quality and a qualitative test for packaging damage.</span></span> <span data-ttu-id="ad321-123">Şirket, test değişkenini (örneğin hasarlı ambalaj) ve sonuçlarını tanımlamak için ek bilgiler tanımlıyor.</span><span class="sxs-lookup"><span data-stu-id="ad321-123">The company specifies additional information about the qualitative test to define the test variable (for example, damaged packaging) and its outcomes.</span></span> <span data-ttu-id="ad321-124">Şirket **Test grupları** sayfasını iki testleri bir test grubuna atamak için ve teste özgü bilgileri belirtmek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="ad321-124">The company uses the **Test groups** page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="ad321-125">Test grubu, şirketin iki teste ait test sonuçlarını rapor edebilmesi için bir kalite emrine atanır.</span><span class="sxs-lookup"><span data-stu-id="ad321-125">The test group is assigned to a quality order so that the company can report test results for the two tests.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="ad321-126">Test oluşturun</span><span class="sxs-lookup"><span data-stu-id="ad321-126">Create a test</span></span>

<span data-ttu-id="ad321-127">Bir test oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ad321-127">Follow these steps to create a test.</span></span>

1. <span data-ttu-id="ad321-128">**Stok yönetimi \> Kurulum \> Kalite kontrol \> Testler** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="ad321-128">Go to **Inventory management \> Setup \> Quality control \> Tests**.</span></span>
1. <span data-ttu-id="ad321-129">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ad321-129">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ad321-130">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="ad321-130">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ad321-131">**Test** – Test için benzersiz bir kod ya da ad girin.</span><span class="sxs-lookup"><span data-stu-id="ad321-131">**Test** – Enter a unique ID or name for the test.</span></span>
    - <span data-ttu-id="ad321-132">**Açıklama** – Testin detaylı bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="ad321-132">**Description** – Enter a detailed description of the test.</span></span>
    - <span data-ttu-id="ad321-133">**Tür** – Testin ürettiği sonuçların türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="ad321-133">**Type** – Select the type of results that the test produces.</span></span> <span data-ttu-id="ad321-134">Niceliksel testler için *Kesir* veya *Tamsayı* seçin.</span><span class="sxs-lookup"><span data-stu-id="ad321-134">For quantitative tests, select *Fraction* or *Integer*.</span></span> <span data-ttu-id="ad321-135">Niteliksel testler için, *Seçenek* seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ad321-135">For qualitative tests, select *Option*.</span></span>
    - <span data-ttu-id="ad321-136">**Test aracı** – Test için kullanılacak [test aracını](quality-test-instruments.md) seçin.</span><span class="sxs-lookup"><span data-stu-id="ad321-136">**Test instrument** – Select a [test instrument](quality-test-instruments.md) that should be used for the test.</span></span>
    - <span data-ttu-id="ad321-137">**Birim** – **Tür** alanında *Kesir* veya *Tamsayı* seçtiyseniz (test bir niceliksel test ise), test sonuçlarının kaydedilmesi gereken ölçü birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="ad321-137">**Unit** – If you selected *Fraction* or *Integer* in the **Type** field (that is, if the test is a quantitative test), select the unit of measure that test results should be recorded in.</span></span>

1. <span data-ttu-id="ad321-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ad321-138">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="ad321-139">Testi kaydettikten sonra, ızgarada **Tür** alanını düzenleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad321-139">After you save a test, you can no longer edit the **Type** field in the grid.</span></span> <span data-ttu-id="ad321-140">Test için kaydedilecek test sonuçlarının türünü değiştirmeniz gerekiyorsa, Eylem Bölmesinde **Kalite test türünü değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ad321-140">If you must change the type of test results that will be recorded for a test, select **Change quality test type** on the Action Pane.</span></span> <span data-ttu-id="ad321-141">**Kalite test türünü değiştir** iletişim kutusunda, **Yeni tür** alanını istediğiniz türe ayarlayın ve sonra iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ad321-141">In the **Change quality test type** dialog box, set the **New type** field to the desired type, and then select **OK** to close the dialog box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad321-142">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ad321-142">Additional resources</span></span>

- [<span data-ttu-id="ad321-143">Kalite yönetimi test gereçleri</span><span class="sxs-lookup"><span data-stu-id="ad321-143">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="ad321-144">Kalite yönetimi test grupları</span><span class="sxs-lookup"><span data-stu-id="ad321-144">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="ad321-145">Kalite yönetimi test değişkenleri</span><span class="sxs-lookup"><span data-stu-id="ad321-145">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="ad321-146">Kalite ilişkileri</span><span class="sxs-lookup"><span data-stu-id="ad321-146">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
