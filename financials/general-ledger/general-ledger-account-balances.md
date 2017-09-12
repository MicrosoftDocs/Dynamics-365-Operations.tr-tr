---
title: Genel defter hesap bakiyeleri
description: "Bu makalede, genel muhasebe hesabı bakiyelerini görüntülemek için kullanılan iki yöntem açıklanmaktadır -  Mizan listesi sayfası ve mali raporlar. Makalede, boyut kümesi bakiyelerinin nasıl güncelleştirileceği de ele alınmaktadır."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13191
ms.assetid: ea3650ac-34a0-4516-b75b-801c2164107d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 05db6bc373b69a623939eb0e39876332b64cd64b
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---

# <a name="general-ledger-account-balances"></a><span data-ttu-id="9e0b1-104">Genel defter hesap bakiyeleri</span><span class="sxs-lookup"><span data-stu-id="9e0b1-104">General ledger account balances</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9e0b1-105">Bu makalede, genel muhasebe hesabı bakiyelerini görüntülemek için kullanılan iki yöntem açıklanmaktadır -  Mizan listesi sayfası ve mali raporlar.</span><span class="sxs-lookup"><span data-stu-id="9e0b1-105">This article explains two ways to view general ledger account balances -  the Trial balance list page and financial reports.</span></span> <span data-ttu-id="9e0b1-106">Makalede, boyut kümesi bakiyelerinin nasıl güncelleştirileceği de ele alınmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9e0b1-106">It also discusses how to update dimension set balances.</span></span>

<span data-ttu-id="9e0b1-107">Kullanıcıların genel defterdeki bakiyeleri görebilmesi için çeşitli yöntemler mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="9e0b1-107">There are a variety of ways users can view balances in the general ledger.</span></span> <span data-ttu-id="9e0b1-108">En yaygın kullanılan seçeneklerden bazıları şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9e0b1-108">Some of the most common options are:</span></span>

-   <span data-ttu-id="9e0b1-109">Mizan</span><span class="sxs-lookup"><span data-stu-id="9e0b1-109">Trial balance</span></span>
-   <span data-ttu-id="9e0b1-110">Mali raporlar</span><span class="sxs-lookup"><span data-stu-id="9e0b1-110">Financial reports</span></span>
-   <span data-ttu-id="9e0b1-111">Fiş hareketleri</span><span class="sxs-lookup"><span data-stu-id="9e0b1-111">Voucher transactions</span></span>
-   <span data-ttu-id="9e0b1-112">Genel muhasebe raporları</span><span class="sxs-lookup"><span data-stu-id="9e0b1-112">Ledger reports</span></span>

<span data-ttu-id="9e0b1-113">En yaygın yöntemler arasında mizan liste sayfası ve mali raporlar yer alır.</span><span class="sxs-lookup"><span data-stu-id="9e0b1-113">The most common ways are the trial balance list page and financial reports.</span></span>

## <a name="trial-balance"></a><span data-ttu-id="9e0b1-114">Mizan</span><span class="sxs-lookup"><span data-stu-id="9e0b1-114">Trial balance</span></span>
<span data-ttu-id="9e0b1-115">Mizan, bir hesabın bakiyelerinin ve/veya belirli bir zaman dilimi için boyutların tümünü gösteren bir liste sayfasıdır.</span><span class="sxs-lookup"><span data-stu-id="9e0b1-115">The trial balance is a list page that shows all of the balances of an account and/or dimensions for a given period of time.</span></span> <span data-ttu-id="9e0b1-116">Mizan ilk kez açıldığında, Parametreler altında ayarlanmış olan tarih ve özellik bilgileri için bakiyelerle birlikte yenilenir.</span><span class="sxs-lookup"><span data-stu-id="9e0b1-116">When the trial balance is first opened it refreshes with the balances for the dates and properties that are set in the Parameters.</span></span> <span data-ttu-id="9e0b1-117">Tarihler, nakil katmanı, açılış bakiyelerinin nasıl görüntüleneceği ve hangi kapatma hareket türlerinin görüntüleneceği Parametreler altında değiştirilebilen özellikler arasındadır.</span><span class="sxs-lookup"><span data-stu-id="9e0b1-117">Properties that can be changed in Parameters are the dates, posting layer, how they want opening balances to appear, and what closing transaction types to show.</span></span> 

<span data-ttu-id="9e0b1-118">Bir kullanıcı parametreleri değiştiğinde bakiyeleri yenilenir.</span><span class="sxs-lookup"><span data-stu-id="9e0b1-118">When a user changes the parameters the balances are refreshed.</span></span> <span data-ttu-id="9e0b1-119">Kullanıcı ayrıca bakiyeleri hangi boyut grubu için görüntülemek istediğini ve boyutların her birinin ayrı sütunlarda görüntülenip görüntülenmeyeceğini seçebilir.</span><span class="sxs-lookup"><span data-stu-id="9e0b1-119">The user can also pick what dimension set they want to view balances for and whether each of the dimensions show in separate columns.</span></span> 

<span data-ttu-id="9e0b1-120">Kullanıcılar, bakiyeyi oluşturan hareketleri görüntülemek için bakiyeleri ayrıntılı olarak gözden geçirebilirler.</span><span class="sxs-lookup"><span data-stu-id="9e0b1-120">Users can drill down on the balances to view the transactions that make up the balance.</span></span>    

<span data-ttu-id="9e0b1-121">Daha fazla bilgi için bkz. [Finansal raporlara göz at](view-financial-reports.md).</span><span class="sxs-lookup"><span data-stu-id="9e0b1-121">For more information, see [View financial reports](view-financial-reports.md).</span></span>




