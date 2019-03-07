---
title: Gider ilkelerini tanımla
description: Microsoft Dynamics 365 for Finance and Operations içinde çalışanlarınızın gider raporlarını ve seyahat taleplerini girerken veya gönderirken izlemeleri gereken gider ilkeleri tanımlayabilirsiniz.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04eaff110fea021ddee32be650be540894eb703b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "342443"
---
# <a name="expense-policies"></a><span data-ttu-id="41836-103">Gider ilkeleri</span><span class="sxs-lookup"><span data-stu-id="41836-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41836-104">Çalışanlarınızın gider raporlarını ve seyahat taleplerini girerken veya gönderirken izlemeleri gereken ilkeleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41836-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="41836-105">Gider ilkelerinin uygulanması giderleri etkili bir şekilde yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="41836-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="41836-106">Örneğin, New York City için bir gecelik otel giderlerinin 250 ABD dolarını aşamayacağını belirten bir ilke ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41836-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="41836-107">Bir çalışan oda ücretinin bu tutarı aştığı bir seyahat talebi veya gider raporu gönderirse, sistem çalışanı</span><span class="sxs-lookup"><span data-stu-id="41836-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="41836-108">gider için ilke tutarının aşıldığı konusunda bilgilendirir.</span><span class="sxs-lookup"><span data-stu-id="41836-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="41836-109">İlkeyi tanımlarken çalışanın alacağı iletiyi</span><span class="sxs-lookup"><span data-stu-id="41836-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="41836-110">yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41836-110">define the policy.</span></span>      
        
<span data-ttu-id="41836-111">Üç farklı ilke türü tanımlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="41836-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="41836-112">Uyarı – Çalışanın bir gider raporu veya seyahat talebi göndermesine izin verir ancak gider sonra raporlanmak üzere tüm</span><span class="sxs-lookup"><span data-stu-id="41836-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="41836-113">onaylayıcılar için işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="41836-113">for later reporting.</span></span>        

- <span data-ttu-id="41836-114">Hata – Çalışanın gider raporu veya seyahat talebini göndermeden önce ilke ile uyum sağlar hale getirmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="41836-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
  - <span data-ttu-id="41836-115">Mazeret – Çalışanın veya bir yöneticini, gider raporunu veya seyahat talebini girmeden önce ilke tutarını aşmasına dair bir mazeret girmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="41836-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
  <span data-ttu-id="41836-116">Ayrıca, gider ilkelerinin yürürlükte olacağı bir tarih aralığı da ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41836-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="41836-117">Örneğin Danimarka ile New York City arasındaki</span><span class="sxs-lookup"><span data-stu-id="41836-117">For example, airline fares for flights between Denmark</span></span>      
  <span data-ttu-id="41836-118">uçuşlar için bilet ücreti tatil dönemlerinde pahalı olabilir.</span><span class="sxs-lookup"><span data-stu-id="41836-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="41836-119">New York City'ye yapılacak uçuşlar için maliyeti</span><span class="sxs-lookup"><span data-stu-id="41836-119">You can define a flight expense rule that restricts the</span></span>      
  <span data-ttu-id="41836-120">5000 DKK ile sınırlayacak bir gider kuralı oluşturabilir ve bu kuralın 15 Mart ile</span><span class="sxs-lookup"><span data-stu-id="41836-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
  <span data-ttu-id="41836-121">15 Eylül arasında geçerli olacağını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41836-121">September 15.</span></span>
