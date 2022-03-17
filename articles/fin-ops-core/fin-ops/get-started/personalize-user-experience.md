---
title: Kullanıcı deneyimini kişiselleştirme
description: Bu konuda uygulamayı nasıl kişiselleştirebileceğiniz açıklanmaktadır.
author: jasongre
ms.date: 03/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4bdce3cd12358112e40a783c73795bd6f35545c8
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384655"
---
# <a name="personalize-the-user-experience"></a>Kullanıcı deneyimini kişiselleştirme

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Bu konu, uygulamayı nasıl kişiselleştirebileceğinizi açıklamakta ve aşağıdaki konuları nasıl ele almaktadır: 

- **Sistem genelindeki seçenekler** – Bu kişiselleştirme seçenekleri bir kurulum sayfasında yapılır ve tüm kullanıcılar tarafından kullanılabilir. Örneğin renk teması ve saat dilimi. 
- **Kısıtlı kişiselleştirme erişimi** – Bu erişim düzeyinde, normal sayfa kullanımıyla ilişkili kullanıcı eylemleri uygulama tarafından otomatik olarak kaydedilir ve sayfayı bir sonraki ziyaretindeki geri yüklenir. Örneğin uygulama, ayarladığınız takdirde kılavuz sütunlarının genişliğini ve hızlı sekmelerin genişletme/daraltma durumunu kaydeder. 
- **Tam kişiselleştirme erişimi** – Bu erişim düzeyinde, kullanıcıların uygulamadaki tüm kişiselleştirme özelliklerine erişimi vardır. Özellikle, **Kişiselleştirme** araç çubuğuna erişebilirler. 
- **Paylaşım kişiselleştirmeleri** – Tam kişiselleştirme erişimi olan kullanıcılar sayfa kişiselleştirmelerini dışa aktarabilir ve bunları diğer kullanıcılarla paylaşabilir.
- **Kişiselleştirmelerin yönetimi** – Ayrıcalıklı kullanıcılar, kuruluş düzeyinde tüm kişiselleştirmeleri yönetmek için **Kişiselleştirme** yönetim sayfasına erişebilirler. 

## <a name="system-wide-options-for-the-current-user"></a>Geçerli kullanıcının sistem çapında seçenekleri

**Kullanıcı seçenekleri** sayfası, geçerli kullanıcı için sistem genelinde çeşitli ayarlar içerir. Bu seçenekler, tüm kullanıcılar tarafından kullanılabilir ve kişiselleştirmeye hiçbir erişim verilmemiş kullanıcılar bile kullanabilir. **Kullanıcı seçenekleri** sayfasını açmak için gezinti çubuğundaki **Ayarlar** düğmesini ve ardından **Kullanıcı seçenekleri**'ni seçin. **Kullanıcı seçenekleri** sayfasında çeşitli kullanıcı ayarlarını içeren dört sekme vardır:

- **Görsel** – Bir renk teması ve sayfalardaki öğelerin varsayılan boyutunu seçin.
- **Tercihler** – Sistemi her açtığınızda kullanılacak varsayılan değerleri seçin. Bu değerler varsayılan şirket, ilk sayfa ve varsayılan görüntüleme/düzenleme modunu içerir. (Görüntüleme/düzenleme modu, sayfayı her açışınızda, görüntülemeye karşı kilitli olup olmadığını veya düzenlemeye açık olup olmadığını belirler.) Bu sekmede dil, saat dilimi, tarih, saat ve sayı biçimi için seçenekler de vardır. Son olarak, bu sekme sürümden sürüme değişiklik gösteren çeşitli tercihler içerir.
- **Hesap** – Kullanıcı adınızı ve hesapla ilgili diğer seçenekleri görüntüleyin veya ayarlayın.
- **İş akışı** – İş akışıyla ilgili seçenekleri belirleyin.

Kullanıcı ayarlarınızı değiştirmenin yanı sıra, kullanım verilerinizi ve kişiselleştirmelerinizi görüntülemek ve silmek için **Kullanıcı seçenekleri** sayfasını kullanabilirsiniz. Kullanım verilerinizi görmek için Eylem Bölmesinde **Kullanım verileri**'ni seçin. **Kişiselleştirme** sekmesi sistemdeki sayfalarda yaptığınız kişisel değişiklikleri görüntülemenize ve yönetmenize olanak sağlar. Bu sekmede ayrıca özellik açıklamalarını da (yeni sistem özellikleri sunan açılır pencereleri) sıfırlayabilirsiniz. Daha sonra, daha önce karşılaşılan özelliklerle ilgili uyarı alırsınız.

> [!NOTE]
> [Kaydedilmiş görünümler](saved-views.md) özelliği açıksa, **Kullanıcı seçenekleri** sayfasında Eylem bölmesinde **Kişiselleştirme**'yi seçerek kişiselleştirmeleri görüntüleyebilir ve yönetebilirsiniz.

## <a name="restricted-personalization-access-formerly-implicit-personalizations"></a>Kısıtlı kişiselleştirme erişimi (daha önce örtülü kişiselleştirmeler)

**Kısıtlı kişiselleştirme erişimi** düzeyinde, normal sayfa kullanımıyla ilişkili kullanıcı eylemleri uygulama tarafından otomatik olarak kaydedilir ve sayfayı bir sonraki ziyaretindeki geri yüklenir. Açık bir kaydetme eylemi gerekmez. 

Tipik sayfa kullanımında yer alan ve kısıtlı kişiselleştirme erişimi kapsamına giren eylemlerin listesi aşağıdadır: 

