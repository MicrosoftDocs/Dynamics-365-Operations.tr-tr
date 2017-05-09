---
title: "Kullanıcı deneyimini kişiselleştirme"
description: "Bu makalede Microsoft Dynamics 365 for Operations&quot;ı nasıl kişiselleştirebileceğiniz açıklanmaktadır."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 8965c193839002776b3c61036b23b54625c974a4
ms.lasthandoff: 03/31/2017


---

# <a name="personalize-the-user-experience"></a>Kullanıcı deneyimini kişiselleştirme

[!include[banner](../includes/banner.md)]


Bu makalede Microsoft Dynamics 365 for Operations'ı nasıl kişiselleştirebileceğiniz açıklanmaktadır.

Microsoft Dynamics 365 for Operations'da birçok kişiselleştirme türü vardır. Bazı kişiselleştirmeler bir kurulum sayfasında bulunan seçenekler listesinde yaptığınız seçimlerdir. Bazı kişiselleştirmeler dolaylıdır; örneğin, Dynamics 365 for Operations ayarladığınız takdirde ızgara sütunların genişliğini ve Hızlı Sekmelerin genişletilme/daraltılma durumunu izler. Diğer kişiselleştirmeler açıktır. Açık kişiselleştirmeler için, etkileşimli kişiselleştirme moduna girip, doğrudan öğelerin sayfadaki görünüşünü veya çalışmasını yöneterek bir sayfanın görünümünü değiştirebilirsiniz. 

Kullanıcının etkileşimde bulunduğu şirket ne olursa olsun, Dynamics 365 for Operations'da bir kullanıcının yaptığı, her türden tüm kişiselleştirmeler yalnızca o kullanıcıya aittir. Kullanıcının bir sayfada yaptığı değişiklikler sistemdeki diğer kullanıcıları etkilemez.

## <a name="systemwide-options-for-the-current-user"></a>Geçerli kullanıcının sistem çapında seçenekleri
Gezinti çubuğunda **Ayarlar** menü düğmesi olarak adlandırılan bir dişli çark imgesi bulacaksınız. **Ayarlar** menüsü açıldığında bir dizi seçenek görünür. **Seçenekleri** öğesi seçildiğinde, kullanıcı **Seçenekler** sayfası açılır. Burada dört seçenek öğesi bulunur: **Görsel**, **Tercihler**, **Hesap** ve **İş akışı**.

-   **Görsel: **Bir renk teması ve sayfalarınızdaki öğelerin varsayılan boyutunu seçmek için kullanılır.
-   **Tercihler: ** Burada şirket, ilk sayfa ve (bir sayfanın görüntülenmesinin kilitlenip kilitlenmemesini veya her açtığınızda düzenleme için açılıp açılmamasını belirleyen) varsayılan görüntüleme/düzenleme modu dahil olmak üzere, Dynamics  365 for Operations'ı her açışınızda varsayılanları burada seçebilirsiniz. Ayrıca, dil, saat dilimi ve tarih, saat ve sayı biçimlendirme seçeneklerini bulacaksınız. Son olarak bu sayfa sürümden sürüme değişiklik gösterecek birçok muhtelif tercih içerir.
-   **Hesap: **Kullanıcı kimliğinizi ve hesapla ilgili diğer seçenekleri sağlamak için kullanılır.
-   **İş akışı: **Burada iş akışı ile ilgili seçenekleri seçebilirsiniz.

## <a name="implicit-personalizations"></a>Dolaylı kişiselleştirmeler
Dolaylı kişiselleştirmeler, salt o anki güncel durumlarını hatırlayan belli kontrollerle etkileşime girerek yaptığınız kişiselleştirmelerdir. 

**Izgara sütunları:** Bir listedeki bir sütunun genişliğini, sütun başlığının solundaki ya da sağındaki boyutlandırma çubuğunu seçerek ve bunu istenen genişliğe kadar sola veya sağa kaydırarak ayarlayabilirsiniz. Dynamics 365 for Operations, istediğiniz genişliği kaydeder ve o listeyi içeren sayfayı her açtığınızda o sütunu o genişlikte gösterir. 

