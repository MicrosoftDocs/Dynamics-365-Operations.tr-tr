---
title: Dalga etiketi yazdırma
description: Bu konu, dalga etiketi yazdırma özelliğini ve bunu nasıl ayarlayabileceğinizi açıklamaktadır.
author: GarmMSFT
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fe04b841dbb3bb237de53f74d73f2b3f9162ae6b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840449"
---
# <a name="wave-label-printing"></a>Dalga etiketi yazdırma

[!include [banner](../includes/banner.md)]

Dalga etiketi yazdırma özelliği, dalga yürütme sırasında doğrudan dalga şablonundan etiket oluşturup yazdırmanıza olanak sağlayan yeni bir dalga adımı yöntemi sunarak, etiket yazdırmaya alternatif bir yaklaşım sunar. Böylece, çalışanlar bir mobil cihazda iş emrini çalıştırmadan önce etiketler kullanılabilir durumda olur. Çalışanlar, gerekli etiketleri malzeme çekme sonrasında değil malzeme çekme sırasında ekleyebilir.

Dalga etiketi yazdırma etiket düzenleri oluşturmak için Zebra Programlama Dili (ZPL) kullanır. Etiket düzeni, yinelenen yapıya sahip etiketlere izin vermek üzere üç bölüme (üstbilgi, gövde ve altbilgi) bölünmüştür. Dalga etiketi şablonları sisteme hangi etiket düzeninin kullanılacağını söyler. Kullanıcılar hangi yazıcının kullanılacağını belirtebilir. Ayrıca, gerekirse etiketleri aynı anda birçok yazıcıda da yazdırabilirler. **Dalga etiketi geçmişi** sayfası, bu kurulum kullanılarak oluşturulmuş tüm etiketlerin kayıtlarını gösterir.

Etiketleri iş başlıklarına göre yazdırabilir ve harmanlayabilir, her iş başlığı için kesme etiketleri yazdırabilir ve konteyner içerik etiketlerini, kutu etiketlerini ve diğer benzer etiketleri yazdırabilirsiniz.

> [!NOTE]
> Bu işlev, belge yönlendirmeyi temel alan mevcut etiket yazdırma işlevinin yerini almaz.

Dalga etiketi yazdırma özelliği aşağıdaki geliştirmeleri sunar:

- Etiketleri, tek bir iş satırındaki koli sayısına göre konteyner kullanımı olmadanyazdırın. (Bir "koli", birim sıra grubu satırlarında belirlenmiş bir birimdir.)
- Birkaç farklı etiket sırasını (örneğin, karton ve palet etiketleri) yazdırın.
- Etiket numaralandırmasını (örneğin, 1/124, 2/124,... 124/124) dahil edin ve numaralandırma aralığını tanımlayın (örneğin iş satırı, yük satırı veya sevkiyat).
- Konşimento oluşturulmadan önce, bir konşimento kodu oluşturun ve etiketlere yazdırın.
- Her koli için benzersiz bir seri sevkiyat konteyner kodu (SSCC) oluşturun ve her etikete ekleyin.
- Konşimento kodları ve SSCC'ler için GS1-uyumlu numara serileri oluşturun.
- Etiketleri hem mobil uygulamadan hem de zengin istemciden yeniden yazdırın.
- Etiketleri hükümsüz kılın (örneğin, eksik çekme senaryolarında) ve yeniden yazdırın.
- Dalga etiketi geçmişini temizleme.
- Belge yönlendirme düzenlerinde yapılan geliştirmeler, belge yönlendirme düzenleri ile dalga etiketi düzenleri arasında paylaşılır. (Daha fazla bilgi için bkz. [Plakalar için belge yönlendirme düzeni](../warehousing/document-routing-layout-for-license-plates.md).)

Bu geliştirmeler, paletlemeden önce kolileri etiketlemeyi daha etkili hale getirir. Bunlar özellikle, her koliyi ayrı olarak tarayıp sipariş girişlerini otomatik olarak onaylayan büyük perakendecilere sevkiyat yapan şirketler için yararlıdır.

