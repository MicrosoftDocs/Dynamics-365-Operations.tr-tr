---
title: İleri tarih atılmış çekler
description: Bu makalede, Microsoft Dynamics 365 Finance'te ileri tarih atılmış çeklere verilen destek hakkında bilgi verilmektedir. İleri tarih atılmış çekler, ileri bir tarihte ödeme yapmak veya almak için kesilen çeklerdir. Bu nedenle, çek belirtilen tarihe kadar nakde çevrilemez.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38ee6c5b3d258c313a2066b388a83330bf696d39
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448967"
---
# <a name="postdated-checks"></a><span data-ttu-id="fb6f0-105">İleri tarih atılmış çekler</span><span class="sxs-lookup"><span data-stu-id="fb6f0-105">Postdated checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb6f0-106">Bu makalede, ileri tarih atılmış çeklere verilen destek hakkında bilgi verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-106">This article provides information about support for postdated checks.</span></span> <span data-ttu-id="fb6f0-107">İleri tarih atılmış çekler, ileri bir tarihte ödeme yapmak veya almak için kesilen çeklerdir.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="fb6f0-108">Bu nedenle, çek belirtilen tarihe kadar nakde çevrilemez.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="fb6f0-109">Dynamics 365 Finance aşağıdaki tabloda gösterildiği gibi hem Borç hesapları hem Alacak hesapları altında ileri tarih atılmış çekler için tam yönetim döngüsünü destekler.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-109">Dynamics 365 Finance supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb6f0-110">Senaryo</span><span class="sxs-lookup"><span data-stu-id="fb6f0-110">Scenario</span></span></th>
<th><span data-ttu-id="fb6f0-111">Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="fb6f0-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb6f0-112">Vadeli çek oluşturma</span><span class="sxs-lookup"><span data-stu-id="fb6f0-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="fb6f0-113">Yeni bir ödeme yöntemi ayarlamanız, verilen çekler, alınan çekler ve stopaj vergisi kliring hesaplarının ödeme rutinini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb6f0-114">Kaydolun ve satıcının vadeli çekini nakledin.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="fb6f0-115">Bir satıcıya kestiğiniz ileri tarih atılmış çekin ayrıntılarını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="fb6f0-116">Ödeme deftere nakledildiğinde, satıcı yükümlülüğü tanınmış, ancak banka hesabına alacak kaydedilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="fb6f0-117">Bunun yerine, bu amaçla bir kliring hesabı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb6f0-118">Bir müşteri için vadeli çeki kayıt edin ve nakledin</span><span class="sxs-lookup"><span data-stu-id="fb6f0-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="fb6f0-119">Bir müşteriden alınan ileri tarih atılmış bir çekin ayrıntılarını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="fb6f0-120">Ödeme deftere nakledildiğinde, müşteri alacaklandırılmış, ancak banka hesabına borç kaydedilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="fb6f0-121">Bunun yerine, bu amaçla bir kliring hesabı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb6f0-122">Bir müşteri veya satıcı için ileri tarih atılmış bir yedek çeki kaydedip deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="fb6f0-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="fb6f0-123">Bir satıcıya verdiğiniz veya bir müşteriden aldığınız orijinal çek kaybolur veya hasar görürse, ileri tarih atılmış bir yedek çek yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="fb6f0-124">Çek ayrıntılarını kaydederken, orijinal çeke bir referans girin ve yeni çekin o orijinalin yedeği olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="fb6f0-125">Yedek çeki de deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb6f0-126">İleri tarih atılmış bir müşteri çekini bir satıcıya transfer etme</span><span class="sxs-lookup"><span data-stu-id="fb6f0-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="fb6f0-127">Bir müşteriden ileri tarih atılmış bir çek aldığınızda, bu çeki bir satıcıya ödeme olarak transfer edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb6f0-128">Bir müşteri veya satıcı için, ileri tarih atılmış bir çeki kapatma</span><span class="sxs-lookup"><span data-stu-id="fb6f0-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="fb6f0-129">İleri tarih atılmış bir çekin tarihi geldiğinde müşteri veya satıcı için bir bağlantı hesabına nakledilen çeki kapatın.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="fb6f0-130">Çek kapatılınca, daha önce kullanılan kliring hesabına karşı bankaya borç veya alacak yazılır.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb6f0-131">Bir satıcı için, ileri tarih atılmış çeki iptal etme</span><span class="sxs-lookup"><span data-stu-id="fb6f0-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="fb6f0-132">Bu gibi durumlarda deftere nakledilen ileri tarhi atılmış bir çeki iptal edebilirsiniz: - Çek banka tarafından döndürülür.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="fb6f0-133">- Çek yanlış bir faturaya uygulanmıştır.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="fb6f0-134">- Çek karşılığında nakit ödeme yapılmıştır.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-134">- A cash payment is made against the check.</span></span>
  </td>
  </tr>
  <tr class="even">
  <td><span data-ttu-id="fb6f0-135">İleri tarih atılmış bir çekin ödemesini durdurma</span><span class="sxs-lookup"><span data-stu-id="fb6f0-135">Stop payment for a postdated check</span></span></td>
  <td><span data-ttu-id="fb6f0-136">Yetersiz fon, satıcıyla anlaşma koşullarında değişiklik, satıcıdan tedarik edilen malların kusurlu olması veya satıcıya iade edilmesi gibi nedenlerle, satıcıya verilen, ileri tarih atılmış bir çekin ödemesini durdurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="fb6f0-137">Yalnızca takasa girmemiş çeklerin ödemesini durdurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb6f0-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
  </tr>
  </tbody>
  </table>



<span data-ttu-id="fb6f0-138">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="fb6f0-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="fb6f0-139">İleri tarih atılmış çekleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="fb6f0-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="fb6f0-140">Müşteri için ileri tarih atılmış çeki kaydetme ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="fb6f0-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="fb6f0-141">Müşterinin ileri tarih atılmış çekini kapatma</span><span class="sxs-lookup"><span data-stu-id="fb6f0-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="fb6f0-142">Satıcı için ileri tarih atılmış çeki kaydetme ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="fb6f0-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="fb6f0-143">Satıcının ileri tarih atılmış çekini kapatma</span><span class="sxs-lookup"><span data-stu-id="fb6f0-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)



