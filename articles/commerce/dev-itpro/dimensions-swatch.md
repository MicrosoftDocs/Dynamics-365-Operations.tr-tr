---
title: Ürün boyutu değerlerini renk örneği olarak görünecek şekilde yapılandırma
description: Bu konuda, ürün boyutu değerlerinin Microsoft Dynamics 365 Commerce genel merkezde renk örnekleri olarak nasıl yapılandırılacağı açıklanmaktadır.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.openlocfilehash: 4ffbb6a162e87fd19cdb44224adc8c223ba8e903
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638306"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a>Ürün boyutu değerlerini renk örneği olarak görünecek şekilde yapılandırma

[!include [banner](../../includes/banner.md)]

Bu konuda, ürün boyutu değerlerinin Microsoft Dynamics 365 Commerce genel merkezde renk örnekleri olarak nasıl yapılandırılacağı açıklanmaktadır. Ürün boyutları hakkında daha fazla bilgi için bkz. [Ürün boyutları](../../supply-chain/pim/product-dimensions.md).

Dynamics 365 Commerce, ürün çeşitlerini temsil etmek için boyut, stil ve renk boyutlarının kullanımını destekler. Ürün boyutları, ürün varyasyonlarının seçilebilmesi için ürün ayrıntıları sayfalarında (PDF) gösterilen kolay adlara sahiptir. Bu kolay adlara örnek olarak boyutlar için "Küçük", "Orta" ve "Büyük", renkler için "Siyah" ve "Kahverengi" verilebilir. Ancak, bir ürün birçok varyasyonu destekliyorsa her varyasyon için görüntüyü görüntülemek için birden fazla seçim gerekir. Bu nedenle, müşterilerin ürün varyasyonlarına göz atıp seçmesi yavaş ve sıkıcı olabilir.

Boyutlar PDF'lerde renk örneği olarak gösterildiğinde, müşteriler bir ürünün varyasyonlarının görsel önizlemesini alır. Çok çeşitli renklere, desenlere ve dokulara kolayca göz atabilir ve farklı ürün varyasyonlarının kombinasyonlarını hızlı bir şekilde görüntüleyebilirler.

Renk örnekleri olarak görüntüleme boyutları özelliği, Commerce'in boyutları renk örneği olarak göstermek için onaltılık (onaltılık) kodları ve görüntüleri kullanmasını sağlar. Ayrıca, renkler gibi benzer boyutlar ürün listesi sayfalarında gruplandırılabilir. Örneğin, bir müşteri mavi olan ürünleri arıyor. Çeşitli mavi boyut değerleri birlikte gruplandırılırsa arama sonuçları listesi sayfasında mavinin farklı tonlarına sahip ürünler gösterilir. Boyut gruplandırma, ürün iyileştirme deneyimini önemli ölçüde geliştirir ve müşterilerin tek bir ürün arama sorgusu aracılığıyla daha fazla ürün bulmasına yardımcı olur.

> [!NOTE]
> Renk örneği olarak görüntüleme boyutları özelliği Dynamics 365 Commerce 10.0.20 sürümünden önce kullanılabilir.

Aşağıdaki resimde, bir Commerc PDP'deki renklerin renk örnekleri olarak görüldüğü bir örnek gösterilmektedir.

![Ürün ayrıntıları sayfasında renk örneği olarak gösterilen renk örneği.](../dev-itpro/media/swatch_pdp.png)

Aşağıdaki resimde, bir Commerc arama sonuçları liste sayfasındaki renklerin renk örnekleri olarak görüldüğü bir örnek gösterilmektedir.

