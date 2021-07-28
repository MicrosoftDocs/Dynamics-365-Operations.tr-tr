---
title: İşlem yapılacak yerleşimlere giriş
description: Bu konuda, Varlık Yönetimi'ndeki işlem yapılacak yerleşimlere genel bir bakış sağlanmaktadır.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationEditSubLocations, EntAssetFunctionalLocationLookup, EntAssetFunctionalLocationRename, EntAssetFunctionalLocation
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
ms.openlocfilehash: f31504d2e4ce61e64eb96c2b69326bcb4f1f2560
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337111"
---
# <a name="introduction-to-functional-locations"></a>İşlem yapılacak yerleşimlere giriş

[!include [banner](../../includes/banner.md)]

 

Bu konuda, Varlık Yönetimi'ndeki işlem yapılacak yerleşimlere genel bir bakış sağlanmaktadır. İşlem yapılacak yerleşimler, bir sistemdeki işlevsel birimler gibi teknik bir yapının unsurlarından biridir. İşlem yapılacak yerleşimler hiyerarşik olarak oluşturulur ve bunlara varlıklar yüklersiniz. Şirketinizdeki işlem yapılacak yerleşimler kurulumu şirketin gereksinimlerine bağlıdır.

İşlem yapılacak yerleşimlerin kullanımına ilişkin bazı örnekler şunlardır:

- **İşlevsel**: İşlem yapılacak yerleşimler kullanıcı odaklı olabilir ve benzer davranışlara sahip varlıkları yönetmek için kullanılır.
- **Süreçle ilgili**: İşlem yapılacak yerleşimler iş akışı odaklı olabilir.
- **Uzamsal**: İşlem yapılacak yerleşimler coğrafi konumları veya tesisleri temsil edebilir.

Her işlem yapılacak yerleşim, Varlık Yönetiminde bağımsız olarak yönetilir. İşlem yapılacak yerleşimlerin yararlı özelliklerden bazıları aşağıda verilmiştir:

- İşlem yapılacak yerleşim özelliklerini ayarlayın.
- Varlık özellik gereksinimlerini ayarlayın.
- Önleyici ve reaktif bakım için bakım sıraları ayarlayın.
- Yüklü varlıkları yönetin.
- Yüklü varlıklarla ilgili etkin istekleri ve iş emirlerini izleyin.
- Varlıklar üzerinde kayıtlı hataları izleyin.
- Herhangi bir zamanda işlem yapılacak yerleşimle ilgili varlıklara yönelik bakım maliyetlerini takip edin.

İşlem yapılacak yerleşimler istekler, iş emirleri, arıza kayıtları, koşul değerlendirmeleri, üretim durdurma kayıtları ve varlık sayaç kayıtları ile ilgili olarak varlık izlenebilirliği sağlar.

> [!NOTE]
> Bir varlık yaşam süresi boyunca çeşitli işlem yapılacak yerleşimlere yüklense bile maliyetler her yerleşimle ilgili olabilir. Başka bir deyişle, varlık maliyetleri her zaman varlığın belirtilen zamanda yüklü olduğu işlem yapılacak yerleşim ile ilişkilidir.

İşlem yapılacak yerleşimler esnek **değildir**. Bu nedenle, işlem yapılacak yerleşim hiyerarşisi ayarladıktan sonra, içindeki konumları taşıyamazsınız. 

İşlem yapılacak yerleşim hiyerarşisi oluşturduktan sonraki adım buna varlıkları yüklemektir. Daha fazla bilgi için bkz. [Varlıkları işlem yapılacak yerleşimlere yükleme](../functional-locations/install-objects-on-functional-locations.md).

## <a name="all-functional-locations"></a>Tüm işlem yapılacak yerleşimler

