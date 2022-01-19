---
title: Görev yönetimi
description: Bu konuda, Microsoft Dynamics 365 Human Resources'ta kullanılabilen görev yönetimi işlevleri açıklanmaktadır.
author: twheeloc
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 614f37236bbd0239925e37ebf29f59ac006d09cd
ms.sourcegitcommit: 4f84540e6121ca3d5ae52ee07e414116d423cefa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/03/2022
ms.locfileid: "7948802"
---
# <a name="task-management"></a>Görev yönetimi

Görev yönetimi, işe almak (ekleme), sona erdirmek (çıkarma) ve transfer (geçiş) çalışanları için tamamlanması gereken görevler oluşturmanıza olanak sağlar. Görev yönetimi, denetim listeleri kavramını kullanır. Denetim listesi; ekleme, çıkarma veya geçiş görevlerinin bir listesidir. Görev yönetimi, görevleri birlikte gruplamak ve onları bireylere veya gruplara atamak için denetim listelerini kullanır. Ekleme, çıkarma ve geçişler için denetim listesi işlevi benzerdir.

## <a name="checklist-overview"></a>Denetim listesine genel bakış

Denetim listesi bir görev grubudur. Denetim listeleri, görevleri gruplandırmak için size esnek bir yöntem sağlar ve yeniden kullanılabilir (örneğin ek çalışanlar işe aldığınızda). Gereksinim duyduğunuz kadar çok sayıda denetim listesi oluşturabilir ve aynı görevleri birden çok denetim listesine atayabilirsiniz.

### <a name="examples"></a>Örnekler

Aşağıdaki örneklerde, denetim listelerinin ekleme işleminde nasıl kullanılabileceği gösterilmektedir. Ancak ekleme, çıkarma ve geçişler için denetim listesi işlevi benzer olduğundan bilgiler, çıkarma ve geçiş işlemleri için de geçerlidir.

Ekleme işleminin bir parçası olarak, İnsan kaynakları (İK) uzmanları gelen ve son işe alınan çalışanların ekleme ilerlemesini izleyen görevler oluşturabilir. Ekleme işlemi, çalışanın konumuna veya coğrafi konumuna bağlı olarak değişebileceğinden, farklı işe alma durumlarını karşılamak için çoklu ekleme listesi oluşturabilirsiniz.

**Örnek 1**

Amerika Birleşik Devletleri'nde işe alınan her çalışan, vergi stopaj formlarını doldurma gibi görevleri tamamlamalıdır. Ancak, şirket arabası atanması gibi görevler yalnızca yönetim düzeyi personele uygulanabilir. Bu durumda, iki ekleme denetim listesi oluşturulabilir: **Yalnızca ABD tabanlı çalışanlar** ve **Yalnızca yöneticiler**. Daha sonra Amerika Birleşik Devletleri'nde bir orta düzey yönetici işe alındığında **ABD tabanlı çalışanlar** denetim listesi seçilir. Ancak, Amerika Birleşik Devletleri'nde bir yönetici işe alındığında, gerekli tüm ekleme görevlerinin tamamlandığından emin olmak için her iki denetim listesi seçilir.

**Örnek 2**

Bir şirketin hem mevsimsel çalışanları hem de düzenli olarak tam zamanlı çalışanları vardır. Bazı görevler (yeni çalışanın varış süresini doğrulama gibi) her iki türden çalışan için geçerlidir ancak bazı ek görevler yalnızca düzenli olarak tam zamanlı çalışanlar için geçerlidir. Bu durumda, iki denetim listesi oluşturabilirsiniz. Her iki denetim listesi de mevsimsel ve düzenli tam zamanlı çalışanlara uygulanan görevleri içerir, ancak yalnızca bir kontrol cetveli düzenli tam zamanlı çalışanlara özgü görevleri içerir.

## <a name="task-management-workspace"></a>Görev yönetimi çalışma alanı

