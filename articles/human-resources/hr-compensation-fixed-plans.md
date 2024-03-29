---
title: Sabit ücret planları oluşturma
description: Bu makalede, sabit maaş planı oluşturabilmeniz veya çalışanları kaydedebilmeniz için ayarlamanız gereken bileşenler açıklanmaktadır.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable, HcmCompensationWorkspace
audience: Application User
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: f254afc37d5afae48c3b2b3b16bd86634ac9aa3a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875756"
---
# <a name="create-a-fixed-compensation-plans"></a>Sabit ücret planları oluşturma


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sabit ücret, çalışanın düzenli brüt maaşını veya ücretlerini ifade eder. Bu makalede, sabit maaş planı oluşturabilmeniz veya çalışanları kaydedebilmeniz için ayarlamanız gereken bileşenler açıklanmaktadır.

Sabit ücret tutarları performans, bölge ve bütçe artışları gibi faktörlere dayalı olarak çalışanlarınız için hesaplanabilir. Dynamics 365 Human Resources adım, sınıf ve bant ücret türlerini destekler.

## <a name="fixed-compensation-components"></a>Sabit ücret bileşenleri
### <a name="compensation-levels"></a>Ücret düzeyleri

Çeşitli işler için ücret ayarlamak üzere **Ücret düzeyleri**'ni kullanabilir ve bu işleri gerçekleştiren personellerin adil şekilde ücret almasını garanti edebilirsiniz. **Ücret düzeyleri** sayfasında, her adım, sınıf ve bant planı için gerekli olan ücret düzeylerini ayarlayabilirsiniz. Türüne göre düzeyleri doğru sıraya koymak için **Yukarı** ve **Aşağı** düğmelerini kullanın. Bir işteki ücret seviyelerini ayarlayarak, bu iş için bir pozisyonda çalışan tüm çalışanların aynı düzeyde ödeme aldığını garanti edersiniz.

### <a name="reference-points"></a>Referans noktaları

**Referans noktaları** ızgarada her bir düzey için ücret aralıklarını tanımlayan sütunlardır. Ücret düzeyi ızgaradaki satırdır. Sınıf türü için tipik referans noktaları bir minimum, orta nokta ve maksimumdur. Referans noktalarını **Referans noktası kurulumları** sayfasında oluşturabilirsiniz.

### <a name="compensation-grids"></a>Maaş kılavuzları

Düzeyleri ve referans noktalarını ayarladıktan sonra **Ücret ızgarası** oluşturmak için birleştirebilirsiniz. **Ücret ızgaraları** sayfasında, ızgara bilgilerini tanımlayın. Örneğin, ızgaranın ne için kullanılmak üzere tasarlandığını, ne tür planla birlikte kullanılacağını ve ızgarada hangi referans noktalarının veya sütunlarının gerekli olduğunu belirtin. Bu bilgileri girmeyi bitirdiğinizde, ızgaranıza düzeyleri ve tutarları eklemek için **Ücret yapısı** öğesini tıklatın. 

**İpucu:** İlk tutarları ayarlamak için ücret yapısında **Toplu değişiklikler** işlevini kullanın ve ardından düzeylerinizde veya referans noktalarınızda geçerli yüzdelere veya tutarlara göre yükseltin.

### <a name="pay-frequencies"></a>Ödeme sıklıkları

**Ödeme sıklıkları** bir çalışanın maaşının veya ücretinin nasıl belirtileceğini (örnek, saatlik 10$ - yıllık 50.000$) ve saatlik, haftalık, aylık (12 ay) ve yıllık ücretler arasındaki dönüşümü tanımlamak için kullanılır. Örneğin, saatlik çalışanları için 38 saatlik çalışma haftası kullanan bir şirket saatlik ücreti 1, haftalık ücreti 38, aylık ücreti 164.6666666667 ve yıllık ücreti 1.976 olan bir ödeme sıklığı ayarlıyor. Bu dönüşümler, bir çalışanın sabit ücret kaydında görüntülenen çeşitli ödeme ücretlerinin hesaplanması için kullanılır.

