---
title: Vergi, fişte yanlış genel muhasebe hesabına naklediliyor
description: Bu konu, verginin fişteki yanlış genel muhasebe hesabına nakledilmesiyle ilgili sorun giderme bilgileri sağlar.
author: qire
manager: beya
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0404d71f0492e188ed5da62387bb90a336e69c5a
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947723"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="3d0cc-103">Vergi, fişte yanlış genel muhasebe hesabına naklediliyor</span><span class="sxs-lookup"><span data-stu-id="3d0cc-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d0cc-104">Deftere nakledilme sırasında, vergi fişte yanlış genel muhasebe hesabına nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="3d0cc-105">Bu sorunu gidermek için, aşağıdaki bölümlerde gereken adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="3d0cc-106">Bu konudaki örneklerde, iş belgesi olarak bir satış siparişi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="3d0cc-107">Yanlış nakledilen vergi hareketinin vergi kodunu bulma</span><span class="sxs-lookup"><span data-stu-id="3d0cc-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="3d0cc-108">**Fiş hareketleri** sayfasında, çalışmak istediğiniz hareketi seçin ve **Deftere nakledilen satış vergisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="3d0cc-109">[![Fiş hareketleri sayfasındaki deftere nakledilen satış vergisi düğmesi](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="3d0cc-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="3d0cc-110">**Satış vergisi kodu** alanındaki değeri inceleyin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="3d0cc-111">Bu örnekte bu değer **VAT 19**'dur.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="3d0cc-112">[![Deftere nakledilen satış vergisi sayfasındaki satış vergisi kodu alanı](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="3d0cc-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="3d0cc-113">Vergi kodunun genel muhasebe deftere nakil grubunu denetleme</span><span class="sxs-lookup"><span data-stu-id="3d0cc-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="3d0cc-114">**Vergi** \> **Dolaylı vergiler** \> **Satış vergisi** \> **Satış vergisi kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="3d0cc-115">Vergi kodunu bulun ve seçin, sonra **Genel muhasebe deftere nakil grubu** alanındaki değeri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="3d0cc-116">Bu örnekte bu değer **VAT**'dır.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="3d0cc-117">[![Satış vergisi kodları sayfasındaki genel muhasebe deftere nakil alanı.](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="3d0cc-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="3d0cc-118">**Genel muhasebe deftere nakil grubu** alanındaki değer bir bağlantıdır.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="3d0cc-119">Grup yapılandırmasının ayrıntılarını görüntülemek için bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="3d0cc-120">Alternatif olarak, alanı seçin ve basılı tutun (veya sağ tıklayın) ve sonra **Ayrıntıları görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="3d0cc-121">[![Ayrıntıları görüntüle komutu](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="3d0cc-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="3d0cc-122">**Satış vergisi borcu** alanında, hareket türüne göre hesap numarasının doğru olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="3d0cc-123">Doğru değilse, deftere nakledilecek hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="3d0cc-124">Bu örnekte, satış siparişinin satış vergisi, satış vergisi borçları hesabı 222200'e nakledilmelidir.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="3d0cc-125">[![Genel muhasebe deftere nakil grupları sayfasındaki satış vergisi borcu alanı.](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="3d0cc-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="3d0cc-126">Aşağıdaki tablo, **Genel muhasebe deftere nakil grupları** sayfasındaki her alan hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="3d0cc-127">Alan</span><span class="sxs-lookup"><span data-stu-id="3d0cc-127">Field</span></span>                  | <span data-ttu-id="3d0cc-128">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d0cc-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="3d0cc-129">Satış vergisi borcu</span><span class="sxs-lookup"><span data-stu-id="3d0cc-129">Sales tax payable</span></span>      | <span data-ttu-id="3d0cc-130">Vergi dairesine borç olan giden satış vergileri için ana hesap.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="3d0cc-131">Satış vergisi alacağı</span><span class="sxs-lookup"><span data-stu-id="3d0cc-131">Sales tax receivable</span></span>   | <span data-ttu-id="3d0cc-132">Vergi dairesinden alacak gelen vergiler için ana hesap.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="3d0cc-133">Kullanım vergisi gideri</span><span class="sxs-lookup"><span data-stu-id="3d0cc-133">Use tax expense</span></span>        | <span data-ttu-id="3d0cc-134">Avrupa Birliği (AB) ters gider Ürün ve Hizmet Vergisi (GST)/Uyumlaştırılmış Satış Vergisinin (HST) bir parçası olarak satıcıların talep etmediği ya da bildirmediği, vergiden düşülebilir kullanım vergilerini deftere nakledilmek için kullanılan ana hesap.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="3d0cc-135">Harekette kullanılan satış vergisi grubunda satış vergisi kodu için **Kullanım vergisi** seçeneği belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="3d0cc-136">**Genel muhasebe parametreleri** sayfasında **Satış vergisi vergilendirme kurallarını uygula** seçeneği belirtildiyse bu alan kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="3d0cc-137">Kullanım vergisi borcu</span><span class="sxs-lookup"><span data-stu-id="3d0cc-137">Use tax payable</span></span>        | <span data-ttu-id="3d0cc-138">Vergi dairelerine ödenecek gelen kullanım vergilerini deftere nakletmek için kullanılan ana hesap.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="3d0cc-139">Kapatma hesabı</span><span class="sxs-lookup"><span data-stu-id="3d0cc-139">Settlement account</span></span>     | <span data-ttu-id="3d0cc-140">**Kullanım vergisi borcu** ve **Satış vergisi alacağı** alanlarında belirtilen genel muhasebe hesaplarının net bakiyesinin nakledildiği ana hesap.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="3d0cc-141">Satıcı nakit iskontosu</span><span class="sxs-lookup"><span data-stu-id="3d0cc-141">Vendor cash discount</span></span>   | <span data-ttu-id="3d0cc-142">Bu genel muhasebe deftere nakil grubuyla ilişkili satış vergisi kodları için nakit iskontosunun nakledildiği ana hesap.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="3d0cc-143">Müşteri servis talebi iskontosu</span><span class="sxs-lookup"><span data-stu-id="3d0cc-143">Customer case discount</span></span> | <span data-ttu-id="3d0cc-144">Bu genel muhasebe deftere nakil grubuyla ilişkili satış vergisi kodları için nakit iskontosunun nakledildiği ana hesap.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="3d0cc-145">Daha fazla bilgi için bkz. [Satış vergisi için Genel muhasebe deftere nakil grupları ayarlama](tasks/set-up-ledger-posting-groups-sales-tax.md).</span><span class="sxs-lookup"><span data-stu-id="3d0cc-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="3d0cc-146">Genel muhasebe boyutlarını denetlemek için kodda hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="3d0cc-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="3d0cc-147">Kodda, deftere nakil hesabı genel muhasebe boyutuna göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="3d0cc-148">Genel muhasebe boyutu, bir hesabın veritabanındaki kayıt kodunu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="3d0cc-149">Bir satış siparişi için, bir **Tax::saveAndPost()** ve **Tax::post()** yöntemlerinde bir kesme noktası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="3d0cc-150">**\_ledgerDimension** değerine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="3d0cc-151">[![Kesme noktası olan satış siparişi kodu örneği](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="3d0cc-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="3d0cc-152">Bir satınalma siparişi için, **TaxPost::saveAndPost()** ve **TaxPost::postToTaxTrans()** yöntemlerinde bir kesme noktası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="3d0cc-153">**\_ledgerDimension** değerine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="3d0cc-154">[![Kesme noktası olan satınalma siparişi kodu örneği](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="3d0cc-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="3d0cc-155">Genel muhasebe boyutu tarafından kaydedilen kayıt koduna göre veritabanındaki hesabın görüntüleme değerini bulmak için aşağıdaki SQL sorgusunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="3d0cc-156">[![Kayıt kodunun görünüm değeri](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="3d0cc-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="3d0cc-157">**_ledgerDimension** değerinin nerede atandığını bulmak için çağrı yığınını inceleyin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="3d0cc-158">Genellikle bu değer **TmpTaxWorkTrans**'tan alınır.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="3d0cc-159">Bu durumda, değerin atanma yerini bulmak için **TmpTaxWorkTrans::insert()** ve **TmpTaxWorkTrans::update()** yönteminde bir kesme noktası eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="3d0cc-160">Özelleştirme olup olmadığını belirleyin</span><span class="sxs-lookup"><span data-stu-id="3d0cc-160">Determine whether customization exists</span></span>

<span data-ttu-id="3d0cc-161">Önceki bölümlerdeki adımları tamamladıysanız ve bir sorun bulamadıysanız bir özelleştirme olup olmadığını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="3d0cc-162">Hiçbir özelleştirme yoksa daha fazla destek için bir Microsoft servis talebi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3d0cc-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
