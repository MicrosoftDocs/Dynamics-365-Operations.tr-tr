--- 
title: "Çalışanı bir değişken tazminat planına kaydetme"
description: "Tazminat ve Kazançlar yöneticisi, nakit ve nakit olmayan personel ikramiyelerini hesaplamak için personeli değişken ücret planlarına kaydedebilir."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMCompVarEnrollEmpl
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: 6ab2533293b5c8cb37953427893b75a98ddf3976
ms.contentlocale: tr-tr
ms.lasthandoff: 09/17/2018

---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="9acbe-103">Çalışanı bir değişken tazminat planına kaydetme</span><span class="sxs-lookup"><span data-stu-id="9acbe-103">Enroll an employee in a variable compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9acbe-104">Tazminat ve Kazançlar yöneticisi, nakit ve nakit olmayan personel ikramiyelerini hesaplamak için personeli değişken ücret planlarına kaydedebilir.</span><span class="sxs-lookup"><span data-stu-id="9acbe-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="9acbe-105">Bu prosedürde, bir değişken ücret planının oluşturulduğu ve planda Kaydı etkinleştirin alanı ayarının Evet yapıldığı, söz konusu değişken ücret planı için uygunluk kuralları oluşturulduğu varsayılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9acbe-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="9acbe-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="9acbe-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9acbe-107">Bu prosedüre başlamak için İnsan Kaynakları > Çalışanlar > Personel > Ücret > Değişken plan kaydı'na gidin</span><span class="sxs-lookup"><span data-stu-id="9acbe-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="9acbe-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9acbe-108">Click New.</span></span>
2. <span data-ttu-id="9acbe-109">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9acbe-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9acbe-110">Plan arama, yalnızca, Uygunluk kurallarına göre personelin uygun olduğu değişken ücret planlarını gösterecek biçimde filtre edilir.</span><span class="sxs-lookup"><span data-stu-id="9acbe-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="9acbe-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9acbe-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9acbe-112">Genel bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="9acbe-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="9acbe-113">Yürürlük tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9acbe-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="9acbe-114">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9acbe-114">Click Save.</span></span>
7. <span data-ttu-id="9acbe-115">Geçersiz Kılmalar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="9acbe-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="9acbe-116">İsteğe bağlı olarak, seçili değişken plan için belirtilen işe alma kuralı Yüzde olduğu zaman personelin işe alınma tarihini geçersiz kılmak üzere bir işe alma kuralı tarihi ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="9acbe-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="9acbe-117">Değişken plan bir temel yüzdesi planıysa, personel için ikramiye yüzdesi geçersiz kılınabilir.</span><span class="sxs-lookup"><span data-stu-id="9acbe-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="9acbe-118">Değişken ücret planı bir birim sayısı planıysa, personel için birim sayısı geçersiz kılınabilir.</span><span class="sxs-lookup"><span data-stu-id="9acbe-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="9acbe-119">Personele ikramiye olarak sabit bir tutar verilecekse, tutar burada ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="9acbe-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="9acbe-120">Kuruluş geçersiz kılmaları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="9acbe-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="9acbe-121">Personelin performansı, farklı departmanların performansı veya çalışanın pozisyonuna atanmış olandan farklı bir departmanın performansı göz önünde bulundurulacaksa, departman geçersiz kılınabilir.</span><span class="sxs-lookup"><span data-stu-id="9acbe-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="9acbe-122">Yüzde sütununun toplamı 100 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9acbe-122">The Percent column should total 100.</span></span>  


