---
title: "Gider iş akışı"
description: "Bu konu, iş akışı sistemini Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'da, Gider yönetimindeki gider raporları için bir gözden geçirme işlemini nasıl kullanabileceğinizi açıklar."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d60d2f462a1fd27d4655e68aab7f96fb28a34b77
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="expense-workflow"></a><span data-ttu-id="cf351-103">Gider iş akışı</span><span class="sxs-lookup"><span data-stu-id="cf351-103">Expense workflow</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cf351-104">İş akışı sistemini Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'da, Gider yönetimindeki gider raporları için bir gözden geçirme işlemi için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cf351-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="cf351-105">Gider raporlarını kimin onaylayacağını belirlemek için aşağıdaki ölçütleri kullanan bir iş akışı ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="cf351-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="cf351-106">Çalışan raporlama hiyerarşisi ve önceden belirlenmiş onaylama limitleri</span><span class="sxs-lookup"><span data-stu-id="cf351-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="cf351-107">Ara onaylayıcıları ve bir nihai onaylayıcıyı içeren çok düzeyli onay</span><span class="sxs-lookup"><span data-stu-id="cf351-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="cf351-108">Mali boyutlar ve proje sorumluluğu</span><span class="sxs-lookup"><span data-stu-id="cf351-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="cf351-109">Belirli kullanıcılar veya kullanıcı gruplarına atama</span><span class="sxs-lookup"><span data-stu-id="cf351-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="cf351-110">İş akışı onayları, seyahat talepleri, nakit avanslar ve katma değer vergisi (KDV) iadesi için onaylar oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="cf351-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="cf351-111">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="cf351-111">**Example**</span></span>

<span data-ttu-id="cf351-112">Aşağıda bir gider raporuna ilişkin gider yönetimi iş akışı örneği verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="cf351-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="cf351-113">Bir personel bir gider raporu oluşturur ve kaydeder.</span><span class="sxs-lookup"><span data-stu-id="cf351-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="cf351-114">Personel gider raporunu onay için gönderir.</span><span class="sxs-lookup"><span data-stu-id="cf351-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="cf351-115">Onaylayıcı, iş akışı ayarlandığında tanımlanmış kurallara dayanarak tespit edilir.</span><span class="sxs-lookup"><span data-stu-id="cf351-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="cf351-116">Onaylayıcı, bir gider raporunun onaylamaya hazır olduğunu belirten bir bildirim alır.</span><span class="sxs-lookup"><span data-stu-id="cf351-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="cf351-117">Onaylayıcı, gider raporunu gözden geçirir ve aşağıdaki koşulların sağlandığını doğrular:</span><span class="sxs-lookup"><span data-stu-id="cf351-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="cf351-118">Giderler, hiçbir gider ilkesini ihlal etmiyor.</span><span class="sxs-lookup"><span data-stu-id="cf351-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="cf351-119">Bir gider bir ilkeyi ihlal ediyorsa, onaylayıcı gider raporunun geçerli bir iş gerekçesi içerdiğini doğrular.</span><span class="sxs-lookup"><span data-stu-id="cf351-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="cf351-120">Elektronik girişler gider raporuna iliştirilir.</span><span class="sxs-lookup"><span data-stu-id="cf351-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="cf351-121">Onaylayıcı gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="cf351-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="cf351-122">Gider raporu, deftere nakledilmesi için Borç hesapları koordinatörüne atanır.</span><span class="sxs-lookup"><span data-stu-id="cf351-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="cf351-123">Aşağıdaki adımlardan biri, otomatik deftere nakilin yapılandırmış olup olmamasına bağlı olarak gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="cf351-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="cf351-124">Otomatik deftere nakil yapılandırılmışsa, gider raporu ödem için işleme alınır ve gider raporunun durumu güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="cf351-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="cf351-125">Otomatik raporlama yapılandırılmamışsa, Borç hesapları koordinatörü, tüm orijinal makbuzların gönderildiğini ve makbuzların, gider raporundaki giderlere karşılık geldiğini doğrular.</span><span class="sxs-lookup"><span data-stu-id="cf351-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="cf351-126">Gider raporuna girilen tüm vergi kodlarının da doğru olarak doğrulanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf351-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="cf351-127">Bu gereksinimler doğrulandıktan sonra gider raporu deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="cf351-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="cf351-128">Gider raporu deftere nakledildikten sonra, gider raporu için ödeme onaylanır ve personele ödeme yapılır.</span><span class="sxs-lookup"><span data-stu-id="cf351-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>

