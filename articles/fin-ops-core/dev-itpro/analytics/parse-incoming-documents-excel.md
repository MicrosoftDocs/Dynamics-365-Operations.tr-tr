---
title: Gelen belgeleri Excel biçiminde ayrıştırma
description: Bu konu, gelen Microsoft Excel dosyalarındaki içeriği ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlama hakkında bilgi vermektedir.
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0c41a062d817307adb2889d3678764f1ea4066e2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755192"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="aed70-103">Genel belgeleri Excel biçiminde ayrıştırma</span><span class="sxs-lookup"><span data-stu-id="aed70-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="aed70-104">Microsoft Excel çalışma kitaplarındaki (XLSX biçimindeki dosyalar) verileri temsil eden gelen Microsoft Excel dosyalarını ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aed70-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="aed70-105">Bunun ardından, uygulama verilerini güncelleştirmek için bu dosyalardaki içeriği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aed70-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="aed70-106">Bu, şunu yaptığınız zaman size yarar sağlar:</span><span class="sxs-lookup"><span data-stu-id="aed70-106">This is useful if you:</span></span>

- <span data-ttu-id="aed70-107">Yeni bir model ve biçim tasarlamak ve çalıştırma zamanında bunları test etmek.</span><span class="sxs-lookup"><span data-stu-id="aed70-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="aed70-108">Bu durumda, Excel gerçek uygulama verilerinin benzetimini yapacaktır.</span><span class="sxs-lookup"><span data-stu-id="aed70-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="aed70-109">Uygulamanızın dışında, verileri Excel'de yönetmek ve belirli bir rapor gönderme amacıyla bu verileri içe aktarmak.</span><span class="sxs-lookup"><span data-stu-id="aed70-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="aed70-110">Bu özellik hakkında daha fazla bilgi için, **ER - Microsoft Excel dosyasından verileri içe aktarma (Bölüm 1: Biçim tasarlama)** ve **ER - Microsoft Excel dosyasından verileri içe aktarma (Bölüm 2: Verileri içe aktarma)** (7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677) iş sürecinin parçaları).</span><span class="sxs-lookup"><span data-stu-id="aed70-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="aed70-111">Bu görev kılavuzları, gelen belgelerden bilgileri içe aktarmak ve uygulama verilerini güncelleştirmek için, ER biçimi kullanarak, gelen Excel dosyasının nasıl ayrıştırılabileceği konusunda size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="aed70-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="aed70-112">Görev kılavuzu dosyalarını [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684)'dan indirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aed70-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="aed70-113">Yukarıda sözü edilen görev kılavuzlarını tamamlamak için aşağıdaki dosyaları indirin:</span><span class="sxs-lookup"><span data-stu-id="aed70-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="aed70-114">İçerik açıklaması</span><span class="sxs-lookup"><span data-stu-id="aed70-114">Content description</span></span>                         | <span data-ttu-id="aed70-115">Dosya</span><span class="sxs-lookup"><span data-stu-id="aed70-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="aed70-116">XLSX biçimindeki gelen dosya - şablon</span><span class="sxs-lookup"><span data-stu-id="aed70-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="aed70-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="aed70-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="aed70-118">XLSX biçimindeki gelen dosya - örnek veriler</span><span class="sxs-lookup"><span data-stu-id="aed70-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="aed70-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="aed70-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="aed70-120">Finance and Operations uygulamasında henüz [ER - Harici bir dosyadan veri içeri aktarmak için gerekli yapılandırmaları oluşturma](./tasks/er-required-configurations-import-data.md) görev kılavuzunu yürütmediyseniz aşağıdaki dosyayı indirin.</span><span class="sxs-lookup"><span data-stu-id="aed70-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Finance and Operations application, download the following file.</span></span>

| <span data-ttu-id="aed70-121">İçerik açıklaması</span><span class="sxs-lookup"><span data-stu-id="aed70-121">Content description</span></span>    | <span data-ttu-id="aed70-122">Dosya</span><span class="sxs-lookup"><span data-stu-id="aed70-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="aed70-123">ER modeli yapılandırması</span><span class="sxs-lookup"><span data-stu-id="aed70-123">ER model configuration</span></span> | [<span data-ttu-id="aed70-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="aed70-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]