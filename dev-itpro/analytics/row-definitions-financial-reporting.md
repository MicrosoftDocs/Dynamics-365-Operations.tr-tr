---
title: "Finansal rapor tasarımcısında satır tanımları"
description: "Satır tanımını finansal rapordaki her satırın içeriğini belirten bir rapor bileşeni veya yapı taşıdır. Satır tanımı birden çok şirket tarafından kullanılabilen bir yapı taşı grubu oluşturmak için sütun tanımları, raporlama ağacı tanımları ve rapor tanımları ile birleştirilebilir."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 770a1681e4fa9974b081d0c63a10eb1961f13014
ms.openlocfilehash: 6d4697af6f7467f25a461fae4e9320402f83b0e3
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="row-definitions-in-financial-report-designer"></a>Finansal rapor tasarımcısında satır tanımları

[!include[banner](../includes/banner.md)]


Satır tanımını finansal rapordaki her satırın içeriğini belirten bir rapor bileşeni veya yapı taşıdır. Satır tanımı birden çok şirket tarafından kullanılabilen bir yapı taşı grubu oluşturmak için sütun tanımları, raporlama ağacı tanımları ve rapor tanımları ile birleştirilebilir.

<a name="create-a-row-definition"></a>Satır tanımı oluşturma
-----------------------

1.  Rapor Tasarımcısında gezinme bölmesinde **Satır Tanımları** öğesine tıklayın.
2.  **Dosya** menüsünde, **Yeni** öğesine ve ardından **Satır Tanımı** öğesine tıklayın. Her bir hücrenin içeriği hakkında daha fazla bilgi için [Satır tanımı hücrelerini değiştirme](modify-row-definition-cells-financial-reporting.md) bölümüne bakın.

## <a name="open-a-row-definition"></a>Bir satır tanımını açma
1.  Rapor Tasarımcısında gezinme bölmesinde **Satır Tanımları** öğesine tıklayın.
2.  Açılacak satır tanımının adını çift tıklayın.
3.  Satır tanımıyla ilişkili olan tüm yapı taşlarını görüntülemek için satır tanımına sağ tıklayın ve arından **İlişkiler** öğesini seçin.

## <a name="contents-of-a-row-definition"></a>Bir satır tanımının içeriği
Bir satır tanımı, 20.000 mali boyut satırına kadar alabilir ve şu bilgileri içerebilir:

-   Örneğin **nakit** veya **Toplam Gelir** gibi bölüm üstbilgileri, satırları ve boşlukları oluşturarak rapora anlam katan açıklayıcı metinler
-   Microsoft Dynamics 365 for Finance and Operations'taki boyut değerlerini içerebilen mali verilere bağlantılar. **Not:** Rapor her üretildiğinde mali boyutlar sisteminden veri çekecek bir satır tanımını ayarlayabilirsiniz.
-   Bağlantılı mali verilere dayalı satır toplamları ve formülleri

Genellikle, her bir satır tanımındaki her bir satır aşağıdaki veri türlerinden birini içerir:

-   Mali boyutlar sistemine başvurular
-   Verilere dayalı toplamlar veya hesaplamalar
-   Biçimlendirme

Satır tanımına veri girmek için iki yöntem bulunmaktadır:

-   Yeni satır tanımında satır bilgilerini el ile girin. Daha fazla bilgi için [Satır tanımı hücrelerini değiştirme](modify-row-definition-cells-financial-reporting.md) bölümüne bakın.
-   Satır bilgilerini doğrudan finansal boyutlardan çekmek için rapor tasarımcısını kullanın. Daha fazla bilgi için bkz. [Satır tanımı hücrelerini değiştirme](modify-row-definition-cells-financial-reporting.md) içindeki "İlgili formüller/satırlar/birimler" bölümü.

## <a name="add-dimensions-in-a-row-definition"></a>Bir satır tanımına boyutlar ekleme
Bir boyut, veri ve değerlerin bir kesişimidir. Rapor tasarımcısında verileri ve değerleri gruplandırabilirsiniz. Ardından hareketleri sınıflandırabilir ve daha ayrıntılı şekilde çözümleyebilirsiniz. Bir satır tanımına aynı anda birden fazla satır eklemek için **Boyutlardan Satır Ekle** iletişim kutusunu kullanabilirsiniz. İletişim kutusu her bir boyut için bir sütun görüntüler. Aşağıdaki tabloda her boyut için belirtebileceğiniz bilgiler açıklanmaktadır.

