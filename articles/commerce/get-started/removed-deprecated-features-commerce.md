---
title: Dynamics 365 Commerce'ta kaldırılan veya artık kullanılmayan özellikler
description: Bu konu Dynamics 365 Commerce'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: josaw
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b582b8b95fcf2ad45aa1bb49eb5594d30874e0f4
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559571"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Dynamics 365 Commerce'ta kaldırılan veya artık kullanılmayan özellikler

[!include [banner](../includes/banner.md)]

Bu konu Dynamics 365 Commerce'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır. 

> [!NOTE]
> Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](/dynamics/s-e/) raporları altından ulaşabilirsiniz. Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Commerce 10.0.21 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Commerce parametrelerinde çakışan iskontoların işlenme ayarı

**Commerce parametreleri** sayfasındaki **Çakışan iskontoların işlenmesi** ayarı, Commerce 10.0.21 sürümünde kullanım dışı bırakılmıştır. Gelecekte, Commerce fiyatlandırma altyapısı, çakışan iskontoların en uygun birleşimini belirlemek için tek bir algoritma kullanacaktır.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | <p>Commerce parametrelerindeki **Çakışan iskontoların işlenmesi** ayarı, Commerce fiyatlandırma altyapısının nasıl arama yaptığını denetler ve çakışan iskontoların en uygun birleşimini belirler. Bu ayar şu anda üç seçenek sunuyor:<p><ul><li> **En iyi performans**: Bu seçenek, en iyi iskonto birleşimini zamanında önceliklendirmek, değerlendirmek ve belirlemek için gelişmiş bir buluşsal algoritma ve [marjinal değer sıralaması](../optimal-combination-overlapping-discounts.md) yöntemini kullanır.</li><li>**Dengelenmiş hesaplama**: Bu seçenek, geçerli kod tabanında tıpkı **En iyi performans** seçeneği gibi çalışır. Bu nedenle, bu seçenek esasen yinelenmiş bir seçenektir.</li><li>**Kapsamlı hesaplama**: Bu seçenek, fiyat hesaplaması sırasında tüm olası iskonto birleşimlerini kullanan eski bir algoritma kullanır. Bu seçenek, çok fazla satırı ve miktarı olan siparişler için performans sorunlarına neden olabilir.</li></ul><p>Yapılandırmayı basitleştirmeye, performansı iyileştirmeye ve eski algoritmanın neden olduğu sorunları azaltmaya yardımcı olmak için **Çakışan iskontoların işlenmesi** ayarını tamamen kaldıracağız ve Commerce fiyatlandırma altyapısının dahili mantığını artık yalnızca gelişmiş algoritmayı (**En iyi performans** seçeneğinin kullandığı algoritma) kullanacak şekilde güncelleştireceğiz.</p> |
| **Başka bir özellikle mi değiştirildi?**   | Hayır. **Dengelenmiş hesaplama** veya **Kapsamlı hesaplama** seçeneğini kullanan kuruluşların bu özellik kaldırılmadan önce **En iyi performans** seçeneğine geçmesini öneririz. |
| **Etkilenen ürün alanları**         | Fiyatlandırma ve iskontolar |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Ekim 2022'de yayımlanacak 10.0.21 sürümü itibarıyla **Çakışan iskontoların işlenmesi** ayarı Commerce parametrelerinden kaldırılacaktır. |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>Lifecycle Services kullanılarak dağıtılan Retail SDK

