---
title: "Bir kısmi tutar için satıcı ödemeleri"
description: "Bazen, bir satıcıya bir fatura tutarından daha az ödeme yapabilirsiniz. Bu makalede, bu durumu çözmeye yönelik çeşitli seçenekler açıklanmaktadır. Kullanabileceğiniz seçenekler, iş gereksinimlerinize ve yapılandırmanıza bağlıdır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: eeed8bc4ad0fc24b04055e26bb33c2c56856c52b
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>Bir kısmi tutar için satıcı ödemeleri

[!include[banner](../includes/banner.md)]


Bazen, bir satıcıya bir fatura tutarından daha az ödeme yapabilirsiniz. Bu makalede, bu durumu çözmeye yönelik çeşitli seçenekler açıklanmaktadır. Kullanabileceğiniz seçenekler, iş gereksinimlerinize ve yapılandırmanıza bağlıdır. 

<a name="cash-discount-amounts"></a>Nakit iskontosu tutarları
---------------------

Bir satıcı fatura vade tarihinden önce ödeme yapmanız durumunda size bir nakit iskontosu sunabilir. Örneğin, faturanın 10 gün içinde ödenmesi durumunda yüzde 2 nakit indirimi belirten, 100,00 değerinde bir fatura girebilirsiniz. Vade dönemi 30 gündür. Bir ödeme teklifi, bir faturanın seçiminde ölçüt olarak nakit iskontosu kullanıyorsa ve teklif nakit iskontosu tarihinde veya öncesinde çalışıyorsa, fatura ödeme için seçilir ve 98.00 için ödeme oluşturulur. Bir nakit iskontosu el ile oluşturulan özel bir ödeme için de alınabilir.

## <a name="partial-payments-with-cash-discounts"></a>Nakit iskontolarıyla kısmi ödemeler
Bir kısmi ödeme yaptığınızda faturayı tamamen kapatmak için ek bir kısmi ödeme yapmayı planlıyor olabilirsiniz. Bir kısmi ödeme için bir nakit iskontosu almak için, **Borç hesapları parametreleri** sayfasından **Kısmi ödemeler için nakit iskontolarını hesapla** seçeneğini **Evet** olarak ayarlamanız gerekir. 

Örneğin, faturanın hazırlandıktan sonra 10 gün içinde ödenmesi durumunda yüzde 2'lik bir nakit iskontosu alıyorsunuz. 100.00 değerinde bir fatura nakledilir. 10 gün içinde 49,00 tutarında bir ödeme yaparsanız, ödeme defterine 49,00 tutarında bir borç girersiniz. Kısmi ödemeyi **Açık hareketleri kapat** sayfasında kapatırsanız **Alınacak nakit iskonto tutar** alanında **1,00** tutarı görüntülenir. 

> [!NOTE] 
> Bir kısmi ödeme girer ve **Kapatılacak tutar** alanındaki tam fatura tutarını değiştirmeden bırakırsanız, hareketleri naklettiğinizde **Alınacak nakit iskontosu tutarı** alanı otomatik olarak yeniden hesaplanır.

## <a name="credit-notes-with-cash-discounts"></a>İskonto indirimleri içeren credit note'lar
Bir faturadaki ürünlerden bazılarını iade edebilir ve bir credit note hazırlayabilirsiniz. Orijinal faturadan bir nakit iskontosu almışsanız iskonto değerini çıkarabilir ve doğru tutar için bir iade alabilirsiniz. **Alacak dekontları için nakit iskontolarını hesapla** seçeneğini **Borç hesapları parametreleri** sayfasından **Evet**'e getirirseniz, alacak dekontu için iskonto otomatik olarak hesaplanır. 

Örneğin, faturanın hazırlandıktan sonra 10 gün içinde ödenmesi durumunda yüzde 2'lik bir nakit iskontosu alıyorsunuz. 100.00 tutarında bir fatura nakledilir. Mal iade edip ve alacak dekontu alırsanız, alacak dekontunda da tanımlanmış olan yüzde 2'lik nakit iskontosuyla birlikte 100,00 orijinal fatura toplam tutarı için alacak dekontu girebilirsiniz.  Alacak dekontunu **Hareketleri kapat** sayfasında görüntülediğinizde **Kapatılacak tutar** alanında **98,00** tutar ve **Nakit iskontosu tutarı** alanında **-2,00** tutar görüntülenir. İskonto tutarı, bir nakit iskontosu hesabına nakledilir.

## <a name="overpaymentunderpayment-amounts"></a>Fazla ödeme/eksik ödeme tutarları
Hala kapatılması gereken tutar çok küçük ise bir kısmi ödeme gerçekleştirebilirsiniz. Örneğin, satıcı faturası, 1.000,00 tutarındayken 999.90 tutarında bir ödeme yaptınız. Kalan tutar, **Borç hesapları parametreleri** sayfasında fazla ödemeler veya eksik ödemeler için tanımlanan tutarın altındaysa bu ark otomatik olarak bir fazla ödeme/eksik ödeme defter hesabına nakledilir.




