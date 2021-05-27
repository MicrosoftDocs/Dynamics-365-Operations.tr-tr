---
title: TaxTrans kaydı oluşturulmuyor
description: Bu konu, TaxTrans kaydı oluşturulmuyorsa yardımcı olabilecek sorun giderme bilgileri sağlar.
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
ms.openlocfilehash: 74987506699834d86703702106e5abf87bfa45da
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018793"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="6ef04-103">TaxTrans kaydı oluşturulmuyor</span><span class="sxs-lookup"><span data-stu-id="6ef04-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ef04-104">Bir hareket için **Deftere nakledilen satış vergisi**'ni seçerseniz ancak **Deftere nakledilen satış vergisi** sayfası hiçbir vergi satırı göstermiyor veya bir vergi satırı eksikse, **TaxTrans** kaydı oluşturulmamış olabilir.</span><span class="sxs-lookup"><span data-stu-id="6ef04-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="6ef04-105">[![Satır maddeleri olmayan deftere nakledilen satış vergisi sayfası](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="6ef04-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="6ef04-106">Bu sorunu gidermek için, aşağıdaki bölümlerde gereken adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6ef04-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="6ef04-107">Hareketi deftere nakletmeden önce satış vergisini denetleyin</span><span class="sxs-lookup"><span data-stu-id="6ef04-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="6ef04-108">Hareketi deftere nakletmeden önce, **Faturayı deftere nakletme** sayfasında hesaplamayı denetlemek için **Satış vergisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="6ef04-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="6ef04-109">[![Fatura deftere nakli sayfasındaki satış vergisi düğmesi](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="6ef04-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="6ef04-110">**Geçici satış vergisi hareketleri** sayfasında, hesaplama sonucunu gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="6ef04-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="6ef04-111">Herhangi bir vergi hesaplanmamışsa bkz. [Vergi hesaplanmıyor veya vergi tutarı sıfır](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span><span class="sxs-lookup"><span data-stu-id="6ef04-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="6ef04-112">Tüm deftere nakledilen satış vergilerinde TaxTrans kaydını bulun</span><span class="sxs-lookup"><span data-stu-id="6ef04-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="6ef04-113">**Vergi** \> **Sorgular ve bildirimler** \> **Satış vergisi sorguları** > **Deftere nakledilen satış vergisi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6ef04-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="6ef04-114">**TaxTrans** kaydını bulmak için **Fiş** sütunu başlığında filtre sembolünü seçin.</span><span class="sxs-lookup"><span data-stu-id="6ef04-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="6ef04-115">Aradığınız satış vergisi kayıtlarını bulursanız, tarihi kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="6ef04-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="6ef04-116">Tarih, günlük başlığındaki tarihten farklıysa, ek destek için bir Microsoft servis talebi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6ef04-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="6ef04-117">[![Deftere nakledilen satış vergisi sayfası](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="6ef04-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="6ef04-118">Ayrıntıları denetlemek için hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="6ef04-118">Debug to check details</span></span>

1. <span data-ttu-id="6ef04-119">Hata ayıklama ve **TmpTaxWorkTrans** ve **TaxUncommitted**'ın doğru oluşturulup oluşturulmadığını tespit etmek hakkında bilgi edinmek için bkz. [TaxTrans'taki alan değeri hatalı](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span><span class="sxs-lookup"><span data-stu-id="6ef04-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="6ef04-120">**TaxTmpWorkTrans** veya **TaxUncommitted** öğesi doğru oluşturulduysa, **TaxTrans**'ın eklenmeme nedeninde hata ayıklama yapmak için **TaxPost::SaveAndPost()** ve **Tax::SaveAndPost** yönteminde kesme noktası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6ef04-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="6ef04-121">[![Kodda eklenen kesme noktaları](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="6ef04-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="6ef04-122">[![Eklenen kesme noktalarının sonuçları](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="6ef04-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="6ef04-123">Özelleştirme olup olmadığını belirleyin</span><span class="sxs-lookup"><span data-stu-id="6ef04-123">Determine whether customization exists</span></span>

<span data-ttu-id="6ef04-124">Önceki bölümlerdeki adımları tamamladıysanız ve bir sorun bulamadıysanız bir özelleştirme olup olmadığını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="6ef04-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="6ef04-125">Hiçbir özelleştirme yoksa daha fazla destek için bir Microsoft servis talebi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6ef04-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
