---
title: Bütçe planlama
description: Bu laboratuvarın amacı, Bütçe planlama alanındaki Microsoft Dynamics 365 Finance işlevi güncelleştirmelerine ilişkin rehber eşlikli bir görünüm sağlamaktır. Bu laboratuvarın amacı, bütçe planlama modülü yapılandırmasının hızlı bir örneğini ve bu yapılandırmayla bütçe planlamanın nasıl tamamlanabileceğini göstermektir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9558013236a728e0fb9691f4edd719fe58d5457
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448943"
---
# <a name="budget-planning"></a>Bütçe planlama

[!include [banner](../includes/banner.md)]

Bu laboratuvarın amacı, Bütçe planlama alanındaki Microsoft Dynamics 365 Finance işlevi güncelleştirmelerine ilişkin rehber eşlikli bir görünüm sağlamaktır. Bu laboratuvarın amacı, bütçe planlama modülü yapılandırmasının hızlı bir örneğini ve bu yapılandırmayla bütçe planlamanın nasıl tamamlanabileceğini göstermektir.  Bu laboratuar özellikle şu iş süreçleriyle veya görevlerle ilgilidir:
- Bütçe planlama için organizasyon hiyerarşisi oluşturma ve kullanıcı güvenliğini yapılandırma
- Bütçe planı senaryoları, bütçe planı sütunları, düzenler ve Excel şablonları tanımlama
- Bütçe planlama süreci oluşturma ve etkinleştirme
- Genel muhasebeden fiili değerleri çekerek bütçe planı belgesi oluşturma
- Bütçe planı belge verilerini ayarlamak için tahsisatları kullanma
- Excel'de bütçe planı belge verilerini düzenleme 

<a name="prerequisites"></a>Önkoşullar 
------------------

Bu eğitim için Contoso demo verileri ile birlikte Microsoft Dynamics 365 Finance'a erişebiliyor ve örneğine bir yönetici olarak atanmış olmanız gerekir. Bu laboratuvar için Gizli tarayıcı modunu kullanmayın - gerekirse tarayıcıdaki diğer hesaplarda oturumunuzu kapatın ve yönetici kimlik bilgilerinizle oturum açın. Oturum açarken "Oturumumu açık bırak" onay kutusunu **MUTLAKA** işaretlemeniz gerekir. Böylece Excel Uygulamasının şu anda gerektirdiği kalıcı bir tanımlama bilgisi üretmiş olursunuz. Uygulamada IE dışında bir tarayıcı kullanarak oturum açarsanız Excel Uygulamasında oturum açmanız istenir. Excel Uygulamasında "Oturum Aç" düğmesini tıklattığınızda bir IE açılır penceresi görüntülenir ve oturum açarken **MUTLAKA** "Oturumumu açık bırak" onay kutusunu işaretlemeniz gerekir. Excel Uygulamasında "Oturum Aç" düğmesini tıklattığınızda hiçbir şey görüntülenmiyorsa IE tanımlama bilgisi önbelleğini temizlemeniz gerekir.

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
Tüm bütçe süreci Finans departmanında cereyan etmektedir, bu nedenle Julia sadece Finans departmanını içeren, çok basit bir organizasyon hiyerarşisi oluşturuyor. 

1.1. Kuruluş hiyerarşilerine gidin (Kuruluş yönetimi &gt; Kuruluşlar &gt; Kuruluş hiyerarşileri) ve Yeni düğmesine tıklayın.

![Kuruluş hiyerarşileri](./media/screenshot3.png) 

1.2. Ad kutusuna kuruluş hiyerarşisinin adını yazın ve Amaç ata seçeneğine tıklayın.

1.3. Bütçe planlama amacını seçin, Ekle'ye tıklayın ve yeni oluşturulan kuruluş hiyerarşisini atayın. 

