---
title: Sayfa modeli sözlüğü
description: Bu makale, bir Microsoft Dynamics 365 Commerce sitesinin sayfalarında kullanılan çeşitli öğeleri açıklamaktadır.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: intro-internal
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: a4c2a29e8c2112622b5e30064e26523b4f9e2d5a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281440"
---
# <a name="page-model-glossary"></a>Sayfa modeli sözlüğü


[!include [banner](includes/banner.md)]

Bu makale, bir Microsoft Dynamics 365 Commerce sitesinin sayfalarında kullanılan çeşitli öğeleri açıklamaktadır.

## <a name="page-element-definitions"></a>Sayfa öğesi tanımları

Aşağıdaki tabloda sitenizin görünümünü, hissini ve içeriğini değiştirirken öğrenmeniz gereken terimler özeti sağlanmaktadır. Daha kapsamlı açıklamalar ve yordamlar için, bağlantıları izleyin.

| Vade | Açıklama ve notlar |
|------|-----------------------|
| [Modül](work-with-modules.md) | <p>**Tanım:** Modüller, yazılma ve bir Web sayfasının çatısı olmasını sağlayan yapı taşlarıdır. Örnekler, Hero ve döngü modüller sayılabilir.</p><p>**Seçildiği yer:** Dağıtılan modüller, site yazma iş akışının şablon, düzen, sayfa ve parça yazma aşamaları gibi çeşitli aşamalarında seçilebilir ve konfigüre edilebilir.</p><p>**Düzenlenme yeri:** özel modüller yazılım geliştirme seti (SDK) kullanılarak kod içinde oluşturulur. Bunlar, daha sonra, seçim için kullanılabilir olduklarında sitenize yüklenir.</p> |
| Modül özelliği | <p>**Tanım:** Modül özellikleri modül tarafından tanımlanan belirli ayarlarla aynıdır. E-ticaret geliştirme araçlarında düzenlenebilirler. Örneğin, bir başlık modülünün başlığını ve arka plan resmini ayarlamak için modül özellikleri kullanılır.</p><p>**Yapılandırma konumu:** Modül özellikleri, şablonlar, düzenler, sayfalar, parçalar ve uygulama ayarları için yazma ortamlarında (düzenleyiciler) görünen Özellik bölmesinde seçilir ve konfigüre edilir.</p> |
| [Şablon](templates-layouts-overview.md) | <p>**Tanım:** şablonlar bir Sayfa kategorisi (örneğin, pazarlama sayfaları, kategori sayfaları ve ürün sayfaları) için kullanılması gereken modül birleşimlerini ve seçenekleri tanımlar.</p><p>**Seçildiği yer:** şablonlar, sayfa veya düzen oluşturma iş akışları sırasında seçilebilir.</p><p>**Nerede düzenlenmişse:** şablonlar, şablon düzenleyicisinde yazılmıştır. Bunları oluşturmak veya değiştirmek için kod gerekmez.</p> |
| [Düzen](templates-layouts-overview.md) | <p>**Açıklama:** mizanpajlar üst şablonun seçenekler kümesinden son seçim ve modüllerin düzenlemesini tanımlar. Tek bir sayfa (*özel düzen*) için bir düzen konfigüre edilebilir veya birden çok sayfa tarafından paylaşılabilir (*önceden ayarlanmış Düzen*).</p><p>**Seçildiği yer:** Yeni sayfa oluşturma sırasında veya varolan bir sayfa için farklı bir düzen gerekiyorsa, düzenler seçilebilir.</p><p>**Nerede düzenlenmişse:** Düzenler, düzen düzenleyicisinde yazılmıştır. Bunları oluşturmak veya değiştirmek için kod gerekmez.</p> |
| [Sayfa örneği](modify-existing-page.md) | <p>**Tanım:** Sayfa örnekleri tek bir sayfa için son, sayfaya özel yerelleştirilmiş içeriği tanımlar. Bu içerik modül özelliklerinin değerlerinden türetilir.</p><p>**Seçildiği yer:** URL'ler atandığında sayfalar seçilir.</p><p>**Nerede düzenlenmişse:** Sayfalar, sayfa düzenleyicisinde yazılmıştır. Bunları oluşturmak veya değiştirmek için kod gerekmez.</p> |
| [Tema](select-site-theme.md) | <p>**Açıklama:** Temalar geçişli stil sayfası (CSS) tanımlar ve bir sayfada oluşturulan modüllerin görünüşünü ve kullanımını belirler.</p><p>**Seçili olduğunda:** Bir tema, Microsoft Dynamics Lifecycle Services (LCS) kullanılarak sitenize yüklendikten sonra, sayfa kapsayıcı modülünün bir özelliği olarak seçilebilir.</p><p>**Nereye düzenlenmekte:** Temalar, SDK kullanılarak oluşturulur ve düzenlenir. Bunlar daha sonra LCS kullanarak sitenize yüklenir.</p> |
| [Parça](work-with-fragments.md) | <p>**Tanım:** parçalar, yeniden kullanılabilen ve birden çok sayfa boyunca merkezi olarak güncelleştirilen yerelleştirilmiş içeriğe sahip tam olarak konfigüre edilmiş modüllerdir. Örneğin, bir başlık modülünden oluşturulan parça tüm şablonlarda ve sitenizdeki tüm sayfalarda kullanılabilir ve merkezi olarak tek bir yerde güncelleştirilebilir.</p><p>**Seçildiği yer:** modüllerin seçilebileceği her yerde parçacık seçilebilir. Yeniden kullanılabilir ve merkezi geliştirme arasında verimliliği artırmaya yardımcı olmak amacıyla bir modülün yerine kullanılabilir.</p><p>**Nerede düzenlenmişse:** Parçalar, parça düzenleyicisinde yazılmıştır. Bunları oluşturmak veya değiştirmek için kod gerekmez.</p> |
| [URL](create-page-URL.md) | <p>**Tanım:** Tekdüzen Kaynak Konumlandırıcı (URL'ler) Web sayfalarını veya diğer URL'leri gösteren adreslerdir.</p><p>**Seçildiği yer:** URL'ler, sayfalar arasında bağlantılar gerektiğinde seçilir.</p><p>**Nerede düzenlenmişse:** URL'ler, URL düzenleyicisinde yazılmıştır. Bunları oluşturmak veya değiştirmek için kod gerekmez.</p> |
| Aktif | <p>**Tanım:** Varlıklar .jpg, .docx, .PDF veya .mpg gibi bir uzantıya sahip olan dosya ikili dosyasıdır.</p><p>**Seçildiği yer:** varlıklar, bunları gerektiren modüller için modül özellikleri olarak seçilir.</p><p>**Nerede düzenlenir:** varlıklar karşıya yüklenir ve ilişkili meta veriler kıymet yöneticisinde düzenlenir.</p> |

## <a name="additional-resources"></a>Ek kaynaklar

[İçerik ekleme yolları](add-manage-content.md)

[Belge durumları ve yaşam döngüsü](document-states-overview.md)

[Yayımlama gruplarıyla çalışma](publish-groups.md)

[Kanallar arası paylaşımı etkinleştirme ve kullanma](cross-channel-sharing.md)

[Modüllerle çalışma](work-with-modules.md)

[Parçalarla çalışma](work-with-fragments.md)

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Site gezintisini özelleştirme](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
