---
title: Onayla ve aktar
description: Bu konu, kullanıcıların, o yüklerle ilişkilendirilmiş tüm işleri tamamlayabilmeleri için ambardan sevk yüklemelerini sağlayan Onayla ve transfer özelliğinin nasıl kullanılacağını açıklar.
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate,WHSWorkTemplateTable,WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 70ebe47997f3b5945a433150ae66de6eb41ff12acf4f4f3c8268351116bdd313
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767963"
---
# <a name="confirm-and-transfer"></a>Onayla ve aktar

[!include [banner](../includes/banner.md)]

Kullanıcıların, o yüklerle ilişkilendirilmiş tüm işleri tamamlayabilmeleri için ambardan sevk yüklemelerini sağlayan *Onayla ve transfer* özelliği. Tam olarak çekilmemiş olan yükleme satırlarını içeren bir sevkiyat teslim alındığında, onay kullanıcısına, kalan miktarların yeni bir yük üzerine bölünmesi veya eksik miktarları iptal etmek istenir.

Planlanmış ve kısmen yüklenen yüklerin yeni veya değişen koşullar nedeniyle uyarılmasının nedeni yük bölme destek senaryolarına izin verecek şekilde ayarlanmış sistemler.

İstemci, kısmen yüklenmiş bir yükün kapatılmış ve sevk edilmiş olarak onaylanmasına olanak tanıyan mantığı içerir. Tüm sevk irsaliyeleri ve yükleme satırları (tam veya kısmi satır miktarları dahil) daha sonra, bu geçiş gerekiyorsa ve kurulum bunu yapmanızı istiyorsanız, yeni oluşturulan bir yükleme ve sevkiyat ile başa alınır. Yeni sevkiyatlar ve Yüklemeler, Sevkiyat ve yükleme oluşturmayla ilgili ilk ölçüte göre otomatik olarak oluşturulur ve onların ana öznitelikleri değişmeden kalır. Bir iş emri henüz oluşturulmadıysa ve Kullanıcı bu iptali gerekli hale gelediyse, kalan miktarları otomatik olarak iptal etmek için bir seçenek de vardır.

Bu işlevsellik, tam yükün tek bir kamyona sığmadığı veya yükün bir kısmının geri kalan kısmı sevkiyat için hazır hale geçmeden önce ambarı bırakması gereken senaryoları destekler. Bu senaryolarda, kalan ürünler yeni bir yüklemeye transfer edilebilir ve bu nedenle de yeni bir kamyona aktarılır. Bu özellik, aksi durumda tam yük sevkiyatı gerektirecek şekilde amaçlanan yüklerle kullanılabileceği için, aktarım yöneticilerinin standart dışı veya öngörülemeyen senaryoları çözebilmesi için ek esneklik sağlar.

Bir yük bölündüğünde, *Onayla ve transfer* özelliği aşağıdaki eylemleri gerçekleştirir:

- Yeni yüklemeler ve sevkiyatlar gerektiğinde oluşturulur. Her yükleme veya sevkiyat, orijinal yükleme veya sevk irsaliyesiyle aynı özniteliklerin çoğuna sahip olacaktır. Özel durum, çalışma durumuna göre yeniden hesaplanacak olan yükleme durumudur.
- Kullanıcıya yeni bir yükleme oluşturulduğu bildirilir. Kullanıcıya ayrıca yeni yükün kimliği de bildirilmez.
- Bölünen yükleme satırları, iş başlıkları ve iş satırları yeni yükleme ve sevkiyat bilgileriyle güncelleştirilir.
- Tüm sevkiyat bölünüp, Sevkiyat sürdürülür ve yalnızca yük referansları güncelleştirilir. Sevkiyatın bölünmesi gerekiyorsa, yeni bir sevkiyat oluşturulur.

Kalan miktarlar iptal edildiğinde, çekilmeyen ve kendileri ile ilişkilendirilmiş iptal edilmemiş bir iş bulunmayan tüm yükleme satırı miktarları yükleme işleminden kaldırılır. İşlemde olan herhangi bir iş varsa, Kullanıcı yalnızca yükü bölebilir. Kalan miktarlar iptal edilemez.

