---
title: Genel mobil cihaz parametreleri
description: Bu makalede, Ambar yönetimi parametreleri sayfasında mobil cihaz ayarlarının nasıl yapılandırılacağı açıklanmaktadır.
author: Mirzaab
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e6e03414edd9243fcc4156195928455b30a7cee9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847773"
---
# <a name="global-mobile-device-parameters"></a>Genel mobil cihaz parametreleri

[!include [banner](../includes/banner.md)]

Bu makalede, sistemin mobil cihazlarla etkileşim biçimini etkileyen genel ambar yönetimi parametrelerinin nasıl ayarlanacağı açıklanmaktadır.

Ambar çalışanlarını ayarlama hakkında daha fazla bilgi için bkz. [Ambar çalışanlarını yönetme](manage-warehouse-workers.md). Mobil cihazlarda plaka işleme hakkında daha fazla bilgi için bkz. [Warehouse Management mobil uygulaması aracılığıyla plaka teslim alma](warehousing-mobile-device-app-license-plate-receiving.md). Döngü sayımı işlemleri hakkında daha fazla bilgi için bkz. [Döngü sayımı](cycle-counting.md) ve [Döngü sayımı örnek senaryoları](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>Ambar yönetimi parametreleri sayfasını açma

**Ambar yönetimi parametreleri** sayfasını açmak için **Ambar yönetimi \> Kurulum \> Ambar yönetimi parametreleri**'ne gidin. Ardından bu makalenin sonraki bölümünde açıklandığı üzere mobil cihaz işi ile ilgili alanları ayarlayabilirsiniz.

## <a name="mobile-device-fasttab-on-the-general-tab"></a>Genel sekmesindeki mobil cihaz hızlı sekmesi

Genel mobil cihaz ayarları, **Ambar yönetimi parametreleri** sayfasının **Genel** sekmesindeki **Mobil cihaz** hızlı sekmesinde bulunur. Aşağıdaki alanlar kullanılabilir.

| Alan | Tanım |
|---|---|
| Mobil cihaz not türü | Satış siparişi malzeme çekme sırasında çalışanlara gösterilen bilgi türünü seçin. |
| Taranan miktar sınırı | Çalışanın *Ayarlama etkin* için **İş oluşturma işlemi** değerine sahip bir mobil cihaz menü öğesini kullanarak her oturum sırasında tarayabildiği maksimum madde miktarını girin. Bu alan, başka bir menü öğesi türünü kullanarak yapılan taramaları etkilemez. |
| Mobil cihaz oturum günlüğü kullan | Çalışan oturum açma geçmişi günlüğünü tutmak için bu seçeneği *Evet* olarak ayarlayın. Günlüğü görüntülemek için **İş kullanıcıları oturumları \> Sorgular ve raporlar \> Mobil cihaz günlükleri \> İş kullanıcısı oturumları**'na gidin. |
| Depolanan hataların sayısı | Sistemin depolaması gereken maksimum hata kaydı sayısını girin. Hata günlüğünü görüntülemek için **İş kullanıcıları oturumları \> Sorgular ve raporlar \> Mobil cihaz günlükleri \> İş kullanıcısı oturumları**'na gidin. |
| Varsayılan ambar transfer günlüğü | Çalışanlar ürünleri bir ambardan diğerine taşımak için mobil cihaz kullandığında kullanılacak günlüğü seçin. |
| Harici incelemede satınalma siparişi satırı kaydına izin ver | Çalışanların, *Harici incelemede* için **Onay durumu** değerine sahip satınalma siparişlerinin sipariş satırlarını kaydetmek üzere mobil cihaz kullanabilmesi gerekiyorsa bu seçeneği *Evet* olarak ayarlayın. Çalışanların, harici incelemede olan satınalma siparişlerinin satırlarını kaydetmesini önlemek için bu seçeneği *Hayır* olarak ayarlayın. |
| RSAT desteğini etkinleştir | Alan, uygulamanın gerçekleştirdiği her adımı günlüğe kaydeden ve doğrulayan Warehouse Management mobil uygulaması görev doğrulayıcısını etkinleştirir. Bu işlem sistem performansını önemli ölçüde yavaşlatabileceğinden doğrulayıcıyı yalnızca test sırasında etkinleştirmeniz gerekir. Bunu üretim ortamında hiçbir zaman etkinleştirmemelisiniz. |
