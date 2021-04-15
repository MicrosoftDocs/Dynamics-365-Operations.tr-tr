---
title: Excel şablonlarını yeniden uygulayarak Elektronik raporlama biçimlerini değiştirme
description: Bu konuda, değiştirilen bir Excel şablonunu yeniden uygulayarak iş belgeleri oluşturmak için kullanılan Elektronik raporlama biçimini nasıl değiştirebileceğiniz açıklanmaktadır.
author: NickSelin
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ab7686ac0aba982fd44195214df878ba3ede446
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748729"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a><span data-ttu-id="8dbf7-103">Excel şablonlarını yeniden uygulayarak Elektronik raporlama biçimlerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="8dbf7-103">Modify Electronic reporting formats by reapplying Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8dbf7-104">Elektronik raporlama (ER) aracı, elektronik biçimde iş belgeleri oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8dbf7-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="8dbf7-105">Bir iş belgesi oluşturmak için bir ER biçimi oluşturmanız, ardından iş belgesinin düzenini tanımlamak için ER tasarımcısını kullanmanız ve buna dahil edilmesi gereken bilgileri belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8dbf7-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="8dbf7-106">Daha sonra iş belgeleri oluşturmak için ER biçimini çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8dbf7-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="8dbf7-107">ER aracı Microsoft Excel dosyaları biçiminde iş belgeleri oluşturmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8dbf7-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="8dbf7-108">Bu belgeler için bir Excel belgesini şablon olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8dbf7-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="8dbf7-109">ER tasarımcısında belge düzenini tanımlamak için, kullanmak istediğiniz Excel belgesinin içeriklerini şablon olarak tanımlanan ER biçimine aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8dbf7-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="8dbf7-110">Ayrıntılı bilgi edinmek ve bu senaryoyu uygulamak için **ER OPENXML biçiminde raporlar oluşturmak için bir yapılandırma tasarlama** görev kılavuzunu (7.5.4.3 Al/BT hizmeti geliştir/çözüm bileşenleri (10677) iş işleminin parçası ) oynatın.</span><span class="sxs-lookup"><span data-stu-id="8dbf7-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="8dbf7-111">Bir iş belgesi için bir şablon olarak kullanılan Excel belgesinde düzenleme yaparsanız, yeni ER işlevi güncelleştirilen şablonu ER biçimine yeniden uygulamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="8dbf7-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="8dbf7-112">ER biçimi daha sonra güncelleştirilir ve güncelleştirilen şablona bağlı kalır.</span><span class="sxs-lookup"><span data-stu-id="8dbf7-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="8dbf7-113">Bu işlev hakkında daha fazla bilgi için **ER Bir Excel şablonu uygulayarak bir biçimi değiştirme** (7.5.5.3 Al/BT hizmeti geliştirme/çözüm bileşenleri (10683) iş sürecinin parçası olarak) görev kılavuzunu oynatın.</span><span class="sxs-lookup"><span data-stu-id="8dbf7-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="8dbf7-114">Görev kılavuzunda güncelleştirilmiş bir şablonu içe aktardığınız adımda, şablon olarak Ödeme Raporu Excel dosyasının değiştirilen şablonunu (SampleVendPaymWsReport2) kullanın.</span><span class="sxs-lookup"><span data-stu-id="8dbf7-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]