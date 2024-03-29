---
title: Mali rapor bileşenleri
description: Bu makalede rapor tanımlarının bileşenlerinin veya yapı taşlarının finansal raporlamada nasıl kullanıldığı açıklanmaktadır.
author: aprilolson
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.form: FinancialReports
ms.openlocfilehash: 180b3c64b9eb506f162071a67b1fa9b728a569ce
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831623"
---
# <a name="financial-report-components"></a>Mali rapor bileşenleri

[!include [banner](../includes/banner.md)]

Bu makalede rapor tanımlarının bileşenlerinin veya yapı taşlarının finansal raporlamada nasıl kullanıldığı açıklanmaktadır. Bu yapı taşları satır tanımlarını, sütun tanımlarını ve raporlama ağacı tanımlarını içerir. Bu makalede yapı taşlarının nasıl düzenleneceği ve kilitleneceği açıklanmaktadır.

Finansal rapor tasarımcısının ardında yatan tasarım felsefesi bilgiyi en küçük bileşenlerine veya yapı taşlarına ayırmak ve bileşenleri gerektiği gibi karıştırıp eşleştirmektir. Bu nedenle rapor biçimlendirmeniz mali verilerinizden ayrıdır ve bir raporun tasarımını Microsoft Dynamics 365 Finance'taki mali verileri değiştirmeden değiştirebilirsiniz. Bu yapı taşı yaklaşımını kullanarak, ihtiyaç duyduğunuz raporları üretmek için metinleri, tutarları ve hesaplamaları birleştirebilirsiniz. Ayrıca, bu esneklik işlemlerinizi farklı yollarla görüntülemenizi kolaylaştırarak yaratıcılığı teşvik eder. Bir rapor tanımının bağımsız yapı taşları üç boyutlu bir elektronik tabloya benzer, ancak daha fazla güce sahiptir. Bir rapor tanımı, satır tanımı, sütun tanımı ve rapor için kullanılması gereken isteğe bağlı raporlama ağacı tanımını belirtir. Ayrıca oluşturulan raporun nerede saklanacağı ve nasıl biçimlendirileceği hakkında bilgiler içerir.

## <a name="building-blocks-of-a-report"></a>Bir raporun yapı taşları

| Yapı taşı            | Tanım | Daha fazla bilgi için |
|---------------------------|-------------|----------------------|
| Satır tanımı            | Satır tanımı bir rapordaki açıklayıcı satırları (örneğin, maaşlar veya satışlar) tanımlar. Ayrıca her kalemin değerlerini içeren segment değerlerini veya boyutlarını belirtir ve satır biçimlendirmesi ile hesaplamalarını içerir. | [Satır tanımları](row-definitions-financial-reporting.md) |
| Sütun tanımı         | Sütun tanımı veriler mali boyutlardan çıkarıldığında kullanılacak dönemi tanımlar. Ayrıca sütun biçimlendirmesini ve hesaplamalarını da içerir. | [Sütun tanımları](column-definitions-financial-reports.md) |
| Raporlama ağacı tanımı | Raporlama ağacı tanımı bir kuruluş şemasına benzer. Şemadaki her kutuyu temsil eden bağımsız raporlama birimleri içerir. Birimler mali verilerdeki bağımsız departmanlar ya da diğer raporlama birimlerindeki verileri özetleyen üst düzey birimler olabilir. | [Raporlama ağacı tanımları](financial-reporting-tree-definitions.md) |
| Rapor tanımı         | Bir rapor tanımında, bir satır tanımı, bir sütun tanımı ve rapor oluşturmak için isteğe bağlı bir raporlama ağacı tanımı kullanılır. Ayrıca bir rapor özelleştirmek için kullanabileceğiniz ek seçenekler ve ayarlar sağlar. | [Rapor tanımı](design-financial-report-definitions.md) |

Rapor tasarlamaya yeni başladıysanız daha sonra özelleştirebileceğiniz bir rapor tanımını hızlıca oluşturmak için rapor sihirbazını kullanmanız iyi olabilir. Rapor tasarımında deneyimliyseniz ve rapor tasarımı için daha fazla esneklik istiyorsanız yeni bir rapor tanımı oluşturmak için yeni veya var olan yapı taşlarını birleştirebilirsiniz. Kaliteli raporlar oluşturmak için tüm kullanılabilen rapor tanımı seçeneklerini eksiksiz olarak anlamanız gerekmez. Rapor tasarlama konusunda bilgi edindikçe daha gelişmiş özelliklerden yararlanmak için rapor tanımlarınızı genişletebilirsiniz. Temel bir rapor oluşturduktan sonra, rapor tanımını ve rapor tanımındaki herhangi bir yapı taşını özelleştirebilirsiniz.

