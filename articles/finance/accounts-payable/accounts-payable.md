---
title: Borç hesapları giriş sayfası
description: Bu konu, Borç hesapları konusuna genel bir bakış sağlar.
author: ShylaThompson
manager: AnnBe
ms.date: 02/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 21901
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 882afecdb33e5ad59a793f2f2391cb1ad27f911e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250710"
---
# <a name="accounts-payable-home-page"></a>Borç hesapları giriş sayfası

[!include [banner](../includes/banner.md)]

Bu konu, Borç hesapları konusuna genel bir bakış sağlar. 

Satıcı faturalarını el ile girebilir veya bir veri varlığı aracılığıyla elektronik olarak alabilirsiniz. Faturalar girildikten veya alındıktan sonra, bir fatura onay günlüğü veya **Satıcı faturası** sayfasını kullanarak faturaları gözden geçirebilir veya onaylayabilirsiniz. Belirli ölçütlere uyan faturaların otomatik olarak onaylanması için fatura eşleştirme, satıcı fatura ilkeleri ve iş akışını kullanarak gözden geçirme işlemini otomatikleştirebilirsiniz. Kalan faturalar, yetkili kullanıcı tarafından gözden geçirilmek üzere işaretlenir.

**İş süreçleri**

[![İş süreçleri diyagramı](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>Borç hesaplarını kurma

Satıcı grupları, satıcılar, deftere nakil profilleri, çeşitli ödeme seçenekleri ve satıcılara yönelik parametreler, masraflar, teslimatlar ve gönderilecek yerler, senetler ve diğer türdeki Borç hesapları bilgilerini oluşturun. 

[Borç hesaplarını yapılandırmaya genel bakış](accounts-payable-overview.md)

[Satıcı faturaları için muhasebe dağılımları ve yardımcı defter günlüğü girdileri](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[Borç hesapları ve Alacak hesapları için yabancı para birimi yeniden değerleme işlemi](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>Satıcı faturalarını yapılandırma

Faturaları ve satıcılara yapılan harcamaları izlemek için Borç hesapları bölümünü kullanın.

[Borç hesapları için fatura eşleştirmeye genel bakış](accounts-payable-invoice-matching.md)

[Satıcı deftere nakil profilleri](vendor-posting-profiles.md)

[Borç hesapları fatura eşleştirme doğrulaması ayarlama](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[Üç yönlü eşleştirme ilkeleri](three-way-matching-policies.md)

[Fatura eşleştirme ve şirketlerarası satınalma siparişleri](invoice-matching-intercompany-purchase-orders.md)

[Fatura toplamlarını eşleştirme sırasında uyuşmazlıkları gidermeye genel bakış](resolve-invoice-totals-invoice-matching-discrepancies.md)

[Satıcı faturası günlükleri ve fatura onay günlükleri için varsayılan mahsup hesaplar](default-offset-accounts-vendor-invoice-journals.md)

[Mobil fatura onayları](mobile-invoice-approvals.md)

[Satıcı işbirliği faturalama çalışma alanı](vendor-portal-invoicing-workspace.md)

[Satıcı faturası otomasyonu](vendor-invoice-automation.md)

## <a name="configure-vendor-payments"></a>Satıcı ödemelerini yapılandırma 

Çek, elektronik ödeme ve senet gibi sistem tarafından tanımlanan bir ödeme türünü kullanıcı tarafından tanımlanan ödeme yöntemine atayın. Ödeme türleri isteğe bağlıdır ancak elektronik ödemeleri doğrularken ve bir ödemenin kullandığı ödeme türünü hızlı bir şekilde belirlemek istediğinizde kullanışlıdır. 

[Satıcı ödemeleri çalışma alanı](vendor-payments-workspace.md)

[Satıcı ödeme masraflarını tanımlama](tasks/define-vendor-payment-fees.md)

[Satıcı ödeme koşullarını tanımlama](tasks/define-vendor-payment-terms.md)

[Pozitif ödemeye genel bakış](positive-pay-overview.md)

[Pozitif ödeme dosyaları ayarlama ve oluşturma](set-up-generate-positive-pay-files.md)

[Ödeme teklifi kullanarak satıcı ödemeleri oluşturma](create-vendor-payments-payment-proposal.md)

[Bir kısmi tutar için satıcı ödemeleri](vendor-payments-partial-amount.md)

[Satıcı ödemesi için hesaplanan iskontodan daha fazla iskonto alma](take-discount-more-calculated-discount-vendor-payment.md)

[Nakit iskontosu döneminin dışında bir nakit iskontosu alma](take-cash-discount-outside-cash-discount-timeframe.md)

[Satıcı çekleri için elektronik raporlama örneği](electronic-reporting-sample-vendor-checks.md)

[Satıcı ödemesini tersine çevirme](reverse-vendor-payment.md)

[Ön ödeme faturaları ve ön ödemeler karşılaştırması](prepayments-invoices-vs-prepayments.md)

[Borç hesapları için merkezi ödemeler](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>Kapatmalar

Aşağıdaki konular kapatmalar hakkında bilgi sağlar. Kapatma, ödemeleri faturalarla kapatma işlemidir. 

[Kapatma yapılandırma](../cash-bank-management/configure-settlement.md)

[Kısmi satıcı ödemesini iskonto tarihinden önce, iskonto tarihinden sonraki bir son ödeme ile kapatma](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[Satıcı alacak dekontları üzerinden iskontosu olan kısmi satıcı ödemesini kapatma](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[Birden fazla iskonto dönemi olan bir kısmi satıcı ödemesini kapatma](settle-partial-vendor-payment-multiple-discount-periods.md)

[Kısmi satıcı ödemesini ve son ödemeyi iskonto tarihinden önce tamamen kapatma](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[Birden fazla müşteri veya satıcı kaydına sahip tek bir fiş](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>Ek kaynaklar

#### <a name="whats-new-and-in-development"></a>Yenilikler ve geliştirilen özellikler

Planlanan yeni özellikleri görmek için [Microsoft Dynamics 365 sürüm planlarına](https://go.microsoft.com/fwlink/?linkid=2010158) bakın. 

#### <a name="blogs"></a>Bloglar

[Microsoft Dynamics 365 blogunda](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) ve [Microsoft Dynamics 365 Finance - Financials blogunda](https://community.dynamics.com/365/financeandoperations/b/financials) Borç hesapları ve diğer çözümler hakkında fikirlere, haberlere ve diğer bilgilere ulaşabilirsiniz.

[Microsoft Dynamics Operations İş Ortağı Topluluk Blogu](https://community.dynamics.com/partner/b/operationspartnercommunityblog)'nda Microsoft Dynamics İş Ortakları'na Dynamics 365'teki yenilikler ve eğilimler hakkında bilgi edinebilecekleri tek bir kaynak sunmaktadır.

#### <a name="community-blogs"></a>Topluluk blogları

[Dynamics 365 Finance'da borçları yönetme](https://financefunction.tech/2019/02/15/how-to-manage-payables-in-dynamics-365-for-finance-and-operations)

#### <a name="task-guides"></a>Görev kılavuzları
Ek yardıma uygulama içinde görev kılavuzları olarak ulaşılabilir. Görev kılavuzlarına erişmek için herhangi bir sayfada Yardım düğmesine tıklayın.

#### <a name="videos"></a>Videolar

Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Kanalı](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ)'nda bulunan nasıl yapılır videolarına hemen göz atın.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]