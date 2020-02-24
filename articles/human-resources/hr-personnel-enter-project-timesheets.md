---
title: Proje zaman çizelgelerini girme
description: Bu yöntem, bir zaman çizelgesini, boş zaman çizelgesi formu kullanarak oluşturmanızı sağlar.
author: andreabichsel
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Human Resources
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 136efa1178089adb88820002a19e99ef83e1b47e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010897"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="10b22-103">Proje zaman çizelgelerini girme</span><span class="sxs-lookup"><span data-stu-id="10b22-103">Enter project timesheets</span></span>



<span data-ttu-id="10b22-104">Bu yöntem, bir zaman çizelgesini, boş zaman çizelgesi formu kullanarak oluşturmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="10b22-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="10b22-105">Yeni Zaman Çizelgesi, önceki bir zaman çizelgesi bilgilerini veya **Sık Kullanılanlarım** sayfasındaki proje ve faaliyet atamalarını baz alabilir.</span><span class="sxs-lookup"><span data-stu-id="10b22-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="10b22-106">Varsayılan olarak, **Tüm zaman çizelgeleri** listesi sayfası, geçerli dönem için tüm zaman çizelgelerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="10b22-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="10b22-107">**Çizelgelerim** sayfasındaki **Göster** alanındaki aşağı açılan listeyi, çizelgeleri süre ya da proje zaman çizelgesi listesine göre filtrelemek, veya diğer çalışanlar adına oluşturulan zaman çizelgelerini görüntülemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10b22-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="10b22-108">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USSI'dir.</span><span class="sxs-lookup"><span data-stu-id="10b22-108">The demo data company used to create this procedure is USSI.</span></span> 

1. <span data-ttu-id="10b22-109">**Gezinti bölmesi**'nde **Modüller > Proje yönetimi muhasebe parametreleri > Zaman çizelgeleri > Benim zaman çizelgelerim**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="10b22-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="10b22-110">Yeni bir zaman çizelgesi girmek için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10b22-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="10b22-111">Kaynak aşağı açılan listesi varsayılan olarak mevcut kullanıcıya atanmış olan çalışanı gösterir.</span><span class="sxs-lookup"><span data-stu-id="10b22-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="10b22-112">Kullanıcı, bir temsilci olarak belirlendiyse, bu durum adları kullanıcının kendi adına bir zaman çizelgesi girebileceği şekilde listeler.</span><span class="sxs-lookup"><span data-stu-id="10b22-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="10b22-113">**Tarih** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="10b22-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="10b22-114">Bu seçenek işaretliyse, Sık Kullanılanlar olarak yapılandırılmış olan zaman çizelgesi ayarları kullanarak yeni zaman çizelgesi satırları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="10b22-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="10b22-115">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10b22-115">Click **OK**.</span></span>
5. <span data-ttu-id="10b22-116">**Yeni satır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10b22-116">Click **New line**.</span></span>
6. <span data-ttu-id="10b22-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="10b22-117">In the list, mark the selected row.</span></span> <span data-ttu-id="10b22-118">**Tüzel Kişilik** alanı mevcut tüzel kişiliği varsayılan olarak görüntüler.</span><span class="sxs-lookup"><span data-stu-id="10b22-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="10b22-119">**Proje** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10b22-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="10b22-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="10b22-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="10b22-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10b22-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="10b22-122">**Faaliyet numarası** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="10b22-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="10b22-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="10b22-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="10b22-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10b22-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="10b22-125">**Kategori** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10b22-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="10b22-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="10b22-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="10b22-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10b22-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="10b22-128">Her bir gün için çalışılan saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="10b22-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="10b22-129">Saatleri ondalık biçimde girin.</span><span class="sxs-lookup"><span data-stu-id="10b22-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="10b22-130">Örneğin, iki saat on beş dakika çalıştıysanız 2,25 değerini girin.</span><span class="sxs-lookup"><span data-stu-id="10b22-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="10b22-131">**Satır detaylarında** aşağıdaki güncelleştirme seçenekleri mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="10b22-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="10b22-132">Vergiler ve mali boyutlarla ilgili bilgileri **Genel** ve **Mali boyutlar** sekmesinde ekleyin.</span><span class="sxs-lookup"><span data-stu-id="10b22-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="10b22-133">**Yorum** sekmesinde zaman çizelgesi satırı hakkında açıklama ekleyin.</span><span class="sxs-lookup"><span data-stu-id="10b22-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="10b22-134">**Eylem bölmesi**'nde, bırakma iletişim kutusunu açmak için **İş akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="10b22-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="10b22-135">**Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10b22-135">Click **Submit**.</span></span>
22. <span data-ttu-id="10b22-136">**Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10b22-136">Click **Submit**.</span></span>