Yalnızca aşağıdaki ölçütlere uyan yükleri bölebilirsiniz:

- Bir veya daha fazla yükleme satırında malzeme çekme miktarları var.
- Yükleme durumu, yüklenden daha küçük.
- Yükleme satırı verisi yok. (Bu veriler, hazırlama konumunda lisans levhası konsolidasyonu aracılığıyla oluşturulur ve *Onayla ve transfer* özelliği, lisans levha birleştirmeyi desteklemiyor.)
- Şu anda ambalaj yerleşimindeki sevk için bekleyen stok yok. (Bu *Onayla ve transfer* özelliği, paket istasyonuna çekilen ancak henüz paketlenememiş olan stoğu desteklemez.)

> [!NOTE]
> Bu işlevsellik, malzeme çekme öncesinde hiç çalıştırılmamış ve oluşturmayacak ambarlarda kullanılması gereken taşıma yükleme işlevselliğinden farklıdır, ancak bunun yerine mevcut taşıma alanını malzeme çekme tamamlandıktan sonra yükler.
>
> Yükün genellikle planlandığı ve zaman içinde oluşturulduğu durumlarda, *onaylama ve transfer* özelliğini kullanın, ancak yükleme işleminin mevcut aktarıma (kamyonun gibi) uygun olmadığı durumlarda bazen özel durumlar meydana gelir.

## <a name="turn-on-confirm-and-transfer"></a>Onayla ve transfer 'i aç

*Onayla ve transfer et* özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Onayla ve transfer et*

## <a name="set-up-confirm-and-transfer"></a>Onayla ve transfer'i ayarla

*Onayla ve transfer* özelliğini kullanmak için ilgili yükleme şablonunda bunu açmanız gerekir. Ayrıca, gereksinimlerinize bağlı olarak, iş şablonlarınızı özelliği destekleyecek şekilde hazırlamak isteyebilirsiniz. Bu konunun ilerleyen kısımlarında sağlanan örnek senaryo aracılığıyla çalışmak istiyorsanız, sisteminizi bu bölümde anlatıldığı şekilde ayarlayın. (Bu senaryo şu temel alan **USMF** tanıtım verileri.)

### <a name="prepare-your-load-templates"></a>Yükleme şablonlarınızı hazırlayın

1. **Ambar yönetimi \> Kurulum \> Yük \> Yük şablonları**'na gidin.
1. Eylem bölmesinde, sayfayı düzenleme moduna yerleştirecek **Düzenle** seçin.
1. Özelliği etkinleştirmek istediğiniz varolan her şablon için, **Sevkiyat sırasında yük bölünmesini izin ver** onay kutusunu seçin. Alternatif olarak, **Yeni** bir şablon oluşturmak için yeni 'yi ve gereksinim duyduğunuz şekilde konfigüre edin. Bu şablonu kullanarak oluşturduğunuz her yükleme bu işlevi devralır. (Bununla çalışıyorsanız, **USMF** demo verileri olarak **20' kapsayıcı** yükleme şablonu özelliğini etkinleştirin.)

### <a name="prepare-your-work-templates"></a>İş şablonlarınızı hazırlayın

Bu kurulum tüm durumlarda gerekli değildir. Burada gösterilen örnek, bu konunun ilerleyen kısımlarında sağlanan örnek senaryoyu desteklemek için çalışmanın sevkiyat yoluyla parçalanmasını sağlar. Bu sonuca ulaşmak için başka yollar da vardır.

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. Sayfanın üst kısmındaki kılavuzda, *Onayla ve transfer* özelliğini ayarlamak istediğiniz varolan bir iş şablonunu seçin. (Bununla çalışıyorsanız, **USMF** tanıtım verileri, **51 malzeme çekme** iş şablonu seçeneğini belirleyin.) Alternatif olarak, yeni bir iş şablonu da oluşturabilirsiniz.
1. Eylem Bölmesinde, **Satış** iletişim kutusunu açmak için **Sorguyu düzenle**'yi seçin.
1. **Satış** İletişim kutusundaki **Sıralama** sekmesinde **Ekle**'yi seçerek kılavuza bir satır ekleyin:
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo:** *geçici iş hareketleri*
    - **Türetilmiş tablo:** *geçici iş hareketleri*
    - **Alan:** *Sevkiyat kodu*
    - **Arama yönü:** *Azalan*

