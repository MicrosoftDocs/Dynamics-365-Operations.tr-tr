---
title: Dalga tahsisatı
description: Bu konu, dalga tahsisatı adımının nasıl ayarlanacağını açıklar (paralel işlemenin nasıl etkinleştirileceği dahil).
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 541e6c42ae1fa7d803b5becc1b52e34860777594
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920610"
---
# <a name="wave-allocation"></a>Dalga tahsisatı

[!include [banner](../includes/banner.md)]

Dalga işleme zaman alabilir ve işlem süresinin çoğu tahsisat adımında ve iş oluşturma adımında harcanır.

Bu adımların her birini paralel olarak çalıştırmak mümkündür, bu da dalga işlemenin performansını artırır ve aynı ambardaki daha fazla dalga üretimi için izin verebilir. Bu konu, dalga tahsisat yönteminin paralel çalışacak şekilde nasıl ayarlanacağını açıklar. İş oluşturmanın paralel olarak çalışacak şekilde ayarlanması hakkında daha fazla bilgi için, bkz. [Dalga sırasında iş oluşturmayı planlama](configure-wave-schedule-work-creation.md).

Daha önce, bir seferde aynı anda tek bir dalga tahsis etmek mümkündü. Bu sınırlama kaldırıldı ve yalnızca ayırma hiyerarşisinde konumun üzerinde olan madde ve boyutları kilitleyen yeni bir kısıtlamayla değiştirildi. Yerleşimin üzerindeki boyutlar her zaman ürün boyutlarını içerir. Örneğin, bir öğe *renk* kullanılarak yapılandırılırsa, *kırmızı*, *mavi* ve *sarı* çeşitlerinin her biri paralel olarak işlenebilir.

Bu, konumun üzerinde aynı boyutlara sahip aynı madde bir dalgaya göre ayrılmazsa, diğer dalgaların aynı madde ve boyutlar için kilit almayı beklemesi gerektiği anlamına gelir. Kilit zamanında elde edilemezse, bir hata oluşacaktır ve dalga işleme başarısız olur.

Paralel işlemeyi kullanmak için, dalganın toplu işte çalışması gerekir.

## <a name="performance-improvements"></a>Performans iyileştirmeleri

Paralel işlemenin performans yararları iki kategoride yapılır:

- **Geliştirilmiş aktarım hızı**: Dalgaların aktarım hızı özellikle de dalgalar içindeki öğelerde çakışma bulunmayan senaryolar için paralel işlem konfigüre edilmemiş olsa bile gelişecektir.
- **Tek bir dalga için ayırmanın geliştirilmesi**: Müşteri verilerinde test etme, paralel ayırmaya geçtikten sonra yaklaşık % 50 performans iyileştirmesi olduğunu göstermiştir. Paralel işleme, yerleşimin üzerindeki madde ve boyut başına gerçekleştirilir, bu nedenle iyileştirmeler bir dalganın kaç farklı öğe içerdiğine, kullanılabilir alt yapıya ve iş oluşturma süresi ve tahsisat süresine bağlıdır.

## <a name="configure-parallel-allocation"></a>Paralel tahsisatı yapılandırma

### <a name="warehouse-management-parameters"></a>Ambar yönetim parametreleri

Paralel tahsisat işlemeyi kullanmak için **ambar yönetimi > kurulum > ambar yönetimi parametrelerine** gidin, **dalga işleme** sekmesini açın ve aşağıdaki ayarları yapın:

- **Dalga işleme toplu iş grubu**: Dalgaların ilk işlenmesinin kullanması gereken toplu iş grubunu seçin. Tahsisatın sonraki işlemesi farklı toplu gruplar kullanılarak yapılabilir.
- **Dalgaları toplu işle**: Paralel işlemeyi kullanmak için *Evet* olarak ayarlayın.
- **Kilidi bekle (ms)**: Tahsisat adımının, başka bir tahsisat kaynağı tarafından kilitlenmiş olan bir sistem kaynağı için bekleyeceği zamanı, milisaniye cinsinden girin. Bu süre aşıldığında, dalga işlenmez ve bir hata iletisi görüntülenir. Bir mantıksal birimin tahsisatının bitmesi için en az birkaç saniye izin vermeniz önerilir.

**Ambar yönetimi parametreleri** sayfasındaki bu ve diğer dalga işleme seçenekleri hakkında bilgi için bkz. [Dalga işleme için ambar parametreleri](wave-warehouse-parameters.md).

