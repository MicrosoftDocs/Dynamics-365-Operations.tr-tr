---
title: Mobil iş cihazında ilerlemeyi rapor etme
description: Bu yordam, iş cihazı kayıt formundaki üretim işiyle ilgili ilerlemenin nasıl başlatılacağını ve raporlanacağını gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationTouch, JmgRegistrationTouchUserConfiguration, JmgRegistrationTouchStart, JmgRegistrationTouchReportFeedback, JmgRegistrationTouchAssignedJobs, JmgRegistrationTouchBreak, JmgRegistrationTouchLeave, JmgRegistrationTouchIndirectActivity, JmgDialogForm, JmgRegistrationTouchReportProgress, JmgFeedbackWizard, JmgJobBundleProdFeedback
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34067902f05546b5c420feca633f77f16033ed2c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983904"
---
# <a name="report-progress-on-a-mobile-job-device"></a><span data-ttu-id="123b1-103">Mobil iş cihazında ilerlemeyi rapor etme</span><span class="sxs-lookup"><span data-stu-id="123b1-103">Report progress on a mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="123b1-104">Bu yordam, iş cihazı kayıt formundaki üretim işiyle ilgili ilerlemenin nasıl başlatılacağını ve raporlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="123b1-104">This procedure shows you how to start and report progress on a production job in the job device registration form.</span></span>



<span data-ttu-id="123b1-105">Bu yordamı çalıştırabilmek için kullanıcı hesabı ile ilişkili Sistem yöneticisi veya Makine operatörü rolünüz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="123b1-105">To be able to run this procedure you must have the System administator or Machine Operator role associated with the user account.</span></span>

1. <span data-ttu-id="123b1-106">Üretim denetimi > Üretim yürütme > İş kartı cihazı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="123b1-106">Go to Production control > Manufacturing execution > Job card device.</span></span>
2. <span data-ttu-id="123b1-107">WorkerTextField alanında çalışanın unvanını girin.</span><span class="sxs-lookup"><span data-stu-id="123b1-107">In the WorkerTextField field, enter the badge of a worker.</span></span> <span data-ttu-id="123b1-108">USMF demo verisinde Canan Yılmaz için '123' yazın...</span><span class="sxs-lookup"><span data-stu-id="123b1-108">In the USMF demo data type '123' for Christina Portra..</span></span>
3. <span data-ttu-id="123b1-109">Oturum aç'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-109">Click Log in.</span></span>
4. <span data-ttu-id="123b1-110">Filtre düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-110">Click the Filter button.</span></span>
5. <span data-ttu-id="123b1-111">Yapılandırma filtresi uygula onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="123b1-111">Check or uncheck the Apply configuration filter check box.</span></span> <span data-ttu-id="123b1-112">Bir filtre ayarlarsanız, USMF'de 110 üretim birimini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="123b1-112">If you set a filter you can use production unit 110 in USMF.</span></span>
6. <span data-ttu-id="123b1-113">Üretim birimi alanında, çalışanın çalışabileceği üretim işinin kaynak grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="123b1-113">In the Production unit field, select the ressource group for which production jobs the worker can work on.</span></span>
7. <span data-ttu-id="123b1-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="123b1-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="123b1-115">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="123b1-115">Click OK.</span></span>
9. <span data-ttu-id="123b1-116">İşi başlat düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-116">Click the Start job button.</span></span>
10. <span data-ttu-id="123b1-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="123b1-117">Click OK.</span></span>
11. <span data-ttu-id="123b1-118">İlerlemeyi raporla düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-118">Click the Report progress button.</span></span>
12. <span data-ttu-id="123b1-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="123b1-119">Click OK.</span></span>
13. <span data-ttu-id="123b1-120">Sonraki iş düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-120">Click the Next job button.</span></span>
14. <span data-ttu-id="123b1-121">Tüm üretim işlerine genel bakış düğmesini görmek için Atanan'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-121">Click the Assigned to see an overview of all production jobs button.</span></span>
15. <span data-ttu-id="123b1-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-122">Close the page.</span></span>
16. <span data-ttu-id="123b1-123">Mola düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-123">Click the Break button.</span></span>
17. <span data-ttu-id="123b1-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="123b1-124">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="123b1-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="123b1-125">Click OK.</span></span>
19. <span data-ttu-id="123b1-126">Ayrılma düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-126">Click the Leaving button.</span></span>
20. <span data-ttu-id="123b1-127">Oturumu kapatmak için seçin.</span><span class="sxs-lookup"><span data-stu-id="123b1-127">Select to log out.</span></span>
21. <span data-ttu-id="123b1-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="123b1-128">Click OK.</span></span>
22. <span data-ttu-id="123b1-129">WorkerTextField alanında yeniden oturum açın.</span><span class="sxs-lookup"><span data-stu-id="123b1-129">In the WorkerTextField field, log in again.</span></span> <span data-ttu-id="123b1-130">USMF demo verisinde '123' çalışanı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="123b1-130">You can select worker '123' in USMF demo data.</span></span>
23. <span data-ttu-id="123b1-131">Oturum aç'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-131">Click Log in.</span></span>
24. <span data-ttu-id="123b1-132">Molayı durdur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-132">Click Stop break.</span></span>
25. <span data-ttu-id="123b1-133">Faaliyet düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-133">Click the Activity button.</span></span>
26. <span data-ttu-id="123b1-134">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="123b1-134">Click Cancel.</span></span>
27. <span data-ttu-id="123b1-135">Ayrılma düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="123b1-135">Click the Leaving button.</span></span>
28. <span data-ttu-id="123b1-136">Erken çıkış için seçin.</span><span class="sxs-lookup"><span data-stu-id="123b1-136">Select to clock out.</span></span>
29. <span data-ttu-id="123b1-137">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="123b1-137">Click OK.</span></span>
30. <span data-ttu-id="123b1-138">Neden erken çıkış yapıldığının nedenini seçin.</span><span class="sxs-lookup"><span data-stu-id="123b1-138">Select a reason why you are clocking out early.</span></span>

