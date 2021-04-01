---
title: Bakım kesinti süresi faaliyetleri
description: Bu konuda bakım kesinti süresinin, belirli bir dönem boyunca belirli varlıklarda bakım işleri gerçekleştirmek için gerekli kapasitenin genel görünümünü edinmek üzere nasıl kullanılacağı anlatılır.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenanceStopCopy, EntAssetMaintenanceStopObject, EntAssetObjectProductionStop, EntAssetProductionStopType, EntAssetMaintenanceStop
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6251422755cf39930d48221e9de82ef16b4d96a7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252930"
---
# <a name="maintenance-downtime-activities"></a>Bakım kesinti süresi faaliyetleri

[!include [banner](../../includes/banner.md)]

Bakım kesinti süresi, belirli bir dönem boyunca belirli varlıklarda bakım işleri gerçekleştirmek için gerekli kapasitenin genel görünümünü edinmek üzere kullanılır. Örneğin, üretim tesisi 02'de Üretim Salonu 29 A'da Üretim satırı 10 için bakım kesinti süresi kaydı oluşturabilirsiniz. Bakım kesinti süresi kaydı, bakım molasıyla ilgili varlıkların üretim için kullanılabilir olmadığı dönemi belirten başlangıç ve bitiş saatine sahiptir.

**Bakım kesinti süresi faaliyetleri** belirli bir dönem boyunca ilgili varlıklardaki bakım zamanlaması satırları ve iş emri bakım işlerinin özetidir. İş emri bakım işleriyle ilgili satırların tümü, bakım molası dönemi içinde olan beklenen başlangıç tarihine sahiptir. Yararlı bilgileri ayıklayabilir ve planlı bakım işleri için ayarlamalar yapabilirsiniz:

- Üretim ekipmanlarının (varlıklar) gerekli kapatma dönemlerinin özetini edinin.  
- Yetkinlikler (sorumlu bakım görevlisi grupları veya bakım görevlileri) tarafından gruplanan, örneğin planlı bakım işlerinin yapılması için gereken elektrikçiler, demirciler veya diğer bakım iş grupları üzerindeki kapasite yükü gibi planlı bakım özetini (saatler) edinin.  
- Varlıklarla ilgili bakım zamanlama satırları veya iş emri bakım işleri için, örneğin satırdaki beklenen başlangıç ve bitiş zamanlarını değiştirme ya da bakım görevlileri veya bakım görevlisi grupları için iş akışını en iyi duruma getirmek üzere diğer bakım görevlilerini seçme gibi ayarlamalar yapın.

Bakım kesinti süresi kaydında varlıklar seçildiğinde etkin iş emirleriyle ilgili tüm açık bakım zamanlaması satırları ve iş emri bakım işleri, bakım kesinti süresi kaydına dahil edilir.

## <a name="maintenance-downtime-activities"></a>Bakım kesinti süresi faaliyetleri

Tüm bakım kesinti süresi faaliyetlerinin listesini açmak ve faaliyetlerle ilgili bazı bilgileri görmek için **Varlık yönetimi** > **Genel** > **Bakım kesinti süresi faaliyetleri** > **Tüm bakım kesinti süresi faaliyetleri**'ne tıklayın. Ayrıntılar görünümünü açmak için **Bakım kesinti süresi faaliyetleri** sütunundaki bağlantıya tıklayın. Aşağıdaki çizimde bir **Bakım kesinti süresi faaliyetleri** listesi örneği gösterilmektedir.

![Şekil 1](media/19-preventive-maintenance.png)


## <a name="create-a-maintenance-downtime-activity"></a>Bakım kesinti süresi faaliyeti oluşturma

1. **Varlık yönetimi** > **Genel** > **Bakım kesinti süresi faaliyetleri** > **Tüm bakım kesinti süresi faaliyetleri** veya **Etkin bakım kesinti süresi faaliyetleri**.

2. **Yeni**'ye tıklayın.

3. **Bakım kesinti süresi faaliyetleri** alanına bir kimlik ve **Ad** alanına bir ad ekleyin.

