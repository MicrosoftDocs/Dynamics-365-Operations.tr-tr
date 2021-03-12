---
title: Teminat mektupları
description: Bu makalede, teminat mektupları hakkında bilgiler verilmektedir. Teminat mektubunda bir banka, müşterilerinin bir kişiye ödeme veya yükümlülüğünü varsayılan olarak belirlediği zaman, o banka o kişiye belirli tutarda bir parayı ödemeyi kabul eder.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: roschlom
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b86ccc46475babb302cdbf82f5c99c26e2091501
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978801"
---
# <a name="letters-of-guarantee"></a><span data-ttu-id="fb65c-104">Teminat mektupları</span><span class="sxs-lookup"><span data-stu-id="fb65c-104">Letters of guarantee</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb65c-105">Bu makalede, teminat mektupları hakkında bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fb65c-105">This article provides information about letters of guarantee.</span></span> <span data-ttu-id="fb65c-106">Teminat mektubunda bir banka, müşterilerinin bir kişiye ödeme veya yükümlülüğünü varsayılan olarak belirlediği zaman, o banka o kişiye belirli tutarda bir parayı ödemeyi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="fb65c-106">In a letter of guarantee, a bank agrees to pay a specific amount of money to a person if one of the bank's customers defaults on a payment or obligation to that person.</span></span> 

<span data-ttu-id="fb65c-107">Garanti mektubu, bir banka (garantör) tarafından verilen bir anlaşmadır ve banka bu anlaşmayla banka müşterisinin (muhatap) bir kişiye (lehtar) ödemesini yapmaması veya bu kişiye karşı bir yükümlülüğünü yerine getirmemesi durumunda bu kişiye belirlenen miktarda parayı ödemeyi garanti eder.</span><span class="sxs-lookup"><span data-stu-id="fb65c-107">A letter of guarantee is an agreement by a bank (the guarantor) to pay a set amount of money to some person (the beneficiary) if a bank customer (the principal) defaults on a payment or an obligation to the beneficiary.</span></span> <span data-ttu-id="fb65c-108">Garanti mektupları transfer edilemez.</span><span class="sxs-lookup"><span data-stu-id="fb65c-108">Letters of guarantee aren't transferable.</span></span> <span data-ttu-id="fb65c-109">Sadece anlaşmada adı geçen lehtar için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="fb65c-109">They apply only to the beneficiary who is named in the agreement.</span></span> <span data-ttu-id="fb65c-110">Muhatap, anlaşma hükümlerine bağlı olarak, garanti mektubunun değerinde artış veya azaltma talep edebilir.</span><span class="sxs-lookup"><span data-stu-id="fb65c-110">The principal can request an increase or decrease in the value of a letter of guarantee, subject to the terms of the agreement.</span></span> 

<span data-ttu-id="fb65c-111">Bir garanti mektubunun likiditeye çevrilebilmesi için lehtarın mutlaka garanti belgesinin orijinalini sunması ve geçerlilik bitiş tarihinden önce muhatabın borcunu ödemediğini bankaya bildirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="fb65c-111">To liquidate a letter of guarantee, the beneficiary must submit the original letter of guarantee and inform the bank of the principal’s default before the expiration date.</span></span> <span data-ttu-id="fb65c-112">Banka daha sonra garanti mektubunun hükümlerine dayalı olarak, lehtarın hesabına borç tutarını öder.</span><span class="sxs-lookup"><span data-stu-id="fb65c-112">The bank then pays the amount that is due to the beneficiary's account, according to the terms in the letter of guarantee.</span></span> <span data-ttu-id="fb65c-113">Banka, kar olarak ödemeden bir yüzde ayırır.</span><span class="sxs-lookup"><span data-stu-id="fb65c-113">The bank reserves a percentage of the payment as a margin.</span></span> <span data-ttu-id="fb65c-114">Bu yüzde, taraflar arasında anlaşma yoluyla belirlenir ve anlaşma hükümlerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="fb65c-114">The percentage is agreed upon and specified in the terms of the agreement.</span></span> 

<span data-ttu-id="fb65c-115">Garanti mektubunun amacını izlemek için bir kod oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb65c-115">You can create a code to track the purpose of a letter of guarantee.</span></span> <span data-ttu-id="fb65c-116">Ayrıca, bir garanti mektubu iptal edildiğinde mektupla ilişkilendirilebilecek nedenleri belirletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb65c-116">You can also specify the reasons that can be associated with a letter of guarantee when the letter is canceled.</span></span> <span data-ttu-id="fb65c-117">Amaç kodlarını ve banka nedenlerini **Ödeme amacı kodları** ve **Banka nedenleri** sayfalarında görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb65c-117">You can view the purpose codes and bank reasons on the **Payment purpose codes** and **Bank reasons** pages.</span></span> 

<span data-ttu-id="fb65c-118">**Garanti mektubu** sayfasını şu görevleri tamamlamak için kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="fb65c-118">You can use the **Letter of guarantee** page to complete these tasks:</span></span>

