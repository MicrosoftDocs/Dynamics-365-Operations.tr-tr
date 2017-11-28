---
title: "Mali rapor bileşenleri"
description: "Bu makalede rapor tanımlarının bileşenlerinin veya yapı taşlarının finansal raporlamada nasıl kullanıldığı açıklanmaktadır. Bu yapı taşları satır tanımlarını, sütun tanımlarını ve raporlama ağacı tanımlarını içerir. Bu makalede yapı taşlarının nasıl düzenleneceği ve kilitleneceği ve yapı taşı grupları ile nasıl çalışılacağı açıklanmaktadır."
author: aolson
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7b283b8550bd7e5eff969d45c761d0a54d93a33e
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="financial-report-components"></a>Mali rapor bileşenleri

[!include[banner](../includes/banner.md)]


Bu makalede rapor tanımlarının bileşenlerinin veya yapı taşlarının finansal raporlamada nasıl kullanıldığı açıklanmaktadır. Bu yapı taşları satır tanımlarını, sütun tanımlarını ve raporlama ağacı tanımlarını içerir. Bu makalede yapı taşlarının nasıl düzenleneceği ve kilitleneceği açıklanmaktadır. 

Finansal rapor tasarımcısının ardında yatan tasarım felsefesi bilgiyi en küçük bileşenlerine veya yapı taşlarına ayırmak ve bileşenleri gerektiği gibi karıştırıp eşleştirmektir. Bu nedenle rapor biçimlendirmeniz mali verilerinizden ayrıdır ve bir raporun tasarımını Microsoft Dynamics ERP sisteminizdeki mali verileri değiştirmeden değiştirebilirsiniz. Bu yapı taşı yaklaşımını kullanarak, ihtiyaç duyduğunuz raporları üretmek için metinleri, tutarları ve hesaplamaları birleştirebilirsiniz. Ayrıca, bu esneklik işlemlerinizi farklı yollarla görüntülemenizi kolaylaştırarak yaratıcılığı teşvik eder. Bir rapor tanımının bağımsız yapı taşları üç boyutlu bir elektronik tabloya benzer, ancak daha fazla güce sahiptir. Bir rapor tanımı, satır tanımı, sütun tanımı ve rapor için kullanılması gereken isteğe bağlı raporlama ağacı tanımını belirtir. Ayrıca oluşturulan raporun nerede saklanacağı ve nasıl biçimlendirileceği hakkında bilgiler içerir. 

## <a name="building-blocks-of-a-report"></a>Bir raporun yapı taşları
| Yapı taşı            | Tanım                     | Daha fazla bilgi için                                    |
|---------------------------|---------------------------------|---------------------------------------------------------|
| Satır tanımı            | Satır tanımı bir rapordaki açıklayıcı satırları (örneğin, maaşlar veya satışlar) tanımlar. Ayrıca her kalemin değerlerini içeren segment değerlerini veya boyutlarını belirtir ve satır biçimlendirmesi ile hesaplamalarını içerir.                                                    | [Satır tanımları](row-definitions-financial-reporting.md)                       |
| Sütun tanımı         | Sütun tanımı veriler mali boyutlardan çıkarıldığında kullanılacak dönemi tanımlar. Ayrıca sütun biçimlendirmesini ve hesaplamalarını da içerir.                                                                                                                                 | [Sütun tanımları](column-definitions-financial-reports.md)         |
| Raporlama ağacı tanımı | Raporlama ağacı tanımı bir kuruluş şemasına benzer. Şemadaki her kutuyu temsil eden bağımsız raporlama birimleri içerir. Birimler mali verilerdeki bağımsız departmanlar ya da diğer raporlama birimlerindeki verileri özetleyen üst düzey birimler olabilir. | [Raporlama ağacı tanımları](financial-reporting-tree-definitions.md) |
| Rapor tanımı         | Bir rapor tanımında, bir satır tanımı, bir sütun tanımı ve rapor oluşturmak için isteğe bağlı bir raporlama ağacı tanımı kullanılır. Ayrıca bir rapor özelleştirmek için kullanabileceğiniz ek seçenekler ve ayarlar sağlar.                                                                    | [Rapor tanımı](design-financial-report-definitions.md)                  |

Rapor tasarlamaya yeni başladıysanız daha sonra özelleştirebileceğiniz bir rapor tanımını hızlıca oluşturmak için rapor sihirbazını kullanmanız iyi olabilir. Rapor tasarımında deneyimliyseniz ve rapor tasarımı için daha fazla esneklik istiyorsanız yeni bir rapor tanımı oluşturmak için yeni veya var olan yapı taşlarını birleştirebilirsiniz. Kaliteli raporlar oluşturmak için tüm kullanılabilen rapor tanımı seçeneklerini eksiksiz olarak anlamanız gerekmez. Rapor tasarlama konusunda bilgi edindikçe daha gelişmiş özelliklerden yararlanmak için rapor tanımlarınızı genişletebilirsiniz. Temel bir rapor oluşturduktan sonra, rapor tanımını ve rapor tanımındaki herhangi bir yapı taşını özelleştirebilirsiniz.