## <a name="organize-the-building-blocks"></a>Yapı taşlarını düzenleme
Rapor Tasarımcısı'nda yapı taşlarınızı düzenlemek için klasörleri kullanın. Tüm klasörler içerdikleri yapı taşının türüne özeldir. Örneğin, satır tanımlarını içeren tüm klasörler Report Designer'da **Satır Tanımları** bölmesinde yer alır.

### <a name="create-a-folder"></a>Klasör oluşturma

1. Report Designer'da, gezinti bölmesinde düzenlemek için yapı taşı türünü seçin. Örneğin, bir satır tanımını sıralamak için **Satır Tanımları**'na tıklayın.
2. Gezinti bölmesinde, altta yeni bir klasör oluşturmak için var olan bir klasörü seçin ve ardından şu adımlardan birini izleyin:

    - Üst klasöre sağ tıklayın ve ardından **Yeni klasör**'e tıklayın.
    - Üst klasörü seçin, **Dosya**'ya ve ardından **Yeni klasör**'e tıklayın.

3. Yeni klasör göründüğünde, yeni klasörün adını girin ve ardından **Enter**'a basın.

## <a name="lock-a-building-block"></a>Bir yapı taşını kilitleme
Kilitlemek için parola oluşturarak yapı taşını korumaya yardımcı olabilirsiniz. Bu şekilde tüm sistemi güvenlik altına almadan bir rapor bileşenine bir güvenlik düzeyi ekleyebilirsiniz. Parola ay sonu raporlama işleminiz açısından önemli olan yapı taşı bilgilerini korumaya yardımcı olabilir. Bir yapı taşını tüm rollerdeki kullanıcılar kilitleyebilir. Ancak diğer kullanıcıların kilitli bileşene her zaman salt okunur erişimi olur. Kullanıcılar kilitli bileşeni açabilir, değiştirebilir ve yeni bir adla kaydedebilir. Yönetici rolüne sahip bir kullanıcı her zaman kilitli bir yapı taşına erişebilir ve yapı taşını değiştirebilir.

1. Report Designer'da, satır tanımı, sütun tanımı, rapor tanımı veya raporlama ağacı tanımı gibi kilitlenecek rapor bileşenini açın.
2. **Araçlar** menüsünde, **Koru/Korumayı Kaldır**'a tıklayın. Ayrıca araç çubuğundaki **Koru/Korumayı Kaldır**'a (kilit simgesi) da tıklayabilirsiniz.
3. **Koru** iletişim kutusunda, parola girip onaylayın ve ardından **Tamam**'a tıklayın. Araç çubuğundaki kilit simgesi açık bir yapı taşı kilitlendiğinde vurgulanır.

Kilitli bir yapı taşının kilidini açmak için, yapı taşını açın ve ardından araç çubuğunda **Koru/Korumayı Kaldır**'a tıklayın. Alternatif olarak, **Araçlar** menüsünde, **Korumayı Kaldır**'a tıklayın.

## <a name="building-block-groups"></a>Yapı taşı grupları

Yapı taşları bir rapor için oluşturduğunuz satır tanımları, sütun tanımları, raporlama ağacı tanımları ve rapor tanımlarıdır. Yapı taşı grupları tanımlardan ve boyut değeri kümelerinden oluşan koleksiyonlardır.

### <a name="view-a-building-block-group"></a>Bir yapı taşı grubunu görüntüleme

Bir yapı taşı grubuna atanan tüm yapı taşlarını görüntüleyebilirsiniz. Ayrıca bir yapı taşı grubunu dışa veya içe aktarabilirsiniz.

1. Report Designer'da, **Şirket** menüsünde, **Yapı taşı grupları**'na tıklayın.
2. **Yapı taşı grupları** iletişim kutusunda, görüntülenecek yapı taşı grubunu seçin.
3. **Görüntüle**'ye tıklayarak **Yapı taşı grubunu görüntüle** iletişim kutusunu açın. Burada yapı taşı grubunun içindekileri görüntüleyebilirsiniz.
4. İletişim kutularını kapatmak için **Kapat**'a tıklayın.

### <a name="export-a-building-block-group"></a>Bir yapı taşı grubunu dışa aktarma

Bir yapı taşı grubunu veya bir yapı taşı grubundaki belirli rapor yapı taşlarını dışa aktarabilirsiniz. Dışa aktarılan yapı taşı grubunu yedek olarak kullanabilirsiniz. Dışa aktarılan veriyi kurulumlar arasında kopyalayabilirsiniz. Report Designer, yapı taşı grubuyla birlikte başvurulan yazı tipi stillerini ve boyut değeri kümelerini içerir.

