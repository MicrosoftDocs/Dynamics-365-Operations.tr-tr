---
title: Kıymet hata analizi
description: Bu konuda Varlık Yönetimi'ndeki varlık hata analizinde açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f4d7b4a92486287027cba79c43ca5933cce42a1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253866"
---
# <a name="asset-fault-analysis"></a>Kıymet hata analizi

[!include [banner](../../includes/banner.md)]

 

Belirli bir dönemde kaydedilen toplam hata sayısını genel olarak almak için, varlık yönetiminde varlık hata kayıtlarını analiz edebilirsiniz. Örneğin varlıklar, varlık türleri, işlevsel yerleşimler, hata belirtileri veya arıza tipleri üzerinde odak bulunan bir arıza kaydı farklı açılardan analiz edilebilir.

1. **Varlık Yönetimi** > **Sorgular** > **Varlık hatası** > **Varlık hata analizi**'ni tıklatın.

2. **Varlık arıza Analizi hesaplaması** iletişim kutusunda, kıymet arıza satırlarının işlevsel yerleşimleriyle ilgili olmasını istediğiniz ayrıntıları göstermek için **Düzey** alanını kullanabilirsiniz. 

    Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm varlık arızası satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. 
        
    **Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeyinde bulunan tüm varlık arızası satırlarını gösteren ayrıntılı bir sonuç görürsünüz.

3. Aramayı sınırlandırmak istiyorsanız, Hızlı Sekme **dahil edilecek kayıtlar** üzerinde belirli kıymetleri, arıza tarihlerini, arıza nedenlerini ve arıza düzeltme 'leri seçebilirsiniz.

4. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

5. **Varlık arıza analizi** sekmesinde, bir veya daha fazla **Gruplama ölçütü** düğmesine tıklayarak istediğiniz ayrıntı düzeyini görüntüleyin. Etkinleştirilen düğmeler vurgulanır. Düğmelere tıklayarak onları etkinleştirin veya devre dışı bırakın.

6. Seçimlerinizi ekranda göstermek için **Hesaplamaları Güncelleştir**'i tıklatın. 

>[!NOTE]
>**Gruplama ölçütü** düğmesini her etkinleştirdiğinizde veya devre dışı bıraktığınızda, **Hesaplamaları güncelleştir** düğmesine tıklamayı unutmayın. Hata olasılığını yeniden hesaplama sırasında büyük miktarda veri işlendiğinden, bu gereklidir.

## <a name="examples"></a>Örnekler

Arıza kayıtlarını çözümlemenin birçok yolu vardır. Bu bölümde, farklı veri seçimlerinin varlık arıza kayıtları analiz edilirken nasıl daha fazla öngörü sağlayabildiğini gösteren beş örnek bulunmaktadır.

### <a name="group-by-symptoms"></a>Belirtilere göre grupla

Aşağıdaki ekran görüntüsünde yalnızca **Belirti** düğmesi seçilidir.

- Hata kayıtları üç hata belirtiyle yapılmaktadır: "hava sızıntısı", "sigorta yanması" ve "donanım sıkıştı".  
- **Olasılık %** sütununda, tüm yüzdeler %100 kadar toplanır. Olasılık bu arıza Analizi içindeki tüm **belirti** kayıtlarını temel alan bir olasılıktır.

