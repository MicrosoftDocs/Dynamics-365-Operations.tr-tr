---
title: Satıcı için ileri tarih atılmış çeki kaydetme ve deftere nakletme
description: Günlük fişi kullanarak bir satıcıya çek kesmeden önce vadeli çekin ayrıntılarını kaydedebilirsiniz.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb7f9935b20d042551b0ce77fd6bdbf55e9f9669
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834680"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="3e146-103">Satıcı için ileri tarih atılmış çeki kaydetme ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="3e146-103">Register and post a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e146-104">Günlük fişi kullanarak bir satıcıya çek kesmeden önce vadeli çekin ayrıntılarını kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e146-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="3e146-105">Veya vadeli çeki nakledip finansal işlem oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e146-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="3e146-106">Bir satıcıdan ileri tarihe atılmış bir çeki kaydetmeden ve deftere nakletmeden önce, aşağıdaki görevi tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="3e146-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="3e146-107">İleri tarihe atılmış çekleri Nakit ve banka yönetimi sayfasında yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="3e146-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="3e146-108">Bu görevin rolü Haznedar'dır.</span><span class="sxs-lookup"><span data-stu-id="3e146-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="3e146-109">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3e146-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="3e146-110">Hesaplar > Ödemeler > Ödeme günlüğü seçeneğine gidin</span><span class="sxs-lookup"><span data-stu-id="3e146-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="3e146-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e146-111">Click New.</span></span>
3. <span data-ttu-id="3e146-112">İsim alanına VendPay' yazın.</span><span class="sxs-lookup"><span data-stu-id="3e146-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="3e146-113">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e146-113">Click Lines.</span></span>
5. <span data-ttu-id="3e146-114">Hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="3e146-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="3e146-115">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3e146-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="3e146-116">Borç alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3e146-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="3e146-117">Ödeme yöntemi alanında açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="3e146-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3e146-118">Vadeli çekin ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="3e146-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="3e146-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3e146-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="3e146-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e146-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="3e146-121">Vadeli çekler sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3e146-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="3e146-122">Çek numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3e146-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="3e146-123">Vadeli çek üzerindeki numarayı girin veya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="3e146-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="3e146-124">Amir banka adına alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3e146-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="3e146-125">Düzenleyen bankanın bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="3e146-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="3e146-126">Liste sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e146-126">Click the List tab.</span></span>
15. <span data-ttu-id="3e146-127">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e146-127">Click Post.</span></span>
16. <span data-ttu-id="3e146-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3e146-128">Close the page.</span></span>
17. <span data-ttu-id="3e146-129">Vadeli çekler sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3e146-129">Click the Postdated checks tab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]