1. Ayarlarınızı kaydedip **Satış** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Gruplandırmanın sıfırlanacağı iletisini bildiren bir ileti alırsanız, devam etmek için **Evet** 'i seçin.
1. **Çalışma şablonları** sayfasının üst kısmındaki kılavuzda, az önce düzenlediğiniz şablonu seçin ve sonra eylem bölmesinde **çalışma başlığı sonlarını** seçin.
1. Eylem bölmesinde, sayfayı düzenleme moduna yerleştirecek **Düzenle** seçin.
1. Kılavuzda aşağıdaki değerleri ayarlayın:

    - **Tablo adı:** *geçici iş hareketleri*
    - **Alan adı:** *Sevkiyat kodu*
    - **Bu alana göre gruplandır:** Bu onay kutusunu seçin.

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Sayfayı kapatın.

## <a name="scenario"></a>Senaryo

Bu senaryoda, malzeme çekme işleminin henüz tamamlanmamış olduğu bir örnek gösterilir, ancak şimdiye kadar çekildi olan maddelerin bir kamyon üzerine yüklenmesi ve her zaman sevk edilmeleri gerekir. Bu nedenle, Kullanıcı çekilmemiş yükleme satırlarını yeni bir yük üzerine bölebilir. Böylece tüm veri ilişkileri otomatik olarak güncelleştirilir.

> [!NOTE]
> Bu senaryoda açıklanan belirli değerler, **USMF** demo verilerine dayanır. Bu tanıtım verilerini, özelliği görüntülerken veya nasıl kullanacağınızı öğreniken kullanmanızı öneririz. **USMF** demo verilerini kullanmıyorsanız, kendi değerlerinizi gerektiği gibi değiştirin.

### <a name="step-1-create-a-load-that-has-multiple-load-lines"></a>Adım 1: çoklu yükleme satırları içeren bir yükleme oluşturun

Bu işlevi kullanabilmeniz için, çoklu yükleme satırları içeren bir yükleme olmalıdır. Çekme yerleşimlerinin oluşturacağınız satış siparişlerdeki tüm maddeler için yeterli stok içerdiğinden emin olun. Yerleşim yönergesi kurulumunu gözden geçirin (**Ambar Yönetimi \> Kurulum \> konumu emirleri**) ve satış siparişi çekme için kullanılan malzeme çekme yerleşimlerini not alın. Stoku ayarlamanız gerekiyorsa, el ile hareketler oluşturabilir, stok yenilemeyi veya başka bir akışı kullanabilirsiniz.

Nitelikli bir yük oluşturmak için, önce bu adımları izleyerek üç satış siparişi oluşturun.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Satış siparişleri oluştur** iletişim kutusunu açmak için **Yeni**'i seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri (en azından) ayarlayın:

    - **Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını *ABD-004* (*Mağara Toptan Satış*) olarak ayarlayın.
    - **Genel** hızlı sekmesinde, **Ambar** alanının ayarını *51* yapın.

1. Satış siparişini oluşturmak ve **Satış siparişi oluştur** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişiniz açılır. **Satış siparişi satırları** kılavuzunda, aşağıdaki değerlere sahip bir satır ekleyin:

    - **Madde numarası:** *M9200*
    - **Miktar:** *40*
    - **Birim:** *ea*

1. Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.
1. **Rezervasyon** sayfasını açmak için Eylem bölmesinde, **Lot ayır**'ı seçin.
1. Satış satırında stoku rezerve edin ve **rezervasyon** sayfasını kapatın.
1. Aynı müşteri ve ambar için ikinci bir satış siparişi eklemek üzere 1 ' den 4 ' e kadar olan adımları yineleyin.
1. Aşağıdaki değerlere sahip iki satış satırı ekleyin. Her bir satırı ekledikten sonra, bu satır için 6 ile 8 arasındaki adımlarda belirtilen stoğu rezerve edin.

    - **Satır 1:** **Madde numarası** alanını *M9200* olarak, **Miktar** alanını *30* olarak ve **Birim** alanını *beher* olarak ayarlayın.
    - **Satır 2:** **Madde numarası** alanını *M9201* olarak, **Miktar** alanını *20* olarak ve **Birim** alanını *beher* olarak ayarlayın.

1. Aynı müşteri ve ambar için üçüncü bir satış siparişi eklemek üzere 1 ' den 4 ' e kadar olan adımları yineleyin.
1. Aşağıdaki değerlere sahip iki satış satırı ekleyin. Her bir satırı ekledikten sonra, bu satır için 6 ile 8 arasındaki adımlarda belirtilen stoğu rezerve edin.

    - **Satır 1:** **Madde numarası** alanını *M9201* olarak, **Miktar** alanını *20* olarak ve **Birim** alanını *beher* olarak ayarlayın.
    - **Satır 2:** **Madde numarası** alanını *M9202* olarak, **Miktar** alanını *60* olarak ve **Birim** alanını *beher* olarak ayarlayın.

#### <a name="load-planning-workbench"></a>Yük planlama çalışma ekranı

Yük planlama sürümü, sevk irsaliyelerini oluşturmak ve satış siparişi satırlarını ambara serbest bırakmak için yükleme şablonu kodunu kullanır.

1. **Ambar yönetimi \> Yükler \> Yük planlama çalışma ekranı** öğesine gidin.
1. **Ambar** alanında *51*'i seçin.

    Şimdi oluşturduğunuz satış siparişleri için yük oluşturacaksınız.

1. **Satış satırları** sekmesinde, kılavuzda, yeni satış siparişleriyle ilgili satış satırlarını seçin.
1. Eylem Bölmesinde **Arz ve talep** sekmesindeki **Ekle** grubunda **Yeni yüke**'yi seçin.
1. **Yük şablonu ataması** iletişim kutusunda **Yük şablonu kodunu** *20' Konteyner* olarak ayarlayın.
1. **Tamam**'ı seçin.
1. **Yükleme planlama ekranı** 'nı yükle sayfasının **Yüklemeler** bölümünde , kılavuzda, ambar *51* için yeni oluşturulan yükleme kodunu bulun. **Sevkiyat onay sütunu sırasında yük bölünmeye izin ver** sütununu görene kadar sağa doğru kaydırın. Bu onay kutusu yükleme için seçilmelidir.
1. Yükü seçin.
1. Kılavuzun üzerindeki **serbest bırakma** menüsünde, iş oluşturmak için ambara **serbest bırak**'ı seçin.
1. **Ambara yükleme sürümü** iletişim kutusunda, Hızlı Sekme 'yi **dahil edilecek kayıtlar** yükleme kimliğinizi gösterir.
1. **Tamam**'ı seçin.

    Sistem Sevkiyat ve çalışma işlerini oluştururken "İşlem işlemi" iletisi alabilirsiniz.

1. **Yükleme planlama sürümünü yükle** sayfasının **Yüklemeler** bölümünde , yüklemeniz için yükleme durumu *Dalgalı* olmalıdır. Yükü seçin ve sonra kılavuzun üzerindeki **ilgili bilgi** menüsünde, oluşturulan sevkiyat kimliklerini görüntülemek için **dalga ayrıntıları**'nı seçin. Bitirdiğinizde, **dalgalar** sayfasını kapatın.
1. **Yük planlama sürümünü yükle** sayfasının **Yüklemeler** bölümünde , yükü seçin ve sonra kılavuzun üzerindeki **ilgili bilgi** menüsünde, Satış siparişleri için oluşturulan işi görüntülemek üzere **iş ayrıntılarını** seçin.
1. Oluşturulan iş kimliklerini not edin. Satış siparişi numarasını ve iş koduyla ilişkilendirilmiş sevkiyat kodunu görmek için sağa doğru gitmeniz gerekebilir.

