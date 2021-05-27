---
title: Vergi hesaplanmıyor veya vergi tutarı sıfır
description: Bu konu, vergi tutarı 0'sa (sıfır) veya vergi hesaplanmıyorsa yardımcı olabilecek sorun giderme bilgileri sağlar.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c398579a0a408e7f5625a3e801a967955c4b1e5b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020127"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="e11b8-103">Vergi hesaplanmıyor veya vergi tutarı sıfır</span><span class="sxs-lookup"><span data-stu-id="e11b8-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e11b8-104">Bir harekette 0 (sıfır) olmayan bir satır tutarı olabilir ancak vergi hesaplanmıyordur veya hesaplanan vergi tutarı 0'dır.</span><span class="sxs-lookup"><span data-stu-id="e11b8-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="e11b8-105">Bu sorunu gidermek için, aşağıdaki bölümlerde gereken adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="e11b8-106">Vergi kodlarının hareket tarafından doğru şekilde seçildiğini doğrulayın</span><span class="sxs-lookup"><span data-stu-id="e11b8-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="e11b8-107">Hareket doğru vergi kodlarını seçmiyorsa veya hiçbir vergi kodu seçmiyorsa, bunlar üzerinde vergi hesaplanmaz.</span><span class="sxs-lookup"><span data-stu-id="e11b8-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="e11b8-108">Vergi kodlarının hareket tarafından doğru şekilde seçildiğini doğrulamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="e11b8-109">Hareket satırında, **Satır ayrıntıları** hızlı sekmesinde, **Kurulum** sekmesinde, **Satış vergisi** bölümünde, **Madde satış vergisi grubu** ve **Satış vergisi grubu** alanlarında doğru vergi gruplarının seçilmiş olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e11b8-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="e11b8-110">Doğru vergi grupları seçilmemişse doğruları seçin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="e11b8-111">[![Madde satış vergisi grubu ve Satış vergisi grupları](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="e11b8-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="e11b8-112">**Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Satış vergisi grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="e11b8-113">Uygun satış vergisi grubunu seçin ve **Kurulum** hızlı sekmesinde **Satış vergisi kodu** alanındaki vergi kodunu not edin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="e11b8-114">[![Satış vergisi grupları sayfası](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="e11b8-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="e11b8-115">**Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Madde satış vergisi grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="e11b8-116">Uygun madde satış vergisi grubunu seçin ve **Kurulum** hızlı sekmesinde **Satış vergisi kodu** alanındaki vergi kodunun, satış vergisi grubunun vergi koduyla eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e11b8-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="e11b8-117">[![Madde satış vergisi grupları sayfası](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="e11b8-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="e11b8-118">Vergi kodları eşleşmiyorsa gruplardan birinin satış vergisi kodunu güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="e11b8-119">Seçilen vergi kodlarının muaf olmadığını ve doğru vergi oranı değerine sahip olduklarını doğrulayın</span><span class="sxs-lookup"><span data-stu-id="e11b8-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="e11b8-120">Vergi kodları muafsa veya vergi oranı 0 (sıfır) ise, vergi hesaplama sonucu 0 olur.</span><span class="sxs-lookup"><span data-stu-id="e11b8-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="e11b8-121">Seçili vergi kodlarının muaf olup olmadığını ve bunlara doğru vergi oranının uygulanıp uygulanmadığını doğrulamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="e11b8-122">**Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Satış vergisi grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="e11b8-123">Uygun satış vergisi grubunu seçin ve **Kurulum** hızlı sekmesinde **Muafiyet** onay kutusunun işaretlenmemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e11b8-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="e11b8-124">Onay kutusu işaretliyse işareti kaldırın.</span><span class="sxs-lookup"><span data-stu-id="e11b8-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="e11b8-125">[![Satış vergisi grupları sayfasındaki Muafiyet onay kutusu](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="e11b8-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="e11b8-126">**Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Satış vergisi kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="e11b8-127">Uygun satış vergisi kodunu seçin ve **Değer** alanında vergi oranı değerinin 0 (sıfır) olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e11b8-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="e11b8-128">0 ise, alanı doğru vergi oranına ayarlanmış şekilde güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="e11b8-129">[![Satış vergisi kod değerleri sayfasındaki değer alanı](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="e11b8-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="e11b8-130">Doğru vergi tutarının sıfır olup olmadığını belirleyin</span><span class="sxs-lookup"><span data-stu-id="e11b8-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="e11b8-131">Bazı senaryolarda, vergi tutarı 0 (sıfır) doğrudur.</span><span class="sxs-lookup"><span data-stu-id="e11b8-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="e11b8-132">Hareketiniz için 0'ın doğru vergi tutarı olup olmadığını belirlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="e11b8-133">**Genel muhasebe** \> **Genel muhasebe ayarı** \> **Genel muhasebe parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="e11b8-134">**Satış vergisi** sekmesinde, **Hesaplama yöntemi** alanında, **Toplam**'ın seçildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e11b8-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="e11b8-135">[![Genel muhasebe parametreleri sayfasındaki Hesaplama yöntemi alanı](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="e11b8-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="e11b8-136">**Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Satış vergisi kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="e11b8-137">Uygun satış vergisi kodunu seçin, **Hesaplama** \> **Marjinal taban**'ı seçin ve marjinal tabanın, **Fatura bakiyesinin net tutarı** veya **Diğer satış vergi tutarları dahil fatura toplamı** olarak ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e11b8-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="e11b8-138">Daha fazla bilgi için bkz. [Diğer satış vergisi tutarları dahil fatura toplamı](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span><span class="sxs-lookup"><span data-stu-id="e11b8-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="e11b8-139">2 ve 4 numaralı adımlarda doğru değerler ayarlıysa, hareketin toplam tutarının 0 (sıfır) olup olmadığını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="e11b8-140">Toplam tutar 0 ise, vergi tutarının 0 olması beklenen sonuçtur.</span><span class="sxs-lookup"><span data-stu-id="e11b8-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="e11b8-141">Vergi hesaplaması, fatura bakiyesinin toplam tutarını temel aldığından ve bu tutar satır başına olmadığından, vergi hesaplamasından sonraki her satıra 0 numaralı vergi tutarı tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="e11b8-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="e11b8-142">Özelleştirme olup olmadığını belirleyin</span><span class="sxs-lookup"><span data-stu-id="e11b8-142">Determine whether customization exists</span></span>

<span data-ttu-id="e11b8-143">Önceki bölümlerdeki adımları tamamladıysanız ve bir sorun bulamadıysanız bir özelleştirme olup olmadığını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e11b8-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="e11b8-144">Hiçbir özelleştirme yoksa daha fazla destek için bir Microsoft servis talebi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e11b8-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
