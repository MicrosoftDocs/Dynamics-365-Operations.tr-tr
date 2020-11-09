---
title: Satış siparişlerinin otomatik serbest bırakılması kullanılarak ambara serbest bırakıldıklarında sevkiyatları konsolide etme
description: Bu konu, çoklu siparişlerin aynı otomatik ambara serbest bırakma periyodik yordamında yer alarak ambara serbest bırakıldığı bir senaryo sunar.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ac3ab25dc1355ee15e1209950ff0f3b3933b7095
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016874"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a>Satış siparişlerinin otomatik serbest bırakılması kullanılarak ambara serbest bırakıldıklarında sevkiyatları konsolide etme

[!include [banner](../includes/banner.md)]

Bu konu, çoklu siparişlerin aynı otomatik ambara serbest bırakma periyodik yordamında yer alarak ambara serbest bırakıldığı bir senaryo sunar. Siparişler, sevkiyat konsolidasyon ilkeleri olarak tanımlanan kurallara göre otomatik olarak sevkiyatlar halinde konsolide edilecektir.

Senaryo sırasında, satış siparişi kümeleri oluşturacak ve her kümeyi ambara serbest bırakacaksınız. Böylece, yapılandırılan ilkelere göre, sevkiyat konsolidasyonu sırasında oluşturulan veya güncelleştirilen sevkiyatları gözden geçireceksiniz.

## <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur. Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Sevkiyat konsolidasyon ilkelerini ve ürün filtrelerini ayarlama

Burada açıklanan senaryo, özelliği önceden açtığınız, [Sevkiyat konsolidasyonu ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) alıştırmalarını yaptığınız ve burada açıklanan ilkeleri ve diğer kayıtları oluşturduğunuz varsayımına dayanır. Bu senaryoya devam etmeden önce söz konusu alıştırmaları yaptığınızdan emin olun.

## <a name="create-the-sales-orders-for-this-scenario"></a>Bu senaryo için satış siparişleri oluşturma

Çalışabileceğiniz bir satış siparişleri koleksiyonu oluşturarak başlayın. Gelişmiş ambar (WMS) işlemleri için etkinleştirilen bir ambarla çalışmanız gerekir. Başka bir ambar açıkça belirtilmedikçe, aşağıdaki sipariş kümelerinin her biri için aynı ambar kullanılmalıdır.

**Alacak hesapları \> Siparişler \> Tüm satış siparişleri** öğesine gidin ve aşağıdaki alt bölümlerde açıklanan ayarlara sahip bir satış siparişleri koleksiyonu oluşturun.

### <a name="create-order-set-1"></a>Sipariş kümesi 1'i oluşturma

#### <a name="sales-order-1-1"></a>Satış siparişi 1-1

1. Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Teslimat şekli:** *Airwa-Air*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* ( **Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

#### <a name="sales-order-1-2"></a>Satış siparişi 1-2

1. Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Teslimat şekli:** *Airwa-Air*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* ( **Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

#### <a name="sales-order-1-3"></a>Satış siparişi 1-3

1. Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Teslimat şekli:** *10*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* ( **Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:

    - **Madde numarası:** *A0002* ( **Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*
    - **Teslimat şekli:** *Airwa-Air*

### <a name="create-order-set-2"></a>Sipariş kümesi 2'yi oluşturma

#### <a name="sales-orders-2-1-and-2-2"></a>Satış siparişleri 2-1 ve 2-2

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-002*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *M9200* ( **Kod 4** filtresinin *Yanıcı* değerine ayarlandığı bir madde)
    - **Miktar:** *1.00*

1. Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:

    - **Madde numarası:** *M9201* ( **Kod 4** filtresinin *Patlayıcı* değerine ayarlandığı bir madde)
    - **Miktar:** *1.00*
    - **Teslimat şekli:** *Airwa-Air*

### <a name="create-order-set-3"></a>Sipariş kümesi 3'ü oluşturma

#### <a name="sales-order-3-1"></a>Satış siparişi 3-1

1. Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-002*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *M9200* ( **Kod 4** filtresinin *Yanıcı* değerine ayarlandığı bir madde)
    - **Miktar:** *1.00*

1. Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:

    - **Madde numarası:** *M9201* ( **Kod 4** filtresinin *Patlayıcı* değerine ayarlandığı bir madde)
    - **Miktar:** *1.00*
    - **Teslimat şekli:** *Airwa-Air*

> [!NOTE]
> Bu sipariş, sipariş kümesi 2 için oluşturduğunuz iki siparişle aynıdır. Ancak, bu senaryoda daha sonra ayrı olarak serbest bırakacağınız için kendi sipariş kümesi olarak listelenir.

### <a name="create-order-set-4"></a>Sipariş kümesi 4'ü oluşturma

#### <a name="sales-order-4-1"></a>Satış siparişi 4-1

1. Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Müşteri talebi:** *1*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* ( **Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

### <a name="create-order-set-5"></a>Sipariş kümesi 5'yi oluşturma

#### <a name="sales-orders-5-1-and-5-2"></a>Satış siparişleri 5-1 ve 5-2

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Müşteri talebi:** *2*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* ( **Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

#### <a name="sales-order-5-3"></a>Satış siparişi 5-3

1. Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Müşteri talebi:** *1*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* ( **Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

### <a name="create-order-set-6"></a>Sipariş kümesi 6'yi oluşturma

#### <a name="sales-orders-6-1-and-6-2"></a>Satış siparişleri 6-1 ve 6-2

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-003*
    - **Müşteri talebi:** *2*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* ( **Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>Satış siparişleri 6-3 ve 6-4

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-004*
    - **Müşteri talebi:** *1*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* ( **Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>Satış siparişleri 6-5 ve 6-6

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-007*
    - **Tesis:** *6*
    - **Ambar:** *61*
    - **Havuz:** *ShipCons*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* ( **Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>Satış siparişleri 6-7 ve 6-8

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-007*
    - **Tesis:** *6*
    - **Ambar:** *61*
    - **Havuz:** Bu alanı boş bırakın.

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* ( **Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>Satış siparişlerini ambara otomatik olarak serbest bırakma

Daha önce oluşturduğunuz her satış siparişi kümesi için ambara otomatik olarak serbest bırakma yordamını tamamlayacaksınız. Her örnekte, burada sağlanan [temel ambara serbest bırakma yordamı](#release-procedure) üzerinden çalışacaksınız.

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>Temel ambara serbest bırakma yordamı

Daha önce oluşturduğunuz her satış siparişi kümesi için aşağıdaki alt bölümlerde özetlenen üç yordamı tamamlayacaksınız.

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>Serbest bırakma sırasında kullanılacak dalga şablonunu güncelleştirme

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları** 'na gidin.
1. **Dalga şablonu türü** alanını *Sevkiyat* olarak ayarlayın.
1. Bu senaryo için oluşturduğunuz sipariş kümelerinde kullandığınız ambarla ilişkilendirilmiş dalga şablonunu bulun ve seçin. Örneğin, ambar *24* 'ü kullandıysanız **24 Sevkiyat Varsayılan** dalga şablonunu seçin. Ambar *61* 'i kullandıysanız **61 Sevkiyat** dalga şablonunu seçin.
1. Eylem Bölmesi'nde, **Düzenle** 'yi seçin.
1. **Dalgayı ambara serbest bırakma sırasında işle** seçeneğini *Hayır* olarak ayarlayın.

#### <a name="release-to-the-warehouse"></a>Ambara serbest bırakma

1. **Ambar yönetimi \> Ambara serbest bırakma \> Satış siparişlerini otomatik serbest bırakma** seçeneğine gidin.
1. **Serbest bırakılacak miktar** alanını *Tümü* olarak ayarlayın.
1. **Eklenecek kayıtlar** hızlı sekmesinde, sorgu iletişim kutusunu açmak için **Filtre** 'yi seçin.
1. Kılavuza aşağıdaki ayarlara sahip bir satır eklemek için **Aralık** sekmesinde **Ekle** 'yi seçin:

    - **Tablo:** *Satış siparişi*
    - **Türetilmiş tablo:** *Satış siparişi*
    - **Alan:** *Satış siparişi*
    - **Ölçütler:** İstenen sipariş kümesinden satış siparişi numaralarının virgülle ayrılmış listesini girin.

1. Sorgunuzu kaydetmek için **Tamam** 'ı seçin.
1. *Otomatik ambara serbest bırakma* yordamını başlatmak için **Tamam** 'ı seçin.

#### <a name="review-the-shipment-that-is-created-or-updated"></a>Oluşturulan veya güncelleştirilen sevkiyatı gözden geçirme

1. **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar** 'a gidin.
1. Gerekli sevkiyatı bulun ve seçin.
1. Sevkiyat oluşturulduğunda veya güncelleştirildiğinde bir konsolidasyon ilkesi kullanılmışsa bunu **Sevkiyat konsolidasyon ilkesi** alanında görmeniz gerekir.

### <a name="release-sales-orders-from-order-set-1"></a>Sipariş kümesi 1'deki satış siparişlerini serbest bırakma

Sipariş kümesi 1'deki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.

Bitirdiğinizde, iki sevkiyatın oluşturulduğunu görmelisiniz:

- İlk sevkiyat üç satır içerir ve *CustomerMode* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.
- Taşıma teslimat şekli için *Hava yolu* kullanmayan ikinci sevkiyat, *CustomerOrderNo* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.

### <a name="release-sales-orders-from-order-set-2"></a>Sipariş kümesi 2'deki satış siparişlerini serbest bırakma

Sipariş kümesi 2'deki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.

Bitirdiğinizde, üç sevkiyatın oluşturulduğunu görmelisiniz:

- İlk sevkiyat *Yanıcı* maddeleri içerir.
- Diğer iki sevkiyatın her biri, *Patlayıcı* madde içeren bir satır içerir.

### <a name="release-sales-orders-from-order-set-3"></a>Sipariş kümesi 3'teki satış siparişlerini serbest bırakma

Sipariş kümesi 3'teki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.

Bitirdiğinizde, aşağıdaki eylemlerin gerçekleştiğini görmelisiniz:

- Var olan bir sevkiyat (sipariş kümesi 2 ambara serbest bırakıldığında oluşturulan sevkiyat) güncelleştirilmiştir. *Yanıcı* maddeyi içeren bir satır eklenmiştir.
- *Patlayıcı* maddeyi içeren yeni bir sevkiyat oluşturulmuştur.

### <a name="release-sales-orders-from-order-set-4"></a>Sipariş kümesi 4'teki satış siparişlerini serbest bırakma

Sipariş kümesi 4'teki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.

Bitirdiğinizde, var olan bir sevkiyatın ( **Müşteri talebi** alanının *1* olarak ayarlandığı) güncelleştirilmiş olduğunu görmelisiniz. Buna yeni bir satır eklenmiştir.

### <a name="release-sales-orders-from-order-set-5"></a>Sipariş kümesi 5'teki satış siparişlerini serbest bırakma

Sipariş kümesi 5'teki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.

Bitirdiğinizde, aşağıdaki eylemlerin gerçekleştiğini görmelisiniz:

- Var olan bir sevkiyat ( **Müşteri talebi** alanı *1* olarak ayarlandığı) güncelleştirilmiştir. Satış siparişi 5-3'ten bir satır ( **Müşteri talebi** alanının *1* olarak ayarlandığı) buna eklenmiştir.
- Satış siparişi 5-1 ve 5-2'den satırların tek bir sevkiyat olarak gruplandırıldığı, yeni bir sevkiyat oluşturulmuştur.

### <a name="release-sales-orders-from-order-set-6"></a>Sipariş kümesi 6'daki satış siparişlerini serbest bırakma

Sipariş kümesi 6'daki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.

Bitirdiğinizde, dört sevkiyatın oluşturulduğunu görmelisiniz:

- Müşteri *US-003* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.
- Müşteri *US-004* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.
- Müşteri *US-007* ile ilgili satış siparişi 6-5 ve 6-6'daki satırlar, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.
- Müşteri *US-007* ile ilgili satış siparişi 6-7 ve 6-8'deki satırlar, *CrossOrder* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.

## <a name="additional-resources"></a>Ek kaynaklar

- [Sevkiyat konsolidasyonu ilkeleri](about-shipment-consolidation-policies.md)
- [Sevkiyat konsolidasyon ilkelerini yapılandırma](configure-shipment-consolidation-policies.md)
