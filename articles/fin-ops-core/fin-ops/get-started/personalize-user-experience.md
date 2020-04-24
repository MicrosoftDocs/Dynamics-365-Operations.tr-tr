---
title: Kullanıcı deneyimini kişiselleştirme
description: Bu konuda uygulamayı nasıl kişiselleştirebileceğiniz açıklanmaktadır.
author: jasongre
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0a995d25cfc5e78cc76dd73ddea2fb8bd904328
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2020
ms.locfileid: "3260518"
---
# <a name="personalize-the-user-experience"></a>Kullanıcı deneyimini kişiselleştirme

[!include [banner](../includes/banner.md)]

Bu konuda uygulamayı nasıl kişiselleştirebileceğiniz açıklanmaktadır.

Üç temel kişiselleştirme sınıfı bulunmaktadır.

- Bir kurulum sayfasında yapılan kişiselleştirmeler. Örneğin renk teması ve saat dilimi.
- Sayfa kullanımıyla ilgili kişiselleştirmeler. Bu kişiselleştirmeler *örtülü* kişiselleştirmeler olarak bilinir. Örneğin sistem, ayarladığınız takdirde ızgara sütunlarının genişliğini ve Hızlı Sekmelerin genişletme/daraltma durumunu izler.
- Bir kullanıcının bir öğenin bir sayfadaki görünüşünü veya davranışını değiştirerek sayfanın görünümünde genellikle etkileşimli bir kişiselleştirme moduyla uyguladığı kişiselleştirmeler. Bu kişiselleştirmeler *açık* kişiselleştirmeler olarak bilinir. Örneğin, kullanıcı sayfadaki öğeleri eklemiş, gizlemiş veya yeniden düzenlemiş olabilir.

Kullanıcının yaptığı her kişiselleştirme, ilgili kişiselleştirmenin türünden veya kullanıcının etkileşimde olduğu şirketten bağımsız olarak yalnızca o kullanıcıya aittir. Bir kullanıcının sayfada yaptığı değişiklikler sistemdeki diğer kullanıcıları etkilemez.

## <a name="system-wide-options-for-the-current-user"></a>Geçerli kullanıcının sistem çapında seçenekleri

**Kullanıcı seçenekleri** sayfası, geçerli kullanıcı için sistem genelinde çeşitli ayarlar içerir. **Kullanıcı seçenekleri** sayfasını açmak için gezinti çubuğundaki **Ayarlar** düğmesini (çark simgesi) ve ardından **Kullanıcı seçenekleri**'ni seçin. **Kullanıcı seçenekleri** sayfasında çeşitli kullanıcı ayarlarını içeren dört sekme vardır:

- **Görsel** – Bir renk teması ve sayfalardaki öğelerin varsayılan boyutunu seçin.
- **Tercihler** – Sistemi her açtığınızda kullanılacak varsayılan değerleri seçin. Bu değerler şirket, ilk sayfa ve varsayılan görüntüleme/düzenleme modunu içerir. (Görüntüleme/düzenleme modu, sayfayı her açışınızda, görüntülemeye karşı kilitli olup olmadığını veya düzenlemeye açık olup olmadığını belirler.) Bu sekmede dil, saat dilimi, tarih, saat ve sayı biçimi için seçenekler de vardır. Son olarak, bu sekme sürümden sürüme değişiklik gösteren çeşitli tercihler içerir.
- **Hesap** – Kullanıcı adınızı ve hesapla ilgili diğer seçenekleri ayarlayın.
- **İş akışı** – İş akışıyla ilgili seçenekleri belirleyin.

Kullanıcı ayarlarınızı değiştirmenin yanı sıra, kullanım verilerinizi ve kişiselleştirmelerinizi görüntülemek ve silmek için **Kullanıcı seçenekleri** sayfasını kullanabilirsiniz. Yalnızca Eylem bölmesindeki **Kullanım verileri**'ni seçin.

Uygulamayı kullandığınızda, seçimlerinizin pek çoğu sistemi gelecekte kullanmanızı kolaylaştırmak için depolanır. **Kişiselleştirme** sekmesi sistemdeki sayfalarda yaptığınız kişisel değişiklikleri görüntülemenize ve yönetmenize olanak sağlar. Bu sekmede ayrıca özellik açıklamalarını da (yeni sistem özellikleri sunan açılır pencereleri) sıfırlayabilirsiniz. Daha sonra, daha önce karşılaşılan özelliklerle ilgili uyarı alırsınız.

> [!NOTE]
> [Kaydedilmiş görünümler](saved-views.md) özelliği açıksa, **Kullanıcı seçenekleri** sayfasında Eylem bölmesinde **Kişiselleştirme**'yi seçerek kişiselleştirmeleri görüntüleyebilir ve yönetebilirsiniz.

## <a name="implicit-personalizations"></a>Dolaylı kişiselleştirmeler

