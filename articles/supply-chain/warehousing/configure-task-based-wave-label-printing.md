---
title: Dalga sırasında dalga etiketi yazdırmayı zamanlama
description: Bu makalede, görev tabanlı dalga etiketi yazdırma işlevselliğinin nasıl ayarlanacağı ve kullanılacağı açıklanmaktadır.
author: perlynne
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ac2bc4cce42bada43334b82301d716414cd6d654
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889471"
---
# <a name="schedule-wave-label-printing-during-wave"></a>Dalga sırasında dalga etiketi yazdırmayı zamanlama

[!include [banner](../../includes/banner.md)]

Verimliliği artırmaya yardımcı olmak ve sistemin dalga etiketleri oluşturmasını ve ayrı görevlerde çalışmasını sağlamak için dalga işleminizin bir parçası olarak *Görev tabanlı dalga etiketi yazdırma* özelliğini kullanın.

Dalga etiketi yazdırmayı yapılandırma işlemi karmaşıktır ve doğru yapılandırmaya ve ana verilere dayanır. Dalga etiketi kayıtlarının oluşturulmasında başarısızlık olması sık karşılaşılan bir durumdur ve başarısız olduğunda, tüm dalga işleme geri alınır. *Görev tabanlı dalga etiketi yazdırma* özelliği, bir dalga etiketi her yanlış yazdırıldığında iş ve iş satırlarını yeniden oluşturmak zorunda kalmamanıza yardımcı olur.

*Görev tabanlı dalga etiketi yazdırma* özelliğini kullandığınızda, sistem önce iş ve iş satırları oluşturur. Daha sonra dalga etiketleri oluşturur ve yazdırır. Son olarak, dalga etiketleri doğru oluşturulursa, malzeme çekme için işi ve dalgayı serbest bırakır.

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>Özellik yönetiminde Görev tabanlı dalga etiketi yazdırma özelliğini açma

Bu makalede açıklanan özellikleri kullanmak için, bunların sisteminiz için etkinleştirilmiş olması gerekir. Özellikleri aşağıdaki sırada açmak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanın:

1. *Dalga etiketi yazdırma*: Bu özellik, dalga etiketi yazdırma için dalga işlemi yöntemini etkinleştirmek için gereklidir.
1. *Kuruluş genelinde iş durdurma*: Bu özellik, planlanan iş oluşturma işleminin hem el ile hem de otomatik yapılandırılması için gereklidir. (Supply Chain Management sürüm 10.0.21 itibariyle bu özellik zorunludur; bu nedenle varsayılan olarak açıktır ve yeniden kapatılamaz.)
1. *Görev tabanlı dalga etiketi yazdırma*: Bu özellik, dalga etiketi yazdırmayı ayrı bir hareket kapsamına bölmek için gereklidir.

## <a name="manually-enable-the-new-wave-step-method"></a>Yeni dalga adımı yöntemini el ile etkinleştirme

