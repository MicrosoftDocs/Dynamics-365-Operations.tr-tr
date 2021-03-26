---
title: Toplu işle izlenen maddeler için geliştirilmiş işleme
description: Bu konuda, ekstrenin deftere nakil işlemi sırasında toplu olarak izlenen maddeler için toplu işlerin işlenmesine yönelik yapılan geliştirmeler açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 00e1fcb36d685798f3ad7d667805c97bddcceb36
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211165"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="6ba65-103">Toplu işle izlenen maddeler için geliştirilmiş işleme</span><span class="sxs-lookup"><span data-stu-id="6ba65-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]


<span data-ttu-id="6ba65-104">Satış Noktası'nda (POS), toplu iş numaraları toplu olarak izlenen maddeler için satış sırasında yakalanamaz.</span><span class="sxs-lookup"><span data-stu-id="6ba65-104">In Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="6ba65-105">Ancak, belirli yapılandırmalarda satışlar merkezde müşteri siparişleri veya ekstre deftere nakil işlemi aracılığıyla deftere aktarıldığında, Microsoft Dynamics sistemi toplu izlenen maddeler için geçerli toplu iş numaraları olmasını bekler ve bu numaralar faturalama işlemi sırasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6ba65-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="6ba65-106">Ürünler için geçerli toplu iş numaraları varsa, müşteri siparişi faturalama işlemi ve ekstre deftere nakil işleminden gerçekleştirilen satış siparişi faturalama işlemi bu numaraları kullanır.</span><span class="sxs-lookup"><span data-stu-id="6ba65-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="6ba65-107">Aksi takdirde, müşteri siparişi faturalama işlemi deftere nakledilemez ve POS kullanıcısı hata mesajı alır.</span><span class="sxs-lookup"><span data-stu-id="6ba65-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="6ba65-108">Ekstre deftere nakil işlemi hata durumuna geçer.</span><span class="sxs-lookup"><span data-stu-id="6ba65-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="6ba65-109">Bu hata durumu, ürünler için negatif stok etkinleştirildiğinde de oluşur.</span><span class="sxs-lookup"><span data-stu-id="6ba65-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="6ba65-110">Retail sürüm 10.0.4 ve sonraki sürümlerde yapılan geliştirmeler, toplu işle izlenen maddeler için negatif stok etkinleştirildiğinde, stoğun 0 (sıfır) olması veya toplu iş numarasının kullanılabilir olmaması durumunda müşteri siparişi faturalama ve ekstre deftere nakil işlemi aracılığıyla satış siparişi faturalama işleminin engellenmemesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="6ba65-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="6ba65-111">Yeni işlev, toplu iş numaraları olmadığında satış satırları için varsayılan bir toplu iş kodu kullanır.</span><span class="sxs-lookup"><span data-stu-id="6ba65-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="6ba65-112">Müşteri siparişleri için kullanılan varsayılan toplu iş kodunu tanımlamak için **Commerce parametreleri** sayfasında bulunan **Müşteri siparişleri** sekmesindeki **Sipariş** hızlı sekmesinde **Varsayılan toplu iş kodu** alanını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6ba65-112">To define the default batch ID that is used for customer orders, on the **Commerce parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="6ba65-113">Ekstre deftere nakil işlemi aracılığıyla satış siparişi faturalama için kullanılan varsayılan toplu iş kodunu tanımlamak üzere **Commerce parametreleri** sayfasında bulunan **Deftere nakil** sekmesindeki **Stok güncelleştirmesi** hızlı sekmesinde **Varsayılan toplu iş kodu** alanını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6ba65-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Commerce parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="6ba65-114">Bu işlev yalnızca, belirli mağaza ambarı ve maddeleri için gelişmiş ambarlama etkin olduğunda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6ba65-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="6ba65-115">Sonraki bir sürümde, işlev gelişmiş ambar yönetimi kullanılmayan senaryolar için de desteklenecektir.</span><span class="sxs-lookup"><span data-stu-id="6ba65-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="6ba65-116">Gelişmiş olmayan ambar yönetimi senaryoları için ekstre deftere nakledilirken, toplu işle izlenen maddelerin gelişmiş şekilde işlenmesiyle ilgili destek Retail 10.0.5 sürümünde kullanıma sunuldu.</span><span class="sxs-lookup"><span data-stu-id="6ba65-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]