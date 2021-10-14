---
title: Dalga sırasında iş oluşturmayı zamanlama
description: Bu konu, İş oluşturmayı zamanlama dalga işleme yönteminin nasıl ayarlanacağını ve kullanılacağını açıklamaktadır.
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 358f5a87cdb42f0ff646948da8d38475cf49e3f2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577924"
---
# <a name="schedule-work-creation-during-wave"></a>Dalga sırasında iş oluşturmayı zamanlama

[!include [banner](../../includes/banner.md)]

Sistemin paralel işlemeyi kullanarak iş oluşturmasıyla dalga işleme aktarım hızını artırmak için dalga işlemenin parçası olarak *İş oluşturmayı zamanla* özelliğini kullanın.

İşlev etkinleştirildiğinde, planlanan çalışma otomatik olarak oluşturulur ve sistem daha sonra bunu asılı işi oluşturmak için kullanılır. Dalga yükü satırlarının sayısı önceden belirlenmiş bir eşiğe ulaşırsa sistem paralel, zaman uyumsuz işlem uygulayarak asıl işi daha hızlı oluşturur.

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a>Özellik yönetiminde, planlanan iş oluşturma özelliklerini açma

Bu konuda açıklanan özellikleri kullanmak için, bunlar sisteminiz için açık olmalıdır. Aşağıdaki özellikleri aşağıdaki sırada açmak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanın:

1. **Kuruluş genelinde iş durdurma**: Planlanan iş oluşturma işleminin hem el ile hem de otomatik yapılandırması için gereklidir.
1. **İş oluşturmayı planlama**: Planlanan iş oluşturma işleminin hem el ile hem de otomatik yapılandırması için gereklidir.
1. **Kuruluş genelinde "İş oluşturmayı planlama" dalga yöntemi**: Planlanan iş oluşturma işleminin otomatik yapılandırması için gereklidir. Yalnızca el ile yapılandırmayı kullanacaksanız bu özelliğe gerek yoktur.

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a>Planlanan iş oluşturmayı otomatik olarak yapılandırma

*Kuruluş genelinde "iş oluşturmayı planlama" dalga yöntemi* özelliğini etkinleştirirseniz, aşağıdakiler sistem üzerinde otomatik olarak gerçekleşir:

- *İş oluşturmayı planlama* dalga yöntemi (`WHSScheduleWorkCreationWaveStepMethod`), tüm yasal varlıklarda paralel çalışacak şekilde eklenir ve yapılandırılır.
- Hem Sevkiyat, hem de **Dalga şablon türü** *Sevkiyat* ve **Şablon durumu** *geçerli* olarak ayarlanmış, tüm yasal varlıklardaki dalga şablonlarında *İş Oluştur* yöntemi *İş oluşturmayı planla* ile değiştirilecektir. Ancak, *iş oluştur* yönteminin yinelenebilir olmasına izin verilen yasal varlıklardan gelen dalga şablonları değiştirilmeyecektir.
- **Ambarı yönetim işlemlerini kullan** ayarı etkinleştirilmiş olan tüm tüzel kişilikler için *iş oluşturmayı planla* yöntemi görev yapılandırmaları oluşturulacaktır. Bu, *İş oluşturmayı planla* yönteminin varsayılan olarak paralel çalışacağı anlamına gelir. **Ambar yönetim işlemlerini kullan** ayarını *Hayır*'dan *Evet*'e değiştirdiğiniz mevcut Ambarla da bu yöntemi varsayılan olarak paralel olarak çalıştırır.
- Tüm tüzel varlıklar dalgaları toplu iş olarak işleyecek ve **Kilidi bekle (ms)** önceden *0* ms olarak ayarlanmışsa varsayılan değer olan *60.000* Ms değerine ayarlanacaktır.
- Oluşturduğunuz tüm yeni dalga şablonları, *İş oluşturmayı planla* dalga yöntemi yerine *İş oluştur* dalga yöntemine sahip olacaktır.

Varolan görev ve dalga işleme yapılandırmaları, son olarak dalgaları işlemek üzere konfigüre edilmiş olan tüm yasal varlıklar için ve *İş oluşturmayı zamanla* yöntemini paralel olarak kullanacak şekilde konfigüre edilmiş tüm ambarlarda saklanacaktır.

Gerekirse, aşağıdakileri yaparak, *kuruluş genelinde iş oluşturmayı planla dalga yöntemi* özelliğini etkinleştirdiğinizde otomatik olarak yapılan ayarların herhangi birini veya tümünü el ile geri alabilirsiniz:

- Dalga şablonları için **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin. *İş oluşturmayı planla* yöntemini, *İş oluştur* ile değiştirin.
- Ambar parametreleri için **Ambar yönetimi\>Kurulum \> Ambar yönetim parametreleri**'ne gidin. **Dalga işleme** sekmesinde, **dalgaları toplu işle** ve **kilidi bekle (ms)** için tercih ettiğiniz değerleri uygulayın.
- Dalga yöntemleri için **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga işleme yöntemleri**'ne gidin. `WHSScheduleWorkCreationWaveStepMethod` öğesini seçin ve Eylem Panosundan **Görev Yapılandırması**'nı seçin. Listelenen her ambar için toplu iş görevlerini ve atanan dalga grubu sayısını gerektiği gibi değiştirin veya silin.

## <a name="manually-configure-scheduled-work-creation"></a>Planlanan iş oluşturmayı elle yapılandırma

