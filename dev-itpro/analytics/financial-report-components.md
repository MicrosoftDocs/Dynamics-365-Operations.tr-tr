---
title: "Mali rapor bileşenleri"
description: "Bu makalede rapor tanımlarının bileşenlerinin veya yapı taşlarının finansal raporlamada nasıl kullanıldığı açıklanmaktadır. Bu yapı taşları satır tanımlarını, sütun tanımlarını ve raporlama ağacı tanımlarını içerir. Bu makalede yapı taşlarının nasıl düzenleneceği ve kilitleneceği ve yapı taşı grupları ile nasıl çalışılacağı açıklanmaktadır."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18 - 54 - 02
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: a423dff4d8796f454c9c4db03c8ceb2b8c3d6456
ms.lasthandoff: 03/30/2017


---

# <a name="financial-report-components"></a>Mali rapor bileşenleri

Bu makalede rapor tanımlarının bileşenlerinin veya yapı taşlarının finansal raporlamada nasıl kullanıldığı açıklanmaktadır. Bu yapı taşları satır tanımlarını, sütun tanımlarını ve raporlama ağacı tanımlarını içerir. Bu makalede yapı taşlarının nasıl düzenleneceği ve kilitleneceği ve yapı taşı grupları ile nasıl çalışılacağı açıklanmaktadır. 

Finansal rapor tasarımcısının ardında yatan tasarım felsefesi bilgiyi en küçük bileşenlerine veya yapı taşlarına ayırmak ve bileşenleri gerektiği gibi karıştırıp eşleştirmektir. Bu nedenle, rapor biçimlendirmeniz finansal verilerinizden ayrıdır ve bir raporun tasarımını Microsoft Dynamics ERP sistemindeki finansal verilerinizi etkilemeden değiştirebilirsiniz. Bu yapı taşı yaklaşımını kullanarak metin, tutarlar ve hesaplamaları birleştirerek ihtiyacınız olan raporları oluşturabilirsiniz. Ayrıca, bu esneklik, operasyonlarınızı farklı şekillerde görüntülemenizi kolaylaştırarak yaratıcılığı da teşvik eder. Bir rapor tanımının ayrı yapı taşları, üç boyutlu bir elektronik tabloya oldukça benzerdir, ancak daha güçlü özellikler barındırır. Bir rapor tanımı rapor için kullanılması gereken satır tanımını, sütun tanımını ve opsiyonel raporlama ağacı tanımını belirler. Ayrıca, oluşturulan raporun nerede saklanacağı ve bunun nasıl biçimlendirileceği hakkında bilgiler de içerir. Tekrar kullanım ve paylaşım kolaylığı için, bir şirketle bağlantılı olan mevcut rapor tanımları, satır tanımları, sütun tanımları, raporlama ağacı tanımları ve boyut kümelerinin bir birleşimi olan bir yapı taşı grubu oluşturabilirsiniz.

## <a name="building-blocks-of-a-report"></a> Bir raporun yapı taşları
| Yapı taşı            | Açıklama                                                                                                                                                                                                                                                                              | Daha fazla bilgi için                                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Satır tanımı            | Bir satır tanımı bir rapordaki açıklayıcı satırları (örneğin maaşları veya satışları) tanımlar. Ayrıca, segment değerlerini ve her bir satır maddesi için değerleri ve satır biçimlendirmesini ve hesaplamalarını içeren boyutları listeler.                                                    | [Satır tanımları](row-definitions-financial-reporting.md)                       |
| Sütun tanımı         | Bir sütun tanımı, verilerin mali boyutlardan çekilmesi sırasında kullanılacak dönemi tanımlar. Ayrıca, sütun biçimlendirmeyi ve hesaplamalarını içerir.                                                                                                                                 | [Sütun tanımları](column-definitions-financial-reports.md)         |
| Raporlama ağacı tanımı | Bir raporlama ağaç tanımı bir organizasyon çizelgesine benzer. Çizelgedeki her bir kutuyu temsil eden ayrı raporlama birimleri içerir. Birimler, mali verilerden çekilen ayrı departmanlar veya diğer raporlama birimlerinden gelen verileri özetleyen, yüksek düzeyli birimler olabilir. | [Raporlama ağacı tanımları](financial-reporting-tree-definitions.md) |
| Rapor tanımı         | Bir rapor tanımı bir rapor oluşturmak üzere bir satır tanımı, bir sütun tanımı ve bir opsiyonel raporlama ağacı tanımı kullanır. Ayrıca, bir raporunun özelleştirilmesi için kullanabileceğiniz ilave seçenekler ve ayarlar sağlar.                                                                    | [Rapor tanımı](design-financial-report-definitions.md)                  |