- **Izgara sütun genişlikleri** – Izgaradaki bir sütunun genişliğini, sütun başlığının solundaki veya sağındaki boyutlandırma çubuğunu seçerek ve bunu sütun istediğiniz genişliğe gelene kadar sola veya sağa kaydırarak ayarlayabilirsiniz. Uygulama, sütun için ayarladığınız genişlik bilgisini depolar. Daha sonra, ilgili sayfayı tekrar açtığınızda sütunu o genişliğe ayarlanır.
- **Kılavuz alt bilgi sütun toplamları** - *(Yalnızca yeni kılavuz kontrolü etkin olduğunda mevcuttur)* Kılavuzda bir sayısal sütunun altında bir toplam gösterilip gösterilmeyeceğini ve kılavuz altbilginin görünür olup olmayacağını belirleyebilirsiniz. Uygulama bu tercihleri depolar ve sayfayı bir sonraki açışınızda hatırlanır olmasını sağlayabilirsiniz. Daha fazla bilgi için [Kılavuz özellikleri](grid-capabilities.md) bölümüne bakın. 
- **Hızlı Sekmeler** – Bazı sayfaların *Hızlı Sekmeler* olarak bilinen genişletilebilir bölümleri vardır. Uygulama, genişlettiğiniz veya daralttığınız hızlı sekmeler hakkındaki bilgileri depolar. Sayfayı sonraki açışınızda o hızlı sekmeler, sayfayla son etkileşiminize göre genişletilir veya daraltılır. Bazı durumlarda, uygulamanın bir hızlı sekme genişletilene kadar o hızlı sekmeye ilişkin bilgilere ulaşmasına gerek olmadığından, hızlı sekmeyi daraltarak sistem performansının artırılmasına yardımcı olabilirsiniz. Bu konuda daha ileride açıklanacağı üzere, bir sayfadaki hızlı sekmelerin sırasını da değiştirebilirsiniz.
- **Bilgi Kutuları** – Bazı sayfalarda, sayfanın geçerli konusuyla ilgili salt okunur bilgileri gösteren **İlgili bilgi** bölmesi bulunur. **İlgili bilgi** bölmesindeki her bölüm *Bilgi Kutusu* olarak adlandırılır. **İlgili bilgi** bölmesini genişletebilir veya daraltabilir ve ayrıca, Bilgi Kutularını tek tek genişletebilir veya daraltabilirsiniz. Uygulama, bu tercihleri depolar. Sayfaya bir sonraki açışınızda sayfayla son etkileşiminize göre, **İlgili bilgi** bölmesi ve tek tek Bilgi Kutuları genişletilir veya daraltılır. Bazı durumlarda, uygulamanın bir Bilgi Kutusu genişletilene kadar o Bilgi Kutusuna ilişkin bilgilere ulaşmasına gerek olmadığından, **İlgili bilgi** Bölmesini veya Bilgi Kutusunu daraltarak sistem performansının artırılmasına yardımcı olabilirsiniz.
- **Eylem Bölmeleri** – Bir *Eylem Bölmesi* çoğu sayfanın en üst kısmında görünür. Eylem Bölmesi, geçerli sayfada gerçekleştirebildiğiniz eylemlerin birçoğu için düğmeler içerir. Bu düğmeler genellikle sekmeler halinde düzenlenir. Eylem Bölmesini açık haliyle *sabitleyebilir* veya varsayılan olarak daraltabilirsiniz. Sayfayı sonraki açışınızda Eylem bölmesi sayfayla son etkileşiminize göre açık veya daraltılmış olur. Eylem bölmesini açık olarak sabitlediğiniz takdirde, kullandığınız son sekme gösterilir.
- **Hızlı Filtreler** – Bir *Hızlı Filtre* birçok kılavuzun üst kısmında görünür. Hızlı Filtre, seçtiğiniz tek bir sütuna göre kılavuza filtrelemenize olanak sağlar. Uygulama, filtre uyguladığınız sütunu depolar. Daha sonra, o sayfayı sonraki açışınızda kılavuz varsayılan olarak filtreleme için aynı sütunu kullanır. Bununla birlikte, kılavuzu filtrelemek için farklı bir sütun da seçebilirsiniz.
- **Sütun başlığı filtreleri** – Bir ızgarayı *Sütun başlığı filtrelerini* kullanarak filtrelediğiniz zaman, istediğiniz verileri bulmak için gereksinim duyduğunuzda filtre işlecini değiştirebilirsiniz. Örneğin **ile başlayan** işlecini değiştirip **tam olarak** yapabilirsiniz. Her sütun başlığı filtresi kullandığınız ve filtre işlecini değiştirdiğinizde uygulama bu değişikliği depolar. ARdından, bu sütunu daha sonraki filtreleyişinizde, filtre işleci geri yüklenir.
- **Gezinti bölmesi** – Sayfanın sol üst köşesindeki *Gezinti bölmesini genişlet* düğmesini seçerek **Gezinti bölmesini** açabilirsiniz. (Bu düğmeye bazen _**Menü** düğmesi_, *hamburger*, *hamburger menüsü* veya *hamburger düğmesi* adı da verilir.) Gezinti bölmesini açık haliyle sabitleyebilir veya varsayılan olarak daraltılmış tutabilirsiniz. Gezinti bölmesini açık olarak sabitlemenizin ardından uygulama, bölmeyi siz daraltana kadar açık tutar.

## <a name="full-personalization-access-formerly-explicit-personalizations"></a>Tam kişiselleştirme erişimi (daha önce açık kişiselleştirmeler)

**Tam kişiselleştirme erişimi** düzeyinde, kullanıcıların uygulamadaki tüm kişiselleştirme özelliklerine erişimi vardır. Farklı kişilerin ve şirketlerin uygulamayla etkileşimde bulunduklarında özellikle de kullanılan alanlar açısından farklı gereksinimleri olduğundan kişiselleştirme, kullanıcıların ve kuruluşların uygulama içinde bilginin sırasını ve etkileşim şeklini özelleştirmesini sağlayan araçlar sunar. Bu özellikler, size ve kuruluşunuza özel uygulamada basitleştirilmiş ve optimize edilmiş deneyimler sağlamak için çok önemlidir. 

[Kaydedilen görünümler](saved-views.md) özelliği açıksa, bu değişikliklerin belirli bir görünüm için kullanıcı deneyimine uygulanması için açık bir kaydetme gereklidir. **Kaydedilen görünümler** özelliği kapalıyken, bu değişiklikler otomatik olarak kaydedilir.

