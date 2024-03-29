---
title: Kullanım hakkı varlığı amortismanı kaydetme (Önizleme)
description: Bu makalede, bir kuruluşun bilanço tablosunda kabul edilen kiralamalar için gerekli olan amortismanın günlük girişinin nasıl oluşturulacağı açıklanmaktadır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseAssetSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 93e521cf409af4c01d625f27bdd7a7564e471bd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903290"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a>Kullanım hakkı varlığı amortismanı kaydetme (Önizleme)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Bir kuruluşun bilanço tablosunda kabul edilen kiralamalar için, kullanım hakkı (ROU) varlığına aylık amortisman uygulanır. Bu makalede, amortisman için günlük girişin nasıl oluşturulacağı açıklanmaktadır. Deftere nakil profilinize ve kiralama türünüze bağlı olarak, amortisman gider genel muhasebe hesabını borçlandırı ve birikmiş amortisman genel muhasebe hesabını alacaklandırır. Bu girişler her kiralama için ayrı ayrı oluşturulabilir veya toplu iş günlük işlevleri kullanılarak birden fazla kiralama için oluşturulabilir.

## <a name="asset-depreciation-schedule"></a>Kıymet amortismanı zamanlaması

1. **Kiralama özeti** sayfasında bir kiralama seçin. Ardından, **Varlık amortisman planı** sayfasını açmak için **Defterler \> Varlık amortisman planı**'nı seçin.

    ROU varlığı amortisman gideri günlük girişi, **Amortisman Gideri** sütunundaki tutara dayanır. Muhasebe standardına uyum kılavuzu örneği için bu makalenin ilerleyen kısımlarındaki [Finansal kiralamalar için ROU varlığı amortisman giderinin hesaplanması](#calculation-of-rou-asset-amortization-expense-for-finance-leases) bölümüne bakın.
    
2. Amortisman dönemini seçin ve **Günlük oluştur**'u seçin. Amortismanı kaydetmek için kullanılacak günlüğün oluşturulduğunu bildiren bir ileti alırsınız.
3. **Varlık kiralama günlüğü** sayfasını açmak için **Günlükler \> Varlık kiralama günlükleri**'ni seçin. Burada, oluşturulan amortisman gideri günlük girişini görüntüleyebilirsiniz.

   Sistem, hareketler ve zamanlamalar arasındaki farkları önlemek için belirli mali alanların düzenlenmesini kilitler. Kilitlenen bazı alanlar şunlardır: **Hesap**, **Tutarlar**, **Mali boyutlar**, **Para birimi** ve **Hareket türü**. Ayrıca zamanlamalar ve hareketler arasında farklara neden olabileceğinden Varlık kiralama yevmiye defteri girişlerine yevmiye defteri girişi satırları ekleyemez veya bunları silemezsiniz.

4. Günlük girişini seçin ve amortisman girişini Genel muhasebe defterine kaydetmek için **Deftere naklet**'i seçin.

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a>İşletme kiralamaları için ROU varlığı amortisman giderinin hesaplanması

İşletme kiralamasının amortisman gideri, ABD'de Genel Kabul Görmüş Muhasebe İlkeleri'nde (ABD GAAP) standart olan Muhasebe Standartları Kodlaması Konu 842 (ACS 842) uyarınca aylık sabit esaslı gider ile kiralama yükümlülüğündeki aylık faiz gideri arasındaki fark olarak hesaplanır. Sabit kiralama gideri, tüm kira ödemelerinin aylık olarak kira süresine bölünmesiyle hesaplanır. (Kira ödemelerinin toplamı tüm ön ödemeleri, başlangıçtaki doğrudan maliyetleri, parçalara ayırma maliyetlerini ve kiralama teşviklerini içerir.) Aşağıdaki tabloda, bir işletme kiralaması için amortisman gideri örneği verilmiştir.

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a>İşletme kiralamaları için ROU varlığı amortisman giderinin örneği

| Alan                                          | Değer       |
|------------------------------------------------|-------------|
| Ödeme tutarı                                 | 1,000       |
| Ödeme sıklığı                              | Monthly     |
| Kiralama süresi (ay)                            | 24          |
| Toplam kira ödemeleri                           | 24,000      |
| Alternatif borçlanma oranı                     | %5          |
| Yıllık ödeme türü                                   | Vadesi dolan yıllık ödeme |
| Bileşim Aralığı                           | Monthly     |
| Gelecekteki minimum kira ödemelerinin bugünkü değeri | 22,888.87   |

Daha önce belirtildiği gibi sabit kiralama gideri, tüm ödemelerin toplamının kira süresine bölünmesiyle hesaplanır. Sistem, yükümlülük amortisman planındaki aylık faiz giderini otomatik olarak hesaplar. Faiz giderleri, efektif faiz oranı yöntemi kullanılarak hesaplanır. Sistem, her ayın faiz giderini çıkarmak için sabit esaslı kiralama maliyetini kullanır. Değer, ROU varlığını azaltmak için kullanılır.

| Ay | Sabit esaslı kiralama maliyeti | Vade farkı gideri                        | ROU varlığı amortisman giderinin hesaplanması |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| 1     | (24.000 ÷ 24) = 1.000,00 | (22.888,87 – 1.000) × (%5 ÷ 12) = 91,20 | 1.000 – 91,20 = 908,80                        |
| 2     | (24.000 ÷ 24) = 1.000,00 | (21.980,08 – 1.000) × (%5 ÷ 12) = 87,42 | 1.000 – 87,42 = 912,58                        |
| 3     | (24.000 ÷ 24) = 1.000,00 | (21.067,49 – 1.000) × (%5 ÷ 12) = 83,62 | 1.000 – 83,62 = 916,39                        |

> [!NOTE]
> ASC 842 uyarınca, bir işletme kiralaması için ROU varlığının amortismanı gelir tablosunda kiralama gideri olarak sınıflandırılır. Görünürlük açısından Varlık kiralama, girişi ROU varlığının amortismanı olarak tanımlar. Ancak, borç girişi bir işletme kiralama gideri hesabına atanmalıdır ve alacak girişi, doğrudan işletme kiralaması için ROU varlığına atanmalıdır. Bununla birlikte, kiralama parametrelerinde, alacak girişlerinin işletme ROU varlıkları için birikmiş amortisman hesabına yapılması gerektiğini belirtebilirsiniz.

Kira, bir işletim kirası olarak sınıflandırılıyorsa, değer düşüşü ardından aylık amortisman, sabit amortisman kullanılarak hesaplanır.

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a>Finansal kiralamalar için ROU varlığı amortisman giderinin hesaplanması

Finans sınıflandırmasına sahip kiralamalar için sistem, ROU varlığı amortismanını sabit olarak hesaplar. Bu nedenle, amortisman gideri her ay için aynı olacaktır.

Uluslararası Finansal Raporlama Standardı 16 (IFRS 16) ve ASC 842 uyarınca, kiralama süresi veya varlığın faydalı ömrü boyunca (hangisi daha azsa) varlığa amortisman uygulanır. Ayrıca, kiralama için **Sahiplik aktarımı** parametresi açıksa kiralama varlığın faydalı ömrü boyunca otomatik olarak amorti edilir.

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a>Finansaş kiralamalar için ROU varlığı amortisman giderinin örneği

| Alan                                | Değer                                   |
|--------------------------------------|-----------------------------------------|
| Başlangıç kullanım hakkı varlığı bakiyesi | 22,889.87                               |
| Kiralama süresi (ay)                  | 24                                      |
| Varlık faydalı ömrü (ay)           | 36                                      |
| Ay                                | Kullanım hakkı varlığı amortisman gideri |
| 1                                    | 22.889,87 ÷ 24 = 953,74                 |
| 2                                    | 22.889,87 ÷ 24 = 953,74                 |
| 3                                    | 22.889,87 ÷ 24 = 953,74                 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
