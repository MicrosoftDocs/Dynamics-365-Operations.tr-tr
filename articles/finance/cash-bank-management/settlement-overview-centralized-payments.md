---
title: Merkezi ödemeler için kapatmaya genel bakış
description: Bu makale, Microsoft Dynamics 365 Finance için merkezi ödeme kapatmalarını açıklar.
author: angelad116
ms.date: 11/22/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "222414"
- intro-internal
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42c359edbe49af151ac76c9873c0d429bbe1ca12
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804239"
---
# <a name="settlement-overview-for-centralized-payments"></a>Merkezi ödemeler için kapatmaya genel bakış

[!include [banner](../includes/banner.md)]

Birden çok tüzel kişilik içeren kuruluşlar tüm ödemeleri yöneten bir tüzel kişilik kullanarak ödemeleri oluşturabilir ve yönetebilirler. Bu, aynı hareketi birden fazla tüzel kişiliğe girme gereksinimini ortadan kaldırır ve merkezi ödemeler için ödeme teklifi işlemi, kapatma işlemi, açık hareket düzenleme ve kapalı hareket düzenleme akışını sağlayarak zaman kazandırır. 

Bir tüzel kişiliğe müşteri veya satıcı ödemesi girildiğinde ve başka bir tüzel kişilik için girilen bir faturayla kapatıldığında, uygulanabilen kapatma, vade sonu ve vade başlangıç hareketleri her tüzel kişilik için otomatik olarak oluşturulur. Hareketteki her fatura ve ödeme birleşimi için bir kapatma kaydı oluşturulur. Her kapatma kaydına, müşteriler için **Alacak hesapları parametreleri** sayfasında ve satıcılar için **Borç hesapları parametreleri** sayfasında belirtilen ödeme fişi numara serisini temel alan yeni bir fiş numarası atanır. 

Nakit iskontoları, yabancı para birimi yeniden değerleme işlemleri, kuruş farkları, fazla ödemeler veya eksik ödemeler için ek kapatma kayıtları oluşturulursa, bunlar ödeme veya fatura hareketinin daha sonraki tarihine atanır. Kapatma, ödeme deftere nakledildikten sonra gerçekleşirse, kapatma kayıtları **Açık hareketleri kapat** sayfasında belirtilen kapatma deftere nakil tarihini kullanır.

## <a name="posting-types-transaction-types-and-default-descriptions"></a>Deftere nakil türleri, hareket türleri ve varsayılan açıklamalar

Şirketlerarası kapatma fişi hareketleri şirketlerarası kapatma deftere nakil türünü, şirketlerarası müşteri kapatmayı ve şirketlerarası satıcı kapatma hareket türlerini kullanır. Hareket türüne yönelik bilgileri **Varsayılan açıklamalar** sayfasında ayarlayabilirsiniz. 

Aşağıdaki hareket tipleri tek bir şirket veya şirketlerarası kapatma işlemleri için kullanılabilir:

-   Kapatma
-   Nakit iskontosu
-   Yabancı para birimi yeniden değerleme işlemi (gerçekleşmiş ve gerçekleşmemiş yabancı para birimi yeniden değerleme işlemleri dahil)
-   Kuruş farkı
-   Fazla ödeme/eksik ödeme

Ayrıca şirketlerarası kapanış fişleri için varsayılan açıklamalar da oluşturabilirsiniz.

## <a name="currency-exchange-gains-or-losses"></a>Döviz kuru kazançları veya kayıpları

Müşteri veya satıcı hareketleri için kullanılan döviz kuru, hareketle birlikte depolanır. Döviz kuruyla ilgili olarak gerçekleşen kazançlar veya kayıplar ödemenin tüzel kişiliğine ait **Şirketlerarası muhasebe** sayfasındaki **Döviz kuru kazancını veya kaybını deftere naklet** alanında belirlenmiş olan seçeneğe bağlı olarak, faturanın tüzel kişiliğine veya ödemenin tüzel kişiliğine nakledilir. Aşağıdaki örneklerde bu para birimleri kullanılır:
-   Ödeme muhasebe para birimi: Euro
-   Fatura muhasebe para birimi: ABD Doları
-   Ödeme hareketi para birimi: DKK
-   Fatura hareketi para birimi: Kanada Doları

