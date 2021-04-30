---
title: Üretimdeki çalışanlar için karma gerçeklik Kılavuzları sağlama
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'taki üretim yönetimi modülünün Dynamics 365 Guides ile nasıl tümleştirileceğini açıklamaktadır.
author: cabeln
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 15595c46f9d6ff91f6fd618859e9f059ae88bd78
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910101"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>Üretimdeki çalışanlar için karma gerçeklik Kılavuzları sağlama

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Üretim süreçlerinde çalışan çalışanlar, çalışmaları bağlamında doğru zamanda sağlanan ilgili yönergelerden faydalanır. *Yönergeler* aşağıdakiler dahil olmak üzere birçok iş alanında uygulanır: derleme servis, operasyonlar, sertifika ve güvenlik. Devam eden eğitim yönergeleri bu temel iş işlevlerinin tümünde, çalışanların daha fazlasını elde etmesine ve daha iyi çalışmasına yardımcı olabilir.

## <a name="introduction"></a>Giriş

Yönergeleri farklı şekillerde sağlayabilirsiniz. Kullanıma hazır olarak gelen etkili bir sistem [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) kullanır.

Dynamics 365 Guides uygulamalı eğitimle çalışanlarınızı desteklemenize yardımcı olabilir. Çalışanlarınıza gereksinim duydukları araçlar ve parçalara yönelik kılavuzluk sağlayan adım adım yönergelerle standartlaştırılmış süreçler belirleyebilir ve bu araçların gerçek çalışma durumlarında nasıl kullanılacağını çalışanlarınıza gösterebilirsiniz.

Kılavuzları, üretim denetiminin aşağıdakiler dahil çeşitli aşamalarına iliştirebilirsiniz:

- [Kaynaklar](#resources)
- [Kaynak grupları](#resource-groups)
- [Serbest bırakılan ürünler](#released-products)
- [Formüller](#formulas)
- [Formül sürümleri](#formula-versions)
- [Ürün reçeteleri (BOM'lar)](#bom)
- [BOM süürmleri](#bom-versions)
- [Rotalar](#routes)
- [Rota sürümleri](#route-versions)
- [Rota operasyonu ilişkileri](#route-operation-relations)

> [!NOTE]
> Ayrıca, VArlık Yönetimi ile de Kılavuzlar ekleyebilirsiniz. Bu seçenek hakkında daha fazla bilgi için bkz. [Dynamics 365 Supply Chain Management'ı (Varlık Yönetimi) Dynamics 365 Guides ile tümleştirme](../asset-management/asset-management-guides-integration.md).

Bir saha çalışan Supply Chain Management üzerinden atölyede bir iş seçtiğinde, çalışan [ilgili kılavuzları](#logic) iş kartında görebilir. Çalışan belirli bir kılavuzu seçtiğinde, ekranda o kılavuz için bir QR kodu gösterilir. Çalışan, QR kodunu taramak HoloLens'i kullanır ve bu, Guides'ı başlatarak gerekli yönergeleri görüntüler.

Aşağıdaki alt bölümlerde, farklı sektörlerdeki şirketlerin üretim yönergelerini sunmak için Guides kullanırken en büyük değeri elde ettiği birkaç seçili senaryo açıklanmaktadır.

### <a name="assembly"></a>Montaj

![Derleme görevlerinde Guides kullanma](media/instruction-guides-hero-assembly.png "Servis görevlerinde Guides kullanma")

Derleme işlemlerinde yönergeler, çalışanlara gereksinim duydukları araç ve bölümleri ve gerçek çalışma durumlarında bunların nasıl kullanılacağını gösterir.

Üretim yöneticileri, örneğin [üretim rotaları](routes-operations.md), [operasyon ilişkileri](routes-operations.md#operation-relations) veya [ürün reçeteleri](bill-of-material-bom.md) için Kılavuzlar oluşturabilir ve atayabilir. Çalışanlar ilgili yönergeleri, atölyede ilgili operasyon deneyiminde bulabilir.

### <a name="service"></a>Servis

![Servis görevlerinde Guides kullanma](media/instruction-guides-hero-service.png "Servis görevlerinde Guides kullanma")

Teknisyenleri iş sahasında kılavuzlu talimatlarla donatın ve ek ziyaretler planlama ihtiyacını ortadan kaldırın.

Servis yöneticileri, örneğin kalite değerlendirmesi yordamlarına geçiş yapan belirli [ürünlere](../../commerce/product.md) Kılavuzlar atayabilirler.

### <a name="quality"></a>Kalite

![Kalite güvence görevlerinde Guides kullanma](media/instruction-guides-hero-quality.png "Kalite güvence görevlerinde Guides kullanma")

Yeni süreçler kullanıma sunun ve çalışanların bilgisini tekrarlanabilir bir araca çevirerek artan tutarlılık sağlayın.

Kalite güvencesi yöneticileri, örneğin kalite değerlendirmesi yordamlarına geçiş yapan belirli [ürünlere](../../commerce/product.md) kılavuzlar atayabilirler.

### <a name="certifications"></a>Sertifikalar

![Sertifika ile ilgili görevler için Guides kullanma](media/instruction-guides-hero-certification.png "Sertifika ile ilgili görevler için Guides kullanma")

Kimin ve nerede yardıma ihtiyacı olduğunu hızlı bir şekilde tanımlayarak, her çalışanın yüksek standartları karşıladığından emin olun.

### <a name="safety"></a>Güvenlik

![İş güvenliği yönergelerinde Guides kullanma](media/instruction-guides-hero-safety.png "İş güvenliği yönergelerinde Guides kullanma")

Fiziksel ortamda çalışmadan önce tehlikeli yordamları sanal olarak uygulayan yönergeler sağlayın. Karma gerçeklik yaklaşımıyla, çalışanlar tehlikeli yordamları sanal olarak deneyimleyebilir.

Üretim yöneticileri [ürün öğelerine ](../../commerce/product.md), [rotalara](routes-operations.md) ve [operasyonlara](routes-operations.md#operation-relations) yönergeler atayarak, tehlikeli malzeme işleme veya hassas malzeme işleme yordamları için özel işleme yönergeleri sağlayabilir.

## <a name="get-started-with-instructions-and-guides"></a>Yönergeler ve Guides ile başlayın

Üretim süreçlerinde yönergeleri etkinleştirmek için, Supply Chain Management, Dynamics 365 Guides ile kullanıma hazır tümleştirme sağlar. Üretim varlıklarına ve işine karma gerçeklik yönergeleri oluşturmak, yönetmek ve atamak için Guides'ın lisanslı ve yüklenmiş uygulama örneği gereklidir.

### <a name="prerequisites"></a>Önkoşullar

Bu özelliği kullanmak için sisteminizde şunlar olmalıdır:

- Dynamics 365 Supply Chain Management sürüm 10.0.15 veya üstü
- Supply Chain Management uygulamaları için [Çift yazma](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- [Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) sürüm 400.0.1.48 veya üstü

### <a name="turn-on-the-feature"></a>Özelliği etkinleştirme

Özelliği sisteminizde kullanılabilir hale getirmek için yapılandırma anahtarlarını etkinleştirmeniz gerekir. Bunu yalnızca bir kere yapmanız gerekir. Bunu yapmak için bir yöneticinin aşağıdakileri yapması gerekir:

1. Sisteminizi [Bakım modunda](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) anlatıldığı şekilde bakım moduna alın.
1. **Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin.
1. **Karma gerçeklik** bölümünü genişletin ve sonra **Karma gerçeklik kılavuzu** onay kutusunu seçin.
1. **Üretim yönetimi** bölümünü genişletin ve sonra **Üretim yönergeleri** onay kutusunu seçin.
1. [Bakım modunda](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) anlatıldığı şekilde bakım modunu kapatın.
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>Guides'ın atölyede nasıl görüneceğini yapılandırma

Guides'ın atölyede nasıl görüneceğini konfigüre etmek için **Karma Gerçeklik \> Dynamics 365 Guides \> Guides tümleştirmesini yapılandır** öğesine gidin.

![Üretim için Guides tümleştirmesini yapılandırma](media/instruction-guides-configure-integration.png "Üretim için Guides tümleştirmesini yapılandırma")

Aşağıdaki alanları ayarlayın:

- **Microsoft Dataverse URL'si** - Guides oluşturduğunuz Microsoft Dataverse ortamının URL'sini belirtin. Bu biçim, URL'nin ilk bölümünün genellikle kuruluşunuzun adı (örneğin "contoso.") olduğu durumda "contoso.crm4.dynamics.com" şeklindedir, ikinci bölüm ise ortamınızın veri bölgesine özgüdür ("crm4" gibi) ve son bölüm etki alanıdır ("dynamics.com" gibi). Doğru URL'yi bulmanın yollarından biri [home.dynamics.com](https://home.dynamics.com/) adresine gitmek ve sonra Guides uygulamanızı açmaktır. Guides açıldığında, tarayıcınızın adres çubuğunda URL'yi görürsünüz (yalnızca önceki örneğe benzeyen temel URL'yi alın). Bu değer, kılavuzlarınız için adres oluşturmak amacıyla kullanılır ve QR kodlarına kodlanır.
- **QR kodu boyutu** - İşlenen QR kodu boyutunu ayarlayın. Ekranınızın büyük bir boyutunu dolduracak, ancak daha fazlasını doldurmayacak bir boyut seçmeniz önerilir. Genellikle, *15* iyi bir değerdir.
- **QR kodu hata düzeltme düzeyi** - QR kodunun öğe boyutunu ayarlayın. Yüksek öğe boyutu, kodun güvenilirliğini artırmaya yardımcı olabilir ancak **QR kodu boyutunuz** seçtiğiniz düzeltme düzeyinin gerektirdiği ayrıntı düzeyini destekleyecek büyüklükte olmalıdır.

> [!TIP]
> - Ekranınız için çok büyük olan QR kodu boyutlarının işlenmesi biraz daha uzun sürer ve ekrana sığacak şekilde ölçeklenir. Bunlar bir avantaj sağlamaz.
> - Çok küçük olan QR kodu boyutları, HoloLens'in bazı ortamlarda kodu doğru okuma yeteneğini azaltabilir.
> - QR kodları görüntüleyen her cihazın ayarlarını HoloLens kullanıcıları için test etmenizi öneririz. Atölye ortamınıza yeterli okunabilirlik sağlayan ayarları seçin.  

## <a name="get-an-overview-of-all-guide-assignments"></a>Tüm Kılavuz atamalarının genel görünümünü alma

Kuruluşunuzdaki tüm kullanılabilir Kılavuzların listesini ve üretim süreçlerinize ve kaynaklarınıza yapılan tüm atamaları görmek için **Tüm Kılavuzlar** sayfasını kullanın. Açmak için, **Karma gerçeklik \> Kılavuzlar \> Tüm Kılavuzlar**'a gidin. Üstteki listede bulunan tüm Kılavuzlar gösterilir ve bu alanı, listeye filtre uygulamak için kullanabilirsiniz. Alttaki listede tüm Kılavuz atamaları gösterilir ve bunları yönetmek için bir araç çubuğu sağlanır.

![Kılavuzları Yönetme](media/instruction-guides-allguides.png "Kılavuzları Yönetme")

Aşağıdaki bölümlerde, Kılavuzlar atayabildiğiniz nesne türleri açıklanmıştır. Her atanan kılavuz, ilgili üretim işlerine otomatik olarak eklenen yönergeleri sağlar ve atölyede kullanılabilir olacaktır.

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>Kılavuzu kaynakla ilişkilendirme

Kılavuzu ilgili üretim işleri bağlamında sunmak için bir [kaynağa](operations-resources.md) Kılavuz ekleyin.

### <a name="typical-scenario-using-resources"></a>Kaynakları kullanan tipik senaryo

Örneğin, genel makine güvenliğiyle veya makine türündeki bir kaynağa ilişkin yönergeleri ele alarak bir Kılavuz ekleyebilirsiniz. Daha sonra, bu Kılavuz makinede gerçekleştirilen her iş için kullanılabilir olacaktır.

### <a name="add-a-guide-to-a-resource"></a>Kaynağa Kılavuz ekleme

Kaynağa Kılavuz eklemek için:

1. **Üretim denetimi \> Kurulum \> Kaynaklar \> Kaynaklar**'a gidin.
1. Liste bölmesinden Kılavuz atamak istediğiniz kaynağı seçin.
1. **İlişkili Kılavuzlar** hızlı sekmesini genişletin.
1. **İlişkili Kılavuzlar** araç çubuğundan **Ekle**'yi seçin. Kılavuza yeni bir satır eklenir.
1. Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin. Çok sayıda Kılavuzunuz varsa, aradığınız bir kılavuzu bulmak için listeye filtre uygulayabilirsiniz.
    ![Kılavuzları Yönetme](media/instruction-guides-allguides.png "Kılavuzları Yönetme")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>Kılavuzu kaynak grubuyla ilişkilendirme

Makine gruplarını, üretim hatlarını veya çalışma hücrelerini yönetmek için kullanıyorsanız [kaynak gruplarına](tasks/define-discrete-manufacturing-resource-group.md) kılavuz ekleyebilirsiniz.

### <a name="typical-scenarios-using-resource-groups"></a>Kaynak gruplarını kullanan tipik senaryolar

**Örnek 1:** Aynı model birkaç makine için bir kaynak grubu tanımladınız. İlgili her kaynağa makine modeli için uygun işleme talimatı kılavuzu atamak yerine, Kılavuzu makine modelini yansıtan kaynak grubuna atayabilirsiniz.

**Örnek 2:** Farklı makineler içeren bir çalışma hücresi için bir kaynak grubu tanımladınız ve çalışma hücresinin nasıl yönetileceğine ilişkin genel yönergeler sağlayan bir Kılavuzunuz var. Kılavuz bu iş hücresindeki tüm üretim faaliyetleri için geçerli olur.

### <a name="add-a-guide-to-a-resource-group"></a>Kaynak grubuna Kılavuz ekleme

Kaynak grubuna Kılavuz eklemek için:

1. **Üretim denetimi \> Kurulum \> Kaynaklar \> Kaynaklar grupları**'na gidin.
1. Liste bölmesinden Kılavuz atamak istediğiniz kaynak grubunu seçin.
1. **İlişkili Kılavuzlar** hızlı sekmesini genişletin.
1. **İlişkili Kılavuzlar** araç çubuğundan **Ekle**'yi seçin. Kılavuza yeni bir satır eklenir.
1. Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin. Çok sayıda Kılavuzunuz varsa, aradığınız bir kılavuzu bulmak için listeye filtre uygulayabilirsiniz.
    ![Kaynak grubuna Kılavuz ekleme](media/instruction-guides-resourcegroup.png "Kaynak grubuna Kılavuz ekleme")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>Kılavuzu serbest bırakılan ürünle ilişkilendirme

Herhangi bir [serbest bırakılan ürüne](../pim/tasks/create-released-product-single-company.md) kılavuz ekleyebilirsiniz.

### <a name="typical-scenario-using-released-products"></a>Serbest bırakılan ürünler kullanan tipik senaryo

Ürün düzeyindeki Kılavuzlar, belirli bir serbest bırakılan ürün veya maddeyi çalıştırma veya işleme ile ilgili yönergelerle atölye çalışanlarına yardımcı olur.

### <a name="add-a-guide-to-a-released-product"></a>Kılavuzu serbest bırakılan ürüne ekleme

Serbest bırakılan ürüne Kılavuz eklemek için:

1. **Üretim bilgi yönetimi \> Ürünler \> Serbest bırakılan ürünler**'e gidin.
1. Kılavuz atamak istediğiniz ürünü açın.
1. Eylem Bölmesinde, **Mühendis** sekmesini açın ve **Görünüm** grubundan **İlişkili Kılavuzlar**'ı seçin.
1. Seçili ürününüz için **İlişkili Kılavuzlar** sayfası açılır.
1. Eylem bölmesinde, kılavuza yeni satır eklemek için **Ekle**'yi seçin. 
1. Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.
    ![Serbest bırakılan ürüne Kılavuz ekleme](media/instruction-guides-ReleasedProduct-AddGuides.png "Serbest bırakılan ürüne Kılavuz ekleme")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>Kılavuzu formülle ilişkilendirme

Herhangi bir [formüle](bill-of-material-bom.md#formulas-co-products-and-by-products) kılavuz ekleyebilirsiniz.

### <a name="typical-scenario-using-formulas"></a>Formülleri kullanan tipik senaryo
  
Formül düzeyindeki Kılavuzlar, atölye çalışanlarına bir formül veya reçete bağlamında, kılavuzlu işleme talimatları sağlar. Kılavuzlar, bir formülün sürümlerine de atanabilir.

> [!NOTE]
> Bir rotaya, rota sürümüne veya rota operasyon ilişkilerine formüle dayalı olarak üretim süreçleriyle ilgili kılavuz atayabilirsiniz.  

> Kılavuzlar, şu anda bireysel formül satırlarına eklenemez.

### <a name="add-a-guide-to-a-formula"></a>Formüle Kılavuz ekleme

Formüle Kılavuz eklemek için:

1. **Üretim bilgi yönetimi \> Ürün reçeteleri ve formülleri \> Formüller** seçeneğine gidin.
1. Kılavuz atamak istediğiniz formülü açın.
1. Üst hızlı sekmenin yukarısındaki **Başlık** sekmesini açın.
1. **İlişkili Kılavuzlar** hızlı sekmesini genişletin.
1. **İlişkili Kılavuzlar** araç çubuğundan **Ekle**'yi seçin. Kılavuza yeni bir satır eklenir.
1. Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.
    ![Formüle Kılavuz ekleme](media/instruction-guides-Formula.png "Formüle Kılavuz ekleme")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>Kılavuzu formül sürümüyle ilişkilendirme

Herhangi bir [formül sürümüne](bill-of-material-bom.md#bom-and-formula-versions) kılavuz ekleyebilirsiniz.

### <a name="typical-scenario-using-formula-versions"></a>Formül sürümlerini kullanan tipik senaryo

Bir formülün bağımsız bir sürümüne eklenen kılavuzlar, atölye çalışanlarına formül reçetesinin söz konusu sürümünün üretiminde yol gösteren yönergeler sağlar.

> [!TIP]
> Bir rotaya, rota sürümüne veya rota operasyon ilişkilerine bu formül sürümüne dayalı olarak üretim süreçleriyle ilgili kılavuz atayabilirsiniz.  

> [!NOTE]
> Kılavuzlar, şu anda bireysel formül satırlarına eklenemez.

### <a name="add-a-guide-to-a-formula-version"></a>Formül sürümüne Kılavuz ekleme

Formül sürümüne Kılavuz eklemek için:

1. **Üretim bilgi yönetimi \> Ürün reçeteleri ve formülleri \> Formüller** seçeneğine gidin.
1. Kılavuza atamak istediğiniz sürümü içeren formülü açın.
1. Üst hızlı sekmenin yukarısındaki **Başlık** sekmesini açın.
1. **Formül sürümleri** hızlı sekmesinde, Kılavuz atamak istediğiniz sürümü seçin.
1. **Formül sürümleri** araç çubuğunda **İlişkili Kılavuzlar**'ı seçin.
    ![Seçili formül sürümüyle ilişkilendirilen Kılavuzları açma](media/instruction-guides-FormulaVersion.png "Seçili formül sürümüyle ilişkilendirilen Kılavuzları açma")
1. Formül sürümünüz için **İlişkili Kılavuzlar** sayfası açılır.
1. Eylem bölmesinde, kılavuza yeni satır eklemek için **Ekle**'yi seçin. 
1. Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.
    ![Formül sürümüne Kılavuz ekleme](media/instruction-guides-FormulaVersionAddGuide.png "Formül sürümüne Kılavuz ekleme")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>Kılavuzu ürün reçeteleriyle ilişkilendirme

Herhangi bir [ürün reçetesine](bill-of-material-bom.md) (BOM) bir kılavuz ekleyebilirsiniz.

### <a name="typical-scenario-using-bills-of-materials"></a>Ürün reçeteleri kullanan tipik senaryo

Ürün reçetesine iliştirilen kılavuzlar, atölye çalışanlarına bir ürün reçetesinin nasıl hazırlanacağını ve işleneceğini açıklayan yönergeler sağlar. Kılavuzlar, bir ürün reçetesinin sürümlerine de atanabilir.

> [!NOTE]
> Kılavuzlar, şu anda bireysel BOM satırlarına eklenemez.

### <a name="add-a-guide-to-a-bill-of-materials"></a>Ürün reçetelerine Kılavuz ekleme

Ürün reçeteine Kılavuz eklemek için:

1. **Ürün bilgi yönetimi \> Ürün reçeteleri ve formüller \> Ürün reçetesi**'ne gidin.
1. Kılavuz atamak istediğiniz ürün reçetesini açın.
1. Üst hızlı sekmenin yukarısındaki **Başlık** sekmesini açın.
1. **İlişkili Kılavuzlar** hızlı sekmesini genişletin.
1. **İlişkili Kılavuzlar** araç çubuğundan **Ekle**'yi seçin. Kılavuza yeni bir satır eklenir.
1. Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.
    ![BOM'a Kılavuz ekleme](media/instruction-guides-BOM.png "BOM'a Kılavuz ekleme")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>Kılavuzu ürün reçetesi sürümüyle ilişkilendirme

Herhangi bir [ürün reçetesi sürümüne](bill-of-material-bom.md#bom-and-formula-versions) bir kılavuz ekleyebilirsiniz.

### <a name="typical-scenario-using-bill-of-materials-versions"></a>Ürün reçetesi sürümleri kullanan tipik senaryo

Tek bir ürün reçetesi sürümüne iliştirilmiş kılavuzlar, atölye çalışanlarına genel ürün reçetesinden veya bunun diğer sürümlerinden farklı bir ürün reçetesi sürümü için malzemenin nasıl hazırlanacağını ve işleneceğini açıklayan yönergeler sağlar.

> [!NOTE]
> Kılavuzlar, şu anda bireysel BOM satırlarına eklenemez.

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>Ürün reçetesi sürümüne Kılavuz ekleme

Ürün reçetesi sürümüne Kılavuz eklemek için:

1. **Ürün bilgi yönetimi \> Ürün reçeteleri ve formüller \> Ürün reçetesi**'ne gidin.
1. Kılavuza atamak istediğiniz sürümü içeren BOM'u açın.
1. Üst hızlı sekmenin yukarısındaki **Başlık** sekmesini açın.
1. **BOM sürümleri** hızlı sekmesinde, Kılavuz atamak istediğiniz sürümü seçin.
1. **BOM sürümleri** araç çubuğunda **İlişkili Kılavuzlar**'ı seçin.
    ![Seçili BOM sürümüyle ilişkilendirilen Kılavuzları açma](media/instruction-guides-BOMVersion.png "Seçili BOM sürümüyle ilişkilendirilen Kılavuzları açma")
1. BOM sürümünüz için **İlişkili Kılavuzlar** sayfası açılır.
1. Eylem bölmesinde, kılavuza yeni satır eklemek için **Ekle**'yi seçin.
1. Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.
    ![BOM sürümüne Kılavuz ekleme](media/instruction-guides-BOMVersionAddGuide.png "BOM sürümüne Kılavuz ekleme")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>Kılavuzu rotayla ilişkilendirme

Herhangi bir [rotaya](routes-operations.md) kılavuz ekleyebilirsiniz.

### <a name="typical-scenario-using-routes"></a>Rotaları kullanan tipik senaryo

Rotalar genellikle, belirli bir serbest bırakılan ürünün bir ürün reçetesine veya ürün reçetesi sürümüne dayalı olup, bir dizi kaynak veya kaynak grubu ile ilgili olarak nasıl üretileceğini belirtmek için kullanılır.

İlgili üretim işlemiyle ilgili adım adım yönergeler sağlamak için bir rotaya bir kılavuz atayın.

### <a name="add-a-guide-to-a-route"></a>Rotaya Kılavuz ekleme

Rotaya Kılavuz eklemek için:

1. **Üretim denetimi \> Tüm rotalar**'a gidin.
1. Kılavuz atamak istediğiniz rotayı açın.
1. **İlişkili Kılavuzlar** hızlı sekmesini genişletin.
1. **İlişkili Kılavuzlar** araç çubuğundan **Ekle**'yi seçin. Kılavuza yeni bir satır eklenir.
1. Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.
    ![Rotaya Kılavuz ekleme](media/instruction-guides-Route.png "Rotaya Kılavuz ekleme")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>Kılavuzu rota sürümüyle ilişkilendirme

Herhangi bir [rota sürümüne](routes-operations.md#route-versions) kılavuz ekleyebilirsiniz.

### <a name="typical-scenario-using-route-versions"></a>Rota sürümlerini kullanan tipik senaryo

Rota sürümleri genellikle, varolan bir rotaya dayalı olarak üretim süreçlerinin varyantlarını belirtmek için kullanılır. Her rota sürümüne farklı Kılavuzlar atayabilirsiniz.

### <a name="add-a-guide-to-a-route-version"></a>Rota sürümüne Kılavuz ekleme

Rota sürümüne Kılavuz eklemek için:

1. **Üretim denetimi \> Tüm rotalar**'a gidin.
1. Kılavuz atamak istediğiniz rotayı açın.
1. **Sürümler** hızlı sekmesinde, Kılavuz atamak istediğiniz sürümü seçin.
1. **Sürümler** araç çubuğunda **İlişkili Kılavuzlar**'ı seçin.
    ![Seçili rota sürümüyle ilişkilendirilen Kılavuzları açma](media/instruction-guides-RouteVersion.png "Seçili rota sürümüyle ilişkilendirilen Kılavuzları açma")
1. BOM sürümünüz için **İlişkili Kılavuzlar** sayfası açılır.
1. Eylem bölmesinde, kılavuza yeni satır eklemek için **Ekle**'yi seçin.
1. Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.
    ![Rota sürümüne Kılavuz ekleme](media/instruction-guides-RouteVersionAddGuide.png "Rota sürümüne Kılavuz ekleme")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>Kılavuzu rota operasyonu ilişkisiyle ilişkilendirme

Herhangi bir [rota operasyonu ilişkisine](routes-operations.md#operation-relations) kılavuz ekleyebilirsiniz.

### <a name="typical-scenario-using-route-operation-relations"></a>Rota operasyonu ilişkilerini kullanan tipik senaryo

Operasyon ilişkileri, bir ürün işlemine ve ilgili operasyonlarına rehberlik eklemenin en belirgin yoludur. Bir rotadaki her operasyon için rehberlik belirtebilir ve belirli maddeler, yapılandırmalar ve daha fazlası gibi bir rotaya ilişkin herhangi bir ilişki bağlamı türü için farklı bir kılavuz belirtebilirsiniz. Ayrıca, kılavuzun operasyonda uyguladığı aşamaları (kurulum, kuyruğa alma, işleme veya taşıma gibi) belirtebilirsiniz.

> [!NOTE]
> Bir rotanın çeşitli operasyon ilişkileri için kılavuzlar belirtirseniz, bu kılavuzlar arasından yalnızca en belirli ilişkilerden gelen kılavuz oluşturulan iş için atölyede gösterilir.

### <a name="add-a-guide-to-a-route-operation-relation"></a>Kılavuzu rota operasyonu ilişkisine ekleme

Kılavuzu rota operasyonu ilişkisine eklemek için:

1. **Üretim denetimi \> Tüm rotalar**'a gidin.
1. Kılavuz atamak istediğiniz rotayı açın.
1. Eylem Bölmesinde, **Rota** sekmesini açın ve **Yönet** grubundan **Rota ayrıntıları**'nı seçin.
1. **Rota ayrıntıları** sayfası, seçtiğiniz rota için açılır.
1. Üst kılavuzda, kılavuzluk sağlamak istediğiniz işlemi seçin.
1. Alt kılavuzda, belirli bir ilişki (veya genel **Tümü** ilişkisini) seçin.
    ![Bir operasyon ve ardından bir ilişki seçin](media/instruction-guides-RouteOperationRelation.png "Bir operasyon ve ardından bir ilişki seçin")
1. Alt kılavuzun üzerinde, **İlişkili kılavuzlar** sekmesini açın. ![İlişkili Kılavuzlar sekmesi](media/instruction-guides-RouteOperationRelation-AddGuide.png "İlişkili Kılavuzlar sekmesi")
1. Kılavuza yeni bir satır eklemek için, alt kılavuzun üstündeki araç çubuğundan **Ekle**'yi seçin.
1. Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin. Satırın geri kalanında, seçili Kılavuzun kullanılabilir olması gereken her bağlamın onay kutusunu seçin.

> [!NOTE]
> Her bir operasyonun her aşaması için bir veya daha fazla kılavuz ekleyebilirsiniz.

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>Atölye yürütme arabiriminden kılavuz seçme

Bir çalışan atölye yürütme arabiriminde bir iş listesi açtığında, Supply Chain Management gösterilen işler için ilgili kılavuzları bulur. İlgili kılavuzları görüntülemek için **Kılavuzlar** düğmesini kullanın.

![Atölye yürütme arabirimindeki Kılavuzlar düğmesi](media/instruction-guides-Shopfloor1.png "Atölye yürütme arabirimindeki Kılavuzlar düğmesi")

Daha sonra HoloLens'e yerleştirin ve QR kodunu kullanarak ve ilgili Kılavuzu etkinleştirerek ilgili kılavuza erişin.

![HoloLens kullanarak kılavuzlara erişmek için QR kodu](media/instruction-guides-Shopfloor2.png "HoloLens kullanarak kılavuzlara erişmek için QR kodu")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>Kılavuz seçme mantığını çözme

Aşağıdaki üretim verilerine Kılavuzlar ekleyebilirsiniz:

- [Kaynaklar](#resources)
- [Kaynak grupları](#resource-groups)
- [Serbest bırakılan ürünler](#released-products)
- [Formüller](#formulas)
- [Formül sürümleri](#formula-versions)
- [Ürün reçeteleri (BOM'lar)](#bom)
- [BOM sürümleri](#bom-versions)
- [Rotalar](#routes)
- [Rota sürümleri](#route-versions)
- [Rota operasyonu ilişkileri](#route-operation-relations)

Supply Chain Management üretim katı için işleri oluşturduğunda, ilgili Kılavuzları bu kaynaklardan alır. Aşağıdaki önemli kurallara dikkat edin.

- Bir rotaya veya üretim emrine ürün reçetesi sürümü veya formül sürümü eklerseniz, bu sürüme iliştirilmiş tüm Kılavuzlar ve ayrıca o sürümün ana ürün reçetesine veya formülüne eklenen kılavuzlar işte gösterilir.
- Bir üretim emrine rota sürümü eklerseniz, bu sürüme iliştirilmiş tüm Kılavuzlar ve ayrıca o sürümün ana reçetesine eklenen kılavuzlar işte gösterilir.
- *Tümü* ilişkisi içeren birkaç rota operasyonu ilişkisi tanımlarsanız ve bunlara Kılavuzlar atarsanız, iş için yalnızca en belirgin ilişkideki Kılavuzlar gösterilir.  

![İlgili kılavuzları çözümlemeyle ilgili diyagram](media/instruction-guides-Resolve.png "İlgili kılavuzları çözümlemeyle ilgili diyagram")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]