## <a name="wave-process-methods"></a>Dalga işleme yöntemleri

Paralel işlemeyi ayarlamak için:

1. **Ambar yönetimi > Kurulum > Dalgalar > Dalga işleme yöntemleri**'ne gidin.
1. Kılavuzdaki `allocateWave` yöntemini seçin.
1. Eylem Panosundan **Görevi Yapılandırması**'nı seçin.
1. **Dalga nakletme yöntemi görev yapılandırması** sayfası açılır. Bu kılavuzda, `allocateWave` yöntemini yapılandırdığınız her ambar listelenir. Paralel işleme yalnızca listelenen ambarlar için kullanılacaktır. Gerektiğinde ızgaraya ambar eklemek veya kaldırmak için eylem bölmesi düğmelerini kullanın. 
1. Her ambar için aşağıdaki ayarları yapın:
    - **Maksimum Toplu görev sayısı**: Seçili Ambar tahsisatı için kullanılacak toplu iş görevlerinin sayısını belirtin. Toplu görevlerin en uygun sayısı kullanılabilir alt yapıya ve sunucuda işlenmekte olan diğer toplu işlere bağlıdır. Dalga işlemeye ayrılmış dört ana ortamda yapılan testler, sekiz görev kullanmanın iyi sonuç ürettiğini gösterdi.
    - **Dalga işleme toplu işi**: Özel toplu iş grupları, tahsisat işlemenin ambar başına ölçeklenmesini sağlamak üzere farklı ambarlar için kullanılabilir.

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a>Tüm yasal varlıklarda paralelleşmeyi etkinleştirme veya devre dışı bırakma

Dalga işleme performansını artırmaya yardımcı olacağından, tüm yasal varlıklarda paralel olarak çalıştırmak için `allocateWave` yöntemini ayarlamanız önerilir. Supply Chain Management sürüm 10.0.17'den başlayarak, *dalga tahsisat yöntemi için dalga paralelizasyonu* özelliği tüm yeni ve güncelleştirilmiş yüklemelerde varsayılan olarak etkinleştirilir ve yeniden kapatılamaz. Bu özellik etkinleştirildikten sonra aşağıdaki gerçekleşir:

- `allocateWave` Yöntemi, aynı anda çalışacak olan ve paralel işlem sayısına eşdeğer olan görevlerin sayısını tanımlamak için **dalga işleme yöntemleri** sayfasını kullanmanıza olanak tanıyan bir görev yapılandırma ayarı içerecek şekilde güncelleştirilir. Sonuç olarak, dalga tahsisatı adımında kullanılan süre (genellikle toplam işleme süresinin %30'u ile yüzde 60'ı kadardır), kabaca görev sayısına eşdeğer bir oranda azaltılır. Ayrıca, bu görevleri işlemek için hangi toplu işin atanacağını seçmek de mümkündür. Tüm yasal varlıklarınızın, dalgaları toplu işle işleyecek şekilde yapılandırılacağını unutmayın. Dalgaları toplu işle işlemek üzere yapılandırılmış olan ambarlar için ve `allocateWave` yöntemini paralel olarak kullanmak üzere yapılandırılmış ambarlar için, varolan yapılandırma korunur.
- Varsayılan olarak, tüm yeni yasal varlıklar dalgaları toplu işle işleyecek şekilde yapılandırılır. **Ambar yönetimi işlemleri** seçeneği etkinleştirilmiş tüm yeni ambarlar, Varsayılan olarak paralel çalışacak şekilde yapılandırılmış `allocateWave` yöntemine sahip olacaktır.
- **Ambar yönetimi parametreleri** sayfasında, **Dalgaları toplu olarak işle** *Evet* olarak ayarlanır ve **kilidi bekle (ms)** Varsayılan olarak 15 saniyeye ayarlanır. Bu, tüm dalgalarının toplu olarak yürütüleceği anlamına gelir. Dalga çalıştığında, tahsisat adımı sırasında madde ve konum üzerindeki boyutlar için bir kilit alır. Başka bir dalga işleme görevi aynı kayıt için aynı kilidi elde etmeye çalışırsa, geçerli işlem bitene kadar durdurulur. **Kilidi bekle (ms)** ayarları sistemin kilit açılmadan önce bekleyeceği maksimum süreyi ayarlar.

