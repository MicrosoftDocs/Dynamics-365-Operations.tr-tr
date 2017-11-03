--- 
title: "Elektronik raporlama (ER) için mali boyutları veri kaynağı olarak kullanan bir raporu çalıştırma"
description: "Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: cdecf5fb3f3047a56353ee6d4a8f94957f508e4b
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="a81ce-103">Elektronik raporlama (ER) için mali boyutları veri kaynağı olarak kullanan bir raporu çalıştırma</span><span class="sxs-lookup"><span data-stu-id="a81ce-103">Run a report that uses financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a81ce-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="a81ce-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="a81ce-105">Bu adımlar DEMF şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="a81ce-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="a81ce-106">Bu adımları tamamlamak için öncelikle "ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 3: Raporu tasarlama)" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a81ce-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="a81ce-107">Ayrıca Elektronik raporlama parametreleri sayfasındaki varsayılan belge türlerini de yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a81ce-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="a81ce-108">ER yapılandırmasını indirdiğinizde ve içe aktardığınızda varsayılan belge türleri de ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a81ce-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="a81ce-109">Raporu çalıştırma</span><span class="sxs-lookup"><span data-stu-id="a81ce-109">Run report</span></span>
1. <span data-ttu-id="a81ce-110">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="a81ce-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a81ce-111">Ağaçta, 'Mali boyutlar örnek modeli' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a81ce-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a81ce-112">Ağaçta, 'Mali boyutlar örnek modeli\Genel muhasebe günlüğü raporu' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a81ce-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="a81ce-113">Çalıştır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a81ce-113">Click Run.</span></span>
5. <span data-ttu-id="a81ce-114">Boyut adı alanında, bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a81ce-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="a81ce-115">Geçerli şirketteki tüm boyutları seçmek için şunları girin:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="a81ce-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="a81ce-116">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a81ce-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="a81ce-117">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a81ce-117">Click Filter.</span></span>
8. <span data-ttu-id="a81ce-118">Genel muhasebe günlük tablosu satırını ve Günlük toplu iş numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="a81ce-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="a81ce-119">Ölçütler alanına '00057' yazın.</span><span class="sxs-lookup"><span data-stu-id="a81ce-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="a81ce-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a81ce-120">Click OK.</span></span>
11. <span data-ttu-id="a81ce-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a81ce-121">Click OK.</span></span>
    * <span data-ttu-id="a81ce-122">Ortaya çıkan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="a81ce-122">Review the generated output.</span></span> <span data-ttu-id="a81ce-123">Seçili toplu işlere ilişkin her hareket için, ilgili boyut kümesinden mali boyutların sunulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a81ce-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="a81ce-124">Bu raporu çalıştırın ve raporun seçili boyutların sayısına veya bu , Dynamics 365 for Finance and Operations, Enterprise edition kurulumu için yapılandırılmış boyutların sayısına bağlı olmadığını görmek için farklı boyutlar seçin.</span><span class="sxs-lookup"><span data-stu-id="a81ce-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  

