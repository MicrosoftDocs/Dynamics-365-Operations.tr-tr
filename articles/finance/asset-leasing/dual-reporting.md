---
title: Çift raporlama
description: Bu makalede, hem Uluslararası Mali Raporlama Standardı (IFRS) hem de Varlık kiralamada yasal raporlama gereksinimlerini nasıl karşılayabileceğinizi gösteren bir örnekle rehberlik sağlanmaktadır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9941d0bb251a95a71338c59f6eaa4bb9a505a5b5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886385"
---
# <a name="dual-reporting"></a>Çift raporlama

[!include [banner](../includes/banner.md)]

Bu makalede, hem Uluslararası Mali Raporlama Standardı (IFRS) hem de Varlık kiralamada yasal raporlama gereksinimlerini nasıl karşılayabileceğinizi gösteren bir örnekle rehberlik sağlanmaktadır. Microsoft Dynamics 365 Finance'te deftere nakil katmanları hakkında bilgi sahibi olmanız gereklidir ve örneği anlamanızı kolaylaştırır.

## <a name="example"></a>Örnek

Aşağıdaki örnekte, hem nakit bazlı yöntem hem de IFRS raporlama yöntemleri kullanarak İtalya yasal raporlaması kapsamında bir kiralama ele alınır. Şirketin hem İtalya yasal gereksinimlerini hem de IFRS 16 gereksinimlerini karşılamak için üç defter oluşturması gerekir. Defterlerden biri IFRS 16, biri yasal gereksinimler ve biri de yasal deftere nakil işlemlerini otomatik olarak ters kaydetme için gereklidir. Defterler, aşağıdaki tablolarda gösterilen şekilde ayarlanır.

**IFRS 16 defteri**

IFRS 16 defteri, IFRS 16 muhasebe standardı ile uyumlu olacak şekilde ayarlanır. Bu deftere nakledilecek tüm girişler, özel bir katmana nakledilir.

| Kuruluş adı                                    | Tanım    |
|-----------------------------------------|----------------|
| Defter türü                               | IFRS 16        |
| Defter açıklaması                        | IFRS 16        |
| Deftere Nakletme Katmanı                           | Özel katman 1 |
| Kiralama Türü                              | Finance        |
| Muhasebe Altyapısı                    | IFRS 16        |
| Kiralama Süresi / Faydalı ömür Ayarı         | 0,00           |
| Bugünkü Değer / Varlık Adil Değeri Ayarı | 0,00           |
| Kısa süre eşiği                    | 12             |
| Düşük Değer Eşiği                     | 5,000.00       |
| Satıcıya Öde                           | Hayır             |

**Yasal defter**

Yasal defter, şirketin kiralama giderini her ay kira için ödenen nakit tutarı olarak kaydedeceği nakit bazlı bir defterdir. Bu kitap, kullanım hakkı (ROU) varlığı veya kiralama yükümlülüğü oluşturmaz.

| Kuruluş adı                                    | Tanım |
|-----------------------------------------|-------------|
| Defter türü                               | Yasal   |
| Defter açıklaması                        | Yerel GAAP  |
| Deftere Nakletme Katmanı                           | Cari     |
| Kiralama Türü                              | Otomatik   |
| Muhasebe Altyapısı                    | Nakit esası  |
| Kiralama Süresi / Faydalı ömür Ayarı         | 0,00        |
| Bugünkü Değer / Varlık Adil Değeri Ayarı | 0,00        |
| Kısa süre eşiği                    | 0           |
| Düşük Değer Eşiği                     | 0           |
| Satıcıya Öde                           | Hayır          |

**Yasal ters kayıt defteri**

Yasal ters kayıt defteri, yasal defterle aynı şekilde ayarlanır.

