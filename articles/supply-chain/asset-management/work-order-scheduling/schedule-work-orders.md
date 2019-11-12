---
title: İş emirlerini planla
description: Bu konuda Varlık Yönetimi'nde iş emirleri planlama işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 953c4bb17329205c5d8d14b6570a6bac152e9320
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652161"
---
# <a name="schedule-work-orders"></a>İş emirlerini planla

[!include [banner](../../includes/banner.md)]

 

Bu konuda Varlık Yönetimi'nde iş emirleri planlama işlemi açıklanmaktadır. 

Bir iş emri için gereken saat sayısı, toplam tahmin saat eksi deftere nakledilen saate göre tanımlanır. Daha fazla zaman gerekiyorsa, tahmin uygun şekilde ayarlanmalıdır. **Varlık yönetimi** > **Ortak** > **İş emirleri** > **Tüm iş emirleri** veya **Etkin iş emirleri**'nde, iş emrini seçip **İş emri** sekmesinde **Tahmin**'e tıklayarak iş emrindeki tahminleri görüntüleyebilir veya düzenleyebilirsiniz. İş emirleri oluşturulduğunda ve tahmin edildiğinde, sonraki adım iş emirlerini tamamlamak için gerekli bakım çalışanlarını ve araçları tahsis etmektir.

Yalnızca planlamaya izin veren iş emri yaşam döngüsü durumuna sahip iş emirleri planlanabilir. Planlamaya izin ver ayarı **Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Yaşam döngüsü durumları** > **Genel** Hızlı Sekmesi > **Planlamaya izin ver** düğmesinde ayarlanır.

1. **Varlık yönetimi** > **Ortak** > **İş emirleri** > **Tüm iş emirleri**'ne tıklayın.

2. Listede planlamak istediğiniz iş emirlerini seçin. Örneğin, listeyi **Geçerli yaşam döngüsü durumuna**göre sıralayabilirsiniz.

3. **Genel** sekmesinde, **Planla** seçeneğine tıklayın.

4. **İş emirlerini  planla** iletişim kutusunda gerekirse, beklenen başlangıç tarihi ve hizmet düzeyi ile ilgili seçimler ekleyebilirsiniz. Planlama işlemi başka işler için zaten zamanlanmış olan kaynaklarla ilgili kapasite sınırlamalarını gözlemlemek zorundaysa, **Varlık**, **Araç** ve **Çalışan** düğmelerinin "Evet" olarak ayarlandığından emin olun.

    [!NOTE]
    **Varlık**, **Araç** ve **Çalışan** düğmelerini "Hayır" olarak ayarlarsanız, varolan rezervasyonlar yok sayılır. Bilgi günlüğünde, çakışan iş emri planlamalarının listesi görüntülenir ve gerekirse bir iş emrini açmak ve yeniden planlamak için iletilere tıklayabilirsiniz.

5. Planlama işlemiyle ilgili ayrıntılı bilgi görmek için **Ayrıntılı** düğmesinde "Evet" seçeneğini seçin. Bu, iş emirlerindeki ve bakım görevlilerindeki hesaplanan puanlar hakkında ayrıntılı bilginin Bilgi günlüğünde gösterildiği anlamına gelir.

6. Planlama işlemini başlatmak için **Tamam**'a tıklayın.

7. Planlama tamamlandığında, bir Bilgi günlüğü planlanan iş emirlerinin sayısını ve **Ayrıntılı** düğmesi "Evet" olarak ayarlandığında daha ayrıntılı bilgi gösterir.

>[!NOTE]
>İş emirleri, her iş emri işi için değil, iş emri başına bir döngüde planlanır. Ayrıca **İş emirlerini planla** iletişim kutusunu doğrudan **Varlık Yönetimi** > **Periyodik** > **İş emirleri** > **İş emirlerini planla**'dan da açabilirsiniz. Seçimlerinizi yapın ve İş emri planlamasını başlatmak için **Tamam**'a tıklayın. İş emri planlamasını **İş emirlerini planla** iletişim kutusu >**Arka planda çalıştır** hızlı sekmesinde toplu iş olarak ayarlamak da mümkündür.

*Örnek:* Aşağıdaki şekilde, **Beklenen başlangıç** alanına eklenen formül, şu andan itibaren bir hafta ve sonrası olan beklenen başlangıç tarihine sahip tüm iş emirleri için iş emri planlaması oluşturur. Bu formül iş emri planlamasını sürekli olarak çalıştırdığınızda ancak sonraki 5-6 gün için planlanan iş emirlerinin yeniden planlanmadığından emin olmak istediğinizde yararlı olabilir.

