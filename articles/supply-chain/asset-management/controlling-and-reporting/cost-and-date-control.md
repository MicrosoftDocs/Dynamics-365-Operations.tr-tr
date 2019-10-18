---
title: Maliyet ve tarih kontrolü
description: Bu konuda Varlık Yönetimi'nde maliyeti ve tarih denetimini açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918407"
---
# <a name="cost-and-date-control"></a>Maliyet ve tarih kontrolü

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Kıymet yönetiminde, sabit kıymetler, işlevsel yerleşimler ve iş emirleriyle ilgili bütçe maliyetleriyle karşılaştırıldığında fiili maliyetlerin genel görünümünü elde etmek için maliyetleri hesaplayabilirsiniz. Fiili maliyetler deftere nakledilen hareketleri temel alarak yapılır. Ayrıca, planlanan başlangıç ve bitiş tarihlerini çalışma emirlerindeki gerçek başlangıç ve bitiş tarihleriyle karşılaştırmak istiyorsanız, tarih hesaplaması da yapabilirsiniz.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Kıymetler, işlevsel yerleşimler ve iş emirleri için maliyet kontrolü

Varlıklar, işlevsel yerleşimler ve çalışma emirleri için oluşturulan hesaplamalar neredeyse aynıdır. Tek fark, varlıklar ve işlem yapılacak konumlar için alt varlıkları ve alt konumları da hesaplamanıza dahil edebiliyor olmanızdır. Tarih, kayıt kaydedildiği hareket tarihidir.

1. **Varlık yönetimi** > **Sorgular** > **Varlıklar** > **Varlık maliyet denetimi** veya **İşlem yapılacak yerleşim maliyet denetimi** veya **Varlık yönetimi** > **Sorgular** > **İş emirleri** > **İş emri maliyet denetimi**'ne tıklayın.

2. **Varlık maliyet denetimi** / **İşlem yapılacak yerleşim maliyet denetimi** / **İş emri maliyet denetimi** iletişim kutusunda, hesaplanacak bir dönemi seçin.

3. Gerekirse, hesaplamaya dahil edilecek bir mali boyut kümesi seçin.

4. Sıfır saat içeren sonuçları göstermek istemiyorsanız, **sıfır atlama** düğmesi üzerinde "Evet" seçeneğini belirleyin.

5. İşlem yapılacak yerleşimlerle ilgili olarak maliyet denetimi satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz. Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim hiyerarşiniz varsa, işlem yapılacak yerleşim için tüm maliyet denetimi satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. **Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeyinde bulunan tüm maliyet denetimi satırlarını gösteren ayrıntılı bir sonuç görürsünüz.

6. Bu sütunu hesaplamaya dahil etmek istiyorsanız **Açık taahhüt edilen maliyeti göster** değiştir düğmesini göster üzerinde "Evet" seçeneğini belirleyin.

7. Alt kıymetlerle ilgili maliyetleri ayrı satırlar olarak göstermek için **alt kıymetleri dahil et** düğmesini seçin.

8. Aramayı sınırlandırmak istiyorsanız, Hızlı Sekme **dahil edilecek kayıtlar** üzerinde belirli varlıkları / işlem yapılacak yerleşimleri / iş emirlerini seçebilirsiniz.

9. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

Aşağıdaki şekil, **Varlık maliyet denetimi** iletişim kutusunun bir örneğini gösterir.

![Şekil 1](media/01-controlling-and-reporting.png)

10. **Varlık maliyet denetimi** sayfasındaki **Şuna göre grupla...** eylem panosu gruplarında, hesaplamanın gerekli ayrıntı düzeyini gösteren ilgili düğmelere tıklayın. Seçilen eylem bölmesi düğmeleri vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

Aşağıdaki şekil, **Varlık maliyet denetimi** içinde hesaplama sonuçlarının bir örneğini gösterir.

![Şekil 2](media/02-controlling-and-reporting.png)

Maliyet hesaplaması yapmanın bir başka yolu **Tüm varlıklar** veya **Etkin varlıklar** içinde çoklu varlıkları seçmektir. Daha sonra, **genel** sekmesindeki **maliyet denetimi** düğmesini tıklatın. **Varlık maliyet denetimi** iletişim kutusunda, seçilen kıymetler hızlı sekme **dahil edilecek kayıtlar** içindeki **Varlık** alanına otomatik eklenir. **Tamam**'ı tıklattın ve seçilen varlıklar için bir maliyet hesaplaması gösterilir. Aynı işlem **Tüm işlem yapılacak yerleşimler** veya **Etkin işlem yapılacak yerleşimler** içindeki işlem yapılacak yerleşimler ve **Tüm iş emirleri** veya **Etkin iş emirleri** içindeki tüm iş emirleri için kullanılabilir.

>[!NOTE]
>**Orijinal bütçe** alanı, bütçe maliyetlerini iş emri tahmininden gösterir. **Taahhüt edilen maliyet** alanı, tüzel kişiliğin kendisi ödemek üzere taahhüt ettiği giderlerin tutarın toplamını gösterir. **Açık taahhüt edilen maliyet** alanı, sipariş ettiğiniz veya aldığınız, ancak henüz ödenmemiş olan maddeler, saatler ve servisler için ödeme taahhütlerini gösterir. Tüm tüketim kayıtları gönderildikten sonra, ilgili maliyetler **Fiili maliyet** alanına eklenir.

## <a name="work-order-date-control"></a>İş emri tarih denetimi

İş emirlerindeki gerçek başlangıç ve bitiş tarihleriyle karşılaştırıldığında, beklenen başlangıç ve bitiş tarihlerinin özetini almak için bu sayfayı kullanın.

1. **Varlık yönetimi** > **Sorgular** > **İş emirleri** > **İş emri tarih denetimi**'ne tıklayın.

2. **Hesapla** üzerine tıklayın.

3. **İşlem yapılacak yerleşim** alanında bir işlem yapılacak yerleşim seçin.

4. **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında hesaplamayı yapmak istediğiniz dönemi girin. Dönem içinde başlaması beklenen tüm iş emirleri dahil edilir.

5. **Tamam**'a tıklayın.

6. **Gruplandırma ölçütü...** eylem bölmesi gruplarında, hesaplamanın gerekli ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın. Seçilen eylem bölmesi düğmeleri vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

Aşağıdaki şekil, **İş emri tarih denetimi** içinde hesaplama sonuçlarının bir örneğini gösterir.

![Şekil 3](media/03-controlling-and-reporting.png)

- **Ortalama başlangıç gecikmesi** alanı, fiili başlangıç tarihiyle karşılaştırıldığında bir iş emri için planlanan başlangıç tarihi arasındaki farkı gösterir. Örneğin, gerçek başlangıç tarihi planlanan başlangıç tarihinden iki gün önce ise, bu alanda "-2" görüntülenir.  
- **Ortalama bitiş gecikmesi** alanı, fiili bitiş tarihiyle karşılaştırıldığında bir iş emri için planlanan bitiş tarihi arasındaki farkı gösterir. Örneğin, gerçek bitiş tarihi planlanan bitiş tarihinden üç gün sonra ise, bu alanda "3" görüntülenir.  
- **Oluşum** alanları, planlanan ve fiili başlangıç tarihiyle ilişkili olarak sapmalarının kaç kere yinelendiğini ve iş emrindeki zamanlanan ve gerçek bitiş tarihini gösterir.
