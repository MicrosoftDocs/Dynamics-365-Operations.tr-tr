---
title: TDS vergi kodlarını, TDS vergi gruplarına ekle ve TDS hesaplama formülünü belirle
description: Bu konu, Kaynakta Kesilen Vergi (TDS) gruplarının nasıl kurulduğunu ve TDS vergi kodlarını TDS vergi gruplarına ilişkilendirmeyi açıklamaktadır. Bir TDS vergi grubu için TDS'yi hesaplamak için, gruba iliştirilen TDS vergi kodlarının formülünü belirlemeniz gerekir.
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
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023667"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="6e864-104">TDS vergi kodlarını, TDS vergi gruplarına ekle ve TDS hesaplama formülünü belirle</span><span class="sxs-lookup"><span data-stu-id="6e864-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e864-105">Bu konu, Kaynakta Kesilen Vergi (TDS) gruplarının nasıl kurulduğunu ve TDS vergi kodlarını TDS vergi gruplarına ilişkilendirmeyi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="6e864-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="6e864-106">Bir TDS vergi grubu için TDS'yi hesaplamak için, gruba iliştirilen TDS vergi kodlarının formülünü belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6e864-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="6e864-107">TDS vergi grubunu ayarlamak, TDS vergi kodlarını gruba iliştirmek ve TDS'yi hesaplama formülünü belirlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6e864-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="6e864-108">**Vergi \> Dolaylı vergiler \> Stopaj vergisi \> Stopaj vergisi grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="6e864-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="6e864-109">[![Stopaj vergisi grupları sayfası](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="6e864-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="6e864-110">Eylem bölmesinde, TDS için stopaj vergisi grubu oluşturmak üzere **Yeni**'yi seçin ve gerekli ayrıntıları girin.</span><span class="sxs-lookup"><span data-stu-id="6e864-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="6e864-111">**Vergi türü** alanında **TDS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6e864-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="6e864-112">**Kurulum** hızlı sekmesinde satır oluşturmak için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6e864-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="6e864-113">**Stopaj vergisi kodu** alanında TDS vergi grubu için TDS vergi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6e864-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="6e864-114">**Stopaj vergisi adı** alanı, TDS vergi kodunun adını ve **Değer** alanı değeri gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e864-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="6e864-115">TDS hareketlerinde TDS vergi koduna iliştirilmiş TDS vergi bileşeni için tanımlanan eşik sınırını ve istisna eşik sınırını yok saymak için **Eşiği dikkate alma** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6e864-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="6e864-116">Vergi grubunun hareketlerde hesaplanmasını önlemek için, **Muaf** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6e864-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="6e864-117">Eylem bölmesinde, bu TDS vergi grubunun TDS hesaplama formülünü belirleyebilmek için formül tasarımcısını açmak üzere **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6e864-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="6e864-118">**Tasarımcı** sayfasında, **Vergiler** sekmesi, TDS vergi grubu için seçilen TDS vergi kodlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e864-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="6e864-119">[![Tasarımcı sayfası](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="6e864-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="6e864-120">Bir satır oluşturmak için, **Hesaplama** sekmesinde **Alt+N**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6e864-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="6e864-121">**Kimlik** alanı, TDS hesaplaması için otomatik olarak oluşturulan öncelik kimliğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e864-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="6e864-122">**Vergi kodu** alanında formül için belirlenecek TDS vergi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6e864-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="6e864-123">TDS vergi grubu için seçilen tüm TDS vergisi kodları, bu alanda seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="6e864-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="6e864-124">**Vergilendirilebilir esas** alanında, TDS hesaplamasının esasını seçin:</span><span class="sxs-lookup"><span data-stu-id="6e864-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="6e864-125">**Brüt tutar** – TDS'yi, vergi kodu için belirlenen hesaplama ifadesini kullanarak, brüt hareket tutarına (yani fatura tutarı) göre hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="6e864-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="6e864-126">**Brüt tutar hariç** – TDS'yi, vergi kodu için tanımlanan hesaplama ifadesine göre hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="6e864-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6e864-127">Öncelik kimliği **1** olan TDS vergi kodlarının **Vergilendirilebilir esas** alanı, **Brüt tutar hariç** olarak ayarlanamaz.</span><span class="sxs-lookup"><span data-stu-id="6e864-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="6e864-128">TDS hesaplaması, TDS vergi grubuna iliştirilmiş her vergi kodu için **Hesaplama ifadesi** alanında belirlenen formüle dayanır.</span><span class="sxs-lookup"><span data-stu-id="6e864-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="6e864-129">**Hesaplama ifadesi** alanında seçili TDS vergi koduna ait hesaplama ifadesini girmek için artı işareti (**+**), eksi işareti (**-**), çarpma işareti (**\**_) veya bölme işareti (_*/**) düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6e864-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6e864-130">Öncelik kodu **1** olan TDS vergi kodu için herhangi bir hesaplama ifadesi tanımlanamaz.</span><span class="sxs-lookup"><span data-stu-id="6e864-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="6e864-131">Bu TDS vergi kodu için **Hesaplama ifadesi** alanında hesaplama ifadesini tanımlamak için, **Vergiler** sekmesinde mevcut olan TDS vergi kodlarını ekleyin. **Hesaplama ifadesi** alanında TDS vergi kodlarını eklemek için aşağıdaki yöntemlerden birini kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="6e864-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="6e864-132">Gerekli vergi kodunu **Vergiler** sekmesinden **Hesaplama ifadesi** alanına sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="6e864-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="6e864-133">**Vergiler** sekmesinde gerekli vergi koduna çift dokunun (veya çift tıklayın).</span><span class="sxs-lookup"><span data-stu-id="6e864-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="6e864-134">**Vergiler** sekmesinde gerekli vergi kodunu seçin ve basılı tutun (veya sağ tıklayın) ve sonra **Vergi kodu ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6e864-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6e864-135">Her TDS vergi kodundan önce bir hesaplama ifadesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6e864-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="6e864-136">Hesaplama ifadesine eklenen TDS vergi kodları köşeli ayraç (\[...\]) içinde görünür.</span><span class="sxs-lookup"><span data-stu-id="6e864-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="6e864-137">**Hesaplama ifadesi** alanında vergi kodu için tanımlanan hesaplama ifadesini temizlemek için **C** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6e864-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="6e864-138">**Hesaplama** sekmesindeki bir kaydı silmek için , **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6e864-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="6e864-139">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6e864-139">Close the page.</span></span>
