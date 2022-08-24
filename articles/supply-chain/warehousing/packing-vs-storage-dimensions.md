---
title: Paketleme ve depolama için farklı boyutlar ayarlama
description: Bu makalede, belirtilen her boyutun kullanıldığı işlemin (paketleme, depolama veya iç içe paketleme) nasıl belirtileceğini gösterir.
author: Mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8ebea86e5ea63ab4f5a844cd3d0936c0d65bbe2b
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220257"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>Paketleme ve depolama için farklı boyutlar ayarlama

[!include [banner](../../includes/banner.md)]

Bazı maddeler, birçok farklı işlemin her biri için fiziksel boyutları farklı izlemeniz gerekebilecek şekilde paketlenebilir veya depolanır. *Ürün paketleme boyutları* özelliği, her ürün için bir veya daha fazla boyut türü ayarlamanıza olanak tanır. Her boyut türü, bir dizi fiziksel ölçü (ağırlık, genişlik, derinlik ve yükseklik) sağlar ve bu fiziksel ölçüm değerlerinin geçerli olduğu işlemi oluşturur. Bu özellik etkinleştirildiğinde, sisteminiz aşağıdaki boyut türlerini desteklecektir:

- *Depolama*: Depolama boyutları, her maddeden çeşitli ambar yerleşimlerinde kaç tane depolanabileceğini belirlemek için yerleşim hacimleriyle birlikte kullanılır.
- *Paketleme*: Paketleme boyutları konteyner kullanımı ve el ile paketleme işlemi sırasında çeşitli konteyner türlerine her bir maddeden kaç tane sığacağını belirlemek için kullanılır.
- *İç içe paketleme*: İç içe paketleme boyutları, paketleme işleminin birden fazla düzey içerdiği durumlarda kullanılır.

*Depolama* boyutları, *Ürün paketleme boyutları* özelliği etkinleştirilmediğinde bile desteklenir. Bunları, Supply Chain Management'ta **Fiziksel boyut** sayfasını kullanarak ayarlarsınız. Bu boyutlar, paketleme ve iç içe paketleme boyutlarının belirtilmediği tüm işlemler tarafından kullanılır.

*Paketleme* ve *iç içe paketleme* boyutları, *Ürün paketleme boyutları* özelliğini etkinleştirdiğinizden eklenen **Fiziksel ürün boyutları** sayfasını kullanarak ayarlanır.
Bu makale, bu özelliğin nasıl kullanılacağını açıklayan bir senaryo içermektedir.

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>Ürün paketleme boyutları özelliğini etkinleştirme

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Ürün paketleme boyutları*

## <a name="example-scenario"></a>Örnek senaryo

### <a name="set-up-the-scenario"></a>Senaryoyu ayarlama

Örnek senaryoyu çalıştırabilmeniz için, sisteminizi bu bölümde anlatıldığı şekilde hazırlamanız gerekir.

#### <a name="enable-demo-data"></a>Tanıtım verilerini etkinleştirme

