---
title: IoT Zekası için senaryo kurulumu
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management uygulamasında IoT Zekası için senaryoların nasıl yapılandırılacağını açıklamaktadır.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2927a976c38e9ed8166c62b030d665a159119ae1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826431"
---
# <a name="scenario-setup-for-iot-intelligence"></a>IoT Zekası için senaryo kurulumu

[!include [banner](../../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Supply Chain Management uygulamasında IoT Zekası için senaryoların nasıl yapılandırılacağını açıklamaktadır. Senaryoları ayarlamadan önce, [Microsoft Dynamics Lifecycle Services (LCS) ayarlamanız](iot-lcs-setup.md) gerekir.

Bu konuda, **Ekipman kesinti süresi** senaryosunu bir makine arızalandığında Supply Chain Management'ta bildirim oluşturulacak şekilde yapılandıracaksınız. Bu konu ayrıca, bir maddenin özniteliği belirli bir aralığın dışında olduğunda bir bildirimin oluşturulması için **Ürün kalite** senaryosunun nasıl yapılandırılacağını ve üretim verimi bir eşik değerinin altına düştüğünde bir bildirim üretilmesi için **Üretim gecikmeleri** senaryosunun nasıl yapılandırılacağını açıklar.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Supply Chain Management'ta Ekipman kesinti süresi senaryosunu yapılandırma

**Ekipman kesinti süresi** senaryosu, bir **PartOut** sinyalini makine uyarı eşiğine eşler. Makine, yalnızca senaryo için seçildiğinde ve Supply Chain Management içinde **Çalışıyor** olarak ayarlandığında izlenir. Makineden son alınan **PartOut** sinyalinden bu yana geçen süre, uyarı eşiğinden büyükse **Makine arızası** bildirimi tetiklenir. Makine hala çalışıyorsa bir sonraki **PartOut** sinyali alındığında **Makine devrede** bildirimi tetiklenir. Makine, 30 dakika boyunca arızada kalırsa yeni bir **Makine arızası** bildirimi tetiklenir.

**Ekipman kesinti süresi** senaryosu, aşağıdaki bağımlılıklara sahiptir:

+ Uyarının tetiklenmesi için eşlenmiş bir makinede üretim emri çalışıyor olmalıdır.
+ Eşlenmiş bir makinenin **PartOut** sinyalini temsil eden bir sinyal, benzersiz bir özellik adıyla IoT Hub'a gönderilmelidir ve benzersiz bir ad eklenmelidir.
+ Değerin milisaniye (MS) olarak ifade edildiği bir UNIX **zaman damgası** özelliği, Azure IoT Hub iletisinde bulunmalıdır.

Senaryoyu yapılandırmak için şu adımları izleyin.

1. Supply Chain Management'ta oturun açın.
2. IoT Zekası özellik bayrağını etkinleştirin. Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
3. Ölçümleri yapılandırın. Daha fazla bilgi için bkz. [Ölçümleri yapılandıma](iot-metrics-setup.md#configure-metrics).
4. **Üretim denetimi \> Kurulum \> IoT Zekası \> Senaryo Yönetimi** seçeneğine gidin.
6. **Ekipman kesinti süresi** kutusunda yapılandırma sihirbazını açmak için **Yapılandır**'ı seçin.

   Sihirbazı ilk sayfası **Ekipman sensörü şema tanımı** sayfasıdır. Bu sayfada, amaç, IoT Hub iletilerindeki JavaScript nesne gösterimi (JSON) biçimiyle eşleşmesi için Supply Chain Management içerisinde şemayı ayarlamak olacaktır. Birden çok ileti şeması tanımlanabilir. Daha fazla bilgi için bkz. [IoT Hub iletilerinde şema biçimleri](iot-schema-format.md). Bu örnekte ileti yükü, aşağıdaki biçimi içeren bir toplu iletileri içerir.

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Tabloya bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    1. **Şema adı** alanını **Kod** olarak ayarlayın.
    2. **Şema yolu** alanını **/payload\[\*\]/id** olarak ayarlayın.
    3. **Açıklama** alanını **İleti kodu** olarak ayarlayın.

8. Tabloya başka bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    1. **Şema adı** alanını **Zaman damgası** olarak ayarlayın.
    2. **Şema yolu** alanını **/payload\[\*\]/timestamp** olarak ayarlayın.
    3. **Açıklama** alanını **İleti zaman damgası** olarak ayarlayın.

9. Tabloya başka bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    1. **Şema adı** alanını **Değer** olarak ayarlayın.
    2. **Şema yolu** alanını **/payload\[\*\]/value** olarak ayarlayın.
    3. **Açıklama** alanını **İleti değeri** olarak ayarlayın.

    > [!NOTE]
    > İletideki tüm özellikleri tanımlamanız gerekmez. Yalnızca gereksinim duyduğunuz özellikleri tanımlayın. Önceki adımlarda, **Kök zaman damgası** için bir satır oluşturmadınız. **Kök zaman damgası** yolu **/timestamp** olacaktır.

10. **Ekipman sensörü şema tanımı** sayfasına gitmek için **İleri**'yi seçin.
11. **Ekipman kaynak kodu** satırında **Şema adı** alanında **Kod** öğesini seçin.
12. **UTC saati** satırında **Şema adı** alanında **Zaman damgası** öğesini seçin.
13. **Parça üretildi sinyali** satırında **Şema adı** alanında **Değer** öğesini seçin.
14. **Ekipman kaynağı kod yapılandırması** sayfasına gitmek için **İleri**'yi seçin.
15. IoT Hub iletide değerleri Supply Chain Management kaynaklarıyla eşlemek için şu adımları izleyin:

    1. **Sinyal Veri Değerleri** tablosunda yeni bir satır ekleyin. **Değer** alanında **IoTInt.Machine1225.PartOut** değerini girin. Bu değer, IoT Hub iletisindeki JSON **id** özelliğinden gelir.
    2. **Kaydet**'i seçin.
    3. **İş Kaydı Eşleme** tablosunda **Yeni**'yi seçin. **İş kaydı türü** alanı için varsayılan değer otomatik olarak doldurulmuştur ve değiştirmenize gerek yoktur.
    4. **İş kaydı** alanında, bu sinyal değerinin gönderildiği Supply Chain Management makine kaynağını seçin.
    5. **Kaydet**'i seçin.
    6. **Machine1226** için yeni bir iş kaydı eşlemesi eklemek için bu adımları tekrarlayın. Birden çok sinyal veri değerini Supply Chain Management'ta tek bir kayda eşleyebilirsiniz.

16. İşlemek istediğiniz makineleri seçmek için **Seçili** sütununu kullanın. Tüm sinyal değerlerini tanımlamanız ve tüm makineleri seçmeniz gerekmez.
17. **Parça üretildi sinyali yapılandırması** sayfasına gitmek için **İleri** düğmesini seçin.
18. **Sinyal Veri Değerleri** tablosuna bir satır ekleyin ve **Değer** alanını **Doğru** olarak ayarlayın. Bu değer, IoT Hub iletisindeki JSON **value** özelliğinden gelir. Senaryonuz için gereksinim duyduğunuz kadar değer ekleyebilirsiniz.
19. **Kaydet**'i seçin.
20. **Ekipman kesinti süresi eşiği** sayfasına gitmek için **İleri**'yi seçin. Listelenen makineler, daha önce sinyal değerlerine eşlenen makinelerdir. Bu sayfada, bir makinenin arızalı olup olmadığını belirlemek için bir eşik tanımlarsınız. Örneğin eşiği **10** olarak ayarlarsanız, 10 dakika boyunca bir makineden **PartOut** sinyali gelmediğinde Supply Chain Management bir bildirim oluşturur.
21. **Senaryoyu etkinleştir** sayfasına gitmek için **İleri**'yi seçin. Profili etkinleştirmek için seçeneği ayarlayın.
22. **Bitir**'i seçin.

Senaryo kurulumu artık tamamlandı. IoT Zekası, IoT Hub iletilerini otomatik olarak işlemeye başlayacaktır.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Supply Chain Management'ta Ürün kalitesi senaryosunu yapılandırma

Maddenin özelliği, belirtilen aralığın dışındaysa **Ürün kalitesi** senaryosu bir bildirim oluşturur. Örneğin, bir sensör her maddenin ağırlığını IoT Hub'a gönderir. Supply Chain Management'ta, madde çok ağır veya çok hafifse bir bildirim oluşturulur.

**Ürün kalitesi** senaryosu, aşağıdaki bağımlılıklara sahiptir:

+ Uyarının tetiklenebilmesi için bir üretim emrinin eşlenmiş bir makinede çalışması ve eşlenen toplu iş özniteliğe sahip bir ürün üretmesi gerekir.
+ Toplu iş özniteliğini temsil eden bir sinyal IoT Hub'a gönderilmelidir ve benzersiz özellik adı eklenmelidir.
+ Değerin milisaniye (MS) olarak ifade edildiği bir UNIX **zaman damgası** özelliği, IoT Hub iletisinde bulunmalıdır.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Supply Chain Management'ta Üretim gecikmeleri senaryosunu yapılandırma

Üretim iş çıkarma yeteneği bir eşik değerinin altına düşerse **Üretim gecikmeleri** senaryosu bir bildirim oluşturur. Bu senaryoda, üretilen her madde için IoT Hub'a bir **PartOut** sinyali gönderilir. Supply Chain Management içinde, sipariş gecikmesi üretim emrinin çalışmak üzere zamanlandığı zaman miktarına, üretilmesi gereken maddelerin sayısına, işin çalıştığı sürenin miktarına ve teslim alınan **PartOut** sinyallerin sayısına bağlı olarak hesaplanır. İş için **PartOut** sinyallerinin sayısı beklenen eşik değerinin altına düşerse bir gecikme bildirimi oluşturulur.

**Üretim gecikmeleri** senaryosu, aşağıdaki bağımlılıklara sahiptir:

+ Uyarının tetiklenmesi için eşlenmiş bir makinede üretim emri çalışıyor olmalıdır.
+ Eşlenmiş bir makinenin **PartOut** sinyalini temsil eden bir sinyal, benzersiz bir özellik adıyla Azure IoT Hub'a gönderilmelidir ve benzersiz bir ad eklenmelidir.
+ Değerin milisaniye (MS) olarak ifade edildiği bir UNIX **zaman damgası** özelliği, IoT Hub iletisinde bulunmalıdır.

## <a name="disable-a-scenario"></a>Senaryoyu devre dışı bırakma

Senaryoyu devre dışı bırakmak için şu adımları izleyin.

1. Supply Chain Management'ta **Üretim denetimi \> Kurulum \> IoT Zekası \> Senaryo yönetimi**'ne gidin.
2. Senaryonun kutusundan **Yapılandır**'ı seçin.
3. Son sihirbaz sayfasına gitmek için **İleri**'yi seçin.
4. Profili devre dışı bırakmak için seçeneği ayarlayın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]