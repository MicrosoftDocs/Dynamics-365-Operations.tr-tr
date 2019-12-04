---
title: Gelen belgeleri JSON biçiminde ayrıştırma
description: Bu konu, gelen belgeleri JavaScript Nesne Gösterimi (JSON) biçiminde ayrıştırmak için Elektronik raporlama (ER) biçimlerinin nasıl ayarlanacağını açıklamaktadır.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
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
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 8be4e225507a18a92d642ff0f3a6ca3d0ff68564
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772547"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="37b74-103">Gelen belgeleri JSON biçiminde ayrıştırma</span><span class="sxs-lookup"><span data-stu-id="37b74-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="37b74-104">JavaScript (başka bir deyişle JavaScript Nesne Gösterimi \[JSON\] biçimindeki dosyalar) tabanlı bir metin biçiminde verileri temsil eden elektronik belgeleri ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37b74-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="37b74-105">Bu özellik hakkında daha fazla bilgi edinmek için, aşağıdaki tabloda bulunan dosyaları yükleyin ve sonra da bir harici JSON dosyası görev kılavuzundaki verileri içe aktarmak üzere bir biçim yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="37b74-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="37b74-106">Bu görev kılavuzu, bir ER biçiminin uygulama verilerini güncelleştirmek üzere gelen bir JSON dosyasını ayrıştırmak için nasıl kullanılabileceğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="37b74-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="37b74-107">Ünvan</span><span class="sxs-lookup"><span data-stu-id="37b74-107">Title</span></span>                                  | <span data-ttu-id="37b74-108">Dosya adı</span><span class="sxs-lookup"><span data-stu-id="37b74-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="37b74-109">ER biçim yapılandırması</span><span class="sxs-lookup"><span data-stu-id="37b74-109">ER format configuration</span></span>                | [<span data-ttu-id="37b74-110">Satıcıların hareketlerini içe aktarma biçimi trans_JSON.xml</span><span class="sxs-lookup"><span data-stu-id="37b74-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="37b74-111">.cvs biçimindeki gelen dosya örneği</span><span class="sxs-lookup"><span data-stu-id="37b74-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="37b74-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="37b74-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="37b74-113">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="37b74-113">Requirements</span></span>

<span data-ttu-id="37b74-114">Bir ER biçim yapılandırması tamamlanmadan önce harici bir JSON dosyası görev kılavuzundan veri içe aktarmak için aşağıdaki gereksinimin karşılanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="37b74-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="37b74-115">JSON dosyasındaki üst öğeler yalnızca nesne öğeleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="37b74-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="37b74-116">Bir nesnenin iç içe yerleştirilmiş öğeleri özellik öğeleri olmalıdır ve böylece geçerli bir JSON yapısı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="37b74-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="37b74-117">JSON dizileri, bir nesnenin özellik öğelerinin yalnızca iç içe yerleştirilmiş öğelerdir.</span><span class="sxs-lookup"><span data-stu-id="37b74-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="37b74-118">JSON dizileri yalnızca JSON nesnelerini içerebilir.</span><span class="sxs-lookup"><span data-stu-id="37b74-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="37b74-119">Doğrudan dize/sayısal değerler ve iç içe diziler içeremez.</span><span class="sxs-lookup"><span data-stu-id="37b74-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="37b74-120">Bu dizilerde bulunan öğeler, (biçiminde belirtildiği gibi) sıralı olarak ayrıştırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="37b74-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="37b74-121">Her JSON nesnesindeki çokluluk ayarları dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="37b74-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="37b74-122">Ek olarak, henüz tamamlamadıysanız [ER Harici bir dosyadan veri almak için gerekli olan yapılandırmaları oluşturma](tasks/er-required-configurations-import-data.md) görev kılavuzunu tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="37b74-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="37b74-123">Görev kılavuzunu tamamlamak için aşağıdaki dosyayı indirin.</span><span class="sxs-lookup"><span data-stu-id="37b74-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="37b74-124">Ünvan</span><span class="sxs-lookup"><span data-stu-id="37b74-124">Title</span></span>                  | <span data-ttu-id="37b74-125">Dosya adı</span><span class="sxs-lookup"><span data-stu-id="37b74-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="37b74-126">ER modeli yapılandırması</span><span class="sxs-lookup"><span data-stu-id="37b74-126">ER model configuration</span></span> | [<span data-ttu-id="37b74-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="37b74-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
