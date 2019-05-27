---
title: Fatura günlüğüne satıcı faturası kaydetme
description: Bu görev kılavuzu satınalma siparişleriyle ilişkili olmayan satıcı faturalarının nasıl kaydedileceğini gösterir.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 775f3764d34cecbfc071ff7420d32c7832b42308
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556375"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="46232-103">Fatura günlüğüne satıcı faturası kaydetme</span><span class="sxs-lookup"><span data-stu-id="46232-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46232-104">Bu görev kılavuzu satınalma siparişleriyle ilişkili olmayan satıcı faturalarının nasıl kaydedileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="46232-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="46232-105">Malzeme veya hizmet giderleri bu fatura türünün örneklerindendir.</span><span class="sxs-lookup"><span data-stu-id="46232-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="46232-106">Bu kayıtta USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="46232-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="46232-107">Borç hesapları > Çalışma alanları > Satıcı faturası girişi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="46232-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="46232-108">Yeni fatura günlüğü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="46232-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="46232-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="46232-109">Click New.</span></span>
4. <span data-ttu-id="46232-110">Ad alanına günlük adını girin veya açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="46232-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="46232-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="46232-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="46232-112">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="46232-112">Click Lines.</span></span>
    * <span data-ttu-id="46232-113">Tarih alanında, Genel Muhasebenin güncelleştirileceği nakil tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="46232-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="46232-114">Hesap alanında, Satıcı hesabını belirtin.</span><span class="sxs-lookup"><span data-stu-id="46232-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="46232-115">Fatura alanına fatura numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="46232-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="46232-116">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="46232-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="46232-117">Alacak alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="46232-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="46232-118">Mahsıp hesap alanına hesap numarasını girin veya açılır menü düğmesine tıklayarak aramayı açın</span><span class="sxs-lookup"><span data-stu-id="46232-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="46232-119">Satış vergisi grubunun varsayılan değeri satıcı hesabından alınır.</span><span class="sxs-lookup"><span data-stu-id="46232-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="46232-120">Madde satış vergisi grubu, Mahsup hesap alanında belirtilen ana hesaptan alınır.</span><span class="sxs-lookup"><span data-stu-id="46232-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="46232-121">Vade tarihi, Ödeme koşullarına göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="46232-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="46232-122">Nakit iskontosunun varsayılan değeri Satıcı hesabından alınır.</span><span class="sxs-lookup"><span data-stu-id="46232-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="46232-123">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="46232-123">Click Post.</span></span>
13. <span data-ttu-id="46232-124">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="46232-124">Close the page.</span></span>

