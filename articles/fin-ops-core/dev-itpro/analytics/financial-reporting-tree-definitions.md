---
title: Mali raporlarda raporlama ağacı tanımları
description: Bu makalede raporlama ağacı tanımları açıklanmaktadır. Raporlama ağacı tanımı, kuruluşun yapısını tanımlayan bir rapor bileşenidir.
author: jinniew
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 92da476f64b937d339b5f0c6088b8ce722a0584938ccf2a6c6cbd39fdc15544d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714647"
---
# <a name="reporting-tree-definitions-in-financial-reports"></a>Mali raporlarda raporlama ağacı tanımları

[!include [banner](../includes/banner.md)]

Bu makalede raporlama ağacı tanımları hakkında bilgi verilmektedir. Raporlama ağacı tanımı, kuruluşunuzun yapısı ve hiyerarşisini tanımlamaya yardımcı olan bir rapor bileşeni veya yapı taşıdır.

Mali raporlama, iş yapınız değiştikçe kolaylıkla değişiklik yapabilmeniz için esnek raporlamayı destekler. Raporlar çeşitli bileşenlerden veya yapı taşlarından oluşturulur. Bu yapı taşlarından biri raporlama ağaç tanımıdır. Raporlama ağacı tanımı kuruluşunuzun yapısı ve hiyerarşisini tanımlamaya yardımcı olur. Mali verilerinizde boyutlu ilişkilere dayanan çapraz boyutlu hiyerarşik bir yapıdır. Ağaçtaki tüm birimler için raporlama birimi düzeyinde ve özet düzeyinde bilgi sağlar. Raporlama ağacı tanımları, birden çok şirket tarafından kullanılabilen bir yapı taşı grubu oluşturmak için sütün tanımları ve rapor tanımları ile birleştirilebilir. Raporlama birimi bir kuruluş şemasındaki her bir kutu için kullanılır. Bir raporlama birimi mali verilerdeki tek bir departman veya diğer raporlama birimlerindeki bilgileri birleştiren üst düzey bir özet birimi olabilir. Raporlama ağacı içeren bir rapor tanımı için, her özet düzeyi ve raporlama birimi için bir rapor oluşturulur. Rapor tanımı satır tanımından raporlama ağacının kullanılması gerektiğini belirtmediği sürece, tüm bu raporlar rapor tanımında belirtilen satır ve sütun tanımlarını kullanır. Satır ve sütun tanımları, tasarım ve mali raporlar işlevselliğinin önemli bileşenleridir. Raporlama ağaçları bileşenleri gücünü artırır ve iş yapısı değiştikçe esnek raporlamayı destekler. Raporlama ağacına dayalı olmayan mali raporlar, mali raporlama özelliklerinin yalnızca bir bölümünü kullanır. Kuruluşunuzun verilerini farklı yollarla görüntülemek için aynı satır ve sütun tanımları ile birlikte birden çok raporlama ağacı tanımı kullanabilirsiniz.

## <a name="reporting-tree-best-practices"></a>Raporlama ağacıyla ilgili en iyi uygulamalar
Bir raporlama ağacı oluşturmadan önce aşağıdaki en iyi uygulamaları dikkate alın:

- Önce tüzel kişilik veya şirketinizin hangi raporlama boyutlarını gerektirdiğini belirleyin.
- Yapınızı nasıl kurduğunuzu düşünün ve ardından şirketinizin kuruluş şemasını çizin. Kuruluş şeması, raporlama birimlerini nasıl bir veya daha fazla raporlama ağacı halinde gruplandıracağınızı görselleştirmenize yardımcı olur.
- Departmanlar ve mali verilerde tanımlı projeler gibi detayların en düşük düzeyi ile başlayın. Daha yüksek düzeyli bölümler veya bölgeler göstermek için ayrıntı düzeyinde olabildiğince çok kutuyu gereken şekilde ekleyin. Her kutu, oluşturduğunuz herhangi bir raporlama ağacında olası bir raporlama birimini temsil eder.
- Ağaçları oluşturmak için en iyi yolu dikkate almanız gerekir. Raporlama ağacı oluşturmak için otomatik yapılandırma işlemini kullanabilir veya elle bir raporlama ağacı oluşturabilirsiniz. Ağaçlarınızı tasarlamadan önce her iki yöntemi de anlamanız önemlidir.
- Raporlama birimlerini raporlama ağacı tanımına eklemek için mali veriler sistemi içinde tanımlanan raporlama birimlerini kullanabilirsiniz.

