---
title: Bir kısmi tutar için satıcı ödemeleri
description: Bazen, bir satıcıya bir fatura tutarından daha az ödeme yapabilirsiniz. Bu makale, bu durumda yapılabilecek çeşitli seçenekleri açıklamaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2644e0a27eff3e45ddcddb89c9aac9230190788f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "318914"
---
# <a name="vendor-payments-for-a-partial-amount"></a>Bir kısmi tutar için satıcı ödemeleri

[!include [banner](../includes/banner.md)]

Bazen, bir satıcıya bir fatura tutarından daha az ödeme yapabilirsiniz. Bu makalede, bu durumu çözmeye yönelik çeşitli seçenekler açıklanmaktadır. Kullanabileceğiniz seçenekler, iş gereksinimlerinize ve yapılandırmanıza bağlıdır. 

<a name="cash-discount-amounts"></a>Nakit iskontosu tutarları
---------------------

Bir satıcı fatura vade tarihinden önce ödeme yapmanız durumunda size bir nakit iskontosu sunabilir. Örneğin, faturanın 10 gün içinde ödenmesi durumunda yüzde 2 nakit indirimi belirten, 100,00 değerinde bir fatura girebilirsiniz. Vade dönemi 30 gündür. Bir ödeme teklifi, bir faturanın seçiminde ölçüt olarak nakit iskontosu kullanıyorsa ve teklif nakit iskontosu tarihinde veya öncesinde çalışıyorsa, fatura ödeme için seçilir ve 98.00 için ödeme oluşturulur. Bir nakit iskontosu el ile oluşturulan özel bir ödeme için de alınabilir.

## <a name="partial-payments-with-cash-discounts"></a>Nakit iskontolarıyla kısmi ödemeler
Bir kısmi ödeme yaptığınızda faturayı tamamen kapatmak için ek bir kısmi ödeme yapmayı planlıyor olabilirsiniz. Bir kısmi ödeme için bir nakit iskontosu almak için, **Borç hesapları parametreleri** sayfasından **Kısmi ödemeler için nakit iskontolarını hesapla** seçeneğini **Evet** konumuna ayarlamanız gerekir. 

Örneğin, faturanın hazırlandıktan sonra 10 gün içinde ödenmesi durumunda yüzde 2'lik bir nakit iskontosu alıyorsunuz. 100.00 değerinde bir fatura nakledilir. 10 gün içinde 49,00 tutarında bir ödeme yaparsanız, ödeme defterine 49,00 tutarında bir borç girersiniz. Kısmi ödemeyi **Açık hareketleri kapat** sayfasında kapatırsanız **Alınacak nakit iskonto tutar** alanında **1,00** tutarı görüntülenir. 

> [!NOTE] 
> Bir kısmi ödeme girer ve **Kapatılacak tutar** alanındaki tam fatura tutarını değiştirmeden bırakırsanız, hareketleri naklettiğinizde **Alınacak nakit iskontosu tutarı** alanı otomatik olarak yeniden hesaplanır.

## <a name="credit-notes-with-cash-discounts"></a>İskonto indirimleri içeren credit note'lar
Bir faturadaki ürünlerden bazılarını iade edebilir ve bir credit note hazırlayabilirsiniz. Orijinal faturadan bir nakit iskontosu almışsanız iskonto değerini çıkarabilir ve doğru tutar için bir iade alabilirsiniz. **Credit note'lar için nakit iskontolarını hesapla**seçeneğini **Borç hesapları parametreleri** sayasından **Evet** konumuna getirirseniz credit note üzerinden iskonto otomatik olarak hesaplanır. 

Örneğin, faturanın hazırlandıktan sonra 10 gün içinde ödenmesi durumunda yüzde 2'lik bir nakit iskontosu alıyorsunuz. 100.00 tutarında bir fatura nakledilir. Mal iade edip ve alacak dekontu alırsanız, alacak dekontunda da tanımlanmış olan yüzde 2'lik nakit iskontosuyla birlikte 100,00 orijinal fatura toplam tutarı için alacak dekontu girebilirsiniz.  Alacak dekontunu **Hareketleri kapat** sayfasında görüntülediğinizde **Kapatılacak tutar** alanında **98,00** tutar ve **Nakit iskontosu tutarı** alanında **-2,00** tutar görüntülenir. İskonto tutarı, bir nakit iskontosu hesabına nakledilir.

## <a name="overpaymentunderpayment-amounts"></a>Fazla ödeme/eksik ödeme tutarları
Hala kapatılması gereken tutar çok küçük ise bir kısmi ödeme gerçekleştirebilirsiniz. Örneğin, satıcı faturası, 1.000,00 tutarındayken 999.90 tutarında bir ödeme yaptınız. Kalan tutar, **Borç hesapları parametreleri** sayfasında fazla ödemeler veya eksik ödemeler için tanımlanan tutarın altındaysa bu ark otomatik olarak bir fazla ödeme/eksik ödeme defter hesabına nakledilir.


Daha fazla bilgi için bkz. [Satıcı ödeme genel bakışı](../cash-bank-management/tasks/vendor-payment-overview.md).
