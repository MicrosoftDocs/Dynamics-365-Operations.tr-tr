---
title: Değişken ücret planları oluşturma
description: Bu makalede, değişken ücret kullanabilmeniz ve çalışanları bir değişken ücret planına kaydedebilmeniz için ayarlanması gereken bileşenler açıklanmaktadır.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan, HcmCompensationWorkspace
audience: Application User
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: f2f51a095a23b651dca645b14e652519f20037e2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070573"
---
# <a name="create-variable-compensation-plans"></a>Değişken ücret planları oluşturma


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Değişken ücret, çalışanın düzenli almadığı, prim, hisse senedi ikramiyesi gibi ödemeleri ifade eder. Bu makalede, değişken ücret için gerekli bileşenlerin nasıl ayarlanacağı ve çalışanların bir değişken ücret planına nasıl kaydedileceği açıklanmaktadır.

Çalışanlarınız için değişken ücret tutarlarının hesaplanması çalışanın performansı, çalışanın ücret düzeyi ve departmanın performansı gibi çok sayıda faktöre dayalı olabilir.

## <a name="variable-compensation-components"></a>Değişken ücret bileşenleri
### <a name="create-compensation-types"></a>Ücret türleri oluşturma

**Değişken ücret türleri** zorunlu bir bileşendir. **Değişken ücret türleri**, kuruluşunuzun verdiği değişken ücret türlerini tanımlar. Ayrıca, ücretin nakit mi, yoksa hisse senedi vb. gibi parasal olmayan bir türde mi olacağını belirlemenize izin verir.

### <a name="describe-vesting-rules"></a>Hakediş ödeme kuralları tanımlama

İsteğe bağlı olarak, şirketler **Hakediş ödeme kuralları** ayarlayabilir. **Hakediş ödeme kuralları**, değişken ikramiyenin zaman içerisinde nasıl tahsis edilmesi gerektiğini açıklar. Örneğin, bir hakediş ödeme kuralı, çalışanın toplam ikramiyenin yüzde 25'ini, sonraki dört yıl boyunca için alacağını belirtebilir. Hakediş ödeme kuralları yalnızca bilgilendirme amaçlıdır.

## <a name="variable-compensation-plans"></a>Değişken maaş planları
**Değişken ücret planı** kurallar, hesaplama yöntemleri ve kayıtlı çalışanlar için değişken ücret hesaplamasına ilişkin varsayılan değerleri içerir. Bir değişken ücret planı oluşturduğunuzda, değişken ücret türünü ayarlamanız gerekir. Değişken ücret türü, ikramiye olarak sistem para birimi tutarını mı yoksa birim sayısını mı ikramiye olarak hesaplayacağını belirler. 

**Seçili rollere erişimi kısıtla** parametreleri ücret planında erişimi, İnsan Kaynakları içinde bu plana atanmış olan seçili güvenlik rolleriyle kısıtlar. Örneğin yöneticiler için olan ve İK'ya özel tüm rollerde görülmemesi gereken ücret planları oluşturduğunuzda, bu ücret planlarına erişimi kısıtlamak için bu parametreyi kullanabilirsiniz. 

Ayrıca, hesaplama yöntemini de ayarlamanız gerekir:

-   **Bir zaman noktasına** – Değişken ikramiyenin hesaplanması, belirli bir tarihte çalışanın sahip olduğu sabit maaşa dayanır. Yeni ücret tutarları işleme alındığında, tarih işlemde belirtilir.
-   **Bileşik** – Bir ikramiye tutarı, çalışanın süreç olayındaki döngü başlangıç tarihi ile döngü bitiş tarihi arasında sahip olduğu her bir özgün sabit ücret ödeme oranı için hesaplanır. Tarihler son ikramiyeyi belirlemek için daha sonra eklenir. Örneğin, döngü sırasında bir personel farklı ödeme oranı olan başka bir konuma transfer olur. Bu durumda değişken ikramiye, çalışanın her bir ödeme oranına sahip olduğu zaman uzunluğuna göre ayarlanır.

Değişken ikramiye tutarı, çalışanın düzenli taban kazançlarına veya ayarlanan bir birim sayısına dayalı olabilir.

