---
title: Giden konteynerleri paketlemeye ve sevkiyatları işlemeye yönelik paketleme işi
description: Bu makalede, konteynerleri paketlemeye yönelik işi yöneten ve stok maddelerinin paketlenmediği yüklerle ilişkili paketlenmiş konteynerlerin kısmi sevkiyatlarını destekleyen "Paketleme" iş emri türü açıklanır.
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220633"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Giden konteynerleri paketlemeye ve sevkiyatları işlemeye yönelik paketleme işi

[!include [banner](../../includes/banner.md)]

Bu makalede, konteynerleri paketlemeye yönelik işi yöneten ve stok maddelerinin paketlenmediği yüklerle ilişkili paketlenmiş konteynerlerin kısmi sevkiyatlarını destekleyen *Paketleme* iş emri türü açıklanır. Paketleme çalışması, konteynerlerle ilişkili giden sevkiyatları onaylamak için [Onayla ve aktar](confirm-and-transfer.md) işlevini kullanmanızı sağlar.

Kaynak belge çalışması ile ilgili stok, *Paketleme yerleşimi* türünün yerleşimlerine konulduğu zaman paketleme çalışması otomatik olarak oluşturulur. İş, biri *Çekme* ve diğeri *Koyma* için olmak üzere iki satırdan oluşur ve konteyner kapatma/yeniden açma işleminin parçası olarak otomatik olarak sürdürülür.

Konteyner paketleme işleminin nasıl ayarlanacağı ve kullanılacağı hakkında daha fazla bilgi için bkz. [Sevkiyat için konteynerleri paketleme](packing-containers.md).

## <a name="turn-on-the-feature"></a>Özelliği etkinleştirme

