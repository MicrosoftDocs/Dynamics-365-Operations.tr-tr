---
title: "Fatura toplamları eşleştirme sırasındaki tutarsızlıkları çözümleme"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f7e1261838866688c97529b0edfa1354034247b
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="34cca-102">Fatura toplamları eşleştirme sırasındaki tutarsızlıkları çözümleme</span><span class="sxs-lookup"><span data-stu-id="34cca-102">Resolve discrepancies during invoice totals matching</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="34cca-103">Bir fatura doğrulama karşılaştırma türü eşleşen fatura toplamlarıdır.</span><span class="sxs-lookup"><span data-stu-id="34cca-103">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="34cca-104">Sistemin eşleşen fatura toplamları gerçekleştirmesi gerektiğini belirtmek için **Borç hesapları parametreleri** sayfası **fatura doğrulama** sekmesinde, **fatura toplamları eşleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="34cca-104">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="34cca-105">Fatura toplamları eşleştirmesini, toplam fatura tutarlarının beklenen tutarlar ile aralarındaki farkın kabul edilebilir bir düzeyden fazla olmadığını garanti etmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34cca-105">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="34cca-106">Altı toplamları **fatura toplamları eşleşme ayrıntıları** sayfasında karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="34cca-106">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="34cca-107">Toplamlardan herhangi birini beklenen karşılık gelen satınalma siparişi toplamından saparsa, eşleşen bir tutarsızlık işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="34cca-107">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="34cca-108">Toplamlar eşleşme tutarsızlıkları içeren faturayı gözden geçirmek için **satıcı fatura girişi** çalışma alanında **bekleyen faturalar** döşemesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="34cca-108">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="34cca-109">Daha sonra eylem bölmesinde, üzerinde **İnceleme** sekmesinde, **eşleştirme ayrıntıları**'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="34cca-109">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="34cca-110">Eşleşme tutarsızlığı algılanırsa, uyarı simgeleri fatura tutarı yanında görünür.</span><span class="sxs-lookup"><span data-stu-id="34cca-110">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="34cca-111">Toplamları hakkında daha fazla ayrıntıyı fatura toplamları eşleşme ayrıntılarını görüntüleyerek görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34cca-111">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="34cca-112">Farklılığı belirledikten sonra, faturadaki bilgilerin yanlış olduğunu düşünüyorsanız satıcınıza başvurmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="34cca-112">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="34cca-113">Satıcıyla son anlaşmanıza bağlı olarak aşağıdaki eylemlerden birini gerçekleştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="34cca-113">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="34cca-114">Fiyat farkını kabul edin ve eşleşme tutarsızlıkları içeren faturayı nakledin.</span><span class="sxs-lookup"><span data-stu-id="34cca-114">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="34cca-115">Eşleşen çelişki olursa deftere nakletmeden önce onay gerektirecek şekilde sisteminiz ayarlanmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="34cca-115">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="34cca-116">Bu durumda, eşleşen bir tutarsızlık onaylamanız gerekir ve isteğe bağlı olarak bir onay yorumu girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34cca-116">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="34cca-117">Sonra faturayı nakletmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34cca-117">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="34cca-118">Fatura tutarını beklenen tutarla değiştirin ve faturayı nakledin.</span><span class="sxs-lookup"><span data-stu-id="34cca-118">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="34cca-119">Satıcıdan tam kredi ve düzeltilmiş yeni bir fatura talep edin.</span><span class="sxs-lookup"><span data-stu-id="34cca-119">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="34cca-120">Daha fazla bilgi için bkz. [Özel durumları araştırma ve çözme](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="34cca-120">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



