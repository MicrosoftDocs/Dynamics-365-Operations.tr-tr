---
title: "Ürün reçetesi ve formül satırlarını ambara serbest bırakma"
description: "Bu konuda, ürün reçetesi satırları ve formül satırları için ambara ham madde serbest bırakma süreci açıklanmaktadır."
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.3.0, Operations, UnifiedOperations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-03-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 6aec3532a36a2c1e67ee0c189e45a352ad7670f6
ms.contentlocale: tr-tr
ms.lasthandoff: 12/14/2017

---

# <a name="release-bom-and-formula-lines-to-the-warehouse"></a>Ürün reçetesi ve formül satırlarını ambara serbest bırakma

Bu konuda, ürün reçetesi satırları ve formül satırları için ambara ham madde serbest bırakma süreci açıklanmaktadır. Bir ürün reçetesi veya formül satırını ambara serbest bıraktığınızda, sistem önce malzemenin üretim sürecinde tüketileceği yer alan atölyedeki ürün girişi konumunda halihazırda kullanılabilir olup olmadığını belirler.

- Malzeme üretim giriş konumunda kullanılabilir durumdaysa, malzemenin ambara serbest bırakılması için sinyal verildikten hemen sonra bu konumdan çekilir.
- Malzeme üretim giriş konumunda kullanılabilir durumda değilse, malzeme serbest bırakma malzemenin ambardaki konumlardan ürün giriş konumuna taşınması gerektiğini belirtir. Malzeme, ham madde çekmeyle yönelik ambar işi aracılığıyla taşınır. Bu nedenle, ham madde çekmeye yönelik ambar süreçlerinin yapılandırılması gerekir. Daha fazla bilgi için bkz. [Stok yenileme](../warehousing/replenishment.md) ve [İş şablonları ve konum yönergelerini kullanarak ambar işini denetleme](../warehousing/control-warehouse-location-directives.md).

## <a name="methods-for-releasing-bom-and-formula-lines"></a>Ürün reçetesi ve formül satırlarını serbest bırakma yöntemleri

Ürün reçetesi ve formül satırlarını serbest bırakmayı yapılandırabilirsiniz; böylece bu işlem bir üretim emrini veya toplu siparişi serbest bırakmanın bir parçası olarak gerçekleşir. Alternatif olarak, serbest bırakma bir toplu iş tarafından denetlenebilir veya el ile etkileşim olarak yapılabilir.

Ürün reçetesi ve formül satırlarını serbest bırakmak için kullanılan yöntem **Üretim satırı serbest bırakma** parametresi tarafından denetlenir. Bu parametreyi **Üretim denetimi** \> **Kurulum** \> **Üretim parametreleri** altında bulabilirsiniz.

- **Ürün reçetesi ve formül satırlarını üretim emrini veya toplu siparişi serbest bırakmanın bir parçası olarak serbest bırakma** – Bu yöntemde, bir üretim veya toplu iş emri için ürün reçetesi ve formül satırları siparişi serbest bırakma işleminin bir parçası olarak serbest bırakılır. Genellikle, bir üretim veya toplu iş emrinin serbest bırakılması sırasında, üretim işleri atölye çalışanlarına serbest bırakılır ve üretim belgeleri yazdırılır. Bu işlem sırasında siparişin durumu da **Serbest bırakıldı** olarak değişir.
- **Ürün reçetesi veya formül satırlarını bir toplu iş aracılığıyla veya el ile etkileşim olarak serbest bırakma** – Bu yöntemde, ürün reçetesi ve formül satırları yalnızca **Ürün reçetesi ve formül satırlarını otomatik serbest bırakma** toplu işi aracılığıyla veya el ile etkileşim olarak serbest bırakılabilir. Ürün reçetesi ve formül satırlarını el ile serbest bırakmak için, Eylem Bölmesindeki üretim emri liste sayfasında veya üretim emri ayrıntıları sayfasında **Ambar için serbest bırak**'ı seçin.

## <a name="releasing-the-bom-and-formula-lines-by-using-a-batch-job"></a>Ürün reçetesi veya formül satırlarını bir toplu iş kullanarak serbest bırakma

**Ürün reçetesi ve formül satırlarını otomatik serbest bırak** toplu işi, serbest bırakılacak kalan miktarı bulunan seçili ürün reçetesi ve formül satırları ile ilerler. İş yalnızca **Serbest bırakıldı**, **Başladı** veya **Bitti olarak rapor edildi** durumundaki siparişleri dikkate alır. Bir ürün reçetesi veya formül satırında serbest bırakılmak üzere kalan bir miktar varsa, iş yalnızca daha önce fiziksel olarak rezerve edilmiş olan miktar ve fiziksel olarak kullanılabilir olan miktar tarafından karşılanabilecek olan kadar miktarı serbest bırakır.

### <a name="example-of-a-batch-job-release"></a>Toplu iş serbest bırakma örneği

