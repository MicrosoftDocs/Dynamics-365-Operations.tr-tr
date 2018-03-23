---
title: "Gider raporları ve birden çok onaylayan"
description: "Bu konu, birden fazla kişi tarafından onay gerektiren gider raporları hakkında bilgi sağlar."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 0f7592c580a21040c8b630885939ceaab3855c2c
ms.contentlocale: tr-tr
ms.lasthandoff: 03/13/2018

---

# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="fbe19-103">Gider raporları ve birden çok onaylayan</span><span class="sxs-lookup"><span data-stu-id="fbe19-103">Expense reports and multiple approvers</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fbe19-104">Kuruluşunuzun gider onay ilkelerine bağlı olarak, bir çalışan tarafından gönderilen bir gider raporunu birden fazla kişinin onaylaması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="fbe19-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="fbe19-105">Gider raporu onayı için iş akışı işlemi ayarlarken, bir veya daha fazla gider raporu onaylayanı için görevleri veya adımları içeren iş akışı öğeleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbe19-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="fbe19-106">Örneğin, tüm gider raporlarının öncelikle raporu gönderen kişinin yöneticisi ve ardından bir Borç hesapları koordinatörü tarafından onaylanması gerektiğini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbe19-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="fbe19-107">Birden fazla gider raporu onaylayanın gerekli olduğuna karar verirseniz, iş akışı öğelerini şu şekilde ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="fbe19-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="fbe19-108">Bir adım içeren bir onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fbe19-108">Add one approval element that has one step.</span></span> <span data-ttu-id="fbe19-109">Örneğin, adım bir gider raporunun bir kullanıcı grubuna atanmasını ve bunun kullanıcı grubu üyelerinin yüzde 50'si tarafından onaylanmasını gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="fbe19-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="fbe19-110">Birden fazla adım içeren bir onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fbe19-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="fbe19-111">Örneğin, onay öğesi aşağıdaki adımları içerebilir:</span><span class="sxs-lookup"><span data-stu-id="fbe19-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="fbe19-112">Gider raporunu gönderen çalışanın yöneticisi raporu onaylar.</span><span class="sxs-lookup"><span data-stu-id="fbe19-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="fbe19-113">Borç hesapları memuru girişleri ve gider raporu öğelerini doğrular.</span><span class="sxs-lookup"><span data-stu-id="fbe19-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="fbe19-114">Bütçe sahibi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="fbe19-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="fbe19-115">Her birinin tek bir adımı bulunan birden fazla onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fbe19-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="fbe19-116">Örneğin, aşağıdaki adımların her biri için ayrı onay bir öğesi ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="fbe19-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="fbe19-117">Çalışanın yöneticisi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="fbe19-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="fbe19-118">Bütçe sahibi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="fbe19-118">The budget owner approves the expense report.</span></span>

