---
title: Elektronik faturalama SSS
description: Bu konu, elektronik faturalamayla ilgili sık sorulan sorular hakkında bilgi sağlar.
author: gionoder
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 41cddcdad5043ec314a94dda67f4f2e9de406cac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840184"
---
# <a name="electronic-invoicing-faq"></a>Elektronik faturalama SSS

[!include [banner](../includes/banner.md)]

Bu konu, elektronik faturalamayla ilgili sık sorulan soruların yanıtlarını sağlar. Elektronik faturalama, Dynamics 365 Finance, Dynamics 365 Supply Chain Management ve Dynamics 365 Project Operations'da varolan elektronik faturalama yeteneklerini genişletir. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Elektronik faturalama ile ilgili önemli olan nedir ve neden Kuruluşum için önemlidir?

Operasyonel karmaşıklık ve risk, kuruluşlar global olarak büyüdükçe ve bölgelerde ayak izlerini genişlettikçe artmaya devam eder. Sıkça değişiklik yapılan düzenlemelere uyum sağlamak ve uyumluluğu korumak artan bir zorluk sunar ve faturalama konusunda ayrı bir öneme sahiptir. Şirketler basılı belgelerle ve yoğun olarak elle yapılan işlemlerle çalışırken faturalama pahalı ve hataya açıktı.  

Kuruluşlar, maliyeti azaltmak ve uçtan uca işlemleri hızlandırmak için kağıt faturaları kullanmamaya başladı. Hükümetler, vergi dijitalleşmesinin anahtar bileşeni olarak giderek elektronik faturalamaya geçiyor. Hükümetler, kuruluşların gerçek zamanlı vergi bilgilerini vergi dairesine dijital olarak göndermelerini isteyerek vergi kaçırma ve manipülasyonunu en aza indirip sahtekarlığı azaltabilir. 

Dünya, kağıtsız belge işlemeye geçiyor ve elektronik faturalamayı uygulamayan müşteriler uyumluluk sorunları, gereksiz maliyetler ve rakiplerden geri kalma riskleriyle karşılaşabilir. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Finance, Supply Chain Management ve Project Operations zaten elektronik faturalama işlevi içermiyor mu? Bu bir müşteri olarak bana hangi değeri sağlar? 

Elektronik faturalama, Finance, Supply Chain Management ve Project Operations içinde bulunan elektronik faturalama yeteneklerini geliştirir. Bu işlevler ayrıca en yeni elektronik faturalama standartlarına uymayı basitleştirilir ve elektronik fatura işlemede ve döviz kuru konusunda farklı coğrafi bölgeler için tutarlı deneyimler sağlar. Elektronik faturalama özellikleri aşağıdakiler dahil olmak üzere bir dizi avantaj sunar: 

   - Ülkeye/bölgeye özel gereksinimleri daha hızlı ve kolay şekilde benimseme.
   - E-faturalama çözümü uygulamaları standartlaştırma. 
   - Geliştirilmiş e-Fatura işleme izleme yeteneği.  
   - Değişen yasal gereksinimleri ve yerel iş uygulamalarıyla uyumlu olacak şekilde daha kolay bakım. 
   - Basitleştirilmiş çözüm paketi.
   - Daha hızlı döngü ile sonuçlanan büyük hacimlerde belge gönderme için ölçekleme yetenekleri.
   - Çözümlerinizi diğer şirketlerle paylaşma yeteneği.

## <a name="does-electronic-invoicing-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Elektronik faturalama, Finance, Supply Chain Management ve Project Operations'ın şirket içi yüklemelerini destekliyor mu? 

Geçerli platform şirket içi sürümünün kullanılmasına izin vermiyor ve gelecekte bunu destekleyecek bir plan içermiyor.

## <a name="does-electronic-invoicing-interface-with-the-vendor-import-automation-feature"></a>Elektronik faturalama, satıcı içe aktarma otomasyonu özelliğiyle arabirim oluşturuyor mu?

