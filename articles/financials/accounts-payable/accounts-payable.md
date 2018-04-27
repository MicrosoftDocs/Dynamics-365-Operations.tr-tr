---
title: "Borç hesapları giriş sayfası"
description: "Bu konu, Borç hesapları konusuna genel bir bakış sağlar."
author: twheeloc
manager: AnnBe
ms.date: 08/18/2017
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 21901
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7bc09cbd108949b37ea1b2207fc3e0c6961abf4b
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---

# <a name="accounts-payable-home-page"></a>Borç hesapları giriş sayfası

[!INCLUDE [banner](../includes/banner.md)]

Bu konu, Borç hesapları konusuna genel bir bakış sağlar. 

Satıcı faturalarını el ile girebilir veya bir veri varlığı aracılığıyla elektronik olarak alabilirsiniz. Faturalar girildikten veya alındıktan sonra, bir fatura onay günlüğü veya **Satıcı faturası** sayfasını kullanarak faturaları gözden geçirebilir veya onaylayabilirsiniz. Belirli ölçütlere uyan faturaların otomatik olarak onaylanması için fatura eşleştirme, satıcı fatura ilkeleri ve iş akışını kullanarak gözden geçirme işlemini otomatikleştirebilirsiniz. Kalan faturalar, yetkili kullanıcı tarafından gözden geçirilmek üzere işaretlenir.

**İş süreçleri**

[![İş süreci](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>Borç hesaplarını kurma

Satıcı grupları, satıcılar, deftere nakil profilleri, çeşitli ödeme seçenekleri ve satıcılara yönelik parametreler, masraflar, teslimatlar ve gönderilecek yerler, senetler ve diğer türdeki Borç hesapları bilgilerini oluşturun. 

[Borç hesaplarını yapılandırma](accounts-payable-overview.md)

[Satıcı faturaları için muhasebe dağılımları ve yardımcı defter günlüğü girdileri](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[Borç hesapları ve Alacak hesapları için yabancı para birimi yeniden değerleme işlemi](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>Satıcı faturalarını yapılandırma

Faturaları ve satıcılara yapılan harcamaları izlemek için Borç hesapları bölümünü kullanın.

[Borç hesapları fatura eşleştirmesi](accounts-payable-invoice-matching.md)

[Satıcı deftere nakil profilleri](vendor-posting-profiles.md)

[Borç hesapları fatura eşleştirme doğrulaması ayarlama](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[Üç yönlü eşleştirme ilkeleri](three-way-matching-policies.md)

[Fatura eşleştirme ve şirketlerarası satınalma siparişleri](invoice-matching-intercompany-purchase-orders.md)

[Fatura toplamları eşleştirme sırasında uyuşmazlıkları çözümleme](resolve-invoice-totals-invoice-matching-discrepancies.md)

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

[Satıcı çekleri için elektronik raporlama](electronic-reporting-sample-vendor-checks.md)

[Satıcı ödemesini tersine çevirme](reverse-vendor-payment.md)

[Ön ödeme faturaları ve ön ödemelere genel bakış](prepayments-invoices-vs-prepayments.md)

[Borç hesapları için merkezi ödemeler](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>Kapatmalar

Aşağıdaki konular kapatmalar hakkında bilgi sağlar. Kapatma, ödemeleri faturalarla kapatma işlemidir. 

[Kapatma yapılandırma](../cash-bank-management/configure-settlement.md)

[Kısmi satıcı ödemesini iskonto tarihinden önce kapatma](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[Satıcı alacak dekontları üzerinden iskontosu olan kısmi satıcı ödemesini kapatma](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[Birden fazla iskonto dönemi olan bir kısmi satıcı ödemesini kapatma](settle-partial-vendor-payment-multiple-discount-periods.md)

[Kısmi satıcı ödemesini veya son ödemeyi iskontodan önce kapatma](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[Birden fazla müşteri veya satıcı kaydına sahip tek bir fiş](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>Ek kaynaklar

#### <a name="whats-new-and-in-development"></a>Geliştirmedeki yenilikler

Yayımlanmış ve geliştirilmekte olan yeni özellikleri görmek için [Microsoft Dynamics 365 Yol Haritası](https://roadmap.dynamics.com/) bölümüne gidin. 

#### <a name="blogs"></a>Bloglar

[Microsoft Dynamics 365 blogunda](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) Borç hesapları ve diğer çözümler hakkında fikirlere, haberlere ve diğer bilgilere ulaşabilirsiniz.

[Microsoft Dynamics AX ürün ekibi blogunda](https://blogs.msdn.microsoft.com/dax/), Borç hesapları hakkında pek çok ileti bulunmaktadır. Bu gönderilerin bazıları Borç hesaplarının önceki sürümü için yazılmıştır ancak aynı kavramlar hala geçerlidir ve yordamlar da geçerli sürümdekine benzerdir.

[Microsoft Dynamics Operations İş Ortağı Topluluğu Blogu](https://community.dynamics.com/partner/b/operationspartnercommunityblog), Microsoft Dynamics İş Ortakları'na MBS Operations'daki yenilikler ve eğilimler hakkında bilgi edinebilecekleri tek bir kaynak sunar.

#### <a name="task-guides"></a>Görev kılavuzları
Ek yardıma Finance and Operations içinde görev kılavuzları olarak ulaşılabilir. Görev kılavuzlarına erişmek için herhangi bir sayfada Yardım düğmesine tıklayın.

#### <a name="videos"></a>Videolar

[Microsoft Dynamics 365 YouTube Kanalında](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) bulunan nasıl yapılır videolarına hemen göz atın.





