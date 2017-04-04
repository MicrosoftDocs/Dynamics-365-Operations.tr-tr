---
title: "Bütçe planlama genel bakış"
description: "Bu makale bütçe planlamayı tanıtır ve bütçe planlamayı yapılandırmanıza ve bütçe planlama süreçleri oluşturmanıza yardımcı olacak bilgileri içerir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: d5073958f8ffe90e47dc10cde67e081420e559a1
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-overview"></a>Bütçe planlama genel bakış

Bu makale bütçe planlamayı tanıtır ve bütçe planlamayı yapılandırmanıza ve bütçe planlama süreçleri oluşturmanıza yardımcı olacak bilgileri içerir.

<a name="overview-of-budget-planning"></a>Bütçe planlamaya genel bakış
---------------------------

Bir organizasyonun uygulayacağı bütçeleri hazırlanırken, bütçe planlama gerçekleştirirsiniz. Bir organizasyon, bütçe planlamayı yapılandırabilir ve ardından bütçe hazırlama ilkelerini, prosedürlerini ve gereksinimlerini karşılamak için bütçe planlama işlemleri ayarlayabilir. 

Kavramları ve Microsoft Dynamics 365 içinde işlemleri için kullanılan terminolojiyi anlamanız, bütçe planlama kuruluşunuza uygulamak size daha kolay olur.

### <a name="key-terms"></a>Önemli terimler

-   **Bütçe planlama süreçleri** – Bütçe planlama süreçleri bütçe planlarının bütçe planlayan organizasyonun hiyerarşisinde nasıl güncelleştirileceğini, yönlendirileceğini, gözden geçirileceğini ve onaylanacağını belirler. Bir bütçe planlama süreci, bir tüzel kişilik üzerinden bir bütçe döngüsü ve bir organizasyon ile ilişkilendirilir.
-   **Bütçe planları** – Bütçe planları bir bütçe döngüsü için bütçe verilerini içerir. Çeşitli amaçlarla kullanılan birden fazla bütçe planına sahip olabilirsiniz. Örneğin, bütçe planları, farklı organizasyon birimleri için bütçe tutarlarının oluşturulması için kullanılabilir veya karşılaştırmalar yapmanıza ve bilinçli kararlar vermenize yardımcı olabilir.
-   **Bütçe planı senaryoları** – Bütçe planı senaryoları, bütçe planları için veri kategorilerini tanımlar. Bütçe plan senaryolarını parasal birimler ve miktar gibi diğer ölçü birimi sınıflarını destekleyecek şekilde tanımlayabilirsiniz. Parasal bütçe planı senaryolarına örnekler, Departman önceki yıl ve Departman taleplerini içerir. Miktarlar kullanan bütçe planı senaryolarına örnekler, Önceki yıl destek aramalarını ve Tam zamanlı eşdeğeri (FTE) sayısı içerir.
-   **Bütçe planlama aşamaları** – Bütçe planlama aşamaları, bütçe planının başlangıçtan son onaya kadar olan süreçte takip edeceği adımları tanımlar. Bütçe planlama aşamaları bütçe planlama iş akışlarında düzenlenir.
-   **Bütçe planlama iş akışları** – Bütçe planlama iş akışları, bütçe planlama aşamalarını içerir ve bunları tanımlar. Bütçe planlama iş akışları, Bütçeleme iş akışları ile ilişkilidir. Bütçeleme iş akışları, bütçe planlarını bütçe planlama aşamalarıyla taşıyan otomatik ve manuel süreçlerden meydana gelir.

