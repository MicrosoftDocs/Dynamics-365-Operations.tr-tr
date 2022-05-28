---
title: Sevkiyat konsolidasyonu çalışma ekranı kullanılarak sevkiyatları konsolide etme
description: Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, sevkiyat konsolidasyon çalışma ekranı kullanılarak sevkiyatlar halinde konsolide edildiği bir senaryo sunar.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 43669bc302ac0d5dd9e6f161e17dde1155aae0f6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673340"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a>Sevkiyat konsolidasyonu çalışma ekranı kullanılarak sevkiyatları konsolide etme

[!include [banner](../includes/banner.md)]

Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, sevkiyat konsolidasyon çalışma ekranı kullanılarak sevkiyatlar halinde konsolide edildiği bir senaryo sunar.

## <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur. Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Sevkiyat konsolidasyon ilkelerini ve ürün filtrelerini ayarlama

Burada açıklanan senaryo, özelliği önceden açtığınız, [Sevkiyat konsolidasyonu ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) alıştırmalarını yaptığınız ve burada açıklanan ilkeleri ve diğer kayıtları oluşturduğunuz varsayımına dayanır. Bu senaryoya devam etmeden önce söz konusu alıştırmaları yaptığınızdan emin olun.

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a>Manuel sevkiyat konsolidasyon özelliğini açma

*Manuel sevkiyat konsolidasyon* özelliğini kullanabilmeniz için önce sisteminizde bu özelliği açmanız gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Manuel sevkiyat konsolidasyonu*

[Sevkiyat konsolidasyon ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) konusunda bahsedildiği gibi ilkeleri oluşturabilmeniz için önce *Sevkiyatı konsolide et* özelliğini de etkinleştirmeniz gerekir. Ancak, o adımı zaten tamamlamış olmalısınız.

## <a name="create-the-sales-orders-for-this-scenario"></a>Bu senaryo için satış siparişleri oluşturma

Çalışabileceğiniz bir satış siparişleri koleksiyonu oluşturarak başlayın. Gelişmiş ambar (WMS) işlemleri için etkinleştirilen bir ambarla çalışmanız gerekir. Başka bir ambar açıkça belirtilmedikçe, aşağıdaki sipariş kümelerinin her biri için aynı ambar kullanılmalıdır.

**Alacak hesapları \> Siparişler \> Tüm satış siparişleri** öğesine gidin ve aşağıdaki alt bölümlerde açıklanan ayarlara sahip bir satış siparişleri koleksiyonu oluşturun.

### <a name="create-order-set-1"></a>Sipariş kümesi 1'i oluşturma

#### <a name="sales-orders-1-1-and-1-2"></a>Satış siparişleri 1-1 ve 1-2

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Teslimat şekli:** *Airwa-Air*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

#### <a name="sales-order-1-3"></a>Satış siparişi 1-3

1. Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Teslimat şekli:** *10*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.
1. Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:

    - **Madde numarası:** *A0002* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*
    - **Teslimat şekli:** *Airwa-Air*

1. **Stok \> Rezervasyon**'u ve sonra Eylem Bölmesi'nde, ikinci sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

### <a name="create-order-set-2"></a>Sipariş kümesi 2'yi oluşturma