## <a name="create-multiple-reporting-trees"></a> Birden fazla raporlama ağacı oluşturma
Kuruluşunuzun verilerini farklı yollarla görüntülemek için sınırsız sayıda raporlama ağacı oluşturabilirsiniz. Her raporlama ağacı herhangi bir departman ve özet birimi birleşimini içerebilir. Bir rapor tanımı bir seferde yalnızca bir adet raporlama ağacı bağlantısı içerebilir. Raporlama birimleri yapısını yeniden düzenleyerek, farklı raporlama ağaçları oluşturabilirsiniz. Daha sonra her bir raporlama ağacı için aynı satır ve sütun tanımlarını kullanabilirsiniz. Bu şekilde, farklı mali rapor düzenlerini hızlı bir şekilde oluşturabilirsiniz. Birden fazla raporlama ağacı oluşturursanız şirketinizin operasyonlarını analiz eden ve çeşitli şekillerde sunan bir dizi mali tabloyu her ay yazdırabilirsiniz. Daha fazla bilgi için bu makalenin sonundaki raporlama birimi yapıları örneklerine bakın.

## <a name="create-a-reporting-tree-definition"></a> Bir raporlama ağacı tanımı oluşturma
Raporlama ağacı tanımı aşağıdaki tabloda açıklanan sütunları içerir.

| Raporlama ağacı sütunu | Tanım |
|-----------------------|-------------|
| Şirket               | Raporlama birimi için şirket adı. Genellikle yalnızca özet düzeyine atanan **\@ANY** değeri tüm şirketler için kullanılabilecek raporlama ağacını etkinleştirir. Tüm alt şubelerin kendilerine atanmış bir şirketi vardır. |
| Birim Adı             | Bu raporlama birimini grafiksel raporlama ağacında tanımlayan kod. Tutarlı ve kullanıcılar için anlaşılması kolay olacak benzersiz bir kodlama sistemi kurduğunuzdan emin olun. |
| Birim Açıklama      | Raporlama birimi başlığı, rapor tanımı **Üstbilgiler ve Altbilgiler** sekmesinin bir kodu olarak **UnitDesc** girerseniz rapor üst bilgisinde veya alt bilgisinde görüntülenir. Satır tanımının **Açıklama** hücresine **UnitDesc** ifadesini girerseniz başlık rapor satırı açıklamasında görünür. |
| Boyutlar            | Doğrudan mali verilerden bilgi alan bir raporlama birimi. Hesap ve ilgili segmentler için mantıksal konumlandırmayı ve uzunlukları tanımlar. Her bir raporlama birimi satırı bu sütunda bir boyuta sahip olmalıdır. Özet birimi satırına bir boyut da yerleştirebilirsiniz (örneğin, bu birimle doğrudan ilgili giderler için). Özet birimi satırına boyut girerseniz üst birimlerde kullanılan hesaplar alt birimlerde kullanılmamalıdır. Aksi halde, tutarlar yinelenebilir. |
| Satır Tanımları       | Raporlama birimi için satır tanımı adı. Aynı satır tanımı raporlama ağacının her birimi için kullanılır. Rapor oluşturduğunuzda, bu satır tanımı her bir raporlama birimi için kullanılır. Satır tanımı birden fazla mali boyut bağlantısı içerebilir. Satır tanımı raporlama ağacında belirtilmişse rapor tanımının **Rapor** sekmesindeki **Raporlama ağacındaki satır tanımını kullan** onay kutusunu işaretleyin. |
| Mali Boyutlar bağlantısı| Raporlama birimi için kullanılacak mali boyutlar bağlantısı. Bağlantı verilecek mali boyutları tanımlamak üzere satır tanımı için mali boyut bağlantıları tanımlanır. |
| Sayfa Seçenekleri          | Bu sütun, rapor görüntülendiğinde veya yazdırıldığında raporlama birimi ayrıntılarının gizlenip gizlenmediğini denetler. |
| Toplama %              | Ana birime tahsis edilmesi gereken raporlama biriminin yüzdesi. Bu sütuna girdiğiniz yüzde, satır değeri üst rapora eklenmeden önce satır tanımının her satırı için geçerlidir. Örneğin, alt birimin iki bölüm arasında eşit olarak bölünmesi gerekiyorsa değer departman raporuna eklenmeden önce her satırdaki tutarlar yüzde 50 ile çarpılır. Bir raporlama birimi iki ana birime sahip olamaz. Bir raporlama biriminden gelen tutarları iki ana birime tahsis etmek için ek yüzde 50 toplanacak aynı boyuta sahip başka bir raporlama birimi oluşturun. Tam yüzdeleri ondalık basamak olmadan girin. Örneğin, **25** ana birime yüzde 25 tahsisi temsil eder. Ondalık değer (**0,25**) eklerseniz ana birime yüzde 0,25 tahsis edilir. Yüzde 1'den küçük bir yüzde kullanmak için rapor tanımında **&lt;%1 Toplamaya İzin Ver** seçeneğini kullanın. Bu seçenek, **rapor ayarları** iletişim kutusu **Ek Seçenekler** sekmesinde bulunur. Bu iletişim kutusuna rapor tanımının **Ayarlar** sekmesindeki **Diğer** düğmesinden erişebilirsiniz. |
| Birim Güvenliği         | Raporlama biriminin bilgilerine erişebilen kullanıcılar ve gruplar üzerindeki kısıtlamalar. |
| Ek Metin       | Bu rapora dahil edilen metin. |

