---
title: Kiralama defterlerini ayarlama
description: Bu konuda, kiralama defterlerinde saklanan bilgiler açıklanmaktadır. Kiralama defterleri sistemde kiralamanın nasıl hesaplandığını belirleyen muhasebe ilkelerini içerir.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4449012"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="b9b0d-104">Kiralama defterlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="b9b0d-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9b0d-105">Kiralama defterleri sistemde kiralamanın nasıl hesaplandığını belirleyen muhasebe ilkelerini içerir.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="b9b0d-106">Nakit bazlı muhasebeye ek olarak Varlık kiralama aşağıdaki standartları destekler:</span><span class="sxs-lookup"><span data-stu-id="b9b0d-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="b9b0d-107">ABD'deki Genel Kabul Görmüş Muhasebe İlkeleri (ABD GAAP)</span><span class="sxs-lookup"><span data-stu-id="b9b0d-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="b9b0d-108">Muhasabe Standartları Kodlaması Konu 842 (ACS 842)</span><span class="sxs-lookup"><span data-stu-id="b9b0d-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="b9b0d-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="b9b0d-109">ASC 840</span></span>
- <span data-ttu-id="b9b0d-110">Uluslararası Mali Raporlama Standardı 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="b9b0d-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="b9b0d-111">Uluslararası Muhasebe Standardı 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="b9b0d-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="b9b0d-112">Yeni bir kiralama defteri oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="b9b0d-113">**Varlık kiralama \> Kurulum \> Kiralama defterleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="b9b0d-114">Defter eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="b9b0d-115">Aşağıdaki alanları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-115">Set the following fields.</span></span>

    | <span data-ttu-id="b9b0d-116">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="b9b0d-116">Name</span></span>                                     | <span data-ttu-id="b9b0d-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9b0d-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="b9b0d-118">Deftere nakil katmanı</span><span class="sxs-lookup"><span data-stu-id="b9b0d-118">Posting layer</span></span>                            | <span data-ttu-id="b9b0d-119">Kullanılacak deftere nakil katmanını seçin.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-119">Select the posting layer to use.</span></span> <span data-ttu-id="b9b0d-120">Bir kiralamaya eklenen her defter, belirli bir nakil katmanı için ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="b9b0d-121">Her deftere nakil katmanı farklı bir deftere nakil amacına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="b9b0d-122">Kiralama türü</span><span class="sxs-lookup"><span data-stu-id="b9b0d-122">Lease type</span></span>                               | <span data-ttu-id="b9b0d-123">Kiralamanın otomatik olarak mı sınıflandırılacağını yoksa finansal kiralama veya işletme kiralaması olarak önceden tanımlanmış mı olacağını seçin.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="b9b0d-124">Muhasebe altyapısı</span><span class="sxs-lookup"><span data-stu-id="b9b0d-124">Accounting framework</span></span>                     | <span data-ttu-id="b9b0d-125">Defterle ilişkili çerçeveyi seçin.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="b9b0d-126">Kiralama süresi/Faydalı ömür Ayarlama</span><span class="sxs-lookup"><span data-stu-id="b9b0d-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="b9b0d-127">Kiralama **Otomatik** olarak ayarlanmışsa ve varlığın faydalı ömrü üzerinden kiralama süresi bu alana girilen yüzdeye eşit veya bundan fazlaysa, sistem kiralamayı finansal olarak sınıflandıracaktır.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="b9b0d-128">Bugünkü değer/Varlık adil değeri ayarı</span><span class="sxs-lookup"><span data-stu-id="b9b0d-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="b9b0d-129">Kiralama türünü belirleyecek eşiği tanımlamak için bir tamsayı girin.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="b9b0d-130">Gelecekteki minimum kira ödemelerinin bugünkü değeri, defter kurulumundaki kullanıcı tanımlı değerden daha fazla ise ve defterin kiralama sınıflandırması otomatik olarak ayarlanmışsa sistem kiralamayı finansal kiralama olarak sınıflandırır.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="b9b0d-131">Kısa süre eşiği</span><span class="sxs-lookup"><span data-stu-id="b9b0d-131">Short-term threshold</span></span>                     | <span data-ttu-id="b9b0d-132">Kısa süreli kiralamalar için bir eşik olarak kullanılacak ay sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="b9b0d-133">Kiralama süresi buraya girdiğiniz ay sayısından azsa veya bu sayıya eşitse sistem, kiralamayı kısa süreli kiralama olarak sınıflandıracaktır ve ertelenmiş kira işlemi uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="b9b0d-134">Düşük değer eşiği</span><span class="sxs-lookup"><span data-stu-id="b9b0d-134">Low value threshold</span></span>                      | <span data-ttu-id="b9b0d-135">Düşük değerli kiralamalar için eşik olarak kullanılacak bir tutar girin.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="b9b0d-136">Varlığın adil değeri buraya girdiğiniz değerden azsa veya bu değere eşitse sistem, kiralamayı düşük değerli kiralama olarak sınıflandıracaktır ve ertelenmiş kira işlemi uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="b9b0d-137">Satıcıya öde</span><span class="sxs-lookup"><span data-stu-id="b9b0d-137">Pay to vendor</span></span>                            | <span data-ttu-id="b9b0d-138">Kiralama ödemelerinin, her kiralamada belirtilen satıcı hesabına fatura olarak nakledilmesine izin vermek için bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="b9b0d-139">Kiralama ödemesi deftere nakledildiğinde satıcı hesabı alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="b9b0d-140">Bu seçenek **Hayır** olarak ayarlanırsa, bunun yerine **Kiralama deftere nakil parametreleri** sayfasındaki **Kira ödemesi** deftere nakil türü için beliritilen hesap alacaklandırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="b9b0d-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
