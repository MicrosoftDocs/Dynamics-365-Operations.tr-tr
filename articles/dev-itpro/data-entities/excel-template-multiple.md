---
title: "Birden çok çalışma sayfası olan Excel veri varlığı şablonlarından içeri veri aktarma"
description: "Bu konuda, verilerin Excel veri varlığı şablonları kullanılarak Microsoft Dynamics 365 for Finance and Operations'a nasıl aktarılacağı açıklanmaktadır."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 2aefea9373df20bd3e99026e30aed096dcea9814
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="excel-templates-with-multiple-worksheets"></a><span data-ttu-id="e2428-103">Birden çok çalışma sayfası içeren Excel şablonları</span><span class="sxs-lookup"><span data-stu-id="e2428-103">Excel templates with multiple worksheets</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e2428-104">Microsoft Dynamics 365 for Finance and Operations'da veri yönetimi veri varlıkları için Microsoft Excel tabanlı şablonları destekler.</span><span class="sxs-lookup"><span data-stu-id="e2428-104">Data management in Microsoft Dynamics 365 for Finance and Operations supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="e2428-105">Bu şablonlar, bir veya daha fazla çalışma sayfası içerebilir.</span><span class="sxs-lookup"><span data-stu-id="e2428-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="e2428-106">Birden çok çalışma sayfası içeren şablonlar genellikle verileri tek bir dosyada yönetmek ve dosyayı birden çok veri varlığına aktarmak uygun olduğunda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e2428-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="e2428-107">Tesisler ve ambarlar bir örnek olabilir.</span><span class="sxs-lookup"><span data-stu-id="e2428-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="e2428-108">Önce bir dosya yükleyin ve bunu tüm varlıklarla eşleştirin</span><span class="sxs-lookup"><span data-stu-id="e2428-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="e2428-109">**Tesisler** ve **Ambarlar** adlı çalışma sayfaları içeren bir Excel dosyasının kullanıldığı bir örneği ele alalım.</span><span class="sxs-lookup"><span data-stu-id="e2428-109">Let’s take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="e2428-110">Veri içe aktarma projesini ayarlamak için öncelikle **Tesisler** veri varlığını ekler ve sonra dosyayı karşıya yüklersiniz.</span><span class="sxs-lookup"><span data-stu-id="e2428-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="e2428-111">Bu varlık için kullanılacak çalışma sayfası olarak **Tesisler**'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2428-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="e2428-112">İkinci varlık olan **Ambarlar**'ı **Dosya Ekle** formunu kapatmadan seçerseniz, çalışma sayfası araması **Ambarlar** çalışma sayfasını dosyayı yeniden karşıya yüklemenize gerek kalmadan seçmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="e2428-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="e2428-113">Yeni bir dosyayı karşıya yüklemenin tek nedeni **Ambarlar** verisinin farklı bir dosyada bulunması olabilir.</span><span class="sxs-lookup"><span data-stu-id="e2428-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![Birden çok çalışma sayfası](./media/AddFileMultipleWorkSheets.png) 

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="e2428-115">Çalışma sayfası ile varlık eşlemesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="e2428-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="e2428-116">Çalışma sayfasının bir içe aktarma işinde veri varlığı eşlemesi kılavuzdan düzeltilebilir.</span><span class="sxs-lookup"><span data-stu-id="e2428-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="e2428-117">Kılavuzdaki **Çalışma sayfası** sütunu eşlenen dosyadaki çalışma sayfalarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2428-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="e2428-118">Açılan menüden başka bir çalışma sayfasını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2428-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="e2428-119">Seçilen çalışma sayfası zaten veri projesindeki bir varlıkla eşlenmişse, sistem değişikliği onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e2428-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="e2428-120">Tüm eşlemeleri ızgarada düzeltmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="e2428-120">We recommend that you fix all mappings in the grid.</span></span>

![Çalışma sayfası eşlemesini güncelleştirme](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="e2428-122">Yeni bir dosyayla yeniden eşleme</span><span class="sxs-lookup"><span data-stu-id="e2428-122">Re-map to a new file</span></span>

<span data-ttu-id="e2428-123">Veri projesindeki mevcut varlıklar için aynı dosyanın yeni bir sürümünün veya tamamen yeni bir dosyanın yüklenmesi gereken durumlarda, **Dosya ekle** deneyimini kullanmanız ve varlıkları sanki ilk kez ekleniyormuş gibi tekrar eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e2428-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="e2428-124">Sistem devam etmeden önce veri projesindeki mevcut varlıkların üzerine yazmak istediğinizi onaylar.</span><span class="sxs-lookup"><span data-stu-id="e2428-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="e2428-125">Tekrar eklenmeyen (veya üzerine yazılmayan) varlıklar önceki dosyadaki önceki eşlemeleri korumaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="e2428-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="e2428-126">Projeyi çalıştır özelliğini kullanarak dosya yükleme</span><span class="sxs-lookup"><span data-stu-id="e2428-126">Upload a file using Run project</span></span>

<span data-ttu-id="e2428-127">Bir içe aktarma projesini yürütmek için **Projeyi çalıştır** seçeneğini kullanırken bir Excel dosyası yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2428-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="e2428-128">Yalnızca veri projesinde yer alan veri varlıklarındaki mevcut eşlemelerle aynı çalışma sayfalarına sahip dosyaları yüklemeye dikkat etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e2428-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="e2428-129">Yeni yüklenen bir dosyada bir çalışma sayfası bulunamazsa, sistem bir hata görüntüler ve içe aktarma işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="e2428-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="e2428-130">Çalışma sayfası eşlemesinin bir varlık için değiştirilmesi gerekirse, **Projeyi çalıştır** seçeneğindeki dosya kullanılmadan önce ilk olarak veri projesindeki eşlemelerin veri projesi içinden güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="e2428-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>


