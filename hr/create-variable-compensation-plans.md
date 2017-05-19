---
title: "Değişken ücret planları oluşturma"
description: "Değişken ücret, çalışanın düzenli almadığı, prim, hisse senedi ikramiyesi gibi ödemeleri ifade eder. Bu konuda, değişken ücret kullanabilmeniz ve çalışanları bir değişken ücret planına kaydedebilmeniz için ayarlanması gereken bileşenler açıklanmaktadır."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 917771596a0c56561bf302ae990d95a987f442e0
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="create-variable-compensation-plans"></a>Değişken ücret planları oluşturma

[!include[banner](includes/banner.md)]


Değişken ücret, çalışanın düzenli almadığı, prim, hisse senedi ikramiyesi gibi ödemeleri ifade eder. Bu makalede, değişken ücret kullanabilmeniz ve çalışanları bir değişken ücret planına kaydedebilmeniz için ayarlanması gereken bileşenler açıklanmaktadır.

Çalışanlarınız için değişken ücret tutarlarının hesaplanması çalışanın performansı, çalışanın ücret düzeyi ve departmanın performansı gibi çok sayıda faktöre dayalı olabilir.

## <a name="variable-compensation-components"></a>Değişken ücret bileşenleri
### <a name="create-compensation-types"></a>Ücret türleri oluşturma

**Değişken ücret türleri**zorunlu bir bileşendir. Değişken ücret türler, organizasyonunuzun verdiği değişken ücret türlerini tanımlar. Ayrıca, ücretin nakit mi, yoksa hisse senedi vb. gibi parasal olmayan bir türde mi olacağını belirlemenize izin verir.

### <a name="describe-vesting-rules"></a>Hakediş ödeme kuralları tanımlama

İsteğe bağlı olarak, şirketler **hakediş ödeme kuralları** oluşturabilir. Hakediş kuralları, değişken ikramiyenin zaman içerisinde nasıl ayrılacağını açıklar. Örneğin, bir hakediş ödeme kuralı, çalışanın kendi toplam ikramiyesinin yüzde 25'ini, sonraki dört yıl boyunca için alacağını belirtebilir. Hakediş ödeme kuralları yalnızca bilgilendirme amaçlıdır.

## <a name="variable-compensation-plans"></a>Değişken maaş planları
**Değişken ücret planı** kurallar, hesaplama yöntemleri ve kayıtlı çalışanlar için değişken ücret hesaplamasına ilişkin varsayılan değerleri içerir. Bir değişken ücret planı oluşturduğunuzda, değişken ücret türünü ayarlamanız gerekir. Değişken ücret türü, ikramiye olarak sistem para birimi tutarını mı yoksa birim sayısını mı ikramiye olarak hesaplayacağını belirler. Ayrıca, hesaplama yöntemini de ayarlamanız gerekir:

-   **Bir zaman noktasına** – Değişken ikramiyenin hesaplanması, belirli bir tarihte çalışanın sahip olduğu sabit maaşa dayanır. Yeni ücret tutarları işleme alındığında, tarih işlemde belirtilir.
-   **Bileşik** – Bir ikramiye tutarı, çalışanın süreç olayındaki döngü başlangıç tarihi ile döngü bitiş tarihi arasında sahip olduğu her bir özgün sabit ücret ödeme oranı için hesaplanır. Tarihler son ikramiyeyi belirlemek için daha sonra eklenir. Örneğin, döngü sırasında bir personel farklı ödeme oranı olan başka bir konuma transfer olur. Bu durumda değişken ikramiye, çalışanın her bir ödeme oranına sahip olduğu zaman uzunluğuna göre ayarlanır.

Değişken ikramiye tutarı, çalışanın düzenli taban kazançlarına veya ayarlanan bir birim sayısına dayalı olabilir.

