---
title: Toplu işe alma projesi oluşturma
description: Bu prosedürde, bir toplu işe alma projesini ayarlama sürecinde size yol gösterilecek.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject,  HRMMassHireLineCreate, HcmJobLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea0f4638a968d2aecf4e3bb27acbd19e6455a8b3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190638"
---
# <a name="create-a-mass-hire-project"></a><span data-ttu-id="937a3-103">Toplu işe alma projesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="937a3-103">Create a mass hire project</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="937a3-104">Bu prosedürde, bir toplu işe alma projesini ayarlama sürecinde size yol gösterilecek.</span><span class="sxs-lookup"><span data-stu-id="937a3-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="937a3-105">Bir işveren kolayca çok sayıda pozisyon oluşturmak ve birçok çalışanı bu pozisyonlarda işe almak için toplu işe alma projelerini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="937a3-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="937a3-106">Bu prosedüre başlatmak için İnsan kaynakları > İşe alma > Toplu işe alma projeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="937a3-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="937a3-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="937a3-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="937a3-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="937a3-108">Click New.</span></span>
2. <span data-ttu-id="937a3-109">Toplu işe alma projesi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="937a3-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="937a3-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="937a3-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="937a3-111">Proje başlangıcı alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="937a3-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="937a3-112">Proje bitişi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="937a3-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="937a3-113">Projeyi aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="937a3-113">Click Open project.</span></span>
7. <span data-ttu-id="937a3-114">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="937a3-114">Click Yes.</span></span>
8. <span data-ttu-id="937a3-115">Pozisyon oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="937a3-115">Click Create positions.</span></span>
9. <span data-ttu-id="937a3-116">Miktar alanına, oluşturmak istediğiniz pozisyon sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="937a3-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="937a3-117">Başlangıç tarihi, yeni çalışanlar için İşe alınma tarihi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="937a3-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="937a3-118">Bitiş tarihi, yeni çalışanlar için Ayrılma tarihi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="937a3-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="937a3-119">Yeni çalışanların Kadrolu mu, yoksa Sözleşmeli mi olacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="937a3-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="937a3-120">İş alanında, pozisyonları oluşturulacak işi seçmek için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="937a3-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="937a3-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="937a3-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="937a3-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="937a3-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="937a3-123">Varsayılan tam zamanlı eşdeğeri, seçilen işten alınır.</span><span class="sxs-lookup"><span data-stu-id="937a3-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="937a3-124">Gerekirse bunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="937a3-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="937a3-125">İsteğe bağlı olarak, yeni pozisyonlar için Departman seçin.</span><span class="sxs-lookup"><span data-stu-id="937a3-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="937a3-126">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="937a3-126">Click OK.</span></span>

