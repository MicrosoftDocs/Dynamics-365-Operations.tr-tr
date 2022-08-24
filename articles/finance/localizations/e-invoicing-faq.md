---
title: Elektronik faturalama SSS
description: Bu makalede, Elektronik faturalamayla ilgili sık sorulan sorular hakkında bilgi sağlanmaktadır.
author: gionoder
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.17
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: cf712c188e27deef4edfce7f5473fec4bb759bdf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285832"
---
# <a name="electronic-invoicing-faq"></a>Elektronik Faturalama ile ilgili SSS

[!include [banner](../includes/banner.md)]

Bu makalede, Elektronik Faturalama hizmetiyle ilgili sık sorulan soruların yanıtları yer almaktadır. Elektronik faturalama; Dynamics 365 Finance, Dynamics 365 Supply Chain Management ve Dynamics 365 Project Operations'daki mevcut elektronik faturalama özelliklerini genişletir. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Elektronik faturalama ile ilgili önemli olan nedir ve neden Kuruluşum için önemlidir?

Operasyonel karmaşıklık ve risk, kuruluşlar global olarak büyüdükçe ve bölgelerde ayak izlerini genişlettikçe artmaya devam eder. Sıkça değişiklik yapılan düzenlemelere uyum sağlamak ve uyumluluğu korumak artan bir zorluk sunar ve faturalama konusunda ayrı bir öneme sahiptir. Şirketler basılı belgelerle ve yoğun olarak elle yapılan işlemlerle çalışırken faturalama pahalı ve hataya açıktı.  

Kuruluşlar, maliyeti azaltmak ve uçtan uca işlemleri hızlandırmak için kağıt faturaları kullanmamaya başladı. Hükümetler, vergi dijitalleşmesinin anahtar bileşeni olarak giderek elektronik faturalamaya geçiyor. Hükümetler, kuruluşların gerçek zamanlı vergi bilgilerini vergi dairesine dijital olarak göndermelerini isteyerek vergi kaçırma ve manipülasyonunu en aza indirip sahtekarlığı azaltabilir. 

Dünya, kağıtsız belge işlemeye geçiyor ve elektronik faturalamayı uygulamayan müşteriler uyumluluk sorunları, gereksiz maliyetler ve rakiplerden geri kalma riskleriyle karşılaşabilir. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Finance, Supply Chain Management ve Project Operations zaten elektronik faturalama işlevi içermiyor mu? Bu bir müşteri olarak bana hangi değeri sağlar? 

Elektronik Faturalama, Finance, Supply Chain Management ve Project Operations içinde bulunan elektronik faturalama yeteneklerini geliştirir. Bu işlevler ayrıca en yeni elektronik faturalama standartlarına uymayı basitleştirilir ve elektronik fatura işlemede ve döviz kuru konusunda farklı coğrafi bölgeler için tutarlı deneyimler sağlar. Elektronik faturalama özellikleri aşağıdakiler dahil olmak üzere bir dizi avantaj sunar: 

   - Ülkeye/bölgeye özel gereksinimleri daha hızlı ve kolay şekilde benimseme.
   - E-faturalama çözümü uygulamaları standartlaştırma. 
   - Geliştirilmiş e-Fatura işleme izleme yeteneği.  
   - Değişen yasal gereksinimleri ve yerel iş uygulamalarıyla uyumlu olacak şekilde daha kolay bakım. 
   - Basitleştirilmiş çözüm paketi.
   - Daha hızlı döngü ile sonuçlanan büyük hacimlerde belge gönderme için ölçekleme yetenekleri.
   - Çözümlerinizi diğer şirketlerle paylaşma yeteneği.

## <a name="does-electronic-invoicing-service-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Elektronik Faturalama hizmeti, Finance, Supply Chain Management ve Project Operations'ın şirket içi yüklemelerini destekliyor mu? 

Geçerli platform şirket içi sürümünün kullanılmasına izin vermiyor ve gelecekte bunu destekleyecek bir plan içermiyor.

## <a name="does-electronic-invoicing-service-interface-with-the-vendor-import-automation-feature"></a>Elektronik Faturalama hizmeti, satıcı içe aktarma otomasyonu özelliğiyle arabirim oluşturuyor mu?