-   Bir varsayılan yüzde girmek için **Taban yüzdesi** öğesini seçin ve tabanın çalışanın sabit ödeme oranımı mı, yoksa çalışanın ücret seviyesi için kontrol noktası mı olduğunu belirtin. Ücret düzeyi, personelin işinde ayarlanır. Ücret yapısından bir referans noktası, sabit ücret planında bir denetim noktası olarak ayarlanabilir. Sistem, personelin ücret seviyesi için denetim noktası tutarını bulmak için personelin işindeki ücret seviyesi kullanır ve bunu personelin sabit ücret planında listelenen denetim noktasıyla çapraz referanslar. Daha sonra, kontrol noktası tutarı tutar için temel olarak personelin sabit ödeme oranının yerine kullanılır.
-   Ücret planı nakit olmayan bir ikramiye (örneğin, 40 USD değerinde 200 birim hisse senedi) ise varsayılan birim sayısını, her bir birimin değerini ve birim değerinin para birimini girmek için **Birim sayısı** öğesini seçin veya ücret planı bir nakit ikramiye için ise sadece birim sayısını girin. Nakit ikramiye için personel, kendisinin sabit ücret planının para birimi cinsinden belirli sayıda birimi alacaktır (örneğin, 500 birim 1 USD). Bire bir ilişki denetimi, birim sayısı ve birim değeri arasında bire bir eşleşme olup olmadığını belirtmek üzere kullanılabilir. Nakit tabanlı bir plan için birim sayısı kullanarak bir değişken ücret planı oluşturursanız, bu seçenek otomatik biçimde **Evet** olarak sabitlenir ve birim değeri **1,0000**'dir.

**İşe alma** kuralı ayarı, çalışanların işe alınma tarihinden (**İşe alma kuralı** = **Yok**) bağımsız olarak aynı artışı alıp almayacağını veya çalışanların döngü sırasında çalıştıkları süreye dayalı olarak bir ikramiye yüzdesi alıp almayacağını (**İşe alma kuralı** = **Yüzde**) belirlemenize izin verir. 

**Dengeleme**, bir personelin ikramiyesini, personelin departmanının performansına dayalı ayarlamanıza olanak sağlar. Performans ölçüleri, her bir bölüm için **Bölümler** sayfasında, **İlgili formlar** &gt; **Ücret** &gt; **Performans** altında ayarlanabilir. Söz konusu bölümdeki çalışanların aldığı ikramiye, bölümün performansını belirten **Ulaşılan hedefin yüzdesi** alanının değerine bağlıdır:

-   Departmanın performansı yüzde 100 ise, o departmanındaki çalışanlar için ikramiye,**%100'de ödeme** alanında ayarlanan yüzdeyle çarpılır.
-   Departmanın performansı yüzde 100'den fazla ise sistem, **Hedefin üzerindeki her %1 için** alanında ayarlanan yüzdeyi **%100'de ödeme** alanına ekler ve bu işleme **İzin verilen en yüksek ödeme** alanında ayarlanan değere ulaşılana kadar devam edilir.
-   Departmanın performansı yüzde 100'den az ise sistem, **Hedefin üzerindeki her %1 için** alanında ayarlanan yüzdeyi **%100'de ödeme** alanından çıkarır ve bu işleme **İzin verilen en düşük ödeme** alanında ayarlanan değere ulaşılana kadar devam edilir.

Eşik yüzdeleri üzerinde **tolerans düzeyleri** ayarlayabilirsiniz, böylece dengeleme, yüzdenin eşik yüzdesinin dışında kalmasına neden oluyorsa bir uyarı mesajı görüntülenir. 

Varsayılan olarak, sistem çalışanın pozisyonu üzerinde ayarlanmış departmanı arar. Ancak, bazı çalışanların ödülü birden fazla bölümün performansına bağlı olabilir. Bu durumda, çeşitli departmanlar ve her bir departmanın performansına atanan ikramiye yüzdesi çalışanın değişken ücret kaydında ayarlanabilir. Daha fazla bilgi için aşağıdaki "Değişken ücret kaydı" bölümüne bakın. 

Dengeleme yalnızca dengeleme süreci çalışırken **Performans için ödeme** seçimi yapılırsa kullanılır. 

**Düzeylerini geçersiz kılar** sekmesi ikramiyenin varsayılan yüzdesini veya birim sayını, personelin ücret düzeyine dayalı olarak geçersiz kılmanıza olanak sağlar. **Düzeyler için varsayılan geçersiz kılmalar**, değişken ücret planına kayıtlı personeller için **Evet** olarak ayarlanmışsa, sistem düzeyi personelin işinden alır ve daha sonra, bu seviye için yüzdeyi veya birim sayısını belirlemek için düzey geçersiz kılma tablosuna bakar. Düzey, düzey geçersiz kılma tablosunda bulunmazsa, **Genel** sekmesindeki varsayılan yüzde veya birim sayısı kullanılır. Yüzde ve birim sayısı, personelin kaydında, değişken ücret planında da geçersiz kılınabilir.

## <a name="variable-compensation-enrollment"></a>Değişken maaş kaydı
### <a name="determine-who-is-eligible-for-the-plan"></a>Plan için kimlerin uygun olduğunu belirleme

