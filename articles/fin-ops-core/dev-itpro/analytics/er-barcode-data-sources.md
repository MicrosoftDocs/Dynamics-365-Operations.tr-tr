---
title: Barkod görüntüleri oluşturmak için Barkod veri kaynaklarını kullanma
description: Bu konu Barkod veri kaynaklarının barkod görüntülerini oluşturmak için nasıl kullanılacağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: c549a476f854ffcf962ffb62e430b459d3445734
ms.sourcegitcommit: cc78f9bf585082ce65c2ab0b011ff62620fa883d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088209"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a>Barkod görüntüleri oluşturmak için Barkod veri kaynaklarını kullanma

[!include[banner](../includes/banner.md)]

İhtiyacınız olan elektronik ve yazdırılabilir giden belgeleri oluşturmak için çalıştırabileceğiniz [ER biçimi bileşenlerini](general-electronic-reporting.md#FormatComponentOutbound) tasarlamak üzere [Elektronik raporlama (ER)](general-electronic-reporting.md) çerçevesini kullanabilirsiniz. Microsoft Office biçiminde bir giden belge oluşturmak için öncelikle rapor şablonu olarak Microsoft Excel belgesi veya Microsoft Word belgesi bir rapor şablonu olarak kullanarak raporun düzenini belirtmeniz gerekir. [ER İşlemleri tasarımcısı](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base), ER biçimi için bir Excel veya Word belgesi eklemenize olanak tanır. Ekli şablondaki aşağıdaki adlandırılmış öğeler, yapılandırılmış biçim bileşeninin öğeleriyle ilişkilendirilmiştir:

- Word'de içerik denetimleri
- Excel'de adlandırılmış sayfalar, aralıklar, hücreler, şekiller ve görüntüler

Bu adlandırılmış öğeler, bir ER biçimi çalıştırıldığında, oluşturulmuş bir belgeye girilen veriler için yer tutucu olarak kullanılır. ER biçimi öğeleri veri kaynaklarına bağlıdır. Bu veri kaynakları çalışma zamanında oluşturulan belgelere girilecek verileri belirtir. Daha fazla bilgi için [Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](electronic-reporting-embed-images-shapes.md)

ER şimdi **Barkod** veri kaynağı türünü destekler. Bu nedenle, artık belirtilen metin için barkodu temsil eden bir resim oluşturabilirsiniz. Bir ER biçimi yapılandırdığınızda, barkod görüntüleri oluşturmak için **Barkod** türünün veri kaynaklarını belirtebilirsiniz. Daha sonra bu görüntüleri oluşturulan iş belgelerine (örneğin siparişler, faturalar, sevk irsaliyeleri ve makbuzlar) ekleyebilirsiniz. Bunları, ürün ve raf etiketleri, paketleme ve sevkiyat etiketleri gibi çeşitli türdeki etiketlere de ekleyebilirsiniz.

Aşağıdaki yer tutucular rapor şablonlarında barkod görüntüleri girmek için kullanılabilir:

- Word için [Resim](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) içeriği denetimi
- Excel'de [Resim](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) nesnesi

**Barkod** türünde bir veri kaynağı kullanarak , aşağıdaki biçimlerde barkodlar oluşturabilirsiniz:

- Tek boyutlu barkodlar:

    - Codabar
    - Code 39
    - Code 93
    - Code 128
    - EAN-8
    - EAN-13
    - ITF-14
    - Akıllı Posta
    - MSI
    - Plessey
    - PDF417
    - UPC-A
    - UPC-E

- İki boyutlu barkodlar:

    - Aztec
    - Veri Matrisi
    - QR Kodu

**Barkod** veri kaynağı yapılandırdığınızda, görüntü oluşturmak için kullanılan belirli işleme parametrelerini tanımlayabilirsiniz:

- **Genişlik** : Barkod genişliğini piksel olarak belirtin. **0** (sıfır) değeri, varsayılan genişliğin kullanıldığını belirtir. Anlamı farklı biçimler için farklılık gösterebilir.
- **Yükseklik** : Barkod yüksekliğini piksel olarak belirtin. **0** (sıfır) değeri, varsayılan yüksekliğin kullanıldığını belirtir. Anlamı farklı biçimler için farklılık gösterebilir.
- **Kenar boşluğu** : Barkod kenar boşluğunun boyutunu piksel cinsinden belirtir. Kenar boşluğu, bir barkodun her iki tarafında, boş (sessiz bölge) olarak tutulması gereken alandır. **0** (sıfır) değeri, varsayılan kenar boşluğunun kullanıldığını belirtir. Anlamı farklı biçimler için farklılık gösterebilir.
- **Çıktı içeriği** : Kodlanmış bilgilerin metin olarak bulunduğu bir bar kod görüntüsü oluşturmak için, değeri **Evet** olarak ayarlayın. Varsayılan değer **Hayır** değeridir.
- **Kodlama** : Oluşturulan barkod görüntüsünde kodlanan karakter türünü belirtir. Varsayılan olarak, **UTF-8** kodlaması kullanılır.

> [!IMPORTANT]
> Yeni bir **Barkod** veri kaynağı eklediğinizde, bunu bir iç içe öğe olarak başka bir öğenin (kapsayıcı) altına yerleştirmeniz gerekir.
>
> Bir **Barkod** veri kaynağını bir biçimdeki bir hücre öğesine bağladığınızda ve hücre öğesi bir Word içerik denetimini veya Excel resmini temsil ettiğinde, veri kaynağı bu bağlamada **Dize** türünde tek bir parametresi olan bir işlev olarak sunulur. Bir barkod görüntüsüne dönüştürülmesi gereken metni belirtmek ve oluşturulan bir bar kod tarandığında bunu okumak için bu parametreyi kullanmalısınız.

Bu özellik hakkında daha fazla bilgi için bu konudaki örnekleri tamamlayın.

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a>Örnek: Ödenecek tutarı kodlayan bir barkod içeren bir ödeme denetimi oluşturma

Bu örnek, **Sistem Yöneticisi** veya **Elektronik raporlama işlev danışmanı**  rolündeki bir kullanıcının, bir barkod içeren Excel biçiminde giden belge oluşturmak için kullanılan bir şablon ER biçiminin nasıl yapılandırabileceğini gösterir. İlgili adımların özeti aşağıdadır.

1. [Önkoşulları tamamlayın](#ExamplePrerequisites).
2. [Yapılandırma sağlayıcısı etkinleştirin](#ExampleProvider).
3. [Sağlanan ER çözümünü içe aktarın](#ExampleImportSolution).
4. [Ödeme çeki oluşturun](#ExampleGenerateCheque).
5. [Oluşturulan ödeme çekini gözden geçirin](#ExampleReviewGeneratedCheque).
6. [Sağlanan ER çözümünün biçimini değiştirin](#ExampleModifyFormat).

    1. [Yeni çek şablonu uygulayın](#ExampleModifyFormatApplyTemplate).
    2. [Yeni bir Barkod veri kaynağı ekleyin](#ExampleModifyFormatAddDataSource).
    3. [Yeni bir biçim öğesi bağlayın](#ExampleModifyFormatBindFormatElement).
    4. [Değiştirilmiş sürümü test çalıştırmaları için kullanılabilir yapın](#ExampleModifyFormatMakeVersionAvailable).

        1. [Değiştirilmiş biçim sürümünü tamamlayın](#CompleteToRun).
        2. [Taslak sürümü kullanılabilir hale getirin](#MarkToRun).

7. [Ödeme çeki oluşturun](#ExampleGenerateCheque2).
8. [Oluşturulan çeki PDF'ye dönüştürün](#ExampleConvertToPDF).

Bu örnekte, ödeme çekleri oluşturmak için yapılandırılmış sağlanan ER çözümünü kullanacaksınız. Bu çözüm, ödeme tutarının hem sayı hem de metin olarak yazıldığı bir ödeme çeki oluşturur. Bu ER çözümünü çek, ödenecek tutarının kodlandığı ve bir barkod tarayıcısı kullanılarak okunabileceği şekilde oluşturulmuş bir barkod içerecek şekilde değiştireceksiniz.

Bu adımlar Microsoft Dynamics 365 Finance'taki **USMF** şirketinde gerçekleştirilir.

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a>Önkoşulları tamamlayın

Bu örneği tamamlamak üzere aşağıdaki rollerden biri için Finance'teki USMF şirketine erişiminiz olmalıdır:

- Elektronik raporlama işlev danışmanı
- Sistem yöneticisi

[ER kullanarak oluşturduğunuz belgelere görüntüler ve şekiller ekleme](electronic-reporting-embed-images-shapes.md) konusundaki örneği henüz tamamlamadıysanız, örnek ER çözümünün aşağıdaki yapılandırmalarını indirin.

| İçerik açıklaması         | Dosya adı                   |
|-----------------------------|-----------------------------|
| ER data model configuration | Model for cheques.xml       |
| ER format configuration     | Cheques printing format.xml |

Ek olarak, sağlanan ER çözümü için değiştirilmiş şablonu içeren aşağıdaki Excel dosyasını indirin.

| İçerik açıklaması | Dosya adı                 |
|---------------------|---------------------------|
| Rapor şablonu     | Check template Excel.xlsx |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a>Bir yapılandırma sağlayıcısını etkinleştirme

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** 'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasındaki **Yapılandırma sağlayıcıları** bölümünde, **Litware, Inc.** örnek şirketine ait [yapılandırma sağlayıcısının](general-electronic-reporting.md#Provider) listelendiğinden ve etkin olarak işaretlendiğinden emin olun. Listede yoksa veya etkin olarak işaretli değilse [Bir yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları izleyin.

![Yerelleştirme yapılandırmaları sayfasında örnek şirketi etkin olarak ayarlama](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a>Sağlanan ER çözümünü içe aktarma

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** 'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.
3. **Yapılandırmalar** sayfasında, yapılandırma ağacında **Çek modeli** yapılandırması yoksa, ER veri modeli yapılandırmasını içe aktarmak için aşağıdaki adımları izleyin:

    1. Eylem Bölmesinde, **Exchange** \> **XML dosyasından yükle** 'yi seçin.
    2. İletişim kutusunda, **Gözat** 'ı seçin, **Model for cheques.xml** dosyasını bulup seçin ve **Tamam** 'ı seçin.

4. Yapılandırma ağacında **Çek yazdırma biçimi** yapılandırması yoksa, ER biçimi yapılandırmasını içe aktarmak için aşağıdaki adımları izleyin:

    1. Eylem Bölmesinde, **Exchange** \> **XML dosyasından yükle** 'yi seçin.
    2. İletişim kutusunda, **Gözat** 'ı seçin, **Cheques printing format.xml** dosyasını bulup seçin ve **Tamam** 'ı seçin.

5. Yapılandırma ağacında, **Çek modeli** 'ni genişletin.
6. Yapılandırma ağacındaki içe aktarılan ER yapılandırmaları listesini inceleyin.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a>Ödeme çeki oluşturma

1. **Nakit ve banka yönetimi** \> **Banka hesapları** \> **Banka hesapları** öğesine gidin.
2. **Banka hesapları** sayfasında, **USMF OPER** hesabını seçin.
3. Banka hesabı ayrıntıları sayfasındaki Eylem Bölmesinde, **Kurulum** sekmesinin **Düzen** grubunda **Çek** 'i seçin.
4. **Çek düzeni** sayfasında **Düzenle** 'yi seçin.
5. **Genel** hızlı sekmesinde **Genel elektronik Dışa aktarma biçimi** seçeneğini **Evet** olarak ayarlayın.
6. **Dışa aktarma biçimi yapılandırması** alanında, daha önce içe aktardığınız **Çek yazdırma biçimi** ER biçimini seçin.
7. Eylem Bölmesinde, **Yazdırma testi** 'ni seçin.
8. İletişim kutusunda, **Ciro edilebilir çek biçimi** seçeneğini **Evet** olarak ayarlayıp **Tamam** 'ı seçin.

    ![Çek düzeni - yazdırma testi iletişim kutusu](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a>Oluşturulan ödeme çekini gözden geçirme

- Oluşturulan çeki Excel'de açın.
2. Oluşturulan çeki gözden geçirin.

    ![Excel'de oluşturulan ödeme çeki](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a>Sağlanan ER çözümünün biçimini değiştirme

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a>Yeni çek şablonu uygulama

Daha önce içe aktardığınız **Cheque template Excel.xlsx** dosyasını açmak için Excel masaüstü uygulamasını kullanabilirsiniz. Bu şablonun, sağlanan ER çözümünde bir ödeme denetimi oluşturmak için kullandığınız şablondan farklı olduğuna dikkat edin. Ayrıca, Bar kod görüntüsü için bir **AmountBarcode** öğesi içerir.

![Excel şablonunda AmountBarcode öğesi](./media/er-barcode-data-source-cheque2.png)

Şimdi ER çözümünü değiştirmeniz ve değiştirilen şablonu [yeniden uygulamanız](modify-electronic-reporting-format-reapply-excel-template.md) gerekir.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** 'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** 'nı seçin.
3. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Çek modeli** 'ni genişletin ve **Çek yazdırma biçimi** 'ni seçin.
4. Eylem Bölmesinde, **Tasarımcı** 'yı seçin.
5. ER İşlemleri tasarımcısında, sayfanın sağ tarafındaki **Eşleme** sekmesini seçin ve sonra soldaki biçim ağacı bölmesinde **Genişlet/Daralt** 'ı seçin.
6. Tüm hücre biçimi öğelerinin uygun veri kaynaklarına bağlı olduğuna dikkat edin.

    ![ER İşlemleri tasarımcısında hücre biçimi öğelerinin veri kaynaklarına bağlanması](./media/er-barcode-data-source-cells-bound.png)

7. Sayfanın sağ tarafındaki **Biçim** sekmesini seçin.
8. Eylem Bölmesinde üç noktayı ( **...** ) seçin ve ardından **İçe aktar** 'ı seçin.
9. **İçe aktarma** grubunda, **Excel'den güncelleştir** 'i seçin ve **Şablonu güncelleştir** 'i seçin.
10. İletişim kutusunda, bilgisayarınıza kaydedilen **Cheque template Excel.xlsx** dosyasına gözatın, dosyayı seçin ve seçilen şablonun uygulanmasını onaylamak için **Tamam** 'ı seçin.
11. Sayfanın sağ tarafındaki **Eşleme** sekmesini seçin ve sonra soldaki biçim ağacı bölmesinde **Genişlet/Daralt** 'ı seçin.
12. **AmountBarcode** hücre öğesinin biçime eklendiğini unutmayın. Bu öğe, Excel şablonuna barkod görüntüsü için yer tutucu olarak eklenmiş olan **AmountBarcode** öğesiyle ilişkilendirilir.

    ![ER İşlemleri tasarımcısındaki biçime eklenen AmountBarcode hücre öğesi](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a>Yeni bir Barkod veri kaynağı ekleme

Sonra, **Barkod** türünün yeni bir veri kaynağını eklemeniz gerekir.

1. ER İşlemleri tasarımcısında, sayfanın sağ tarafındaki **Eşleme** sekmesinde, **yazdırma** veri kaynağını seçin.
2. **Ekle** 'yi seçin ve sonra **İşlevler** grubunda **Barkod** veri kaynağı türünü seçin.

    ![Barkod veri kaynağı türünü seçme](./media/er-barcode-data-source-add.png)

3. İletişim kutusunda, **Ad** alanına **barkod** girin.
4. **Barkod biçimi** 'nde, **Code 128** 'i seçin.
5. **Genişlik** alanına **500** yazın.
6. **Tamam** 'ı seçin.

    ![Veri kaynağı özellikleri iletişim kutusu](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a>Yeni bir biçim öğesi bağlama

Sonra, yeni biçim öğesini eklediğiniz veri kaynağına bağlamanız gerekir.

1. ER İşlemleri tasarımcısında, sayfanın sağ tarafındaki **Eşleme** sekmesinde, **print\\barcode** veri kaynağını seçin.
2. Soldaki biçim ağacı bölmesinde, **AmountBarcode** hücre öğesini seçin ve sonra **Bağla** 'yı seçin.
3. Eylem Bölmesinde, **Ayrıntıları göster** 'i seçin.
4. **Barkod** veri kaynağı bağlamada tek bir parametre içeren bir işlev olarak temsil edildiğinden, bağlı biçim öğesi adının otomatik olarak bu parametrenin bağımsız değişkeni olarak alındığını unutmayın.

    ![ER İşlemleri tasarımcısındaki Barkod veri kaynağının ayrıntıları](./media/er-barcode-data-source-bind1.png)

5. Bağlamayı ayarlamak için **Biçimi düzenle** 'yi seçin.

    Hücre öğesinin adının geri döndürülmesini istemezsiniz. Bu nedenle, geçerli çekin ödenecek tutarını içeren metni döndüren bir ifade yapılandırmanız gerekir. Üst **ChequeLines** **model.cheques** veri kaynağına bağlı olduğundan, geçerli çekin ödenecek tutarı **Gerçek** veri türünün **model.cheques.attributes.amount** alanında bulunur.

6. **Formül** alanına, **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))** yazın.
7. **Kaydet** 'i seçin ve [ER Formül tasarımcısını](general-electronic-reporting-formula-designer.md) kapatın.
8. Bağlamanın ayarlanmış olduğuna dikkat edin.

    ![ER İşlemleri tasarımcısında ayarlanan bağlama](./media/er-barcode-data-source-bind2.png)

9. **Kaydet** 'i seçin ve ardından ER İşlemleri tasarımcısını kapatın.

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a>Değiştirilmiş sürümü test çalıştırmaları için kullanılabilir yapma

Varsayılan olarak, yalnızca **Tamamlandı** ve **Paylaşıldı** durumuna sahip sürümler ER biçimi çalışıtırılırken kullanılır.

Değişikliklerinizi bitirdiyseniz, işinizi geçerli taslak sürümüyle tamamlayabilir ve değişikliklerinizi kullanıma açık hale getirebilirsiniz. Yönergeler için takip eden [Değiştirilen biçim sürümünü tamamlama](#CompleteToRun) bölümüne bakın.

Geçerli taslak sürümüyle çalışmaya devam etmek istiyorsanız, ancak bu sürümü çek oluşturmak için kullanmanız gerekiyorsa, yürütme için biçimin taslak sürümünü kullanmak istediğinizi açıkça belirtmeniz gerekir. Yönergeler için [Taslak sürümünü kullanılabilir hale getirme](#MarkToRun) bölümünü inceleyin.

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a>Değiştirilmiş biçim sürümünü tamamlama

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** 'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** 'nı seçin.
3. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Çek modeli** 'ni genişletin ve **Çek yazdırma biçimi** 'ni seçin.
4. **Sürümler** hızlı sekmesinde durumu **Taslak** olan kaydı seçin.
5. **Durumu değiştir** 'i ve ardından **Tamam** 'ı seçin.
6. İletişim kutusunda **Tamam** 'ı seçin.

Geçerli sürümün durumu **Taslak** yerine **Tamamlandı** olarak değiştirilir ve **Taslak** durumundaki yeni bir sürüm oluşturulur. Ek değişiklikler uygulamak için bu yeni taslak sürümünü kullanabilirsiniz.

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a>Taslak sürümü kullanılabilir hale getirme

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** 'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** 'nı seçin.
3. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri** 'ni seçin.
4. İletişim kutusunda, **Çalıştırma ayarı** seçeneğini **Evet** olarak ayarlayıp **Tamam** 'ı seçin.
5. Yapılandırma ağacında, **Çek modeli** 'ni genişletin ve **Çek yazdırma biçimi** 'ni seçin.
6. **Taslak çalıştır** seçeneğini **Evet** olarak ayarlayın.
7. **Kaydet** 'i seçin.

Seçilen biçimin taslak sürümü, seçilen biçim çalıştırıldığında kullanılmak üzere kullanılabilir olarak işaretlenir.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a>Ödeme çeki oluşturma

1. **Nakit ve banka yönetimi** \> **Banka hesapları** \> **Banka hesapları** öğesine gidin.
2. **Banka hesapları** sayfasında, **USMF OPER** hesabını seçin.
3. Banka hesabı ayrıntıları sayfasındaki Eylem Bölmesinde, **Kurulum** sekmesinin **Düzen** grubunda **Çek** 'i seçin.
4. **Çek düzeni** sayfasında, Eylem Bölmesinde, **Yazdırma testi** 'ni seçin.
5. İletişim kutusunda, **Ciro edilebilir çek biçimi** seçeneğini **Evet** olarak ayarlayın.
6. **Tamam** 'ı seçin.
7. Oluşturulan çeki gözden geçirin. Çekin ödenecek tutarını kodlamak için bir barkod oluşturulduğuna dikkat edin.

    ![Excel'de barkod ile oluşturulan ödeme çeki](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> **Barkod** veri kaynağının bağımsız değişkeni barkod biçimine özgü uygun gereksinimlere uymazsa, bir özel durum oluşur. Örneğin, **Barkod** veri kaynağı sağlanan metin için [EAN-8](https://wikipedia.org/wiki/EAN-8) barkodunu oluşturmak üzere çağrıldığında, metnin uzunluğu yedi karakteri aşarsa bir özel durum oluşur.

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a>Oluşturulan çeki PDF'ye dönüştürme

[Yazdırılabilir FTI formları oluşturma](er-generate-printable-fti-forms.md#finland) konusunda açıklandığı gibi, oluşturulan belgede barkodlar oluşturmak için özel bir yazı tipi kullanabilirsiniz. Bu durumda, oluşturulan belgedeki ek dönüştürme işlemleri bu yazı tipinin dönüştürme ortamındaki kullanılabilirliğine bağlı olabilir. Örneğin, bir belgeyi PDF formatına dönüştürmeye veya yazı tipinin bulunmadığı bir ortamda önizlemeye çalışırsanız, barkodlar doğru işlenmez.

Ancak **Barkod** veri kaynağını, barkodları oluşturmak için kullandığınızda, bu barkodların işlenmesi herhangi bir yazı tipine bağlı değildir. Bu nedenle, barkodların bulunduğu belgeleri PDF formatına kolayca dönüştürebilirsiniz. Aşağıdaki şekilde, yapılandırılan ER [hedefinin](electronic-reporting-destinations.md) ayarına bağlı olarak PDF'ye [dönüştürülmüş](electronic-reporting-destinations.md#OutputConversionToPDF) bir ödeme çekinin önizlemesi gösterilir.

![Ödeme çeki PDF dosyasının önizlemesi](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a>Sınırlamalar

> [!NOTE]
> Oluşturulan bazı barkod türleri, sabit bir en boy oranına sahiptir. Bu davranış, **Elektronik raporlama çerçevesinde EPPlus kitaplığı kullanımını etkinleştir** özelliğini ER'de Excel belgeleriyle çalışmak üzere etkinleştirdiyseniz yararlıdır. Bu durumda, kilitli en boy oranınayer tutucuya bir resim girilir. Bu nedenle, bir şablondaki yer tutucunun boyutları girilen bir görüntünün oranıyla ilişkili olduğunda, gerekli en boy oranını korumak için oluşturulan belgedeki gerçek bir resim yeniden boyutlandırılabilir. Resim yeniden boyutlandırmayı önlemek için, beklenen en boy oranına sahip bir yer tutucu kullanın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)
- [Elektronik Raporlama hedefleri](electronic-reporting-destinations.md)
- [Elektronik raporlamada formül dili](er-formula-language.md)
- [NUMBERFORMAT işlevi](er-functions-text-numberformat.md)