![Şekil 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a>Belirtilere ve döneme göre grupla

Aşağıdaki ekran görüntüsünde , seçili bir dönem içinde hata kayıtlarını nasıl kullanabileceğinizi göstermek için **yıl** ve **ay** eklenir.

- Hata belirtileri şimdi her yıl/ay kaydı olarak gösteriliyor.  
- **Olasılık %** sütununda, her ay için tüm yüzdeleri eklerseniz, bu değerler %100'e kadar toplanır. Olasılık bu arıza Analizi içindeki **belirti** kayıtlarını temel alan bir olasılıktır. Bir kıymette çok sayıda satır varsa, ancak bir satırda büyük bir yüzde değeri varsa, bu hata belirtisiyle ilgili kayıt sayısını sınırlamak için bir yöntem bulmayı daha yakından incelemek amacıyla hata belirtinin göstergesi olacaktır.

![Şekil 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a>Birden çok belirtiye ve varlığa göre grupla

Aşağıdaki üç ekran görüntüsünde gösterilen hesaplamalarda temel olarak kıymet ve kıymet türü birleşimi ayrıntı düzeyinde kullanılmaktadır.  

Genel olarak, **Tarihe göre grupla**, **Varlığa göre grupla**, **İşlem yapılacak yerleşime göre grupla** Eylem Bölmesi gruplarındaki düğmeler ve **Arıza** düğmesi (Hata Kodu), dönem veya varlık ilişkileri içerir. **Belirti**, **Alan**, **Tür**, **Sebep** ve **Çözüm** düğmeleri, arıza yönetiminde kullanılan kategorizasyonlardır ve varlık arıza kayıtlarını analizde ve sorunlu alanları tespitte kullanılır.  

**Belirtiye, varlığa ve varlık türüne göre grupla**

Aşağıdaki ekran görüntüsünde, arıza kayıtları ile ilgili daha ayrıntılı bilgi sağlamak amacıyla **varlık** ve **kıymet türü** eklenmiştir.

- Hata belirtileri şimdi **Varlı** / **Varlık Türü** / **Belirti** kombinasyonlarına ayrılmıştır.  
- **Olasılık %** sütununda, **Varlık** / **Varlık türü** / **Belirti** için tüm yüzdeleri toplanırsanız, her biri %100'e ulaşır. Olasılık bu arıza Analizi içindeki **belirti** kayıtlarını temel alan bir olasılıktır. Bir kıymette çok sayıda satır varsa, ancak bir satırda büyük bir yüzde değeri varsa, bu hata belirtisiyle ilgili kayıt sayısını sınırlamak için bir yöntem bulmayı daha yakından incelemek amacıyla hata belirtinin göstergesi olacaktır.

![Şekil 3](media/08-controlling-and-reporting.png)

**İki belirtiye, varlığa ve varlık türüne göre grupla**

Aşağıdaki ekran görüntüsünde **Alan**, **Belirti**, **Varlık** ve **Varlık türü**'ne eklenerek hata kayıtları için daha fazla ayrıntı sağlar.

- **Olasılık %** sütununda, bir varlıktaki **Varlık** / **Varlık türü** / **Belirti** için tüm yüzdeleri toplanırsanız, her biri %100'e ulaşır. Olasılık, bu hata analizindeki **Belirti** ve **Alan** kombinasyonuna dayanır. Bir kıymette çok sayıda satır varsa, ancak bir satırda büyük bir yüzde değeri varsa, bu hata alanıyla ilgili kayıt sayısını sınırlamak için bir yöntem bulmayı daha yakından incelemek amacıyla hata alanının göstergesi olacaktır.  

![Şekil 4](media/09-controlling-and-reporting.png)

**Üç belirtiye, varlığa ve varlık türüne göre grupla**

Aşağıdaki ekran görüntüsünde **Tür** eklenmiştir ve bu örnekteki en ayrıntılı hesaplama gösterilir.
 
- **Olasılık %** sütununda, bir varlıktaki **Varlık** / **Varlık türü** / **Belirti** için tüm yüzdeleri toplanırsanız, her biri %100'e ulaşır. Olasılık, bu hata analizindeki **Belirti** ve **Alan** ve **Tür** kombinasyonuna dayanır. Bir kıymette çok sayıda satır varsa, ancak bir satırda büyük bir yüzde değeri varsa, bu hata türüyle ilgili kayıt sayısını sınırlamak için bir yöntem bulmayı daha yakından incelemek amacıyla hata türünün göstergesi olacaktır.

![Şekil 5](media/10-controlling-and-reporting.png)


>[!NOTE]
>İş emirlerinde ve bakım taleplerinde oluşturulan tüm arıza kayıtlarının genel bakışı için **Varlık yönetimi** > **Sorgular** > **Varlık arızası** > **Varlık arızaları** üzerine tıklayın. **Varlık arızaları** sayfasında, bir varlık arızası kaydını seçin ve **İlgili bilgi** panosunu genişleterek ilgili iş emri veya bakım talebiyle ilgili bilgiyi görüntüleyin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]