---
title: Dalga şablonu gruplandırması
description: Dalga şablonu gruplandırması, sistemin serbest bırakılan satırları nasıl böleceğini ve yeni ya da varolan dalgalara nasıl atayacağını (tanımladığınız ölçütlere dayanarak) belirlemek için dalga şablonu kurulumları kullanmasını sağlar. Bu özellik, dalgaların belirli ölçütlere göre oluşturulduğu ancak yöneticilerin dalgaları el ile değil otomatik oluşturmayı tercih ettikleri ambarlar için yararlı olabilir.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b422eb432e579d4ae914fbc0efa79aaa15f1de27
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998390"
---
# <a name="wave-template-grouping"></a>Dalga şablonu gruplandırması

[!include [banner](../includes/banner.md)]

Dalga şablonu gruplandırması, sistemin serbest bırakılan satırları nasıl böleceğini ve yeni ya da varolan dalgalara nasıl atayacağını (tanımladığınız ölçütlere dayanarak) belirlemek için [dalga şablonu](tasks/configure-wave-processing.md) kurulumları kullanmasını sağlar. Bu özellik, dalgaların belirli ölçütlere göre oluşturulduğu ancak yöneticilerin dalgaları el ile değil otomatik oluşturmayı tercih ettikleri ambarlar için yararlı olabilir. Sistemin, eşleşen gruplandırma alan değerleri olduğunu saptadığı ilk dalgaya her yeni serbest bırakılan sevkiyatı eklemesini sağlar. Eşleşme bulunamazsa, sistem yeni sevkiyat için yeni bir dalga oluşturur.

> [!IMPORTANT]
> Dalga şablonu gruplandırması *üretim hammadde çekme* veya *Kanban çekme* iş türlerinde desteklenmez. Bunun nedeni, dalga gruplandırmasının sevkiyatları temel alması ve bu iş türlerinin sevkiyatları kullanmamasıdır.

## <a name="turn-on-the-wave-template-grouping-feature"></a>Dalga şablonu gruplandırması özelliğini açma

*Dalga şablonu gruplandırması* özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Dalga şablonu gruplandırması*

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a>Dalga şablonu gruplandırmasını kullanmak için bir dalga şablonu ayarlama

Dalga şablonu gruplandırmasını kullanılabilir hale getirmek için, bu adımları izleyerek [dalga şablonunuzu](tasks/configure-wave-processing.md) ayarlayın.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.
1. Sol bölmede, ayarlanacak dalga şablonunu seçin. Bu konudaki tanıtım verilerini kullanarak daha sonra senaryo üzerinde çalışmaya hazırlanıyorsanız, **62 Sevkiyat varsayılanı** şablonunu seçin.
1. Sayfayı düzenleme moduna sokmak için **Düzenle**'yi seçin.
1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Dalga oluşturmayı otomatikleştir:** *Evet*
    - **Açık dalgalara ata:** *Evet*
    - **Dalgayı ambara serbest bırakma sırasında işle**: *Hayır*

1. Eylem bölmesinde, **Sorguyu düzenle**'yi seçerek sorgu iletişim kutusunu açın.
1. Sorgu iletişim kutusundaki **Sıralama** sekmesinde sıralama ölçütlerini gözden geçirin ve dalgalarınızı gruplandırmak için kullanmak istediğiniz alanı içeren bir kural olduğundan emin olun.

    Tanıtım verilerini kullanarak senaryo üzerinden çalışmaya hazırlanıyorsanız aşağıdaki değerleri taşıyan bir satır ekleyin:

    - **Tablo:** *Sevkiyatlar*
    - **Türetilmiş tablo:** *Sevkiyatlar*
    - **Alan:** *Taşıyıcı hizmeti*

        > [!NOTE]
        > Bu değeri seçtikten sonra şu iletiyi alabilirsiniz: "Taşıyıcı hizmeti alanı bir dizin alanı değil. Bunun üzerinde sıralama eklemek istiyor musunuz?" Sıralama eklemek için **Evet**'i seçin.

    - **Arama yönü:** *Artan*

