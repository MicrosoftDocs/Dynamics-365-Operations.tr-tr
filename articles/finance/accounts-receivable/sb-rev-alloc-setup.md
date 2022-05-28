---
title: Çok öğeli gelir tahsisatı ayarla
description: Bu konu, abonelik faturalamasında çoklu öğe gelir tahsisatı için parametrelerin nasıl ayarlanacağını açıklar.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: bb5b220dd941cbb9f1fda5d0eb821a86a9135309
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685813"
---
# <a name="set-up-multiple-element-revenue-allocation"></a>Çok öğeli gelir tahsisatı ayarla

Çoklu öğe gelir tahsisatı, birden fazla madde arasında gelir hesaplamak ve bölmek için kullanılan farklı şablonlar ayarlamanıza olanak sağlar. Bu işlevsellik, Muhasebe Standartları Kodlaması Konu 606 (ASC 606) ve/veya Uluslararası Mali Raporlama Standardı 15 (IFRS 15) gerekliliklerine uymanıza yardımcı olabilir.

## <a name="multiple-element-revenue-allocation-parameters"></a>Çok öğeli gelir tahsisatı parametreleri

Çok öğeli gelir tahsisatı için parametreleri ayarlamak üzere **Çok öğeli gelir tahsisatı parametreleri** sayfasını kullanın.

### <a name="standalone-selling-price-origin"></a>Tek başına satış fiyatı kaynağı

**Tek başına satış fiyatı kaynağı** alanı, tek başına satış fiyatının nereden geldiğini belirtir. **Maddenin tek başına satış fiyatı** sayfasındaki ve hareketteki değeri güncelleştirebilirsiniz. Aşağıdaki seçenekler kullanılabilir.

| Seçenek | Açıklama |
|--------|-------------|
| Tutar | Tek başına satış fiyatı, 0'dan (sıfır) büyük olan ve sizin belirttiğiniz bir tutardır. Tutar, gereken şekilde işlevsel ve kaynak para birimleri arasında dönüştürülür. |
| Taban satış fiyatı | Tek başına satış fiyatı maddenin temel satış fiyatıyla eşleşir. |
| Fatura fiyatı | Tek başına satış fiyatı maddenin fatura fiyatıyla eşleşir. |
| Madde yüzdesi | Tek başına satış fiyatı yüzde değeri olarak belirtilir ve maddenin fiyatına göre hesaplanır. Bu seçeneği seçerseniz, varsayılan yüzdeyi belirtin. |
| Kalan tutarı tahsis et | <p>Tek başına satış fiyatının kaynağı, *Ana maddenin toplam sözleşme değeri* – *Alt maddelerin toplam tek başına satış fiyatı* olarak hesaplanır:</p><ul><li>*Ana maddenin toplam sözleşme değeri*, net veya faturalanan tutardır.</li><li>*Alt maddelerin toplam tek başına satış fiyatı*, bu tek başına satış fiyatı kaynağını kullanan alt madde dışındaki tüm alt maddelerin genişletilmiş veya sözleşme tek başına satış fiyatı toplamıdır.</li></ul><p>Hesaplanan tutar negatif bir değer ise, tutar 0 (sıfır) olarak ayarlanır.</p><p>**Not:** Bu seçenek, gelir bölünmesi alanında yalnızca bir alt madde için seçilebilir.</p> |
| Yok | Tek başına satış fiyatının kaynağı, alt maddelere dayanır. Bu seçenek, gelir bölünmesi şablonunda üst madde olarak tanımlanan maddelere uygulanır. **Gelir bölme** onay kutusu işaretliyse, bu seçenek otomatik olarak seçilir ve ayar değiştirilemez. |
| Ana fatura fiyatının yüzdesi | Tek başına satış fiyatının kaynağı, ana maddenin fatura fiyatının bir yüzdesidir. Varsayılan değeri değiştirebilirsiniz. Bu seçenek yalnızca gelir bölme şablonundaki alt maddeler için kullanılabilir. |
| Ana standart fiyatın yüzdesi | Tek başına satış fiyatının kaynağı, ana maddenin standart fiyatının bir yüzdesidir. Varsayılan değeri değiştirebilirsiniz. Bu seçenek yalnızca gelir bölme şablonundaki alt maddeler için kullanılabilir. Bu, alt öğeler için varsayılan seçenektir. Bir alt maddeye ait seçenek, **Ana standart fiyatın yüzdesi** ayarından **Ana fatura fiyatının yüzdesi** ayarına veya **Ana fatura fiyatının yüzdesi** ayarından **Ana standart fiyatın yüzdesi** ayarına değiştirilirse, hesaplanan değerler de güncelleştirilir. |

### <a name="account-for-revenue-allocation-rounding-differences"></a>Gelir tahsisatı yuvarlama farkları hesabı

