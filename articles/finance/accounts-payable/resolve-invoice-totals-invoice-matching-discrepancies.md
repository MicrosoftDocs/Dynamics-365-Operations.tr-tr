---
title: Fatura toplamlarını eşleştirme sırasında uyuşmazlıkları gidermeye genel bakış
description: Fatura toplamları eşleştirmesini, toplam fatura tutarlarının beklenen tutarlar ile aralarındaki farkın kabul edilebilir bir düzeyden fazla olmadığını garanti etmek için kullanabilirsiniz.
author: abruer
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 804800cccdfd0473c9e3514f6c17405eb2ec8335
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827926"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a><span data-ttu-id="e33db-103">Fatura toplamlarını eşleştirme sırasında uyuşmazlıkları gidermeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="e33db-103">Resolve discrepancies during invoice totals matching overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e33db-104">Bir fatura eşleştirme doğrulaması türü eşleşen fatura toplamlarıdır.</span><span class="sxs-lookup"><span data-stu-id="e33db-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="e33db-105">Sistemin eşleşen fatura toplamları gerçekleştirmesi gerektiğini belirtmek için **Borç hesapları parametreleri** sayfası **fatura doğrulama** sekmesinde, **fatura toplamları eşleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e33db-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="e33db-106">Fatura toplamları eşleştirmesini, toplam fatura tutarlarının beklenen tutarlar ile aralarındaki farkın kabul edilebilir bir düzeyden fazla olmadığını garanti etmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e33db-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="e33db-107">Altı toplamları **fatura toplamları eşleşme ayrıntıları** sayfasında karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="e33db-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="e33db-108">Toplamlardan herhangi birini beklenen karşılık gelen satınalma siparişi toplamından saparsa, eşleşen bir tutarsızlık işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="e33db-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="e33db-109">Toplamlar eşleşme tutarsızlıkları içeren faturayı gözden geçirmek için **satıcı fatura girişi** çalışma alanında **bekleyen faturalar** döşemesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e33db-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="e33db-110">Daha sonra eylem bölmesinde, üzerinde **İnceleme** sekmesinde, **eşleştirme ayrıntıları**'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e33db-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="e33db-111">Eşleşme tutarsızlığı algılanırsa, uyarı simgeleri fatura tutarı yanında görünür.</span><span class="sxs-lookup"><span data-stu-id="e33db-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="e33db-112">Toplamları hakkında daha fazla ayrıntıyı fatura toplamları eşleşme ayrıntılarını görüntüleyerek görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e33db-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="e33db-113">Farklılığı belirledikten sonra, faturadaki bilgilerin yanlış olduğunu düşünüyorsanız satıcınıza başvurmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="e33db-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="e33db-114">Satıcıyla son anlaşmanıza bağlı olarak aşağıdaki eylemlerden birini gerçekleştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="e33db-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="e33db-115">Fiyat farkını kabul edin ve eşleşme tutarsızlıkları içeren faturayı nakledin.</span><span class="sxs-lookup"><span data-stu-id="e33db-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="e33db-116">Eşleşen çelişki olursa deftere nakletmeden önce onay gerektirecek şekilde sisteminiz ayarlanmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="e33db-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="e33db-117">Bu durumda, eşleşen bir tutarsızlık onaylamanız gerekir ve isteğe bağlı olarak bir onay yorumu girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e33db-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="e33db-118">Sonra faturayı nakletmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e33db-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="e33db-119">Fatura tutarını beklenen tutarla değiştirin ve faturayı nakledin.</span><span class="sxs-lookup"><span data-stu-id="e33db-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="e33db-120">Satıcıdan tam kredi ve düzeltilmiş yeni bir fatura talep edin.</span><span class="sxs-lookup"><span data-stu-id="e33db-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="e33db-121">Daha fazla bilgi için bkz. [Özel durumları Araştırma/Çözme](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="e33db-121">For more information, see [Research/Resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]