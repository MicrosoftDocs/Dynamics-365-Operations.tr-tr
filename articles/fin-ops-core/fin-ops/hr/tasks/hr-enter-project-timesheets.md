---
title: Proje zaman çizelgelerini girme
description: Bu yöntem, bir zaman çizelgesini, boş zaman çizelgesi formu kullanarak oluşturmanızı sağlar.
author: andreabichsel
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4a600137fc583aef8c85c920ca3cd2949a1a19d
ms.sourcegitcommit: 0cca2f82ae5c91c409e2abbf5867ff4e59ba71d6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2021
ms.locfileid: "5055951"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="02871-103">Proje zaman çizelgelerini girme</span><span class="sxs-lookup"><span data-stu-id="02871-103">Enter project timesheets</span></span>

<span data-ttu-id="02871-104">Bu yöntem, bir zaman çizelgesini, boş zaman çizelgesi formu kullanarak oluşturmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="02871-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="02871-105">Yeni Zaman Çizelgesi, önceki bir zaman çizelgesi bilgilerini veya **Sık Kullanılanlarım** sayfasındaki proje ve faaliyet atamalarını baz alabilir.</span><span class="sxs-lookup"><span data-stu-id="02871-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="02871-106">Varsayılan olarak, **Tüm zaman çizelgeleri** listesi sayfası, geçerli dönem için tüm zaman çizelgelerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="02871-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="02871-107">**Çizelgelerim** sayfasındaki **Göster** alanındaki aşağı açılan listeyi, çizelgeleri süre ya da proje zaman çizelgesi listesine göre filtrelemek, veya diğer çalışanlar adına oluşturulan zaman çizelgelerini görüntülemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02871-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="02871-108">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USSI'dir.</span><span class="sxs-lookup"><span data-stu-id="02871-108">The demo data company used to create this procedure is USSI.</span></span>  

1. <span data-ttu-id="02871-109">**Gezinti bölmesi**'nde **Modüller > Proje yönetimi muhasebe parametreleri > Zaman çizelgeleri > Benim zaman çizelgelerim**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="02871-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="02871-110">Yeni bir zaman çizelgesi girmek için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02871-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="02871-111">Kaynak aşağı açılan listesi varsayılan olarak mevcut kullanıcıya atanmış olan çalışanı gösterir.</span><span class="sxs-lookup"><span data-stu-id="02871-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="02871-112">Kullanıcı, bir temsilci olarak belirlendiyse, bu durum adları kullanıcının kendi adına bir zaman çizelgesi girebileceği şekilde listeler.</span><span class="sxs-lookup"><span data-stu-id="02871-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="02871-113">**Tarih** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="02871-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="02871-114">Bu seçenek işaretliyse, Sık Kullanılanlar olarak yapılandırılmış olan zaman çizelgesi ayarları kullanarak yeni zaman çizelgesi satırları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="02871-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="02871-115">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02871-115">Click **OK**.</span></span>
5. <span data-ttu-id="02871-116">**Yeni satır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02871-116">Click **New line**.</span></span>
6. <span data-ttu-id="02871-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="02871-117">In the list, mark the selected row.</span></span> <span data-ttu-id="02871-118">**Tüzel Kişilik** alanı mevcut tüzel kişiliği varsayılan olarak görüntüler.</span><span class="sxs-lookup"><span data-stu-id="02871-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="02871-119">**Proje** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02871-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="02871-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="02871-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="02871-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02871-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="02871-122">**Faaliyet numarası** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="02871-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="02871-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="02871-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="02871-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02871-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="02871-125">**Kategori** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02871-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="02871-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="02871-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="02871-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02871-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="02871-128">Her bir gün için çalışılan saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="02871-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="02871-129">Saatleri ondalık biçimde girin.</span><span class="sxs-lookup"><span data-stu-id="02871-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="02871-130">Örneğin, iki saat on beş dakika çalıştıysanız 2,25 değerini girin.</span><span class="sxs-lookup"><span data-stu-id="02871-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="02871-131">**Satır detaylarında** aşağıdaki güncelleştirme seçenekleri mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="02871-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="02871-132">Vergiler ve mali boyutlarla ilgili bilgileri **Genel** ve **Mali boyutlar** sekmesinde ekleyin.</span><span class="sxs-lookup"><span data-stu-id="02871-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="02871-133">**Yorum** sekmesinde zaman çizelgesi satırı hakkında açıklama ekleyin.</span><span class="sxs-lookup"><span data-stu-id="02871-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="02871-134">**Eylem bölmesi**'nde, bırakma iletişim kutusunu açmak için **İş akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="02871-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="02871-135">**Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02871-135">Click **Submit**.</span></span>
22. <span data-ttu-id="02871-136">**Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="02871-136">Click **Submit**.</span></span>

