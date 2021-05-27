---
title: Serbest metin faturası sayfasındaki faturalarda TDS hesaplaması
description: Bu konu, faturalardaki Kaynakta Kesilen Verginin (TDS) serbest metin faturası sayfasını kullanarak nasıl hesaplanacağını açıklamaktadır.
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023664"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="de9b5-103">Serbest metin faturası sayfasındaki faturalarda TDS hesaplaması</span><span class="sxs-lookup"><span data-stu-id="de9b5-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de9b5-104">Bu konu, faturalardaki Kaynakta Kesilen Verginin (TDS) **Serbest metin faturası** sayfasını kullanarak nasıl hesaplanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="de9b5-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="de9b5-105">**Alacak hesapları \> Faturalar \> Tüm serbest metin faturaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="de9b5-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="de9b5-106">[![Serbest metin faturası sayfası](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="de9b5-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="de9b5-107">Serbest metin faturası oluşturmak için **Yeni**'yi seçin ve gerekli ayrıntıları girin.</span><span class="sxs-lookup"><span data-stu-id="de9b5-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="de9b5-108">**Fatura** sekmesini seçin. **Stopaj vergisi grubu** bölümündeki **Değerlendirilenin yapısı** alanı, müşterinin değerlendirilen kategorisinin yapısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de9b5-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="de9b5-109">**TDS grubu** alanında, satıcı veya müşteri için tanımlanmış varsayılan TDS grubunu görüntüleyebilir veya değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de9b5-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de9b5-110">**TDS grubu** alanında bir değer seçtiğinizde, **TCS grubu** alanı kullanılamaz hale gelir.</span><span class="sxs-lookup"><span data-stu-id="de9b5-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="de9b5-111">TDS yalnızca, **Tüm müşteriler** sayfasındaki müşteri için **Stopaj vergisini hesapla** seçeneği **Evet** olarak belirlenmişse hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="de9b5-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="de9b5-112">**Vergi bilgileri** sekmesinde, **Şirket bilgileri** bölümünde, **Ad** alanında, şirket için ayarlanmış alternatif adresin şirket adını seçin.</span><span class="sxs-lookup"><span data-stu-id="de9b5-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="de9b5-113">**Stopaj vergisi** bölümünde, **Vergi Hesap Numarası (TAN)** alanı, seçilen şirketin vergi hesap numarasını (TAN) gösterir.</span><span class="sxs-lookup"><span data-stu-id="de9b5-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="de9b5-114">**Fatura satırları** sekmesinde, fatura satırları oluşturun ve gerekli ayrıntıları girin.</span><span class="sxs-lookup"><span data-stu-id="de9b5-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="de9b5-115">**Stopaj vergisi grubu** bölümünde, **Vergi hesap numarası (TAN)** alanı TAN'ı gösterirken **TDS grubu** alanı ise TDS grubunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="de9b5-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="de9b5-116">**Geçici stopaj vergisi hareketleri** sayfasını açmak için **Stopaj vergisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="de9b5-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="de9b5-117">Bu sayfanın üst bölümünde aşağıdaki alanlar vardır:</span><span class="sxs-lookup"><span data-stu-id="de9b5-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="de9b5-118">**Stopaj vergisinin toplam tutar değeri** – TDS grubunun hareketleri için hesaplanan toplam TDS.</span><span class="sxs-lookup"><span data-stu-id="de9b5-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="de9b5-119">**Değer** – Hareket için TDS hesaplamasında kullanılan toplam yüzde.</span><span class="sxs-lookup"><span data-stu-id="de9b5-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="de9b5-120">Toplam yüzde, TDS grubu ve iliştirilmiş TDS vergi kodları için tanımlanan formüle dayanır.</span><span class="sxs-lookup"><span data-stu-id="de9b5-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="de9b5-121">**Düzeltilmiş stopaj vergisi tutarı** –  TDS grubundaki tüm vergi kodları için toplam düzeltilmiş TDS tutarı.</span><span class="sxs-lookup"><span data-stu-id="de9b5-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="de9b5-122">**TDS** – Seçili bir onay kutusu, TDS grubunun harekete iliştirildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="de9b5-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="de9b5-123">**Genel bakış**, **Genel** ve **Düzeltme** sekmelerindeki alanlar, TDS grubuna iliştirilmiş her TDS vergi kodu için hesaplanmış TDS tutarı ve düzeltilmiş TDS tutarı ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="de9b5-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="de9b5-124">Belirli bir TDS vergi koduna iliştirilmiş TDS vergi bileşeni için tanımlanan eşik sınırını gözden geçirmek için **Eşik** sayfasını açmak üzere **Eşik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="de9b5-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="de9b5-125">Belirli bir TDS vergi kodu için tanımlanan formülü gözden geçirebileceğiniz **Formül tasarımcısı** sayfasını açmak için **Formül tasarımcısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="de9b5-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="de9b5-126">Serbest metin faturasını deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="de9b5-126">Post the free text invoice.</span></span> <span data-ttu-id="de9b5-127">Serbest metin faturaları için hesaplanan TDS tutarı, TDS grubundaki her bir TDS vergi kodu için tanımlanan alacak hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="de9b5-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="de9b5-128">TDS vergi kodları için borç hesapları **Stopaj vergisi kodları** sayfasında tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="de9b5-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="de9b5-129">**Stopaj vergisi hareketleri** sayfasını açmak için **Deftere nakledilen stopaj vergisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="de9b5-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="de9b5-130">**Değer** alanı, hareket için TDS hesaplamasında kullanılan toplam yüzdeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="de9b5-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="de9b5-131">**Genel bakış**, **Genel** ve **Tutar** sekmelerindeki alanlar, fatura satırlarında hesaplanan TDS tutarlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de9b5-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="de9b5-132">TDS grubuna iliştirilmiş her TDS vergi kodu için TDS hesaplama bilgilerini inceleyin.</span><span class="sxs-lookup"><span data-stu-id="de9b5-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