### <a name="currency-calculations"></a>Para birimi hesaplamaları

Bir tüzel kişiliğe girilen fatura, başka bir tüzel kişiliğe girilen ödemeyle kapatılıyorsa, ödemenin hareket para birimi (DKK) üç adımda dönüştürülür:
1.  Ödeme tüzel kişiliğinin döviz kurları kullanılarak, ödemenin muhasebe para birimine dönüştürülür (Euro).
2.  Faturanın muhasebe para birimine dönüştürülür (ABD Doları).
3.  Faturanın tüzel kişiliğinin döviz kurları kullanılarak, faturanın hareket para birimine dönüştürülür (Kanada Doları).

Dönüştürme işlemi ödeme tarihindeki döviz kurlarını kullanır. İşlem sonucunda faturanın hareket para birimindeki (CAD) ödeme tutarı fatura tutarına (CAD) eşitse, fatura tümüyle ödenmiş olarak kabul edilir. 

**Açık hareketleri kapat** sayfası ödeme tutarının girilmediği bir ödeme günlüğünden açıldığında, kapatılacak tutar **Açık hareketleri kapat** sayfasında kapatılmak üzere seçilen faturalara göre hesaplanır. Kapatılacak tutar üç adımda dönüştürülür:
1.  Faturanın tüzel kişiliğinin ödeme tarihindeki döviz kurları kullanılarak, faturanın muhasebe para birimine dönüştürülür (ABD Doları).
2.  Faturanın tüzel kişiliğinin ödeme tarihindeki döviz kurları kullanılarak, ödemenin muhasebe para birimine dönüştürülür (Euro).
3.  Ödemenin hareket para birimine dönüştürülür (DKK).

Sonuç olarak elde edilen ödeme tutarı, **Açık hareketleri kapat** sayfasını kapattığınızda ödeme günlüğü satırına transfer edilir.

### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a>Farklı muhasebe para birimleri nedeniyle oluşan kazancı veya kaybı deftere nakletme

Döviz kuru kazancı veya kaybı oluşursa, kazanç ya da kayıp ödemenin tüzel kişiliğine ait **Şirketlerarası muhasebe** sayfasındaki **Döviz kuru kazancını veya kaybını deftere naklet** alanı için belirtilen tüzel kişiliğe nakledilir. Kazanç veya kayıp, nakledildiği tüzel kişiliğin muhasebe para birimine, söz konusu tüzel kişilik için tanımlanan döviz kuru kullanılarak dönüştürülür.

## <a name="cash-discounts"></a>Nakit iskontoları

Şirketlerarası kapatma işlemi sırasında oluşturulan nakit iskontoları, ödemenin tüzel kişiliğine ait **Şirketlerarası muhasebe** sayfasındaki **Nakit iskontosunu deftere naklet** alanı için belirtilen seçeneğe bağlı olarak, faturanın tüzel kişiliğine veya ödemenin tüzel kişiliğine nakledilir. Faturanın tüzel kişiliğinde, buna karşılık gelen kapatma hareketi oluşturulur.

## <a name="overpayments-and-underpayments"></a>Fazla ödemeler ve eksik ödemeler

Fazla ödeme, eksik ödeme ve kuruş farkı toleransları, fazla ödemeler için ödemenin tüzel kişiliğine, eksik ödemeler için faturanın tüzel kişiliğine göre belirlenir. Kullanılan deftere nakil hesabı, müşterinin **Alacak hesapları parametreleri** sayfasındaki **Nakit iskontosu yönetimi** alanında ve satıcının **Borç hesapları parametreleri** sayfasındaki **Nakit iskontosu yönetimi** alanındaki ayara göre belirlenir.

