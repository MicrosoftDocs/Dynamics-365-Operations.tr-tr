---
title: Regulatory Configuration Service (RCS) kurulumu
description: Bu makalede, Regulatory Configuration Service'ın (RCS) nasıl ayarlanacağı açıklanmaktadır.
author: gionoder
ms.date: 10/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 32ced98925ee66e02f0b073b4acbd586666ac20c
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710794"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Regulatory Configuration Service (RCS) kurulumu

[!include [banner](../includes/banner.md)]

Bu makalede, Regulatory Configuration Service'ın (RCS) nasıl ayarlanacağı açıklanmaktadır.

## <a name="turn-on-globalization-features"></a>Genelleştirme özellikleri açma

1. RCS hesabınızda oturum açın.
2. **Özellik yönetimi** kutucuğunu seçin.
3. **Özellik Yönetimi** çalışma alanında, listeden **Genelleştirme özellikleri**'ni seçin ve **Şimdi etkinleştir**'i seçin.

**Genelleştirme özellikleri** çalışma alanı için bir kutucuk, artık ana RCS panosunda görünmelidir.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Elektronik faturalamayla RCS entegrasyonu için parametreleri ayarlama

1. **Genelleştirme özellikleri** çalışma alanındaki **İlgili ayarlar** bölümünde, **Elektronik raporlama parametreleri**'ni seçin.
2. Parametreleri ilk defa ayarladığınızda Life Cycle Services'a (LCS) bağlanmanız istenir. **Lifecycle Services'a bağlanmak için buraya tıklayın**'ı seçin ve bağlantı kurulduğunda **Tamam** seçeneğini belirleyin.

    > [!IMPORTANT]
    > Veri ikametinin uygulandığı ülke veya bölgelerde ve RCS'niz LCS'nin sağlandığı farklı bir bölgede sağlandıysa RCS'de şu bağlantı hatası iletisini alabilirsiniz: "İstek URI'si ile eşleşen HTTP kaynağı bulunamadı". **Tamam**'ı seçin. RCS'de başka bir hata iletisi alabilirsiniz. "Dynamics Lifecycle Services için () kullanıcısı adına kullanıcı belirteci oluşturulamadı. Lütfen sistem yöneticinize başvurun."
    >  
    > Bunun nedeni, LCS'nin global bir hizmet olması ve bir ABD bölgesinde sağlanmasıdır. Veri ikamet politikası nedeniyle geçerli bölgenizdeki RCS, LCS'ye bağlanamıyor. Bu koşullar altında 2 olası çözüm vardır:
    > - RCS'yi geçerli bölgenizden silin ve ABD bölgesinde yeniden oluşturun.
    > - Hataları yoksayıp Elektronik faturalama kurulumu ile devam edin. Bu hataların Elektronik faturalama işlevi üzerinde etkisi yoktur.

3. **Elektronik Faturalama** sekmesinde, **Hizmet uç noktası URI**'sı alanına aşağıdaki tabloda gösterildiği gibi Microsoft Azure coğrafyanız için uygun hizmet uç noktasını girin.

    | Veri merkezi Azure coğrafyası | Hizmet uç noktası URI'si |
    |----------------------------|----------------------|
    | Amerika Birleşik Devletleri              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Avrupa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Birleşik Krallık             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asya                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japonya                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | İsviçre                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Brezilya                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Birleşik Arap Emirlikleri       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Avustralya                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Kanada                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Fransa                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Hindistan                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Norveç                     | <p>`https://gw.no-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Güney Afrika               | <p>`https://gw.za-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. **0cdb527f-a8d1-4bf8-9436-b352c68682b2** sabit değerini inceleyin ve **Başvuru kodu** alanına girin. Yalnızca genel benzersiz bir tanımlayıcının (GUID) girildiğinden ve değerin boşluk, virgül, nokta veya tırnak işareti gibi herhangi bir simge içermediğinden emin olun.
