---
title: Vergi için çift para birimi desteği
description: Bu makalede, vergi etki alanındaki çift para birimiyle muhasebe özelliğinin nasıl genişletileceği ve bunun vergi hesaplama ve deftere nakil işlemleri üzerindeki etkisi açıklanmaktadır
author: EricWang
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 13d70d964a83c2efba090244d549bdb38ad25af2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909054"
---
# <a name="dual-currency-support-for-sales-tax"></a>Satış vergisi için çift para birimi desteği
[!include [banner](../includes/banner.md)]

Bu makalede, satış vergileri için çift para birimiyle muhasebe özelliğinin nasıl genişletileceği ve bunun satış vergisi hesaplama ve deftere nakil işlemlerine etkisi açıklanmaktadır.

Dynamics 365 Finance için çift para birimi özelliği 8.1 (2018 Ekim) sürümünde kullanılmaya başlandı. Raporlama para birimi cinsinden hesap girişlerinin hesaplanma biçimini değiştirir.

Önceki sürümlerde, işlemler raporlama para birimine aşağıdaki sırada dönüştürüldü: 

- Hareket toplamı hareket para birimi cinsinden hesaplandı > hareket tutarı muhasebe para birimine dönüştürüldü > muhasebe para birimi tutarı raporlama para birimine dönüştürüldü

Çift para birimi özelliğini etkinleştirdikten sonra, hareketler raporlama para birimine aşağıdaki sırada dönüştürüldü:

- Hareket para birimi tutarı > Raporlama para birimi tutarı

Çift para birimi hakkında daha fazla bilgi için lütfen [çift para birimine](dual-currency.md) bakın.

Çift para birimleri desteğinin bir sonucu olarak özellik yönetiminde iki yeni özellik bulunur: 

- Satış vergisi dönüştürmesi (10.0.13 sürümde yeni)
- Satış vergisi kapatması için gerçekleşen para birimi ayarlama kar/zarar hesaplarına mali boyutlar girin (sürüm 10.0.17 yeni)

Satış vergileri için çift para birimi desteği, vergi para birimi cinsinden vergilerin doğru hesaplanmasını ve satış vergisi kapatma bakiyesinin hem muhasebe para birimi, hem de raporlama para birimi cinsinden doğru şekilde hesaplanmasını sağlar.

## <a name="sales-tax-conversion"></a>Satış vergisi dönüştürme

**Satış vergisi dönüştürme** parametresi, vergi tutarını hareket para biriminden vergi para birimine dönüştürmek için iki seçenek sunar. 

