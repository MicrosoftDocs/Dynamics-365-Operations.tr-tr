---
title: "Abonelik ücretlerindeki günleri azaltma"
description: "Varolan bir abonelik ücretinin gün sayısını azaltmak için, artık abonelik ücreti aralığının bir parçası olmaması gereken dönemi kaldırdığınız yeni bir işlem oluşturabilirsiniz."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c70e393c125eecef85e8711d1635250f5ff408d9
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---


# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="7e87f-103">Abonelik ücretlerindeki günleri azaltma</span><span class="sxs-lookup"><span data-stu-id="7e87f-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7e87f-104">Varolan bir abonelik ücretinin gün sayısını azaltmak için, artık abonelik ücreti aralığının bir parçası olmaması gereken dönemi kaldırdığınız yeni bir işlem oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e87f-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="7e87f-105">Bir abonelik ücretindeki günleri azaltma</span><span class="sxs-lookup"><span data-stu-id="7e87f-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="7e87f-106">**Servis yönetimi** \> **Ortak** \> **Servis abonelikleri** \> **Tüm servis abonelikleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7e87f-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="7e87f-107">Servis aboneliğini seçin ve Eylem Bölmesinde **Abonelik ücretleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7e87f-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="7e87f-108">**Abonelik türü** alanında **Azaltma günleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7e87f-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="7e87f-109">Abonelik ücreti döneminden kaldırılmasını istediğiniz abonelik ücreti tarih aralığını girmek için **Başlangıç tarihi** ve **Bitiş tarihi** alanını kullanın ve ardından **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7e87f-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="7e87f-110">Oluşturulan işlemi görüntülemek için, **Abonelik** formunda **Ücret hareketleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7e87f-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="7e87f-111">Örnek</span><span class="sxs-lookup"><span data-stu-id="7e87f-111">Example</span></span>

<span data-ttu-id="7e87f-112">Bir abonelik işlemi dönemi 1 Ocak ile 31 Ocak arasında ise ve dönemi 10 gün azaltmak istiyorsanız, azaltma döneminin 1 Ocak ile 10 Ocak arasında olduğu yeni bir işlem oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7e87f-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="7e87f-113">(Azaltma dönemi 5 Ocak ile 15 Ocak arası ya da başka bir on günlük dönem olabilir).</span><span class="sxs-lookup"><span data-stu-id="7e87f-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="7e87f-114">Ayrıca, azaltma dönemindeki **Başlangıç tarihi** 21 Ocak ise (31 eksi 10), **Bitiş tarihi**'ni 31 Ocak'tan sonraki herhangi bir tarihe ayarlayabilirsiniz; bu durumda 10 gün yine ücret hareketi döneminden kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="7e87f-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e87f-115">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="7e87f-115">See also</span></span>

[<span data-ttu-id="7e87f-116">Azaltma günleri örneği</span><span class="sxs-lookup"><span data-stu-id="7e87f-116">Reduction days example</span></span>](reduction-days-example.md)

  