4. **Başlangıç tarihi/saati** ve **Bitiş tarihi/saati** alanlarına bakım molası için dönem ekleyin.

5. Bakım kesinti süresi faaliyetine her defasında bir varlık eklemek için **Bakım kesinti süresi faaliyetleri varlıkları** hızlı sekmesinde **Satır ekle**'ye tıklayın.

6. Tüm varlıklar eklendiğinde **Kaydet**'e tıklayın. Aşağıdaki çizimde ilgili varlıklar ve bakım işleri bulunan bir bakım kesinti süresi faaliyeti örneği gösterilmektedir.

7. Seçilen varlıklarla ilgili iş emri bakım işleri ve açık bakım zamanlaması satırları **Oluşturulan iş emri bakım işleri** ve **Bakım zamanlaması satırları** hızlı sekmelerinde gösterilir. **Genel** hızlı sekmesi > **İş emirleri** grubu > **Bakım tahmini saatleri** alanında ve **Genel** hızlı sekmesi > **Bakım zamanlaması** grubu > **Bakım tahmini saatleri** alanında iş emri bakım işleri ve bakım zamanlaması satırları için tahmin edilen toplam saat sayısını görürsünüz.

Aşağıdaki çizimde bir **Bakım kesinti süresi faaliyetleri** ayrıntıları görünümü örneği gösterilmektedir.

![Şekil 2](media/20-preventive-maintenance.png)

>[!NOTE]
>Bakım kesinti süresi faaliyeti oluşturmanızın ardından yeni iş emirleri veya bakım zamanlaması satırları oluşturulursa seçilen varlıklarla ilgili iş emri bakım işleri ve bakım zamanlaması satırları otomatik olarak güncelleştirilir. Örneğin, bakım kesinti süresi faaliyetinin oluşturulmasından iki gün sonra varlıklarla ilgili bakım planları veya bakım sıraları zamanlarsanız yeni bakım zamanlaması satırları otomatik olarak bakım kesinti süresi faaliyetine eklenir.

8. **Tüm bakım kesinti süresi faaliyetleri** > **Bakım kesinti süresi faaliyetleri**'nde listede bir bakım kesinti süresi faaliyeti seçin ve **Kapasite yükünü hesapla** iletişim kutusunu açmak için **Kapasite yükü**'ne tıklayın. Örneğin tarihler, varlıklar, varlık türleri ve bakım işi türleri üzerindeki kapasite yükünün özetini edinmek için bu iletişim kutusunu kullanın. İletişim kutusunda gösterilen tarihlerin **Bakım kesinti süresi faaliyetleri**'nde seçilen başlangıç ve bitiş tarihleri olduğunu unutmayın. Bu hesaplama, bakım kesinti süresi faaliyetiyle ilgili varlıkları içerir.

9. **Kapasite yükünü hesapla** iletişim kutusunda gerekirse başlangıç ve bitiş tarihlerini düzenleyin ve hesaplamaya iş emirlerini ve bakım zamanlamalarını dahil etmek isteyip istemediğinizi seçin. İşlem yapılacak yerleşimlerle ilişkilendirmek istediğiniz kapasite yükü hesaplamasının ayrıntılarını göstermek için **Düzey** alanını kullanabilirsiniz. Örneğin, alana "1" sayısını girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa işlem yapılacak yerleşim için bakım kesinti süresi faaliyetinde seçilen tüm varlıklar üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. **Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm kapasite yükü satırlarını gösteren ayrıntılı bir sonuç görürsünüz.

10. Hesaplamayı başlatmak için **Tamam**'a tıklayın. Toplam saat sayısı, **Kapasite yükü** özetinde gösterilir. **Kapasite yükü** sekmesi > **Gruplama ölçütü** Eylem Bölmesi gruplarında tahmini saatlerin tahsisatına dair daha ayrıntılı özet edinmek için ilgili düğmelere tıklayın. Aşağıdaki çizimde bir **Kapasite yükü** hesaplamasının sonuçları gösterilmektedir.

