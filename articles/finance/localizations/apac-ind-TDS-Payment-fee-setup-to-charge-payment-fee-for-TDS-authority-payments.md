---
title: TDS yetkili ödemeleri için ödeme masrafları ayarlama
description: Bu konu, Kaynakta Kesilen Vergi (TDS) yetkili ödemelerinde için ücretlendirilen ödeme ücretlerini nasıl ayarlayabileceğinizi açıklamaktadır.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023673"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="00e48-103">TDS yetkili ödemeleri için ödeme masrafları ayarlama</span><span class="sxs-lookup"><span data-stu-id="00e48-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00e48-104">Bu konu, Kaynakta Kesilen Vergi (TDS) yetkili ödemelerinde için ücretlendirilen ödeme ücretlerini nasıl ayarlayabileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="00e48-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="00e48-105">**Borç hesapları \> Ödeme kurulumu \> Ödeme masrafı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="00e48-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="00e48-106">[![Ödeme ücreti sayfası](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="00e48-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="00e48-107">Ödeme ücreti oluşturmak için **Yeni**'yi seçin ve gerekli ayrıntıları girin.</span><span class="sxs-lookup"><span data-stu-id="00e48-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="00e48-108">**Ücret tipi** alanında ödeme ücreti türünü seçin:</span><span class="sxs-lookup"><span data-stu-id="00e48-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="00e48-109">**Hiçbiri**</span><span class="sxs-lookup"><span data-stu-id="00e48-109">**None**</span></span>
    - <span data-ttu-id="00e48-110">**Faiz** – Faiz, TDS yetkili satıcısına yapılan geç ödemeler üzerinde ücretlendirildir.</span><span class="sxs-lookup"><span data-stu-id="00e48-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="00e48-111">**Diğer** – Diğer ücretler, TDS yetkili satıcısına yapılan geç ödemeler üzerinde ücretlendirildir.</span><span class="sxs-lookup"><span data-stu-id="00e48-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="00e48-112">**Faiz** veya **Diğer**'i seçerseniz, **Ücret** alanı otomatik olarak **Genel muhasebe** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="00e48-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="00e48-113">**Alan türü** alanında **Faiz** veya **Diğer**'i seçtiyseniz, **Ana hesap** alanında faiz veya diğer ücretlerin nakledileceği genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="00e48-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="00e48-114">Gerekli diğer ayrıntıları girin.</span><span class="sxs-lookup"><span data-stu-id="00e48-114">Enter the other required details.</span></span>
6. <span data-ttu-id="00e48-115">Çeşitli bankalar, ödeme yöntemleri, ödeme özellikleri, para birimleri ve tarih aralıkları birleşimleri için ödeme ücretlerini ayarlayabileceğiniz **Ödeme ücreti kurulumu** sayfasını açmak için Eylem Bölmesinde, **Ödeme ücreti kurulumu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="00e48-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="00e48-116">[![Ödeme masrafı kurulumu sayfası](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="00e48-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="00e48-117">**Genel bakış** sekmesinde, **Gruplandırmalar** alanında, ödeme ücretini hangi bankalar için ayarladığınızı belirtin:</span><span class="sxs-lookup"><span data-stu-id="00e48-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="00e48-118">**Tablo** – Ücret, belirli bir banka hesabı için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="00e48-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="00e48-119">**Grup** – Ücret, belirli bir banka grubu için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="00e48-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="00e48-120">**Tümü** – Ücret, tüm banka hesapları için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="00e48-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="00e48-121">**Gruplandırmalar** alanında **Tablo** veya **Grup**'u seçtiyseniz, **Banka ilişkisi** alanında, ödeme ücretini ayarladığınız belirli banka hesabını veya banka grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="00e48-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="00e48-122">**Ödeme yöntemi** alanında, ödeme ücretlerinin ödenmesi için ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="00e48-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="00e48-123">**Ödeme özellikleri** alanında, **Ödeme özellikleri** sayfasında oluşturulan ödeme özelliği kodunu seçin veya girin.</span><span class="sxs-lookup"><span data-stu-id="00e48-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="00e48-124">Ödeme belirtimi, elektronik fon transferli ödeme yöntemleriyle birlikte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="00e48-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="00e48-125">**Ödeme para birimi** alanında ücreti etkinleştiren para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="00e48-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="00e48-126">Yalnızca seçilen para birimini kullanan hareketler ücreti etkinleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="00e48-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="00e48-127">Bu alanı boş bırakırsanız, tüm para birimleri ücreti etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="00e48-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="00e48-128">**Yüzde/Tutar** alanında, hesaplama yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="00e48-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="00e48-129">Seçenekler şöyledir: **Tutar**, **Yüzde** ve **Aralık**.</span><span class="sxs-lookup"><span data-stu-id="00e48-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="00e48-130">**Ücret tutarı** alanında, ödeme yüzdesi olarak veya bir ödemenin tutarı olarak ücret tutarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="00e48-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="00e48-131">**Ücret para birimi** alanında ücretin para birimi kodunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="00e48-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="00e48-132">Seçili banka hesabının ayrıntılarını görüntülemek veya değiştirmek için **Genel** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="00e48-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="00e48-133">[![Genel sekmesi](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="00e48-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="00e48-134">**Minimum** alanında, ücreti etkinleştirecek minimum hareket tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="00e48-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="00e48-135">**Maksimum** alanında, ücreti etkinleştirecek maksimum hareket tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="00e48-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="00e48-136">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarında, ücretleri hesaplamak için kullanılacak bir tarih aralığı tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="00e48-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="00e48-137">**Minimum ücret** alanında, ödeme yüzdesi olarak veya bir ödemenin tutarı olarak ücret tutarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="00e48-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="00e48-138">**Satış vergisi grubu** alanında, ücret tutarı için satış vergisini hesaplamak üzere kullanılacak satış vergisi grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="00e48-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="00e48-139">**Madde satış vergisi grubu** alanında, ücret tutarı için madde satış vergisini hesaplamak üzere kullanılacak madde satış vergisi grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="00e48-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="00e48-140">**Aralık** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="00e48-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="00e48-141">[![Aralık sekmesi](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="00e48-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="00e48-142">**Günler** alanında, ödemenin nakil tarihi (iskonto tarihi) ve senedin vade tarihi arasındaki gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="00e48-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="00e48-143">**Yüzde/Tutar** alanında, özelliğin yüzde mi yoksa belirli bir tutar mı olduğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="00e48-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="00e48-144">**Ücret tutarı** alanında, ödeme yüzdesi olarak veya bir ödemenin tutarı olarak ücret tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="00e48-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="00e48-145">**Ödeme ücreti kurulumu** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="00e48-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="00e48-146">**Ödeme ücreti** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="00e48-146">Close the **Payment fee** page.</span></span>
