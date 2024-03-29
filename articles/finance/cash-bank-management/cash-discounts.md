---
title: Nakit iskontoları
description: Nakit iskontoları Borç hesapları ve Alacak hesapları için ayarlanır ve paylaşılır.  Yapılabilecek nakit iskontosu müşteri faturasında veya satıcı faturasında tanımlanabilir ve fatura, nakit iskontosu tarihi geçmeden ödendiği takdirde alınır.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: kfend
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b75637bfb38c13591223ff11be36d958b3972d4f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804149"
---
# <a name="cash-discounts"></a>Nakit iskontoları

[!include [banner](../includes/banner.md)]

Nakit iskontoları Borç hesapları ve Alacak hesapları için ayarlanır ve paylaşılır. Yapılabilecek nakit iskontosu müşteri faturasında veya satıcı faturasında tanımlanabilir ve fatura, nakit iskontosu tarihi geçmeden ödendiği takdirde alınır. 

## <a name="cash-discounts"></a>Nakit iskontoları

Hem müşteriler veya hem de satıcılar için nakit iskontoları, **Nakit iskontoları** sayfasında oluşturulabilir. Ayrıca, önceki nakit iskontosunun vadesi dolduğunda birbirini izleyecek nakit iskontolarını, **Sonraki iskonto kodu** alanını kullanarak tanımlayabilirsiniz. Daha fazla bilgi için bu makalenin devamındaki "Örnek: Nakit iskontoları dizisi" bölümüne bakın. Eğer bir fatura, iade hareketi (ödeme veya alacak dekontu) veya her ikisi, tüzel kişiliğin hesap para birimini farklı bir para biriminde girilirse, nakit iskontosu, ödeme veya alacak dekontunun döviz kuru kullanılarak hesaplanır. Fatura ve iade belgesi farklı tüzel kişiliklere girildiye ve tüzel kişiliklerin muhasebe para birimleri farklıysa, döviz kuru faturanın bir tüzel kişiliğinden kredi belgesine göre alınır. Daha fazla bilgi için bu makalenin devamındaki "Örnek: Nakit için döviz kurları" bölümüne bakın.

## <a name="defaulting-order-of-cash-discount-main-account"></a>Nakit iskontosu ana hesabı varsayılan ilkesi

Bir fatura nakit iskontosu elde etmek için zamanında kapatılmışsa, nakit iskontosu aşağıdaki varsayılan ilkesi önceliğine göre otomatik olarak bir nakit iskontosu ana hesabına nakledilir:
1.  Ana hesap, **Açık hareketleri kapat** sayfası veya **Satıcı açık hareketleri kapat** sayfasındaki **Alternatif nakit iskontosu hesabı** alanında belirtilir.
2.  Ana hesap, Faturaya atanan satış vergisi kodunun Genel muhasebe deftere nakletme grubunun, **Müşteri nakit iskontosu** alanı veya **Satıcı satış iskontosu** alanında belirtilir. Genel muhasebe deftere nakil gruplarını, **Genel muhasebe deftere nakil grupları** sayfasında ayarlayın ve onları satış vergisi koduna **Satış vergisi kodları** sayfasından atayın.
3.  Kapatılmış faturadaki nakit iskontosu kodu için, **Müşteri iskontoları için ana hesap** alanı veya **Satıcı iskontoları için ana hesap** alanı **Nakit iskontolar** sayfasındadır.
4.  Nakit iskontoları için ana hesap, **Otomatik hareketler için hesaplar** sayfasında tanımlandığı gibi.

## <a name="example-series-of-cash-discounts"></a>Örnek: Nakit iskontoları dizisi
Aşağıdaki gibi üç nakit iskontosu kodu ayarlayın:
-   Kod 5D10% – Tutar 5 gün içinde ödendiğinde %10 oranında bir nakit iskontosu.
-   Kod 10D5% – Tutar 10 gün içinde ödendiğinde %5 oranında bir nakit iskontosu.
-   Kod 14D2% - Tutar 14 gün içinde ödendiğinde %2 oranında bir nakit iskontosu.

**Sonraki iskonto kodu** alanında:
-   5D10% kodu için 10D5% seçimini yapın.
-   10D5% kodu için 14D2% seçimini yapın.
-   14D2% kodu için Sonraki iskonto kodu alanını boş bırakın.

Fatura üzerindeki ödeme tarihi, bir önceki nakit indirimi tarihini geçtikçe, üç nakit indirimi bir birini izler. Fatura ödendiğinde nakit iskontosu sırasınndaki hangi nakit iskonto tarihi uyduğuna bağlı olarak, yalnızca bir nakit iskontosu verilir.

## <a name="example-exchange-rates-for-cash-discounts"></a>Örnek: Nakit iskontoları için döviz kurları
Tüzel kişiliğinizin muhasebe para birimi EUR'dur ve aşağıdaki döviz kurları USD için belirtilmiştir:
-   1 Şubat = 110
-   1 Mart = 80

20D2% nakit iskonto koşullarına sahip 1000 USD'lik bir fatura 15 Şubat'ta nakledilir. Faturanın muhasebe para birimi tutarı 1100 EUR'dur. 980 USD için bir ödeme, fatura ile 1 Mart'ta kapatılır. Nakit iskontosu tutarı 20 USD'dir. Ödemenin muhasebe para birimi tutarı 784 Euro'dur. Nakit iskontosu hesap para miktarı, 1 Mart itibariyle döviz kuru kullanılarak hesaplanır: 20 \* 80 / 100 = 16 EUR.

> [!NOTE]
> **Alacak hesapları parametreleri** ya da **Borç hesapları parametreleri** sayfalarında **Kısmi ödemeler için nakit iskontolarını hesapla** seçili olduğunda, her kısmi ödemenin tarihinde geçerli olan döviz kuru kullanılır. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