Raporlama ağacı tanımı oluşturmak için aşağıdaki adımları izleyin.

1. Rapor Tasarımcısını açın.
2. **Dosya** &gt; **Yeni** &gt; **Raporlama Ağacı Tanımı** seçeneğine tıklayın.
3. **Düzenle** &gt; **Boyutlardan Raporlama Birimleri Ekle** seçeneğine tıklayın.
4. **Boyutlardan Raporlama Birimi Ekle** onay kutusunda raporlama ağacına eklemek her boyut için iletişim kutusunu seçin. **Boyutlardan Raporlama Birimleri Ekle** iletişim kutusu aşağıdaki bölümleri içerir.

    | Bölüm                          | Açıklama |
    |----------------------------------|-------------|
    | Raporlama boyutu segmentasyonu | Parçaların sayısı ve uzunluğunu değiştirmek için **Parçaları Böl** ve **Parçaları Birleştir** düğmelerini kullanın.<blockquote>[!NOTE] Yalnızca böldüğünüz segmentleri birleştirebilirsiniz. Birden fazla boyutu birleştirmek için, boyut değerlerinizde joker karakterler kullanın.</blockquote> |
    | Dahil et/Karakter konumu       | Bu bölümde mali verilerde tanımlanan boyutlar listelenir ve her boyut için tanımlanmış en uzun değerde karakter sayısı gösterilir. Raporlama ağacı hiyerarşisine bu boyutu eklemek için boyutun onay kutusunu seçin. |
    | Parça hiyerarşisi ve aralıkları     | Bu bölümde boyut hiyerarşisi gösterilir. Boyutları raporlama sıralamalarını değiştirmek için listede taşıyabilirsiniz. **Kaynak Boyut** ve **Hedef Boyut** alanlarında, her bir boyutta bir değer aralığı belirtebilirsiniz. Bir aralık belirlemezseniz tüm boyut değerleri raporlama ağacına eklenir.<blockquote>[!NOTE] Birden fazla boyut kullanıyorsanız yalnızca deftere nakledilen boyut birleşimleri sonuçlara döndürülür.</blockquote> |

    **Boyutlardan Raporlama Birimleri Ekle** iletişim kutusu örneğini gösteren bir resim için bu makalenin ilerleyen bölümlerinde yer alan "Boyutlardan Raporlama Birimleri Ekle iletişim kutusu örneği" bölümüne bakın.

