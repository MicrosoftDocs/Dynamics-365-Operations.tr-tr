---
title: ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 4 - Raporu çalıştırma)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ae9f72df5d6ff6add4eb97836cf32509aebd511
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141983"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="2df50-103">ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 4 - Raporu çalıştırma)</span><span class="sxs-lookup"><span data-stu-id="2df50-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2df50-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2df50-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="2df50-105">Bu adımlar DEMF şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="2df50-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="2df50-106">Bu adımları tamamlamak için öncelikle "ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 3: Raporu tasarlama)" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2df50-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="2df50-107">Ayrıca Elektronik raporlama parametreleri sayfasındaki varsayılan belge türlerini de yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2df50-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="2df50-108">ER yapılandırmasını indirdiğinizde ve içe aktardığınızda varsayılan belge türleri de ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="2df50-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="2df50-109">Raporu çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2df50-109">Run report</span></span>
1. <span data-ttu-id="2df50-110">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="2df50-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="2df50-111">Ağaçta, 'Mali boyutlar örnek modeli' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="2df50-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="2df50-112">Ağaçta, 'Mali boyutlar örnek modeli\Genel muhasebe günlüğü raporu' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2df50-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="2df50-113">Çalıştır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2df50-113">Click Run.</span></span>
5. <span data-ttu-id="2df50-114">Boyut adı alanında, bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2df50-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="2df50-115">Geçerli şirketteki tüm boyutları seçmek için şunları girin:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="2df50-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="2df50-116">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="2df50-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="2df50-117">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2df50-117">Click Filter.</span></span>
8. <span data-ttu-id="2df50-118">Genel muhasebe günlük tablosu satırını ve Günlük toplu iş numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="2df50-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="2df50-119">Ölçütler alanına '00057' yazın.</span><span class="sxs-lookup"><span data-stu-id="2df50-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="2df50-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2df50-120">Click OK.</span></span>
11. <span data-ttu-id="2df50-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2df50-121">Click OK.</span></span>
    * <span data-ttu-id="2df50-122">Ortaya çıkan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="2df50-122">Review the generated output.</span></span> <span data-ttu-id="2df50-123">Seçili toplu işlere ilişkin her hareket için, ilgili boyut kümesinden mali boyutların sunulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2df50-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="2df50-124">Bu raporu çalıştırın ve raporun seçili boyutların sayısına veya bu kurulum için yapılandırılmış boyutların sayısına bağlı olmadığını görmek için farklı boyutlar seçin.</span><span class="sxs-lookup"><span data-stu-id="2df50-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

