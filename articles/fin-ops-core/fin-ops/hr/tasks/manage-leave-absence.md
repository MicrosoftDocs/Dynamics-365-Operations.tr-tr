---
title: Devamsızlıkları yönetme
description: Bu yordam çalışan izin kayıtlarının oluşturulmasıyla ilgili bilgi içerir.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 002700ae7f6474b48fbe09cb3aaa72e9516b8224
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143580"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="6737b-103">Devamsızlıkları yönetme</span><span class="sxs-lookup"><span data-stu-id="6737b-103">Manage leave of absence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6737b-104">Bu yordam çalışan izin kayıtlarının oluşturulmasıyla ilgili bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="6737b-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="6737b-105">Tıbbi, eğitim veya ebeveynlik etkinliklerini kapsayan nedenler için izin süresini izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6737b-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="6737b-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="6737b-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="6737b-107">İnsan kaynakları > Çalışanlar > Çalışanlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="6737b-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="6737b-108">Listeden bir çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="6737b-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="6737b-109">Çalışan adını seçerek seçili çalışanla ilgili ayrıntılı bilgileri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="6737b-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="6737b-110">İstihdam sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6737b-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="6737b-111">İzin öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6737b-111">Click Leave.</span></span>
6. <span data-ttu-id="6737b-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6737b-112">Click New.</span></span>
7. <span data-ttu-id="6737b-113">İzin türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6737b-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6737b-114">İzin türleri formunda bir izin türünü bir kazanç koduyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6737b-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="6737b-115">İzin türü bir kazanç koduyla ilişkilendirilirse, girdiğiniz izin dönemi süresince ilişkilendirilen kazanç koduyla bir kazanç satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6737b-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="6737b-116">Listeden izin türü seçin.</span><span class="sxs-lookup"><span data-stu-id="6737b-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="6737b-117">Örneğin: Benimseme</span><span class="sxs-lookup"><span data-stu-id="6737b-117">For example: Adoption</span></span>  
9. <span data-ttu-id="6737b-118">İznin başlayacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="6737b-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="6737b-119">Örnek: '2015-10-26'</span><span class="sxs-lookup"><span data-stu-id="6737b-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="6737b-120">Örneğin: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="6737b-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="6737b-121">İznin başlayacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="6737b-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="6737b-122">Örneğin: 2015-11-20</span><span class="sxs-lookup"><span data-stu-id="6737b-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="6737b-123">Not alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="6737b-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="6737b-124">Örneğin: Benimseme için izin</span><span class="sxs-lookup"><span data-stu-id="6737b-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="6737b-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6737b-125">Click Save.</span></span>

