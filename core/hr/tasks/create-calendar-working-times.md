--- 
title: "Bir takvim ve çalışma zamanları oluşturma"
description: "Takvimler, kapasiteyi ve işlem kaynaklarının çalışma zamanlarını açıklar."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d65fe0363e418f9c2e78bd78e802a4b0ea98599c
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-calendar-and-generate-working-times"></a><span data-ttu-id="f345b-103">Bir takvim ve çalışma zamanları oluşturma</span><span class="sxs-lookup"><span data-stu-id="f345b-103">Create a calendar and generate working times</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f345b-104">Takvimler, kapasiteyi ve işlem kaynaklarının çalışma zamanlarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="f345b-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="f345b-105">Bu yordam, bir çalışma saati şablonunu temel alan bir iş takvimi tanımlamanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="f345b-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="f345b-106">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f345b-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="f345b-107">Tüm çalışma alanları > Kaynak yaşam döngüsü yönetimi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f345b-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="f345b-108">Takvimler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f345b-108">Click Calendars.</span></span>
3. <span data-ttu-id="f345b-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f345b-109">Click New.</span></span>
4. <span data-ttu-id="f345b-110">Takvim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f345b-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="f345b-111">Bu, bir işlemler kaynağına veya kaynak grubuna takvim atarken referans olarak kullanılan takvimin kodudur.</span><span class="sxs-lookup"><span data-stu-id="f345b-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="f345b-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f345b-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="f345b-113">Saat alanında Standart iş gününde bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f345b-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="f345b-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f345b-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="f345b-115">Çalışma zamanları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f345b-115">Click Working times.</span></span>
9. <span data-ttu-id="f345b-116">Çalışma zamanları oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f345b-116">Click Compose working times.</span></span>
    * <span data-ttu-id="f345b-117">İş planlaması yapabilmek istediğiniz dönem içindeki her bir gün için çalışma saatleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f345b-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="f345b-118">Zaman geçtikçe, ek dönemler için çalışma zamanları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f345b-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="f345b-119">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="f345b-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="f345b-120">Bu, takvimin açılması gereken ilk gündür.</span><span class="sxs-lookup"><span data-stu-id="f345b-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="f345b-121">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="f345b-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="f345b-122">Bu, takvimin açılacağı son gündür.</span><span class="sxs-lookup"><span data-stu-id="f345b-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="f345b-123">Çalışma zamanı şablonu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f345b-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="f345b-124">Çalışma zamanı şablonu, haftanın her günü için çalışma saatlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f345b-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="f345b-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f345b-125">Click OK.</span></span>
14. <span data-ttu-id="f345b-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f345b-126">Close the page.</span></span>