Hayır. Bu arabirim için planlar var, ancak planlı bir zaman çizelgesi yok. Planlandığında tarihler [Sürüm planlarında](https://docs.microsoft.com/dynamics365/release-plans/) duyurulacak.

## <a name="how-does-electronic-invoicing-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Elektronik faturalama, dosya eklerini elektronik faturaya nasıl işler? SharePoint PDF dosyalarını XML dosyasına gömmek için bir sunucu gerekli mi?

Elektronik faturaya iliştirilmiş dosyalar bir XML öğesinde katıştırılmış ikili veri olarak işlenir. PDF dosyalarını katıştırmak için bir SharePoint sunucusu gerekmez, ancak ekin Finance, Supply Chain Management ve Project Operations belge yönetim sisteminde depolanması gerekir.

## <a name="is-electronic-invoicing-available-according-to-the-regulations-of-my-countryregion"></a>Elektronik faturalama ülke/bölge düzenlemelerine göre mi mevcuttur?

Elektronik faturalama, global olarak kullanılabilecek bir mikro hizmet platformudur.

Microsoft, işlevsel olarak Microsoft tarafından yerelleştirilmiş ülkeler için elektronik fatura biçimlerini ve tümleştirmeleri yayımlamayı planlamaktadır. Daha fazla bilgi için, [elektronik faturalama özelliklerinin kullanılabilirliği](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features) konusuna bakın.

Ülkeniz/bölgeniz için elektronik faturalama biçimi listelenmiyorsa, platform bu senaryoyu gelecekte desteklemeyi amaçlar. Elektronik faturalamanın sahip olduğu yapılandırma yeteneklerinden yararlanabilir ve elektronik faturalama formatını kendiniz yapılandırabilirsiniz veya kuruluşunuz için bunları yapılandırmak üzere bir ortak/ISV ile çalışabilirsiniz.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Dynamics 365 for Regulatory Services; Finance veya Supply Chain Management'a bağlı Human Resources veya Project Operations gibi yeni bir modül mü? Bunun için ekstra maliyetler var mı?

Dynamics 365 for Regulatory Services (RCS), Genelleştirme kaynaklarını yapılandırmak için bir bulut hizmetidir. RCS, Finance, Supply Chain Management ve Project Operations lisans sahipleri için ücretsizdir.

RCS kaydı için <https://marketing.configure.global.dynamics.com/> adresine gidin.

Daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing--or-just-turn-it-on-in-feature-management"></a>Elektronik faturalamayı elde etmek için kaydolmam gerekiyor mu yoksa Özellik yönetiminde etkinleştirmem yeterli mi?

Finance, Supply Chain Management ve Project Operations için lisansınız varsa, Elektronik faturalamaya kaydolmak için [elektronik faturalama eklentisi servis yönetimine başlarken](e-invoicing-get-started-service-administration.md) konusuna bakın.

## <a name="does-electronic-invoicing-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Elektronik faturalama katman 1 sanal makinelerle çalışıyor mu? Gerekli en düşük ortam nedir?

Elektronik faturalama ile tümleştirme için, Finance veya Supply Chain Management'ı barındıracak en az bir katman 2 sanal makine gerekir. Ortam planlama hakkında daha fazla bilgi için [ortam planlama](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) konusuna bakın.

## <a name="does-electronic-invoicing-have-a-test-mode-for-testing-invoice-submission"></a>Elektronik faturalama, fatura gönderimi test etmek için bir test moduna sahip mi?

Bu, yapılandırma tarafından sağlanabilir. Fatura gönderimini test etmek için, bir kullanıcı kabul testi (UAT) ortamından Finance veya Supply Chain Management'a bağlanabilir ve test faturalarını gönderebilirsiniz. Elektronik faturalama, test dijital sertifikalarının yapılandırılmasını destekler ve dijital onay gerektiren e-faturalar olduğunda, vergi yetkilileri tarafından yayımlanan test Web hizmetlerinden URL kurulumunu destekler.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Kullanıma hazır, ülkeye özel elektronik faturalama özellikleri hakkında herhangi bir belge var mı?

Evet. Elektronik faturalama özelliklerinin kullanılabilirliği ve destekledikleri biçimler hakkında bilgi için, [elektronik faturalama özelliklerinin kullanılabilirliği](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features) konusuna bakın.

> [!NOTE] 
> Aradığınız yanıtı bulamadıysanız <D365EInvoicePreview@microsoft.com> adresine e-posta göndererek sorunuzu ürün geliştirme ekibine sorun. Sizinle iletişime geçecek veya bu SSS'nin kapsamını geliştireceğiz.
