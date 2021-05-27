---
title: Sistem yöneticileri, yetkilendirilmedikleri için sipariş tutma bilgilerini temizleyemiyor
description: Sistem yöneticileri, yetkilendirilmedikleri için sipariş tutma bilgilerini temizleyemiyor.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027000"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="67df6-103">Sistem yöneticileri, yetkilendirilmedikleri için sipariş tutma bilgilerini temizleyemiyor</span><span class="sxs-lookup"><span data-stu-id="67df6-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="67df6-104">KB numarası: 4614642</span><span class="sxs-lookup"><span data-stu-id="67df6-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="67df6-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="67df6-105">Symptoms</span></span>

<span data-ttu-id="67df6-106">Sistem yöneticileri sipariş tutma kodunda atanan belirli bir role sahip olmadıkça satış siparişi tutmalarını temizleyemez.</span><span class="sxs-lookup"><span data-stu-id="67df6-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="67df6-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="67df6-107">Resolution</span></span>

<span data-ttu-id="67df6-108">Satış siparişi tutmalarını temizleme gibi bazı işlemlere erişim, iş ilkesinin kurulumu tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="67df6-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="67df6-109">Sistem yöneticilerinin bu tür işlemleri gerçekleştirmesine genelde izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="67df6-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="67df6-110">Daha çok, belirli bir görevi gerçekleştirmek için erişim iş ilkelerine göre yönetilir ve bu görevi gerçekleştirmek için yalnızca bir kuruluştaki belirli kişiler onaylanır.</span><span class="sxs-lookup"><span data-stu-id="67df6-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="67df6-111">Örnek olarak, iş akışı onayları ve iş akışı yapılandırmasının sonucu olan belirli görevler sonucu olan iş akışı onayları gösterilebilir.</span><span class="sxs-lookup"><span data-stu-id="67df6-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="67df6-112">Sipariş tutmalarla ilişkilendirilmiş bir iş akışı olmasa da, ilke benzerdir.</span><span class="sxs-lookup"><span data-stu-id="67df6-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="67df6-113">İlgili bir rol, kuruluştaki sipariş tutmaları temizleme yetkisine sahip belirli kişi gruplarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67df6-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="67df6-114">Bu yetki, tanımlanmış işletme ilkesini ihlal ettiğinden tüm yöneticilere verilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="67df6-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>