[![Bütçe planlama terminolojisi](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="common-tasks"></a>Yaygın görevler  

Bütçe planlamayı şu görevleri gerçekleştirmek için kullanabilirsiniz:

-   Bir bütçe döngüsü için beklenen gelirleri ve harcamaları tanımlamak üzere bütçe planları oluşturun.
-   Birden fazla senaryo için bütçe planlarını analiz edin ve güncelleştirin.
-   Bütçe planlarını çalışma sayfaları, gerekçe belgeleri ve diğer eklerle birlikte gözden geçirme ve onay aşamalarına yönlendirin.
-   Organizasyonun bir alt düzeyindeki birden fazla bütçe planını organizasyonun daha yüksek bir düzeyindeki tek bir ana bütçe planına birleştirin. Ayrıca, organizasyonun daha yüksek bir düzeyinde tek bir bütçe planı geliştirebilir ve bu bütçeyi organizasyonun daha düşük düzeylerine atayabilirsiniz.

Bütçe planlama işlemleri modülleri için diğer Microsoft Dynamics 365 ile tümleşiktir. Bu nedenle, önceki bütçelere, fiili harcamalara, sabit kıymetlere ve insan kaynaklarına ait bilgi çağırabilirsiniz. Bütçe planlama ayrıca Microsoft Excel ve Microsoft Word ile de tümleşik olduğundan, bu programları kullanarak bütçe planlama verileri ile çalışabilirsiniz. Örneğin, bir bütçe yöneticisi bir bütçe planı senaryosundaki bir departmanın bütçe talebini bir Excel çalışma sayfasına aktarabilir. Veriler çalışma sayfasında analiz edilebilir, güncelleştirilebilir ve çizelge ile gösterilebilir ve ardından bütçe planı satırlarına geri yayınlanabilir.

## <a name="configuring-budget-planning"></a>Bütçe planlamasını yapılandırma
**Bütçe planlama yapılandırma** sayfası, bütçe planlama oluşturmak için ihtiyaç duyduğunuz ayarların birçoğunu içerir. Aşağıdaki bölümlerde bütçe planlama yapılandırılırken dikkate almanız gereken bazı önemli faktörler açıklanmıştır. Yapılandırmayı tamamladıktan sonra bütçe planlama sürecini ayarlarsınız.

### <a name="create-a-budget-planning-schema"></a>Bir bütçe planlama şeması oluşturma

Bu isteğe bağlı, ancak önerilen ilk adım organizasyonunuzun bir bütçeyi formüle etme prosedürünü gösteren bir şema oluşturmaktır. Bu şemayı oluşturmak istediğiniz herhangi bir yöntemini kullanabilirsiniz. Aşağıdaki şekilde, farklı organizasyon düzeyleri için ayrı bütçe planlama iş akışlarının oluşturulduğu genel bir örnek gösterilmiştir. Aşamalar her bir iş akışında tanımlanır ve bütçe verilerini tutmak için her bir aşamaya özel senaryolar atanır. Görevler, verilerin bir aşamadan diğerine taşınması için yerine getirilir. Örneğin, tutarlar farklı hesaplara, onaylara veya diğer gözden geçirmelere atanabilir veya bunlar altında birleştirilebilir. Bu örnekte, italik yazılan metin bu aşamada düzenlenemeyen bir senaryoyu ve geçmişe ait olan veya daha erken bir aşamada onaylanmış olan ve bu nedenle değiştirilemeyen verileri gösterir. 

[![Bütçe planlama genel şeması](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Aşağıdaki örnekte, şirket genel müdürlüğü tahminleri temel başlangıç bütçe tutarları ve bunları satış departmanlarına dağıtır. Satış departmanları ardından tahminlerini kestirir ve bunları genel merkezlere gönderir ve burada bütçe yöneticisi tahminleri bir araya getirir ve düzenler. Son olarak, bütçe yöneticisi, ayarlanmış bütçe tutarlarını gözden geçirilmesi, nihai düzenlemeler ve onay için CFO'ya gönderir. 

[![Bütçe planlama şeması örneği](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

###  <a name="organization-hierarchy-for-budget-planning"></a>Bütçe planlama için organizasyon hiyerarşisi

**Organizasyon hiyerarşisi** sayfasında, bir organizasyon hiyerarşisini her bir bütçe planlama süreci için bir bütçe planlama hiyerarşisi olarak belirleyebilirsiniz. Bütçe planlama hiyerarşisi, başka amaçlar için kullanılan standart organizasyon hiyerarşisiyle eşleşmek zorunda değildir. Bu hiyerarşi, verilerin toplanması ve dağıtılması için kullanıldığından, farklı bir yapıya sahip olmasını isteyebilirsiniz. Bu örnek şemada, satış departmanları bütçe ve finans departmanlarını içeren bir genel merkez düzeyi altındadır. Bu yapı, satış departmanlarına yönelik işlemlerin yönetilmesi için kullanılan yapı büyük olasılıkla farklı olacaktır. Her bir bütçe planlama sürecine sadece tek bir organizasyon hiyerarşisi atanabilir. 

Daha fazla bilgi için, bkz. [Organizasyonlar ve organizasyon hiyerarşileri](/dynamics365/operations/organization-administration/organizations-organizational-hierarchies).

### <a name="user-security"></a>Kullanıcı güvenliği

Bütçe planlama, kullanıcı izinlerinin tanımlanması için iki güvenlik modelinden birini takip edebilir. Güvenlik modelini belirtmek için, **Bütçe planlama yapılandırma** sayfasından bir bütçe planlama parametresi ayarlarsınız.

### <a name="budget-planning-workflows-stages"></a>Bütçe planlama iş akışları aşamaları

Bütçe planlama iş akışları, bütçe planlarının oluşturulması ve geliştirilmesi için Bütçeleme iş akışlarıyla birlikte kullanılır.

Bir bütçe planlama iş akışı bir bütçe planının geçtiği, belirlenen bir aşama grubundan meydana gelir. Her bir bütçe planlama iş akışı bir Bütçeleme iş akışı ile ilişkilidir. Bütçeleme iş akışları iş akışı işlemleri için kullanılan Microsoft Dynamics 365 türlerini biridir. Bütçeleme iş akışları, gözden geçirme ve onay için çalışma sayfaları, gerekçeler ve ekler ile birlikte bütçe planlarını organizasyonda yönlendirir. 

**Bütçe planlama yapılandırma** sayfasının**İş akışı aşamaları** bölümünde bütçe planlama iş akışı oluşturursunuz. Burada, kullanılacak aşamaları ve Bütçeleme iş akışını seçebilir ve ayrıca ek ayarları yapılandırabilirsiniz. 

Bir bütçeleme hiyerarşisinin her bir düzeyi için bir bütçe planlama iş akışının oluşturulması iyi bir uygulamadır. Ardından, bütçe planlama iş akışındaki aşamalara karşılık gelen öğeleri içeren bir Bütçeleme iş akışı atarsınız. Bu makalenin başında verilen örnek şemada, satış departmanları için bir bütçe planlama iş akışı ve genel merkezler için başka bir bütçe planlama iş akışı oluşturulacaktır. Bir Bütçeleme iş akışı, bütçe planlarını aşamalardan geçirir. 

**Bütçeleme iş akışları** sayfasında bütçe planlama için Bütçeleme iş akışı oluşturursunuz. Bu işlem Microsoft Dynamics 365 işlemleri için de diğer iş akışları oluşturma süreci benzer. Aşağıdaki şekilde bir Genel merkez iş akışı örneği gösterilmiştir. 

[![Bütçe planlama, bütçeleme iş akışı](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

İş akışı öğelerini ayırmak için satış departmanlarına ve toplama onların gönderimleri, bütçe Yöneticisi tarafından gözden geçirme, CFO tarafından onaylanması ve arasındaki her aşama aşama geçişleri içerir. 

**Bütçe planlama yapılandırma** sayfasının **İş akışı aşamaları** sayfasında Bütçeleme iş akışını her bir bütçe planlama iş akışına atarsınız.

### <a name="parameters-scenarios-and-stages"></a>Parametreler, senaryolar ve aşamalar

**Bütçe planlama yapılandırma** sayfasındaki başlangıç ayarları, daha sonraki yapılandırma adımları için bir takım yapı taşları oluşturmanıza izin verir:

-   **Parametreler** – Parametreler, bütçe planlarına uygulamak istediğiniz güvenlik kurallarını kullanıcılar bütçe planı senaryosu tutarlarını ayrıntılı şekilde incelerken kullanılması gereken varsayılan mali boyutları tanımlar.
-   **Senaryolar** – Senaryolar, bütçe planları için istediğiniz veri kategorilerini kapsar. Bütçe plan senaryolarını parasal birimler ve miktar gibi diğer ölçü birimi sınıflarını destekleyecek şekilde tanımlayabilirsiniz. Bir bütçe planında, senaryolar bütçe planlama verilerinin bir sürümünü temsil eder. Parasal bütçe planı senaryolarına örnekler Önceki yıl satışlarını ve İmzalanan sözleşmeleri içerir. Tutarlar kullanan senaryolara örnekler, Satış ziyareti sayısı ve Tam zamanlı eşdeğer (FTE) sayısını içerir.
-   **Aşamalar** – Aşamalar bütçe planının başlangıçtan son onaya kadar olan süreçte takip edeceği adımları tanımlar. Bütçe planlama aşamalarına örnekler Genel merkez özeti, CFO gözden geçirme ve Nihai aşamalarından meydana gelir.

### <a name="allocation-schedules"></a>Tahsisat zamanlamaları

Bütçe planlamada, bütçe planlama satırlarındaki tutarları veya miktarları bir senaryodan başka bir senaryoya veya hatta aynı senaryoya atayabilirsiniz. Örneğin, bir senaryodaki mali boyutlarda veya tutar tarihlerinde değişiklikler yapmak istiyorsanız bunları aynı senaryoya atayabilirsiniz. Bir tahsisat işlemi bir bütçe planı içinde veya bir bütçe planından diğerine gerçekleştirilebilir. 

Tahsisat programları, iş akışının işlenmesi sırasında otomatik olarak bütçe planı satırlarını tahsis eder. Tahsisat işlemlerini **Tahsisat yöntemi** listesinde bulunan, aşağıdaki yöntemlerden herhangi birini kullanarak gerçekleştirebilirsiniz:

-   **Dönemler arasında tahsis et** – Bütçe planı satırlarını kaynak bütçe planı senaryosundan hedef senaryodaki dönemler arasında tahsis etmek için bir dönem tahsisat anahtarı kullanırsınız. **Not:** dönem ayırabilirsiniz önce üzerinde dönem tahsisat anahtarlarını ayarlamanız gerekir *** dönem tahsisat kategoriler *** sayfa.
-   **Boyutlara tahsis et** – Bütçe planı satırları kaynak bütçe planı senaryosundan hedef senaryodaki mali boyutlara tahsis edilir. **Not:** boyutları ayırabilirsiniz önce üzerinde bütçe Tahsisat koşulları ayarlamanız gerekir *** bütçe Tahsisat koşulları *** sayfa.
-   **Toplama** – Bütçe planı satırları, ilgili bütçe planlarındaki kaynak bütçe planı senaryodan ana bütçe planındaki hedef senaryoya toplanır.
-   **Dağıtma** – Bütçe planı satırları, ana bütçe planındaki kaynak bütçe planı senaryodan ilişkili bütçe planlarındaki hedef senaryoya dağıtılır.
-   **Genel muhasebe tahsisat kurallarını kullan** – Bütçe planı satırları, seçilen genel muhasebe tahsisat kuralına dayalı olarak kaynak bütçe planı hedef senaryoya dağıtılır.
-   **Bütçe planından kopyala** – Tahsisatın kaynağı olarak kullanılmak üzere başka bir bütçe planı seçebilirsiniz.

### <a name="stage-allocations"></a>Aşama tahsisatları

Aşama tahsisatları, iş akışının işlenmesi sırasında bütçe planı satırlarının otomatik olarak atanması için kullanılır. Aşama tahsisatları kullanıldığında hedef senaryodaki bütçe planı satırları, bütçe planını hazırlayan veya gözden geçiren kişinin müdahalesi olmaksızın oluşturulabilir ve değiştirilebilir.

Bir aşama tahsisatı kurduğunuzda, bütçe planlama iş akışını ve aşamasını tahsisat programıyla ilişkilendirirsiniz. Bütçe planlama iş akışı kullanan bir bütçeleme akışıyla ilişkili *** bütçe planlama aşaması ayırma *** otomatik iş akışı görevi. İş akışı, belirtilen aşamaya ulaştığında tahsisat otomatik olarak gerçekleşir. Bu otomatik görev yeni bir senaryoda bütçe planı oluşturulması için kullanılabilir. 

Bu makalenin başında verilen örnek şemada, bir bütçe planındaki tutarların ve genel merkez temel aşamasındaki senaryoların başka bütçe planına ve Satış departmanı Tahmin aşamasındaki senaryolara aktarılması için bir tahsisat gerçekleştirilmektedir. Aşağıdaki şekilde örnek şemanın ilgili bölümü gösterilmiştir.

[![Sahne alanı ayırma](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Ayrıca, örnek Şeması'nda, bir toplama bütçe planları ve satış departmanında gönderildi Sahne senaryoları için HQ toplama aşamasında ana plan yapılır. Aşağıdaki şekilde örnek şemanın ilgili bölümü gösterilmiştir.

[![Aggregation](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Öncelikler

Kurmuş olduğunuz bütçe planları için kategoriler ve hedefler tanımlama üzere, isteğe bağlı olarak bütçe planı öncelikleri kullanabilirsiniz. Birkaç bütçe planını organize etmek, sınıflandırmak ve değerlendirmek için de öncelikleri kullanabilirsiniz. Örneğin, işçi sağlığı ve iş güvenliği için bir bütçe planlama önceliği oluşturabilir ve ardından bu önceliğe atanmış bütçe planlarını değerlendirebilirsiniz. Ayrıca, tüm bütçe planlarında bütçe planlarını sıralamak için bir numara atayabilirsiniz.

### <a name="columns-and-layouts"></a>Sütunlar ve düzenler

Bütçe rakamları bir bütçe planında satırlar ve sütunlar olarak görünür. Öncelikle sütunları tanımlamanız ve ardından sütunların sunumu için bir düzen oluşturmanız gerekir. 

Bir sütunu tanımlamak için bir bütçe planı senaryosu seçin. Bu senaryodaki satır tutarları bütçe planında gösterilir. Tutarı filtrelemek için bir dönem seçebilirsiniz ve ayrıca genel muhasebe hesabına dayalı olarak filtreler uygulayabilirsiniz. 

Bir düzen tanımlarken, görüntülemek istediğiniz bütçe planı satırlarını oluşturmak için bir genel muhasebe boyut kümesi seçin ve düzen öğeleri olarak sütunları seçin. Birden fazla düzen oluşturabilirsiniz, böylece bir bütçe planı, bütçe planlama sürecinin farklı aşamalarında istediğiniz verileri gösterir. 

Bütçe tutarları sütunlarına ek olarak proje, teklif edilen proje, kıymet ve önerilen kıymet alanları için bütçe planında sütunlar tanımlayabilirsiniz. Ayrıca, bütçelenen pozisyonlar için de bir sütun tanımlayabilirsiniz. Bu seçenek, kişisel bütçeleri analiz etmeniz gerektiği durumlarda çok kullanışlıdır. 

Örnek şemada PY Satışları, Sözleşmeler ve Tahmin senaryoları için sütunlar oluşturmak isteyebilirsiniz (aşağıdaki şekilde şemanın ilgili bölümü gösterilmiştir). Ardından, mali yılın her bir çeyreği için bu senaryoların birini veya tümünü ayrı sütunlara dağıtabilirsiniz, böylece satış departmanı yöneticisi her bir dönem için tahmin tutarlarını doğru şekilde girebilir.

[![Columns](./media/columns.png)](./media/columns.png) 

Ayrıca her Düzen öğesi (sütun) düzenlenebilir olup olmadığını ve bu düzen için oluşturulan herhangi bir çalışma sayfası şablonu kullanılabilir olup olmadığını belirleyin. Örnek şemada, Tahmin aşaması için kullanılan düzende Tahmin sütunları düzenlenebilirken, PY Satışları ve Sözleşmeler sütunları salt okunurdur.

### <a name="templates"></a>Şablonlar

**Bütçe planlama yapılandırması** sayfasının **Düzenler** bölümünde Excel şablonları oluşturabilir, görüntüleyebilir veya yükleyebilirsiniz. Bu şablonlar ilave analizler, çizelgeler ve veri giriş özellikleri sunulması için her bir bütçe planıyla ilişkilendirilir. 

Her bir düzen için bir şablon oluşturabilir, görüntüleyebilir veya yükleyebilirsiniz. Bir şablon oluşturulduğunda düzen kilitlenir ve düzenlenemez. Bu kilitleme özelliği, şablon formatının bütçe planı düzenine uygun olmasını ve aynı verileri içermesini garanti eder. Bir şablon oluşturulduğunda görüntülenebilir ve düzenlenebilir. Örneğin, şablona çizelgeler ekleyebilir veya bunların görünümünü özelleştirebilirsiniz.

> [!NOTE] 
> Böylece düzenleme tamamlandıktan sonra bu düzene yüklenebilir şablon için kullanıcının erişebileceği bir konuma kaydedilmesi gerekir. Bu şekilde şablon, düzeni kullanan bütçe planlarıyla birlikte kullanılacaktır.

### <a name="descriptions"></a>Açıklamalar

**Düzenler** bölümünde atayabileceğiniz açıklamalar, bir düzene dahil edilen bir mali boyutun adının görüntülenmesi için kullanılır. Örneğin, bir organizasyon bir bütçe planında ana hesap adını ana hesap numarasının yanında görüntülemek, ancak ekranın çok kalabalıklaşmaması için diğer mali boyutların adlarını gizlemek isteyebilir.

## <a name="setting-up-budget-planning-processes"></a>Bütçe planlama süreçleri oluşturma

Bütçe planlama yapılandırmayı bitirdikten sonra **Bütçe planlama süreci** sayfasında bütçe planlama süreçlerini ayarlayabilirsiniz. Bütçe planlama süreçleri, bütçe planlarının bütçe planlayan organizasyonun hiyerarşisinde nasıl güncelleştirileceğini, yönlendirileceğini, gözden geçirileceğini ve onaylanacağını belirleyen kurallar kümesidir. 

Her bir bütçe planlama süreci için, öncelikle bir bütçe döngüsü ve bir genel muhasebe seçersiniz. Her bir bütçe planlama süreci sadece tek bir bütçe dönüsü ve bir genel muhasebe ile ilgilidir. Ardından, **Bütçe planlama süreci yönetimi** hızlı sekmesinden bütçe organizasyon hiyerarşisini seçin ve kılavuzda görüntülenen organizasyondaki tüm sorumluluk merkezlerine bir bütçe planlama iş akışı atayın. 

Benzer sorumluluk merkezleri için bütçe planlama iş akışı atamak veya bunu değiştirmek için **İş akışı ata** öğesini tıklayın ve hedeflenecek organizasyon türünü ve kullanılacak bütçe planlama iş akışını seçin. Her bir bütçe planlama iş akışıyla ilişkilendirilen Bütçeleme iş akışı kimliği otomatik olarak kılavuza eklenir. 

**Bütçe planlama aşaması kuralları ve düzenleri** hızlı sekmesinde aşama kuralları ve şablonları tanımlarken, her bir bütçe planlama aşaması için farklı bir kural kümesi ve varsayılan düzenler tanımlayabilirsiniz.  Örneğin, Satış departmanı Tahmin aşaması, kullanıcıların bir bütçe planındaki satırları değiştirmesine izin verebilir, ancak kullanıcıların satır eklemesini engelleyebilir. Gönderildi aşaması, kullanıcıların satırları görüntülemesine izin verebilir, ancak kullanıcılar satır ekleyemez ve bunları değiştiremez, çünkü bu aşamadaki çalışma tamamlanmıştır ve bütçe planlarındaki değişikliklerin mutlaka önlenmesi gerekir. Bütçe planları için kullanılabilecek düzenleri seçmek için **Diğer düzenler** öğesini tıklayın. 

İsteğe bağlı olarak, **Bütçe planı öncelik kısıtlamaları** hızlı sekmesinden bütçe planlama önceliklerini de seçebilirsiniz. Öncelikler daha sonra bütçe planlarında seçilebilir. 

Nihai aşama, **Eylemler** menüsünden bütçe planlama sürecini etkinleştirmektir. Bir bütçe planlama süreci etkinleştirilinceye kadar kullanılamaz. 

**Eylemler** menüsünden ayrıca mevcut bir süreci kopyalayarak yeni bir süreç de oluşturabilirsiniz. Bu özellik, her bütçe döngüsü için aynı süreç akışını takip eden ve bunlar üzerinde birkaç değişiklik yapan veya hiçbir değişiklik yapmayan organizasyonlar için kullanışlıdır. 

**Eylemler** menüsündeki bir diğer kullanışlı komut da **Bütçe sürecinin durumunu göster** komutudur. Bu komut, planların iş akışı durumu, tutara ve birime göre özetler ve bütçe planlarına tek tıklamayla ulaşma vb. gibi ilgili verilerle birlikte, bir süreç içindeki bütçe planlarını grafiksel olarak gösterir.

[![Budget planning process status](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)