5. Ek parçalar oluşturmak (örneğin, bir parçayı iki kısa parçaya bölmek) için **Karakter konumu** alanında doğru konuma tıklayın ve ardından **Parçaları Böl** seçeneğine tıklayın.
6. İki parçayı bir parçada birleştirmek için parça kutularından birine tıklayarak birleştirin ve sonra **Parçaları Birleştir** seçeneğine tıklayın.
7. Hiyerarşi, boyutların birbirleriyle nasıl rapor verdiğini ve her boyut için aralığı tanımlar. **Parça hiyerarşisi ve aralıklar** alanında boyutların hiyerarşisini değiştirmek için taşınacak boyutu seçin ve sonra **Yukarı Taşı** veya **Aşağı Taşı** seçeneğine tıklayın.
8. Yeni raporlama ağacına eklenecek bir boyut aralığı belirtmek için **Parça hiyerarşisi ve aralıklar** alanında, aşağıdaki adımları izleyin:

    1. İlgili boyut için **Kaynak boyut** alanına, aralıktaki ilk değeri girin.
    2. **Hedef Boyut** alanına, aralıktaki son değeri girin.

9. **Parça hiyerarşisi ve aralıkları** alanındaki her bir boyut için 7. ve 8. adımları yineleyin.
10. Raporlama birimlerinizin yeni raporlama ağacına nasıl getirilmesi gerektiğini tanımlamayı bitirdikten sonra **Tamam** seçeneğine tıklayın.
11. Raporlama ağacını kaydetmek için **Dosya** &gt; **Kaydet** seçeneğine tıklayın. Benzersiz bir ad ve raporlama ağacı için açıklama girin ve ardından **Tamam** seçeneğine tıklayın.

### <a name="open-an-existing-reporting-tree-definition"></a>Var olan bir raporlama ağacı tanımını açma

1. Rapor Tasarımcısı'nda gezinme bölmesinde **Raporlama Ağaç Tanımları** seçeneğine tıklayın.
2. Açmak için raporlama ağaç listesinden bir adı çift tıklatın.
3. Raporlama ağaç ile ilişkili olan tüm yapı taşlarını görüntülemek için raporlama ağaç tanımına sağ tıklayın ve sonra **İlişkiler** seçeneğini seçin.

### <a name="roll-up-data-in-a-reporting-tree"></a>Raporlama ağacında veri topla

Raporlama ağacı kullandığınızda, alt raporlama birimlerinden gelen tutarları üst raporlama birimi düzeyinde toplayabilirsiniz. Bu toplama verilerin toplanması denir. Raporlama ağacında üst birimlere tutarları toplamak için aşağıdaki kurallar kullanılır:

- Raporlama ağacı tek düzeyli ağaç olmadığı sürece bir raporlama ağacındaki alt birimler boyutları içermelidir. Üst birimler raporlama ağacındaki boyutları genellikle içermez.

    > [!NOTE]
    > Alt birimler ve ana birimler için boyutları belirtirseniz raporda verilerin yinelenmesine neden olabilirsiniz.

