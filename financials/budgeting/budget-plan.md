---
title: "Bütçe planlama"
description: "Amacı, bu Laboratuvar alanı planlama bütçe işlemlerini işlevselliği güncelleştirmeleri Microsoft Dynamics 365 destekli bir görünümünü sağlamaktır. Bu laboratuvarın amacı, bütçe planlama modülü yapılandırmasının hızlı bir örneğini ve bu yapılandırmayla bütçe planlamanın nasıl tamamlanabileceğini göstermektir.  Bu laboratuar özellikle aşağıdaki iş süreçleri veya görevleri--bütçe planlama ve kullanıcı güvenlik yapılandırma - bütçe planı senaryoları, bütçe planı sütunlar, düzenleri ve Excel şablonları oluşturma ve bütçe planlama süreci - göre genel muhasebedeki fiili değerlerin çekmek - bütçe planı belge verileri ayarlamak için ayırmaları kullanarak oluşturma bütçe planı belge - düzenleme bütçe planı belge verileri Excel&quot;de etkinleştirme - tanımlama için kuruluş hiyerarşisi oluşturma odaklanmak"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>Bütçe planlama

Amacı, bu Laboratuvar alanı planlama bütçe işlemlerini işlevselliği güncelleştirmeleri Microsoft Dynamics 365 destekli bir görünümünü sağlamaktır. Bu laboratuvarın amacı, bütçe planlama modülü yapılandırmasının hızlı bir örneğini ve bu yapılandırmayla bütçe planlamanın nasıl tamamlanabileceğini göstermektir.  Bu laboratuar özellikle aşağıdaki iş süreçleri veya görevleri--bütçe planlama ve kullanıcı güvenlik yapılandırma - bütçe planı senaryoları, bütçe planı sütunlar, düzenleri ve Excel şablonları oluşturma ve bütçe planlama süreci - göre genel muhasebedeki fiili değerlerin çekmek - bütçe planı belge verileri ayarlamak için ayırmaları kullanarak oluşturma bütçe planı belge - düzenleme bütçe planı belge verileri Excel'de etkinleştirme - tanımlama için kuruluş hiyerarşisi oluşturma odaklanmak 

<a name="prerequisites"></a>Önkoşullar 
------------------

Bu öğretici için Contoso demo verileri ile işlem ortamı için Dynamics 365 erişmek ve örneğinde yönetici olarak sağlanması gerekir. İçinde özel tarayıcı modunu kullanmayın bu Laboratuvar - Oturumu Kapat tarayıcıda herhangi bir firmaya gerekirse ve işlemler için yönetici kimlik bilgileri ile Dynamics 365 günlük. Dynamics 365 işlemleri için oturum açma sırasında **gerekir** "oturum Koru" onay kutusunu işaretleyin. Böylece Excel Uygulamasının şu anda gerektirdiği kalıcı bir tanımlama bilgisi üretmiş olursunuz. Sonra Dynamics 365 işlemlerinde IE dışında bir tarayıcı kullanarak oturum açarsanız, Excel App içinde oturum istenir. Excel Uygulamasında "Oturum Aç" düğmesini tıklattığınızda bir Internet Explorer açılır penceresi görüntülenir ve oturum açarken **MUTLAKA** "Oturumumu açık bırak" onay kutusunu işaretlemeniz gerekir. Excel Uygulamasında "Oturum Aç" düğmesini tıklattığınızda hiçbir şey görüntülenmiyorsa IE tanımlama bilgisi önbelleğini temizlemeniz gerekir.

## <a name="scenario-overview"></a>**Scenario overview**
Julia, Almanya'daki Contoso Entertainment Systems (DEMF) firmasında finans yöneticisi olarak çalışıyor. MY2016 yaklaşırken Julia'nın gelecek yıl için şirketin bütçesini oluşturmak için çalışmaya başlaması gerekiyor. Bütçe hazırlığı şu şekildedir:

1.  Julia, bütçe oluşturmak için başlangıç noktası olarak önceki yılın fiili tutarlarını kullanıyor.
2.  Önceki yılın fiili tutarlarına dayalı olarak gelecek yılın 12 ayı için tahminler oluşturuyor
3.  Julia, CFO ile bütçeyi gözden geçiriyor. Gözden geçirmeyi tamamladıktan sonra bütçe planı için gerekli düzeltmeleri yapıyor ve bütçe hazırlığına son veriyor.

Bütçe planlama senaryosu için yapılandırma Şeması aşağıdaki gibi görünür:

![Screenshot1](./media/screenshot1-300x152.png)

Julia, bütçe hazırlamak için aşağıdaki Excel şablonu kullanır:

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>Alıştırma 1: Yapılandırma
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**Görev 1: kuruluş hiyerarşisi oluşturma**
Tüm bütçe süreci Finans departmanında cereyan etmektedir, bu nedenle Julia sadece Finans departmanını içeren, çok basit bir organizasyon hiyerarşisi oluşturuyor. 1.1. Kuruluş hiyerarşileri için gidin (kuruluş yönetim &gt;kuruluşların &gt;kuruluş hiyerarşileri) ve yeni düğmesini tıklatın

![Screenshot3](./media/screenshot3.png) 

1.2. Kuruluş hiyerarşisi için bir ad yazın ve düğme Ata amaç'ı tıklatın

