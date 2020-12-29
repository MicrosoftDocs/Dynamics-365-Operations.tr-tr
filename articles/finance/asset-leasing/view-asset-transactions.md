---
title: Yükümlülük, varlık ve gider hareketlerini görüntüleme
description: Bu konu, kiralanan varlıkla ilgili hareketlerin nasıl görüntüleneceğini açıklamaktadır. Bu hareketler, kira yükümlülüğü hareketlerini ve deftere nakledilen icra gideri hareketlerini kapsar.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7008891d194dc990d13a9f56db155c6990aae0c0
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4449027"
---
# <a name="view-liability-asset-and-expense-transactions"></a><span data-ttu-id="91f75-104">Yükümlülük, varlık ve gider hareketlerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="91f75-104">View liability, asset, and expense transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91f75-105">Bu konu, kiralanan varlıkla ilgili hareketlerin nasıl görüntüleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="91f75-105">This topic explains how to view transactions for a leased asset.</span></span> <span data-ttu-id="91f75-106">Bu hareketler, kira yükümlülüğü hareketlerini ve deftere nakledilen icra gideri hareketlerini kapsar.</span><span class="sxs-lookup"><span data-stu-id="91f75-106">These transactions include lease liability transactions and executory expense transactions that have been posted.</span></span> <span data-ttu-id="91f75-107">Yükümlülük ve kullanım hakkı (ROU) varlığının defter değerleri birçok raporda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="91f75-107">The carrying values of the liability and right-of-use (ROU) asset are used on several reports.</span></span> <span data-ttu-id="91f75-108">Bunlar düzeltme değerlerini hesaplamada da kullanılırlar.</span><span class="sxs-lookup"><span data-stu-id="91f75-108">They are also used to calculate adjustment values.</span></span>

## <a name="liability-transactions"></a><span data-ttu-id="91f75-109">Pasif hareketleri</span><span class="sxs-lookup"><span data-stu-id="91f75-109">Liability transactions</span></span>

<span data-ttu-id="91f75-110">Kira yükümlülük hareketlerini görüntülemek için **Kiralama özeti** sayfasında bir kiralama seçin ve kiralama kaydına eklenmiş defterleri açmak için **Defterler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="91f75-110">To view the lease liability transactions, select a lease on the **Lease summary** page, and then select **Books** to open the books that are attached to the lease record.</span></span> <span data-ttu-id="91f75-111">İlk kabul, fatura veya faiz günlüğü deftere nakledildikten sonra **Yükümlülük hareketleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="91f75-111">After an initial recognition, an invoice, or an interest journal has been posted, select **Liability transactions**.</span></span>

<span data-ttu-id="91f75-112">**Yükümlülük hareketleri** sayfası , kiralama yükümlülüğünü artıran ve azaltan hareketleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="91f75-112">The **Liability transactions** page shows the transactions that either increase or decrease the lease liability.</span></span> <span data-ttu-id="91f75-113">Bu sayfadaki negatif tutarlar standart uygulamadaki alacak hareketlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="91f75-113">Negative amounts on this page represent credit transactions in the standard application.</span></span> <span data-ttu-id="91f75-114">Tüm faiz tahakkukları negatif değerler olarak gösterilir ve toplam kiralama yükümlülüğünü artırır.</span><span class="sxs-lookup"><span data-stu-id="91f75-114">Any interest accruals are shown as negative values and increase the total lease liability.</span></span> <span data-ttu-id="91f75-115">Tüm kiralama düzeltmeleri, kiralama defterinin yapısına ve etkisine bağlı olarak pozitif veya negatif değer olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="91f75-115">Any lease adjustments are shown as positive or negative values, depending on the nature and impact of the lease book.</span></span> <span data-ttu-id="91f75-116">Seçili kiralama için kiralama yükümlülüğünün net toplam bakiyesi sayfanın sol alt kısmında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="91f75-116">The current net total balance of the lease liability for the selected lease is shown at the bottom left of the page.</span></span>

## <a name="asset-transactions"></a><span data-ttu-id="91f75-117">Kıymet hareketleri</span><span class="sxs-lookup"><span data-stu-id="91f75-117">Asset transactions</span></span>

<span data-ttu-id="91f75-118">Kiralama varlığı hareketlerini görüntülemek için **Kiralama özeti** sayfasında bir kiralama seçin ve kiralama kaydına eklenmiş kiralama defterlerini açmak için **Defterler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="91f75-118">To view the lease asset transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="91f75-119">Ardından **Varlık hareketleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="91f75-119">Then select **Asset transactions**.</span></span>

<span data-ttu-id="91f75-120">**Varlık hareketi** sayfası, kiralama varlığını ve birikmiş amortisman hesaplarını artıran veya azaltan hareketleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="91f75-120">The **Asset transaction** page shows the transactions that either increase or decrease the lease asset and accumulated depreciation accounts.</span></span> <span data-ttu-id="91f75-121">**Yükümlülük hareketleri** sayfasında olduğu gibi borçlar, pozitif değerler olarak gösterilir; alacaklar, negatif değerler olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="91f75-121">Debits are shown as positive values, and credits are shown as negative values, as on the **Liability transactions** page.</span></span> <span data-ttu-id="91f75-122">Deftere nakledilen ilk kabul ve ardından birikmiş amortisman sayfanın sol alt kısmında varlık bakiyesi olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="91f75-122">The posted initial recognition and the next of accumulated depreciation are shown at the bottom left of the page as the asset balance.</span></span> 

## <a name="expenses-transactions"></a><span data-ttu-id="91f75-123">Gider hareketleri</span><span class="sxs-lookup"><span data-stu-id="91f75-123">Expenses transactions</span></span>

<span data-ttu-id="91f75-124">Kiralama gider hareketlerini görüntülemek için **Kiralama özeti** sayfasında bir kiralama seçin ve kiralama kaydına eklenmiş kiralama defterlerini açmak için **Defterler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="91f75-124">To view the lease expense transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="91f75-125">Ardından **Gider hareketleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="91f75-125">Then select **Expense transactions**.</span></span>

<span data-ttu-id="91f75-126">**Gider hareketleri** sayfası, kiralama için deftere nakledilen tüm giderleri (ör. faiz giderleri, amortisman giderleri ve icra maliyetleri) gösterir.</span><span class="sxs-lookup"><span data-stu-id="91f75-126">The **Expense transactions** page shows all the expenses that have been posted against the lease, such as interest expenses, depreciation expenses, and any executory costs.</span></span>
