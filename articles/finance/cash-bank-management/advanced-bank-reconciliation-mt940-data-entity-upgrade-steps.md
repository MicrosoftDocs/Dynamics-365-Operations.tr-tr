---
title: Gelişmiş banka mutabakatı MT940 İçe Aktarma – Bileşik veri varlığı yükseltme
description: MT940 biçimini desteklemek için banka ekstresi içe aktarma varlığına bir sıra numarası eklenmesi gerekir.
author: panolte
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 65970cdac114b72363d2fbbc08766c99ace00b88
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899385"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="82f13-103">Gelişmiş banka mutabakatı MT940 İçe Aktarma – Bileşik veri varlığı yükseltme</span><span class="sxs-lookup"><span data-stu-id="82f13-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82f13-104">MT940 biçimini desteklemek için banka ekstresi içe aktarma varlığına bir sıra numarası eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="82f13-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="82f13-105">MT940 biçimini desteklemesi için banka ekstresi içe aktarma varlığını eklemek amacıyla aşağıdaki adımları kullanın.</span><span class="sxs-lookup"><span data-stu-id="82f13-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="82f13-106">Aşağıdakileri derleyin ve eşitleyin:</span><span class="sxs-lookup"><span data-stu-id="82f13-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="82f13-107">Birleşik Varlık\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="82f13-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="82f13-108">Varlık\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="82f13-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="82f13-109">Varlık\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="82f13-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="82f13-110">Varlık\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="82f13-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="82f13-111">Varlık\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="82f13-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="82f13-112">Tablolar\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="82f13-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="82f13-113">Veri yönetimi\\veri projeleri.</span><span class="sxs-lookup"><span data-stu-id="82f13-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="82f13-114">MT940 içe aktarma projeleri</span><span class="sxs-lookup"><span data-stu-id="82f13-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="82f13-115">XSLT'yi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="82f13-115">Change XSLT.</span></span>
            -   <span data-ttu-id="82f13-116">**Eşlemeyi görüntüle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="82f13-116">Click **View map**.</span></span>
            -   <span data-ttu-id="82f13-117">Banka ekstresi belgesinde **Eşlemeyi görüntüle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="82f13-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="82f13-118">**Dönüşümler**'e tıklayın</span><span class="sxs-lookup"><span data-stu-id="82f13-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="82f13-119">BankReconciliation-to-Composite.xslt dosyasını silin.</span><span class="sxs-lookup"><span data-stu-id="82f13-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="82f13-120">BankReconiliation-to-Composite.xsl dosyasının yeni sürümünü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="82f13-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="82f13-121">**Kaynak Veri** düzeninde **Sıra numarası**'nı gösterin.</span><span class="sxs-lookup"><span data-stu-id="82f13-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="82f13-122">Kaynak veri biçimi = XML Öğesi.</span><span class="sxs-lookup"><span data-stu-id="82f13-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="82f13-123">Varlık adı = Banka ekstreleri.</span><span class="sxs-lookup"><span data-stu-id="82f13-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="82f13-124">Yükleme veri dosyası = yeni sürüm ÖrnekBankaBirleşikVarlığı.xml.</span><span class="sxs-lookup"><span data-stu-id="82f13-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="82f13-125">Mevcut dosyanın üzerine yazmak için **Evet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="82f13-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="82f13-126">Yeni bir eşleme oluşturmak için **Evet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="82f13-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="82f13-127">**SıraNumarası**'nın eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="82f13-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="82f13-128">Ekstre varlığında **Eşlemeyi Görüntüle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="82f13-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="82f13-129">**SıraNumarası**'nın Kaynak'tan Aşamalandırma'ya eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="82f13-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="82f13-130">Yeni ekstreyi içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="82f13-130">Import the new statement.</span></span>




