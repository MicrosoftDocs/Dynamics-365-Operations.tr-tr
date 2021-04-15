---
title: Görev Kaydedici'yle belge veya eğitim oluşturma
description: Bu konuda, Görev kaydedici ve görev kılavuzlarının neler olduğu, kayıtların nasıl oluşturulacağı ve Microsoft görev kılavuzlarının özelleştirilip bunların Yardım bölümünüze nasıl ekleneceği açıklanmaktadır.
author: josaw1
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b0be27fc759c525dcc1ffe4f2717b2e2378c52a5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744175"
---
# <a name="create-documentation-or-training-with-task-recorder"></a>Görev Kaydedici'yle belge veya eğitim oluşturma

[!include [banner](../includes/banner.md)]

Bu konuda, Görev kaydedici ve görev kılavuzlarının neler olduğu, görev kayıtlarının nasıl oluşturulacağı ve Microsoft görev kılavuzlarının özelleştirilip bunların Yardım bölümünüze nasıl ekleneceği açıklanmaktadır.

> [!IMPORTANT]
> Dynamics 365 Human Resources için kendi görev kılavuzlarınızı kaydedebilirsiniz ancak bunları İş Süreci Modelleyici (BPM) kitaplığına kaydedemez veya Yardım bölmesinden açamazsınız. Bunları yerel olarak veya ağ konumuna kaydedebilir ve daha sonra Görev kaydediciyi kullanarak açabilir ve oynatabilirsiniz. 

<a name="learn-about-task-recorder"></a>Görev kaydedici hakkında bilgi edinin
-------------------------

Görev kaydedici, ürün kullanıcı arabiriminde (UI) gerçekleştirdiğiniz eylemleri kaydetmek için kullanabileceğiniz bir araçtır. Görev kaydediciyi kullandığınızda, kullanıcı biriminde gerçekleştirdiğiniz ve sunucuda yürütülen tüm olaylar yakalanır. Bunlara değer ekleme, ayarları değiştirme ve veri kaldırma da dahildir. Kaydettiğiniz tüm adımlar toplu olarak *görev kaydı* olarak adlandırılır. Görev kayıtları birçok şekilde kullanılabilir:

-   **Görev kayıtları görev kılavuzları olarak oynatılabilir.** Görev kılavuzları Yardım deneyiminin ayrılmaz bir parçasıdır. Görev kılavuzu size bir iş sürecinin adımları boyunca yol gösteren denetimli, destekli, etkileşimli bir deneyimdir. Kullanıcı kullanıcı arabirimi ve kullanıcının etkileşim kurması gereken kullanıcı arabirimi öğesinde oynatılacak bir açılır pencere istemi (veya "balon") yoluyla her adımı tamamlaması için yönlendirilir. "Balon", öğeyle nasıl etkileşime girileceği hakkında bilgi de sağlar (ör. "Buraya tıklayın" veya "Bu alana bir değer girin"). Görev kılavuzu, kullanıcının geçerli veri kümesine göre çalışır ve girilen veriler kullanıcının ortamına kaydedilir.
-   **Görev kayıtları Word belgeleri olarak kaydedilebilir.** Bu kolaylıkla, yazdırılabilir eğitim kılavuzları üretmenizi sağlar.

Kendi görev kayıtlarınızı oluşturabilir, Microsoft tarafından sağlanan görev kayıtlarını oynatabilir veya yapılandırmanızı yansıtmak için Microsoft tarafından sağlanan görev kayıtlarını değiştirebilirsiniz. Görev kaydedici hakkında daha fazla bilgi için bkz. [Görev kaydedici](task-recorder.md).

## <a name="plan-your-task-recording"></a>Görev kaydınızı planlayın
Yeni bir görev kaydı oluştururken veya kaydınızı bir Microsoft görev kaydına bağlarken, aşağıdaki bilgileri göz önünde bulundurun.

-   Kaydınızı bir video gibi planlayın. Önceden tüm kararlarınızı alın.
-   Adımları anlamak için iş sürecini kayıt yapmadan bir iki kez uygulayın.
-   Kayıt yapmadan önce süreci uygularken, kısayol tuşlarını veya **Anahtarı** girin'i nerede kullandığınıza dikkat edin, böylece onları gerçek kayıt sırasında kullanmaktan kaçınabilirsiniz.
-   Şunları tanımlayın:
    -   Adımları alt görevler ile gruplamak istiyor musunuz? Alt görevler bir işlemin bölümlerini görsel olarak ayırır. Örneğin, "Bir ürün oluşturma ve kullanıma sunma" için bir kayıt oluşturuyorsanız, ürün oluşturmak için gerekli adımları gruplandırmak ve ardından bir ürünü kullanıma sunma için gerekli adımları gruplandırmak isteyebilirsiniz. Alt görevler ayrıca uzun işlemlerin okunmasını kolaylaştırır.
    -   Ek açıklamalar mı eklemek istiyorsunuz ve bu öyleyse, nereye? Daha fazla bilgi için aşağıdaki "Farklı ek açıklama türlerini anlamak"a bakınız.
    -   İş sürecinin adımlarını tamamlarken farklı alanlara hangi değerleri ekleyeceksiniz? Kayıt yaparken geri dönmemek veya hataları düzeltmemek için ilerlerken ne seçeceğinizi veya gireceğinizi bilmek iyi bir fikirdir.

