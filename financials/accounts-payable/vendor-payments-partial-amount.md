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
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 4d243e6a9a68b69a6b32748344fc606ff3f2d965
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>Bir kısmi tutar için satıcı ödemeleri

Bazen, bir satıcıya bir fatura tutarından daha az ödeme yapabilirsiniz. Bu makalede, bu durumu çözmeye yönelik çeşitli seçenekler açıklanmaktadır. Kullanabileceğiniz seçenekler, iş gereksinimlerinize ve yapılandırmanıza bağlıdır. 

<a name="cash-discount-amounts"></a>Nakit iskontosu tutarları
---------------------

Bir satıcı fatura vade tarihinden önce ödeme yapmanız durumunda size bir nakit iskontosu sunabilir. Örneğin, faturanın 10 gün içinde ödenmesi durumunda yüzde 2 nakit indirimi belirten, 100,00 değerinde bir fatura girebilirsiniz. Vade dönemi 30 gündür. Bir ödeme teklifi nakit iskontosunun fatura seçmek için bir ölçüt olarak kullanır ve teklif nakit iskontosu tarihinden önce çalıştırılırsa, fatura ödeme için seçilir ve ödeme 98.00 için oluşturulur. Nakit iskontosu el ile oluşturulan özel bir ödeme için de alınabilir.

## <a name="partial-payments-with-cash-discounts"></a>Nakit iskontolarıyla kısmi ödemeler
Bir kısmi ödeme yaptığınızda faturayı tamamen kapatmak için ek bir kısmi ödeme yapmayı planlıyor olabilirsiniz. Kısmi ödeme için bir nakit iskontosu almak için ayarlamanız gerekir ** kısmi ödemeler için nakit iskontolarını hesaplamak ** için seçenek **Evet** üzerinde **Hesap Borç parametreleri** sayfa. 

Örneğin, faturanın hazırlandıktan sonra 10 gün içinde ödenmesi durumunda yüzde 2'lik bir nakit iskontosu alıyorsunuz. 100.00 değerinde bir fatura nakledilir. 10 gün içinde 49.00 ödeme yaparsanız, 49.00 borç ödeme günlüğünde girin. Ne zaman, kapatmak istediğiniz kısmi ödemenin üzerinde **açık kapanış hareketleri** sayfası, **1.00** görünür **yararlanmak için nakit iskontosu tutarı** alan. 

> [!NOTE] 
> Kısmi ödeme girin ve tam fatura tutarı bırakın **kapatılacak tutar** alan **yararlanmak için nakit iskontosu tutarı** alan hareketleri deftere naklettiğinizde otomatik olarak yeniden.

## <a name="credit-notes-with-cash-discounts"></a>İskonto indirimleri içeren credit note'lar
Bir faturadaki ürünlerden bazılarını iade edebilir ve bir credit note hazırlayabilirsiniz. Orijinal faturadan bir nakit iskontosu almışsanız iskonto değerini çıkarabilir ve doğru tutar için bir iade alabilirsiniz. Varsa ** alacak dekontları için nakit iskontolarını hesaplamak ** seçeneği ayarlanmış **Evet** üzerinde **hesaplarına borç parametreleri** sayfa, iskonto otomatik olarak alacak dekontu için hesaplanır. 

Örneğin, faturanın hazırlandıktan sonra 10 gün içinde ödenmesi durumunda yüzde 2'lik bir nakit iskontosu alıyorsunuz. 100.00 tutarında bir fatura nakledilir. Mal iadesi ve kredi notu almak, alacak dekontu ile birlikte iade faturasına ayrıca tanımlanır yüzde 2 oranında nakit iskontosu 100,00 orijinal fatura tutarının tamamı için girebilirsiniz.  Üzerinde kredi notu görüntülerken **kapatma hareketleri** sayfası, **98.00** görünür **kapatılacak tutar** alan, ve **-2.00** yer **nakit iskontosu tutarı** alan. İskonto tutarı, bir nakit iskontosu hesabına nakledilir.

## <a name="overpaymentunderpayment-amounts"></a>Fazla ödeme/eksik ödeme tutarları
Hala kapatılması gereken tutar çok küçük ise bir kısmi ödeme gerçekleştirebilirsiniz. Örneğin, satıcı faturası, 1.000,00 tutarındayken 999.90 tutarında bir ödeme yaptınız. Kalan tutar, **Borç hesapları parametreleri** sayfasında fazla ödemeler veya eksik ödemeler için tanımlanan tutarın altındaysa bu ark otomatik olarak bir fazla ödeme/eksik ödeme defter hesabına nakledilir.