## <a name="organize-the-building-blocks"></a>Yapı taşlarını düzenleme
Rapor Tasarımcısı'nda yapı taşlarınızı düzenlemek için klasörleri kullanın. Tüm klasörler içerdikleri yapı taşının türüne özeldir. Örneğin, satır tanımlarını içeren tüm klasörler Rapor Tasarımcısı'ndaki **Satır Tanımları** bölmesinde yer alır.

### <a name="create-a-folder"></a>Klasör oluşturma

1.  Rapor Tasarımcısı'nda, gezinti bölmesinde düzenlemek için yapı taşı türünü seçin. Örneğin, bir satır tanımını sıralamak için **Satır Tanımları**'na tıklayın.
2.  Gezinti bölmesinde, altta yeni bir klasör oluşturmak için var olan bir klasörü seçin ve ardından şu adımlardan birini izleyin:
    -   Üst klasöre sağ tıklayın ve ardından **Yeni Klasör**'e tıklayın.
    -   Üst klasörü seçin, **Dosya**'ya ve ardından **Yeni Klasör**'e tıklayın.

3.  Yeni klasör göründüğünde, yeni klasörün adını girin ve ardından Enter'a basın.

## <a name="lock-a-building-block"></a>Bir yapı taşını kilitleme
Kilitlemek için parola oluşturarak yapı taşını korumaya yardımcı olabilirsiniz. Bu şekilde tüm sistemi güvenlik altına almadan bir rapor bileşenine bir güvenlik düzeyi ekleyebilirsiniz. Parola ay sonu raporlama işleminiz açısından önemli olan yapı taşı bilgilerini korumaya yardımcı olabilir. Herhangi bir roldeki bir kullanıcı bir yapı taşını kilitleyebilir. Ancak, diğer kullanıcılar kilitli bir bileşene yalnızca salt okunur olarak erişebilir. Kullanıcılar kilitli bileşeni açabilir, değiştirebilir ve yeni bir adla kaydedebilir. Yönetici rolüne sahip bir kullanıcı her zaman kilitli bir yapı taşına erişebilir ve yapı taşını değiştirebilir.
1.  Rapor Tasarımcısı'nda, satır tanımı, sütun tanımı, rapor tanımı veya raporlama ağacı tanımı gibi kilitlenecek rapor bileşenini açın.
2.  **Araçlar** menüsünde, **Koru/Korumayı Kaldır**'a tıklayın. Ayrıca araç çubuğundaki **Koru/Korumayı Kaldır**'a (kilit simgesi) da tıklayabilirsiniz.
3.  **Koru** iletişim kutusunda, parola girip onaylayın ve ardından **Tamam**'a tıklayın. Araç çubuğundaki kilit simgesi açık bir yapı taşı kilitlendiğinde vurgulanır.

Kilitli bir yapı taşının kilidini açmak için, yapı taşını açın ve ardından araç çubuğunda **Koru/Korumayı Kaldır**'a tıklayın. Alternatif olarak, **Araçlar** menüsünde, **Korumayı Kaldır**'a tıklayın.

## <a name="building-block-groups"></a>Yapı taşı grupları

Yapı taşları bir rapor için oluşturduğunuz satır tanımları, sütun tanımları, raporlama ağacı tanımları ve rapor tanımlarıdır. Yapı taşı grupları tanımlardan ve boyut kümelerinden oluşan koleksiyonlardır. 


### <a name="view-a-building-block-group"></a>Bir yapı taşı grubunu görüntüleme

Bir yapı taşı grubuna atanan tüm yapı taşlarını görüntüleyebilirsiniz. Ayrıca bir yapı taşı grubunu dışa veya içe aktarabilirsiniz.
1.  Rapor Tasarımcısı'nda, **Şirket** menüsünde, **Yapı Taşı Grupları**'na tıklayın.
2.  **Yapı Taşı Grupları** iletişim kutusunda, görüntülenecek yapı taşı grubunu seçin.
3.  **Görüntüle**'ye tıklayarak **Yapı Taşı Grubunu Görüntüle** iletişim kutusunu açın. Burada yapı taşı grubunun içindekileri görüntüleyebilirsiniz.
4.  İletişim kutularını kapatmak için **Kapat**'a tıklayın.

### <a name="export-a-building-block-group"></a>Bir yapı taşı grubunu dışa aktarma

