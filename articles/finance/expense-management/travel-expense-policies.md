---
title: Gider ilkelerini tanımla
description: Microsoft Dynamics 365 Finance'te çalışanlarınızın gider raporlarını ve seyahat taleplerini girerken veya gönderirken izlemeleri gereken gider ilkeleri tanımlayabilirsiniz.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
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
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389727"
---
# <a name="define-expense-policies"></a><span data-ttu-id="4fa97-103">Gider ilkelerini tanımla</span><span class="sxs-lookup"><span data-stu-id="4fa97-103">Define expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fa97-104">Çalışanlarınızın gider raporlarını ve seyahat taleplerini girerken veya gönderirken izlemeleri gereken ilkeleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4fa97-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="4fa97-105">Gider ilkelerinin uygulanması giderleri etkili bir şekilde yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="4fa97-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="4fa97-106">Örneğin, New York City için bir gecelik otel giderlerinin 250 ABD dolarını aşamayacağını belirten bir ilke ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4fa97-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="4fa97-107">Bir çalışan oda ücretinin bu tutarı aştığı bir seyahat talebi veya gider raporu gönderirse, sistem çalışanı</span><span class="sxs-lookup"><span data-stu-id="4fa97-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="4fa97-108">gider için ilke tutarının aşıldığı konusunda bilgilendirir.</span><span class="sxs-lookup"><span data-stu-id="4fa97-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="4fa97-109">İlkeyi tanımlarken çalışanın alacağı iletiyi</span><span class="sxs-lookup"><span data-stu-id="4fa97-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="4fa97-110">yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4fa97-110">define the policy.</span></span>      
        
<span data-ttu-id="4fa97-111">Üç farklı ilke türü tanımlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="4fa97-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="4fa97-112">Uyarı – Çalışanın bir gider raporu veya seyahat talebi göndermesine izin verir ancak gider sonra raporlanmak üzere tüm</span><span class="sxs-lookup"><span data-stu-id="4fa97-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="4fa97-113">onaylayıcılar için işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="4fa97-113">for later reporting.</span></span>        

- <span data-ttu-id="4fa97-114">Hata – Çalışanın gider raporu veya seyahat talebini göndermeden önce ilke ile uyum sağlar hale getirmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4fa97-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="4fa97-115">Mazeret – Çalışanın veya bir yöneticini, gider raporunu veya seyahat talebini girmeden önce ilke tutarını aşmasına dair bir mazeret girmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4fa97-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="4fa97-116">İlke ipuçları</span><span class="sxs-lookup"><span data-stu-id="4fa97-116">Policy tips</span></span>
<span data-ttu-id="4fa97-117">Burada, gider yönetimi için yeni ilkeler oluşturmanıza yardımcı olabilecek birkaç öneri verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4fa97-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="4fa97-118">İlkelerin geçerlilik tarihi vardır ve ilke giderin gerçekleştiği tarihten sonraki bir tarihle oluşturulduysa geçerli olmaz.</span><span class="sxs-lookup"><span data-stu-id="4fa97-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="4fa97-119">Örneğin, en fazla $50 yemek gideri kullanmaya zorlamak için bugün yeni bir ilke oluşturuyorsanız, dün girilen tüm mevcut giderler bu ilkeye göre denetlenmez.</span><span class="sxs-lookup"><span data-stu-id="4fa97-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="4fa97-120">Dökümü yapılabilecek bir gider kategorisi için ilke oluştururken, gider satırı türü için bir koşul eklemeyi düşünün.</span><span class="sxs-lookup"><span data-stu-id="4fa97-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="4fa97-121">Makbuz gerektirme gibi bazı ilkeler, dökümü yapılan satırlar için anlamlı olmayabilir ve yalnızca başlık satırına veya dökümü oluşturulmamış bir satıra uygulanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4fa97-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="4fa97-122">Gider yönetimi ilkeleri varsayılan olarak kaynak varlığa göre değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="4fa97-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="4fa97-123">Şirketlerarası senaryolarda, ilkeyi bunun yerine hedef varlığa (borç alan varlık) göre değerlendirilecek şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4fa97-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="4fa97-124">İlkeleri hedef varlığa göre çalıştırmak için **Özellik yönetimi** çalışma alanındaki "Gider ilkesini borç alan tüzel varlığa göre değerlendir" özelliğini açın.</span><span class="sxs-lookup"><span data-stu-id="4fa97-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="4fa97-125">İlkeler ne zaman değerlendirilir</span><span class="sxs-lookup"><span data-stu-id="4fa97-125">When to evaluate policies</span></span>

<span data-ttu-id="4fa97-126">Gider yönetimi parametrelerinde, bir satır kaydedildiğinde veya gider raporu gönderildiğinde gider yönetim ilkelerini değerlendirmek için bir seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="4fa97-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="4fa97-127">Bir satır kaydedildiğinde değerlendirmeyi seçerseniz bu, kullanıcıların gider raporlarını bir kerede tamamlamak için yapmaları gerekenler hakkında daha önceden görünürlüğe sahip olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="4fa97-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="4fa97-128">Aksi takdirde, iş akışına gönderim sırasında doğrulamanın sonda gerçekleşmesi durumunda ilke değerlendirmesini erteleyebilir ve zamandan tasarruf edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4fa97-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
