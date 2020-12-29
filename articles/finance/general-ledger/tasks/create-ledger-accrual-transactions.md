---
title: Genel muhasebe tahakkuk hareketleri oluşturma
description: Bu görev kılavuzu, tahakkuk düzenlerine dayalı genel muhasebe tahakkuk hareketleri oluşturmayı adım adım açıklar.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2112336045086d0eb3b2fb0018f33631528a05ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448718"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="04d4c-103">Genel muhasebe tahakkuk hareketleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="04d4c-103">Create ledger accrual transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04d4c-104">Bu görev kılavuzu, tahakkuk düzenlerine dayalı genel muhasebe tahakkuk hareketleri oluşturmayı adım adım açıklar</span><span class="sxs-lookup"><span data-stu-id="04d4c-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="04d4c-105">Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="04d4c-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="04d4c-106">Listede, istediğiniz günlüğü bulun ve seçin veya yeni bir tane oluşturun.</span><span class="sxs-lookup"><span data-stu-id="04d4c-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="04d4c-107">Günlük toplu iş numarası alanındaki bağlantıyı izlemek için tıklatın.</span><span class="sxs-lookup"><span data-stu-id="04d4c-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="04d4c-108">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="04d4c-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="04d4c-109">Hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="04d4c-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="04d4c-110">Bu örnekte, sigorta harcaması tanımlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="04d4c-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="04d4c-111">Bu, düzenli gider tutarı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="04d4c-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="04d4c-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="04d4c-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="04d4c-113">Borç alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="04d4c-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="04d4c-114">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="04d4c-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="04d4c-115">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="04d4c-115">Click Functions.</span></span>
10. <span data-ttu-id="04d4c-116">Genel muhasebe tahakkukları öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="04d4c-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="04d4c-117">Tahakkuk kimliği alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="04d4c-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="04d4c-118">Listede, uygulamak istediğiniz tahakkuk düzenini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="04d4c-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="04d4c-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04d4c-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="04d4c-120">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="04d4c-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="04d4c-121">Hareketler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04d4c-121">Click Transactions.</span></span>
16. <span data-ttu-id="04d4c-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="04d4c-122">Close the page.</span></span>
17. <span data-ttu-id="04d4c-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04d4c-123">Click OK.</span></span>
18. <span data-ttu-id="04d4c-124">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="04d4c-124">Click Post.</span></span>

