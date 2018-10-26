---
title: "Kullanıcı deneyimini kişiselleştirme"
description: "Bu konuda Microsoft Dynamics 365 for Finance and Operations'ı nasıl kişiselleştirebileceğiniz açıklanmaktadır."
author: TLeforMicrosoft
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7344f460fcb443a78b254e2387fbf5c9134bf674
ms.openlocfilehash: 1860b603f789aabca1ca58848a88e11a6e08e31f
ms.contentlocale: tr-tr
ms.lasthandoff: 09/28/2018

---

# <a name="personalize-the-user-experience"></a>Kullanıcı deneyimini kişiselleştirme

[!include [banner](../includes/banner.md)]

Bu konuda Microsoft Dynamics 365 for Finance and Operations'ı nasıl kişiselleştirebileceğiniz açıklanmaktadır.

Finance and Operations'ta üç temel kişiselleştirme sınıfı vardır. 
- Bir kurulum sayfasında yapılan kişiselleştirmeler. Örneğin renk teması ve saat dilimi.
- *Dolaylı* kişiselleştirmeler denilen, sayfa kullanımıyla ilgili kişiselleştirmeler. Örneğin, Finance and Operations, ayarladığınız takdirde ızgara sütunlarının genişliğini ve hızlı sekmelerin genişletilme/daraltılma durumunu izler. 
- Bir kullanıcının bir öğenin bir sayfadaki görünüşünü veya davranışını değiştirerek sayfanın görünümünde değişiklik yapmak için, genellikle etkileşimli bir kişiselleştirme moduyla uyguladığı kişiselleştirmeler. Bu kişiselleştirmelere *açık* kişiselleştirmeler adı verilir. Örneğin, kullanıcı sayfadaki öğeleri eklemiş, gizlemiş veya yeniden sıralamış olabilir.

Kullanıcının Finance and Operations'ta yaptığı her kişiselleştirme, kişiselleştirmenin türünden veya kullanıcının etkileşimde olduğu şirketten bağımsız olarak yalnızca o kullanıcıya aittir. Bir kullanıcının sayfada yaptığı değişiklikler sistemdeki diğer kullanıcıları etkilemez.

## <a name="system-wide-options-for-the-current-user"></a>Geçerli kullanıcının sistem çapında seçenekleri
**Kullanıcı seçenekleri** sayfası, geçerli kullanıcı için sistem genelinde çeşitli ayarlar içerir. **Kullanıcı seçenekleri** sayfasını açmak için gezinti çubuğundaki **Ayarlar** menüsünü (çark simgesi) ve ardından **Kullanıcı seçenekleri**'ni seçin. **Kullanıcı seçenekleri** sayfasında çeşitli kullanıcı ayarlarını içeren dört sekme vardır:

- **Görsel** – Bir renk teması ve sayfalardaki öğelerin varsayılan boyutunu seçin.
- **Tercihler** – Finance and Operations'ı her açtığınızda kullanılacak varsayılan değerleri seçin. Bu değerler şirket, ilk sayfa ve varsayılan görüntüleme/düzenleme modunu içerir. (Görüntüleme/düzenleme modu, sayfayı her açışınızda, görüntülemeye karşı kilitli olup olmadığını veya düzenlemeye açık olup olmadığını belirler.) Bu sekmede dil, saat dilimi, tarih, saat ve sayı biçimi için seçenekler de vardır. Son olarak, bu sekme sürümden sürüme değişiklik gösteren çeşitli tercihler içerir.
- **Hesap** – Kullanıcı adınızı ve hesapla ilgili diğer seçenekleri ayarlayın.
- **İş akışı** – İş akışıyla ilgili seçenekleri belirleyin.

## <a name="implicit-personalizations"></a>Dolaylı kişiselleştirmeler
Dolaylı kişiselleştirmeler, mevcut görünür durumlarını "anımsayan" denetimlerle etkileşime girerek yaptığınız kişiselleştirmelerdir.