**Hızlı Sekmeler:** Bazı sayfaların Hızlı Sekmeler denilen genişletilebilir bölümleri vardır. Dynamics 365 for Operations hangi Hızlı Sekmeleri genişlettiğinizi, hangilerini daralttığınızı kaydeder. Sayfaya her geri döndüğünde, bu Hızlı Sekmeler son kullandığınız zamanki ayarlamanıza göre genişletilir veya daraltılır. Bu makalede, Hızlı Sekme bölümlerinizin sırasını nasıl değiştireceğinizi açıklayacağız. Bazı durumlarda, Dynamics 365 for Operations'ın bir Hızlı Sekme genişletilene kadar o Hızlı Sekmeye ilişkin bilgilere ulaşmasına gerek olmayacağı için, bir Hızlı Sekmeyi daraltmak performansı arttırabilir. 

**Bilgi Kutuları:** Bazı sayfalarda Bilgi Kutusu bölmesi denilen bir bölüm bulunur. Bu bölme, o sayfadaki güncel konuyla ilgili salt okunur bilgileri içerir. Bilgi Kutusu Bölmesindeki her bölüm bir Bilgi Kutusu olarak adlandırılır. Bir Bilgi Kutusunu genişletebilir veya daraltabilirsiniz ve Dynamics 365 for Operations tercihinizi saklar. Bazı durumlarda, Dynamics 365 for Operations'ın bir Bilgi Kutusu genişletilene kadar o Bilgi Kutusuna ilişkin bilgilere ulaşmasına gerek olmayacağı için, bir Bilgi Kutusunu daraltmak performansı arttırabilir.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Kişiselleştirme araç çubuğu kullanılarak açık kişiselleştirmeler
Her kişi ve şirketin onlar için en önemli verilerin neler olduğu veya işlerini yürütmeleri için hangi verilerin gerekli olmadığı konusunda farklı bir bakış açısı vardır. Bilgilerinizi düzenleme, etkileşime girdirme, hatta gizleme şeklinizi uyarlayabilme özelliği, Dynamics 365 for Operations'ı kişisel ve verimli bir deneyim haline getirmenin temel unsurdur. 

Açık kişiselleştirmeler, bir kişiselleştirme menüsü seçerek bir öğe ya da sayfanın davranışını veya görünümünü değiştirmek amacıyla açık şekilde gerçekleştirdiğiniz kişiselleştirmelerdir. Açık kişiselleştirmenin en temel türü bir öğeye sağ tıklayıp **Kişiselleştir**'i seçtiğiniz kişiselleştirmedir. (Sayfanızdaki tüm öğelerin kişiselleştirilemeyeceğini unutmayın.) Bu kişiselleştirme yöntemini seçtiğinizde, öğenin özellik penceresini görürsünüz. 