Bir yapı taşı grubunu veya bir yapı taşı grubundaki belirli rapor yapı taşlarını dışa aktarabilirsiniz. Dışa aktarılan yapı taşı grubunu yedek olarak kullanabilirsiniz. Dışa aktarılan veriyi Finance and Operations kurulumları arasında kopyalayabilirsiniz. Rapor tasarımcısı, yapı taşı grubuyla birlikte başvurulan yazı tipi stillerini ve boyut kümelerini içerir.
1.  Rapor Tasarımcısı'nda, **Şirket** menüsünde, **Yapı Taşı Grupları**'na tıklayın.
2.  **Yapı Taşı Grupları** iletişim kutusunda, dışa aktarılacak yapı taşı grubunu seçin ve ardından **Dışa Aktar**'a tıklayın.
3.  **Dışa Aktar** iletişim kutusunda, dışa aktarılacak rapor tanımlarını seçin:
    -   Tüm rapor tanımlarınızı ve ilişkili yapı taşlarını dışa aktarmak için **Tümünü Seç**'e tıklayın.
    -   Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini dışa aktarmak için, ilgili sekmeye tıklayın ve ardından dışa aktarılacak maddeleri seçin. Bir sekme birden fazla öğeyi seçmek için Ctrl tuşunu basılı tutun. **Not:** Dışa aktarılacak raporları seçtiğinizde ilişkili satırlar, sütunlar, ağaçlar ve boyut kümeleri seçilir.

4.  Dışa aktarılacak maddeleri seçmeyi tamamladığınızda, **Dışa Aktar**'a tıklayın.
5.  **Farklı Kaydet** iletişim kutusunda, yapı taşının dışa aktarılacağı konumu seçin.
6.  **Dosya Adı** alanına dosya için bir ad girin. Rapor tasarımcısı otomatik olarak bir .tdbx dosya adı uzantısı ekler.
7.  **Kaydet**'i tıklatın. Yapı taşı grubu belirttiğiniz konuma kaydedilir.

### <a name="import-a-building-block-group"></a>Bir yapı taşı grubunu içe aktarma

Bir yapı taşı grubunu mevcut bir yapı taşı grubuna aktarabilirsiniz. İçe aktarılan tüm yapı taşı grupları kendi orijinal yazı tipi stillerini ve şirket referanslarını korur ve ilgili boyut kümelerini içerir.
1.  Rapor Tasarımcısı'nda, **Şirket** menüsünde, **Yapı Taşı Grupları**'na tıklayın.
2.  **Yapı Taşı Grupları** iletişim kutusunda, bir yapı taşı grubuna aktarılacak yapı taşını seçin ve ardından **İçe Aktar**'a tıklayın.
3.  **Aç** iletişim kutusunda, içe aktarılacak yapı taşı grubunu seçin ve ardından **Aç**'a tıklayın.
4.  **İçe Aktar** iletişim kutusunda, içe aktarılacak rapor tanımlarını seçin:
    -   Tüm rapor tanımlarını ve destekleyici yapı taşlarını içe aktarmak için **Tümünü Seç**'e tıklayın.
    -   Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini içe aktarmak için, içe aktarılacak raporları, satırları, sütunları, ağaçları veya boyut kümelerini seçin.

5.  İçe aktarılacak maddeleri seçmeyi tamamladığınızda, **İçe Aktar**'a tıklayın.

### <a name="undo-a-checkout-of-a-building-block"></a>Bir yapı taşını kullanıma almayı geri alma

Bir yapı taşını açtığınızda, diğer kullanıcılar söz konusu yapı taşına salt okunur olarak erişebilir. Bazen, kullanıcılar bir yapı taşını kapatmayı unutur veya yapı taşını kapatmadan sistemlerini kapatır. Bu nedenle, yapı taşı etkin kalır ve diğer kullanıcılar bu yapı taşını açamaz. Böyle durumlarda, bir finansal raporlama yöneticisi **Kullanıma Alınan Maddeler** iletişim kutusunu kullanarak, kullanıcıların kullanıma alınmış bıraktıkları yapı taşlarını görebilirler. **Not:** **Kullanıma Alınan Maddeler** iletişim kutusunu kullanarak yapı taşlarını denetlemek için yönetici rolüne sahip olmanız gerekir.
1.  Rapor Tasarımcısı'nda, **Araçlar** menüsünde, **Kullanıma Alınan Maddeler**'e tıklayın.
2.  **Kullanıma Alınan Maddeler** iletişim kutusunda, **Tüm kullanıcılara ait maddeleri göster**'i seçin. Liste kullanıma alının tüm yapı taşlarını ve bunları kullanıma alan kullanıcıları gösterecek şekilde güncelleştirilir.
3.  Bir yapı taşı seçin ve ardından **Etkinliği Geri Al** öğesini tıklayın.
4.  Yapı taşını kullanıma sokmak için **Evet** öğesini tıklayın.

# <a name="see-also"></a>Ayrıca bkz.

[Mali raporlama](financial-reporting-intro.md)