Hayır. Bu arabirim için planlar var, ancak planlı bir zaman çizelgesi yok. Planlandığında tarihler [Sürüm planlarında](/dynamics365/release-plans/) duyurulacak.

## <a name="how-does-electronic-invoicing-service-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Elektronik Faturalama hizmeti, dosya eklerini elektronik faturaya nasıl işler? SharePoint PDF dosyalarını XML dosyasına gömmek için bir sunucu gerekli mi?

Elektronik faturaya iliştirilmiş dosyalar bir XML öğesinde katıştırılmış ikili veri olarak işlenir. PDF dosyalarını katıştırmak için bir SharePoint sunucusu gerekmez, ancak ekin Finance, Supply Chain Management ve Project Operations belge yönetim sisteminde depolanması gerekir.

## <a name="is-electronic-invoicing-service-available-according-to-the-regulations-of-my-countryregion"></a>Elektronik Faturalama hizmeti ülke/bölge düzenlemelerine göre mi mevcuttur?

Elektronik Faturalama hizmeti, global olarak kullanılabilecek bir mikro hizmet platformudur.

Microsoft, işlevsel olarak Microsoft tarafından yerelleştirilmiş ülkeler için elektronik fatura biçimlerini ve tümleştirmeleri yayımlamayı planlamaktadır. Daha fazla bilgi için, [elektronik faturalama özelliklerinin kullanılabilirliği](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features) konusuna bakın.

Ülkeniz/bölgeniz için elektronik faturalama biçimi listelenmiyorsa, platform bu senaryoyu gelecekte desteklemeyi amaçlar. Elektronik faturalamanın sahip olduğu yapılandırma yeteneklerinden yararlanabilir ve elektronik faturalama formatını kendiniz yapılandırabilirsiniz veya kuruluşunuz için bunları yapılandırmak üzere bir ortak/ISV ile çalışabilirsiniz.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Dynamics 365 for Regulatory Services; Finance veya Supply Chain Management'a bağlı Human Resources veya Project Operations gibi yeni bir modül mü? Bunun için ekstra maliyetler var mı?

Dynamics 365 for Regulatory Services (RCS), Genelleştirme kaynaklarını yapılandırmak için bir bulut hizmetidir. RCS, Finance, Supply Chain Management ve Project Operations lisans sahipleri için ücretsizdir.

RCS kaydı için <https://marketing.configure.global.dynamics.com/> adresine gidin.

Daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing-service-or-just-turn-it-on-in-feature-management"></a>Elektronik Faturalama hizmetini elde etmek için kaydolmam gerekiyor mu yoksa Özellik yönetiminde etkinleştirmem yeterli mi?

Finance, Supply Chain Management ve Project Operations için lisansınız varsa, Elektronik faturalamaya kaydolmak için [elektronik faturalama eklentisi servis yönetimine başlarken](e-invoicing-get-started-service-administration.md) konusuna bakın.

## <a name="does-electronic-invoicing-service-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Elektronik Faturalama hizmeti katman 1 sanal makinelerle çalışıyor mu? Gerekli en düşük ortam nedir?

Elektronik Faturalama hizmeti ile tümleştirme için, Finance veya Supply Chain Management'ı barındıracak en az bir katman 2 sanal makine gerekir. Ortam planlama hakkında daha fazla bilgi için [ortam planlama](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) konusuna bakın.

## <a name="does-electronic-invoicing-service-have-a-test-mode-for-testing-invoice-submission"></a>Elektronik Faturalama hizmeti, fatura gönderimi test etmek için bir test moduna sahip mi?

Bu, yapılandırma tarafından sağlanabilir. Fatura gönderimini test etmek için, bir kullanıcı kabul testi (UAT) ortamından Finance veya Supply Chain Management'a bağlanabilir ve test faturalarını gönderebilirsiniz. Elektronik faturalama, test dijital sertifikalarının yapılandırılmasını destekler ve dijital onay gerektiren e-faturalar olduğunda, vergi yetkilileri tarafından yayımlanan test Web hizmetlerinden URL kurulumunu destekler.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Kullanıma hazır, ülkeye özel Elektronik Faturalama özellikleri hakkında herhangi bir belge var mı?