| Kuruluş adı                                    | Tanım                    |
|-----------------------------------------|--------------------------------|
| Defter türü                               | Yasal - Ters Kayıt           |
| Defter açıklaması                        | Yasal defterin ters kaydedileceği defter |
| Deftere Nakletme Katmanı                           | Özel katman 1                 |
| Kiralama Türü                              | Otomatik                      |
| Muhasebe Altyapısı                    | Nakit esası                     |
| Kiralama Süresi / Faydalı ömür Ayarı         | 0,00                           |
| Bugünkü Değer / Varlık Adil Değeri Ayarı | 0,00                           |
| Kısa süre eşiği                    | 0                              |
| Düşük Değer Eşiği                     | 0                              |
| Satıcıya Öde                           | Hayır                             |

Bu örnekte, **Genel** ve **Ödeme planı satırları** sekmelerinde aşağıdaki ayarlara sahip bir kiralama oluşturulur.

**Genel sekmesi**

| Alan                      | Değer            |
|----------------------------|------------------|
| Alternatif borçlanma oranı | %5               |
| Başlangıç tarihi          | 01.01.2020         |
| Kiralama grubu                | Binalar        |
| Satıcı                     | 1001             |
| Kıymetin adil değeri    | 245,000          |
| Varlık faydalı ömrü          | 120              |
| Yıllık ödeme türü               | Normal yıllık ödeme |
| Bileşim aralığı       | Monthly          |

**Ödeme planı satırları sekmesi**

| Alan             | Değer      |
|-------------------|------------|
| Başlangıç tarihi        | 01.01.2020   |
| Dönem aralığı   | Aylar     |
| Dönemler           | 24         |
| Bitiş tarihi          | 31.12.2020 |
| Ödeme sıklığı | Monthly    |
| Ödeme tutarı    | 1,000      |

Bu kiralamayı iki altyapıda kaydetmek için geçerli deftere nakil katmanını ve özel deftere nakil katmanını kullanırsınız. Aşağıdaki tabloda, her bir raporlama standardı kapsamında mali bilgilerin adil bir şekilde temsil edilmesini gerektiren her bir günlük girişi örneği gösterilir. Kiralamanın ilk ayı için her bir günlük girişinin ayrıntılı açıklaması daha sonra sağlanır.

<table>
<thead>
<tr>
<th rowspan='3'>Hesap numarası</th>
<th rowspan='3'>Tanım</th>
<th colspan='3'>Yasal defter (geçerli katman)</th>
<th rowspan='3'>Geçerli katman toplamı</th>
<th>Ters kayıt defteri (özel katman)</th>
<th colspan='4'>IFRS 16 defteri (özel katman)</th>
<th rowspan='3'>Geçerli katman + özel katman toplamı</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
<th>JE-130</th>
<th>JE-140</th>
<th>JE-150</th>
<th>JE-160</th>
<th>JE-170</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Kiralama gideri</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
<td>-1.000,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>2</td>
<td>Banka masrafı</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>KDV gideri</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Kliring hesabı</td>
<td>-1.000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
<td>1,000.00</td>
<td></td>
<td>-1.000,00</td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Borç hesapları</td>
<td></td>
<td>-1.008,00</td>
<td>1,008.00</td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>ROU varlığı</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>22,794.00</td>
<td></td>
<td></td>
<td></td>
<td>22,793.90</td>
</tr>
<tr>
<td>7</td>
<td>Finansal kiralama yükümlülüğü</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>-22.794,00</td>
<td>1,000.00</td>
<td>-94,97</td>
<td></td>
<td>-21.888,87</td>
</tr>
<tr>
<td>8</td>
<td>Vade farkı gideri</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td>94.97</td>
<td></td>
<td>94.97</td>
</tr>
<tr>
<td>9</td>
<td>Nakit</td>
<td></td>
<td></td>
<td>-1.008,00</td>
<td>-1.008,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-1.008,00</td>
</tr>
<tr>
<td>10</td>
<td>Amortisman gideri</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>949.75</td>
<td>949.75</td>
</tr>
<tr>
<td>11</td>
<td>Birikmiş amortisman</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-949,75</td>
<td>-949,75</td>
</tr>
</tbody>
</table>