1. Report Designer'da, **Şirket** menüsünde, **Yapı taşı grupları**'na tıklayın.
2. **Yapı taşı grupları** iletişim kutusunda, dışa aktarılacak yapı taşı grubunu seçin ve ardından **Dışa Aktar**'a tıklayın.
3. **Dışa Aktar** iletişim kutusunda, dışa aktarılacak rapor tanımlarını seçin:

    - Tüm rapor tanımlarınızı ve ilişkili yapı taşlarını dışa aktarmak için **Tümünü seç**'e tıklayın.
    - Belirli raporları, satırları, sütunları, ağaçları veya boyut değeri kümelerini dışa aktarmak için, ilgili sekmeye tıklayın ve ardından dışa aktarılacak maddeleri seçin. Bir sekmedeki birden fazla maddeyi seçmek için Ctrl tuşunu basılı tutun.

    > [!NOTE]
    > Dışa aktarılacak raporları seçtiğinizde ilişkili satırlar, sütunlar, ağaçlar ve boyut değeri kümeleri seçilir.

4. Dışa aktarılacak maddeleri seçmeyi tamamladığınızda, **Dışa Aktar**'a tıklayın.
5. **Farklı Kaydet** iletişim kutusunda, yapı taşının dışa aktarılacağı konumu seçin.
6. **Dosya adı** alanına dosya için bir ad girin. Rapor tasarımcısı otomatik olarak bir .tdbx dosya adı uzantısı ekler.
7. **Kaydet**'i tıklatın. Yapı taşı grubu belirttiğiniz konuma kaydedilir.

### <a name="import-a-building-block-group"></a>Bir yapı taşı grubunu içe aktarma

Bir yapı taşı grubunu mevcut bir yapı taşı grubuna aktarabilirsiniz. İçe aktarılan tüm yapı taşı grupları kendi orijinal yazı tipi stillerini ve şirket referanslarını korur ve ilgili boyut değeri kümelerini içerir.

1. Report Designer'da, **Şirket** menüsünde, **Yapı taşı grupları**'na tıklayın.
2. **Yapı taşı grupları** iletişim kutusunda, bir yapı taşı grubuna aktarılacak yapı taşını seçin ve ardından **İçe Aktar**'a tıklayın.
3. **Aç** iletişim kutusunda, içe aktarılacak yapı taşı grubunu seçin ve ardından **Aç**'a tıklayın.
4. **İçe Aktar** iletişim kutusunda, içe aktarılacak rapor tanımlarını seçin:

    - Tüm rapor tanımlarını ve destekleyici yapı taşlarını içe aktarmak için **Tümünü seç**'e tıklayın.
    - Belirli raporları, satırları, sütunları, ağaçları veya boyut değeri kümelerini içe aktarmak için, içe aktarılacak raporları, satırları, sütunları, ağaçları veya boyut değeri kümelerini seçin.

5. İçe aktarılacak maddeleri seçmeyi tamamladığınızda, **İçe Aktar**'a tıklayın.

### <a name="undo-a-checkout-of-a-building-block"></a>Bir yapı taşını kullanıma almayı geri alma

Bir yapı taşını açtığınızda, diğer kullanıcılar söz konusu yapı taşına salt okunur olarak erişebilir. Bazen, kullanıcılar bir yapı taşını kapatmayı unutur veya yapı taşını kapatmadan sistemlerini kapatır. Bu nedenle, yapı taşı etkin kalır ve diğer kullanıcılar bu yapı taşını açamaz. Bu gibi durumlarda, bir finansal raporlama yöneticisi **Kullanıma Alınan Maddeler** iletişim kutusunu kullanarak kullanıcıların kullanıma aldığı yapı taşlarını kullanıma açabilir.

> [!NOTE]
> **Kullanıma Alınan Öğeler** iletişim kutusunu kullanarak yapı taşlarını kullanımdan çıkarmak için yönetici rolüne sahip olmanız gerekir.

1. Report Designer'da, **Araçlar** menüsünde, **Kullanıma alınan maddeler**'e tıklayın.
2. **Kullanıma alınan maddeler** iletişim kutusunda, **Tüm kullanıcılara ait maddeleri göster**'i seçin. Liste kullanıma alının tüm yapı taşlarını ve bunları kullanıma alan kullanıcıları gösterecek şekilde güncelleştirilir.
3. Bir yapı taşı seçin ve ardından **Kullanıma almayı geri al**'a tıklayın.
4. Yapı taşı grubunu kullanımdan çıkarmak için **Evet**'e tıklayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Mali raporlama](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
