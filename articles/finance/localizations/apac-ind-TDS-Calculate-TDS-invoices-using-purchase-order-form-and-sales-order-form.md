---
title: TDS faturalarını, satınalma siparişi formu ve satış siparişi formu kullanarak hesaplama
description: Bu konuda, çeşitli fatura türlerinde Kaynakta Kesilen Vergi (TDS) hesaplamaya yönelik adımlar listelenmektedir.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023648"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="371be-103">TDS faturalarını, satınalma siparişi formu ve satış siparişi formu kullanarak hesaplama</span><span class="sxs-lookup"><span data-stu-id="371be-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="371be-104">Bu konu, **Satınalma siparişi**, **Satınalma günlüğü**, **Paket sipariş** ve **Satış siparişi** sayfalarını kullanan çeşitli fatura türlerinde Kaynakta Kesilen Vergi (TDS) hesaplanmasında kullanılan adımları listeler.</span><span class="sxs-lookup"><span data-stu-id="371be-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="371be-105">Listelenen sayfayı kullanarak bir satınalma siparişi, satınalma günlüğü, paket satınalma siparişi veya bir satış siparişi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="371be-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="371be-106">Gerekli ayrıntıları girin.</span><span class="sxs-lookup"><span data-stu-id="371be-106">Enter the required details.</span></span>

2. <span data-ttu-id="371be-107">Satıcı veya müşterinin değerlendirilen yapısını görüntülemek için **Kurulum** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="371be-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="371be-108">Bu bilgiler **Değerlendirilenin yapısı** alanında, **Stopaj vergisi grubu** alan grubu altında listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="371be-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="371be-109">**TDS grubu** alanında, satıcı veya müşteri için tanımlanan varsayılan TDS grubunu görüntüleyin veya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="371be-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="371be-110">**TDS grubu** alanında TDS grubunu seçtiğinizde, **TCS grubu** alanı kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="371be-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="371be-111">TDS yalnızca, **Tüm satıcılar** veya **Tüm müşteriler** sayfasındaki satıcı veya müşteri için **Stopaj vergisini hesapla** onay kutusu seçilmişse hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="371be-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="371be-112">**Satırlar** sekmesinde madde satırları oluşturun ve gerekli ayrıntıları girin.</span><span class="sxs-lookup"><span data-stu-id="371be-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="371be-113">Başlık düzeyinde tanımlanan TDS grubunu görüntülemek veya değiştirmek için **Kurulum** sekmesini (satır düzeyi) seçin.</span><span class="sxs-lookup"><span data-stu-id="371be-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="371be-114">TDS grubu, **Stopaj vergisi grubu** alan grubunun altında olan **TDS grubu** alanında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="371be-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="371be-115">**Vergi bilgileri** sekmesini seçin ve ardından bu alanda görüntülenen şirket adı için ayarlanmış alternatif adresleri seçin.</span><span class="sxs-lookup"><span data-stu-id="371be-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="371be-116">Şirket adı, **Şirket bilgileri** alan grubunun altında bulunan **Ad** alanında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="371be-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="371be-117">Seçilen şirket adının TAN değeri, **Stopaj vergisi** alan grubunun altında **Vergi Hesap Numarası** (**TAN**) alanında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="371be-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="371be-118">**Geçici stopaj vergisi hareketleri** sayfasını açmak için **Stopaj vergisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="371be-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="371be-119">**Geçici stopaj vergisi hareketleri** sayfasının üst bölmesinde aşağıdaki alanları görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="371be-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="371be-120">**Stopaj** **vergisinin** **toplam** **tutar** **değeri**- TDS grubunun hareketleri için hesaplanan toplam TDS.</span><span class="sxs-lookup"><span data-stu-id="371be-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="371be-121">**Değer** -Hareket için TDS hesaplamasında kullanılan toplam yüzde.</span><span class="sxs-lookup"><span data-stu-id="371be-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="371be-122">Toplam yüzde, TDS grubuna iliştirilmiş TDS vergi kodları için tanımlanan formüle dayanır.</span><span class="sxs-lookup"><span data-stu-id="371be-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="371be-123">**Düzeltilmiş stopaj vergisi tutarı** - TDS grubundaki tüm vergi kodları için toplam düzeltilmiş TDS tutarı.</span><span class="sxs-lookup"><span data-stu-id="371be-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="371be-124">**TDS** - Seçilirse, hareketle bir TDS grubu ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="371be-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="371be-125">**Geçici stopaj vergisi hareketleri** sayfasındaki **Genel bakış**, **Genel** ve **Düzeltme** sekmelerindeki alanlar, TDS grubuna iliştirilmiş her TDS vergi kodu için hesaplanmış TDS tutarı ve düzeltilmiş TDS tutarı ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="371be-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="371be-126">**Eşik** sayfasını açmak için **Eşik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="371be-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="371be-127">Bu sayfada, belirli bir TDS vergi koduna ilişkilendirilmiş TDS vergi bileşeni için tanımlanan eşik sınırını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="371be-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="371be-128">**Formül tasarımcısı** sayfasını açmak için **Formül tasarımcısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="371be-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="371be-129">Bu sayfada, belirli bir TDS vergi kodu için tanımlanan formülü görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="371be-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="371be-130">Faturayı deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="371be-130">Post the invoice.</span></span> <span data-ttu-id="371be-131">Satınalma faturalarında hesaplanan TDS tutarı, borç hesabına nakledilir ve satış faturalarında hesaplanan TDS tutarı, TDS grubundaki her bir TDS vergi kodu için tanımlanan alacak hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="371be-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="371be-132">TDS vergi kodları için borç hesapları veya alacak hesapları **Stopaj vergisi kodları** sayfasında tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="371be-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="371be-133">**Stopaj vergisi hareketleri** sayfasını açmak **Sorgu** düğmesi **> Fatura > Deftere nakledilen stopaj vergisi** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="371be-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="371be-134">**Değer** alanında, hareket için TDS hesaplamasında kullanılan toplam yüzdeyi görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="371be-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="371be-135">**Stopaj vergisi hareketleri** sayfasındaki **Genel bakış**, **Genel** ve **Tutar** sekmelerindeki alanlar, hareket için hesaplanan TDS bilgilerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="371be-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="371be-136">TDS grubuna iliştirilmiş her TDS vergi kodu için TDS hesaplama bilgilerini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="371be-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