4. **LCS Ortam Kimliği** alanına Microsoft Dynamics Lifecycle Services (LCS) ortamınızın kimliğini girin. Bu değer, Elektronik Faturalama servisi ile kullanacağınız Finance veya Supply Chain Management ortamına başvurudur. Kimliğinizi almak için [LCS](https://lcs.dynamics.com/)'de oturum açın ve sonra **Ortam yönetimi** sekmesindeki **Ortam ayrıntıları** bölümünde **Ortam kimliği** alanına bakın.

    > [!IMPORTANT]
    > Elektronik Faturalama eklentisi LCS'de birden çok Finance veya Supply Chain Management ortamına yüklenmişse, en son yüklenen ortamın ortam kimliğini her zaman kullanın. Elektronik Faturalama işlevlerini kurup kullandıktan sonra eklentiyi yeni bir ortama yüklemeye karar verirseniz, RCS'deki **LCS Ortam Kimliği** alanını en son değere güncelleştirin.

5. **Kaydet**'i seçip sayfayı kapatın.

## <a name="configuration-providers"></a>Konfigürasyon sağlayıcıları

Elektronik raporlama işlemlerinde ve sahiplerin Genelleştirme özelliklerinde kullanılan Elektronik Raporlama (ER) konfigürasyonlarının sahiplerini ayırt etmek için konfigürasyon sağlayıcılarını kullanabilirsiniz. Microsoft tarafından sağlanan ve genel havuzda yayınlanan tüm Genelleştirme özellikleri için, yapılandırma sağlayıcısı **Microsoft** (`http://microsoft.com` ) olarak ayarlanır.

Yalnızca etkin konfigürasyon sağlayıcısına ait olan ER konfigürasyonlarını ve genelleştirme özelliklerini ayarlayabilirsiniz. Bu yapılandırmaları ve özellikleri, etkin konfigürasyon sağlayıcısına ait konfigürasyon ve özellikleri oluşturmak için şablon olarak kullanabilirsiniz; böylece bunları ayarlayabilirsiniz.

Öncelikle, yapılandırma sağlayıcılarını oluşturun. Ardından, bunlardan birini etkin olarak ayarlayın. **Microsoft** konfigürasyon sağlayıcısını etkin olarak ayarlayamazsınız.

### <a name="create-a-configuration-provider"></a>Bir yapılandırma sağlayıcısı oluşturma

1. **Elektronik raporlama** çalışma alanında, **İlgili bağlantılar**  bölümünde, **Yapılandırma sağlayıcıları**'nı seçin.
2. **Yeni**'yi seçin.
3. Yapılandırma sağlayıcısı için **Ad** alanına benzersiz bir ad girin.
4. **Internet adresi** alanına, yapılandırma sağlayıcısının benzersiz URL'sini girin.
5. **Kaydet**'i seçip sayfayı kapatın.

### <a name="select-a-configuration-provider-as-active"></a>Bir yapılandırma sağlayıcısını etkin olarak seçin

1. Konfigürasyon sağlayıcıları listesinde, etkin olarak ayarlamak istediğiniz konfigürasyon sağlayıcısını seçin.
2. **Etkin olarak ayarla**'ya tıklayın.

## <a name="import-er-configurations-from-the-global-repository"></a>Genel depodan ER yapılandırmalarını içe aktarma

1. **Elektronik raporlama** çalışma alanında, **İlgili bağlantılar**  bölümünde, **Yapılandırma sağlayıcıları**'nı seçin.
2. Yapılandırma sağlayıcıları listesinde **Microsoft**'u seçin ve ardından **Depolar**'ı seçin.
3. **Genel**'i seçin ve ardından eylem bölmesinde **Aç**'ı seçin.
4. Aşağıdaki ER modellerini içe aktarma:

    - **Müşteri faturası bağlam modeli**
    - **Fatura modeli**
    - **Mali belgeler** (gerekirse Brezilya senaryoları için)
    - **Yanıt iletisi modeli**

5. **Fatura modeli eşlemesi** otomatik olarak içe aktarılmamışsa, içe aktarın.
6. Sayfayı kapatın.