Örtülü kişiselleştirmeler, mevcut görünür durumlarını depolayab denetimlerle etkileşime girerek yaptığınız kişiselleştirmelerdir.

- **Izgara sütun genişlikleri** – Izgaradaki bir sütunun genişliğini, sütun başlığının solundaki veya sağındaki boyutlandırma çubuğunu seçerek ve bunu sütun istediğiniz genişliğe gelene kadar sola veya sağa kaydırarak ayarlayabilirsiniz. Uygulama, sütun için ayarladığınız genişlik bilgisini depolar. Daha sonra, o ızgarayı içeren sayfayı tekrar açtığınızda sütunu o genişliğe ayarlanır.
- **Kılavuz sütun toplamları** -(yalnızca yeni kılavuz kontrolü etkin olarak mevcuttur) kılavuzda bir sayısal sütunun altında bir toplam gösterilip gösterilmeyeceğini ve kılavuz altbilginin görünür olup olmadığını belirleyebilirsiniz. Uygulama bu verileri depolar; böylece sayfayı bir sonraki açışınızda bu tercihlerin hatırlanır olmasını sağlayabilirsiniz. Daha fazla bilgi için [kılavuz yetenekleri](grid-capabilities.md) konusuna bakın. 
- **Hızlı Sekmeler** – Bazı sayfaların *Hızlı Sekmeler* olarak bilinen genişletilebilir bölümleri vardır. Uygulama, genişlettiğiniz veya daralttığınız Hızlı Sekmeler hakkındaki bilgileri depolar. Bunun ardından, sayfayı sonraki açışınızda o hızlı sekmeler, sayfayla son etkileşiminize göre genişletilir veya daraltılır. Bazı durumlarda, uygulamanın bir hızlı sekme genişletilene kadar o hızlı sekmeye ilişkin bilgilere ulaşmasına gerek olmadığından, hızlı sekmeyi daraltarak sistem performansının artırılmasına yardımcı olabilirsiniz. Bu konuda daha ileride açıklanacağı gibi, bir sayfadaki hızlı sekmelerin sırasını da değiştirebilirsiniz.
- **Bilgi Kutuları** – Bazı sayfalarda, sayfanın geçerli konusuyla ilgili salt okunur bilgileri gösteren **İlgili bilgi** bölmesi bulunur. **İlgili bilgi** bölmesindeki her bölüm *Bilgi Kutusu* olarak adlandırılır. **İlgili bilgi** bölmesini genişletebilir veya daraltabilir ve ayrıca, Bilgi Kutularını tek tek genişletebilir veya daraltabilirsiniz. Uygulama, bu tercihleri depolar. Daha sonra sayfaya bir sonraki açışınızda sayfayla son etkileşiminize göre, **İlgili bilgi** bölmesi ve tek tek Bilgi Kutuları genişletilir veya daraltılır. Bazı durumlarda, uygulamanın bir Bilgi Kutusu genişletilene kadar o Bilgi Kutusuna ilişkin bilgilere ulaşmasına gerek olmadığından, bilgi kutusunu daraltarak sistem performansının artırılmasına yardımcı olabilirsiniz.
- **Eylem Bölmeleri** – Bir *Eylem Bölmesi* çoğu sayfanın en üst kısmında görünür. Eylem Bölmesi, geçerli sayfada gerçekleştirebildiğiniz eylemlerin birçoğu için düğmeler içerir. Bu düğmeler genellikle sekmeler halinde düzenlenir. Eylem Bölmesini açık haliyle "sabitleyebilir" veya varsayılan olarak daraltabilirsiniz. Bunun ardından, sayfayı sonraki açışınızda Eylem bölmesi sayfayla son etkileşiminize göre açık veya daraltılmış olur. Eylem bölmesini açık olarak sabitlediğiniz takdirde, kullandığınız son sekme gösterilir.
- **Hızlı Filtreler** – Bir *Hızlı Filtre* birçok kılavuzun üst kısmında görünür. Hızlı Filtre, seçtiğiniz bir sütuna göre ızgarayı filtrelemenize olanak sağlar. Uygulama, filtre uyguladığınız sütunu depolar. Daha sonra, o ızgarayı içeren sayfayı sonraki açışınızda ızgara aynı sütunda filtrelenir. Bununla birlikte, kılavuzu filtrelemek için farklı bir sütun seçebilirsiniz.
- **Sütun başlığı filtreleri** – Bir ızgarayı *Sütun başlığı filtrelerini* kullanarak filtrelediğiniz zaman, istediğiniz verileri bulmak için gereksinim duyduğunuzda filtre işlecini değiştirebilirsiniz. Örneğin **ile başlayan** işlecini değiştirip **tam olarak** yapabilirsiniz. Her sütun başlığı filtresi kullandığınız ve filtre işlecini değiştirdiğinizde uygulama bu değişikliği depolar. ARdından, bu sütunu daha sonraki filtreleyişinizde, filtre işleci geri yüklenir.
- **Gezinti bölmesi** – Sayfanın sol üst köşesindeki *Gezinti bölmesini genişlet* düğmesini seçerek **Gezinti bölmesini** açabilirsiniz. (Bu düğmeye bazen _**Menü** düğmesi_, *hamburger*, *hamburger menüsü* veya *hamburger düğmesi* adı da verilir.) Gezinti bölmesini açık haliyle sabitleyebilir veya varsayılan olarak daraltılmış tutabilirsiniz. Gezinti bölmesini açık olarak sabitlemenizin ardından uygulama, bölmeyi siz daraltana kadar açık tutar.