Rapor tasarımında yeniyseniz, daha sonra özelleştirebileceğiniz bir rapor tanımını kısa sürede oluşturmak için rapor sihirbazını kullanışlı bulabilirsiniz. Rapor tasarımında deneyimliyseniz ve rapor tasarımı için daha fazla esneklik istiyorsanız, yeni bir rapor tanımı oluşturmak için yeni veya mevcut yapı taşlarını birleştirebilirsiniz. Kaliteli raporlar üretmek için kullanılabilen tüm rapor tanımı seçeneklerini tamamen anlamak zorunda değilsiniz. Rapor tasarımına alıştıkça, daha gelişmiş özelliklerden yararlanmak üzere rapor tanımlarınızı genişletebilirsiniz. Bir temel rapor oluşturduktan sonra rapor tanımını ve rapor tanımındaki yapı taşlarından herhangi birini özelleştirebilirsiniz.

## <a name="organize-the-building-blocks"></a>Yapı taşlarını düzenleme
Rapor Tasarımcısında yapı taşlarını düzenlemek için klasörleri kullanın. Tüm klasörler, içerdikleri yapı taşı türüne özgüdür. Örneğin, satır tanımlarını içeren tüm klasörler Rapor Tasarımcısının **Satır Tanımları** bölmesinde bulunur.

### <a name="create-a-folder"></a>Klasör oluşturma

1.  Rapor Tasarımcısında, gezinti bölmesinde düzenlemek üzere yapı taşı türünü seçin. Örneğin, bir satır tanımını sıralamak için **Satır Tanımları** öğesini tıklayın.
2.  Gezinti bölmesinde, altında yeni klasörün oluşturulacağı mevcut klasörü seçin ve aşağıdaki adımlardan birini izleyin:
    -   Ana klasörü sağ tıklayın ve **Yeni Klasör** öğesine tıklayın.
    -   Ana klasörü seçin, **Dosya** düğmesine ve ardından **Yeni Klasör** öğesine tıklayın.

3.  Yeni klasör görüntülendiğinde yeni klasörün adını girin ve Enter tuşuna basın.

## <a name="lock-a-building-block"></a> Bir yapı taşını kilitleme
Bir yapı taşını kilitlemek ve korunmasına yardımcı olmak için bir parola oluşturabilirsiniz. Bu şekilde, tüm sistemi korumaya almanıza gerek kalmaksızın bir rapor bileşenine bir güvenlik seviyesi ekleyebilirsiniz. Parola ay sonu raporlama süreciniz açısından önem taşıyan yapı taşı bilgilerinin korunmasına yardımcı olabilir. Bir yapı taşını tüm rollerdeki kullanıcılar kilitleyebilir. Ancak diğer kullanıcıların kilitli bir bileşen için her zaman salt okunur erişimi olmalıdır. Kullanıcılar kilitli bir bileşeni açabilir, değiştirebilir ve başka bir adla kaydedebilir. Yönetici rolüne sahip bir kullanıcı her zaman kilitli bir yapı taşına erişebilir ve bunu değiştirebilir.
1.  Rapor Tasarımcısında kilitlenecek rapor bileşenini, örneğin bir satır tanımını, sütun tanımını, rapor tanımını veya raporlama ağacı tanımını açın.
2.  **Araçlar** menüsünde **Koru/Korumayı Kaldır** öğesine tıklayın. Ayrıca, araç çubuğundaki **Koru/Korumayı Kaldır** (kilit simgesi) öğesine de tıklayabilirsiniz.
3.  **Koru** iletişim kutusunda parolayı girip onaylayın ve ardından **Tamam**'a tıklayın. Araç çubuğundaki kilit simgesi, bir açık yapı taşı kilitlendiğinde vurgulanır.

Kilitli bir yapı taşının kilidini açmak için, yapı taşını açın ve ardından araç çubuğundaki **Koru/Korumayı Kaldır** öğesine tıklayın. Alternatif olarak, **Araçlar** menüsünde **Koru/Korumayı Kaldır** öğesine tıklayın.

## <a name="building-block-groups"></a>Yapı taşı grupları

Yapı taşları bir rapor için oluşturduğunuz satır tanımları, sütun tanımları, raporlama ağacı tanımları ve rapor tanımlarıdır. Yapı taşı grupları ise bir şirketle ilişkili tanımların ve boyut kümelerinin toplamıdır. Yapı taşı grupları bir şirkete özel olabilir veya birkaç şirket aynı yapı taşı kümesini paylaşabilir. Şirketlerinizden bazıları farklı hesap planlarına sahipse her bir şirket için farklı bir yapı taşı grubu kullanmak isteyebilirsiniz. Alternatif olarak, hangi şirketle uyumlu olduğunu göstermesi için tüm ayrı yapı taşlarınızı adlandırmak isteyebilirsiniz.
### <a name="create-a-building-block-group"></a>Bir yapı taşı grubu oluşturma