Evet. Elektronik Faturalama özelliklerinin kullanılabilirliği ve destekledikleri biçimler hakkında bilgi için, [elektronik faturalama özelliklerinin kullanılabilirliği](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features) konusuna bakın.

## <a name="does-the-electronic-invoicing-service-allow-a-legal-entity-in-finance-or-supply-chain-management-that-is-configured-for-a-specific-country-to-consume-electronic-invoicing-features-from-different-countryregions"></a>Elektronik Faturalama hizmeti, belirli bir ülke/bölgedeki elektronik faturalama özelliklerini tüketecek şekilde yapılandırılmış Finance veya Supply Chain Management'ta tüzel kişilere izin veriyor mu?

Evet. Elektronik faturalama özellikleri, tüzel kişiliğin ülkesinden bağımsız olarak iş belgesi gönderimlerini işlemek için kullanılabilir (aşağıdaki hususlar geçerliyse):

   - Oluşturulan iş belgesi, uygun belge modeli eşlemesi kullanıyor.
   - Elektronik faturalama özelliğinde yapılandırılan uygulanabilirlik kuralları ve iş belgesi eşleşiyor.

## <a name="does-the-electronic-invoicing-service-use-the-same-configuration-and-design-experience-provided-by-the-electronic-reporting-module-in-finance-and-supply-chain-management"></a>Elektronik Faturalama hizmeti, Finance ve Supply Chain Management'ta Elektronik raporlama modülü tarafından sağlanan aynı konfigürasyon ve tasarım deneyimini mi kullanıyor? 

Evet. Finance ve Supply Chain Management'taki Elektronik raporlama (ER) modülünde kullanılan tasarımcı araçlarının aynıları, veri modeli eşleme ve dosya biçimi konfigürasyonları oluşturmak ve yapılandırmak için kullanılır. Bu tasarımcı araçları, e-faturalama özelliklerinin yapılandırmasında kullanılan veri modeli eşlemesi ve dosya biçimi konfigürasyonları oluşturmak ve yapılandırmak için Regulatory Configuration Services'da (RCS) da kullanılır.

## <a name="can-the-applicability-rules-be-extended-and-configured-so-that-they-arent-tied-to-any-specific-parameter-such-as-a-legal-entity"></a>Uygulanabilirlik kuralları, tüzel kişilik gibi herhangi bir parametreye bağlı olmayacak şekilde genişletilip yapılandırılabilir mi?

