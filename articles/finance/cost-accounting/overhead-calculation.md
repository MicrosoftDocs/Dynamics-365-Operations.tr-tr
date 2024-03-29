---
title: Genel gider hesaplaması
description: Bu makalede, genel gider maliyetlerinin hesaplanması için tipik işlemler açıklanmaktadır.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: twheeloc
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 9322fb5237afdbf73147bb549eb3f70929c46ce2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882005"
---
# <a name="overhead-calculation"></a>Genel gider hesaplaması

[!include [banner](../includes/banner.md)]

Bu makalede, genel gider maliyetlerinin hesaplanması için tipik işlemler açıklanmaktadır.

## <a name="term-definition"></a>Terim tanımı

Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir. Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar. Aşağıda bazı genel gider örnekleri verilmiştir:

-   Kira
-   Elektrik
-   Yönetim maaşları

## <a name="overhead-calculation-overview"></a>Genel gider hesaplaması genel bakış
Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır. Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz. Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur. Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır. Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir. Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:

-   Sürüm türü
-   Tarih ve saat
-   Maliyet muhasebesi defteri
-   Mali yıl
-   Mali dönem

Genel gider hesaplama, sürümden bağımsız olarak çalışır. Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz. Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi. Her adımda, yevmiye defteri girişleri olan bir günlük başlığı oluşturulur. Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar. İlkeler ve kurallar her yevmiye defteri satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur. Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz. 

