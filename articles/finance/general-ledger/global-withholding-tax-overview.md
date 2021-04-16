---
title: Genel stopaj vergisi
description: Bu konu, genel stopaj vergisi işlevselliği ve nasıl ayarlanacağı hakkında bilgiler sağlar. Genel stopaj vergisi işlevselliği satıcı ve müşteri hareketleri için geliştirilmiştir, böylece stopaj vergisi kalem düzeyinde hesaplanır.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 9a73d34fb4fbf007cbb5a996cfa6e9719532869c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826678"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="8c0b8-104">Genel stopaj vergisi</span><span class="sxs-lookup"><span data-stu-id="8c0b8-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c0b8-105">Bu konu, genel stopaj vergisi işlevselliği hakkında bilgiler sağlar ve nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="8c0b8-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="8c0b8-106">Bu yeni işlev, 10.0.17 sürümü ve sonrasında bulunur.</span><span class="sxs-lookup"><span data-stu-id="8c0b8-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="8c0b8-107">Genel stopaj vergisi işlevselliği satıcı ve müşteri hareketleri için geliştirilmiştir, böylece stopaj vergisi kalem düzeyinde hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="8c0b8-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="8c0b8-108">Satın alma hareketlerinden stopaj vergisi hesabındaki bakiye, stopaj vergisi ödeme işini stopaj vergisi kapatma hesabıyla karşılaştırılarak kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="8c0b8-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="8c0b8-109">Genel stopaj vergisi, satın alma siparişi, satıcı faturası ve satış siparişi sayfalarındaki **Giderleri koru** işlevini desteklemez.</span><span class="sxs-lookup"><span data-stu-id="8c0b8-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="8c0b8-110">Genel stopaj vergisini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="8c0b8-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="8c0b8-111">**Özellik Yönetimi** çalışma alanında, listeden **Genel stopaj vergisi**'ni seçin ve **Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c0b8-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="8c0b8-112">**Vergi \> Kurulum \> Parametreler \> Genel muhasebe parametreleri**'ne gidin ve **Stopaj vergisi** sekmesinde **Genel stopaj vergisini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8c0b8-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="8c0b8-113">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c0b8-113">Select **Save**.</span></span>
4. <span data-ttu-id="8c0b8-114">Web tarayıcınızda sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="8c0b8-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="8c0b8-115">Yerelleştirilmiş stopaj vergisi çözümlerinin zaten sunulmakta olduğu ülkeler/bölgeler için genel stopaj vergisi işlevselliği etkinleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="8c0b8-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="8c0b8-116">Bu alanlar Hindistan, Brezilya, Tayland, Suudi Arabistan, İrlanda, Büyük Britanya ve ABD'yi içerir ancak bunlarla sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="8c0b8-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]