[*Organizasyon genelinde "iş oluşturmayı planla dalga yöntemi* özelliğini etkinleştirmediyseniz](#Auto-enable-schedule-work-creation), bu bölümde sağlanan yordamları kullanarak planlanan iş oluşturmayı gerektiği gibi el ile konfigüre edebilirsiniz.

### <a name="manually-enable-batch-processing-of-waves"></a>Dalgaların toplu işlenmesini etkinleştirme

Ambar işi oluştururken paralel zaman uyumsuz yöntemden yararlanmak için dalga işleminizin toplu iş olarak çalışıyor olması gerekir. Bunu ayarlamak için:

1.  **Ambar yönetimi \> Kurulum \> Ambar yönetimi parametreleri**'ne gidin.
1. **Genel** sekmesinde, **Dalgaları toplu iş halinde işle** seçeneğini *Evet* olarak ayarlayın. İsteğe bağlı olarak, toplu iş kuyruğu işlemenin diğer işlemlerle aynı anda çalışmasını önlemek için özel bir **Dalga işleme toplu iş grubu** da seçebilirsiniz.
1. Sistem, aynı anda birden fazla dalga işlerken geçerli olan **Kilit süresini bekle (ms)** özelliğini de ayarlayabilirsiniz. Daha uzun dalga işlemleri için *60000* değerini öneririz.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Mevcut dalga şablonları için yeni dalga adımı yöntemini el ile etkinleştirme

Yeni dalga adımı yöntemini oluşturarak ve bu yöntemi paralel zaman uyumsuz görev işleme için etkinleştirerek başlayın.

1.  **Ambar yönetimi \>Kurulum \> Dalgalar \> Dalga işleme yöntemleri**'ne gidin.
1.  **Yöntemi yeniden oluştur**'u seçin; *WHSScheduleWorkCreationWaveStepMethod* yönteminin sevkiyat dalga şablonlarınızda kullanabileceğiniz dalga işleme yöntemleri listesine eklendiğini görürsünüz.
1. *WHSScheduleWorkCreationWaveStepMethod* **Yöntem adı**'na sahip kaydı seçin ve **Görev yapılandırması**'nı seçin.
1. Izgaraya yeni satır eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve aşağıdaki ayarları kullanın:

    - **Ambar**: İş oluşturma işlemesini zamanlamak için kullanacağınız ambarı seçin.
    - **Maksimum toplu görev sayısı**: Maksimum toplu görev sayısını belirtin. Çoğu durumda bu değer 8-16 aralığında olmalıdır, ancak senaryolarınıza göre en iyi ayarı denemeniz önerilir.
    - **Dalga işleme toplu iş grubu**: Toplu iş kuyruğu işlemenizi iyileştirmek için özel bir dalga işleme toplu iş grubu seçin.

Şimdi, *İş oluşturmayı zamanla* dalga işleme yöntemini kullanmak için mevcut bir dalga şablonunu güncelleştirmeye hazırsınız (veya yeni bir tane oluşturabilirsiniz).

1.  **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.
1. Eylem Bölmesinde, **Düzenle**'yi seçin.
1. Liste bölmesinde, güncelleştirmek istediğiniz dalga şablonunu seçin (tanıtım verilerini kullanarak test ediyorsanız, *24 Sevkiyat varsayılan*'ı kullanabilirsiniz).
1. **Yöntemler** hızlı sekmesini genişletin ve **Kalan yöntemler** ızgarasında *İş oluşturmayı zamanla* **Adı**'na sahip satırı seçin.
1. Seçili satırı ilgili sütuna taşımak için **Seçili yöntemler** sütununu işaret eden oku seçin. (Bir seferde yalnızca `WHSScheduleWorkCreationWaveStepMethod` veya `createWork` yöntemini kullanan seçili bir yönteminiz olabilir. Bu nedenle, `createWork` **Yöntem adı**'na sahip mevcut satır otomatik olarak **Kalan yöntemler** ızgarasına taşınır.)

## <a name="set-wave-task-processing-threshold-data"></a>Dalga görevi işleme eşik verilerini ayarla

Dalga işlemi ilk kez görev tabanlı işleme kullanarak çalıştırıldığında sistem, varsayılan dalga görevi işleme eşik değeri oluşturur. Bu veri, dalga işleminin zaman uyumsuz olarak çalıştırıldığı ve görev tabanlı olduğu durumları kontrol etmek için kullanılır. Bu da işi paralel olarak işlemesini ve oluşturmasını sağlar.

Varsayılan veriler, ilk başta minimum yük satırı sayısı olarak 15 eşik değerini kullanacaktır (`MINIMUMWAVELOADLINES`). Bu, sistemin 15 yük satırından fazlasını içeren bir dalgayı işlediğinde zaman uyumsuz görev işlemeyi kullanacağı anlamına gelir. Test ortamlarınızda bu verileri `WHSWaveTaskProcessingThresholdParameters` tablosuna el ile ekleyebilir/güncelleştirebilirsiniz. Üretim ortamında bu ayarı değiştirmeniz gerekiyorsa, güncelleştirmeyi istemek için Microsoft desteğine başvurmanız gerekir.

## <a name="work-with-the-scheduled-work-creation"></a>Planlanan iş oluşturma ile çalışma

Planlanan iş oluşturma ile nasıl çalışılacağı hakkında ayrıntılı bilgi için, bkz. [Dalga oluşturma ve işleme](wave-processing.md). 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
