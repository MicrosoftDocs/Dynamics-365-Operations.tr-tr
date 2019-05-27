---
title: Gelen belgeleri Excel biçiminde ayrıştırma
description: Bu konu, gelen Microsoft Excel dosyalarındaki içeriği ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlama hakkında bilgi vermektedir.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 490a9325be25908564a40478a1ee29feea67fc02
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545065"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="6c45e-103">Genel belgeleri Excel biçiminde ayrıştırma</span><span class="sxs-lookup"><span data-stu-id="6c45e-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6c45e-104">Microsoft Excel çalışma kitaplarındaki (XLSX biçimindeki dosyalar) verileri temsil eden gelen Microsoft Excel dosyalarını ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c45e-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="6c45e-105">Bunun ardından, uygulama verilerini güncelleştirmek için bu dosyalardaki içeriği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c45e-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="6c45e-106">Bu, şunu yaptığınız zaman size yarar sağlar:</span><span class="sxs-lookup"><span data-stu-id="6c45e-106">This is useful if you:</span></span>

- <span data-ttu-id="6c45e-107">Yeni bir model ve biçim tasarlamak ve çalıştırma zamanında bunları test etmek.</span><span class="sxs-lookup"><span data-stu-id="6c45e-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="6c45e-108">Bu durumda, Excel gerçek uygulama verilerinin benzetimini yapacaktır.</span><span class="sxs-lookup"><span data-stu-id="6c45e-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="6c45e-109">Uygulamanızın dışında, verileri Excel'de yönetmek ve belirli bir rapor gönderme amacıyla bu verileri içe aktarmak.</span><span class="sxs-lookup"><span data-stu-id="6c45e-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="6c45e-110">Bu özellik hakkında daha fazla bilgi için, **ER - Microsoft Excel dosyasından verileri içe aktarma (Bölüm 1: Biçim tasarlama)** ve **ER - Microsoft Excel dosyasından verileri içe aktarma (Bölüm 2: Verileri içe aktarma)** (7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677) iş sürecinin parçaları).</span><span class="sxs-lookup"><span data-stu-id="6c45e-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="6c45e-111">Bu görev kılavuzları, gelen belgelerden bilgileri içe aktarmak ve uygulama verilerini güncelleştirmek için, ER biçimi kullanarak, gelen Excel dosyasının nasıl ayrıştırılabileceği konusunda size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c45e-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="6c45e-112">Görev kılavuzu dosyalarını [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684)'dan indirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c45e-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="6c45e-113">Yukarıda sözü edilen görev kılavuzlarını tamamlamak için aşağıdaki dosyaları indirin:</span><span class="sxs-lookup"><span data-stu-id="6c45e-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="6c45e-114">İçerik açıklaması</span><span class="sxs-lookup"><span data-stu-id="6c45e-114">Content description</span></span>                         | <span data-ttu-id="6c45e-115">Dosya</span><span class="sxs-lookup"><span data-stu-id="6c45e-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="6c45e-116">XLSX biçimindeki gelen dosya - şablon</span><span class="sxs-lookup"><span data-stu-id="6c45e-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="6c45e-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="6c45e-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="6c45e-118">XLSX biçimindeki gelen dosya - örnek veriler</span><span class="sxs-lookup"><span data-stu-id="6c45e-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="6c45e-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="6c45e-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="6c45e-120">Geçerli Dynamics 365 for Finance and Operation uygulamasında henüz [ER - Harici bir dosyadan veri içe aktarmak için gerekli yapılandırmaları oluşturma](./tasks/er-required-configurations-import-data.md) görev kılavuzunu oynatmadıysanız aşağıdaki dosyayı indirin.</span><span class="sxs-lookup"><span data-stu-id="6c45e-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Dynamics 365 for Finance and Operation application, download the following file.</span></span>

| <span data-ttu-id="6c45e-121">İçerik açıklaması</span><span class="sxs-lookup"><span data-stu-id="6c45e-121">Content description</span></span>    | <span data-ttu-id="6c45e-122">Dosya</span><span class="sxs-lookup"><span data-stu-id="6c45e-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6c45e-123">ER modeli yapılandırması</span><span class="sxs-lookup"><span data-stu-id="6c45e-123">ER model configuration</span></span> | [<span data-ttu-id="6c45e-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="6c45e-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
