---
title: Stok Görünürlüğü ipuçları
description: Bu konu, Stok Görünürlüğü eklentisini ayarlayıp kullanırken dikkate almanız gereken bazı ipuçları sağlar.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f5fb4c7cb941b352bbc6e2fcf5347244e1c8a40c
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920822"
---
# <a name="inventory-visibility-tips"></a>Stok Görünürlüğü ipuçları

[!include [banner](../includes/banner.md)]

Stok Görünürlüğü eklentisini ayarlayıp kullanırken dikkate almanız gereken bazı ipuçları aşağıda verilmiştir:

- Şu anda, Stok Görünürlüğü eklentisi yalnızca Microsoft Dynamics Lifecycle Services (LCS) kullanılarak oluşturulan Microsoft Dataverse ortamlarını desteklemektedir. Dataverse ortamınız başka bir yolla (örneğin, Power Apps yönetim merkezi kullanılarak) oluşturulduysa ve Dynamics 365 Supply Chain Management ortamınıza bağlıysa eşleme sorununu çözmek için durumu ilk olarak Stok Görünürlüğü ürün ekibine sormanız gerekir. Ekiple [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden iletişime geçebilirsiniz. Ekip, ortamınız Stok Görünürlüğü eklentisini yüklemeye hazır olduğunda sizi bilgilendirecektir.
- Birden fazla LCS ortamınız varsa her ortam için farklı bir Azure Active Directory (Azure AD) uygulaması oluşturun. Farklı ortamlar için Stok Görünürlüğü Eklentisini yüklemek üzere aynı uygulama kimliğini ve kiracı kimliğini kullanırsanız daha eski ortamlar için bir belirteç sorunu oluşur. Yüklenmiş olan Stok Görünürlüğü eklentisinin yalnızca son örneği geçerli olacaktır.
- Stok Görünürlüğü şu anda, bulutta barındırılan ortamlar için desteklenmemektedir. Yalnızca Katman-2+ ortamları için desteklenmektedir.
- Uygulama programlama arabirimi (API) şu anda `ProductID` değerine göre en çok 100 ayrı öğeye kadar sorgulamayı desteklemektedir. Her sorguda birden çok `SiteID` ve `LocationID` değeri de belirtilebilir. Maksimum sınır `NumOf(SiteID) * NumOf(LocationID) <= 100` olarak tanımlanmıştır.
- `fno` veri kaynağı, Supply Chain Management için rezerve edilmiştir. Stok Görünürlüğü eklentiniz bir Supply Chain Management ortamıyla tümleşikse [veri kaynağındaki](inventory-visibility-configuration.md#data-source-configuration) `fno` ile ilgili yapılandırmaları silmemenizi öneririz.
- Şu anda [bölüm yapılandırması](inventory-visibility-configuration.md#partition-configuration), verilerin nasıl dağıtıldığını gösteren iki temel boyuttan (`SiteId` ve `LocationId`) oluşur. Aynı bölüm altındaki işlemler daha düşük maliyetle daha yüksek performans sağlayabilir. Çözüm varsayılan olarak bu bölüm yapılandırmasını içerir. Bu nedenle, *kendiniz tanımlamak zorunda değilsiniz*. Varsayılan bölüm yapılandırmasını özelleştirmeyin. Yapılandırmayı siler veya değiştirirseniz beklenmeyen bir hataya neden olabilirsiniz.
- Bölüm yapılandırmasında tanımlanan temel boyutlar, [ürün dizini hiyerarşi yapılandırmasında](inventory-visibility-configuration.md#index-configuration) tanımlanmamalıdır.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