**Varlık yönetimi** \> **Genel** \> **İşlem yapılacak yerleşimler** \> **Tüm işlem yapılacak yerleşimler**'i seçip **Tüm işlem yapılacak yerleşimler** liste sayfasını açın. Bu sayfa tüm işlem yapılacak yerleşimleri ve her biriyle ilgili bazı bilgileri gösterir. Yalnızca etkin işlem yapılacak yerleşimleri görüntülemek için **Etkin işlem yapılacak yerleşimler**'i seçin. Yalnızca çalışan olarak ilgili olduğunuz işlem yapılacak yerleşimleri görüntülemek için **Etkin işlem yapılacak yerleşimlerim**'i seçin. (Bu ilişki **Çalışanlar** sayfasında ayarlanır. Daha fazla bilgi için [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md) bölümüne bakın.)

**Tüm işlem yapılacak yerleşimler** liste sayfasında, seçili kaydın ayrıntılarını görüntülemek için **İşlem yapılacak yerleşim** sütunundan bir bağlantı seçin. İşlem yapılacak yerleşimi düzenlemek için **Düzenle** düğmesini seçin. Ayrıntılar görünümü yerleşimle ilgili ayrıntılı bilgileri gösterir. Ayrıca sağda bulunan bir **İlgili bilgi** bölmesi içerir. Bu bölme, işlem yapılacak yerleşim hiyerarşisini gösterir. **İlgili bilgi** bölmesini genişletebilir ve daraltabilirsiniz.

Eylem Bölmesi'ndeki düğmeler sekmeler halinde düzenlenmiştir. Aşağıdaki tabloda Kıymet Yönetimi'yle ilgili düğmeler kısaca açıklanmaktadır.

| Düğme adı                         | Tanım                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Düzenle                                | Sayfa için düzenleme modu ve görüntüleme modu arasında geçiş yapın.                                                                                         |
| Yeni                                 | Yeni bir işlem yapılacak yerleşim oluşturun.                                                                                                            |
| Sil                              | Seçili işlem yapılacak yerleşimi silin.                                                                                                     |
| Yeniden adlandır                              | Seçili işlem yapılacak yerleşimi yeniden adlandırın.                                                                                                     |
| İşlem yapılacak yerleşim yapısını kopyala  | İşlem yapılacak yerleşim hiyerarşisini kopyalayın.                                                                                                      |
| Varlık yükle                       | İşlem yapılacak yerleşime alt varlıklar da dahil olmak üzere bir varlık yükleyin.                                                                        |
| Varlığı değiştir                       | Varlık hiyerarşisini işlem yapılacak yerleşimdeki başka bir varlık hiyerarşisiyle değiştirin.                                                         |
| Maliyet kontrolü                        | Seçili işlem yapılacak yerleşim için maliyet hesaplaması yapabileceğiniz **İşlem yapılacak yerleşim maliyet kontrolü** sayfasını açın.                |
| Saat denetimi                        | Seçili işlem yapılacak yerleşim için maliyet hesaplaması yapabileceğiniz **İşlem yapılacak yerleşim saat kontrolü** sayfasını açın.                |
| Varlıklar                              | Seçili işlem yapılacak yerleşimle ilgili varlıkların listesini görüntüleyebileceğiniz **Tüm varlıklar** sayfasını açın.                      |
| Talepler                            | Seçili işlem yapılacak yerleşimle ilgili taleplerin listesini görüntüleyebileceğiniz **Etkin talepler** sayfasını açın.               |
| İş emirleri                         | Seçili işlem yapılacak yerleşimle ilgili iş emirlerinin listesini görüntüleyebileceğiniz **Etkin iş emirleri** sayfasını açın.         |
| Hatalar                              | Seçili işlem yapılacak yerleşimle ilgili varlık arıza kayıtları listesini görüntüleyebileceğiniz **Varlık hataları** sayfasını açın. |
| İşlem yapılacak yerleşim durumunu güncelleştir    | Seçili işlem yapılacak yerleşimin aşamasını güncelleştirin.                                                                                        |
| Yaşam döngüsü durumu günlüğü                 | Seçili işlem yapılacak yerleşimin aşamalarını gösteren günlüğü görüntüleyin.                                                                        |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]