## <a name="fixed-compensation-plans"></a>Sabit maaş planları
Yapılandırıldığınız tüm bileşenleri birleştirmek için sabit ücret planını tanımlayabilirsiniz. Bir sabit ücret planı oluşturmak için **Sabit ücret planları** sayfasını açın. Buradan planınıza bir ad ve açıklama girebilir, hangi türde (adım, sınıf veya bant) bir plan olduğunu seçebilir, çalışanların ödeme ücreti (saatlik tutar, yıllık tutar vb.) için kullanacağınız ödeme sıklığını seçebilir ve ücretin nasıl işleneceğini kontrol eden seçenekleri ayarlayabilirsiniz. 

**Aralık dışı tolerans** ayarı, ücret tutarlarının minimum ve maksimum tutarlar arasında olduğundan emin olmak için ne ölçüde katı olduğunu belirlemenize izin verir. Bir **Sabit** tolerans, ücretin belirli bir düzey için tanımlanan aralık içinde olmasını gerektirir. Bir **Yumuşak** toleransı, ücret tutarının aralık dışında olduğunda sizi uyarır, ancak devam etmenize izin verir. Toleransı **Yok** olarak ayarlarsanız uyarı veya hata mesajları almadan bir çalışan için herhangi bir ücret tutarı girebilirsiniz. 

**İşe alma kuralı** ayarı, tüm çalışanların işe alınma tarihinden bağımsız olarak aynı artışı alıp almayacağını (**İşe alma kuralı** = **Yok**) veya çalışanların döngü sırasında ne kadar süreyle çalıştıklarına bağlı olarak ikramiyeden bir yüzde alıp almayacağını (**İşe alma kuralı** = **Yüzde**) belirlemenize izin verir. 

**Ücret kademesi kullanım oranı matrisi**, çalışanların aralığın orta noktasına ulaşması için gereken süreyi azaltmak veya çalışanların aralıktaki maksimum referans noktasına ulaşması için gereken süreyi artırmak istediğinizde kullanışlıdır. Örneğin, bulundukları aralıkta alttaki yüzde 25'lik dilim içinde bulunan çalışanlara hedef ikramiyesinden yüzde 110 ve bulundukları aralıkta üstteki yüzde 25'lik dilim içinde bulunan çalışanlara maksimum düzeye kısa sürede ulaşmalarını önlemek için hedef ikramiyesinden yüzde 80 vermek istiyorsunuz. 

Sabit ücret planının temelleri tanımladıktan sonra plan için ücret yapısını oluşturabilirsiniz. **Ücret ayarla**'ya tıklayın. Bir iletişim kaydırıcı açılarak size üç seçenek sağlar:

-   Referans noktası ayarı seçerek ve ızgaraya ad vererek **yeni bir ücret matrisi oluşturun**.
-   Başlangıç noktası olarak kullanabileceğiniz mevcut bir ızgaranın kopyasını oluşturarak **yeni bir ücret matrisi oluşturun**.
-   Zaten tanımlanmış **mevcut bir ücret matrisini kullanın**. Aynı ızgarayı kullanan tüm ücret planları, o ızgara değiştirildiğinde güncelleştirmeler alır.

Bir seçenek belirlediğinizde **Ücret yapısı** sayfası açılır ve yeni ücret ızgarasında veya mevcut ücret ızgarasında değişiklikler yapabilirsiniz.

## <a name="fixed-compensation-enrollment"></a>Sabit ücret kaydı
### <a name="determine-who-is-eligible-for-the-plan"></a>Plan için kimlerin uygun olduğunu belirleme

