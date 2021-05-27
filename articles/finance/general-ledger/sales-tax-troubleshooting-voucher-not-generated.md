---
title: Fiş oluşturulmuyor
description: Bu konu, oluşturulması gereken fiş oluşturulmuyorsa yardımcı olabilecek sorun giderme bilgileri sağlar.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ba23b597b1d7d283b99638fb7d5d91da00afb09c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018769"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="12610-103">Fiş oluşturulmuyor</span><span class="sxs-lookup"><span data-stu-id="12610-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12610-104">Bir fiş oluşturulması gerekirken **Fiş hareketleri** sayfasında herhangi bir fiş görüntülenmiyorsa bu sorunu gidermek için aşağıdaki bölümlerdeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="12610-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="12610-105">[![Fiş görüntülenmeyen fiş hareketleri sayfası](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="12610-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="12610-106">Vergi uygulanabilirliğini kontrol edin</span><span class="sxs-lookup"><span data-stu-id="12610-106">Check the tax applicability</span></span>

1. <span data-ttu-id="12610-107">**Vergi** \> **Periyodik görevler** \> **Henüz transfer edilmemiş alt muhasebe günlük girişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="12610-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="12610-108">Defter kaydı varsa bunu seçin ve **Şimdi transfer et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12610-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="12610-109">[![Henüz transfer edilmemiş alt genel muhasebe günlük girişleri sayfasındaki Şimdi transfer et düğmesi](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="12610-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="12610-110">Fişin oluşturulup oluşturulmadığını görmek için **Fiş hareketleri** sayfasını yeniden açın.</span><span class="sxs-lookup"><span data-stu-id="12610-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="12610-111">Özelleştirme olup olmadığını belirleyin</span><span class="sxs-lookup"><span data-stu-id="12610-111">Determine whether customization exists</span></span>

<span data-ttu-id="12610-112">Önceki bölümdeki adımları tamamladıysanız ve bir sorun bulamadıysanız bir özelleştirme olup olmadığını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="12610-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="12610-113">Hiçbir özelleştirme yoksa daha fazla destek için bir Microsoft servis talebi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="12610-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
