---
title: Müşteri alacak grupları
description: Bu konu, müşteri kredi gruplarıyla ilgili bilgiler vermektedir.
author: mikefalkner
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3cdf4f7e72a55292c64b7a9191974242aab85a90
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835328"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="b8985-103">Müşteri alacak grupları</span><span class="sxs-lookup"><span data-stu-id="b8985-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8985-104">Paylaşılan kredi limitine sahip olan müşteri grupları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b8985-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="b8985-105">Müşteri fatura hesabında tanımlanan bireysel kredi limiti de dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="b8985-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="b8985-106">Bir müşteri kredi grubunun üyeleri farklı tüzel kişiliklerden seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="b8985-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="b8985-107">Müşteri kredi grubunda müşteriler listesine bir müşteri eklediğinizde, her müşterinin kredi limiti bitiş tarihi, gruba atanan bitiş tarihi olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="b8985-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="b8985-108">Müşteri kredi gruplarını **Müşteri kredi grupları** sayfasında (**Kredi yönetimi \> Müşteri kredi grupları \> Müşteri kredi grupları**) oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b8985-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="b8985-109">**Grup numarası** ve **Açıklama** alanlarına grup için bir tanımlayıcı ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="b8985-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="b8985-110">**Kredi limiti** ve **Para birimi** alanlarına, sistem grup üyesinin kredi limitini kontrol ederken kullanılacak kredi limitini ve para birimini girin.</span><span class="sxs-lookup"><span data-stu-id="b8985-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="b8985-111">**Kredi limiti bitiş tarihi** alanına, kredi limitinin bitiş tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="b8985-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="b8985-112">Müşteri kredi gruplarının bitiş tarihleri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b8985-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="b8985-113">Bir müşteri kredi grubunu ayarlamayı bitirdikten sonra, tüzel kişiliklerini ve müşteri hesabı kodlarını belirterek müşterileri gruba ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b8985-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="b8985-114">Müşteri kredi grubuna yeni müşteri eklediğiniz zaman, sistem tüm tüzel kişiliklerde aynı müşteri hesabını arar ve bunu müşteri kredi grubuna eklemenizi ister.</span><span class="sxs-lookup"><span data-stu-id="b8985-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="b8985-115">Müşteri kredi grubundaki tüm fatura müşterilerinin yaşlandırma bakiyesi ayrıntılarını görüntülemek için **Yaşlandırılmış bakiyeler** menüsünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="b8985-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="b8985-116">**Yaşlandırma bakiyesi** sayfası, fatura müşterisi hesaplarına ait eski bakiyelerin özetini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8985-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]