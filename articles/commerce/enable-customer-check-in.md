---
title: Satış noktasında (POS) müşteri giriş bildirimlerini etkinleştirme
description: Bu makalede, Microsoft Dynamics 365 Commerce satış noktasında (POS) müşteri giriş bildirimlerinin nasıl etkinleştirileceği açıklanmıştır.
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ae53657c95128eae793f670bd9dbc31d9fac0fe4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885157"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Satış noktasında (POS) müşteri giriş bildirimlerini etkinleştirme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce satış noktasında (POS) müşteri giriş bildirimlerinin nasıl etkinleştirileceği açıklanmıştır.

"Sipariş teslim alma için hazır" e-postalarında kuruluşlar, müşterilere, şirket içinde bulunduklarını ve paketin kendilerine teslim edilmesini beklediklerini mağazaya bildirmelerine olanak tanıyan bir bağlantı veya düğme sunabilir. Ardından müşteriler giriş alır ve mağaza, POS uygulamasında görev olarak bir bildirim alır. Bu görev, bir satış temsilcisinin siparişi müşterinin aracına teslim etmesi için bir istem görevi görür. Bu sayede müşterinin mağazaya girmesi gerekmez.

Müşteri girişi iş akışı, müşterilerden, park yeri numarası, araçlarının marka, model ve rengi ile teslimat talimatları gibi ek bilgiler toplamak için de yapılandırılabilir. Perakende mağaza görevlisi, bu bilgileri kullanarak sipariş karşılama işlemini kolaylaştırır.

## <a name="enable-customer-check-in"></a>Müşteri giriş özelliğini etkinleştirme

Müşteri giriş özelliği etkinleştirildiğinde, Commerce bir sipariş onay kodu (kanal referans kodu olarak da bilinir) oluşturur. Ayrıca, satış noktası (POS) veya çağrı merkezi kanalları üzerinden oluşturulan siparişler için de sipariş onay kodları oluşturur. 

Commerce genel merkezde müşteri girişi özelliğini açmak için aşağıdaki adımları izleyin.

1. **Çalışma alanları \> Özellik yönetimi**'ne gidin.
2. **Kanallar arasında tutarlı bir kanal referans kodu biçimi oluştur** özelliğini arayın. 
3. Özelliği seçin, daha sonra özellikler bölmesinde yer alan **Şimdi etkinleştir**'i seçin. 

## <a name="create-a-check-in-confirmation-page"></a>Giriş onayı sayfası oluşturma

