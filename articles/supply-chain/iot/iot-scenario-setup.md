---
title: IoT Zekası için senaryo kurulumu
description: Bu konuda, IoT Zekası için Supply Chain Management'ta bir senaryonun nasıl yapılandırılacağı açıklanmaktadır.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597180"
---
# <a name="scenario-setup-for-iot-intelligence"></a>IoT Zekası için senaryo kurulumu

[!include [banner](../../includes/banner.md)]

Bu konuda, IoT Zekası için Supply Chain Management'ta bir senaryonun nasıl yapılandırılacağı açıklanmaktadır. Senaryoları ayarlamadan önce [LCS'yi kurmalısınız](iot-lcs-setup.md).

Bu konuda, **Ekipman kesinti süresi** senaryosunu bir makine arızalandığında Supply Chain Management'ta bildirim oluşturacak şekilde yapılandıracaksınız.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Supply Chain Management'ta **Ekipman kesinti süresi** senaryosunu yapılandırma

**Ekipman kesinti süresi** senaryosu, bir parça çıkış sinyalini makine uyarı eşiğine eşler. Makine, yalnızca senaryo için seçildiğinde ve Supply Chain Management içinde çalışmaya ayarlandığında izlenir. Makinenin son alınan Parça Çıkış sinyalinden bu yana geçen süre, uyarı eşiğinden büyükse **Makine arızası** bildirimi tetiklenir. Makine hala çalışıyorsa bir sonraki **PartOut** sinyali alındığında **Makine devrede** bildirimi tetiklenir. Makine, 30 dakika boyunca arızada kalırsa yeni bir **Makine arızası** bildirimi tetiklenir.

**Ekipman kesinti süresi** senaryosu, şu bağımlılıklara sahiptir:

+ Uyarının tetiklenmesi için eşlenmiş bir makinede üretim emri çalışıyor olmalıdır.
+ Eşlenmiş bir makinenin parça çıkış sinyalini temsil eden bir sinyal, benzersiz bir özellik adıyla IoT Hub'a gönderilmelidir.
+ IoT Hub iletisinde bir Unix milisaniye zaman damgası özelliği bulunmalıdır.

Senaryoyu yapılandırmak için şu adımları izleyin:

1. Supply Chain Management'ta oturum açın.
2. IoT Zekası özellik bayrağını etkinleştirin. Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Ölçümleri yapılandırın. Daha fazla bilgi için bkz. [Ölçümleri yapılandıma](iot-metrics-setup.md#configure-metrics).
4. **Üretim denetimi**'ne gidin.
5. **Kurulum \> IoT Zekası \> Senaryo yönetimi**'ne gidin.
6. **Ekipman kesinti süresi** kutucuğunda **Yapılandır**'a tıklayın. Yapılandırma sihirbazı **Ekipman sensörü şema tanımı** sayfası ile başlar. Buradaki amaç, Supply Chain Management'ta şemayı IoT iletilerinin JSON biçimiyle eşleşecek şekilde ayarlamaktır. Birden çok ileti şeması tanımlanabilir. Daha fazla bilgi için bkz. [IoT Hub için ileti şeması biçimleri](iot-schema-format.md). Bu örnekte ileti yükü, şu biçimde bir toplu ileti içerir:

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

7. Tabloya satır ekleyin.

    1. **Şema adı**'nı **Kod** olarak ayarlayın.
    2. **Şema yolu**'nu **/payload[\*]/id** olarak ayarlayın.
    3. **Açıklama**'yı **İleti kodu** olarak ayarlayın.

8. Tabloya satır ekleyin.

    1. **Şema adı**'nı **Zaman damgası** olarak ayarlayın.
    2. **Şema yolu**'nu **/payload[\*]/timestamp** olarak ayarlayın.
    3. **Açıklama**'yı **İleti zaman damgası** olarak ayarlayın.

9. Tabloya satır ekleyin.

    1. **Şema adı**'nı **Değer** olarak ayarlayın.
    2. **Şema yolu**'nu **/payload[\*]/value** olarak ayarlayın.
    3. **Açıklama**'yı **İleti değeri** olarak ayarlayın.

    İletideki tüm özellikleri tanımlamanız gerekmez, yalnızca ihtiyacınız olanları tanımlayın. Bu örnekte, **Kök zaman damgası** için bir satır oluşturmadınız. **Kök zaman damgası** yolu **/timestamp** olacaktır.
  
10. **Ekipman sensörü şema tanımı** sayfasına gitmek için **İleri**'ye tıklayın.
11. **Ekipman kaynak kodu** satırında **Şema adı**'nı **Kod** olarak ayarlayın. Geçerli değerler, bir açılan tabloda görüntülenir.
12. **UTC saati** satırında **Şema adı**'nı **Zaman damgası** olarak ayarlayın. Geçerli değerler, bir açılan tabloda görüntülenir.
13. **Parça üretildi sinyali** satırında **Şema adı**'nı **Değer** olarak ayarlayın. Geçerli değerler, bir açılan tabloda görüntülenir.
14. **Ekipman kaynağı kod yapılandırması** sayfası için **İleri**'yi tıklayın.
15. Bu adımda IoT Hub ileti değerlerini Supply Chain Management kaynaklarıyla eşlersiniz.

    1. **Sinyal Veri Değerleri** tablosuna yeni bir satır ekleyin ve **Değer** sütununa **IoTInt.Machine1225.PartOut** girin. **IoTInt.Machine1225.PartOut** değeri, IoT Hub iletisindeki JSON **kod** özelliğinden gelir.
    2. **Kaydet**'e tıklayın.
    3. **İş Kaydı Eşleme** tablosunda **Yeni**'ye tıklayın. **İş kaydı türü** için varsayılan değer otomatik olarak doldurulmuştur ve değiştirmenize gerek yoktur.
    4. **İş kaydı** sütununda, bu sinyal değerinin gönderildiği Supply Chain Management makine kaynağını seçin.
    5. **Kaydet**'e tıklayın.
    6. **Machine1226** için yeni bir iş kaydı eşlemesi ekleyerek bu adımları tekrarlayın. Birden çok sinyal veri değerini Supply Chain Management'ta tek bir kayda eşleyebilirsiniz.

16. Hangi makineleri işlemek istediğinizi seçmek için **Seçili** sütununu kullanın. Tüm sinyal değerlerini tanımlamanız ve tüm makineleri seçmeniz gerekmez.
17. **Parça üretildi sinyali yapılandırması** sayfasına gitmek için **İleri** düğmesine tıklayın.
18. **Sinyal Veri Değerleri** tablosuna bir satır ekleyin ve **Değer**'i **Doğru** olarak ayarlayın. **Doğru** değeri, IoT Hub iletisindeki JSON **değer** özelliğinden gelir. Senaryonuz için gereksinim duyduğunuz kadar değer ekleyebilirsiniz.
19. **Kaydet**'e tıklayın.
20. **Ekipman kesinti süresi eşiği** sayfasına gitmek için **İleri**'ye tıklayın. Listelenen makineler, daha önce sinyal değerlerine eşlenen makinelerdir. Bu adımda, bir makinenin arızalı olup olmadığını belirlemek için bir eşik tanımlarsınız. Örneğin eşiği 10 olarak ayarlarsanız, 10 dakika boyunca bir makineden parça çıkışı mesajı yoksa Supply Chain Management bir bildirim oluşturur.
21. **Senaryoyu etkinleştir** sayfasına gitmek için **İleri**'ye tıklayın. Senaryoyu etkinleştirmek için kaydırıcıyı kaydırın.
22. **Son** düğmesine tıklayın.

Senaryo kurulumu tamamlandı. IoT Zekası, IoT Hub iletilerini otomatik olarak işlemeye başlayacaktır.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Supply Chain Management'ta **Ürün kalitesi** senaryosunu yapılandırma

Maddenin özelliği, belirtilen aralığın dışındaysa **Ürün kalitesi** senaryosu bir bildirim oluşturur. Örneğin, bir sensör her maddenin ağırlığını IoT Hub'a gönderebilir. Supply Chain Management'ta, madde çok ağır veya çok hafifse bir bildirim oluşturulur.

Senaryo şu bağımlılıklara sahiptir:

+ Uyarının tetiklenmesi için bir Üretim Emri'nin eşlenmiş bir makinede çalışması ve eşlenen toplu iş özniteliğe sahip bir ürün üretmesi gerekir.
+ Toplu iş özniteliğini temsil eden bir sinyal, benzersiz bir özellik adıyla IoT Hub'a gönderilmelidir.
+ IoT Hub iletisinde bir Unix milisaniye zaman damgası özelliği bulunmalıdır.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Supply Chain Management'ta **Üretim gecikmeleri** senaryosunu yapılandırma

Üretim iş çıkarma yeteneği bir eşik değerinin altına düşerse **Üretim gecikmeleri** senaryosu bir bildirim oluşturur. Bu senaryoda, üretilen her madde için IoT Hub'a bir **PartOut** sinyali gönderilir. Supply Chain Management'ta sipariş gecikmesi; üretim emrinin çalışması planlanan süre, üretilmesi gereken madde sayısı, işin ne kadar süredir çalıştığı ve **PartOut** sinyali alınma sayısına göre hesaplanır. İş için **PartOut** sinyallerinin sayısı beklenen eşik değerinin altına düşerse bir gecikme bildirimi oluşturulur.

Senaryo şu bağımlılıklara sahiptir:

+ Uyarının tetiklenmesi için eşlenmiş bir makinede Üretim Emri çalışıyor olmalıdır.
+ Eşlenmiş bir makinenin parça çıkış sinyalini temsil eden bir sinyal, benzersiz bir özellik adıyla IoT Hub'a gönderilmelidir.
+ IoT Hub iletisinde bir Unix milisaniye zaman damgası özelliği bulunmalıdır.

## <a name="how-to-disable-a-scenario"></a>Senaryoyu devre dışı bırakma

Senaryoyu devre dışı bırakmak için şu adımları izleyin:

1. Supply Chain Management'ta **Üretim denetimi \> Kurulum \> IoT Zekası \> Senaryo yönetimi**'ne gidin.
2. Senaryoda **Yapılandır**'a tıklayın.
3. Son sihirbaz sekmesine ulaşmak için **İleri**'ye tıklayın.
4. Senaryoyu devre dışı bırakmak için kaydırıcıyı kaydırın.
