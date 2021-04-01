---
title: Garanti sözleşmeleri
description: Bu konuda Varlık Yönetimi'ndeki satış sözleşmelerini açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 35b5c89751d17687bd7e306094a1e4e5e144a8dc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245359"
---
# <a name="warranty-agreements"></a><span data-ttu-id="14d4a-103">Garanti sözleşmeleri</span><span class="sxs-lookup"><span data-stu-id="14d4a-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="14d4a-104">Kıymet yönetiminde, bir kıymet veya kıymet türüne bağlı olabilecek garanti koşulları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="14d4a-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="14d4a-105">Garanti koşulları belirli bir dönem için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="14d4a-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="14d4a-106">Garanti, tam tedarik veya kısmi tedarik sağlayacak şekilde ayarlanabilir ve saatler, giderler ve öğelerle ilgili şartlar ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="14d4a-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="14d4a-107">İlk adım, ekipmanınız için olan tüm satıcı garanti sözleşmelerini oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="14d4a-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="14d4a-108">Sonra, kıymet veya kıymet türlerine garanti sözleşmelerini iliştirin.</span><span class="sxs-lookup"><span data-stu-id="14d4a-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="14d4a-109">Satıcı garanti sözleşmeleri yalnızca bilgilendirme amaçlı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="14d4a-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="14d4a-110">Satıcı garantisi bir kıymet için ayarlanmışsa, kıymet üzerinde garanti tedarik dönemini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="14d4a-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="14d4a-111">Garanti sözleşmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="14d4a-111">Create a warranty agreement</span></span>

<span data-ttu-id="14d4a-112">Garanti sözleşmesi, çalışma saatleri, giderler ve maddeler için garantiyi kapsayacak birkaç sözleşme satırı içerebilir.</span><span class="sxs-lookup"><span data-stu-id="14d4a-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="14d4a-113">**Kıymet yönetimi** \> **Kurulum** \> **Kıymetler** \> **Garanti**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="14d4a-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="14d4a-114">Bir ürün oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="14d4a-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="14d4a-115">**Garanti** alanına bir garanti kodu girin.</span><span class="sxs-lookup"><span data-stu-id="14d4a-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="14d4a-116">**Ad** alanında, bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="14d4a-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="14d4a-117">**Ayrıntılar** hızlı sekmesinde, **Kıymetler** alanında garanti sözleşmesini kullanan etkin kıymetlerin sayısı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="14d4a-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="14d4a-118">**Garanti satırları** hızlı sekmesinde, garanti sözleşmesine dahil edilmesi gereken satırları eklemek için aşağıdaki adımları uygulayın:</span><span class="sxs-lookup"><span data-stu-id="14d4a-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="14d4a-119">Garantiye yeni bir koşul eklemek için **Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="14d4a-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="14d4a-120">Sıralı satır numarası **Satır** alanına otomatik olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="14d4a-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="14d4a-121">**Dönem** alanında, garanti döneminin türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="14d4a-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="14d4a-122">**Aralık** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="14d4a-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="14d4a-123">Bu alan, garantinin geçerli olması gereken dönem sayısını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="14d4a-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="14d4a-124">**Yüzde** alanına, garanti satırı için karşılama yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="14d4a-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="14d4a-125">Yüzde, şirketiniz tarafından kapsanan miktarı gösterir.</span><span class="sxs-lookup"><span data-stu-id="14d4a-125">The percentage indicates how much is covered by your company.</span></span>

![Garanti sayfası](media/01-warranty.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]