#### <a name="sales-orders-2-1-and-2-2"></a>Satış siparişleri 2-1 ve 2-2

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-002*
    - **Teslimat şekli:** *Airwa-Air*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *M9200* (**Kod 4** filtresinin *Yanıcı* değerine ayarlandığı bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.
1. Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:

    - **Madde numarası:** *M9201* (**Kod 4** filtresinin *Patlayıcı* değerine ayarlandığı bir madde)
    - **Miktar:** *1.00*
    - **Teslimat şekli:** *Airwa-Air*

1. **Stok \> Rezervasyon**'u ve sonra Eylem Bölmesi'nde, ikinci sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

### <a name="create-order-set-3"></a>Sipariş kümesi 3'ü oluşturma

#### <a name="sales-orders-3-1-and-3-2"></a>Satış siparişleri 3-1 ve 3-2

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Müşteri talebi:** *1*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

#### <a name="sales-orders-3-3-and-3-4"></a>Satış siparişleri 3-3 ve 3-4

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Müşteri talebi:** *2*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

### <a name="create-order-set-4"></a>Sipariş kümesi 4'ü oluşturma

#### <a name="sales-orders-4-1-and-4-2"></a>Satış siparişleri 4-1 ve 4-2

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-003*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

#### <a name="sales-orders-4-3-and-4-4"></a>Satış siparişleri 4-3 ve 4-4

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-004*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

#### <a name="sales-orders-4-5-and-4-6"></a>Satış siparişleri 4-5 ve 4-6

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-007*
    - **Tesis:** *6*
    - **Ambar:** *61*
    - **Havuz:** *ShipCons*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

#### <a name="sales-orders-4-7-and-4-8"></a>Satış siparişleri 4-7 ve 4-8

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-007*
    - **Tesis:** *6*
    - **Ambar:** *61*
    - **Havuz:** Bu alanı boş bırakın.

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

## <a name="release-the-orders-to-the-warehouse"></a>Siparişleri ambara serbest bırakma

Bu senaryo için oluşturduğunuz her satış siparişini ambara serbest bırakmak için aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Siparişler \> Tüm satış siparişleri**'ne gidin.
1. Serbest bırakılacak satış siparişini bulun ve seçin.
1. Eylem Bölmesi'ndeki **Ambar** sekmesinde, seçili satış siparişini serbest bırakmak için **Eylemler \> Ambara serbest bırak**'ı seçin.
1. Bu yordamı, bu senaryo için oluşturduğunuz diğer satış siparişlerinin her biri için yineleyin.

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a>Sevkiyat konsolidasyonu çalışma ekranı kullanılarak sevkiyatları konsolide etme

1. **Ambar yönetimi \> Ambara serbest bırakma \> Sevkiyat konsolidasyonu çalışma ekranı**'na gidin.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Sorgu düzenleyici iletişim kutusunda, kılavuza aşağıdaki ayarlara sahip bir satır eklemek için **Aralık** sekmesinde **Ekle**'yi seçin:

    - **Tablo:** *Satış siparişleri*
    - **Alan:** *Satış siparişi*
    - **Ölçütler:** Bu senaryo için oluşturduğunuz her sipariş kümesi için virgülle ayrılmış satış siparişi numaralarının listesini girin.

1. Sorgunuzu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.
1. Eylem Bölmesi'nde, **Sevkiyatları konsolide et**'i seçin.
1. Tüm sevkiyatları seçin ve ardından Eylem Bölmesi'nde, **Konsolide et**'i belirleyin.

## <a name="verify-the-shipments"></a>Sevkiyatları doğrulama

Aşağıdaki yordam, sevkiyat konsolidasyonu nedeniyle oluşturulan veya güncelleştirilen sevkiyatları doğrulamanıza olanak verir. Bu senaryo için oluşturduğunuz her bir sipariş kümesini gözden geçirmek için bunu kullanın ve sonra, beklenen sonuçları elde ettiğinize emin olmak için izleyen alt bölümleri gözden geçirin.

1. **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.
1. Gerekli sevkiyatı bulun ve seçin.
1. Sevkiyat oluşturulduğunda veya güncelleştirildiğinde bir konsolidasyon ilkesi kullanılmışsa bunu **Sevkiyat konsolidasyon ilkesi** alanında görmeniz gerekir.

### <a name="related-shipments-for-order-set-1"></a>Sipariş kümesi 1 için ilgili sevkiyatlar

İki sevkiyat oluşturulmuş olmalıdır:

- İlk sevkiyat üç satır içerir ve *CustomerMode* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.
- Taşıma teslimat şekli için *Hava yolu* kullanmayan ikinci sevkiyat, *CustomerOrderNo* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.

### <a name="related-shipments-for-order-set-2"></a>Sipariş kümesi 2 için ilgili sevkiyatlar

Üç sevkiyat oluşturulmuş olmalıdır:

- İlk sevkiyat *Yanıcı* maddeleri içerir.
- Diğer iki sevkiyatın her biri, *Patlayıcı* madde içeren bir satır içerir.

### <a name="related-shipments-for-order-set-3"></a>Sipariş kümesi 3 için ilgili sevkiyatlar

İki sevkiyat oluşturulmuş olmalıdır:

- İlk sevkiyat, **Müşteri talebi** alanının *1* olarak ayarlandığı satış siparişinden sipariş satırları içerir.
- İkinci sevkiyat, **Müşteri talebi** alanının *2* olarak ayarlandığı satış siparişinden sipariş satırları içerir.

### <a name="related-shipments-for-order-set-4"></a>Sipariş kümesi 4 için ilgili sevkiyatlar

Dört sevkiyat oluşturulmuş olmalıdır:

- Müşteri *US-003* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.
- Müşteri *US-004* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.
- Müşteri *US-007* ile ilgili satış siparişi 4-5 ve 4-6'daki satırlar, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.
- Müşteri *US-007* ile ilgili satış siparişi 4-7 ve 4-8'daki satırlar, *CrossOrder* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.

## <a name="additional-resources"></a>Ek kaynaklar

- [Sevkiyat konsolidasyonu ilkeleri](about-shipment-consolidation-policies.md)
- [Sevkiyat konsolidasyon ilkelerini yapılandırma](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]