---
title: "Çalışanlara ödünç verilen öğeleri yönetme"
description: "Ödünç verilen maddeler, yöneticilerin şirketin çalışanlarına ödünç verdiği fiziksel öğeleri izlemede yardımcı kayıtlardır."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: 6c22e85360c3e6e40e0338960866b96d66a0ba50
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="cf1f8-103">Çalışanlara ödünç verilen öğeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="cf1f8-103">Manage items that are lent to workers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf1f8-104">Ödünç verilen maddeler, yöneticilerin şirketin çalışanlarına ödünç verdiği fiziksel öğeleri izlemede yardımcı kayıtlardır.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="cf1f8-105">Aşağıdaki noktalar şirket çalışanlarına ödünç verilebilecek öğeleri listeler:</span><span class="sxs-lookup"><span data-stu-id="cf1f8-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="cf1f8-106">Cep telefonları</span><span class="sxs-lookup"><span data-stu-id="cf1f8-106">Mobile telephones</span></span>
-   <span data-ttu-id="cf1f8-107">Otomobiller</span><span class="sxs-lookup"><span data-stu-id="cf1f8-107">Automobiles</span></span>
-   <span data-ttu-id="cf1f8-108">Bilgisayar ekipmanı</span><span class="sxs-lookup"><span data-stu-id="cf1f8-108">Computer equipment</span></span>

<span data-ttu-id="cf1f8-109">Her fiziksel öğeye karşılık gelen bir ödünç verilen madde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="cf1f8-110">Ödünç verilen her madde kaydı neyin ödünç verildiği, ödünç verme işleminden kimin sorumlu olduğu ve maddenin bir çalışana ödünç verilebileceği gün sayısı açıklanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="cf1f8-111">Aynı anda birden fazla ödünç verilen maddeler, örneğin anahtar, erişim kartı veya üniforma gibi maddeler için, oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="cf1f8-112">Bir maddeyi ödünç verirken, maddenin ödünç verildiği tarihi ve planlanan iade tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="cf1f8-113">Madde iade edildiğinde, asıl iade tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="cf1f8-114">Çalışanlar, kendilerine ödünç verilen maddelerin kaydını görüntülemek için Çalışan self servis çalışma alanını kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="cf1f8-115">Ek fiziksel öğeler alırlarsa, mevcut kayıtlarını düzenleyebilir veya yeni ödünç verilen maddeler girebilirler.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="cf1f8-116">İş akışı, yeni veya mevcut ödün verilen öğeleri onay işleminden yönlendirmek üzere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="cf1f8-117">Yöneticiler doğrudan raporları aracılığıyla ödünç öğeleri görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="cf1f8-118">Ayrıca çalışanları adına yeni bir ödünç verilen maddeler ekleme izni de verilebilirler.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="cf1f8-119"> Kayıp veya hatalı yerleştirilen ödünç verilen maddelere ait hesap</span><span class="sxs-lookup"><span data-stu-id="cf1f8-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="cf1f8-120">Bir madde hasar görürse veya yanlış yere yerleştirilirse, hayali bir iade kaydı girin.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="cf1f8-121">Sonra maddeyi silin veya özet kısmında tutun ve maddenin kullanılamaz olduğunu belirtmek için açıklamasını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="cf1f8-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="cf1f8-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cf1f8-122">Additional resources</span></span>
--------

[<span data-ttu-id="cf1f8-123">İnsan kaynakları</span><span class="sxs-lookup"><span data-stu-id="cf1f8-123">Human resources</span></span>](index.md)