1.  Rapor Tasarımcısında, **Şirket** menüsündeki **Yapı taşı grupları** öğesine tıklayın.
2.  **Yapı taşı grupları** iletişim kutusunda **Yeni** öğesine tıklayın.
3.  Yapı taşı grubu için özgün bir ad ve açıklama girin. Her alan en çok 256 karakter içerebilir. (Bu sayı boşlukları da içerir.)
4.  Yeni yapı taşı grubunu oluşturmak için **Tamam** öğesine tıklayın.

### <a name="assign-a-building-block-group"></a>Bir yapı taşı grubu atama

Blok grubu oluşturduktan sonra, bunu en az bir şirkete atamanız gerekir. Rapor, satır, sütun ve raporlama ağacı tanımları oluşturabilir ve bunları yapı taşı grubuna kaydedebilirsiniz. Aşağıdaki prosedüre geçmeden önce tüm yapı taşı bloklarını kapatmalısınız.
1.  Rapor Tasarımcısında **Şirket** menüsündeki **Şirketler** öğesini tıklayın.
2.  **Şirketler** iletişim kutusunda, bir yapı taşı bloğunun atanacağı şirketi seçin.
3.  **Değiştir** öğesini tıklayın.
4.  **Şirketi Değiştir** iletişim kutusunda **Yapı taşı grubu** alanında, şirkete atanacak yapı taşı grubunu seçin veya yeni bir yapı taşı grubu oluşturmak için **Yeni** öğesini tıklayın.
5.  Yapı taşı grubunu atamak için **Tamam** öğesini tıklayın.
6.  **Şirketler** iletişim kutusunu kapatmak için **Kapat** öğesine tıklayın. Seçtiğiniz yapı taşı grubu şimdi şirkete atanır. Artık, oluşturulan tüm yeni satır tanımları, sütun tanımları vb. satır tanımları, bu şirkete atanan yapı taşı grubunun bir parçası olacaktır. Ayrıca, başka bir sistemden bir .tdbx dosyası veya rapor atayabilirsiniz.

### <a name="view-a-building-block-group"></a> Bir yapı taşı grubunu görüntüleme

Bir yapı taşı grubu oluşturulduktan ve kullanılmaya başladıktan sonra, bu gruba atanan tüm yapı taşlarını görüntüleyebilirsiniz. Ayrıca bir yapı taşı grubunu dışa veya içe aktarabilir ve yapı taşı grupları üzerinde ek bakım işlemleri gerçekleştirebilirsiniz.
1.  Rapor Tasarımcısında, **Şirket** menüsündeki **Yapı Taşı Grupları** öğesini tıklayın.
2.  **Yapı Taşı Grupları** iletişim kutusunda, görüntülenecek yapı taşını seçin.
3.  **Görünüm** öğesine tıklayarak yapı taşı grubunun içeriğini görüntüleyebileceğiniz **Yap Taşı Grubunu Göster** iletişim kutusunu açın.
4.  İletişim kutularını kapatmak için **Kapat** öğesini tıklayın.

### <a name="save-a-building-block-group-under-a-new-name"></a>Yeni bir ad ile bir yapı taşı grubunu kaydetme

Mevcut bir yapı taşı grubunu yeni bir ad ile kaydedebilirsiniz. Ardından, orijinal yapı taşı bloğunu değiştirmeden yeni yapı taşı grubunu değiştirebilirsiniz.
1.  Rapor Tasarımcısında, **Şirket** menüsündeki **Yapı Taşı Grupları** öğesini tıklayın.
2.  **Yapı Taşı Grupları** iletişim kutusunda, yeni bir adla kaydedilecek yapı taşı grubunu seçin.
3.  **Farklı Kaydet** öğesini tıklayın.
4.  Yapı taşı grubu için yeni bir ad ve açıklama girin.
5.  **Tamam** düğmesini tıklatın. Yeni yapı taşı grubu, **Yapı Taşı Grupları** iletişim kutusunda görüntülenecektir.

### <a name="export-a-building-block-group"></a> Bir yapı taşı grubunu dışa aktarma