-   Bir varsayılan yüzde girmek için **Taban yüzdesi** öğesini seçin ve tabanın çalışanın sabit ödeme oranımı mı, yoksa çalışanın ücret seviyesi için kontrol noktası mı olduğunu belirtin. Ücret düzeyi, personelin işinde ayarlanır. Ücret yapısından bir referans noktası, sabit ücret planında bir denetim noktası olarak ayarlanabilir. Personelin ücret düzeyi için denetim noktası tutarını bulmak üzere personelin işindeki ücret seviyesi kullanılır ve personelin sabit ücret planında listelenen denetim noktasıyla çapraz referanslanır. Daha sonra, kontrol noktası tutarı tutar için temel olarak personelin sabit ödeme oranının yerine kullanılır.
-   Ücret planı nakit olmayan bir ikramiye (örneğin, 40 USD değerinde 200 birim hisse senedi) ise varsayılan birim sayısını, her bir birimin değerini ve birim değerinin para birimini girmek için **Birim sayısı** öğesini seçin veya ücret planı bir nakit ikramiye için ise sadece birim sayısını girin. Nakit ikramiye için personel, sabit ücret planının para birimi cinsinden belirli sayıda birimi alacaktır (örneğin, 500 birim 1 USD). Bire bir ilişki denetimi, birim sayısı ve birim değeri arasında bire bir eşleşme olup olmadığını belirtmek üzere kullanılabilir. Nakit tabanlı bir plan için birim sayısı kullanarak bir değişken ücret planı oluşturursanız, bu seçenek otomatik biçimde **Evet** olarak sabitlenir ve birim değeri **1,0000**'dir.

**İşe alma kuralı**, çalışanların işe alınma tarihinden (**İşe alma kuralı** = **Yok**) bağımsız olarak aynı artışı alıp almayacağını veya çalışanların döngü sırasında çalıştıkları süreye dayalı olarak bir ikramiye yüzdesi alıp almayacağını (**İşe alma kuralı** = **Yüzde**) belirtir. 

**Dengeleme**, bir personelin ikramiyesini, personelin departmanının performansına dayalı ayarlar. Performans ölçüleri, her bir bölüm için **Bölümler** sayfasında, **İlgili formlar** &gt; **Ücret** &gt; **Performans** altında ayarlanabilir. Söz konusu bölümdeki çalışanların aldığı ikramiye, bölümün performansını belirten **Ulaşılan hedefin yüzdesi** alanının değerine bağlıdır:

-   Departmanın performansı yüzde 100 ise, o departmanındaki çalışanlar için ikramiye,**%100'de ödeme** alanında ayarlanan yüzdeyle çarpılır.
-   Departmanın performansı yüzde 100'den fazla ise sistem, **Hedefin üzerindeki her %1 için** alanında ayarlanan yüzdeyi **%100'de ödeme** alanına ekler ve bu işleme **İzin verilen en yüksek ödeme** alanında ayarlanan değere ulaşılana kadar devam edilir.
-   Departmanın performansı yüzde 100'den az ise sistem, **Hedefin üzerindeki her %1 için** alanında ayarlanan yüzdeyi **%100'de ödeme** alanından çıkarır ve bu işleme **İzin verilen en düşük ödeme** alanında ayarlanan değere ulaşılana kadar devam edilir.

**Tolerans düzeyleri**, eşik yüzdelerinde ayarlanabilir, böylece dengeleme yüzdenin eşik yüzdesinin dışında kalmasına neden oluyorsa bir uyarı iletisi görüntülenir. 

Varsayılan olarak, çalışanın pozisyonu üzerinde ayarlanmış departman çalışan ikramiyesi için kullanılır. Ancak, bazı çalışanların ödülü birden fazla bölümün performansına bağlı olabilir. Bu durumda, çeşitli departmanlar ve her bir departmanın performansına atanan ikramiye yüzdesi çalışanın değişken ücret kaydında ayarlanabilir. Daha fazla bilgi için aşağıdaki "Değişken ücret kaydı" bölümüne bakın. 

Dengeleme yalnızca dengeleme süreci çalışırken **Performans için ödeme** seçimi yapılırsa kullanılır. 

**Düzeylerini geçersiz kılar** sekmesi ikramiyenin varsayılan yüzdesini veya birim sayını, personelin ücret düzeyine dayalı olarak geçersiz kılmanıza olanak sağlar. Değişken ücret planına kayıtlı personeller için **Düzeyler için geçersiz kılma işlemlerini etkinleştir** seçeneği **Evet** olarak ayarlanırsa personelin işindeki düzey, bu düzey için birim yüzdesini veya sayısını belirlemek üzere düzey geçersiz kılma tablosuyla karşılaştırılır. Düzey, düzey geçersiz kılma tablosunda bulunmazsa, **Genel** sekmesindeki varsayılan yüzde veya birim sayısı kullanılır. Yüzde ve birim sayısı, personelin kaydında, değişken ücret planında da geçersiz kılınabilir.

