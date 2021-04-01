---
title: Yük oluşturma çalışma ekranı
description: Bu konuda, yük oluşturma ekranı ile nasıl çalışılacağı açıklanmaktadır.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 480006a6d091acdf5c88fdbf0d9e625088d660d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247250"
---
# <a name="load-building-workbench"></a><span data-ttu-id="11ed3-103">Yük oluşturma çalışma ekranı</span><span class="sxs-lookup"><span data-stu-id="11ed3-103">Load building workbench</span></span>

<span data-ttu-id="11ed3-104">Yük oluşturma ekranı, yük oluştururken yük oluşturma stratejilerini uygulamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="11ed3-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="11ed3-105">Yük oluşturma stratejisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="11ed3-105">Create a load building strategy</span></span>

<span data-ttu-id="11ed3-106">Yükleri otomatik olarak oluşturmak için yük oluşturma stratejilerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11ed3-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="11ed3-107">Bu özellik, aşağıdaki durumlarda yararlı olabilir:</span><span class="sxs-lookup"><span data-stu-id="11ed3-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="11ed3-108">Belirli bir ürün kümesini düzenli olarak sevk ediyorsanız yük stratejileri zamandan tasarruf etmenize yardımcı olur çünkü her seferinde aynı yükü oluşturmak zorunda kalmazsınız.</span><span class="sxs-lookup"><span data-stu-id="11ed3-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="11ed3-109">Verimliliği en yüksek düzeye çıkarmak için yarı dolu yükleri önlemek istiyorsanız yük stratejileri her bir yükü mümkün olduğunca doldurmaya yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="11ed3-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="11ed3-110">`TMSLoadBuildingVolumeStrategy` adlı bir yük oluşturma stratejisi sınıfı, *Hacim temelli yük oluşturma stratejisi* adında bir oluşturma stratejisi elde etmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="11ed3-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="11ed3-111">Bu strateji, yük şablonunda yükseklik ve ağırlık için belirtilen maksimum değerleri kullanmanıza olanak tanır; veya yeni değerler girerek ayarları geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11ed3-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="11ed3-112">Bu strateji kullanıma hazır olarak sunulan tek stratejidir.</span><span class="sxs-lookup"><span data-stu-id="11ed3-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="11ed3-113">(Ancak, bazı özel stratejileriniz olabilir.)</span><span class="sxs-lookup"><span data-stu-id="11ed3-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="11ed3-114">Kullanıma hazır *Hacim temelli yük oluşturma stratejisi* adlı stratejiyi kullanmak için **Yük oluşturma çalışma ekranı** sayfasındaki (**Taşıma yönetimi &gt; Planlama &gt; Yük oluşturma çalışma ekranı**) **Yük oluşturma stratejisi** alanından seçin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="11ed3-115">Yük oluşturma stratejisi oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="11ed3-116">**Taşıma yönetimi &gt; Kurulum &gt;Yük oluşturma &gt; Yük oluşturma stratejileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="11ed3-117">Eylem bölmesinde, tüm kullanılabilir sınıfların en son sürümlerine sahip olduğunuzdan emin olmak için **Sınıf listesini oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="11ed3-118">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="11ed3-119">Strateji için benzersiz bir ad girin, yük oluşturma stratejisi sınıfını seçin ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="11ed3-120">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="11ed3-121">Eylem Bölmesi'nde, **Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="11ed3-122">**Yük oluşturma stratejisi** parametreleri sayfasında, listeden **Hacim kapasitesi**'ni seçin ve ardından **Değer** alanına yeni yük oluşturma stratejisi için uygulanacak yük toplam hacim kapasitesi yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="11ed3-123">Listeden **Ağırlık kapasitesi**'ni seçin ve ardından **Değer** alanına yeni yük oluşturma stratejisi için uygulanacak yük toplam ağırlık kapasitesi yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="11ed3-124">**Yük oluşturma stratejisi parametreleri** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="11ed3-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="11ed3-125">**Yük oluşturma stratejileri** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="11ed3-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="11ed3-126">Yük oluşturma stratejisini artık bir yük oluşturma şablonuna atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11ed3-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="11ed3-127">Alternatif olarak, bunu doğrudan yük planlama çalışma ekranında da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11ed3-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="11ed3-128">Yük oluşturma çalışma ekranında yük oluşturma stratejisi kullanma</span><span class="sxs-lookup"><span data-stu-id="11ed3-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="11ed3-129">**Taşıma yönetimi &gt; Planlama &gt; Yük oluşturma çalışma ekranı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="11ed3-130">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="11ed3-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="11ed3-131">**Yük oluşturma stratejisi** alanında bir strateji seçin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="11ed3-132">Bir yük oluşturma şablonu tanımladıysanız ve buna yük oluşturma stratejisini atadıysanız, Eylem bölmesinde **Şablonları yönet** sekmesinde **Şablonu Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="11ed3-133">Sonra, **Yük oluşturma şablonu uygula** iletişim kutusunda **Yük oluşturma şablonu adı** alanından bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="11ed3-134">**Yük şablonları sırası** hızlı sekmesinde, bir veya daha fazla [yük şablonu](load-template.md) seçin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="11ed3-135">Çalışma ekranı, burada belirtilen sıraya göre yükü bu tür konteynerlere sığdırmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="11ed3-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="11ed3-136">Genellikle en küçük konteynerleri listenin en üstüne koymanız gerekir, böylece önce olası en düşük konteynerin seçildiğinden emin olursunuz.</span><span class="sxs-lookup"><span data-stu-id="11ed3-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="11ed3-137">Eylem Bölmesinde, **Yük öner**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="11ed3-138">Önerilen yükleri ve önerilen yük satırlarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="11ed3-139">Eylem bölmesinde, **Önerilen yük satırları** hızlı sekmesindeki kaynak belge satırlarına dayalı yükler oluşturmak için **Yük oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="11ed3-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="11ed3-140">**Yük oluşturma çalışma ekranı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="11ed3-140">Close the **Load building workbench** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]