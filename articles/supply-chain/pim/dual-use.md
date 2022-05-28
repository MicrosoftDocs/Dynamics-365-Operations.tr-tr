---
title: Çift kullanımlı mallar
description: Bu konu, çift kullanımlı mal olarak tanımlanan ürünlerin nasıl izleneceğini, ilgili her ürün ve hedef ülkeye ilişkin sertifika numaralarının nasıl depolanacağını ve ilgili faturalara, sevk irsaliyelerine ve/veya satış siparişlerine geçerli sertifika numaralarının nasıl yazdırılacağını açıklar.
author: t-benebo
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 787d0c4ebcf83d6bfec05943f2bb0ddc5961a93a
ms.sourcegitcommit: e18ea2458ae042b7d83f5102ed40140d1067301a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2022
ms.locfileid: "8736047"
---
# <a name="dual-use-goods"></a>Çift kullanımlı mallar

[!include [banner](../includes/banner.md)]

Çift kullanımlı mallar genellikle hem sivil hem de askeri kullanım uygulamaları olan maddelerdir. Örneğin, bir kimyasal gübre veya patlayıcı olarak kullanılabilir. Birçok ülkede, çift kullanımlı malların ihracatına, ithalatına ve taşınmasına ilişkin geçerli özel düzenlemeler vardır. Bu nedenle, çift kullanımlı malların uluslararası ticaretiyle uğraşan şirketlerin çeşitli ilkeleri ve sertifikaları takip etmesi önemlidir.

Çift kullanım özelliği, şirketlere çift kullanımlı mal olarak tanımlanan ürünleri izleme, ilgili her ürün ve hedef ülkeye ilişkin sertifika numaralarını depolama ve ilgili faturalara, sevk irsaliyelerine ve/veya satış siparişlerine geçerli sertifika numaralarını yazdırma konusunda yardımcı olur. Ürünleriniz sevk edildiğinde her zaman güncel sertifikaları içerdiklerinden emin olmanıza yardımcı olur.

Aşağıdaki senaryoyu inceleyin:

1. Sisteminizdeki **Çift kullanım ülke kurulumu** sayfası, Fransa'ya sevkiyatların bir sertifika gerektirdiğini gösterir.
2. X-100 ürünü için **Serbest bırakılan ürün ayrıntıları** sayfası, bunun çift kullanımlı bir mal olduğunu gösterir. Kod, kategori, grup ve rejim öğeleri ürünün ait olduğu ihracat denetim sınıflandırmasını gösterir.
3. **Çift kullanım sertifikaları** sayfası Fransa'ya sevk edildiğinde X-100 ürünü için bir sertifika içerir. Bu sertifikanın süresi 1 Ocak 2020 tarihinde sona erer.
4. 17 Haziran 2020'de, Fransa'da bulunan müşteri şirketi için bir satış siparişi oluşturursunuz ve sipariş X-100 ürünü içerir.
5. Satış siparişini onayladığınızda sistem aşağıdaki bilgileri belirler:

    1. Sipariş, çift kullanımlı mal olan herhangi bir ürün içeriyor mu?
    2. Siparişte çift kullanımlı mallar varsa, hedef ülke çift kullanım için sertifika istiyor mu?
    3. Ülke çift kullanım sertifikası gerektiriyorsa, hedef ülke için her çift kullanımlı mala ilişkin geçerli bir sertifika var mı?

6. Sipariş X-100 ürününü içeriyor, ürün Fransa'ya sevk ediliyor ve ürün için bir Fransa sertifikası var. Ancak, bu sertifikanın süresi sona ermiş. Bu nedenle, aşağıdaki uyarı iletisini alırsınız: "Bu satış siparişindeki bir veya daha fazla çift kullanımlı madde için çift kullanım sertifikaları geçerli değil. Onay işlemine devam etmek istiyor musunuz?"

Bu konu, çift kullanımlı malları ayarlamak ve bu senaryoyu desteklemek için gereken tüm ayarları nasıl yapılandıracağınızı açıklamaktadır.

## <a name="define-dual-use-requirements-for-each-relevant-country"></a>İlgili her ülke için çift kullanım gereksinimleri tanımlama

Farklı ülkelerin, çift kullanımlı mallar için farklı gereklilikleri vardır. Sertifika gerektiren veya gerektirmeyen ülkeleri izlemek için **Çift kullanım ülke kurulumu** sayfası kullanılır. Burada belirttiğiniz bilgiler satış siparişleri oluşturduğunuzda denetlenir ve gerekli sertifikaları sağlamanız anımsatılır.

Farklı ülkeler için çift kullanım gereklilikleri hakkındaki bilgileri ayarlamak üzere aşağıdaki adımları izleyin.

1. **Ürün bilgileri yönetimi \> Kurulum \> Ürün uyumluluğu \> Çift kullanımlı ürünler \> Çift kullanım ülke kurulumu**'na gidin.
2. Düzenlemek için mevcut bir ülke kurulumu seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir ülke kurulumu oluşturun.
3. Seçili veya yeni ülke kurulumu için aşağıdaki değerleri ayarlayın.

    | Alan | Tanım |
    |---|---|
    | Ülke/bölge | Gerekliliklerini izlemekte olduğunuz ülkeyi seçin. |
    | Sertifika Gereklidir | Çift kullanımlı mallar için sertifika gerektiren ülkeler için bu onay kutusunu seçin. Bu sertifikayı gerektirmeyen ülkelerde kutunun işaretini kaldırın. |

