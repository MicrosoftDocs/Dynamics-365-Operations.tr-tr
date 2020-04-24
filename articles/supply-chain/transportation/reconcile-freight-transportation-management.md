---
title: Navlun taşımacılık yönetiminde mutabakat sağlama
description: Bu konu altında navlun mutabakatı işlemi anlatılmaktadır.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e1680572f1ba9816c9ec45ef52498cab1f45247
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206231"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="06aa8-103">Navlun taşımacılık yönetiminde mutabakat sağlama</span><span class="sxs-lookup"><span data-stu-id="06aa8-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06aa8-104">Bu konu altında navlun mutabakatı işlemi anlatılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="06aa8-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="06aa8-105">Navlun mutabakatı el ile yapılabilir veya otomatik olarak gerçekleşmek üzere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="06aa8-106">Otomatik navlun mutabakatı kullanmak için, otomatik olarak eşleştirilecek navlun faturalarını belirleyen ölçütleri tanımlayabileceğiniz bir ana denetim ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="06aa8-107">Navlun mutabakat işlemi</span><span class="sxs-lookup"><span data-stu-id="06aa8-107">The freight reconciliation process</span></span>
<span data-ttu-id="06aa8-108">Navlun oranları ilgili sevkiyat taşıyıcısı ile ilişkilendirilmiş değerlendirme altyapısı tarafından hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="06aa8-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="06aa8-109">Bir yük onaylandığında, navlun faturası oluşturulur ve navlun giderleri bu faturaya aktarılır.</span><span class="sxs-lookup"><span data-stu-id="06aa8-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="06aa8-110">Navlun giderleri normal faturalandırma sürecinde kullanılan kuruluma bağlı olarak, ilgili kaynak belgesine sair masraflar (satınalma siparişi, satış siparişi ve/veya transfer emri) olarak paylaştırılır.</span><span class="sxs-lookup"><span data-stu-id="06aa8-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="06aa8-111">Navlun mutabakatı süreci (eşleştirme süreci olarak da adlandırılır) navlun faturası sevkiyat taşıyıcısından ulaştığı anda başlayabilir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="06aa8-112">Fatura elektronik veya kağıt üzerinde alınabilir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="06aa8-113">Fatura kağıt üzerinde alınırsa navlun faturasını şablon olarak kullanarak elektronik bir fatura oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06aa8-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="06aa8-114">[![Navlun mutabakatı işlemi](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="06aa8-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="06aa8-115">El ile mutabakat</span><span class="sxs-lookup"><span data-stu-id="06aa8-115">Manual reconciliation</span></span>
<span data-ttu-id="06aa8-116">Navlun mutabakatını el ile gerçekleştiriyorsanız her fatura satırını faturalandırılan yüke ait navlun faturasındaki satır veya satırlarla eşleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="06aa8-117">Bu eşleştirme işlemi **Navlun faturası ve fatura eşleştirme** sayfasından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="06aa8-118">Fatura satırındaki tutar navlun faturası tutarıyla eşleşmiyorsa, aradaki fark için bir mutabakat nedeni seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="06aa8-119">Mutabakatın birden fazla nedeni varsa eşleşmeyen tutarı bu nedenler arasında paylaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06aa8-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="06aa8-120">Mutabakat nedeni farklı tutarların genel muhasebe defterine nasıl nakledileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="06aa8-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="06aa8-121">Tüm fatura tutarının mutabakatı açıklandığında, onay için gönderilir ve deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="06aa8-122">Aşağıdaki resimde navlun faturası oluşturma ve navlun mutabakatı gerçekleştirme işlemleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span> 
<span data-ttu-id="06aa8-123">[![Navlun mutabakat görevleri](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="06aa8-123">[![Freight reconcilation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="06aa8-124">Otomatik mutabakat</span><span class="sxs-lookup"><span data-stu-id="06aa8-124">Automatic reconciliation</span></span>
<span data-ttu-id="06aa8-125">Otomatik mutabakat kullanmak için mutabakatın zaman çizelgesini, faturaları ve kullanılacak sevkiyat taşıyıcılarını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="06aa8-126">Fatura satırları ile navlun faturalarını eşleştirme işlemi ana denetim kurulumuna ve navlun faturası türüne göre gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="06aa8-127">Otomatik mutabakat çalıştırdıktan sonra sistemin eşleştiremediği tüm faturaları el ile incelemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="06aa8-128">Bundan sonra tüm faturaları ödeme için nakledebilmeniz için bu faturaları el ile işlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="06aa8-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>



