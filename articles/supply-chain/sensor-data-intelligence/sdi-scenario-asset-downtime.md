---
title: Varlık kapalı kalma süresi senaryosu
description: Bu makalede, varlıklarınızın kullanılabilirliğini izlemek için sensör verilerini kullanmanıza olanak tanıyan varlık kapalı kalma süresi senaryosu açıklanmaktadır.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetObjectProductionStop
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: b82d757d1e69203012949bc397220fa42ada4ac2
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689442"
---
# <a name="the-asset-downtime-scenario"></a>Varlık kapalı kalma süresi senaryosu

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Varlık kapalı kalma süresi senaryosu, son sinyalin alınmasından bu yana belirli bir zaman eşiği içinde bir makineden sinyal alınmazsa bir bakım kesinti süresi kaydı oluşturur. Senaryo, makinenize, makine çalışırken Azure IoT Hub'ınıza düzenli aralıklarla sinyal gönderen ancak makine çalışmadığında sinyal göndermeyen bir sensör takmanızı gerektirir.

## <a name="set-up-the-asset-downtime-scenario"></a>Varlık kapalı kalma süresi senaryosunu ayarlama

Supply Chain Management'ta *varlık kapalı kalma süresi* senaryosunu ayarlamak için aşağıdaki adımları izleyin.

1. Senaryolar sayfasını açmak için **Varlık Yönetimi \> Kurulum \> Sensör Veri Yönetim Bilgileri**'ne gidin ve \> **Senaryolar**'ı seçin.
2. **Varlık kapalı kalma süresi** senaryosu kutusunda, bu senaryonun kurulum sihirbazını açmak için **Yapılandır**'ı seçin.
3. **Sensörler** sayfasında, ızgaraya sensör eklemek için **Yeni**'yi seçin. Ardından bunun için aşağıdaki alanları ayarlayın:

    - **Sensör Kimliği**: Kullandığınız sensörün kimliğini girin. (Raspberry PI Azure IoT Online Simulator kullanıyorsanız ve bunu [Test için sanal algılayıcı ayarlama](sdi-set-up-simulated-sensor.md) bölümünde açıklandığı gibi ayarladıysanız *AssetDownTime* girin.)
    - **Sensör açıklaması**: Sensörle ilgili açıklama girin.

4. Şimdi eklemek istediğiniz diğer tüm sütunlar için önceki adımı yineleyin. İstediğiniz zaman geri dönüp daha fazla sensör ekleyebilirsiniz.
5. **Sonraki**'yi seçin.
6. **İşletme kaydı eşleme** sayfasında, **Sensörler** bölümünde, yeni eklediğiniz sensörlerden birinin kaydını seçin.
7. **İşletme kaydı eşlemesi** bölümünde, kılavuza satır eklemek için **Yeni**'yi seçin.
8. Yeni satırda, **İşletme kaydı** alanını, izlemek için seçilen sensörü kullandığınız kaynağa ayarlayın. (Demo veriler kullanıyorsanız *Satır 1 için AK-101, Hava Bıçağı*'nı seçin.)
9. **Sonraki**'yi seçin.
10. **Varlık kapalı kalma süresi eşiği** sayfasında, sistemin bir varlık kapalı kalma süresi bildirimi göndermek için son sinyalden ne kadar süre sonra beklemesi gerektiğini tanımlayın. Eşiği tanımlamanın iki yolu vardır:

    - **Varsayılan eşik (dakika)**: Varsayılan eşiği tanımlamak için bu alanı ayarlayın. Bu değer, **Bildirim eşiği (dakika)** alanının iki dakika veya daha kısa bir süreye ayarlandığı tüm kaynaklar için geçerlidir. Minimum değer *2* (dakika) şeklindedir.
    - **Makinenin yanıt vermediğini belirleme eşiği (dakika)**: Varsayılan eşiği kullanmak istemediğiniz ızgaradaki her kaynak için bu alana bir geçersiz kılma değeri girin. İki dakika veya daha kısa bir eşik kullanacak şekilde ayarlanan kaynaklar, bunun yerine **Varsayılan eşik (dakika)** ayarını kullanır.
11. **Sonraki**'yi seçin.
12. **Sensörleri etkinleştirin** sayfasında, ızgarada, ayarladığınız sensörü seçin ve ardından **Etkinleştir**'i seçin. Izgaradaki her etkinleştirilen sensör için **Etkin** sütununda bir onay işareti görünür.
13. **Bitir**'i seçin.

## <a name="work-with-the-asset-downtime-scenario"></a>Varlık kapalı kalma süresi senaryosuyla çalışma

Senaryo yapılandırmasında tanımlanan eşik dahilinde bir varlıktan sensör sinyali alınmazsa sistem bu varlık için bir bakım kapalı kalma süresi kaydı oluşturur. Yöneticiler, kesinti süresi kayıtlarını periyodik olarak gözden geçirmeli (örneğin, her çalışma vardiyasında bir kez) ve her kesinti süresi kaydı için uygun neden kodlarını ve bitiş saatlerini uygulamalıdır. Bir varlığın bakım kapalı kalma süresi kayıtlarını görüntülemek için şu adımları izleyin:

1. **Varlık yönetimi > Varlıklar > Tüm varlıklar**'a gidin.
2. İncelemek istediğiniz varlığı bulup seçin. (Demo verilerini kullanıyorsanız *AK-101*'i seçin.)
3. Eylem Bölmesinde, **Varlık** sekmesini açın ve **İş emri** grubundan, seçilen varlığın bakım kesinti süresi kayıtları sayfasını açmak için **Bakım kesinti süresi**'ni seçin.