![Arama sonuçları listesi sayfasında renk örneği olarak gösterilen renk örneği.](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a>Commerce genel merkezinde görüntü boyutlarını renk örnekleri olarak etkinleştirme özelliği

Commerce genel merkezinde renk örnekleri olarak görüntü boyutları özelliğini etkinleştirmek için **Çalışma Alanları \> Özellik yönetimi**'ne gidin ve **Ürün boyutu değerleri için görüntü desteğini etkinleştir** özelliğini açın. Bu özellik bayrağı etkinleştirildiğinde, Commerce genel merkezindeki uygun tablolarda her boyut için üç yeni alan eklenir: **Onaltılık**, **URL** (görüntüler için) ve **RefinerGroup**.

## <a name="configure-dimension-values-in-commerce-headquarters"></a>Commerce genel merkezinde boyut değerlerini yapılandırma

Renk örnekleri olarak görüntüleme boyutları unsuru boyut, stil ve renk boyutları için desteklenir. Uygun boyutlar için onaltılık kod ve resim URL değerleri Commerce genel merkezinde belirtilebilir. Varsayılan olarak, bir boyut için onaltılık kod ve resim URL değerleri sağlanmadıysa, sistem boyutun kolay adının metnini gösterir.

Yapılandırma aşağıdaki düzeylerden herhangi biri ile yapılabilir:

- **Boyut** – Commerce genel merkezinde, **Renk**, **Boyut** veya **Stil** 'i arayarak bir boyutun sayfasını açın. Her sayfada, bir kılavuz boyut değerlerini listeler. Görüntüleme sırasını, onaltılık kodu ve resim URL değerlerini yönetebilirsiniz. Aşağıdaki çizimde bir **Renk** sayfasında yapılandırmanın bir örneği gösterilmektedir.

    ![Renkler sayfasındaki boyut yapılandırması örneği.](../dev-itpro/media/swatch_Color.PNG)

- **Boyut grubu** – Dynamics 365 Commerce içinde, boyut grupları oluşturmak için **RefinerGroup** özelliğini kullanabilirsiniz. Boyut grupları tanımlanmışsa, **Renk grubu**, **Boyut grubu** veya **Stil grubu** arayarak uygun sayfayı açın. Her sayfada onaltılık kod, resim URL'si ve iyileştirici grup değerlerini yönetebilirsiniz. Aşağıdaki çizimde bir **Renk grupları** sayfasında yapılandırmanın bir örneği gösterilmektedir.

    ![Renk grupları sayfasındaki boyut yapılandırması örneği.](../dev-itpro/media/swatch_colorGroup.PNG)

- **Ürün boyutu (ürün oluşturma sırasında)** – Yeni bir ürün oluşturduğunuzda, boyut değerlerini girmek için **Ürün boyutları** sayfasını kullanabilirsiniz. Varolan ürünler için **Onaltılık**, **URL** (görüntüler için) ve **RefinerGroup** alanları zaten ayarlanmış olabilir. Ancak, değerleri istediğiniz gibi değiştirebilirsiniz. Aşağıdaki çizimde bir **Ürün boyutları** sayfasında yapılandırmanın bir örneği gösterilmektedir.

    ![Ürün boyutları sayfasındaki boyut yapılandırması örneği.](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> Onaltılık kod ve resim URL yapılandırmalarını yönetme işlemi, boyutların görüntüleme sırasını yönetmek için kullanılan deseni izler.

## <a name="configure-dimension-values-by-using-hex-codes"></a>Onaltılık kodlar kullanarak boyut değerlerini yapılandırma

Çoğu renk boyutu için, Commerce genel merkezindeki boyut sayfalarında onaltılık kod renk değeri sağlanmalıdır. Örneğin, siyah rengin onaltılık kod değeri **#00000** olmalıdır. Commerce bir site sayfası oluşturduğunda, altıgen kod renkli bir renk örneğiyle temsil edilir.

Aşağıdaki resimde, renk boyutlarının onaltılık kod değerleri kullanılarak yapılandırıldığı bir örnek gösterilmektedir.

![Onaltılık kodları kullanan boyut yapılandırması örneği.](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a>Görüntü URL'leri kullanarak boyut değerlerini yapılandırma

Bazı renk boyutları düz renkleri değil, desenleri temsil eder. Örneğin, bir renk boyutu "leopar" olarak tanımlanabilir. Bu gibi durumlarda, renk örnekleri için onaltılık kodlar yerine yayımlanlanmış görüntüleri kullanarak renk boyutlarını daha etkili bir şekilde temsil edebilirsiniz.

Her resmi Commerce site oluşturucusa yüklemeli ve yayınlamalısınız. Ardından, Commerce genel merkezindeki uygun boyut sayfalarına yayınlanan görüntünün resim URL'sini girin. Renk örneği olarak görüntülenmek üzere bir boyut seçilmişse, ancak bir altıgen kod tanımlanmamışsa, Commerce sayfayı işlerken görüntü araması yapar. Görüntü araması başarısız olursa, Commerce boyutun kolay adının metnini gösterir.

Aşağıdaki çizimde bir **Renkler** sayfasında yapılandırma için görüntü URL'lerinin kullanıldığı bir örneği gösterilmektedir.

![Görüntü URL'lerini kullanan boyut yapılandırması örneği.](../dev-itpro/media/swatch_color_urls.PNG)

Ürün ve kategori görüntüleri için olduğu gibi görüntü URL'lerini tanımlamak için bir medya şablonu kullanabilirsiniz. Site oluşturucuya resim yüklediğinizde, dosya adı kuralları ve dosya yolları tutarlı olmalıdır.

Aşağıdaki çizimde bir Ortam şablonu yapılandırma için görüntü URL'lerinin kullanıldığı bir örneği gösterilmektedir.

![Ortam şablonu yapılandırması örneği.](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a>Hem onaltılık kodları hem de görüntü URL'leri kullanarak boyut değerlerini yapılandırma

Çoğu renk boyutu için hem onaltılık kodları hem de görüntü URL'lerini yapılandırabilirsiniz. Commerce işleme geri dönüş mantığı, renk örneğini göstermek için otomatik olarak bir altıgen kod veya görüntü URL'si arar. Renk boyutlarını yapılandırmak için hem onaltılık kodları hem de görüntü URL'lerini kullanarak, renk sayısı büyük olduğunda görüntü yönetimini basitleştirmeye yardımcı olursunuz.

Aşağıdaki çizimde bir **Renkler** sayfasında yapılandırma için hem onaltılık hem de görüntü URL'lerinin kullanıldığı bir örneği gösterilmektedir.

![Hem onaltılık kodlar hem de Görüntü URL'lerini kullanan boyut yapılandırması örneği.](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a>İyileştirici gruplarını yapılandırma

Boyut değeri için onaltılık kod veya resim URL'si tanımladığınızda, **RefinerGroup** alanı için bir değer de belirtebilirsiniz. Bu alan, iyileştirici deneyiminde benzer boyut değerlerini gruplamak için kullanılması gereken boyutu tanımlar.

Örneğin, renk boyutu değerleriniz "mavi", "mavi ekose", "mavi yıkama" ve "koyu mavi" ise, her değer farklı bir onaltılık koda veya resim URL'sine eşlenir. Bu nedenle, her değer uygun ürünler için PDF'lerde ve ürün kartlarında farklı bir renk olarak görünecektir. Ancak, tüm bu renk boyutu değerlerini Bir **RefinerGroup** değeri olan **Mavi** ile eşlerseniz, "mavi" ürünler için yapılan bir arama, boyut renk değerleri "mavi", "mavi ekose", "mavi yıkama" ve "koyu mavi" olan ürünler için liste sayfası arama sonuçları oluşturur.

Aşağıdaki resimdeki örnek, Commerce genel merkezindeki **Renk** ve **RefinerGroup** özellikleri arasındaki ilişkiyi gösterir.

![İyileştirici grup yönetimi örneği.](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a>Commerce Site Builder'daki görüntüleri yönetme

Görüntü URL'leri herhangi bir boyut değeri için kullanılıyorsa, ilgili görüntülerin Commerce site oluşturucusa yüklenmesi gerekir. Her görüntünün konumu, Commerce genel merkezindeki görüntü için tanımlanan dosya adı ve klasör yolu ile eşleşmelidir. Resim dosyaları site oluşturucuda uygun kategori konumlarına yüklenmelidir. Örneğin, renkli görüntülerin **Renk** kategorisi klasörüne yüklenmesi gerekir. Görüntüleri site oluşturucu yükleme hakkında daha fazla bilgi için bkz. [Resimleri yükleme](../dam-upload-images.md).

Aşağıdaki resimde, site oluşturucu ortam kitaplığına resim yüklemek için **Dosyaları karşıya yükle** iletişim kutusunun kullanıldığı bir örnek gösterilmektedir. Seçim için kullanılabilen **Boyut**, **Renk** ve **Stil** kategorilerini vurgular.

![Site oluşturucu medya kitaplığına yükleme sırasında resim dosyası kategorileri örneği.](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a>E-ticaret sitesi sayfalarında renk örneği görüntülemeyi etkinleştirme

Renk örneklerinin PDF'ler ve liste sayfaları gibi boyut seçimi gerektiren e-ticaret sitesi sayfalarında görünebilmesi için Önce Commerce genel merkezinde boyut sitesi ayarlarını yapılandırmanız gerekir. Daha fazla bilgi için bkz. [Boyutlar için site ayarları uygulama](../dimension-settings.md)

Ayrıca, arama sonuçları modülleri için **Ürün özniteliklerini arama sonuçlarına ekle** özelliğini etkinleştirmeniz gerekir. Siteniz özelleştirilmiş kategori sayfaları kullanıyorsa, bu sayfalarda kullanılan arama sonuçları modüllerini güncelleştirmeniz gerekir, böylece **ürün özniteliklerini arama sonuçlarına dahil et** özelliği etkinleştirilir. Daha fazla bilgi için bkz. [Arama sonuçları modülü](../search-result-module.md).

## <a name="display-swatches-in-pos-and-other-channels"></a>Renk örneklerini POS ve diğer kanallarda görüntüleme

Commerce şu anda Satış Noktası (POS) ve diğer kanallarda renk örneklerinin görüntülenmesini destekleyen ilk çalıştırma uygulamasına sahip değildir. Ancak, renk örneği görüntüleme işlevini, kanal API'lerinin renk örneklerini işlemek için gereken onaltılık kodları ve görüntü URL'lerini döndürmesini sağlayan bir uzantı olarak uygulayabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Arama sonuçları modülü](../search-result-module.md)

[Boyutlar için site ayarlarını uygulama](../dimension-settings.md)

[Ürün boyutları](../../supply-chain/pim/product-dimensions.md)

[Resmi karşıya yükle](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
