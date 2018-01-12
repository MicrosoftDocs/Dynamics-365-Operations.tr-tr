---
title: "Gider ilkelerini tanımla"
description: "Microsoft Dynamics 365 for Finance and Operations, Enterprise edition içerisinde gider raporları ve seyahat taleplerini girerken ve gönderirken çalışanlarınızın izlemesi gereken gider ilkelerini tanımlayabilirsiniz."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: e04fae56cf0ed988b267477ba1ed327e8e8f72c0
ms.contentlocale: tr-tr
ms.lasthandoff: 01/12/2018

---

# <a name="expense-policies"></a><span data-ttu-id="4e3cf-103">Gider ilkeleri</span><span class="sxs-lookup"><span data-stu-id="4e3cf-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4e3cf-104">Çalışanlarınızın gider raporlarını ve seyahat taleplerini girerken veya gönderirken izlemeleri gereken ilkeleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e3cf-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="4e3cf-105">Gider ilkelerinin uygulanması giderleri etkili bir şekilde yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="4e3cf-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="4e3cf-106">Örneğin, New York City için bir gecelik otel giderlerinin 250 ABD dolarını aşamayacağını belirten bir ilke ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e3cf-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="4e3cf-107">Çalışan oda ücreti bu tutarı aşan bir gider raporu veya seyahat talebi gönderirse, sistem çalışana giderle ilgili ilke tutarının aşılmış olduğunu bildirir.</span><span class="sxs-lookup"><span data-stu-id="4e3cf-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="4e3cf-108">İlkeyi tanımlarken çalışanın alacağı iletiyi yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e3cf-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="4e3cf-109">Üç farklı ilke türü tanımlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="4e3cf-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="4e3cf-110">Uyarı – Çalışanın bir gider raporu veya seyahat talebi göndermesine izin verir ancak gider sonra raporlanmak üzere tüm</span><span class="sxs-lookup"><span data-stu-id="4e3cf-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="4e3cf-111">onaylayıcılar için işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="4e3cf-111">for later reporting.</span></span> 
 - <span data-ttu-id="4e3cf-112">Hata – Çalışanın gider raporu veya seyahat talebini göndermeden önce ilke ile uyum sağlar hale getirmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4e3cf-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="4e3cf-113">Mazeret – Çalışanın veya bir yöneticini, gider raporunu veya seyahat talebini girmeden önce ilke tutarını aşmasına dair bir mazeret girmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4e3cf-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="4e3cf-114">Ayrıca, gider ilkelerinin yürürlükte olacağı bir tarih aralığı da ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e3cf-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="4e3cf-115">Örneğin, Danimarka ile New York City arasındaki uçuşların havayolu ücretleri tatil sezonunda pahalı olabilir.</span><span class="sxs-lookup"><span data-stu-id="4e3cf-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="4e3cf-116">New York City'ye uçuşların maliyetini 5000 Danimarka Kronuyla sınırlayan bir uçuş gideri kuralı tanımlayabilir ve bu kuralın 15 Mart ile 15 Eylül tarihleri arasında yürürlükte olacağını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e3cf-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

