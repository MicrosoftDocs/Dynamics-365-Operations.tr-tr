---
title: Finansal rapor tasarımcısında satır tanımları
description: Satır tanımını finansal rapordaki her satırın içeriğini belirten bir rapor bileşeni veya yapı taşıdır.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e84f882f69fbc7fceae8a6e0332716a82830dfdc
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344060"
---
# <a name="row-definitions-in-financial-report-designer"></a>Finansal rapor tasarımcısında satır tanımları

[!include [banner](../includes/banner.md)]

Satır tanımını finansal rapordaki her satırın içeriğini belirten bir rapor bileşeni veya yapı taşıdır. Satır tanımı birden çok şirket tarafından kullanılabilen bir yapı taşı grubu oluşturmak için sütun tanımları, raporlama ağacı tanımları ve rapor tanımları ile birleştirilebilir.

## <a name="create-a-row-definition"></a>Satır tanımı oluşturma

1. Rapor Tasarımcısı'ndaki gezinti bölmesinde **Satır Tanımları**'na tıklayın.
2. **Dosya** menüsünde, **Yeni**'ye ve ardından **Satır Tanımı**'na tıklayın. Her hücrenin içeriği hakkında daha fazla bilgi için, bkz. [Satır tanımı hücrelerini değiştirme](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Bir satır tanımını açma
1. Rapor Tasarımcısı'ndaki gezinti bölmesinde **Satır Tanımları**'na tıklayın.
2. Açmak için satır tanımının adına çift tıklayın.
3. Satır tanımıyla ilişkili tüm yapı taşlarını görüntülemek için, satır tanımına sağ tıklayın ve ardından **İlişkiler**'i seçin.

## <a name="contents-of-a-row-definition"></a>Bir satır tanımının içerikleri
Bir satır tanımı en fazla 20.000 mali boyut içerebilir ve içinde aşağıdaki bilgiler bulunabilir:

- **Nakit** veya **Toplam Gelir** gibi bölüm başlıkları, satırlar ve alanlar oluşturarak rapora anlam ekleyen açıklayıcı metin
- Microsoft Dynamics 365 Finance'te boyut değerleri içerebilen finansal veri bağlantıları

    > [!NOTE]
    > Rapor her oluşturulduğunda mali boyutlar sisteminden verileri çekmek için bir satır tanımı ayarlayabilirsiniz.

- İlişkili mali verileri esas alan satır toplamları ve formüller

Genellikle, bir satır tanımındaki her satır aşağıdaki bilgi türlerinden birini içerir:

- Mali boyutlar sisteminin referansları
- Verileri esas alan toplamlar veya hesaplamalar
- Biçimlendirme

Bir satır tanımına bilgi girmek için iki yöntem vardır:

- Satır bilgilerini el ile yeni bir satır tanımına girin. Daha fazla bilgi için [Satır tanımı hücrelerini değiştirme](modify-row-definition-cells-financial-reporting.md) bölümüne bakın.
- Satır bilgilerini doğrudan finansal boyutlardan çekmek için rapor tasarımcısını kullanın. Daha fazla bilgi için, [Satır tanımı hücrelerini değiştirme](modify-row-definition-cells-financial-reporting.md) bölümündeki "İlgili formüller/satırlar/birimler" kısmına bakın.

## <a name="add-dimensions-in-a-row-definition"></a>Bir satır tanımına boyut ekleme
Bir boyut, veri ve değerlerin bir kesişimidir. Rapor tasarımcısında verileri ve değerleri gruplandırabilirsiniz. Ardından hareketleri sınıflandırabilir ve daha ayrıntılı şekilde çözümleyebilirsiniz. **Boyutlardan Satır Ekle** iletişim kutusunu kullanarak bir satır tanımına aynı anda birden fazla satır ekleyebilirsiniz. İletişim kutusu her boyut için bir sütun görüntüler. Aşağıdaki tabloda her boyut için belirtebileceğiniz bilgiler açıklanmaktadır.

| Seçenek                | Açıklama |
|-----------------------|-------------|
| Boyut             | Satır tanımına eklenecek boyutu tanımlayan model. Bu model, boyutlardaki her bir konum için bir ve işareti (&) veya rakam işareti (\#) içerir. Genellikle, Ana Hesap boyutu için tüm ve işaretlerini ve diğer boyutlar için tüm rakam işaretlerini kullanırsınız. |
| Boyut Aralığı Başlangıcı | Bu boyutun satır tanımına eklenecek ilk değeri. |
| Boyut Aralığı Sonu   | Bu boyutun satır tanımına eklenecek son değeri. |

Bir satır tanımına boyut eklemek için bu adımları izleyin.

1. Rapor Tasarımcısı'nda, **Satır Tanımları**'na tıklayın ve ardından değiştirilecek satır tanımını açın.
2. **Düzenle** menüsünde, **Boyutlardan Satır Ekle**'ye tıklayın.
3. **Boyutlardan Satır Ekle** iletişim kutusundaki **Boyutlar** satırında, satır tanımına aktarılacak boyuta ait hücreyi seçin ve ardından **Tüm &&&** seçeneğine tıklayın.
4. Satır tanımını belirli bir boyut değerleri aralığıyla sınırlandırmak için, **Boyut Aralığı Başlangıcı** hücresine başlangıç boyut değerini ve ardından **Boyut Aralığı Sonu** hücresindeki son boyut değerini girin. Seçilen boyuta ait tüm değerleri eklemek için bu hücreleri boş bırakın.

    > [!NOTE]
    > Boyut aralıklarındaki joker karakterler (\* veya ?) ERP veritabanının verileri nasıl harmanladığına bağlı olarak istediğiniz tüm sonuçları vermeyebilir.

5. **Başlangıç satır kodu** alanında, satır tanımına eklenecek ilk boyut değerine ait satır kodunu belirtin.
6. **Her satırı şu kadar artır:** alanında, art arda gelen satır kodları arasındaki boşluğu belirtin. Örneğin, ilk satır kodu 100 ve artış değeri 30 ise, ilk yeni satırların kodları 100, 130, 160, 190 ve 220 olur. Yeni biçim ve formül satırlarını eklemek için yeterli alan sağlayan bir artış değerini kullanın.
7. **Tamam** düğmesini tıklatın. Seçilen boyut değerlerinin her biri için satır tanımına bir satır eklenir.

## <a name="adjust-rounding-in-a-row-definition"></a>Bir satır tanımındaki yuvarlamayı ayarlama
Tutarların yuvarlandığı bir bilançonuz varsa toplamlar eşitlenmeyebilir. Bu sorun, örneğin bir bilanço raporunda yuvarlama seçeneğini kullanıyorsanız ve aynı zamanda rapor tanımı da yuvarlamayı belirtiyorsa görülebilir. Bilançolardaki tutarları eşitlemek için satır tanımındaki **Yuvarlama ayarlaması** seçeneğini kullanabilirsiniz. Yuvarlamayı rapor tanımının **Ayarlar** sekmesinde kapatabilir veya değiştirebilirsiniz. Aşağıdaki tabloda tutarların nasıl yuvarlandığı gösterilmektedir. Bu tabloda, yuvarlama açıkken 100 ve 200. satırların toplamları farklı olur.

| Satır kodu | Yuvarlamasız tutarlar | Tam binlere yuvarlamayla tutar |
|----------|--------------------------|-----------------------------------------|
| 100      | 3.600                    | 4                                       |
| 200      | 3.700                    | 4                                       |
| Toplam    | 7.300                    | 8                                       |

Bir bilançodaki yuvarlamayı ayarlamak için bu adımları izleyin.

1. Rapor Tasarımcısı'nda, **Satır Tanımları**'na tıklayın ve ardından değiştirilecek satır tanımını açın.
2. **Düzenle** menüsünde, **Yuvarlama Ayarlaması**'na tıklayın.
3. **Yuvarlama Ayarlamaları** iletişim kutusunda, şu değerleri girin:

    - **Yuvarlama ayarlaması satırı**: Bilançoyu eşitlemek için ayarlanması gereken satıra ait satır kodu.
    - **Toplam kıymetler satırı**: Bilançoda toplam kıymetleri içeren satıra ait satır kodu.
    - **Toplam borçlar ve öz sermaye satırı**: Bilançoda toplam borçları ve öz sermayeyi içeren satıra ait satır kodu.
    - **Ayarlama tutarı sınırı**: Otomatik ayarlamalarda sınırı belirten pozitif bir tam sayı. Bu tutar gerçek yuvarlama farkının mutlak değeriyle kıyaslanır.

    > [!NOTE]
    > Bu satır kodları mali verilerinizle ilişkilendirilmelidir. Başka bir deyişle, satırın **Mali Boyutlarla İlişkilendir** hücresinde bir boyut değeri olmalıdır. Bir açıklamaya (**DESC**), hesaplanan (**CALC**) ya da toplamı alınan (**TOT**) satıra **başvurmayın**.

Artık bilançonuzdaki tutarlar yuvarlama açıkken eşitlenir.

> [!NOTE]
> Ayarlama sınırı, rapor tanımı için belirtilen **Yuvarlama duyarlığı** seçeneğine göre uygulanır. Örneğin, raporunuzu binlere yuvarlayıp **Ayarlama tutarı sınırı** alanına **2** girerseniz **Yuvarlama ayarlaması satırı** alanındaki değer 2.000'den fazla artarsa veya azalırsa bir uyarı mesajı alırsınız.

## <a name="format-row-and-column-text"></a>Satır ve sütun metnini biçimlendirme
Raporlarınızın görünümünü yazı tiplerini değiştirip metni biçimlendirerek özelleştirebilirsiniz. Aşağıdaki bölümlerde raporlardaki satırların ve sütunların görünümünün nasıl değiştirileceği açıklanmaktadır.

### <a name="manage-font-styles"></a>Yazı tipi stillerini yönetme

Raporunuz için yazı tipi stilleri oluşturup bunları değiştirebilirsiniz. Ardından bu stilleri belgeye ya da rapordaki belirli bir satıra veya sütuna uygulayabilirsiniz.

<table>
<tbody>
<tr>
<td><strong>Yazı tipi stili oluşturma</strong></td>
<td>
<ol>
<li>Rapor Tasarımcısı'nda, <strong>Biçim</strong> menüsünde, <strong>Stiller ve Biçimlendirme</strong>'ye tıklayın.</li>
<li><strong>Stiller ve Biçimlendirme</strong> iletişim kutusunda, <strong>Yeni</strong>'ye tıklayın ve ardından yeni stil için benzersiz bir ad girin.</li>
<li>Yazı tipi seçimlerinizi yapın ve <strong>Tamam</strong>'a tıklayın.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Bir yazı tipi stilini değiştirme</strong></td>
<td>
<ol>
<li>Rapor Tasarımcısı'nda, <strong>Biçim</strong> menüsünde, <strong>Stiller ve Biçimlendirme</strong>'ye tıklayın.</li>
<li><strong>Stiller ve Biçimlendirme</strong> iletişim kutusunda, değiştirmek için bir stil seçin ve ardından <strong>Değiştir</strong>'e tıklayın.</li>
<li>Yazı tipi seçimlerinizi yapın ve <strong>Tamam</strong>'a tıklayın.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Bir yazı tipi stilini uygulama</strong></td>
<td>
<ol>
<li>Rapor Tasarımcısı'ndaki bir tanımda veya sütun tanımında ya da üst bilgilerde ve alt bilgilerde bir veya daha fazla hücreyi seçin.</li>
<li>Araç çubuğundaki <strong>Stil</strong> listesinden bir yazı tipi stili seçin.</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Satır metnini biçimlendirme

Satır tanımında belirtilen biçimlendirme sütun tanımında ve rapor tanımında belirtilen her türlü biçimlendirmeyi geçersiz kılar. Metin biçimini biçimlendirme araç çubuğundaki kontrolleri kullanarak değiştirebilirsiniz. Bu kontroller standart Microsoft Windows kontrolleridir.

1. Rapor Tasarımcısı'nda, değiştirilecek satır tanımını açın.
2. Biçimlendirilecek satırları seçin. Birden fazla hücre seçmek için, hücreyi seçerken Ctrl tuşunu basılı tutun.
3. Uygulanacak biçimin araç çubuğu düğmesine tıklayın. Örneğin, bir satıra girinti vermek için satırı seçin ve ardından araç çubuğundaki **Girintiyi Artır** ![Girintiyi Artır.](media/indent.gif "Girintiyi Artır") düğmesine tıklayın.

### <a name="adjust-columns-while-you-design-reports"></a>Rapor tasarlarken sütunları ayarlama

Satır tanımında üzerinde çalıştığınız sütunları görüntülemeyi kolaylaştırmak için, bir sütunun genişliğini ayarlayabilir ve aynı zamanda görünüm bölmesinde sütunları gizleyebilir (küçültebilir) veya gösterebilirsiniz. Yaptığınız değişiklikler yalnızca sütunların ekrandaki görünümlerini etkiler. Raporlardaki sütun biçimlendirmesini etkilemez.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Görünüm bölmesinde bir sütunun genişliğini değiştirme

1. Rapor Tasarımcısı'nda, değiştirilecek satır tanımını açın.
2. **Biçim** menüsünde, **Sütun Genişliği**'ni seçin.
3. **Sütun Genişliği** iletişim kutusunda, bir değer girin ve ardından **Tamam**'a tıklayın. Alternatif olarak, sütunun genişliğini değiştirmek için bir sütun başlığı hücresinin sağ sınırını sürükleyebilirsiniz.

### <a name="hide-columns-in-the-view-pane"></a>Görünüm bölmesindeki sütunları gizleme

1. Rapor Tasarımcısı'nda, değiştirilecek satır tanımını açın.
2. Küçültülecek sütunu veya sütunları seçin.
3. Sağ tıklayın ve ardından **Gizle**'ye tıklayın.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Görünüm bölmesindeki tüm gizli sütunları gösterme

1. Rapor Tasarımcısı'nda, değiştirilecek satır tanımını açın.
2. Görüntülemek için küçültülen sütuna sağ tıklayın ve ardından **Göster**'e tıklayın.


## <a name="additional-resources"></a>Ek kaynaklar

[Mali raporlama](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]