-   <span data-ttu-id="fb65c-119">Doğru defter girişleri oluşturma ve el ile girişi ortadan kaldırma.</span><span class="sxs-lookup"><span data-stu-id="fb65c-119">Create correct ledger entries, and eliminate manual entry.</span></span>
-   <span data-ttu-id="fb65c-120">Tüm parasal ve parasal olmayan hareketleri kaydetme ve garanti mektuplarının bakiyelerini takip etme.</span><span class="sxs-lookup"><span data-stu-id="fb65c-120">Record all monetary and nonmonetary transactions, and track balances of letters of guarantee.</span></span>
-   <span data-ttu-id="fb65c-121">Garanti mektuplarının durumlarını ve geçerlilik bitiş tarihlerini kaydetme ve takip etme.</span><span class="sxs-lookup"><span data-stu-id="fb65c-121">Record and track the status and expiration of letters of guarantee.</span></span>
-   <span data-ttu-id="fb65c-122">Elinde garanti mektubu bulunan bankları listeleyen bir rapor oluşturma.</span><span class="sxs-lookup"><span data-stu-id="fb65c-122">Generate a report that lists the banks that are holding letters of guarantee.</span></span>

<span data-ttu-id="fb65c-123">Aşağıdaki tabloda garanti mektubunda gerçekleştirebileceğiniz eylemler açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="fb65c-123">The following table describes the actions that you can perform on a letter of guarantee.</span></span>

| <span data-ttu-id="fb65c-124">Eylem</span><span class="sxs-lookup"><span data-stu-id="fb65c-124">Action</span></span>              | <span data-ttu-id="fb65c-125">Amaç</span><span class="sxs-lookup"><span data-stu-id="fb65c-125">Purpose</span></span>                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb65c-126">Bankaya gönderilen</span><span class="sxs-lookup"><span data-stu-id="fb65c-126">Submit to bank</span></span>      | <span data-ttu-id="fb65c-127">Bankaya garanti mektubu talebi gönderin.</span><span class="sxs-lookup"><span data-stu-id="fb65c-127">Submit the letter of guarantee request to the bank.</span></span>                                                                       |
| <span data-ttu-id="fb65c-128">Bankadan alınan</span><span class="sxs-lookup"><span data-stu-id="fb65c-128">Receive from bank</span></span>   | <span data-ttu-id="fb65c-129">Banka, gönderilen talebi kabul ettiğinde bankadan garanti mektubunu teslim alın.</span><span class="sxs-lookup"><span data-stu-id="fb65c-129">After the bank agrees to the submitted request, collect the letter of guarantee from the bank.</span></span>                            |
| <span data-ttu-id="fb65c-130">Lehdara verilen</span><span class="sxs-lookup"><span data-stu-id="fb65c-130">Give to beneficiary</span></span> | <span data-ttu-id="fb65c-131">Garanti mektubunu bankadan teslim aldığınızda garanti mektubunu muhataba verin.</span><span class="sxs-lookup"><span data-stu-id="fb65c-131">After you receive the letter of guarantee from the bank, provide the letter of guarantee to the beneficiary.</span></span>              |
| <span data-ttu-id="fb65c-132">Değer artışı</span><span class="sxs-lookup"><span data-stu-id="fb65c-132">Increase value</span></span>      | <span data-ttu-id="fb65c-133">Lehtar ve muhatap anlaşmaya varırsa parasal değerini yükseltin.</span><span class="sxs-lookup"><span data-stu-id="fb65c-133">If the beneficiary and the principal agree, increase the monetary value.</span></span>                                                  |
| <span data-ttu-id="fb65c-134">Değer azalışı</span><span class="sxs-lookup"><span data-stu-id="fb65c-134">Decrease value</span></span>      | <span data-ttu-id="fb65c-135">Lehtar ve muhatap anlaşmaya varırsa parasal değerini düşürün.</span><span class="sxs-lookup"><span data-stu-id="fb65c-135">If the beneficiary and the principal agree, decrease the monetary value.</span></span>                                                  |
| <span data-ttu-id="fb65c-136">Uzat</span><span class="sxs-lookup"><span data-stu-id="fb65c-136">Extend</span></span>              | <span data-ttu-id="fb65c-137">Garanti mektubunu lehtara verdikten sonra, uzatma gerekiyorsa geçerlilik süresini uzatın.</span><span class="sxs-lookup"><span data-stu-id="fb65c-137">After you provide the letter of guarantee to the beneficiary, extend the period of validity, if an extension is required.</span></span> |
| <span data-ttu-id="fb65c-138">İptal</span><span class="sxs-lookup"><span data-stu-id="fb65c-138">Cancel</span></span>              | <span data-ttu-id="fb65c-139">Garanti mektubunun talep edildiği amaç artık geçerli değilse, anlaşmayı iptal edin.</span><span class="sxs-lookup"><span data-stu-id="fb65c-139">When the purpose that the letter of guarantee was requested for no longer applies, cancel the agreement.</span></span>                  |
| <span data-ttu-id="fb65c-140">Tasfiye et</span><span class="sxs-lookup"><span data-stu-id="fb65c-140">Liquidate</span></span>           | <span data-ttu-id="fb65c-141">Lehtar, garanti mektubunu bankaya sunduğunda garanti mektubunu paraya çevirin.</span><span class="sxs-lookup"><span data-stu-id="fb65c-141">When the beneficiary presents the letter of guarantee to the bank, cash out the letter of guarantee.</span></span>                      |


<span data-ttu-id="fb65c-142">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="fb65c-142">For more information, see the following topics:</span></span>

[<span data-ttu-id="fb65c-143">Teminat mektubu hareketi</span><span class="sxs-lookup"><span data-stu-id="fb65c-143">Letter of guarantee transaction</span></span>](tasks/letter-guarantee-transaction.md)

[<span data-ttu-id="fb65c-144">Teminat mektupları için banka hizmetlerini ve banka deftere nakil profillerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="fb65c-144">Set up bank facilities and posting profiles for letters of guarantee</span></span>](tasks/set-up-bank-facilities-posting-profiles.md)


