---
title: Dynamics 365 Commerce'te kaldırılan veya kullanım dışı bırakılan özellikler
description: Bu makale Dynamics 365 Commerce'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: josaw1
ms.date: 07/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 541e21999884a2d51b27009d72a2f8bc9084557f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287636"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Dynamics 365 Commerce'te kaldırılan veya kullanım dışı bırakılan özellikler

[!include [banner](../includes/banner.md)]

Bu makale Dynamics 365 Commerce'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır. 

> [!NOTE]
> Finans ve operasyon uygulamalarındaki nesneler hakkında ayrıntılı bilgiye [Teknik referans raporları](/dynamics/s-e/) altından ulaşabilirsiniz. Finans ve operasyon uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="feature-deprecation-effective-july-2022"></a>Temmuz 2022'den itibaren geçerli olmak üzere özellik kullanımdan kaldırma bildirimi

### <a name="commerce-analytics-preview"></a>Commerce analizleri (Önizleme)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Dynamics 365 Commerce ekibi, Ticari analiz (Önizleme) özelliğinin kullanımını ve alımını analiz etti ve özelliğin genel kullanılabilirliği konusunda artık ilerlememe kararı aldı.   |
| **Başka bir özellikle mi değiştirildi?**   | Bu aşamada, Ticari analiz (Önizleme) başka bir özellik veya çözümle değiştirilmeyecektir. Finans ve operasyon uygulamalarındaki ham işlemlerin ve ana verilerin Azure Data Lake'e dışa aktarılması, [Finans ve operasyon uygulamalarında Data Lake öğesine dışa aktarma](../../fin-ops-core/dev-itpro/data-entities/finance-data-azure-data-lake.md) bölümünde açıklandığı gibi kullanılabilir olmaya devam eder. İş ortakları ve müşteriler, iş gereksinimlerine ilişkin amaçlanan analiz raporları yazmak için bu veri akışını geliştirebilir.
| **Etkilenen ürün alanları**         | Commerce analizleri (Önizleme) |
| **Dağıtım seçeneği**              | Tümü |
| **Çalıştırma Durumu**                         | Bu özelliği 30 Ağustos 2022 tarihine kadar devre dışı bırakmak istiyorsunuz.  Bu tarihten itibaren Ticari analiz (Önizleme) tarafından sağlanan geçerli Power BI raporlarda herhangi bir yenileme yapılmayacaktır.     |


## <a name="features-removed-or-deprecated-in-the-commerce-10025-release"></a>Commerce 10.0.25 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="modern-point-of-sale-mpos"></a>Modern Satış Noktası (MPOS)

Modern Satış Noktası (MPOS) uygulaması, Commerce sürüm 10.0.25'te kullanımdan kalkacaktır ve bunun yerini Store Commerce uygulaması alacaktır.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Mağaza içi uygulamalar, Dynamics 365 Commerce çok kanallı sunumunun kenar taşı. Modern ve akıllı depolama deneyimlerinden sürekli olarak yenilik yapma ve çözümlerimizi daha iyi modernize, Windows'ta varolan yerleşik uygulamalarımız ile BT işlemlerini ve kullanıcı deneyimlerini önemli ölçüde artıran yeni değişiklikler sağlıyor. Yeni Store Commerce uygulaması, varolan MPOS'nin teknolojisini yükseltir. Windows platformunda gelişmiş performans, güvenilirlik ve uzun süreli destek sağlar ve uygulamanın her güncelleştirmeyle yeniden paketliğinin gerekli olduğunu ortadan kaldırır. |
| **Başka bir özellikle mi değiştirildi?**   |  [Store Commerce](../dev-itpro/store-commerce.md) |
| **Etkilenen ürün alanları**         | Modern Satış Noktası |
| **Dağıtım seçeneği**              | Tümü |
| **Çalıştırma Durumu**                         | Kullanım dışı: Commerce sürüm 10.0.25 ile, LCS sanal makineleri (VM'ler) aracılığıyla gönderilen MPOS yükleyicisi, Ekim 2023'te kaldırılacak. |

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
| **Durum**                         | Kullanım dışı: 10.0.21 sürümünden itibaren LCS VM'leri aracılığıyla gönderilen SDK, Ekim 2023'te kaldırılacaktır. |

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

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>Retail SDK'da ModernPos.Sln ve CloudPos.sln

ModernPos.sln, CloudPos.sln, POS.Extension.csproj ve POS klasörünü kullanarak POS uzantısı geliştirme, 10.0.21 sürümünde kullanım dışı bırakılmıştır. Bundan sonra, POS uzantıları için POS bağımsız paketleme SDK'sini kullanın.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Retail SDK'nin önceki sürümlerinde, POS uzantıları varsa POS'un en son sürümüne güncelleştirmek için bir kod birleştirme ve yeniden paketleme işlemi gerekir. Kod birleştirme, zaman alan bir yükseltme işlemiydi ve depoda tam Retail SDK'yi tutmanız gerekiyordu. Ayrıca çekirdek POS.App projesini derlemeniz gerekiyordu. Bağımsız paketleme modelini kullandığınızda yalnızca uzantınızı korumanız gerekir. POS uzantılarının en son sürümüne güncelleştirme işlemi, projenizin tükettiği NuGet paketi sürümünü güncelleştirmek kadar kolaydır. Uzantılar bağımsız olarak dağıtılabilir ve hizmetler, uzantı yükleyicilerini kullanır. Temel POS ayrı olarak dağıtılıp korunabilir ve temel yükleyici veya kod ile kod birleştirme ya da yeniden paketleme gerekmez. |
| **Başka bir özellikle mi değiştirildi?**   | [POS bağımsız paketleme SDK'si](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Etkilenen ürün alanları**         | Dynamics 365 Commerce POS uzantısı ve dağıtımı |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanım dışı: 10.0.21 sürümünden itibaren, Retail SDK'de ModernPos.Sln, CloudPOs.sln ve POS.Extensons.csproj kullanan birleşik POS paketleri ve uzantı modeli desteği Ekim 2023'te kaldırılacaktır. |

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
| **Başka bir özellikle mi değiştirildi?**   | Sisteminizi güncelleştirmek için [Retail SDK'yı Visual Studio 2015'ten Visual Studio 2017'ye taşıma](../dev-itpro/retail-sdk/migrate-sdk.md) bölümündeki bilgileri izlemenizi öneririz. |
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