Aşağıdaki bölümler, **tam kişiselleştirme erişimi** düzeyinde kullanıcıların kullanabildiği kişiselleştirme özelliklerinin kapsamını kapsar. Bu özelliklerden birkaçı şunlardır:

- Kısayol menüsü seçenekleri
- **Kişiselleştirme** araç çubuğu
- Çalışma alanlarına döşeme, liste ve bağlantı ekleme
- Çalışma alanından panoya özet ekleme
- Panoyu kişiselleştirme

### <a name="shortcut-menu-options"></a>Kısayol menüsü seçenekleri

Kısayol menüleri, sizin veya kuruluşunuzun gereksinimlerini daha iyi karşılamak amacıyla bir arabirimi açıkça değiştirmek için bir yol sağlar. (Kısayol menüsü *sağ tıklama menüsü* veya bir *bağlam menüsü* olarak da bilinir.)

Bir sayfada yapılabilecek en tipik ve önemli değişikliklerden bazıları, kısayol menüsündeki seçenekler olarak doğrudan sunulur. Örneğin, kılavuza sütun eklemek veya gizlemek isterseniz bir sütun başlığına sağ tıklayıp **Sütunlar ekle** veya **Bu sütunu gizle**'yi seçmeniz yeterlidir.

Ayrıca, kişiselleştirmelerin en temel türleri de bir öğeye sağ tıklayıp **Kişiselleştir**'i seçerek kullanılabilir. (Sayfanızdaki tüm öğelerin kişiselleştirilemeyeceğini unutmayın.) Bu kişiselleştirme yöntemini kullandığınızda, öğenin *özellik penceresi* görünür.

![Bir öğenin özelliklerini kişiselleştirme.](./media/cli-element-property-window.png)

Bir öğeyi aşağıdaki yöntemlerle kişiselleştirmek için özellik penceresini kullanabilirsiniz:

- Öğenin etiketini değiştirmek.
- Öğeyi gizleyerek sayfada gösterilmemesini sağlamak. Alandaki veriler silinmez veya değiştirilmez. Bilgiler artık sayfada görünmez hale gelir.
- Hızlı sekme özet bölümüne bilgi eklemek (öğe, hızlı sekmedeyse).
- Alanı atlayın, böylece sayfa boyunca sekme üzerinde geçiş yaptığınızda odağı hiçbir zaman alamaz.
- Alandaki verilerin düzenlenmesini önleme (herhangi bir kayıt için).
- Veri girişi için gerekli olacak alanı belirtin. Bu alana değer girilmezse, kırmızı bir kenarlıkla görüntülenir ve bu durumu belirten bir yıldız işareti bulunur. Bu seçenek yalnızca 10.0.11 sürümünden itibaren [Kaydedilen görünümler](saved-views.md) ve **Kişiselleştirme kullanarak alanları gerektiği gibi belirle** özellikleri açıldığında kullanılabilir.

Öğeye bağlı olarak, özellik penceresi başka kişiselleştirme yetenekleri içerebilir. Örneğin, bir kutucuğun özellik penceresi sayesinde o kutucuğu bir panoya yükseltebilir ve bir varsayılan panodaki öğeler için özellik penceresiyle yeni bir özel çalışma alanı oluşturabilirsiniz.

### <a name="personalization-toolbar"></a>Kişiselleştirme araç çubuğu

Bir sayfada birden çok değişiklik veya diğer mekanizmalarla gerçekleştirilemeyen değişiklikler yapmak istiyorsanız (öğeleri yeniden düzenleme istediğinizde), **Kişiselleştirme** araç çubuğunu kullanabilirsiniz. **Kişiselleştirme** araç çubuğunu açmak için, aşağıdaki adımlardan birini izleyin:

- Sayfadaki herhangi bir öğeden **Ctrl + ÜstKrkt + P**'yi seçin.
- Bir öğenin özellik penceresinde **Bu sayfayı kişiselleştir**'i seçin.
- Sayfanın Eylem Panosunda, **Seçenekler** sekmesinde, **Kişiselleştir** grubunda, **Bu formu kişiselleştir**'i seçin.
- Gezinti çubuğundaki **Ayarlar** düğmesini (dişli sembolü) seçin ve sonra **Kişiselleştir**'i seçin.