Evet. Uygulanabilirlik kuralları tamamen yapılandırılabilir. Yan tümceler ekleyebilir veya kaldırabilir, mantık işlemleri oluşturabilir ve yan tümceleri gruplandırabilir ya da mevcut grupları bozabilirsiniz. Daha fazla bilgi için bkz. [Uygulanabilirlik kuralları](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#applicability-rules).

## <a name="does-the-electronic-invoicing-service-support-adding-other-er-format-configurations-to-generate-other-types-of-documents-does-it-support-sending-the-documents-electronically-to-customers-such-as-a-delivery-note"></a>Elektronik Faturalama hizmeti, farklı tür belgeleri oluşturmak için başka bir ER biçim konfigürasyonu eklemeyi destekliyor mu? Teslimat notu gibi belgelerin müşterilere elektronik olarak gönderilmesini destekliyor mu?

Dilediğiniz çıktı dosyaları oluşturmak için farklı ER biçim konfigürasyonları kullanabilirsiniz. Ancak, ER biçim konfigürasyonu; iş belgeleri oluşturmak üzere Finance veya Supply Chain Management'ta konfigüre edilmiş aynı ER faturası modeli eşleştirmesinden türetilmelidir. Çıktı dosyasını doğrudan bir EDI hareketi olarak müşteriye göndermek, kullanıma hazır olarak gelen Elektronik Faturalama tarafından desteklenmez.

## <a name="does-the-electronic-invoicing-service-support-exchanging-electronic-invoices-with-customers-does-it-support-configuring-different-invoice-formats-for-the-same-invoice"></a>Elektronik Faturalama hizmeti, müşterilerle elektronik fatura alışverişini destekliyor mu? Aynı fatura için farklı fatura biçimlerinin yapılandırılmasını destekliyor mu?

Satıcı elektronik faturalarını alma ve içe aktarma yeteneği yol haritamızda yer alıyor ancak elektronik faturaları müşterilere otomatik olarak gönderme işlemi şu anda desteklenmiyor.

## <a name="does-the-electronic-invoicing-service-extend-to-support-exchanging-edi-messages-with-other-companies"></a>Elektronik Faturalama hizmeti, başka şirketlerle EDI iletileri alışverişini destekliyor mu?

Elektronik Faturalama hizmetinin odağı, mevzuat uyumluluk gereksinimleri tarafından yönetilen elektronik fatura iletisi tipleri alışverişidir. Satıcı elektronik faturalarını alma ve içe aktarma yol haritamızda bulunuyor ancak elektronik fatura dosyalarının müşterilere gönderilmesi şu anda kullanıma hazır olarak gelen sürümde şu anda desteklenmemektedir (müşteriye elektronik faturanın göndermenin mevzuat tarafından zorunlu tutulduğu senaryolar dışında).

## <a name="does-the-electronic-invoicing-service-support-importing-or-merging-customizations-made-in-the-er-format-configurations-from-the-legacy-electronic-invoicing-feature"></a>Elektronik faturalama hizmeti, eski Elektronik faturalama özelliğinden, ER biçim konfigürasyonlarında yapılan özelleştirmeleri içe aktarma veya birleştirmeyi destekliyor mu?

Elektronik Faturalama hizmetinde ER biçim konfigürasyonlarını yeniden kullanabilirsiniz. Ancak, ER biçim konfigürasyonu; iş belgeleri oluşturmak üzere Finance veya Supply Chain Management'ta konfigüre edilmiş ve elektrik fatura özelliğinin kullanılmak üzere tasarlandığı aynı ER faturası modeli eşleştirmesinden türetilmelidir.

## <a name="does-the-electronic-invoicing-service-support-issuing-electronic-invoices-from-custom-made-tables-if-so-how-do-you-create-the-er-data-model-configurations-for-these-new-tables-and-entities"></a>Elektronik Faturalama hizmeti, özel tablolardan müşterilere elektronik fatura kesmeyi destekliyor mu? Destekliyorsa, bu yeni tablolar ve varlıklar için ER veri modeli konfigürasyonları nasıl oluşturulur?

Evet. Ancak, fatura modeli eşlemesinin özelleştirilmesine ve özel hazırlanmış tablolara gerekli referansların eklenmesini gerektirir veya karmaşıklığa bağlı olarak yeni bir fatura modeli eşlemesi oluşturulmasını gerektirir.

## <a name="does-the-electronic-invoicing-service-support-different-web-service-endpoints"></a>Elektronik Faturalama hizmeti, farklı web servis uç noktalarını destekliyor mu?

Elektronik Faturalama hizmeti, farklı web servis uç noktalarını destekler. REST web servisleriyle konfigüre edilebilir tümleştirmeyi veya birçok parametreleştirilmiş ülkeye özel web servisi tümleştirmelerini kullanabilirsiniz. Farklı konfigürasyon sürümleri kullanan aynı web servisleri ve API'ler için ayrı son noktalar yapılandırılabilir. Daha fazla bilgi için bkz. [Eyleme göre parametreler listesi](e-invoicing-setup.md#list-of-parameters-by-action).

## <a name="is-electronic-invoicing-integrated-with-the-various-invoice-operators-apis-from-the-nordic-countries-or-should-that-be-handled-on-a-case-by-case-basis"></a>Elektronik Faturalama hizmeti, İskandinavya ülkelerinden alınan çeşitli fatura operatörlerinin API'leri ile tümleştirilmiş midir yoksa bu durum özel olarak olay bazında mı ele alınmalıdır?

Microsoft, elektronik faturalama özelliklerini kullanarak kullanıma hazır tümleştirmeler sağlamaya yönelik işlevsel kapsamını sürekli olarak genişletmektedir. Desteklenen biçimler ve tümleştirmeler hakkında daha fazla bilgi için bkz. [Elektronik faturalama özelliklerinin kullanılabilirliği](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Aradığınız yanıtı bulamadıysanız <D365EInvoicePreview@microsoft.com> adresine e-posta göndererek sorunuzu ürün geliştirme ekibine sorun. Sizinle iletişime geçecek veya bu SSS'nin kapsamını geliştireceğiz.
