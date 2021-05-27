---
title: TDS vergi türü için stopaj vergisi raporlama kodlarını ayarlama
description: Stopaj vergisi raporlama kodları, Kaynakta Kesilen Vergi (TDS) için Form 26Q ve Form 27Q raporlarını oluşturmak üzere kullanılır. Bu konu, TDS raporlama kodlarını ayarlamak için stopaj vergisi raporlama kodları adımlarının nasıl ayarlanacağını açıklar.
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
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023668"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="66c2c-104">TDS vergi türü için stopaj vergisi raporlama kodlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="66c2c-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66c2c-105">Stopaj vergisi raporlama kodları, Kaynakta Kesilen Vergi (TDS) için Form 26Q ve Form 27Q raporlarını oluşturmak üzere kullanılır.</span><span class="sxs-lookup"><span data-stu-id="66c2c-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="66c2c-106">Bu konu, TDS raporlama kodlarını ayarlamak için stopaj vergisi raporlama kodları adımlarının nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="66c2c-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="66c2c-107">**Vergi \> Kurulum \> Stopaj vergisi \> Stopaj vergisi raporlama kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="66c2c-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="66c2c-108">[![Stopaj vergisi raporlama kodları sayfası](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="66c2c-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="66c2c-109">TDS vergi türü için stopaj vergisi raporlama kodlarını belirlemek üzere **Vergi türü** alanında **TDS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="66c2c-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="66c2c-110">**Stopaj vergisi bileşeni** alanında, adına stopaj vergisi raporlama kodunu tanımladığınız TDS bileşenini seçin.</span><span class="sxs-lookup"><span data-stu-id="66c2c-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="66c2c-111">**Stopaj vergisi bileşen grubu** alanı, tanımladığınız TDS bileşeni için tanımlanan TDS bileşen grubunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="66c2c-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="66c2c-112">**Genel** hızlı sekmesindeki **Bölüm kodu** alanı, TDS bileşen grubuna iliştirilmiş bölüm kodunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="66c2c-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="66c2c-113">**Genel** hızlı sekmesindeki **Raporlama kodu** alanında TDS raporlama kodunu seçin:</span><span class="sxs-lookup"><span data-stu-id="66c2c-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="66c2c-114">TDS</span><span class="sxs-lookup"><span data-stu-id="66c2c-114">TDS</span></span>
    - <span data-ttu-id="66c2c-115">TCS</span><span class="sxs-lookup"><span data-stu-id="66c2c-115">TCS</span></span>
    - <span data-ttu-id="66c2c-116">Ek maliyet</span><span class="sxs-lookup"><span data-stu-id="66c2c-116">Surcharge</span></span>
    - <span data-ttu-id="66c2c-117">PE\_Cess</span><span class="sxs-lookup"><span data-stu-id="66c2c-117">PE\_Cess</span></span>
    - <span data-ttu-id="66c2c-118">SHE\_Cess</span><span class="sxs-lookup"><span data-stu-id="66c2c-118">SHE\_Cess</span></span>

5. <span data-ttu-id="66c2c-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="66c2c-119">Close the page.</span></span>