| Seçenek                | Açıklama                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boyut             | Satır tanımına eklenecek boyutu tanımlayan model. Bu model, boyutlardaki her bir konum için bir ve işareti (&) veya rakam işareti (\#) içerir. Genellikle, Ana Hesap boyutu için tüm ve işaretlerini ve diğer boyutlar için tüm rakam işaretlerini kullanırsınız. |
| Boyut Aralığı Başlangıcı | Bu boyutun satır tanımına ekleyeceği ilk değer.                                                                                                                                                                                                                 |
| Boyut Aralığı Sonu   | Bu boyutun satır tanımına ekleyeceği son değer.                                                                                                                                                                                                                  |

Bir satır tanımına boyutlar eklemek için şu adımları izleyin.

1.  Rapor Tasarımcısında **Satır Tanımları** öğesine tıklayın ve ardından değiştirmek için satır tanımını açın.
2.  **Düzenle** menüsündeki **Boyutlardan Satır Ekle** öğesini tıklayın.
3.  **Boyutlardan Satır Ekle** iletişim kutusunda, **Boyutlar** satırında, boyutun satır tanımına aktarılacağı hücreyi seçin ve **Tüm &&&** öğesine tıklayın.
4.  Satır tanımını boyut değerlerinin belirli bir aralığıyla sınırlandırmak için **Boyut Aralığı Başlangıcı** hücresine başlangıç boyut değerini ve ardından **Boyut Aralığı Sonu** hücresine bitiş boyut değerini girin. Seçilen boyut için tüm değerleri eklemek için bu hücreleri boş bırakın. **Not:** Boyut aralıklarındaki joker karakterler (\* veya ?) boyut aralıkları, ERP veritabanının verileri nasıl topladığına bağlı olarak istediğiniz tüm sonuçları vermeyebilir.
5.  **Başlangıç satırı kodu** alanında, satır tanımına eklenecek ilk boyut için satır kodunu belirtin.
6.  **Her satıra şuna göre artır** alanında, birbirini takip eden satır kodları arasındaki boşluğu belirtin. Örneğin, ilk satır kodu 100 ve artış değeri 30 ise, ilk yeni satırların kodları 100, 130, 160, 190 ve 220 olur. Yeni biçim ve formül satırlarını eklemek için yeterli alan sağlayan bir artış değerini kullanın.
7.  **Tamam** düğmesini tıklatın. Seçili boyut değerlerinin her biri için satır tanımına bir satır eklenir.

## <a name="adjust-rounding-in-a-row-definition"></a>Bir satır tanımında yuvarlamayı ayarlama
Tutarların yuvarlandığı bir bilançonuz varsa, toplamlar bakiyeyi vermeyebilir. Bu sorun, örneğin bilanço raporunda yuvarlama seçeneğini kullandığınızda ve rapor tanımını da yuvarlama işlemi belirttiğinde ortaya çıkabilir. Bilançolarınızdaki tutarları dengelemek için satır tanımındaki **Yuvarlama düzeltmesi** seçeneğini kullanabilirsiniz. Yuvarlama seçeneğini rapor tanımlarının **Ayarlar** sekmesinden kapatabilir veya değiştirebilirsiniz. Aşağıdaki tabloda tutarların nasıl yuvarlandığı gösterilmiştir. Bu tabloda, satır 100 ve 200 toplamları yuvarlama açık konuma getirildiğinde farklı çıkmaktadır.

| Satır kodu | Yuvarlama yapılmadan tutarlar | Tam binlere yuvarlama yapıldığında tutar |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| Toplam    | 7,300                    | 8                                       |

Bir bilançoda yuvarlamayı ayarlamak için şu adımları izleyin.

1.  Rapor Tasarımcısında **Satır Tanımları** öğesini tıklayın ve ardından değiştirmek için satır tanımını açın.
2.  **Düzenle** menüsünden **Yuvarlama Ayarı** öğesini tıklayın.
3.  **Yuvarlama Ayarları** iletişim kutusunda şu değerleri girin:
    -   **Yuvarlama ayar satırı** – Bilançonun dengelenmesi için ayarlanması gereken satır için satır kodu.
    -   **Toplam kıymetler satırı** – Toplam kıymetleri içeren bilançodaki satır için satır kodu.
    -   **Toplam borçlar ve öz varlık satırı** – Toplam borçları ve öz varlığı içeren bilançodaki satır için satır kodu.
    -   **Ayar tutarı sınırı** – Otomatik ayarlar için sınırı belirten pozitif tam sayı. Bu tutar, fiili yuvarlama farkının mutlak değeri ile karşılaştırılır.

    **Not:** Bu satır kodları mutlaka mali verilerinizle ilişkilendirilmelidir. Başka bir ifadeyle, satır mutlaka **Mali Boyutları Bağlantı** hücresinde bir boyut değerine sahip olmalıdır. **Kesinlikle** bir açıklama satırına (**DESC**), hesaplanan satıra (**CALC**) veya toplanan satıra (**TOT**) başvuru vermeyin.

Bilançonuzdaki tutarlar, yuvarlama açık konumdayken eşit şekilde dengelenir. **Not:** Ayar sınırı, rapor tanımı için belirtilen **Yuvarlama hassasiyeti** seçeneğine bağlı olarak uygulanır. Örneğin raporu binlere yuvarlayıp **Ayar tutarı sınırı** alanına **2** girdiğinizde **Yuvarlama ayar satırı** alanındaki değer 2.000'den fazla artar veya azalırsa bir uyarı mesajı alırsınız.

## <a name="format-row-and-column-text"></a>Satır ve sütun metni biçimlendirme
Yazı tiplerini değiştirerek ve metni biçimlendirerek raporlarınızın görünümünü özelleştirebilirsiniz. Aşağıdaki bölümde raporların satır ve sütunlarının görünümünün nasıl biçimlendirileceği açıklanmıştır.

### <a name="manage-font-styles"></a>Yazı tipi stillerini yönetme

Raporunuz için yazı tipi stilleri oluşturabilir ve değiştirebilirsiniz. Bu stilleri belgeye veya rapordaki belirli bir satıra veya sütuna uygulayabilirsiniz.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Bir yazı tipi stili oluşturma</td>
<td><ol>
<li>Rapor Tasarımcısında, <strong>Biçim </strong>menüsünde <strong>Stiller ve Biçimlendirme</strong> öğesini tıklayın.</li>
<li><strong>Stiller ve Biçimlendirme</strong> iletişim kutusunda <strong>Yeni</strong> öğesine tıklayın ve ardından yeni stil için bir özgün ad girin.</li>
<li>Yazı tipi seçimlerini oluşturun ve ardından <strong>Tamam</strong> düğmesini tıklayın.</li>
</ol></td>
</tr>
<tr class="even">
<td>Bir yazı tipi stilini değiştirme</td>
<td><ol>
<li>Rapor Tasarımcısında, <strong>Biçim </strong>menüsünde <strong>Stiller ve Biçimlendirme</strong> öğesini tıklayın.</li>
<li><strong>Stiller ve Biçimlendirme</strong> iletişim kutusundan değiştirilecek stili seçin ve ardından <strong>Değiştir</strong> öğesine tıklayın.</li>
<li>Yazı tipi seçimlerini oluşturun ve ardından <strong>Tamam</strong> düğmesini tıklayın.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Bir yazı tipi stili uygulama</td>
<td><ol>
<li>Rapor Tasarımcısı'nda bir tanımda veya bir sütun tanımında veya üstbilgilerde ve altbilgilerde bir veya daha fazla sayıda hücre seçin.</li>
<li>Araç çubuğundaki <strong>Stil</strong> listesinden bir yazı tipi stili seçin.</li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Satır metnini biçimlendirme

Satır tanımında belirtilen biçimlendirme sütun ve rapor tanımında belirtilen biçimlendirmeyi geçersiz kılar. Metin biçimini biçimlendirme araç çubuğundaki denetimleri kullanarak değiştirebilirsiniz. Bu kontroller standart Microsoft Windows kontrolleridir.

1.  Rapor Tasarımcısında değiştirilecek satır tanımını açın.
2.  Biçimlendirilecek hücreleri seçin. Birden fazla hücre seçmek için, hücreleri seçerken Ctrl tuşunu basılı tutun.
3.  Araç çubuğunda uygulanacak biçimlendirmeye karşılık gelen düğmeyi tıklayın. Örneğin, bir satıra girinti vermek için satırı seçin ve araç çubuğundaki **Girintiyi Artır** ![Girintiyi Artır](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Girintiyi Artır") düğmesine tıklayın.

### <a name="adjust-columns-while-you-design-reports"></a>Rapor tasarlarken sütunları ayarlama

Üzerinde çalıştığınız satırları satır tanımında daha kolay görüntüleyebilmek için, bir sütunun genişliğini ayarlanabilir ve sütunları görünüm bölmesinde gizleyebilir (simge durumuna küçültebilir) veya gösterebilirsiniz. Yaptığınız değişiklikler sütunların yalnızca ekrandaki görünümlerini etkiler. Raporlardaki sütun biçimlendirmesini etkilemez.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Bir sütunun görünüm bölmesindeki genişliğini değiştirme

1.  Rapor Tasarımcısında değiştirilecek satır tanımını açın.
2.  **Biçim** menüsünde **Sütun Genişliği** öğesini seçin.
3.  **Sütun Genişliği** iletişim kutusuna bir değer girin ve ardından **Tamam**'a tıklayın. Alternatif olarak, sütun genişliğini değiştirmek için bir sütun üstbilgi hücresinin sağ sınırını da sürükleyebilirsiniz.

### <a name="hide-columns-in-the-view-pane"></a>Sütunları görünüm bölmesinde gizleme

1.  Rapor Tasarımcısında değiştirilecek satır tanımını açın.
2.  Simge durumuna getirilecek sütunu veya sütunları seçin.
3.  Sağ tıklayın ve ardından **Gizle** öğesini tıklayın.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Görünüm bölmesindeki tüm gizli sütunları gösterme

1.  Rapor Tasarımcısında değiştirilecek satır tanımını açın.
2.  Görüntülenecek simge durumuna küçültülmüş sütuna sağ tıklayın ve ardından **Göster** öğesine tıklayın.


<a name="see-also"></a>Ayrıca bkz.
--------

[Mali raporlama](financial-reporting-intro.md)




