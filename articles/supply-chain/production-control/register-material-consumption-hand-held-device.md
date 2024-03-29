---
title: Mobil cihaz kullanarak malzeme tüketimini kaydetme
description: Bu makale, bir taşınabilir aygıt kullanarak üretimdeki ham madde tüketimini kaydetmeyi sağlayan bir iş akışını açıklar.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1dbc399eb06d1049950bbdd755b479ef275563
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849256"
---
# <a name="register-material-consumption-using-a-mobile-device"></a>Mobil cihaz kullanarak malzeme tüketimini kaydetme

[!include [banner](../includes/banner.md)]

Bu makale, bir taşınabilir aygıt kullanarak üretimdeki ham madde tüketimini kaydetmeyi sağlayan bir iş akışını açıklar.

## <a name="introduction"></a>Giriş

Bu iş akışı malzeme izlenebilirliği için sıkı bir gereksinim varsa geçerlidir. Bu gibi durumlarda, malzemelerin izlenebilirliğini korumak için tam saat ve miktar tüketim için bildirilmelidir. Bu işlem, kayıt zamanı ile gerçek tüketimin gerçekleştiği zaman arasında bir denkleştirme bulunan önce veya sonra otomatik tüketim işleminin tersi olarak görülebilir. Bu, izlenebilirlik gereksinimleri olan bazı maddeler için neden otomatik tüketimi stratejisi kullanılamayacağını açıklar. Taşınabilir cihaz kullanarak üretimdeki ham madde tüketimi kaydını etkinleştirmek için bir iş akışının nasıl ayarlanacağını açıklayan basit bir senaryoya bakalım. [![bir taşınabilir cihaz kullanarak hammadde tüketimi kaydını etkinleştirmek için iş akışını ayarlama.](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a>Senaryo ayrıntıları

Sürekli üretim işlemi (5) toplu iş tarafından denetlenen hammadde RM-100'ü tüketir. Yerleşimde PL-1 plakası üzerinde eldeki malzeme Toplu-001 (1)'dir, her birinin miktarı 100 lbs olan B1 ve B2 toplu işleri mevcuttur. Ambar işi (2) RM-100 için serbest bırakılır ve işlenir ve malzeme plaka denetimsiz olarak tanımlanan PIL-01(3) imalat giriş yerleşimine Toplu-001'den çekilir. Makine operatörü üretim giriş yerinden (3) gelen malzemeyi tartar ve ağırlığı ve toplu iş numarasını (4) tüketildi olarak kaydeder. Üretim giriş yerleşiminden, malzemenin bir bölümü tanımlanan zaman aralıklarına el ile üretim işlemine eklenir. Makine operatörü malzemeyi eklediği zaman, tartıda ölçülür ve toplu iş numarası kaydedilir.

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a>Taşınabilir bir cihaz kullanarak tüketimi kaydetmek için iş akışı ayarlama
Ürün reçetesinde toplu iş denetimli ham madde RM-100 bulunan bir tamamlanmış bir ürün oluşturun. Yerleşime miktarı 100 olan iki RM-100 toplu işi (B1 ve B2) ekleyin: PL-1 plakasında Toplu-001. RM-100 için ürün reçetesi satırındaki otomatik tüketim ilkesi **El ile** olarak ayarlanır. Üretim girişi yerleşimini PIL-01 olarak ayarlayın. Bunu, ambar 51'de bu yerleşimi varsayılan üretim giriş yerleşimi olarak seçerek yapabilirsiniz.

1.  Yeni bir mobil cihaz menü öğesi oluşturun: 

-    **Menü öğesi adı**: Malzeme tüketimini kaydedin. 
-    **Başlık** - Malzeme tüketimini kaydet. 
-    **Mod** - Dolaylı. 
-    **Etkinlik kodu**: Malzeme tüketimini kaydedin.

2.  Menü öğesini **Üretim Mobil** cihaz menüsüne ekleyin.
3.  Bitmiş ürün için bir üretim emri oluşturun: 

-    **Madde numarası**: FG-100 
-    **Tesis**: 5 
-    **Ambar**: 51 
-    **Miktar** - 150

Üretim emri **Tahmini** ve **Serbest bırakıldı** olur ve ambar işi oluşturulur.

4.  Taşınabilir cihaz için ham madde çekme iş akışını kullanarak işi tamamlayın.

Bu malzemeyi toplu yerleşimden üretim giriş yerleşimi PIL-01'e getirir. İş tamamlandığında, malzemenin durumu **Üretim giriş yerleşiminde çekildi** olur. İş işlendikten sonra durum **Çekildi** veya **Fiziksel olarak rezerve** olabilir. Bu **Ambar formuna koyduktan sonra çıkış durumu** parametresiyle yapılandırılır.

5.  Üretim emrini istemciden veya taşınabilir cihazdan **Üretim başlangıcı** menü öğesini kullanarak başlatın.

Üretim emri başlatıldıktan sonra, taşınabilir cihaz için malzeme tüketimini iş akışıyla kaydedebilirsiniz. Toplu iş B1 için 25 lbs tüketim kaydederek başlayalım.

6.  Taşınabilir cihaz menüsünden **Malzeme** **tüketimini kaydet** menü öğesini seçip aşağıdaki ayrıntıları girin: 

-    Üretim emri numarası. 
-    Malzemenin tüketileceği yerleşim, burada PIL-01. 
-    Madde numarası RM-100. 
-    Toplu iş numarası B1. 
-    Miktar: 25.

7.  **Tamam**'ı seçin.

"Günlük satırı oluşturuldu" iletisi ekranda görünür. Üretim emrinde, RM-100 madde numarası ve B1 toplu iş numarası için **Üretim malzeme çekme listesi** türünde açık bir günlük bulunur. 

Şimdi kaydınıza (örneğin toplu iş numarası B2'de) devam etmeyi seçebilirsiniz ve **Tamam**'ı her seçtiğinizde açık günlüğe yeni bir günlük satırı eklenir. 

Kaydınız tamamladıktan sonra günlüğü deftere nakletmek ve iş akışını sonlandırmak için **Bitti**'yi seçin.

### <a name="additional-comments"></a>Ek açıklamalar 

-   Bir günlük satırı oluşturulduktan sonra kullanıcı bir iş akışını iptal ederse, günlük deftere nakledilmemiş durumda kalır ancak ilerleyen bir noktada kullanıcı aynı üretim emri için iş akışını kullanırsa, satırlar yeni bir günlük yerine açık günlüğe eklenir.
-   Yeni iş akışı seri numaraları kaydını da destekler.
-   Seçilen üretim emri veya toplu iş emri için yalnızca ürün reçetesinde veya formülde tanımlanan bir madde numarası kaydetmek mümkündür.
-   Malzeme fazla tüketilebilir. Örneğin, malzemenin 100 libre miktarında tüketileceği tahmin edilirse, ürün daha fazla miktarda (örneğin 105 libre) tüketilebilir.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]