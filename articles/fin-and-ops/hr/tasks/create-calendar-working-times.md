--- 
title: "Takvim yaratma ve çalışma zamanları oluşturma"
description: "Takvimler, kapasiteyi ve işlem kaynaklarının çalışma zamanlarını açıklar."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 8a556367857890acdb926ed29518cf2f2f2b92ea
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="create-calendar-and-generate-working-times"></a><span data-ttu-id="0d2da-103">Takvim yaratma ve çalışma zamanları oluşturma</span><span class="sxs-lookup"><span data-stu-id="0d2da-103">Create calendar and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d2da-104">Takvimler, kapasiteyi ve işlem kaynaklarının çalışma zamanlarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="0d2da-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="0d2da-105">Bu yordam, bir çalışma saati şablonunu temel alan bir iş takvimi tanımlamanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0d2da-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="0d2da-106">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d2da-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="0d2da-107">Tüm çalışma alanları > Kaynak yaşam döngüsü yönetimi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="0d2da-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="0d2da-108">Takvimler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0d2da-108">Click Calendars.</span></span>
3. <span data-ttu-id="0d2da-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d2da-109">Click New.</span></span>
4. <span data-ttu-id="0d2da-110">Takvim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="0d2da-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="0d2da-111">Bu, bir işlemler kaynağına veya kaynak grubuna takvim atarken referans olarak kullanılan takvimin kodudur.</span><span class="sxs-lookup"><span data-stu-id="0d2da-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="0d2da-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="0d2da-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="0d2da-113">Saat alanında Standart iş gününde bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0d2da-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="0d2da-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="0d2da-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="0d2da-115">Çalışma zamanları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0d2da-115">Click Working times.</span></span>
9. <span data-ttu-id="0d2da-116">Çalışma zamanları oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0d2da-116">Click Compose working times.</span></span>
    * <span data-ttu-id="0d2da-117">İş planlaması yapabilmek istediğiniz dönem içindeki her bir gün için çalışma saatleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0d2da-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="0d2da-118">Zaman geçtikçe, ek dönemler için çalışma zamanları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d2da-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="0d2da-119">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="0d2da-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="0d2da-120">Bu, takvimin açılması gereken ilk gündür.</span><span class="sxs-lookup"><span data-stu-id="0d2da-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="0d2da-121">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="0d2da-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="0d2da-122">Bu, takvimin açılacağı son gündür.</span><span class="sxs-lookup"><span data-stu-id="0d2da-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="0d2da-123">Çalışma zamanı şablonu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0d2da-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="0d2da-124">Çalışma zamanı şablonu, haftanın her günü için çalışma saatlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="0d2da-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="0d2da-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d2da-125">Click OK.</span></span>
14. <span data-ttu-id="0d2da-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0d2da-126">Close the page.</span></span>


