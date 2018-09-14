--- 
title: "Genel muhasebe tahakkuk hareketleri oluşturma"
description: "Bu görev kılavuzu, tahakkuk düzenlerine dayalı genel muhasebe tahakkuk hareketleri oluşturmayı adım adım açıklar."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4a65bec066bdcb01ce8acf8cfbf2d31611104921
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="76e30-103">Genel muhasebe tahakkuk hareketleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="76e30-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76e30-104">Bu görev kılavuzu, tahakkuk düzenlerine dayalı genel muhasebe tahakkuk hareketleri oluşturmayı adım adım açıklar</span><span class="sxs-lookup"><span data-stu-id="76e30-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="76e30-105">Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="76e30-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="76e30-106">Listede, istediğiniz günlüğü bulun ve seçin veya yeni bir tane oluşturun.</span><span class="sxs-lookup"><span data-stu-id="76e30-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="76e30-107">Günlük toplu iş numarası alanındaki bağlantıyı izlemek için tıklatın.</span><span class="sxs-lookup"><span data-stu-id="76e30-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="76e30-108">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="76e30-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="76e30-109">Hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="76e30-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="76e30-110">Bu örnekte, sigorta harcaması tanımlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="76e30-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="76e30-111">Bu, düzenli gider tutarı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="76e30-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="76e30-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="76e30-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="76e30-113">Borç alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="76e30-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="76e30-114">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="76e30-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="76e30-115">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="76e30-115">Click Functions.</span></span>
10. <span data-ttu-id="76e30-116">Genel muhasebe tahakkukları öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="76e30-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="76e30-117">Tahakkuk kimliği alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="76e30-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="76e30-118">Listede, uygulamak istediğiniz tahakkuk düzenini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="76e30-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="76e30-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76e30-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="76e30-120">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="76e30-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="76e30-121">Hareketler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76e30-121">Click Transactions.</span></span>
16. <span data-ttu-id="76e30-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="76e30-122">Close the page.</span></span>
17. <span data-ttu-id="76e30-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76e30-123">Click OK.</span></span>
18. <span data-ttu-id="76e30-124">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76e30-124">Click Post.</span></span>


