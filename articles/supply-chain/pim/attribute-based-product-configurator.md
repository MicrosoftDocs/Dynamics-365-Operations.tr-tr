---
title: Sabit tabanlı ürün yapılandırması için öznitelik tabanlı satış fiyatları
description: Bu konu, fiziksel ürün reçetesi ve rota yerine bileşenleri ve öznitelikleri temel alan satış fiyatlarıyla satış fiyatı modellerinin nasıl oluşturulacağını açıklamaktadır.
author: sorenva
manager: tfehr
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: cba4b1eac33ae53e214297728c1cdf2710ebd9d9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007928"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a>Sabit tabanlı ürün yapılandırması için öznitelik tabanlı satış fiyatları

Bu konu, fiziksel ürün reçetesi ve rota yerine bileşenleri ve öznitelikleri temel alan satış fiyatlarıyla satış fiyatı modellerinin nasıl oluşturulacağını açıklamaktadır. Her ürün yapılandırması modeli için birkaç satış fiyatı modeli oluşturabilirsiniz.

## <a name="set-relevant-product-information-management-parameters"></a>İlgili ürün bilgileri yönetim parametrelerini ayarlama

Fiyat modellerinizi oluşturmaya başlamadan önce, satış fiyatı modellerinizi oluştururken kullanılan varsayılan para birimini tanımlamanız gerekir. Ayrıca, tüm sipariş veya teklif satırları için fiyat dökümü olan bir Microsoft Excel dosyası eklenip eklenmeyeceğini de seçebilirsiniz. Fiyat dökümü, yapılandırılan bir ürünle ilgili belirli bir satış fiyatına nasıl ulaşacağınız hakkındaki ayrıntıları müşterilerle paylaşmanıza olanak sağlar.

Varsayılan para birimini ayarlamak için:

1. **Ürün bilgileri yönetimi \> Kurulum \> Ürün bilgileri yönetimi parametreleri** bölümüne gidin.
1. **Kısıtlama tabanlı ürün yapılandırma modelleri** sekmesini açın.
1. **Varsayılan para birimi** açılan listesini açın ve para birimini seçin.

    ![Sınırlama tabanlı ürün yapılandırması için varsayılan para birimini ayarlama](media/prod-config-currency.png "Sınırlama tabanlı ürün yapılandırması için varsayılan para birimini ayarlama")

1. Tüm sipariş veya teklif satırları için fiyat dökümü içeren bir Excel dosyası iliştirmek istiyorsanız, **Fiyat modeli** bölümünde **Ekle**'yi *Evet* olarak ayarlayın.

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a>Satış fiyatı modellerinizi oluşturma

Satış fiyatı modeli oluşturmak için:

1. **Ürün bilgileri yönetimi \>  Ürünler \> Ürün yapılandırma modelleri**'ne gidin.
1. Hedef ürün yapılandırma modelini seçin.
1. Eylem Bölmesinde, **Model** sekmesini açın ve **Ayarla** grubundan **Fiyat modelleri**'ni seçin.
1. **Fiyat modelleri** sayfası açılır.
1. Bir fiyat modeli seçin veya kılavuza yeni bir model ekleyin.
1. Aşağıdaki özellikleri sağlayan seçtiğiniz modele ait düzenleme sayfasını açmak için **Düzenle**'yi seçin:
    - Formun başlığı varsayılan para birimini gösterir ve fiyat kurulumunuz için yeni para birimleri eklemenize olanak tanır.
    - Sol bölme, ürün modelinin tüm bileşenlerini ve Kullanıcı gereksinimlerini gösterir. Ürün modeli ağacındaki her düğümün bir temel fiyat ifadesi ve isteğe bağlı sayıda ifade kuralı olabilir. İfade kuralı bir koşul ve bir ifadeden oluşur ve her ifade kuralı, ürünün fiyatını denetlemenize yardımcı olan bir ürün seçeneği içerir.
    - Koşullarınızı ve deyimlerinizi yapılandırdığınızda, bir ürün modelindeki hesaplamalarda olduğu gibi kullanılabilen işleçlere sahip olursunuz. İfade düzenleyicisi her iki koşulu ve ifadeyi de destekler.
1. Sol sütunda bir düğüm seçin ve daha sonra fiyatlandırma kuralları oluşturmak için önceki adımda açıklanan özellikleri kullanın (ayrıca bu yordamdan sonra sağlanan örneğe bakın). Gerektiğinde her düğüm için bu adımı yineleyin.

Aşağıdaki örnek, müşteri tarafından seçilen yapılandırmaya bağlı olarak, aşağıdaki beş ifade kuralından biri veya daha fazlası tarafından değiştirilebilen statik sayı olan 899,95 Euro taban fiyatını gösterir:

- Beyaz kabin için 59,95 EUR çıkarın.
- Köşe koruması için 35,95 Euro ekleyin.
- Metal ön ızgara için 89,95 Euro ekleyin.
- Gül ağacı kabin yüzeyi için 119,95 Euro ekleyin.
- Her bir hoparlör yükseklik birimi için 12,95 EUR ekleyin.

![Örnek fiyat modeli](media/prod-config-rules-example.png "Örnek fiyat modeli")

## <a name="add-support-for-multiple-currencies"></a>Çoklu para birimi desteği ekleme

Yapılandırılabilir bir ürün satıldığında sistem, fiyatların müşterinin para biriminde açık olarak ayarlanıp ayarlanmadığını denetler. Ayarlanmışsa, açık değerler kullanılır. Ayarlanmadıysa, sistem varsayılan para birimi değerini müşterinin para birimine dönüştürmek için satış şirketi tarafından oluşturulan döviz kurlarını kullanır.

Ek para biriminde açık fiyatlar eklemek için:

1. [Satış fiyatı modellerinizi oluşturma](#build-price-model) konusunda açıklandığı gibi, fiyat modelinizi düzenleme sayfasını açın.
1. Kullanılabilir para birimlerini listeleyen **Para birimleri** açılır iletişim kutusunu açmak için fiyat modelinin başlığında **Ekle** düğmesini seçin.
1. **Para birimleri** açılan iletişim kutusuna eklemek istediğiniz para birimini seçin ve **Tamam**'ı seçin.
1. **Geçerli para birimi** açılan listesi şimdi eklediğiniz para birimini ve daha önce eklenmiş olabilecek diğer para birimlerini içerir. Yeni para biriminizi seçin ve **İfade kuralları** bölümündeki kılavuzun artık iki ifade alanı içerdiğine dikkat edin:
    - **İfade** - **Geçerli para birimi** için seçilmiş olan para birimini kullanarak fiyatı bulmak için kullanılan ifadeyi (veya sabit değeri) gösterir.
    - **Varsayılan ifadeler** - Geçerli varsayılanı (**Varsayılan para birimi** alanında gösterilir) kullanarak fiyatı bulmak için ifadeyi (veya sabit değeri) gösterir.

    > [!NOTE]
    > İfade kurallarının **Koşul** alanı varsayılan para birimi tarafından "sahiplenilir"; bu, diğer para birimleri için koşulu değiştiremeyeceğiniz anlamına gelir. **Geçerli para birimi** olarak varsayılan para birimi dışında bir para birimi seçildiğinde de yeni ifade kuralları ekleyemezsiniz.
1. Geçerli para birimi için gereken şekilde **İfade** sütunundaki değerleri düzenleyin.

Aşağıdaki örnekte, _EUR_ varsayılan para birimi, _USD_ ise ek para birimi olarak eklenmiştir.

![Çoklu para birimli model örneği](media/prod-config-rules-currency-example.png "Çoklu para birimli model örneği")

> [!NOTE]
> Varsayılan olmayan bir para birimi için benzersiz ifade kuralları ekleyemezsiniz. Yalnızca varsayılan para birimi dışında bir para birimiyle ilgili olan ifade kuralları oluşturmak için, varsayılan para birimi için fiyat ifadesini sıfır olarak ayarlayın. Sonra varsayılan olmayan para birimi için uygun ifadeyi ayarlayın.

## <a name="test-your-price-model"></a>Fiyat modelinizi test etme

Satış fiyatlarının bir yapılandırma oturumunda nasıl çalıştığını test etmek için, [Satış fiyatı modellerinizi oluşturma](#build-price-model) bölümünde açıklandığı gibi fiyat modelinizin düzenleme sayfasını açın ve eylem bölmesinde **Test**'i seçin. Aşağıdakileri yapabileceğiniz, **Ürün modelini test et** iletişim kutusu açılır:

- Burada sunulan yapılandırma ayarlarını kullanarak ürün seçeneklerini seçin ve sonra **Fiyat ve sevk tarihi** için gösterilen değeri nasıl etkilediğini görün.
- Fiyatın hesaplanma şekli ile ilgili tüm ayrıntıları gösteren bir Excel belgesi indirmek için **Fiyat dökümünü görüntüle**'yi seçin.

![Ürün modelinizi test etme](media/prod-config-test.png "Ürün modelinizi test etme")

İndirilen elektronik tablo her bir etkin fiyat öğesi için hem mutlak değerini hem de yüzde olarak katkıyı gösterir. **Ürün bilgileri yönetim parametreleri** **Ekle** fiyat modelini ayarladıysanız, bu Excel sayfası sipariş veya teklif satırına iliştirilir.

![Fiyat dökümünü gösteren Excel elektronik tablosu](media/prod-config-excel-example.png "Fiyat dökümünü gösteren Excel elektronik tablosu")

## <a name="set-up-selection-criteria-for-price-models"></a>Fiyat modelleri için seçim ölçütü ayarla

Fiyat modelleriniz yerinde olduğunda, teklif veya sipariş olarak yapılandırdığınızda fiyat modeli almak için en az bir seçim ölçütü oluşturmanız gerekir. Bunu bir veya daha fazla sorgu ayarlayarak yapabilirsiniz. Eşleşen satış fiyatı modelleriyle birlikte, sorgular belirli müşteriler, bölgeler, dönemler ve diğer ölçütlere göre satış fiyatlarını hedeflemede büyük esneklik sağlar.

Fiyat modelleri için seçim ölçütü ayarlamak üzere:

1. **Ürün bilgileri yönetimi \>  Ürünler \> Ürün yapılandırma modelleri**'ne gidin.
1. Hedef ürün yapılandırma modelini seçin.
1. Eylem Bölmesinde, **Model** sekmesini açın ve **Ayarla** grubundan **Fiyat modeli ölçütü**'nü seçin. **Fiyat modeli ölçütü** sayfası açılır.
1. İhtiyacınız olan sorgu satırı henüz yoksa, kılavuza yeni bir satır eklemek üzere eylem bölmesinde **Yeni**'yi seçin ve aşağıdaki ayarları yapın:
    - **Ad** -  Bu satır için bir ad girin.
    - **Açıklama** - Sorguyu ve ne için olduğunu kısaca açıklayın.
    - **Fiyat modeli** - Tetiklendiğinde sorgunun uygulanacağı bir [fiyat modeli](#build-price-model) (geçerli yapılandırma modelinden) seçin.
    - **Sipariş türü** - Sorgunun uygulanacağı sipariş türünü seçin.
    - **Geçerlilik başlangıcı** - Sorgunun geçerli olacağı ilk günü belirtin.
    - **Geçerlilik sonu** - Sorgunun geçerli olacağı son tarihi belirtin.

    ![Fiyat modeli ölçütleri](media/prod-config-price-model-criteria.png "Fiyat modeli ölçütleri")

1. Tanımlamak istediğiniz sorgunun satırını seçin ve sonra **Eylem bölmesinde** **Düzenle**'yi seçin. Sorgu tasarımcısı iletişim kutusu açılır. Supply Chain Management'taki çoğu sorgu tasarımcısı gibi çalışır. Seçtiğiniz satırla ilgili fiyat modelinin hangi koşullarda uygulanacağını tanımlamak için bunu kullanın.

1. Gereksinim duyduğunuz her sorgu için 4-5 arasındaki adımları yineleyin.
    > [!TIP]
    > Eklemeniz gereken yeni satıra çok benzer olan mevcut bir satırı kopyalayarak zamandan tasarruf edebilirsiniz. Bunu yapmak için, bir hedef satır seçin ve sonra Eylem Bölmesinde **Çoğalt**'ı seçin.

1. Ölçütlerinizi ayarlamayı bitirdiğinizde, bunları **Fiyat modeli ölçütleri** listesinde doğru sıraya göre düzenleyin. Bir satırı yeniden konumlandırmak için satırı seçin ve sonra Eylem bölmesinde **Yukarı** veya **Aşağı**'yı seçin.

    > [!IMPORTANT]
    > Yapılandırma sırasında, sistem listenin en üstünden aramaya başlar ve teklif veya sipariş satırındaki verilerle eşleşen ilk sorguyu kullanır. Bu nedenle, en son sorguları en üste koymanız gerekir. Genel bir sorguyu listenin en üstüne koyarsanız, yapılandırmada doğru müşteri veya aday müşteriyi hedefleyen listede daha kapsamlı bir sorgu bulunsa bile bu kullanılır.

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a>Ürün modeli sürümü için öznitelik tabanlı satış fiyatları ayarlama

Son adım, ürün modeli sürümü için öznitelik temelli satış fiyatları belirtmektir. Bunun için:

1. **Ürün bilgileri yönetimi \>  Ürünler \> Ürün yapılandırma modelleri**'ne gidin.
1. Hedef ürün yapılandırma modelini seçin.
1. Eylem Bölmesinde, **Model** sekmesini açın ve **Ürün modeli ayrıntıları** grubundan **Sürümler**'i seçin.
1. **Sürümler** sayfası açılır. **Fiyatlandırma yönteminin** **Öznitelik tabanlı** olarak ayarlandığından emin olun.
    ![Fiyatlandırma yönteminin öznitelik tabanlı olarak ayarlama](media/prod-config-versions.png "Fiyatlandırma yönteminin öznitelik tabanlı olarak ayarlama")