- Muhasebe para birimi: Yol "hareket para birimi tutarı > muhasebe para birimi tutarı > vergi para birimi tutarı" olur. Para birimi dönüştürmesi için, (Muhasebe Kurulumu 'nda konfigüre edilen) muhasebe para birimi döviz kuru türü kullanılır.
- Raporlama para birimi: Yol "hareket para birimi tutarı > raporlama para birimi tutarı > vergi para birimi tutarı" olur. Para birimi dönüştürmesi için, (Muhasebe Kurulumu 'nda konfigüre edilen) raporlama para birimi döviz kuru türü kullanılır.

### <a name="example"></a>Örnek

Bu işlevi gösteren basit bir örnek aşağıdaki bir örnektir:

Genel muhasebe ve vergi için para birimi kurulumu

| Hareket para birimi | Muhasebe para birimi | Raporlama para birimi | Vergi para birimi |
| -------------------- | ------------------- | ------------------ | ------------ |
| Euro                  | ABD Doları                 | GBP                | GBP          |

Döviz kuru

| Kaynak para birimi | Hedef para birimi | Katsayı | Döviz kuru |
| ------------- | ----------- | ------ | ------------- |
| Euro           | ABD Doları         | 1      | 1.11          |
| Euro           | GBP         | 1      | 0.83          |
| ABD Doları           | GBP         | 1      | 0.75          |

Farklı parametre seçeneklerinde vergi tutarı hesaplaması

Vergi tutarı = 100 EUR

| Satış vergisi dönüştürme parametreleri | Hareket para birimi (EUR) | Muhasebe para birimi (USD) | Raporlama para birimi (GBP) | Vergi Para Birimi (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Muhasebe para birimi             | 100                        | 111                       | 83                       | **83.25**          |
| Raporlama para birimi              | 100                        | 111                       | 83                       | **83**             |

Bu parametre vergi dairesinden uyumluluk gereksinimini temel alarak konfigüre edilebilir.


### <a name="upgrade-consideration"></a>Yükseltme değerlendirmesi

Bu özellik yalnızca yeni hareketler için geçerlidir. Vergi hareketi için TAXTRANS tablosunda zaten kaydedilmiş ancak henüz kapatılmayan bir deftere nakil vergisi zaman noktasındaki Döviz Kuru zaten eksik olduğundan, sistem vergi para birimi cinsinden vergi tutarını yeniden hesaplamayacaktır.

Önceki senaryoyu önlemek için bu parametre değerini, kapatılmamış vergi hareketleri içermeyen yeni (temiz) vergi kapatma döneminde değiştirmenizi öneririz. Vergi kapatma döneminin ortasındaki bu değeri değiştirmek için, lütfen bu parametre değerini değiştirmeden önce geçerli vergi kapatma dönemi için "Satış vergisini kapat ve deftere naklet" programını çalıştırın.

Bu özellik, döviz alım satımlarından elde edilen kazanç ve kayıpları netleştiren muhasebe girişleri ekler. Girişler, satış vergisi kapatması sırasında yeniden değerleme yapıldığında gerçekleşen para birimi ayarlama kar ve zarar hesaplarında yapılacaktır. Daha fazla bilgi için, bu makalenin sonraki bölümlerinde yer alan [Raporlama para birimi cinsinden vergi kapatma otomatik bakiyesi](#tax-settlement-auto-balance-in-reporting-currency) bölümüne bakın.

> [!NOTE]
> Kapatma sırasında, mali boyutlara ilişkin bilgiler bilanço hesapları olan satış vergisi hesaplarından alınır ve kar ve zarar tablosu hesapları olan para birimi ayarlama kar ve zarar hesaplarına girilir. Mali boyutların değerine ilişkin kısıtlamalar bilanço hesapları ile kar ve zarar tablosu hesapları arasında farklılık sağladığından, Satış vergisi kapatma ve deftere naklet işlemi sırasında bir hata oluşabilir. Hesap yapılarını değiştirmek zorunda kalmamak için, "Mali boyutları satış vergisi kapatması için gerçekleşen para birimi ayarlama kar/zarar hesaplarına doldur" özelliğini açabilirsiniz. Bu özellik, finansal boyutların para birimi düzeltme kar/zarar hesaplarına türetilmesini zorlayacaktır. 

## <a name="track-reporting-currency-tax-amount"></a>Raporlama para birimi vergi tutarını izleme

Raporlama para birimi cinsinden tutarları izlemek için vergiyle ilişkili tablolara üç yeni alan eklenmiştir. Bu alanlar, TAXUNCOMMITTED ve TAXTRANS tablolarının içindedir:

- TaxAmountRep: Raporlama para birimi cinsinden vergi tutarı
- TaxBaseAmountRep: Raporlama para birimi cinsinden baz tutar
- TaxInCostPriceRep: raporlama para birimi cinsinden kesinti yapılamayan tutar

Vergi yalnızca TAXUNCOMMITTED tablosunda kaydedilmiş ancak henüz deftere nakledilmemişse, sistem deftere nakil ve TAXTRANS tablosunda kaydetme sırasında vergi tutarını raporlama para birimi cinsinden yeniden hesaplar.

Bu serbest bırakma, raporlama para birimi cinsinden vergi tutarını gösteren rapor ve formlarda yapılan değişiklikleri içermez. Rapor ve formlardaki değişiklikler gelecek sürümde teslim edilecek.



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a>Raporlama para birimi cinsinden vergi kapatma otomatik bakiyesi

Satış vergisi dönüştürme yolu "muhasebe para birimi" veya tek bir vergi kapatma döneminde Döviz Kuru değişikliği gibi belirli bir nedenden dolayı vergi kapatması raporlama para birimi cinsinden dengeli değilse, sistem vergi tutarı farkını ayarlamak ve genel muhasebe kurulumunda konfigüre edilen gerçekleştirilmiş bir döviz kazanç/zarar hesabıyla dengelemek üzere hesap girişlerini otomatik olarak oluşturur.

Önceki örneği bu özelliği göstermek için kullanmak, deftere nakil sırasında TAXTRANS tablosundaki verilerin aşağıdaki gibi olduğunu varsayın.

| Satış vergisi dönüştürme parametreleri | Hareket para birimi (EUR) | Muhasebe para birimi (USD) | Raporlama para birimi (GBP) | Vergi Para Birimi (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Muhasebe para birimi             | 100                        | 111                       | 83                       | **83.25**          |
| Raporlama para birimi              | 100                        | 111                       | 83                       | **83**             |

Satış vergisi kapatma programını ay sonu ile çalıştırdığınızda, hesap girişi aşağıdaki gibi olur.
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a>Senaryo: satış vergisi dönüştürme = "Muhasebe para birimi"

| Ana hesap           | Hareket para birimi (GBP) | Muhasebe para birimi (USD) | Raporlama para birimi (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Ödenecek/Alınacak Vergi | -83,25                     | -111                      | -83,25                   |
| Vergi Kapatma         | 83.25                      | 111                       | 83.25                    |
| Gerçekleşmemiş kazanç/zarar     | 0                          | 0                         | -0,25                    |
| Ödenecek/Alınacak Vergi | 0                          | 0                         | 0.25                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a>Senaryo: satış vergisi dönüştürme = "Raporlama para birimi"


| Ana hesap           | Hareket para birimi (GBP) | Muhasebe para birimi (USD) | Raporlama para birimi (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Ödenecek/Alınacak Vergi | -83                        | -110,67                   | -83                      |
| Vergi Kapatma         | 83                         | 110.67                    | 83                       |
| Gerçekleşmemiş kazanç/zarar     | 0                          | 0.33                      | 0                        |
| Ödenecek/Alınacak Vergi | 0                          | -0,33                     | 0                        |



Daha fazla bilgi edinmek için aşağıdaki konulara bakın:

- [Çift para birimi](dual-currency.md)
- [Satış vergisine genel bakış](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
