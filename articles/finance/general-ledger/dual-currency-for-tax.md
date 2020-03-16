---
title: Vergi için çift para birimi desteği
description: Bu konu, vergi etki alanındaki iki para birimi ile muhasebe özelliğinin nasıl uzatılacağını ve vergi hesaplama ve deftere nakil işlemlerinin etkisini açıklamaktadır
author: EricWang
manager: Ann Beebe
ms.date: 12/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c9318f518135bf7aa545cdb5ddd2e68c54a6d211
ms.sourcegitcommit: bcc8cba8905ed51797d36e1712d7360452cfc5c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/27/2020
ms.locfileid: "3090576"
---
# <a name="dual-currency-support-for-sales-tax"></a>Satış vergisi için çift para birimi desteği
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konu, satış vergileri için iki para birimi ile muhasebe özelliğinin nasıl uzatılacağını ve satış vergisi hesaplama ve deftere nakil işlemlerinin etkisini açıklamaktadır.

Dynamics 365 Finance için çift para birimi özelliği 8.1 (2018 Ekim) sürümünde kullanılmaya başlandı. Raporlama para birimi cinsinden hesap girişlerinin hesaplanma biçimini değiştirir.

Önceki sürümlerde, işlemler raporlama para birimine aşağıdaki sırada dönüştürüldü: 

Hareket toplamı hareket para birimi cinsinden hesaplandı > hareket tutarı muhasebe para birimine dönüştürüldü > muhasebe para birimi tutarı raporlama para birimine dönüştürüldü

Çift para birimi özelliğini etkinleştirdikten sonra, hareketler raporlama para birimine aşağıdaki sırada dönüştürüldü:

- Hareket para birimi tutarı > Raporlama para birimi tutarı

Çift para birimi hakkında daha fazla bilgi için lütfen [çift para birimine](dual-currency.md) bakın.

Çift para birimleri desteğinin bir sonucu olarak özellik yönetiminde iki yeni özellik bulunur: 

- Satış vergisi dönüştürmesi (10.0.9 sürümde yayınlandı)
- Raporlama para birimi cinsinden vergi kapatma otomatik bakiyesi (10.0.11 sürümde yayınlandı)

Satış vergileri için çift para birimi desteği, vergi para birimi cinsinden vergilerin doğru hesaplanmasını ve satış vergisi kapatma bakiyesinin hem muhasebe para birimi, hem de raporlama para birimi cinsinden doğru şekilde hesaplanmasını sağlar. 

Yeni özellikler şu anda özel önizleme müşterileri için etkin durumda. Özellikleri etkinleştirmek için ilgili kanallarla Microsoft'a bir servis isteği yükseltin.

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

Satış vergisi kapatma programını ay sonu ile çalıştırdığınızda, hesap girişi aşağıdaki gibi olur:.
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