[![Genel gider hesaplaması.](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>Elektrik genel gideri maliyetini hesapla ve tahsis et
Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir. Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz. Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir. Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır. Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.

<table>
<thead>
<tr>
<th>Muhasebeleşme tarihi</th>
<th colspan="2">Maliyet merkezi</th>
<th colspan="2">Ana hesap</th>
<th>Muhasebe para birimi cinsinden tutar</th>
</tr>
</thead>
<tbody>
<tr>
<td>3 Ocak 2017</td>
<td>CC099</td>
<td>Varsayılan maliyet merkezi</td>
<td>10001</td>
<td>Elektrik</td>
<td>10,000.00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>Adım 1: Maliyet davranışı hesaplamayı işle

Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar. Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.

#### <a name="define-the-cost-behavior-rule"></a>Maliyet davranış kuralını tanımlayın

Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır. Elektrik faturaları genellikle bu tanıma uyar. Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız. Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:

-   Sabit tutar 1.000,00
    -   0 &lt;= 1.000,00 = Sabit
    -   1000,01 &lt; N = Değişken

##### <a name="journal"></a>Günlük

<table>
<thead>
<tr>
<th>Günlük</th>
<th>Günlük türü:</th>
<th colspan="3">Mali takvim dönemi</th>
<th>Sürüm</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>Maliyet davranışı hesaplama günlüğü</td>
<td>Mali</td>
<td>2017</td>
<td>Dönem 1</td>
<td>Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Yevmiye defteri girişleri (Maliyet nesnesi bakiyesi yevmiye defteri girişleri)

<table>
<thead>
<tr>
<th>Muhasebeleşme tarihi</th>
<th colspan="2">Maliyet nesnesi</th>
<th colspan="2">Maliyet öğesi</th>
<th>Maliyet davranışı</th>
<th>Tutar</th>
</tr>
</thead>
<tbody>
<tr>
<td>3 Ocak 2017</td>
<td>CC099</td>
<td>Varsayılan maliyet merkezi</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sınıflandırılmamış</td>
<td>10,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Maliyet girişleri

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th colspan="2">Maliyet öğesi</th>
<th>Maliyet davranışı</th>
<th>Tutar</th>
<th>Muhasebeleşme tarihi</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Varsayılan maliyet merkezi</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sınıflandırılmamış</td>
<td>10,000.00</td>
<td>3 Ocak 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Varsayılan maliyet merkezi</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sınıflandırılmamış</td>
<td>-10.000,00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Varsayılan maliyet merkezi</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>1.000,00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Varsayılan maliyet merkezi</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>9,000.00</td>
<td>31 Ocak 2017</td>
</tr>
</tbody>
</table>

Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).
### <a name="step-2-process-the-cost-distribution-calculation"></a>Adım 2: Maliyet dağıtımı hesaplamayı işle

Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır. Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.

#### <a name="define-the-cost-distribution-rule"></a>Maliyet dağıtım kuralını tanımlayın

Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir. Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir. Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır. En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur. Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir. Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Kwh</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>İK</td>
<td>1.000</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>6,000</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>0</td>
</tr>
</tbody>
</table>

Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Büyüklük</th>
<th>Tahsisat faktörü</th>
<th>Tutar</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>İK</td>
<td>1.000</td>
<td>(1.000 ÷ 7.000) × 9.000,00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>6,000</td>
<td>(6.000 ÷ 7.000) × 9.000,00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>0</td>
<td>(0 ÷ 7.000) × 9.000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır. Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Formül</th>
<th>Büyüklük</th>
<th>Tahsisat faktörü</th>
<th>Tutar</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>İK</td>
<td>(1,000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1.000,00</td>
<td>500.00</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>(6,000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1.000,00</td>
<td>500.00</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>(0 &gt; 0,00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1.000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Günlük

<table>
<thead>
<tr>
<th>Günlük</th>
<th>Günlük türü:</th>
<th colspan="3">Mali takvim dönemi</th>
<th>Sürüm</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>Maliyet dağıtımı hesaplama günlüğü</td>
<td>Mali</td>
<td>2017</td>
<td>Dönem 1</td>
<td>Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Yevmiye defteri girişleri (Maliyet nesnesi bakiyesi yevmiye defteri girişleri)

<table>
<thead>
<tr>
<th>Muhasebeleşme tarihi</th>
<th colspan="2">Maliyet nesnesi</th>
<th colspan="2">Maliyet öğesi</th>
<th>Maliyet davranışı</th>
<th>Tutar</th>
</tr>
</thead>
<tbody>
<tr>
<td>31 Ocak 2017</td>
<td>CC099</td>
<td>Varsayılan maliyet merkezi</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>1.000,00</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>CC099</td>
<td>Varsayılan maliyet merkezi</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>9,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Maliyet girişleri

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th colspan="2">Maliyet öğesi</th>
<th>Maliyet davranışı</th>
<th>Tutar</th>
<th>Muhasebeleşme tarihi</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Varsayılan maliyet merkezi</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>-1.000,00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>İK</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>500.00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>500.00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Varsayılan maliyet merkezi</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>-9.000,00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>İK</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>1,285.71</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>7,714.29</td>
<td>31 Ocak 2017</td>
</tr>
</tbody>
</table>

Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md). 

### <a name="step-3-process-the-overhead-rate-calculation"></a>Adım 3: Genel gider oranı hesaplama işlemi

Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır. Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır. 

#### <a name="define-the-overhead-rate"></a>Genel gider oranını tanımlama

Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur. HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Saatler</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>Proje 1</td>
<td>3</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Proje 2</td>
<td>1</td>
</tr>
</tbody>
</table>

Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Maliyet öğesi</th>
<th>Maliyet davranışı</th>
<th>Birimler</th>
<th>Ücret</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>İK</td>
<td>10001</td>
<td>Değişken maliyet</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Büyüklük</th>
<th>Maliyet öğesi</th>
<th>Tahsisat faktörü</th>
<th>Tutar</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>Proje 1</td>
<td>3</td>
<td>10001</td>
<td>(3 ÷ 1) × 10,00</td>
<td>30.00</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Proje 2</td>
<td>1</td>
<td>10001</td>
<td>(1 ÷ 1) × 10,00</td>
<td>10,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Günlük

<table>
<thead>
<tr>
<th>Günlük</th>
<th>Günlük türü:</th>
<th colspan="3">Mali takvim dönemi</th>
<th>Sürüm</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>Genel gider oranı hesaplaması günlüğü</td>
<td>Mali</td>
<td>2017</td>
<td>Dönem 1</td>
<td>Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>Yevmiye defteri girişleri (Genel gider oranı hesaplaması için yevmiye defteri girişleri)

<table>
<thead>
<tr>
<th>Muhasebeleşme tarihi</th>
<th colspan="2">Maliyet nesnesi</th>
<th>Büyüklük</th>
</tr>
</thead>
<tbody>
<tr>
<td>31 Ocak 2017</td>
<td>Proj 1</td>
<td>Dahili Proj 1</td>
<td>3,00</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>Proj 2</td>
<td>Dahili Proj 2</td>
<td>1.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Maliyet girişleri

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th colspan="2">Maliyet öğesi</th>
<th>Maliyet davranışı</th>
<th>Tutar</th>
<th>Muhasebeleşme tarihi</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>İK</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>-30,00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>Proj 1</td>
<td>Dahili Proj 1</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>30.00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>İK</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>-10,00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Dahili Proj 2</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>10,00</td>
<td>31 Ocak 2017</td>
</tr>
</tbody>
</table>

Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.

### <a name="step-4-process-the-cost-allocation-calculation"></a>Adım 4: Maliyet tahsisat hesaplamayı işle

Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder. Finance karşılıklı tahsisat yöntemini desteklemektedir. Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır. Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler. Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir. Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir. Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir. 

[![Karşılıklı yöntemi.](./media/reciprocal-method.png)](./media/reciprocal-method.png)

#### <a name="define-the-cost-allocation"></a>Maliyet tahsisatını tanımla

Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir, Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur. HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>HR hizmetleri</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>Paketleme</td>
<td>10</td>
</tr>
</tbody>
</table>

Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur. Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Finans hizmetleri</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>Paketleme</td>
<td>35</td>
</tr>
</tbody>
</table>

Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur. Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Derleme Hizmetleri (saat)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Ürün 1</td>
<td>60</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Ürün 2</td>
<td>20</td>
</tr>
</tbody>
</table>

Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur. Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Ambalajlama hizmetleri (saat)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Ürün 1</td>
<td>80</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Ürün 2</td>
<td>15</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler, doğrudan kaynak verilerinden alınabilir. Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın. Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Büyüklük</th>
<th>Tahsisat faktörü</th>
<th>Tutar</th>
<th>Maliyet davranışı</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>35</td>
<td>(35 ÷ 100) × 500,00</td>
<td>175.00</td>
<td>Sabit maliyet</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>55</td>
<td>(55 ÷ 100) × 500,00</td>
<td>275.00</td>
<td>Sabit maliyet</td>
</tr>
<tr>
<td>CC004</td>
<td>Paketleme</td>
<td>10</td>
<td>(10 ÷ 100) × 500,00</td>
<td>50,00</td>
<td>Sabit maliyet</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>35</td>
<td>(35 ÷ 100) × 1.245,71</td>
<td>436.00</td>
<td>Değişken maliyet</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>55</td>
<td>(55 ÷ 100) × 1.245,71</td>
<td>685.14</td>
<td>Değişken maliyet</td>
</tr>
<tr>
<td>CC004</td>
<td>Paketleme</td>
<td>10</td>
<td>(10 ÷ 100) × 1.245,71</td>
<td>124.57</td>
<td>Değişken maliyet</td>
</tr>
</tbody>
</table>

Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Büyüklük</th>
<th>Tahsisat faktörü</th>
<th>Tutar</th>
<th>Maliyet davranışı</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>65</td>
<td>(65 ÷ 100) × (500,00 + 175,00)</td>
<td>438.75</td>
<td>Sabit maliyet</td>
</tr>
<tr>
<td>CC004</td>
<td>Paketleme</td>
<td>35</td>
<td>(35 ÷ 100) × (500,00 + 175,00)</td>
<td>236.25</td>
<td>Sabit maliyet</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>65</td>
<td>(65 ÷ 100) × (7.714,29 + 436,00)</td>
<td>5,297.69</td>
<td>Değişken maliyet</td>
</tr>
<tr>
<td>CC004</td>
<td>Paketleme</td>
<td>35</td>
<td>(35 ÷ 100) × (7.714,29 + 436,00)</td>
<td>2,852.60</td>
<td>Değişken maliyet</td>
</tr>
</tbody>
</table>

Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Büyüklük</th>
<th>Tahsisat faktörü</th>
<th>Tutar</th>
<th>Maliyet davranışı</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Ürün 1</td>
<td>60</td>
<td>(60 ÷ 80) × (275,00 + 438,75)</td>
<td>535.31</td>
<td>Sabit maliyet</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Ürün 2</td>
<td>20</td>
<td>(20 ÷ 80) × (275,00 + 438,75)</td>
<td>178.44</td>
<td>Sabit maliyet</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Ürün 1</td>
<td>60</td>
<td>(60 ÷ 80) × (5.297,69 + 685,14)</td>
<td>4,487.12</td>
<td>Değişken maliyet</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Ürün 2</td>
<td>20</td>
<td>(20 ÷ 80) × (5.297,69 + 685,14)</td>
<td>1,495.71</td>
<td>Değişken maliyet</td>
</tr>
</tbody>
</table>

Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th>Büyüklük</th>
<th>Tahsisat faktörü</th>
<th>Tutar</th>
<th>Maliyet davranışı</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prod 1</td>
<td>Ürün 1</td>
<td>80</td>
<td>(80 ÷ 95) × (50,00 + 236,25)</td>
<td>241.05</td>
<td>Sabit maliyet</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Ürün 2</td>
<td>15</td>
<td>(15 ÷ 95) × (50,00 + 236,25)</td>
<td>45.20</td>
<td>Sabit maliyet</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Ürün 1</td>
<td>80</td>
<td>(80 ÷ 95) × (2.852,60 + 124,57)</td>
<td>2,507.09</td>
<td>Değişken maliyet</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Ürün 2</td>
<td>15</td>
<td>(15 ÷ 95) × (2.852,60 + 124,57)</td>
<td>470.08</td>
<td>Değişken maliyet</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Yevmiye defteri girişleri (maliyet nesnesi bakiyesi yevmiye defteri girişleri)

<table>
<thead>
<tr>
<th>Günlük</th>
<th>Günlük türü:</th>
<th colspan="3">Mali takvim dönemi</th>
<th>Sürüm</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>Maliyet tahsisatı günlüğü</td>
<td>Mali</td>
<td>2017</td>
<td>Dönem 1</td>
<td>Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>Yevmiye defteri satırları

<table>
<thead>
<tr>
<th>Muhasebeleşme tarihi</th>
<th colspan="2">Maliyet nesnesi</th>
<th colspan="2">Maliyet öğesi</th>
<th>Maliyet davranışı</th>
<th>Tutar</th>
</tr>
</thead>
<tbody>
<tr>
<td>31 Ocak 2017</td>
<td>CC001</td>
<td>İK</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>500.00</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>CC001</td>
<td>İK</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>1,245.71</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>675.00</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>8,150.29</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>CC003</td>
<td>Montaj</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>713.75</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>CC003</td>
<td>Montaj</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>5,982.83</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>CC003</td>
<td>Paketleme</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>286.25</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>CC003</td>
<td>Paketleme</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>2,977.17</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>Prod 1</td>
<td>Ürün 1</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>776.36</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>Prod 1</td>
<td>Ürün 1</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>6,994.21</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>Prod 2</td>
<td>Ürün 1</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>223.64</td>
</tr>
<tr>
<td>31 Ocak 2017</td>
<td>Prod 2</td>
<td>Ürün 1</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Maliyet girişleri

<table>
<thead>
<tr>
<th colspan="2">Maliyet nesnesi</th>
<th colspan="2">Maliyet öğesi</th>
<th>Maliyet davranışı</th>
<th>Tutar</th>
<th>Muhasebeleşme tarihi</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>İK</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>-500.00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>175.00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>275.00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Paketleme</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>50,00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC001</td>
<td>İK</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>-1.245,71</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>436.00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>685.14</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Paketleme</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>124.57</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>-675,00</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>438.75</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Paketleme</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>236.25</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Finans</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>-8.150,29</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>5,297.69</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Paketleme</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>2,852.60</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>-713.75</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Ürün 1</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>535.31</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Ürün 2</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>178.44</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>-5.982,83</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Ürün 1</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>4,487.12</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Ürün 2</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>1,495.71</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>-286,25</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Ürün 1</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>241.05</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Ürün 2</td>
<td>10001</td>
<td>Elektrik</td>
<td>Sabit maliyet</td>
<td>45.20</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Montaj</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>-2.977,17</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>Prod 1</td>
<td>Ürün 1</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>2,507.09</td>
<td>31 Ocak 2017</td>
</tr>
<tr>
<td>Prod 2</td>
<td>Ürün 2</td>
<td>10001</td>
<td>Elektrik</td>
<td>Değişken maliyet</td>
<td>470.08</td>
<td>31 Ocak 2017</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>Sonuç
Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir. Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler. Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar. Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.

Maliyet öğesi | Maliyet nesnesi<br>CC099 | Maliyet nesnesi<br>CC001 | Maliyet nesnesi<br>CC002 | Maliyet nesnesi<br>CC003 | Maliyet nesnesi<br>CC004 | Maliyet nesnesi<br>Proj 1 | Maliyet nesnesi<br>Proj 2 | Maliyet nesnesi<br>Prod 1 | Maliyet nesnesi<br>Prod 2 | Toplam
---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:
10001 Elektrik | 0,00 | 0,00 | 0,00 | 0,00 |  | 30.00 | 10,00 | 7,770.57 | 2,189.43 | 10,000.00 |
Sınıflandırılmamış | 0,00 |  |  |  |  |  |  |  |  |  |
Sabit maliyet | 0,00 | 0,00 | 0,00 | 0,00 | 0,00 |  |  | 776.36 | 223.64 | 1,000.00 |
Değişken maliyet | 000 | 0,00 | 0,00 | 0,00 | 0,00 | 30.00 | 10,00 | 6,994.21 | 1,965.79 | 9,000.00 |

> [!NOTE]
> Bu makalede, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığı gösterilmektedir. Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir. Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir. Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz. Daha fazla bilgi için bkz. [Maliyet yuvarlama ilkesi ve genel gider hesaplaması](cost-rollup.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
