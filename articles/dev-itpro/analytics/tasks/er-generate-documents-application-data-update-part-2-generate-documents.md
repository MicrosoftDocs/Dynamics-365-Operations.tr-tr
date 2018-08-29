--- 
title: "Uygulama verileri içeren belgeler oluşturmak için yapılandırmalar tasarlama"
description: "Bu yordamdaki adımları tamamlamak için ilk önce ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 1 - Yapılandırmaları içe aktar) yordamını tamamlamalısınız."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8376107a33dd83e04f82fcab6847e7f073f08dbc
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="d1413-103">Uygulama verileri içeren belgeler oluşturmak için yapılandırmalar tasarlama</span><span class="sxs-lookup"><span data-stu-id="d1413-103">Design configurations to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1413-104">Bu yordamdaki adımları tamamlamak için ilk önce ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 1: Yapılandırmaları içe aktar) yordamını tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="d1413-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="d1413-105">Bu yordamdaki adımlar bir Elektronik raporlama (ER) yapılandırmasının, bir elektronik belge oluşturmak için nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="d1413-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="d1413-106">Bu yordamda, örnek şirket Litware Inc. için oluşturulmuş ER içe aktarılan biçim yapılandırmasını çalıştırırsınız.</span><span class="sxs-lookup"><span data-stu-id="d1413-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="d1413-107">Bu yordam, sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="d1413-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="d1413-108">Bu adımlar DEMF veri kümesi kullanılarak tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="d1413-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="d1413-109">Başlamadan önce, DEMF şirketi için ülke bağlamını DEU'dan (Almanya) BEL'e (Belçika) çevirin.</span><span class="sxs-lookup"><span data-stu-id="d1413-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="d1413-110">Tüzel varlık DEMF'in birincil adresindeki ülke kodunu güncelleştirmek için Kuruluş yönetimi > Kuruluşlar > Tüzel kişilikler seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d1413-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="d1413-111">Uygulamanızı yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="d1413-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="d1413-112">İçe aktarılan ER biçimini çalıştır</span><span class="sxs-lookup"><span data-stu-id="d1413-112">Run imported ER format</span></span>
1. <span data-ttu-id="d1413-113">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="d1413-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d1413-114">Ağaçta, 'Intrastat (model)' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="d1413-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="d1413-115">Ağaçta, 'Intrastat (model)\Intrastat (biçim)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d1413-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="d1413-116">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d1413-116">Click Run.</span></span>
    * <span data-ttu-id="d1413-117">Intrstat raporunu oluşturmak için ER biçim yapılandırmasının taslak sürümünü çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d1413-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="d1413-118">Dosya adı gir alanında, 'intrastat.xml' yazın.</span><span class="sxs-lookup"><span data-stu-id="d1413-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="d1413-119">Dosyanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d1413-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="d1413-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d1413-120">Click OK.</span></span>
    * <span data-ttu-id="d1413-121">Oluşturulan XML dosyasını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="d1413-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="d1413-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d1413-122">Close the page.</span></span>
8. <span data-ttu-id="d1413-123">Vergi > Bildirimler > Dış ticaret > Intrastat öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d1413-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="d1413-124">Oluşturulan elektronik belgeye dahil edilen Intrastat hareketlerini görüntülemek için bu formu açın.</span><span class="sxs-lookup"><span data-stu-id="d1413-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="d1413-125">Intrastat arşivini tıklat.</span><span class="sxs-lookup"><span data-stu-id="d1413-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="d1413-126">Çalıştırılan ER biçimi uygulama veri güncelleştirmesi için herhangi bir ayar içermediğinden, tamamlanan Intrasta raporunun ayrıntıları arşivlenmez.</span><span class="sxs-lookup"><span data-stu-id="d1413-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="d1413-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d1413-127">Close the page.</span></span>
11. <span data-ttu-id="d1413-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d1413-128">Close the page.</span></span>


