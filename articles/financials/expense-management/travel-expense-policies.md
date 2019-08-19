---
title: Gider ilkelerini tanımla
description: Microsoft Dynamics 365 for Finance and Operations içinde çalışanlarınızın gider raporlarını ve seyahat taleplerini girerken veya gönderirken izlemeleri gereken gider ilkeleri tanımlayabilirsiniz.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26336710b277ce9594c8546f2214e152a3460204
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840901"
---
# <a name="expense-policies"></a><span data-ttu-id="bb9ce-103">Gider ilkeleri</span><span class="sxs-lookup"><span data-stu-id="bb9ce-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb9ce-104">Çalışanlarınızın gider raporlarını ve seyahat taleplerini girerken veya gönderirken izlemeleri gereken ilkeleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="bb9ce-105">Gider ilkelerinin uygulanması giderleri etkili bir şekilde yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="bb9ce-106">Örneğin, New York City için bir gecelik otel giderlerinin 250 ABD dolarını aşamayacağını belirten bir ilke ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="bb9ce-107">Bir çalışan oda ücretinin bu tutarı aştığı bir seyahat talebi veya gider raporu gönderirse, sistem çalışanı</span><span class="sxs-lookup"><span data-stu-id="bb9ce-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="bb9ce-108">gider için ilke tutarının aşıldığı konusunda bilgilendirir.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="bb9ce-109">İlkeyi tanımlarken çalışanın alacağı iletiyi</span><span class="sxs-lookup"><span data-stu-id="bb9ce-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="bb9ce-110">yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-110">define the policy.</span></span>      
        
<span data-ttu-id="bb9ce-111">Üç farklı ilke türü tanımlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="bb9ce-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="bb9ce-112">Uyarı – Çalışanın bir gider raporu veya seyahat talebi göndermesine izin verir ancak gider sonra raporlanmak üzere tüm</span><span class="sxs-lookup"><span data-stu-id="bb9ce-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="bb9ce-113">onaylayıcılar için işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-113">for later reporting.</span></span>        

- <span data-ttu-id="bb9ce-114">Hata – Çalışanın gider raporu veya seyahat talebini göndermeden önce ilke ile uyum sağlar hale getirmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="bb9ce-115">Mazeret – Çalışanın veya bir yöneticini, gider raporunu veya seyahat talebini girmeden önce ilke tutarını aşmasına dair bir mazeret girmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="bb9ce-116">İlke ipuçları</span><span class="sxs-lookup"><span data-stu-id="bb9ce-116">Policy tips</span></span>
<span data-ttu-id="bb9ce-117">Burada, gider yönetimi için yeni ilkeler oluşturmanıza yardımcı olabilecek birkaç öneri verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-117">Here are a few suggestions that can assist you whe creating new policies for expense management.</span></span> 
* <span data-ttu-id="bb9ce-118">İlkelerin geçerlilik tarihi vardır ve ilke giderin gerçekleştiği tarihten sonraki bir tarihle oluşturulduysa geçerli olmaz.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="bb9ce-119">Örneğin, en fazla $50 yemek gideri kullanmaya zorlamak için bugün yeni bir ilke oluşturuyorsanız, dün girilen tüm mevcut giderler bu ilkeye göre denetlenmez.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="bb9ce-120">Dökümü yapılabilecek bir gider kategorisi için ilke oluştururken, gider satırı türü için bir koşul eklemeyi düşünün.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="bb9ce-121">Makbuz gerektirme gibi bazı ilkeler, dökümü yapılan satırlar için anlamlı olmayabilir ve yalnızca başlık satırına veya dökümü oluşturulmamış bir satıra uygulanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="bb9ce-122">İlkeler ne zaman değerlendirilir</span><span class="sxs-lookup"><span data-stu-id="bb9ce-122">When to evaluate policies</span></span>

<span data-ttu-id="bb9ce-123">Gider yönetimi parametrelerinde, bir satır kaydedildiğinde veya gider raporu gönderildiğinde gider yönetim ilkelerini değerlendirmek için bir seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-123">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="bb9ce-124">Bir satır kaydedildiğinde değerlendirmeyi seçerseniz bu, kullanıcıların gider raporlarını bir kerede tamamlamak için yapmaları gerekenler hakkında daha önceden görünürlüğe sahip olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-124">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="bb9ce-125">Aksi takdirde, iş akışına gönderim sırasında doğrulamanın sonda gerçekleşmesi durumunda ilke değerlendirmesini erteleyebilir ve zamandan tasarruf edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9ce-125">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
