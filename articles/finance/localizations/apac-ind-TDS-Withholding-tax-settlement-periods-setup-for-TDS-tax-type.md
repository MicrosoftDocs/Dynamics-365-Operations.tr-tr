---
title: TDS vergi türü için stopaj vergisi kapatma dönemlerini ayarlama
description: Bu konu, Kaynakta Kesilen Vergi (TDS) kapatma dönemleri için kapatma dönemlerinin nasıl ayarlanabileceğini açıklar.
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023645"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="1279d-103">TDS vergi türü için stopaj vergisi kapatma dönemlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1279d-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1279d-104">Bu konu, Kaynakta Kesilen Vergi (TDS) kapatma dönemleri için kapatma dönemlerinin nasıl ayarlanabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="1279d-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="1279d-105">**Vergi \> Dolaylı vergiler \> Stopaj vergisi \> Stopaj vergisi kapatma dönemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1279d-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="1279d-106">[![Stopaj vergisi kapatma dönemleri sayfası](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="1279d-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="1279d-107">TDS vergi türü için stopaj vergisi kapatma dönemlerini ayarlamak üzere **Vergi türü** alanında **TDS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1279d-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="1279d-108">Bir satır oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1279d-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="1279d-109">**Kapatma dönemi** alanında, TDS kapatma dönemi için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="1279d-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="1279d-110">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="1279d-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="1279d-111">**Stopaj vergisi yetkilisi** alanında, adına TDS kapatma dönemi tanımladığınız TDS yetkilisini seçin.</span><span class="sxs-lookup"><span data-stu-id="1279d-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="1279d-112">**Genel** hızlı sekmesinde, **Dönem aralığı** alanında, TDS kapatma dönemi için dönem aralığı türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="1279d-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="1279d-113">**Birim sayısı** alanında, dönem aralığı türü için birim sayısını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1279d-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="1279d-114">**Dönemler** hızlı sekmesinde, **Başlangıç tarihi** alanında, TDS kapatma döneminin başlangıç tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="1279d-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="1279d-115">**Bitiş tarihi** alanında, bitiş tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="1279d-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="1279d-116">Mevcut bir dönem için, dönem aralığı ve dönem birimlerine dayanan sonraki bir TDS kapatma dönemi oluşturmak için **Yeni dönem**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1279d-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="1279d-117">Belirli bir kapatma dönemi için çalıştırılan dönemsel TDS kapatmasının ayrıntılarını görüntülemek için **Stopaj vergisi ödemesi** sayfasını açmak için ve **Stopaj vergisi ödemeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="1279d-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1279d-118">Dönemsel TDS kapatma işlemini çalıştırmak için, **Genel muhasebe \> Dönemsel \> Stopaj vergisi \> Stopaj vergisi ödemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1279d-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="1279d-119">[![Stopaj vergisi ödemesi sayfası](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="1279d-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="1279d-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1279d-120">Close the page.</span></span>