1. Değişikliklerinizi kaydedip sorgu iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Eylem bölmesinde, **Dalga şablonu gruplandırması**'nı seçin.
1. **Dalga şablonu gruplandırması** sayfasında, sipariş satırlarını dalgalar halinde gerektiği gibi gruplandırmak için kullanmak istediğiniz her satır için **Gruplandırma ölçütü** onay kutusunu işaretleyin. Tanıtım verilerini kullanarak senaryo üzerinden çalışmaya hazırlanıyorsanız, *Taşıyıcı hizmeti* satırı için **Gruplandırma ölçütü** onay kutusunu işaretleyin.
1. **Kaydet**'i seçin.
1. **Dalga şablonu gruplandırması** sayfasını kapatın.
1. Şablonunuzu kaydetmek için **Kaydet**'i seçin.

## <a name="scenario"></a>Senaryo

Bu bölüm, özelliğin ne yaptığını ve bu özellikle nasıl çalışılacağını öğrenmek için kullanabileceğiniz bir metin sunmaktadır.

### <a name="make-sample-data-available"></a>Örnek verilerini kullanılabilir hale getirme

Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

Bu senaryodan, üretim sisteminde çalışırken özelliği kullanmaya yönelik kılavuz olarak da yararlanabilirsiniz. Ancak, bu durumda kendi değerlerinizi değiştirmeniz gerekir ve standart tanıtım verilerinin sağladığı bazı gerekli kayıt türleri kaybolabilir.

### <a name="scenario-wave-template-grouping"></a>Senaryo: Dalga şablonu gruplandırması

Bu senaryo, bir dalga şablonunda tanımlanan gruplandırma ölçütlerine göre çoklu dalgaları otomatik olarak oluşturmak için dalga şablonu gruplandırmasının nasıl kullanılacağını gösteriyor. Bu senaryoda, dalga şablonu, sistemde taşıyıcı hizmeti başına bir dalga oluşturmak üzere ayarlanmıştır.

