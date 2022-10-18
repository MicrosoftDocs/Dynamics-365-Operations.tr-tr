---
title: Varlık bakım senaryosu
description: Bu makalede, bir makine varlığının kullanımını izleyen sayaç kayıtları oluşturmak için sensör verilerini kullanmanıza olanak tanıyan varlık bakım senaryosu açıklanmaktadır.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: fcd16d09b4293046c457b602857ef8950e8259c6
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644070"
---
# <a name="the-asset-maintenance-scenario"></a>Varlık bakım senaryosu

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

*Varlık bakım* senaryosu, sayaç kayıtları oluşturmak için sensör verilerini kullanmanıza olanak tanır. Sayaç kayıtları bir makine varlığının kullanımını izler ve makine varlıklarının bakım zamanlamasını oluşturmak için girdi olarak kullanılır.

## <a name="video-instructions"></a>Video yönergeleri

Aşağıdaki videoda varlık bakım senaryosunun standart [demo verileri](../../fin-ops-core/fin-ops/get-started/demo-data.md) kullanılarak nasıl ayarlanacağı ve kullanılacağı gösterilmektedir. Aynı yönergeler, bu makalenin geri kalan bölümlerinde metin şeklinde sunulmuştur.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58aRW]

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>Varlık bakım senaryosu için demo verileri hazırlama

*Varlık bakım* senaryosunu test etmek için bir demo sistemi kullanmak istiyorsanız demo verilerinin yüklü olduğu bir sistem kullanın, *USMF* tüzel kişiliğini (şirket) seçin ve ek [demo verilerini](../../fin-ops-core/fin-ops/get-started/demo-data.md) bu bölümde açıklandığı gibi hazırlayın. Kendi sensörlerinizi ve verilerinizi kullanıyorsanız bu bölümü atlayabilirsiniz.

Bu bölümde, örnek olarak demo verilerinde *AK-101, Hava bıçağı* varlığını ayarlayacaksınız. Daha sonra, hava bıçağının çalıştığı saat sayısını ölçen sensör sinyallerine dayanarak yaklaşan bakım çalışmalarının nasıl tahmin edilebileceğini göreceksiniz. Ayrıca, hava bıçağının her 10.000 saatte bir bakımı gereken bir bakım planı da oluşturacaksınız.

### <a name="set-up-a-sensor-simulator"></a>Sensör simülatörü ayarlama

Fiziksel bir sensör kullanmadan bu senaryoyu denemek istiyorsanız gerekli sinyalleri üretmek için bir simülatör ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Test için simülasyonu yapılmış bir sensör ayarlama](sdi-set-up-simulated-sensor.md).

### <a name="create-an-asset-counter-to-track-production-hours"></a>Üretim saatlerini izlemek için varlık sayacı oluşturma

Üretim saatlerini izlemek üzere bir varlık sayacı oluşturmak için aşağıdaki adımları izleyin.

1. **Kıymet yönetimi \> Kurulum \> Kıymet türleri \> Sayaçlar**'a gidin.
1. Eylem bölmesinde **Yeni**'yi seçerek bir sayaç oluşturun.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Sayaç:** *ProductionHr*
    - **Ad:** *Üretim saatleri*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Birim:** *sa*
    - **Güncelleştirme:** *El ile*
    - **Toplama toplamı:** *Toplam*

1. **Varlık türleri** hızlı sekmesinde **Satır ekle**'yi seçin.
1. Yeni satırda, **Varlık türü** alanını *Hava bıçağı* olarak ayarlayın.

### <a name="create-a-maintenance-plan-for-the-asset"></a>Varlık için bakım planı oluşturma

Varlık için bir bakım planı oluşturmak üzere aşağıdaki adımları izleyin.

1. **Varlık yönetimi \> Kurulum \> Önleyici bakım \> Bakım planı**'na gidin.
1. Eylem Bölmesi'nde, bakım planı oluşturmak için **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Bakım planı:** *AirKnife*
    - **Ad:** *Hava bıçakları için plan*

1. **Ayrıntılar** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Plan tarihi:** Bugünün tarihini seçin.
    - **Etkin:** *Evet*

1. **Satırlar** hızlı sekmesinde, kılavuza satır eklemek için **Varlık sayacı satırı ekle**'yi seçin. Ardından bunun için aşağıdaki değerleri ayarlayın:

    - **İş emri açıklaması:** *Hava bıçağı bakımı*
    - **Bakım işi türü:** *Önleyici*
    - **Aralık türü:** *Son iş emrinden tekrarlanır*
    - **Dönem sıklığı:** *10000*
    - **Sayaç:** *ProductionHr*

