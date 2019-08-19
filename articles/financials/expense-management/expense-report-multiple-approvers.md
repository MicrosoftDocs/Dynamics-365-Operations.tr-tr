---
title: Gider raporları ve birden çok onaylayan
description: Bu konu, birden fazla kişi tarafından onay gerektiren gider raporları hakkında bilgi sağlar.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d83a473e2e894856c12b36b4d005c6cb06b765a
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795136"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="6de63-103">Gider raporları ve birden çok onaylayan</span><span class="sxs-lookup"><span data-stu-id="6de63-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6de63-104">Kuruluşunuzun gider onay ilkelerine bağlı olarak, bir çalışan tarafından gönderilen bir gider raporunu birden fazla kişinin onaylaması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="6de63-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="6de63-105">Gider raporu onayı için iş akışı işlemi ayarlarken, bir veya daha fazla gider raporu onaylayanı için görevleri veya adımları içeren iş akışı öğeleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6de63-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="6de63-106">Örneğin, tüm gider raporlarının öncelikle raporu gönderen kişinin yöneticisi ve ardından bir Borç hesapları koordinatörü tarafından onaylanması gerektiğini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6de63-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="6de63-107">Birden fazla gider raporu onaylayanın gerekli olduğuna karar verirseniz, iş akışı öğelerini şu şekilde ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="6de63-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="6de63-108">Bir adım içeren bir onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6de63-108">Add one approval element that has one step.</span></span> <span data-ttu-id="6de63-109">Örneğin, adım bir gider raporunun bir kullanıcı grubuna atanmasını ve bunun kullanıcı grubu üyelerinin yüzde 50'si tarafından onaylanmasını gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="6de63-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="6de63-110">Birden fazla adım içeren bir onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6de63-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="6de63-111">Örneğin, onay öğesi aşağıdaki adımları içerebilir:</span><span class="sxs-lookup"><span data-stu-id="6de63-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="6de63-112">Gider raporunu gönderen çalışanın yöneticisi raporu onaylar.</span><span class="sxs-lookup"><span data-stu-id="6de63-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="6de63-113">Borç hesapları memuru girişleri ve gider raporu öğelerini doğrular.</span><span class="sxs-lookup"><span data-stu-id="6de63-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="6de63-114">Bütçe sahibi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="6de63-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="6de63-115">Her birinin tek bir adımı bulunan birden fazla onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6de63-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="6de63-116">Örneğin, aşağıdaki adımların her biri için ayrı onay bir öğesi ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="6de63-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="6de63-117">Çalışanın yöneticisi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="6de63-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="6de63-118">Bütçe sahibi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="6de63-118">The budget owner approves the expense report.</span></span>
