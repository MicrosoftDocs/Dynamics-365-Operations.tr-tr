---
title: "Görev kayıtlarını kullanarak belgeler veya eğitim oluşturma"
description: "Bu konu, hangi görev kaydedici ve görev kılavuzları, görev kayıtları oluşturmak nasıl olduğunu ve Microsoft görevi özelleştirmek nasıl rehberlik eder ve onları Yardım&quot;ınıza eklemek açıklar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 38bce4a843f0db575c8d1ba08b7dc2ece8366663
ms.lasthandoff: 03/31/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Görev kayıtlarını kullanarak belgeler veya eğitim oluşturma
Bu konu, hangi görev kaydedici ve görev kılavuzları, görev kayıtları oluşturmak nasıl olduğunu ve Microsoft görevi özelleştirmek nasıl rehberlik eder ve onları Yardım'ınıza eklemek açıklar.

<a name="learn-about-task-recorder"></a>Görev kaydedici hakkında bilgi edinin
-------------------------

Görev Kaydedicisi Microsoft Dynamics 365 ürün kullanıcı arabiriminde (UI) ele eylemleri kaydetmek için kullanabileceğiniz işlemleri aracı için olur. Görev kaydediciyi kullandığınızda, kullanıcı arabiriminde gerçekleştirdiğiniz tüm olaylar sunucuda yürütülür —değer ekleme, ayarları değiştirme, veri kaldırma dahil olmak üzere— yakalanır. Kaydettiğiniz tüm adımlar toplu olarak *görev kaydı* olarak adlandırılır. Görev kayıtları birçok şekilde kullanılabilir:

-   **Görev kayıtları görev kılavuzları olarak oynatılabilir.** Görev kılavuzları Dynamics 365 işlemleri Yardım deneyimi ayrılmaz bir parçası olan. Görev Kılavuzu, iş süreci adımları boyunca kontrollü, Destekli, etkileşimli bir deneyimdir. Kullanıcı kullanıcı arabirimi ve kullanıcının etkileşim kurması gereken kullanıcı arayüzü öğesinde oynatılacak bir açılır pencere istemi (veya "kabarcık) yoluyla her adımı tamamlaması için yönlendirilir. "Kabarcık" öğe ile "burayı tıklatın" veya "Bu alana bir değer girin." gibi etkileşim hakkında bilgi de sağlar. Görev kılavuzu kullanıcının geçerli veri kümesi karşı çalışır ve kullanıcının ortamında girilen veriler kaydedilir.
-   **Görev kayıtları yordam adımları Yardım Bölmesi'nde görüntülenebilir.** Yardım Bölmesi, aramak ve görev kayıtlarını görüntülemek için kullanabilirsiniz. Yardım Bölmesi'i tıklatarak erişebileceğiniz **?** Veya, üst gezinti çubuğu simgesini kısayol tuş bileşimini kullanabilirsiniz **Ctrl + Shift +?**. Yardım Bölmesi'nde kaydı görevin adımları okuyabilir veya kullanıcı Arabirimi aracılığıyla rehberlik eder şekilde görev kılavuz olarak kaydý çalmak göndermemeyi seçebilirsiniz.
-   **Görev kayıtları BPM'ye kaydedilebilir.** Görev kaydınızı Lifecycle Hizmetleri'ndeki (LCS) İş Süreci Modeli'ndeki (BPM) bir hiyerarşi sırasına kaydedebilirsiniz. Kayıttan bir adım listesi ve bir iş süreci akış çizelgesi oluşturulur. BPM kitaplığa kaydedilen görev kayıtları Dynamics 365 Yardım gibi işlemler için de gösterilebilir.
-   **Görev kayıtları Word belgeleri olarak kaydedilebilir.** Bu kolaylıkla, yazdırılabilir eğitim kılavuzları üretmenizi sağlar.

Kendi görev kayıtları oluşturma, Microsoft tarafından sağlanan görev kayıtlarını çalmak veya yapılandırmanızı yansıtmak için Microsoft tarafından sağlanan görev kayıtlarını değiştirin. Görev Kaydedicisi hakkında daha fazla bilgi için bkz: [Dynamics 365 görev Kaydedicisi işlemleri için](task-recorder.md).

## <a name="plan-your-task-recording"></a>Görev kaydınızı planlayın
Yeni bir görev kaydı oluştururken veya kaydınızı bir Microsoft görev kaydına bağlarken, aşağıdaki bilgileri göz önünde bulundurun.

-   Kaydınızı bir video gibi planlayın. Önceden tüm kararlarınızı alın.
-   Adımları anlamak için iş sürecini kayıt yapmadan bir iki kez uygulayın.
-   Kayıt yapmadan önce süreci uygularken, kısayol tuşlarını veya **Anahtarı** girin'i nerede kullandığınıza dikkat edin, böylece onları gerçek kayıt sırasında kullanmaktan kaçınabilirsiniz.
-   Şunları tanımlayın:
    -   Adımları alt görevler ile gruplamak istiyor musunuz? Alt görevler bir işlemin bölümlerin, görsel olarak ayırır. Örneğin, "Bir ürün oluşturma ve serbest bırakma" için bir kayıt oluşturuyorsanız, bir ürün oluşturmak için gerekli adımları gruplamak ve ardından bir ürünü serbest bırakmak için gerekli adımları gruplamak isteyebilirsiniz. Alt görevler ayrıca uzun işlemlerin okunmasını kolaylaştırır.
    -   Ek açıklamalar mı eklemek istiyorsunuz ve bu öyleyse, nereye? Daha fazla bilgi için aşağıdaki "Farklı ek açıklama türlerini anlamak"a bakınız.
    -   İş sürecinin adımlarını tamamlarken farklı alanlara hangi değerleri ekleyeceksiniz? Kayıt yaparken geri dönmemek veya hataları düzeltmemek için ilerlerken ne seçeceğinizi veya gireceğinizi bilmek iyi bir fikirdir.

**Açıklama ve ek açıklamaları önceden yazın**

-   Her görev kaydının başında, kayda bir giriş girmenizi sağlayan bir açıklama alanı vardır. Kayıt yaparken kopyalayıp yapıştırabilmeniz için açıklamayı önceden ayrı bir belgeye yazmak ve kaydetmek iyi bir fikirdir. Bu şekilde, kayıt işlemi sırasında olmadığınız zamanlarda metni düzeltmeye zaman ayırabilirsiniz. Metni kesip yapıştırmak kayıt işleminin daha hızlı ve sorunsuz olmasını sağlar.
-   Bir görev kaydındaki her adım için, ek açıklamalar oluşturabilirsiniz. Bir görev kılavuzunun oynatımı sırasında, adımlar için metnin üstünde ve altında not olarak "kabarcık" içinde ek açıklamalar görünür. Yardım Bölmesi'nde metin olarak görüntülendiğinde adımdaki metni satır içi olarak ek açıklamalar görünür. Açıklamada olduğu gibi, ek açıklamaları da ayrı bir dosyaya yazmak ve kaydetmek iyi bir fikirdir. Görev kaydını kaydederken, bu belgedeki ek açıklamaları kesin ve yapıştırın.

**Farklı ek açıklama türlerini anlamak** Tüm ek açıklamalar isteğe bağlıdır. Bunları yalnızca kullanıcı için yararlı bilgiler sağlayacağı zaman ekleyin.

-   **Başlık**: Kaydedici otomatik olarak görev adım metin oluşturmadan önce bir başlık ek açıklama görüntülenir. Görev Kılavuzu'nda başlık ek açıklamayı otomatik olarak oluşturulan metnin üstünde görünür. Kullanıcının adımı neden yaptığını açıklamak veya ek bağlam sağlamak için bu tür ek açıklama kullanın.

Bu, kayıt oluştururken bir ek açıklama eklediğinizde gördüğünüz düzenleme bölmesidir. **Başlık** kutusuna bir başlık ek açıklaması girin. 

[![Ekran 1](./media/screen1.png)](./media/screen1.png) 

Görev kılavuzunda "kabarcığında" başlık ek açıklaması bu şekilde görünür. 

[![ekran2](./media/screen2.png)](./media/screen2.png)

-   **Notlar:** Görev kaydedicinin otomatik olarak oluşturduğu adım metninden sonra not ek açıklaması görünür. Görev kılavuzunda ancak kullanıcı görev kılavuzu kabarcığındaki **daha fazla göster** linkine tıkladığında görülebilir. Bu tür ek açıklamayı bir kullanıcının adımı tamamlaması için bilmesi gereken her şeyi açıklamak için kullanın.

Bu, kayıt oluştururken bir ek açıklama eklediğinizde gördüğünüz düzenleme bölmesidir. **Notlar **kutusuna bir not ek açıklaması girin. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

Not ek açıklama nasıl görev Kılavuzu'nda "Kabarcık" olarak göründüğünü budur.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Adım bilgi**: Bu ek açıklamalar sağ bir denetim veya herhangi bir form tıklatılarak oluşturulur &lt;**Görev Kaydedici**&lt; ** bilgi adım Ekle. ** Hiçbir eylem kullanıcı arabiriminde kaydedildiği halde bilgi adımları herhangi bir noktada, eklemeden bir numaralı adımı olarak görünür. Bir form düzeyi bilgi adımı veya bir denetimle ilişkilendirilmiş bir bilgi adımı ekleyebilirsiniz. Bir bilgi adımı bir formla ilişkilendirildiğinde, görev kılavuzu oynatıldığında, formun herhangi bir yerinde işaretçi olmaksızın görev kılavuzu "kabarcığı" görünecektir. Info adım bir denetimle ilişkili olduğunda görev Kılavuzu "Kabarcık" görev Kılavuzu çalındığında denetime işaret edecektir. Yardım Bölmesi'nde, girdiğiniz herhangi bir metni ek açıklama bilgisi adım numaralandırılmış bir adım olarak görünecektir. Kullanıcı işlemleri için Dynamics 365 dışında yapılması veya diğer kayıtları için (hyperinks ek açıklamalar oluşturamazsınız. rağmen) başvurmak için gereken adımları açıklamak için sonraki adımlar için hazırlamak için bilgi adımları kullanın.

**Kaydınızın süresini belirleyin**

-   Kullanıcı genellikle kaydı ya başından sonuna okuyacak ya da oynatacaktır, bu nedenle ayrı ayrı yapılması daha iyi olan adımları veya görevleri birleştirmeyin.
-   Birden çok alt işleme yayılan uzun bir senaryo kaydetmemeye çalışın. Örneğin, "Operate mağaza müşteri servis masasına" çok geniş olan; "Kabul et döner" ve "Ekle Hediye kartı" gibi kısa görevler halinde bölmek
-   Bir görev birden fazla iş sürecinin bir parçası olarak yürütülebiliyorsa, bunun için ayrı bir kayıt oluşturun ve böylece diğer kayıtlarda ona başvurabilirsiniz.
-   İşlem kişinin büyük olasılıkla aynı anda yaptığı birden çok görevi içeriyorsa, görevleri bir kayıtta tutabilirsiniz, örneğin, "İşlevsellik profilleri ayarlama ve atama."
-   Eğer kişinin bir kez yapıp (yapılandırma gibi) ve hemen sonrasında yapabileceği ama tekrar tekrar ve tek başına yapabileceği başka bir görev söz konusuysa, onları iki görev kaydına bölün.

**Kaydı başlatmak için kullanıcı arabiriminde nerede karar** hangi sayfa için görev kılavuzu görüntülenir görev kayıt kaydı başlattığınızda bulunduğunuz sayfayı etkiler. Örneğin, genel muhasebe parametreleri sayfasında Yardım kullanıcı tıklattığında Yardım Bölmesi'nde listelenecek, görev kaydı istiyorsanız, kaydınızı genel muhasebe parametreleri sayfasında başlamalıdır. **Kayıtları .axtr dosyaları olarak kaydetme** Bir görev kaydı oluşturmayı veya düzenlemeyi bitirdiğinizde, onu karşıdan nasıl yüklemek veya kaydı nasıl kaydetmek istediğinizle ilgili birkaç seçenek sunulur. Dosyayı bir görev kaydı paketi (.axtr) olarak yükleyebilir, ham bir kayıt dosyası (.xml) olarak yükleyebilir, bir Word belgesi olarak yükleyebilir veya dosyayı bir LCS kitaplığına kaydedebilirsiniz. Görev kaydınızı bir görev kaydı paket dosyası (.axtr) olarak kaydetmek her zaman iyi bir fikirdir. Bu, daha sonra yordamları veya ek açıklamaları değiştirmek istediğinizde dosyanın bakımını kolaylaştırır. Dosyayı bir Word belgesi olarak karşıdan yüklemek isterseniz, onu ayrıca bir görev kaydı paket dosyası olarak kaydedin.

## <a name="create-your-task-recording"></a>Görev kaydınızı oluşturun
Ayrıntılı gözden geçirme adımları için bkz [görev kaydı oluşturmak nasıl](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Microsoft'un görev kayıtlarını kopyalayın ve özelleştirin
Karşıdan yükleme ve kendi Yardım belgelerine veya eğitim malzemeleri kullanmak için Microsoft'un görev kayıtları düzenleyin. Bir Microsoft görev kaydını karşıdan yüklemek için şu adımları izleyin:

1.  İşlemler için Dynamics 365 içinde görev Kaydedicisi'ni açın. Görev kaydedicisi **Ayarlar** menüsünde bulunur.
2.  Görev Kaydedici bölmesinde **Bir kaydı koruyun.**tıklayın
3.  **Kayıt nerede**altında,'ı **Bir LCS kitaplığında yer alan** tıklayın
4.  **LCS kitaplığını seçin** tıklayın.
5.  Microsoft Genel kitaplığı seçin.
6.  Ağaçta, görev kaydının ilişkilendirildiği iş süreci kitaplığı düğümünü seçin.
7.  **Tamam** düğmesine tıklayın.
8.  **Başlat**'a tıklayın.
9.  Bu noktada, adım aracılığıyla yeniden kaydetmek için adım adım adımlar değiştirme kayıt. **Not**: sadece kayıt metni değiştirmeniz gerekirse, kayıtta açmak **kayıt 's ek açıklamaları düzenleme** modu ve kaydedin.
10. Kayıt sonuna kadar oynatıldıktan sonra, ekranın en üstündeki görev kaydedici çubuğundaki**Durdur'u** tıklayın.
11. Görev kaydını nasıl kaydetmek istediğinizi seçin.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Yardım Bölmesi'nde görev kayıtlarınızı içerir
Böylece bunlar görev kılavuzları çalınma veya metin olarak görüntülenen Yardım Bölmesi'nde, kendi özel görev kayıtları göstermek için görev kayıtlarınızı kendi BPM kitaplığına kaydedin ve sonra Yardım sistem parametrelerinizi BPM Kitaplığı'na işaret edecek şekilde güncelleştirin. Daha fazla bilgi için bkz: [Yardım sistemine bağlayın.](../get-started/help-connect.md)

<a name="see-also"></a>Ayrıca bkz.
--------

[Dynamics 365 işlemleri için Yardım](..\get-started\help-overview.md)

[Yardım Bağlan](..\get-started\help-connect.md)

[İşlemler için Dynamics 365 Görev Kaydedici](task-recorder.md)

[En son eklenen görev Kaydedicisi Özellikleri](\core\get-started\recently-added-editing-features-in-task-recorder)

[Dynamics AX dahilinde ömrü (dış bağlantı) görev Kaydedicisi'ni kullanarak hizmetleri için yeni eğitim kitaplıkları oluşturma](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

[Görev Kaydedicisi (dış bağlantı) ile zengin Yardım konuları oluşturmak](https://mbspartner.microsoft.com/AX/Videos/970)


