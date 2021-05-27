---
title: TDS vergi türü için vergi bileşenlerini ayarlama
description: Bu konu, Kaynakta Kesilen Vergi (TDS) türü için stopaj vergisi bileşenlerinin nasıl ayarlanabileceğini açıklar. Ayrıca her TDS bileşeni için TDS'yi hesaplama amacıyla kullanılan eşik sınırının nasıl tanımlanacağını açıklar.
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023653"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="e26f4-104">TDS vergi türü için vergi bileşenlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="e26f4-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e26f4-105">Bu konu, Kaynakta Kesilen Vergi (TDS) türü için stopaj vergisi bileşenlerinin nasıl ayarlanabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="e26f4-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="e26f4-106">TDS bileşenleri şunlardır: TDS, ek talep, PE-Cess ve SHE Cess.</span><span class="sxs-lookup"><span data-stu-id="e26f4-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="e26f4-107">Bu konu ayrıca her TDS bileşeni için TDS'yi hesaplama amacıyla kullanılan eşiğin nasıl tanımlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="e26f4-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="e26f4-108">Ek olarak, her TDS bileşeni için TDS'yi hesaplamak üzere kullanılan bir istisna eşiği tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e26f4-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="e26f4-109">TDS bileşenlerini ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e26f4-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="e26f4-110">**Vergi \> Kurulum \> Stopaj vergisi \> Stopaj vergisi bileşenleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e26f4-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="e26f4-111">[![Stopaj vergisi bileşenleri sayfası](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="e26f4-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="e26f4-112">TDS vergi türü için stopaj vergisi bileşenlerini ayarlamak üzere **Vergi türü** alanında **TDS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e26f4-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="e26f4-113">Eylem bölmesinde, bir satır oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e26f4-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="e26f4-114">**Stopaj vergisi bileşeni** alanında, TDS bileşeni için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="e26f4-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="e26f4-115">**Stopaj vergisi bileşen grubu** alanında, TDS bileşeninin ekleneceği TDS stopaj vergisi bileşen grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e26f4-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="e26f4-116">**Genel** hızlı sekmesinde, **Açıklama** alanına TDS bileşeninin açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="e26f4-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="e26f4-117">Eylem Bölmesinde, **Eşik** sayfasını açmak için **Eşik** seçeneğini belirleyin; böylece TDS bileşeni için TDS'yi hesaplamak üzere kullanılacak eşiği tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e26f4-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="e26f4-118">Eşiğin uygulanabileceği dönemi tanımlamak için **Başlangıç tarihi** ve **Bitiş tarihi** alanlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="e26f4-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="e26f4-119">**Genel** hızlı sekmesinde, **Eşik** alanına TDS bileşeni için TDS hesaplamasında kullanılacak eşik tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="e26f4-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="e26f4-120">Vergi yalnızca, kümülatif fatura tutarı eşiği aştığında kaynakta kesilecektir.</span><span class="sxs-lookup"><span data-stu-id="e26f4-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="e26f4-121">Örneğin, eşik tutarı 10.000 ise kümülatif fatura tutarı 10.000'i aştığında (yani 10.001 veya daha fazla olduğunda) TDS hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="e26f4-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="e26f4-122">**İstisna eşik** alanında, TDS bileşeni için TDS hesaplamasında kullanılacak istisna eşik tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="e26f4-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="e26f4-123">Bir fatura satırında vergi yalnızca, tutar istisna eşiği aştığında kaynakta kesilecektir.</span><span class="sxs-lookup"><span data-stu-id="e26f4-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="e26f4-124">Örneğin, istisna eşik tutarı 5.000 ise, fatura satır tutarı 5.000 değerini aştığında (yani 5.001 veya daha fazla) TDS belirli bir fatura satırında hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="e26f4-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="e26f4-125">[![Eşik sayfası](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="e26f4-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="e26f4-126">İstisna eşik tutarı, eşik tutarına eşit veya tutardan daha az olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e26f4-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="e26f4-127">Kümülatif fatura tutarı, **Eşik** alanında belirtilen eşiği aşmasa bile, hareket tutarı istisna eşiği aşarsa vergi, bir hareket için kesilir.</span><span class="sxs-lookup"><span data-stu-id="e26f4-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="e26f4-128">**Stopaj vergisi bileşenleri** sayfasına dönmek için **Eşik** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="e26f4-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="e26f4-129">Eylem Bölmesinde, **Stopaj vergisi bileşenlerini kopyala** iletişim kutusunu açmak için **Kopyala**'yı seçerek bir TDS bileşen grubu için ayarlanmış olan TDS bileşenlerini başka bir TDS bileşen grubuna kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e26f4-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="e26f4-130">**Kaynak** alanında, TDS bileşenlerinin kopyalanmak için alınacağı TDS bileşen grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e26f4-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="e26f4-131">**Hedef** alanında, TDS bileşenlerinin kopyalanacağı stopaj vergisi bileşen grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e26f4-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e26f4-132">Her iki TDS bileşen grubuna eklenen ortak TDS bileşenleri kopyalanmaz.</span><span class="sxs-lookup"><span data-stu-id="e26f4-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="e26f4-133">**Stopaj vergisi bileşenleri** sayfasında diğer TDS bileşen grubu için TDS bileşenlerini kopyalamak ve oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e26f4-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="e26f4-134">[![Stopaj vergisi bileşenlerini kopyala iletişim kutusu](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="e26f4-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="e26f4-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e26f4-135">Close the page.</span></span>
