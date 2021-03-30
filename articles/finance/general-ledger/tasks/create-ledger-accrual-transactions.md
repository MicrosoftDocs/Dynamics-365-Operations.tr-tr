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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1722c72ebc5ea7c0f8704ba3761f971f5075744
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216461"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="41827-103">Genel muhasebe tahakkuk hareketleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="41827-103">Create ledger accrual transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41827-104">Bu görev kılavuzu, tahakkuk düzenlerine dayalı genel muhasebe tahakkuk hareketleri oluşturmayı adım adım açıklar</span><span class="sxs-lookup"><span data-stu-id="41827-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="41827-105">Genel muhasebe > Günlük girişleri > Genel günlükler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="41827-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="41827-106">Listede, istediğiniz günlüğü bulun ve seçin veya yeni bir tane oluşturun.</span><span class="sxs-lookup"><span data-stu-id="41827-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="41827-107">Günlük toplu iş numarası alanındaki bağlantıyı izlemek için tıklatın.</span><span class="sxs-lookup"><span data-stu-id="41827-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="41827-108">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="41827-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="41827-109">Hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="41827-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="41827-110">Bu örnekte, sigorta harcaması tanımlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="41827-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="41827-111">Bu, düzenli gider tutarı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="41827-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="41827-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="41827-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="41827-113">Borç alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="41827-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="41827-114">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="41827-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="41827-115">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="41827-115">Click Functions.</span></span>
10. <span data-ttu-id="41827-116">Genel muhasebe tahakkukları öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="41827-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="41827-117">Tahakkuk kimliği alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="41827-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="41827-118">Listede, uygulamak istediğiniz tahakkuk düzenini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="41827-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="41827-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41827-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="41827-120">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="41827-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="41827-121">Hareketler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41827-121">Click Transactions.</span></span>
16. <span data-ttu-id="41827-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="41827-122">Close the page.</span></span>
17. <span data-ttu-id="41827-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41827-123">Click OK.</span></span>
18. <span data-ttu-id="41827-124">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41827-124">Click Post.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]