- **Izgara sütunları** – Izgaradaki bir sütunun genişliğini, sütun başlığının solundaki veya sağındaki boyutlandırma çubuğunu seçerek ve bunu sütun istediğiniz genişliğe gelene kadar sola veya sağa kaydırarak ayarlayabilirsiniz. Finance and Operations, sütun için ayarladığınız genişlik bilgisini depolar. Daha sonra, o ızgarayı içeren sayfayı her açtığınızda sütunu o genişliğe ayarlar.
- **Hızlı Sekmeler** – Bazı sayfaların *Hızlı Sekmeler* olarak bilinen genişletilebilir bölümleri vardır. Finance and Operations, genişlettiğiniz veya daralttığınız hızlı sekmeler hakkındaki bilgileri depolar. Bunun ardından, sayfaya her dönüşünüzde o hızlı sekmeler, sayfayla son etkileşiminize göre genişletilir veya daraltılır. Bazı durumlarda, Finance and Operations'ın bir hızlı sekme genişletilene kadar o hızlı sekmeye ilişkin bilgilere ulaşmasına gerek olmadığı için, hızlı sekmeyi daraltarak sistem performansının artırılmasına yardımcı olabilirsiniz. Bu konuda daha ileride açıklanacağı gibi, bir sayfadaki hızlı sekmelerin sırasını da değiştirebilirsiniz.
- **Bilgi Kutuları** – Bazı sayfalarda *Bilgi Kutusu bölmesi* olarak bilinen bir bölüm vardır. Bu bölme, sayfadaki güncel konuyla ilgili salt okunur bilgileri içerir. Bilgi Kutusu bölmesindeki her bölüm bir *Bilgi Kutusu* olarak adlandırılır. Tüm Bilgi Kutusu bölmesini gizleyebilir veya gösterebilir ve ayrıca, Bilgi Kutularını tek tek genişletebilir veya daraltabilirsiniz. Finance and Operations, tercihlerinizi depolar. Daha sonra sayfaya her dönüşünüzde, sayfayla son etkileşiminize göre, Bilgi Kutusu bölmesinin ve tek tek Bilgi Kutularının durumları geri yüklenir. Bazı durumlarda, Finance and Operations'ın bir Bilgi Kutusu genişletilene kadar o Bilgi Kutusuna ilişkin bilgilere ulaşmasına gerek olmadığı için, Bilgi Kutusunu daraltarak sistem performansının artırılmasına yardımcı olabilirsiniz.
- **Eylem Bölmeleri** – Bir *Eylem Bölmesi* çoğu sayfanın en üst kısmında görünür. Eylem Bölmesi, geçerli sayfada gerçekleştirebildiğiniz eylemlerin birçoğu için düğmeler içerir. Bu düğmeler genellikle sekmeler halinde düzenlenir. Eylem Bölmesini açık haliyle sabitleyebilir veya varsayılan olarak daraltabilirsiniz. Daha sonra, sayfayı sonraki açışınızda Finance and Operations bu Eylem Bölmesinin sabit durumunu geri yükleyecektir. Eylem bölmesi açık haliyle sabitlendiyse, Finance and Operations, son kullandığınız eylemlerin sekmelerini de gösterir.
- **Hızlı Filtreler** – Bir *Hızlı Filtre* birçok kılavuzun üst kısmında görünür. Hızlı Filtre, seçtiğiniz bir sütuna göre ızgarayı filtrelemenize olanak sağlar. Finance and Operations, filtre uyguladığınız sütunu depolar. Daha sonra, o ızgarayı içeren sayfayı sonraki açışınızda ızgara aynı sütunda filtrelenir. Bununla birlikte, daha sonra kılavuzu farklı bir sütunda filtreleyebilirsiniz.
- **Sütun başlığı filtreleri** – Bir ızgarayı *Sütun başlığı filtrelerini* kullanarak filtrelediğiniz zaman, istediğiniz verileri bulmak için gereksinim duyduğunuzda filtre işlecini değiştirebilirsiniz. Örneğin **ile başlayan** işlecini değiştirip **tam olarak** yapabilirsiniz. Her sütun başlığı filtresi kullandığınız ve filtre işlecini değiştirdiğinizde, Finance and Operations bu değişikliği depolar. Bu sütunu daha sonraki filtreleyişinizde, filtre işlecini geri yükler.
- **Gezinti bölmesi** – Sayfanın sol üst köşesindeki *Menü* düğmesini seçerek **Gezinti bölmesini** açabilirsiniz. (**Menü** düğmesine bazen *hamburger*, *hamburger menüsü* veya *hamburger düğmesi* adı da verilir.) Gezinti bölmesini açık haliyle sabitleyebilir veya varsayılan olarak daraltılmış tutabilirsiniz. Gezinti bölmesini açık haliyle sabitlemenizin ardından, Finance and Operations bölmeyi siz daraltana kadar açık tutar.