Sisteminiz bu makalede açıklanan özellikleri zaten içermiyorsa [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve aşağıdaki özellikleri aşağıdaki sırayla açın: (Her iki özellik de **Ambar Yönetimi** modülünün bir parçasıdır.)

1. *Onayla ve aktar*
1. *Sevk istasyonları için sevk işi*

## <a name="set-up-a-location-for-packing-work"></a>Paketleme işi için yerleşim ayarlama

Paketleme yerleşimlerini ayarlamak için aşağıdaki yordamı kullanın. Her yerleşim için, sistemin otomatik olarak ambalaj çalışması oluşturup oluşturmayacağını seçebilirsiniz.

1. **Ambar Yönetimi \> Kurulum \> Paketleme \> Paketleme istasyonu kurulumu**'na gidin.
1. Eylem Bölmesinde, paketleme istasyonu kurulum kaydı eklemek için **Yeni**'yi seçin.
1. Yeni kayıtta aşağıdaki alanları ayarlayın:

    - **Ambar** – Varsayılan ambalaj yerleşiminin bulunduğu ambarı seçin veya girin.
    - **Yerleşim** – Paketleme istasyonunu seçin veya girin. Bu yerleşim, **Ambar yönetimi parametreleri** sayfasında şirketiniz için paketleme yerleşimi türü olarak yapılandırılan yerleşim türünü kullanan bir yerleşim profiline atanmalıdır. Daha fazla bilgi için bkz. [Sevkiyat için konteynerleri paketleme](packing-containers.md).
    - **Paketleme çalışması oluştur** – Maddelerin paketleme konumuna teslim edileceği her seferinde paketleme çalışması oluşturmak için bu onay kutusunu seçin. Çalışmaya kısmi yüklerin paketlenebilmesi ve sevk edilebilmesi için ilgili yükleme satırlarının bağlantıları dahil edilir.

## <a name="example-scenario"></a>Örnek senaryo

Bu örnek senaryo bir konteyner paketleyerek ve kısmi yük sevk ederek giden satış siparişi akışının nasıl işlendiğini gösterir.

### <a name="make-sample-data-available"></a>Örnek verilerini kullanılabilir hale getirme

Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/fin-ops/get-started/demo-data.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

Bu senaryoyu, özelliği üretim sisteminde kullanmaya yönelik bir kılavuz olarak da kullanabilirsiniz. Ancak, bu durumda, burada açıklanan her ayar için kendi değerlerinizi kullanmanız gerekir.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Ambar paketleme yeri için paketleme çalışmalarını yapılandırma

Başlamak için, belirli bir ambar ve yerleşim için *Paketleme* iş sürecini yapılandırmalısınız.

1. **Ambar Yönetimi \> Kurulum \> Paketleme \> Paketleme istasyonu kurulumu**'na gidin.
1. Kurulum kaydı eklemek için Eylem Bölmesinde **Yeni**'yi seçin.
1. Yeni kayıtta aşağıdaki değerleri ayarlayın:

    - **Ambar:** *62*
    - **Yerleşim:** *Paket*
    - **Paketleme işi oluştur:** *Evet*

1. **Paketleme istasyonu kurulumu** sayfasını kapatın.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Kısmi sevkiyata izin veren bir yük şablonu oluşturma

Bir yükün birden fazla sevkiyat üzerinden teslim edilmesini etkinleştirmek için, bunu kısmi sevkiyat için izin verilen bir yük şablonuyla ilişkilendirmeniz gerekir. Gerekli şablonu oluşturmak için şu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Yük \> Yük şablonları**'na gidin.
1. Kurulum kaydı eklemek için Eylem Bölmesinde **Yeni**'yi seçin.
1. Yeni kayıtta aşağıdaki değerleri ayarlayın:

    - **Yük şablonu kodu:** *Kısmi*
    - **Sevkiyat onaylama sırasında yük bölmeye izin ver:** *Evet*

1. **Yük şablonları** sayfasını kapatın.

Daha fazla bilgi için bkz. [Onaylama ve transfer etme](Confirm-and-transfer.md).

### <a name="process-a-sales-order"></a>Satış siparişini işleme

Bir satış siparişini işlemek ve kısmen sevk etmek için bu adımları izleyin.

1. [Konteynerleri sevkiyat için paketleme](packing-containers.md#scenario) bölümünde sağlanan [örnek senaryoyu](packing-containers.md) tamamlayın. Bu senaryo sırasında, bir maddenin iki adedi için bir satış siparişi oluşturacaksınız. Ardından maddelerden yalnızca birini bir konteynerde paketleyecek ve konteyneri kapatacaksınız. Senaryoda belirtildiği gibi oluşturduğunuz sevkiyat kodunu not etmelisiniz.
1. **Ambar yönetimi \> İş \> Tüm çalışmalar**'a gidin.
1. Filtre alanında, **Kapatılan işi göster** onay kutusunu seçin. Ardından, **Filtre** alanına sevkiyat kodunu girin ve **Sevkiyat kodu** değerine göre filtre uygulamayı seçin. Şimdi üç iş başlığı görmelisiniz. Biri satış siparişi malzeme çekme işi içindir ve *Kapalı* durumuna sahiptir. İkisi ise paketleme işlemi içindir: Bunlardan biri kapalı konteynerle ilgilidir ve *Kapalı* durumuna sahiptir, diğeri ise paketlenmemiş kalan maddeyle ilgilidir ve *Açık* durumuna sahiptir.
1. Yük için **Yük ayrıntıları** sayfasını açmak üzere iş üstbilgilerinden herhangi birinin **Yük kodu** değerini seçin.
1. **Üst bilgi** görünümüne geçin.
1. **Genel** hızlı sekmesinde, **Yük şablonu kodu** alanı için **Düzenle** düğmesini seçin. Ardından, bu senaryo için oluşturduğunuz kısmi sevkiyat yük şablonunu seçin (*Kısmi*).
1. Eylem Bölmesinde **Sevk ve teslim alma** sekmesindeki **Onayla** grubunda **Giden sevkiyat**'ı seçin.
1. **Sevk onayı** iletişim kutusunda **Miktarı yeni yüke böl** seçeneğini seçin.
1. **Tamam**'ı seçin.

Artık özgün yükle ilişkili bir sevk edilmiş konteyneriniz vardır ve sistem, hala konteynerlerde paketlenmesi gereken kalan maddeler için, yeni bir yük oluşturmuştur.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
