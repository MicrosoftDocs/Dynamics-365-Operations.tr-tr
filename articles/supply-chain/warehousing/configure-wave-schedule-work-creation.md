---
title: Dalga sırasında iş oluşturmayı zamanlama
description: Bu konu, İş oluşturmayı zamanlama dalga işleme yönteminin nasıl ayarlanacağını ve kullanılacağını açıklamaktadır.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501234"
---
# <a name="schedule-work-creation-during-wave"></a>Dalga sırasında iş oluşturmayı zamanlama

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Sistemin paralel işlemeyi kullanarak iş oluşturmasıyla dalga işleme aktarım hızını artırmak için dalga işlemenin parçası olarak *İş oluşturmayı zamanla* özelliğini kullanın.

İşlev etkinleştirildiğinde, planlanan çalışma otomatik olarak oluşturulur ve sistem daha sonra bunu asılı işi oluşturmak için kullanılır. Dalga yükü satırlarının sayısı önceden belirlenmiş bir eşiğe ulaşırsa sistem paralel, zaman uyumsuz işlem uygulayarak asıl işi daha hızlı oluşturur.

## <a name="enable-the-schedule-work-creation-feature"></a>İş oluşturmayı zamanla özelliğini etkinleştirme

### <a name="enable-the-feature-in-feature-management"></a>Özelliği özellik yönetiminde etkinleştirme

*İş oluşturmayı zamanla* özelliğini kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *İş oluşturmayı zamanla*

> [!NOTE]
> *İşi oluşturmayı zamanla* özelliğini etkinleştirebilmeniz için *Kuruluş çapında işi engelleme* özelliğinin etkin olması gerekir.

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

1. Seçili satırı ilgili sütuna taşımak için **Seçili yöntemler** sütununu işaret eden oku seçin. (Bir seferde yalnızca *WHSScheduleWorkCreationWaveStepMethod* veya *createWork* yöntemini kullanan seçili bir yönteminiz olabilir. Bu nedenle, *createWork* **Yöntem adı**'na sahip mevcut satır otomatik olarak **Kalan yöntemler** ızgarasına taşınır.)

## <a name="set-wave-task-processing-threshold-data"></a>Dalga görevi işleme eşik verilerini ayarla

Dalga işlemi ilk kez görev tabanlı işleme kullanarak çalıştırıldığında sistem, varsayılan dalga görevi işleme eşik değeri oluşturur. Bu veri, dalga işleminin zaman uyumsuz olarak çalıştırıldığı ve görev tabanlı olduğu durumları kontrol etmek için kullanılır. Bu da işi paralel olarak işlemesini ve oluşturmasını sağlar.

Varsayılan veriler, ilk başta minimum yük satırı sayısı olarak 15 eşik değerini kullanacaktır (MINIMUMWAVELOADLINES). Bu, sistemin 15 yük satırından fazlasını içeren bir dalgayı işlediğinde zaman uyumsuz görev işlemeyi kullanacağı anlamına gelir. Test ortamlarınızda **WHSWaveTaskProcessingThresholdParameters** tablosundaki bu veriyi el ile ekleyebilirsiniz/güncelleştirebilirsiniz ancak bu ayarı üretim ortamında değiştirmeniz gerekirse güncelleştirmeyi istemek için Microsoft Desteği ile iletişim kurmanız gerekir.

## <a name="work-with-the-feature"></a>Özellik ile çalışma

*İş oluşturmayı zamanla* işlevi etkinleştirildiğinde dalga işleme, planlı iş oluşturacaktır. Bu da daha sonra yeni iş oluşturma işlemi tarafından kullanılacaktır. İş oluşturma sırasında iş, *Kuruluş genelinde iş engelleme* özelliği kullanılarak engellenir.

Aşağıdaki akış çizelgesi, dalga işleme sırasında planlanan işin nasıl oluşturulduğunu gösterir.

![İş oluşturmayı planla](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Planlı iş

**Planlı iş ayrıntıları** sayfası (**Ambar yönetimi \> İş \> Planlı iş ayrıntıları**), dalga işleme sırasında oluşturulan planlı iş hakkında bilgiler gösterir. Aşağıdaki **İşleme durumu** değerleri mevcuttur:

- **Sıraya Alındı**: Planlanan iş, iş oluşturmak için kullanılmak üzere bekliyor.
- **Tamamlandı**: Planlanan iş, iş oluşturmak için kullanıldı.
- **Başarısız**: Dalga işleme başarısız oldu. Planlı işin, ilgili gerçek iş olup olmadığına bakılmaksızın **Başarısız** durumunda olabileceğini unutmayın. Asıl iş oluşturma işlemi başarısız olduğunda asıl iş, *İptal edildi* durumunda kalır.

### <a name="batch-job-for-the-work-creation-process"></a>İş oluşturma işlemi için toplu iş

Dalgaları işlemeye yönelik toplu işleri görüntülemek için **Tüm dalgalar** sayfasındaki Eylem Bölmesinde **Toplu işler**'i seçin.

Buradan, toplu iş kodlarının her biri için tüm toplu görev ayrıntılarını görüntüleyebilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]