[![Screenshot4](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Bütçe planlama amaç seçin, Ekle düğmesini tıklatın ve yeni oluşturulan organizasyon hiyerarşisine atayabilirsiniz: 

[![Screenshot5](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Yukarıdaki adımı Güvenlik organizasyon amacı için yineleyin. İşiniz bittiğinde formu kapatın.

[![Screenshot6](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Organizasyon Hiyerarşileri formda Görünüm düğmesini tıklatın. Hiyerarşi tasarımcısında Düzenle düğmesini tıklatın ve Ekle düğmesini tıklatarak bir hiyerarşi oluşturun.

[![Screenshot7](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Bütçeleme hiyerarşi için Finans departmanını seçin. 

[![Screenshot8](./media/screenshot8.png)](./media/screenshot8.png)

1.7. İşiniz bittiğinde Yayımla ve Kapat düğmesini tıklatın. Hiyerarşinin yayınlanması için geçerlilik tarihi olarak 1/1/2015 tarihini seçin.

[![Screenshot9](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>Görev 2: Kullanıcı güvenliği yapılandırma
Bütçe planlama, bütçe plan verilerine erişim yapılandırmak için özel güvenlik ilkeleri kullanır. Julia'nın kendisi için Finans bütçe planlarına erişim yetkisi vermesi gerekiyor. 2.1. DEMF tüzel içeriğine geçiş: [![Screenshot10](./media/screenshot10.png)](./media/screenshot10.png) 2.2. Bütçeleme için gitmek &gt;Kurulum &gt;bütçe planlama &gt;bütçe planlama yapılandırma. Parametreler sekmesinde, güvenlik modeli değeri için temel güvenlik kuruluşları temel set [![Screenshot11](./media/screenshot11.png)](./media/screenshot11.png) 2.3. Sistem Yönetimi'ne gidin &gt;kullanıcı &gt;kullanıcıları. Kullanıcıya Yönetici (Julia Funderburk) Bütçe yöneticisi görevi verin. [![Screenshot12](./media/screenshot12.png)](./media/screenshot12.png) 2.4. Kullanıcı rolü seçin ve ata kuruluşlar'ı [![Screenshot13](./media/screenshot13.png)](./media/screenshot13.png)2.5. “Belirli organizasyonlara erişim izni ver” öğesini seçin. İlk adımda oluşturulan Organizasyon hiyerarşisini seçin. Finans düğümünü seçin ve Grant çocuklar düğmesine tıklayın ***önemli!*** *– Olun emin kuruluş güvenlik tüzel uygulanan olarak bu görevi gerçekleştirirken DEMF tüzel içerikte olan*[![Screenshot14](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>Görev 3: Senaryo oluşturma
3.1. Bütçeleme için gitmek&gt;Kurulum &gt;bütçe planlama &gt;bütçe planlama yapılandırma. Senaryolar sayfasında, bu laboratuvarda kullanacağımız senaryolara dikkat edin: Önceki yılın fiili tutarları ve bütçelenen tutarları. *Not: İsterseniz bu alıştırma için yeni senaryolar oluşturabilir ve mevcut senaryolar yerine bunları kullanabilirsiniz.* [![Screenshot15](./media/screenshot15.png)](./media/screenshot15.png)*Not: Julia resmi onay işlemi için bütçe hazırlık kullanarak değil, biz iş akışları, aşamaları atlar ve iş akışı aşamaları Kurulum bu laboratuvarda ve mevcut kurulum için otomatik – kullanacak şekilde onaylama iş akışı. Bu iş akışı yapılandırması için ekin bakın.*

## <a name="task-4-create-budget-plan-columns"></a>Görev 4: Bütçe planı sütunları oluşturma
Bütçe plan sütunları, bütçe plan belgesi düzeninde kullanılabilen Parasal değere veya miktara dayalı sütunlardır. Örneğimizde Önceki yılın fiili tutarları için bir sütun ve bütçelenen bir yıldaki her bir ayı temsil etmesi için 12 sütun oluşturmamız gerekiyor. Sütunlar Ekle düğmesi tıklandıktan sonra değerler doldurularak veya Veri varlığı yardımıyla oluşturulabilir. Bu laboratuvarda değerleri doldurmak için Veri varlığını kullanacağız. 4.1. Bütçeleme,&gt;Kurulum &gt;bütçe planlama &gt;bütçe planlama yapılandırma sütunlar sayfayı aç. Formun sağ üst köşesinde Office düğmesini tıklatın ve sütun (filtrelenmemiş) çekme [![Screenshot16](./media/screenshot16.png)](./media/screenshot16.png) 4.2. Sistem, değerlerin doldurulması için kullanılacak Excel çalışma kitabını açar. İstenirse, düzenlemeyi etkinleştir'i tıklatın ve bu app güven [![Screenshot18](./media/screenshot18.png)](./media/screenshot18.png)[![Screenshot17](./media/screenshot17.png)](./media/screenshot17.png) 4.3. Daha fazla sütun değerleri doldurmak için ihtiyacımız. Tasarım kılavuzuna sütunları eklemek için Sağdaki bölmeyi tıklatın: [![Screenshot19](./media/screenshot19.png)](./media/screenshot19.png) 4.4. Kılavuza eklemek için kullanılabilen sütunları görmek için PlanColumns yanındaki küçük kalem düğmesini [![Screenshot20](./media/screenshot20.png)](./media/screenshot20.png) 4.5. Güncelleştir'i tıklatın ve bunları seçili alanları eklemek için kullanılabilir her alanı çift tıklatın [![Screenshot21](./media/screenshot21.png)](./media/screenshot21.png) 4.6. Excel tablosunda oluşturulmasını gerektiren tüm sütunları ekleyin. Excel'de satırları kısa sürede eklemek için Otomatik Doldur özelliğini kullanın. Satırlar tablonun bir parçası eklenir emin olun (dikey kaydırma kullanırken, kılavuz üstünde sütun başlıklarının görmeye olmalıdır) [![Screenshot22](./media/screenshot22.png)](./media/screenshot22.png) 4.7. Dynamics 365 işlemleri için geri dönün ve sayfayı yenileyin. Yayınlanan değerleri Dynamics 365 işlemleri için görüntülenir. [![Screenshot23](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Görev 5: Bütçe planı belge düzenleri ve şablonları oluşturma
Düzen; kullanıcı, bütçe planı belgesini açtığında bütçe planı belge satırları ızgarasının nasıl görüneceğini tanımlar. Aynı verileri farklı açılardan görmek için bütçe planı belge düzenine geçiş yapılması da mümkündür. Şimdi, bütçe planı belgesiyle kullanılmak üzere tanımlanan sütunlara sahip olan Julia'nın şimdi de bütçe verilerini oluşturmak için kullandığı Excel tablosuna oldukça benzer bir görünüme sahip olacak bir bütçe plan belgesi düzeni oluşturması gerekiyor (bu laboratuvardaki Senaryoya genel bakış bölümüne bakın) 5.1. Bütçeleme,&gt;Kurulum &gt;bütçe planlama &gt;bütçe planlama yapılandırma düzenleri sayfayı aç. Aylık bütçe girişi için yeni bir düzen oluşturun:

-   Ana hesapları ve Ticari birimleri düzeye eklemek için MA+BU boyut setini seçin.
-   Önceki adımda Öğeler bölümünde oluşturulan tüm bütçe planı sütunlarını listeleyin. Önceki yılık fiili tutarları dışındaki tüm sütunları düzenlenebilir hale getirin.
-   Izgarada hangi mali boyutları Tanımlar göstermesi gerektiğini seçmek için Tanımlar düğmesini tıklayın.

[![Screenshot24](./media/screenshot24.png)](./media/screenshot24.png) göre bütçe plan düzen tanımı biz bütçe verilerini düzenlemek için alternatif bir yol kullanılmak üzere bir Excel şablonu oluşturabilirsiniz. Excel şablonunun, bütçe planı düzen tanımıyla eşleşmesi gerektiğinden Excel şablonu oluşturulduktan sonra bütçe planı düzenini düzenleyemezsiniz, bu nedenle bu görev tüm düzen bileşenleri tanımlandıktan sonra gerçekleştirilmelidir. 5.2. 5.1 oluşturulan düzeni. Adım, şablon düğmesini &gt;oluşturur. Uyarı mesajını onaylayın. Şablon şablonu görüntülemek için tıklatın &gt;görünüm. *Not: "Farklı Kaydet" ve nerede şablonu düzenlemek için depolanması gereken yeri seçin emin olun. Kaydetmeden iletişim kutusunda "Aç" kullanıcı seçerse dosya kapatıldığında dosyaya yapılan değişiklikleri korunmaz.* [![Screenshot25](./media/screenshot25.png)](./media/screenshot25.png) 5.3. &lt;İsteğe bağlı adım&gt; görünmesi daha fazla kullanıcı dostu – hale getirmek için değiştirmek Excel şablonu toplam formülleri, biçimlendirme, vb. üstbilgi alanları ekleyin. Değişiklikleri kaydetmek ve Düzen'i tıklatarak bütçe plan düzeni için dosyayı karşıya yüklemeyi &gt;karşıya [![Screenshot26](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>Görev 6: Bütçe planlama süreci oluşturma
Julia, bütçe planlarını girmeye başlamak için yukarıdaki tüm kurulumu birleştiren yeni bir bütçe planlama süreci oluşturmalı ve bunu etkinleştirmelidir. Bütçe planlama süreci, bütçe planlarının oluşturulması için hangi bütçeleme organizasyonlarının, iş akışının, düzenlerin ve şablonların kullanılacağını tanımlar. 6.1. Bütçeleme için gitmek &gt;Kurulum &gt;bütçe planlama &gt;bütçe planlama işleminin ve yeni bir kayıt oluşturun.

-   Bütçe planlama süreci – DEMF bütçeleme MY2016
-   Bütçe döngüsü – MY2016
-   Genel Muhasebe – DEMF
-   Varsayılan hesap yapısı – Üretim kar ve zarar
-   Organizasyon hiyerarşisi – laboratuvarın başında oluşturduğunuz hiyerarşiyi seçin
-   Bütçe planlama iş akışı– Otomatik ata – Finans departmanı için iş akışını onaylayın
-   Bütçe planlama aşaması kuralları ve şablonlarında, her bir iş akışı Bütçe planlama aşaması için Satırların eklenmesinin ve Satırların değiştirilmesinin mümkün olup olmadığını ve varsayılan olarak hangi Düzenin kullanılacağını seçin

*Not: Alternatif düzenler düğmesini tıklayarak ek belge düzenleri oluşturabilir ve bunları bütçe planlama iş akışı aşamasına dahil edilmek üzere atayabilirsiniz.* [![Screenshot27](./media/screenshot27.png)](./media/screenshot27.png) 6.2. Eylemleri seçin &gt;bu bütçe planlama iş akışını etkinleştirmek için Etkinleştir [![Screenshot28](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>Alıştırma 2: İşlem simülasyonu
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Görev 7: Genel muhasebeden bütçe planı için ilk verileri oluşturma
7.1. Bütçeleme için gitmek &gt;Periyodik &gt;genel muhasebedeki bütçe planı oluştur. Periyodik süreç parametrelerini doldurun ve Oluştur düğmesini tıklatın. [![Screenshot29](./media/screenshot29.png)](./media/screenshot29.png) 7.2. Bütçeleme için gitmek &gt;bütçe planları oluşturma işlemi tarafından yaratılan bir bütçe planı bulmak. [![Screenshot30](./media/screenshot30.png)](./media/screenshot30.png) 7.3. Belge numarası köprüsünü tıklayarak belge bilgilerini açın. Bu Laboratuvar sırasında oluşturulan düzen içinde tanımlandığı şekilde bütçe planı görüntülenir [![Screenshot31](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Görev 8: Önceki yılın fiili değerlerine dayalı olarak mevcut yıl bütçesi oluşturma
Bütçe planları için bir senaryodaki bilgileri kolayca başka bir senaryoya kopyalamak / bunları dönemler arasında dağıtmak / boyutlara atamak için bütçe planında tahsisat yöntemleri kullanılabilir. Mevcut yıl bütçesini önceki yılı fiili tutarlarından oluşturmak için tahsisatları kullanacağız. 8.1. Bütçe plan belge kılavuzunda tüm satırları seçin ve düğmesini tıklatın bütçe tahsis [![Screenshot32](./media/screenshot32.png)](./media/screenshot32.png) 8.2. Tahsisat yöntemi, dönem anahtarını, kaynak ve hedef senaryoları seçin ve Tahsis Et'i tıklatın. 

[![Screenshot33](./media/screenshot33.png)](./media/screenshot33.png)

Önceki yıl fiili tutarlar geçerli yıl bütçeye kopyalanır ve satış eğri Dönem anahtarı kullanılarak dönem onları ayırmak. 

[![Screenshot34](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Görev 9: Bütçe planı belgesini Excel kullanarak ayarlama ve belgeyi son haline getirme
9.1. Belge içeriğini Excel'de açmak için çalışma düğmesini tıklatın

[![Screenshot35](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Excel çalışma kitabı açıldığında bütçe planı belgesindeki numaraları ayarlayın ve Yayınla düğmesini tıklatın.

[![Screenshot36](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Dynamics 365 işlemleri için bütçe planı belgeye dönün. İş Akışı'ı &gt;için otomatik olarak onaylanacak belge gönderme

[![Screenshot37](./media/screenshot37.png)](./media/screenshot37.png) 

İş akışı tamamlandıktan sonra bütçe planı belgenin Sahne Alanı Onaylandı olarak değişir. [![Screenshot38](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Ek
========

### <a name="auto-approve-workflow-configuration"></a>İş akışı yapılandırmasını otomatik onaylama

A. Bütçeleme &gt;Kurulum &gt;bütçe planlama &gt;bütçeleme iş akışı şablonu bütçe planlama iş akışlarını kullanarak yeni bir iş akışı oluşturun:

[![Screenshot39](./media/screenshot39.png)](./media/screenshot39.png)

Bu iş akışı yalnızca bir görev – aşamasına geçiş bütçe planı içerir 

[![Screenshot40](./media/screenshot40.png)](./media/screenshot40.png) 

Kaydet ve iş akışını etkinleştirin. 

B. Bütçeleme için gitmek &gt;Kurulum &gt;bütçe planlama &gt;bütçe planlama yapılandırma. Aşamalı olarak sekme oluşturmak 2 aşamaları – başlangıç ve gönderildi 

[![Screenshot41](./media/screenshot41.png)](./media/screenshot41.png)

C. Bütçeleme için gitmek &gt;Kurulum &gt;bütçe planlama &gt;bütçe planlama yapılandırma. İş akışı aşamaları sekmesinde Otomatik iş akışı ilişkilendirme – onaylaması ile ilk ve gönderildi aşamaları bir adımda oluşturduğunuz 

[![Screenshot42](./media/screenshot42.png)](./media/screenshot42.png)  


