---
title: "Oluşturulan dosyaları dosya boyutu ve içerik miktarına göre bölme"
description: "Bu konu, oluşturulan dosyaların dosya boyutuna ve içerik öğesi miktarına göre nasıl bölüneceği hakkında bilgi sağlamaktadır."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: afdf5b2596af7641182be50ced8159967164b115
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2018

---

# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a><span data-ttu-id="8837e-103">Oluşturulan XML dosyalarını dosya boyutu ve içerik miktarına göre bölme</span><span class="sxs-lookup"><span data-stu-id="8837e-103">Split generated XML files based on file size and content quantity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8837e-104">XML biçiminde giden belgeler oluşturmak için Elektronik raporlama (ER) biçimleri tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8837e-104">You can design Electronic reporting (ER) formats to generate outgoing documents in XML format.</span></span> <span data-ttu-id="8837e-105">Bazen bu belgeler yalnızca belirli ölçütleri (maksimum dosya boyutu, bazı XML düğümlerinin maksimum sayısı vb.) karşıladıkları zaman kabul edilebilir.</span><span class="sxs-lookup"><span data-stu-id="8837e-105">Sometimes, those documents can be accepted only when they meet specific criteria, such a maximum file size or a maximum number of some XML nodes.</span></span> <span data-ttu-id="8837e-106">Bu belgelerin alıcılarının belirttiği gereksinimleri karşılayan elektronik belgeler oluşturmak için ER biçimleri tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8837e-106">You can design ER formats to generate electronic documents that satisfy the requirements that the recipients of those documents specify.</span></span>

- <span data-ttu-id="8837e-107">FILE biçim öğesi için, ER ifadesi olarak bir dosya boyutu sınırı tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8837e-107">For the FILE format element, you can define a limit on the file size as an ER expression.</span></span> <span data-ttu-id="8837e-108">Bir ER raporu oluşturulurken, tanımlanan sınır aşılırsa, ER o geçerli dosyayı oluşturmayı bitirir ve sonraki dosyayı oluşturmaya geçer.</span><span class="sxs-lookup"><span data-stu-id="8837e-108">If the defined limit is exceeded when an ER report is generated, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="8837e-109">Herhangi bir XML ELEMENT biçimi için, ER ifadesi olarak bir öğe sayısı sınırı tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8837e-109">For any XML ELEMENT format, you can define a limit on the number of elements as an ER expression.</span></span> <span data-ttu-id="8837e-110">Bir ER raporu çalıştırılırken, oluşturulan dosyadaki XML düğümü sayısı aşılırsa, ER o geçerli dosyayı oluşturmayı bitirir ve sonraki dosyayı oluşturmaya geçer.</span><span class="sxs-lookup"><span data-stu-id="8837e-110">If the number of XML nodes in the file that is generated exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="8837e-111">Herhangi bir XML SEQUENCE biçim öğesi için, ER ifadesi olarak bir alt öğe sayısı sınırı tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8837e-111">For any XML SEQUENCE format element, you can define a limit on the number of child elements as an ER expression.</span></span> <span data-ttu-id="8837e-112">Bir ER raporu çalıştırılırken, oluşturulan dosyadaki biçim öğesinin iç içe XML düğümü sayısı aşılırsa, ER o geçerli dosyayı oluşturmayı bitirir ve sonraki dosyayı oluşturmaya geçer.</span><span class="sxs-lookup"><span data-stu-id="8837e-112">If the number of nested XML nodes of the format element in the generated file exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="8837e-113">Bir XML ELEMENT biçim öğesini bölünemez olarak işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8837e-113">You can mark any XML ELEMENT format element as non-breakable.</span></span> <span data-ttu-id="8837e-114">Bu sayede, biçim öğesi altında oluşturulan XML düğümlerinin iç içe öğelerini, oluşturulan tek bir dosyada tutabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8837e-114">In this way, you can keep the nested items of XML nodes that are generated under the format element in a single generated file.</span></span>

