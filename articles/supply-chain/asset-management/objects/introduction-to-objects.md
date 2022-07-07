---
title: Kıymetler tanıtımı
description: Bu makalede, Kıymet Yönetimi'ndeki kıymetlere genel bir bakış sağlanmaktadır.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetTimeline, EntAssetObjectTableLookup, EntAssetObjectTableParent, EntAssetObjectOverview, EntAssetObjectImage, EntAssetObjectTable, EntAssetLifecycleStateLog, EntAssetObjectWorkOrderActive, EntAssetObjectAttribute
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2214"
- intro-internal
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8498d6099112cea2c57a6387e7596adb5bcd84e
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016028"
---
# <a name="introduction-to-assets"></a>Kıymetler tanıtımı

[!include [banner](../../includes/banner.md)]

 

Bu makalede, Kıymet Yönetimi'ndeki kıymetlere genel bir bakış sağlanmaktadır. *Kıymet* makine veya makine parçası gibi, bakım, servis veya onarım gerektiren her türlü ekipmandır.

Kıymet ilgili bilgilerle otomatik olarak güncelleştirilir. Örneğin bu ilgili bilgiler yeni veya güncelleştirilmiş iş emirleri hakkında olabilir. Kıymetleri **Tüm kıymetler** menü öğesini veya **Bekleyen kıymetler** menü öğesini kullanarak oluşturabilirsiniz. Bu makalede kıymetlerin **Tüm kıymetler** menü öğesi kullanarak nasıl oluşturulacağı açıklanmaktadır. Kıymetleri **Bekleyen kıymetler** menü öğesini kullanarak oluşturma hakkında bilgi için [Kıymetleri satınalma siparişlerine göre oluşturma](../objects/create-objects-based-on-purchase-orders.md) bölümüne bakın.

## <a name="all-assets"></a>Tüm kıymetler

**Kıymet yönetimi** \> **Kıymetler** \> **Tüm kıymetler** öğesini seçin. **Tüm kıymetler** listesi sayfası tüm kıymetleri ve bunlarla ilgili bazı bilgileri gösterir. Yalnızca etkin kıymetleri görüntülemek için **Etkin kıymetler**'i seçin. Yalnızca bakım görevlisi olarak ilgili olduğunuz işlem yapılacak yerleşimde kurulu kıymetleri görüntülemek için **Etkin kıymetlerim**'i seçin. (Bu ilişki **Çalışanlar** sayfasında ayarlanır. Daha fazla bilgi için [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md) bölümüne bakın.)

**Tüm kıymetler** ızgara görünümünde seçili kaydın ayrıntılarını görüntülemek için **Kıymet** sütunundan bir bağlantı seçin. Kaydı düzenlemek için **Düzenle** düğmesini seçin. Ayrıntılar görünümü kıymetle ilgili ayrıntılı bilgileri gösterir. Sağdaki bir **İlgili bilgiler** bölmesi kıymetle ilgili ek bilgileri içerir. Seçili kıymet için ilgili bilgileri göstermek için bölmeyi genişletin.

Eylem Bölmesi'ndeki düğmeler sekmeler halinde düzenlenmiştir. Aşağıdaki tabloda Kıymet Yönetimi'yle ilgili düğmeler kısaca açıklanmaktadır.