Retail SDK, Lifecycle Services (LCS) ile birlikte gelir. Bu dağıtım modu, 10.0.21 sürümünde kullanım dışı bırakılmıştır. Bundan sonra Retail SDK başvuru paketleri, kitaplıklar ve örnekler GitHub'daki genel depolarda yayımlanacaktır.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Retail SDK, LCS ile birlikte gelir. LCS işleminin tamamlanması birkaç saat sürer ve işlemin her güncelleştirme için tekrarlanması gerekir. Bundan sonra Retail SDK başvuru paketleri, kitaplıklar ve örnekler GitHub'daki genel depolarda yayımlanacaktır. Uzantı örnekleri ve başvuru paketleri kolayca tüketilebilir ve güncelleştirmeler birkaç dakika içinde tamamlanır. |
| **Başka bir özellikle mi değiştirildi?**   |  [GitHub ve NuGet'ten Retail SDK örnekleri ve başvuru paketleri indirme](../dev-itpro/retail-sdk/sdk-github.md) |
| **Etkilenen ürün alanları**         | Retail SDK'si |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 10.0.21 sürümünden itibaren LCS VM'leri aracılığıyla gönderilen SDK, Ekim 2022'de kaldırılacaktır. |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>Perakende dağıtılabilir paketi ve birleşik POS, Donanım istasyonu ve Bulut Ölçeği birimi yükleyicileri

Retail SDK MSBuild kullanılarak oluşturulan perakende dağıtılabilir paketleri 10.0.21 sürümünde kullanım dışı bırakılmıştır. Bundan sonra, Bulut Ölçek Birimi uzantıları (Commerce Runtime, kanal veritabanı, Gözetimsiz ticari API'ler, Ödemeler ve Bulut Satış Noktası (POS)) için Bulut Ölçek Birimi (CSU) paketini kullanın. POS, Donanım istasyonu ve Şirket içinde barındırılan bulut ölçek birimi için yalnızca uzantılı yükleyiciler kullanın.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Perakende dağıtılabilir paketi, eksiksiz bir uzantı paketleri ve yükleyiciler setinden oluşan birleşik bir pakettir. CSU uzantıları Bulut ölçek birimine gittiğinden ve yükleyiciler mağazalarda dağıtıldığından bu birleşik paket, dağıtımı karmaşık hale getirir. Yükleyicilerde güncelleştirmeleri zorlaştıran uzantı ve temel ürün bulunur. Her yükseltme işleminde, kod birleştirme ve paket oluşturma gereklidir. Bu işlemi basitleştirmek üzere uzantı paketleri artık kolay dağıtım ve yönetim için bileşenlere ayrılmıştır. Yeni yaklaşımla, uzantılar ve temel ürün yükleyicileri ayrılır ve kod birleştirme veya yeniden paketleme olmadan bağımsız olarak sunulup yükseltilebilir.|
| **Başka bir özellikle mi değiştirildi?**   | CSU uzantıları, POS uzantısı yükleyicileri, Donanım istasyonu uzantısı yükleyicileri |
| **Etkilenen ürün alanları**         | Dynamics 365 Commerce uzantısı ve dağıtım |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 10.0.21 sürümünden itibaren, RetailDeployablePackage'i LCS'de dağıtma desteği Ekim 2022'de kaldırılacaktır. |

Daha fazla bilgi için bkz:

+ [Commerce Bulut Ölçek Birimi (CSU) için ayrı bir paket oluşturma](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [Modern POS uzantı paketi oluşturma](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [POS'u yeni bir donanım cihazıyla tümleştirme](../dev-itpro/hardware-device-extension.md)
+ Kod örnekleri
    + [Bulut Ölçek Birimi](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [POS, CSU ve Donanım istasyonu](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>Retail SDK'da ModernPos.Sln ve CloudPOs.sln

ModernPos.sln, CloudPOs.sln, POS.Extension.csproj ve POS klasörünü kullanarak POS uzantısı geliştirme, 10.0.21 sürümünde kullanım dışı bırakılmıştır. Bundan sonra, POS uzantıları için POS bağımsız paketleme SDK'sini kullanın.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Retail SDK'nin önceki sürümlerinde, POS uzantıları varsa POS'un en son sürümüne güncelleştirmek için bir kod birleştirme ve yeniden paketleme işlemi gerekir. Kod birleştirme, zaman alan bir yükseltme işlemiydi ve depoda tam Retail SDK'yi tutmanız gerekiyordu. Ayrıca çekirdek POS.App projesini derlemeniz gerekiyordu. Bağımsız paketleme modelini kullandığınızda yalnızca uzantınızı korumanız gerekir. POS uzantılarının en son sürümüne güncelleştirme işlemi, projenizin tükettiği NuGet paketi sürümünü güncelleştirmek kadar kolaydır. Uzantılar bağımsız olarak dağıtılabilir ve hizmetler, uzantı yükleyicilerini kullanır. Temel POS ayrı olarak dağıtılıp korunabilir ve temel yükleyici veya kod ile kod birleştirme ya da yeniden paketleme gerekmez. |
| **Başka bir özellikle mi değiştirildi?**   | [POS bağımsız paketleme SDK'si](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Etkilenen ürün alanları**         | Dynamics 365 Commerce POS uzantısı ve dağıtımı |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 10.0.21 sürümünden itibaren, Retail SDK'de ModernPos.Sln, CloudPOs.sln ve POS.Extensons.csproj kullanan birleşik POS paketleri ve uzantı modeli desteği Ekim 2022'de kaldırılacaktır. |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Commerce 10.0.17 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="full-dataset-generation-interval-is-deprecated"></a>Tam veri kümesi oluşturma aralığı kullanım dışıdır

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Bu sürümden itibaren, Dynamics 365 Headquarters'daki **Commerce planlayıcı parametreleri** formunda, **Gün cinsinden tam veri kümesi oluşturma aralığı** alanı kullanım dışı olacaktır. Ayrıca, bu sürümden itibaren, değerin düzenlenememesi için alan görsel olarak kaldırılır. Bu, **0** değeri olarak kalır. |
| **Başka bir özellikle mi değiştirildi?**   | Hayır |
| **Etkilenen ürün alanları**         | Dynamics 365 Commerce |
| **Dağıtım seçeneği**              | Tümü|
| **Durum**                         | Kaldırıldı. Bu alanı kullanmayın veya içindeki değeri değiştirmeyin.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Commerce 10.0.15 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 için Internet Explorer 11 desteği kullanım dışı bırakılmıştır

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Aralık 2020 itibarıyla geçerli olmak üzere tüm Dynamics 365 ürünleri için Microsoft Internet Explorer 11 desteği kullanım dışı, bırakılacaktır ve Internet Explorer 11, Ağustos 2021'den sonra desteklenmeyecektir.<br><br>Bu, Internet Explorer 11 arabirimi aracılığıyla kullanılmak üzere tasarlanmış olan Dynamics 365 ürünlerini kullanan müşterileri etkileyecektir. Ağustos 2021'den sonra, Internet Explorer 11, bu tür Dynamics 365 ürünleri için desteklenmeyecektir. |
| **Başka bir özellikle mi değiştirildi?**   | Müşterilerin Microsoft Edge'e geçiş yapması önerilir.|
| **Etkilenen ürün alanları**         | Tüm Dynamics 365 ürünleri |
| **Dağıtım seçeneği**              | Tümü|
| **Durum**                         | Kaldırıldı. Internet Explorer 11 Ağustos 2021'den sonra desteklenmeyecektir.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Commerce 10.0.11 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler
### <a name="data-action-hooks"></a>Veri eylemi kancaları
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Veri eylemi kancaları özelliği performans sorunları nedeniyle kullanımdan kaldırıldı. |
| **Başka bir özellikle mi değiştirildi?**   | Veri eylem katmanındaki iş mantığını değiştirmek için [veri eylemi geçersiz kılmaları](../e-commerce-extensibility/data-action-overrides.md) kullanmanızı öneririz.|
| **Etkilenen ürün alanları**         | e-Ticaret genişletilebilirliği veri eylemleri |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kaldırıldı: 10.0.11 sürümü itibarıyla |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Visual Studio 2015 için Retail SDK desteği, msbuild 14.0 ve Retail SDK\Referans kitaplıklar ve araçlar
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Visual Studio 2015 için Retail SDK desteği kullanım dışı bırakıldı ve VS 2017, msbuild 15.0 desteğine güncelleştirildi; RetailSDK\Referanslar klasöründeki tüm referans kitaplıkları ve ticaret ara sunucu oluşturucu araçları uzantı modeli ve SDK yükseltme işlemini kolaylaştırmak için NuGet paketlerine taşındı.|
| **Başka bir özellikle mi değiştirildi?**   | Sisteminizi güncelleştirmek için [Retail SDK'yı Visual Studio 2015'den Visual Studio 2017'ye taşıma](../dev-itpro/retail-sdk/migrate-sdk.md) bölümündeki bilgileri izlemenizi öneririz. |
| **Etkilenen ürün alanları**         | Retail SDK uzantıları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kaldırıldı: 10.0.11 sürümü itibarıyla |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>IEdmModelExtender ve CommerceController kullanan Retail Server Uzantısı
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | IEdmModelExtender ve CommerceController kullanan Retail Server uzantısı, daha basşt uzantı modeli sağlamak amacıyla kullanım dışı bırakıldı. Yeni uygulamanın herhangi bir ek IEdmModelExtender sınıfı uygulaması olmadan yalnızca denetleyici sınıfı olacaktır. Bu, ayrıca belirli bir OData sürümüne bağımlılığı önler (OData sürümü güncelleştirilmişse uzantıları kesebilir.) |
| **Başka bir özellikle mi değiştirildi?**   |  NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) paketini içe aktararak IController sınıf uzantısı modelini kullanmanızı öneririz. |
| **Etkilenen ürün alanları**         | Retail server uzantıları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kaldırıldı: 10.0.11 sürümü itibarıyla |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>IHardwareStationController kullanan Hardware Station Uzantısı
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | IHardwareStationController kullanan Hardware Station uzantısı daha basit uzantı modeli sağlamak amacıyla kullanım dışı bırakıldı. Yeni uygulamanın, ek sınıf uygulaması olmadan yalnızca IController sınıfı olacaktır ve temel donanım istasyonu kitaplıklarına bağımlılığın engellenmesi amaçlanmıştır; önceki uzantının birden fazla kitaplığa başvurması gerekir.) |
| **Başka bir özellikle mi değiştirildi?**   | NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) paketini içe aktararak IController sınıf uzantısı modelini kullanmanız önerilir. |
| **Etkilenen ürün alanları**         | Hardware Station uzantıları |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanımdan kaldırıldı: 10.0.11 sürümü itibarıyla |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Commerce 10.0.10 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler
### <a name="pos-operation-803---picking-and-receiving"></a>POS işlemi 803 - Malzeme çekme ve teslim alma
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Yeni işlem tasarımı nedeniyle, malzeme çekme ve teslim alma işlemleri kullanımdan kaldırıldı. |
| **Başka bir özellikle mi değiştirildi?**   | Evet. Bunun yerine iki yeni POS işlemi sunuldu: gelen işlem (804) ve giden işlem (805).|
| **Etkilenen ürün alanları**         | Satış noktası (POS) uygulaması |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 10.0.10 sürümü itibarıyla, malzeme çekme ve teslim alma işlemi artık yeni özellik güncelleştirmesi almayacak. Gelecekteki sürümlerde bu işlem için yalnızca kritik hata düzeltmeleri yapılacak. Tüm kullanıcıların, uzun dönemli ürün oyl haritasının bir parçası olmaya devam edecek yeni [Gelen işlemler](../pos-inbound-inventory-operation.md) ve [Giden işlemler](../pos-outbound-inventory-operation.md) özelliğine geçiş yapması önerilir. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Commerce 10.0.7 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities ve GetAvailableInventoryNearby API'ları
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | GetProductAvailabilities ve GetAvailableInventoryNearby API'larının yerini almak üzere yeni optimize edilmiş API'lar oluşturuldu. |
| **Başka bir özellikle mi değiştirildi?**   | Evet: GetEstimatedAvailabilty ve GetEstimatedProductWarehouseAvailability API'ları ile değiştirildi. |
| **Etkilenen ürün alanları**         | e-Ticaret uygulaması SDK |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 10.0.7 sürümü itibarıyla, GetProductAvailabilities ve GetAvailableInventoryNearby için mühendislik yatırımlar yapılmayacaktır. E-ticaret dağıtımlarında bu API'ları kullanan kuruluşların yeni GetProductAvailabilities ve GetAvailableInventoryNearby API'larına geçiş yapması ve [En iyi duruma getirilmiş ürün kullanılabilirliği hesaplama özelliğini](../calculated-inventory-retail-channels.md) etkinleştirmesi gerekir.  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular
Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json) bakın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
