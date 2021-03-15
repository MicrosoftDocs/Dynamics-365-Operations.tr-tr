---
title: Yerleşim ürün boyutu karıştırması
description: Bu konu, konum ürün boyutu karıştırma hakkında bilgiler sağlar. Bu konum profili işlevi, kullanım sektörü gibi ürün çeşitleri veya boyutları olan ürünler kullanıldığında yerleşim yönetiminin artırılmasına yardımcı olur. Konfigürasyonların, renklerin, stillerin ve boyutların belirli bir yerleşim profili için karıştırılıp karışlamayacağını veya bu boyutlardan yalnızca birinin veya bunların bir bileşimin aynı konuma konulacağını belirlemenize olanak tanır.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: c4e42864bfde9ed0650a88961b5a71b33b34c89d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004614"
---
# <a name="location-product-dimension-mixing"></a>Yerleşim ürün boyutu karıştırması

[!include [banner](../includes/banner.md)]

Konum ürün boyutu karıştırma, kullanım sektörü gibi ürün çeşitleri veya boyutları olan ürünler kullanıldığında yerleşim yönetiminin artırılmasına yardımcı olur. Konfigürasyonların, renklerin, stillerin ve boyutların belirli bir yerleşim profili için karıştırılıp karışlamayacağını veya bu boyutlardan yalnızca birinin veya bunların bir bileşimin aynı konuma konulacağını belirlemenize olanak tanır.

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a>Ürün boyut karıştırma özelliğini aç

Konum ürün boyutu karıştırma özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Konum Ürün boyut karıştırma*

## <a name="setup"></a>Ayar

Ambardaki her konumun, konum özelliklerini açıklayan, kendisiyle ilişkili bir konum profiline sahip olması gerekir. Bu nedenle, oluşturulduktan sonra, aynı yerleşim profilini kullanan tüm konumlar ürün boyutu karıştırmaya izin verebilir.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>Ürün boyutu karıştırılmasına izin vermek için yerleşim profillerini konfigüre et

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.
1. Yerleşim profilleri listesinde **toplu** 'u seçin .
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Genel** hızlı sekmesinde, **ürün boyutuna özel karıştırma** seçeneğini *Evet* olarak ayarlayın.

    > [!NOTE]
    > Bu seçeneği yalnızca, **karışık öğelere izin ver** seçeneği *Hayır* olarak ayarlanmışsa *Evet* olarak ayarlayabilirsiniz .

1. **İzin verilen ürün boyutlandırma karışımı** hızlı sekmesinde, **Boyut** seçeneğini *Evet* olarak ayarlayın. Bu konuda açıklanan senaryoda, karıştırma yalnızca farklı **boyut** boyutları olan ürünler için yapılabilir . Ancak diğer seçenekler de kullanılabilir.
1. **Kaydet**'i seçin.

### <a name="create-a-new-product-master-and-product-variants"></a>Yeni ana ürünler ve ürün çeşitleri oluşturun

1. **Ürün bilgi yönetimi \> Ürünler \> Ana ürünler**'e gidin.
1. Eylem bölmesinde **Yeni**'yi seçerek ürün uzmanı oluşturun.
1. **Yeni ürün** iletişim kutusunda aşağıdaki değerleri ayarlayın.

    - **Ürün türü:** *Madde*
    - **Ürün alt türü:** *Ürün Yöneticisi*
    - **Ürün numarası:** *B0001*
    - **Ürün adı:** *B0001 boyutu*
    - **Ürün boyut grubu:** *Boyut*
    - **Yapılandırma teknolojisi:** *Önceden tanımlanan değişken*

1. **Tamam**'ı seçin.
1. **Ürün ayrıntıları** sayfasında, **genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Çeşitleri otomatik olarak oluştur:** *Evet*
    - **Boyut grubu:** *CASUALDHIR*

1. Önceden tanımlanmış varyantları görüntülemek için eylem bölmesinde **ürün varyantlarını** seçin .

    **Ürün çeşitleri** sayfası görüntülenir ve boyut grubu konfigürasyonundaki varyantlar listesini gösterir.

### <a name="release-products-to-the-usmf-company"></a>USMF şirketi ürünlerini serbest bırakın

1. Eylem bölmesinde **Ürünleri kullanıma sun**'u seçin.
1. **Serbest bırakmak için ürünleri seçin** sayfasında, ürün numarası *B0001* listede olduğunu onaylayın ve **ileri**'yi seçin.
1. Serbest bırakmak üzere ürün varyantlarını onaylamak için **ileri** 'yi seçin.
1. **Yayınlanacak firmaları seçin** sayfasında, *USMF*'yi seçin ve sonra seçimi onaylamak için **ileri**'yi seçin.
1. **Seçimi Onayla** sayfasında, yayımı tamamlamak için **son**'u seçin.

    Bir "İş Tamamlandı" iletisi alırsınız.

### <a name="update-a-released-product-in-the-usmf-company"></a>USMF şirketinde yayınlanmış bir ürünü güncelleştirme

