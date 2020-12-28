---
title: ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 4 - Raporu çalıştırma)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb7f49310aa25ff7c17ab4bcd50e1842be84fe2d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684751"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="d451a-103">ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 4 - Raporu çalıştırma)</span><span class="sxs-lookup"><span data-stu-id="d451a-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d451a-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="d451a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="d451a-105">Bu adımlar DEMF şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="d451a-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="d451a-106">Bu adımları tamamlamak için öncelikle "ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 3: Raporu tasarlama)" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d451a-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="d451a-107">Ayrıca Elektronik raporlama parametreleri sayfasındaki varsayılan belge türlerini de yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d451a-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="d451a-108">ER yapılandırmasını indirdiğinizde ve içe aktardığınızda varsayılan belge türleri de ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d451a-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="d451a-109">Raporu çalıştırma</span><span class="sxs-lookup"><span data-stu-id="d451a-109">Run report</span></span>
1. <span data-ttu-id="d451a-110">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="d451a-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d451a-111">Ağaçta, 'Mali boyutlar örnek modeli' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="d451a-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="d451a-112">Ağaçta, 'Mali boyutlar örnek modeli\Genel muhasebe günlüğü raporu' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d451a-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="d451a-113">Çalıştır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d451a-113">Click Run.</span></span>
<span data-ttu-id="d451a-114">![ER yapılandırma sayfası](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="d451a-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="d451a-115">Boyut adı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d451a-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="d451a-116">Geçerli şirketteki tüm boyutları seçmek için şunları girin:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="d451a-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![ER yapılandırma sayfası](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="d451a-118">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="d451a-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="d451a-119">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d451a-119">Click Filter.</span></span>
8. <span data-ttu-id="d451a-120">Genel muhasebe günlük tablosu satırını ve Günlük toplu iş numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="d451a-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="d451a-121">Ölçütler alanına '00057' yazın.</span><span class="sxs-lookup"><span data-stu-id="d451a-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="d451a-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d451a-122">Click OK.</span></span>
11. <span data-ttu-id="d451a-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d451a-123">Click OK.</span></span>
<span data-ttu-id="d451a-124">![ER yapılandırma sayfası](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="d451a-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="d451a-125">Ortaya çıkan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="d451a-125">Review the generated output.</span></span> <span data-ttu-id="d451a-126">Seçili toplu işlere ilişkin her hareket için, ilgili boyut kümesinden mali boyutların sunulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="d451a-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="d451a-127">Bu raporu çalıştırın ve raporun seçili boyutların sayısına veya bu kurulum için yapılandırılmış boyutların sayısına bağlı olmadığını görmek için farklı boyutlar seçin.</span><span class="sxs-lookup"><span data-stu-id="d451a-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![ER yapılandırma sayfası](../media/er-financial-dimensions-guides-run4.png)