**Açıklama ve ek açıklamaları önceden yazın**

-   Her görev kaydının başında, kayda bir giriş girmenizi sağlayan bir açıklama alanı vardır. Kayıt yaparken kopyalayıp yapıştırabilmeniz için açıklamayı önceden ayrı bir belgeye yazmak ve kaydetmek iyi bir fikirdir. Bu şekilde, kayıt işlemi sırasında olmadığınız zamanlarda metni düzeltmeye zaman ayırabilirsiniz. Metni kesip yapıştırmak kayıt işleminin daha hızlı ve sorunsuz olmasını sağlar.
-   Bir görev kaydındaki her adım için, ek açıklamalar oluşturabilirsiniz. Bir görev kılavuzunun oynatımı sırasında, adımlar için metnin üstünde ve altında not olarak "balon" içinde ek açıklamalar görünür. Ek açıklamalar, Yardım bölmesinde metin olarak görüntülendiğinde adım içinde metin satır içi olarak görünür. Açıklamada olduğu gibi, ek açıklamaları ayrı bir dosyaya yazmak ve kaydetmek iyi bir fikirdir. Görev kaydını kaydederken, bu belgedeki ek açıklamaları kesin ve yapıştırın.

**Farklı ek açıklama türlerini anlamak** Tüm ek açıklamalar isteğe bağlıdır. Bunları yalnızca kullanıcı için yararlı bilgiler sağlayacağı zaman ekleyin.

-   **Başlık**: Görev kaydedicinin otomatik olarak oluşturduğu adım metninden önce başlık ek açıklaması görünür. Görev kılavuzunda başlık ek açıklaması otomatik olarak oluşturulan metnin yukarısında görünür. Kullanıcının adımı neden yaptığını açıklamak veya ek bağlam sağlamak için bu tür ek açıklama kullanın.

Bu, kayıt oluştururken bir ek açıklama eklediğinizde gördüğünüz düzenleme bölmesidir. **Başlık** kutusuna bir başlık ek açıklaması girin. 

[![Başlık ek açıklamasıyla bölmeyi düzenleme](./media/screen1.png)](./media/screen1.png) 

Görev kılavuzunda "kabarcığında" başlık ek açıklaması bu şekilde görünür. 

[![Görev kılavuzunda başlık ek açıklama görünümü](./media/screen2.png)](./media/screen2.png)

-   **Notlar:** Görev kaydedicinin otomatik olarak oluşturduğu adım metninden sonra not ek açıklaması görünür. Görev kılavuzunda ancak kullanıcı görev kılavuzu kabarcığındaki **daha fazla göster** linkine tıkladığında görülebilir. Bu tür ek açıklamayı bir kullanıcının adımı tamamlaması için bilmesi gereken her şeyi açıklamak için kullanın.

Bu, kayıt oluştururken bir ek açıklama eklediğinizde gördüğünüz düzenleme bölmesidir. **Notlar** kutusuna bir not ek açıklaması girin. 

[![Notlar kutusunda ek açıklama bulunan bölmeyi düzenleme](./media/screen3.png)](./media/screen3.png) 

Görev kılavuzundaki "kabarcıkta" not ek açıklaması bu şekilde görünür.

[![Görev kılavuzunda notlar ek açıklama görünümü](./media/screen4.png)](./media/screen4.png)

