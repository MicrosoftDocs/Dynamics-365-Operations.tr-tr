---
title: Deftere nakledilen TDS ödemelerini ve TDS kapatma dönemine ilişkin hareketleri görüntüleme
description: Bu konu, bir kapanış dönemi için deftere nakledilen Kaynaktan Kesilen Vergi (TDS) ödemeleri ve hareketlerini görüntülemeyi açıklar.
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
ms.openlocfilehash: 2bada42073e46c69101e6d31f3328a2eeb95f880
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023651"
---
# <a name="view-posted-tds-payments-and-transactions-for-a-tds-settlement-period"></a><span data-ttu-id="9adc7-103">Deftere nakledilen TDS ödemelerini ve TDS kapatma dönemine ilişkin hareketleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="9adc7-103">View posted TDS payments and transactions for a TDS settlement period</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9adc7-104">Bu konu, bir kapanış dönemi için deftere nakledilen Kaynaktan Kesilen Vergi (TDS) ödemeleri ve hareketlerini görüntülemeyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="9adc7-104">This topic explains how to view the Tax Deducted at Source (TDS) payments and transactions that were posted for a settlement period.</span></span>

1. <span data-ttu-id="9adc7-105">**Vergi \> Dolaylı vergiler \> Stopaj vergisi \> Stopaj vergisi kapatma dönemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9adc7-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="9adc7-106">[![Stopaj vergisi kapatma dönemleri sayfası](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span><span class="sxs-lookup"><span data-stu-id="9adc7-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span></span>

2. <span data-ttu-id="9adc7-107">**Stopaj vergisi kapatma dönemleri** sayfasında, belirli bir TDS kapatma dönemi için yapılan TDS kapatmalarını görüntüleyebileceğiniz **Stopaj vergisi ödemeleri** sayfasını açmak için **Stopaj vergisi ödemeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="9adc7-107">On the **Withholding tax settlement periods** page, select **Withholding tax payments** to open the **Withholding tax payments** page, where you can view the TDS settlements that were made for a specific TDS settlement period.</span></span>

    <span data-ttu-id="9adc7-108">**Genel Bakış** sekmesinde aşağıdaki bilgiler görüntülenir:</span><span class="sxs-lookup"><span data-stu-id="9adc7-108">The **Overview** tab shows the following information:</span></span>

    - <span data-ttu-id="9adc7-109">**Tarih** – TDS kapanış tarihi.</span><span class="sxs-lookup"><span data-stu-id="9adc7-109">**Date** – The date of TDS settlement.</span></span>
    - <span data-ttu-id="9adc7-110">**Fiş** – TDS kapanış hareketinin fiş numarası.</span><span class="sxs-lookup"><span data-stu-id="9adc7-110">**Voucher** – The voucher number of the TDS settlement transaction.</span></span>
    - <span data-ttu-id="9adc7-111">**Vergi türü** – Kapatma işleminin adına çalıştırıldığı vergi türü.</span><span class="sxs-lookup"><span data-stu-id="9adc7-111">**Tax type** – The tax type that the settlement process is run for.</span></span>
    - <span data-ttu-id="9adc7-112">**Vergi Hesap Numarası (TAN)** – Kapatılan TDS hareketinin Vergi Hesap Numarası (TAN).</span><span class="sxs-lookup"><span data-stu-id="9adc7-112">**Tax Account Number (TAN)** – The Tax Account Number (TAN) of the settled TDS transaction.</span></span>
    - <span data-ttu-id="9adc7-113">**Kapatma dönemi** – TDS kapanış işleminin adına çalıştırıldığı kapatma dönemi.</span><span class="sxs-lookup"><span data-stu-id="9adc7-113">**Settlement period** – The settlement period that the TDS settlement process is run for.</span></span>
    - <span data-ttu-id="9adc7-114">**Başlangıç tarihi** - Kapatma döneminin başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="9adc7-114">**From date** – The start date of the settlement period.</span></span>
    - <span data-ttu-id="9adc7-115">**Bitiş tarihi** - Kapatma döneminin bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="9adc7-115">**To date** – The end date of the settlement period.</span></span>
    - <span data-ttu-id="9adc7-116">**Stopaj vergisi ödemesi sürümü** – Stopaj vergisi ödemesinin sürümü: **Orijinal**, **En son düzeltmeler** veya **Toplam liste**.</span><span class="sxs-lookup"><span data-stu-id="9adc7-116">**Withholding tax payment version** – The version of the withholding tax payment: **Original**, **Latest corrections**, or **Total list**.</span></span>

5. <span data-ttu-id="9adc7-117">TDS hareketiyle ilgili fiş girişlerini görüntülemek için **Fiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9adc7-117">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
6. <span data-ttu-id="9adc7-118">Bir kapatma döneminde belirli bir dönem için kapatılan TDS hareketlerinin ayrıntılarını görüntülemek için **Stopaj vergisi hareketleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="9adc7-118">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for a specific period during a settlement period.</span></span> <span data-ttu-id="9adc7-119">TDS hareketiyle ilgili fiş girişlerini görüntülemek için **Fiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9adc7-119">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span> <span data-ttu-id="9adc7-120">Belirli bir TDS vergi koduyla ilgili her TDS vergi bileşeni için hesaplanan TDS'yi görüntülemek için **Stopaj vergisi bileşenleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="9adc7-120">Select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>
7. <span data-ttu-id="9adc7-121">**Stopaj vergisi kapatma dönemleri** sayfasına dönmek için **Stopaj vergisi ödemeleri** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="9adc7-121">Close the **Withholding tax payments** page to return to the **Withholding tax settlement periods** page.</span></span>
8. <span data-ttu-id="9adc7-122">Kapatma dönemi için kapatılan TDS hareketlerinin ayrıntılarını görüntülemek için **Stopaj vergisi hareketleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="9adc7-122">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for the settlement period.</span></span>
