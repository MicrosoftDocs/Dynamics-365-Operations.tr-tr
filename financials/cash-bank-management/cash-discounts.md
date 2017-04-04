---
title: "Nakit iskontoları"
description: "Nakit iskontoları Borç hesapları ve Alacak hesapları için ayarlanır ve paylaşılır.  Yapılabilecek nakit iskontosu müşteri faturasında veya satıcı faturasında tanımlanabilir ve fatura, nakit iskontosu tarihi geçmeden ödendiği takdirde alınır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 44d51807cd6bb64ae2c4bef58d8a445417ffa3a9
ms.openlocfilehash: 741b41e005be963aa3548a56faa1310e7cf4d2de
ms.lasthandoff: 03/31/2017


---

# <a name="cash-discounts"></a>Nakit iskontoları

Nakit iskontoları Borç hesapları ve Alacak hesapları için ayarlanır ve paylaşılır.  Yapılabilecek nakit iskontosu müşteri faturasında veya satıcı faturasında tanımlanabilir ve fatura, nakit iskontosu tarihi geçmeden ödendiği takdirde alınır. 

<a name="cash-discounts"></a>Nakit iskontoları
--------------

Hem müşteriler veya hem de satıcılar için nakit iskontoları, Nakit iskontoları sayfasında oluşturulabilir. Ayrıca, önceki nakit iskontosunun vadesi dolduğunda birbirini izleyecek nakit iskontolarını, Sonraki iskonto kodu alanını kullanarak tanımlayabilirsiniz, Daha fazla bilgi için bu konunun devamındaki "Örnek: Nakit iskontoları serileri" başlığına bakınız. Eğer bir fatura, iade hareketi (ödeme veya alacak dekontu) veya her ikisi, tüzel kişiliğin hesap para birimini farklı bir para biriminde girilirse, nakit iskontosu, ödeme veya alacak dekontunun döviz kuru kullanılarak hesaplanır. Fatura ve iade belgesi farklı tüzel kişiliklere girildiye ve tüzel kişiliklerin muhasebe para birimleri farklıysa, döviz kuru faturanın bir tüzel kişiliğinden kredi belgesine göre alınır. Daha fazla bilgi için bu konunun devamındaki "Örnek: Nakit için döviz kurları" başlığına bakınız.
Nakit iskontosu ana hesabı varsayılan ilkesi
----------------------------------------------

Bir fatura nakit iskontosu elde etmek için zamanında kapatılmışsa, nakit iskontosu aşağıdaki varsayılan ilkesi önceliğine göre otomatik olarak bir nakit iskontosu ana hesabına nakledilir:
1.  Ana hesap, Açık hareketleri kapat sayfası veya Satıcı açık hareketleri kapat sayfasındaki Alternatif nakit iskontosu hesabı alanda belirtilir.
2.  Ana hesap, Faturaya atanan satış vergisi kodunun Genel muhasebe deftere nakletme grubunun, Müşteri nakit iskontosu alanı veya Satıcı satış iskontosu alanında belirtilir. Genel muhasebe deftere nakil gruplarını, genel muhasebe deftere nakil grupları sayfasında ayarlayın ve onları satış vergisi koduna satış vergisi kodları sayfasından atayın.
3.  Kapatılmış faturadaki nakit iskontosu kodu için, Müşteri iskontoları için ana hesap alanı veya Satıcı iskontoları için ana hesap alan Nakit iskontosu sayfasındadır.
4.  Nakit iskontoları için ana hesap, Otomatik hareketler için hesaplar sayfasında tanımlandığı gibi.

## <a name="example-series-of-cash-discounts"></a> Örnek: Nakit iskontoları dizisi
Aşağıdaki gibi üç nakit iskontosu kodu ayarlayın:
-   Kod 5D10% – Tutar 5 gün içinde ödendiğinde %10 oranında bir nakit iskontosu.
-   Kod 10D5% – Tutar 10 gün içinde ödendiğinde %5 oranında bir nakit iskontosu.
-   Kod 14D2% - Tutar 14 gün içinde ödendiğinde %2 oranında bir nakit iskontosu.

Bir sonraki iskonto kodu alanına:
-   5G%1 kodu için 10G%5 seçimini yapın.
-   10G%5 kodu için 14G%2 seçimini yapın.
-   14D2% kodu için Sonraki iskonto kodu alanını boş bırakın.

Fatura üzerindeki ödeme tarihi, bir önceki nakit indirimi tarihini geçtikçe, üç nakit indirimi bir birini izler. Fatura ödendiğinde nakit iskontosu sırasınndaki hangi nakit iskonto tarihi uyduğuna bağlı olarak, yalnızca bir nakit iskontosu verilir.

## <a name="example-exchange-rates-for-cash-discounts"></a> Örnek: Nakit iskontoları için döviz kurları
Tüzel kişiliğinizin muhasebe para birimi EUR'dur ve aşağıdaki döviz kurları USD için belirtilmiştir:
-   1 Şubat = 110
-   1 Mart = 80

Bir fatura nakit iskontosu % 20 D 2 ile 1000 USD için 15 Şubat nakledilir. Hesap para birimi fatura 1100 EUR miktarıdır Fatura ile ödeme 980 USD için 1 Mart kapatılır. Nakit iskontosu tutarı 20 USD olur. Ödemenin muhasebe para birimi tutarı 784 Euro'dur. 1:20 Mart itibariyle döviz kuru kullanılarak hesaplanan nakit iskontosu hesap para miktarını \*80 / 100 = 16 EUR
| **Note**                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Alacak hesapları parametreleri ya da hesapların borç parametreleri sayfaları hesapla nakit iskontoları için kısmi ödeme seçeneği seçili olduğunda her bir kısmi ödeme tarihinde geçerli olan döviz kuru kullanılır. |

 
=

 