-   **Bilgi adımı**: Bu ek açıklamalar bir denetime veya bir formdaki herhangi bir yere sağ tıklayıp &lt; **Görev kaydedici** &lt; **Bilgi adımı ekle**'ye tıklayarak oluşturulur. Bilgi adımları kullanıcı arabirimine herhangi bir işlem kaydedilmemiş olsa bile eklediğiniz noktada numaralı adım olarak görünür. Bir form düzeyi bilgi adımı veya bir denetimle ilişkilendirilmiş bir bilgi adımı ekleyebilirsiniz. Bir bilgi adımı bir formla ilişkilendirildiğinde, görev kılavuzu oynatıldığında, formun herhangi bir yerinde işaretçi olmaksızın görev kılavuzu "kabarcığı" görünecektir. Bir bilgi adımı bir denetimle ilişkilendirildiğinde, görev kılavuzu oynatıldığı zaman, görev kılavuzu "kabarcığı" denetimi gösterir. Yardım bölmesinde, bir bilgi adımı ek açıklaması, girdiğiniz metni içeren numaralı bir adım olarak görünür. Kullanıcıyı sonraki adımlara hazırlamak, uygulamanın dışında yapılması gereken adımları açıklamak veya diğer kayıtlara başvurmak için bilgi adımlarını kullanın (ancak ek açıklamalarda köprüler oluşturamazsınız).

**Kaydınızın süresini belirleyin**

-   Kullanıcı genellikle kaydı ya başından sonuna okuyacak ya da oynatacaktır, bu nedenle ayrı ayrı yapılması daha iyi olan adımları veya görevleri birleştirmeyin.
-   Birden çok alt işleme yayılan uzun bir senaryo kaydetmemeye çalışın. Örneğin, "Mağaza içi müşteri hizmetleri masasında işlem yapın" çok geniştir. Bunu "İadeleri kabul edin" ve "Hediye kartına ekleyin" gibi küçük görevlere bölün.
-   Bir görev birden fazla iş sürecinin bir parçası olarak yürütülebiliyorsa, bunun için ayrı bir kayıt oluşturun ve böylece diğer kayıtlarda ona başvurabilirsiniz.
-   İşlem kişinin büyük olasılıkla aynı anda yaptığı birden çok görevi içeriyorsa, görevleri bir kayıtta tutabilirsiniz, örneğin, "İşlevsellik profilleri ayarlama ve atama."
-   Eğer kişinin bir kez yapıp (yapılandırma gibi) ve hemen sonrasında yapabileceği ama tekrar tekrar ve tek başına yapabileceği başka bir görev söz konusuysa, onları iki görev kaydına bölün.

**Bir kaydı başlatmak için kullanıcı arabiriminde nerede olacağına karar verme** Bir görev kaydını başlattığınız sırada bulunduğunuz sayfa, görev kılavuzunun hangi sayfa için görüntüleneceğini belirler. Örneğin, bir kullanıcı Genel muhasebe parametreleri sayfasında Yardım'a tıkladığında görev kaydınızın Yardım bölmesinde listelenmesini istiyorsanız, kaydınızı Genel muhasebe parametreleri sayfasında başlatmanız gerekir. **Kayıtları .axtr dosyaları olarak kaydetme** Bir görev kaydı oluşturmayı veya düzenlemeyi bitirdiğinizde, kaydı nasıl indirmek veya kaydetmek istediğinizle ilgili birkaç seçenek sunulur. Dosyayı bir görev kaydı paketi (.axtr) olarak yükleyebilir, ham bir kayıt dosyası (.xml) olarak yükleyebilir, bir Word belgesi olarak yükleyebilir veya dosyayı bir LCS kitaplığına kaydedebilirsiniz. Görev kaydınızı bir görev kaydı paket dosyası (.axtr) olarak kaydetmek her zaman iyi bir fikirdir. Bu, daha sonra yordamları veya ek açıklamaları değiştirmek istediğinizde dosyanın bakımını kolaylaştırır. Dosyayı bir Word belgesi olarak indirmek isterseniz dosyayı ayrıca bir görev kaydı paket dosyası olarak kaydedin.

## <a name="create-your-task-recording"></a>Görev kaydınızı oluşturun
Ayrıntılı gözden geçirme adımları için bkz. [Görev kaydedici kaynakları](task-recorder.md).

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
9.  Bu noktada, kaydı adım adım geçin ve yeniden kaydetmek için ilerlerken her adımda değişiklikler yapın. **Not**: Bir kaydın yalnızca metnini değiştirmek istiyorsanız, kaydı **Kaydın ek açıklamalarını düzenle** modunda açabilir ve sonra kaydedebilirsiniz.
10. Kayıt sonuna kadar oynatıldıktan sonra, ekranın en üstündeki görev kaydedici çubuğundaki **Durdur'u** tıklayın.
11. Görev kaydını nasıl kaydetmek istediğinizi seçin.



<a name="additional-resources"></a>Ek kaynaklar
--------

[Yardım sistemi](../../fin-ops/get-started/help-overview.md)

[Yardım sistemini bağlama](../../fin-ops/get-started/help-connect.md)

[Görev Kaydedici](task-recorder.md)

[Görev Kaydediciyle Zengin Yardım Konuları Oluşturma (dış bağlantı)](https://mbspartner.microsoft.com/AX/Videos/970)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]