> [!NOTE]
> İş gereksinimlerinize bağlı olarak, bu konuda açıklanan yapılandırma senaryolarını ayrı olarak veya birlikte uygulayabilirsiniz. Sırayla çalışan birkaç dalga etiketi şablonu (senaryo 3'te gösterildiği gibi) tasarlayabilirsiniz. Örneğin, koli etiketlerini yazdırmak için senaryo 1'i, palet etiketleri yazdırmak için de senaryo 2'yi kullanabilirsiniz (stoktaki paletler boyut ve kompozisyon olarak farklılık gösteriyorsa).

## <a name="turn-on-the-wave-label-printing-feature"></a>Dalga etiketi yazdırma özelliğini açma

*Dalga etiketi yazdırma* özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Dalga etiketi yazdırma*

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a>Senaryo 1: Tek bir dalga etiketinin oluşturulduğu dalga etiketi yazdırma

Bu senaryoda, bir şirketin sipariş girişlerini her koliyi ayrı olarak tarayarak otomatik onaylayan büyük bir perakendeci için sevkiyat etiketlerini nasıl yazdırabileceği gösterilmektedir.

Bu senaryo uçtan uca akışı gösterir.

### <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu senaryoyu izlemek için, demo verilerinin yüklenmiş olması ve **USMF** tüzel kişiliğini kullanmanız gerekir.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Dalga etiketi yönteminin kullanılabilir olduğundan emin olun

Dalga etiketi yazdırma yöntemini kullanılabilir hale getirmek için dalga işlemi yöntemlerini yeniden oluşturmanız gerekebilir.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga işleme yöntemleri**'ne gidin.
1. **waveLabelPrinting** öğesinin listede olduğunu onaylayın. Seçili değilse, eklemek Için eylem bölmesindeki **Yöntemleri yeniden üret**'i seçin.

### <a name="configure-a-wave-template"></a>Dalga şablonu yapılandırma

Dalga şablonları, belirli dalga yöntemi örneklerini ilgili dalga etiketi şablonuna bağlayabilmenizi sağlar.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.
1. **62 Sevkiyat Varsayılanı** gibi bir şablon seçin.
1. **Yöntemler** hızlı sekmesinde, **Dalga etiketi yazdırma** yöntemini **Seçili yöntemler** sütununa taşıyın.
1. **Seçili Yöntemler** sütununda, **Dalga etiketi yazdırma** yöntemini seçin ve **Dalga adımı kodu** alanını *PrintLabel* olarak ayarlayın. Dalga adım kodları hakkında daha fazla bilgi için bkz. [Dalga adımı kodları](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Dalga etiketi düzeni oluşturma

Etiket düzeni, etiket üzerine hangi bilgilerin basıldığını ve bunun nasıl yerleştirileceğini denetler. Buraya, yazıcıya gönderilen ZPL kodunu girersiniz.

1. **Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi düzenleri** öğesine gidin.
1. Aşağıdaki ayarlara sahip bir kayıt oluşturun:

    - **Etiket düzeni kodu:** *Koli*
    - **Açıklama:** *Koli (SSCC)*

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem bölmesinde, **Dalga etiketi satır ayarları**'nı seçin.

    **Dalga etiketi satır ayarları** sayfası görüntülenir. Burada, etiketin dinamik parçasını yapılandırabilirsiniz.

1. Aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Satır kodu:** *WaveLabel*
    - **Satır tablosu adı:** *WHSWaveLabel*
    - **Satır başlangıç konumu:** *0*

        Bu alan, satırın etikette başlayacağı dikey konumu tanımlar.

    - **Satır yüksekliği:** *0*

        Bu alan, ZPL standardına göre her satırın yüksekliğini (punto olarak) tanımlar. Yatay etiketler için satır yüksekliği pozitif, dikey etiketler için negatif olur. Bu örnekte tek bir satır olduğu için, değeri *0* (sıfır) olarak ayarlayabilirsiniz.

    - **Sayfa başına satır:** *1*

        Bu alan, her bir etikete yazdırılabilen satır sayısını tanımlar.

        > [!NOTE]
        > Bu kurulum, dalga etiketleri tablosundaki her kayıt için ayrı bir ZPL etiketinin yazdırılmasına neden olur.

1. Sayfayı kapatın.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Tablo:** *İş satırları*
    - **Türetilen tablo:** *İş satırları*
    - **Alan:** *İş türü*
    - **Ölçüt:** *Malzeme çekme*

    Bu sorgu yalnızca çekme türü iş satırlarının etiket üzerine yazdırılmasını (yerine koyma türü iş satırları değil) sağlar.

1. Konşimento kodunu yazdırabilmek istiyorsanız, **Birleşimler** sekmesinde **İş satırları** tablosunu seçin ve **Sevkiyatlar** tablosunu bu tabloya birleştirin.
1. Sorgu düzenleyicisi iletişim kutusunu kapatın.
1. **Yazıcı metin düzeni** hızlı sekmesinde, yazıcı kodunu yazabileceğiniz üç bölüm vardır: **Üstbilgi bölümü**, **Gövde bölümü** ve **Altbilgi bölümü**. **Üstbilgi bölümü** bölümünde, **Etiket başlığı** alanına gereken başlığa ait kodu girin. Örneğin, Zebra yazıcılar kullanıyorsanız, aşağıdaki kodu kullanabilirsiniz.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. **Gövde bölümü** bölümünde, **Etiket gövdesi** alanına gövde için gereken ZPL kodunu girin. Aşağıda bir örnek verilmiştir.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. **Gövde bölümü** bölümünde, **Etiket alt bilgisi** alanına alt bilgi için gereken ZPL kodunu girin. Aşağıda bir örnek verilmiştir.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Bu kurulum her etiketin bir kopyasını yazdırır. Daha fazla kopyaya gereksinim duyarsanız (örneğin, paletin her iki tarafı için bir kopya), alt bilgideki **\^PQn** bölümü için **n** değerini gerekli kopya sayısı olarak ayarlayın. Örneğin, her etiketin dört kopyasını yazdırmak için **\^PQ4** girin.

Etiketiniz şimdi kullanıma hazır.

### <a name="create-a-wave-label-type"></a>Dalga etiketi türü oluşturma

Dalga etiketi türleri, dalga etiketi şablonlarını birim dizi grubu satırlarındaki bir birime bağlamak için kullanılır.

1. **Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi türleri** öğesine gidin.
1. Aşağıdaki ayarlara sahip bir dalga etiketi türü ekleyin:

    - **Etiket türü:** *Koli*
    - **Açıklama:** *Koli*

### <a name="set-up-unit-sequence-groups"></a>Birim sıra gruplarını ayarla

Sonra, dalga etiketi türü için birim sırası grubunu ayarlayın.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri\> Birim sırası grubu**'na gidin.
1. **Ea Kutu PL** grubunu seçin.
1. **Kutu** satırı için **Dalga düzeyi türü** alanını *Koli* olarak ayarlayın.

### <a name="create-a-wave-label-template"></a>Dalga etiketi şablonu oluşturma

Sonra, dalga etiketi türü için dalga etiketi şablonunu oluşturun.

1. **Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi şablonları** öğesine gidin.
1. Dalga düzeyi şablonu ekleyin ve üst bilgide aşağıdaki değerleri ayarlayın:

    - **Etiket şablonu adı:** *Koli etiketleri*
    - **Açıklama:** *Koli etiketleri*
    - **Dalga adımı kodu:** *PrintLabel*
    - **Ambar:** *62*

1. **Genel** hızlı sekmesinde, **Dalga etiketi türü** alanını *Koli* olarak ayarlayın.
1. **Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, aşağıdaki ayarlara sahip yeni bir satır ekleyin:

    - **Etiket düzeni kodu:** *Koli*
    - **Yazıcı adı:** Uygun bir ZPL yazıcı seçin.
    - **Sorguyu çalıştır:** *Evet* (Bu ayar isteğe bağlıdır, ancak en iyi performans için önerilir.)

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. İsteğe bağlı: Müşteriye özel etiket tasarımını ayarlıyorsanız, müşterinin hesabını bulmak için bir sorgu oluşturmanız gerekir. **Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, **Sorguyu düzenle**'yi seçin. Ardından, sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Tablo:** *Sevkiyatlar*
    - **Türetilmiş tablo:** *Sevkiyatlar*
    - **Alan:** *Hesap numarası*
    - **Ölçüt:** İlgili müşteri hesap numarasını girin.

    Bitirdiğinizde sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.

1. Eylem Bölmesinde, tam etiket şablonu için sorgu düzenleyicisi iletişim kutusunu açmak için **Sorguyu düzenle**'yi seçin.
1. Sorgu düzenleyicisi iletişim kutusunda **Tasnif** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Tablo:** *İş satırları*
    - **Türetilen tablo:** *İş satırları*
    - **Alan:** *Referans yükleme satırı kodu (Kayıt kodu)*
    - **Arama yönü:** *Artan*

1. Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Bir ileti kutusu, gruplandırma sıfırlama işlemini onaylamanızı ister. Devam etmek için **Eve**'i seçin.
1. Eylem bölmesinde, **Dalga etiketi şablon grubu**'nu seçin.
1. **Dalga etiketi şablon grubu** iletişim kutusunda, **Referans alan adı** alanının *Referans yük satırı kodu*'na ayarlandığı satırı seçin ve sonra bu satır için **Etiket derleme kodu** onay kutusunu seçin.

    > [!NOTE]
    > Bu kurulum, iş gruplandırma kurulumu ne olursa olsun, dalga boyunca her yükleme satırı için bir etiket sırası ("Koli 1/X") oluşturacaktır. Bu etiket sırası etiket düzeninde yazdırılabilir.

### <a name="configure-number-sequence-extensions"></a>Numara serisi uzantıları yapılandırma

Numara serisi uzantıları, belirli numara serilerinin GS1 uyumluluğunu denetler. Bu yapılandırma, geçerli senaryo için isteğe bağlıdır. Daha fazla bilgi ve yapılandırma yönergeleri için bkz. [Numara serisi uzantılarını yapılandırma](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Satış siparişi oluşturma ve ambara serbest bırakma

1. **Satış ve pazarlama \> Satış siparişi \> Tüm satış siparişleri**'ne gidin.
1. Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Ambar:** *62*

1. Aşağıdaki ayarlara sahip iki satış siparişi satırı ekleyin.

    - Satış sipariş satırı 1:

        - **Madde numarası:** *A0001*
        - **Miktar:** *9024*
        - **Birim:** *ea* (9024 ea = 376 Kutu = 47 PL)

    - Satış sipariş satırı 2:

        - **Madde numarası:** *A0002*
        - **Miktar:** *9016*
        - **Birim:** *ea* (9016 ea = 322 Kutu = 46 PL)

    > [!NOTE]
    > Burada sunulan maddeler ve miktarlar yalnızca örnektir. Bunlar için daha önce tanımladığınız birim sırası grubunu kullanmaları, bunlar için *ea*'dan *kutu*'ya *PL*'ye uygun birim dönüşümlerinin tanımlanması ambar *62*'de stokta bulunmaları gerekir. Daha fazla bilgi için, bkz. [Ölçü birimi ve stoklama ilkeleri](unit-measure-stocking-policies.md).

1. Satış siparişi satırı 1'i seçin. Ardından, **Satış siparişi satırı** bölümünde **Stok** menüsünde **Rezervasyonlar**'ı seçin.
1. **Rezervasyon** sayfasında, Eylem Bölmesi'nde **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.
1. Satış siparişi satırı 2 için 4 ve 5 numaralı adımları yineleyin.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

    Aşağıdaki olaylar gerçekleşir:

    - Sistem, oluşturulan sevkiyatı etiket yazdırma adımını içeren şablonu kullanarak işler. Etiket düzeni, etiketin biçimini tanımlamak için kullanılır ve sonuç etiket şablonunda seçilen yazıcıda yazdırılan bir etiket olacaktır.
    - Dalga etiketleri oluşturulur ve yazdırılır. Etiket sayısı koli sayısına eşit olacaktır (bu örnekte, satır 1 için 376 Kutu etiketi ve satır 2 için 322 kutu etiketi).
    - Sevk irsaliyeleri için yeni bir konşimento kodu oluşturulur. Numara serisi uzantılarını yapılandırdıysanız, dalga etiketi kodları **SSCC-18** numara biçimini izler. 

Dalga etiketlerini aşağıdaki sayfalardan görüntüleyebilir ve yeniden yazdırabilirsiniz. Her sayfanın Eylem Bölmesinde **Sevkiyatlar** sekmesindeki **İlgili bilgiler** grubunda **Dalga etiketleri**'ni seçin.

- Tüm sevkiyatlar \> Sevkiyat ayrıntıları
- Tüm yükler \> Yük ayrıntıları
- Tüm dalgalar
- Dalga etiketleri
- Dalga etiketi geçmişi

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a>Senaryo 2: Konteyner kullanımı için dalga etiketi yazdırma (dalga etiketi kayıtları olmadan)

Bu senaryo, maddeleri otomatik olarak kolilere bölmek için konteyner kullanımı etiketleri kullanırken dalga etiketlerini yazdırmanıza olanak tanır ve bu nedenle bir dalga etiketi kaydı gerektirmez. Bu durumda, konteyner kodu SSCC için bir yer tutucu olarak işlem gerçekleştirir.

Bu senaryo ve senaryo 1 arasındaki başlıca farklar aşağıdadır:

- **Dalga etiketi şablonları:** Dalga etiketi şablonunda bir dalga etiketi türü seçemezsiniz ve etiket derleme gruplandırması gerekli değildir. Aksi durumda, dalga etiketi şablonunu yapılandırırsınız ve senaryo 1'de açıklanan şekilde dalga şablonuna bağlarsınız. Dalga etiketlerinin oluşturulmasını önlemek için dalga etiketi türünü boş bırakmanız gerekir.
- **Dalga etiketi düzenleri:** Dalga etiketi kayıtları yerine iş satırları için dalga etiketi düzen satırı ayarlarını yapılandırırsınız. Etiket düzeni için satır ayarını **WHSWaveLabel** tablosu yerine  **WHSWorkLine** tablosunu kullanarak yapılandırmanız gerekir. **Sayfa başına satır sayısı** ayarı, gövde bölümünde bulunacak satır sayısını denetler. 

Bu yapılandırma ayrıca, birden fazla farklı maddenin tek etiketli bir kutu veya bir palette bulunduğu iş senaryolarında kullanılabilir ve bu paketleme süreci iş oluşturma ile (örneğin, sevkiyata göre gruplandırılan iş) tanımlanabilir.

Bu senaryo uçtan uca akışı gösterir.

### <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu senaryoyu izlemek için, demo verilerinin yüklenmiş olması ve **USMF** tüzel kişiliğini kullanmanız gerekir.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Dalga etiketi yönteminin kullanılabilir olduğundan emin olun

Dalga etiketi yazdırma yöntemini kullanılabilir hale getirmek için dalga işlemi yöntemlerini yeniden oluşturmanız gerekebilir.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga işleme yöntemleri**'ne gidin.
1. **waveLabelPrinting** öğesinin listede olduğunu onaylayın. Seçili değilse, eklemek Için eylem bölmesindeki **Yöntemleri yeniden üret**'i seçin.

### <a name="set-up-a-wave-template"></a>Dalga şablonu ayarlama

Dalga şablonları, belirli dalga yöntemi örneklerini ilgili dalga etiketi şablonuna bağlayabilmenizi sağlar.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.
1. **63 Konteyner Kullanımı** gibi bir şablon seçin.
1. **Yöntemler** hızlı sekmesinde, **Dalga etiketi yazdırma** yöntemini **Seçili yöntemler** sütununa taşıyın.
1. **Seçili Yöntemler** sütununda, **Dalga etiketi yazdırma** yöntemini seçin ve **Dalga adımı kodu** alanını *PrintLabel* olarak ayarlayın. Dalga adım kodları hakkında daha fazla bilgi için bkz. [Dalga adımı kodları](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Dalga etiketi düzeni oluşturma

1. **Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi düzenleri** öğesine gidin.
1. Aşağıdaki ayarlara sahip bir kayıt oluşturun:

    - **Etiket düzeni kodu:** *Koli*
    - **Açıklama:** *Koli (SSCC)*

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem bölmesinde, **Dalga etiketi satır ayarları**'nı seçin.

    **Dalga etiketi satır ayarları** sayfası görüntülenir. Burada, etiketin dinamik parçasını yapılandırabilirsiniz.

1. Aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Satır kodu:** *WorkLine*
    - **Satır tablosu adı:** *WHSWaveLine*
    - **Satır başlangıç konumu:** *500*

        Bu alan, satırın etikette başlayacağı dikey konumu tanımlar.

    - **Satır yüksekliği:** *-50*

        Bu alan her satırın yüksekliğini tanımlar. Yatay etiketler için satır yüksekliği pozitif, dikey etiketler için negatif olur.

    - **Sayfa başına satır:** *5*

        Bu alan, her bir etikete yazdırılabilen satır sayısını tanımlar.

        > [!NOTE]
        > Bu ayar her iş için her bir sayfada en fazla beş iş satırı bulunan birkaç ZPL etiketi yazdırır. Örneğin, 12 satırı bulunan bir konteyner için etiket yazdırılıyorsa, üç etiket yazdırılacaktır. Her bir çekme satırı için ayrı bir etiket yazdırmak istiyorsanız, bu değeri *1* olarak ayarlayın.

1. Sayfayı kapatın.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Tablo:** *İş satırları*
    - **Türetilen tablo:** *İş satırları*
    - **Alan:** *İş türü*
    - **Ölçüt:** *Malzeme çekme*

1. Konşimento kodunu yazdırabilmek istiyorsanız, **Birleşimler** sekmesinde **İş satırları** tablosunu seçin ve **Sevkiyatlar** tablosunu bu tabloya birleştirin.
1. Sorgu düzenleyicisi iletişim kutusunu kapatın.
1. **Yazıcı metin düzeni** hızlı sekmesinde, yazıcı kodunu yazabileceğiniz üç bölüm vardır: **Üstbilgi bölümü**, **Gövde bölümü** ve **Altbilgi bölümü**. **Üstbilgi bölümü** bölümünde, **Etiket başlığı** alanına gereken başlığa ait kodu girin. Örneğin, Zebra yazıcılar kullanıyorsanız, aşağıdaki kodu kullanabilirsiniz.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. **Gövde bölümü** bölümünde, **Etiket gövdesi** alanına gövde için gereken ZPL kodunu girin. Aşağıda bir örnek verilmiştir.

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. **Gövde bölümü** bölümünde, **Etiket alt bilgisi** alanına alt bilgi için gereken ZPL kodunu girin. Aşağıda bir örnek verilmiştir.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Bu kurulum her etiketin bir kopyasını yazdırır. Daha fazla kopyaya gereksinim duyarsanız (örneğin, paletin her iki tarafı için bir kopya), alt bilgideki **\^PQn** bölümü için **n** değerini gerekli kopya sayısı olarak ayarlayın. Örneğin, her etiketin dört kopyasını yazdırmak için **\^PQ4** girin.

Etiketiniz şimdi kullanıma hazır.

### <a name="create-a-wave-label-template"></a>Dalga etiketi şablonu oluşturma

1. **Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi şablonları** öğesine gidin.
1. Dalga düzeyi şablonu ekleyin ve üst bilgide aşağıdaki değerleri ayarlayın:

    - **Etiket şablonu adı:** *Konteyner etiketleri*
    - **Açıklama:** *Konteyner etiketleri*
    - **Dalga adımı kodu:** *PrintLabel*
    - **Ambar:** *63*

1. **Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Etiket düzeni kodu:** *Konteyner*
    - **Yazıcı adı:** Uygun bir ZPL yazıcı seçin.
    - **Sorguyu çalıştır:** *Evet* (Bu ayar isteğe bağlıdır, ancak en iyi performans için önerilir.)

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. İsteğe bağlı: Müşteriye özel etiket tasarımını ayarlıyorsanız, müşterinin hesabını bulmak için bir sorgu oluşturmanız gerekir. **Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, **Sorguyu düzenle**'yi seçin. Ardından, sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Tablo:** *Sevkiyatlar*
    - **Türetilmiş tablo:** *Sevkiyatlar*
    - **Alan:** *Hesap numarası*
    - **Ölçüt:** İlgili müşteri hesap numarasını girin.

    Bitirdiğinizde sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.

### <a name="configure-number-sequence-extensions"></a>Numara serisi uzantıları yapılandırma

Numara serisi uzantıları, belirli numara serilerinin GS1 uyumluluğunu denetler. Bu yapılandırma, geçerli senaryo için isteğe bağlıdır. Daha fazla bilgi ve yapılandırma yönergeleri için bkz. [Numara serisi uzantılarını yapılandırma](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Satış siparişi oluşturma ve ambara serbest bırakma

1. **Satış ve pazarlama \> Satış siparişi \> Tüm satış siparişleri**'ne gidin.
1. Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Ambar:** *63*

1. Beş satış siparişi satırı ekleyin:

    - Satış sipariş satırı 1:

        - **Madde numarası:** *A0001*
        - **Miktar:** *10*

    - Satış sipariş satırı 2:

        - **Madde numarası:** *A0002*
        - **Miktar:** *20*

    - Satış sipariş satırı 3:

        - **Madde numarası:** *L0006*
        - **Miktar:** *20*

    - Satış sipariş satırı 4:

        - **Madde numarası:** *L0100*
        - **Miktar:** *40*

    - Satış sipariş satırı 5:

        - **Madde numarası:** *L0101*
        - **Miktar:** *50*

    > [!NOTE]
    > Burada sunulan maddeler ve miktarlar yalnızca örnektir. Bunlar belirtilen ambarda stokta bulunmalıdır.

1. Satış siparişi satırı 1'i seçin. Ardından, **Satış siparişi satırı** bölümünde **Stok** menüsünde **Rezervasyonlar**'ı seçin.
1. **Rezervasyon** sayfasında, Eylem Bölmesi'nde **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.
1. Eklenen her satış siparişi satırı için 4 ve 5 numaralı adımları yineleyin.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

    Aşağıdaki olaylar gerçekleşir:

    - Sistem, oluşturulan sevkiyatı etiket yazdırma adımını içeren şablonu kullanarak işler. Etiket düzeni, etiketin biçimini tanımlamak için kullanılır ve sonuç etiket şablonunda seçilen yazıcıda yazdırılan ve beş satırı bulunan bir etiket olacaktır.
    - Sevk irsaliyeleri için yeni bir konşimento kodu oluşturulur. Numara serisi uzantılarını yapılandırdıysanız, dalga etiketi kodları **SSCC-18** numara biçimini izler. 

**Ambar Yönetimi \> Sorgular ve raporlar \> Dalga etiketi geçmişi**'ne giderek bu dalga etiketlerini yeniden yazdırabilirsiniz.

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a>Senaryo 3: Çok katmanlı etiketler için dalga etiketi yazdırma

Bu senaryo, ambar işlemleri birkaç sevkiyat etiketi katmanı gerektirdiğinde dalga etiketi yazdırma işlevinin nasıl kullanılacağını gösterir. Örneğin, koliler ve paletler için ayrı etiketler yazdırılması gerekebilir ve tüm sevkiyat için bir kesme etiketi yazdırılması gerekli olabilir. Kesme etiketleri, sevkiyat kodu ve barkod için olan etiketler gibi, rulolar ve konteynerler arasında bir ayırıcı gibi kullanılabilen ayrı bir etiket türüdür; böylece etiketler yazdırıldıktan sonra kolaylıkla tasnif edilebilir.

Bu senaryonun yapılandırması ile senaryo 1'in yapılandırılması arasındaki temel fark, kesme etiketlerinin etkinleştirilmesi dışında, çok sayıda dalga etiketi türünün dalga etiketi şablonları ve birim sırası grup satırlarıyla ilişkilendirilmesinin gerekli olmasıdır. Bu yapılandırmayı tamamlamak için, bu senaryo için aşağıdaki öğeleri ayarlayın:

- **Dalga işleme yöntemleri:** Dalga etiketi yöntemini "yinelenebilir" olarak işaretler, dalga şablonuna iki (veya daha fazla) defa ekler ve farklı dalga adımı kodları ayarlarsınız.
- **Dalga etiketi şablonları:** Dalga etiketi şablonlarını yapılandırır ve onları dalga şablonuna bağlarsınız. Her dalga etiketi şablonunun kendi dalga etiketi türü vardır.
- **Dalga etiketi düzenleri:** Birden çok dalga etiketi düzeni oluşturursunuz. Etiketlerin her "katmanı" için ayrı bir etiket düzeni olur ve aynı zamanda bir kesme etiketi düzeni bulunur.

Bu senaryo uçtan uca akışı gösterir.

### <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu senaryoyu izlemek için, demo verilerinin yüklenmiş olması ve **USMF** tüzel kişiliğini kullanmanız gerekir.

### <a name="set-up-a-wave-process-method"></a>Dalga işlemi yöntemi ayarlama

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga işleme yöntemleri**'ne gidin.
1. **waveLabelPrinting** öğesinin listede olduğunu onaylayın. Seçili değilse, eklemek Için eylem bölmesindeki **Yöntemleri yeniden üret**'i seçin.
1. **waveLabelPrinting** yöntemi için **Yöntemi yinelenebilir yap** onay kutusunu seçin.

### <a name="set-up-a-wave-template"></a>Dalga şablonu ayarlama

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.
2. **62 Sevkiyat Varsayılanı** gibi bir şablon seçin.
3. **Yöntemler** hızlı sekmesinde, **Dalga etiketi yazdırma** yöntemini **Seçili yöntemler** sütununa taşıyın.
4. **Seçili yöntemler** sütununda, **Dalga etiketi yazdırma** yöntemine *Koli* gibi bir **Dalga adımı kodu** değeri atayın. Dalga adım kodları hakkında daha fazla bilgi için bkz. [Dalga adımı kodları](wave-step-codes.md).
5. **Dalga etiketi yazdırma** yöntemini ikinci kez **Seçili yöntemler** sütununa taşıyın.
6. **Seçili yöntemler** sütununda, ikinci **Dalga etiketi yazdırma** yöntemine *Palet* gibi farklı bir **Dalga adımı kodu** değeri atayın. Dalga adım kodları hakkında daha fazla bilgi için bkz. [Dalga adımı kodları](wave-step-codes.md).

### <a name="create-three-wave-label-layouts"></a>Üç dalga etiketi düzeni oluşturma

1. **Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi düzenleri** öğesine gidin.
1. Aşağıdaki ayarlara sahip bir kayıt oluşturun:

    - **Etiket düzeni kodu:** *Koli*
    - **Açıklama:** *Koli (SSCC)*

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem bölmesinde, **Dalga etiketi satır ayarları**'nı seçin.

    **Dalga etiketi satır ayarları** sayfası görüntülenir. Burada, etiketin dinamik parçasını yapılandırabilirsiniz.

1. Aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Satır kodu:** *WaveLabel*
    - **Satır tablosu adı:** *WHSWaveLabel*
    - **Satır başlangıç konumu:** *0*

        Bu alan, satırın etikette başlayacağı dikey konumu tanımlar.

    - **Satır yüksekliği:** *0*

        Bu alan, ZPL standardına göre her satırın yüksekliğini (punto olarak) tanımlar. Yatay etiketler için satır yüksekliği pozitif, dikey etiketler için negatif olur. Bu örnekte tek bir satır olduğu için, değeri *0* (sıfır) olarak ayarlayabilirsiniz.

    - **Sayfa başına satır:** *1*

        Bu alan, her bir etikete yazdırılabilen satır sayısını tanımlar.

        > [!NOTE]
        > Bu kurulum, dalga etiketleri tablosundaki her kayıt için ayrı bir ZPL etiketinin yazdırılmasına neden olur.

1. Sayfayı kapatın.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Tablo:** *İş satırları*
    - **Türetilen tablo:** *İş satırları*
    - **Alan:** *İş türü*
    - **Ölçüt:** *Malzeme çekme*

    Bu sorgu yalnızca çekme türü iş satırlarının etiket üzerine yazdırılmasını (yerine koyma türü iş satırları değil) sağlar.

1. Konşimento kodunu yazdırabilmek istiyorsanız, **Birleşimler** sekmesinde **İş satırları** tablosunu seçin ve **Sevkiyatlar** tablosunu bu tabloya birleştirin. 
1. Sorgu düzenleyicisi iletişim kutusunu kapatın.
1. **Yazıcı metin düzeni** hızlı sekmesinde, yazıcı kodunu yazabileceğiniz üç bölüm vardır: **Üstbilgi bölümü**, **Gövde bölümü** ve **Altbilgi bölümü**. **Üstbilgi bölümü** bölümünde, **Etiket başlığı** alanına gereken başlığa ait kodu girin. Örneğin, Zebra yazıcılar kullanıyorsanız, aşağıdaki kodu kullanabilirsiniz.


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. **Gövde bölümü** bölümünde, **Etiket gövdesi** alanına gövde için gereken ZPL kodunu girin. Aşağıda bir örnek verilmiştir.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. **Gövde bölümü** bölümünde, **Etiket alt bilgisi** alanına alt bilgi için gereken ZPL kodunu girin. Aşağıda bir örnek verilmiştir.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Bu kurulum her etiketin bir kopyasını yazdırır. Daha fazla kopyaya gereksinim duyarsanız (örneğin, paletin her iki tarafı için bir kopya), alt bilgideki **\^PQn** bölümü için **n** değerini gerekli kopya sayısı olarak ayarlayın. Örneğin, her etiketin dört kopyasını yazdırmak için **\^PQ4** girin.

1. İlk etiketiniz şimdi kullanıma hazır.
1. Aşağıdaki ayarlara sahip ikinci bir düzen kaydı oluşturun:

    - **Etiket düzeni kodu:** *Palet*
    - **Açıklama:** *Palet*

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem bölmesinde, **Dalga etiketi satır ayarları**'nı seçin.

    **Dalga etiketi satır ayarları** sayfası görüntülenir. Burada, etiketin dinamik parçasını yapılandırabilirsiniz.

1. Aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Satır kodu:** *WaveLabel*
    - **Satır tablosu adı:** *WHSWaveLabel*
    - **Satır başlangıç konumu:** *0*

        Bu alan, satırın etikette başlayacağı dikey konumu tanımlar.

    - **Satır yüksekliği:** *0*

        Bu alan, ZPL standardına göre her satırın yüksekliğini (punto olarak) tanımlar. Yatay etiketler için satır yüksekliği pozitif, dikey etiketler için negatif olur. Bu örnekte tek bir satır olduğu için, değeri *0* (sıfır) olarak ayarlayabilirsiniz.

    - **Sayfa başına satır:** *1*

        Bu alan, her bir etikete yazdırılabilen satır sayısını tanımlar.

        > [!NOTE]
        > Bu kurulum, dalga etiketleri tablosundaki her kayıt için ayrı bir ZPL etiketinin yazdırılmasına neden olur.

1. Sayfayı kapatın.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Tablo:** *İş satırları*
    - **Türetilen tablo:** *İş satırları*
    - **Alan:** *İş türü*
    - **Ölçüt:** *Malzeme çekme*

    Bu sorgu yalnızca çekme türü iş satırlarının etiket üzerine yazdırılmasını (yerine koyma türü iş satırları değil) sağlar.

1. Konşimento kodunu yazdırabilmek istiyorsanız, **Birleşimler** sekmesinde **İş satırları** tablosunu seçin ve **Sevkiyatlar** tablosunu bu tabloya birleştirin.
1. Sorgu düzenleyicisi iletişim kutusunu kapatın.
1. **Yazıcı metin düzeni** hızlı sekmesinde, yazıcı kodunu yazabileceğiniz üç bölüm vardır: **Üstbilgi bölümü**, **Gövde bölümü** ve **Altbilgi bölümü**. **Üstbilgi bölümü** bölümünde, **Etiket başlığı** alanına gereken başlığa ait kodu girin. Örneğin, Zebra yazıcılar kullanıyorsanız, aşağıdaki kodu kullanabilirsiniz.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. **Gövde bölümü** bölümünde, **Etiket gövdesi** alanına gövde için gereken ZPL kodunu girin. Aşağıda bir örnek verilmiştir.

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. **Gövde bölümü** bölümünde, **Etiket alt bilgisi** alanına alt bilgi için gereken ZPL kodunu girin. Aşağıda bir örnek verilmiştir.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Bu kurulum her etiketin bir kopyasını yazdırır. Daha fazla kopyaya gereksinim duyarsanız (örneğin, paletin her iki tarafı için bir kopya), alt bilgideki **\^PQn** bölümü için **n** değerini gerekli kopya sayısı olarak ayarlayın. Örneğin, her etiketin dört kopyasını yazdırmak için **\^PQ4** girin.

1. İkinci etiketiniz şimdi kullanıma hazır.
1. Aşağıdaki ayarlara sahip üçüncü bir düzen kaydı oluşturun:

    - **Etiket düzeni kodu:** *Kesme*
    - **Açıklama:** *Kesme etiketi*

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Yazıcı metin düzeni** hızlı sekmesinde, yazıcı kodunu yazabileceğiniz üç bölüm vardır: **Üstbilgi bölümü**, **Gövde bölümü** ve **Altbilgi bölümü**. **Üstbilgi bölümü** bölümünde, **Etiket başlığı** alanına gereken başlığa ait ZPL kodunu girin. Aşağıda bir örnek verilmiştir.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. Bu kez, gövde gerekli değildir. Bu nedenle, gerekli metni **Alt bilgi bölümü** bölümüne girmeniz yeterlidir. Aşağıda bir örnek verilmiştir.

    ```plaintext
    ^XZ
    ```

    Üçüncü etiketiniz şimdi kullanıma hazır.

    > [!NOTE]
    > Bu üçüncü etiket, etiket ruloları arasında ayırıcı olarak kullanılacak bir kesme etiketidir.

### <a name="create-two-wave-label-types"></a>İki dalga etiketi türü oluşturma

1. **Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi türleri** öğesine gidin.
1. Aşağıdaki ayarlara sahip bir kayıt oluşturun:

    - **Etiket türü:** *Koli*
    - **Açıklama:** *Koli*

1. Aşağıdaki ayarlara sahip ikinci bir kayıt oluşturun:

    - **Etiket türü:** *Palet*
    - **Açıklama:** *Palet*

### <a name="set-up-unit-sequence-groups"></a>Birim sıra gruplarını ayarla

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri\> Birim sırası grubu**'na gidin.
1. **Ea Kutu PL** grubu seçin veya oluşturun.
1. **Kutu** satırı için **Dalga düzeyi türü** alanını *Koli* olarak ayarlayın.
1. **PL** satırı için **Dalga düzeyi türü** alanını *Palet* olarak ayarlayın.

### <a name="create-wave-label-templates"></a>Dalga etiketi şablonları oluşturma

1. **Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi şablonları** öğesine gidin.
1. Aşağıdaki ayarlara sahip bir etiket şablonu oluşturun:

    - **Etiket şablonu adı:** *Koli etiketleri*
    - **Açıklama:** *Koli etiketleri*
    - **Dalga adımı kodu:** *Koli*
    - **Ambar:** *62*

1. **Genel** hızlı sekmesinde **Dalga etiketi türü** alanında *Koli* gibi bir değer seçin.
1. **Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Etiket düzeni kodu:** *Koli*
    - **Yazıcı adı:** Uygun bir ZPL yazıcı seçin.
    - **Sorguyu çalıştır:** *Evet* (Bu ayar isteğe bağlıdır, ancak en iyi performans için önerilir.)

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. İsteğe bağlı: Müşteriye özel etiket tasarımını ayarlıyorsanız, müşterinin hesabını bulmak için bir sorgu oluşturmanız gerekir. **Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, **Sorguyu düzenle**'yi seçin. Ardından, sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Tablo:** *Sevkiyatlar*
    - **Türetilmiş tablo:** *Sevkiyatlar*
    - **Alan:** *Hesap numarası*
    - **Ölçüt:** İlgili müşteri hesap numarasını girin.

    Bitirdiğinizde sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.

1. Eylem Bölmesinde, tam etiket şablonu için sorgu düzenleyicisi iletişim kutusunu açmak için **Sorguyu düzenle**'yi seçin.
1. Sorgu düzenleyicisi iletişim kutusunda **Tasnif** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Tablo:** *İş satırları*
    - **Türetilen tablo:** *İş satırları*
    - **Alan:** *Referans yükleme satırı kodu (Kayıt kodu)*
    - **Arama yönü:** *Artan*

1. Aşağıdaki ayarlara sahip ikinci bir satır ekleyin:

    - **Tablo:** *İş satırları*
    - **Türetilen tablo:** *İş satırları*
    - **Alan:** *Sevkiyat kodu*
    - **Arama yönü:** *Artan*

1. Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Bir ileti kutusu, gruplandırma sıfırlama işlemini onaylamanızı ister. Devam etmek için **Eve**'i seçin.
1. Eylem bölmesinde, **Dalga etiketi şablon grubu**'nu seçin.
1. **Dalga etiketi şablon grubu** iletişim kutusunda, **Referans alan adı** alanının *Sevkiyat kodu* olarak ayarlandığı satır için aşağıdaki değerleri ayarlayın:

    - **Kesme etiketi yazdır:** Bu onay kutusunu seçin.
    - **Etiket düzeni kodu:** Bir kesme etiketi seçin. (Örneğin, bu senaryoda daha önce oluşturduğunuz *Kesme* etiketi düzenini seçin)
    - **Yazıcı adı:** Kesme etiketi için yazıcıyı seçin. (Tipik olarak, etiket rulolarını ayırmak amacıyla, **Dalga etiketi şablon ayrıntıları** hızlı sekmesinde seçilenle aynı yazıcıyı seçmeniz gerekir. Ancak, başka senaryolar da olabilir.)

1. **Referans alan adı** alanının *Referans yük satırı kodu* olarak ayarlandığı satır için , **Etiket derleme kodu** onay kutusunu seçin.

    > [!NOTE]
    > Bu kurulum, iş gruplandırma kurulumu ne olursa olsun, dalga boyunca her yükleme satırı için bir etiket sırası ("Koli 1/X") oluşturacaktır. Bu etiket sırası etiket düzeninde yazdırılabilir. Ek olarak, farklı sevkiyatların etiketleri seçili kesme etiketiyle ayrılacaktır.

1. **Dlga etiketi şablon grubu** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Aşağıdaki ayarlara sahip ikinci bir etiket şablonu oluşturun:

    - **Etiket şablonu adı:** *Palet etiketleri*
    - **Açıklama:** *Palet etiketleri*
    - **Dalga adımı kodu:** *Palet*
    - **Ambar:** *62*

1. **Genel** hızlı sekmesinde **Dalga etiketi türü** alanında *Palet* gibi bir değer seçin.
1. **Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Etiket düzeni kodu:** *Palet*
    - **Yazıcı adı:** Uygun bir ZPL yazıcı seçin.
    - **Sorguyu çalıştır:** *Evet* (Bu ayar isteğe bağlıdır, ancak en iyi performans için önerilir.)

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. İsteğe bağlı: Müşteriye özel etiket tasarımını ayarlıyorsanız, müşterinin hesabını bulmak için bir sorgu oluşturmanız gerekir. **Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, **Sorguyu düzenle**'yi seçin. Ardından, sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Tablo:** *Sevkiyatlar*
    - **Türetilmiş tablo:** *Sevkiyatlar*
    - **Alan:** *Hesap numarası*
    - **Ölçüt:** İlgili müşteri hesap numarasını girin.

    Bitirdiğinizde sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin. 

1. Eylem Bölmesinde, tam etiket şablonu için sorgu düzenleyicisi iletişim kutusunu açmak için **Sorguyu düzenle**'yi seçin.
1. Sorgu düzenleyicisi iletişim kutusunda **Tasnif** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Tablo:** *İş satırları*
    - **Türetilen tablo:** *İş satırları*
    - **Alan:** *Referans yükleme satırı kodu (Kayıt kodu)*
    - **Arama yönü:** *Artan*

1. Aşağıdaki ayarlara sahip ikinci bir satır ekleyin:

    - **Tablo:** *İş satırları*
    - **Türetilen tablo:** *İş satırları*
    - **Alan:** *Sevkiyat kodu*
    - **Arama yönü:** *Artan*

1. Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Bir ileti kutusu, gruplandırma sıfırlama işlemini onaylamanızı ister. Devam etmek için **Eve**'i seçin.
1. Eylem bölmesinde, **Dalga etiketi şablon grubu**'nu seçin.
1. **Dalga etiketi şablon grubu** iletişim kutusunda, **Referans alan adı** alanının *Sevkiyat kodu* olarak ayarlandığı satır için aşağıdaki değerleri ayarlayın:

    - **Kesme etiketi yazdır:** Bu onay kutusunu seçin.
    - **Etiket düzeni kodu:** Bir kesme etiketi seçin. (Örneğin, bu senaryoda daha önce oluşturduğunuz *Kesme* etiketi düzenini seçin)
    - **Yazıcı adı:** Kesme etiketi için yazıcıyı seçin. (Tipik olarak, etiket rulolarını ayırmak amacıyla, **Dalga etiketi şablon ayrıntıları** hızlı sekmesinde seçilenle aynı yazıcıyı seçmeniz gerekir. Ancak, başka senaryolar da olabilir.)

1. **Referans alan adı** alanının *Referans yük satırı kodu* olarak ayarlandığı satır için , **Etiket derleme kodu** onay kutusunu seçin.

    > [!NOTE]
    > Bu kurulum, iş gruplandırma kurulumu ne olursa olsun, dalga boyunca her yükleme satırı için bir etiket sırası ("Koli 1/X") oluşturacaktır. Bu etiket sırası etiket düzeninde yazdırılabilir. Ek olarak, farklı sevkiyatların etiketleri seçili kesme etiketiyle ayrılacaktır.

### <a name="configure-number-sequence-extensions"></a>Numara serisi uzantıları yapılandırma

Numara serisi uzantıları, belirli numara serilerinin GS1 uyumluluğunu denetler. Bu yapılandırma, geçerli senaryo için isteğe bağlıdır. Daha fazla bilgi ve yapılandırma yönergeleri için bkz. [Numara serisi uzantılarını yapılandırma](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Satış siparişi oluşturma ve ambara serbest bırakma

1. **Satış ve pazarlama \> Satış siparişi \> Tüm satış siparişleri**'ne gidin.
1. Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Ambar:** *62*

1. İki satış siparişi satırı ekleyin:

    - Satış sipariş satırı 1:

        - **Madde numarası:** *A0001*
        - **Miktar:** *9024*
        - **Birim:** *ea* (9024 ea = 376 Kutu = 47 PL)

    - Satış sipariş satırı 2:

        - **Madde numarası:** *A0002*
        - **Miktar:** *9016*
        - **Birim:** *ea* (9016 ea = 322 Kutu = 46 PL)

    > [!NOTE]
    > Burada sunulan maddeler ve miktarlar yalnızca örnektir. Bunlar için daha önce tanımladığınız birim sırası grubunu kullanmaları, bunlar için *ea*'dan *kutu*'ya *PL*'ye uygun birim dönüşümlerinin tanımlanması ambar *62*'de stokta bulunmaları gerekir. Daha fazla bilgi için, bkz. [Ölçü birimi ve stoklama ilkeleri](unit-measure-stocking-policies.md).

1. Satış siparişi satırı 1'i seçin. Ardından, **Satış siparişi satırı** bölümünde **Stok** menüsünde **Rezervasyonlar**'ı seçin.
1. **Rezervasyon** sayfasında, Eylem Bölmesi'nde **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.
1. Satış siparişi satırı 2 için 4 ve 5 numaralı adımları yineleyin.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

    Aşağıdaki olaylar gerçekleşir: 

    - Sistem, oluşturulan sevkiyatı etiket yazdırma adımını içeren şablonu kullanarak işler. Etiket düzeni, etiketin biçimini tanımlamak için kullanılır ve sonuç etiket şablonunda seçilen yazıcıda yazdırılan bir etiket olacaktır.
    - Dalga etiketleri oluşturulur ve yazdırılır. Etiket sayısı koli sayısına eşit olacaktır (bu örnekte, satır 1 için 376 Kutu etiketi, satır 2 için 322 Kutu etiketi, satır 1 için 47 PL etiketi, satır 2 için 47 PL etiketi ve sevkiyat koduna sahip iki kesme etiketi).
    - Sevk irsaliyeleri için yeni bir konşimento kodu oluşturulur. Numara serisi uzantılarını yapılandırdıysanız, dalga etiketi kodları **SSCC-18** numara biçimini izler. 

Dalga etiketlerini aşağıdaki sayfalardan görüntüleyebilir ve yeniden yazdırabilirsiniz:

- Tüm sevkiyatlar \> Sevkiyat ayrıntıları
- Tüm yükler \> Yük ayrıntıları
- Tüm dalgalar
- Dalga etiketleri
- Dalga etiketi geçmişi

Bu sayfaların çoğu için, Eylem bölmesindeki **Sevkiyatlar** sekmesinde yer alan **İlgili bilgi** grubunda **Dalga etiketleri**'ni seçerek ilgili işlevi bulabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

- [Dalga etiketlerini yeniden yazdırma ve hükümsüz kılma](reprint-and-void-wave-labels.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]