![Şekil 3](media/21-preventive-maintenance.png)

11. Kapasite yükünün özetini edinmenizin ardından iş emri bakım işleri veya bakım zamanlaması satırlarında ayarlama yapmak isterseniz **Bakım kesinti süresi etkinlikleri** ayrıntıları özetine dönün ve **Oluşturulan iş emri bakım işleri** ve **Bakım zamanlaması satırları** hızlı sekmelerinde ayarlamak istediğiniz satırları seçin.

12. **Ayarla** düğmesine tıklayın ve seçilen iş emri bakım işleri veya bakım zamanlaması satırları için beklenen başlangıç/bitiş tarihleri, servis düzeyi veya sorumlu bakım görevlilerini güncelleştirin.

13. Gerekli ayarlamaları yaptığınızda **Tamam**'a tıklayın. 

>[!NOTE]
>Ayarlamaları yapmanızın ardından bakım kesinti süresi dönemine dahil edilmeyen iş emri bakım işleri ve bakım zamanlaması satırları, **Bakım kesinti süresi faaliyetleri**'nden otomatik olarak kaldırılır.

14. **Tüm bakım kesinti süresi faaliyetleri** > **Bakım kesinti süresi faaliyetleri**'nde listede bir bakım kesinti süresi faaliyeti seçin ve **Madde tahminini hesapla** iletişim kutusunu açmak için **Madde tahmini**'ne tıklayın. Maddeler (yedek parçalar ve diğer gerekli maddeler) için tahminleri hesaplamak için bu iletişim kutusunu kullanın ve özet edinmek için bunları örneğin tarih, varlık, varlık türü ve bakım işi türüne göre gruplayın. İletişim kutusunda gösterilen tarihlerin **Bakım kesinti süresi faaliyetleri**'nde seçilen başlangıç ve bitiş tarihleri olduğunu unutmayın. Bu hesaplama, bakım kesinti süresi faaliyetinde seçilen varlıklarla ilgili yedek parçaları ve maddeleri içerir.

15. **Madde tahminini hesapla** iletişim kutusunda gerekirse başlangıç ve bitiş tarihlerini düzenleyin ve hesaplamaya iş emirlerini ve bakım zamanlamalarını dahil etmek isteyip istemediğinizi seçin. İşlem yapılacak yerleşimlerle ilişkilendirmek istediğiniz kapasite yükü hesaplamasının ayrıntılarını göstermek için **Düzey** alanını kullanabilirsiniz. Örneğin, alana "1" sayısını girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa işlem yapılacak yerleşim için bakım kesinti süresi faaliyetinde seçilen tüm varlıklar üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. **Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm kapasite yükü satırlarını gösteren ayrıntılı bir sonuç görürsünüz.

16. Hesaplamayı başlatmak için **Tamam**'a tıklayın. Toplam madde tahmini sayısı, **Madde tahmini** özetinde gösterilir. **Madde tahmini** sekmesi > **Şunlara göre grupla...** Eylem Bölmesi gruplarında tahmini saatlerin tahsisatına dair daha ayrıntılı özet edinmek için ilgili düğmelere tıklayın. Aşağıdaki çizimde bir **Madde tahmini** hesaplamasının sonuçları gösterilmektedir.

![Şekil 4](media/22-preventive-maintenance.png)

- Varlıkları bir bakım kesinti süresi faaliyetinden diğerine kopyalayabilirsiniz. **Tüm bakım kesinti süresi faaliyetleri**'nde **Bakım kesinti süresi faaliyetlerini kopyala** düğmesini seçin ve **Bakım kesinti süresi faaliyetlerinden** ve **Bakım kesinti süresi faaliyetlerine** alanlarında seçimlerinizi yapıp **Tamam**'a tıklayın.
- **Tüm bakım kesinti faaliyetleri**'nde ilgili listeleri açmak ve seçilen bakım kesinti süresi faaliyetiyle ilgili satırları görüntülemek için **Bakım zamanlaması satırları** düğmesine veya **Etkin iş emirleri** düğmesine tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]