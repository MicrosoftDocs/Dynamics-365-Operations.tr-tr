---
title: Müşteriyle tarafındaki bir satış siparişini faturalayamazsınız
description: Faturayı otomatik olarak deftere naklet seçeneğini etkinleştirdikten sonra, orijinal satış siparişini ve başlangıçtaki doğrudan teslim alma siparişini faturalayamazsınız.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026979"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="eed23-103">Müşteriyle tarafındaki bir satış siparişini faturalayamazsınız</span><span class="sxs-lookup"><span data-stu-id="eed23-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="eed23-104">KB numarası: 4611793</span><span class="sxs-lookup"><span data-stu-id="eed23-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="eed23-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="eed23-105">Symptoms</span></span>

<span data-ttu-id="eed23-106">Bir satıcı için **Şirketlerarası** sayfasında **Faturayı otomatik olarak deftere naklet** seçeneğini etkinleştirdikten sonra, orijinal satış siparişini ve başlangıçtaki doğrudan teslim alma siparişini faturalayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="eed23-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="eed23-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="eed23-107">Resolution</span></span>

<span data-ttu-id="eed23-108">Şirketlerarası ve doğrudan teslimat siparişi faturalarının eşitleme davranışı, [Şirketlerarası siparişi deftere nakletmek için parametreleri ayarlama](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order) bölümünde açıklanan parametreler tarafından kontrol edilir ve zorlanır.</span><span class="sxs-lookup"><span data-stu-id="eed23-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="eed23-109">Bu parametreleri ayarladıktan sonra, öncelikle şirketlerarası satış siparişini faturalamalısınız.</span><span class="sxs-lookup"><span data-stu-id="eed23-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="eed23-110">Ardından orijinal satış siparişleri ve satınalma siparişleri eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="eed23-110">The original sales orders and purchase orders will then be synchronized.</span></span>
