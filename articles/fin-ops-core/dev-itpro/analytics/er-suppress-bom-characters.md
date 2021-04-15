---
title: Oluşturulan dosyalardaki BOM karakterlerini gizlemek için ER yapılandırmaları tasarlama
description: Bu konuda, bayt sırası işaretlerini (BOM) gizleyen raporlar oluşturmak için Elektronik raporlama (ER) biçiminin nasıl yapılandırılacağı açıklanmaktadır.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fabc308b1b0682c6fdce3e81e7335417846bebd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743545"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>Oluşturulan dosyalardaki BOM karakterlerini gizlemek için ER yapılandırmaları tasarlama

[!include [banner](../includes/banner.md)]

Giden belgeler oluşturmak için bir [Elektronik raporlama (ER)](general-electronic-reporting.md) [çözümü](er-quick-start1-new-solution.md) tasarlayabilirsiniz. Belgeleri metin veya XML dosyaları olarak oluşturmak için çözümde, ER [biçimi](general-electronic-reporting.md#FormatComponentOutbound) içeren bir ER [yapılandırması](general-electronic-reporting.md#Configuration) bulunmalıdır. Oluşturulan dosyalardaki karakter kümesini temsil eden [karakter kodlamasını](https://docs.microsoft.com/windows/win32/intl/character-sets) belirtmek için ER biçimi, **Common\\File** biçim öğesini içermelidir. ER biçim bileşenini yapılandırmak için ER biçim tasarımcısında ER yapılandırmasının [taslak](general-electronic-reporting.md#component-versioning) sürümünü açın ve **Common\\File** öğesini ekleyin. **Kodlama** alanında, bu bileşen kullanılarak çalışma zamanında oluşturulan giden dosyaların kodlamasını belirtin.

> [!NOTE]
> Biçim yanlış bir kodlama adı içeriyorsa değişikliklerinizi biçim ayarlarında kaydettiğinizde hata oluşur.

![Biçim tasarımcısı sayfasına kök öğe ekleme](./media/er-suppress-bom-characters-image1.gif)

Kodlama olarak **UTF-8**, **UTF-16** veya **UTF-32** kodlamalarını belirtirseniz **BOM karakterlerini gizle** seçeneği sunulur. Düzenlenebilir ER biçimi çalıştırıldığında çalışma zamanında oluşturulan giden dosyalarda [bayt sırası işareti (BOM) karakterlerini](https://docs.microsoft.com/globalization/encoding/byte-order-mark) gizlemek için bu seçeneği **Evet** olarak ayarlayın.

> [!NOTE]
> **Kodlama** alanını boş bırakırsanız varsayılan **UTF-8** kodlaması kullanılır.

![Biçim tasarımcısı sayfasında BOM karakterlerini gizle seçeneğini ayarlama](./media/er-suppress-bom-characters-image2.gif)

Çalışma zamanında işlevi incelemek için uygun yordamı tamamlayın. Örneğin, [ER biçimindeki XML öğelerinin yürütülmesini erteleme](er-defer-xml-element.md) konusundaki adımları tamamlayın. Konunun [Hesaplamada, oluşturulan çıktının temel alınması için biçimi değiştirme](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) bölümündeki adımları tamamladıktan sonra aşağıdaki ek adımları da izleyin.

1. UTF kodlamasını belirtin:

    1. **Common\\File** türünün **Rapor** öğesini seçin.
    2. **Kodlama** alanında **UTF-8** kodlamasını belirtin.

2. BOM karakteri içeren bir XML dosyası oluşturun:

    1. Oluşturulan XML dosyalarına BOM karakterlerini eklemek için **BOM karakterlerini gizle** seçeneğini **Hayır** olarak ayarlayın.
    2. [ER biçimindeki XML öğelerinin yürütülmesini erteleme](er-defer-xml-element.md) konusunun [Hesaplanan toplamın kullanılmasını sağlamak için özet XML öğesinin yürütülmesini erteleme](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) bölümündeki adımları tamamlayın ve oluşturulan dosyayı **SampleXmlReport.xml** olarak kaydedin.

3. BOM karakteri içermeyen bir XML dosyası oluşturun:

    1. Oluşturulan XML dosyalarında BOM karakterlerini gizlemek için **BOM karakterlerini gizle** seçeneğini **Evet** olarak ayarlayın.
    2. [ER biçimindeki XML öğelerinin yürütülmesini erteleme](er-defer-xml-element.md) konusunun [Hesaplanan toplamın kullanılmasını sağlamak için özet XML öğesinin yürütülmesini erteleme](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) bölümündeki adımları tamamlayın ve oluşturulan dosyayı **SampleXmlReport (1).xml** olarak kaydedin.

4. Dosya karşılaştırma yardımcı programında, oluşturulan dosyaları karşılaştırın.

    Göreceğiniz ilk fark dosya üst bilgisinde olur. SampleXmlReport.xml file dosyası, BOM karakteri içerirken SampleXmlReport (1).xml dosyası içermez.

    ![Dosya karşılaştırma yardımcı programı kullanarak, oluşturulan dosyaları karşılaştırma](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>Ayrıca bkz.

- [ER biçimindeki XML öğelerinin yürütülmesini erteleme](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]