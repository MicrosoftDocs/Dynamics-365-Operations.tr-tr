---
title: Üretim katı yürütme arabirimini düzenleme
description: Bu konu, form denetimlerinin varsayılan üretim kat yürütme stillerinin uygulanmasını sağlayacak şekilde konfigüre etme biçimini açıklar.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ef39dc6414f0afdadd4a4b5a41e1fb1fe60e4974
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790902"
---
# <a name="style-the-production-floor-execution-interface"></a>Üretim katı yürütme arabirimini düzenleme

[!include [banner](../includes/banner.md)]

Bu konu, form denetimlerinin varsayılan üretim kat yürütme stillerinin uygulanmasını sağlayacak şekilde konfigüre etme biçimini açıklar.

## <a name="forms-and-dialogs"></a>Formlar ve iletişim kutuları

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde bir forma veya bir iletişim kutusuna uygulanabilir:

- Form varolan rapor ilerlemesi formuna benzemesi gerekiyorsa, formunuzun veya iletişim kutusunun adı `JmgProductionFloorExecutionCustomInputDialog` ile başlamalıdır.
- Form veya diyalog bir ayrıntı formu parçası içerebilir. Stilleri uygulamak için, ayrıntı formunun adının `JmgProductionFloorExecutionCustomDetailsDialog` ile başlaması gerekir.
- Formda veya iletişim kutusunda basit bir görünüm olması gerekiyorsa, basit görünümün adı `JmgProductionFloorExecutionCustomDialog` ile başlamalıdır. Basit bir görünüme sahip formların örnekleri başlangıç formunu ve dolaylı faaliyet formunu içerir.
- İletişim kutusuna ait tüm denetimler bu konuda anlatıldığı şekilde konfigüre edilmelidir.

> [!IMPORTANT]
> Bu listenin ilk iki madde işareti noktasında sözü edilen özellikler, Supply Chain Management sürüm 10.0.19 veya üstünü gerektirir.

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde bir iletişim kutusundaki **Tamam** düğmesine uygulanabilir:

- Düğme, bir form grubunda yer alır.
- Grup adı, `OkButtonGroup` ile başlar.

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde bir iletişim kutusundaki **İptal** düğmesine uygulanabilir:

- Düğme, bir form grubunda yer alır.
- Grup adı, `CancelButtonGroup` ile başlar.

### <a name="header"></a>Başlık

Aşağıdaki resimde, tipik bir form veya iletişim kutusu gösterilmektedir.

![Tipik form veya iletişim üst bilgisi.](media/pfe-styles-header.png "Tipik form veya iletişim üst bilgisi")

Visual Studio'da, üst bilgiler aşağıdaki çizimde gösterilen gibi bir yapı kullanılarak oluşturulur.

![Başlık oluşturmak için kullanılan tipik kod yapısı.](media/pfe-styles-header-code-structure.png "Başlık oluşturmak için kullanılan tipik kod yapısı")

Üst bilginize metin eklemek için aşağıdaki örnekte olduğu gibi bir kod kullanın.

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

Üst bilgi kodunuzu yazdığınızda, aşağıdaki kuralları uygula:

- Ana grup adı `TableRowHeaderGroup` olmalıdır.
- Her metin bloğu (madde işaretleriyle ayrılmış olarak) `HeaderFieldWithSeparatorText` ile başlamalıdır.
- Son metin adı `HeaderFieldText` ile başlamalıdır.
- `CaptionImage` atlanabilir.

### <a name="progress-indicator"></a>İlerleme göstergesi

Başlığın sağında gösterilen bir ilerleme göstergesi ekleyebilirsiniz. Aşağıdaki resimde ilerleme göstergesi gösterilmektedir.

![Tipik ilerleme göstergesi.](media/pfe-styles-header-progress.png "Tipik ilerleme göstergesi")

İlerleme göstergesini göstermek için metin alanının `ShowProgress` olarak adlandırılması gerekir.

## <a name="grid"></a>Kılavuz

Stiller, otomatik olarak uygulanır. Belirli bir konfigürasyon gerekmez.