## <a name="explicit-personalizations"></a>Açık kişiselleştirmeler

Farklı kişi ve şirketler, kendileri için en önemli buldukları ve işlerini yürütme tarzı açısından gerekli bulmadıkları veriler bakımından farklı bakış açılarına sahiptir. Bilgilerinizi sıralama ve bilgilerinizle etkileşime girme tarzını özelleştirebilirsiniz. Bazı bilgilerin gizlenmesi gerektiğini de belirtebilirsiniz. Bu yetenekler kişisel ve üretken bir deneyim için anahtar niteliğindedir ve açık kişiselleştirmelere örnektir. Açık kişiselleştirmeler, bir öğenin veya sayfanın görünüşünü veya davranışını değiştirmek amacıyla açık şekilde gerçekleştirdiğiniz kişiselleştirmelerdir.

### <a name="shortcut-menu-options"></a>Kısayol menüsü seçenekleri

Kısayol menüleri, sizin veya şirketinizin gereksinimlerini daha iyi karşılamak amacıyla bir sayfayı açıkça değiştirmek için birkaç yol sağlar. (Kısayol menüsü *sağ tıklama menüsü* veya *bağlam menüsü* olarak da bilinir.)

Bir sayfada yapılabilecek en tipik ve önemli değişikliklerden bazıları, kısayol menüsündeki seçenekler olarak doğrudan sunulur. Örneğin, Platform güncelleştirmesi 17'den itibaren, isterseniz bir ızgarada sütun eklemek veya gizlemek için bir sütun başlığına sağ tıklayıp **Sütunlar ekle** veya **Bu sütunu gizle**'yi seçmeniz yeterlidir.

Ayrıca, açık kişiselleştirmenin en temel türleri de bir öğeye sağ tıklayıp **Kişiselleştir**'i seçerek kullanılabilir. (Sayfanızdaki tüm öğelerin kişiselleştirilemeyeceğini unutmayın.) Bu kişiselleştirme yöntemini kullandığınızda, öğenin özellik penceresi görünür.

![Bir öğenin özelliklerini kişiselleştirme](./media/cli-element-property-window.png)

Bir öğeyi aşağıdaki yöntemlerle kişiselleştirmek için özellik penceresini kullanabilirsiniz:

- Öğenin etiketini değiştirmek.
- Öğeyi gizleyerek sayfada gösterilmemesini sağlamak. Alandaki veriler silinmez veya değiştirilmez. Bilgiler artık sayfada görünmez hale gelir.
- Hızlı sekme özet bölümüne bilgi eklemek (öğe, hızlı sekmedeyse).
- Alanı atlayın, böylece sayfa boyunca sekme üzerinde geçiş yaptığınızda odağı hiçbir zaman alamaz.
- Alandaki verilerin düzenlenmesini önleme (herhangi bir kayıt için).
- Veri girişi için gerekli olacak alanı belirtin. Bu alana değer girilmezse, kırmızı bir kenarlıkla görüntülenir ve bu durumu belirten bir yıldız işareti bulunur. Bu seçenek yalnızca 10.0.11 sürümünden itibaren [Kaydedilen görünümler](saved-views.md) ve **Kişiselleştirme kullanarak alanları gerektiği gibi belirle** özellikleri etkin olduğunda kullanılabilir.

Öğeye bağlı olarak, özellik penceresi başka kişiselleştirme yetenekleri içerebilir. Örneğin, bir kutucuğun özellik penceresi sayesinde o kutucuğu bir panoya yükseltebilir ve bir panonun özellik penceresiyle o panoda yeni bir çalışma alanı oluşturabilirsiniz.

### <a name="the-personalization-toolbar"></a>Kişiselleştirme araç çubuğu

Bir sayfada birden çok değişiklik veya diğer mekanizmalar aracılığıyla gerçekleştirilemeyen değişiklikler yapmak istiyorsanız (öğeleri yeniden düzenleme istediğinizde), **Kişiselleştirme** araç çubuğunu kullanabilirsiniz. **Kişiselleştirme** araç çubuğunu açmak için, aşağıdaki adımlardan birini izleyin:

- Bir öğenin özellik penceresinde **Bu sayfayı kişiselleştir**'i seçin.
- Sayfanın Eylem Panosunda, **Seçenekler** sekmesinde, **Kişiselleştir** grubunda, **Bu formu kişiselleştir**'i seçin.
- Gezinti çubuğundaki **Ayarlar** düğmesini (dişli sembolü) seçin ve sonra **Kişiselleştir**'i seçin.

[![Kişiselleştirme araç çubuğu](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Sayfada gezinme

**Kişiselleştirme** araç çubuğu açıkken, temel sayfa salt okunurdur (başka bir deyişle, verileri düzenleyemezsiniz), ancak hala etkileşimlidir. Özellikle bu eylemleri sayfada gerçekleştirirken olduğu gibi, **İlgili bilgi** bölmesini genişletebilir veya daraltabilir, sekmeler arasında geçiş yapabilir ve bölümleri genişletebilir veya daraltabilirsiniz. Daraltılabilir bir bölüm veya bir sekmede bir kişiselleştirme yapmak için (örneğin bir hızlı sekmeyi gizlemek için) klavye odağında olduğunda veya üzerinde durduğunuzda bölüm veya sekmenin yanında görüntülenen düğmeyi seçmeniz gerekir.

#### <a name="personalization-tools"></a>Kişiselleştirme araçları

**Kişiselleştirme** araç çubuğunda aşağıdaki araçlar mevcuttur:

- Bir öğeyi seçip özelliklerini değiştirmek için **Seç** aracını kullanın. Bu aracı kullanmak için, araç çubuğunda **Seç** düğmesini seçin ve sonra istediğiniz öğeyi seçin. Öğenin özellik penceresi görünür ve o öğenin özelliklerini değiştirebilirsiniz. Sayfada kişiselleştirilebilecek başka öğeler için işlemi yineleyebilirsiniz. Bazı senaryolarda bazı kişiselleştirme özelliklerinin kullanılabilir olmayacağını unutmayın. Örneğin, gerekli bir alanı kilitleyemezsiniz.
- Sayfadaki bir öğeyi gizlemek için **Gizle** aracını kullanın. Bu aracı kullanmak için, araç çubuğunda **Gizle** düğmesini seçin ve sonra gizlenecek öğeyi seçin. **Gizle** aracını kullandığınız zaman, gizli durumdaki tüm öğeler görünür hale gelir ancak gölgeli bir kapsayıcıda gösterilir. Böylece, öğeyi seçerek görünür yapabilirsiniz. Öğeler gizli olduğunda sayfanın nasıl görüneceğini görmek için, başka bir kişiselleştirme aracına geçin.
- Sayfanıza bir alan eklemek için **Alan ekle** aracını kullanın. Bu aracı kullandığınızda, yalnızca sayfa tanımının bir parçası olan alanlar ekleyebilirsiniz. Geçerli sayfa tanımının bir parçası olmayan yeni alanların nasıl oluşturulacağı hakkında bilgi için bkz. [Özel alanlar oluşturma ve bunlarla çalışma](user-defined-fields.md). Araç çubuğunda **Alan ekle** düğmesini seçtikten sonra, ilk olarak, alan eklemek istediğiniz grubu veya bölgeyi seçmeniz gerekir. Bir iletişim kutusunda, seçilen grupla veya bölgeyle ilgili alanların listesi görüntülenir. İletişim kutusunda, eklenecek bir veya daha fazla alan seçin ve ardından **Ekle**'yi seçin. Önceden eklediğiniz bir alanı kaldırmak için bu işlemi yineleyin ancak iletişim kutusundaki alan seçimini temizleyin.
- Bir öğeyi mevcut öğeler grubu içinde farklı bir konuma taşımak için **Taşı** aracını kullanın. Bir öğeyi üst grubunun dışına taşıyamazsınız. Bu aracı kullanmak için, araç çubuğunda **Taşı** düğmesini seçin ve sonra taşınacak öğeyi seçin. Bir öğeyi seçtiğinizde uygulama öğenin taşınabileceği konumları belirler. Bu konumlara *bırakma alanları* denir. Öğeyi mevcut grup içinde sürükledikçe, her bırakma bölgesi, öğenin bırakılabileceği alanın yanında renkli ve kalın bir çizgi olarak gösterilir.
- Sayfanın klavye sekmesi sırasından bir öğeyi kaldırmak için **Atla** aracını kullanın. Araç çubuğunda **Atla** düğmesini seçtiğiniz zaman, atlanmış durumdaki tüm öğeler gölgeli bir kapsayıcıda gösterilir. Etkileşimli olarak sekme sırasına alan ekleme veya kaldırma yapabilirsiniz.
- Bir öğenin hızlı sekme özet bölümünde görünmesini isterseniz **Başlıkta göster** aracını kullanın. Araç çubuğunda **Başlıkta göster** düğmesini seçtiğiniz zaman, özet alanı olarak seçilen tüm alanlar gölgeli bir kapsayıcıda gösterilir. Hızlı sekme özetine etkileşimli olarak alan ekleyebilir veyaalanları seçerek kaldırabilirsiniz.
- Veri girişi için bir öğeyi gerekli olarak belirlemek üzere **Gerekli** aracını kullanın. Araç çubuğunda **Gerekli** düğmesini seçtiğiniz zaman, gerekli olacak kişiselleştirilmiş tüm öğeler gölgeli bir kapsayıcıda gösterilir. Bu durumda bu öğeleri yeniden gerekli değil durumuna getirebilirsiniz. Bu seçenek yalnızca [Kaydedilen görünümler](saved-views.md) ve **Kişiselleştirme kullanarak alanları gerektiği gibi belirle** özellikleri etkinken bir özellik sürümünde kullanılabilir.
- Bir öğeyi düzenlenebilir veya düzenlenemez olarak işaretlemek için **Kilitle** aracını kullanın. Araç çubuğunda **Kilitle** düğmesini seçtiğiniz zaman, düzenlenemez durumdaki tüm öğeler gölgeli bir kapsayıcıda gösterilir. Bu durumda bu öğeleri yeniden düzenlenebilir hale getirebilirsiniz. Bazı alanların gerekli olduğunu ve düzenlenemez yapılamayacağını unutmayın. Bu alanların yanında bir asma kilit simgesi görünür.
- Microsoft Power Apps kullanarak oluşturulmuş bir uygulamayı sayfaya katıştırmak için, **Power Apps'ten uygulama ekle** düğmesini kullanın. Power Apps uygulamasını bir sayfaya katıştırma hakkında ayrıntılı bilgi için bkz. [Power Apps uygulamalarını katıştırma](embed-power-apps.md). Bu seçenek yalnızca [Kaydedilmiş görünümler](saved-views.md) özelliği devre dışı bırakılınca kullanılabilir.  
- Microsoft Power Apps veya üçüncü taraf kullanarak oluşturulmuş bir uygulamayı sayfaya katıştırmak için, **uygulama ekle** düğmesini kullanın. Bu seçenek yalnızca [kaydedilmiş görünümler](saved-views.md) özelliği etkin olduğunda kullanılabilir. 
- Sayfayı varsayılan, ilk yüklendiği durumuna sıfırlamak için **Temizle** aracını kullanın. Geçerli sayfadaki tüm kişiselleştirmeler temizlenir. Geri alma eylemi yoktur. Bu nedenle, bu aracı ancak sayfa sıfırlamak istediğinizden emin olduğunuzda kullanın.
- Sizin veya başka birinin daha önce oluşturduğu bir dosyadan kişiselleştirme yüklemek için **İçe aktar** aracını kullanın. Bir sayfa için kişiselleştirmeleri içe aktardığınızda, sayfa için var olan tüm kişiselleştirmelere eklenip eklenmeyeceğini veya bunların yerini alıp almayacaklarını seçebilirsiniz. Geri alma eylemi yoktur. Bu nedenle, kişiselleştirmeleri içe aktardıktan sonra, istemediğiniz değişiklikleri el ile temizlemeniz veya geri almanız gerekir.
- Sayfadaki kişiselleştirmelerinizi bir dosyaya kaydetmek için **Dışa aktar** aracını kullanın. Böylece kişiselleştirmelerinizi başka kullanıcılarla paylaşabilirsiniz. Bu kullanıcıların, sayfaya ilişkin kişiselleştirmelerinizi içeren dosyayı içe aktarmaları gerekir.
- **Kişiselleştirme** araç çubuğunu kapatmak ve sayfayı önceki etkileşimli durumuna döndürmek için **Kapat** düğmesini seçin.

Geleneksel olarak, **Kişiselleştirme** araç çubuğu kullanıldığında, kişiselleştirmeleri yaptığınız anda etkin olur. Ancak, [Kaydedilmiş görünümler](saved-views.md) özelliği açıksa, kişiselleştirmeleri özel olarak seçtiğiniz bir görünüme kaydetmeniz gerekir.

Bazı durumlarda, bir araç seçtiğiniz zaman öğenin yanında bir asma kilit simgesi görünür. Bu simge, seçilen araçla ilgili öğe özelliklerini değiştiremeyeceğiniz çünkü bu özelliklerde yapılan değişikliklerin sayfanın doğru işleyişini engelleyeceği anlamına gelir.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Çalışma alanına kutucuk, liste veya bağlantı ekleme

Listeler içeren bazı sayfalarda, **Çalışma alanına ekle** kişiselleştirme özelliği, Eylem bölmesinin **Seçenekler** sekmesindeki **Kişiselleştir** grubunda yer alır. Bu özellik, ilgili bilgileri geçerli listeden belirli bir çalışma alanına itmenizi sağlar. Çalışma alanında görünen bilgiler tüm listeyi veya listenin filtrelenmiş ve sıralanmış bir sürümünü temel alabilir. Çalışma alanında bilgilerin bir liste veya listedeki öğe sayısını gösterebilen bir özet kutucuk ya da bir bağlantı olarak görüneceğini de belirtebilirsiniz.

> [!NOTE]
> [Kaydedilmiş görünümler](saved-views.md) özelliği açıksa bir çalışma alanına ittiğiniz içerik doğrudan bir görünüme bağlıdır. Görünümün sorgusu, çalışma alanındaki verileri getirmek için kullanılır ve çalışma alanındaki ilgili döşeme veya bağlantı sayfayı bu görünüme açar; böylece görünümün sorgu ve kişiselleştirmeleri buna uygulanır.

[![Çalışma alanına ekle](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Çalışma alanına liste eklerken, çalışma alanında listenin bilgileri istediğiniz gibi göstermesini sağlamak için sayfada listeyi sıralayın veya filtreleyin. (Kaydedilmiş görünümler özelliği açıksa, bu koşullara sahip bir görünümü kaydedene kadar devam edemezsiniz). Sonra **Çalışma alanına ekle**'yi seçin. Bir çalışma alanı seçin ve ardından **Sunum** alanında **Liste**'yi seçin. **Yapılandır**'ı seçtikten sonra, çalışma alanındaki listede görünmesi gereken sütunları seçebildiğiniz bir iletişim kutusu görünür. Çalışma alanındaki liste için kullanılan etiketi de belirtebilirsiniz.
- Çalışma alanına kutucuk eklemek için, önce özetlenmesi gereken veya hızlı erişilmesini istediğiniz verileri göstermesi için sayfadaki listeyi filtreleyin. (Kaydedilmiş görünümler özelliği açıksa, bu koşullara sahip bir görünümü kaydedene kadar devam edemezsiniz). Sonra **Çalışma alanına ekle**'yi seçin. Bir çalışma alanı seçin ve ardından **Sunum** alanında **Kutucuk**'u seçin. **Yapılandır**'ı seçtikten sonra, çalışma alanındaki kutucuk için kullanılması gereken etiketi belirtebildiğiniz bir iletişim kutusu görünür. Kutucukta bir sayı gösterilip gösterilmeyeceğini de belirtebilirsiniz. Kutucuk çalışma alanına eklendikten sonra, geçerli sayfayı çalışma alanından açmak için onu seçebilirsiniz. Böylece,kutucukla ilişkili filtre uygulanmış listeyi görüntüleyebilirsiniz.
- Bir çalışma alanına bağlantı eklemek için, önce sayfadaki listeyi filtreleyerek, ilgilendiğiniz verileri göstermesini sağlayın. (Kaydedilmiş görünümler özelliği açıksa, bu koşullara sahip bir görünümü kaydedene kadar devam edemezsiniz). Sonra **Çalışma alanına ekle**'yi seçin. Bir çalışma alanı seçin ve ardından **Sunum** alanında **Bağlantı**'yı seçin. **Yapılandır**'ı seçtikten sonra, bağlantı için kullanılması gereken etiketi belirtebildiğiniz bir iletişim kutusu görünür. İsteğe bağlı olarak, bu bağlantıyı içeren yeni bir bölüm için etiket de belirtebilirsiniz.

Liste, kutucuk veya bağlantıyı bir çalışma alanına ekledikten sonra o çalışma alanı açıp, öğeleri istediğiniz gibi yeniden düzenleyebilirsiniz.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Çalışma alanından panoya özet ekleme

Bazı çalışma alanları sayı kutucukları (yani üzerinde sayılar bulunan kutucuklar) içerir ve bu kutucukların panonuzda da görünmesini isteyebilirsiniz. Çalışma alanında bir sayı kutucuğuna sağ tıklayın, **Kişiselleştir**'i ve ardından kutucuğun özellik penceresinde **Panoya sabitle**'yi seçin. Ardından, seçilen panoyu bir dahaki açışınızda (ve yenilemenizde) sayı o çalışma alanının gezinti kutucuğunun altında görünür. Bu sayıyı doğrudan seçerek, temsil ettiği verilere doğrudan gidebilirsiniz.

### <a name="personalizing-your-dashboard"></a>Panonuzu kişiselleştirme

Pano, çoğunlukla uygulamayı açtığınızda gördüğünüz ilk sayfadır. Panoyu kişiselleştirerek yalnızca görmek istediğiniz çalışma alanı kutucuklarını göstermesini sağlayabilirsiniz. Ayrıca, kutucukları görmeyi tercih ettiğiniz sırayla yeniden düzenleyebilir, çalışma alanı gezinti kutucuklarını yeniden adlandırabilir ve yeni bir çalışma alanı kutucuğu ekleyebilirsiniz.

Panoyu kişiselleştirmek için herhangi bir kutucuğa sağ tıklayın ve **Kişiselleştir**'i seçerek kutucuğun özellik penceresini açın.

- Seçilen kutucuğu gizlemek veya yeniden adlandırmak isterseniz, değişikliği özellik penceresinde doğrudan yapabilirsiniz.
- Çalışma alanı kutucuklarını yeniden sıralamak istiyorsanız, özellik penceresinde **Bu sayfayı kişiselleştir**'i seçerek **Kişiselleştirme** araç çubuğunu açın. Bunun ardından, **Taşı** aracını kullanarak kutucukları istediğiniz gibi yeniden düzenleyebilirsiniz.
- Yeni bir çalışma alanı kutucuğu eklemek için, özellik penceresinde **Çalışma alanı ekle**'yi seçin. Panonun alt kısmında yeni bir çalışma alanı kutucuğu oluşturulur. Bu yeni çalışma alanı kutucuğunu istediğiniz gibi yeniden adlandırabilirsiniz. Bu konunun [Çalışma alanlarına liste, kutucuk veya bağlantı ekleme](#adding-a-tile-list-or-link-to-a-workspace) bölümünde açıklandığı gibi, çalışma alanına listeler, kutucuklar ve bağlantılar da ekleyebilirsiniz.

## <a name="administration-of-personalizations"></a>Kişiselleştirme yönetimi

Bir sayfayı kişiselleştirdikten sonra, kişiselleştirilmiş sayfayı dışa aktararak kişiselleştirmelerinizi diğer kullanıcılarla paylaşabilirsiniz. Daha sonra diğer kullanıcıların kişiselleştirilmiş sayfayı açmalarını ve oluşturduğunuz kişiselleştirme dosyasını içe aktarmalarını isteyebilirsiniz. Alternatif olarak, kişiselleştirmenizi yönetici ayrıcalıklarına sahip bir kullanıcıya verebilirsiniz. Kullanıcı, bunun ardından, kişiselleştirme dosyanızı aynı anda çok sayıda kullanıcıya uygulayabilir.

Yönetici ayrıcalıklarına sahip kullanıcılar, bu kişi **Kişiselleştirme** sayfasında diğer kullanıcılara ait kişiselleştirmeleri de yönetebilir.

[Kaydedilmiş görünümler](saved-views.md) özelliğini etkinleştirmemiş olan müşteriler için bu sayfanın dört sekmesi vardır:

- **Uygula** – Bir veya birden fazla kullanıcı için bir kişiselleştirmeyi içe aktarabilir veya seçebilirsiniz. Bir kişiselleştirmeyi bir veya daha fazla kullanıcıya uygulamak için önce bir rol ve o role sahip kullanıcıları seçin. Daha sonra, ya seçilen kullanıcılara uygulamak üzere mevcut bir kişiselleştirmeyi seçin veya bir kişiselleştirme dosyasını içe aktarın. Kişiselleştirme doğrulanır ve seçilen tüm kullanıcılara, seçili sayfayı bir dahaki açışlarında uygulanır.
- **Temizle** – Bir sayfanın veya çalışma alanının tüm kişiselleştirmelerini bir veya birden fazla kullanıcı için temizleyebilirsiniz. Önce bir sayfayı veya çalışma alanını özelleştiren kullanıcıların listesini görmek için o sayfayı veya çalışma alanını seçin. Ardından, o sayfa veya çalışma alanı için kişiselleştirmelere sahip olması gereken kullanıcıları seçin ve **Temizle**'yi seçin. Seçili kullanıcıların seçili sayfaya veya çalışma alanına uyguladığı tüm kişiselleştirmeler silinir. Bu eylem geri alınamaz. Ancak, sayfa veya çalışma alanı için kaydedilmiş bir kişiselleştirme varsa, kişiselleştirme yeniden içe aktarılabilir.
- **Kullanıcılar** – Bir kullanıcı seçerek, kullanıcının kişiselleştirdiği sayfaların listesini görün. Bunun ardından, seçili kullanıcıların belirli sayfalar veya tüm sistem için kişiselleştirme kullanma yeteneklerini etkinleştirebilir veya devre dışı bırakabilirsiniz. Ayrıca, kullanıcı için bir kişiselleştirmeyi içe veya dışa aktarabilir ya da temizleyebilirsiniz. Ek olarak, kullanıcı için özellik açıklamalarını sıfırlayabilirsiniz. Bu durumda, kullanıcı yeni özellikler içeren açılır pencereleri önceden devre dışı bırakmışsa, bu özellikler kullanıcının bir sonraki karşılaştığı sefer yeniden görünürler.
- **Sistem:** Tüm kullanıcılar için kişiselleştirmeleri geçici olarak devre dışı bırakabilirsiniz. Bu durumda, tüm kullanıcılar için tüm kişiselleştirmeler silinir ve tüm sayfalar varsayılan durumlarına sıfırlanır. Kişiselleştirmeyi daha sonra yeniden etkinleştirirseniz, tüm kişiselleştirmeler yeniden uygulanır. Ayrıca sistemdeki tüm kullanıcılar için tüm kişiselleştirmeleri kalıcı olarak silebilirsiniz. Silinmiş kişiselleştirmeler kurtarılamaz. Bu nedenle, bu görevi uygulamadan önce, daha sonra içeri aktarmak isteyebileceğiniz kişiselleştirmeleri dışa aktardığınızdan emin olun.

[Kaydedilmiş görünümler](saved-views.md) özelliğini etkinleştirmiş olan müşteriler için **Kişiselleştirmeler** sayfasında beş sekme vardır:

- **Yayınlamış görünümler** – Bu görünümler kuruluşunuza yayımlanmıştır. Bu görünümlerin hedeflediği kullanıcıları değiştirmek için, her görünümle ilişkili güvenlik rollerini veya tüzel kişilikleri değiştirebilirsiniz. Ayrıca, bir veya daha fazla yayımlanmış görünümü dışa aktarabilir veya silebilirsiniz.
- **Yayımlanmamış görünümler** – Bu görünümler sisteminize aktarılan ancak henüz yayınlanmamış olan şablon görünümleridir. Bu görünümleri yayımlayabilir, dışa aktarabilir veya silebilirsiniz.
- **Kişisel görünümler** – Bu görünümler sistemdeki kullanıcılar tarafından oluşturulur. Bir kişisel görünümü kuruluşa yayımlayabilir veya bu görünümlerden birini veya birkaçını diğer kullanıcılara kopyalayabilirsiniz. Bu görünümleri gerektiğinde dışa aktarabilir veya silebilirsiniz.
- **Kullanıcılar** – Bir kullanıcı seçerek, kullanıcının kişiselleştirdiği sayfaların listesini görün. Bunun ardından, seçili kullanıcıların belirli sayfalar veya tüm sistem için kişiselleştirme kullanma yeteneklerini etkinleştirebilir veya devre dışı bırakabilirsiniz. Ayrıca, kullanıcı için bir kişiselleştirmeyi içe veya dışa aktarabilir ya da temizleyebilirsiniz. Ek olarak, kullanıcı için özellik açıklamalarını sıfırlayabilirsiniz. Bu durumda, kullanıcı yeni özellikler içeren açılır pencereleri önceden devre dışı bırakmışsa, bu özellikler kullanıcının bir sonraki karşılaştığı sefer yeniden görünürler.
- **Sistem:** Tüm kullanıcılar için kişiselleştirmeleri geçici olarak devre dışı bırakabilirsiniz. Bu durumda, tüm kullanıcılar için tüm kişiselleştirmeler silinir ve tüm sayfalar varsayılan durumlarına sıfırlanır. Kişiselleştirmeyi daha sonra yeniden etkinleştirirseniz, tüm kişiselleştirmeler yeniden uygulanır. Ayrıca sistemdeki tüm kullanıcılar için tüm kişiselleştirmeleri kalıcı olarak silebilirsiniz. Silinmiş kişiselleştirmeler kurtarılamaz. Bu nedenle, bu görevi uygulamadan önce, daha sonra içeri aktarmak isteyebileceğiniz kişiselleştirmeleri dışa aktardığınızdan emin olun.

**Kişiselleştirme** sayfasına erişimi olan kullanıcılar, Eylem bölmesindeki **Görünümleri içe aktar** düğmesini kullanarak kişisel veya şablon görünümlerini de içe aktarabilir.

## <a name="personalizing-inventory-dimensions"></a>Stok boyutlarının kişiselleştirilmesi

Bir sayfadaki stok boyutlarının ayarlamasını kişiselleştirirseniz, **Görüntü boyutları** seçeneği kullanılarak oluşturulan ayarları dikkate alın. Örneğin, Toplu iş numarası stok boyutu için bir sütunu gizlemek amacıyla kişiselleştirme kullanıyorsunuz ancak sayfa bir daha açıldığında sütun görünüyor. Bu davranış, gösterilen stok boyutu sütunlarını **Boyutların görünümü** ayarlarının kontrol etmesinden kaynaklanır. **Boyutların görünümü** ayarları tüm sayfalar için geçerlidir ve stok boyutu alanlarının ayrı sayfalardaki kişiselleştirme ayarlarını geçersiz kılar.

Bu nedenle, önceki örnekteki Toplu iş numarası stok boyutu için sütunun bir sayfada istemiyorsanız o boyutu, tablonun **Boyutların görünümü** seçeneğinin bir parçası olarak sayfadan temizlemeniz gerekir.
