---
title: Satış vergisi gruplarını ve madde satış vergisi gruplarını ayarlama
description: Bu görev kaydı, Satış vergisi ve Madde satış vergisi gruplarının kurulumunda size yol gösterir.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec5bbe37aa06f18172c417e903538cadc8a6f312
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "320064"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="2520a-103">Satış vergisi gruplarını ve madde satış vergisi gruplarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="2520a-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2520a-104">Bu görev kaydı, Satış vergisi ve Madde satış vergisi gruplarının kurulumunda size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="2520a-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="2520a-105">Satış vergisi grupları, müşterilere ve satıcılara iliştirilmiş satış vergisi kodu gruplarıdır.</span><span class="sxs-lookup"><span data-stu-id="2520a-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="2520a-106">Bu gruplar, belirli bir satıcıya veya müşteriye nakledilmemiş hareketlere ait genel muhasebe hesaplarına da eklenir.</span><span class="sxs-lookup"><span data-stu-id="2520a-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="2520a-107">Madde satış vergisi grupları, ürün gibi kaynaklara iliştirilmiş satış vergisi kodu gruplarıdır.</span><span class="sxs-lookup"><span data-stu-id="2520a-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="2520a-108">Belirli bir harekete uygulanan satış vergileri, hareketin hem satış vergisi grubuna hem de madde satış vergisi grubuna dahil edilen satış vergisi kodlarıyla belirlenir.</span><span class="sxs-lookup"><span data-stu-id="2520a-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="2520a-109">Satış vergisi, yalnızca, satış vergisi hesaplanması veya kaydedilmesi gereken her bir hareket için birer satış vergisi grubu ve madde satış vergisi grubu seçildiği zaman hesaplanabilir.</span><span class="sxs-lookup"><span data-stu-id="2520a-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="2520a-110">Vergi > Dolaylı vergiler | Satış vergisi | Satış vergisi grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2520a-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="2520a-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2520a-111">Click New.</span></span>
3. <span data-ttu-id="2520a-112">Satış vergisi grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="2520a-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="2520a-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="2520a-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2520a-114">Kurulum bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="2520a-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="2520a-115">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2520a-115">Click Add.</span></span>
7. <span data-ttu-id="2520a-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2520a-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="2520a-117">Satış vergisi kodu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="2520a-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="2520a-118">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2520a-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="2520a-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2520a-119">Click Save.</span></span>
11. <span data-ttu-id="2520a-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2520a-120">Close the page.</span></span>
12. <span data-ttu-id="2520a-121">Vergi > Dolaylı vergiler > Satış vergisi > Madde satış vergisi grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2520a-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="2520a-122">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2520a-122">Click New.</span></span>
14. <span data-ttu-id="2520a-123">Madde satış vergisi grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="2520a-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="2520a-124">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="2520a-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="2520a-125">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2520a-125">Click Add.</span></span>
17. <span data-ttu-id="2520a-126">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2520a-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="2520a-127">Satış vergisi kodu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="2520a-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="2520a-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2520a-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="2520a-129">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2520a-129">Click Save.</span></span>

