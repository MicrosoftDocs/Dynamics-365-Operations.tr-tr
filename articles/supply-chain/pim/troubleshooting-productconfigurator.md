---
title: Ürün yapılandırıcısındaki sorunları giderme
description: Bu konuda, ürün yapılandırıcı ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 77d0c21fbb5a8479ca5e7bdb759c1373b6b255a4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841563"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="b7777-103">Ürün yapılandırıcısındaki sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="b7777-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="b7777-104">Bu konuda, ürün yapılandırıcı ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b7777-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="b7777-105">Satış siparişi satırındaki bir ürünü yapılandırırken madde metninin üzerine yazılıyor.</span><span class="sxs-lookup"><span data-stu-id="b7777-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b7777-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b7777-106">Issue description</span></span>

<span data-ttu-id="b7777-107">Bu sorun, yapılandırılabilir bir madde için satış siparişi satırı oluşturup madde metnini değiştirdiğinizde oluşur.</span><span class="sxs-lookup"><span data-stu-id="b7777-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="b7777-108">Maddeyi yapılandırıp **Tamam**'ı seçtiğinizde , standart metin metnin üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="b7777-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b7777-109">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b7777-109">Issue resolution</span></span>

<span data-ttu-id="b7777-110">Bu davranış beklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="b7777-110">This behavior is expected.</span></span> <span data-ttu-id="b7777-111">Metin alanı, yalnızca satır yapılandırıldıktan sonra doldurulan varyant adını içerir.</span><span class="sxs-lookup"><span data-stu-id="b7777-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="b7777-112">Bu nedenle, metni satırı yapılandırmadan önce değil, sonra değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b7777-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="b7777-113">Ürün yapılandırma modelleri hesaplanırken, tamsayı nitelikleri yanlış yuvarlanıyor.</span><span class="sxs-lookup"><span data-stu-id="b7777-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b7777-114">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b7777-114">Issue description</span></span>

<span data-ttu-id="b7777-115">Bu sorun, aşağıdaki eylem dizilerini gerçekleştirdiğinizde oluşabilir:</span><span class="sxs-lookup"><span data-stu-id="b7777-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="b7777-116">Üretim yapılandırması modelinde aşağıdaki öznitelikleri ayarlama:</span><span class="sxs-lookup"><span data-stu-id="b7777-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="b7777-117">Giriş (tamsayı)</span><span class="sxs-lookup"><span data-stu-id="b7777-117">Input (integer)</span></span>
    - <span data-ttu-id="b7777-118">Yüzde (ondalık)</span><span class="sxs-lookup"><span data-stu-id="b7777-118">Percent (decimal)</span></span>
    - <span data-ttu-id="b7777-119">Sonuç (tamsayı)</span><span class="sxs-lookup"><span data-stu-id="b7777-119">Result (integer)</span></span>

2. <span data-ttu-id="b7777-120">Aşağıdaki ifadeye sahip bir hesaplama oluşturma:</span><span class="sxs-lookup"><span data-stu-id="b7777-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="b7777-121">*Sonuç* = *Giriş* × *Yüzde* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="b7777-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="b7777-122">Bu durumda, tamsayı sonucu her zaman doğru olarak yuvarlanmaz.</span><span class="sxs-lookup"><span data-stu-id="b7777-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="b7777-123">Örneğin, giriş 1.000 ve yüzde 2,40'tır.</span><span class="sxs-lookup"><span data-stu-id="b7777-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="b7777-124">Bu nedenle, 1.000'in yüzde 2,40'ı 24 (veya ondalık biçimde 24,00) olduğundan tamsayı sonucunun 24 olmasını beklersiniz.</span><span class="sxs-lookup"><span data-stu-id="b7777-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="b7777-125">Bunun yerine, sonuç 23 olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b7777-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="b7777-126">Ancak, yüzde değeri 2,39 olduğunda, hesaplama 23 yerine 24'e yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="b7777-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="b7777-127">Yüzde değeri 2,50 olduğunda, hesaplama beklendiği şekilde 25'e yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="b7777-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b7777-128">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b7777-128">Issue resolution</span></span>

<span data-ttu-id="b7777-129">Bu sorun, Microsoft Solver Foundation dahili olarak sayıları kesirleri kullanarak temsil ettiğinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="b7777-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="b7777-130">Önceki örnekte, yüzdenin 2,40 olduğu hesaplamanın sonucu 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375 olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b7777-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="b7777-131">.NET bu değeri tamsayı olarak verdiğinde 23 değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b7777-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="b7777-132">Başka senaryolar buna bağlı olduğu için bu davranış değiştirilmez.</span><span class="sxs-lookup"><span data-stu-id="b7777-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="b7777-133">Önceki örnekte, ek bir ondalık özniteliği ve hesaplama ekleyerek sorunu giderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7777-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="b7777-134">Örneğin, üretim yapılandırması modelinde aşağıdaki öznitelikleri ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b7777-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="b7777-135">Giriş (tamsayı)</span><span class="sxs-lookup"><span data-stu-id="b7777-135">Input (integer)</span></span>
- <span data-ttu-id="b7777-136">Yüzde (ondalık)</span><span class="sxs-lookup"><span data-stu-id="b7777-136">Percent (decimal)</span></span>
- <span data-ttu-id="b7777-137">ResultDecimal (ondalık)</span><span class="sxs-lookup"><span data-stu-id="b7777-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="b7777-138">ResultInteger (tamsayı)</span><span class="sxs-lookup"><span data-stu-id="b7777-138">ResultInteger (integer)</span></span>

<span data-ttu-id="b7777-139">Bunun ardından aşağıdaki hesaplamaları ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b7777-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="b7777-140">*ResultDecimal* = *Giriş* × *Yüzde* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="b7777-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="b7777-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="b7777-141">*ResultInteger* = *ResultDecimal*</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]