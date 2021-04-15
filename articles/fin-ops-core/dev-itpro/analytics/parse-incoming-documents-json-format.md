---
title: Gelen belgeleri JSON biçiminde ayrıştırma
description: Bu konu, gelen belgeleri JavaScript Nesne Gösterimi (JSON) biçiminde ayrıştırmak için Elektronik raporlama (ER) biçimlerinin nasıl ayarlanacağını açıklamaktadır.
author: kfend
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 4e598dc15b619c2f6a0525ea18c371484ca26fa4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755166"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="d7984-103">Gelen belgeleri JSON biçiminde ayrıştırma</span><span class="sxs-lookup"><span data-stu-id="d7984-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d7984-104">JavaScript (başka bir deyişle JavaScript Nesne Gösterimi \[JSON\] biçimindeki dosyalar) tabanlı bir metin biçiminde verileri temsil eden elektronik belgeleri ayrıştırmak için Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d7984-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="d7984-105">Bu özellik hakkında daha fazla bilgi edinmek için, aşağıdaki tabloda bulunan dosyaları yükleyin ve sonra da bir harici JSON dosyası görev kılavuzundaki verileri içe aktarmak üzere bir biçim yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d7984-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="d7984-106">Bu görev kılavuzu, bir ER biçiminin uygulama verilerini güncelleştirmek üzere gelen bir JSON dosyasını ayrıştırmak için nasıl kullanılabileceğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="d7984-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="d7984-107">Ünvan</span><span class="sxs-lookup"><span data-stu-id="d7984-107">Title</span></span>                                  | <span data-ttu-id="d7984-108">Dosya adı</span><span class="sxs-lookup"><span data-stu-id="d7984-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="d7984-109">ER biçim yapılandırması</span><span class="sxs-lookup"><span data-stu-id="d7984-109">ER format configuration</span></span>                | [<span data-ttu-id="d7984-110">Satıcıların hareketlerini içe aktarma biçimi trans_JSON.xml</span><span class="sxs-lookup"><span data-stu-id="d7984-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="d7984-111">.cvs biçimindeki gelen dosya örneği</span><span class="sxs-lookup"><span data-stu-id="d7984-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="d7984-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="d7984-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="d7984-113">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="d7984-113">Requirements</span></span>

<span data-ttu-id="d7984-114">Bir ER biçim yapılandırması tamamlanmadan önce harici bir JSON dosyası görev kılavuzundan veri içe aktarmak için aşağıdaki gereksinimin karşılanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="d7984-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="d7984-115">JSON dosyasındaki üst öğeler yalnızca nesne öğeleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="d7984-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="d7984-116">Bir nesnenin iç içe yerleştirilmiş öğeleri özellik öğeleri olmalıdır ve böylece geçerli bir JSON yapısı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d7984-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="d7984-117">JSON dizileri, bir nesnenin özellik öğelerinin yalnızca iç içe yerleştirilmiş öğelerdir.</span><span class="sxs-lookup"><span data-stu-id="d7984-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="d7984-118">JSON dizileri yalnızca JSON nesnelerini içerebilir.</span><span class="sxs-lookup"><span data-stu-id="d7984-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="d7984-119">Doğrudan dize/sayısal değerler ve iç içe diziler içeremez.</span><span class="sxs-lookup"><span data-stu-id="d7984-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="d7984-120">Bu dizilerde bulunan öğeler, (biçiminde belirtildiği gibi) sıralı olarak ayrıştırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="d7984-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="d7984-121">Her JSON nesnesindeki çokluluk ayarları dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="d7984-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="d7984-122">Ek olarak, henüz tamamlamadıysanız [ER Harici bir dosyadan veri almak için gerekli olan yapılandırmaları oluşturma](tasks/er-required-configurations-import-data.md) görev kılavuzunu tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d7984-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="d7984-123">Görev kılavuzunu tamamlamak için aşağıdaki dosyayı indirin.</span><span class="sxs-lookup"><span data-stu-id="d7984-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="d7984-124">Ünvan</span><span class="sxs-lookup"><span data-stu-id="d7984-124">Title</span></span>                  | <span data-ttu-id="d7984-125">Dosya adı</span><span class="sxs-lookup"><span data-stu-id="d7984-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="d7984-126">ER modeli yapılandırması</span><span class="sxs-lookup"><span data-stu-id="d7984-126">ER model configuration</span></span> | [<span data-ttu-id="d7984-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="d7984-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]