---
title: İş emirlerine giriş
description: Bu konuda, Varlık Yönetimi'ndeki iş emirleribe genel bir bakış sağlanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9483c50a15fca566b1f5e089297795bbbe09c042
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875953"
---
# <a name="introduction-to-work-orders"></a>İş emirlerine giriş

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

İş emirleri, bakım işlerini yönetmek, bu işlere ilişkin gerekli bilgileri sağlamak ve tüketimi kaydetmek için kullanılır. Bir iş emri bir veya daha fazla iş emri işi içerebilir ve bir veya daha fazla varlık iş emrine bağlanabilir. Her iş emri satırı, varlık üzerinde planlanan bir bakım işini tanımlar.

İş emirleri el ile veya otomatik olarak oluşturulabilir.

- "Otomatik oluştur" olarak ayarlanmış takvim tabanlı bakım planları için otomatik olarak **Bakım planlarını zamanla** formunu kullanarak.  

- "Otomatik oluştur" olarak ayarlanmış takvim tabanlı bakım sıraları için otomatik olarak **Bakım sıralarını planla** formunu kullanarak.  

- Önleyici bakım işleri veya bakım istekleri olabilecek bakım zamanlamasından oluşturun.  

- Bir iş emrini el ile oluşturun.  

- **Tüm bakım istekleri** veya **Etkin bakım istekleri** veya **İşlem yapılacak yerleşim bakım isteklerim**'den bir iş emri oluşturun.

>[!NOTE]
>Aynı varlıkla ilgili iş emri işleri aynı proje koduyla ilgilidir.

## <a name="all-work-orders"></a>Tüm iş emirleri

Listeyi açmak için **Varlık yönetimi** > **Ortak** > **İş emirleri** > **Tüm iş emirleri**'ne tıklayın. **Tüm iş emirleri** tüm iş emirlerinin listesini içerir ve iş emriyle ilgili bazı bilgileri görüntüler.

![Şekil 1](media/01-work-orders.png)

- Etkin iş emirlerinin listesini görmek için **Varlık yönetimi** > **Genel** > **İş emirleri** > **Etkin İş emirleri**'ne tıklayın.

- Çalışan olarak ilgili olduğunuz işlem yapılacak yerleşimlere yüklenen iş emri işlerini içeren listeyi görmek için **Varlık yönetimi** > **Genel** > **İş emirleri** > **İşlem yapılacak yerleşim iş emri bakım işlerim**'e tıklayın (şurada ayarlanır: [Bakım görevlileri ve çalışan gruplarında](../setup-for-objects/workers-and-worker-groups.md)).

- **Tüm İş emirleri** listesinde (kılavuz görünümü), seçili kaydın Ayrıntılar görünümünü görüntülemek için **İş emri** sütunundaki bir bağlantıya tıklayın. Düzenlemek için açmak üzere üzere **Düzenle** düğmesini tıklatın.  

- Ayrıntılar görünümünde, iş emriyle ilgili ayrıntılı bilgileri görürsünüz.  

- Ayrıntılar görünümünde, iş emri iş ayrıntılarını görmek için **Satırlar** bağlantısını veya iş emri ayrıntılarını görmek için **Başlık** bağlantısını seçin.  

- Ekranın sağındaki dikey **İlgili bilgiler** bölmesi, iş emriyle ilgili ek bilgiler içerir. Seçili iş emri için ilgili bilgileri göstermek için bölmeyi genişletin.  


![Şekil 2](media/02-work-orders.png)


Eylem bölmesindeki eylem bölmesi düğmeleri sekmeler halinde düzenlenmiştir. Aşağıda, Kurumsal Varlık Yönetimiyle ilgili düğmelerin kısa bir açıklaması verilmektedir:



| Düğme adı                     | Tanım                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Düzenle                            | Seçilen iş emrini düzenleyin.                                                                                                                                                                                                                                           |
| Yeni                             | Yeni iş emri oluşturun.                                                                                                                                                                                                                                                  |
| Sil                          | Seçili iş emrini silin.                                                                                                                                                                                                                                         |
| İş emri havuzu                 | Seçili iş emrini bir iş emri havuzuna ekleyin veya iş emri havuzundan kaldırın.                                                                                                                                                                                           |
| Düzelt                          | Seçili iş emirlerinde beklenen başlangıç ve bitiş, hizmet düzeyi, sorumlu bakım görevlisi veya sorumlu bakım görevlisi grubu hakkındaki bilgileri ayarlayın.                                                                                                                                     |
| İlgili iş emri              | Seçili iş emri işiyle ilgili yeni bir iş emri oluşturun. Birincil ve ikincil iş emirlerini kaydetmek istiyorsanız bu yararlıdır.                                                                                                                              |
| İş emrini kopyala                 | Varolan bir iş emrine dayalı olarak yeni bir iş emri oluşturun.                                                                                                                                                                                                                |
| Olay geçmişi                   | İş emrindeki kayıt geçmişini görüntüleyin.                                                                                                                                                                                                                |
| İş emri bakım işi notları                           | Açıklama oluşturun, bir iş emrine bir notlar veya açıklamalar ekleyin. Nota kullanıcı adınızı ve zaman damgasu eklemek için **Zaman damgası ekle** düğmesini tıklatarak başlayın. Notlar **İş emri** formu > **Satır ayrıntıları** hızlı sekmesi > **Açıklama** sekmesinde görüntülenir. |
| Araçlar                           | Bir iş emrinde gerekli araçların listesini oluşturun. Araçlar **Kuruluş Yönetimi** > **Genel** > **Kaynaklar** > **Kaynaklar**'da ayarlanır.                                                                                                      |
| Bakım denetim listesi           | İş emrine bağlı varlıkla ilgili denetim listesini görüntüleyin.                                                                                                                                                                                                              |
| Kıymet hatası                     | Arıza yönetimi için kullanılacak bir varlıkla ilgili arıza bilgilerini görüntüleyin veya kaydedin.                                                                                                                                                                                        |
| Bakım kesinti süresi            | Bir iş emri için bakım kesinti süresini belirtin.                                                                                                                                                                                                                               |
| Koşul değerlendirme            | İş emri üzerinde koşul değerlendirmesi ölçümlerini kaydedin.                                                                                                                                                                                                             |
| Varlık sayaçları                 | Varlıkta sayaç kaıtları oluşturun veya bu kayıtları görüntüleyin.                                                                                                                                                                                                                     |
| Tahmin                        | Bir iş emrinde tahminleri görüntüleyin veya oluşturun.                                                                                                                                                                                                                               |
| Günlükler                        | İş emri günlüklerini görüntüleyin veya oluşturun. Tahminden günlük satırları kopyalanabilir.                                                                                                                                                                                         |
| Proje hareketleri            | Varlık için oluşturulan iş emirleriyle ilgili deftere nakledilen tüm hareketleri görüntüleyin.                                                                                                                                                                                             |
| İş emri durumunu güncelleştirme                | İş emri yaşam döngüsü durumunu güncelleştirin.                                                                                                                                                                                                                                                |
| Yaşam döngüsü durumu günlüğü                       | Seçili iş emrinin yaşam döngüsü durumlarını görüntüleyen günlük.                                                                                                                                                                                                                   |
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


**İş emri** sekmesi > **Proje** grubundaki düğmeler **Proje yönetimi ve muhasebe** modülündeki tahminler, günlükler ve faturalama gibi işlevselliklerle ilişkilidir.

>[!NOTE]
>Bir iş emrinde oluşturulan tahminler, **Varlık yönetimi parametreleri** formunda seçilen tahmin modeli kullanılarak Master planlama çalıştırılırken dahil edilebilir.