## <a name="set-up-the-asset-maintenance-scenario"></a>Varlık bakım senaryosunu ayarlama

Supply Chain Management'ta *varlık bakım* senaryosunu ayarlamak için aşağıdaki adımları izleyin.

1. **Varlık yönetimi \> Kurulum \> Sensör Veri Yönetim Bilgileri \> Senaryoları**'a gidin.
1. **Varlık bakım** senaryosu kutusunda, bu senaryonun kurulum sihirbazını açmak için **Yapılandır**'ı seçin.
1. **Sensörler** sayfasında, ızgaraya sensör eklemek için **Yeni**'yi seçin. Ardından bunun için aşağıdaki alanları ayarlayın:

    - **Sensör Kimliği**: Kullandığınız sensörün kimliğini girin. (Raspberry PI Azure IoT Online Simulator'ı kullanıyorsanız ve bunu [Test için sanal sensör ayarlama](sdi-set-up-simulated-sensor.md) bölümünde açıklandığı gibi ayarladıysanız *AssetMaintenance* girin.)
    - **Sensör açıklaması**: Sensörle ilgili açıklama girin.

1. Şimdi eklemek istediğiniz diğer tüm sütunlar için önceki adımı yineleyin. İstediğiniz zaman geri dönüp daha fazla sensör ekleyebilirsiniz.
1. **Sonraki**'yi seçin.
1. **İşletme kaydı eşleme** sayfasında, **Sensörler** bölümünde, yeni eklediğiniz sensörlerden birinin kaydını seçin.
1. **İşletme kaydı eşlemesi** bölümünde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda, **İş kaydı türü** alanı otomatik olarak *Assets(EntAssetObjectTable)* olarak ayarlanmalıdır. **İşletme kaydı** alanını, izlemek için seçilen sensörü kullandığınız kaynağa ayarlayın. (Bu makalenin önceki bölümlerinde oluşturduğunuz demo verilerini kullanıyorsanız bunu *Satır 1 için AK-101, AK-101 Hava Bıçağı* olarak ayarlayın.)
1. Önceki adımda eklediğiniz satır için bir iş kaydı türü seçtikten hemen sonra, kılavuza otomatik olarak ikinci bir satır eklenir. Bu satırda, **İşletme kaydı türü** alanı *Counters(EntAssetCounterType)* olarak ayarlanmalıdır. **İşletme kaydı** alanını, seçilen sensörden gelen sinyallere göre güncelleştirilen varlık sayacına ayarlayın. (Bu makalenin önceki bölümlerinde oluşturduğunuz demo verilerini kullanıyorsanız bunu *ProductionHr, Üretim saatleri* olarak ayarlayın.)
1. **Sonraki**'yi seçin.
1. **Sensörleri etkinleştirin** sayfasında, ızgarada, eklediğiniz sensörü seçin ve ardından **Etkinleştir**'i seçin. Izgaradaki her etkinleştirilen sensör için **Etkin** sütununda bir onay işareti görünür.
1. **Bitir**'i seçin.

## <a name="work-with-the-asset-maintenance-scenario"></a>Varlık bakım senaryosuyla çalışma

### <a name="view-counter-values"></a>Sayaç değerlerini görüntüleme

Veriler hazırlandıktan ve *varlık bakım* senaryosu yapılandırılıp etkinleştirildikten sonra, sensör verilerine dayalı olarak bir varlık sayacı kayıtlarının nasıl eklendiğini görebilirsiniz.

1. **Varlık yönetimi \> Varlıklar \> Etkin varlıklar**'a gidin.
1. İncelemek istediğiniz varlığı bulup seçin. (Bu makalenin önceki bölümlerinde oluşturduğunuz demo verilerini kullanıyorsanız *AK-101*'i seçin.)
1. Eylem Bölmesinde, **Varlık** sekmesinde, **Önleyici** grubunda, *AK-101* varlığının sayaç kayıtları sayfasını açmak için **Sayaçlar**'ı seçin.

### <a name="generate-maintenance-work-orders"></a>Bakım iş emirleri oluşturma

*Varlık bakım* senaryosunu etkinleştirdikten ve bakım planını ayarladıktan sonra, bakım iş emirleri oluşturmak için bakım zamanlamasını çalıştırabilirsiniz. Önleyici bakımla nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Önleyici bakıma genel bakış](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md).
