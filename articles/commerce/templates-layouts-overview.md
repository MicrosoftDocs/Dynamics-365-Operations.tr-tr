---
title: Şablonlar ve düzenlere genel bakış
description: Bu konu Microsoft Dynamics 365 Commerce'te şablonlarını ve düzenlerini kapsamaktadır.
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
ms.openlocfilehash: d805c39b77d653eaa9935751ae89012c98b930d2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416541"
---
# <a name="templates-and-layouts-overview"></a>Şablonlar ve düzenlere genel bakış


[!include [banner](includes/banner.md)]

Şablonlar, Microsoft Dynamics 365 Commerce sayfa modelinin yapısal bir öğesidir. Amacınız, site yazma iş akışlarının verimliliğini ve tutarlılığını en üst düzeye çıkarmaksa, Web sitenizin şablonlarının nasıl yararlanacağınızı öğrenmeniz çok önemlidir. Şablon yapısı hakkında erken kararlar önemli olduğunu ve günlük, dönemlik ve site genelindeki marka güncelleştirmeleri için maliyeti ve becerisi önemli şekilde etkileyebilir. İyi yapılandırılmış şablonların başka yararları da vardır. Örneğin, site genelinde arama motoru iyileştirme (SEO) puanlarını geliştirmeye ve hata sayılarını en aza indirmeye yardımcı olurlar.

Şablonlarla çalışmaya başlamak için şablonların ve düzenlerin işlevsel yararlarını, aralarındaki farkları ve hiyerarşiyi anlamanızın iyi bir yoldur.

Aşağıdaki şekil, sayfa modeli hiyerarşisini işlenmiş bir Web sayfasının arkasında gösterir.

![Sayfa modeli şeması](../commerce/media/page-model-diagram.png)

| Varlık        | Temel işlev |
|---------------|----------------|
| Şablon      | Şablonlar, bir dizi düzen ve sayfa örneği için modül seçeneklerini ve temel iskele tanımlar. |
| Düzen        | Düzenler bir sayfa veya bir sayfa kümesi için son seçim ve modüllerin düzenlemesini tanımlar. |
| Sayfa örneği | Sayfa örnekleri, belirli sayfaların verilerini ve içeriğini tanımlar. |

## <a name="templates"></a>Şablonlar

Şablonlar Dynamics 365 Commerce sayfa modeli hiyerarşisinin en üstünde yer aldığı gibi, site konfigürasyonu için önemli bir erken adımı temsil etmektedir. Kavramsal olarak, şablonlar, aşağı akış düzeni oluşturma ve sayfa oluşturma iş akışları için temel yapıyı ve yazma seçeneklerini tanımlayarak alt öğe düzenlerinin ve sayfaların ailesi üzerindeki tutarlılığı denetlemenize yardımcı olur. Şablonlar, önceden tanımlanmış, merkezi olarak yönetilen öğeler (üstbilgiler ve altbilgiler gibi) aracılığıyla içerik yazma işlemini ve modül konfigürasyonu seçeneklerinin markalarda olmasını sağlamaya yardımcı olan Kılavuzlu yazma akışlarını basitleştirmeye yardımcı olabilir.

### <a name="controlling-consistency"></a>Tutarlılığı denetleme

Bir şablon tasarladığınızda, oluşturmak zorunda olduğunuz en büyük iş kararı, şablonun sayfa oluşturma işlemi üzerinde sahip olması gereken denetimi ne kadar denetler. Aşağı akış yazarı için açık her şeyi bırakan bir şablon, oluşturulacak en kolay şablon türüdür, ancak bundan oluşturulan sayfaların bakımıyla ilgili uzun süreli sonuçlara sahip olabilir. İyi yazılmış bir şablon kılavuz ve kolay yazma deneyimi sağlar, ancak yazarların görevini tamamlayabilmeleri için yeterli esneklik sağlar. Tüm bu yönleri, şablonun uyguladığı kontrol düzeyine bağlıdır.

Şablonlar, içerik yazarlarının daha etkili olmasını ve marka üzerinde aşağıdaki yollarla kesintisiz kalmasına yardımcı olur:

- Bir sayfada kullanılabilen modülleri sınırlayın.
- Varsayılan modülü ve konfigürasyon seçimlerini öner.
- Şablon düzeyinde denetlenen bir modül ve konfigürasyon seçimlerini açıkça yapın. Bu işlem, bir ayarı *kilitlemek* olarak da bilinir.

Aşağıdaki örnek, temel bir şablonun (şablon X) nasıl konfigüre edilebilir olduğunu gösterir:

- X şablonunun tüm alt düzenleri bir üstbilgi kapsayıcısına, bir gövde kapsayıcısına ve bir altbilgi kapsayıcısına sahip olmalıdır.
- Şablon X'te, başlık konteynerinin konfigürasyonu kilitlidir ve yalnızca X şablonu içinde değiştirilebilir. Tüm alt düzen ve sayfalar her zaman bu başlığa sahiptir.
- Gövde konteyner en az bir modül ve maksimum on modül gerektirir. Bu modüller, aşağı akış düzenleri ve sayfalar tarafından tanımlanmıştır.
- Gövde konteyner için, Hero, özellik, döngü ve başlık modülleri kullanılabilir.
- Bir altbilgi konteyneri şablon X'de yapılandırılmış, ancak akış yönündeki düzenler ve sayfalar tarafından geçersiz kılınabilir.

Bu örnekteki şablon, aşağı akış içerik yazarları için basit bir yapıyı ve seçenek kümesini tanımlar. Sayfanın bazı bölümlerinin (Bu örnekte başlık) şablonda tanımlanıp tanımlandığını ve kilitlenip kilitlendiğini ve akış yönündeki yazarlar tarafından değiştirilemeyeceğini unutmayın. Diğer bölümler (bu örnekte gövde), belirli yönergeler içinde (bu örnekte, en az sayıda ve belirli türlerdeki modül sayısı alt sınırı), akış aşağı yazarları tarafından tanımlanabilir. Ve diğer bölümler (bu durumda altbilgi) şablonda tanımlanmıştır, ancak akış yönündeki yazarlar tarafından geçersiz kılınabilir.

Site ve marka yöneticileri için önemli bir başlangıç adımı, alt düzen ve sayfa yazarları için sınırlama ve esneklik arasındaki doğru dengeyi belirlemektir. Şablonlar kullanıldığında, bu bakiye tamamen konfigüre edilebilir. Sayfa öğelerinin merkezi olarak (şablonda kilitli) veya sayfa hiyerarşisinde alt düzeylerin soluna güncelleştirilip güncelleştirilmediğini etkiler.

Şablonları kullanmaya başlamak için [şablonlarla çalışın](work-with-templates.md).

## <a name="layouts"></a>Düzenler

Düzenler sayfa modeli hiyerarşisindeki şablonların altında bir sonraki düzeydir. Bir şablon bir sayfa için izin verilen tüm modülleri tanımladığında, düzen açık bir seçimdir ve modüller düzenlemesidir. Sayfalar sayfa modeli hiyerarşisindeki düzenlerin altında bir sonraki düzeydir. Bunlar, düzende seçilen modüller için yerelleştirilmiş içeriği tanımlar.

Aşağıdaki örnek önceki bölümden alınan şablon örneği üzerinde oluşturulur ve temel düzenin nasıl konfigüre edilebilir olduğunu gösterir:

- Düzenin üst şablonu, gövde konteynerinin bir ile on modül arasında olmasını gerektiriyor. Bu modüller, yalnızca hero, özellik, döngü ve başlık modülleri olabilir. Bu nedenle, düzen aşağıdaki seçili modülleri ve düzenlemeleri tanımlayabilir:

    - Gövde konteynerindeki ilk modül bir ana başlık modülüdür ve bunu takip eden bir hero modülü ve iki özellik modülüdür.
    - İlk özellik modülü sola hizalanır ve ikinci özellik modülü sağa hizalanır.

- Ana şablondan devralınan varsayılan alt bilgi olsa bile, şablon yazarı altbilginin kilidini kaldırılmış bırakır. Bu nedenle, düzen farklı bir altbilgi parçası tanımlayarak bunu geçersiz kılabilir.

Bu örnekteki düzen, alt sayfalar için son modül düzenlemesini tanımlar. Şablon gibi, düzen, her zaman alt sayfalar tarafından miras alınacak varsayılan veya kilitli modül özelliklerini tanımlayabilir (örneğin, özellik modüllerinin hizalanması). Mizanpajdaki her modülün gerçek içeriği veya verileri, her bir alt sayfa örneğinde hiyerarşi altında olacak şekilde tanımlanır. Burada önemli bir ayrım olduğundan, mizanpajlar doğrudan yerelleştirilebilir içerik içermez, alt sayfaları ise bu şekilde yapılır. Düzenin birincil işlevi, son düzenleme ve alt sayfaları için modüllerin varsayılan yapılandırmasını tanımlamaktır.