Önceki tabloda gösterildiği gibi, hem yasal raporlama hem de IFRS raporlaması kapsamında raporlamak için üç defter gereklidir.

- Yasal defter, kira ödemesini, geçerli katmanda nakit bazlı muhasebe kurallarına göre kaydeder.
- Yasal ters kayıt defteri, yasal günlük girişlerini ters kaydeder.
- IFRS 16 defteri, IFRS 16 kapsamında gerekli olan günlük girişlerini oluşturur.

Kiralamayı yalnızca bir kez girmeniz gerekir. Ardından, kiralamayla ilişkili tüm defterleri görmek için **Defterler** sayfasını açabilirsiniz.

> [!NOTE]
> Defterleri oluşturduğunuzda, bunların üçü aynı kiralama kaydıyla ilişkilendirilmelidir.

İlk günlük girişi, kiralama giderini yasal deftere kaydeder. Ödemeleri toplu işte veya yasal defterdeki ödeme planını seçerek oluşturabilirsiniz.

Bu örnekte, aşağıdaki günlük girişi yasal defter için ödeme planından oluşturulmuştur.

### <a name="lease-payment--1312020--je-100"></a>Kira ödemesi – 31.01.2020 – JE 100

| Hesap türü | Hesap numarası | Katman   | Hesap açıklaması | Borç    | Kredi   |
|--------------|----------------|---------|---------------------|----------|----------|
| Genel muhasebe       | 1              | Cari | Kiralama gideri       | 1,000.00 |          |
| Genel muhasebe       | 4              | Cari | Kliring hesabı    |          | 1,000.00 |

Borç hesapları uzmanı, Varlık kiralama dışındaki kirayı ödemek için fatura oluştururken standart Dynamics 365 işlevini kullanır. Ancak, Borç hesapları uzmanı aşağıdaki girişi oluşturmak için borç hesabı olarak **Kiralama gideri**'ni seçmek yerine kliring hesabı seçer.

### <a name="ap-process--1312020--je-110"></a>AP işlemi – 31.01.2020 – JE 110

| Hesap türü | Hesap numarası | Katman   | Hesap açıklaması | Borç    | Kredi   |
|--------------|----------------|---------|---------------------|----------|----------|
| Genel muhasebe       | 4              | Cari | Kliring hesabı    | 1,000.00 |          |
| Genel muhasebe       | 2              | Cari | Banka masrafı            | 3.00     |          |
| Genel muhasebe       | 3              | Cari | KDV gideri         | 5.00     |          |
| Satıcı       | 5              | Cari | Borç hesapları    |          | 1,008.00 |

Ekstre satıcıya verildiğinde, normal ödeme sürecini takip edersiniz. Bu işlem sırasında aşağıdaki günlük girişi oluşturulur.

### <a name="cash-payment--1312020--je-120"></a>Nakit ödemesi – 31.01.2020 – JE 120

| Hesap türü | Hesap numarası | Katman   | Hesap açıklaması | Borç    | Kredi   |
|--------------|----------------|---------|---------------------|----------|----------|
| Satıcı       | 5              | Cari | Borç Hesapları    | 1,008.00 |          |
| Banka         | 9              | Cari | Nakit                |          | 1,008.00 |

Bu aşamada, yasal raporlama gereksinimleri kaypsamında bu kiralamayı tam olarak kaydetmiş olursunuz ve geçerli katmanı kullanarak bir mizan oluşturabilirsiniz. Sistem, aşağıdaki rakamları içeren bir mizan döndürür.

<table>
<thead>
<tr>
<th rowspan='3'>Hesap numarası</th>
<th rowspan='3'>Tanım</th>
<th colspan='3'>Yasal defter (geçerli katman)</th>
<th rowspan='3'>Geçerli katman toplamı</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Kiralama gideri</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
</tr>
<tr>
<td>2</td>
<td>Banka masrafı</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>KDV gideri</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Kliring hesabı</td>
<td>-1.000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Borç hesapları</td>
<td></td>
<td>-1.008,00</td>
<td>1,008.00</td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>ROU varlığı</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>7</td>
<td>Finansal kiralama yükümlülüğü</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>8</td>
<td>Vade farkı gideri</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>9</td>
<td>Nakit</td>
<td></td>
<td></td>
<td>-1.008,00</td>
<td>-1.008,00</td>
</tr>
<tr>
<td>10</td>
<td>Amortisman gideri</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>11</td>
<td>Birikmiş amortisman</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
</tbody>
</table>