Çalışanların bir sabit ücret planına kaydedilmesinin ilk adımı, planda tanımlanan ücret için kimlerin uygun olduğunu belirlemektir. Uygunluğunu belirleyene kadar planı hiçbir çalışana atayamazsınız. Uygunluk ayarlamak için **Uygunluk kuralları** sayfasını açın. Burada, ücret planınız için yeni bir uygunluk kuralı oluşturabilir ve bir personelin bir planın uygunluğunu karşılamak için sahip olması gereken ölçütleri tanımlayabilirsiniz. Uygunluğu departmana, işçi sendikasına, ücret bölgesine (konuma), işe, iş görevine, iş türüne veya ücret seviyesine göre sınırlayabilirsiniz. Çalışanlar bir ücret planına ancak uygunluk kuralında belirlenen tüm koşulları karşılamaları şartıyla kaydedilebilir. 

**Not:** Uygunluk kuralları hem sabit hem de değişken ücret planları için uygunluğun belirlenmesinde kullanılır. 

Uygunluk kuralı bir çalışanın bir ücret planı için uygun olup olmadığını belirlemek üzere **İş**, **Pozisyon** ve **Çalışan** kayıtlarındaki özel alanların değerini dikkate alır.

-   **İş** sayfasında uygunluk kuralı şu alanları dikkate alır:
    -   **İş** alanı
    -   **İş sınıflandırma** sekmesinde **Görev** ve **İş türü** alanlarını seçin
    -   **Ücret** sekmesinde **Düzey** alanı
-   **Pozisyonlar** sayfasında uygunluk kuralı, **Departman** ve **Ücret bölgesi** alanlarını dikkate alır.

Uygunluk kuralı ayrıca çalışanla bağlantılı işçi sendikalarını da dikkate alır (**Personeller** sayfasında **Çalışan** sekmesinden **Kişisel bilgiler** &gt; **İşçi sendikaları** öğelerini tıklayın).

### <a name="define-fixed-compensation-actions"></a>Sabit ücret eylemlerini tanımlama

**Sabit ücret eylemleri** bir çalışanın sabit ücretinde değişiklikler yapmak veya değişiklikleri uygulamak istediğinizde kullanılır. Sabit ücret eylemleri bir ücret ve kazanç yöneticisinin gerçekleştirebileceği eylem türlerine açıklayıcı adlar vermenizi sağlar. Farklı eylem türlerinin arkasında özel mantıklar bulunur, böylece bunlar özel zamanlarda kullanılabilir. 

Örneğin, bir çalışan için sabit ücret oluşturulduğunda, sadece **İşe alma/Yeniden işe alma** türüne sahip eylemler kullanılabilir. Bu durumda, **İşe alma/yeniden işe alma** türünde üç farklı eylem oluşturmak ve bunlara **İşe alma**, **Yeniden işe alma** ve **Transfer** adlarını vermek isteyebilirsiniz. Ardından, bir çalışana neden sabit ücret verildiğini veya bunun neden değiştirildiğini açıklayan daha ayrıntılı tanımlara sahip olursunuz.

### <a name="enroll-the-employee"></a>Çalışanı kaydetme

Şimdi bir sabit ücret planına bir çalışan atayabilirsiniz. **Çalışanları** sayfasını açın ve ücret planına kaydedilecek çalışanı seçin. Eylem Bölmesinde, **Ücret** &gt; **Sabit plan** üzerine tıklayın. Şimdi bu personel için yeni bir sabit ücret eylemi oluşturabilirsiniz. 

**Not:** **Ücret planı** alanı, her bir plan için oluşturulan uygunluk kuralları altında yalnızca çalışanın uygun olduğu planları gösterir. Bir plan için hiçbir uygunluk kuralı oluşturulmamışsa o plan için hiçbir çalışan uygun olmayacaktır. 

Derece veya bant türündeki bir ücret planı için belirtilen ücret tutarı, çalışanın işinde ilgili ücret düzeyi açısından minimum ve maksimum referans noktaları içinde olduğunu doğrular. Telafi tutarı izin verilen aralıkta bulunuyorsa, sabit ücret planında ayarlanan tolerans düzeyine dayalı olarak bir uyarı veya hata mesajı görüntülenir.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
