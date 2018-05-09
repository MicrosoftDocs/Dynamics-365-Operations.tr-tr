--- 
title: "Proje zaman çizelgelerini girme"
description: "Bu yöntem, bir zaman çizelgesini, boş zaman çizelgesi formu kullanarak oluşturmanızı sağlar."
author: kherr75
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.search.industry: Service industries
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b1ccaeffde4c288667fe797d07e08b5a346b4716
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="enter-project-timesheets"></a><span data-ttu-id="c78e7-103">Proje zaman çizelgelerini girme</span><span class="sxs-lookup"><span data-stu-id="c78e7-103">Enter project timesheets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c78e7-104">Bu yöntem, bir zaman çizelgesini, boş zaman çizelgesi formu kullanarak oluşturmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="c78e7-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="c78e7-105">Yeni Zaman Çizelgesi, önceki bir zaman çizelgesi bilgilerini veya Sık Kullanılanlarım sayfasındaki proje ve faaliyet atamalarını baz alabilir.</span><span class="sxs-lookup"><span data-stu-id="c78e7-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the My favorites page.</span></span> <span data-ttu-id="c78e7-106">Varsayılan olarak, tüm zaman çizelgeleri listesi sayfası, geçerli dönem için tüm zaman çizelgelerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c78e7-106">By default, the All timesheets list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="c78e7-107">Çizelgelerim sayfasındaki Göster alanındaki aşağı açılan listeyi, çizelgeleri süre ya da proje zaman çizelgesi listesine göre filtrelemek, veya diğer çalışanlar adına oluşturulan zaman çizelgelerini görüntülemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c78e7-107">You can use the drop-down list for the Show field in the My timesheets page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="c78e7-108">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USSI'dir.</span><span class="sxs-lookup"><span data-stu-id="c78e7-108">The demo data company used to create this procedure is USSI.</span></span> <span data-ttu-id="c78e7-109">Bu yöntemi başlatmak için: Proje yönetimi ve muhasebe > Zaman çizelgeleri > Çizelgelerim seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-109">To begin this procedure, go to Project management and accounting > Timesheets >My timesheets</span></span>

1. <span data-ttu-id="c78e7-110">Yeni bir zaman çizelgesi girmek için yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c78e7-110">To enter a new timesheet, click New.</span></span>
    * <span data-ttu-id="c78e7-111">Kaynak aşağı açılan listesi varsayılan olarak mevcut kullanıcıya atanmış olan çalışanı gösterir.</span><span class="sxs-lookup"><span data-stu-id="c78e7-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    * <span data-ttu-id="c78e7-112">Kullanıcı, bir temsilci olarak belirlendiyse, bu durum adları kullanıcının kendi adına bir zaman çizelgesi girebileceği şekilde listeler.</span><span class="sxs-lookup"><span data-stu-id="c78e7-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
2. <span data-ttu-id="c78e7-113">Tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-113">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="c78e7-114">Bu seçenek işaretliyse, Sık Kullanılanlar olarak yapılandırılmış olan zaman çizelgesi ayarları kullanarak yeni zaman çizelgesi satırları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c78e7-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
3. <span data-ttu-id="c78e7-115">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c78e7-115">Click OK.</span></span>
4. <span data-ttu-id="c78e7-116">Yeni satırına tıklayın</span><span class="sxs-lookup"><span data-stu-id="c78e7-116">Click New line.</span></span>
5. <span data-ttu-id="c78e7-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c78e7-118">Tüzel kişilik alanı mevcut tüzel kişiliği varsayılan olarak görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c78e7-118">The Legal Entity field displays the current Legal entity by default.</span></span>   
6. <span data-ttu-id="c78e7-119">Proje alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c78e7-119">In the Project field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c78e7-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-120">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c78e7-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c78e7-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c78e7-122">Faaliyet alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c78e7-122">In the Activity field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="c78e7-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-123">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="c78e7-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c78e7-124">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="c78e7-125">Kategori alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c78e7-125">In the Category field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="c78e7-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-126">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="c78e7-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c78e7-127">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="c78e7-128">Her bir gün için çalışılan saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-128">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="c78e7-129">Saatleri ondalık biçiminde girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c78e7-129">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="c78e7-130">Örneğin, iki saat on beş dakika çalıştıysanız 2,25 değerini girin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
16. <span data-ttu-id="c78e7-131">Her bir gün için çalışılan saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-131">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="c78e7-132">Saatleri ondalık biçiminde girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c78e7-132">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="c78e7-133">Örneğin, iki saat on beş dakika çalıştıysanız 2,25 değerini girin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-133">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="c78e7-134">Her bir gün için çalışılan saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-134">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="c78e7-135">Saatleri ondalık biçiminde girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c78e7-135">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="c78e7-136">Örneğin, iki saat on beş dakika çalıştıysanız 2,25 değerini girin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-136">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
18. <span data-ttu-id="c78e7-137">Her bir gün için çalışılan saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-137">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="c78e7-138">Saatleri ondalık biçiminde girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c78e7-138">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="c78e7-139">Örneğin, iki saat on beş dakika çalıştıysanız 2,25 değerini girin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-139">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
19. <span data-ttu-id="c78e7-140">Her bir gün için çalışılan saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-140">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="c78e7-141">Saatleri ondalık biçiminde girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c78e7-141">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="c78e7-142">Örneğin, iki saat on beş dakika çalıştıysanız 2,25 değerini girin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-142">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
    * <span data-ttu-id="c78e7-143">Satır detaylarında aşağıdaki güncelleştirme seçenekleri mevcuttur:  o  Vergi ve mali boyutlar hakkında bilgi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-143">In Line details, the following options are available:  o  Add information about taxes and financial dimensions.</span></span>  <span data-ttu-id="c78e7-144">o    Zaman çizelgesi satırı hakkında açıklamalar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c78e7-144">o    Add comments about the timesheet line.</span></span>  
20. <span data-ttu-id="c78e7-145">İletişim kutusu formunu açmak için İş akışı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c78e7-145">Click Workflow to open the drop dialog.</span></span>
21. <span data-ttu-id="c78e7-146">Gönder'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c78e7-146">Click Submit.</span></span>
22. <span data-ttu-id="c78e7-147">Gönder'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c78e7-147">Click Submit.</span></span>


