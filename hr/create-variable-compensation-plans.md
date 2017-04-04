---
title: "Değişken ücret planları oluşturma"
description: "Değişken ücret, çalışanın düzenli almadığı, prim, hisse senedi ikramiyesi gibi ödemeleri ifade eder. Bu konuda değişken maaş kullanın ve bir değişken maaş planında bir çalışan kayıt önce ayarlanmış olması gerekir bileşenleri açıklar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: be156afa73de731e54985485b617bcbae883db3a
ms.lasthandoff: 03/31/2017


---

# <a name="create-variable-compensation-plans"></a>Değişken ücret planları oluşturma

Değişken ücret, çalışanın düzenli almadığı, prim, hisse senedi ikramiyesi gibi ödemeleri ifade eder. Bu makalede, değişken ücret kullanabilmeniz ve çalışanları bir değişken ücret planına kaydedebilmeniz için ayarlanması gereken bileşenler açıklanmaktadır.

Çalışanlarınız için değişken ücret tutarlarının hesaplanması çalışanın performansı, çalışanın ücret düzeyi ve departmanın performansı gibi çok sayıda faktöre dayalı olabilir.

## <a name="variable-compensation-components"></a>Değişken ücret bileşenleri
### <a name="create-compensation-types"></a>Ücret türleri oluşturma

**Değişken ücret türleri **zorunlu bir bileşendir. Değişken ücret türler, organizasyonunuzun verdiği değişken ücret türlerini tanımlar. Ayrıca, ücretin nakit mi, yoksa hisse senedi vb. gibi parasal olmayan bir türde mi olacağını belirlemenize izin verir.

### <a name="describe-vesting-rules"></a>Hakediş ödeme kuralları tanımlama

İsteğe bağlı olarak, şirketler **hakediş ödeme kuralları** oluşturabilir. Hakediş ödeme kuralları değişken ikramiye zamanla nasıl ayrılacağını açıklar. Örneğin, çalışanın kendi toplam ikramiye yüzde 25'i her yıl sonraki dört yıl için alacaksınız Hakediş ödeme kuralı belirtebilir. Hakediş ödeme kuralları yalnızca bilgilendirme.

## <a name="variable-compensation-plans"></a>Değişken maaş planları
**Değişken ücret planı** kurallar, hesaplama yöntemleri ve kayıtlı çalışanlar için değişken ücret hesaplamasına ilişkin varsayılan değerleri içerir. Değişken maaş planı oluşturduğunuzda, değişken maaş türü ayarlamanız gerekir. Değişken maaş tür sistem para birimi tutarı veya birim sayısı ikramiye olarak hesaplayıp hesaplamayacağını belirler. Ayrıca, hesaplama yöntemini de ayarlamanız gerekir:

-   **Bir zaman noktasına** – değişken ikramiye hesaplanması, belirli bir tarihte çalışana sahip olduğu sabit maaş dayanır. İşlem olayı yeni maaş tutarları işlendiğinde bu tarih belirtilir.
-   **Bileşik** – Bir ikramiye tutarı, çalışanın süreç olayındaki döngü başlangıç tarihi ile döngü bitiş tarihi arasında sahip olduğu her bir özgün sabit ücret ödeme oranı için hesaplanır. Oranları daha sonra eklenen son ödül birlikte belirlemek için. Örneğin, bir çalışanın döngüsü sırasında farklı ödeme oranı olan başka bir konuma transfer. Bu durumda değişken ikramiye, çalışanın her bir ödeme oranına sahip olduğu zaman uzunluğuna göre ayarlanır.

Değişken ikramiye tutarı, çalışanın düzenli taban kazançlarına veya ayarlanan bir birim sayısına dayalı olabilir.