![Şekil 1](media/03-work-order-scheduling.png)

İş emirleriyle ilgili iş emri türü bir bakım görevlisi için planlama ayarlayabilir (**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **İş emri türleri** > **Bir bakım görevlisi** düğmesi "Evet" olarak ayarlanır). Bu, iş emri türünün bir iş emrinde kullanılıyor olması durumunda, **Bir bakım görevlisi** düğmesinin **Tüm iş emirleri** ayrıntıları sayfası > **Başlık** görünümü > **Planla** hızlı sekmesinde otomatik olarak "Evet" olarak ayarlanacağı anlamına gelir. İş emri planlama sırasında, iş emrinde oluşturulan tüm iş emri işleri aynı bakım çalışanına planlanacaktır. Gerekirse, iş emri işlerinde birçok çalışanın veya bir çalışanın planlanmasına izin vermek için **Tüm iş emirlerindeki** **Bir bakım görevlisi** düğmesindeki seçimi düzenleyebilirsiniz.

Varlık Yönetiminde planlama işlemi, planlama hesaplamasında çeşitli etmenler içerir:

- Hem iş emirleri hem de bakım çalışanları için puanları hesaplama. İş emirlerinin ve bakım görevlilerinin puanları **Varlık yönetimi parametrelerinde**ayarlanır. 
- İşin gerçekleştirilmesi için eşleşen yeteneklerin yani beceriler ve sertifikaların kontrol edilmesi. Beceriler ve sertifikalar bakım görevlileri için **İnsan kaynakları** modülünde ayarlanır (**İnsan kaynakları** > **Çalışanlar** > **Çalışanlar** > listeden çalışan seçin > **Çalışan** sekmesi > **Yeterlilikler** bölümü > **Beceriler** ve **Sertifikalar** düğmeleri). Ayrıca, beceriler ve sertifikalar bakım iş türlerine ve bakım işi görevlerine eklenebilir. Yeterlilikler ve bakım işi türleriyle ilgili daha fazla bilgi için [Bakım işi türü kategorileri ve bakım iş türleri, bakım iş türü çeşitleri, bakım işi işlemleri ve bakım denetim listeleri](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)'ne bakın.  

## <a name="scores-used-in-work-order-scheduling"></a>İş emri planlamada kullanılan puanlar

Bir iş emri işi için puanları hesaplama, iş emrinin beklenen başlangıç tarihini ve hizmet düzeyini temel alır.

**Başlangıç tarihi** hesaplaması: Beklenen başlangıç tarihinden sonraki her bir tarih için, başlangıç tarihi puanı çıkarılır ve aşağıdaki örneklerde "10" olan puanla çarpılır.

**Kritiklik** hesaplaması: Kritiklik puanı iş emrindeki kritiklik değeriyle çarpılır.

**Servis düzeyi** hesaplaması: Servis düzeyi puanı iş emrindeki hizmet düzeyine bölünür.

Aşağıdaki örneklerde, kritiklik puanı "2" ve hizmet düzeyi puanı "5" ve "100"dür.

**Örnek 1:**

| İş emri kodu | Beklenen başlangıç tarihi | İş emri kritikliği | İş emri hizmet düzeyi | Hesaplama               | Sonuç      |
|---------------|---------------------|------------------------|--------------------------|---------------------------|------------|
| WO-00010816   | Yarın            | 2                      | 20              | (-1 \* 10) + (2 \* 2) + 5 / 20     | \- 5.75    |
| WO-00010817   | Şu andan itibaren iki gün   | 2                      | 20              | (-2 \* 10) + (2 \* 2) + 5 / 20     | \- 15.75   |
| WO-00010818   | Şu andan itibaren iki gün   | 3                      | 5               | (-2 \* 10) + (2 \* 3) + 5 / 5      | \- 13      |

İş emirleri şu sırada planlanır: WO-000108**16**, WO-000108**18**, WO-000108**17**.

**Örnek 2:**