## <a name="explicit-personalizations"></a>Açık kişiselleştirmeler
Farklı kişi ve şirketler, kendileri için en önemli buldukları veya işlerini yürütme tarzı açısından gerekli bulmadıkları veriler bakımından farklı bakış açılarına sahiptir. Finance and Operations'ta bilgilerinizi sıralama ve bilgilerinizle etkileşime girme tarzını özelleştirebilirsiniz. Bazı bilgilerin gizlenmesi gerektiğini de belirtebilirsiniz. Bu yetenekler kişisel ve üretken bir deneyim için anahtar niteliğindedir ve açık kişiselleştirmelere örnektir. Açık kişiselleştirmeler, bir öğenin veya sayfanın görünüşünü veya davranışını değiştirmek amacıyla açık şekilde gerçekleştirdiğiniz kişiselleştirmelerdir.

### <a name="shortcut-menu-options"></a>Kısayol menüsü seçenekleri
Kısayol menüleri, sizin veya şirketinizin gereksinimlerini daha iyi karşılamak amacıyla bir sayfayı açıkça değiştirmek için birkaç yol sağlar. (Kısayol menüsü *sağ tıklama menüsü* veya *bağlam menüsü* olarak da bilinir.)

Bir sayfada yapılabilecek en tipik ve önemli değişikliklerden bazıları, kısayol menüsündeki seçenekler olarak doğrudan sunulur. Örneğin, Platform güncelleştirmesi 17'den itibaren, isterseniz bir ızgarada sütun eklemek veya gizlemek için bir kılavuz sütun başlığına sağ tıklayıp **Sütunlar ekle** veya **Bu sütunu gizle**'yi seçmeniz yeterlidir.

Ayrıca, açık kişiselleştirmenin en temel türleri de bir öğeye sağ tıklayıp **Kişiselleştir**'i seçerek kullanılabilir. (Sayfanızdaki tüm öğelerin kişiselleştirilemeyeceğini unutmayın.) Bu kişiselleştirme yöntemini kullandığınızda, öğenin özellik penceresi görünür.

