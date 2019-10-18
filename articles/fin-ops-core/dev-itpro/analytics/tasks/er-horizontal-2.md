---
title: ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 2 - Biçimi çalıştırma)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, gerekli sütunların yatay olarak genişletilebilir aralıklar şeklinde oluşturulabileceği OPENXML çalışma sayfası (Excel) dosyaları şeklinde raporlar oluşturmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.
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
ms.openlocfilehash: ec81aba054718452dac3c10253dcd87091414fb5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182290"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2-run-format"></a><span data-ttu-id="6bfbe-103">ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 2: Biçimi çalıştırma)</span><span class="sxs-lookup"><span data-stu-id="6bfbe-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6bfbe-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, gerekli sütunların yatay olarak genişletilebilir aralıklar şeklinde oluşturulabileceği OPENXML çalışma sayfası (Excel) dosyaları şeklinde raporlar oluşturmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="6bfbe-105">Bu adımlar DEMF şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="6bfbe-106">Bu adımları tamamlamak için öncelikle "ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 1: Biçimi tasarlama)" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="6bfbe-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="6bfbe-108">Oluşturulan biçimi bulma</span><span class="sxs-lookup"><span data-stu-id="6bfbe-108">Find created format</span></span>
1. <span data-ttu-id="6bfbe-109">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6bfbe-110">Ağaçta, 'Mali boyutlar örnek modeli' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="6bfbe-111">Ağaçta, "Mali boyutlar örnek modeli\Yatay olarak genişletilebilir aralıklarla örnek rapor" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="6bfbe-112">Excel çıktısı oluşturmak için biçimi yürütme</span><span class="sxs-lookup"><span data-stu-id="6bfbe-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="6bfbe-113">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-113">Click Run.</span></span>
2. <span data-ttu-id="6bfbe-114">Boyut adı alanına "BusinessUnit;CostCenter;Department" yazın.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="6bfbe-115">Boyut adı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="6bfbe-116">Geçerli şirket için tüm boyutları seçmek için şunları girin:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="6bfbe-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="6bfbe-117">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="6bfbe-118">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-118">Click Filter.</span></span>
5. <span data-ttu-id="6bfbe-119">Genel muhasebe günlük tablosu satırını ve Günlük toplu iş numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="6bfbe-120">Ölçütler alanına "00057..00058" yazın.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="6bfbe-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="6bfbe-121">00057..00058</span></span>  
7. <span data-ttu-id="6bfbe-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-122">Click OK.</span></span>
8. <span data-ttu-id="6bfbe-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-123">Click OK.</span></span>
    * <span data-ttu-id="6bfbe-124">Ortaya çıkan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-124">Review the generated output.</span></span> <span data-ttu-id="6bfbe-125">Yeni oluşturulan Excel dosyasının mali boyutlar için seçilen ile aynı sayıda sütun içerdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="6bfbe-126">Bu sütunlardaki rapor başlığı mali boyutların adlarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="6bfbe-127">Bu sütunlardaki hareketlerin satırları mali boyutları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="6bfbe-128">Bu raporu çalıştırın ve raporun seçili boyutların sayısına veya bu kurulum için yapılandırılmış boyutların sayısına bağlı olmadığını görmek için farklı boyutlar seçin.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