Yeni bir kılavuz henüz desteklenmediğinden, kılavuz bir `TabularView` stiline sahip olmalı ve özel formdaki `run()` yönteminin üzerine yazılmalı. Aşağıdaki kodu ekleyin.

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

Bir ana görünümdeki verileri yenilemek için, eylemlerinizin bir `click` yönteminde olduğu gibi bir `this.parmParentForm().updateLayout();` kullanmak isteyebilirsiniz. (Örneğin, `JmgProductionFloorExecutionReportFeedbackAction` sınıfa bakın) Yalnızca yeni formunuzda `parmDataSource`'un, `init`'te ayarlandığından emin olun (`formCaller.parmDataSource(this.dataSource(1));`). Örneğin, `JmgProductionFloorExecutionMainGrid` formuna bakın.

## <a name="card-view"></a>Kart görünümü

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde kart görünümü kontrollerine uygulanabilir:

- Her kart görünümü, bir form grubunda yer alır.
- Grup adı, `CardGroup`ile başlar (örneğin `CardGroupJobsView`).

Aşağıdaki resimde, içinde denetimleri olmayan bir kart görünümü gösterilmektedir.

![Öğe olmadan kart görünümü.](media/pfe-styles-empty-card.png)

Aşağıdaki resimlerde, içinde denetimleri olan kart görünümleri gösterilmektedir.

![Hz gösteren öğeleri olan kart.](media/pfe-styles-elements.png)

