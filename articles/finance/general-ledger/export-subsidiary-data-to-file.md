---
title: Bağlı şirket verilerini dosyalara dışarı aktarma
description: Bu konu, Microsoft Dynamics 365 Finance'teki verileri dışarı aktarmak ve daha sonra konsolide edilmiş bir tüzel kişiliğe içeri aktarmak için nasıl hazırlık yapılacağı açıklanmaktadır.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: bae0a28c59f327e47378eef6392d5e304bbde9a8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826190"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="517ec-103">Bağlı şirket verilerini dosyalara dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="517ec-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="517ec-104">Bağlı verileri, daha sonra konsolide edilmiş bir tüzel kişiliğe içeri aktarılabilen dosyalara dışarı aktarmaya hazırlanmak için **Dışarı Aktar** sayfasını (**Sistem yönetimi \> Çalışma alanları \> İçeri aktarma/Dışarı aktarma**) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="517ec-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="517ec-105">İçeri ve dışarı aktarma işlemleri hakkında daha fazla bilgi için bkz. [Verileri içeri ve dışarı aktarma işlerine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="517ec-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="517ec-106">Konsolidasyon işlemi için tüzel kişilik oluşturun.</span><span class="sxs-lookup"><span data-stu-id="517ec-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="517ec-107">Tüzel kişilik oluşturma hakkında bilgi için bkz. [Tüzel kişilik oluşturma](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="517ec-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="517ec-108">Daha fazla bilgi için bkz [Konsolidasyon işleminde kullanılacak tüzel kişilik hazırlama](prepare-company-for-consolidation.md) ve [Konsolidasyon için bir alt şirket tüzel kişiliği ayarlama](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="517ec-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="517ec-109">**Konsolidasyonlar \> Şirket bakiyelerini dışarı aktar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="517ec-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="517ec-110">**Şirket bakiyelerini dışarı aktar** sayfasında, **Ölçüt** sekmesinde, aşağıdaki alanları ayarlayarak konsolidasyonun ayrıntılarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="517ec-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="517ec-111">Alan</span><span class="sxs-lookup"><span data-stu-id="517ec-111">Field</span></span>                             | <span data-ttu-id="517ec-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="517ec-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="517ec-113">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="517ec-113">Main account</span></span>                      | <span data-ttu-id="517ec-114">Konsolide edilecek hesapları belirtin.</span><span class="sxs-lookup"><span data-stu-id="517ec-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="517ec-115">Tüm hesapları dahil etmek için bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="517ec-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="517ec-116">Konsolidasyon hesabı kullanma</span><span class="sxs-lookup"><span data-stu-id="517ec-116">Use consolidation account</span></span>         | <span data-ttu-id="517ec-117">Konsolidasyon hesaplarını belirlediyseniz bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="517ec-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="517ec-118">Şuradan konsolidasyon hesabı seç:</span><span class="sxs-lookup"><span data-stu-id="517ec-118">Select consolidation account from</span></span> | <span data-ttu-id="517ec-119">**Ana hesap** veya **Konsolidasyon hesabı grubu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="517ec-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="517ec-120">Konsolidasyon hesap grubu</span><span class="sxs-lookup"><span data-stu-id="517ec-120">Consolidation account group</span></span>       | <span data-ttu-id="517ec-121">Seçtiğiniz konsolidasyon hesabı için bir konsolidasyon hesabı grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="517ec-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="517ec-122">Konsolidasyon dönemi</span><span class="sxs-lookup"><span data-stu-id="517ec-122">Consolidation period</span></span>              | <span data-ttu-id="517ec-123">Konsolidasyon için "Başlangıç" ve "Bitiş" tarihi belirtin.</span><span class="sxs-lookup"><span data-stu-id="517ec-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="517ec-124">Gerçek tutarları dahil et</span><span class="sxs-lookup"><span data-stu-id="517ec-124">Include actual amounts</span></span>            | <span data-ttu-id="517ec-125">Fiili tutarları dahil etmek için bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="517ec-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="517ec-126">Bütçe tutarlarını dahil et</span><span class="sxs-lookup"><span data-stu-id="517ec-126">Include budget amounts</span></span>            | <span data-ttu-id="517ec-127">Bütçe tutarlarını konsolidasyona dahil etmek için bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="517ec-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="517ec-128">Bütçe modelleri</span><span class="sxs-lookup"><span data-stu-id="517ec-128">Budget models</span></span>                     | <span data-ttu-id="517ec-129">Dahil edilecek bütçe modelini belirtin.</span><span class="sxs-lookup"><span data-stu-id="517ec-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="517ec-130">**Mali boyutlar** sekmesinde konsolidasyon ayrıntılarını belirtin:</span><span class="sxs-lookup"><span data-stu-id="517ec-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="517ec-131">Bağlı hesaplardaki hareketlerden konsolide edilmiş tüzel kişilikteki hareketlere aktarılması gereken mali boyut bilgilerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="517ec-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="517ec-132">Listeden mali boyutları seçin.</span><span class="sxs-lookup"><span data-stu-id="517ec-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="517ec-133">Konsolide edilen her mali boyut için doğru özellikleri tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="517ec-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="517ec-134">Mevcut seçenekler arasında **Boyut**, **Grup boyutu**, **Şirket hesapları** ve **Hesap** vardır.</span><span class="sxs-lookup"><span data-stu-id="517ec-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="517ec-135">**Grup boyutu** seçeneği, konsolide edilen şirket grupları tarafından kullanılan boyut değerini tanımlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="517ec-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="517ec-136">Konsolide edilecek segment emrini belirtin.</span><span class="sxs-lookup"><span data-stu-id="517ec-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="517ec-137">**Tüzel kişilikler** sekmesinde, dışarı aktardığınız tüzel kimliği belirtmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="517ec-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="517ec-138">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="517ec-138">Select **New**.</span></span>
    2. <span data-ttu-id="517ec-139">**Kaynak tüzel kişilik** alanına tüzel kişiliği girin.</span><span class="sxs-lookup"><span data-stu-id="517ec-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="517ec-140">Aynı ölçütler aynı veritabanında bulunan birkaç yan kuruluş için de geçerliyse, dosyaları dışarı aktarmayı tek bir işlemde ayırmak için bu yan kuruluşlardan veri aktarabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="517ec-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="517ec-141">Dosyalara dışarı aktarılması gereken her yan kuruluş tüzel kişiliği için bir satır oluşturun.</span><span class="sxs-lookup"><span data-stu-id="517ec-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="517ec-142">Bu dosyalar daha sonra konsolide edilen tüzel kişiliğe içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="517ec-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="517ec-143">Her bağlı şirket için bağlı şirket adını ve dışa aktarma işi sırasında oluşturulacak dışa aktarma dosyasının adını girin.</span><span class="sxs-lookup"><span data-stu-id="517ec-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="517ec-144">**Dönüştürme farkları için hesap türü** alanında, **Kar ve zarar**'ı veya **Bilanço**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="517ec-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="517ec-145">Oluşturulacak dışarı aktarma dosyası için bir dosya adı girin.</span><span class="sxs-lookup"><span data-stu-id="517ec-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="517ec-146">Dışarı aktarmayı çalıştırmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="517ec-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="517ec-147">Dışa aktarma işlemi tamamlandığında, her dosyaya kaydedilen kayıt sayısını gösteren bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="517ec-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="517ec-148">Artık dosyaları konsolide tüzel kişilikteki dosyalara içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="517ec-148">You can then import the files into the consolidated legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]