---
title: TDS vergi türü için stopaj vergisi kodlarını ayarlama
description: Bu konu, Kaynakta Kesilen Vergi (TDS) için vergi kodlarının nasıl ayarlanacağını açıklar.
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023670"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="41ef4-103">TDS vergi türü için stopaj vergisi kodlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="41ef4-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41ef4-104">Bu konu, Kaynakta Kesilen Vergi (TDS) için vergi kodlarının nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="41ef4-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="41ef4-105">**Vergi \> Dolaylı vergiler \> Stopaj vergisi \> Stopaj vergisi kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="41ef4-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="41ef4-106">[![Stopaj vergisi kodları sayfası](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="41ef4-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="41ef4-107">Eylem bölmesinde, TDS için stopaj vergisi kodu oluşturmak üzere **Yeni**'yi seçin ve gerekli ayrıntıları girin.</span><span class="sxs-lookup"><span data-stu-id="41ef4-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="41ef4-108">**Genel** hızlı sekmesinde, **Vergi türü** alanında, vergi kodunu TDS vergi kodu olarak sınıflandırmak için **TDS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="41ef4-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="41ef4-109">**Kapatma dönemi** alanında, TDS vergi kodunun TDS kapatma dönemini seçin.</span><span class="sxs-lookup"><span data-stu-id="41ef4-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="41ef4-110">**Ana hesap** alanında, TDS tutarının nakledileceği genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="41ef4-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="41ef4-111">**Alacak hesabı** alanında, satış hareketlerinde kesilen TDS tutarının nakledileceği alacak hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="41ef4-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="41ef4-112">**Kaynak** alanı otomatik olarak **Brüt tutarın yüzdesi** olarak ayarlanır ve değer değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="41ef4-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="41ef4-113">TDS vergi türünün vergi kodları için kaynak alanını **Net tutar yüzdesi** olarak ayarlayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="41ef4-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="41ef4-114">**Stopaj vergisi bileşeni** alanında, TDS vergi kodunun TDS vergi bileşenini seçin.</span><span class="sxs-lookup"><span data-stu-id="41ef4-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="41ef4-115">**Stopaj vergisi değerleri** sayfasını açmak için, Eylem Bölmesinde **Değerler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="41ef4-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="41ef4-116">**Başlangıç tarihi** alanında, TDS değerinin başlangıç tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="41ef4-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="41ef4-117">**Bitiş tarihi** alanında, bitiş tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="41ef4-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="41ef4-118">**Minimum limit**, **Üst limit** ve **Hariç tutma yüzdesi** alanları, TDS vergi türünün vergi kodlarında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="41ef4-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="41ef4-119">**Değer** alanına, TDS vergi kodunun TDS yüzdesini girin.</span><span class="sxs-lookup"><span data-stu-id="41ef4-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="41ef4-120">**Stopaj vergisi kodları** sayfasına dönmek için **Stopaj vergisi değerleri** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="41ef4-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="41ef4-121">**Stopaj vergisi kodları** sayfasındaki **Limitler** düğmesi, TDS vergi türüyle ilgili vergi kodları için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="41ef4-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="41ef4-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="41ef4-122">Close the page.</span></span>