-   Bir varsayılan yüzde girmek için **Taban yüzdesi** öğesini seçin ve tabanın çalışanın sabit ödeme oranımı mı, yoksa çalışanın ücret seviyesi için kontrol noktası mı olduğunu belirtin. Çalışanın işte maaş düzeyi ayarlanır. Referans noktaları maaş yapısından biri Sabit maaş planı üzerinde denetim noktası olarak ayarlanabilir. Sistem, çalışanın işten maaş düzeyi kullanın ve denetim noktası için çalışanın maaş düzeyi bulmak için çalışan Sabit maaş planı üzerinde listelenen denetim noktası ile çapraz başvuru. Denetim noktası tutar sonra yerine çalışanın sabit ödeme oranı temeli olarak ikramiye için kullanılacaktır.
-   Ücret planı nakit olmayan bir ikramiye (örneğin, 40 USD değerinde 200 birim hisse senedi) ise varsayılan birim sayısını, her bir birimin değerini ve birim değerinin para birimini girmek için **Birim sayısı** öğesini seçin veya ücret planı bir nakit ikramiye için ise sadece birim sayısını girin. Bir nakit ödül için kendi Sabit maaş planı (örneğin, 500 birim 1 USD) için kullanılan para biriminin birim sayısı belirtilen sayıda çalışan alacaktır. Bire bir ilişki denetim birim ve birim değeri arasında doğrudan bire bir eşleşme olup olmadığını belirtmek için kullanılabilir. Birim sayısını kullanarak nakit dayalı planı için bir değişken maaş planı oluşturduğunuzda, bu seçenek için otomatik olarak kilitlenir **Evet**, ve birim değeri **1,0000**.

**İşe alma kuralı** ayarı tüm çalışanları işe alma tarihi ne olursa olsun aynı artış alması gereken belirtmenize olanak verir (**işe alma kuralı** = **yok**), veya çalışanları döngüsü sırasında kendi İstihdam uzunluğunu dayalı ikramiye yüzdesi mi alacağını (**işe alma kuralı** = **yüzde**). 

**Dengeleme**, bir çalışanın Ödülü, çalışanın bölümünün performansına dayalı ayarlamanıza olanak sağlar. Performans ölçülerini üzerindeki her bölüm için ayarlanabilir **bölümler** altında sayfa **ilgili formlar**&gt;**maaş**&gt;**performans**. O departmanındaki çalışanlar almak ikramiye durumunun değerine bağlı **elde edilen hedefinin yüzde** departmanın performansı gösteren alan:

-   Departmanın performansı yüzde 100 ise, o departmanındaki çalışanlar için ikramiye,** %100'de ödeme** alanında ayarlanan yüzdeyle çarpılır.
-   Departmanın performansı yüzde 100'den fazla ise sistem, **Hedefin üzerindeki her %1 için** alanında ayarlanan yüzdeyi **%100'de ödeme** alanına ekler ve bu işleme **İzin verilen en yüksek ödeme** alanında ayarlanan değere ulaşılana kadar devam edilir.
-   Departmanın performansı yüzde 100'den az ise sistem, **Hedefin üzerindeki her %1 için** alanında ayarlanan yüzdeyi **%100'de ödeme** alanından çıkarır ve bu işleme **İzin verilen en düşük ödeme** alanında ayarlanan değere ulaşılana kadar devam edilir.

Eşik yüzdeleri üzerinde **tolerans düzeyleri** ayarlayabilirsiniz, böylece dengeleme, yüzdenin eşik yüzdesinin dışında kalmasına neden oluyorsa bir uyarı mesajı görüntülenir. 

Varsayılan olarak, sistem üzerinde çalışanın konumu ayarlanır departmanı arar. Ancak, bazı çalışanlar için ödül birden fazla bölümlerin performansını bağlı olabilir. Bu durumda, çeşitli Departmanlar ve performansını her bölüm için ayrılan ikramiye yüzdesi üzerinde çalışan değişken maaş kaydı ayarlanabilir. Daha fazla bilgi için aşağıdaki "değişken maaş kaydı" bölümüne bakın. 

Dengeleme yalnızca dengeleme süreci çalışırken **Performans için ödeme** seçimi yapılırsa kullanılır. 

**Düzeylerini geçersiz kılar** sekmesi Ödülü'nın varsayılan yüzde veya sayı, çalışanın maaş düzeyine dayalı birim geçersiz kılmanıza olanak sağlar. Yoksa **etkinleştir düzeylerini geçersiz kılar** ayarlamak **Evet** değişken maaş planında kayıtlı olan çalışanlar için sistem düzeyinde bir çalışanın işten alır ve arar onu düzeylerinde yüzde veya bu düzeyin birim sayısını belirlemek için tablo geçersiz kılıp kılmayacağını. Düzeyi içinde bulunmazsa düzeyi, varsayılan yüzde veya birim geçersiz kılar **genel** sekmesi kullanılır. Ayrıca birim sayısı ve yüzdesi üzerinde çalışanın kaydı değişken maaş planında kılınabilir.

