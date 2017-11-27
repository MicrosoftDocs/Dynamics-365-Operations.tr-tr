---
title: "Bir kısmi tutar için müşteri ödemeleri"
description: "Bazen müşteriler, faturanın toplam miktarından az olan bir ödeme yaparlar. Bu makale, bu durumda yapılabilecek çeşitli seçenekleri açıklamaktadır. Kullanabileceğiniz seçenekler, iş gereksinimlerinize ve yapılandırmanıza bağlıdır."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c2ba17b97bf7a00ff111e72314e98f5af7aaed80
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="customer-payments-for-a-partial-amount"></a>Bir kısmi tutar için müşteri ödemeleri

[!include[banner](../includes/banner.md)]


Bazen müşteriler, faturanın toplam miktarından az olan bir ödeme yaparlar. Bu makale, bu durumda yapılabilecek çeşitli seçenekleri açıklamaktadır. Kullanabileceğiniz seçenekler, iş gereksinimlerinize ve yapılandırmanıza bağlıdır.

<a name="partial-payment-with-no-discount"></a>İskontosuz kısmi ödeme
--------------------------------

Müşteriler, faturayı tam olarak ödeyebilmek için ellerinde yeterli nakit paraları olmadığından veya faturadaki bir ürün için bir anlaşmazlık bulunduğundan kısmi ödeme yaparlar. Bu durumda fatura, ödeme ile birlikte kısmen kapatılabilir. Fatura açık kalır ve bir bakiyeyi gösterir.

## <a name="discount-amounts"></a>İskonto tutarları
Müşterilere fatura vade tarihinden önce ödeme yapmaları durumunda bir nakit iskontosu sunabilirsiniz. Örneğin, faturanın 10 gün içinde ödenmesi durumunda yüzde 2 nakit indirimi belirten, 100,00 değerinde bir fatura girebilirsiniz. Vade dönemi 30 gündür. 10 gün içinde 98.00 tutarında bir ödeme alırsanız, ödeme için 98.00 girersiniz. Daha sonra fatura kapatılmak üzere işaretlenir ve nakit iskontosu otomatik olarak alınır.

## <a name="partial-payments-with-cash-discounts"></a>Nakit iskontolarıyla kısmi ödemeler
Müşteriler kısmi ödeme yaptığında faturayı tamamen kapatmak için ek bir kısmi ödeme yapmayı planlıyor olabilirsiniz. Bir kısmi ödeme için bir nakit iskontosu almak için, **Alacak hesapları parametreleri** sayfasından **Kısmi ödemeler için nakit iskontolarını hesapla** seçeneğini **Evet** konumuna ayarlamanız gerekir. 

Örneğin, faturanın hazırlandıktan sonra 10 gün içinde ödenmesi durumunda yüzde 2'lik bir nakit iskontosu veriyorsunuz. 100.00 değerinde bir fatura nakledilir. 10 gün içinde 49.00 tutarında bir ödeme alırsanız, ödeme defterine 49.00 tutarında bir borç girersiniz. Kısmi ödemeyi **Kapatma işlemleri** sayfasında kapatırsanız **Alınacak nakit iskonto tutar** alanında **1.00** tutarı görüntülenir. İskonto tutarı, bir nakit iskontosu hesabına nakledilir. 

> [!NOTE] 
> Bir kısmi ödeme girer ve **Kapatılacak tutar** alanındaki tam fatura tutarını değiştirmeden bırakırsanız, hareketleri naklettiğinizde **Alınacak nakit iskontosu tutarı** alanı otomatik olarak yeniden hesaplanır.

## <a name="credit-notes-with-discounts"></a>İskonto içeren credit note'lar
Müşteriler bir faturadaki ürünlerden bazılarını iade ederse bir credit note hazırlayabilirsiniz. Orijinal faturada bir nakit iskontosu yapılırsa müşteriye yönelik credit memo, müşteri tarafından alınmış olan nakit iskontosunun neti olmalıdır. **Alacak hesapları parametreleri** sayfasından **Credit note'ları için nakit iskontolarını hesapla** seçeneğini **Evet** konumuna ayarlarsanız credit note için iskonto otomatik olarak hesaplanır.  

Örneğin, faturanın hazırlandıktan sonra 10 gün içinde ödenmesi durumunda yüzde 2'lik bir nakit iskontosu veren bir ödeme süresi önerdiniz. 100.00 tutarında bir fatura nakledildi ve müşteri, nakit iskontosunu aldı. Müşteri malları iade ederse ve bir credit note hazırlarsanız 100.00 için credit note girebilirsiniz. Credit note'u **Açık hareketleri kapat** sayfasında görüntülediğinizde **Kapatılacak tutar** alanında **98.00** tutarı ve **Nakit iskontosu tutarı** alanında **-2.00** tutarı görüntülenir. İskonto tutarı, bir nakit iskontosu hesabına nakledilir.

## <a name="overpaymentunderpayment-amounts"></a>Fazla ödeme/eksik ödeme tutarları
Müşteriler bir ödeme yaptığında, hala kapatılması gereken çok küçük bir miktar kalabilir. Örneğin, müşteriye 1.000,00 fatura kestiniz ve müşteri 999.90 ödedi. Kalan tutar,**Alacak hesapları parametreleri** sayfasında belirtilen fazla ödeme veya eksik ödeme tutarının altında kalıyorsa fark otomatik olarak bir fazla ödeme/eksik ödeme defter hesabına nakledilir.

## <a name="full-settlement"></a>Tam kapatma
**Hesap borç parametreleri** sayfasında kalan tutar ödenmeyecek ama eksik ödeme tutarından büyük olduğunda, müşteriler kısmi ödeme yapabiliriler. Faturayı tamamen kapatılmış olarak işaretlemek istiyorsanız, **Hareketi kapat** sayfası üzerinde **Tam kapatma** seçeneğini kullanabilirsiniz. (Tam kapatma işlevini bir konfigürasyon anahtarı kullanarak etkinleştirebilirsiniz.) Örneğin, 1,000.00 tutarı için bir fatura nakledildi ve müşteri 990.00 tutarında bir ödeme yaptı. Müşterinin kalan 10,00'u ödemek zorunda olmadığını kabul ettiniz.. Faturayı kapatmak üzere işaretledikten sonra, **Tam kapatma**'yı da seçebilirsiniz. Fatura bu durumda tam olarak kapatılmış olarak değerlendirilir. 10.00 tutarındaki fark ise bir nakit iskontosu hesabına bir ilave nakit iskontosu tutarı olarak nakledilir.


Daha fazla bilgi için bkz. [Müşteri ödemlerini havale etme](tasks/deposit-customer-payments.md).

