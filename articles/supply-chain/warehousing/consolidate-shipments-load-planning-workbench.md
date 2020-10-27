---
title: Yük planlama çalışma ekranından Ambara serbest bırakma kullanılarak sevkiyatları konsolide etme
description: Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, otomatik olarak sevkiyatlar halinde birleştirildiği bir senaryo sunar.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 2f1dd5c743664e638c043b600ae7b0f6bce5ddcd
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986852"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a>Yük planlama çalışma ekranından Ambara serbest bırakma kullanılarak sevkiyatları konsolide etme

[!include [banner](../includes/banner.md)]

Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, otomatik olarak sevkiyatlar halinde birleştirildiği bir senaryo sunar.

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

    - **Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

#### <a name="sales-order-1-2"></a>Satış siparişi 1-2

1. Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:

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

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a>Yükler oluşturmak ve bunları ambara serbest bırakmak için yük planlama çalışma ekranını kullanma

Bu senaryo için oluşturduğunuz her sipariş kümesi için bir yük oluşturmak ve sonra bunu ambara serbest bırakmak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Yükler \> Yük planlama çalışma ekranı** öğesine gidin.
1. **Satış satırları** sekmesinde, bu senaryo için oluşturduğunuz sipariş kümelerinden birindeki tüm satış siparişi satırlarını bulun ve seçin.
1. Eylem Bölmesi'ndeki **Arz ve talep** sekmesinde, seçili sipariş satırlarını yeni bir Yüke eklemek için **Ekle \> Yeni yüke** öğesini seçin.
1. **Yük şablonu ataması** iletişim kutusundaki **Yük şablonu kimliği** alanında, *Stnd Yük Şablonu* gibi bir yük şablonu seçin.
1. İletişim kutusunu kapatmak için **Tamam**'ı seçin. 
1. **Yükler** bölümünde, az önce oluşturduğunuz yükü bulun ve seçin.
1. Seçili yükü ambara serbest bırakmak için **Serbest bırak \> Ambara serbest bırak** öğesini seçin.
1. Bu yordamı, bu senaryo için oluşturduğunuz diğer üç sipariş kümesi için yineleyin.

## <a name="verify-the-shipments"></a>Sevkiyatları doğrulama

Aşağıdaki yordam, sevkiyat konsolidasyonu nedeniyle oluşturulan veya güncelleştirilen sevkiyatları doğrulamanıza olanak verir. Bu senaryo için oluşturduğunuz her bir sipariş kümesini gözden geçirmek için bunu kullanın ve sonra, beklenen sonuçları elde ettiğinize emin olmak için izleyen alt bölümleri gözden geçirin.

1. **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.
1. Gerekli sevkiyatı bulun ve seçin.
1. Sevkiyat oluşturulduğunda veya güncelleştirildiğinde bir konsolidasyon ilkesi kullanılmışsa bunu **Sevkiyat konsolidasyon ilkesi** alanında görmeniz gerekir.

### <a name="release-order-set-1-in-one-load"></a>Bir yükte sipariş kümesi 1'i serbest bırakma

İki sevkiyat oluşturulmuş olmalıdır:

- İlk sevkiyat üç satır içerir ve *CustomerMode* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.
- Taşıma teslimat şekli için *Hava yolu* kullanmayan ikinci sevkiyat, *CustomerOrderNo* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.

### <a name="release-order-set-2-in-one-load"></a>Bir yükte sipariş kümesi 2'yi serbest bırakma

Üç sevkiyat oluşturulmuş olmalıdır:

- İlk sevkiyat *Yanıcı* maddeleri içerir.
- Diğer iki sevkiyatın her biri, *Patlayıcı* madde içeren bir satır içerir.

### <a name="release-order-set-3-in-one-load"></a>Bir yükte sipariş kümesi 3'ü serbest bırakma

İki sevkiyat oluşturulmuş olmalıdır:

- İlk sevkiyat, **Müşteri talebi** alanının *1* olarak ayarlandığı satış siparişinden sipariş satırları içerir.
- İkinci sevkiyat, **Müşteri talebi** alanının *2* olarak ayarlandığı satış siparişinden sipariş satırları içerir.

### <a name="release-order-set-4-in-one-load"></a>Bir yükte sipariş kümesi 4'ü serbest bırakma

Dört sevkiyat oluşturulmuş olmalıdır:

- Müşteri hesabı *US-003* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.
- Müşteri hesabı *US-004* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.
- Müşteri hesabı *US-007* ile ilgili satış siparişi 4-5 ve 4-6'daki satırlar, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.
- Müşteri hesabı *US-007* ile ilgili satış siparişi 4-7 ve 4-8'daki satırlar, *CrossOrder* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.

## <a name="additional-resources"></a>Ek kaynaklar

- [Sevkiyat konsolidasyonu ilkeleri](about-shipment-consolidation-policies.md)
- [Sevkiyat konsolidasyon ilkelerini yapılandırma](configure-shipment-consolidation-policies.md)
