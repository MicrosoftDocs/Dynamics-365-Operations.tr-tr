---
title: Bütçe planlamaya genel bakış
description: Bu konu bütçe planlamasını açıklamaktadır. Bütçe planlamayı yapılandırmanıza ve bütçe planlama süreçlerini ayarlamanıza yardımcı olabilecek bilgiler içerir.
author: panolte
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14a5e1cea5a249b6087ef87560dd06bc026dd129
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822143"
---
# <a name="budget-planning-overview"></a>Bütçe planlamaya genel bakış

[!include [banner](../includes/banner.md)]

Bu konu bütçe planlamasını açıklamaktadır. Bütçe planlamayı yapılandırmanıza ve bütçe planlama süreçlerini ayarlamanıza yardımcı olabilecek bilgiler içerir.

## <a name="overview-of-budget-planning"></a>Bütçe planlamaya genel bakış

Bir organizasyon, bütçe planlamayı yapılandırabilir ve ardından bütçe hazırlama ilkelerini, prosedürlerini ve gereksinimlerini karşılamak için bütçe planlama işlemleri ayarlayabilir. Microsoft Dynamics 365 Finance'da kullanılan kavramları ve terimleri anladığınızda bütçe planlamayı kuruluşununda daha kolay ve etkin şekilde uygulayabilirsiniz.

### <a name="key-terms"></a>Önemli terimler

- **Bütçe planlama süreçleri** – Bütçe planlama süreçleri bütçe planlarının bütçe planlayan organizasyonun hiyerarşisinde nasıl güncelleştirileceğini, yönlendirileceğini, gözden geçirileceğini ve onaylanacağını belirler. Bir bütçe planlama süreci, bir tüzel kişilik üzerinden bir bütçe döngüsü ve bir organizasyon ile ilişkilendirilir.
- **Bütçe planları** – Bütçe planları bir bütçe döngüsü için bütçe verilerini içerir. Çeşitli amaçlarla kullanılan birden fazla bütçe planına sahip olabilirsiniz. Örneğin, farklı kuruluş birimleri için bütçe tutarları oluşturmak üzere bütçe planlarını kullanabilirsiniz. Bunları karşılaştırma yapmak ve bilgiye dayalı kararlar almak için de kullanabilirsiniz.
- **Bütçe planı senaryoları** – Bütçe planı senaryoları, bütçe planları için veri kategorilerini tanımlar. Bütçe plan senaryolarını parasal sınıflar ve miktar gibi diğer ölçü birimi sınıflarını destekleyecek şekilde tanımlayabilirsiniz. Parasal bütçe planı senaryolarına örnekler, "Departman önceki yıl" ve "Departman talepleri"ni içerir. Miktarları kullanan bütçe planı senaryolarına örnekler, "Önceki yıl destek aramaları" ve "Tam zamanlı eşdeğeri (FTE) sayısı"nı içerir.
- **Bütçe planlama aşamaları** – Bütçe planlama aşamaları, bütçe planının başlangıçtan son onaya kadar olan süreçte takip edeceği adımları tanımlar. Bütçe planlama aşamaları bütçe planlama iş akışlarında düzenlenir.
- **Bütçe planlama iş akışları** – Bütçe planlama iş akışları, bütçe planlama aşamalarını içerir ve bunları tanımlar. Bütçe planlama iş akışları, bütçeleme iş akışları ile ilişkilidir. Bütçeleme iş akışları, bütçe planlarını bütçe planlama aşamalarıyla taşıyan otomatik ve manuel süreçlerden meydana gelir.

