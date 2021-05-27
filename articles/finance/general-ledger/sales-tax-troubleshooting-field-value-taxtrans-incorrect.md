---
title: TaxTrans'ta hatalı alan değeri
description: Bu konu, TaxTrans'taki hatalı alan değerleriyle ilgili sorunları giderme hakkında bilgi sağlar.
author: bijian
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 488ff54f1dd99208db940024a2fe8b2d25861f44
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020175"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="67a22-103">TaxTrans'ta hatalı alan değeri</span><span class="sxs-lookup"><span data-stu-id="67a22-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67a22-104">**TaxTrans**'taki bir alan değeri yanlışsa, sorunu gidermeye çalışmak için bu konudaki bilgileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="67a22-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="67a22-105">Değerlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="67a22-105">Overview of values</span></span>
<span data-ttu-id="67a22-106">Aşağıdaki listede **TaxTrans**, **TaxUncommitted** ve **TmpTaxWorkTrans**'ın nasıl benzer veri kümeleri olduğu ancak farklı şekilde çalıştıkları anlatılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="67a22-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="67a22-107">**TaxTrans**, veritabanında kalıcı, deftere nakledilen nihai vergi hareketi sonucudur.</span><span class="sxs-lookup"><span data-stu-id="67a22-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="67a22-108">**TaxUncommitted**, veritabanında (geçerliyse) kalıcı olan ve daha sonra deftere nakil için kullanılacak ortadaki hesaplanan vergi sonucudur.</span><span class="sxs-lookup"><span data-stu-id="67a22-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="67a22-109">**TmpTaxWorkTrans**, bellek içi tabloda (Tablo Türü = InMemory) geçici olarak hesaplanan vergi sonucudur.</span><span class="sxs-lookup"><span data-stu-id="67a22-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="67a22-110">Yanlış bir **TaxTrans** sütununun kök nedenini bulursanız, aynı zamanda yanlış **TaxUncommitted** veya **TmpTaxWorkTrans** sütununun da kök nedenini bulmuş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="67a22-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="67a22-111">Bunun nedeni, üç sütunun birbirinden kopyalanmasıdır.</span><span class="sxs-lookup"><span data-stu-id="67a22-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="67a22-112">Tipik olarak, vergi hesaplaması sırasında, **TmpTaxWorkTrans** oluşturulur ve daha sonra geçerliyse **TaxUncommitted** oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="67a22-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="67a22-113">Verginin deftere nakli sırasında, **TaxTrans** oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="67a22-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="67a22-114">Kesme noktaları ekleme</span><span class="sxs-lookup"><span data-stu-id="67a22-114">Add breakpoints</span></span>
<span data-ttu-id="67a22-115">Kesme noktaları eklemek için aşağıdaki adımları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="67a22-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="67a22-116">Uzantılarda *insert()* ve *update()* içindeki uzantıları ve kesme noktalarını aşağıda gösterildiği gibi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="67a22-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="67a22-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="67a22-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="67a22-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="67a22-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="67a22-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="67a22-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="67a22-120">Alternatif olarak, **TaxUncommitted** dahil olmadığında doğrudan kesme noktaları ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="67a22-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="67a22-121">*TaxTrans.insert()*, *TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="67a22-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="67a22-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="67a22-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="67a22-123">Yeniden oluşturma ve hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="67a22-123">Reproduce and debug</span></span>

<span data-ttu-id="67a22-124">Kesme noktaları ayarladıktan sonra, hata ayıklama sırasında her veri kalıcılığı değişikliği görünür.</span><span class="sxs-lookup"><span data-stu-id="67a22-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="67a22-125">Yanlış bir **TaxTrans**, **TaxUncommitted** veya **TmpTaxWorkTrans** sütununun kök nedenini bulmak için, aşağıdaki hususları gözden geçirin ve not alın:</span><span class="sxs-lookup"><span data-stu-id="67a22-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="67a22-126">Sütunun doğru olduğu son kesme noktası.</span><span class="sxs-lookup"><span data-stu-id="67a22-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="67a22-127">Sütunun hatalı olduğu ilk kesme noktası.</span><span class="sxs-lookup"><span data-stu-id="67a22-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="67a22-128">Bu iki nokta arasında ne gerçekleştiği.</span><span class="sxs-lookup"><span data-stu-id="67a22-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="67a22-129">Özelleştirme olup olmadığını belirleyin</span><span class="sxs-lookup"><span data-stu-id="67a22-129">Determine whether customization exists</span></span>
<span data-ttu-id="67a22-130">Önceki bölümlerdeki adımları tamamladıysanız ve sorunu çözemediyseniz bir özelleştirme olup olmadığını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="67a22-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="67a22-131">Hiç özelleştirme yoksa yardım için Microsoft Desteğine başvurun.</span><span class="sxs-lookup"><span data-stu-id="67a22-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

