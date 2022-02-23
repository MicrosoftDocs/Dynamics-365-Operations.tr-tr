---
title: İş emirlerine giriş
description: Bu konuda, Varlık Yönetimi'ndeki iş emirleribe genel bir bakış sağlanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderLineNote, EntAssetWorkOrderTable, EntAssetWorkOrderActive, EntAssetWorkOrderHoursInfoPart, EntAssetWorkOrderLineListPage, EntAssetWorkOrderAddObjectBOMItem, EntAssetWorkOrderTablePoolAdd, EntAssetWorkOrderPurchReqListPagePreviewPane, EntAssetWorkOrderPoolReferenceAdd, EntAssetWorkOrderWorkspace, EntAssetWorkOrderTableAdjust, EntAssetWorkOrderGantt, EntAssetWorkOrderNotes, EntAssetWorkOrderActivePart, EntAssetWorkOrderTableInfoPart, EntAssetWorkOrderLineListPagePreviewPane, EntAssetWorkOrderTool, EntAssetMobileWorkOrderLineDetails, EntAssetMobileWorkOrderLineList, EntAssetMobileWorkOrderDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 378fc6d55deada95e94f91ed3f73f2518efbeb1f
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021892"
---
# <a name="introduction-to-work-orders"></a>İş emirlerine giriş

[!include [banner](../../includes/banner.md)]



İş emirleri bakım işlerini yönetmek, bu işlere ilişkin gerekli bilgileri sağlamak ve tüketimi kaydetmek için kullanılır. Her iş emri bir veya daha fazla iş emri işi içerebilir ve her iş emrine bir veya daha fazla varlık bağlanabilir. Her iş emri işi, varlık üzerinde planlanan bir bakım işini tanımlar.

İş emirlerini aşağıdaki biçimlerde oluşturabilirsiniz:

- "Otomatik oluştur" ayarının etkin olduğu takvim tabanlı bakım planları için [Bakım planlarını zamanla](../preventive-and-reactive-maintenance/schedule-maintenance-plans.md) formunu kullanarak otomatik olarak.

- "Otomatik oluştur" ayarının etkin olduğu bakım sıraları için [Bakım sıralarını zamanla](../preventive-and-reactive-maintenance/maintenance-rounds.md) formunu kullanarak otomatik olarak.

- Önleyici bakım işleri veya bakım talepleri için [Bakım zamanlamasından](../preventive-and-reactive-maintenance/maintenance-schedule.md).

- El ile

- **Tüm bakım istekleri** veya **Etkin bakım istekleri** veya **İşlem yapılacak yerleşim bakım isteklerim** sayfasından.

>[!NOTE]
>Aynı varlıkla ilgili iş emri işleri aynı proje koduyla ilgilidir.

## <a name="all-work-orders"></a>Tüm iş emirleri

**Varlık yönetimi** > **Ortak** > **İş emirleri** > **Tüm iş emirleri**'ni seçerek **Tüm iş emirleri** liste sayfasını açın. Bu sayfa tüm iş emirlerini ve her biriyle ilgili bazı bilgileri gösterir.

Aşağıdaki örnekte **Tüm iş emirleri** liste sayfasının bir örneği gösterilmektedir.

![Şekil 1](media/01-work-orders.png)

Yalnızca etkin iş emirlerinin listesini görmek için **Varlık yönetimi** > **Genel** > **İş emirleri** > **Etkin İş emirleri**'ni seçin. 

Çalışan olarak ilgili olduğunuz işlem yapılacak yerleşimlere yüklenen iş emri işlerini içeren listeyi görmek için **Varlık yönetimi** > **Genel** > **İş emirleri** > **İşlem yapılacak yerleşim iş emri bakım işlerim**'i seçin. (Çalışanlar ve işlem yapılacak yerleşimler arasındaki ilişki **Çalışanlar** sayfasında ayarlanır. Daha fazla bilgi için [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md) bölümüne bakın.)

Aşağıda, **Tüm iş emirleri** sayfasını kullanabileceğiniz bazı yöntemler verilmiştir:

- Izgara görünümünde seçili kaydın ayrıntılar görünümü görüntülemek için **İş emri** sütunundan bir bağlantı seçin. Böylece, kaydı düzenlemek üzere açmak için **Düzenle**'yi seçebilirsiniz.

- Ayrıntılar görünümünde, iş emriyle ilgili ayrıntılı bilgileri görürsünüz.  

- Ayrıntılar görünümünde, iş emri iş ayrıntılarını görmek için **Satırlar** bağlantısını veya iş emri ayrıntıları görünümünü görmek için **Başlık** sekmesini seçin.  

- Seçili iş emriyle ilgili ek bilgileri görmek için sayfanın sağ tarafındaki **İlgili bilgi** bölmesini genişletin.

Aşağıdaki örnekte **Tüm iş emirleri** ayrıntıları görünümünün bir örneği gösterilmektedir.

![Şekil 2](media/02-work-orders.png)


Eylem Bölmesi'ndeki düğmeler sekmeler halinde düzenlenmiştir. Aşağıdaki tabloda Varlık Yönetimiyle ilgili düğmeler kısaca açıklanmaktadır.



