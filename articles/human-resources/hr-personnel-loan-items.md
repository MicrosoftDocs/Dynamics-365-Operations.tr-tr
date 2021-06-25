---
title: Çalışanlara ödünç verilen öğeleri yönetme
description: Ödünç verilen maddeler, yöneticilerin şirketin çalışanlarına ödünç verdiği fiziksel öğeleri izlemede yardımcı kayıtlardır.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e4109762a2db3114ad66882092d6729dd9b08364
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190220"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="3f216-103">Çalışanlara ödünç verilen öğeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="3f216-103">Manage items that are lent to workers</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3f216-104">Ödünç verilen maddeler, yöneticilerin şirketin çalışanlarına ödünç verdiği fiziksel öğeleri izlemede yardımcı kayıtlardır.</span><span class="sxs-lookup"><span data-stu-id="3f216-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="3f216-105">Aşağıdaki noktalar şirket çalışanlarına ödünç verilebilecek öğeleri listeler:</span><span class="sxs-lookup"><span data-stu-id="3f216-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="3f216-106">Cep telefonları</span><span class="sxs-lookup"><span data-stu-id="3f216-106">Mobile telephones</span></span>
-   <span data-ttu-id="3f216-107">Otomobiller</span><span class="sxs-lookup"><span data-stu-id="3f216-107">Automobiles</span></span>
-   <span data-ttu-id="3f216-108">Bilgisayar ekipmanı</span><span class="sxs-lookup"><span data-stu-id="3f216-108">Computer equipment</span></span>

<span data-ttu-id="3f216-109">Her fiziksel öğeye karşılık gelen bir ödünç verilen madde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3f216-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="3f216-110">Ödünç verilen her madde kaydı neyin ödünç verildiği, ödünç verme işleminden kimin sorumlu olduğu ve maddenin bir çalışana ödünç verilebileceği gün sayısı açıklanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3f216-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="3f216-111">Aynı anda birden fazla ödünç verilen maddeler, örneğin anahtar, erişim kartı veya üniforma gibi maddeler için, oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f216-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="3f216-112">Bir maddeyi ödünç verirken, maddenin ödünç verildiği tarihi ve planlanan iade tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="3f216-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="3f216-113">Madde iade edildiğinde, asıl iade tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="3f216-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="3f216-114">Çalışanlar, kendilerine ödünç verilen maddelerin kaydını görüntülemek için Çalışan self servis çalışma alanını kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="3f216-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="3f216-115">Ek fiziksel öğeler alırlarsa, mevcut kayıtlarını düzenleyebilir veya yeni ödünç verilen maddeler girebilirler.</span><span class="sxs-lookup"><span data-stu-id="3f216-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="3f216-116">İş akışı, yeni veya mevcut ödün verilen öğeleri onay işleminden yönlendirmek üzere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="3f216-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="3f216-117">Yöneticiler doğrudan raporları aracılığıyla ödünç öğeleri görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="3f216-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="3f216-118">Ayrıca çalışanları adına yeni bir ödünç verilen maddeler ekleme izni de verilebilirler.</span><span class="sxs-lookup"><span data-stu-id="3f216-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

##  <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="3f216-119"> Kayıp veya hatalı yerleştirilen ödünç verilen maddelere ait hesap</span><span class="sxs-lookup"><span data-stu-id="3f216-119">Account for lost or misplaced loan items</span></span>

<span data-ttu-id="3f216-120">Bir madde hasar görürse veya yanlış yere yerleştirilirse, hayali bir iade kaydı girin.</span><span class="sxs-lookup"><span data-stu-id="3f216-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="3f216-121">Sonra maddeyi silin veya özet kısmında tutun ve maddenin kullanılamaz olduğunu belirtmek için açıklamasını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="3f216-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="3f216-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3f216-122">Additional resources</span></span>

[<span data-ttu-id="3f216-123">İnsan kaynakları</span><span class="sxs-lookup"><span data-stu-id="3f216-123">Human resources</span></span>](index.md)





[!INCLUDE[footer-include](../includes/footer-banner.md)]