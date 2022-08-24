---
title: Dynamics 365 Commerce 10.0.29 önizlemesi (Ekim 2022)
description: Bu makalede, Microsoft Dynamics 365 Commerce 10.0.29'taki yeni veya değişen özellikler açıklanmaktadır.
author: josaw1
ms.date: 08/02/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c1f85fcd8f79106a3af93489d3bef608b9840bf3
ms.sourcegitcommit: 91f58a9863f4e8f30ac787c2a9771c1ff6a05f72
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/03/2022
ms.locfileid: "9224251"
---
# <a name="preview-of-dynamics-365-commerce-10029-october-2022"></a>Dynamics 365 Commerce 10.0.29 önizlemesi (Ekim 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce önizleme sürümü 10.0.29'daki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.1326 derleme numarasına sahiptir ve aşağıdaki planlamaya göre kullanıma sunulmuştur:

- **Sürümün önizlemesi:** Ağustos 2022
- **Sürüm genel kullanılabilirliği (kendi kendini güncelleştirme):** Eylül 2022
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Ekim 2022

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. Bu makale ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren |
|---------|------------------|----------------|--------------| 
| B2B | [Kanallar arasında satış sözleşmesi desteğini etkinleştirme](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-b2b-sales-agreement-contract-based-pricing) | Bu özellik, işletmeler arası (B2B) satıcı kuruluşlarının, kendi alıcıları için sözleşme tabanlı fiyatlandırma tanımlamak üzere Commerce Headquarters'da satış anlaşmalarını kullanmasını sağlar. Bir B2B alıcısı e-ticaret web sitesinde alışveriş yaparken, B2B alıcı kuruluşu için yapılandırılan sözleşme tabanlı fiyatlandırma, tüm ürün bulma, satınalma ve ödeme deneyimine otomatik olarak uygulanır. | Özellik yönetimi<p>*Ticari kanallar arasında satış sözleşmesi desteği* |
| Customer Service | [Dynamics 365 Customer Service için Çok Yönlü Kanal ile Müşteri Hizmetlerini Etkinleştirme](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/chat-dynamics-365-commerce-omnichannel-customer-service) | Birinci sınıf müşteri desteği deneyimi, tüketiciler için kişiselleştirilmiş ve keyifli ticari deneyim sağlamak için çok önemlidir. Şu anda fiziksel mağazalar, çevrimiçi kanallar ve sosyal içerik kanalları gibi birden fazla ticari temas noktası mevcuttur. Tüketiciler tüm bu temas noktalarında kişiselleştirilmiş destek deneyimi almayı bekler. Bu özellik, Dynamics 365 Customer Service için Çok Yönlü Kanal ile tümleştirme yoluyla alışveriş sepetinin satışa dönüşme oranını artırmanıza, müşterilerle kişiselleştirilmiş etkileşimi artırmanıza ve müşteri hizmetlerini geliştirmenize yardımcı olur. | Yönetici/yetkililer tarafından etkinleştirildi |
| E-ticaret | E-ticarette ürün karşılaştırması desteği | Alışverişçilerin, kendi başlarına doğru satın alma kararı verecek şekilde geniş bir kategori yelpazesi üzerinde ürün karşılaştırmalarını sağlayın. Bu özellik, işletmeden tüketiciye (B2C) ve B2B siteleri için kullanılabilir. | Site oluşturucu | 
| Hediye kartları | Şirketler arası veri paylaşımı için perakende hediye kartı tabloları desteği | Dynamics headquarters, Dynamics mimarisinde belirli tablolar için şirketler arası veri paylaşımını etkinleştirme yeteneğini destekler. Bu özellikte Dynamics 365 Commerce, perakende hediye kartı tabloları için şirketler arası veri paylaşımı desteği ekler. Bu nedenle, bir şirketteki hediye kartının verileri artık ortamdaki başka bir şirket tarafından çoğaltılabilecek. Kaynak şirket hediye kartı tablosunda yapılan değişiklikler mükerrer şirket hediye kartı tablosu ile paylaşılır. | Geliştiriciler |
| Performans | "Müşteri düzenle" senaryoları için RTS bağımlılığını kaldırma | Yüksek kullanılabilirlik ve yüksek performans, satış noktası (POS) ve e-ticaret kanalları için varsayılan beklentilerdir. Bu beklentileri karşılamanıza yardımcı olmak için, Dynamics 365 Commerce kanallarının artık müşteri bilgileri düzenlendiğinde Commerce Headquarters ile gerçek zamanlı iletişime dayanması gerekmez. Zaman uyumsuz ve zaman uyumsuz olmayan müşteriler için müşteri bilgilerini zaman uyumsuz olarak düzenleme yeteneği, Commerce Headquarters'a yapılan gerçek zamanlı çağrıları azaltmaya yardımcı olabilir. | Yönetici/yetkililer tarafından etkinleştirildi |