## <a name="create-dual-use-categories"></a>Çift kullanım kategorileri oluşturma

Çift kullanımlı mallar genellikle ihracat denetimi sınıflandırma numarasına (ECCN) göre kategorilere ayrılmalıdır. ECCN, maddeleri emtia ve teknoloji gibi etkenleri temel alarak kategorilere ayıran alfasayısal bir koddur. **Çift kullanım kategorileri** sayfası, raporlama amacıyla, kullandığınız kategorilerin listesini oluşturmanıza yardımcı olur.

Çift kullanım kategorileri ayarlamak için aşağıdaki adımları takip edin.

1. **Ürün bilgileri yönetimi \> Kurulum \> Ürün uyumluluğu \> Çift kullanımlı ürünler \> Çift kullanım kategorileri**'ne gidin.
2. Düzenlemek için mevcut bir kategori seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir kategori oluşturun.
3. Seçili veya yeni kategori için aşağıdaki değerleri ayarlayın.

    | Alanlar | Tanım |
    |---|---|
    | Çift kullanım kodu | Tam ECCN kodunu girin (örneğin, *3A001*).|
    | Çift kullanım kategorisi | ECCN kodunun ticari kontrol listesi (CCL) kategori bölümünü girin. Örneğin, ECCN kodu *3A001* için bu değer *3*'tür. |
    | Çift kullanım grubu | ECCN kodunun ürün grubu kısmını girin. Örneğin, ECCN kodu *3A001* için bu değer *A*'dır. |
    | Çift kullanım rejimi | Madde için rejim kodunu girin. Bu kod, maddenin çift kullanımlı olarak sınıflandırılma nedenini tanımlar. Örneğin, ECCN kodu *3A001* için bu değer *001*'dir. |

## <a name="apply-dual-use-categories-to-products"></a>Ürünlere çift kullanım kategorileri uygulama

Bir ürünü çift kullanımlı mal olarak tanımlamak ve ona çift kullanım kategorisi uygulamak için, aşağıdaki adımları izleyin.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. **Serbest bırakılan ürün ayrıntıları** sayfasını açmak için bir ürün oluşturun veya açın.
1. **Dış ticaret** hızlı sekmesinde, geçerli ürünü çift kullanımlı mal olarak tanımlamak için **Çift kullanımlı ürünler** seçeneğini **Evet** olarak ayarlayın.
1. **Çift kullanım kodu** alanını geçerli ürüne uygulanan koda ayarlayın. (Bu kodu **Çift kullanım kategorileri** sayfasında tanımladınız.)

Bir satış siparişi oluşturduğunuzda, bu kurulum işaretlenir.

## <a name="set-up-dual-use-certificates"></a>Çift kullanım sertifikaları ayarlama

Her ürün ve ülke için gerekli çift kullanım sertifikaları ayarlamak ve yönetmek için **Çift kullanım sertifikaları** sayfasını kullanırsınız. Her sertifikanın ülke ve geçerlilik tarihleri gibi ayrıntılarını izleyebilirsiniz. Bu bilgilerin nereye yazdırılması gerektiğini belirtmek için seçenekleri ayarlayabilirsiniz. Örneğin, bilgiler faturaya, sevk irsaliyesine ve/veya satış siparişine yazdırılabilir. Bir satış siparişi oluşturduğunuzda, bu kurulum işaretlenir.

1. **Ürün bilgileri yönetimi \> Kurulum \> Ürün uyumluluğu \> Çift kullanımlı ürünler \> Çift kullanım sertifikaları**'na gidin.
2. Düzenlemek için mevcut bir sertifika seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir sertifika oluşturun.
3. Seçili veya yeni sertifika için aşağıdaki değerleri ayarlayın.

    | Alan | Tanım |
    |---|---|
    | Madde kodu | Bu sertifikanın uygulanacağı çift kullanımlı malın madde numarasını seçin. |
    | Ülke/bölge | Bu sertifikayı kullanmanız gereken hedef ülke veya bölge. |
    | Sertifika numarası | Satıcıya veya müşteriye verilen sertifikada görünen numara. |
    | Etkin | Geçerli sertifikanın geçerli olduğu ilk tarihi seçin.|
    | Bitiş tarihi | Geçerli sertifikanın geçerli olduğu son tarihi seçin. |
    | Faturaya yazdır | Belirtilen tarih aralığında belirtilen ülkeye yönelik faturalara sertifika numarası yazdırmak için bu onay kutusunu seçin. |
    | Sevk irsaliyesine yazdır | Belirtilen tarih aralığında belirtilen ülkeye yönelik sevk irsaliyelerine sertifika numarası yazdırmak için bu onay kutusunu seçin. |
    | Satış siparişine yazdır | Belirtilen tarih aralığında belirtilen ülkeye yönelik satış siparişlerine sertifika numarası yazdırmak için bu onay kutusunu seçin. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
