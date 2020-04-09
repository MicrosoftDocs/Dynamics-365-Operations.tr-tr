---
title: Satış vergisi gruplarını ve madde satış vergisi gruplarını ayarlama
description: Bu görev kaydı, Satış vergisi ve Madde satış vergisi gruplarının kurulumunda size yol gösterir.
author: twheeloc
manager: AnnBe
ms.date: 07-01-2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b539129e62b9b0b10df1f505cbfec5c1143138
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141638"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="ae7d8-103">Satış vergisi gruplarını ve madde satış vergisi gruplarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ae7d8-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae7d8-104">Bu görev kaydı, Satış vergisi ve Madde satış vergisi gruplarının kurulumunda size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="ae7d8-105">Satış vergisi grupları, müşterilere ve satıcılara iliştirilmiş satış vergisi kodu gruplarıdır.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="ae7d8-106">Bu gruplar, belirli bir satıcıya veya müşteriye nakledilmemiş hareketlere ait genel muhasebe hesaplarına da eklenir.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="ae7d8-107">Madde satış vergisi grupları, ürün gibi kaynaklara iliştirilmiş satış vergisi kodu gruplarıdır.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="ae7d8-108">Belirli bir harekete uygulanan satış vergileri, hareketin hem satış vergisi grubuna hem de madde satış vergisi grubuna dahil edilen satış vergisi kodlarıyla belirlenir.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="ae7d8-109">Satış vergisi, yalnızca, satış vergisi hesaplanması veya kaydedilmesi gereken her bir hareket için birer satış vergisi grubu ve madde satış vergisi grubu seçildiği zaman hesaplanabilir.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="ae7d8-110">**Gezinme bölmesi > Modüller > Vergi > Dolaylı vergiler > Satış vergisi > Satış vergisi grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="ae7d8-111">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-111">Click **New**.</span></span>
3. <span data-ttu-id="ae7d8-112">**Satış vergisi grubu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="ae7d8-113">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="ae7d8-114">**Kurulum** bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="ae7d8-115">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-115">Click **Add**.</span></span>
7. <span data-ttu-id="ae7d8-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="ae7d8-117">**Satış vergisi kodu** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ae7d8-118">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ae7d8-119">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-119">Click **Save**.</span></span>
11. <span data-ttu-id="ae7d8-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-120">Close the page.</span></span>
12. <span data-ttu-id="ae7d8-121">**Vergi > Dolaylı vergiler > Satış vergisi > Madde satış vergisi grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="ae7d8-122">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-122">Click **New**.</span></span>
14. <span data-ttu-id="ae7d8-123">**Madde satış vergisi grubu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="ae7d8-124">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="ae7d8-125">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-125">Click **Add**.</span></span>
17. <span data-ttu-id="ae7d8-126">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="ae7d8-127">**Satış vergisi kodu** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="ae7d8-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="ae7d8-129">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-129">Click **Save**.</span></span>