1. **USMF** şirketinde oturum açtığınızdan emin olun.
1. Serbest bırakılan ürün ayrıntıları sayfasını açmak için **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılan ürünler**'i seçin.
1. **Serbest bırakılmış ürün ayrıntıları** sayfasını açmak için madde numarası *B0001* bulun ve seçin .
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Genel** hızlı sekmesinde, **Madde modeli grubu** alanının *FIFO* olarak ayarlandığından emin olun .
1. Eylem Bölmesi'nde, **Ürün** sekmesindeki **Ayar** gurubunda **Boyut grupları**'ni seçin.
1. Aşağıdaki değerleri ayarlayın:

    - **Depolama boyutu grubu:** *Ambar*
    - **İzleme boyutu grubu:** *Yok*

1. **Tamam**'ı seçin.
1. Eylem Bölmesi'nde, **Ürün** sekmesindeki **Ayar** gurubunda **Rezervasyon hiyerarşisi**'ni seçin.
1. **Rezervasyon hiyerarşisi** alanını *varsayılan* olarak ayarlayın ve **Tamam** 'ı seçin.
1. **Genel** hızlı sekmesinde, **Yönetim** bölümünde seçimlerinizin güncelleştirilmiş olduğuna dikkat edin.
1. **Satın alma** hızlı sekmesinde, **Fiyat** alanında, *10* girin.
1. **Maliyetleri yönet** hızlı sekmesinde, **Madde grubu** alanında *Ses* girin.
1. **Satın alma** hızlı sekmesinde, **Fiyat** alanında, *10* girin.
1. **Ambar** hızlı sekmesinde, **Ünite sıralama grubu kodu** alanına, *beher*'ı girin.
1. **Kaydet**'i seçin.

### <a name="create-a-location-directive"></a>Yerleşim yönergeleri oluşturma

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. Sol bölmedeki **İş emri türü** alanında *Satın alma emirleri*'ni seçin.
1. Listede, *24 SAS Direct* olarak adlandırılan konum yönergesini seçin.
1. **Konum Yönerge Eylemleri** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** *1*

        Yeni satır önceden varolan satırın önünde olmalıdır. Değişikliği yapmak için, araç çubuğunda **yukarı taşı** ve **Aşağı Taşı** düğmelerini kullanın veya varolan satırın **sıra numarası** değerini *2* olarak değiştirin.

    - **Ad:** *toplu yerleşim profiline koy*
    - **Sabit yerleşim kullanımı:** *Sabit ve sabit olmayan yerleşimler*
    - **Negatif stoka izin ver:** *Bu onay kutusunun işaretini kaldırın (=Hayır)*
    - **Toplu iş etkin:** *Bu onay kutusunun işaretini kaldırın (=Hayır)*
    - **Strateji:** *Yok*

1. Yeni satır seçiliyken, kılavuzun üzerinde **Düzenle sorgu** seçin.
1. Sorgu iletişim kutusundaki **Aralık** sekmesinde **Ekle**'yi seçerek kılavuza bir satır ekleyin:
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** *Yerleşimler*
    - **Türetilmiş tablo:** *Yerleşimler*
    - **Alan:** *Yerleşim profili kodu*
    - **Ölçüt:** *BULK*

1. **Tamam**'ı seçin.
1. **Konum direktifleri** sayfasında, yeni yerleşim yönergesini kaydetmek için **Kaydet**'i seçin.

> [!NOTE]
> **Konum yönergesi eylemleri** Hızlı sekmesi **strateji** alanında, *Sağlamlaştırma* konum stratejisini kullanırsanız **yerleşim profillerinde** **izin verilen ürün boyut karıştırma** hızlı sekmesinin kurulumu geçersiz kılınır ve bu davranışa kurulum tarafından izin verilmese bile maddeler aynı yerleşime yerleştirilir.

### <a name="create-a-mobile-device-menu-item"></a>Mobil cihaz menü öğesi oluşturma

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Eylem bölmesinde, sıralama amacıyla kullanılacak menü öğesini oluşturmak için **yeni** 'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Menü madde adı:** *Satınalma siparişi satın alma*
    - **Başlık:** *Satınalma siparişi satın alma*
    - **Mod:** *İş*
    - **Varolan çalışmayı kullan:** *Hayır*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **İş oluşturma işlemi:** *Satınalma siparişi satırı alma ve yerleştirme*
    - **Plaka oluştur:** *Evet*

1. **Kaydet**'i seçin.

### <a name="configure-the-mobile-device-menu"></a>Mobil cihaz menüsünü yapılandırma

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.
1. Menüler listesinde **Gelen**'i seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Mevcut menüler ve menü öğeleri** listesinde, **SAS satırı teslim** menüsü maddesini bulun ve seçin.
1. **SAS satırı alma** menü öğesini **menü yapısı** listesine taşımak için sağ ok düğmesini seçin. Böylece, yeni menü öğesini seçili menüye eklersiniz.
1. **Kaydet**'i seçin.

## <a name="scenario"></a>Senaryo