![Bakım isteği için öğelerle ilgili kart.](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>Kartvizit

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde kartvizit kontrollerine uygulanabilir:

- Her kartvizit, bir form grubunda yer alır.
- Grup adı, `BusinessCardGroup`ile başlar (örneğin `BusinessCardGroupJobsList`).

Kartvizit üzerinde aşağıdaki özellikleri ayarlayın:

- **Stil:** *liste*
- **Genişletilmiş stil:** *cardList*
- **Çoklu Seçim:** *Hayır*
- **Sütun Etiketlerini Göster:** *Hayır*

![Kartvizit.](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>Radyo düğmesi

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde radyo düğmelerine uygulanabilir:

- Her radyo düğmesi, bir form grubunda yer alır.
- Metnin görünmesini istediğiniz yere bağlı olarak, grup adı `RadioTextBelow` veya `RadioTextRight` ile başlar.

Radyo düğmesi üzerinde aşağıdaki özellikleri ayarlayın:

- **İki durumlu düğme:** *Kontrol*
- **İki durumlu düğme değeri:** Radyo düğmesinin seçilmesi gerekiyorsa *Açık*; Aksi durumda *Kapalı*

Aşağıdaki çizimde, metnin radyo düğmelerinin altında göründüğü bir örnek gösterilmektedir.

![Altında metin bulunan radyo düğmeleri.](media/pfe-styles-radio-text-below.png)

Aşağıdaki çizimde, metnin radyo düğmelerinin sağında göründüğü bir örnek gösterilmektedir.

![Sağ tarafta metin bulunan radyo düğmeleri.](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Internet Explorer içinde radyo düğmeleri

Internet Explorer'da desteklenmeyen radyo düğmesi stilleri. Aşağıdaki çizim, radyo düğmelerinin Internet Explorer'da nasıl gözükeceğini gösterir.

![Internet Explorer içinde radyo düğmeleri.](media/pfe-styles-browser.png)

## <a name="buttons"></a>Düğmeler

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde düğmelere uygulanabilir:

- Her düğme grubu, bir form grubunda yer alır. Gruptaki tüm düğmelerin aynı stile sahip olması gerekir.
- Grup adı hakkında herhangi bir gereksinim yoktur.

Düğmeler üzerinde aşağıdaki özellikleri ayarlayın:

- **Düğme görünümü:** *TextWithImageLeft*
- **Normal resim:** Bu özellik boş olamaz. Örneğin, *CoffeeScript* kullanın.
- **Metin:** Bu özellik boş olamaz. Örneğin, *Mola Başlat* kullanın.
- **Genişlik:** *Otomatik* veya *SizeToContent*
- **Yükseklik:** *Otomatik* veya *SizeToContent*

### <a name="primary-button"></a>Birincil düğme

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde temel düğmeye uygulanabilir:

- Düğme, bir form grubunda yer alır.
- Grup adı, `DefaultButtonGroup` veya `PrimaryButtonGroup` ile başlar (örneğin `DefaultButtonGroup10`).

![Birincil düğme.](media/pfe-styles-first.png)

### <a name="secondary-button"></a>İkincil düğme

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde ikincil düğmeye uygulanabilir:

- Düğme, bir form grubunda yer alır.
- Grup, **Sağ panel** adını taşır veya grup adı `SecondaryButtonGroup` ile başlar.

![İkincil düğme.](media/pfe-styles-second.png)

### <a name="third-group-button"></a>Üçüncü grup düğmesi

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde üçüncü grup düğmeye uygulanabilir:

- Düğme, bir form grubunda yer alır.
- Grup, **Sol panel** adını taşır veya grup adı `ThirdButtonGroup` ile başlar.

![Üçüncü grup düğmesi.](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>Dördüncü grup düğmesi

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde dördüncü grup düğmeye uygulanabilir:

- Düğme, bir form grubunda yer alır.
- Grup adı, `FourthButtonGroup` ile başlar.

Düğme üzerinde aşağıdaki özellikleri ayarlayın:

- **Düğme görünümü:** *TextOnly*
- **Normal resim:** Bu özellik boş olmalıdır.
- **Metin:** Bu özellik boş olamaz. Örneğin, *Görünüm* veya *Düzenle* kullanın.
- **Genişlik:** *Otomatik*
- **Yükseklik:** *Otomatik*

![Dördüncü grup düğmesi.](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>Düz düğme

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde düz düğmeye uygulanabilir:

- Düğme, bir form grubunda yer alır.
- Grup adı, `FlatButtonGroup` ile başlar.

Düğme üzerinde aşağıdaki özellikleri ayarlayın:

- **Düğme görünümü:** *ImageOnly*
- **Normal resim:** Bu özellik boş olamaz. Örneğin, *CoffeeScript* kullanın.
- **Metin:** Bu özellik boş olmalıdır.
- **Genişlik:** *Otomatik* veya *SizeToContent*
- **Yükseklik:** *Otomatik* veya *SizeToContent*

![Düz düğme.](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>Devam düğmesi

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde devam düğmesine uygulanabilir:

- Düğme, bir form grubunda yer alır.
- Grup adı, `ContinueButtonGroup` ile başlar.

Düğme üzerinde aşağıdaki özellikleri ayarlayın:

- **Düğme görünümü:** *ImageOnly*
- **Normal resim:** *İleri*
- **Metin:** Bu özellik boş olmalıdır.
- **Genişlik:** *Otomatik* veya *SizeToContent*
- **Yükseklik:** *Otomatik* veya *SizeToContent*

![Devam düğmesi.](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>Açılan kutu

Kombo kutusu, üç denetim birleşimidir: giriş denetimi, giriş denetimini temizleyen düğme ve arama çalıştıran düğme.

Stiller, yalnızca aşağıdaki gereksinimlerin karşılanması halinde kombo kutusuna uygulanabilir:

- Kombo kutusu, bir form grubunda yer alır.
- Grup adı, `Combobox` ile başlar.
- Grup içinde, ilk denetim bir `AxFormStringControl` denetimidir. Bu denetim, geçerli değeri gösterir ve kullanıcının gerekli değeri girdiği yerdir.
- İkinci denetim, `CommonButton` denetimidir ve adı `ClearButton` ile başlar. Bu düğme, düğmeyi göstermek veya gizlemek için `enable` özelliğini kullanan kodu içermelidir. Örneğin, kullanıcı giriş denetimine bilgi yazarken **Temizle** düğmesini göstermek ya da gizlemek için aşağıdaki kodu kullanabilirsiniz.

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    Giriş denetiminde verilerin ayarlandığı bir yönteminiz olmalıdır. Bu yöntemdeki **Temizle** düğmesini etkinleştirin. Aşağıda bir örnek verilmiştir.

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    **Temizle** düğmesinin `clicked` yöntemi için aşağıdaki kodu kullanın.

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    Form, `init` yöntemi kullanılarak başlatıldığında, giriş denetiminin (`AxFormStringControl`) değerini ayarlayın. Değer boş değilse, **Temizle** düğmesini etkinleştirin. Değer boşsa, **Temizle** düğmesini devre dışı bırakın.

- Üçüncü denetim, `CommonButton` denetimidir ve adı `SearchButton` ile başlar.

Aşağıdaki resimde, iki kombo kutusu denetimi gösterilmektedir. Soldaki kombo kutusunda boş bir metin kutusu vardır ve **Temizle** düğmesi devre dışı bırakılmıştır. Sağdaki kombo kutusunda metin kutusunda metin vardır ve **Temizle** düğmesi etkinleştirilmiştir.

![Temizle düğmesi olan ve olmayan kombo kutuları.](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>Hızlı filtre

Hızlı filtre denetimi, sayfaya bir arama alanı ekler. Aşağıdaki gereksinimlerin karşılanması koşuluyla, hızlı filtreye stil uygulayabilirsiniz:

- Hızlı filtre, bir form grubunda yer alır.
- Grup adı, `SearchInputGroup` ile başlar.
- Grup içinde, ilk denetim bir `QuickFilter` denetimidir. (Bu denetim, kullanıcının arama dizesine girdiği yerdir.)
- İkinci denetim `NumberOfResults` adlı bir `FormStaticTextControl` denetimidir. (Bu kontrol isteğe bağlıdır. Dahil edilirse bulunan madde sayısını gösterir.)
- Üçüncü denetim, `CommonButton` denetimidir ve adı `ClearButton` ile başlar.

Aşağıdaki resimde, iki hızlı filtre denetimi gösterilmektedir. Soldaki hızlı filtrenin boş bir hızlı filtresi vardır ve sonuç sayısı görünür değildir. Sağdaki hızlı filtre bir arama dizesi içerir ve sonuçların sayısını gösterir.

![Arama dizesi olan ve olmayan hızlı filtre denetimi örnekleri.](media/pfe-styles-quick-filter.png "Arama dizesi olan ve olmayan hızlı filtre denetimi örnekleri")

## <a name="center-align-elements-on-a-tab"></a>Sekmedeki öğeleri ortala

Öğeleri bir sekmenin ortasına hizalamak için, grup adının `TabContentGroup` ile başlaması ve grubun aşağıdaki özelliklere sahip olması gerekir:

- **Genişlik Modu:** `SizeToAvailable`
- **Yükseklik Modu:** `SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>Kılavuzu, ayrıntı parçasını ve hızlı filtreyi hizalama

Özelleştirilmiş bir kılavuz, ayrıntı parçasını ve hızlı filtreyi standart tasarıma benzeyecek şekilde düzenlemek için, tümünü birlikte yerleştirdiğinizde aşağıdaki noktaları aklınızda bulundurun:

- Kılavuzun hızlı bir filtresi varsa, hem kılavuzun hem de hızlı filtrenin, adı `GridGroup` ile başlayan grubun içinde olması gerekir.
- Stilleri ayrıntı parçasına uygulamak için grup adının `DetailInformationGroup` ile başlaması gerekir,

Aşağıdaki çizim, bir hızlı filtre ve bir ayrıntı bölümünü içeren tipik bir Kılavuzu göstermektedir.

![Hızlı filtreleme ve ayrıntı parçası dahil olan tipik bir kılavuz.](media/pfe-styles-align-grid.png "Hızlı filtreleme ve ayrıntı parçası dahil olan tipik bir kılavuz")

Visual Studio'da, kılavuz, ayrıntı parçası ve hızlı filtre aşağıdaki çizimde gösterilen gibi bir yapı kullanılarak oluşturulur.

![Kılavuz, ayrıntı parçası ve hızlı filtreleme dahil olan tipik bir kod yapısı.](media/pfe-styles-header-code-structure2.png "Kılavuz, ayrıntı parçası ve hızlı filtreleme dahil olan tipik bir kod yapısı")

## <a name="additional-resources"></a>Ek kaynaklar

- [Üretim katı yürütme arabirimini özelleştirme](production-floor-execution-customize.md)
- [Üretim katı yürütme arabirimini tasarlama](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