Aynı mizanı çalıştırmak için IFRS 16 rakamlarını kullanmak istiyorsanız yasal muhasebe günlük girişlerine ters kayıt işlemi uygulanmalıdır ve IFRS 16 günlük girişleri deftere nakledilmelidir. Yasal günlük girişlerini ters kaydetmek için bu örnek, yasal defterle aynı kuruluma sahip, ancak ters bir deftere nakil profili bulunan bir yasal ters kayıt defteri içerir. Örneğin, yasal defter bir kiralama gideri hesabını *borçlandırır* ancak ters kayıt defteri bu hesabı *alacaklandırır*. Bu ilişkiler, **Varlık kiralama parametreleri** sayfasındaki Varlık kiralama deftere nakil hesaplarında kolayca tanımlanır (**Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**).

Yasal defter için kullanılan işlemin aynısı ters kayıt defteri için kullanılırsa aşağıdaki günlük girişi oluşturulur. Aradaki fark, ters kayıt defterinin ters kayıt girişlerini yasal defterden kaydetmesidir. Ters kayıt girişleri de özel katmanda yapılır. Geçerli katmanda bir mizan çalıştırıldığında, ters kayıt günlük girişleri dahil edilmez.

### <a name="lease-payment--1312020--je-130"></a>Kira ödemesi – 31.01.2020 – JE 130

| Hesap türü | Hesap numarası | Katman  | Hesap açıklaması | Borç    | Kredi   |
|--------------|----------------|--------|---------------------|----------|----------|
| Genel muhasebe       | 4              | Özel | Kliring hesabı    | 1,000.00 |          |
| Genel muhasebe       | 1              | Özel | Kiralama gideri       |          | 1,000.00 |

Yasal günlük girişlerini kaldırdığınıza göre IFRS 16'nın gerektirdiği tüm günlük girişlerini IFRS 16 defterine kaydedersiniz. Bu girişler arasında ROU varlığının ve yükümlülüğün ilk kabulü ile faiz ve amortisman kaydı yer alır.

### <a name="initial-recognition--112020--je-140"></a>İlk kabul – 01.01.2020 – JE 140

| Hesap türü | Hesap numarası | Katman  | Hesap açıklaması      | Borç     | Kredi    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| Genel muhasebe       | 6              | Özel | ROU Varlığı                | 22,793.90 |           |
| Genel muhasebe       | 7              | Özel | Finansal kiralama yükümlülüğü |           | 22,793.90 |

Kira ödemesi diğer kira ödemeleriyle aynı şekilde deftere nakledilir. Kliring hesabının kullanılma nedeni, nakitin yalnızca bir kez alacak olarak kaydedilmesini sağlamaktır.

### <a name="lease-payment--1312020--je-150"></a>Kira ödemesi – 31.01.2020 – JE 150

| Hesap türü | Hesap numarası | Katman  | Hesap açıklaması      | Borç    | Kredi   |
|--------------|----------------|--------|--------------------------|----------|----------|
| Genel muhasebe       | 7              | Özel | Finansal kiralama yükümlülüğü | 1,000.00 |          |
| Genel muhasebe       | 4              | Özel | Kliring hesabı         |          | 1,000.00 |

Faiz gideri günlüğü girişi, yükümlülük amortisman planlamasından oluşturulur.

### <a name="interest-expense--1312020--je-160"></a>Faiz gideri – 31.01.2020 – JE 160