**Görev yönetimi** çalışma alanı; ekleme, çıkarma ve geçiş işlemlerindeki kişilere atanan tüm görevleri listeler. Bir işlemle ilgili görevleri görüntülemek için, sol üst köşedeki uygun sekmeyi seçin: **Ekleme**, **Çıkarma** veya **Geçişler**. Varsayılan olarak, **Görev yönetimi** çalışma alanına yalnızca İK uzmanları erişebilir.

**Ekleme** sekmesi, gelen çalışanları gösteren **Yakında başlıyor** listesini ve yeni işe alınan çalışanları gösteren **Yeni işe alınanlar** listesini içerir. Her iki listede de yalnızca bir çalışan seçebilirsiniz. Bir çalışan seçtiğinizde, o çalışanın ekleme ile ilişkili olduğu tüm görevler sayfanın sağ tarafında gösterilir. **Ekleme** sekmesi ayrıca gelen veya son işe alınan çalışanların tüm görevlerini gösteren bir **Tüm görevler** listesi de içerir. Son olarak ise, süresi geçen görevlerin bir listesini ve geçerli kullanıcıya atanan görevlerin listesini içerir.

**Çıkarma** sekmesi, şirketten çıkış yapan çalışanların ve şirketten çıkış yapmış olan çalışanların bir listesini içerir. Her iki listede de yalnızca bir çalışan seçebilirsiniz. Bir çalışan seçtiğinizde, o çalışanın çıkarma ile ilişkili olduğu tüm görevler gösterilir. **Çıkarma** sekmesi ayrıca çıkan veya çıkmış çalışanların tüm görevlerini gösteren bir **Tüm görevler** listesi de içerir. Son olarak ise, süresi geçen görevlerin bir listesini ve geçerli kullanıcıya atanan görevlerin listesini içerir.

**Geçişler** sekmesi, pozisyonları değiştiren veya en son değiştirilen pozisyonları olan tüm çalışanlar için tüm görevleri gösteren **Tüm görevler** listesini içerir. Ayrıca süresi geçen görevlerin bir listesini ve geçerli kullanıcıya atanan görevlerin listesini içerir.

Her üç sekmede İK asistanları ve yöneticiler aşağıdaki faaliyetleri tamamlayabilir:

- Bir çalışana denetim listesi uygulayın.
- Görevin durumunu güncelleştirin.
- Görevi yeniden atayın.
- Görevin son tarihini güncelleştirin.

> [!NOTE]
> Varsayılan olarak, **Ekleme** sekmesi, son yedi gün içinde işe alınan çalışanları gösterir. Bu ayarı değiştirmek için, **İnsan kaynakları parametreleri** sayfasında, **Genel** sekmesinde **En son işe alımlar** için bir zaman dilimi belirleyin. **En son işe alımlar** listesindeki bilgiler belirli sayıda gün, ay veya yıl için gösterilebilir. Örneğin, son 14 günde işe alınan çalışanların listesini görüntülemek için **Dönem** alanını **14** olarak ve **Birim** alanını **Gün** olarak ayarlayın.
>
> **İnsan kaynakları parametreleri** sayfasında, **Çıkarma** sekmesinde gösterilen çıkış ve çıkış çalışanlarına ait tarih aralığını da güncelleştirebilirsiniz.
>
> Bu ayarlar, **Personel yönetimi** çalışma alanına da uygulanır.

## <a name="setting-up-tasks"></a>Görevleri ayarlama

Görevleri tek olarak oluşturup birden çok denetim listesinde yeniden kullanabilirsiniz. Görev oluşturmak için, **Ekleme kurulumu** sayfasında, **Görevler** sekmesinde, **Yeni**'yi seçin.

Alternatif olarak, görevleri doğrudan bir denetim listesine ekleyebilirsiniz. Bir denetim listesine görev eklemek için, **Ekleme kurulumu** sayfasında, **Denetim listesi** sekmesinde, görevi eklemek için yeni bir denetim listesi oluşturun veya görevi varolan bir denetim listesine ekleyin.