**Gelir tahsisatı yuvarlama farkları hesabı** alanı, bir sözleşme gelir tutarına yapılan yuvarlama düzeltmelerini kaydetmek için kullanılan hesabı belirtir. Yinelenen sözleşme faturalaması kullanıldığında kullanılabilir.

## <a name="item-standalone-selling-price"></a>Madde tek başına satış fiyatı

Bir maddenin kaynak ve tek başına satış fiyatını belirtmek için **Madde tek başına satış fiyatı** sayfasını kullanın. Bu sayfada belirtilen değerler, çok öğeli gelir tahsisatı ve yinelenen sözleşme faturalamasındaki **Gelir tahsisatı** sayfasında varsayılan değerler olarak kullanılır.

### <a name="specify-item-standalone-selling-price"></a>Madde tek başına satış fiyatını belirtme

Bir maddenin tek başına fiyatını belirtmek için aşağıdaki adımları izleyin.

1. **Madde tek başına satış fiyatı** sayfasında, **Tek başına satış fiyatı kaynağı** alanında, tek başına satış fiyatının kaynağını seçin.
2. **Tek başına satış fiyatı kaynağı** alanında seçtiğiniz değere bağlı olarak, aşağıdaki adımlardan birini izleyin:

    * **Madde yüzdesi**'ni seçtiyseniz, **Yüzde** alanında yüzdeyi belirtin.
    * **Tutar**'ı seçtiyseniz , **Tek başına satış fiyatı** alanında tutarı belirtin.

2. Listeye eklemek istediğiniz her madde için **Ekle**'yi seçin.
3. **Madde kodu** alanında madde kodunu seçin. **Madde ilişkisi** alanında madde ilişkisini seçin. **Gelir bölme** onay kutusunun temizlenmiş olduğu maddeler için, seçilen madde kodu ve madde ilişkisi kombinasyonu benzersiz olmalıdır.
4. İhtiyaç duyduğunuz şekilde **Tek başına satış fiyatı kaynağı**, **Tek başına satış fiyatı** veya **Yüzde** alanının varsayılan değerini değiştirin.
5. Listeye eklemek istediğiniz her üst madde için **Ekle**'yi seçin.
6. **Madde kodu** alanında madde kodunu seçin. **Madde ilişkisi** alanında madde ilişkisini seçin.
7. **Gelir bölme** onay kutusunu işaretleyin.
8. **Madde ilişkisi** alanında madde ilişkisini seçin. Liste, ana maddeyle ve tüm alt maddelerle birlikte güncelleştirilir.
9. Alt madde için, gereksinim duyduğunuz şekilde **Tek başına satış fiyatı kaynağı**, **Ana standart fiyatın yüzdesi**, **Ana fatura fiyatının yüzdesi** veya **Kalan tutarı tahsis et** alanının varsayılan değerini değiştirin.
10. Bir seferde birden fazla madde eklemek için, **Madde ekle**'yi seçin.
11. Eklemek istediğiniz madde aralığını seçmek için sorguyu güncelleştirin.
12. **Tamam**'ı seçin, eklediğiniz maddelerin listesini gözden geçirin ve **Tamam**'ı seçin.

### <a name="fields"></a>Alanlar

**Madde tek başına satış fiyatı** sayfası aşağıdaki alanları içerir.

