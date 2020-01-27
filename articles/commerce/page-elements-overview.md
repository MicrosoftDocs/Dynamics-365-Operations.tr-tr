---
title: Sayfa modeli sözlüğü
description: Bu konu, bir Microsoft Dynamics 365 Commerce sitesinin sayfalarında kullanılan çeşitli öğeleri açıklamaktadır.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0285af2f73a25db3199b3cb089bc0b253a3b3f00
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914876"
---
# <a name="page-model-glossary"></a>Sayfa modeli sözlüğü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, bir Microsoft Dynamics 365 Commerce sitesinin sayfalarında kullanılan çeşitli öğeleri açıklamaktadır.

## <a name="page-element-definitions"></a>Sayfa öğesi tanımları

Aşağıdaki tabloda sitenizin görünümünü, hissini ve içeriğini değiştirirken öğrenmeniz gereken terimler özeti sağlanmaktadır. Daha kapsamlı açıklamalar ve yordamlar için, bağlantıları izleyin.

| Vade | Açıklama ve notlar |
|------|-----------------------|
| [Modül](work-with-modules.md) | <p>**Tanım:** Modüller, yazılma ve bir Web sayfasının çatısı olmasını sağlayan yapı taşlarıdır. Örnekler, Hero ve döngü modüller sayılabilir.</p><p>**Seçildiği yer:** Dağıtılan modüller, site yazma iş akışının şablon, düzen, sayfa ve parça yazma aşamaları gibi çeşitli aşamalarında seçilebilir ve konfigüre edilebilir.</p><p>**Düzenlenme yeri:** özel modüller yazılım geliştirme seti (SDK) kullanılarak kod içinde oluşturulur. Bunlar, daha sonra, seçim için kullanılabilir olduklarında sitenize yüklenir.</p> |
| Modül özelliği | <p>**Tanım:** Modül özellikleri modül tarafından tanımlanan belirli ayarlarla aynıdır. E-ticaret geliştirme araçlarında düzenlenebilirler. Örneğin, bir başlık modülünün başlığını ve arka plan resmini ayarlamak için modül özellikleri kullanılır.</p><p>**Yapılandırma konumu:** Modül özellikleri, şablonlar, düzenler, sayfalar, parçalar ve uygulama ayarları için yazma ortamlarında (düzenleyiciler) görünen Özellik bölmesinde seçilir ve konfigüre edilir.</p> |
| [Şablon](templates-layouts-overview.md) | <p>**Tanım:** şablonlar bir Sayfa kategorisi (örneğin, pazarlama sayfaları, kategori sayfaları ve ürün sayfaları) için kullanılması gereken modül birleşimlerini ve seçenekleri tanımlar.</p><p>**Seçildiği yer:** şablonlar, sayfa veya düzen oluşturma iş akışları sırasında seçilebilir.</p><p>**Nerede düzenlenmişse:** şablonlar, şablon düzenleyicisinde yazılmıştır. Bunları oluşturmak veya değiştirmek için kod gerekmez.</p> |
| [Düzen](templates-layouts-overview.md) | <p>**Açıklama:** mizanpajlar üst şablonun seçenekler kümesinden son seçim ve modüllerin düzenlemesini tanımlar. Tek bir sayfa (*özel düzen*) için bir düzen konfigüre edilebilir veya birden çok sayfa tarafından paylaşılabilir (*önceden ayarlanmış Düzen*).</p><p>**Seçildiği yer:** Yeni sayfa oluşturma sırasında veya varolan bir sayfa için farklı bir düzen gerekiyorsa, düzenler seçilebilir.</p><p>**Nerede düzenlenmişse:** Düzenler, düzen düzenleyicisinde yazılmıştır. Bunları oluşturmak veya değiştirmek için kod gerekmez.</p> |
| Sayfa örneği | <p>**Tanım:** Sayfa örnekleri tek bir sayfa için son, sayfaya özel yerelleştirilmiş içeriği tanımlar. Bu içerik modül özelliklerinin değerlerinden türetilir.</p><p>**Seçildiği yer:** URL'ler atandığında sayfalar seçilir.</p><p>**Nerede düzenlenmişse:** Sayfalar, sayfa düzenleyicisinde yazılmıştır. Bunları oluşturmak veya değiştirmek için kod gerekmez.</p> |
| [Tema](select-site-theme.md) | <p>**Açıklama:** Temalar geçişli stil sayfası (CSS) tanımlar ve bir sayfada oluşturulan modüllerin görünüşünü ve kullanımını belirler.</p><p>**Seçili olduğunda:** Bir tema, Microsoft Dynamics Lifecycle Services (LCS) kullanılarak sitenize yüklendikten sonra, sayfa kapsayıcı modülünün bir özelliği olarak seçilebilir.</p><p>**Nereye düzenlenmekte:** Temalar, SDK kullanılarak oluşturulur ve düzenlenir. Bunlar daha sonra LCS kullanarak sitenize yüklenir.</p> |
| [Parça](work-with-fragments.md) | <p>**Tanım:** parçalar, yeniden kullanılabilen ve birden çok sayfa boyunca merkezi olarak güncelleştirilen yerelleştirilmiş içeriğe sahip tam olarak konfigüre edilmiş modüllerdir. Örneğin, bir başlık modülünden oluşturulan parça tüm şablonlarda ve sitenizdeki tüm sayfalarda kullanılabilir ve merkezi olarak tek bir yerde güncelleştirilebilir.</p><p>**Seçildiği yer:** modüllerin seçilebileceği her yerde parçacık seçilebilir. Yeniden kullanılabilir ve merkezi geliştirme arasında verimliliği artırmaya yardımcı olmak amacıyla bir modülün yerine kullanılabilir.</p><p>**Nerede düzenlenmişse:** Parçalar, parça düzenleyicisinde yazılmıştır. Bunları oluşturmak veya değiştirmek için kod gerekmez.</p> |
| URL | <p>**Tanım:** Tekdüzen Kaynak Konumlandırıcı (URL'ler) Web sayfalarını veya diğer URL'leri gösteren adreslerdir.</p><p>**Seçildiği yer:** URL'ler, sayfalar arasında bağlantılar gerektiğinde seçilir.</p><p>**Nerede düzenlenmişse:** URL'ler, URL düzenleyicisinde yazılmıştır. Bunları oluşturmak veya değiştirmek için kod gerekmez.</p> |
| Aktif | <p>**Tanım:** Varlıklar .jpg, .docx, .PDF veya .mpg gibi bir uzantıya sahip olan dosya ikili dosyasıdır.</p><p>**Seçildiği yer:** varlıklar, bunları gerektiren modüller için modül özellikleri olarak seçilir.</p><p>**Nerede düzenlenir:** varlıklar karşıya yüklenir ve ilişkili meta veriler kıymet yöneticisinde düzenlenir.</p> |

## <a name="additional-resources"></a>Ek kaynaklar

[İçerik ekleme yolları](add-manage-content.md)

[Belge durumları ve yaşam döngüsü](document-states-overview.md)

[Yayınlama gruplarıyla çalışma](publish-groups.md)

[Modüllerle çalışma](work-with-modules.md)

[Parçalarla çalışma](work-with-fragments.md)

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Site gezintisini özelleştirme](customize-site-navigation.md)
