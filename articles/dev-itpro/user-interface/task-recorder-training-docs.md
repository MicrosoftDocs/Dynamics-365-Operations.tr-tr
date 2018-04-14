---
title: "Görev kayıtlarını kullanarak belgeler veya eğitim oluşturma"
description: "Bu konuda, Görev kaydedici ve görev kılavuzlarının neler olduğu, görev kayıtlarının nasıl oluşturulacağı ve Microsoft görev kılavuzlarının özelleştirilip bunların Yardım bölümünüze nasıl ekleneceği açıklanmaktadır."
author: josaw1
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 9550faec1bbbdc233631e149c09b8e4faf25f5ff
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="create-documentation-or-training-using-task-recordings"></a>Görev kayıtlarını kullanarak belgeler veya eğitim oluşturma

[!INCLUDE [banner](../includes/banner.md)]

Bu konuda, Görev kaydedici ve görev kılavuzlarının neler olduğu, görev kayıtlarının nasıl oluşturulacağı ve Microsoft görev kılavuzlarının özelleştirilip bunların Yardım bölümünüze nasıl ekleneceği açıklanmaktadır.

> [!IMPORTANT]
> Dynamics 365 for Talent için kendi görev kılavuzlarınızı kaydedebilirsiniz ancak bunları İş Süreci Modelleyici (BPM) kitaplığına kaydedemez veya Yardım bölmesinden açamazsınız. Bunları yerel olarak veya ağ konumuna kaydedebilir ve daha sonra Görev kaydediciyi kullanarak açabilir ve oynatabilirsiniz. 

<a name="learn-about-task-recorder"></a>Görev kaydedici hakkında bilgi edinin
-------------------------

Görev kaydedici, ürün kullanıcı arabiriminde (UI) gerçekleştirdiğiniz eylemleri kaydetmek için kullanabileceğiniz bir araçtır. Görev kaydediciyi kullandığınızda, kullanıcı arabiriminde gerçekleştirdiğiniz tüm olaylar sunucuda yürütülür —değer ekleme, ayarları değiştirme, veri kaldırma dahil olmak üzere— yakalanır. Kaydettiğiniz tüm adımlar toplu olarak *görev kaydı* olarak adlandırılır. Görev kayıtları birçok şekilde kullanılabilir:

-   **Görev kayıtları görev kılavuzları olarak oynatılabilir.** Görev kılavuzları Yardım deneyiminin ayrılmaz bir parçasıdır. Bir görev kılavuzu size bir iş sürecinin adımları boyunca yol gösteren denetimli, destekli, etkileşimli bir deneyimdir. Kullanıcı kullanıcı arabirimi ve kullanıcının etkileşim kurması gereken kullanıcı arayüzü öğesinde oynatılacak bir açılır pencere istemi (veya "kabarcık) yoluyla her adımı tamamlaması için yönlendirilir. "Kabarcık," öğe ile nasıl etkileşime girileceği hakkında bilgi de sağlar ("Buraya tıklayın" veya "Bu alana bir değer girin" gibi). Bir görev kılavuzu, kullanıcının geçerli veri kümesine göre çalışır ve girilen veriler kullanıcının ortamına kaydedilir.
-   **Görev kayıtları Yardım bölmesinde prosedür adımları olarak görüntülenebilir.** Yardım bölmesini görev kayıtlarını aramak ve görüntülemek için kullanabilirsiniz. Yardım Bölmesine **?** simgesine tıklayarak (üst gezinti çubuğundadır) veya **Ctrl + Shift +?** kısayol tuş bileşimini kullanarak erişebilirsiniz. Bir görev kaydının adımlarını Yardım bölmesinde okuyabilirsiniz veya size kullanıcı arabirimi ile aracılık etmesi için kaydı bir görev kılavuzu olarak oynatabilirsiniz.
-   **Görev kayıtları BPM'ye kaydedilebilir.** Görev kaydınızı Lifecycle Services'taki (LCS) BPM kitaplığındaki bir hiyerarşi satırına kaydedebilirsiniz. Kayıttan bir adım listesi ve bir iş süreci akış çizelgesi oluşturulur. BPM kitaplığına kaydedilen görev kayıtları Yardım olarak gösterilebilir.
-   **Görev kayıtları Word belgeleri olarak kaydedilebilir.** Bu kolaylıkla, yazdırılabilir eğitim kılavuzları üretmenizi sağlar.

Kendi görev kayıtlarınızı oluşturabilir, Microsoft tarafından sağlanan görev kayıtlarını oynatabilir veya yapılandırmanızı yansıtmak için Microsoft tarafından sağlanan görev kayıtlarını değiştirebilirsiniz. Görev kaydedici hakkında daha fazla bilgi için bkz. [Görev kaydedici](task-recorder.md)

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
-   Bir görev kaydındaki her adım için, ek açıklamalar oluşturabilirsiniz. Bir görev kılavuzunun oynatımı sırasında, adımlar için metnin üstünde ve altında not olarak "kabarcık" içinde ek açıklamalar görünür. Yardım bölmesinde bir metin olarak görüntülendiğinde, ek açıklamalar adım içinde metin satır içi olarak görünür. Açıklamada olduğu gibi, ek açıklamaları da ayrı bir dosyaya yazmak ve kaydetmek iyi bir fikirdir. Görev kaydını kaydederken, bu belgedeki ek açıklamaları kesin ve yapıştırın.

**Farklı ek açıklama türlerini anlamak** Tüm ek açıklamalar isteğe bağlıdır. Bunları yalnızca kullanıcı için yararlı bilgiler sağlayacağı zaman ekleyin.

-   **Başlık**: Görev kaydedicinin otomatik olarak oluşturduğu adım metninden önce başlık ek açıklaması görünür. Görev kılavuzunda başlık ek açıklaması otomatik olarak oluşturulan metnin yukarısında görünür. Kullanıcının adımı neden yaptığını açıklamak veya ek bağlam sağlamak için bu tür ek açıklama kullanın.

Bu, kayıt oluştururken bir ek açıklama eklediğinizde gördüğünüz düzenleme bölmesidir. **Başlık** kutusuna bir başlık ek açıklaması girin. 

[![ekran1](./media/screen1.png)](./media/screen1.png) 

Görev kılavuzunda "kabarcığında" başlık ek açıklaması bu şekilde görünür. 

[![ekran2](./media/screen2.png)](./media/screen2.png)

-   **Notlar:** Görev kaydedicinin otomatik olarak oluşturduğu adım metninden sonra not ek açıklaması görünür. Görev kılavuzunda ancak kullanıcı görev kılavuzu kabarcığındaki **daha fazla göster** linkine tıkladığında görülebilir. Bu tür ek açıklamayı bir kullanıcının adımı tamamlaması için bilmesi gereken her şeyi açıklamak için kullanın.

Bu, kayıt oluştururken bir ek açıklama eklediğinizde gördüğünüz düzenleme bölmesidir. **Notlar** kutusuna bir not ek açıklaması girin. 

[![ekran3](./media/screen3.png)](./media/screen3.png) 

Görev kılavuzundaki "kabarcıkta" not ek açıklaması bu şekilde görünür.

[![ekran4](./media/screen4.png)](./media/screen4.png)

-   **Bilgi adımı**: Bu ek açıklamalar bir denetime veya bir formdaki herhangi bir yere sağ tıklayıp &lt; **Görev Kaydedici** &lt; **Bilgi adımı ekle'ye tıklayarak oluşturulur. **Bilgi adımları, kullanıcı arabirimine herhangi bir işlem kaydedilmemiş olsa bile, eklediğiniz noktada numaralı adım olarak görünür. Bir form düzeyi bilgi adımı veya bir denetimle ilişkilendirilmiş bir bilgi adımı ekleyebilirsiniz. Bir bilgi adımı bir formla ilişkilendirildiğinde, görev kılavuzu oynatıldığında, formun herhangi bir yerinde işaretçi olmaksızın görev kılavuzu "kabarcığı" görünecektir. Bir bilgi adımı bir denetimle ilişkilendirildiğinde, görev kılavuzu oynatıldığı zaman, görev kılavuzu "kabarcığı" denetimi gösterir. Yardım bölmesinde, bir bilgi adımı ek açıklaması, girdiğiniz metni içeren numaralı bir adım olarak görünür. Kullanıcıyı sonraki adımlara hazırlamak, Microsoft Dynamics 365 for Finance and Operations dışında yapılması gereken adımları açıklamak veya diğer kayıtlara başvurmak için bilgi adımlarını kullanın (ancak ek açıklamalarda köprüler oluşturamazsınız.).

**Kaydınızın süresini belirleyin**

-   Kullanıcı genellikle kaydı ya başından sonuna okuyacak ya da oynatacaktır, bu nedenle ayrı ayrı yapılması daha iyi olan adımları veya görevleri birleştirmeyin.
-   Birden çok alt işleme yayılan uzun bir senaryo kaydetmemeye çalışın. Örneğin, "Operate mağaza müşteri servis masasına" çok geniş olan; "Kabul et döner" ve "Ekle Hediye kartı" gibi kısa görevler halinde bölmek
-   Bir görev birden fazla iş sürecinin bir parçası olarak yürütülebiliyorsa, bunun için ayrı bir kayıt oluşturun ve böylece diğer kayıtlarda ona başvurabilirsiniz.
-   İşlem kişinin büyük olasılıkla aynı anda yaptığı birden çok görevi içeriyorsa, görevleri bir kayıtta tutabilirsiniz, örneğin, "İşlevsellik profilleri ayarlama ve atama."
-   Eğer kişinin bir kez yapıp (yapılandırma gibi) ve hemen sonrasında yapabileceği ama tekrar tekrar ve tek başına yapabileceği başka bir görev söz konusuysa, onları iki görev kaydına bölün.

**Bir kaydı başlatmak için kullanıcı arabiriminde nerede olacağına karar verme** Bir görev kaydını başlattığınız sırada bulunduğunuz sayfa, görev kılavuzunun hangi sayfa için görüntüleneceğini belirler. Örneğin, bir kullanıcı Genel muhasebe parametreleri sayfasında Yardım'a tıkladığında görev kaydınızın Yardım bölmesinde listelenmesini istiyorsanız, kaydınızı Genel muhasebe parametreleri sayfasında başlatmanız gerekir. **Kayıtları .axtr dosyaları olarak kaydetme** Bir görev kaydı oluşturmayı veya düzenlemeyi bitirdiğinizde, onu karşıdan nasıl yüklemek veya kaydı nasıl kaydetmek istediğinizle ilgili birkaç seçenek sunulur. Dosyayı bir görev kaydı paketi (.axtr) olarak yükleyebilir, ham bir kayıt dosyası (.xml) olarak yükleyebilir, bir Word belgesi olarak yükleyebilir veya dosyayı bir LCS kitaplığına kaydedebilirsiniz. Görev kaydınızı bir görev kaydı paket dosyası (.axtr) olarak kaydetmek her zaman iyi bir fikirdir. Bu, daha sonra yordamları veya ek açıklamaları değiştirmek istediğinizde dosyanın bakımını kolaylaştırır. Dosyayı bir Word belgesi olarak karşıdan yüklemek isterseniz, onu ayrıca bir görev kaydı paket dosyası olarak kaydedin.

## <a name="create-your-task-recording"></a>Görev kaydınızı oluşturun
Adımları ayrıntılı olarak incelemek için bkz. [Bir görev kaydı nasıl oluşturulur](task-recorder.md)

## <a name="copy-and-customize-microsofts-task-recordings"></a>Microsoft'un görev kayıtlarını kopyalayın ve özelleştirin
Microsoft'un görev kayıtlarını kendi Yardım belgeniz veya eğitim malzemeleriniz için kullanmak için karşıdan yükleyebilir ve düzenleyebilirsiniz. Bir Microsoft görev kaydını karşıdan yüklemek için şu adımları izleyin:

1.  Görev kaydediciyi açın. Görev kaydedicisi **Ayarlar** menüsünde bulunur.
2.  Görev Kaydedici bölmesinde **Bir kaydı koruyun.** tıklayın
3.  **Kayıt nerede** altında,'ı **Bir LCS kitaplığında yer alan** tıklayın
4.  **LCS kitaplığını seçin** tıklayın.
5.  Microsoft genel kitaplığını seçin.
6.  Ağaçta, görev kaydının ilişkilendirildiği iş süreci kitaplığı düğümünü seçin.
7.  **Tamam** düğmesine tıklayın.
8.  **Başlat**'a tıklayın.
9.  Bu noktada, kaydı adım adım geçin ve yeniden kaydederken her adımda değişiklikler yapın. **Not**: Bir kaydın yalnızca metnini değiştirmek istiyorsanız, kaydı **Bir kaydın ek açıklamalarını düzenle** modunda açabilir ve sonra kaydedebilirsiniz.
10. Kayıt sonuna kadar oynatıldıktan sonra, ekranın en üstündeki görev kaydedici çubuğundaki **Durdur'u** tıklayın.
11. Görev kaydını nasıl kaydetmek istediğinizi seçin.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Görev kayıtlarınızı Yardım bölmesine ekleme
Görev kayıtlarınızın görev kılavuzları olarak oynatılabilmesi veya metin olarak görüntülenebilmesi için onları Yardım bölmesinde göstermek için, görev kayıtlarınızı kendi BPM kitaplığınıza kaydetmelisiniz ve sonra Yardım sistemi parametrelerinizi BPM kitaplığınıza işaret edecek şekilde güncelleştirmelisiniz. Daha fazla bilgi için bkz. [Yardım sistemine bağlanma](../../fin-and-ops/get-started/help-connect.md)

<a name="see-also"></a>Ayrıca bkz.
--------

[Yardıma genel bakış](../../fin-and-ops/get-started/help-overview.md)

[Yardım'a bağlanma](../../fin-and-ops/get-started/help-connect.md)

[Görev Kaydedici](task-recorder.md)

[Görev Kaydediciyle Zengin Yardım Konuları Oluşturma (dış bağlantı)](https://mbspartner.microsoft.com/AX/Videos/970)