| Alan | Açıklama |
|-------|-------------|
| Tek başına satış fiyatı kaynağı | <p>Tek başına satış fiyatının kaynağını seçin:</p><ul><li>**Tutar** – Tek başına satış fiyatı, 0'dan (sıfır) büyük olan ve sizin belirttiğiniz bir tutardır. Tutar, gereken şekilde işlevsel ve kaynak para birimleri arasında dönüştürülür.</li><li>**Temel satış fiyatı** – Tek başına satış fiyatı, maddenin temel satış fiyatıyla eşleşir.</li><li>**Fatura fiyatı** – Tek başına satış fiyatı, maddenin fatura fiyatıyla eşleşir.</li><li>**Madde yüzdesi** – Tek başına satış fiyatı yüzde değeri olarak belirtilir ve maddenin fiyatına göre hesaplanır. Bu seçeneği seçerseniz, varsayılan yüzdeyi belirtin.</li></ul>**Kalan tutarı tahsis et** – Tek başına satış fiyatının kaynağı, *Ana maddenin toplam sözleşme değeri* – *Alt maddelerin toplam tek başına satış fiyatı* olarak hesaplanır:</p><ul><li>*Ana maddenin toplam sözleşme değeri*, net veya faturalanan tutardır.</li><li>*Alt maddelerin toplam tek başına satış fiyatı*, bu tek başına satış fiyatı kaynağını kullanan alt madde dışındaki tüm alt maddelerin genişletilmiş veya sözleşme tek başına satış fiyatı toplamıdır.</li></ul><p>Hesaplanan tutar negatif bir değer ise, tutar 0 (sıfır) olarak ayarlanır.</p><p>**Not:** Bu seçenek, gelir bölünmesi alanında yalnızca bir alt madde için seçilebilir.</p></li><li>**Yok** – Tek başına satış fiyatının kaynağı, alt maddelere dayanır. Bu seçenek, gelir bölünmesi şablonunda üst madde olarak tanımlanan maddelere uygulanır. **Gelir bölme** onay kutusu işaretliyse, bu seçenek otomatik olarak seçilir ve ayar değiştirilemez.</li><li>**Ana fatura fiyatının yüzdesi** – Tek başına satış fiyatının kaynağı, ana maddenin fatura fiyatının bir yüzdesidir. Varsayılan değeri değiştirebilirsiniz. Bu seçenek yalnızca gelir bölme şablonundaki alt maddeler için kullanılabilir.</li><li>**Ana standart fiyatın yüzdesi** – Tek başına satış fiyatının kaynağı, ana maddenin standart fiyatının bir yüzdesidir. Varsayılan değeri değiştirebilirsiniz. Bu seçenek yalnızca gelir bölme şablonundaki alt maddeler için kullanılabilir. Bu, alt öğeler için varsayılan seçenektir. Bir alt maddeye ait seçenek, **Ana standart fiyatın yüzdesi** ayarından **Ana fatura fiyatının yüzdesi** ayarına veya **Ana fatura fiyatının yüzdesi** ayarından **Ana standart fiyatın yüzdesi** ayarına değiştirilirse, hesaplanan değerler de güncelleştirilir.</li></ul> |
| Tek başına satış fiyatı | Maddenin tek başına satış fiyatını belirtin. Bu alan, **Tek başına satış fiyatı kaynağı** alanı **Tutar** olarak ayarlandığında kullanılabilir. |
| Yüzde | Tek başına satış fiyatı yüzdesini belirtin. Bu alan, **Tek başına satış fiyatı kaynağı** alanı **Madde yüzdesi**, **Ana fatura fiyatının yüzdesi** veya **Ana standart fiyatın yüzdesi** olarak ayarlandığında kullanılabilir. |
| Gelir bölme | <p>Bir satırın gelir bölmeyi kullanıp kullanmayacağını belirtin:</p><ul><li>**Seçildi** – Yalnızca bir gelir bölme şablonunun ayarlandığı maddeler **Madde ilişkisi** alanında seçilebilir. Bu onay kutusunu yalnızca gelir bölme şablonunun ana maddeleri için seçebilirsiniz.</li><li>**Temizlendi** – Madde, gelir bölmeyi kullanmayan standart bir maddedir.</li></ul> |
| İlişki | Bir simge, maddenin gelir bölmede üst madde mi yoksa alt madde mi olduğunu belirtir. |
| Madde kodu | <p>Madde kodunu seçin: **Tablo** veya **Grup**.</p><p>**Gelir bölme** onay kutusu işaretliyse, bu alan **Tablo** olarak ayarlanır ve değer değiştirilemez.</p> |
| Madde ilişkisi | <p>Madde numarası seçin.</p><p>**Gelir bölme** onay kutusu işaretliyse, yalnızca bir gelir bölme şablonu için ayarlanmış olan maddeler seçim için kullanılabilir. Üst madde seçildiğinde liste, ilgili üst maddenin alt maddeleriyle otomatik olarak güncelleştirilir.</p> |
| Ana madde | Ana madde için bu alan madde kodunu gösterir. Gelir bölünmesi içindeki alt maddeler için, ana maddenin madde numarasını gösterir. |

## <a name="mea-templates"></a>MEA şablonları

Birden çok öğe düzenleme (MEA) şablon kimlikleri oluşturmak ve düzenlemek için **MEA şablonları** sayfasını kullanın. Bu kimlikler, maddeleri birlikte gruplamak için **Gelir tahsisatı** sayfasında kullanılır.

### <a name="create-a-template"></a>Şablon oluşturma

MEA şablonu ayarlamak için aşağıdaki adımları izleyin.

1. **MEA şablonları** sayfasında, **Yeni**'yi seçin.
1. **MEA şablon kimliği** alanına benzersiz bir kimlik girin.
1. **Açıklama** alanına bir açıklama girin.
1. **Ertelenen sözleşme gelir hesabı** alanında, bir MEA sözleşme faturası oluşturulduğunda günlük girişleri için kullanmak istediğiniz hesabı seçin. Bu alan, yinelenen sözleşme faturalaması etkinleştirildiğinde ve kullanılırken kullanılabilir.
1. **Kaydet**'i seçin.
