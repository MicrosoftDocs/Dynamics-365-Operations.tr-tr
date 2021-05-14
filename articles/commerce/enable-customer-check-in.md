---
title: Satış noktasında (POS) müşteri giriş bildirimlerini etkinleştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce satış noktasında (POS) müşteri giriş bildirimlerinin nasıl etkinleştirileceği açıklanmıştır.
author: bicyclingfool
ms.date: 04/23/2021
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
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937624"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Satış noktasında (POS) müşteri giriş bildirimlerini etkinleştirme

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce satış noktasında (POS) müşteri giriş bildirimlerinin nasıl etkinleştirileceği açıklanmıştır.

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

Bağlantı veya düğmeyi, **Paketleme tamamlandı** bildirimi türü ve yol kenarı sipariş karşılama için kullandığınız teslimat moduna eşlenen şablona ekleyin. Şablonda, oluşturduğunuz giriş onay sayfasının URL'sine yönlendiren bir HTML bağlantısı veya düğme oluşturun. Aşağıda bir örnek verilmiştir.

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
E-posta şablonlarını yapılandırma hakkında daha fazla bilgi için bkz. [Teslimat moduna göre işlem tabanlı e-postaları özelleştirme](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>POS'ta bir giriş onayı görevi oluşturuldu

Müşteri mağazaya, teslim alma için geldiklerini bildirdiklerinde bir giriş onayı bildirimi alırlar ve POS'ta, müşterinin siparişi almak için geldiği mağaza için görevler listesinde bir görev oluşturulur. Görev, siparişi yerine getirmek için gerekli tüm müşteri ve sipariş bilgilerini içerir. Görev içinde, talimatlar alanında, ek bilgiler formu aracılığıyla müşteriden toplanan tüm bilgiler gösterilir. 

## <a name="additional-resources"></a>Ek kaynaklar

[Teslim modülü için giriş](check-in-pickup-module.md)