[![Kişiselleştirme araç çubuğu.](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Sayfada gezinme

**Kişiselleştirme** araç çubuğu açıkken, temel sayfa salt okunurdur (başka bir deyişle, verileri düzenleyemezsiniz), ancak hala etkileşimlidir. Özellikle bu eylemleri sayfada gerçekleştirirken olduğu gibi, **İlgili bilgi** bölmesini genişletebilir veya daraltabilir, sekmeler arasında geçiş yapabilir ve bölümleri genişletebilir veya daraltabilirsiniz. Daraltılabilir bir bölüm veya bir sekmede bir kişiselleştirme yapmak için (örneğin bir hızlı sekmeyi gizlemek için) klavye odağında olduğunda veya üzerinde durduğunuzda bölüm veya sekmenin yanında görüntülenen düğmeyi seçmeniz gerekir.

#### <a name="personalization-tools"></a>Kişiselleştirme araçları

**Kişiselleştirme** araç çubuğunda aşağıdaki araçlar mevcuttur:

- Bir öğeyi seçip özelliklerini değiştirmek için **Seç** aracını kullanın. Bu aracı kullanmak için, araç çubuğunda **Seç** düğmesini seçin ve sonra istediğiniz öğeyi seçin. Öğenin özelliklerini değiştirebileceğiniz özellik penceresi görünür. Sayfada kişiselleştirilebilecek başka öğeler için işlemi yineleyebilirsiniz. Bazı senaryolarda bazı kişiselleştirme özelliklerinin kullanılabilir olmayacağını unutmayın. Örneğin, gerekli bir alanı kilitleyemezsiniz.
- Sayfadaki bir öğeyi gizlemek için **Gizle** aracını kullanın. Bu aracı kullanmak için, araç çubuğunda **Gizle** düğmesini seçin ve sonra gizlenecek öğeyi seçin. **Gizle** aracını kullandığınız zaman, gizli durumdaki tüm öğeler görünür hale gelir ancak gölgeli bir kapsayıcıda gösterilirler. Böylece, öğeyi seçerek görünür yapabilirsiniz. Öğeler gizli olduğunda sayfanın nasıl görüneceğini görmek için başka bir kişiselleştirme aracına geçin veya kişiselleştirme araç çubuğunu kapatın.
- Sayfanıza alan eklemek için **Alan ekle** aracını kullanın. Bu aracı kullandığınızda yalnızca sayfa tanımının parçası olan alanlar ekleyebilirsiniz. Geçerli sayfa tanımının bir parçası olmayan yeni alanların nasıl oluşturulacağı hakkında bilgi için bkz. [Özel alanlar oluşturma ve bunlarla çalışma](user-defined-fields.md). Araç çubuğunda **Alan ekle** düğmesini seçtikten sonra, ilk olarak, alan eklemek istediğiniz kılavuzu veya bölümü seçmeniz gerekir. Bir iletişim kutusunda, seçilen kılavuz veya bölümle ilgili alanların listesi görüntülenir. İletişim kutusunda, **Önerilen alanlar** veya **Tüm alanlar** listesinden eklemek için bir veya daha fazla alan seçin. İstediğiniz alanları seçtikten sonra **Güncelleştir**'i seçin. Önceden eklediğiniz bir alanı kaldırmak için bu işlemi yineleyin ancak iletişim kutusundaki alan seçimini temizleyin.

    **Önerilen alanlar** listesi, kuruluşunuzdaki diğer kullanıcılar tarafından daha önce eklenmiş alanları gösterir. Bu alan listesi, **Önerilen toplu işin** yinelenme sıklığına göre güncelleştirilir. Sayfadaki Filtre bölmesini kullanarak yeni filtre alanları eklerken de benzer bir deneyim yaşanır.

- Bir öğeyi mevcut öğeler grubu içinde farklı bir konuma taşımak için **Taşı** aracını kullanın. Bir öğeyi üst grubunun dışına taşıyamazsınız. Bu aracı kullanmak için, araç çubuğunda **Taşı** düğmesini seçin ve sonra taşınacak öğeyi seçin. Bir öğeyi seçtiğinizde uygulama öğenin taşınabileceği konumları belirler. Bu konumlara *bırakma alanları* denir. Öğeyi mevcut grup içinde sürükledikçe, her bırakma bölgesi, öğenin bırakılabileceği alanın yanında renkli ve kalın bir çizgi olarak gösterilir.
- Sayfanın klavye sekmesi sırasından bir öğeyi kaldırmak için **Atla** aracını kullanın. Araç çubuğunda **Atla** düğmesini seçtiğiniz zaman, atlanmış durumdaki tüm öğeler gölgeli bir kapsayıcıda gösterilir. Etkileşimli olarak sekme sırasına alan ekleme veya kaldırma yapabilirsiniz.
- Bir öğenin hızlı sekme özet bölümünde görünmesini isterseniz **Başlıkta göster** aracını kullanın. Araç çubuğunda **Başlıkta göster** düğmesini seçtiğiniz zaman, özet alanı olarak seçilen tüm alanlar gölgeli bir kapsayıcıda gösterilir. Hızlı sekme özetine etkileşimli olarak alan ekleyebilir veya hızlı sekme özetinden alanları seçerek kaldırabilirsiniz.
- Veri girişi için bir öğeyi gerekli olarak belirlemek üzere **Gerekli** aracını kullanın. Araç çubuğunda **Gerekli** düğmesini seçtiğiniz zaman, gerekli olacak kişiselleştirilmiş tüm öğeler gölgeli bir kapsayıcıda gösterilir. Bu durumda bu öğeleri yeniden gerekli değil durumuna getirebilirsiniz. Bu seçenek yalnızca 10.0.12 ve üzeri sürümünden itibaren **Kişiselleştirme kullanarak alanları gerektiği gibi belirle** özellikleri açıldığında kullanılabilir.
- Bir öğeyi düzenlenebilir veya düzenlenemez olarak işaretlemek için **Kilitle** aracını kullanın. Araç çubuğunda **Kilitle** düğmesini seçtiğiniz zaman, düzenlenemez durumdaki tüm öğeler gölgeli bir kapsayıcıda gösterilir. Bu durumda bu öğeleri yeniden düzenlenebilir hale getirebilirsiniz. Bazı alanların gerekli olduğunu ve düzenlenemez yapılamayacağını unutmayın. Bu alanların yanında bir asma kilit simgesi görünür.
- Microsoft Power Apps kullanarak oluşturulmuş bir uygulamayı sayfaya katıştırmak için **Power Apps'ten uygulama ekle** aracını kullanın. Power Apps uygulamasını bir sayfaya katıştırma hakkında ayrıntılı bilgi için bkz. [Power Apps uygulamalarını katıştırma](embed-power-apps.md). Bu seçenek yalnızca [Kaydedilmiş görünümler](saved-views.md) özelliği kapalıyken kullanılabilir.
- Microsoft Power Apps veya üçüncü taraf kullanarak oluşturulmuş bir uygulamayı sayfaya katıştırmak için, **uygulama ekle** düğmesini kullanın. Bu seçenek yalnızca [Kaydedilmiş görünümler](saved-views.md) özelliği açıkken kullanılabilir. 
- Sayfayı varsayılan, ilk yüklendiği durumuna sıfırlamak için **Temizle** aracını kullanın. Geçerli sayfadaki tüm kişiselleştirmeler temizlenir. Bu eylem geri alınamaz. Bu nedenle, bu aracı ancak sayfa sıfırlamak istediğinizden emin olduğunuzda kullanın. **Kaydedilen görünümler** özelliği açık olduğunda, bu araç geçerli görünümün kişiselleştirmelerini temizler.
- Sizin veya başka birinin daha önce oluşturduğu bir dosyadan kişiselleştirme yüklemek için **İçe aktar** aracını kullanın. 

    - **Kaydedilmiş görünümler** özelliği kapalıyken, sayfa için içe aktarılan kişiselleştirmeleri ekleme veya varolan kişiselleştirmelerinizle değiştirme seçeneklerinden birini belirleyebilirsiniz. Bu eylem geri alınamaz. Bu nedenle, kişiselleştirmeleri içe aktardıktan sonra, istemediğiniz değişiklikleri el ile temizlemeniz veya geri almanız gerekir.
    - **Kaydedilen görünümler** özelliği açık olduğunda, içe aktarılan kişiselleştirmeler sayfada bir görünüm olur. Görünüm zaten varsa, içe aktarmayı atlama, aynı ada sahip geçerli görünümü değiştirme veya içe aktarılan görünümü yeniden adlandırma seçeneğiniz olur.

- Sayfadaki kişiselleştirmelerinizi bir dosyaya kaydetmek için **Dışa aktar** aracını kullanın. Böylece kişiselleştirmelerinizi başka kullanıcılarla paylaşabilirsiniz. Bu kullanıcıların, sayfaya ilişkin kişiselleştirmelerinizi içeren dosyayı içe aktarmaları gerekir. **Kaydedilen görünümler** özelliği açık olduğunda, bu araç geçerli görünümü paylaşma için bir dosyaya kaydeder.
- **Kişiselleştirme** araç çubuğunu kapatmak ve sayfayı önceki etkileşimli durumuna döndürmek için **Kapat** düğmesini seçin.

Geleneksel olarak, **Kişiselleştirme** araç çubuğu kullanıldığında, kişiselleştirmeleri yaptığınız anda etkin olur. Ancak, [Kaydedilmiş görünümler](saved-views.md) özelliği açıksa, kişiselleştirmeleri özel olarak seçtiğiniz bir görünüme kaydetmeniz gerekir.

Bazı durumlarda, bir araç seçtiğiniz zaman öğenin yanında bir asma kilit simgesi görünür. Bu simge, seçilen araçla ilgili öğe özelliklerini değiştiremeyeceğiniz çünkü bu özelliklerde yapılan değişikliklerin sayfanın doğru işleyişini engelleyeceği anlamına gelir.

### <a name="adding-tiles-lists-and-links-to-a-workspace"></a>Bir çalışma alanına döşeme, liste ve bağlantı ekleme

Listeler içeren bazı sayfalarda, **Çalışma alanına ekle** kişiselleştirme özelliği, Eylem bölmesinin **Seçenekler** sekmesindeki **Kişiselleştir** grubunda yer alır. Bu özellik, ilgili bilgileri geçerli listeden belirli bir çalışma alanına itmenizi sağlar. Çalışma alanında görünen bilgiler tüm listeyi veya listenin filtrelenmiş ve sıralanmış bir sürümünü temel alabilir. Çalışma alanında bilgilerin bir liste veya listedeki öğe sayısını gösterebilen bir özet kutucuk ya da bir bağlantı olarak görüneceğini de belirtebilirsiniz.

> [!NOTE]
> [Kaydedilmiş görünümler](saved-views.md) özelliği açıksa bir çalışma alanına ittiğiniz içerik doğrudan bir görünüme bağlıdır. Görünümün sorgusu, çalışma alanındaki verileri getirmek için kullanılır ve çalışma alanındaki ilgili döşeme veya bağlantı sayfayı bu görünüme açar; böylece görünümün sorgu ve kişiselleştirmeleri buna uygulanır. Görünüm güncelleştirilmişse, ilgili çalışma alanı öğeleri yeni görünüm tanımına göre ayarlanacaktır.

[![Çalışma alanına ekleme.](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Çalışma alanına liste eklerken, çalışma alanında listenin bilgileri istediğiniz gibi göstermesini sağlamak için sayfada listeyi sıralayın veya filtreleyin. (**Kaydedilmiş görünümler** özelliği açıksa, bu koşullara sahip bir görünümü kaydedene kadar devam edemezsiniz). Sonra **Çalışma alanına ekle**'yi seçin. Bir çalışma alanı seçin ve ardından **Sunum** alanında **Liste**'yi seçin. **Yapılandır**'ı seçtikten sonra, çalışma alanındaki listede görünmesi gereken sütunları seçebildiğiniz bir iletişim kutusu görünür. Çalışma alanındaki liste için kullanılan etiketi de belirtebilirsiniz.
- Çalışma alanına kutucuk eklemek için, önce özetlenmesi gereken veya hızlı erişilmesini istediğiniz verileri göstermesi için sayfadaki listeyi filtreleyin. (**Kaydedilmiş görünümler** özelliği açıksa, bu koşullara sahip bir görünümü kaydedene kadar devam edemezsiniz). Sonra **Çalışma alanına ekle**'yi seçin. Bir çalışma alanı seçin ve ardından **Sunum** alanında **Kutucuk**'u seçin. **Yapılandır**'ı seçtikten sonra, çalışma alanındaki kutucuk için kullanılması gereken etiketi belirtebildiğiniz bir iletişim kutusu görünür. Kutucukta bir sayı gösterilip gösterilmeyeceğini de belirtebilirsiniz. Kutucuk çalışma alanına eklendikten sonra, geçerli sayfayı çalışma alanından açmak için onu seçebilirsiniz. Böylece,kutucukla ilişkili filtre uygulanmış listeyi görüntüleyebilirsiniz.
    - Sürüm 10.0.26'dan itibaren, **Kullanıcıların kutucu boyutlarını seçmesine ve değiştirmesine izin ver** özelliğini etkinleştirdiyseniz, **Kutucuğu yapılandır** iletişim kutusunda yeni kutucuğa uygun dört **Kutucuk boyutundan** birini seçebilirsiniz. Bu özellik, çalışma alanından doğrudan oluşturulduktan sonra kutucuk boyutunu ayarlamanıza de olanak tanır.   
- Bir çalışma alanına bağlantı eklemek için, önce sayfadaki listeyi filtreleyerek, ilgilendiğiniz verileri göstermesini sağlayın. (**Kaydedilmiş görünümler** özelliği açıksa, bu koşullara sahip bir görünümü kaydedene kadar devam edemezsiniz). Sonra **Çalışma alanına ekle**'yi seçin. Bir çalışma alanı seçin ve ardından **Sunum** alanında **Bağlantı**'yı seçin. **Yapılandır**'ı seçtikten sonra, bağlantı için kullanılması gereken etiketi belirtebildiğiniz bir iletişim kutusu görünür. İsteğe bağlı olarak, bu bağlantının değiştirilebileceği bir bölüm için de etiket belirtebilirsiniz. Bu bölüm yoksa yeni bir bölüm oluşturulur.

> [!NOTE]
> 10.0.25 sürümü itibarıyla listenizi, kutucuğunuzu veya bağlantınızı yapılandırdığınızda **Çalışma alanları için kaydedilmiş görünümler desteği** etkinse öğeyi eklemek istediğiniz çalışma alanı görünümlerini seçmeniz gerekebilir. Kullanılabilir çalışma alanı görünümleri her **Yapılandır** iletişim kutusunun **Çalışma alanı seçenekleri** bölümünde görünür. 

Liste, kutucuk veya bağlantıyı bir çalışma alanına ekledikten sonra o çalışma alanı açıp, öğeleri istediğiniz gibi yeniden düzenleyebilirsiniz.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Çalışma alanından panoya özet ekleme

Bazı çalışma alanları sayı kutucukları (yani üzerinde sayılar bulunan kutucuklar) içerir ve bu kutucukların panonuzda da görünmesini isteyebilirsiniz. Çalışma alanında bir sayı kutucuğuna sağ tıklayın, **Kişiselleştir**'i ve ardından kutucuğun özellik penceresinde **Panoya sabitle**'yi seçin. Panoyu bir dahaki açışınızda (ve yenilemenizde) sayı o çalışma alanının gezinti kutucuğunun altında görünür. Bu sayıyı doğrudan seçerek, temsil ettiği verilere doğrudan gidebilirsiniz.

### <a name="changing-the-size-of-a-tile"></a>Kutucuk boyutunu değiştirme
10.0.26 sürümünden başlayarak, **Kullanıcıların kutucuk boyutlarını seçmesine ve değiştirmesine izin ver** özelliği, kullanıcıların KPI olmayan herhangi bir kutucuğun boyutunu kişiselleştirme yoluyla değiştirmesine olanak tanır. Bir çalışma alanında, kutucuğuna sağ tıklayın ve **Kişiselleştir**'i seçin. Kutucuğun özellik penceresinde, **Kutucuk boyutu** seçeneklerinde istediğiniz boyutu seçin. Kutucu boyutu hemen ayarlanacak. **(Önizleme) Çalışma alanları için kaydedilen görünümler** özelliği etkinleştirildiyse, bu kişiselleştirmeyi bir çalışma görünümüne kaydedebilirsiniz.  

### <a name="personalizing-your-dashboard"></a>Panonuzu kişiselleştirme

Pano, çoğunlukla uygulamayı açtığınızda gördüğünüz ilk sayfadır. Bu konunun önceki bölümlerinde açıklanan mekanizmaları kullanarak, sistemdeki diğer tüm sayfalar gibi kişiselleştirilebilir. 

> [!WARNING]
> Şu anda, panodaki içeriği gizlediğinizde, etrafındaki boşluğu değil, doğrudan bir kutucuğu hedeflemeniz önemlidir. Grubu bir kutucuğun etrafında gizlerseniz, daha sonra daha fazla kutucuk eklenirse veya sistem farklı bir dile geçerse beklenmedik sonuçlar ortaya çıkabilir.

Panoda bulunan benzersiz bir kişiselleştirme özelliği kutucuk ekleyebilme özelliğidir. 

- **Tam sayfa uygulamaları** özelliği kapalıysa, panoda bir öğeye sağ tıklayıp sonra da **Çalışma alanı ekle**'yi seçerek yeni bir kutucuk eklersiniz. Panonun alt kısmında yeni bir çalışma alanı kutucuğu oluşturulur. Bu yeni çalışma alanı kutucuğunu istediğiniz gibi yeniden adlandırabilirsiniz. Bu konunun [Çalışma alanına liste, kutucuk ve bağlantı ekleme](personalize-user-experience.md#adding-tiles-lists-and-links-to-a-workspace) bölümünde açıklandığı gibi, çalışma alanına listeler, kutucuklar ve bağlantılar da ekleyebilirsiniz.
- **Tam sayfa uygulamaları** özelliği kapalıysa, panoda bir öğeye sağ tıklayıp sonra da **Uygulama ekle**'yi seçerek yeni bir kutucuk eklersiniz. İletişim kutusunda, yeni bir çalışma alanına bir kutucuk veya Power Apps ya da bir web sitesinden içerik içeren bir kutucuk eklemeyi seçin. Sonra belirlediğiniz seçeneği yapılandırmak için ilgili adımları izleyin. Panonun alt kısmında yeni bir kutucuk oluşturulur. Bu katıştırılmış uygulamaları ekleme, düzenleme, silme ve paylaşma hakkında daha fazla bilgi için bkz. [Power Apps'teki tuval uygulamalarını katıştırma](embed-power-apps.md) ve [Üçüncü taraf uygulamaları katıştırma](embed-website.md).

## <a name="sharing-personalizations"></a>Kişiselleştirmeler paylaşma

Bir sayfayı kişiselleştirdikten sonra, kişiselleştirmelerinizi diğer kullanıcılarla paylaşmak için kullanabileceğiniz birkaç yöntem bulunur. Aşağıdaki listede, bu yöntemler en çok önerilenden en az önerilene doğru düzenlenmiştir.

1. Görünümleri kullanıcılara yayımlayın.
2. Görünümleri veya kişiselleştirmeleri kullanıcılara kopyalayın.
3. Görünümleri veya kişiselleştirmeleri dışa ve içe aktarın.

### <a name="publish-views-to-users"></a>Görünümleri kullanıcılara yayımlama

[Kaydedilen görünümler](saved-views.md) özelliği açıksa ve sayfa görünümleri destekliyorsa, kişiselleştirmeleri diğer kullanıcılarla paylaşmanın en iyi yolu, görünümü bir veya daha fazla güvenlik rolüne sahip kullanıcılar için yayımlamaktır. Daha fazla bilgi için bkz. [Görünümleri yayımlama](saved-views.md#publishing-views).

### <a name="copy-views-or-personalizations-to-users"></a>Görünümleri veya kişiselleştirmeleri kullanıcılara kopyalama

[Kaydedilen görünümler](saved-views.md) özelliği kapalıysa veya sayfa görünümleri desteklemiyorsa, kişiselleştirmeleri paylaşmak için önerilen yol bunları kullanıcılar arasında kopyalamaktır. Bu yöntem yalnızca ayrıcalıklı kullanıcılar (örneğin, sistem yöneticileri) tarafından kullanılabilir. Ancak, yöneticiler sistemdeki belirli bir kullanıcının kişiselleştirmesini (kaydedilmiş görünümler etkinse kullanıcının kişisel görünümü de dahil) arayabilir ve yapılandırmayı diğer kullanıcılara kopyalayabilir.

Kaydedilmiş görünümler etkinse, kişiselleştirmeleri kopyalamak için aşağıdaki adımları izleyin.

1. **Sistem yönetimi \> Kurulum \> Kişiselleştirme**'ye gidin.
2. Kişisel görünümleri kopyalamak için şu adımları izleyin:

    1. **Kişisel görünümler**'i seçin.
    2. Listeden dilediğiniz görünümleri seçin.
    3. **Kullanıcılara kopyala**'yı seçin.
    4. Görünümlerin dağıtılacağı kullanıcıları seçin.

    Görünümü desteklemeyen sayfalardaki kişiselleştirmeleri kopyalamak için şu adımları izleyin:

    1. **Kullanıcı ayarlarını** seçin.
    2. Dağıtmak istediğiniz kişiselleştirmeye sahip kullanıcıyı seçin.
    3. **Tüm kişiselleştirmeleri yönet**'i seçin.
    4. Listeden dilediğiniz kişiselleştirmeleri seçin.
    5. **Kullanıcılara kopyala**'yı seçin.
    6. Kişiselleştirmelerin dağıtılacağı kullanıcıları seçin.

Kaydedilmiş görünümler etkin değilse kişiselleştirmeyi kopyalamak için aşağıdaki adımları izleyin.

1. **Sistem yönetimi \> Kurulum \> Kişiselleştirme**'ye gidin.
2. **Uygula**'yı seçin.
3. Kişiselleştirmenin dağıtılacağı kullanıcıları seçin.
4. **Varolan kişiselleştirmeyi seç**'i seçin.
5. İlgilendiğiniz (tek) kişiselleştirmeyi bulun ve seçin.
6. **Tamam**'ı seçin.

### <a name="export-and-import-views-or-personalizations"></a>Görünümleri veya kişiselleştirmeleri dışa ve içe aktarma

Kişiselleştirmeleri paylaşmanın başka bir yolu da dışa ve içe aktarmadır. Bireysel kullanıcılar veya bu kişiler adına hareket eden bir yönetici, bu yöntemi kullanarak kendi kişiselleştirmelerini veya görünümlerini dışa aktarabilir ve dışa aktarılan dosyayı içe aktarmaları üzere diğer kullanıcılara verebilir. Alternatif olarak, kullanıcılar yönetici ayrıcalıklarına sahip bir kullanıcıya dışa aktarılan kişiselleştirmelerini verebilir ve böylece söz konusu kullanıcı aynı anda birçok kullanıcıya kişiselleştirme dosyası uygulamak için **kişiselleştirme** yönetim sayfasını kullanabilir.

> [!IMPORTANT]
> Kişiselleştirmeler, güncelleştirmeler arasında kalıcı olarak, bir hizmet güncelleştirmesinden veya başka bir zamanda tüm kişiselleştirmeleri gereksiz ve önerilmez.

#### <a name="export"></a>Dışarı aktar

Genel olarak, kendi görünümlerinizi veya kişiselleştirmelerinizi, uygun sayfayı açıp **Kişiselleştirme** araç çubuğunu açıp **Dışa aktar**'ı seçerek verebilirsiniz. Araç çubuğu hakkında daha fazla bilgi için bu konunun önceki bölümlerinde yer alan [Kişiselleştirme araç çubuğu](#personalization-toolbar) kısmını inceleyin. Alternatif olarak, [kaydedilmiş görünümler](saved-views.md)etkinse, sistem içindeki tüm kişiselleştirmeler listesini görüntülemek için **Ayarlar \> Kullanıcı seçenekleri \> Kişiselleştirme**'ye gidebilirsiniz. Daha sonra dışa aktarılacak görünümleri ya da kişiselleştirmeleri seçebilir ve **Dışa aktar**'ı seçebilirsiniz.

Ek olarak, yöneticiler aşağıdaki adımları izleyerek diğer kullanıcıların kişiselleştirmelerini dışa aktarabilir.

1. **Sistem yönetimi \> Kurulum \> Kişiselleştirme**'ye gidin.
2. **Kullanıcılar** sekmesinde, dilediğiniz kullanıcıyı seçin.
3. İlgilendiğiniz görünümü veya kişiselleştirmeyi bulun ve seçin.
4. **Dışa Aktar**'ı seçin.

#### <a name="import"></a>İthalat

Bir görünümü veya kişiselleştirmeyi içe aktarmak için **Kişiselleştirme** araç çubuğunu açıp **İçe aktar**'ı seçebilirsiniz. Ek olarak, yöneticiler bir dosyayı içe aktarabilir ve bir ya da daha fazla kullanıcıya hemen verebilir.

Kaydedilmiş görünümler etkinse, aşağıdaki adımları izleyin.

1. **Sistem yönetimi \> Kurulum \> Kişiselleştirme**'ye gidin.
2. Eylem Bölmesinde, **Görünümleri içe aktar \> Kullanıcı görünümleri**'ni seçin.
3. İçeri aktar modunu seçin:

    - **Belirli kullanıcıları seç** – Görünüm veya kişiselleştirmeyi seçili kullanıcılara verin.
    - **Olduğu gibi içe aktar** – Görünümü veya kişiselleştirmeyi dışa aktaran kullanıcıya aktarın.

4. **Göz at**'ı seçin ve içe aktarılacak kişiselleştirmeyi bulun ve seçin.
5. **Sonraki**'yi seçin.
6. 3. adımda **Belirli kullanıcıları seç** seçeneğini belirlediyseniz, kişiselleştirmenin aktarılacağı kullanıcıları seçin.
7. **İçe aktar**'ı seçin.
8. Çakışmaları gerektiği gibi çözümleyin.

Kaydedilmiş görünümler etkin değilse, aşağıdaki adımları izleyin.

1. **Sistem yönetimi \> Kurulum \> Kişiselleştirme**'ye gidin.
2. **Uygula**'yı seçin.
3. Kişiselleştirmenin dağıtılacağı kullanıcıları seçin.
4. **Kişiselleştirmeleri bir dosyadan içe aktar**'ı seçin.
5. **Göz at**'ı seçin ve içe aktarılacak kişiselleştirmeyi bulun ve seçin.
6. **Tamam**'ı seçin.

## <a name="administration-of-personalizations"></a>Kişiselleştirme yönetimi

**Kişiselleştirme** sayfası, bir organizasyon düzeyinde kişiselleştirmeleri yönetmek için Merkez hub 'ın bulunduğu yerdir. Bu sayfadaki içerikler ve yetenekler **kaydedilmiş görünümler** özelliğinin açılmış olmasına bağlıdır.

**Kaydedilmiş görünümler** özelliğini açmış olan müşteriler için [kaydedilmiş görünümler](saved-views.md) konusunun "görünümleri genel olarak yönetme" bölümüne bakın.

[Kaydedilmiş görünümler](saved-views.md) özelliğini henüz etkinleştirmemiş olan müşteriler için bu sayfanın dört sekmesi vardır:

- **Uygula** – Bir veya birden fazla kullanıcı için bir kişiselleştirmeyi içe aktarabilir veya seçebilirsiniz. Bir kişiselleştirmeyi bir veya daha fazla kullanıcıya uygulamak için önce bir rol ve o role sahip kullanıcıları seçin. Daha sonra, ya seçilen kullanıcılara uygulamak üzere mevcut bir kişiselleştirmeyi seçin veya bir kişiselleştirme dosyasını içe aktarın. Kişiselleştirme doğrulanır ve seçilen tüm kullanıcılara, seçili sayfayı bir dahaki açışlarında uygulanır.
- **Temizle** – Bir sayfanın veya çalışma alanının tüm kişiselleştirmelerini bir veya birden fazla kullanıcı için temizleyebilirsiniz. Önce bir sayfayı veya çalışma alanını özelleştiren kullanıcıların listesini görmek için o sayfayı veya çalışma alanını seçin. Ardından, o sayfa veya çalışma alanı için kişiselleştirmelere sahip olması gereken kullanıcıları seçin ve **Temizle**'yi seçin. Seçili kullanıcıların seçili sayfaya veya çalışma alanına uyguladığı tüm kişiselleştirmeler silinir. Bu eylem geri alınamaz. Ancak, sayfa veya çalışma alanı için kaydedilmiş bir kişiselleştirme varsa, kişiselleştirme yeniden içe aktarılabilir.
- **Kullanıcılar** – Bir kullanıcı seçerek, kullanıcının kişiselleştirdiği sayfaların listesini görün. Bunun ardından, seçili kullanıcıların belirli sayfalar veya tüm sistem için kişiselleştirme kullanma yeteneklerini etkinleştirebilir veya devre dışı bırakabilirsiniz. Ayrıca, kullanıcı için bir kişiselleştirmeyi içe veya dışa aktarabilir ya da temizleyebilirsiniz. Ek olarak, kullanıcı için özellik açıklamalarını sıfırlayabilirsiniz. Bu durumda, kullanıcı yeni özellikler içeren açılır pencereleri önceden devre dışı bırakmışsa, bu özellikler kullanıcının bir sonraki karşılaştığı sefer yeniden görünürler.
- **Sistem:** Tüm kullanıcılar için kişiselleştirmeleri geçici olarak devre dışı bırakabilirsiniz. Bu durumda, tüm kullanıcılar için tüm kişiselleştirmeler silinir ve tüm sayfalar varsayılan durumlarına sıfırlanır. Kişiselleştirmeyi daha sonra yeniden etkinleştirirseniz, tüm kişiselleştirmeler yeniden uygulanır. Ayrıca sistemdeki tüm kullanıcılar için tüm kişiselleştirmeleri kalıcı olarak silebilirsiniz. Silinmiş kişiselleştirmeler kurtarılamaz. Bu nedenle, bu görevi uygulamadan önce, daha sonra içeri aktarmak isteyebileceğiniz kişiselleştirmeleri dışa aktardığınızdan emin olun.

## <a name="personalizing-inventory-dimensions"></a>Stok boyutlarının kişiselleştirilmesi

Bir sayfadaki stok boyutlarının ayarlamasını kişiselleştirirseniz, **Görüntü boyutları** seçeneği kullanılarak oluşturulan ayarları dikkate alın. Örneğin, Toplu iş numarası stok boyutu için bir sütunu gizlemek amacıyla kişiselleştirme kullanıyorsunuz ancak sayfa bir daha açıldığında sütun görünüyor. Bu davranış, gösterilen stok boyutu sütunlarını **Boyutların görünümü** ayarlarının kontrol etmesinden kaynaklanır. **Boyutların görünümü** ayarları tüm sayfalar için geçerlidir ve stok boyutu alanlarının ayrı sayfalardaki kişiselleştirme ayarlarını geçersiz kılar.

Bu nedenle, önceki örnekteki Toplu iş numarası stok boyutu için sütunun bir sayfada istemiyorsanız o boyutu, tablonun **Boyutların görünümü** seçeneğinin bir parçası olarak sayfadan temizlemeniz gerekir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
