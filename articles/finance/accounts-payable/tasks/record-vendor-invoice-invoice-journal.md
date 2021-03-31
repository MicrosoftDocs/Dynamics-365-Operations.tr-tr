---
title: Fatura günlüğüne satıcı faturası kaydetme
description: Bu görev kılavuzu satınalma siparişleriyle ilişkili olmayan satıcı faturalarının nasıl kaydedileceğini gösterir.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a60a5959046ca9e953bac80aaeb382d07a267643
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227148"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="31d68-103">Fatura günlüğüne satıcı faturası kaydetme</span><span class="sxs-lookup"><span data-stu-id="31d68-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31d68-104">Bu görev kılavuzu satınalma siparişleriyle ilişkili olmayan satıcı faturalarının nasıl kaydedileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="31d68-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="31d68-105">Malzeme veya hizmet giderleri bu fatura türünün örneklerindendir.</span><span class="sxs-lookup"><span data-stu-id="31d68-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="31d68-106">Bu kayıtta USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="31d68-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="31d68-107">**Gezinti bölmesi > Modüller > Borç hesapları > Çalışma alanları > Satıcı faturası girişi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="31d68-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="31d68-108">**Eylem Bölmesi**'nde, **Yeni fatura günlüğü**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31d68-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="31d68-109">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31d68-109">Click **New**.</span></span>
4. <span data-ttu-id="31d68-110">**Ad** alanına günlük adını girin veya açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="31d68-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="31d68-111">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="31d68-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="31d68-112">**Eylem Bölmesi**'nde, **Satırlar** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31d68-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="31d68-113">**Tarih** alanında, Genel Muhasebenin güncelleştirileceği nakil tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="31d68-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="31d68-114">**Hesap** alanında, **Satıcı hesabı**'nı belirtin.</span><span class="sxs-lookup"><span data-stu-id="31d68-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="31d68-115">**Fatura** alanına fatura numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="31d68-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="31d68-116">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="31d68-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="31d68-117">**Alacak** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="31d68-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="31d68-118">**Mahsup hesap** alanına hesap numarasını girin veya açılır menü düğmesine tıklayarak aramayı açın</span><span class="sxs-lookup"><span data-stu-id="31d68-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="31d68-119">**Satış vergisi grubu**'nun varsayılan değeri satıcı hesabından alınır.</span><span class="sxs-lookup"><span data-stu-id="31d68-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="31d68-120">**Madde satış vergisi grubu**, **Mahsup hesap** alanında belirtilen ana hesaptan alınır.</span><span class="sxs-lookup"><span data-stu-id="31d68-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="31d68-121">**Vade tarihi**, Ödeme koşullarına göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="31d68-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="31d68-122">**Nakit iskontosu**'nun varsayılan değeri Satıcı hesabından alınır.</span><span class="sxs-lookup"><span data-stu-id="31d68-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="31d68-123">Satıcı faturası günlüğü iş akışını etkinleştirdiyseniz **İş Akışı > Gönder**'i tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31d68-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="31d68-124">Gönderiminiz onaylandığında, hareket deftere nakil tarihi genel muhasebe defterine nakil için Beklemede veya Kapalı olan bir döneme denk geliyorsa tarih bir sonraki açık dönemin ilk gününe ertelenir.</span><span class="sxs-lookup"><span data-stu-id="31d68-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="31d68-125">**Naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31d68-125">Click **Post**.</span></span>
13. <span data-ttu-id="31d68-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="31d68-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]