[![Bütçe planlama terminolojisi](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="typical-tasks"></a>Tipik görevler

Bütçe planlamayı şu görevleri gerçekleştirmek için kullanabilirsiniz:

- Bir bütçe döngüsü için beklenen geliri ve harcamaları tanımlamak üzere bütçe planları oluşturun.
- Birden fazla senaryo için bütçe planlarını analiz edin ve güncelleştirin.
- Bütçe planlarını çalışma sayfaları, gerekçe belgeleri ve diğer eklerle birlikte gözden geçirme ve onay aşamalarına yönlendirin.
- Kuruluşun bir alt düzeyindeki birden fazla bütçe planını daha yüksek bir düzeydeki tek bir ana bütçe planına birleştirin. Ayrıca, kuruluşun daha yüksek bir düzeyinde tek bir bütçe planı geliştirebilir ve bu bütçeyi daha düşük düzeylere atayabilirsiniz.

Bütçe planlama diğer modüllerle tümleştirilmiştir. Bu nedenle önceki bütçelere, fiili harcamalara, sabit kıymetlere ve İnsan kaynaklarına ait bilgileri dahil edebilirsiniz. Bütçe planlama ayrıca Microsoft Excel ve Microsoft Word ile de tümleşik olduğundan, bu programları kullanarak bütçe planlama verileri ile çalışabilirsiniz. Örneğin, bir bütçe yöneticisi bir bütçe planı senaryosundaki bir departmanın bütçe talebini bir Excel çalışma sayfasına aktarabilir. Veriler daha sonra çalışma sayfasında analiz edilebilir, güncelleştirilebilir ve çizelge ile gösterilebilir ve ardından bütçe planı satırlarına geri yayınlanabilir.

## <a name="configuring-budget-planning"></a>Bütçe planlamasını yapılandırma

Dynamics 365 Finance sürüm 10.0.9'da (Nisan 2020) kullanıma sunulan işlevler arasında Excel'de varolan kayıtları güncelleştirmek ve sonra bunları istemciye geri yayımlamak için **Yayımla** düğmesini kullandığınızda performansın artırılmasına yardımcı olacak bir özellik bulunur. Bu özellik güncelleştirme işlemini hızlandırır ve aynı zamanda birçok kaydı aynı anda güncelleştirdiğinizde bir güncelleştirmenin engellenme olasılığını azaltmaya yardımcı olur. Bu işlevi kullanılabilir hale getirmek için **Özellik yönetimi** çalışma alanına gidin ve **Bütçeleme** altından **Performans için bütçe planlama sorgusu iyileştirmesi**'ni açın. Bu özelliği açmanız önerilir.

**Bütçe planlama yapılandırma** sayfası, bütçe planlama oluşturmak için gerekli olan ayarların birçoğunu içerir. Aşağıdaki bölümlerde bütçe planlama yapılandırılırken dikkate almanız gereken bazı önemli faktörler açıklanmıştır. Yapılandırmayı tamamladıktan sonra bütçe planlama sürecini ayarlayabilirsiniz.

### <a name="budget-planning-schema-optional"></a>Bütçe planlama şeması (isteğe bağlı)

Bu isteğe bağlı, ancak önerilen ilk adım kuruluşunuzun bir bütçeyi formüle etme prosedürünü gösteren bir şema oluşturmaktır. Bu şemayı oluşturmak istediğiniz herhangi bir yöntemini kullanabilirsiniz.

Aşağıdaki şekilde, farklı organizasyon düzeyleri için ayrı bütçe planlama iş akışlarının oluşturulduğu genel bir örnek gösterilmiştir. Aşamalar her bir iş akışında tanımlanır ve bütçe verilerini tutmak için her bir aşamaya özel senaryolar atanır. Görevler, verilerin bir aşamadan diğerine taşınması için tamamlanır. Örneğin, tutarlar farklı hesaplara, onaylara veya diğer gözden geçirmelere atanabilir veya bunlar altında birleştirilebilir. Bu örnekte, italik yazılan metin bu aşamada düzenlenemeyen bir senaryoyu ve geçmişe ait olan veya daha erken bir aşamada onaylanmış olan ve bu nedenle değiştirilemeyen verileri gösterir.

[![Bütçe planlama genel şema](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Aşağıdaki şekilde, şirket genel merkezlerinin başlangıç bütçe temel tutarlarını tahmin ettiği ve bunları Satış departmanlarına dağıttığı bir örnek gösterilmektedir. Satış departmanları ardından tahminlerini kestirir ve bunları genel merkezlere gönderir ve burada bütçe yöneticisi tahminleri bir araya getirir ve düzenler. Son olarak, bütçe yöneticisi, ayarlanmış bütçe tutarlarını gözden geçirilmesi, nihai düzenlemeler ve onay için mali işler müdürüne (CFO) gönderir.

[![Bütçe planlama şeması örneği](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

### <a name="organization-hierarchy-for-budget-planning"></a>Bütçe planlama için organizasyon hiyerarşisi

**Kuruluş hiyerarşisi** sayfasında, bir kuruluş hiyerarşisini her bir bütçe planlama süreci için bir bütçe planlama hiyerarşisi olarak belirtebilirsiniz. Bütçe planlama hiyerarşisi, başka amaçlar için kullanılan standart organizasyon hiyerarşisiyle eşleşmek zorunda değildir. Bu hiyerarşi, verilerin toplanması ve dağıtılması için kullanıldığından, farklı bir yapıya sahip olmasını isteyebilirsiniz. Bu örnek şemada, Satış departmanları Bütçe ve Finans departmanlarını içeren bir genel merkez düzeyi altındadır. Bu yapı, Satış departmanlarına yönelik işlemlerin yönetilmesi için kullanılan yapı büyük olasılıkla farklı olacaktır. Her bir bütçe planlama sürecine sadece tek bir organizasyon hiyerarşisi atanabilir.

Daha fazla bilgi için bkz. [Organizasyonlar ve organizasyon hiyerarşileri](../../fin-and-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Kullanıcı güvenliği

Bütçe planlama, kullanıcı izinlerinin tanımlanması için iki güvenlik modelinden birini takip edebilir. Güvenlik modelini belirtmek için, **Bütçe planlama yapılandırma** sayfasından bir bütçe planlama parametresi ayarlarsınız.

### <a name="budget-planning-workflows-stages"></a>Bütçe planlama iş akışları aşamaları

Bütçe planlama iş akışları, bütçe planlarının oluşturulması ve geliştirilmesi için bütçeleme iş akışlarıyla birlikte kullanılır.

Bir bütçe planlama iş akışı bir bütçe planının geçtiği, belirlenen bir aşama grubundan meydana gelir. Her bir bütçe planlama iş akışı bir bütçeleme iş akışı ile ilişkilidir. Bütçeleme iş akışları, Dynamics 365 Finance'ta kullanılan iş akışı türlerinden biridir. Gözden geçirme ve onay için çalışma sayfaları, gerekçeler ve ekler ile birlikte bütçe planlarını kuruluşta yönlendirir.

**Bütçe planlama yapılandırması** sayfasının **İş akışı aşamaları** bölümünde bütçe planlama iş akışı oluşturursunuz. Burada, kullanılacak aşamaları ve bütçeleme iş akışını seçebilir ve ek ayarları yapılandırabilirsiniz.

Bir bütçeleme hiyerarşisinin her bir düzeyi için bir bütçe planlama iş akışının oluşturulması iyi bir uygulamadır. Ardından, bütçe planlama iş akışındaki aşamalara karşılık gelen öğeleri içeren bir bütçeleme iş akışı atarsınız. Bu konunun başında verilen örnek şemada, Satış departmanları için bir bütçe planlama iş akışı ve genel merkezler için başka bir bütçe planlama iş akışı oluşturulacaktır. Bir bütçeleme iş akışı, bütçe planlarını aşamalardan geçirir.

**Bütçeleme iş akışları** sayfasında bütçe planlama için bütçeleme iş akışı oluşturursunuz. Bu süreç, diğer iş akışlarının oluşturulması için kullanılan sürece benzerdir. Aşağıdaki şekilde Genel merkez için bir iş akışı örneği gösterilmiştir.

[![Bütçe planlama için bütçeleme iş akışı](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

İş akışı aşağıdaki öğeleri içerir:

- Satış departmanlarına tahsisat ve gönderimlerinin toplamı
- Bütçe yöneticisi incelemesi
- CFO onayı
- Bütçe planlama iş akışının her aşaması arasında hazırlama geçişleri

**Bütçe planlama yapılandırma** sayfasının **İş akışı aşamaları** sayfasında bütçeleme iş akışını her bir bütçe planlama iş akışına atarsınız.

### <a name="parameters-scenarios-and-stages"></a>Parametreler, senaryolar ve aşamalar

**Bütçe planlama yapılandırma** sayfasındaki başlangıç ayarları, daha sonraki yapılandırma adımları için bir takım yapı taşları oluşturmanıza izin verir:

- **Parametreler** – Parametreler, bütçe planlarına uygulamak istediğiniz güvenlik kurallarını kullanıcılar bütçe planı senaryosundaki tutarları ayrıntılı şekilde incelerken kullanılması gereken varsayılan mali boyutları tanımlar.
- **Senaryolar** – Senaryolar, bütçe planları için istediğiniz veri kategorilerini kapsar. Bütçe plan senaryolarını parasal sınıflar ve miktar gibi diğer ölçü birimi sınıflarını destekleyecek şekilde tanımlayabilirsiniz. Bir bütçe planında, senaryolar bütçe planlama verilerinin bir sürümünü temsil eder. Parasal bütçe planı senaryolarına örnekler "Önceki yıl satışları" ve "İmzalanan sözleşmeler"i içerir. Tutarlar kullanan senaryolara örnekler, "Satış çağrısı sayısı" ve "Tam zamanlı eşdeğer (FTE) sayısı"nı içerir.
- **Aşamalar** – Aşamalar bütçe planının başlangıçtan son onaya kadar olan süreçte takip edeceği adımları tanımlar. Bütçe planlama aşamalarına örnekler "Genel merkez özeti", "CFO İncelemesi" ve "Nihai" aşamalarından meydana gelir.

### <a name="allocation-schedules"></a>Tahsisat zamanlamaları

Bütçe planlamada, bütçe planlama satırlarındaki tutarları veya miktarları bir senaryodan başka bir senaryoya veya hatta aynı senaryoya atayabilirsiniz. Örneğin, bir senaryodaki mali boyutlarda veya tutar tarihlerinde değişiklikler yapmak istiyorsanız tutarları veya miktarları aynı senaryoya tahsis edebilirsiniz. Bir tahsisat işlemi bir bütçe planı içinde veya bir bütçe planından diğerine gerçekleştirilebilir.

Tahsisat programları, iş akışının işlenmesi sırasında otomatik olarak bütçe planı satırlarını tahsis eder. Tahsisat işlemlerini **Tahsisat yöntemi** listesinde bulunan, aşağıdaki yöntemlerden herhangi birini kullanarak yapabilirsiniz:

- **Dönemler arasında tahsis et** – Bütçe planı satırlarını kaynak bütçe planı senaryosundan hedef senaryodaki dönemler arasında tahsis etmek için bir dönem tahsisat anahtarı kullanırsınız.

    > [!NOTE]
    > Dönemler arasında tahsisat yapmadan önce mutlaka **Dönem tahsisat kategorileri** sayfasında dönem tahsisat anahtarlarını ayarlamanız gerekir.

- **Boyutlara tahsis et** – Bütçe planı satırları kaynak bütçe planı senaryosundan hedef senaryodaki mali boyutlara tahsis edilir.

    > [!NOTE]
    > Boyutlara tahsis etmeden önce mutlaka **Bütçe tahsisat koşulları** sayfasında bütçe tahsisat koşullarını ayarlamanız gerekir.

- **Toplama** – Bütçe planı satırları, ilgili bütçe planlarındaki kaynak bütçe planı senaryodan ana bütçe planındaki hedef senaryoya toplanır.
- **Dağıtma** – Bütçe planı satırları, ana bütçe planındaki kaynak bütçe planı senaryodan ilişkili bütçe planlarındaki hedef senaryoya dağıtılır.
- **Genel muhasebe tahsisat kurallarını kullan** – Bütçe planı satırları, seçilen genel muhasebe tahsisat kuralına dayalı olarak kaynak bütçe planı hedef senaryoya dağıtılır.
- **Bütçe planından kopyala** – Tahsisatın kaynağı olarak kullanılmak üzere başka bir bütçe planı seçebilirsiniz.

### <a name="stage-allocations"></a>Aşama tahsisatları

Aşama tahsisatları, iş akışının işlenmesi sırasında bütçe planı satırlarının otomatik olarak atanması için kullanılır. Aşama tahsisatları kullanıldığında hedef senaryodaki bütçe planı satırları, bütçe planını hazırlayan veya gözden geçiren kişinin müdahalesi olmaksızın oluşturulabilir ve değiştirilebilir.

Bir aşama tahsisatı kurduğunuzda, bütçe planlama iş akışını ve aşamasını tahsisat programıyla ilişkilendirirsiniz. Bütçe planlama iş akışı mutlaka **Bütçe planlama aşama tahsisatı** otomatik iş akışı görevini kullanan bir bütçeleme iş akışıyla ilişkilendirilmelidir. İş akışı, belirtilen aşamaya ulaştığında tahsisat otomatik olarak gerçekleşir. Bu otomatik görev yeni bir senaryoda bütçe planı oluşturulması için kullanılabilir.

Bu konunun başında verilen örnek şemada, bir bütçe planındaki tutarların ve genel merkez "Temel" aşamasındaki senaryoların başka bütçe planına ve Satış departmanlarının "Tahmin" aşamasındaki senaryolara aktarılması için bir tahsisat gerçekleştirilmektedir. Aşağıdaki şekilde örnek şemanın ilgili bölümü gösterilmiştir.

[![Aşama tahsisatı](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Ek olarak, örnek şemada Satış departmanları için "Gönderilen" aşamasındaki bütçe planlarından ve senaryolardan Genel merkez "Toplama" aşamasındaki bir ana plana bir toplama işlemi gerçekleştirilmektedir. Aşağıdaki şekilde örnek şemanın ilgili bölümü gösterilmiştir.

[![Toplam](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Öncelikler

Kurmuş olduğunuz bütçe planları için kategoriler ve hedefler tanımlama üzere, isteğe bağlı olarak bütçe planı öncelikleri kullanabilirsiniz. Birkaç bütçe planını organize etmek, sınıflandırmak ve değerlendirmek için de öncelikleri kullanabilirsiniz. Örneğin, işçi sağlığı ve iş güvenliği için bir bütçe planlama önceliği oluşturabilir ve ardından bu önceliğe atanmış bütçe planlarını değerlendirebilirsiniz. Ayrıca, bir derecelendirmeyi göstermek üzere bütçe planlarınıza numara atayabilirsiniz.

### <a name="columns-and-layouts"></a>Sütunlar ve düzenler

Bütçe planında, bütçe rakamları satırlar ve sütunlar olarak görünür. Öncelikle bu sütunları tanımlamanız ve ardından sütunların sunumu için bir düzen oluşturmanız gerekir.

Bir sütunu tanımlamak için bir bütçe planı senaryosu seçin. Bu senaryodaki satır tutarları bütçe planında gösterilir. Tutarı filtrelemek için bir dönem seçebilirsiniz ve ayrıca genel muhasebe hesabına dayalı olarak filtreler uygulayabilirsiniz.

Bir düzen tanımlarken, göstermek istediğiniz bütçe planı satırlarını oluşturmak için bir genel muhasebe boyut kümesi seçin ve düzen öğeleri olarak sütunları seçin. Birden fazla düzen oluşturabilirsiniz, böylece bir bütçe planı, bütçe planlama sürecinin farklı aşamalarında istediğiniz verileri gösterir.

Bütçe tutarları sütunlarına ek olarak proje, teklif edilen proje, kıymet ve önerilen kıymet alanları için bütçe planında sütunlar tanımlayabilirsiniz. Ayrıca, bütçelenen pozisyonlar için de bir sütun tanımlayabilirsiniz. Bu seçenek, kişisel bütçeleri analiz etmeniz gerektiği durumlarda kullanışlıdır.

Örnek şema için, "PY Satışları," "Sözleşmeler" ve "Tahmin" senaryoları için sütunlar oluşturmak isteyebilirsiniz. (Aşağıdaki şekilde örnek şemanın ilgili bölümü gösterilmiştir.) Ardından, mali yılın her bir çeyreği için bu senaryoların birini veya tümünü ayrı sütunlara dağıtabilirsiniz, böylece Satış departmanı yöneticisi her bir dönem için tahmin tutarlarını doğru şekilde girebilir.

[![Sütunlar](./media/columns.png)](./media/columns.png)

Her bir düzen öğesinin (sütunun) düzenlenebilir olup olmayacağını ve bu düzen için oluşturulan bir çalışma sayfası şablonunda mevcut olup olmayacağını da belirtebilirsiniz. Örnek şemada, "Tahmin" aşaması için kullanılan düzende "Tahmin" sütunları düzenlenebilirken, "PY Satışları" ve "Sözleşmeler" sütunları salt okunurdur.

> [!NOTE]
> [Bütçe planlama düzenini genişlet](./extending-budget-planning-layout.md) bölümündeki adımları izleyerek bütçeleme planlamasını genişletmediğiniz sürece, varsayılan olarak 36 sütunla sınırlandırılırsınız.

### <a name="templates"></a>Şablonlar

**Bütçe planlama yapılandırması** sayfasının **Düzenler** bölümünde her düzen için bir Excel şablonu oluşturabilir, görüntüleyebilir veya yükleyebilirsiniz. Bu şablonlar ilave analizler, çizelgeler ve veri giriş özellikleri sunulması için her bir bütçe planıyla ilişkilendirilir.

Bir şablon oluşturulduğunda düzen kilitlenir ve düzenlenemez. Bu kilitleme özelliği, şablon formatının bütçe planı düzenine uygun olmasını ve aynı verileri içermesini sağlar. Bir şablon oluşturulduğunda görüntülenebilir ve düzenlenebilir. Örneğin, şablona çizelgeler ekleyebilir veya bunların görünümünü özelleştirebilirsiniz.

> [!NOTE]
> Şablon, kullanıcının erişimi olan bir konuma kaydedilmelidir, böylece düzenleme tamamlandıktan sonra düzene yüklenebilir. Bu şekilde şablon, düzeni kullanan bütçe planlarıyla birlikte kullanılacaktır.

### <a name="descriptions"></a>Açıklamalar

**Düzenler** bölümünde bir düzene dahil edilen bir mali boyutun adının görüntülenmesi için açıklamalar atayabilirsiniz. Örneğin, bir kuruluş bir bütçe planında ana hesap numarasının yanında ana hesabın adını göstermek isteyebilir. Ancak, ekrandaki karışıklığı önlemek için diğer finansal boyutların adlarını atlamak isteyebilir.

## <a name="setting-up-budget-planning-processes"></a>Bütçe planlama süreçleri oluşturma

Bütçe planlama yapılandırmayı bitirdikten sonra **Bütçe planlama süreci** sayfasında bütçe planlama süreçlerini ayarlayabilirsiniz. Bütçe planlama süreçleri, bütçe planlarının bütçe planlayan organizasyonun hiyerarşisinde nasıl güncelleştirileceğini, yönlendirileceğini, gözden geçirileceğini ve onaylanacağını belirleyen kurallar kümesidir.

Her bir bütçe planlama süreci için, öncelikle bir bütçe döngüsü ve bir genel muhasebe seçersiniz. Her bir bütçe planlama süreci sadece tek bir bütçe dönüsü ve bir genel muhasebe ile ilgilidir. Ardından, **Bütçe planlama süreci yönetimi** hızlı sekmesinden bütçe kuruluş hiyerarşisini seçin ve kılavuzda görüntülenen kuruluştaki tüm sorumluluk merkezlerine bir bütçe planlama iş akışı atayın.

Benzer sorumluluk merkezleri için bütçe planlama iş akışı atamak veya bunu değiştirmek için **İş akışı ata** öğesini seçin ve hedeflenecek organizasyon türünü ve kullanılacak bütçe planlama iş akışını seçin. Her bir bütçe planlama iş akışıyla ilişkilendirilen bütçeleme iş akışı kimliği otomatik olarak kılavuza eklenir.

**Bütçe planlama aşaması kuralları ve düzenleri** hızlı sekmesinde aşama kuralları ve şablonları tanımlarken, her bir bütçe planlama aşaması için farklı bir kural kümesi ve varsayılan düzenler tanımlayabilirsiniz.  Örneğin, Satış departmanları için "Tahmin" aşaması, kullanıcıların bir bütçe planındaki satırları değiştirmesine izin verebilir, ancak kullanıcıların satır eklemesini engelleyebilir. "Gönderildi" aşaması, kullanıcıların satırları görüntülemesine izin verebilir, ancak kullanıcılar satır ekleyemez ve bunları değiştiremez, çünkü bu aşamadaki çalışma tamamlanmıştır ve bütçe planlarındaki değişikliklerin mutlaka önlenmesi gerekir. Bütçe planları için kullanılabilecek düzenleri seçmek için **Diğer düzenler** öğesini seçin.

İsteğe bağlı olarak, **Bütçe planı öncelik kısıtlamaları** hızlı sekmesinden bütçe planlama önceliklerini de seçebilirsiniz. Öncelikler daha sonra bütçe planlarında seçilebilir.

Son adım, **Eylemler** menüsünü kullanarak bütçe planlama sürecini etkinleştirmektir. Bir bütçe planlama süreci etkinleştirilinceye kadar kullanılamaz.

Ayrıca, mevcut bir süreci kopyalayarak yeni bir süreç oluşturmak için **Eylemler** menüsünü kullanabilirsiniz. Bu özellik, her bütçe döngüsü için aynı süreç akışını takip eden ve bunlar üzerinde birkaç değişiklik yapan veya hiçbir değişiklik yapmayan organizasyonlar için kullanışlıdır.

**Eylemler** menüsündeki bir diğer kullanışlı komut da **Bütçe sürecinin durumunu göster** komutudur. Bu komut, planların iş akışı durumu, tutara ve birime göre özetler ve bütçe planlarına tek tıklamayla ulaşma gibi ilgili verilerle birlikte, bir süreç içindeki bütçe planlarını grafiksel olarak gösterir.

[![Bütçe planlama süreci durumu](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]