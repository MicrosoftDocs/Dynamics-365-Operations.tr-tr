---
title: Takvimler ve çalışma zamanları oluşturma
description: Takvimler, kapasiteyi ve işlem kaynaklarının çalışma zamanlarını açıklar. Bu konuda bir çalışma saati şablonunu temel alan bir iş takvimi tanımlama işlemi açıklanmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38c0482c62e86e3e12e4bdd67f6d8f090ddfbfeb
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010841"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="d5bcf-104">Takvimler ve çalışma zamanları oluşturma</span><span class="sxs-lookup"><span data-stu-id="d5bcf-104">Create calendars and generate working times</span></span>



<span data-ttu-id="d5bcf-105">Takvimler, kapasiteyi ve işlem kaynaklarının çalışma zamanlarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="d5bcf-106">Bu konuda bir çalışma saati şablonunu temel alan bir iş takvimi tanımlama işlemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="d5bcf-107">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="d5bcf-108">Giriş sayfasında, **Kaynak yaşam döngüsü yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="d5bcf-109">**Takvimler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="d5bcf-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-110">Select **New**.</span></span>
4. <span data-ttu-id="d5bcf-111">**Takvim** alanında takviminizi sınıflandırın.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="d5bcf-112">Bu, bir işlemler kaynağına veya kaynak grubuna takvim atarken referans olarak kullanılan takvimin kodudur.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="d5bcf-113">**Ad** alanında, takviminizi adlandırın.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="d5bcf-114">**Saat cinsinden standart çalışma günü** alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="d5bcf-115">Satırın seçili olduğundan emin olun. Ardından Eylem Bölmesi'nden **Çalışma zamanları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="d5bcf-116">**Çalışma zamanları oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-116">Select **Compose working times**.</span></span> <span data-ttu-id="d5bcf-117">İş planlaması yapabilmek istediğiniz dönem içindeki her bir gün için çalışma saatleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="d5bcf-118">Zaman geçtikçe, ek dönemler için çalışma zamanları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="d5bcf-119">**Başlangıç tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="d5bcf-120">Bu, takvimin açılması gereken ilk gündür.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="d5bcf-121">**Bitiş tarihi alanına** bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="d5bcf-122">Bu, takvimin açılacağı son gündür.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="d5bcf-123">**Çalışma zamanı şablonu** alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="d5bcf-124">Çalışma zamanı şablonu, haftanın her günü için çalışma saatlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="d5bcf-125">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-125">Select **OK**.</span></span>
13. <span data-ttu-id="d5bcf-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d5bcf-126">Close the page.</span></span>