Başlamadan önce, bu konuda daha önce ele alınan [Dalga şablonu gruplandırmasını kullanmak için bir dalga şablonu ayarlama](#set-up-template) bölümünde açıklandığı şekilde dalga şablonunuzu hazırlayın. Bu senaryo için tanıtım verileriyle çalışacaksanız, o yordamda önerilen tanıtım veri değerlerini kullandığınızdan emin olun. Bu kurulum, dalgalarınızı her bir satış siparişi için ayarlanan taşıyıcı hizmetine göre gruplandıracaktır.

#### <a name="create-sales-order-1"></a>Satış siparişi oluşturma 1

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Satış siparişi oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını *ABD-004* olarak ayarlayın.
    - **Genel** hızlı sekmesinde, **Ambar** alanının ayarını *62* yapın.

1. Satış siparişini oluşturmak ve **Satış siparişi oluştur** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi **Satırlar** görünümünde açılır. Satış siparişi numarasını not edin.
1. **Üst bilgi** görünümüne geçin.
1. **Teslimat** hızlı sekmesinde, **Taşıma** bölümünde aşağıdaki değerleri ayarlayın:

    - **Sevkiyat taşıyıcısı:** *Hava nakliyesi*
    - **Taşıyıcı hizmeti:** *Hava*

1. **Satırlar** görünümüne dönün.
1. **Satış siparişi satırları** bölümünde, kılavuza satır maddesi eklemek için **Satır ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0002*
    - **Miktar:** *2*

1. Yeni sipariş satırını seçin ve ardından kılavuzun yukarısındaki **Stok** menüsünde **Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, Eylem bölmesinde, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.
1. Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.
1. Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.
1. Bu sipariş için sevkiyatı ve dalgayı gösteren bir bilgi iletisi alırsınız. Dalga kodu numarasını ve sevkiyat kodu numaralarını not edin.

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a>Satış siparişi 1'den oluşturulan dalgayı görüntüleyin

1. **Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.
1. Satış siparişinden oluşturulan dalga kodunu seçin.
1. Dalga ayrıntıları sayfasını açmak için dalga kodu bağlantısını seçin.
1. Sevkiyatın **Dalga satırları** hızlı sekmesine eklendiğini unutmayın.

#### <a name="create-sales-order-2"></a>Satış siparişi oluşturma 2

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Satış siparişi oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını *ABD-005* olarak ayarlayın.
    - **Genel** hızlı sekmesinde, **Ambar** alanının ayarını *62* yapın.

1. Satış siparişini oluşturmak ve **Satış siparişi oluştur** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi **Satırlar** görünümünde açılır. Satış siparişi numarasını not edin.
1. **Üst bilgi** görünümüne geçin.
1. **Teslimat** hızlı sekmesinde, **Taşıma** bölümünde aşağıdaki değerleri ayarlayın:

    - **Sevkiyat taşıyıcısı:** *Çiçek taşıma*
    - **Taşıyıcı hizmeti:** *Std*

1. **Satırlar** görünümüne dönün.
1. **Satış siparişi satırları** bölümünde, kılavuza satır maddesi eklemek için **Satır ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *1*

1. Yeni sipariş satırını seçin ve ardından kılavuzun yukarısındaki **Stok** menüsünde **Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, Eylem bölmesinde, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.
1. Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.
1. Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.
1. Bu sipariş için sevkiyatı ve dalgayı gösteren bir bilgi iletisi alırsınız. Dalga kodu numarasını ve sevkiyat kodu numaralarını not edin. Dalga kodunun ilk satış siparişinin dalga kodundan farklı olduğuna dikkat edin.

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a>Satış siparişi 2'den oluşturulan dalgayı görüntüleyin

1. **Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.
1. İkinci satış siparişinden oluşturulan dalga kodunu seçin.
1. Dalga ayrıntıları sayfasını açmak için dalga kodu bağlantısını seçin.
1. Sevkiyatın **Dalga satırları** hızlı sekmesine eklendiğini unutmayın.

Bu sevkiyat için yeni bir dalga oluşturulmuştur çünkü ilk satış siparişinden farklı bir taşıyıcı hizmeti kullanmaktadır.

#### <a name="create-sales-order-3"></a>Satış siparişi oluşturma 3

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Satış siparişi oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını *ABD-006* olarak ayarlayın.
    - **Genel** hızlı sekmesinde, **Ambar** alanının ayarını *62* yapın.

1. Satış siparişini oluşturmak ve **Satış siparişi oluştur** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi **Satırlar** görünümünde açılır. Satış siparişi numarasını not edin.
1. **Üst bilgi** görünümüne geçin.
1. **Teslimat** hızlı sekmesinde, **Taşıma** bölümünde aşağıdaki değerleri ayarlayın:

    - **Sevkiyat taşıyıcısı:** *Hava Nakliyesi*
    - **Taşıyıcı hizmeti:** *Hava*

1. **Satırlar** görünümüne dönün.
1. **Satış siparişi satırları** bölümünde, kılavuza satır maddesi eklemek için **Satır ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *1*

1. Yeni sipariş satırını seçin ve ardından kılavuzun yukarısındaki **Stok** menüsünde **Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, Eylem bölmesinde, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.
1. Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.
1. Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.
1. Bu sipariş için sevkiyatı ve dalgayı gösteren bir bilgi iletisi alırsınız. Dalga kodu numarasını ve sevkiyat kodu numaralarını not edin. Sevkiyat, ilk satış siparişinden varolan dalgaya atanmıştır.

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a>1 ve 3 numaralı satış siparişleriyle ilgili dalgayı görüntüleyin

1. **Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.
1. Üçüncü satış siparişinden oluşturulan dalga kodunu seçin.
1. Dalga ayrıntıları sayfasını açmak için dalga kodu bağlantısını seçin.
1. İlk satış siparişi için sevkiyatla birlikte, sevkiyatın **Dalga satırları** hızlı sekmesine eklendiğine dikkat edin.
