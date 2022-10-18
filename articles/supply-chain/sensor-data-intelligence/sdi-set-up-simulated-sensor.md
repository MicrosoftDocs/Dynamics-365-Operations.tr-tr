---
title: Test için simüle edilmiş bir sensör ayarlama
description: Bu makalede, herhangi bir fiziksel sensör takmadan Sensör Veri Yönetim Bilgileri'ni test etmek için kullanabileceğiniz bir simülatörün nasıl ayarlanacağı açıklanmaktadır.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc8bd020a53214abab28ec51ffc6d6be74979932
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643989"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>Test için simüle edilmiş bir sensör ayarlama

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Herhangi bir fiziksel sensör takmadan Sensör Veri Yönetim Bilgileri'ni test etmek istiyorsanız sensör sinyallerini taklit etmek ve bunları Microsoft Azure'daki Nesnelerin İnterneti (IoT) çözümünüze göndermek için *Raspberry PI Azure IoT Online Simulator* hizmetini kullanabilirsiniz. Simülatör hakkında daha fazla bilgi için bkz. [Raspberry Pi çevrimiçi simülatörünü Azure IoT Hub'a (Node.js) bağlama](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started).

## <a name="video-instructions"></a>Video yönergeleri

Aşağıdaki videoda test için sensör simülasyonunun nasıl ayarlanacağı gösterilmektedir. Aynı yönergeler, bu makalenin geri kalan bölümlerinde metin şeklinde sunulmuştur.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>Azure IoT Hub'da cihaz oluşturma

Azure IoT Hub'da sensör sinyallerinin kimliğini doğrulamak için önce bir cihaz ayarlamanız gerekir.

1. Azure'da, Sensör Veri Yönetim Bilgileri ile kullanılmak üzere oluşturduğunuz kaynak grubunun kaynak listesine gidin. (Daha fazla bilgi için bkz. [Azure'da IoT çözümü dağıtma](sdi-deploy-iot-solution-on-azure.md).)
1. Kaynak listesinde, **Tür** alanının *IoT Hub* olarak ayarlandığı kaydı bulun. **Ad** sütununda, kaynağın ayrıntılar sayfasını açmak için adı seçin.
1. Soldaki gezinti bölmesinde, **Cihazlar**'ı seçin.
1. **Cihazlar** sayfasında **Cihaz ekle**'yi seçin.
1. **Cihaz oluşturun** sayfasında, aşağıdaki alanları ayarlayın:

    - **Cihaz Kimliği**: Yeni cihaz için bir ad girin (örneğin, *My-IoT-Device*).
    - **Kimlik doğrulaması türü**: *Simetrik anahtarlar*'ı seçin.
    - **Anahtarları otomatik oluştur**: Bu onay kutusunu seçin.
    - **Bu cihazı bir IoT hub'ına bağla**: *Etkinleştir*'i seçin.

1. **Cihazlar** sayfasına dönmek için **Kaydet**'i seçin.
1. Listeden yeni cihazı bulun. **Cihaz Kimliği** sütununda, cihazın ayrıntılar sayfasını açmak için adı seçin. Yeni cihazı listede görmüyorsanız sayfayı yenileyin.
1. **Birincil bağlantı dizesi** değerini kopyalayın (örneğin, **Panoya kopyala** düğmesini seçerek). Bu değere daha sonra sensör sinyallerini taklit etmek için Raspberry Pi IoT simülatörünü ayarladığınızda ihtiyacınız olacaktır. Bu nedenle, şimdilik bir metin dosyasına yapıştırabilirsiniz.

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>Azure bağlantı dizesini Raspberry Pi IoT simülatörüne ekleme

Azure IoT Hub'daki cihazdaki bağlantı dizesini Raspberry hizmetindeki betiğe eklemek için aşağıdaki adımları izleyin.

1. [Raspberry Pi IoT simülatörünü](https://azure-samples.github.io/raspberry-pi-web-simulator/) açın.
1. Kod düzenleyicisi bölmesinde, aşağıdaki komutu içeren satırı bulun.

    `const connectionString = '[Your IoT hub device connection string]';`

1. Parantezler de dahil olmak üzere yardım metnini, önceki bölümde kopyaladığınız **Birincil bağlantı dizesi** değeriyle değiştirin. Sonuç, aşağıdaki örneğe benzeyecektir.

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>Raspberry Pi IoT simülatöründeki yüke sensör kimlikleri ve değerler ekleme

Şimdi Raspberry Pi IoT simülatörünü simüle edilmiş sensörlerle ve yük olarak gönderecekleri değerlerle ayarlamanız gerekir.

- Raspberry Pi IoT simülatörünün kod düzenleyicisinde `getMessage` işlevini bulun ve aşağıdaki kodla eşleşecek şekilde düzenleyin. (Sensörler `cb()` satırlarında ayarlanmıştır.)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > Raspberry Pi IoT simülatörünün kod düzenleyicisinde tanımlanan sensör kimlikleri, daha sonra Supply Chain Management'taki senaryolar için belirteceğiniz sensör kimlikleriyle aynı olmalıdır. Önceki örnek kod, insan tarafından okunabilir sensör kimliklerini kullanır. Ancak, gerçek bir senaryoda, sensör kimlikleri sensör üreticisi tarafından sağlanan genel benzersiz tanımlayıcı (GUID) değerleri olacaktır. Bu örnek kodda kullanılan insan tarafından okunabilir sensör kimlikleri, [Ürün kalitesi senaryosu](sdi-scenario-product-quality.md), [Varlık bakım senaryosu](sdi-scenario-asset-maintenance.md), [Üretim gecikmeleri senaryosu](sdi-scenario-production-delays.md) ve [Makine durumu senaryosundaki](sdi-scenario-equipment-downtime.md) örneklerde de kullanılır. Bu nedenle, bu senaryolar üzerinde çalışacaksanız bu kodu kullanın.

## <a name="edit-the-interval-for-sending-sensor-signals"></a>Sensör sinyallerini gönderme aralığını düzenleme

Şimdi Raspberry Pi IoT simülatörün simüle edilmiş sensör sinyallerini göndermesi gereken aralığı ayarlamanız gerekir.

1. Raspberry Pi IoT simülatörünün kod düzenleyicisinde aşağıdaki işlev çağrısını bulun.

    `setInterval(sendMessage, 2000);`

2. Varsayılan olarak, Raspberry Pi IoT simülatörü her 2.000 milisaniyede (iki saniye) bir sensör sinyali gönderir. Değerleri istediğiniz gibi düzenleyebilirsiniz.

## <a name="run-the-raspberry-pi-iot-simulator"></a>Raspberry Pi IoT simülatörünü çalıştırma

- Simülatörü başlatmak ve simüle edilmiş sensör verilerini göndermeye başlamak için **Çalıştır**'ı seçin.