Burada belirtilen tanıtım kayıtlarını ve değerlerini kullanarak bu senaryo üzerinde çalışmak için standart [tanıtım verilerinin](../../fin-ops-core/fin-ops/get-started/demo-data.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce *USMF* tüzel kişiliğini seçmeniz gerekir.

#### <a name="add-a-new-physical-dimension-to-a-product"></a>Ürüne yeni fiziksel boyut ekleme

Aşağıdakileri yaparak, bir ürün için yeni bir fiziksel boyut ekleyin:

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. **Madde numarası** *A0001* olan bir ürün seçin.
1. Eylem Bölmesinde, **Stok yönet** sekmesini açın ve **Ambar** grubundan **Fiziksel ürün boyutları**'nı seçin.
1. **Fiziksel ürün boyutları** sayfası açılır. Izgaraya aşağıdaki ayarlara sahip yeni bir boyut eklemek için Eylem Bölmesinde **Yeni**'yi seçin.
    - **Fiziksel boyut türü** - *Paketleme*
    - **Fiziksel birim** - *adet*
    - **Ağırlık** - *4*
    - **Ağırlık birimi** - *kg*
    - **Derinlik** - *3*
    - **Yükseklik** - *4*
    - **Genişlik** - *3*
    - **Uzunluk** - *cm*
    - **Hacim birimi** - *cm3*

**Hacim** alanı; **Derinlik**, **Yükseklik** ve **Genişlik** ayarlarınıza göre otomatik olarak hesaplanır.

#### <a name="create-a-new-container-type"></a>Yeni konteyner türü oluşturma

**Ambar yönetimi \> Kurulum \> Konteynerler \> Konteyner türleri**'ne gidin ve aşağıdaki ayarlarla yeni bir kayıt oluşturun:

- **Konteyner türü kodu** - *Kısa Kutu*
- **Açıklama** - *Kısa Kutu*
- **Maksimum net ağırlık** - *50*
- **Hacim** - *144*
- **Uzunluk** - *6*
- **Genişlik** - *6*
- **Yükseklik** - *4*

#### <a name="create-a-container-group"></a>Konteyner grubu oluşturma

**Ambar yönetimi \> Kurulum \> Konteynerler \> Konteyner grupları**'na gidin ve aşağıdaki ayarlarla yeni bir kayıt oluşturun:

- **Konteyner grubu kodu** - *Kısa Kutu*
- **Açıklama** - *Kısa Kutu*

**Ayrıntılar** bölümüne yeni bir satır ekleyin. **Konteyner türü**'nü *Kısa Kutu* olarak ayarlayın.

#### <a name="set-up-a-container-build-template"></a>Bir konteyner yapılandırma şablonu

**Ambar yönetimi \> Kurulum \> Konteynerler \> Konteyner yapı şablonları**'na gidin ve **Kutular**'ı seçin. **Konteyner grubu kodu**'nu *Kısa Kutu* olarak değiştirin.

### <a name="run-the-scenario"></a>Senaryoyu çalıştırma

Sisteminizi önceki bölümde anlatıldığı gibi hazırladıktan sonra, senaryoyu sonraki bölümde anlatıldığı gibi çalıştırmaya hazırsınız demektir.

#### <a name="create-a-sales-order-and-create-a-shipment"></a>Satış siparişi oluşturma ve sevkiyat oluşturma

Bu işlemde, yüksekliği 3'ten az olan madde *paketleme* boyutlarına göre bir sevkiyat oluşturacaksınız.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-001*
    - **Ambar:** *63*

1. Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesi 'ndeki kılavuza yeni, boş bir satır dahil etmelidir. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *5*

1. **Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, Eylem Bölmesi'nde stok rezerve etmek için **Lotu rezerve et**'i seçin.
1. Sayfayı kapatın.
1. Eylem bölmesindeki **Ambar** sekmesini açın ve **Ambara serbest bırak**'ı seçerek ambar için iş oluşturun.
1. **Satış siparişi satırları** hızlı sekmesinde **Ambar \> Sevkiyat ayrıntıları**'nı seçin.
1. Eylem Bölmesinde, **Taşıma** sekmesini açın ve **Konteynerleri görüntüle**'yi seçin. Maddenin, iki *Kısa Kutu* konteyneriyle konteynerlere yerleştirildiğini doğrulayın.

#### <a name="place-an-item-into-storage"></a>Maddeyi depoya yerleştirme

1. Mobil cihazı açın, ambar 63'te oturum açın ve **Stok \> Ayarla**'ya gidin.
1. **Loc** = *SHORT-01* ifadesini girin. **Madde** = *A0001* ve **Miktar** = *1 adet* olacak şekilde yeni bir lisans plakası oluşturun.
1. **Tamam**'ı seçin. "Madde A0001 yerleşimin belirtilen boyutlarına sığmadığından SHORT-01 yerleşimi başarısız oldu." hatasını alırsınız. Bunun nedeni, ürünün *Depolama* türü boyutlarının yerleşim profilinde belirtilen boyutlardan daha büyük olmasıdır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]