E-ticaret sitenizde, giriş onayı deneyimi olarak hizmet verecek yeni bir sayfa oluşturmanız gerekir. Ek yapılandırmalarla sayfaya siparişi karşılama işlemini kolaylaştırmak için müşterilerden ek bilgiler toplayan bir form da ekleyebilirsiniz. Sayfa ve modülün nasıl ayarlanacağı konusunda bilgi için bkz. [Müşteri girişi modülü](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>İşlem tabanlı e-posta şablonunu yapılandırma

Müşterilerin, siparişleri teslim alma için hazır olduğunda aldıkları işlem tabanlı e-posta için şablona bir **Buradayım** bağlantısı veya düğmesi eklemeniz gerekir. Müşteriler, siparişlerini almak üzere geldiklerini mağazaya bildirmek için bu bağlantıyı veya düğmeyi kullanır. 

Bağlantı veya düğmeyi, **Paketleme tamamlandı** bildirimi türü ve yol kenarı sipariş karşılama için kullandığınız teslimat moduna eşlenen şablona ekleyin. Şablonda, oluşturduğunuz giriş onay sayfasının URL'sini belirten ve aşağıdaki örnekte gösterildiği gibi parametre adlarını ve değerlerini içeren bir HTML bağlantısı veya düğmesi oluşturun.

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

E-posta şablonlarını yapılandırma hakkında daha fazla bilgi için bkz. [Teslimat moduna göre işlem tabanlı e-postaları özelleştirme](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>POS'ta bir giriş onayı görevi oluşturuldu

Bir müşteri ürünü mağazadan teslim almaya hazır bulunduğunu söyledikten sonra, giriş sayfasında bir onay iletisi ve müşterinin sipariş onay kodunu içeren isteğe bağlı bir QR kodu gösterilir. Aynı zamanda, müşterinin siparişi aldığı mağaza için POS'taki görevler listesinde bir görev oluşturulur. Bu görev, siparişi yerine getirmek için gereken tüm müşteri ve sipariş bilgilerini içerir. Görevin talimatlar alanında, müşteriden ek bilgi formu aracılığıyla toplanan tüm bilgiler gösterilir.

## <a name="end-to-end-testing"></a>Uçtan uca test

Müşteri girişi, belirli parametrelerin ve değerlerin giriş sayfasına ve ardından müşteri girişi API'sine aktarılmasını gerektirir. Bu nedenle, en kolay yaklaşım, bir test siparişinin oluşturulabileceği ve paketlenebileceği bir ortamda özelliği test etmektir. Bu şekilde, gerekli parametre adlarını ve değerlerini içeren bir URL'ye sahip bir "teslim almaya hazır sipariş" e-postası oluşturulabilir.

Müşteri girişi özelliğini test etmek için şu adımları izleyin.

1. Müşteri girişi sayfasını oluşturun ve ardından müşteri girişi modülünü ekleyip yapılandırın. Daha fazla bilgi için bkz. [Teslim alma için giriş modülü](check-in-pickup-module.md). 
1. Sayfayı iade edin ancak yayınlamayın.
1. Teslim alma modu için paketleme tamamlandı bildirim türünün çağırdıüı bir e-posta şablonuna aşağıdaki bağlantıyı ekleyin. Daha fazla bilgi için bkz. [İşlem tabanlı olaylar için e-posta şablonları oluşturma](email-templates-transactions.md).

    - **Üretim öncesi (UAT) ortamlar için:** Bu makalenin önceki bölümlerindeki [İşlem tabanlı e-posta şablonlarını yapılandırma](#configure-the-transactional-email-template) bölümünde yer alan kod snippet'ini ekleyin.
    - **Üretim ortamları için:** Var olan müşterilerin etkilenmemesi için aşağıdaki yorumlukodu ekleyin.

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. Teslim alma modunun belirtildiği bir sipariş oluşturun.
1. Paketleme tamamlandı bildirim türünün tetiklediği e-postayı aldığınızda, daha önce eklediğiniz URL'yi içeren giriş sayfasını açarak giriş akışını test edin. URL, `&preview=inprogress` bayrağı içerdiğinden, sayfayı görüntülemeden önce kimliğinizi doğrulamanız istenir.
1. Modülü yapılandırmak için gereken tüm ek bilgileri girin.
1. Giriş onayı görünümünün doğru gösterildiğini doğrulayın.
1. Siparişin teslim alınacağı mağaza için bir POS terminali açın.
1. **Teslim alınacak siparişler** kutucuğunu seçin ve siparişin göründüğünü doğrulayın.
1. Giriş modülünde yapılandırılan ek bilgilerin ayrıntılar bölmesinde göründüğünü doğrulayın.

Müşteri girişi özelliğinin uçtan uca çalıştığını doğruladıktan sonra şu adımları izleyin.

1. Giriş sayfasını yayımlayın.
1. Bir üretim ortamında test yapıyorsanız URL'yi "sipariş teslim alınmaya hazır" e-posta şablonunda kullanımdan kaldırarak **Buradayım** bağlantısının veya düğmesinin gösterilmesini sağlayın. Ardından şablonu yeniden yükleyin.

## <a name="additional-resources"></a>Ek kaynaklar

[Teslim modülü için giriş](check-in-pickup-module.md)

[Teslimat şekline göre işlem tabanlı e-postaları özelleştirme](customize-email-delivery-mode.md)

[Hareket olayları için e-posta şablonları oluşturma](email-templates-transactions.md)