[![Amaç ata](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Yukarıdaki adımı Güvenlik kuruluş amacı için yineleyin. İşiniz bittiğinde formu kapatın.

1.5. Kuruluş Hiyerarşileri formunda Görüntüle'ye tıklayın. Hiyerarşi tasarımcısında Düzenle'ye tıklayın ve Ekle seçeneğine tıklayarak bir hiyerarşi oluşturun.

[![Ekle](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Bütçeleme hiyerarşi için Finans departmanını seçin. 

[![Finans](./media/screenshot8.png)](./media/screenshot8.png)

1.7. İşiniz bittiğinde Yayımla ve Kapat'a tıklayın. Hiyerarşinin yayımlanması için geçerlilik tarihi olarak 1.1.2015 tarihini seçin.

[![Yürürlük tarihi](./media/screenshot9.png)](./media/screenshot9.png)

### <a name="task-2-configure-user-security"></a>Görev 2: Kullanıcı güvenliği yapılandırma
Bütçe planlama, bütçe plan verilerine erişim yapılandırmak için özel güvenlik ilkeleri kullanır. Julia'nın kendisi için Finans bütçe planlarına erişim yetkisi vermesi gerekiyor. 

2.1. DEMF tüzel kişilik içeriğine geçiş. 


2.2. Bütçeleme &gt; Kur &gt; Bütçe planlama &gt; Bütçe planlama yapılandırma seçimlerini yapın. Parametreler sekmesinde, Güvenlik modeli değerini Güvenlik kuruluşlarına göre olarak ayarlayın. 

[![Parametreler](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Sistem yönetimi &gt; Kullanıcılar &gt; Kullanıcılar seçimlerini yapın. Kullanıcıya Yönetici (Julia Funderburk) Bütçe yöneticisi görevi verin. 

[![Bütçe yöneticisi](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Kullanıcı görevini seçin ve Kuruluş ata seçeneğine tıklayın. 

[![Kuruluş ata](./media/screenshot13.png)](./media/screenshot13.png)

2.5. “Belirli organizasyonlara erişim izni ver” öğesini seçin. İlk adımda oluşturulan Kuruluş hiyerarşisi'ni seçin. Finans düğümünü seçin ve Alt öğelerle ver düğmesine tıklayın. 

***Önemli!*** *Organizasyon güvenliği tüzel kişilik için uygulandığından bu görev gerçekleştirilirken DMF tüzel kişilik içeriğinde olduğunuzdan emin olun* 

### <a name="task-3-create-scenarios"></a>Görev 3: Senaryo oluşturma
3.1. Bütçeleme&gt;Kur &gt; Bütçe planlama &gt; Bütçe planlama yapılandırma seçimlerini yapın. Senaryolar sayfasında, bu laboratuvarda kullanacağımız senaryolara dikkat edin: Önceki yılın fiili tutarları ve bütçelenen tutarları. 

*Not: İsterseniz bu alıştırma için yeni senaryolar oluşturabilir ve mevcut senaryolar yerine bunları kullanabilirsiniz.* 

[![Yeni senaryolar](./media/screenshot15.png)](./media/screenshot15.png) 

*Not: Julia, bütçe hazırlama için resmi onay sürecini kullanmıyor, bu nedenle bu laboratuvarda İş Akışları, Aşamalar ve İş akışı aşamaları kurulumunu geçiyoruz, Otomatik kurulumu kullanıyor – iş akışını onaylıyoruz. Bu iş akışı yapılandırması için eke bakın*

### <a name="task-4-create-budget-plan-columns"></a>Görev 4: Bütçe planı sütunları oluşturma
Bütçe plan sütunları, bütçe plan belgesi düzeninde kullanılabilen Parasal değere veya miktara dayalı sütunlardır. Örneğimizde Önceki yılın fiili tutarları için bir sütun ve bütçelenen bir yıldaki her bir ayı temsil etmesi için 12 sütun oluşturmamız gerekiyor. Sütunlar Ekle düğmesi tıklandıktan sonra değerler doldurularak veya Veri varlığı yardımıyla oluşturulabilir. Bu laboratuvarda değerleri doldurmak için Veri varlığını kullanacağız. 

4.1. Bütçeleme&gt;Ayar &gt; Bütçe planlama &gt; Bütçe planlama yapılandırması seçeneğinde Sütunlar sayfasını açın. Formun sağ üst köşesindeki Office düğmesine tıklayın ve Sütunlar (filtrelenmemiş) seçeneğini belirleyin. 

[![Filtrelenmemiş sütunlar](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Sistem, değerlerin doldurulması için kullanılacak bir Excel çalışma kitabı açar. İstenirse Düzenlemeyi Etkinleştir ve Bu uygulamaya güven seçeneğine tıklayın. 

4.3. Değerleri doldurmak için daha fazla sütuna ihtiyaç duyacağız. Kılavuza sütunlar eklemek için sağ kenar bölmesinde Tasarım'a tıklayın. 

[![Tasarım](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Kılavuza eklenebilecek sütunları görmek için PlanColumns yanındaki kalem düğmesine tıklayın. 

[![Düzenleme](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Her bir kullanılabilir alana çift tıklayarak bunları Seçili alanlar'a ekleyin ve Güncelleştir'e tıklayın. 

4.6. Excel tablosuna, oluşturulması gereken tüm sütunları ekleyin. Excel'de satırları hızlıca eklemek için Otomatik Doldurma özelliğini kullanın. Satırların tablonun bir parçası olarak eklendiğinden emin olun (dikey kaydırma kullanırken sütun başlıklarını kılavuzun üstünde görebilirsiniz). 

4.7. Uygulamaya geri dönün ve sayfayı yenileyin. Yayımlanan değerler görüntülenir. 

[![Yenile](./media/screenshot23.png)](./media/screenshot23.png)

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Görev 5: Bütçe planı belge düzenleri ve şablonları oluşturma
Düzen; kullanıcı, bütçe planı belgesini açtığında bütçe planı belge satırları ızgarasının nasıl görüneceğini tanımlar. Aynı verileri farklı açılardan görmek için bütçe planı belge düzenine geçiş yapılması da mümkündür. Şimdi, bütçe planı belgesiyle kullanılmak üzere tanımlanan sütunlara sahip olan Julia'nın şimdi de bütçe verilerini oluşturmak için kullandığı Excel tablosuna oldukça benzer bir görünüme sahip olacak bir bütçe plan belgesi düzeni oluşturması gerekiyor (bu laboratuvardaki Senaryoya genel bakış bölümüne bakın) 

5.1. Bütçeleme&gt;Ayar &gt; Bütçe planlama &gt; Bütçe planlama yapılandırma seçeneğinde Düzenler sayfasını açın. Aylık bütçe girişi için yeni bir düzen oluşturun:

-   Ana hesapları ve Ticari birimleri düzeye eklemek için MA+BU boyut setini seçin.
-   Önceki adımda Öğeler bölümünde oluşturulan tüm bütçe planı sütunlarını listeleyin. Önceki yılık fiili tutarları dışındaki tüm sütunları düzenlenebilir hale getirin.
-   Izgarada hangi mali boyutları Tanımlar göstermesi gerektiğini seçmek için Tanımlar düğmesini tıklayın.

[![Açıklamalar](./media/screenshot24.png)](./media/screenshot24.png) 

Bütçe planı düzen tanımına göre, Bütçe verilerini düzenlemek için alternatif bir yöntem olarak kullanılmak üzere Excel şablonu oluşturabilirsiniz. Excel şablonunun, bütçe planı düzen tanımıyla eşleşmesi gerektiğinden Excel şablonu oluşturulduktan sonra bütçe planı düzenini düzenleyemezsiniz, bu nedenle bu görev tüm düzen bileşenleri tanımlandıktan sonra gerçekleştirilmelidir. 

5.2. 5.1 üzerinde oluşturulan düzen için. adım, Şablon &gt; Oluştur düğmesine tıklayın. Uyarı mesajını onaylayın. Şablonu görüntülemek için Şablon &gt; Görünüm düğmelerini tıklayın. 

*Not: "Farklı Kaydet" olarak seçtiğinizden ve düzenleyebilmek için şablonun nerede kaydedileceğinizi seçtiğinizden emin olun. Kullanıcı iletişim kutusunda kaydetmeden "Aç" seçerse, dosya kapandığında yapılmış olan değişiklikler korunmaz.* 
[![Şablon görünümü](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; İsteğe bağlı adım&gt; Daha kullanıcı dostu hale getirmek için Excel şablonunu değiştirin: Toplama formülleri, başlık alanları, biçimlendirme vb. ekleyin. Değişiklikleri kaydedin ve dosyayı Düzen &gt; Yükle'ye tıklayarak bütçe planı düzenine yükleyin. 


### <a name="task-6-create-a-budget-planning-process"></a>Görev 6: Bütçe planlama süreci oluşturma
Julia, bütçe planlarını girmeye başlamak için yukarıdaki tüm kurulumu birleştiren yeni bir bütçe planlama süreci oluşturmalı ve bunu etkinleştirmelidir. Bütçe planlama süreci, bütçe planlarının oluşturulması için hangi bütçeleme organizasyonlarının, iş akışının, düzenlerin ve şablonların kullanılacağını tanımlar. 

6.1. Bütçeleme &gt; Ayar &gt; Bütçe planlama &gt; Bütçe planlama süreci seçeneğine gidin ve yeni bir kayıt oluşturun.

-   Bütçe planlama süreci – DEMF bütçeleme MY2016
-   Bütçe döngüsü – MY2016
-   Genel Muhasebe – DEMF
-   Varsayılan hesap yapısı – Üretim kar ve zarar
-   Organizasyon hiyerarşisi – laboratuvarın başında oluşturduğunuz hiyerarşiyi seçin
-   Bütçe planlama iş akışı– Otomatik ata – Finans departmanı için iş akışını onaylayın
-   Bütçe planlama aşaması kuralları ve şablonlarında, her bir iş akışı Bütçe planlama aşaması için Satırların eklenmesinin ve Satırların değiştirilmesinin mümkün olup olmadığını ve varsayılan olarak hangi Düzenin kullanılacağını seçin

*Not: Alternatif düzenler düğmesini tıklayarak ek belge düzenleri oluşturabilir ve bunları bütçe planlama iş akışı aşamasına dahil edilmek üzere atayabilirsiniz.* 

[![Diğer düzenler](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Bu bütçe planlama iş akışını etkinleştirmek için Eylemler &gt; Etkinleştir'i seçin. 

[![Etkinleştir](./media/screenshot28.png)](./media/screenshot28.png)

## <a name="exercise-2-process-simulation"></a>Alıştırma 2: İşlem simülasyonu

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Görev 7: Genel muhasebeden bütçe planı için ilk verileri oluşturma
7.1. Bütçeleme &gt; Periyodik &gt; Genel muhaseben bütçe planı oluştur öğelerini seçin. Periyodik süreç parametrelerini doldurun ve Oluştur'a tıklayın. 

7.2. Oluşturma süreci tarafından oluşturulan bir bütçe planını bulmak için Bütçeleme &gt; Bütçe planları seçeneğine gidin. 

[![Bütçe planı](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Belge numarası köprüsünü tıklayarak belge bilgilerini açın. Bütçe planı, bu laboratuvar sırasında oluşturulan düzende tanımlandığı şekilde görüntülenir. 

[![Bütçe planı görünümü](./media/screenshot31.png)](./media/screenshot31.png)

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Görev 8: Önceki yılın fiili değerlerine dayalı olarak mevcut yıl bütçesi oluşturma
Bütçe planları için bir senaryodaki bilgileri kolayca başka bir senaryoya kopyalamak / bunları dönemler arasında dağıtmak / boyutlara atamak için bütçe planında tahsisat yöntemleri kullanılabilir. Mevcut yıl bütçesini önceki yılı fiili tutarlarından oluşturmak için tahsisatları kullanacağız. 

8.1. Bütçe planı belge kılavuzundaki tüm satırları seçin ve Bütçe tahsis et seçeneğine tıklayın. 

[![Tüm satırlar](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Tahsisat yöntemi, Dönem anahtarı, Kaynak ve hedef senaryoları seçin ve Tahsis Et'e tıklayın. 

[![Tahsis et](./media/screenshot33.png)](./media/screenshot33.png)

Önceki yılın gerçek tutarları, geçerli yılın bütçesine kopyalanır ve bunları Satış eğrisi dönem anahtarını kullanarak dönemlere tahsis edin. 

[![Satış eğrisi](./media/screenshot34.png)](./media/screenshot34.png)

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Görev 9: Bütçe planı belgesini Excel kullanarak ayarlama ve belgeyi son haline getirme
9.1. Excel'de belge içeriklerini açmak için Çalışma Sayfası düğmesine tıklayın.

9.2. Excel çalışma kitabı açıldığında bütçe planı belgesindeki sayıları ayarlayın ve Yayımla düğmesine tıklayın.

9.3. Bütçe planı belgesine geri dönün. İş Akışı &gt; Belgeyi Otomatik Onaylamaya gönder seçeneğine tıklayın.

[![Otomatik-onayla](./media/screenshot37.png)](./media/screenshot37.png) 

İş akışı tamamlandıktan sonra bütçe planı belge aşaması Onaylandı olarak değişir. [![Onaylandı](./media/screenshot38.png)](./media/screenshot38.png)

## <a name="appendix"></a>Ek

### <a name="auto-approve-workflow-configuration"></a>İş akışı yapılandırmasını otomatik onaylama

A. Bütçeleme &gt; Ayar &gt; Bütçe planlama &gt; Bütçeleme iş akışları. Bütçe planlama iş akışları şablonunu kullanarak yeni bir iş akışı oluşturun:

[![Yeni bir iş akışı oluşturun](./media/screenshot39.png)](./media/screenshot39.png)

Bu iş akışı yalnızca bir görev içerir: Aşama geçişi bütçe planı. 

[![Aşama geçişi bütçe planı](./media/screenshot40.png)](./media/screenshot40.png) 

İş akışını kaydetme ve etkinleştirme. 

B. Bütçeleme &gt; Kur &gt; Bütçe planlama &gt; Bütçe planlama yapılandırma seçimlerini yapın. Aşamalar sekmesinde 2 aşama oluşturun: Başlangıç ve Gönderildi. 

[![Başlangıç ve gönderilen](./media/screenshot41.png)](./media/screenshot41.png)

C. Bütçeleme &gt; Kur &gt; Bütçe planlama &gt; Bütçe planlama yapılandırma seçimlerini yapın. İş Akışı Aşamaları sekmesinde, A adımında oluşturulan iş akışı Otomatik Onaylama'yı Başlangıç ve Gönderildi aşamalarıyla ilişkilendirin.

[![Bütçeleme ve bütçe planlama](./media/screenshot42.png)](./media/screenshot42.png)  





[!INCLUDE[footer-include](../../includes/footer-banner.md)]