Öncelikler yeni dalga adımı yöntemini oluşturmanız ve bu yöntemi paralel zaman uyumsuz görev işleme için etkinleştirmeniz gerekir.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga işleme yöntemleri**'ne gidin.
1. Eylem bölmesinde, **Yöntemi yeniden oluştur**'u seçin. *waveLabelPrinting*'in sevkiyat dalga şablonlarınızda kullanabileceğiniz dalga işlemi yöntemleri listesine eklendiğine dikkat edin.
1. **Yöntem adı** alanının *waveLabelPrinting* olarak ayarlandığı kaydı seçin ve sonra Eylem Bölmesi'nde **Görev yapılandırması**'nı seçin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin. Ardından yeni satırda aşağıdaki alanları ayarlayın:

    - **Ambar**: İş oluşturma işlemesini zamanlamak için kullanacağınız ambarı seçin. (Demo verilerini test amacıyla kullanıyorsanız ambar *24'* ü seçebilirsiniz.)
    - **Maksimum toplu görev sayısı**: Maksimum toplu görev sayısını belirtin. Çoğu durumda, değer *8* ila *16* arasında olmalıdır. Ancak, senaryolarınız için en uygun ayarı bulmak üzere denemeler yapmanızı öneririz.
    - **Dalga işleme toplu iş grubu**: Toplu iş kuyruğu işlemesini iyileştirmek için özel bir dalga işleme toplu iş grubu seçin.

Artık mevcut bir dalga şablonsunu, *Dalga etiketi yazdırma* dalgası işleme yöntemini kullanarak güncelleştirebilirsiniz. Alternatif olarak, onu kullanan yeni bir dalga şablonu oluşturabilirsiniz.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. Liste bölmesinde, güncelleştirilecek dalga şablonunu seçin. (Demo verilerini test amacıyla kullanıyorsanız *24 Sevkiyat varsayılanı*'nı seçebilirsiniz.)
1. **Yöntemler** hızlı sekmesinde bulunan **Kalan yöntemler** sütununda, **Ad** alanının *waveLabelPrinting* olarak ayarlandığı satırı seçin.
1. Seçili satırı **Seçili yöntemler** sütununa taşımak için **ekle**'yi (sağ ok düğmesi) seçin.
1. **Dalga adımı kodu** alanına, dalga şablonunu dalga etiketi şablonuyla bağlamak için kullanılacak bir dalga adımı kodu girin.

## <a name="set-wave-task-processing-threshold-data"></a>Dalga görevi işleme eşik verilerini ayarla

Dalga işlemi ilk kez görev tabanlı işleme kullanarak çalıştırıldığında sistem, varsayılan dalga görevi işleme eşik değeri oluşturur. Bu veri, dalga işleminin zaman uyumsuz olarak çalıştırıldığı ve görev tabanlı olduğu durumları kontrol etmek için kullanılır. Bu da dalga etiketlerini paralel olarak işlemesini ve oluşturmasını sağlar.

Varsayılan veriler, ilk başta minimum iş kodu sayısı olarak (`MinimumWorkThresholdForLabelPrinting`) *1* eşik değerini kullanır. Bu nedenle, sistem birden fazla iş koduna sahip bir dalgayı işlediğinde, dalga etiketlerinin görev tabanlı işlenmesini ayrı bir işlemde kullanır. Test ortamlarınızda bu verileri `WHSWaveTaskProcessingThresholdParameters` tablosuna el ile ekleyebilir veya güncelleştirebilirsiniz. Üretim ortamında bu ayarı değiştirmek için, güncelleştirme istemek üzere Microsoft Desteğine başvurmanız gerekir.

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>Görev tabanlı dalga etiketi yazdırma kullanıldığında dalga işleme mantığındaki değişiklikler

Dalga etiketi işleme dalga görevi işleme eşiğini aşarsa, görev tabanlı işleme başlatılır. Dalga şablonuna uyan bir sonraki dalga işlemede, dalga etiketi yazdırma iş oluşturulduktan hemen sonra bağımsız bir *ttsbegin*/*ttscommit* işleminde çalışır. Dalga şablonunda iş bırakma (engellemeyi kaldırma) otomatik olarak çalışacak şekilde yapılandırılmışsa, yalnızca dalga etiketi yazdırma işlemi başarıyla tamamlandıktan sonra gerçekleşir.

Dalga etiketi oluşturma başarısız olursa (örneğin, iş miktarının dalga etiketi miktarına dönüştürülmesi başarısız olursa ve bir hata oluşursa), yalnızca ilgili işlem başarısız olur. Daha önce oluşturulan çalışma dondurulmuş olarak kalır. Hataları düzeltmek ve dalga etiketlerini yazdırmak için şu adımları izleyin.

1. **Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.
1. Izgaradan ilgili dalgayı seçin.
1. Eylem Bölmesinde, **Dalga** sekmesindeki **Yazdır** gurubunda **Dalga etiketleri**'ni seçin.
1. Etiketleri yazdırmak üzere göndermek için ekrandaki yönergeleri izleyin.
1. Eylem Bölmesi'nde, **Dalga** sekmesinin **Dalga** grubunda, seçili dalga için işi el ile serbest bırakmak üzere **Serbest bırak**'ı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Dalga etiketi yazdırma](configure-wave-label-printing.md)
- [Dalga sırasında iş oluşturmayı zamanlama](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