| Düğme adı                     | Tanım                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Düzenle                            | Seçilen iş emrini düzenleyin.                                                                                                                                                                                                                                           |
| Yeni                             | Yeni iş emri oluşturun.                                                                                                                                                                                                                                                  |
| Delete                          | Seçili iş emrini silin.                                                                                                                                                                                                                                         |
| İş emri havuzu                 | Seçili iş emrini bir iş emri havuzuna ekleyin veya iş emri havuzundan kaldırın.                                                                                                                                                                                           |
| Düzelt                          | Seçili iş emirlerinde beklenen başlangıç ve bitiş, hizmet düzeyi, sorumlu bakım görevlisi veya sorumlu bakım görevlisi grubu hakkındaki bilgileri ayarlayın.                                                                                                                                     |
| İlgili iş emri              | Seçili iş emri işiyle ilgili yeni bir iş emri oluşturun. Birincil ve ikincil iş emirlerini kaydetmek istiyorsanız bu yararlıdır.                                                                                                                              |
| İş emrini kopyala                 | Varolan bir iş emrine dayalı olarak yeni bir iş emri oluşturun.                                                                                                                                                                                                               |
| Olay geçmişi                   | İş emri için kayıt geçmişini görüntüleyin.                                                                                                                                                                                                                |
| İş emri bakım işi notları                           | Bir iş emrinde açıklama oluşturun veya notlar veya açıklamalar ekleyin. Önce, nota kullanıcı adınızı ve zaman damgası eklemek için **Zaman damgası ekle**'yi seçin. Notlar **İş emri** sayfasının **Satır ayrıntıları** hızlı sekmesinin **Açıklama** sekmesinde gösterilir.         |
| Araçlar                           | Bir iş emrinde gerekli araçların listesini oluşturun. Araçlar **Kuruluş yönetimi** > **Kaynaklar** > **Kaynaklar**'da ayarlanır.                                                                                                      |
| Bakım denetim listesi           | İş emrine bağlı varlıkla ilgili denetim listesini görüntüleyin.                                                                                                                                                                                                              |
| Kıymet hatası                     | Bir varlıkla ilgili arıza bilgilerini görüntüleyin veya kaydedin. Bu bilgiler arıza yönetimi için kullanılır.                                                                                                                                                                                      |
| Bakım kesinti süresi            | Bir iş emri için bakım kesinti süresini belirtin.                                                                                                                                                                                                                               |
| Koşul değerlendirme            | İş emri üzerinde koşul değerlendirmesi ölçümlerini kaydedin.                                                                                                                                                                                                             |
| Varlık sayaçları                 | Varlıkta sayaç kaıtları oluşturun veya bu kayıtları görüntüleyin.                                                                                                                                                                                                                     |
| Tahmin                        | Bir iş emrinde tahminleri görüntüleyin veya oluşturun.                                                                                                                                                                                                                               |
| Günlükler                        | İş emri günlüklerini görüntüleyin veya oluşturun. Tahminden günlük satırları kopyalanabilir.                                                                                                                                                                                         |
| Proje hareketleri            | Varlık için oluşturulan iş emirleriyle ilgili deftere nakledilen tüm hareketleri görüntüleyin.                                                                                                                                                                                             |
| İş emri durumunu güncelleştirme           | İş emri yaşam döngüsü durumunu güncelleştirin.                                                                                                                                                                                                                                                |
| Yaşam döngüsü durumu günlüğü                      | Seçili iş emrinin yaşam döngüsü durumlarını gösteren günlüğü görüntüleyin.                                                                                                                                                                                                                   |
| Varlık belgeleri                | Bir iş emriyle ilgili varlıklara iliştirilmiş belgelerin listesini görüntüleyin. Bu belgeler **Varlık yönetimi** > **Kurulum** > **Varlık belgeleri** altından ayarlanır.                                                                                                 |
| Plan                        | Seçili iş emirlerini zamanlayın.                                                                                                                                                                                                                                      |
| Gönder            | Bir çalışan için seçili iş emrini planlayın.                                                                                                                                                                                                                        |
| Planı sil                 | Seçili iş emri için zamanlamayı silin.                                                                                                                                                                                                                          |
| Planlanan iş emri bakım işleri             | **Planlanmış iş emri bakım işleri** liste sayfasını açın.                                                                                                                                                                                                                             |
| İş emri satınalma talebi | **İş emri satınalma talebi** liste sayfasını açın.                                                                                                                                                                                                                 |
| İş emri satınalma işlemi             | **İş emri satınalma** liste sayfasını açın.                                                                                                                                                                                                                             |
| Maliyet kontrolü                    | İş emrindeki bütçe maliyetlerini ve fiili maliyetleri karşılaştırın.                                                                                                                                                                                                                |
| Saat denetimi                    | İş emrindeki tahmini saatleri ve fiili saatleri karşılaştırın.                                                                                                                                                                                                                |
| İş emri raporu               | İş emri raporunu yazdırın.                                                                                                                                                                                                                                                |
| İş emri tüketimi          | Tüketim raporunu yazdırın.                                                                                                                                                                                                                                               |


Eylem Bölmesinin **İş emri** sekmesindeki **Proje** grubundaki düğmeler **Proje yönetimi ve muhasebe** modülünde tahminler, günlükler ve faturalama gibi işlevlerle ilişkilidir.

>[!NOTE]
>Bir iş emrinde oluşturulan tahminleri, Master planlama çalıştırılırken dahil etmek için **Varlık yönetimi parametreleri** sayfasında seçilen tahmin modelini kullanın.