[![Bir öğenin özelliklerini kişiselleştirme](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Salt bir öğenin etiketini değiştirmek, öğeyi sayfada görülmeyecek şekilde gizlemek (bu yüzden hiçbir veri değişmez, sadece bilgileri göremezsiniz), öğeyle gezerken alanı atlamak veya verileri "Düzenleme" olarak işaretleyerek değiştirilemeyecek hale getirmek istiyorsanız, sayfanızda bu öğeyi kişiselleştirebilirsiniz. 

Öğeleri taşımak veya gizlemek ya da birkaç değişiklik yapmak istiyorsanız, **Bu formu kişiselleştir** seçeneğini seçerek öğe Özellikler penceresinden ulaşabileceğiniz Kişiselleştirme araç çubuğunu kullanabilirsiniz. Kişiselleştirme araç çubuğu **Seçenekler** öğesinin Kişiselleştir grubunun altında, formun Eylem bölmesinde de bulunur. **Bu formu kişiselleştir** seçeneğini seçtiğinizde, Kişiselleştirme araç çubuğunu görürsünüz. 

[![Kişiselleştirmeye araç çubuğu](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Kişiselleştirme araç çubuğunda bir dizi kişiselleştirme eylemi bulunur. Pek çok öğenin özelliklerini bir kerede seçip değiştirmek istiyorsanız, **Seç** aracını seçin. İlk olarak, Seç aracına tıklayın ve sonra özelliklerini değiştirmek istediğiniz öğeye tıklayın. Bir öğe seçtiğinizde, öğenin özellik penceresi açılır ve o öğenin özelliklerini değiştirebilirsiniz. Formunuzda bulunan kişiselleştirilebilir diğer öğeler için işlemi yineleyebilirsiniz. Bazı durumlarda, bir öğe seçip bazı özelliklerin değiştirilebilir olmadığını görebilirsiniz. Bu durum geçerli öğenin kullanılış şekline göre Dynamics 365 for Operations'ın o özelliği değiştirmenize izin vermemesi anlamına gelir. Örneğin, gerekli bir alan gizlenemez. 

Bir öğeyi seçip mevcut öğeler grubu içinde farklı bir konuma taşımak istiyorsanız, **Taşı** aracını seçin. (Bir öğeyi ana grubunun dışına taşıyamazsınız). İlk olarak, Taşı aracına tıklayın ve sonra taşımak istediğiniz öğeye tıklayın. Taşımak istediğiniz öğeye tıkladığınızda, Dynamics 365 for Operations bu öğenin nereye taşınabileceğini anlamak ve öğeyi mevcut bir grup içinde sürükleyerek bırakabileceğiniz alanın yanında renkli, kalın bir çizgi olarak görülen "bırakma bölgeleri" serisi oluşturmak için formu tarar. 

Bir öğeyi seçip gizlemek için **Gizle** aracını seçin. Bir öğeyi gizlemek için Gizle aracını seçip gizlemek istediğiniz öğeye tıklamanız yeterlidir. Gizle aracını seçtiğinizde, o anda gizli durumdaki öğelerin tümü görünür hale gelir ve gölgeli bir kutucuk içinde gösterilir, böylece gizliliğini kaldıracağınız öğeyi seçebilirsiniz. Seçili öğeler gizlenmiş durumdayken sayfanın nasıl görüneceğini görmek için Seç aracını seçin. Hızlı Sekme özet alanında bir sayısal alan veya dize alanı gösterilmesini istiyorsanız, **Özet** aracını seçin. Özet aracı yalnızca Hızlı Sekme bölümü içinde yer alanlar için geçerli olacaktır. Özet aracını seçtiğinizde, Dynamics 365 for Operations özet alanları olarak seçilmiş tüm alanları gölgeli bir kutucuk içinde toplayarak gösterir. Alana tıklayarak bir Hızlı Sekme özetinden alanlarını etkileşimli olarak ekleyebilir ve kaldırabilirsiniz. 

Sayfanın klavye sekmesi sırasından bir öğeyi kaldırmak için **Atla** aracını seçin. Atla aracını seçtiğinizde, o anda atlanmış durumdaki tüm öğeler gölgeli bir kutucuk içinde gösterilir; böylece atlanmış bir öğeyi seçerek bunu tekrar öğe sırasının bir parçası haline getirmek üzere seçebilirsiniz. 

Bir öğeyi Düzenlenebilir veya Düzenlenemez olarak işaretlemek için **Düzenle** aracını seçin. Düzenle aracını seçtiğinizde, o anda düzenlenemez durumdaki öğelerin tümü gölgeli bir kutucuk içinde gösterilir, böylece düzenlenebilir hale getireceğiniz öğeyi seçebilirsiniz. Unutmayın, bazı alanlar gereklidir ve düzenlenemez durumuna getirilemez. Bu alanlar yanlarında bir asma kilit simgesi ile görüntülenir. 

Sayfanıza bir alan eklemek için **Ekle** aracını seçin. Ekle aracını kullanarak yeni bir alan oluşturamazsınız, bununla birlikte geçerli sayfa tanımının bir parçası olan, ancak sayfada gösterilmeyen alanlar ekleyebilirsiniz. Ekle aracını seçtiğinizde, önce bir alan eklemek istediğiniz grup veya alanı seçmeniz gerekir. Bir iletişim kutusu seçtiğiniz bölümle ilgili alanların listesini görüntüler. Bu iletişim kutusundan, eklemek için bir veya daha fazla alan seçip Ekle tuşuna tıklayın. Daha sonra, daha önce eklediğiniz bir alanı kaldırmak istiyorsanız, işlemi yineleyin, ancak yalnızca önceden eklediğiniz alanı temizleyin. 

Geçerli sayfaya ilişkin tüm kişiselleştirmelerle ilgili yönetim seçeneklerinin bir listesini görmek için **Yönet** düğmesini seçin. 

Sayfayı varsayılan, ilk yüklendiği durumuna sıfırlamak için **Temizle**'yi seçin. Geçerli sayfadaki tüm kişiselleştirmeler temizlenir. Geriye alma eylemi mümkün değildir, bu yüzden bu seçeneği sadece sayfanızı sıfırlamak istediğinize eminseniz kullanın. 

Sizin veya başka birinin bu sayfa için daha önce oluşturduğu bir kişiselleştirme dosyasından bir kişiselleştirme kullanmak için, **İçe aktar** düğmesini seçin. Bir kişiselleştirme içe aktarıldığında, tüm sayfada yaptığınız tüm kişiselleştirmeler temizlenecek ve yerine seçilen dosyadan gelen tüm kişiselleştirmeler kullanılacaktır. Bir kişiselleştirmeyi kaydetmek veya paylaşmak istiyorsanız, kişiselleştirmeleri bir dosyaya kaydetmek için **Dışa aktar** düğmesini seçin. 

Araç çubuğunu kapatmak ve sayfayı daha önceki interaktif durumuna geri getirmek için **Kapat** düğmesini seçin. 

Kişiselleştirme aracı ile, kaydetme örtülüdür. Kişiselleştirmeleriniz bunları yapar yapmaz hemen kullanıma girer ve ayrıca **Kaydet** düğmesine tıklamanız gerekmez. Bazı durumlarda, bir araç seçtiğinizde, öğenin yanında bir asma kilit simgesi görürsünüz. Bu simge, sayfanın doğru çalışması için seçilen araçla ilgili özellikleri değiştiremeyeceğinizi gösterir. Kişiselleştirme araç çubuğu açıldığında, sayfa etkileşimsiz hale gelir. Veri giremez veya bölümleri genişletip daraltamazsınız.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Açık kişiselleştirme: Çalışma alanına kutucuk veya liste ekleme
Listeler içeren bazı sayfalarda Seçenekler öğesinin Kişiselleştir grubunun altında, Eylem Bölmesi içinde, ek bir kişiselleştirme özelliği bulunacaktır. Size geçerli listedeki bilgileri (filtrelenmiş veya sıralanmış veya varsayılan) Çalışma alanında liste veya özet kutucukları (listedeki kalemlerin sayısını göstermek için kullanılabilir) halinde gösterebilme imkanı veren açılır listeyi açmak için **Çalışma Listesine Ekle** düğmesini seçin. 

[![Çalışma alanına ekle](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Bir listeyi çalışma alanına eklemek için, öncelikle bilgileri içeren listeyi çalışma alanınızda görmek istediğiniz şekilde sıralayıp filtreleyin ve sonra Çalışma Alanına Ekle iletişim kutusunu seçin. Ardından, istenen çalışma alanını seçin ve Sunu açılır listesinden **Liste** düğmesini seçin. **Liste** düğmesini seçtiğinizde, listede görmek istediğiniz sütunları seçmenize olanak veren bir iletişim kutusu ve o listeye ait, listenin çalışma alanında görüneceği etiket açılacaktır. 

Bir çalışma alanına kutucuk eklemek için, önce özetlenmesini istediğiniz (veya hızlı erişmek istediğiniz) verileri temsil etmek üzere listeyi filtreleyin. Sonra, Çalışma Alanına Ekle açılır iletişim kutusunu açın. Ardından, istenen çalışma alanını seçin ve Sunu açılır menüsünden **Kutucuk** düğmesini seçin. **Kutucuk** düğmesini seçtiğinizde, bir kutucuk etiketi sağlamanıza ve kutucuğun bir sayı gösterip göstermemesine karar vermenize olanak sunan bir iletişim kutusu açılır. Bir çalışma alanına yerleştirildiğinde, kutucuk size geçerli sayfayı çalışma alanından açma olanağı verir ve kutucukla ilgili bilgilerin listesini gösterir. 

Listeniz veya kutucuğunuz bir çalışma alanına eklendiğinde, daha sonra bu çalışma alanını açabilir ve liste ya da kutucuğu yerleştirildiği grup içinde yeniden düzenleyebilirsiniz.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Açık kişiselleştirme: Çalışma alanından bir özeti bir panoya ekleme
Bazı çalışma alanları panonuzda da görmek isteyebileceğiniz sayı kutucukları (içlerinde sayı bulunan kutucuklar) içerir. Bir çalışma alanında, sayı kutucuğu üzerine sağ tıklayın ve **Kişiselleştir** öğesini seçin. **Panoya Sabitle** öğesini seçin. Seçilen panoya bir dahaki gidişinizde (ve panoyu yenileyişinizde), o sayıyı panoda çalışma alanının gezinti kutucuğunun altında göreceksiniz.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Açık kişiselleştirme: Panonuzu kişiselleştirme
Pano genellikle Dynamics 365 for Operations'ı açtığınızda göreceğiniz ilk sayfadır. Panonuzu çalışma alanı gezinti kutucuklarını yeniden adlandıracak, sadece görmek istediğinizi kutucukları gösterecek, kutucukları yeniden adlandıracak veya kutucukları görmek istediğiniz sırada düzenleyecek şekilde kişiselleştirebilirsiniz. Panoyu kişiselleştirmek için herhangi bir kutucuğu seçin ve bağlam menüsünü açmak için sağ tıklayın. Bağlam menüsünde **Kişiselleştir** öğesini seçin. Seçilen kutucuk gizlemek ya da yeniden adlandırmak veya atlamak istediğiniz bir kutucuksa, bu değişikliği beliren Özellik penceresinde doğrudan yapabilirsiniz. Kutucukları düzenlemek istiyorsanız, Kişiselleştirme araç çubuğunu açmak için Özellik penceresinde **Bu formu kişiselleştir** öğesini seçin. Daha sonra kutucukları düzenlemek için Taşı Aracının kullanabilirsiniz.

## <a name="administration-of-personalization"></a>Kişiselleştirme yönetimi
Bir sayfayı kişiselleştirmek ve diğer kullanıcılarla paylaşmak mümkündür; bunun için sadece kişiselleştirilmiş sayfayı dışa aktarın ve diğer kullanıcılardan kişiselleştirilmiş sayfaya gelip oluşturduğunuz kişiselleştirme dosyasını içe aktarmalarını isteyin. Bir kullanıcının yönetici ayrıcalıkları varsa, bu kişi **Kişiselleştirme Kurulum** sayfasında diğer kullanıcılara ait kişiselleştirmeleri de yönetebilir. b sayfasına gidin. **Kişiselleştirme** sayfasında, biri **Sistem** ve biri de** Kullanıcı** olmak üzere iki öğe bulacaksınız. 

**Sistem:** Burada sistemdeki tüm kişiselleştirmeleri geçici olarak devre dışı bırakabilir veya "kapatabilirsiniz". Bunu yapmak kişiselleştirmeleri silmez, bunun yerine tüm formları varsayılan durumlarına sıfırlar. Kişiselleştirmeler, daha sonra tümü her bir kullanıcı formuna yeniden uygulanacak şekilde yeniden etkinleştirilebilir. Tüm kullanıcılar için tüm kişiselleştirmeleri de silebilirsiniz. Kişiselleştirmeleri sildiğinizde, bunları sistemden otomatik olarak yeniden etkinleştirmenin hiçbir yolu olmadığını unutmayın. Bu adımı gerçekleştirmeden önce, daha sonra içe aktarmak isteyebileceğiniz kişiselleştirmeleri dışa aktardığınıza emin olun. 

**Kullanıcılar:** Burada kullanıcıların örtülü veya açık kişiselleştirmeler yapıp yapamayacağına karar verebilirsiniz. Ayrıca, her kullanıcının belli bir form üzerinde örtülü veya açık kişiselleştirme yapıp yapamayacağına da karar verebilirsiniz. Son olarak, her kullanıcı için bir kişiselleştirmeyi içe aktarabilir, dışa aktarabilir veya silebilirsiniz. 

**Not:** İlk sürümünde, kişiselleştirme idaresi sadece kullanıcıya göre yönetime izin verir.