- Raporlama ağacında boyutları içeren raporlama birimleri, satır ve sütun tanımlarında kullanılan boyutlara karşılık gelir. Boyutların birleşimi, o birim için iade edilen tutarları belirler. Örneğin, bu makalenin sonraki bölümünde verilen örnek 2'de satır 6 ve 7 sırasıyla sadece departman 00 ve 01 için değerleri döndürür.
- Raporlama ağacında boyutları içermeyen üst raporlama birimleri için tutarlar alt birim raporundan belirlenir ve tutarı belirtilen üst birime toplar. Örneğin, üst birimin (bkz. veri toplama örneklerindeki örnek 2'de Contoso ABD) iki alt birimi (022 ve 023) varsa ve boyutlar içermiyorsa her alt ve üst öğe için bir rapor oluşturulur. İki alt tutarın toplamı üst toplamıdır.

### <a name="manage-reporting-units"></a>Raporlama birimlerini yönetin

Her bir raporlama ağacı tanımı benzersiz görünümlerde görüntülenir. Üst/alt hiyerarşisini gösteren bir grafik görünümü ve her raporlama birimi için belirli bilgileri gösteren bir çalışma sayfası görünümü vardır. Grafik ve çalışma sayfası görünümleri bağlıdır. Raporlama birimi bir görünümde seçildiğinde aynı zamanda diğer görünümde de seçilir. Mali verilerde boyutlu ilişkilere bağlı çapraz boyut hiyerarşileri oluşturabilirsiniz. Raporlama ağacı tanımı oluşturduğunuzda, bir departmana ait gelir tablosu veya bir konsolide özet gelir tablosu oluştursanız da aynı satır tanımlarını birden çok kez kullanabilirsiniz. Satır tanımı içinde tanımlanan boyutlar kuruluşunuzun performansının çeşitli görünümlerini sağlamak için raporlama ağacı tanımında boyutlar ile birleştirilebilir.

### <a name="reporting-unit-structure"></a>Raporlama birim yapısı

Raporlama birimlerinin aşağıdaki türleri mali raporlamada kullanılır:

- Doğrudan mali verilerden bilgi alan bir ayrıntı birimi.
- Özet birim alt düzey birimlerindeki verileri özetler.

Üst raporlama birimi, ayrıntı biriminden özetlenmiş bilgiler toplayan bir özet birimidir. Özet birimi bir ayrıntı birimi ve bir özet birimi olabilir. Bu nedenle, özet birimi bilgileri bir alt düzey birimden veya mali verilerden çekebilir. Ana birim daha yüksek düzeyde bir ana birimin alt birimi olabilir. Alt raporlama birimi bilgileri doğrudan mali verilerden çeken bir ayrıntı birimi olabilir. Alt raporlama birimi bir ara özet birimi de olabilir. Başka bir deyişle, bir alt düzey birimin ana birimi ve bir üst düzey özet biriminin alt birimi de olabilir. Raporlama birimleri için en yaygın senaryoda ana birimler **Boyutlar** sütununda boş bir hücreye sahiptir ve alt birimler belirli veya joker boyut birleşimlerine bağlantılar içerir.

### <a name="organize-reporting-units"></a>Raporlama birimlerini düzenlemek

Grafiksel görünümde raporlama birimlerini taşıyarak bir raporlama ağacı tanımının kuruluş yapısını yeniden düzenleyebilirsiniz. Ayrıca raporlama birimlerini raporlama ağacında üst bir düzeye yükseltebilir ve daha düşük bir düzeye indirebilirsiniz.

1. Rapor Tasarımcısı'nda raporlama ağaç tanımını değiştirmek için açın.
2. Raporlama ağacı tanımı grafik görünümünde bir raporlama birimi seçin.
3. Birimi yeni bir konuma sürükleyin. Alternatif olarak, birime sağ tıklayın ve sonra **Raporlama Birimini Yükselt** veya **Raporlama Birimini İndirge** seçeneğini belirleyin.
4. Değişikliklerinizi kaydetmek için **Dosya** &gt; **Kaydet** seçeneğine tıklayın.

### <a name="add-text-about-a-reporting-unit"></a>Raporlama birim hakkında metin ekleme

Ek metin girişi, raporlama ağacı tanımına bilgiler ekleyen 255 karaktere kadar bir statik metin dizesidir. Örneğin, ek metin kısa şirket açıklaması olabilir. Raporlama ağaç tanımındaki her raporlama birimi için en fazla on ek metin girişi oluşturabilirsiniz. Ek metin, metnin atandığı raporlama biriminin raporunda görünür. Satır tanımının **Açıklama** sütunundan ve rapor tanımındaki **Üstbilgiler ve Altbilgiler** sekmesinden metin girdilerini ekleyebilirsiniz.

1. Rapor Tasarımcısı'nda raporlama ağaç tanımını değiştirmek için açın.
2. Raporlama birimi satırı için **Ek Metin** hücresine çift tıklayın.
3. **Ek Metin** iletişim kutusunun ilk boş satırına metni girin. **Ek Metin** iletişim kutusundaki konumundan bağımsız olarak, metin içeren ilk satır UnitText1 olarak adlandırılır.
4. Bu raporlama birimine daha fazla metin girdileri eklemek için metni boş bir satıra girin.
5. **Tamam** düğmesini tıklatın.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Ek metni bir raporlama biriminden çıkarın

1. Rapor Tasarımcısı'nda, değiştirilecek raporlama ağacı tanımını açın.
2. Raporlama birimi satırı için **Ek Metin** hücresine çift tıklayın.
3. **Ek Metin** iletişim kutusunda, kaldırmak istediğiniz girişi seçin ve ardından **Temizle** seçeneğine tıklayın. Alternatif olarak, girişe sağ tıklayın ve sonra **Kes**'i seçin.
4. **Tamam** düğmesini tıklatın.

### <a name="restrict-access-to-a-reporting-unit"></a>Bir raporlama birimi için erişim sınırlama

Belirli kullanıcıların ve grupların bir raporlama birimine erişimini engelleyebilirsiniz. Raporlama biriminin alt raporlama birimleri için geçerli olacak şekilde kısıtlamalar da tanımlayabilirsiniz.

1. Rapor Tasarımcısı'nda raporlama ağaç tanımını değiştirmek için açın.
2. Erişimi kısıtlanacak raporlama birimi satırının **Birim Güvenliği** hücresine çift tıklayın.
3. **Birim Güvenlik** iletişim kutusunda, **kullanıcılar ve gruplar**'ı seçin.
4. Raporlama birimine erişimi olması gereken kullanıcıları veya grupları seçin ve sonra **Tamam**'a tıklayın.
5. Alt raporlama birimlerine erişimi kısıtlamak için **Alt raporlama birimlerine güvenlik ekle** onay kutusunu seçin.
6. **Tamam** düğmesini tıklatın.

### <a name="remove-access-to-a-reporting-unit"></a>Bir raporlama birimine erişimi kaldırma

1. Rapor Tasarımcısı'nda, değiştirilecek raporlama ağacı tanımını açın.
2. Erişimi kaldırılacak raporlama birimi satırı için **Birim Güvenliği** hücresine çift tıklayın.
3. **Birim Güvenliği** iletişim kutusunda bir ad seçin ve sonra **Kaldır**'a tıklayın.
4. **Tamam**'a tıklayın.

## <a name="examples"></a>Örnekler
### <a name="reporting-unit-structure--example-1"></a>Raporlama birimi yapısı: Örnek 1

Raporlama birimlerinin yapısı aşağıdaki raporlama ağacında verildiği gibidir:

- Contoso Japonya raporlama birimi, Contoso Japonya Satış ve Contoso Japonya Danışmanlık alt birimlerinin ana birimidir.
- Contoso Japonya Satış bölümü birimi hem Contoso Japonya biriminin alt birimi, hem de Yurtiçi Satış ve Otomatik Satış birimleri için bir ana birimdir.
- En düşük düzeydeki ayrıntı raporlama birimleri (Yurtiçi Satışlar, Otomatik Satışlar, Müşteri Hizmetleri ve Operasyonlar) departmanları mali verilerde temsil eder. Bu raporlama birimleri diyagram gölgeli alanındadır.
- Üst düzey özet birimleri ayrıntılı birim bilgilerini özetler.

[![Contoso Özet Rapor Yapısı - Örnek 1.](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Raporlama birimi yapısı: Örnek 2

Aşağıdaki diyagramda, raporlama ağacı iş işlevlerine göre ayrılmış bir organizasyon yapısına sahiptir.

[![Contoso Özet Rapor Yapısı - Örnek 2.](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Boyutlardan Raporlama Birimleri Ekle iletişim kutusu örneği

Aşağıdaki resim, **Boyutlardan Raporlama Birimleri Ekle** iletişim kutusunun bir örneğini göstermektedir. Bu örnekte, sonuçlar iş birimleri, maliyet merkezleri ve departmanların birleşimini döndürür.

[![Raporlama Birimleri Ekleme.](./media/insertreportingunits.png)](./media/insertreportingunits.png)

Sonuç olarak ortaya çıkan raporlama ağacı tanımı iş birimine, ardından maliyet merkezine ve sonra departmana göre sıralanır. Beşinci raporlama biriminin boyutu **İş Birimi = \[001\], Maliyet Merkezi =\[\], Departman = \[022\]** şeklindedir ve iş birimi 001 ve departman 022'ye özel hesaplar için bir raporlama birimini tanımlar.

[![Raporlama ağacının resmi.](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Veri toplama örnekleri

Aşağıdaki örnekler toplanan veriler için bir raporlama ağacı tanımında kullanılan olası bilgileri gösterir.

#### <a name="example-1"></a>Örnek 1

[![Çoklu şirket toplaması.](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>Örnek 2

[![Şirketler arası departman toplaması.](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Mali raporlama](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