> [!NOTE]
> Bir görevi doğrudan bir denetim listesine eklerseniz diğer denetim listelerinde bunu yeniden kullanamazsınız.

Aşağıdaki tablo, iki yöntemden birini kullanarak görev oluşturduğunuzda kullanılabilir olan alanları tanımlar.

| Alan           | Açıklama |
|-----------------|-------------|
| Görev            | Görevin adını girin. |
| Açıklama     | Görevin bir açıklamasını girin. |
| İsteğe bağlı        | Görevin isteğe bağlı olup olmadığını ve yalnızca bilgilendirme amaçlı olup olmadığını belirtin. |
| Görev bağlantısı       | Harici bir web sayfasının veya kullanıcının görevi tamamlaması gereken uygulamada belirli bir sayfanın URL'sini girin. Daha fazla bilgi için bkz. [Görev bağlantıları](#task-links) bölümü. |
| Atama türü | Görevler belirli bir çalışana, pozisyona veya pozisyon grubuna, etkilenen çalışanın yöneticisine (diğer bir deyişle, ekleme, çıkarma işlemi veya geçiş işleminin parçası olan çalışan) veya etkilenen çalışana atanabilir. Atama tipini seçin. Daha fazla bilgi için bkz. [Atama tipleri](#assignment-types) bölümü. |
| Atanan     | Görevi atanacak olan belirli bir çalışanı, pozisyonu veya pozisyon grubunu seçin. |
| İlgili kişi  | Görevle ilgili sorular varsa bağlantı kurulacak kişiyi belirtin. |
| Son tarih sapması | Görevin sona ermesi sırasında ekleme, sonlandırma veya geçiş tarihinden önceki veya sonraki gün sayısını belirtin. Daha fazla bilgi için bkz. [Görev son tarihleri ve Son tarih sapması alanı](#task-due-dates-and-the-due-date-offset-field) bölümü. |
| Yönergeler    | Görevi tamamlamaya yönelik talimatları girin. Daha fazla bilgi için [Talimatlar](#instructions) bölümüne bakın. |

### <a name="task-links"></a>Görev bağlantıları

Görev bağlantısı, Dynamics 365 uygulamasında harici bir web sayfasına veya bir sayfaya bağlantı sağlar. Göreve atanan kişinin belirli bir web sayfasına veya bu görevi tamamlamak için Dynamics 365 uygulamasında belirli bir sayfaya gitmesi gerekiyorsa görev bağlantısını belirtebilirsiniz. Görev bağlantısı oluşturduğunuzda, aşağıdaki seçeneklerden birini seçebilirsiniz:

- **Menü maddesi** – Bu seçeneği belirlerseniz, Dynamics 365 uygulamasında tüm sayfaların listesi gösterilir. Listede bir sayfa seçin.
- **URL** – Bu seçeneği belirlerseniz, göreve atanmış olan kişinin gitmesini istediğiniz web sayfasının URL'sini girin. Belirtilen sayfa, Dynamics 365 uygulamasının parçası olmayan bir sayfa olabilir.
- **Çalışan ayrıntıları** – Bu seçeneği belirlerseniz, aşağıdaki seçeneklerden birini belirleyin:

    - **Çalışan self servis eylemleri** – Bu seçenek, **Çalışan self servis**'de bulunan sayfaların listesini gösterir. Eklenen çalışana atanmış görevin, **Çalışan self servis**'te tamamlanması gerekiyorsa kullanın. Örneğin, çalışanın kendi kişisel ilgili kişi bilgilerini girmesini istiyorsanız, **Çalışan self servis eylemleri**'ni seçin ve **Kişisel Ayrıntılar&gt;Kişisel Bilgiler**'i seçin.
    - **Çalışan yönetim eylemleri** – Bu seçenek, çalışanın kaydıyla ilişkili olan, ancak çalışanların erişemediği sayfaların listesini gösterir. Örneğin, görev sahibinin maaş bilgileri gibi eklenen bir çalışana özgü bilgileri girmesini istiyorsanız, **Çalışan yönetim eylemleri**'ni seçin ve sonra **Ücret&gt;Sabit ücret**'i seçin.

### <a name="assignment-types"></a>Atama türleri

Bir çalışan işe alındığında, işten çıkarıldığında veya transfer edildiğinde, bir veya daha fazla onay listesi seçilebilir. Denetim listesi seçildikten ve işe alma, sonlandırma veya aktarım işlemi tamamlandıktan sonra, görevler oluşturulur ve ilerlemeyi izlemek için kullanıcılara atanır.

Görev oluşturulduğunda, belirli bir kullanıcıya atanır. Görevin atandığı kullanıcı, o görev için seçilen atama türüne bağlıdır. Aşağıdaki değerler, **Atama türü** alanında kullanılabilir:

- **Çalışan** – Görevi belirli bir çalışana atayın. Bu değeri seçtikten sonra, **Atanan kişi** alanında çalışanı seçin.
- **Konum** – Görevi belirli bir konuma atayın. Bu değeri seçtikten sonra, **Atanan kişi** alanında konumu seçin.

    Örneğin, bir BT mühendisi her zaman dizüstü bilgisayarı yeni bir çalışan için hazırlamaktan sorumlu olacaktır. Bu durumda dizüstü bilgisayar yapılandırması görevini oluştururken atama türü olarak **Pozisyon**'u ve ardından pozisyon olarak **BT mühendisi**'ni seçin. Daha sonra, bir çalışan işe alındığında ve denetim listesi atandığında, dizüstü bilgisayar konfigürasyon görevi, işe alma eylemi girildiği sırada BT mühendisinin konumunda hangi çalışana ait olduğunu atanır.

- **Grup** – Görevi bir pozisyon grubuna atayın (atama grubu). Bu değeri seçtikten sonra, **Atanan kişi** alanında grubu seçin. Daha fazla bilgi için, bkz. [Atama grupları ayarlama (İsteğe bağlı) ](#setting-up-assignment-groups-optional) bölümü.
- **Yönetici** -Görevi; işe alınan, işten çıkarılan veya aktarılan çalışanın yöneticisine atayın.

    > [!IMPORTANT]
    > Bir denetim listesi uygulandığında; işe alınan, işten çıkarılan veya transfer edilen çalışana herhangi bir konum atanmamışsa yönetici saptanamaz. Bu durumda, görev denetim listesi sahibine atanır. Daha fazla bilgi için bkz. [Denetim listelerini ayarlama](#setting-up-checklists) bölümü.

- **Çalışan** - İşe alınan, sonlandırılan veya transfer edilen çalışanı atayın.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Görev son tarihleri ve Son tarih sapması alanı

Görev son tarihleri, istihdam başlangıç tarihi, sonlandırma tarihi veya geçiş tarihine dayanır. Diğer görevlerin daha sonra tamamlanması için, bazı görevlerin bir çalışanın başlangıç tarihinden önce tamamlanması gerekir. Bir görevi tanımlarken, **Son tarih sapması** alanını, başlangıç tarihi, işten çıkarma tarihi veya geçiş tarihine relatif bir son tarihe belirleyin. Örneğin, bir BT mühendisi bu çalışanın başlangıç tarihinden iki gün önce yeni bir çalışan için dizüstü bilgisayar hazırlaması gerekir. Bu durumda, dizüstü bilgisayar konfigürasyon görevini oluşturduğunuzda, **Son tarih sapma** alanını **-2** olarak ayarlayın. Daha sonra, bir çalışanın başlangıç tarihi 5 Mayıs ise, görevin son süresi 3 Mayıs olur.

> [!NOTE]
> Son tarihler iş süreci oluşturulduktan sonra da ayarlanabilir.

Son tarihler, denetim listesiyle ilişkilendirilmiş takvime göre hesaplanır. Daha fazla bilgi için bkz. [Denetim listelerini ayarlama](#setting-up-checklists) bölümü.

### <a name="instructions"></a>Yönergeler

Karmaşık görevler için birden fazla adım gerekebilir veya görevleri uygulayan kişilerin ek bilgiler vermesi gerekebilir. **Yönergeler** alanında, görevin atandığı kişiye görevin nasıl tamamlanacağı konusunda yönergeler veya ek bilgiler girebilirsiniz.

## <a name="setting-up-checklists"></a>Denetim listelerini ayarlama

Denetim listesi bir görev grubudur. Gereksinim duyduğunuz kadar çok sayıda denetim listesi oluşturabilir ve aynı görevleri birden çok denetim listesine atayabilirsiniz. Bir denetim listesi oluşturduğunuzda, bir sahip ve takvim belirtirsiniz.

Görevin **Atama türü** alanı **Pozisyon**, **Yönetici** veya **Grup** olarak ayarlanmışsa ancak atama türünden belirli bir kişi türetilemiyorsa görev, denetim listesi sahibine atanır. Aşağıda, görevlerin denetim listesi sahibine atanacağı durumlara örnek verilmiştir:

- İşe alınan veya işten çıkarılan çalışana bir konum atanmaz. Çalışanın pozisyon ataması olmadığından yönetici belirlenemez.
- **Atama türü** alanı **Pozisyon** olarak ayarlanmıştır ancak görev oluşturulduğu sırada pozisyona herhangi bir çalışan atanmamış. Örneğin, **Dizüstü Bilgisayar Kurma** görevi, pozisyon numarası 000876 ( **Teknik Destek Uzmanı**) olarak atanır. Bir çalışanın işe alma sırasında, pozisyon 000876'ya hiçbir çalışan atanmaz. Bu nedenle, denetim listesi sahibi için bir görev oluşturulur.
- **Atama türü** alanı **Grup** olarak ayarlanmıştır ancak görev oluşturulduğu sırada gruptaki pozisyonlara herhangi bir çalışan atanmamış.

Denetim listesi için belirtilen takvim, bu denetim listesinin parçası olan görevlerin son tarihini hesaplamak için kullanılır. Takvim kurulumunda çalışma ve çalışılmayan günler tanımlanmıştır. Çalışma günleri, görevlerin son tarihi hesaplanırken ve çalışılmayan günler hariç tutulacaksa dahil edilir. Çalışma dışı günler hafta sonları ve tatiller içerir. 

Takvim ayarladıktan sonra bir denetim listesi şablonuyla ilişkilendirilir. Bu şekilde, denetim listesindeki tüm görevlerin son tarihi aynı şekilde hesaplanır. Birden çok takvim ayarlayabilirsiniz ancak her bir denetim listesi ile yalnızca bir takvim ilişkilendirilebilir.

## <a name="setting-up-assignment-groups-optional"></a>Atama grupları ayarlama (İsteğe bağlı)

Bazen bir görevden bir grup kişi sorumlu olur. Örneğin, dizüstü bilgisayarların yeni kişiler için hazırlanmasından bir grup BT çalışanı sorumlu olabilir.

Atama grubu oluşturmak için aşağıdaki adımları izleyin.

1. **Grup ataması** sayfasında, **Yeni**'yi seçin.
1. Bir ad (örneğin, **BT dizüstü bilgisayar**) ve grup için bir açıklama girin.
1. **Kaydet**'i seçin.
1. **Üyeler** hızlı sekmesinde **Ekle**'yi seçin.
1. **Pozisyonlar** alanında, görevden sorumlu tüm pozisyonları seçin.

Atama grubu oluşturulduktan sonra, görev oluşturulduğunda kullanılabilir. Bir görev için belirli bir grup seçmek üzere, **Atama türü**'nde **Grup** seçmeniz gerekir. Oluşturduğunuz grup bundan sonra **Atanan kişi** alanında seçilebilecek.

> [!IMPORTANT]
> Görev bir gruba atanmışsa, gruptaki bir kişi bunu tamamladığında görev **Tamamlandı** olarak işaretlenir. Görevler işe alma, sonlandırma veya geçiş sırasında oluşturulur. Bunlar, gruba dahil edilen pozisyonlara atanan kullanıcılar için oluşturulur.

## <a name="setting-up-task-groups-optional"></a>Görev grupları ayarlama (İsteğe bağlı)

Ekleme, çıkarma veya geçiş işlemi birçok görev içerebilir. Gerekli tüm görevlerin bir denetim listesi için atanmasını kolaylaştırmak amacıyla, ilgili görevleri kategorilere ayırmak için isteğe bağlı görev grupları oluşturabilirsiniz. Örneğin, yeni bir çalışan için İK, BT ve Maaş bölümlerinin her birinin özel görevleri olması gerekir. Bu nedenle, aşağıdaki görev gruplarını oluşturursunuz: **İK**, **BT** ve **Maaş**. Daha sonra, bir görev oluşturduğunuzda, bu görev gruplarından birini bununla ilişkilendirebilirsiniz.

Bir denetim listesine görev eklemek istediğinizde, istenen görevin atandığı görev grubuna göre görev listesini süzebilirsiniz. Örneğin, bir kontrol cetveli şablonu oluşturduğunuzda, listeye filtre uygulayabilir ve yalnızca **BT** görev grubuna atanmış BT görevlerinin gösterilmesini sağlayabilirsiniz. Bu nedenle, yalnızca ilgili BT görevlerinin seçildiğinden emin olabilirsiniz.

## <a name="using-checklists"></a>Denetim listelerini kullanma

Bir çalışan işe alındığında, işten çıkarıldığında veya transfer edildiğinde bir veya daha fazla onay listesi seçilebilir. Görev bitiş tarihleri ve çalışan atamaları işe alma, sonlandırma veya geçiş işlemi tamamlandıktan sonra oluşturulur. Örneğin, **İşe alma** veya **İşe alma ve ayrıntı ekleme** düğmesini seçtiğinizde, görevler, atama türüne göre bireyler için oluşturulur.

Bir son tarih, çalışanın başlangıç tarihinden vade tarihi farkı eklenerek veya çıkarılarak her göreve atanır. Daha fazla bilgi için bkz. [Görev son tarihleri ve Son tarih sapması alanı](#task-due-dates-and-the-due-date-offset-field) bölümü.

Personel eylemleri kullanıyorsanız, görevler **Tamamlandı** düğmesi seçildiğinde veya eylem onaylandığında oluşturulur.

**Görev yönetimi** çalışma alanında, çalışanı basit liste sayfasında veya ayrıntılar sayfasında seçerek ve **Denetim listesi uygula**'yı seçerek bir çalışana denetim listesi uygulayabilirsiniz. **Hedef tarih** alanının değeri, görevlerin son tarihinin hesaplanmasında kullanılır. Genellikle, hedef tarih çalışanın işe alma, sonlandırma veya geçiş tarihiyle eşleşmelidir.

Ayrıca, **Çalışan** sayfasını açıp, menüden **Denetim listeleri**'ni seçerek bir çalışana denetim listesi uygulayabilirsiniz.

## <a name="completing-tasks"></a>Görevleri tamamlama

**Çalışan self servis** sayfasında, bir çalışan kendine atanan tüm görevleri görüntüleyebilir. Atanan her görev için **Görev**, **Açıklama**, **Yönergeler** ve **İlgili kişi** değerleri gösterilir. Ek olarak, her görev için çalışan, Dynamics 365 uygulamasında ilişkili harici web sayfasını veya ilişkili sayfayı açabilir.

Görevler, **Devam ediyor**, **İptal edildi** veya **Tamamlandı** olarak işaretlenebilir. Görev bir gruba atanmışsa gruptaki bir kişi bunu tamamladığında görev **Tamamlandı** olarak işaretlenir.

Görevler yeniden atanabilir.
