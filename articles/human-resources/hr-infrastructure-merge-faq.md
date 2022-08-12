---
title: Dynamics 365 Human Resources altyapı birleştirme hakkında SSS
description: Bu makalede, Microsoft Dynamics 365 Human Resources ile finans ve operasyon uygulamaları için altyapı birleştirme hakkında sık sorulan sorular yanıtlanmaktadır.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fd71d728f9c97dc9e2c44a7e7a0e773be891b818
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203214"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources altyapı birleştirme hakkında SSS

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Dynamics 365 Human Resources nedir?

Microsoft Dynamics 365 Human Resources, İK ekiplerinin kurumsal çevikliği artırmasına, personel deneyimini dönüştürmelerine ve İK programlarını optimize ederek çalışanların ve işletmenin gelişebileceği bir iş yeri oluşturmasına yardımcı olan araçlar sağlamaktadır. Dynamics 365 Human Resources hakkında daha fazla bilgi edinmek için bkz. [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Personel deneyimlerini dönüştürün.** Bağlılığı ve büyümeyi teşvik eden bağlantılı self servis deneyimler aracılığıyla yöneticileri ve personeli güçlendirerek en iyi performans gösterenleri elde tutun.
- **İK programlarını iyileştirin.** Operasyon maliyetlerini azaltın ve insanlar merkezli izin ve devamsızlık, zaman, kazanç ve ücret yönetimi programları oluşturun.
- **Kurumsal çevikliği artırın.** Kişi verilerini merkezileştirmek ve Dynamics 365 Human Resources'ı kolayca genişletmek için Dataverse ve Microsoft Power Platform kullanarak İK'nın işletmenin ihtiyaç duyduğu beceriyle çalışmasını sağlayın.
- **İşgücü hakkındaki öngörüleri keşfedin.** Herhangi bir cihazda erişilebilen zengin panolarda kişi verilerini analiz etme ve görselleştirme özelliği ile veri odaklı kararlar verin.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Altyapı birleştirmenin değeri ve avantajları

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Dynamics 365 Human Resources altyapı birleştirme nedir?

Dynamics 365'te şu anda iki farklı altyapıda üzerinde iki ayrı İK özelliği seti bulunmaktadır:

- **Dynamics 365 Human Resources**: Bağımsız bir altyapı üzerinde çalışan bağımsız bir uygulama. Bu uygulama başlatıldığında, altyapı diğer Dynamics 365 operasyon uygulamalarından ayrıldı. Müşterilerimiz bu uygulamayı kurumsal çevikliği artırmak, İK programlarını optimize etmek, personel deneyimlerini dönüştürmek ve işgücü içgörüleri elde etmek için kullanır.
- **HR modülü**: Daha önce Unified Operations lisanslama stok tutma biriminin (SKU) bir parçası olan eski bir özellik seti. HR modülü, tüm operasyon uygulamalarında aynı olan finans ve operasyon altyapısında çalışır. Bu uygulamalar, Dynamics 365 Finance, Dynamics 365 Project Operations ve Dynamics 365 Supply Chain Management içerir. Müşteriler, HR özelliklerini Dynamics 365 Finance veya Dynamics 365 Supply Chain Management'ın bir parçası olarak aldı.

Son üç yılda, Microsoft, İK modülüne yeni bir özellik veya geliştirme eklemedi. Bunun yerine, yol haritası yatırımlarımız Dynamics 365 Human Resources uygulamasına yoğunlaştı.

Bu iki yetenek setini aynı altyapı üzerinde bir araya getirerek müşterilerin aşağıdaki avantajları elde etmelerine yardımcı olacağız:

- Dynamics 365 Human Resources'na son üç yılda eklenen geliştirilmiş izin ve devamsızlık, kazanç yönetimi ve raporlama gibi geliştirmeler.
- Microsoft Power Platform ile geliştirilmiş genişletilebilirlik ve sayfaları kişiselleştirmek için iş mantığını genişletme özelliği.
- Uygulama yaşam döngüsü yönetimi (ALM), yaşam döngüsü hizmetleri, coğrafi kullanılabilirlik ve daha fazlası açısından tutarlı olan geliştirilmiş dağıtım, güncelleme ve bakım.
- Mühendislik ekibimiz paylaşılan hizmetleri, araçları ve azaltılmış platform maliyetlerini kullandıkça, daha fazla teknolojik yenilik.

Bu geçiş, şu anda Dynamics 365 Human Resources veya eski İK modülünü kullanan müşterileri etkileyecek.

## <a name="glossary-of-terms-used-in-this-faq"></a>Bu SSS bölümünde kullanılan terimler sözlüğü

- **Dynamics 365 Human Resources**: Pazar için İK özellikleri sunan şimdiki ve gelecekteki ürünümüz.
- **HR modülü**: Daha önce Unified Operations teklifi ile lisanslanan eski bir özellik seti. Bu özellikler, bir müşteri Dynamics 365 Finance veya Dynamics 365 Supply Chain Management uygulamasına sahip olduğunda etkinleştirilir.
- **Finans ve operasyon altyapısı**: Dynamics 365 Finance, Dynamics 365 Supply Chain Management ve Dynamics 365 Project Operations dahil olmak üzere operasyon portföyü tarafından kullanılan geliştirme mimarisi. Bu altyapı, ilerlemek için kullanılacak olan altyapıdır. Bu SSS'de, *birleştirilmiş altyapı* finans ve operasyon ortamına başvurur.
- **Human resources altyapısı**: Dynamics 365 Human Resources uygulaması için tarihsel olarak kullanılan geliştirme mimarisi. Altyapı birleştirme projesi, Dynamics 365 Human Resources'u finans ve operasyon altyapısına taşır. Bağımsız altyapı, durdurulacaktır.

## <a name="general-questions-about-the-infrastructure-merge"></a>Altyapı birleştirme ile ilgili genel sorular

### <a name="will-customers-lose-any-features-or-capabilities"></a>Müşteriler tüm özellikleri veya yetenekleri kaybedecek mi?

Amacımız, bu geçişin müşteriler üzerindeki etkisini en aza indirmektir. Hiçbir özellik veya yetenek kaldırmayacağız. Dynamics 365 Human Resources ve İK modülü arasında işlevsel eşlik olacaktır. Bir özelliğin her iki altyapıda da mevcut olduğu durumlarda, Dynamics 365 Human Resources deneyimi kullanılacaktır.

### <a name="will-the-user-experience-change"></a>Kullanıcı deneyim değişecek mi?

Kullanıcı deneyimi, standart Dynamics 365 platform deneyimiyle tutarlı olacaktır. Pano ve menülere ilişkin genel deneyimin benzer kalacak olsa da, standart Dynamics 365 Finance uygulaması deneyimi ile uyumlu olacaktır. Navigasyon, hem modülleri hem de çalışma alanlarını içerecek, favorilere ve daha fazlasına izin verecektir. **Personel yönetimi** ve **Kişiler** gibi Dynamics 365 Human Resources çalışma alanları finans ve operasyon altyapısıyla birleşecektir. Daha sonra, müşterilerin yeni özellikleri görüntülemesine ve hangilerini kullanmak istediklerine karar vermelerine olanak tanıyan Özellik yönetimi aracılığıyla sunulacaktır. Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ve [Kullanıcı arabirimi belgeleri](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json).

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Dynamics 365 Human Resources Altyapı birleştirmesi ne zaman tamamlanacak?

Altyapı birleştirme müşterilere gerekli adımları planlamaları ve tamamlamaları için zaman tanımak amacıyla aşamalı olarak hayata geçirilecektir. Dynamics 2021 sürüm dalgası 2'de özellikleri kullanıma sunmaya başladık. Bu proje için tüm ürün geliştirme çalışmalarını 2022 yılı 2. dalga sonuna kadar tamamlamayı planlıyoruz. Zaman çizelgelerinin değişikliğe tabi olduğunu unutmayın. En güncel bilgiler için bkz. [yayın planları](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>Altyapı birleştirmesi konusuna yardımcı olmak için hangi eğitim ve kaynaklar mevcut olacak?

Altyapı birleştirme işleminin her adımını ayrıntılı olarak açıklanan belgeler sunacağız. Müşteriler ve ortakların sorunsuz geçiş yapmalarına yardımcı olmak için gerekli olan videolar ve atölye çalışmaları gibi ek eğitim kaynakları sunacağız.

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>Altyapı birleştirme işlemi tamamlandıktan sonra geliştirme özelliğinde değişiklikler olacak mı?

Geliştirme özellikleri hakkında daha fazla bilgi edinmek için bkz. [Ana sayfayı geliştirme ve özelleştirme](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

## <a name="feature-availability-questions"></a>Özellik kullanılabilirliği soruları

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>LinkedIn Talent Hub tümleştirmesi finans ve operasyon altyapısında çalışacak mı?

Hayır, LinkedIn Hub tümleştirmesi birleştirilmiş altyapının bir parçası olmayacak. Genel uygulama programı arabirimleri (API), işe alma ve başvuran izleme çözümleriyle tümleştirme oluşturmak için kullanılabilir. LinkedIn Talent Hub'ı kullanmayı planlayan müşteriler, sağlanan API'leri kullanarak entegre etmek için Microsoft iş ortaklarıyla birlikte çalışmalıdır. Başvuran İzleme Sistemi (ATS) tümleştirme API'leri hakkında daha fazla bilgi için bkz. [Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>Şu anda yalnızca Dynamics 365 Human Resources içinde bulunan özellikler (örneğin izin yönetimi ve sosyal yardım yönetimi) birleştirme tamamlandıktan sonra kullanılabilir mi?

Evet. Tüm Dynamics 365 Human Resources uygulama özellikleri finans ve operasyon altyapısına taşınır. Özellikler, aşamalı bir yaklaşımda kullanıma sunulacak. Birleştirilmiş altyapının özellik kullanılabilirliği hakkında güncel bilgiler için [yayın planlarını](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) düzenli olarak inceleyin.

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>Altyapı birleştirmesi tamamlandıktan sonra Dynamics 365 Human Resources ile Ceridian Tümleştirmeleri kullanıma sunulacak mı?

Ceridian, Bordro API'lerinin avantajlarından yararlanan Dynamics 365 Human Resources ile bir V2 tümleştirmesi oluşturma sürecinde yer alır. Şu anda Dynamics 365 Human Resources'da bulunan dosya tabanlı tümleştirme finans ve operasyon altyapısına geçirilmeyecek. Daha fazla bilgi için bkz. [Bordro API'sine giriş](./hr-admin-integration-payroll-api-introduction.md).

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>Başvuran izleme veya personel işe alma/çıkarma işlevleri dahil edilecek mi?

Önceki sürümlerde, iş ortaklarının ve müşterilerin İnsan Kaynakları ile ATS Tümleştirmeleri oluşturmalarına olanak tanımak için ATS Integration API'sini oluşturduk. ATS ile ilgili ek işlevler 2022 dalga 1'de kullanıma sunulmuştur. Gelecek sürümlerde bu API'leri geliştirmeye devam edeceğiz.

Şu anda finans ve operasyon altyapısında İK işlevleri, Dynamics 365 Human Resources'ta mevcut olmayan bazı işe alım yönetimi işlevlerini içerir. Altyapı birleştirmesi tamamlandığında, bu işlevler tüm İnsan Kaynakları müşterileri için kullanıma sunulmaktadır. Bu işlevsellik basit ATS işlevleri sağlar. Ancak gelecekte bu işlevleri genişletmeyi planlamadık. Daha gelişmiş işlevlere gereksinim duyan müşteriler iş ortağı ATS tümleştirmelerin avantajlarından yararlanabilir. ATS tümleştirme API'leri hakkında daha fazla bilgi için bkz. [Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Dynamics AX 2012 yükseltme araçları, AX 2012'deki İK modülünü Dynamics 365 Human Resources uygulamasına yükseltmek için kullanılacak mi?

Evet. Dynamics AX 2012'den Dynamics 365 Human Resources'a yükseltme, Dynamics 365 Finance veya Dynamics 365 Supply Chain Management gibi diğer Dynamics 365 operasyon uygulamalarının en son sürümüne yükseltmek için kullanılan yükseltme yolunu ve aracını izler.

Finans ve operasyon altyapısına geçiş hakkında daha fazla bilgi için bkz. [İnsan Kaynakları müşteri geçişi SSS](./customer-migration.md).