| Senaryo | Serbest bırakılacak kalan miktar | Fiziksel olarak ayrılmış miktar | Fiziksel olarak kullanılabilir miktar | Toplu iş tarafından serbest bırakılan miktar |
|----------|-------------------------------|------------------------------|-------------------------------|------------------------------------|
| 1        | 100                           | 20                           | 90                            | 100                                |
| 2        | 100                           | 20                           | 70                            | 90                                 |
| 3        | 100                           | 0                            | 90                            | 90                                 |
| 4        | 100                           | 0                            | 110                           | 100                                |
| 5        | 100                           | 20                           | 0                             | 20                                 |

### <a name="batch-job-setup"></a>Toplu işi kurulumu

**Ürün reçetesi ve formül satırlarını otomatik serbest bırakma** toplu işi sorgusunda, işin serbest bırakılmamış miktarları bulunan satırlara kaç gün önceden bakması gerektiği belirlemek için bir filtre ölçütü ayarlayabilirsiniz. İş sorgusunda, **Ham madde tarihi** alanı, filtre ölçütü olarak **(LessThanDate())** işlevini kullanır.

Aşağıdaki örnekte üretim emri için montaj ve paketlemeyi kapsayan 10 ve 20 şeklinde iki işi bulunan bir üretim emri gösterilmektedir. Her iş bir miktar malzeme tüketmek üzere ayarlanır. Bu örnekte, zaman çizgisi altında yeşil okla belirtilen serbest bırakma zaman aralığı **(LessThanDate())** ölçütünde belirtilen gün sayısına eşittir. Örneğin, **(LessThanDate(2))** işin serbest bırakılmamış olan miktarlara yalnızca iki günlük zaman aralığında bakması gerektiğini belirtir.

![İki toplu işi bulunan bir üretim emri örneği](media/bach-job-setup.PNG)

## <a name="releasing-material-per-operation-number-or-in-proportion-to-the-amount-of-finished-goods"></a>Malzemeyi işlem numarasına göre veya mamul malların miktarıyla orantılı serbest bırakma

Malzemeleri **Üretim emri serbest bırakmada** parametresi ayarını kullanarak serbest bırakırsanız, el ile serbest bırakma yaptığınızda, malzeme serbest bırakmayı denetlemek için iki seçeneğiniz bulunur:

- Malzemeyi işlem numarasına göre serbest bırakma.
- Malzemeyi mamul malların miktarıyla orantılı olarak bırakma.

### <a name="release-material-per-operation-number"></a>Malzemeyi işlem numarasına göre serbest bırakma

Malzemenin serbest bırakılması gereken işlemleri denetlemek için **Ambara serbest bırak** sayfasını kullanın.

- **Üretim denetimi** \> **Üretim emirleri** \> **Tüm üretim emirleri**'ni seçin, bir üretim emri seçin ve ardından **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin. Ardından **İlk İşlem No.** ve **Son İşlem No.** alanlarını kullanarak işlem numaraları aralığını belirtin.

Aşağıdaki örnekte 10 ve 20 şeklinde iki işlemi bulunan bir üretim emri gösterilmektedir. Bu örnekte, serbest bırakmayı 10 işlemiyle sınırlarsanız yalnızca M9203 malzemesi serbest bırakılacaktır.

![İşlem numarasına göre malzeme serbest bırakma örneği](media/two-operations.PNG)

### <a name="release-material-in-proportion-to-the-amount-of-finished-goods"></a>Malzemeyi mamul malların miktarıyla orantılı olarak bırakma

Ham maddeyi kısmi bir mamul ürün miktarı için veya belirli bir birimde serbest bırakabilirsiniz.

- Mamul ürünlerin kısmi bir miktarı için ham maddeyi serbest bırakmak üzere **Üretim denetimi** \> **Üretim emirleri** \> **Tüm üretim emirleri**'ni seçin, bir üretim emri seçin ve ardından **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin. Ardından **Miktar** alanına bir miktar girin.

    Örneğin, 1000 parça (parça) için bir üretim emri oluşturulur ve planlanır. Atölye yöneticisi bir sonraki vardiya için 100 parçalık üretim planlar ve yalnızca bu vardiya için malzemeleri serbest bırakmak ister. Bu durumda, yönetici **Miktar** alanını kullanarak malzemeyi bir sonraki vardiya için planlanan 100 parça için serbest bırakmak bırakabilir.

- Ham maddeyi belirli bir birimde serbest bırakmak üzere **Üretim denetimi** \> **Üretim emirleri** \> **Tüm üretim emirleri**'ni seçin, bir üretim emri seçin ve ardından **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin. Daha sonra **Birim** alanını kullanarak malzemenin serbest bırakılacağı mamul ürün birimini seçin.

    Kullanılabilir birimler mamul ürününün birim sırası grubu kodunda tanımlanır.

    Örneğin, mamul ürün pound (libre) ve palet (PL) arasında şu birin dönüştürmeye sahiptir: 1 PL = 100 libre 10.000 libre mamul ürün için üretim emri oluşturmak üzere üretmeyi planladığınız palet sayısı için ham maddeyi serbest bırakabilirsiniz. Birim olarak **PL** seçin ve ardından **Miktar** alanında karşılık gelen sayıyı seçin.