## <a name="variable-compensation-enrollment"></a>Değişken maaş kaydı
### <a name="determine-who-is-eligible-for-the-plan"></a>Plan için kimlerin uygun olduğunu belirleme

Çalışanları bir değişken ücret planına kaydetmeye hazır olduğunuzda ilk adım, planda tanımlanan ücret için kimlerin uygun olduğunu belirlemektir. Uygunluğunu belirlemeden planı hiçbir çalışana atayamazsınız. Uygunluğu belirlemek için **Uygunluk kuralları** sayfasını açın ve planınız için yeni bir uygunluk kuralı oluşturun ve ardından bir çalışanın ücret planı için uygun olması için karşılaması gereken kriterleri tanımlayın. Uygunluğu departmana, işçi sendikasına, ücret bölgesine (konuma), işe, iş görevine, iş türüne ve/veya ücret seviyesine dayalı olarak sınırlayabilirsiniz. Çalışanlar bir ücret planına ancak uygunluk kuralında belirlenen **tüm** kriterleri karşılamaları şartıyla kaydedilebilir. 

**Not:** Uygunluk kuralları hem sabit ücret planları hem de değişken ücret planları için uygunluğun belirlenmesinde kullanılır. Uygunluk kuralları, bir çalışanın bir ücret planı için uygun olup olmadığını belirlemek için iş, pozisyon ve çalışan kayıtları altındaki şu alanları dikkate alır:

-   **İş** sayfasında:
    -   **İş** alanı
    -   **İş sınıflandırma** sekmesi altındaki **Görev** ve **İş türü** alanları
    -   **Ücret** sekmesindeki **Düzey** alanı
-   **Pozisyonlar** sayfasında: **Departman** ve **Ücret bölgesi** alanları
-   Üzerinde **çalışanları** sayfa: altında çalışan ile ilişkili işçi Sendikaları hakkında bilgi **kişisel bilgiler**&gt;**işçi Sendikaları** üzerinde *** alt *** sekmesi

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Değişken ücret planı için kayıt etkinleştirme

**Değişken ücret planları** sayfasında, uygun çalışanların plana kaydedilmesini sağlamak için **Kayıt etkinleştirme** seçeneğini **Evet** konumuna ayarlayın.

### <a name="enroll-the-employee"></a>Çalışanı kaydetme

Artık, çalışanları değişken ücret planına kaydedebilirsiniz. Bir çalışanı kaydetmek için **Çalışanlar** sayfasına gidin ve ardından çalışanı seçin. Eylem bölmesinde, i **maaş**&gt;**değişken planı kayıt**. 

**Not:** **Kayıt** öğesi mutlaka değişken ücret planında **Evet** konumuna ayarlanmalıdır. **Planı** alan çalışan bu planları için ayarladığınız uygunluk kuralları temel için uygun olan planlarını gösterir. Uygunluk kuralı için bir plan ayarlanmamışsa, çalışan için bu planı uygun olacaktır. 

Emin olun **yürürlük tarihi** alanını doğru şekilde ayarlayın. Değişken maaş planı kullanıyorsa, **bileşik** hesaplama yöntemi, kayıt geçerlilik tarihini kabul çalışanın ikramiye hesaplama sırasında. 

Kullanabileceğiniz **geçersiz kılar** sekmesinde çalışana ait belirli değerleri geçersiz kılmak için. Örneğin, **işe alma kuralı** ayarlamak **yüzde** plan üzerinde ve çalışanın işe alma yüzdesi hesaplama sırasında kullanılması gereken farklı işe alma tarihi, işe alma tarihini ayarlayabilirsiniz **işe alma kuralı tarihi** alan. Ya da kılabilirsiniz **ikramiye yüzde** değeri veya **birim sayısı** planın ayarlarına bağlı olarak, belirli bir çalışan için değer. Bu değerler hala işe alma kuralı, performans faktörleri ve diğer ayarları plan üzerinde çarpanlarına. 

**Kuruluş geçersiz kılmaları** bir çalışanın ikramiye üzerinde bir veya daha fazla bölümleri performansını temel olarak kullanılan. Departmanlar arasında tahsis yüzdesi yüzde 100 toplam. Çalışanın bireysel performans da kabul edilir. Bu ayarlar yalnızca aşağıdaki durumlarda kullanılır **performans için ödeme** maaş işlemini çalıştırdığınızda seçilir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Ücret planları](compensation-plans.md)