<span data-ttu-id="8837e-115">Oluşturulan dosyaya XML düğümleri eklemek için XML ELEMENT ve XML SEQUENCE biçim öğelerinin yanı sıra, RAW XML biçim öğesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8837e-115">In addition to using the XML ELEMENT and XML SEQUENCE format elements to add XML nodes to the generated file, you can use the RAW XML format element.</span></span> <span data-ttu-id="8837e-116">Ancak, öğe sayısındaki sınırları değerlendirmek için düğüm sayısı hesaplanırken, RAW XML biçim öğesini kullanarak eklediğiniz düğümler hesaba katılmaz.</span><span class="sxs-lookup"><span data-stu-id="8837e-116">However, nodes that you add by using the RAW XML format element aren't considered when the number of nodes is calculated to evaluate the limits on the number of elements.</span></span>

<span data-ttu-id="8837e-117">Belirlenen sınırlar her aşıldığında, oluşturulan çıktıyı bölmek için yapılandırılmış bir FILE biçim öğesine ilişkin dosya hedefleri yapılandırdıysanız, oluşturulan çıktının her bir parçası ayrı birer dosya olarak, yapılandırılan dosya hedefine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="8837e-117">If you configured file destinations for a FILE format element that has been configured to split the generated output whenever specific limits are exceeded, each piece of generated output is sent to the configured file destination as an individual file.</span></span> <span data-ttu-id="8837e-118">Çıktının bölünmesiyle oluşturulan dosyalara benzersiz adlar vermek için, FILE biçim öğesine ilişkin bir ER ifadesi yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8837e-118">To uniquely name the files that are created by splitting the output, you must configure an ER expression for the FILE format element.</span></span> <span data-ttu-id="8837e-119">NUMBER SEQUENCE türünde bir ER veri kaynağı eklerseniz, bölünen çıktının her bir parçası için, artan düzende sıra numarası eklenir.</span><span class="sxs-lookup"><span data-stu-id="8837e-119">If you include an ER data source of the NUMBER SEQUENCE type, the number sequence will be incremented for each piece of the split output.</span></span>

<span data-ttu-id="8837e-120">Bu özellik hakkında daha fazla bilgi için, **7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin bir parçası olan ve [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684)'dan indirilebilen **ER - XML dosyalarını dosya boyutu ve içerik miktarına göre bölme** görev kılavuzunu oynatın.</span><span class="sxs-lookup"><span data-stu-id="8837e-120">To learn more about this feature, play the **ER Split XML files based on the file size or content item quantity** task guide, which is part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="8837e-121">Bu görev kılavuzu, oluşturulan dosyaları dosya boyutu ve içerik öğesi miktarı sınırlarına göre bölmek için bir ER biçimi yapılandırma işleminde size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="8837e-121">This task guide walks you through the process of configuring an ER format to split generated files based on limits on the file size and content item quantity.</span></span> <span data-ttu-id="8837e-122">Görev kılavuzunu tamamlamak için aşağıdaki dosyaları indirmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="8837e-122">To complete the task guide, you must download the following files:</span></span>

- [<span data-ttu-id="8837e-123">ER modeli yapılandırması - XmlFilesSplittingModel.xml</span><span class="sxs-lookup"><span data-stu-id="8837e-123">ER model configuration - XmlFilesSplittingModel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
- [<span data-ttu-id="8837e-124">ER biçimi yapılandırması - XmlFilesSplittingFormat.xml</span><span class="sxs-lookup"><span data-stu-id="8837e-124">ER format configuration - XmlFilesSplittingFormat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a><span data-ttu-id="8837e-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8837e-125">Additional resources</span></span>
[<span data-ttu-id="8837e-126">Elektronik raporlama hedefleri</span><span class="sxs-lookup"><span data-stu-id="8837e-126">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="8837e-127">Elektronik raporlamada formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="8837e-127">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