Bu gösteri senaryosu, *yerleşim profili karışık maddeler* için izin vermediği halde Ürün boyutu karıştırma özelliği etkin olduğunda, iki farklı ürün varyantın aynı yerleşime nasıl koyulacağını gösterir. Bu durumda **ölçüt** olarak size varyantını kullanacaksınız.

Başlamadan önce, ambar *24*'te *toplu* yerleşim profili kullanan boş konumlar olduğundan emin olun.

### <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma

Üç satır içeren bir satınalma siparişi oluşturulur: aynı ürün numarası için iki satır, ancak farklı **Boyut** çeşitleri ve çeşitlere sahip olmayan farklı bir ürün için üçüncü bir satır oluşturacaksınız.

1. **Borç hesapları \> Satın alma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Satın alma siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Satıcı hesabı:** *1001*
    - **Ambar:** *24*

1. **Tamam**'ı seçin.
1. Satınalma siparişi oluşturulur ve **Satınalma siparişi satırları** hızlı sekmesi üzerine yeni bir satır eklenir. Satın alma siparişi numarasını not edin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *B0001*
    - **Boyut** *L*
    - **Miktar:** *2*

1. Kılavuzun üzerinde **Satır ekle**'yi seçerek ikinci bir saıtın alma sipariş satırı ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *B0001*
    - **Boyut** *XL*
    - **Miktar:** *2*

1. **Satır ekle**'yi seçerek üçüncü satın alma siparişi satırı ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *1*

1. **Kaydet**'i seçin.

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a>Ambar uygulamasında satınalma siparişi satırları al

1. Ambar *24*'te etkin olan bir kullanıcı olarak ambarı uygulamasına oturum açın.
1. **Gelen** menüsünü seçin.
1. **Satın alma satırı alma**'yı seçin.
1. **PONUM** alanını seçin ve satınalma siparişi numarasını girin.
1. Sayfanın altındaki Onayla düğmesini (✔) seçerek girişinizi onaylayın.
1. Alınmakta olan satınalma siparişindeki satır numarasını girin. **LINENUM** alanını seçin ve *1* girmek için numara panelini kullanın.
1. Girişinizi onaylayın.
1. Alınacak miktarı girin. **Miktar** alanındaki değeri *2* olarak artırmak için iki kez artı işareti (**+**) düğmesini seçin.
1. Sayfanın alt kısmındaki düğmeyi (✔) seçerek girdinizi kaydedin ve sonra düğmeyi (✔) tekrar seçerek girdinizi onaylayın.
1. **Satınalma siparişleri: Koyma** sayfası hakkındaki bilgileri görüntüleyin. Bu sayfa, yerine koyma (iş 1) için oluşturulan işi gösterir.

    Alınan maddenin yerleştirileceği yerleşim, lisans levhası, madde, boyut ve henüz tamamladığınız **SAS satırı alma** görevinin miktarı gösterilir.

1. Yerine koyma işini onaylayın.
1. Satınalma siparişi satırı 2 için 4- 11 adımlarını tekrarlayın. Ancak 8. adımda bir miktar *1* olarak belirtin.

    Yeni yerine koyma çalışması (İş 2) çalışma 1 ile aynı yerleşim için oluşturuldu.

1. Satınalma siparişi satırı 2 için 4 -11 adımlarını tekrarlayın. 8. adımda kalan miktarı *1* olarak belirtin.

    Yeni yerine koyma çalışması (İş 3) İŞ 1 ve İş 2 ile aynı yerleşim için oluşturuldu. Bu davranış, *Sağlamlaştırma* yerleşim yönergesi stratejisinin kullanıldığı ve *toplu* **yerleşim profilleri** kuruluu üzerindeki **izin verilen ürün boyut karıştırma** Hızlı sekmesinin **Boyut** değişkenin bir konumda karıştırılmasına olanak sağladığından oluşur.

1. Satınalma siparişi satırı 3 için 4- 11 adımlarını tekrarlayın. 8. adımda *A0001* madde numarası için *1* miktarını belirtin.

    Yeni yerine koyma çalışması (İş 4), satınalma siparişi satırları 1 ve 2 için kullanılan konumdan farklı bir yerleşim için oluşturulur. Bu davranış, yerleşim profilinin karışık ürünlere izin vermediği, ancak aynı ürün yöneticisinin karma boyutlarına izin vermediği için oluşur.

1. Sayfanın üst kısmındaki menü düğmesini seçin (bazen hamburger veya hamburger düğmesi olarak da adlandırılır) ve **SS satırı teslim alma** programından çıkmak için **iptal**'i seçin.

> [!TIP]
> Bu senaryoyu tekrarlayabilirsiniz ancak bu sefer *TOPLU* **yerleşim profillerindeki** **Ürün boyut karışımına izin ver** hızlı sekmesi altında **Boyut**  - *Hayır* ayarlayın, böylece ürün boyutlarının hiçbiri karışmaz. Bu durumda, satınalma siparişi aldığınızda, her ürün çeşidi yeni bir konuma yerleştirilecek.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]