### <a name="step-2-set-up-the-execution-flow-for-mobile-devices"></a>Adım 2: mobil cihazlar için yürütme akışını ayarlama

Mobil cihaz görevleri, iş kodu veya lisans plakası kimliği gibi kullanıcı girdi bilgilerini gerektirecektir. Bu bilgiler, genellikle belgelerde, paketlemeden veya rafa açık olarak bulunan barkodların formundaki ambar kullanıcıları için sağlanır. Senaryoların mobil aygıt adımlarını tamamlamak için, hareketler için iş kimliklerini ve hareketlerdeki maddenin ve hareketlerin lisans levhalarını tanımladığınızı doğrulayın.

1. Ambar *51* için bir kullanıcı kimliği ve parola kullanarak mobil cihazda oturum açın.
1. **Çıkış**'ı seçin.
1. **Satış çekmeyi** seçin.
1. İş kodunu veya lisans plakası kodunu girme seçeneğiniz vardır. İlk satış siparişi için iş kodunu girin ve sonra **GİR** 'i seçin.
1. **Loc** alanına, malzeme çekme yerleşimini onaylamak için gösterilen yerleşimi girin. **GİR**'ı seçin.
1. **LP** alanında Lisans levhası kimlğini girin. Lisans plakası kimliği, madde, ambar ve seçilen konumdan çekilen maddenin konumu için bir eşleşme olmalıdır. Tamamladıktan sonra **Gir**'i seçin.
1. **Madde** alanına, çekilmiş maddeyi onaylamak için madde kodunu girin ve **GİR** seçeneğini belirleyin.
1. **Miktar** alanına, çekilmiş madde miktarını girin ve **GİR** seçeneğini belirleyin.
1. **Hedef LP** alanında hedef lisans levhası kimlğini girin. Hedef Lisans levhaları Kullanıcı tanımlı. Anımsayacağınız bir lisans plakası kodu girdiğinizden emin olun. Geçerli tarihi artı, *19112301* gibi, biçim olarak iki basamaklı bir sıra (YYAAGG\#\#) kullanmanızı öneririz. Tamamladıktan sonra **Gir**'i seçin.
1. Gösterilen bilgileri gözden geçirin. Bu bilgi, Şimdi koyma hareketi için *Koyma* verileri olacak *çekme* bilgileri olacaktır. Tamamladıktan sonra **Gir**'i seçin.

    - Bir **İş Tamamlandı** iletisi alırsınız.

1. İkinci satış siparişinin iş kodu için 4 ile 10 arasındaki adımları yineleyin.

Sonraki adım, kamyona iki adet çekilen lisans levhayı yüklemede kullanılır.

1. Ambar *51* için bir kullanıcı kimliği ve parola kullanarak mobil cihazda oturum açın.
1. **Çıkış**'ı seçin.
1. **Satış yüklemeyi** seçin.
1. Önceki yordamda ilk iş kimliği için oluşturduğunuz Kullanıcı tanımlı hedef lisans levha kodunu girin. Ardından, hedef lisans plağı 'nı **sahne** alanı 'na yerleştirmek için **GİR** 'i seçin.
1. Hedef Lisans plakası kodunu yeniden girin ve sonra Lisans kalıbınızı **BÖLME KAPISI** konumuna koymak için **GİR** 'i seçin.
1. İkinci iş kodu için oluşturduğunuz hedef lisans plakası kodu için 4 ile 5 arasındaki adımları yineleyin.

Şimdi, iki iş kodu kapatılacak (yüklenmiş).

### <a name="step-3-confirm-the-outbound-shipment"></a>Adım 3: Giden sevkiyatı onaylayın

Bu adımda, yükleme için çekilen maddeleri sevk etmek üzere yükleme işlemi için tamamlanan iki satış siparişi ve çalışmayı onayladınız ve çekilmeyen maddeler için yeni bir yük oluşturur. **Yük ayrıntıları** sayfasında giden sevkiyat onayı yapılmalıdır.

1. **Ambar yönetimi \> Yükler \> Yük planlama çalışma ekranı** öğesine gidin.
1. **Yükler** bölümünde, kılavuzda, oluşturduğunuz yükleme kodunun satırını seçin.
1. **Yükleme ayrıntıları** sayfasını açmak için yük kodu bağlantısını seçin.
1. **Yük ayrıntıları** sayfasında, Eylem bölmesinde, **sevk et ve Al** sekmesindeki **Onay** grubunda onayı başlatmak için **giden sevkiyat** 'ı seçin.
1. **Sevkiyat Onayla** iletişim kutusunda, **Sevkiyat onaylanarak yükleme ayırma yöntemi** alanında, *miktarı yeni yük olarak ayır*'ı seçin.
1. **Tamam**'ı seçin.

    "İşlem işlemi" iletisi alabilirsiniz.

    Yükleriniz için sevkiyatın onaylandığını ve bölünen miktardan yeni bir yükleme oluşturulduğunu belirten bilgi iletileri alırsınız.

Yeni oluşturulan yükü görmek için **yük planlama çalışma alanı** sayfasını Yenileyin.

Hareket ilişkilerinin aşağıdaki yollarla güncelleştirilmiş olduğunu da doğrulayabilirsiniz:

- Kalan (işlenmemiş) Sevkiyat ve Sevkiyat satırları yeni yükleme koduyla güncelleştirilir.
- Satış siparişi yeni yükleme koduna bağlıdır.
- Özgün yükleme kalan yükleme satırlarını içermez.
- Kalan iş yeni yükleme KIMLIĞIYLE güncelleştirildi.
- Dalga o kadar aynı kalır.
- Yeni yükün durumu doğru güncelleştirilmiş. (İş durumu _İşlemde_, yükleme durumu da _işlemde_ olmalıdır.)

## <a name="notes-and-tips"></a>Notlar ve ipuçları

- **Yükleme şablonu** parametresi kapalı olduğunda ancak yükleme işlemi başlatılmadan önce, **yükleme sırasında yük bölünmeye izin ver** parametresini de açabilirsiniz. İstenen yüklemeye gidin ve sonra üstbilgi görünümünde parametreyi açın.
- **Miktarı yeni yük olarak ayır** seçeneği, kalan tüm iş başlıklarındaki *işlem* durumları olduğunda da çalışır. Bu nedenle, çalışanlar zaten çekme emirlerini çalıştırıyor olsa bile işlevleri kullanabilirsiniz.
- **Açık** veya *Sürüyor* durumuna sahip kalan iş olduğunda *yerine getirilmemiş miktarı iptal et*'i seçerseniz, şu hata iletisini alırsınız: "kalan yükleme miktarı iptal edilemiyor. Yükleme için çalışma var."
- Kalan çalışma olmadığında ancak yükleme üzerinde serbest bırakılmış yükleme satırları varken **yerine getirilmemiş miktarı iptal et**'i seçerseniz, aşağıdaki hata iletisini alırsınız: "madde için miktar, teslimat altında tanımlanan yüzdeyi aştığından, yükleme sevkiyatı onaylanamadı." Hatayı önlemek için, serbest bırakılmamış yükleme satırındaki **eksik teslimat** yüzdesini yüzde 100 olarak ayarlayabilirsiniz. Serbest bırakılmamış satırlar yeni bir yüklemeye taşınmaz, ancak geçerli yük, eksik teslimat ile onaylanır. Bu durumda, özgün siparişi yeniden serbest bırakabilirsiniz. Bu nedenle, bunu başka şekilde işlemeniz gerekecektir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]