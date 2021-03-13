---
title: ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 4 - Raporu çalıştırma)
description: Bu konuda, ER raporları için veri kaynağı olarak mali boyutları kullanmak üzere Elektronik raporlama (ER) modelinin nasıl yapılandırılacağı açıklanmaktadır. (4. Bölüm)
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
ms.openlocfilehash: c1fe332de84339d3369ba495ca13f50c4901f366
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092287"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="93dc3-104">ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 4 - Raporu çalıştırma)</span><span class="sxs-lookup"><span data-stu-id="93dc3-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="93dc3-105">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="93dc3-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="93dc3-106">Bu adımlar DEMF şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="93dc3-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="93dc3-107">Bu adımları tamamlamak için öncelikle "ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 3: Raporu tasarlama)" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="93dc3-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="93dc3-108">Ayrıca Elektronik raporlama parametreleri sayfasındaki varsayılan belge türlerini de yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="93dc3-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="93dc3-109">ER yapılandırmasını indirdiğinizde ve içe aktardığınızda varsayılan belge türleri de ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="93dc3-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="93dc3-110">Raporu çalıştırma</span><span class="sxs-lookup"><span data-stu-id="93dc3-110">Run report</span></span>
1. <span data-ttu-id="93dc3-111">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="93dc3-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="93dc3-112">Ağaçta, 'Mali boyutlar örnek modeli' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="93dc3-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="93dc3-113">Ağaçta, 'Mali boyutlar örnek modeli\Genel muhasebe günlüğü raporu' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="93dc3-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="93dc3-114">Çalıştır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93dc3-114">Click Run.</span></span>
<span data-ttu-id="93dc3-115">![ER yapılandırma sayfası](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="93dc3-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="93dc3-116">Boyut adı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="93dc3-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="93dc3-117">Geçerli şirketteki tüm boyutları seçmek için şunları girin:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="93dc3-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![ER yapılandırma sayfası](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="93dc3-119">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="93dc3-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="93dc3-120">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93dc3-120">Click Filter.</span></span>
8. <span data-ttu-id="93dc3-121">Genel muhasebe günlük tablosu satırını ve Günlük toplu iş numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="93dc3-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="93dc3-122">Ölçütler alanına '00057' yazın.</span><span class="sxs-lookup"><span data-stu-id="93dc3-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="93dc3-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93dc3-123">Click OK.</span></span>
11. <span data-ttu-id="93dc3-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93dc3-124">Click OK.</span></span>
<span data-ttu-id="93dc3-125">![ER yapılandırma sayfası](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="93dc3-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="93dc3-126">Ortaya çıkan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="93dc3-126">Review the generated output.</span></span> <span data-ttu-id="93dc3-127">Seçili toplu işlere ilişkin her hareket için, ilgili boyut kümesinden mali boyutların sunulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="93dc3-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="93dc3-128">Bu raporu çalıştırın ve raporun seçili boyutların sayısına veya bu kurulum için yapılandırılmış boyutların sayısına bağlı olmadığını görmek için farklı boyutlar seçin.</span><span class="sxs-lookup"><span data-stu-id="93dc3-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![ER yapılandırma sayfası](../media/er-financial-dimensions-guides-run4.png)
