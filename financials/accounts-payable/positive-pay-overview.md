---
title: "Pozitif ödemeye genel bakış"
description: "Bu makalede bir bankaya sunulabilecek çeklerin bir elektronik listesinin oluşturulması için kullanılan pozitif ödemeler hakkında bilgi verilmiştir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5b88b940e7a590ff99b6ab8a99ce45d32dfe0505
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---

# <a name="positive-pay-overview"></a><span data-ttu-id="1be0a-103">Pozitif ödemeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="1be0a-103">Positive pay overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1be0a-104">Bu makalede bir bankaya sunulabilecek çeklerin bir elektronik listesinin oluşturulması için kullanılan pozitif ödemeler hakkında bilgi verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="1be0a-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="1be0a-105">Pozitif ödeme, bir bankaya sunulabilecek çeklerin bir elektronik listesinin oluşturulması için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1be0a-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="1be0a-106">Pozitif ödeme dosyaları, bankaların çek sahteciliğini önlemesine yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="1be0a-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="1be0a-107">Çeklerin her yazıldığında çeklerin bir elektronik listesini oluşturmak için pozitif ödemeyi oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="1be0a-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="1be0a-108">Ardından, bankaya bir çek sunulduğunda, banka bu çeki daha önce göndermiş olduğunuz çek listesiyle karşılaştırır.</span><span class="sxs-lookup"><span data-stu-id="1be0a-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="1be0a-109">Çek, çek listesindeki bir çekle uyuşuyorsa banka çeki serbest bırakır.</span><span class="sxs-lookup"><span data-stu-id="1be0a-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="1be0a-110">Çek, listedeki bir çekle uyuşmuyorsa banka, çeki gözden geçirmek için tutar.</span><span class="sxs-lookup"><span data-stu-id="1be0a-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="1be0a-111">Pozitif ödeme SafePay olarak da bilinir.</span><span class="sxs-lookup"><span data-stu-id="1be0a-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="1be0a-112">Pozitif ödeme dosyaları, alacaklar ve çek tutarları hakkında hassas bilgiler içermektedir.</span><span class="sxs-lookup"><span data-stu-id="1be0a-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="1be0a-113">Bu nedenle, banka tarafından alınana kadar dosyaların oluşturulduğu süreden itibaren uygun güvenlik önlemlerini uyguladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="1be0a-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="1be0a-114">Pozitif ödeme dosyaları, web tarayıcısının karşıdan yükleme yönergelerine göre yüklenir.</span><span class="sxs-lookup"><span data-stu-id="1be0a-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="1be0a-115">Pozitif ödeme dosyaları veri varlıkları kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1be0a-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="1be0a-116">Bir pozitif ödeme dosyası oluşturmadan önce verileri bankanın işleme koyabileceği bir biçime dönüştüren XML için dönüştürme biçimlerini oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1be0a-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="1be0a-117">Pozitif ödeme bilgisi oluşturmak istediğiniz her bir banka hesabı için, pozitif ödeme biçimini atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1be0a-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="1be0a-118">Ödemeleri oluşturduktan sonra tek bir tüzel kişilik ve tek bir banka hesabı için bir pozitif ödeme dosyası oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1be0a-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="1be0a-119">Alternatif olarak, birden fazla tüzel kişilik ve banka hesabı için aynı anda pozitif ödeme dosyaları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1be0a-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="1be0a-120">Bir pozitif ödeme dosyasında listelenen çekler ödendikten sonra bankanızdan bir onay numarası alırsınız.</span><span class="sxs-lookup"><span data-stu-id="1be0a-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="1be0a-121">Ardından, pozitif ödeme dosyasını Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümünde onaylayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1be0a-121">You can then confirm the positive pay file in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> 

<span data-ttu-id="1be0a-122">Bir pozitif ödeme dosyasını değiştirmeniz gerekiyorsa, bunu geri çağırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1be0a-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="1be0a-123">Ardından, pozitif ödeme dosyasındaki her bir çek için, çekin bir pozitif ödeme dosyasına dahil edilip edilmeyeceğini gösteren alan sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="1be0a-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="1be0a-124">Daha fazla bilgi için bkz. [Pozitif ödeme dosyaları kurma ve oluşturma](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="1be0a-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>




