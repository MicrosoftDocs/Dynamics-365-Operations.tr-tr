---
title: Şirketlerarası hareketlerde TDS hesaplaması
description: Bu konu, şirketlerarası hareketlerdeki aşamalardaki Kaynakta Kesilen Vergiyi (TDS) hesaplamak için kullanılan işlemi açıklamaktadır.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023661"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="70eb7-103">Şirketlerarası hareketlerde TDS hesaplaması</span><span class="sxs-lookup"><span data-stu-id="70eb7-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70eb7-104">Bu konu, şirketlerarası hareketlerdeki aşamalardaki Kaynakta Kesilen Vergiyi (TDS) hesaplamak için kullanılan işlemi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="70eb7-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="70eb7-105">Bir şirketlerarası satınalma siparişi veya satış siparişi oluşturulduğunda, TDS tutarını hesaplamak için müşteri veya satıcı için tanımlanan varsayılan TDS grubu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="70eb7-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="70eb7-106">TDS tutarı, fatura deftere nakledildikten sonra kurtarılabilir veya borç hesaplarına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="70eb7-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="70eb7-107">Orijinal satınalma siparişi veya satış siparişi için otomatik olarak bir şirketlerarası satış siparişi veya satınalma siparişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="70eb7-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="70eb7-108">Varsayılan TDS grubu şirketlerarası siparişte görüntülenir, böylece TDS hesaplanabilir.</span><span class="sxs-lookup"><span data-stu-id="70eb7-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="70eb7-109">TDS grubunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="70eb7-109">You can change the TDS group.</span></span> <span data-ttu-id="70eb7-110">Fatura, yalnızca otomatik olarak oluşturulan şirketlerarası siparişte bulunan net fatura tutarı orijinal siparişteki net fatura tutarıyla eşleşiyorsa deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="70eb7-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="70eb7-111">(Net tutar, TDS kesildikten sonraki fatura miktarıdır).</span><span class="sxs-lookup"><span data-stu-id="70eb7-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="70eb7-112">Örneğin, 50.000 değeri için bir satış faturası oluşturulur ve buna **%10** TDS grubu iliştirilir.</span><span class="sxs-lookup"><span data-stu-id="70eb7-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="70eb7-113">Deftere nakledilen fatura tutarı 45.000'dir, satış faturası için deftere nakledilen TDS tutarı 5.000'dir.</span><span class="sxs-lookup"><span data-stu-id="70eb7-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="70eb7-114">Şirketlerarası satış siparişi için otomatik olarak bir satınalma siparişi oluşturulur ve buna **%10** TDS grubu iliştirilir.</span><span class="sxs-lookup"><span data-stu-id="70eb7-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="70eb7-115">TDS grubunu **%15** olarak değiştirirseniz, otomatik olarak oluşturulan şirketlerarası satış siparişinin net faturası tutarı orijinal satış siparişinin net fatura tutarıyla eşleşmediğinden, faturayı deftere nakledemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="70eb7-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="70eb7-116">Şirketlerarası bir fatura için oluşturulan ödeme günlükleri otomatik olarak deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="70eb7-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="70eb7-117">Ödeme günlüğü yalnızca, bu satırdaki net ödeme tutarı orijinal ödeme günlüğündeki net ödeme tutarıyla eşleşiyorsa nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="70eb7-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
