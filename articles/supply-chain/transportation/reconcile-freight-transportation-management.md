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
# <a name="reconcile-freight-in-transportation-management"></a>Navlun taşımacılık yönetiminde mutabakat sağlama

[!include [banner](../includes/banner.md)]

Bu konu altında navlun mutabakatı işlemi anlatılmaktadır.

Navlun mutabakatı el ile yapılabilir veya otomatik olarak gerçekleşmek üzere ayarlanabilir. Otomatik navlun mutabakatı kullanmak için, otomatik olarak eşleştirilecek navlun faturalarını belirleyen ölçütleri tanımlayabileceğiniz bir ana denetim ayarlamanız gerekir.

## <a name="the-freight-reconciliation-process"></a>Navlun mutabakat işlemi
Navlun oranları ilgili sevkiyat taşıyıcısı ile ilişkilendirilmiş değerlendirme altyapısı tarafından hesaplanır. Bir yük onaylandığında, navlun faturası oluşturulur ve navlun giderleri bu faturaya aktarılır. Navlun giderleri normal faturalandırma sürecinde kullanılan kuruluma bağlı olarak, ilgili kaynak belgesine sair masraflar (satınalma siparişi, satış siparişi ve/veya transfer emri) olarak paylaştırılır. Navlun mutabakatı süreci (eşleştirme süreci olarak da adlandırılır) navlun faturası sevkiyat taşıyıcısından ulaştığı anda başlayabilir. Fatura elektronik veya kağıt üzerinde alınabilir. Fatura kağıt üzerinde alınırsa navlun faturasını şablon olarak kullanarak elektronik bir fatura oluşturabilirsiniz. 

[![Navlun mutabakatı işlemi](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>El ile mutabakat
Navlun mutabakatını el ile gerçekleştiriyorsanız her fatura satırını faturalandırılan yüke ait navlun faturasındaki satır veya satırlarla eşleştirmeniz gerekir. Bu eşleştirme işlemi **Navlun faturası ve fatura eşleştirme** sayfasından gerçekleştirilir. Fatura satırındaki tutar navlun faturası tutarıyla eşleşmiyorsa, aradaki fark için bir mutabakat nedeni seçmeniz gerekir. Mutabakatın birden fazla nedeni varsa eşleşmeyen tutarı bu nedenler arasında paylaştırabilirsiniz. Mutabakat nedeni farklı tutarların genel muhasebe defterine nasıl nakledileceğini belirler. Tüm fatura tutarının mutabakatı açıklandığında, onay için gönderilir ve deftere nakledilir. Aşağıdaki resimde navlun faturası oluşturma ve navlun mutabakatı gerçekleştirme işlemleri gösterilmektedir. 
[![Navlun mutabakat görevleri](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Otomatik mutabakat
Otomatik mutabakat kullanmak için mutabakatın zaman çizelgesini, faturaları ve kullanılacak sevkiyat taşıyıcılarını belirtmeniz gerekir. Fatura satırları ile navlun faturalarını eşleştirme işlemi ana denetim kurulumuna ve navlun faturası türüne göre gerçekleştirilir. Otomatik mutabakat çalıştırdıktan sonra sistemin eşleştiremediği tüm faturaları el ile incelemeniz gerekir. Bundan sonra tüm faturaları ödeme için nakledebilmeniz için bu faturaları el ile işlemeniz gerekir.



