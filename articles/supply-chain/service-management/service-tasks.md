---
title: Servis görevlerine genel bakış
description: Servis görevlerini, servis siparişi sırasında tamamlanacak görevleri açıklamak için kullanın. Teknisyenler ve müşteriler bu bilgileri görebilir.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b5bf87fbe5ecb711f641a006d56c94d6e679944
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338389"
---
# <a name="service-tasks-overview"></a>Servis görevlerine genel bakış

[!include [banner](../includes/banner.md)]

Servis görevlerini, servis siparişi sırasında tamamlanacak görevleri açıklamak için kullanın.
Teknisyenler ve müşteriler bu bilgileri görebilir.

Servis görevlerini **Servis görevleri** sayfasında oluşturur ve servis görevi ilişkileri oluşturarak bu görevleri belirli bir servis sözleşmesi veya servis siparişiyle ilişkilendirirsiniz. Servis görevi ilişkisi oluşturduğunuz her durumda aşağıdakileri oluşturabilirsiniz:

-  Görevle ilgili olarak, görev hakkında teknisyenin bilmesi gereken ayrıntılı teknik talepler gibi dahili notlar oluşturabilirsiniz.

-  Müşterinin görebildiği harici notlar. Bunlar, müşteriyle servis şirketi arasındaki sözleşme uyarınca tamamlanması gereken görevin daha az teknik olan bir açıklamasını sağlayabilir.

Servis göreviyle servis siparişi veya servis sözleşmesi arasında servis görevi ilişkisini ayarladığınızda, geçerli servis siparişi veya servis sözleşmesi için servis siparişi satırları veya servis sözleşmesi satırları oluştururken bu servis görevini belirleyebilirsiniz.

Servis sözleşmesinden servis siparişleri oluştururken, servis siparişi satırlarını servis siparişleri halinde gruplandırmak için her servis sözleşmesi satırına atanmış servis görevlerini kullanabilirsiniz.

## <a name="create-a-service-task"></a>Servis görevi oluşturma

1. **Servis yönetimi** \> **Kurulum** \> **Servis görevleri**'ne tıklayın.
2. Yeni satır oluşturun.
3. Servis kodu ile açıklamasını girin.

## <a name="example"></a>Örnek

Teknisyenin müşterinin tesisinde bir dişli kutusu (servis nesnesi GB-1234) üzerinde iki iş tamamlaması gerekiyor. Müşteri için bir servis sözleşmesi oluşturulur ve birkaç hareket işlerle ilişkilendirilir. İki iş için servis sözleşmesi ve servis sözleşmesi satırları aşağıdaki gibidir:

### <a name="service-agreement"></a>Servis sözleşmesi

| Proje | Servis sözleşmesi | Tanım                                  | Grup   |
|---------|-------------------|----------------------------------------------|---------|
| 9012    | 000008\_001       | İnceleme ve rutin değiştirme – GB-1234 | Prim |

### <a name="service-agreement-lines"></a>Servis sözleşmesi maddeleri

| Tanım             | Hareket türü | Servis nesnesi | Servis görevi |
|-------------------------|------------------|----------------|--------------|
| İnceleme ve temizleme | Saat             | GB-1234        | I/C - GB1234 |
| Seyahat                  | Gider          | GB-1234        | I/C - GB1234 |
| Malzemeler               | Madde             | GB-1234        | I/C - GB1234 |
| Rutin değiştirme     | Saat             | GB-1234        | RR - GB1234  |
| GR-1                    | Madde             | GB-1234        | RR - GB1234  |
| GR-5                    | Madde             | GB-1234        | RR - GB1234  |

İki işin servis sözleşmesi satırlarına eklenmiş iki servis görevi vardır. Servis görevleri, her işe ait olan hareketleri belirler. İlk durumda, I/C - GB1234 servis görevi, GB-1234 parçasını inceleme ve temizleme işlemleri kapsamındaki tüm servis sözleşmesi satırlarını belirler. İkinci durumda, RR - GB1234 servis görevi rutin değiştirme görevinin tamamlanması kapsamındaki tüm servis sözleşmesi satırlarını belirler.

Servis görevlerini bu belirli anlaşmaya bağlayan servis görevi ilişkileri şunlardır:

### <a name="service-tasks"></a>Servis görevleri

| Servis görevi | Açıklama                             | Dahili not                                                                                                                 | Harici not                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| I/C - GB1234 | GB-1234 vites kutusunun denetlenmesi           | GB-1234 vites kutusunu görsel ve mekanik olarak inceleme ve temizleme                                                              | Vites kutusunun rutin denetimi |
| RR - GB1234  | GB-1234 içindeki parçaların rutin değiştirilmesi | GR-1 ve GR-5 bileşenlerinin rutin servis değiştirmesi (2002'den önce üretilmiş vites kutularında GR-2 bileşeni de değiştirilsin) | Parçaları rutin olarak değiştirme  |

## <a name="group-service-orders"></a>Servis siparişlerini gruplama

Servis siparişlerini otomatik olarak oluşturduğunuzda, servis görevlerini gruplandırma ölçütleri olarak kullanabilirsiniz. Servis siparişlerini belirli servis görevlerine göre gruplandırmak için, servis sözleşmesini temel alan servis siparişlerinin gruplandırılmasında ilk gruplandırma ölçütü olarak servis görevi kodunun kullanılacağını servis sözleşmesinde tanımlayın.

**Servis görevine göre gruplandırma**

1. **Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.
2. **Kurulum** sekmesinde, **Servis siparişlerini birleştir** alanında **Servis görevine göre**'yi seçin.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]