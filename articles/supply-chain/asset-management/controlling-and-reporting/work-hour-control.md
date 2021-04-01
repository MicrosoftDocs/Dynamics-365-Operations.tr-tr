---
title: Çalışma saati denetimi
description: Bu konuda Varlık Yönetimi'nde iş saati denetimini açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 482bee9dba22763a065c8aca93745f53f06f99be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253722"
---
# <a name="work-hour-control"></a>Çalışma saati denetimi

[!include [banner](../../includes/banner.md)]

 

Kıymet yönetiminde, sabit kıymetler, işlevsel yerleşimler ve iş emirleriyle ilgili bütçe saatleriyle karşılaştırıldığında fiili saatlerin genel görünümünü elde etmek için saatleri hesaplayabilirsiniz. Gerçek saatler deftere nakledilen hareketleri temel alarak yapılır.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Kıymetler, işlevsel yerleşimler ve iş emirleri için çalışma saatleri kontrolü

Varlıklar, işlevsel yerleşimler ve çalışma emirleri için oluşturulan hesaplamalar neredeyse aynıdır. Tek fark, varlıklar ve işlem yapılacak konumlar için alt varlıkları ve alt konumları da hesaplamanıza dahil edebiliyor olmanızdır. Tarih, kayıt kaydedildiği hareket tarihidir.

1. **Varlık yönetimi** > **Sorgular** > **Varlıklar** > **Varlık saat denetimi** veya **İşlem yapılacak yerleşim saat denetimi** veya **Varlık yönetimi** > **Sorgular** > **İş emirleri** > **İş emri saat denetimi**'ne tıklayın.

2. **Kıymet saati denetimi** iletişim kutusunda.

3. **Varlık saat denetimi** / **İşlem yapılacak yerleşim saat denetimi** / **İş emri saat denetimi** iletişim kutusunda, **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında hesaplanacak bir dönem seçin.

4. Gerekirse, hesaplamaya dahil edilecek bir **Mali boyut kümesi** seçin.

5. Sıfır saat içeren sonuçları göstermek istemiyorsanız, **sıfır atlama** düğmesi üzerinde "Evet" seçeneğini belirleyin.

6. İşlem yapılacak yerleşimlerle ilgili olarak saat denetimi satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz. 

    Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim hiyerarşiniz varsa, işlem yapılacak yerleşim için tüm saat denetimi satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. 
    
    **Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm saat denetimi satırlarını gösteren ayrıntılı bir sonuç görürsünüz.

7. Alt kıymetlerle ilgili maliyetleri ayrı satırlar olarak göstermek için **alt kıymetleri dahil et** düğmesini seçin.

8. Aramayı sınırlandırmak istiyorsanız, Hızlı Sekme **dahil edilecek kayıtlar** üzerinde belirli varlıkları / işlem yapılacak yerleşimleri / iş emirlerini seçebilirsiniz.

9. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

10. **Varlık saat denetimi** sayfasında, hesaplamanın gerekli ayrıntı düzeyini göstermek için **Gruplama ölçütü** düğmelerine tıklayın. Seçilen **Gruplandırma ölçütü** düğmeleri vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

## <a name="example"></a>Örnek

Aşağıdaki ekran görüntüsü, **Varlık saat denetimi** hesaplamasının birkaç örneğini göstermektedir.

- **Orijinal bütçe** alanı, bütçe saatlerini iş emri tahmininden gösterir. 
- **Fiili saatler** alanı, iş emirlerinde deftere nakledilir. 
- **Taahhüt edilen saatler** alanı, şirketinizin iş siparişleri ile ilgili olarak taahhüt edildiği toplam saat miktarını gösterir.

![Varlık saat denetim hesaplaması örneği](media/04-controlling-and-reporting.png)

Bir saat hesaplaması yapmanın bir başka yolu **Tüm varlıklar** veya **Etkin varlıklar** içinde çoklu varlıkları seçmektir. Daha sonra **Genel** Hızlı Sekmesi üzerinde **Saat denetimi** düğmesine tıklayın. Seçilen varlıklar, hızlı sekme **dahil edilecek kayıtlar** alanındaki **varlık** alanına otomatik olarak eklenir. **Varlık saati kontrol** iletişim kutusunda, **Tamam** üzerine tıklayın ve seçilen varlıklar için hesaplama gösterilir. Aynı işlem **Tüm işlem yapılacak yerleşimler** veya **Etkin işlem yapılacak yerleşimler** içindeki işlem yapılacak yerleşimler ve **Tüm iş emirleri** veya **Etkin iş emirleri** içindeki tüm iş emirleri için kullanılabilir.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]