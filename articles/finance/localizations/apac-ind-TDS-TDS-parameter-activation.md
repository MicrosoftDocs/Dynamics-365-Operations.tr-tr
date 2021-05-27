---
title: TDS parametrelerini ayarlama
description: Bu konu, belirtilen hareketlerdeki Kaynakta Kesilen Vergi (TDS) işlevini etkinleştirecek şekilde parametrelerin nasıl ayarlanabileceğini açıklar. Bu, Kaynakta Kesilen Vergi TDS özelliğini kullanmak için zorunlu bir adımdır.
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023656"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="6b95b-104">TDS parametrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="6b95b-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b95b-105">Bu konu, belirtilen hareketlerdeki Kaynakta Kesilen Vergi (TDS) işlevini etkinleştirecek şekilde parametrelerin nasıl ayarlanabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="6b95b-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="6b95b-106">Bu, Kaynakta Kesilen Vergi TDS özelliğini kullanmak için zorunlu bir adımdır.</span><span class="sxs-lookup"><span data-stu-id="6b95b-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="6b95b-107">**Genel muhasebe\> Genel muhasebe ayarı \> Genel muhasebe parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6b95b-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="6b95b-108">**Doğrudan vergiler** sekmesinde, **Kaynakta Kesilen Vergi** bölümünde **TDS'yi etkinleştir** seçeneğini **Evet** olarak ayarlayarak TDS işlevini ve bunun için kullanılan sayfa ve alanları etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="6b95b-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="6b95b-109">TDS'yi fatura düzeyinde hesaplamak ve kesmek için kullanılan alanları etkinleştirmek için **Fatura** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6b95b-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="6b95b-110">TDS'yi ödeme düzeyinde hesaplamak ve kesmek için kullanılan alanları etkinleştirmek için **Ödeme** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6b95b-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="6b95b-111">[![Doğrudan vergiler sekmesi](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="6b95b-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="6b95b-112">**Numara sıraları** sekmesinde, **Referans** alanının **Stopaj vergisi ödemesi** olarak ayarlandığı satırı bulun.</span><span class="sxs-lookup"><span data-stu-id="6b95b-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="6b95b-113">**Numara sırası kodu** alanında, satır için numara sırası kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6b95b-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="6b95b-114">Numara sırası kodu, dönemsel TDS kapatma işlemi için fiş numaraları oluşturmak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6b95b-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6b95b-115">Dönemsel TDS kapatma işlemini çalıştırmak için, **Vergi \> Beyannameler \> Stopaj vergisi \> Stopaj vergisi ödemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6b95b-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="6b95b-116">[![Numara serileri sekmesi](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="6b95b-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="6b95b-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6b95b-117">Close the page.</span></span>
