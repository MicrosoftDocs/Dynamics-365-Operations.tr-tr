---
title: Günlükleri kullanarak faturalardaki TDS'yi hesaplama
description: Bu konuda, günlüklerde Kaynakta Kesilen Vergi (TDS) hesaplamaya yönelik adımlar listelenmektedir.
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023672"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="c688b-103">Günlükleri kullanarak faturalardaki TDS'yi hesaplama</span><span class="sxs-lookup"><span data-stu-id="c688b-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c688b-104">Bu konuda, günlüklerde Kaynakta Kesilen Vergi (TDS) hesaplamaya yönelik adımlar listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="c688b-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="c688b-105">**Yevmiye defterleri** sayfasını açarak (**Genel muhasebe > Günlük girişleri > Yevmiye defterleri**) başlayın.</span><span class="sxs-lookup"><span data-stu-id="c688b-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="c688b-106">[![Yevmiye defterleri](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="c688b-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="c688b-107">Tabloda listelenen günlük formlarını kullanarak günlük satırları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c688b-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="c688b-108">Hesap türü ve mahsup hesap türünü seçin ve hareketin tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="c688b-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="c688b-109">**Fatura onay günlüğü** sayfasında, **Fişleri bul**'u seçin TDS'nin hesaplanacağı faturaları seçin.</span><span class="sxs-lookup"><span data-stu-id="c688b-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="c688b-110">**Fatura kaydı** sayfasında veya **Fişleri bul** sayfasında oluşturulan faturaları görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="c688b-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="c688b-111">**Günlük fişi** sayfasının **Genel** sekmesinde, **TDS grubu** alanında satıcı veya müşteri için tanımlanan varsayılan TDS grubunu görüntüleyin veya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c688b-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="c688b-112">Günlük satırlarında hesaplanan TDS tutarı, **TDS grubu** alanında listelenen TDS vergi kodları için belirlenen formüle dayanır.</span><span class="sxs-lookup"><span data-stu-id="c688b-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="c688b-113">**TDS grubu** alanında bir TDS grubu seçtiğinizde, **Stopaj vergisi grubu** alanı ve **TCS grubu** alanı kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="c688b-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="c688b-114">**Stopaj vergisi grubu** alanı yalnızca **Yevmiye defteri** sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c688b-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="c688b-115">TDS yalnızca, **Tüm satıcılar** veya **Tüm müşteriler** sayfalarındaki satıcı veya müşteri için **Stopaj vergisini hesapla** onay kutusu seçilmişse hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="c688b-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="c688b-116">**Vergi bilgileri** sekmesini seçin. Ardından gerekliyse bu alanda şirket için ayarlanmış alternatif şirket adreslerini seçin.</span><span class="sxs-lookup"><span data-stu-id="c688b-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="c688b-117">Şirket adını, **Şirket bilgileri** alan grubunun altında bulunan **Ad** alanından görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c688b-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="c688b-118">**Stopaj vergisi** alan grubunun altındaki **Değerlendirilenin yapısı** alanında bulunan satıcı veya müşterinin değerlendirilen yapısı kategorisini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="c688b-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="c688b-119">**Vergi Hesap Numarası** (**TAN**) alanında, görüntülenen şirket adının TAN değerini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="c688b-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="c688b-120">**Geçici stopaj vergisi hareketleri** sayfasını açmak için **Stopaj vergisi** menüsünde **Stopaj vergisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c688b-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="c688b-121">**Geçici stopaj vergisi hareketleri** sayfasının üst bölmesinde aşağıdaki alanlar görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c688b-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="c688b-122">**Stopaj vergisinin toplam tutar değeri** - TDS grubunun hareketleri için hesaplanan toplam TDS.</span><span class="sxs-lookup"><span data-stu-id="c688b-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="c688b-123">**Değer** -Hareket için TDS hesaplamasında kullanılan toplam yüzde.</span><span class="sxs-lookup"><span data-stu-id="c688b-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="c688b-124">Toplam yüzde, TDS grubuna iliştirilmiş TDS vergi kodları için tanımlanan formüle dayanır.</span><span class="sxs-lookup"><span data-stu-id="c688b-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="c688b-125">**Düzeltilmiş stopaj vergisi tutarı** - TDS grubundaki tüm vergi kodları için toplam düzeltilmiş TDS tutarı.</span><span class="sxs-lookup"><span data-stu-id="c688b-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="c688b-126">**TDS** - Seçilirse, hareketle bir TDS grubu ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="c688b-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="c688b-127">**Geçici stopaj vergisi hareketleri** sayfasındaki **Genel bakış**, **Genel** ve **Düzeltme** sekmelerindeki alanlar, TDS grubuna iliştirilmiş her TDS vergi kodu için hesaplanmış TDS tutarı ve düzeltilmiş TDS tutarı ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c688b-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="c688b-128">**Eşik** sayfasını açmak için **Eşik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c688b-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="c688b-129">Bu sayfada, belirli bir TDS vergi koduna ilişkilendirilmiş TDS vergi bileşeni için tanımlanan eşik sınırı ve istisna eşik sınırını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="c688b-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="c688b-130">**Formül tasarımcısı** formunu açmak için **Formül tasarımcısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c688b-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="c688b-131">Bu sayfada, belirli bir TDS vergi kodu için tanımlanan formülü görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="c688b-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="c688b-132">**Günlük fişi** sayfasına dönmek için **Formül tasarımcısı**'nı ve **Geçici stopaj vergisi hareketleri** sayfalarını kapatın.</span><span class="sxs-lookup"><span data-stu-id="c688b-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="c688b-133">Gerekli diğer ayrıntıları girin.</span><span class="sxs-lookup"><span data-stu-id="c688b-133">Enter the other required details.</span></span> <span data-ttu-id="c688b-134">Günlüğü doğrulayın ve deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="c688b-134">Validate and post the journal.</span></span> <span data-ttu-id="c688b-135">Satınalma faturalarında hesaplanan TDS tutarı, borç hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="c688b-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="c688b-136">Satış faturalarında hesaplanan TDS tutarı, TDS grubundaki her bir TDS vergi kodu için tanımlanan alacak hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="c688b-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="c688b-137">TDS vergi kodları için borç hesapları veya alacak hesapları **Stopaj vergisi kodları** sayfasında tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c688b-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="c688b-138">**Stopaj** **vergisi** **hareketleri** sayfasını açmak için **Deftere nakledilen stopaj vergisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c688b-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="c688b-139">**Değer** alanında, hareket için TDS hesaplamasında kullanılan toplam yüzde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c688b-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="c688b-140">Stopaj vergisi hareketleri sayfasındaki **Genel bakış**, **Genel** ve **Tutar** sekmelerindeki alanlar, TDS grubuna iliştirilmiş her TDS vergi kodu için hesaplanmış TDS tutarı ve düzeltilmiş TDS tutarı ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c688b-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