[![Bir öğenin özelliklerini kişiselleştirme](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg)

Bir öğeyi aşağıdaki yöntemlerle kişiselleştirmek için özellik penceresini kullanabilirsiniz:

- Öğenin etiketini değiştirmek.
- Öğeyi gizleyerek sayfada gösterilmemesini sağlamak. Alandaki veriler silinmez veya değiştirilmez. Bilgiler artık sayfada görünmez hale gelir.
- Hızlı sekme özet bölümüne bilgi eklemek (öğe, hızlı sekmedeyse).
- Sayfadaki alanlar arasında geçmek için Sekme tuşuna bastığınız sırada alanın atlanmasını sağlamak.
- Alandaki verilerin düzenlenmesini önlemek (herhangi bir kayıt için).

Öğeye bağlı olarak, özellik penceresi başka kişiselleştirme yetenekleri içerebilir. Örneğin, bir kutucuğun özellik penceresi sayesinde o kutucuğu bir panoya yükseltebilir ve bir panonun özellik penceresiyle o panoda yeni bir çalışma alanı oluşturabilirsiniz.

### <a name="the-personalization-toolbar"></a>Kişiselleştirme araç çubuğu
Bir sayfada birden çok değişiklik veya diğer mekanizmalar aracılığıyla gerçekleştirilemeyen değişiklikler yapmak istiyorsanız (öğeleri yeniden düzenlemek gibi), **Kişiselleştirme** araç çubuğunu kullanabilirsiniz. **Kişiselleştirme** araç çubuğunu açmak için, bir öğenin özellik penceresinde **Bu formu kişiselleştir**'i seçin. Her sayfanın Eylem Bölmesinin **Seçenekler** sekmesindeki **Kişiselleştir** grubunda bulunan **Bu formu kişiselleştir**'i de seçebilirsiniz.

[![Kişiselleştirme araç çubuğu](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

#### <a name="navigating-the-page"></a>Sayfada gezinme 
**Kişiselleştirme araç çubuğu** açıkken Sayfada gezinme kabiliyetiniz, çalıştırdığınız platform sürümüne bağlıdır. 

- Platform güncelleştirmesi 19'dan önce, **Kişiselleştirme** araç çubuğu açıkken, sayfa salt okunurdu (hiçbir şey giremezdiniz) ve etkileşime kapalıdır (yalnızca sayfadaki görünür öğelerde değişiklik yapabilirdiniz). Kapatılmış bir bölüm veya farklı bir sekmedeki öğelerde değişiklik yapmak istiyorsanız, **Kişiselleştirme** araç çubuğunu kapatmanız, bir bölümü veya istenilen sekmeyi genişletmeniz ve sonra **Kişiselleştirme** araç çubuğunu yeniden açmanız gerekmekteydi.  

- Platform güncelleştirmesi 19'dan itibaren başlayarak, **Kişiselleştirme** araç çubuğu açıkken, sayfa yine salt okunur moddadır ancak çok daha etkileşimlidir. Özellikle bilgi kutusu bölmesini genişletebilir veya daraltabilir, sekme değiştirebilir ve **Kişiselleştirme** araç çubuğu halen açıkken normalde sayfada yapabileceğiniz şekilde bölümleri genişletebilir veya daraltabilirsiniz. Daraltılabilir bir bölüm veya bir sekmede bir kişiselleştirme değişikliği yapmak için (örneğin bir FastTab'ı gizlemek için) klavye odağında olduğunda sekmeye veya daraltılabilir bölümde çıkan düğmeye basarak bunu tetikleyebileceksiniz.  

#### <a name="personalization-tools"></a>Kişiselleştirme araçları
**Kişiselleştirme** araç çubuğunda aşağıdaki araçlar mevcuttur:

- Bir öğeyi seçip özelliklerini değiştirmek için **Seç** aracını kullanın. **Seç** aracını ve ardından, özellikleri değiştirilecek öğeyi seçin. Bir öğeyi seçtiğinizde, öğenin özellik penceresi görünür ve o öğenin özelliklerini değiştirebilirsiniz. O sayfada kişiselleştirilebilecek başka öğeler için işlemi yineleyebilirsiniz. Ancak, bazı öğeler kullanımda olduğu için, Finance and Operations bu öğelerin bazı özelliklerini değiştirmenize izin vermez. Bu nedenle, bir öğeyi seçtiğiniz zaman bazı özelliklerinin değiştirilemeyeceğini görebilirsiniz. Örneğin, gerekli bir alanı gizleyemezsiniz.

- Bir öğeyi mevcut öğeler grubu içinde farklı bir konuma taşımak için **Taşı** aracını kullanın. (Bir öğeyi üst grubunun dışına taşıyamazsınız.) **Taşı** aracını ve ardından, taşınacak öğeyi seçin. Bir öğe seçtiğinizde, Finance and Operations sayfayı tarayarak, öğenin taşınıp taşınamayacağını belirler. Ardından bir dizi "bırakma bölgesi" oluşturur. Öğeyi mevcut grup içinde sürükledikçe, her "bırakma bölgesi," öğenin bırakılabileceği alanın yanında renkli ve kalın bir çizgi olarak gösterilir.

- Sayfadaki bir öğeyi gizlemek için **Gizle** aracını kullanın. **Gizle** aracını ve ardından, gizlenecek öğeyi seçin. **Gizle** aracını seçtiğiniz zaman, gizli durumdaki tüm öğeler görünür hale gelir ve gölgeli bir kapsayıcıda gösterilir. Bu durumda bu öğeleri gizli olmaktan çıkarabilirsiniz. Seçilen öğeler gizlendiği zaman sayfanın nasıl görüneceğini, **Seç** aracını seçerek görebilirsiniz.
    - Platform Güncelleştirmesi 18 ile başlayarak, gerekli alanları ve gerekli alanları içeren bölümleri gizleyebilirsiniz. Bu basitleştirilmiş deneyimi oluşturmak burada iş mantığı tarafından varsayılan zorunlu alanların görüntülenmemesini sağlar. Bir kaydetmeye teşebbüs edilirse, gizli gerekli alanlar geçici olarak görünür hale gelir. 

- Bir öğenin hızlı sekme özet bölümünde görünmesini isterseniz **Özet** aracını kullanın. Özet aracı yalnızca bir hızlı sekme bölümündeki alanlar için kullanılabilir. **Özet** aracını seçtiğiniz zaman, özet alanı olarak seçilen tüm alanlar gölgeli bir kapsayıcıda gösterilir. Hızlı sekme özetine etkileşimli olarak alan ekleyebilir veya hızlı sekme özetinden alanları seçerek kaldırabilirsiniz.

- Sayfanın klavye sekmesi sırasından bir öğeyi kaldırmak için **Atla** aracını kullanın. **Atla** aracını seçtiğiniz zaman, atlanmış durumdaki tüm öğeler gölgeli bir kapsayıcıda gösterilir. Bunun üzerine, bu öğeleri yeniden sekme sırasına dahil edebilirsiniz.

- Bir öğeyi düzenlenebilir veya düzenlenemez olarak işaretlemek için **Düzenle** aracını kullanın. **Düzenle** aracını seçtiğiniz zaman, düzenlenemez durumdaki tüm öğeler gölgeli bir kapsayıcıda gösterilir. Bu durumda bu öğeleri yeniden düzenlenebilir hale getirebilirsiniz. Bazı alanların gerekli olduğunu ve düzenlenemez yapılamayacağını unutmayın. Bu alanların yanında bir asma kilit simgesi görünür.

- Bir sayfaya eklenebilecek öğelerin listesini görmek için **Ekle** düğmesini kullanın.
    - Sayfanıza alan eklemek için, **Ekle** altındaki **Alan** aracını seçin. **Alan** aracını kullandığınız zaman yalnızca sayfa tanımının bir parçası olan ancak o anda sayfada gösterilmeyen alanları ekleyebilirsiniz. Geçerli sayfa tanımının bir parçası olmayan yeni alanların nasıl oluşturulacağı hakkında bilgi için bkz. [Özel alanlar](user-defined-fields.md). **Alan** aracını seçtikten sonra, ilk olarak, alan eklemek istediğiniz grubu veya bölgeyi seçmeniz gerekir. Bir iletişim kutusunda, seçilen grupla veya bölgeyle ilgili alanların listesi görüntülenir. İletişim kutusunda, eklenecek bir veya daha fazla alan seçin ve ardından **Ekle**'yi seçin. Önceden eklediğiniz bir alanı kaldırmak için bu işlemi yineleyin ancak iletişim kutusundaki alan seçimini temizleyin.
    - Microsoft PowerApps kullanarak oluşturulmuş bir uygulamayı sayfaya katıştırmak için, **Ekle** altındaki **PowerApp** aracını seçin. Sayfaya bir PowerApps uygulamasının nasıl katıştırılacağı hakkında ayrıntılı bilgi için bkz: [PowerApps katıştırma](embed-power-apps.md).

- Geçerli sayfaya ilişkin tüm kişiselleştirmelerle ilgili yönetim seçeneklerinin bir listesini görüntülemek için **Yönet** düğmesini seçin.
    - Sayfayı varsayılan, ilk yüklendiği durumuna sıfırlamak için **Temizle**'yi seçin. Geçerli sayfadaki tüm kişiselleştirmeler temizlenir. Geri alma eylemi yoktur. Bu nedenle, bu seçeneği ancak sayfa sıfırlamak istediğinizden emin olduğunuzda kullanın.
    - Sizin veya başka birinin sayfa için daha önce oluşturduğu bir dosyadan kişiselleştirme yüklemek için **İçe aktar**'ı seçin. Sayfadaki tüm geçerli kişiselleştirmeleriniz, seçilen dosyadan alınan kişiselleştirmelerle değiştirilir.
    - Sayfadaki kişiselleştirmelerinizi bir dosyaya kaydetmek için **Dışa aktar**'ı seçin. Kişiselleştirmelerinizi başka kullanıcılarla paylaşabilirsiniz. Bu kullanıcıların, sayfaya ilişkin kişiselleştirmelerinizi içeren dosyayı içe aktarmaları gerekir.

- **Kişiselleştirme** araç çubuğunu kapatmak ve sayfayı önceki etkileşimli durumuna döndürmek için **Kapat** düğmesini seçin.

**Kişiselleştirme** araç çubuğu kullanılırken kaydedilen işlemler dolaylıdır. Kişiselleştirmeleriniz siz yapar yapmaz yürürlüğe girer ve bir **Kaydet** düğmesi seçmeniz gerekmez. Bazı durumlarda, bir araç seçtiğiniz zaman öğenin yanında bir asma kilit simgesi görünür. Bu simge, seçilen araçla ilgili öğe özelliklerini değiştiremeyeceğiniz çünkü bu özelliklerde yapılan değişikliklerin sayfanın doğru işleyişini engelleyeceği anlamına gelir.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Çalışma alanına kutucuk, liste veya bağlantı ekleme
Listeler içeren bazı sayfalar için ek bir kişiselleştirme özelliği mevcuttur. Eylem Bölmesinin **Seçenekler** sekmesinde **Kişiselleştir** grubundaki **Çalışma alanına ekle** düğmesi, belirli bir çalışma alanındaki geçerli listeden bilgileri göstermenize olanak sağlar. Çalışma alanındaki bilgilerinin filtrelenmiş ve sıralanmış bir görünümünü veya varsayılan görünümü gösterebilirsiniz. Çalışma alanında bilgilerin bir liste veya listedeki öğe sayısını gösterebilen bir özet kutucuk ya da bir bağlantı olarak görüneceğini de belirtebilirsiniz.

[![Çalışma alanına ekle](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Çalışma alanına liste eklerken, çalışma alanında listenin bilgileri istediğiniz gibi göstermesini sağlamak için sayfada listeyi sıralayın veya filtreleyin. Ardından **Çalışma alanına ekle**'yi seçin. Bir çalışma alanı seçin ve ardından **Sunum** alanında **Liste**'yi seçin. **Yapılandır**'ı seçtikten sonra, çalışma alanındaki listede görünmesi gereken sütunları seçebildiğiniz bir iletişim kutusu görünür. Çalışma alanındaki liste için kullanılacak etiketi de belirtebilirsiniz.
- Çalışma alanına kutucuk eklemek için, önce özetlenmesini veya hızlı erişilmesini istediğiniz verileri göstermesi için sayfadaki listeyi filtreleyin. Ardından **Çalışma alanına ekle**'yi seçin. Bir çalışma alanı seçin ve ardından **Sunum** alanında **Kutucuk**'u seçin. **Yapılandır**'ı seçtikten sonra, çalışma alanındaki kutucuk için kullanılacak etiketi belirtebildiğiniz bir iletişim kutusu görünür. Kutucukta bir sayı gösterilip gösterilmeyeceğini de belirtebilirsiniz. Kutucuk çalışma alanına eklendikten sonra kutucuğu seçerek, çalışma alanından geçerli sayfayı açabilir ve kutucukla ilişkili filtrelenmiş listeyi görüntüleyebilirsiniz.
- Bir çalışma alanına bağlantı eklemek için, önce sayfadaki listeyi filtreleyerek, ilgilendiğiniz verileri göstermesini sağlayın. Ardından **Çalışma alanına ekle**'yi seçin. Bir çalışma alanı seçin ve ardından **Sunum** alanında **Bağlantı**'yı seçin. **Yapılandır**'ı seçtikten sonra, bağlantı için kullanılacak etiketi belirtebildiğiniz bir iletişim kutusu görünür. İsteğe bağlı olarak, bu bağlantıyı içerecek yeni bir bölüm için etiket de belirtebilirsiniz.

Liste, kutucuk veya bağlantınız bir çalışma alanına eklendikten sonra o çalışma alanı açıp, öğeleri istediğiniz gibi yeniden sıralayabilirsiniz.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Çalışma alanından panoya özet ekleme
Bazı çalışma alanları sayı kutucukları (yani üzerinde sayılar bulunan kutucuklar) içerir ve bu kutucukların panonuzda da görünmesini isteyebilirsiniz. Bir çalışma alanında, sayı kutucuğuna sağ tıklayın ve **Kişiselleştir**'i seçin. Bunun ardından, kutucuğun özellik penceresinde **Panoya sabitle**'yi seçin. Seçilen panoyu bir dahaki açışınızda (ve yenilemenizde) sayı o çalışma alanının gezinti kutucuğunun altında görünür. Bu sayıyı doğrudan seçerek, temsil ettiği verilere doğrudan gidebilirsiniz.

### <a name="personalizing-your-dashboard"></a>Panonuzu kişiselleştirme
Pano, genellikle, Finance and Operations'ı açtığınızda göreceğiniz ilk sayfadır. Panoyu kişiselleştirerek yalnızca görmek istediğiniz çalışma alanı kutucuklarını göstermesini sağlayabilirsiniz. Ayrıca, kutucukları görmeyi tercih ettiğiniz sırayla yeniden düzenleyebilir, çalışma alanı gezinti kutucuklarını yeniden adlandırabilir ve tamamen yeni bir çalışma alanı kutucuğu ekleyebilirsiniz.

Panoyu kişiselleştirmek için herhangi bir kutucuğa sağ tıklayın ve **Kişiselleştir**'i seçerek kutucuğun özellik penceresini açın.

- Seçilen kutucuğu gizlemek veya yeniden adlandırmak isterseniz, değişikliği özellik penceresinde doğrudan yapabilirsiniz.
- Çalışma alanı kutucuklarını yeniden sıralamak istiyorsanız, özellik penceresinde **Bu formu kişiselleştir**'i seçerek **Kişiselleştirme** araç çubuğunu açın. Bunun ardından, **Taşı** aracını kullanarak kutucukları istediğiniz gibi düzenleyebilirsiniz.
- Yeni bir çalışma alanı kutucuğu oluşturmak için, özellik penceresinde **Çalışma alanı ekle**'yi seçin. Panonun alt kısmında yeni bir çalışma alanı kutucuğu oluşturulur. Bu yeni çalışma alanı kutucuğunu istediğiniz gibi yeniden adlandırabilirsiniz. Bu konunun [Çalışma alanlarına liste, kutucuk veya bağlantı ekleme](personalize-user-experience.md#adding-a-tile-list-or-link-to-a-workspace) bölümünde açıklandığı gibi, çalışma alanına listeler, kutucuklar ve bağlantılar da ekleyebilirsiniz.

## <a name="administration-of-personalization"></a>Kişiselleştirme yönetimi
Bir sayfayı kişiselleştirdikten sonra, kişiselleştirilmiş sayfayı dışa aktararak kişiselleştirmelerinizi diğer kullanıcılarla paylaşabilirsiniz. Daha sonra diğer kullanıcıların kişiselleştirilmiş sayfayı açmalarını ve oluşturduğunuz kişiselleştirme dosyasını içe aktarmalarını isteyebilirsiniz. Alternatif olarak, kişiselleştirmenizi, yönetici ayrıcalıklarına sahip bir kullanıcıya verebilirsiniz. Kullanıcı, bunun ardından, kişiselleştirme dosyanızı aynı anda çok sayıda kullanıcıya uygulayabilir.

Yönetici ayrıcalıklarına sahip kullanıcılar, bu kişi **Kişiselleştirme** sayfasında diğer kullanıcılara ait kişiselleştirmeleri de yönetebilir. Bu sayfada dört sekme vardır:

- **Uygula** – Bir veya birden fazla kullanıcı için bir kişiselleştirmeyi içe aktarabilir veya seçebilirsiniz. Bir kişiselleştirmeyi bir veya daha fazla kullanıcıya uygulamak için önce bir rol ve o role sahip kullanıcıları seçin. Daha sonra, ya seçilen kullanıcılara uygulamak üzere mevcut bir kişiselleştirmeyi seçin veya bir kişiselleştirme dosyasını içe aktarın. Kişiselleştirme doğrulanır ve seçilen tüm kullanıcılara, seçili sayfayı bir dahaki açışlarında uygulanır.
- **Temizle** – Bir sayfanın veya çalışma alanının tüm kişiselleştirmelerini bir veya birden fazla kullanıcı için temizleyebilirsiniz. Önce bir sayfayı veya çalışma alanını özelleştiren kullanıcıların listesini görmek için o sayfayı veya çalışma alanını seçin. Ardından, o sayfa veya çalışma alanı için kişiselleştirmelere sahip olması gereken kullanıcıları seçin ve **Temizle**'yi seçin. Seçili kullanıcıların seçili sayfaya veya çalışma alanına uyguladığı tüm kişiselleştirmeler silinir. Bu eylem geri alınamaz. Ancak, sayfa veya çalışma alanı için kaydedilmiş bir kişiselleştirme varsa, kişiselleştirme yeniden içe aktarılabilir.
- **Kullanıcı başına yönetici** – Bir kullanıcı seçerek, kişiselleştirdiği sayfaların listesini görün. Bunun ardından, seçili kullanıcıların belirli sayfalar veya tüm sistem için kişiselleştirme kullanma yeteneklerini etkinleştirebilir veya devre dışı bırakabilirsiniz. Ayrıca, seçilen kullanıcı için bir kişiselleştirmeyi içe veya dışa aktarabilir ya da temizleyebilirsiniz.
- **Sistem:** Tüm kullanıcılar için tüm kişiselleştirmeleri geçici olarak devre dışı bırakabilirsiniz. Bu durumda, kişiselleştirmeler silinir. Tüm sayfalar hemen tüm kullanıcılar için varsayılan durumlarına sıfırlanır. Kişiselleştirmeyi daha sonra yeniden etkinleştirirseniz, tüm kişiselleştirmeler yeniden uygulanır. Ayrıca sistemdeki tüm kullanıcılar için tüm kişiselleştirmeleri kalıcı olarak silebilirsiniz. Silinmiş kişiselleştirmeler kurtarılamaz. Bu nedenle, bu görevi uygulamadan önce, daha sonra içeri aktarmak isteyebileceğiniz kişiselleştirmeleri dışa aktardığınızdan emin olun.

## <a name="personalization-of-inventory-dimensions"></a>Stok boyutlarının kişiselleştirilmesi

Bir sayfadaki stok boyutlarının ayarlamasını kişiselleştirirseniz, **Görüntü boyutları** seçeneği kullanılarak oluşturulan ayarları dikkate alın. Örneğin, Toplu iş numarası stok boyutu için bir sütunu gizlemek amacıyla kişiselleştirme kullanıyorsunuz ancak sayfa bir daha açıldığında sütun görünüyor. Bu davranış, gösterilen stok boyutu sütunlarını **Boyutların görünümü** ayarlarının kontrol etmesinden kaynaklanır.

**Boyutların görünümü** ayarları tüm sayfalar için geçerlidir ve stok boyutu alanlarının ayrı sayfalardaki kişiselleştirme ayarlarını geçersiz kılar.

Bunun sonucunda, önceki örnekteki Toplu iş numarası stok boyutu için sütunun istemiyorsanız, o boyutu, tablonun **Boyutların görünümü** seçeneğinin bir parçası olarak temizlemeniz gerekir. Sonuç olarak, bu değişiklik yalnızca belirli bir sayfaya değil, tüm sayfalara uygulanır.

