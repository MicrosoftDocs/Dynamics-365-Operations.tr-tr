---
title: Bütçe planlama
description: Bu laboratuvarın amacı, Bütçe planlama alanındaki Microsoft Dynamics 365 for Finance and Operations işlevi güncelleştirmelerine ilişkin rehber eşlikli bir görünüm sağlamaktır. Bu laboratuvarın amacı, bütçe planlama modülü yapılandırmasının hızlı bir örneğini ve bu yapılandırmayla bütçe planlamanın nasıl tamamlanabileceğini göstermektir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac2e98dbbd45becf06e28b6ea4eb9d0ec15e30f6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "311646"
---
# <a name="budget-planning"></a>Bütçe planlama

[!include [banner](../includes/banner.md)]

Bu laboratuvarın amacı, Bütçe planlama alanındaki Microsoft Dynamics 365 for Finance and Operations işlevi güncelleştirmelerine ilişkin rehber eşlikli bir görünüm sağlamaktır. Bu laboratuvarın amacı, bütçe planlama modülü yapılandırmasının hızlı bir örneğini ve bu yapılandırmayla bütçe planlamanın nasıl tamamlanabileceğini göstermektir.  Bu laboratuar özellikle şu iş süreçleriyle veya görevlerle ilgilidir:
- Bütçe planlama için organizasyon hiyerarşisi oluşturma ve kullanıcı güvenliğini yapılandırma
- Bütçe planı senaryoları, bütçe planı sütunları, düzenler ve Excel şablonları tanımlama
- Bütçe planlama süreci oluşturma ve etkinleştirme
- Genel muhasebeden fiili değerleri çekerek bütçe planı belgesi oluşturma
- Bütçe planı belge verilerini ayarlamak için tahsisatları kullanma
- Excel'de bütçe planı belge verilerini düzenleme 

<a name="prerequisites"></a>Ön koşullar 
------------------

Bu eğitim için Contoso demo verileri ile birlikte Finance and Operations erişebiliyor ve örneğine bir yönetici olarak atanmış olmanız gerekir. Bu laboratuvar için Gizli tarayıcı modunu kullanmayın - gerekirse tarayıcıdaki diğer hesaplarda oturumunuzu kapatın ve Finance and Operations yönetici kimlik bilgilerinizle oturum açın. Finance and Operations içerisine oturum açarken "Oturumumu açık bırak" onay kutusunu **MUTLAKA** işaretlemeniz gerekir. Böylece Excel Uygulamasının şu anda gerektirdiği kalıcı bir tanımlama bilgisi üretmiş olursunuz. Finance and Operations'a Internet Explorer dışında bir tarayıcı kullanarak oturum açarsanız Excel Uygulamasında oturum açmanız istenir. Excel Uygulamasında "Oturum Aç" düğmesini tıklattığınızda bir Internet Explorer açılır penceresi görüntülenir ve oturum açarken **MUTLAKA** "Oturumumu açık bırak" onay kutusunu işaretlemeniz gerekir. Excel Uygulamasında "Oturum Aç" düğmesini tıklattığınızda hiçbir şey görüntülenmiyorsa IE tanımlama bilgisi önbelleğini temizlemeniz gerekir.

## <a name="scenario-overview"></a>**Senaryoya genel bakış**
Julia, Almanya'daki Contoso Entertainment Systems (DEMF) firmasında finans yöneticisi olarak çalışıyor. MY2016 yaklaşırken Julia'nın gelecek yıl için şirketin bütçesini oluşturmak için çalışmaya başlaması gerekiyor. Bütçe hazırlığı şu şekildedir:

1.  Julia, bütçe oluşturmak için başlangıç noktası olarak önceki yılın fiili tutarlarını kullanıyor.
2.  Önceki yılın fiili tutarlarına dayalı olarak gelecek yılın 12 ayı için tahminler oluşturuyor
3.  Julia, CFO ile bütçeyi gözden geçiriyor. Gözden geçirmeyi tamamladıktan sonra bütçe planı için gerekli düzeltmeleri yapıyor ve bütçe hazırlığına son veriyor.

Senaryo için bütçe planlama şeması aşağıdaki gibi görünür:

![Bütçe planlama yapılandırma şeması](./media/screenshot1-300x152.png)

Julia, bütçe hazırlamak için aşağıdaki Excel şablonunu kullanır:

[![Excel şablonu](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

## <a name="exercise-1-configuration"></a>Alıştırma 1: Yapılandırma

### <a name="task-1-create-organizational-hierarchy"></a>**Görev 1: Organizasyon hiyerarşisi oluşturma**
Tüm bütçe süreci Finans departmanında cereyan etmektedir, bu nedenle Julia sadece Finans departmanını içeren, çok basit bir organizasyon hiyerarşisi oluşturuyor. 1.1. Organizasyon hiyerarşilerine gidin (Organizasyon yönetimi &gt; Organizasyonlar &gt; Organizasyon hiyerarşileri) ve Yeni düğmesini tıklayın

![Kuruluş hiyerarşisi](./media/screenshot3.png) 

1.2. Organizasyon hiyerarşisinin adını yazın ve Amaç ata düğmesini tıklatın

[![Ad](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Bütçe planlama amacını seçin, Ekle düğmesini tıklatın ve yeni oluşturulan organizasyon hiyerarşisini atayın: 

[![Amaç ata](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Yukarıdaki adımı Güvenlik organizasyon amacı için yineleyin. İşiniz bittiğinde formu kapatın.

[![Güvenlik kuruluşu](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Organizasyon Hiyerarşileri formda Görünüm düğmesini tıklatın. Hiyerarşi tasarımcısında Düzenle düğmesini tıklatın ve Ekle düğmesini tıklatarak bir hiyerarşi oluşturun.

[![Ekle](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Bütçeleme hiyerarşi için Finans departmanını seçin. 

[![Finans](./media/screenshot8.png)](./media/screenshot8.png)

1.7. İşiniz bittiğinde Yayımla ve Kapat düğmesini tıklatın. Hiyerarşinin yayınlanması için geçerlilik tarihi olarak 1/1/2015 tarihini seçin.

[![Yürürlük tarihi](./media/screenshot9.png)](./media/screenshot9.png)

### <a name="task-2-configure-user-security"></a>Görev 2: Kullanıcı güvenliği yapılandırma
Bütçe planlama, bütçe plan verilerine erişim yapılandırmak için özel güvenlik ilkeleri kullanır. Julia'nın kendisi için Finans bütçe planlarına erişim yetkisi vermesi gerekiyor. 

2.1. DEMF tüzel kişilik içeriğine geçiş. 


2.2. Bütçeleme &gt; Kur &gt; Bütçe planlama &gt; Bütçe planlama yapılandırma seçimlerini yapın. Parametreler sekmesinde, Güvenlik modeli değerini güvenlik organizasyonlarına dayalı konumuna ayarlayın 

[![Parametreler](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Sistem yönetimi &gt; Kullanıcılar &gt; Kullanıcılar seçimlerini yapın. Kullanıcıya Yönetici (Julia Funderburk) Bütçe yöneticisi görevi verin. 

[![Bütçe yöneticisi](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Kullanıcı görevini seçin ve Organizasyonları ata düğmesini tıklayın 

[![Kuruluş ata](./media/screenshot13.png)](./media/screenshot13.png)

2.5. “Belirli organizasyonlara erişim izni ver” öğesini seçin. İlk adımda oluşturulan Organizasyon hiyerarşisini seçin. Finans düğümünü seçin ve Alt birimlerle birlikte ver düğmesine tıklayın 

***Önemli!*** *Organizasyon güvenliği tüzel kişilik için uygulandığından bu görev gerçekleştirilirken DMF tüzel kişilik içeriğinde olduğunuzdan emin olun* 

### <a name="task-3-create-scenarios"></a>Görev 3: Senaryo oluşturma
3.1. Bütçeleme&gt;Kur &gt; Bütçe planlama &gt; Bütçe planlama yapılandırma seçimlerini yapın. Senaryolar sayfasında, bu laboratuvarda kullanacağımız senaryolara dikkat edin: Önceki yılın fiili tutarları ve bütçelenen tutarları. 

*Not: İsterseniz bu alıştırma için yeni senaryolar oluşturabilir ve mevcut senaryolar yerine bunları kullanabilirsiniz.* 

[![Yeni senaryolar](./media/screenshot15.png)](./media/screenshot15.png) 

*Not: Julia, bütçe hazırlama için resmi onay sürecini kullanmıyor, bu nedenle bu laboratuvarda İş Akışları, Aşamalar ve İş akışı aşamaları kurulumunu geçiyoruz, Otomatik kurulumu kullanıyor – iş akışını onaylıyoruz. Bu iş akışı yapılandırması için eke bakın*

### <a name="task-4-create-budget-plan-columns"></a>Görev 4: Bütçe planı sütunları oluşturma
Bütçe plan sütunları, bütçe plan belgesi düzeninde kullanılabilen Parasal değere veya miktara dayalı sütunlardır. Örneğimizde Önceki yılın fiili tutarları için bir sütun ve bütçelenen bir yıldaki her bir ayı temsil etmesi için 12 sütun oluşturmamız gerekiyor. Sütunlar Ekle düğmesi tıklandıktan sonra değerler doldurularak veya Veri varlığı yardımıyla oluşturulabilir. Bu laboratuvarda değerleri doldurmak için Veri varlığını kullanacağız. 

4.1. Bütçeleme&gt;Kur &gt; Bütçe planlama &gt; Bütçe planlama yapılandırma altından Sütunlar sayfasını açın. Formun sağ üst köşesindeki Office düğmesini tıklatın ve Sütunları (filtrelenmemiş) 

[![Filtrelenmemiş sütunlar](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Sistem, değerlerin doldurulması için kullanılacak Excel çalışma kitabını açar. İstenirse, Düzenlemeyi Etkinleştir ve Bu uygulamaya güven üzerine tıklayın 

[![Düzenlemeyi etkinleştir](./media/screenshot18.png)](./media/screenshot18.png) 

[![Bu uygulama güven](./media/screenshot17.png)](./media/screenshot17.png)

4.3. Değerleri doldurmak için daha fazla sütuna ihtiyaç duyacağız. Kılavuza sütunlar eklemek için sağ kenar panelinde Tasarım'a tıklayın: 

[![Tasarım](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Izgaraya eklenebilecek sütunları görmek için PlanColumns yanındaki küçük kalem düğmesini tıklatın 

[![Düzenleme](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Her bir kullanılabilir alanı çift tıklayarak bunları Seçilen alanlara ekleyin ve Güncelleştir düğmesini tıklayın 

![Güncelleştir](./media/screenshot21.png)](./media/screenshot21.png) 

4.6. Excel tablosunda oluşturulmasını gerektiren tüm sütunları ekleyin. Excel'de satırları kısa sürede eklemek için Otomatik Doldur özelliğini kullanın. Satırların tablonun bir parçası olarak eklendiğinden emin olun (düşey kaydırma kullanırken sütun başlıklarını ızgaranın üstünde görebilirsiniz) 

[![Otomatik doldurma](./media/screenshot22.png)](./media/screenshot22.png) 

4.7. Finance and Operations'a dönün ve sayfayı yenileyin. Yayınlanan değerler Finance and Operations'ta görüntülenir. 

[![Yenile](./media/screenshot23.png)](./media/screenshot23.png)

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Görev 5: Bütçe planı belge düzenleri ve şablonları oluşturma
Düzen; kullanıcı, bütçe planı belgesini açtığında bütçe planı belge satırları ızgarasının nasıl görüneceğini tanımlar. Aynı verileri farklı açılardan görmek için bütçe planı belge düzenine geçiş yapılması da mümkündür. Şimdi, bütçe planı belgesiyle kullanılmak üzere tanımlanan sütunlara sahip olan Julia'nın şimdi de bütçe verilerini oluşturmak için kullandığı Excel tablosuna oldukça benzer bir görünüme sahip olacak bir bütçe plan belgesi düzeni oluşturması gerekiyor (bu laboratuvardaki Senaryoya genel bakış bölümüne bakın) 

5.1. Bütçeleme&gt; Kur &gt; Bütçe planlama &gt; Bütçe planlama yapılandırma altından Düzenler sayfasını açın. Aylık bütçe girişi için yeni bir düzen oluşturun:

-   Ana hesapları ve Ticari birimleri düzeye eklemek için MA+BU boyut setini seçin.
-   Önceki adımda Öğeler bölümünde oluşturulan tüm bütçe planı sütunlarını listeleyin. Önceki yılık fiili tutarları dışındaki tüm sütunları düzenlenebilir hale getirin.
-   Izgarada hangi mali boyutları Tanımlar göstermesi gerektiğini seçmek için Tanımlar düğmesini tıklayın.

[![Açıklamalar](./media/screenshot24.png)](./media/screenshot24.png) 

Bütçe planı düzen tanımına göre, Bütçe verilerini düzenlemek için alternatif bir yöntem olarak kullanılmak üzere Excel şablonu oluşturabilirsiniz. Excel şablonunun, bütçe planı düzen tanımıyla eşleşmesi gerektiğinden Excel şablonu oluşturulduktan sonra bütçe planı düzenini düzenleyemezsiniz, bu nedenle bu görev tüm düzen bileşenleri tanımlandıktan sonra gerçekleştirilmelidir. 

5.2. 5.1 üzerinde oluşturulan düzen için. adım, Şablon &gt; Oluştur düğmesine tıklayın. Uyarı mesajını onaylayın. Şablonu görüntülemek için Şablon &gt; Görünüm düğmelerini tıklayın. 

*Not: "Farklı Kaydet" olarak seçtiğinizden ve düzenleyebilmek için şablonun nerede kaydedileceğinizi seçtiğinizden emin olun. Kullanıcı iletişim kutusunda kaydetmeden "Aç" seçerse, dosya kapandığında yapılmış olan değişiklikler korunmaz.* 
[![Şablon görünümü](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; Opsiyonel adım&gt; Daha kullanıcı dostu hale getirmek için Excel şablonunu değiştirtirin – toplama formülleri, başlık alanları, biçimlendirme vb. ekleyin. Değişiklikleri kaydedin ve dosyayı Düzen &gt; Yükle düğmelerini tıklayarak bütçe planı düzenine yükleyin [![Karşıya yükle](./media/screenshot26.png)](./media/screenshot26.png)

### <a name="task-6-create-a-budget-planning-process"></a>Görev 6: Bütçe planlama süreci oluşturma
Julia, bütçe planlarını girmeye başlamak için yukarıdaki tüm kurulumu birleştiren yeni bir bütçe planlama süreci oluşturmalı ve bunu etkinleştirmelidir. Bütçe planlama süreci, bütçe planlarının oluşturulması için hangi bütçeleme organizasyonlarının, iş akışının, düzenlerin ve şablonların kullanılacağını tanımlar. 

6.1. Bütçeleme &gt; Kurulum &gt; Bütçe planlama &gt; Bütçe planlama süreci öğelerini seçin ve yeni bir kayıt oluşturun.

-   Bütçe planlama süreci – DEMF bütçeleme MY2016
-   Bütçe döngüsü – MY2016
-   Genel Muhasebe – DEMF
-   Varsayılan hesap yapısı – Üretim kar ve zarar
-   Organizasyon hiyerarşisi – laboratuvarın başında oluşturduğunuz hiyerarşiyi seçin
-   Bütçe planlama iş akışı– Otomatik ata – Finans departmanı için iş akışını onaylayın
-   Bütçe planlama aşaması kuralları ve şablonlarında, her bir iş akışı Bütçe planlama aşaması için Satırların eklenmesinin ve Satırların değiştirilmesinin mümkün olup olmadığını ve varsayılan olarak hangi Düzenin kullanılacağını seçin

*Not: Alternatif düzenler düğmesini tıklayarak ek belge düzenleri oluşturabilir ve bunları bütçe planlama iş akışı aşamasına dahil edilmek üzere atayabilirsiniz.* 

[![Diğer düzenler](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Bu bütçe planlama iş akışını etkinleştirmek için Eylemler &gt; Etkinleştir'i seçin 

[![Etkinleştir](./media/screenshot28.png)](./media/screenshot28.png)

## <a name="exercise-2-process-simulation"></a>Alıştırma 2: İşlem simülasyonu

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Görev 7: Genel muhasebeden bütçe planı için ilk verileri oluşturma
7.1. Bütçeleme &gt; Periyodik &gt; Genel muhaseben bütçe planı oluştur öğelerini seçin. Periyodik süreç parametrelerini doldurun ve Oluştur düğmesini tıklatın. 

[![Oluştur](./media/screenshot29.png)](./media/screenshot29.png) 

7.2. Oluşturma süreci tarafından oluşturulan bir bütçe planını bulmak için Bütçeleme &gt; Bütçe planları seçimlerini yapın. 

[![Bütçe planı](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Belge numarası köprüsünü tıklayarak belge bilgilerini açın. Bütçe planı bu laboratuvar sırasında oluşturulan düzende tanımlandığı şekilde görüntülenir 

[![Bütçe planı görünümü](./media/screenshot31.png)](./media/screenshot31.png)

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Görev 8: Önceki yılın fiili değerlerine dayalı olarak mevcut yıl bütçesi oluşturma
Bütçe planları için bir senaryodaki bilgileri kolayca başka bir senaryoya kopyalamak / bunları dönemler arasında dağıtmak / boyutlara atamak için bütçe planında tahsisat yöntemleri kullanılabilir. Mevcut yıl bütçesini önceki yılı fiili tutarlarından oluşturmak için tahsisatları kullanacağız. 

8.1. Bütçe planı belge ızgarasındaki tüm satırları seçin ve bütçeyi tahsis et düğmesini tıklatın 

[![Tüm satırlar](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Tahsisat yöntemini, Dönem anahtarı, Kaynak ve hedef senaryoları seçin ve Tahsisat üzerine tıklayın. 

[![Tahsis et](./media/screenshot33.png)](./media/screenshot33.png)

Önceki yıl gerçek tutarları, mevcut yıl bütçesine kopyalanır ve Satış eğrisi dönem anahtarı kullanarak onları dönemlere tahsis edin. 

[![Satış eğrisi](./media/screenshot34.png)](./media/screenshot34.png)

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Görev 9: Bütçe planı belgesini Excel kullanarak ayarlama ve belgeyi son haline getirme
9.1. Excel'de belge içeriklerini açmak için çalışma sayfası düğmesini tıklatın

[![Excel](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Excel çalışma kitabı açıldığında bütçe planı belgesindeki numaraları ayarlayın ve Yayınla düğmesini tıklatın.

[![Yayımla](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Finance and Operations bütçe planı belgesine dönün. İş Akışı &gt; Belgeyi otomatik onaylamaya gönder üzerine tıklatın

[![Otomatik-onayla](./media/screenshot37.png)](./media/screenshot37.png) 

İş akışı tamamlandıktan sonra, bütçe planı belge aşaması Onaylandı olarak değişir. [![Onaylandı](./media/screenshot38.png)](./media/screenshot38.png)

## <a name="appendix"></a>Ek

### <a name="auto-approve-workflow-configuration"></a>İş akışı yapılandırmasını otomatik onaylama

A. Bütçeleme &gt; Kurulum &gt; Bütçe planlama &gt; Bütçeleme iş akışı, Bütçe planlama iş akışları kullanarak yeni bir iş akışı oluşturun:

[![Yeni bir iş akışı oluşturun](./media/screenshot39.png)](./media/screenshot39.png)

Bu iş akışı sadece bir görev içerir - Aşama geçiş bütçe planı 

[![Aşama geçişi bütçe planı](./media/screenshot40.png)](./media/screenshot40.png) 

İş akışını kaydetme ve etkinleştirme. 

B. Bütçeleme &gt; Kur &gt; Bütçe planlama &gt; Bütçe planlama yapılandırma seçimlerini yapın. Aşama sekmesinde 2 aşama oluşturun - Başlangıç ve Gönderildi 

[![Başlangıç ve gönderilen](./media/screenshot41.png)](./media/screenshot41.png)

C. Bütçeleme &gt; Kur &gt; Bütçe planlama &gt; Bütçe planlama yapılandırma seçimlerini yapın. İş Akışı Aşamaları sekmesinde, A adımında oluşturulan iş akışı otomatik onaylamayı Başlangıç ve Gönderilen aşamalarıyla ilişkilendirin 

[![Bütçeleme ve bütçe planlama](./media/screenshot42.png)](./media/screenshot42.png)  



