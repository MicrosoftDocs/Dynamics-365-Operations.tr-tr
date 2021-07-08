---
title: İzin satın alma ve satma
description: Dynamics 365 Human Resources'ta, şirketiniz tarafından ayarlanan izin satın alma ve satma ilkelerine göre izin satın alma ve satma istekleri gönderebilirsiniz.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271508"
---
# <a name="buy-and-sell-leave"></a><span data-ttu-id="9de75-103">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="9de75-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9de75-104">Dynamics 365 Human Resources'ta, şirketiniz tarafından ayarlanan izin satın alma ve satma ilkelerine göre izin satın alma ve satma istekleri gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9de75-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="9de75-105">İzin satın alma talebi</span><span class="sxs-lookup"><span data-stu-id="9de75-105">Request to buy leave</span></span>

1. <span data-ttu-id="9de75-106">**Çalışan Self servis** çalışma alanında, **izin satın alma talebi** döşemesinin dışında **izin isteyi** seçin.</span><span class="sxs-lookup"><span data-stu-id="9de75-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="9de75-107">**İzin türü** ekleyin ve satın almak istediğiniz bırakma tutarı için bir **tutar** girin.</span><span class="sxs-lookup"><span data-stu-id="9de75-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="9de75-108">İsteğinizi göndermeye hazır olduğunuzda **Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9de75-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="9de75-109">Bakiyeleriniz otomatik olarak güncelleştirilir veya güncelleştirmeden önce onay işleminden geçer.</span><span class="sxs-lookup"><span data-stu-id="9de75-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="9de75-110">Bu, satın alma ilkesinin nasıl yapılandırıldığına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9de75-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="9de75-111">İzin satma isteği</span><span class="sxs-lookup"><span data-stu-id="9de75-111">Request to sell leave</span></span>

1. <span data-ttu-id="9de75-112">**Personel self servisi** çalışma alanında **Kalan İzinler** kutucuğunda **İzin satma isteği**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="9de75-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="9de75-113">**İzin türü** ekleyin ve satmak istediğiniz izin tutarı için bir **Tutar** girin.</span><span class="sxs-lookup"><span data-stu-id="9de75-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="9de75-114">İsteğinizi göndermeye hazır olduğunuzda **Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9de75-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="9de75-115">Bakiyeleriniz otomatik olarak güncelleştirilir veya güncelleştirmeden önce onay işleminden geçer.</span><span class="sxs-lookup"><span data-stu-id="9de75-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="9de75-116">Bu, satın alma ilkesinin nasıl yapılandırıldığına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9de75-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="9de75-117">Sorun Giderme</span><span class="sxs-lookup"><span data-stu-id="9de75-117">Troubleshooting</span></span> 

<span data-ttu-id="9de75-118">Bir izin satın alma veya satma talebi iş akışı başarısız olursa, **EssLeaveBuySellRequestApprover** ayrıcalığına sahip kullanıcılar, tüm izin satınalma ve satma taleplerini gözden geçirebilir.</span><span class="sxs-lookup"><span data-stu-id="9de75-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="9de75-119">Bunu yapmak için, **İzin ve devamsızlık > Bağlantı > İzin satın alma ve satma talepleri > İleti günlüğü**'ne (solda üst tarafta) gidin.</span><span class="sxs-lookup"><span data-stu-id="9de75-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="9de75-120">**İleti günlüğü** kullanıcılara hareketlerin nasıl işlendiğini ve ilişkili iş akışı geçmişini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9de75-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="9de75-121">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="9de75-121">See also</span></span>

[<span data-ttu-id="9de75-122">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="9de75-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="9de75-123">İzin satın alma ve satma ilkelerini yönetme</span><span class="sxs-lookup"><span data-stu-id="9de75-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