Bu hiyerarşi iki nedenden dolayı güçlüdür. İlk olarak, aynı ana şablonu paylaşan düzenler, düzen değiştirme senaryolarında uyumlu olarak değerlendirilir. Bu nedenle, herhangi bir sayfanın düzeni, sayfa düzeyindeki içeriğin yeniden düzenlenmesi gerekmeden aynı şablon hiyerarşisinden başka bir düzene değiştirilebilir. Mevsimsel tasarım güncelleştirmeleri yapmak, denemeler yapmak veya kalıcı bir site yeniden tasarımı yapmak için bu becerinin avantajlarından yararlanabilirsiniz. İkincisi ise, sayfalar bir grup sayfanın paylaşılan öğelerini, her sayfada güncelleştirme gerektirmeden, merkezi olarak değiştirmek için başka bir yol sağlar. Örneğin, ürün kategorisinde aynı mizanpajı paylaşan 1.000 sayfa varsa, modüller düzende yeniden sıralanabilir ve bu değişiklik hemen tüm 1.000 alt sayfaya yansıtılır.

Bu hiyerarşiyi anlayarak, maliyet tasarrufu sağlayan, ölçeklenebilir olan ve zamanla Site geliştikçe daha iyi sonuçlar elde eden çevik ve etkili bir site yapısı elde edebilirsiniz.

### <a name="preset-and-custom-layouts"></a>Hazır ayar ve özel düzenler

Sitenizdeki düzenler *önceden ayarlanmış* veya *özel* olabilir:

- **Önceden belirlenmiş düzenler** tüm modüllerin zaten seçildiği ve düzenlendiği yerlerde bir sayfa oluşturma iş akışına izin verir ve yalnızca veri girişi gereklidir. Aynı düzen gereksinimlerine sahip birçok sayfa yazılmalı olduğunda bu yaklaşım zamandan tasarruf sağlamaya yardımcı olabilir. Hazır ayar düzenlerinin alt sayfalarıyla bire çok ilişkisi vardır. Bu nedenle, tek bir önceden belirlenmiş düzen yüzlerce veya binlerce alt sayfa için modül düzenlemesini merkezi olarak denetlemek amacıyla kullanılabilir.
- **Özel düzenler**, bir sayfaya katıştırılmış tek kullanılan mizanpajlardır. Bunlar, başka yeni sayfalar oluşturulurken veya Düzen anahtarlama senaryolarında bir seçenek olarak gösterilmezler. Bu yaklaşımın yararı, özel düzen kullanan bir sayfa oluşturarak bir yazarın denebilmesidir. Böylece, yazar diğer sayfalar için mizanpajı yeniden kullanmak isterse, kolayca hazır ayar düzenine dönüştürülebilir. Yeni hazır ayar düzeni daha sonra sayfa oluşturma iş akışlarında bir seçenek olarak ve aynı şablon hiyerarşisinden sayfalar için yerleşim anahtarlama senaryolarında kullanıma sunulur. Buna karşılık, önceden ayarlanmış düzenler özel mizanpajlara dallanmış olabilir. Böylece, bir yazar bir sayfayı hazır ayar düzeninden bozabilir ve yeni bir tek kullanım özel düzeni oluşturabilir. (Bu yeni özel düzen hala üst şablondaki tüm kısıtlamalara bağlıdır.)

Hazır ayar düzeni ve özel mizanpajlar, yazma araç takımının farklı bölümlerinde düzenlenir. Özel mizanpajlar diğer sayfalarda hiçbir bağımlılığa sahip olmadığı için, bunlar doğrudan sayfa Düzenleyicisi 'nde düzenlenirler. Bu durumda, bir düzenin varlığı genellikle kullanıcıya saydamdır ve yalnızca sayfa düzeyi Özellikler içinde ve Mizanpaj seçenekleri için Eylemler aracılığıyla sunulur. Ancak, önceden ayarlanmış düzenlerdeki değişiklikler birçok alt sayfayı etkilediğinden, bunlar, yayımlama eylemlerinin alt sayfalardaki tüm aşağı akış etkisini düşünmediği için, düzen düzenleyicisinde düzenlenmelidir.

Aşağıdaki çizimler, hazır ayar ve özel düzen senaryolarını gösterir.

![Hazır ayar ve özel düzen senaryoları](../commerce/media/template-figure1.png)

Önceden ayarlanmış mizanpajları kullanmaya başlamak için bkz. [Ön ayar düzenleriyle çalış](work-with-layouts.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Şablonlarla çalışma](work-with-templates.md)

[Önceden ayarlanmış düzenlerle çalışma](work-with-layouts.md)

[Yayınlama gruplarıyla çalışma](publish-groups.md)
