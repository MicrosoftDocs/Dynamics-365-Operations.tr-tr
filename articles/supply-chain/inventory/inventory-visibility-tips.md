---
title: Inventory Visibility ipuçları
description: Bu makale, Stok Görünürlüğü eklentisini ayarlayıp kullanırken dikkate almanız gereken bazı ipuçları sağlar.
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
ms.openlocfilehash: 3bdd161815a15d5c39b3c0afc176a288c8d9055a
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306100"
---
# <a name="inventory-visibility-tips"></a>Stok Görünürlüğü ipuçları

[!include [banner](../includes/banner.md)]

Stok Görünürlüğü eklentisini ayarlayıp kullanırken dikkate almanız gereken bazı ipuçları aşağıda verilmiştir:

- Şu anda, Stok Görünürlüğü eklentisi yalnızca Microsoft Dynamics Lifecycle Services (LCS) kullanılarak oluşturulan Microsoft Dataverse ortamlarını desteklemektedir. Dataverse ortamınız başka bir yolla (örneğin, Power Apps yönetim merkezi kullanılarak) oluşturulduysa ve Dynamics 365 Supply Chain Management ortamınıza bağlıysa eşleme sorununu çözmek için durumu ilk olarak Stok Görünürlüğü ürün ekibine sormanız gerekir. Ekiple [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden iletişime geçebilirsiniz. Ekip, ortamınız Stok Görünürlüğü eklentisini yüklemeye hazır olduğunda sizi bilgilendirecektir.
- Birden fazla LCS ortamınız varsa her ortam için farklı bir Azure Active Directory (Azure AD) uygulaması oluşturun. Farklı ortamlar için Stok Görünürlüğü Eklentisini yüklemek üzere aynı uygulama kimliğini ve kiracı kimliğini kullanırsanız daha eski ortamlar için bir belirteç sorunu oluşur. Yüklenmiş olan Stok Görünürlüğü eklentisinin yalnızca son örneği geçerli olacaktır.
- Stok Görünürlüğü şu anda, bulutta barındırılan ortamlar için desteklenmemektedir. Yalnızca Katman-2+ ortamları için desteklenmektedir.
- Uygulama programlama arabirimi (API) şu anda `ProductID` değerine göre en çok 100 ayrı öğeye kadar sorgulamayı desteklemektedir. Her sorguda birden çok `SiteID` ve `LocationID` değeri de belirtilebilir. Maksimum sınır `NumOf(SiteID) * NumOf(LocationID) <= 100` olarak tanımlanmıştır.
- Toplu API, her istek için en fazla 512 kayıt döndürebilir.
- `fno` veri kaynağı, Supply Chain Management için rezerve edilmiştir. Stok Görünürlüğü eklentiniz bir Supply Chain Management ortamıyla tümleşikse [veri kaynağındaki](inventory-visibility-configuration.md#data-source-configuration) `fno` ile ilgili yapılandırmaları silmemenizi öneririz.
- Stok Görünürlüğü, `fno` veri kaynağına ilişkin hiçbir veriyi değiştiremiyor. Veri akışı tek yönlüdür, `fno` veri kaynağına ilişkin tüm miktar değişikliklerinin Supply Chain Management ortamınızdan gelmelidir. Bu nedenle, `fno` veri kaynağına ilişkin eldeki değişiklikler veya rezervasyon istekleri göndermek için API'yi kullanamazsınız.
- Supply Chain Management ortamınıza bir veya daha fazla yeni ölçüm eklerseniz, bunları da Stok Görünürlüğüne eklemelisiniz. Ancak, yeni ölçümler için tüm miktar değişiklikleri Supply Chain Management ortamınızdan gelmelidir.
- Şu anda [bölüm yapılandırması](inventory-visibility-configuration.md#partition-configuration), verilerin nasıl dağıtıldığını gösteren iki temel boyuttan (`SiteId` ve `LocationId`) oluşur. Aynı bölüm altındaki işlemler daha düşük maliyetle daha yüksek performans sağlayabilir. Çözüm varsayılan olarak bu bölüm yapılandırmasını içerir. Bu nedenle, *kendiniz tanımlamak zorunda değilsiniz*. Varsayılan bölüm yapılandırmasını özelleştirmeyin. Yapılandırmayı siler veya değiştirirseniz beklenmeyen bir hataya neden olabilirsiniz.
- Bölüm yapılandırmasında tanımlanan temel boyutlar, [ürün dizini hiyerarşi yapılandırmasında](inventory-visibility-configuration.md#index-configuration) tanımlanmamalıdır.
- [Ürün dizini hiyerarşi yapılandırmanızda](inventory-visibility-configuration.md#index-configuration) en az bir dizin hiyerarşiniz olmalıdır (örneğin, `Empty` temel boyutunu içeren), aksi takdirde sorgular "dizin hiyerarşisi ayarlanmadı" hatasıyla başarısız olur.
- Veri kaynağı `@iv`, önceden tanımlanmış bir veri kaynağıdır ve `@` önekiyle `@iv` içinde tanımlanan fiziksel ölçümlerdir. Bu ölçümler tahsisat özelliği için önceden tanımlanmış bir yapılandırmadır; bu nedenle onları değiştirmeyin veya silmeyin. Aksi durumda, tahsisat özelliğini kullanırken beklenmedik hatalarla karşılaşabilirsiniz.
- Önceden tanımlanmış hesaplanan `@iv.@available_to_allocate` ölçümüne yeni fiziksel ölçümler ekleyebilirsiniz ancak adını değiştirmemeniz gerekir.
- Supply Chain Management veritabanınızı geri yüklemeniz durumunda geri yüklenen veritabanınız daha önce Stok Görünürlüğü ile Dataverse'e eşitlenen veriler ile artık tutarlı olmayan veriler içerebilir. Bu veri tutarsızlığı sistem hatalarına ve diğer sorunlara neden olabilir. Bu nedenle, bir Supply Chain Management veritabanını geri yüklemeden önce daima tüm ilgili Stok Görünürlük verilerini Dataverse'den temizlemeniz önemlidir. Ayrıntılar için bkz. [Supply Chain Management veritabanını geri yüklemeden önce Dataverse'den Stok Görünürlük verilerini temizleme](inventory-visibility-setup.md#restore-environment-database).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