Çalışanları bir değişken ücret planına kaydetmeye hazır olduğunuzda ilk adım, planda tanımlanan ücret için kimlerin uygun olduğunu belirlemektir. Uygunluğunu belirlemeden planı hiçbir çalışana atayamazsınız. Uygunluğu belirlemek için **Uygunluk kuralları** sayfasını açın ve planınız için yeni bir uygunluk kuralı oluşturun ve ardından bir çalışanın ücret planı için uygun olması için karşılaması gereken kriterleri tanımlayın. Uygunluğu departmana, işçi sendikasına, ücret bölgesine (konuma), işe, iş görevine, iş türüne ve/veya ücret seviyesine dayalı olarak sınırlayabilirsiniz. Çalışanlar bir ücret planına ancak uygunluk kuralında belirlenen **tüm** kriterleri karşılamaları şartıyla kaydedilebilir. 

**Not:** Uygunluk kuralları hem sabit ücret planları hem de değişken ücret planları için uygunluğun belirlenmesinde kullanılır. Uygunluk kuralları, bir çalışanın bir ücret planı için uygun olup olmadığını belirlemek için iş, pozisyon ve çalışan kayıtları altındaki şu alanları dikkate alır:

-   **İş** sayfasında:
    -   **İş** alanı
    -   **İş sınıflandırma** sekmesi altındaki **Görev** ve **İş türü** alanları
    -   **Ücret** sekmesindeki **Düzey** alanı
-   **Pozisyonlar** sayfasında: **Departman** ve **Ücret bölgesi** alanları
-   **Personel** sayfasında: ****Personel**** sekmesindeki **Kişisel bilgiler** &gt; **İşçi sendikaları** altında çalışanla bağlantılı işçi sendikaları hakkındaki bilgiler

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Değişken ücret planı için kayıt etkinleştirme

**Değişken ücret planları** sayfasında, uygun çalışanların plana kaydedilmesini sağlamak için **Kayıt etkinleştirme** seçeneğini **Evet** konumuna ayarlayın.

### <a name="enroll-the-employee"></a>Çalışanı kaydetme

Artık, çalışanları değişken ücret planına kaydedebilirsiniz. Bir çalışanı kaydetmek için **Çalışanlar** sayfasına gidin ve ardından çalışanı seçin. Ardından, Eylem Panosunda, **Ücret** &gt; **Değişken plan kaydı** öğelerini tıklayın. 

**Not:** **Kayıt** öğesi mutlaka değişken ücret planında **Evet** konumuna ayarlanmalıdır. **Plan** alanı, bu planlar için oluşturulan uygunluk kurallarına dayanarak sadece çalışanın uygun olduğu planları gösterir. Bir plan için bir uygunluk oluşturulmamışsa o plan için hiçbir çalışan uygun olmayacaktır. 

**Yürürlük tarihi** alanının doğru şekilde ayarlandığından emin olun. Değişken ücret planı **Bileşik** hesaplama yöntemini kullanıyorsa, kayıt geçerlilik tarihi çalışanın ikramiyesi hesaplanırken değerlendirilebilir. 

**Geçersiz kılmalar** sekmesini kullanarak personel için çeşitli değerleri geçersiz kılabilirsiniz. Örneğin, **İşe alma kuralı** plan üzerinde **Yüzde** olarak ayarlanmışsa ve çalışanın işe alma yüzdesini hesaplanması sırasında kullanılması gereken farklı işe alma tarihi varsa, işe alma tarihini **İşe alma kuralı tarihi** alanında ayarlayabilirsiniz.. **İkramiye yüzdesi** veya **Birim sayısı** değerlerini de belirli bir personel için, planın ayarlarına bağlı olarak geçersiz kılabilirsiniz. Bu değerler plan üzerindeki işe alma kuralı, performans faktörleri ve diğer ayarlar üzerinde dikkate alınır. 

**Kuruluş geçersiz kılmaları** bir personelin ikramiyesini bir veya daha fazla bölümlerin performansına temellendirmek için kullanılır. Departmanlar arasında tahsis edilen yüzde, toplamda yüzde 100 olmalıdır. Personelin bireysel performans da dikkate alınır. Bu ayarlar yalnızca dengeleme süreci çalışırken **Performans için ödeme** seçimi yapılırsa kullanılır.

<a name="see-also"></a>Ayrıca bkz.
--------

[Ücret planları](compensation-plans.md)




