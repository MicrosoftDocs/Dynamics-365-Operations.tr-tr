---
title: Stok Görünürlüğü Eklentisi'ne genel bakış
description: Bu konuda, Stok Görünürlüğü'nün ne olduğu açıklanmakta ve özellikleri tanımlanmaktadır.
author: yufeihuang
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea1d8c1b0e8c996ead8461005960fa756ce6ca7
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678921"
---
# <a name="inventory-visibility-add-in-overview"></a>Stok Görünürlüğü Eklentisi'ne genel bakış

[!include [banner](../includes/banner.md)]

Stok Görünürlüğü Eklentisi (ayrıca *Stok Görünürlüğü* olarak da adlandırılır) gerçek zamanlı olarak elden stok takibi sağlayan bağımsız ve yüksek düzeyde ölçeklenebilir bir mikro hizmettir. Bu nedenle, stokun genel görünümünü sunar.

Harici sistemler, RESTful API'ler üzerinden hizmete erişir. Bu şekilde, belirli boyut kümelerinde eldeki bilgileri sorgulayabilir veya farklı özelleştirilmiş veri kaynaklarında stokta değişiklikler yapabilirler.

Microsoft Dataverse'te yerleşik bir mikro hizmet olarak Stok Görünürlüğü, genişletilebilirlik sağlar. Power Apps'i kullanarak uygulama oluşturabilirsiniz. Ayrıca iş gereksinimlerinizi karşılayan özelleştirilmiş işlevsellik sağlamak için Power BI'yı da uygulayabilirsiniz.

Standartlaştırılmış stok boyutları için yapılandırma seçeneklerini ve hareket türlerini ayarlayarak Stok Görünürlüğü'nü birden çok üçüncü taraf sistemle tümleştirebilirsiniz. Stok Görünürlüğü ayrıca yapılandırılabilir hesaplanmış miktarlar üzerinden özelleştirilmiş genişletilebilirliği de destekler.

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management ile Stok Görünürlüğü tümleştirmesi

Tümleşik çözüm, stok verilerini Dynamics 365 Supply Chain Management'tan çeker ve stok değişikliklerini sürekli olarak izler. Daha fazla bilgi için bkz.[Stok Görünürlüğü'nü yükleme ve ayarlama](inventory-visibility-setup.md) ve [Stok Görünürlüğü'nü yapılandırma](inventory-visibility-configuration.md).

## <a name="get-a-global-view-of-inventory"></a>Stokun genel görünümünü alma

Tümleşik çözüm, kendi veri kaynaklarınızı tanımlamanıza ve stok verilerini merkezileştirmenize olanak tanır. Daha fazla bilgi için bkz. [Stok Görünürlüğü'nü yapılandırma](inventory-visibility-configuration.md).

Stokunuzu görüntülemeye dair iki yaklaşım vardır:

- Yüksek performanslı API üzerinden bir sorgu gönderin. Bu API, doğrudan önbelleğe alınmış bir örnekten gerçek zamanlı stok verilerini döndürebilir. [Stok Görünürlüğü genel API'leri](inventory-visibility-api.md) içinde sözleşmeleri ve örnekleri bulabilirsiniz.
- Eldeki hammadde listesini görüntüleyin. Bu liste, önbelleğe alınmış bir örnekten düzenli olarak eşitlenir ve Dataverse'te görünür. Daha fazla bilgi için bkz. [Stok Görünürlüğü uygulaması](inventory-visibility-power-platform.md).

## <a name="soft-reservations"></a>Geçici rezervasyonlar

Geçici rezervasyon, bir işletmenin örneğin fazla satışı önleyecek şekilde satış siparişi tamamlamayı desteklemek için belirli bir ürün miktarını rezerve etmesi gerektiğinde uygulanır. Supply Chain Management'ta veya başka sipariş yönetimi sistemlerinde bir satış siparişi oluşturulup onaylandığında Stok Görünürlüğü'ne miktarı rezerve etme isteği gönderilir. Stok Görünürlüğü, boyut ayrıntılarına ve belirli stok hareket türlerine sahip ürünleri rezerve etmenize olanak tanır. (Daha fazla bilgi için bkz. [Stok Görünürlüğü uygulaması](inventory-visibility-power-platform.md).) Miktar başarıyla rezerve edildikten sonra rezervasyon kimliği döndürülür. Supply Chain Management'ta veya diğer sipariş yönetimi sistemlerinde orijinal siparişe geri bağlantı sağlamak için bu rezervasyon kimliğini kullanabilirsiniz.

Bu işlev, Stok Görünürlüğü'nde bir rezervasyonun toplam miktarı değiştirmeyeceği şekilde tasarlanmıştır. Bunun yerine, yalnızca rezerve edilen miktar işaretlenir. (Bu nedenle, buna *geçici rezervasyon* adı verilir.) Ürünler, Stok Görünürlüğü'nde miktar azaltması yapıp toplam miktarı güncelleştirmek için tekrar API'yi çağırarak Supply Chain Management'ta veya üçüncü taraf bir sistemde tüketildiğinde geçici rezerve edilen miktar denkleştirilebilir. Daha fazla bilgi için bkz. [Stok Görünürlüğü rezervasyonları](inventory-visibility-reservations.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