| İş emri kodu | Beklenen başlangıç tarihi | İş emri kritikliği | İş emri hizmet düzeyi | Hesaplama                 | Sonuç    |
|---------------|---------------------|------------------------|---------------------|----------------------------------|----------|
| WO-00010816   | Yarın            | 2                      | 20                  | (-1 \* 10) + (2 \* 2) + 100 / 20 | \- 1     |
| WO-00010817   | Şu andan itibaren iki gün   | 2                      | 20                  | (-2 \* 10) + (2 \* 2) + 100 / 20 | \- 11    |
| WO-00010818   | Şu andan itibaren iki gün   | 3                      | 5                   | (-2 \* 10) + (2 \* 3) + 100 / 5  | 6        |

Hizmet düzeyi puanı '5' yerine '100'e artırılırsa, planlama sırası şöyle olur: WO-000108**18**, WO-000108**16**, WO-000108**17**

İş emirlerinde hangi bakım çalışanlarının çalışması gerektiğini hesaplamayla ilgili derecelendirme puanları, iş emri planlama sırasında her bakım çalışanı hesaplamasına eklenen sayılar olarak ayarlanır. En yüksek puana sahip bakım çalışanı iş emrinde seçilir. Aşağıda, bakım çalışan puanlarının kısa bir açıklaması yer alır:

| Bakım görevlisi puanı       | Tanım                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sorumlu çalışan | Bakım çalışanı iş emrinde sorumlu çalışan olarak seçilirse, puan eklenir.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Sorumlu bakım görevlisi grubu | Bakım çalışanı iş emrinde sorumlu bakım çalışanı grubunun bir parçası olarak seçilirse, puan eklenir.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tercih edilen bakım görevlisi         | Bakım çalışanı varlıkta tercih edilen bakım çalışanı olarak seçilirse, puan eklenir.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Tercih edilen bakım görevlisi grubu   | Bakım çalışanı varlıkta tercih edilen bakım çalışanı grubunun bir parçası olarak seçilirse, puan eklenir.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Konum                 | Şirketiniz işlem yapılacak yerleşimleri kullanıyorsa bakım çalışanları varlıkla ilgili işlem yapılacak yerleşimde bulunuyorsa tam puan alırlar. Varlığın işlem yapılacak yerleşiminin üst yerleşimi varsa bu işlem yapılacak yerleşimdeki bakım çalışanları 1/2 puan alır. Bu yerleşimin de üst öğesi varsa bu yerleşimdeki bakım çalışanları 1/3 puan alır. Bu yerleşimin de bir üst öğesi varsa bu yerleşimdeki bakım çalışanları 1/4 puan alır ve hesaplama bu şekilde devam eder. Şirketiniz kıymet yerleşimini kullanıyorsa yerleşim puanlarını hesaplamak için yerleşim, alan ve bölge kullanılır. Bu ayarın kullanılmasını önermeyiz. Çalışanlar kıymetle ilgili yerleşim ve alan ve bölgede bulunuyorsa tam puan alır. Çalışan yerleşimi yalnızca yerleşim ve alanla eşleşiyorsa bu bakım çalışanının derecelendirme puanı tam puanın 2/3'ü olur. Bakım çalışanı yerleşimi yalnızca yerleşimle eşleşiyorsa bu bakım çalışanının derecelendirme puanı tam puanın 1/3'ü olur. |
| Çalışanın başlama tarihi               | Planlanan başlangıç tarihinin, beklenen başlangıç tarihinden sonra olduğu her tarih için puan çıkarılır.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |

>[!NOTE]
>Puan "0" olarak ayarlanmışsa, bu puan hesaplanmaz. Bu, örneğin, sorumlu çalışanı planlamaya dahil etmek istemediğinizde yararlıdır.

## <a name="competencies-used-in-work-order-scheduling"></a>İş emri planlamada kullanılan yetkinlikler

Yetenekler ve sertifika gereksinimleri bakım işi türlerinde (**Varlık yönetimi** > **Kurulum** > **İşler** > **Bakım işi türleri**) ve bakım işi görevlerinde (**Varlık yönetimi** > **Kurulum** > **İşler** > **Bakım işi görevi**) ayarlanabilir. 

Bakım işi türleri ve bakım işi görevleri iş emri işlerinde seçilir. Bir bakım iş türü veya bakım işi görevinde yetenekler veya sertifikalar seçilmişse ve bu bakım iş türü veya bakım işi görevi bir iş emri işinde kullanılıyorsa, yalnızca eşleşen becerilere ve sertifikalara sahip olan bakım çalışanları iş emrinde çalışmak üzere planlanır.

