---
title: TDS tahsisatıyla ödeme planlarını ayarlama
description: Bu konu, Kaynakta Kesilen Vergi (TDS) tahsisatıyla ödeme planlarının nasıl ayarlanacağını açıklar.
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023666"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="d3e79-103">TDS tahsisatıyla ödeme planlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="d3e79-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3e79-104">Bu konu, Kaynakta Kesilen Vergi (TDS) tahsisatıyla ödeme planlarının nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="d3e79-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="d3e79-105">**Borç hesapları \> Ödeme kurulumu \> Ödeme planları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d3e79-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="d3e79-106">[![Ödeme planları sayfası](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="d3e79-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="d3e79-107">Eylem bölmesinde, ödeme planı oluşturmak üzere **Yeni**'yi seçin ve gerekli ayrıntıları girin.</span><span class="sxs-lookup"><span data-stu-id="d3e79-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="d3e79-108">**Tahsisat** alanında, ödeme planı için ödemeyi tahsis etmek üzere kullanılacak yöntemi seçin:</span><span class="sxs-lookup"><span data-stu-id="d3e79-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="d3e79-109">Toplam</span><span class="sxs-lookup"><span data-stu-id="d3e79-109">Total</span></span>
    - <span data-ttu-id="d3e79-110">Sabit tutar</span><span class="sxs-lookup"><span data-stu-id="d3e79-110">Fixed amount</span></span>
    - <span data-ttu-id="d3e79-111">Sabit miktar</span><span class="sxs-lookup"><span data-stu-id="d3e79-111">Fixed quantity</span></span>
    - <span data-ttu-id="d3e79-112">Belirtilen</span><span class="sxs-lookup"><span data-stu-id="d3e79-112">Specified</span></span>

    <span data-ttu-id="d3e79-113">**Stopaj vergisi tahsisatı** alanı, ödeme planı için TDS tahsisat yöntemini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3e79-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="d3e79-114">**Tahsisat** alanında **Toplam**'ı seçerseniz, **Stopaj vergisi tahsisatı** alanı otomatik olarak **Toplam**'a ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d3e79-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="d3e79-115">**Sabit tutar**, **Sabit miktar**'ı veya **Tahsisat** alanında **Belirtilen**'i seçerseniz, **Stopaj vergisi tahsisatı** alanı otomatik olarak **Orantılı** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d3e79-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d3e79-116">**Stopaj vergisi tahsisatı** alanı **Toplam** olarak ayarlanmışsa, ödeme taksitleri TDS tutarını içeren brüt tutar temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="d3e79-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="d3e79-117">**Stopaj vergisi tahsisatı** alanı **Orantılı** olarak ayarlanmışsa, ödeme taksitleri TDS tutarı kesildikten sonra net fatura tutarı temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="d3e79-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="d3e79-118">Gerekli diğer ayrıntıları girin ve sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d3e79-118">Enter the other required details, and then close the page.</span></span>
