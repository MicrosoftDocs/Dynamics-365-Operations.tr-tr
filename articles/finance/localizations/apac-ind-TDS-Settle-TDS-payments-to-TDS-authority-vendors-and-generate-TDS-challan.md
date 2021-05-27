---
title: TDS yetkili satıcılarına TDS ödemelerini kapatma ve TDS irsaliyesi oluşturma
description: Bu konu, TDS yetkili satıcılarına yapılan Kaynakta Kesilen Vergi (TDS) ödemelerinin nasıl kapatılacağını açıklar.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023665"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a><span data-ttu-id="e70d8-103">TDS yetkili satıcılarına TDS ödemelerini kapatma ve TDS irsaliyesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e70d8-103">Settle TDS payments to TDS authority vendors and generate TDS challan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e70d8-104">Bu konu, TDS yetkili satıcılarına yapılan Kaynakta Kesilen Vergi (TDS) ödemelerinin nasıl kapatılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="e70d8-104">This topic explains how to settle Tax Deducted at Source (TDS) payments to TDS authority vendors.</span></span>

1. <span data-ttu-id="e70d8-105">**Borç hesapları \> Ödemeler \> Satıcı ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-105">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>

    <span data-ttu-id="e70d8-106">[![Satıcı ödeme günlüğü sayfası](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span><span class="sxs-lookup"><span data-stu-id="e70d8-106">[![Vendor payment journal page](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span></span>

2. <span data-ttu-id="e70d8-107">**Satıcı ödeme günlüğü** sayfasında, günlük satırı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-107">On the **Vendor payment journal** page, select **New** to create a journal line.</span></span>
3. <span data-ttu-id="e70d8-108">**Hesap** alanında adına TDS ödemelerinin kapatılacağı TDS yetkili satıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-108">In the **Account** field, select the TDS authority vendor to settle TDS payments to.</span></span>
4. <span data-ttu-id="e70d8-109">TDS yetkili satıcısı için kapatılan TDS hareketlerini görüntüleyebileceğiniz **Kapatma hareketleri** sayfasını açmak için **Kapatma hareketleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-109">Select **Settlement transactions** to open the **Settlement transactions** page, where you can view the settled TDS transactions for the TDS authority vendor.</span></span>

    <span data-ttu-id="e70d8-110">Bir kapatma dönemi için kapatılan TDS hareketleri aşağıdaki şekilde görüntülenir:</span><span class="sxs-lookup"><span data-stu-id="e70d8-110">The settled TDS transactions for a settlement period are shown in the following way:</span></span>

    - <span data-ttu-id="e70d8-111">Değerlendirilen kategori yapısı **Şirket** olan TDS hareketleri bir hareket satırı olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-111">TDS transactions where the nature of assessee category is **Company** are shown as one transaction line.</span></span>
    - <span data-ttu-id="e70d8-112">Değerlendirilen kategori hapısı **HUF**, **Firma**, **Birey**, **AOP**, **BOI**, **Yerel makam** veya **Diğer** olan TDS hareketleri bir hareket satırı olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-112">TDS transactions where the nature of assessee category is **HUF**, **Firm**, **Individual**, **AOP**, **BOI**, **Local authority**, or **Others** are shown as one transaction line.</span></span>
    - <span data-ttu-id="e70d8-113">**Tutar** alanı, TDS yetkili satıcısına ödenmesi gereken toplam TDS tutarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-113">The **Amount** field shows the total TDS amount that is due to be paid to the TDS authority vendor.</span></span>

5. <span data-ttu-id="e70d8-114">Kapatma kaydı için dahil edilen farklı TDS hareketlerini görüntülemek için **Stopaj vergisi hareketleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-114">Select **Withholding tax transactions** to view the different TDS transactions that are included for the settlement record.</span></span> <span data-ttu-id="e70d8-115">Bu sayfadaki kapatma dönemine ait kapatma işlemine dahil edilen her TDS hareketinin bölünmesini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e70d8-115">You can view the split of each TDS transaction that has been included in the settlement process for the settlement period on this page.</span></span>
6. <span data-ttu-id="e70d8-116">**Genel bakış** sekmesinde, TDS yetkili satıcısına kapatılacak TDS hareketlerinin **İşaretle** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-116">On the **Overview** tab, select the **Mark** check box for the TDS transactions to settle to the TDS authority vendor.</span></span>

    <span data-ttu-id="e70d8-117">**Genel bakış** sekmesi, her açık TDS hareketiyle ilgili olarak aşağıdaki bilgileri gösterir:</span><span class="sxs-lookup"><span data-stu-id="e70d8-117">The **Overview** tab shows the following information for each open TDS transaction:</span></span>

    - <span data-ttu-id="e70d8-118">**Tarih** – TDS hareketi tarihi.</span><span class="sxs-lookup"><span data-stu-id="e70d8-118">**Date** – The TDS transaction date.</span></span>
    - <span data-ttu-id="e70d8-119">**Fiş** – Fiş numarası.</span><span class="sxs-lookup"><span data-stu-id="e70d8-119">**Voucher** – The voucher number.</span></span>
    - <span data-ttu-id="e70d8-120">**Kaynak** – TDS hareketinin içinde deftere nakledildiği modül.</span><span class="sxs-lookup"><span data-stu-id="e70d8-120">**Source** – The module that the TDS transaction is posted in.</span></span>
    - <span data-ttu-id="e70d8-121">**Satıcı/Müşteri** – TDS'nin kesildiği satıcı veya müşteri hesap numarası.</span><span class="sxs-lookup"><span data-stu-id="e70d8-121">**Vendor/Customer** – The vendor or customer account number that the TDS is deducted from.</span></span>
    - <span data-ttu-id="e70d8-122">**Kesinti yapılan kişi/tarafın adı** – TDS'nin kesildiği satıcı veya müşterinin adı.</span><span class="sxs-lookup"><span data-stu-id="e70d8-122">**Name of deductee/party** – The name of the vendor or customer that the TDS is deducted from.</span></span>
    - <span data-ttu-id="e70d8-123">**Değerlendirilen yapısı** – Kesinti yapılan tarafın ait olduğu değerlendirilen kategorisi yapısı.</span><span class="sxs-lookup"><span data-stu-id="e70d8-123">**Nature of assessee** – The nature of assessee category that the deductee belongs to.</span></span>
    - <span data-ttu-id="e70d8-124">**Tutar** – TDS'nin üzerinde hesaplandığı fatura tutarı.</span><span class="sxs-lookup"><span data-stu-id="e70d8-124">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="e70d8-125">**Vergi tutarı** – Hareket için hesaplanan TDS tutarı.</span><span class="sxs-lookup"><span data-stu-id="e70d8-125">**Tax amount** – The TDS amount that was calculated for the transaction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e70d8-126">TDS yetkili satıcısına kapatılmaması gereken tüm TDS hareketleriyle ilgili **İşaret** onay kutusunu kaldırın.</span><span class="sxs-lookup"><span data-stu-id="e70d8-126">Clear the **Mark** check box for any TDS transactions that should not be settled to the TDS authority vendor.</span></span>

    <span data-ttu-id="e70d8-127">**Genel** sekmesinde, **PAN** alanı kesinti yapılan tarafın kalıcı hesap numarasını (PAN) görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e70d8-127">On the **General** tab, the **PAN** field shows the permanent account number (PAN) of the deductee.</span></span> <span data-ttu-id="e70d8-128">**Tarih** alanı TDS hesaplamasının tarihini ve **Değer** alanı, TDS hesaplaması için kullanılan toplam yüzdeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-128">The **Date** field shows the date of the TDS calculation, and the **Value** field shows the total percentage that was used for the TDS calculation.</span></span>

7. <span data-ttu-id="e70d8-129">TDS hareketiyle ilgili fiş girişlerini görüntülemek için **Fiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-129">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
8. <span data-ttu-id="e70d8-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e70d8-130">Close the page.</span></span>
10. <span data-ttu-id="e70d8-131">Belirli bir TDS vergi koduyla ilgili her TDS vergi bileşeni için hesaplanan TDS'yi görüntüleyebileceğiniz **Stopaj vergisi bileşenleri** sayfasını açmak için **Stopaj vergisi bileşenleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-131">Select **Withholding tax components** to open the **Withholding tax components** page, where you can view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>

    <span data-ttu-id="e70d8-132">**Genel bakış** sekmesinde, **Vergi bileşeni** alanı hareket için kullanılan TDS vergi bileşenini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-132">On the **Overview** tab, the **Tax component** field shows the TDS tax component that was used for the transaction.</span></span> <span data-ttu-id="e70d8-133">**Tutar** alanı, TDS vergi bileşeni için hesaplanan TDS tutarını baz para birimi cinsinden gösterir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-133">The **Amount** field shows the TDS amount that was calculated for the TDS tax component, in the base currency.</span></span> <span data-ttu-id="e70d8-134">**Birikmiş tutar** alanı, tüm kapatılan hareketleriyle ilgili olarak TDS vergisi bileşeni için hesaplanan toplam TDS tutarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-134">The **Accumulated amount** field shows the total TDS amount that was calculated for the TDS tax component for all settled transactions.</span></span>

    <span data-ttu-id="e70d8-135">**Tutar** sekmesinde, **Varsayılan para birimi** bölümü, TDS vergisi bileşeni için hesaplanan TDS tutarını varsayılan para birimi cinsinden gösterir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-135">On the **Amount** tab, the **Default currency** section shows the TDS amount that was calculated for the TDS tax component, in the default currency.</span></span> <span data-ttu-id="e70d8-136">**İkincil para birimi** bölümü, tutarı ikincil para birimi cinsinden gösterir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-136">The **Secondary currency** section shows the amount in the secondary currency.</span></span>

11. <span data-ttu-id="e70d8-137">**Stopaj vergisi bileşenleri** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="e70d8-137">Close the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="e70d8-138">**Açık hareket düzenlemesi** sayfasındaki **Tutar** alanında, kapatma dönemi için TDS yetkili satıcısına kapatılacak toplam tutarın güncelleştirilip güncelleştirilmediğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-138">On the **Open transaction editing** page, in the **Amount** field, notice that the total amount to settle to the TDS authority vendor for the settlement period is updated.</span></span>
13. <span data-ttu-id="e70d8-139">Farklı TDS kapatma dönemlerindeki TDS hareketlerini, TDS yetkili satıcısına kapatmak için harekete ait **İşaret** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-139">To settle the TDS transactions of different TDS settlement periods to the TDS authority vendor, select the **Mark** check box for the transactions.</span></span>
14. <span data-ttu-id="e70d8-140">**Açık hareket düzenleme** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="e70d8-140">Close the **Open transaction editing** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e70d8-141">**Stopaj vergisi hareketleri** sayfasında kapatılmak üzere yalnızca birkaç hareket seçilmişse, seçili hareketlerin toplam TDS tutarı **Açık hareket düzenleme** sayfasındaki **Düzeltme** alanında güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-141">If only a few transactions are selected for settlement on the **Withholding tax transactions** page, the total TDS amount of the selected transactions is updated in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="e70d8-142">Düzeltme tutarı, **Günlük fişi** sayfasındaki günlük satırında güncelleştirilir ve **Açık hareket düzenleme** sayfası kapatılır.</span><span class="sxs-lookup"><span data-stu-id="e70d8-142">The correction amount is updated on the journal line on the **Journal voucher** page, and the **Open transaction editing** page is closed.</span></span>

    <span data-ttu-id="e70d8-143">**Günlük fişi** sayfasında, **Borç** alanı, TDS yetkili satıcısına ödenecek toplam tutarı gösterir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-143">On the **Journal voucher** page, the **Debit** field shows the total amount to pay to the TDS authority vendor.</span></span>

15. <span data-ttu-id="e70d8-144">Mahsup hesap ayrıntılarını girin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-144">Enter the offset account details.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e70d8-145">TDS hareketlerinin farklı Vergi Hesap Numaraları (TAN'lar) olması durumunda, **Günlük fişi** sayfasında günlük satırları TAN başına oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e70d8-145">If TDS transactions have different Tax Account Numbers (TANs), journal lines are created per TAN on the **Journal voucher** page.</span></span>

16. <span data-ttu-id="e70d8-146">**Ödeme ücreti** sekmesinde, **Ücret kodu** alanında, TDS yetkili satıcısına yapılan gecikmeli ödemeler için ödeme ücreti almak üzere ücret tipi **Faiz** veya **Diğer** olan bir ücret kimliği seçin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-146">On the **Payment fee** tab, in the **Fee ID** field, select a fee ID that has a fee type of **Interest** or **Others** to charge the payment fee for delayed payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="e70d8-147">**Vergi bilgileri** sekmesinde, **Şirket bilgileri** bölümünde, **Ad** alanında şirket adı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-147">On the **Tax information** tab, in the **Company information** section, the **Name** field shows the company name.</span></span> <span data-ttu-id="e70d8-148">**Stopaj vergisi** bölümünde, **Vergi Hesap Numarası (TAN)** alanı hareket satırına iliştirilen TAN'ı gösterir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-148">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the TAN that is attached to the transaction line.</span></span>

17. <span data-ttu-id="e70d8-149">Günlüğü doğrulayın ve deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-149">Validate and post the journal.</span></span>
18. <span data-ttu-id="e70d8-150">Harekete ait irsaliye ayrıntılarını girmek için **Stopaj vergisi \> İrsaliye bilgileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-150">Select **Withholding tax \> Challan information** to enter the challan details for the transaction.</span></span>

    <span data-ttu-id="e70d8-151">**Fiş** alanı, hareketin fiş numarasını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e70d8-151">The **Voucher** field shows the voucher number of the transaction.</span></span>
    
19. <span data-ttu-id="e70d8-152">TDS tutarı, defter girişi kullanılarak yatırılmışsa **Defter girişiyle yatırılan TDS** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-152">Select the **TDS deposited by book entry** check box if the TDS amount is deposited by using book entry.</span></span>
20. <span data-ttu-id="e70d8-153">**İrsaliye numarası** alanına, TDS yetkili satıcısına yapılacak ödemeyi gerçekleştirmek için kullanılan irsaliye numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-153">In the **Challan number** field, enter the challan number that is used to make the payment to the TDS authority vendor.</span></span>
21. <span data-ttu-id="e70d8-154">**Tarih** alanına irsaliye tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-154">In the **Date** field, enter the challan date.</span></span>
22. <span data-ttu-id="e70d8-155">**Banka adı** alanında, TDS yetkili satıcısına ödenecek TDS tutarının yatırılması gereken bankanın adını seçin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-155">In the **Bank name** field, select the name of the bank that the TDS amount that is payable to the TDS authority vendor should be deposited to.</span></span> <span data-ttu-id="e70d8-156">Bu alan, TDS yetkili satıcısı için **Borç hesapları \>Tüm satıcılar \> Kurulum \> Banka hesapları**'nda kurulan tüm banka hesaplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="e70d8-156">This field lists all the bank accounts that were set up for the TDS authority vendor at **Accounts payable \> All vendors \> Set up \> Bank accounts**.</span></span>
23. <span data-ttu-id="e70d8-157">**BSR kodu** alanında, bankanın Temel İstatistik İade (BSR) kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-157">In the **BSR code** field, enter the Basic Statistical Return (BSR) code of the bank.</span></span>
24. <span data-ttu-id="e70d8-158">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e70d8-158">Close the page.</span></span>

### <a name="example"></a><span data-ttu-id="e70d8-159">Örnek</span><span class="sxs-lookup"><span data-stu-id="e70d8-159">Example</span></span>

<span data-ttu-id="e70d8-160">Dönemsel TDS kapatma işlemi kullanılarak 01/04/2009 döneminin **Kira** TDS bileşen grubu kapatılmış.</span><span class="sxs-lookup"><span data-stu-id="e70d8-160">The period 04/01/2009 is settled for the **Rent** TDS component group by using the periodic TDS settlement process.</span></span> <span data-ttu-id="e70d8-161">Toplam TDS tutarı olan 141.625,00 değeri, TDS kapatma dönemi için TDS satıcısı yetkili hesabına nakledilmiş.</span><span class="sxs-lookup"><span data-stu-id="e70d8-161">The total TDS amount of 141,625.00 is posted to the TDS vendor authority account for the TDS settlement period.</span></span> <span data-ttu-id="e70d8-162">Bu tutarı, TDS yetkili satıcısının **Açık hareket düzenleme** sayfasındaki **Tutar** alanında görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e70d8-162">You can view this amount in the **Amount** field on the **Open transaction editing** page for the TDS authority vendor.</span></span>

<span data-ttu-id="e70d8-163">Dönem için kapatılan farklı TDS hareketlerini görüntülemek için **Stopaj vergisi hareketleri**'ni seçerseniz, aşağıdaki bilgiler görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-163">If you select **Withholding tax transactions** to view the different TDS transactions that were settled for the period, the following information is shown.</span></span>

| <span data-ttu-id="e70d8-164">TDS tutarı</span><span class="sxs-lookup"><span data-stu-id="e70d8-164">TDS amount</span></span> |
|------------|
| <span data-ttu-id="e70d8-165">16,995.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-165">16,995.00</span></span>  |
| <span data-ttu-id="e70d8-166">22,660.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-166">22,660.00</span></span>  |
| <span data-ttu-id="e70d8-167">28,325.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-167">28,325.00</span></span>  |
| <span data-ttu-id="e70d8-168">16,995.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-168">16,995.00</span></span>  |
| <span data-ttu-id="e70d8-169">28,325.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-169">28,325.00</span></span>  |
| <span data-ttu-id="e70d8-170">16,995.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-170">16,995.00</span></span>  |
| <span data-ttu-id="e70d8-171">11,330.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-171">11,330.00</span></span>  |

<span data-ttu-id="e70d8-172">Belirli bir TDS tutarı için, belirli bir TDS vergi koduyla ilgili her TDS vergi bileşeni için hesaplanan TDS'yi görüntülemek için **Stopaj vergisi bileşenleri**'ni seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e70d8-172">For a specific TDS amount, you can select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span> <span data-ttu-id="e70d8-173">Bu örnekte, 16.995,00 değerindeki TDS tutarı için **Stopaj vergisi bileşenleri**'ni seçtiniz.</span><span class="sxs-lookup"><span data-stu-id="e70d8-173">For this example, you select **Withholding tax components** for the TDS amount 16,995.00.</span></span> <span data-ttu-id="e70d8-174">Hareket için bileşen başına hesaplanan vergi tutarı görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-174">The tax amount that was calculated per component for the transaction is shown.</span></span>

| <span data-ttu-id="e70d8-175">Vergi bileşeni</span><span class="sxs-lookup"><span data-stu-id="e70d8-175">Tax component</span></span> | <span data-ttu-id="e70d8-176">Tutar</span><span class="sxs-lookup"><span data-stu-id="e70d8-176">Amount</span></span>    | <span data-ttu-id="e70d8-177">Kümülatif tutar</span><span class="sxs-lookup"><span data-stu-id="e70d8-177">Accumulated amount</span></span> |
|---------------|-----------|--------------------|
| <span data-ttu-id="e70d8-178">TDS</span><span class="sxs-lookup"><span data-stu-id="e70d8-178">TDS</span></span>           | <span data-ttu-id="e70d8-179">1,5000.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-179">1,5000.00</span></span> | <span data-ttu-id="e70d8-180">125,000.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-180">125,000.00</span></span>         |
| <span data-ttu-id="e70d8-181">Ek maliyet</span><span class="sxs-lookup"><span data-stu-id="e70d8-181">Surcharge</span></span>     | <span data-ttu-id="e70d8-182">1,500.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-182">1,500.00</span></span>  | <span data-ttu-id="e70d8-183">12,500.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-183">12,500.00</span></span>          |
| <span data-ttu-id="e70d8-184">PE-Cess</span><span class="sxs-lookup"><span data-stu-id="e70d8-184">PE-Cess</span></span>       | <span data-ttu-id="e70d8-185">330.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-185">330.00</span></span>    | <span data-ttu-id="e70d8-186">2,750.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-186">2,750.00</span></span>           |
| <span data-ttu-id="e70d8-187">SHE Cess</span><span class="sxs-lookup"><span data-stu-id="e70d8-187">SHE Cess</span></span>      | <span data-ttu-id="e70d8-188">165.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-188">165.00</span></span>    | <span data-ttu-id="e70d8-189">1,375.00</span><span class="sxs-lookup"><span data-stu-id="e70d8-189">1,375.00</span></span>           |

<span data-ttu-id="e70d8-190">**Stopaj vergi hareketleri** sayfasında TDS tutarları olarak yalnızca 16.995,00, 22.660,00 ve 28.325,00 değerlerini seçtiyseniz **Açık hareket düzenleme** sayfasında **Düzeltme** alanında kapatmanın toplam tutarı olarak **67.980,00** gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-190">If you selected only the TDS amounts 16,995.00, 22,660.00, and 2,8325.00 for settlement on the **Withholding tax transactions** page, the total amount for settlement is shown as **67,980.00** in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="e70d8-191">Bu hareket kapatılmak üzere işaretlenmişse ve **Açık hareket düzenleme** sayfası kapatılırsa, **67.980,00** tutarı, **Günlük fişi** sayfasındaki **Borç** alanında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-191">If this transaction is marked for settlement, and the **Open transaction editing** page is closed, the amount **67,980.00** is shown in the **Debit** field on the **Journal voucher** page.</span></span>

<span data-ttu-id="e70d8-192">Artık günlüğü deftere nakledebilir ve TDS irsaliyesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e70d8-192">You can now post the journal and generate the TDS challan.</span></span>

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a><span data-ttu-id="e70d8-193">TDS yetkili satıcılarına yapılan avans ödemesi düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="e70d8-193">Adjustment of advance payments that are made to TDS authority vendors</span></span>

<span data-ttu-id="e70d8-194">TDS yetkili satıcısına yapılan bir avans ödemesini gerçek bir ödemeye düzeltmek için **Borç hesapları \> Satıcılar \> Tüm satıcılar \> Hareketleri düzenleme**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="e70d8-194">To adjust an advance payment that was made to the TDS authority vendor to an actual payment, go to **Accounts payable \> Vendors \> All vendors \> Transactions editing**.</span></span> <span data-ttu-id="e70d8-195">Yapılan gerçek ödeme, avans ödemesini aşıyorsa hareket için iki irsaliye numarası oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e70d8-195">If the actual payment that is made exceeds the advance payment, two challan numbers are generated for the transaction.</span></span> <span data-ttu-id="e70d8-196">Ancak, TDS sorgusunda yalnızca ilk irsaliye numarası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e70d8-196">However, only the first challan number is shown in the TDS inquiry.</span></span>
