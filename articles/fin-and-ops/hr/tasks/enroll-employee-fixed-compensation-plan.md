---
title: Personeli sabit ücret planına kaydetme
description: Tazminat ve kazançlar yöneticisi, personelin ödeme oranlarını yönetmek amacıyla, personeli sabit ücret planlarına atayabilir.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0ba197ee47d2a2da2372b12291e5625ddc9ba1
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510510"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="4a4b8-103">Personeli sabit ücret planına kaydetme</span><span class="sxs-lookup"><span data-stu-id="4a4b8-103">Enroll an employee in a fixed compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a4b8-104">Tazminat ve kazançlar yöneticisi, personelin ödeme oranlarını yönetmek amacıyla, personeli sabit ücret planlarına atayabilir.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="4a4b8-105">Bu prosedürde, sabit bir plan oluşturulduğu, planın etkin olduğu ve plan için uygunluk kurallarının ayarlandığı varsayılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="4a4b8-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4a4b8-107">Prosedüre başlamak için İnsan Kaynakları > Çalışanlar > Personel > Ücret > Sabit plan'a gidin</span><span class="sxs-lookup"><span data-stu-id="4a4b8-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="4a4b8-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-108">Click New.</span></span>
2. <span data-ttu-id="4a4b8-109">Eylem alanında, personelin ücretindeki değişikliği açıklamak için, Kirala/Yeniden Kirala türünde bir Sabit ücret eylemi seçin.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="4a4b8-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4a4b8-111">Posizyon alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4a4b8-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4a4b8-113">Görüntülenen düzey, Pozisyondaki İşin Maaş Düzeyi'ndendir.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="4a4b8-114">Çalışana maaş atanabilmesi için önce İş üzerinde düzeyin ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="4a4b8-115">Plan alanında personel için sabit ücret planını seçin.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="4a4b8-116">Plan arama, yalnızca, Uygunluk kurallarına göre personelin uygun olduğu planları gösterecek biçimde filtre edilir.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="4a4b8-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4a4b8-118">Maaşın Yürürlük ve Bitiş tarihlerinin varsayılan değerleri, çalışanın pozisyon atamasının başlangıç ve bitiş tarihlerinden alınır.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="4a4b8-119">Bu tarihleri gerektiği gibi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="4a4b8-120">Sabit ücret planı bir adım planıysa, personel için doğru ödeme oranını içeren adım seçin.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="4a4b8-121">Sabit ücret planı bir kademeli plan veya bant planıysa, personel için doğru ödeme oranını girin.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="4a4b8-122">Ödeme oranı, planın toleransı ayarlarına ve iş maaş düzeyinin minimum maksimum referans noktalarına bakılarak doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="4a4b8-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a4b8-123">Click OK.</span></span>