-   Nakit iskontosu yönetimi ayarı **Belirli** ise veya ayar **Belirsiz** ise ve uygun nakit iskontosu fazla ödemeden farklı bir tüzel kişiliğe nakledildiyse, Müşteri nakit iskontosu, Satıcı nakit iskontosu veya Muhasebe para birimi cinsinden kuruş farkı için otomatik hesap kullanılır. Bu hesapları **Otomatik hareketler için hesaplar** sayfasından belirleyebilirsiniz.
-   Nakit iskontosu yönetimi ayarı **Belirsiz** ise ve fazla ödemeye ilişkin tüzel kişilikle aynı şirkete nakledilirse, (ödemenin tüzel kişiliği ile faturanın tüzel kişiliği aynıdır), nakit iskontosu hesabı düzeltilir. Örneğin, kullanılabilen 3,00 tutarında nakit iskontosu olan 100,00 tutarında bir fatura 98,00 tutarında bir ödemeyle kapatılırsa, nakit iskontosu hesabı 1,00 tutarı için düzeltilir. Net iskonto tutarı 2,.00'dır.
-   Nakit iskontosu yönetimi ayarı **Belirsiz** ise, nakit iskontosu fazla ödemeye ilişkin tüzel kişilikle aynı tüzel kişiliğe nakledilir ve fazla ödeme veya eksik ödeme nakit iskontosu olan birden çok faturayla kapatılır, nakit iskontosu hesabı son fatura için düzeltilir.

Nakit iskontosu yönetimi seçimi **Belirsiz** ise, belirli olmayan ödeme kapatma kuralları yalnızca aşağıdaki durumlarda uygulanır:
-   Fazla ödeme varsa.
-   Fazla ödeme, nakit iskontosu olan bir veya daha fazla faturayla kapatılırsa.
-   Nakit iskontosu fazla ödemeye ilişkin tüzel kişilikle aynı tüzel kişiliğe nakledilirse.

Diğer tüm durumlarda, fazla ödemeler veya eksik ödemeler Müşteri nakit iskontosu, Satıcı nakit iskontosu veya Muhasebe para birimi cinsinden kuruş farkı için otomatik hesaba nakledilir.

## <a name="sales-tax"></a>Satış vergisi
Satış vergisi hareketleri, esas defter nakledildikleri tüzel kişilikte kalır. 

Satış vergileri ön ödeme için deftere nakledildiyse şirketlerarası kapatma, ön ödemenin tüzel kişiliğindeki ön ödemede bulunan satış vergisine ters işlem uygular. Faturanın tüzel kişiliğindeki vergiler faturanın tüzel kişiliğinde kalır.

## <a name="financial-dimensions"></a>Mali boyutlar
Müşteri ödemelerinde, ödemenin tüzel kişiliğindeki vade sonu ve vade başlangıcı hareketleri, kapatılmakta olan ödemedeki alacak hesapları özet hesabı için belirtilen mali boyutları kullanır. Faturanın tüzel kişiliğinde, vade sonu ve vade başlangıcı hareketleri kapatılmakta olan faturadaki alacak hesapları özet hesabı için belirtilen mali boyutları kullanır. 

Satıcı ödemelerinde, ödemenin tüzel kişiliğindeki vade sonu ve vade başlangıcı hareketleri, kapatılmakta olan ödemedeki borç hesapları özet hesabı için belirtilen mali boyutları kullanır. Faturanın tüzel kişiliğinde, vade sonu ve vade başlangıcı hareketleri kapatılmakta olan faturadaki borç hesapları özet hesabı için belirtilen mali boyutları kullanır.

## <a name="withholding-tax"></a>Stopaj vergisi
Fatura ile ilişkili satıcı hesabı stopaj vergisinin hesaplanmasının gerekip gerekmediğini belirlemek için kullanılır. Stopaj vergisi varsa, faturayla ilişkilendirilmiş tüzel kişilikte hesaplanır. Tüzel kişilikler farklı para birimleri kullanıyorsa fatura ile ilişkilendirilmiş tüzel kişiliğin döviz kuru kullanılır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
