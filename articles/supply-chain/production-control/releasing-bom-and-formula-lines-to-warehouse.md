---
title: Ürün reçetesi ve formül satırlarını ambara serbest bırakma
description: Bu konuda, ürün reçetesi satırları ve formül satırları için ambara hammadde serbest bırakma süreci açıklanmaktadır.
author: johanhoffmann
manager: tfehr
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm, ProdParmReleaseToWarehouse, WHSReleaseToWarehouseProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: bf2beef30ba1cf6877325e686b76de5dc8d3ba55
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439643"
---
# <a name="release-bom-and-formula-lines-to-the-warehouse"></a>Ürün reçetesi ve formül satırlarını ambara serbest bırakma

[!include [banner](../includes/banner.md)]

Bu konuda, ürün reçetesi satırları ve formül satırları için ambara hammadde serbest bırakma süreci açıklanmaktadır. Bir ürün reçetesi veya formül satırını ambara serbest bıraktığınızda, sistem önce malzemenin üretim sürecinde tüketileceği yer alan atölyedeki ürün girişi konumunda halihazırda kullanılabilir olup olmadığını belirler.

- Malzeme üretim giriş konumunda kullanılabilir durumdaysa, malzemenin ambara serbest bırakılması için sinyal verildikten hemen sonra bu konumdan çekilir.
- Malzeme üretim giriş konumunda kullanılabilir durumda değilse, malzeme serbest bırakma malzemenin ambardaki konumlardan ürün giriş konumuna taşınması gerektiğini belirtir. Malzeme, hammadde çekmeyle yönelik ambar işi aracılığıyla taşınır. Bu nedenle, hammadde çekmeye yönelik ambar süreçlerinin yapılandırılması gerekir. Daha fazla bilgi için bkz. [Stok yenilemeye genel bakış](../warehousing/replenishment.md) ve [İş şablonları ve konum yönergelerini kullanarak ambar işini denetleme](../warehousing/control-warehouse-location-directives.md).

## <a name="methods-for-releasing-bom-and-formula-lines"></a>Ürün reçetesi ve formül satırlarını serbest bırakma yöntemleri

Ürün reçetesi ve formül satırlarını serbest bırakmayı yapılandırabilirsiniz; böylece bu işlem bir üretim emrini veya toplu siparişi serbest bırakmanın bir parçası olarak gerçekleşir. Alternatif olarak, serbest bırakma bir toplu iş tarafından denetlenebilir veya el ile etkileşim olarak yapılabilir.

Ürün reçetesi ve formül satırlarını serbest bırakmak için kullanılan yöntem **Üretim satırı serbest bırakma** parametresi tarafından denetlenir. Bu parametreyi **Üretim denetimi** \> **Kurulum** \> **Üretim parametreleri** altında bulabilirsiniz.

- **Ürün reçetesi ve formül satırlarını üretim emrini veya toplu siparişi serbest bırakmanın bir parçası olarak serbest bırakma** – Bu yöntemde, bir üretim veya toplu iş emri için ürün reçetesi ve formül satırları siparişi serbest bırakma işleminin bir parçası olarak serbest bırakılır. Genellikle, bir üretim veya toplu iş emrinin serbest bırakılması sırasında, üretim işleri atölye çalışanlarına serbest bırakılır ve üretim belgeleri yazdırılır. Bu işlem sırasında siparişin durumu da **Serbest bırakıldı** olarak değişir.
- **Ürün reçetesi veya formül satırlarını bir toplu iş aracılığıyla veya el ile etkileşim olarak serbest bırakma** – Bu yöntemde, ürün reçetesi ve formül satırları yalnızca **Ürün reçetesi ve formül satırlarını otomatik serbest bırakma** toplu işi aracılığıyla veya el ile etkileşim olarak serbest bırakılabilir. Ürün reçetesi ve formül satırlarını el ile serbest bırakmak için, Eylem Bölmesindeki üretim emri liste sayfasında veya üretim emri ayrıntıları sayfasında **Ambar için serbest bırak**'ı seçin.

Ürün reçetesi ve formül satırlarının toplu iş kullanılarak üretime serbest bırakılması hakkında hızlı bir tanıtım için YouTube'daki şu kısa videoyu izleyin: [Üretim malzeme çekmeyi toplu işte ambara serbest bırakma](https://www.youtube.com/watch?v=8urAJn50dQ8).

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

**Ürün reçetesi ve formül satırlarını otomatik serbest bırakma** toplu işi sorgusunda, işin serbest bırakılmamış miktarları bulunan satırlara kaç gün önceden bakması gerektiği belirlemek için bir filtre ölçütü ayarlayabilirsiniz. İş sorgusunda, **Hammadde tarihi** alanı, filtre ölçütü olarak **(LessThanDate())** işlevini kullanır.

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

Malzemenin, mamul mal miktarına orantılı olarak nasıl serbest bırakılacağı hakkında hızlı bir tanıtım için, YouTube'da [üretim emri serbest bırakma sürecindeki geliştirmeleri](https://www.youtube.com/watch?v=Rm3ojAz6Zu0) hakkındaki kısa videoyu izleyin.

### <a name="release-material-in-proportion-to-the-amount-of-finished-goods"></a>Malzemeyi mamul malların miktarıyla orantılı olarak bırakma

Hammaddeyi kısmi bir mamul ürün miktarı için veya belirli bir birimde serbest bırakabilirsiniz.

- Mamul ürünlerin kısmi bir miktarı için hammaddeyi serbest bırakmak üzere **Üretim denetimi** \> **Üretim emirleri** \> **Tüm üretim emirleri**'ni seçin, bir üretim emri seçin ve ardından **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin. Ardından **Miktar** alanına bir miktar girin.

    Örneğin, 1000 parça (parça) için bir üretim emri oluşturulur ve planlanır. Atölye yöneticisi bir sonraki vardiya için 100 parçalık üretim planlar ve yalnızca bu vardiya için malzemeleri serbest bırakmak ister. Bu durumda, yönetici **Miktar** alanını kullanarak malzemeyi bir sonraki vardiya için planlanan 100 parça için serbest bırakmak bırakabilir.

- Hammaddeyi belirli bir birimde serbest bırakmak üzere **Üretim denetimi** \> **Üretim emirleri** \> **Tüm üretim emirleri**'ni seçin, bir üretim emri seçin ve ardından **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin. Daha sonra **Birim** alanını kullanarak malzemenin serbest bırakılacağı mamul ürün birimini seçin.

    Kullanılabilir birimler mamul ürününün birim sırası grubu kodunda tanımlanır.

    Örneğin, mamul ürün pound (libre) ve palet (PL) arasında şu birin dönüştürmeye sahiptir: 1 PL = 100 libre 10.000 libre mamul ürün için üretim emri oluşturmak üzere üretmeyi planladığınız palet sayısı için hammaddeyi serbest bırakabilirsiniz. Birim olarak **PL** seçin ve ardından **Miktar** alanında karşılık gelen sayıyı seçin.