| Düğme adı          | Tanım                                                                                                                                                       |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Düzenle                 | Seçili kıymeti düzenleyin.                                                                                                                                         |
| Yeni                  | Yeni bir kıymet oluşturun.                                                                                                                                                |
| Sil               | Seçili kıymeti silin.                                                                                                                                       |
| Kıymeti taşı           | Kıymetleri başka bir kıymet yapısına veya aynı kıymet yapısındaki başka bir yerleşime taşıyın.                                                                                         |
| Kıymeti değiştir        | Kıymet hiyerarşisindeki bir alt kıymeti başka bir kıymetle değiştirin.                                                                                                  |
| Kıymet yükle        | Kıymeti bir işlem yapılacak yerleşime yükleyin.                                                                                                                          |
| Kıymeti kopyala           | Kıymet hiyerarşisini başka bir kıymete kopyalayın.                                                                                                                          |
| Talepler             | **Etkin talepler** listesi sayfasını açın. Buradan seçili kıymet için oluşturulan bakım taleplerini görüntüleyebilirsiniz.                                                                         |
| Olay geçmişi        | Kıymet üzerinde yapılmış çeşitli kayıtlara genel bakışı görüntüleyin.                                                                                                         |
| Kıymet ürün reçetesi            | Kıymet üzerinde kullanılan tüm öğelerin (yedek parçalar ve diğer öğeler) listesini görüntüleyin.                                                                                  |
| İş emirleri          | **Etkin iş emirleri** listesi sayfasını açın. Buradan kıymete ilişkin iş emirlerini görüntüleyebilirsiniz.                                                                                        |
| Onay listesi            | Kıymet üzerinde kaydedilmiş bakım denetim listelerine ve ölçümlere genel bakışı görüntüleyin.                                                                                                 |
| Bakım kesinti süresi | Kıymet üzerindeki bakım kesinti süresi kayıtları oluşturun veya bu kayıtları görüntüleyin.                                                                                                       |
| Proje hareketleri | Kıymet için oluşturulan iş emirleriyle ilişkili tüm deftere nakledilen hareketleri görüntüleyin.                                                                                       |
| Kıymet ölçüleri       | Kıymet üzerinde kıymet ölçümleri oluşturun veya görüntüleyin.                                                                                                               |
| Bakım zamanlaması | **Bakım zamanlamasını aç** listesi sayfasını açın. Buradan kıymetle ilişkili ve **Oluşturuldu** durumundaki bakım planlarını, bakım taleplerini ve bakım sıralarını görüntüleyebilirsiniz. |
| Kıymet durumunu güncelleştir   | Kıymet yaşam döngüsü durumunu güncelleştirin. **Tüm kıymetler** listesi sayfasında birden fazla kıymet seçebilir ve aynı anda hepsinin kıymet yaşam döngüsü durumunu güncelleştirebilirsiniz.              |
| Yaşam döngüsü durumu günlüğü  | Seçili kıymetin yaşam döngüsü durumlarını gösteren günlüğü açın.                                                                                                                 |
| Kıymet belgeleri      | Kıymete eklenen belgelerin listesini görüntüleyin. Bu belgeler **Kıymet yönetimi** \> **Kurulum** \> **Kıymet belgeleri** altından ayarlanır.                 |
| Öznitelikler           | Kıymet özniteliklerini oluşturun veya görüntüleyin.                                                                                                                             |
| Görüntü                | Kıymet için bir resim seçin.                                                                                                                                   |
| Üst kıymetler        | Seçili kıymet için üst kıymet geçmişini görüntüleyin.                                                                                                                |
| İşlem yapılacak yerleşimler | Seçili kıymet için işlem yapılacak yerleşim geçmişini görüntüleyin.                                                                                                          |
| Koşul değerlendirmesi | Kıymet üzerinde koşul değerlendirmesi ölçümlerini kaydedin.                                                                                                         |
| Hatalar               | **Kıymet hataları** listesi sayfasını açın. Buradan kıymet üzerinde kaydedilmiş hataları görüntüleyebilirsiniz.                                                                                             |
| Maliyet kontrolü         | Kıymetteki bütçe maliyetlerini ve fiili maliyetleri karşılaştırın.                                                                                                              |
| Saat denetimi         | Kıymet üzerindeki tahmini saatleri ve fiili saatleri karşılaştırın.                                                                                                              |
| Kıymet KPI'ları           | Kıymetin temel performans göstergelerini (KPI'larını) hesaplayın ve görüntüleyin.                                                                                              |
| İş türleri            | Kıymet için geçerli varsayılan iş türlerine genel bakışı görüntüleyin.                                                                                                            |
| Kritiklik türleri    | Kıymet kritiklik türlerini görüntüleyin veya güncelleştirin.                                                                                                                              |
| Yedek parçalar          | Kıymette kullanılabilecek onaylanmış ve alternatif yedek parçaların listesini görüntüleyin.                                                                               |
| Kıymet tüketimi    | Kıymetin tüketim kayıtlarını gösteren bir rapor yazdırın.                                                                                                |
| Kıymet hatası          | Kıymetin hata kayıtlarını gösteren bir rapor yazdırın.                                                                                                      |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]