| Hesap türü | Hesap numarası | Katman  | Hesap açıklaması      | Borç | Kredi |
|--------------|----------------|--------|--------------------------|-------|--------|
| Genel muhasebe       | 8              | Özel | Vade farkı gideri         | 94.97 |        |
| Genel muhasebe       | 7              | Özel | Finansal kiralama yükümlülüğü |       | 94.97  |

Amortisman gideri günlük girişi, varlık amortisman planlamasından oluşturulur.

### <a name="depreciation-expense--1312020--je-170"></a>Amortisman gideri – 31.01.2020 – JE 170

| Hesap türü | Hesap numarası | Katman  | Hesap açıklaması      | Borç  | Kredi |
|--------------|----------------|--------|--------------------------|--------|--------|
| Genel muhasebe       | 10             | Özel | Amortisman gideri     | 949.75 |        |
| Genel muhasebe       | 11             | Özel | Birikmiş amortisman |        | 949.75 |

Tüm bu günlük girişleri oluşturulup deftere nakledildikten sonra, aşağıdaki "özel katman 1" değerlerini görürsünüz. Son sütuna banka ücreti, katma değer vergisi (KDV) gideri ve önceki katmandan nakit azaltmanın dahil olduğunu görürsünüz ancak yasal raporlama günlük girişleri dahil değildir. Bu sayede, doğru çift raporlama özelliklerini kullanmış olursunuz. Bu aşamada, şirketin yalnızca mizanı çalıştırması ve IFRS mizanı oluşturmak için geçerli katman ile özel katmanı birleştirmesi gerekir.

| Hesap No. | Tanım              | Yasal Defter\-Geçerli Katman\-JE\-100\-Dr \(Cr\) | Yasal Defter\-Geçerli Katman\-JE\-110\-Dr \(Cr\) | Yasal Defter\-Geçerli Katman\-JE\-120\-Dr \(Cr\) | Geçerli Katman \- Toplamlar | - | Ters Kayıt Defteri\-Özel katman\-JE\-130\-Dr \(Cr\) | IFRS 16 Defteri\-Özel katman\-JE\-140\-Dr \(Cr\) | IFRS 16 Defteri\-Özel katman\-JE\-150\-Dr \(Cr\) | IFRS 16 Defteri\-Özel katman\-JE\-160\-Dr \(Cr\) | IFRS 16 Defteri\-Özel katman\-JE\-170\-Dr \(Cr\) | Geçerli Katman \+ Geçerli Katman \- Toplamlar |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| 1          | Kiralama gideri            | 1,000\.00                                         |                                                   |                                                   | 1,000\.00               |   | \-1.000                                         |                                                |                                                |                                                |                                                | 0\.00                                   |
| 2          | Banka masrafı                 |                                                   | 3\.00                                             |                                                   | 3\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 3\.00                                   |
| 3          | KDV gideri              |                                                   | 5\.00                                             |                                                   | 5\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 5\.00                                   |
| 4          | Kliring hesabı         | \-1.000\.00                                       | 1,000\.00                                         |                                                   | 0\.00                   |   | 1,000                                           |                                                | \-1.000                                        |                                                |                                                | 0\.00                                   |
| 5          | Borç hesapları         |                                                   | \-1.008\.00                                       | 1,008\.00                                         | 0\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 0\.00                                   |
| 6          | ROU varlığı                |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | 22,794                                         |                                                |                                                |                                                | 22,793\.90                              |
| 7          | Finansal kiralama yükümlülüğü |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | \-22.794                                       | 1,000                                          | \-94\.97                                       |                                                | \-21,888\.87                            |
| 8          | Vade farkı gideri         |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                | 94\.97                                         |                                                | 94\.97                                  |
| 9          | Nakit                     |                                                   |                                                   | \-1.008\.00                                       | \-1.008\.00             |   |                                                 |                                                |                                                |                                                |                                                | \-1.008\.00                             |
| 10         | Amortisman gideri     |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | 949\.75                                        | 949\.75                                 |
| 11         | Birikmiş amortisman |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | \-949\.75                                      | \-949\.75                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