Paralel tahsisat işleme, dalganın toplu işlenmesini gerektirir. Bu nedenle, özellikle dalga işleme, ilgili dalga yöntemleri için görev konfigürasyonuyla tanımlanan bir paralel işlem kullanıyorsa, **Dalgaları toplu işle** ayarını kapatırsanız dalga işleme performansınızı azaltabilirsiniz.

Gerekirse, *Dalga Yöntemi tahsisi için dalga paralelizasyonu* özelliği örneğiniz için otomatik olarak etkinleştirildiğinde varsayılan olarak yapılan ayarların her birini geri alabilirsiniz. Bunun için:

- **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin. **Dalga işleme** sekmesinde, **dalgaları toplu işle** ve **kilidi bekle (ms)** için tercih ettiğiniz değerleri uygulayın.
- **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga işleme yöntemleri**'ne gidin. `allocateWave` yöntemini seçin. Eylem bölmesinde, yöntemin paralel çalışacak şekilde ayarlandığı her ambarı listeleyen bir sayfa açmak için **görev yapılandırmasını** seçin. Listelenen her ambar için toplu iş görevlerini ve atanan dalga grubu sayısını gerektiği gibi değiştirin veya silin.

## <a name="troubleshooting"></a>Sorun Giderme

### <a name="troubleshoot-using-the-infolog"></a>Bilgi günlüğünü kullanmada sorun giderme

Toplu iş çerçevesi kullanıldığı için, dalga işleme sırasında oluşan hatalar, toplu işlerin bir parçası olarak yakalanacaktır. Bir dalgaya ilişkin toplu işleri okumak için:

1. **Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.
1. İncelemek istediğiniz dalgayı seçin.
1. Eylem Bölmesinde, **Dalga** sekmesini açın ve **Dalga** grubundan **Toplu işler**'i seçin.

Dalga işleme kendi kendini düzeltir, bu nedenle işleme sırasında algılanan tüm hata bilgi günlüğü kullanılarak rapor edilmelidir.

Paralel işlemeyle ilgili tipik bir hata, iki dalganın aynı öğeyi aynı anda ayırmaya çalışması ve biri tamamlanmadığı için diğerinin de belirtilen süre içinde kilit elde edememesi olabilir. Bu durum oluşursa toplu işler günlükleri madde kilidinin alınmadığını belirten bilgiler içerir ve bu durumda başarısız olan dalganın yeniden işlenmesi gerekir.

İşlem paralel olduğundan, işlemin durumunu izlemek için verilerin farklı tablolarda tutulması gerekir. Bu, toplu işlerin günlüklerinde tekrarlanan anahtar hataları gibi hatalar bulunduğu anlamına gelir.

Toplu görevlerdeki hatalar aynı zamanda toplu işler günlüğünün bir parçasıdır. En önemli bilgiler genellikle en altta yer alır.

Nadiren de olsa, örneğin SQL bağlantısı sona ermişse, dalga işlemenin, toplu işin çalıştığı, ancak işlemin durdurulduğu gibi görünen tutarsız bir durumda bitmesi mümkündür. Dalga, bunun gibi hataları işleyemez ve bir sonraki dalga çalıştırıldığında başarısız dalgaları Temizleme girişimi gerçekleştirilir. Alternatif olarak, geçerli dalga, tutarsız bir durumdaysa, aşağıdaki adımları uygulayın:

1. **Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.
1. Temizlemeniz gereken dalgayı seçin.
1. Eylem Bölmesinde, **Dalga** sekmesini açın ve **Dalga** grubundan **Dalga verisini temizle**'yi seçin.

### <a name="troubleshoot-using-the-wave-progress-log"></a>Dalga ilerlemesi günlüğünü kullanmada sorun giderme

**Ambar yönetimi parametreleri** sayfasında **dalga ilerlemesi günlükleri oluştur** seçeneği etkinse, bir maddenin her tahsisatı ve boyutları her başlayıp sona erdiğinde günlük kaydı oluşturulur. Bu günlüğü yalnızca gereksinim duyduğunuzda (örneğin, ilk test sırasında veya sorun giderme için) etkinleştirmelisiniz. Bu seçenek etkinleştirildiğinde, aşağıdaki adımları gerçekleştirerek günlüğü görüntüleyebilirsiniz:

1. **Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.
1. İncelemek istediğiniz dalgayı seçin.
1. Eylem Bölmesinde, **Dalga** sekmesini açın **Dalga** grubunda **İlerleme**'yi seçin.
