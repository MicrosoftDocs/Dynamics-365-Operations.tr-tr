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
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac07155e4dde77689b1994abfb8b30f45d5a5a30
ms.sourcegitcommit: b6686265314499056690538eaa95ca51cff7c720
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014520"
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

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>Otomatik veya el ile mutabakatı kullanarak navlun fişleriyle navlun faturalarını eşleştirme

*Eşleme*, her navlun faturasına karşılık gelen navlun fişlerini bulma işlemidir. Bu işlem, fatura satırlarını birer birer (el ile eşleşme) ile veya tüm kullanılabilir faturaların aynı anda eşleştirilmesiyle (otomatik eşleştirme) yapılabilir.

### <a name="auto-matching"></a>Otomatik eşleme

Birden fazla navlun faturasını aynı navlun fişiyle eşleştirmek için otomatik eşleme işlemi aşağıdaki şekilde çalışır:

1. Eşlenmeyen tüm navlun faturaları, en başta en büyük tutar olacak şekilde tutara göre sıralanır.
1. Navlun fişinde pozitif tutar kalmayana kadar navlun faturaları birer birer eşleştirilir.
1. Ana denetimin kurulumuna ve navlun faturalarının kalan tutarına bağlı olarak kalan tutar ayarlanır.

### <a name="manual-matching"></a>El ile eşleştirme

Pozitif tutarları olan tüm navlun fişleri, eşleme için kullanılabilir. Otomatik eşlemeye benzer şekilde kullanıcı, yalnızca negatif tutarı olan navlun faturalarını tamamen eşlenmeyen navlun fişleriyle eşleştirebilir.

### <a name="example"></a>Örnek

1500 tutarında bir navlun faturanız (FB) olduğunu ve aşağıdaki ayarlarla her fatura için bir fatura satırı içeren navlun fişi için üç navlun faturası oluşturduğunuzu varsayın:

- Orijinal navlun fişini (FB): Tutar 1500
- Fatura 1 (Inv1): Tutar 1000
- Fatura 2 (Inv2): Tutar 600
- Fatura 3 (Inv3): Tutar -100

#### <a name="automatic-matching-result"></a>Otomatik eşleştirme sonucu

Otomatik eşleme aşağıdaki sırada çalışır:

1. Tüm navlun faturalarını tutara göre azalan düzende sırala: Inv1-> Inv2-> Inv3.
1. Inv1 ile FB'yi eşleştirme. Inv1, 1000 tutarını eşleştirdi ve FB'nin kalan tutarı 500 oldu. Böylece durum *Kısmen eşleştirildi* olarak ayarlandı.
1. Inv2 ile FB'yi eşleştirme. Inv2, 500 tutarını eşleştirdi ve FB'nin kalan tutarı 0 oldu. Böylece durum *Tamamen eşleştirildi* olarak ayarlandı.
1. FB şu anda tümüyle eşleştirildiğinden Inv3 işlenmez.

#### <a name="manual-matching-result"></a>El ile eşleme sonucu

El ile eşleştirme için, sonuçlar, aşağıdaki örnek durumlarda gösterildiği gibi, eşleştirme sırasına göre değişir.

##### <a name="manual-matching-case-1"></a>El ile eşleme durumu 1

Bu örnek için el ile eşleştirme yapmanın bir yolu aşağıdakileri yapmaktır:

1. FB'yi Inv1 ile eşleştirme. FB'nin kalan tutarı 500'dür. Bu nedenle, durum *Kısmen eşleştirildi* olarak ayarlanmıştır.
1. Inv2 ile FB'yi eşleştirme. Inv2, 500 tutarını eşleştirdi ve FB'nin kalan tutarı 0 oldu. Böylece durum *Tamamen eşleştirildi* olarak ayarlandı.
1. Inv3 el ile eşleştirildiğinde, herhangi bir eşlenmeyen navlun fişi bulamazsınız.

Bu durum temelde, otomatik eşleme ile aynıdır

##### <a name="manual-matching-case-2"></a>El ile eşleme durumu 2

Bu örnek için el ile eşleştirme yapmanın bir diğer yolu da aşağıdakileri yapmaktır:

1. FB'yi Inv3 ile eşleştirme. Şimdi FB'nin kalan tutarı 1600'dür. Bu, 1500'ün üzerine eksi 100 çıkarmak anlamına gelir. Hem FB hem de Inv3'ün eşleşen miktarı -100 olur.
1. Inv1 ve Inv 2'yi arka arkaya FB ile eşleştirme. FB, tümüyle eşlenir.

Bu örnekte görüldüğü gibi, negatif tutarlarla sahip navlun faturalarını eşleme işlemi yalnızca el ile yapılmalıdır. Böylece, eşleşen sırayı denetleyebileceğinzi için navlun faturalarını her zaman tam olarak eşleştirilmeyen bir navlun fişiyle eşleştirebilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]