## <a name="feature-state-changes-in-this-release"></a>Bu sürümdeki özellik durumu değişiklikleri

Aşağıdaki tabloda, 10.0.29 sürümünde zorunlu veya varsayılan olarak açık hale gelen özellikler listelenmektedir. 10.0.29 sürümüne güncelleştirme yaptığınızda, bu özelliklerin tümü sisteminiz için otomatik olarak açılır. Zorunlu özellikler kapatılamaz ancak varsayılan olarak açık olan özellikler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanılarak kapatılabilir.

Tablo ayrıca, daha önce genel önizlemede bulunan, ancak 10.0.29 sürümünde genel kullanıma sunulacak şekilde değiştirilen özellikleri de listeler, bu da özelliklerin artık üretim ortamlarında kullanım için önerildiği anlamına gelir. Bu değişiklik, özelliklerin artık üretim ortamlarında kullanılması için önerildiğini belirtir. Aksi belirtilmedikçe varsayılan olarak, bu özellikler kapalıdır. Dolayısıyla, bu özellikleri kullanmak istiyorsanız etkinleştirmek için [Özellik yönetimini](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanmanız gerekir.

| Özellik | Başlık | Yeni özellik durumu |
| --- | --- | --- |
| BrazilRetailLocalizationFeature_BR |(Brezilya) Brezilya'ya özgü Ticaret işlevi | Varsayılan olarak açık |
| RetailAdvancedGTETaxAdjustmentFeature | (Hindistan) Retail POS'taki perakende hareketleri için hesaplanan GST'yi perakende ekstrelerine uygula | Varsayılan olarak açık |
| RetailChronologicalInvoicePostingFeature_IT | (İtalya) Kronolojik sıra olmadan deftere nakledilen perakende faturalarını etkinleştir | Varsayılan olarak açık |
| RetailDiscountWithoutTaxAdjustingFeature_MX | (Meksika) Perakende CFDI Genelde iskonto ayarlama | Varsayılan olarak açık |
| RetailFiscalIntegrationConfigurationEnhancementFeature | Mali tümleştirme teknik profil geçersiz kılma işlemleri | Varsayılan olarak açık |
| RetailFiscalIntegrationConnectorLocationFeature | POS kayıtlarından doğrudan mali tümleştirme | Varsayılan olarak açık |
| RetailFiscalIntegrationLocalStorageBackupEnableFeature | Mali tümleştirme yerel depolama yedeklemesi | Varsayılan olarak açık |
| RetailFiscalIntegrationPostponeFiscalRegistrationFeature | Belgelerin ertelenen kaydı | Varsayılan olarak açık |
| RetailFiscalIntegrationRegistrationProcessTerminalExceptionFeature | POS Kayıtlarının Mali Kayıt Durumu | Varsayılan olarak açık |
| RetailGSTInvoiceAddressTaxCalculationFeature_IN | (Hindistan) E-ticaret siparişleri için GST'yi fatura adresine göre hesapla | Varsayılan olarak açık |
| RetailInvoicesDefaultSalesDocumentStatusFeature_PL | (Polonya) Perakende faturaları için varsayılan satış belgesi durumu | Varsayılan olarak açık |
| RetailRecalculateRoundingOfTaxBaseAmountsFeature_MX | (Meksika) Retail CFDI Küresel'deki vergi tabanı tutarları için yuvarlama yeniden hesaplaması. | Varsayılan olarak açık |
| RetailSupplementaryInvoiceFeature | Perakende mağazalarında tamamlanan peşin hareketler için tamamlayıcı faturaları etkinleştir | Varsayılan olarak açık |
| RetailInventoryBufferAndInventoryLevelEnableFeature   |  Stok arabelleklerini ve stok düzeylerini etkinleştir    |  Varsayılan olarak açık|
|RetailInboundOutboundInventoryValidationFeature|   POS gelen ve giden stok işleminde doğrulamayı etkinleştir   |   Varsayılan olarak açık   |
|  RetailInventoryChannelCalculationConsolidationFeature    |  Gelişmiş e-Ticaret kanal tarafından stok hesaplama mantığı |   Varsayılan olarak açık   |
|RetailInventoryAdjustmentsInPointOfSaleFeature|    Satış noktasındaki stok düzeltmeleri   |  Varsayılan olarak açık  |
| RetailMultiplePickupDeliveryModeFeature |  Birden fazla teslim alma teslimat modu desteği     |   Zorunlu    |
|  RetailProductAvailabilityOptimizationFeature |   Optimize edilmiş ürün kullanılabilirliği hesaplaması  |  Zorunlu |
|   RetailPricingDataManagerV2Feature   |   Commerce fiyatlandırma altyapısı için performansı iyileştir |   Zorunlu |
|  RetailPricingPreventUnintendedRecalculationFeature   | Ticaret siparişleri için istenmeyen fiyat hesaplamalarını engelle    |  Zorunlu  |
| RetailTeamsIntegration    |   Microsoft Teams tümleştirmesini etkinleştir| Zorunlu   |  
| ConsumerEFDSyncProcessFeature_BR | (Brezilya) NFC-e zaman uyumlu işleme | Varsayılan olarak açık |
| RetailFiscalIntegrationInternalAndExternalServicesEnableFeature | Mali tümleştirme çerçevesinde dahili ve harici bağlayıcılar için destek | Zorunlu |
| RetailTaxRegistrationIdEnableFeature_BR | (Brezilya) Vergi sicil numaralarına göre Retail POS müşterileri ara | Zorunlu |
| RetailTaxRegistrationIdEnableFeature_IN | (Hindistan) Vergi sicil numaralarına göre Retail POS müşterileri ara | Zorunlu |
| RetailTaxRegistrationIdEnableFeature_IT | (İtalya) Retail POS'ta müşteri bilgileri yönetimi | Zorunlu |
| RetailTaxRegistrationIdEnableFeature_PL | (Polonya) Retail POS'ta müşteri bilgileri yönetimi | Zorunlu |
| RetailUpdateReturnOriginalTransactionIdGlobalEnableFeature_IN | (Hindistan için Perakende GST) Orijinal faturalara referansları olan alacak dekontlarını güncelleştir | Zorunlu |
| RetailUserDefinedCertificateProfileFeature | Perakende mağazaları için kullanıcı tarafından tanımlanmış sertifika profilleri | Zorunlu |
  

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finans ve Operasyon uygulamaları için Platform güncelleştirmeleri

Microsoft Dynamics 365 Commerce 10.0.29 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finans ve Operasyon uygulamalarının 10.0.29 sürümü için platform güncelleştirmeleri (Ekim 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). 

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.29 sürümünün parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [KB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559&dbType=3&qc=ec3e3846199f5d3a27a0c4949e3902ffdbc87560f0cf928c4838b3bdd421633c) görüntüleyin. 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 2 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 2 planına](/dynamics365-release-plan/2022wave2/) göz atın. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-features"></a>Kaldırılan ve kullanım dışı olan özellikler

[Dynamics 365 Commerce'teki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-commerce.md) makalesi, Commerce için kaldırılmış veya kullanım dışı bırakılmış özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Commerce'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-commerce.md) makalesinde duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