## <a name="variable-compensation-enrollment"></a>Değişken maaş kaydı
### <a name="determine-who-is-eligible-for-the-plan"></a>Plan için kimlerin uygun olduğunu belirleme

Çalışanları bir değişken ücret planına kaydetmeye hazır olduğunuzda ilk adım, planda tanımlanan ücret için kimlerin uygun olduğunu belirlemektir. Uygunluğunu belirlemeden planı hiçbir çalışana atayamazsınız. Uygunluğu belirlemek için **Uygunluk kuralları** sayfasını açın ve planınız için yeni bir uygunluk kuralı oluşturun ve ardından bir çalışanın ücret planı için uygun olması için karşılaması gereken kriterleri tanımlayın. Uygunluğu departmana, işçi sendikasına, ücret bölgesine (konuma), işe, iş görevine, iş türüne ve/veya ücret seviyesine dayalı olarak sınırlayabilirsiniz. Çalışanlar bir ücret planına ancak uygunluk kuralında belirlenen **tüm** kriterleri karşılamaları şartıyla kaydedilebilir. 

**Not:** Uygunluk kuralları hem sabit ücret planları hem de değişken ücret planları için uygunluğun belirlenmesinde kullanılır. Uygunluk kuralları, bir çalışanın bir ücret planı için uygun olup olmadığını belirlemek için iş, pozisyon ve çalışan kayıtları altındaki şu alanları dikkate alır:

- **İş** sayfasında:
  -   **İş** alanı
  -   **İş sınıflandırma** sekmesi altındaki **Görev** ve **İş türü** alanları
  -   **Ücret** sekmesindeki **Düzey** alanı
- **Pozisyonlar** sayfasında: **Departman** ve **Ücret bölgesi** alanları
- <strong>Personel</strong> sayfasında: *<strong><em>Çalışan</em></strong>* sekmesindeki <strong>Kişisel bilgiler</strong> &gt; <strong>İşçi sendikaları</strong> altında çalışanla bağlantılı işçi sendikaları hakkındaki bilgiler

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Değişken ücret planı için kayıt etkinleştirme

**Değişken ücret planları** sayfasında, uygun çalışanların plana kaydedilmesini sağlamak için **Kayıt etkinleştirme** seçeneğini **Evet** konumuna ayarlayın.

### <a name="enroll-the-employee"></a>Çalışanı kaydetme

Artık, çalışanları değişken ücret planına kaydedebilirsiniz. Bir çalışanı kaydetmek için **Çalışanlar** sayfasına gidin ve ardından çalışanı seçin. Ardından, Eylem Panosunda, **Ücret** &gt; **Değişken plan kaydı** öğelerini tıklayın. 

**Not:** **Kayıt** öğesi mutlaka değişken ücret planında **Evet** konumuna ayarlanmalıdır. **Plan** alanı, bu planlar için oluşturulan uygunluk kurallarına dayanarak sadece çalışanın uygun olduğu planları gösterir. Bir plan için bir uygunluk oluşturulmamışsa o plan için hiçbir çalışan uygun olmayacaktır. 

**Yürürlük tarihi** alanının doğru şekilde ayarlandığından emin olun. Değişken ücret planı **Bileşik** hesaplama yöntemini kullanıyorsa, kayıt geçerlilik tarihi çalışanın ikramiyesi hesaplanırken değerlendirilebilir. 

**Geçersiz kılmalar** sekmesini kullanarak personel için çeşitli değerleri geçersiz kılabilirsiniz. Örneğin, **İşe alma kuralı** plan üzerinde **Yüzde** olarak ayarlanmışsa ve çalışanın işe alma yüzdesini hesaplanması sırasında kullanılması gereken farklı işe alma tarihi varsa, işe alma tarihini **İşe alma kuralı tarihi** alanında ayarlayabilirsiniz.. **İkramiye yüzdesi** veya **Birim sayısı** değerlerini de belirli bir personel için, planın ayarlarına bağlı olarak geçersiz kılabilirsiniz. Bu değerler plan üzerindeki işe alma kuralı, performans faktörleri ve diğer ayarlar üzerinde dikkate alınır. 

**Kuruluş geçersiz kılmaları** bir personelin ikramiyesini bir veya daha fazla bölümlerin performansına temellendirmek için kullanılır. Departmanlar arasında tahsis edilen yüzde, toplamda yüzde 100 olmalıdır. Personelin bireysel performans da dikkate alınır. Bu ayarlar yalnızca dengeleme süreci çalışırken **Performans için ödeme** seçimi yapılırsa kullanılır.





[!INCLUDE[footer-include](../includes/footer-banner.md)]
