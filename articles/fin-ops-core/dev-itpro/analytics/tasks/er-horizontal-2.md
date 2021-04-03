---
title: ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 2 - Biçimi çalıştırma)
description: Bu konuda, OPENXML çalışma sayfası (Excel) dosyaları olarak rapor oluşturmak için Elektronik raporlama (ER) biçiminin nasıl yapılandırılacağı açıklanmaktadır. (2. Bölüm)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0b8c997549bca2cae5500c926ccba916a473b5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569545"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="34d76-104">ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 2 - Biçimi çalıştırma)</span><span class="sxs-lookup"><span data-stu-id="34d76-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34d76-105">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, gerekli sütunların yatay olarak genişletilebilir aralıklar şeklinde oluşturulabileceği OPENXML çalışma sayfası (Excel) dosyaları şeklinde raporlar oluşturmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="34d76-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="34d76-106">Bu adımlar DEMF şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="34d76-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="34d76-107">Bu adımları tamamlamak için öncelikle "ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 1: Biçimi tasarlama)" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="34d76-107">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="34d76-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="34d76-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="34d76-109">Oluşturulan biçimi bulma</span><span class="sxs-lookup"><span data-stu-id="34d76-109">Find created format</span></span>
1. <span data-ttu-id="34d76-110">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="34d76-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="34d76-111">Ağaçta, 'Mali boyutlar örnek modeli' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="34d76-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="34d76-112">Ağaçta, "Mali boyutlar örnek modeli\Yatay olarak genişletilebilir aralıklarla örnek rapor" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="34d76-112">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="34d76-113">Excel çıktısı oluşturmak için biçimi yürütme</span><span class="sxs-lookup"><span data-stu-id="34d76-113">Execute format to create Excel output</span></span>
1. <span data-ttu-id="34d76-114">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="34d76-114">Click Run.</span></span>
2. <span data-ttu-id="34d76-115">Boyut adı alanına "BusinessUnit;CostCenter;Department" yazın.</span><span class="sxs-lookup"><span data-stu-id="34d76-115">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="34d76-116">Boyut adı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="34d76-116">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="34d76-117">Geçerli şirket için tüm boyutları seçmek için şunları girin:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="34d76-117">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="34d76-118">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="34d76-118">Expand the Records to include section.</span></span>
4. <span data-ttu-id="34d76-119">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="34d76-119">Click Filter.</span></span>
5. <span data-ttu-id="34d76-120">Genel muhasebe günlük tablosu satırını ve Günlük toplu iş numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="34d76-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="34d76-121">Ölçütler alanına "00057..00058" yazın.</span><span class="sxs-lookup"><span data-stu-id="34d76-121">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="34d76-122">00057..00058</span><span class="sxs-lookup"><span data-stu-id="34d76-122">00057..00058</span></span>  
7. <span data-ttu-id="34d76-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="34d76-123">Click OK.</span></span>
8. <span data-ttu-id="34d76-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="34d76-124">Click OK.</span></span>
    * <span data-ttu-id="34d76-125">Ortaya çıkan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="34d76-125">Review the generated output.</span></span> <span data-ttu-id="34d76-126">Yeni oluşturulan Excel dosyasının mali boyutlar için seçilen ile aynı sayıda sütun içerdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="34d76-126">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="34d76-127">Bu sütunlardaki rapor başlığı mali boyutların adlarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="34d76-127">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="34d76-128">Bu sütunlardaki hareketlerin satırları mali boyutları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="34d76-128">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="34d76-129">Bu raporu çalıştırın ve raporun seçili boyutların sayısına veya bu kurulum için yapılandırılmış boyutların sayısına bağlı olmadığını görmek için farklı boyutlar seçin.</span><span class="sxs-lookup"><span data-stu-id="34d76-129">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]