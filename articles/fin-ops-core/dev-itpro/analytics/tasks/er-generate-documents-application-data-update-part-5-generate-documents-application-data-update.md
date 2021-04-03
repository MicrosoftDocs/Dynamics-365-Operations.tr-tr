---
title: Uygulama verileri içeren belgeler oluşturma
description: Bu yordamdaki adımları tamamlamak için ilk önce "ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 4 - Biçimi değiştir)" yordamını tamamlamalısınız.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c474f4bc7940a429ed62870e00302c93581eb9a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569593"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="f9067-103">Uygulama verileri içeren belgeler oluşturma</span><span class="sxs-lookup"><span data-stu-id="f9067-103">Generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9067-104">Bu yordamdaki adımları tamamlamak için ilk önce "ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 4 - Biçimi değiştir)" yordamını tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="f9067-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 4: Modify format)".</span></span>



<span data-ttu-id="f9067-105">Bu yordamdaki adımlar bir Elektronik raporlama (ER) yapılandırmasının, bir elektronik belge oluşturmak ve uygulama verisini güncelleştirmek için nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="f9067-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="f9067-106">Bu yordamda, Intrastat raporunu oluşturmak ve raporlama işleminin arşivleme ayrıntıları için uygulama verisini güncelleştirmek amacıyla ER biçim yapılandırmasını çalıştırırsınız.</span><span class="sxs-lookup"><span data-stu-id="f9067-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="f9067-107">Bu yordam, sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="f9067-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="f9067-108">Bu adımlar DEMF veri kümesi kullanılarak tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="f9067-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="f9067-109">Başlamadan önce DEMF şirketin ülke bağlamının BEL (Belçika) olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="f9067-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="f9067-110">Dış ticaret parametreleri ayarla</span><span class="sxs-lookup"><span data-stu-id="f9067-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="f9067-111">Vergi > Kurulum > Dış Ticaret > Dış Ticaret parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f9067-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="f9067-112">Numara serileri sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f9067-112">Click the Number sequences tab.</span></span>

    <span data-ttu-id="f9067-113">Instrastat raporlama işlemlerinin arşivleme ayrıntıları, oluşturduğumuz her arşivin kaydını tanımlamamız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f9067-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="f9067-114">Bunun için özel bir numara serisinin yapılandırılmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f9067-114">A special number sequence must be configured for that.</span></span>  

3. <span data-ttu-id="f9067-115">'Intrastat arşiv kodu' referansını seçin.</span><span class="sxs-lookup"><span data-stu-id="f9067-115">Select the 'Intrastat archive ID' reference.</span></span>
4. <span data-ttu-id="f9067-116">Numara serisi kodu alanında, bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f9067-116">In the Number sequence code field, type a value.</span></span>

    <span data-ttu-id="f9067-117">'Numara sırası kodu' alanında, 'Fore_2' değerini girin ya da seçin.</span><span class="sxs-lookup"><span data-stu-id="f9067-117">In the 'Number sequence code' field, enter or select the value 'Fore_2'.</span></span>  

5. <span data-ttu-id="f9067-118">Numara serisi kodunu ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="f9067-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="f9067-119">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f9067-119">Click Save.</span></span>
7. <span data-ttu-id="f9067-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f9067-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="f9067-121">Değiştirilen ER biçimini çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f9067-121">Run modified ER format</span></span>
1. <span data-ttu-id="f9067-122">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="f9067-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f9067-123">Ağaçta, 'Intrastat (model)' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="f9067-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="f9067-124">Ağaçta, 'Intrastat (model)\Intrastat (biçim)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f9067-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="f9067-125">Çalıştır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f9067-125">Click Run.</span></span>
5. <span data-ttu-id="f9067-126">Dosya adı gir alanında, 'intrastat2.xml' yazın.</span><span class="sxs-lookup"><span data-stu-id="f9067-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
6. <span data-ttu-id="f9067-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f9067-127">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="f9067-128">ER biçimi yürütmesine ait sonuçları gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="f9067-128">Review ER format execution's results</span></span>
<span data-ttu-id="f9067-129">Oluşturulan XML dosyasını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="f9067-129">Review the generated XML file.</span></span>  
1. <span data-ttu-id="f9067-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f9067-130">Close the page.</span></span>
2. <span data-ttu-id="f9067-131">Vergi > Bildirimler > Dış ticaret > Intrastat öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f9067-131">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>

    <span data-ttu-id="f9067-132">Oluşturulan elektronik belgeye dahil edilmiş olan Intrastat hareketlerini görüntülemek için bunları içeren formu açın.</span><span class="sxs-lookup"><span data-stu-id="f9067-132">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  

3. <span data-ttu-id="f9067-133">Intrastat arşivini tıklat.</span><span class="sxs-lookup"><span data-stu-id="f9067-133">Click Intrastat archive.</span></span>

    <span data-ttu-id="f9067-134">Çalıştırılan ER biçimi uygulama veri güncelleştirmesi için herhangi bir ayarı şimdi içerdiğinden, tamamlanan Intrastat raporlamasının ayrıntıları arşivlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="f9067-134">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="f9067-135">Bu formda oluşturulan arşivin başlık kaydını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9067-135">In this form, you can see the header record of the created archive.</span></span>  

4. <span data-ttu-id="f9067-136">Ayrıntılar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f9067-136">Click Details.</span></span>

    <span data-ttu-id="f9067-137">Bu formda oluşturulan arşivin ayrıntılarını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9067-137">In this form, you can see the details for the created archive.</span></span>  

5. <span data-ttu-id="f9067-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f9067-138">Close the page.</span></span>
6. <span data-ttu-id="f9067-139">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f9067-139">Close the page.</span></span>
7. <span data-ttu-id="f9067-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f9067-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]