Bir yapı taşını grubu veya bir yapı taşı grubunda belirli rapor yapı taşları verebilirsiniz. Yedek olarak verilen yapı taşı grubu kullanabilirsiniz. Yapı Taşı grupları veya Dynamics 365 arasında verilen veri işlemleri yüklemeler için de kopyalayabilirsiniz. Yapı Taşı grubu ile birlikte boyut kümeleri ve Rapor Tasarımcısı başvurulan yazı tipi stilleri içerir.
1.  Rapor Tasarımcısında, **Şirket** menüsündeki **Yapı Taşı Grupları** öğesini tıklayın.
2.  **Yapı Taşı Grupları** iletişim kutusunda, dışa aktarılacak yapı taşı grubunu seçin ve ardından **Dışa Aktar** öğesini tıklayın.
3.  **Dışa Aktar** iletişim kutusunda, dışa aktarılacak rapor tanımlarını seçin:
    -   Tüm rapor tanımlarını ve ilgili yapı taşlarını dışa aktarmak için **Tümünü Seç** öğesini tıklayın.
    -   Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini dışa aktarmak için ilgili sekmeye tıklayın ve ardından dışa aktarılacak maddeleri seçin. Bir sekmede birden fazla madde seçmek için CTRL tuşunu basılı tutun. **Not:** Dışa aktarılacak raporları seçtiğinizde ilişkili satırlar, sütunlar, ağaçlar ve boyut kümeleri seçilir.

4.  Dışa aktarılacak öğeleri seçmeyi bitirdiğinizde **Dışa Aktar** öğesine tıklayın.
5.  **Farklı Kaydet** iletişim kutusunda, yapı taşının dışa aktarılacağı konumu seçin.
6.  **Dosya Adı** alanına dosya için bir ad girin. Rapor tasarımcısı otomatik olarak bir .tdbx dosya adı uzantısı ekler.
7.  **Kaydet**'i tıklatın. Yapı taşı grubu, belirttiğiniz konuma kaydedilir.

### <a name="import-a-building-block-group"></a> Bir yapı taşı grubunu içe aktarma

Bir yapı taşı grubunu mevcut bir yapı taşı grubuna içe aktarabilir veya veriler için yeni bir yapı taşı grubu oluşturabilirsiniz. İçe aktarılan tüm yapı taşı grupları orijinal yazı tipi stillerini ve şirket başvurularını korur ve ilgili boyut kümelerini içerir.
1.  Rapor Tasarımcısında, **Şirket** menüsündeki **Yapı Taşı Grupları** öğesini tıklayın.
2.  **Yapı Taşı Grupları** iletişim kutusunda, bir yapı taşı grubunun aktarılacağı yapı taşını seçin ve ardından **İçe Aktar** öğesini tıklayın.
3.  **Aç** iletişim kutusunda, içe aktarılacak yapı taşı grubunu seçin ve ardından **Aç** öğesini tıklayın.
4.  **İçe Aktar** iletişim kutusunda, içe aktarılacak rapor tanımlarını seçin:
    -   Rapor tanımlarının ve destekleyici yapı taşlarının tümünü içe aktarmak için **Tümünü Seç** öğesine tıklayın.
    -   Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini içe aktarmak için, içe aktarılacak raporları, satırları, sütunları, ağaçları veya boyut kümelerini seçin.

5.  İçe aktarılacak öğeleri seçmeyi bitirdiğinizde **İçe Aktar** öğesine tıklayın.

### <a name="undo-a-checkout-of-a-building-block"></a>Bir yapı taşının etkinliğini geri alma

Bir yapı taşını açtığınızda, diğer kullanıcılar bu yapı taşına yalnızca salt okunur erişime sahip olur. Bazen kullanıcılar bir yapı taşını kapatmayı unutur veya yapı taşını kapatmadan sistemini kapatabilirler. Bu nedenle, yapı taşı etkin kalır ve diğer kullanıcılar bu yapı taşını açamaz. Bu gibi durumlarda, bir finansal raporlama yöneticisi **Etkin Maddeler** iletişim kutusunu kullanarak kullanıcıların etkin bıraktığı yapı taşlarını kullanıma açabilir. **Not:** Yapı taşlarını **Etkin Maddeler** iletişim kutusu ile kullanıma açabilmek için yönetici yetkisine sahip olmanız gerekir.
1.  Rapor Tasarımcısında **Araçlar** menüsündeki **Etkin Maddeler** öğesini tıklayın.
2.  **Etkin Maddeler** iletişim kutusunda **Tüm kullanıcıların maddelerini göster** öğesini seçin. Liste, etkin konumdaki tüm yapı taşlarını ve bu yapı taşlarını etkinleştiren kullanıcıları görüntüleyecek şekilde güncelleştirilir.
3.  Bir yapı taşı seçin ve ardından **Etkinliği Geri Al** öğesini tıklayın.
4.  Yapı taşını kullanıma sokmak için **Evet** öğesini tıklayın.

# <a name="see-also"></a>Ayrıca bkz.

[Microsoft Dynamics ERP için finansal raporlama](financial-reporting-intro.md)


