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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1483de5405895d60f0cb302ab622758b2b05d2ca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "362430"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="16057-103">Gider raporları ve birden çok onaylayan</span><span class="sxs-lookup"><span data-stu-id="16057-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16057-104">Kuruluşunuzun gider onay ilkelerine bağlı olarak, bir çalışan tarafından gönderilen bir gider raporunu birden fazla kişinin onaylaması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="16057-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="16057-105">Gider raporu onayı için iş akışı işlemi ayarlarken, bir veya daha fazla gider raporu onaylayanı için görevleri veya adımları içeren iş akışı öğeleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16057-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="16057-106">Örneğin, tüm gider raporlarının öncelikle raporu gönderen kişinin yöneticisi ve ardından bir Borç hesapları koordinatörü tarafından onaylanması gerektiğini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16057-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="16057-107">Birden fazla gider raporu onaylayanın gerekli olduğuna karar verirseniz, iş akışı öğelerini şu şekilde ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="16057-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="16057-108">Bir adım içeren bir onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="16057-108">Add one approval element that has one step.</span></span> <span data-ttu-id="16057-109">Örneğin, adım bir gider raporunun bir kullanıcı grubuna atanmasını ve bunun kullanıcı grubu üyelerinin yüzde 50'si tarafından onaylanmasını gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="16057-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="16057-110">Birden fazla adım içeren bir onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="16057-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="16057-111">Örneğin, onay öğesi aşağıdaki adımları içerebilir:</span><span class="sxs-lookup"><span data-stu-id="16057-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="16057-112">Gider raporunu gönderen çalışanın yöneticisi raporu onaylar.</span><span class="sxs-lookup"><span data-stu-id="16057-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="16057-113">Borç hesapları memuru girişleri ve gider raporu öğelerini doğrular.</span><span class="sxs-lookup"><span data-stu-id="16057-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="16057-114">Bütçe sahibi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="16057-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="16057-115">Her birinin tek bir adımı bulunan birden fazla onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="16057-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="16057-116">Örneğin, aşağıdaki adımların her biri için ayrı onay bir öğesi ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="16057-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="16057-117">Çalışanın yöneticisi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="16057-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="16057-118">Bütçe sahibi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="16057-118">The budget owner approves the expense report.</span></span>
