--- 
title: "Fatura günlüğüne satıcı faturası kaydetme"
description: "Bu görev kılavuzu satınalma siparişleriyle ilişkili olmayan satıcı faturalarının nasıl kaydedileceğini gösterir."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 42f93e6d8fcf62babc3e3244bc1fe76d1efd9d13
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="a75e4-103">Fatura günlüğüne satıcı faturası kaydetme</span><span class="sxs-lookup"><span data-stu-id="a75e4-103">Record a vendor invoice in the invoice journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a75e4-104">Bu görev kılavuzu satınalma siparişleriyle ilişkili olmayan satıcı faturalarının nasıl kaydedileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a75e4-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="a75e4-105">Malzeme veya hizmet giderleri bu fatura türünün örneklerindendir.</span><span class="sxs-lookup"><span data-stu-id="a75e4-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="a75e4-106">Bu kayıtta USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a75e4-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="a75e4-107">Borç hesapları > Çalışma alanları > Satıcı faturası girişi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a75e4-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="a75e4-108">Yeni fatura günlüğü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a75e4-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="a75e4-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a75e4-109">Click New.</span></span>
4. <span data-ttu-id="a75e4-110">Ad alanına günlük adını girin veya açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="a75e4-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="a75e4-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a75e4-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a75e4-112">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a75e4-112">Click Lines.</span></span>
    * <span data-ttu-id="a75e4-113">Tarih alanında, Genel Muhasebenin güncelleştirileceği nakil tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="a75e4-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="a75e4-114">Hesap alanında, Satıcı hesabını belirtin.</span><span class="sxs-lookup"><span data-stu-id="a75e4-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="a75e4-115">Fatura alanına fatura numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="a75e4-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="a75e4-116">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a75e4-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="a75e4-117">Alacak alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a75e4-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="a75e4-118">Mahsıp hesap alanına hesap numarasını girin veya açılır menü düğmesine tıklayarak aramayı açın</span><span class="sxs-lookup"><span data-stu-id="a75e4-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="a75e4-119">Satış vergisi grubunun varsayılan değeri satıcı hesabından alınır.</span><span class="sxs-lookup"><span data-stu-id="a75e4-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="a75e4-120">Madde satış vergisi grubu, Mahsup hesap alanında belirtilen ana hesaptan alınır.</span><span class="sxs-lookup"><span data-stu-id="a75e4-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="a75e4-121">Vade tarihi, Ödeme koşullarına göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="a75e4-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="a75e4-122">Nakit iskontosunun varsayılan değeri Satıcı hesabından alınır.</span><span class="sxs-lookup"><span data-stu-id="a75e4-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="a75e4-123">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a75e4-123">Click Post.</span></span>
13. <span data-ttu-id="a75e4-124">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a75e4-124">Close the page.</span></span>


