---
title: Çalışma zamanı sorunlarını önlemek için yapılandırılmış ER bileşenini denetleme
description: Bu konuda, oluşabilecek çalışma zamanı sorunlarını önlemek için yapılandırılmış elektronik raporlama (ER) bileşenlerinin nasıl denetleneceği açıklamaktadır.
author: NickSelin
ms.date: 01/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c63ffc6316d21d36bb2aad57194b8aa1c477607e
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8074803"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a>Çalışma zamanı sorunlarını önlemek için yapılandırılmış ER bileşenini denetleme

[!include[banner](../includes/banner.md)]

Her yapılandırılmış [Elektronik raporlama (ER)](general-electronic-reporting.md)[biçimi](er-overview-components.md#format-components-for-outgoing-electronic-documents) ve [model eşleme](er-overview-components.md#model-mapping-component) bileşeni, tasarım zamanında [doğrulanabilir](er-fillable-excel.md#validate-an-er-format). Bu doğrulama sırasında, yürütme hataları ve performans düşüşü gibi oluşabilecek çalışma zamanı sorunlarını önlemeye yardımcı olmak için tutarlılık denetimi çalıştırılır. Bulunan her sorun için denetim, sorunlu öğenin yolunu belirtir. Bazı sorunlar için, otomatik düzeltme kullanılabilir.

Varsayılan olarak, aşağıdaki durumlarda yukarıda belirtilen ER bileşenlerini içeren bir ER yapılandırması için doğrulama otomatik olarak uygulanır:

- Microsoft Dynamics 365 Finance kurulumunuza yeni bir ER yapılandırması [sürümü](general-electronic-reporting.md#component-versioning) [içeri aktardığınızda](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally).
- Düzenlenebilir ER yapılandırmasının [durumunu](general-electronic-reporting.md#component-versioning) **Taslak**'tan **Tamamlandı** olarak değiştirdiğinizde.
- Yeni bir taban sürümü uygulayarak düzenlenebilir bir ER yapılandırmasını [yeniden temellendirdiğinizde](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).

Bu doğrulamayı açıkça çalıştırabilirsiniz. Aşağıdaki üç seçenekten birini seçin ve belirtilen adımları izleyin:

- 1. Seçenek:

    1. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
    2. Sol bölmedeki yapılandırmalar ağacında, ER biçimi veya ER model eşleme bileşenini içeren istediğiniz bir ER yapılandırmasını seçin.
    3. **Sürümler** hızlı sekmesinde, seçili ER yapılandırmasının istenen sürümünü seçin.
    4. Eylem bölmesinde **Doğrula**'yı seçin.

- 2. Seçenek (ER biçimi için):

    1. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
    2. Sol bölmedeki yapılandırmalar ağacında, ER biçimi bileşenini içeren istediğiniz bir ER yapılandırmasını seçin.
    3. **Sürümler** hızlı sekmesinde, seçili ER yapılandırmasının istenen sürümünü seçin.
    4. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
    5. **Biçim tasarımcısı** sayfasındaki Eylem Bölmesinde **Doğrula**'yı seçin.

- 3. Seçenek (ER model eşleme için):

    1. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
    2. Sol bölmedeki yapılandırmalar ağacında, ER model eşleme bileşenini içeren istediğiniz bir ER yapılandırmasını seçin.
    3. **Sürümler** hızlı sekmesinde, seçili ER yapılandırmasının istenen sürümünü seçin.
    4. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
    5. **Veri kaynağı eşleme modeli** sayfasında Eylem Panosu üzerinde **Tasarımcı**'yı seçin.
    6. **Model eşleme tasarımcısı** sayfasındaki Eylem bölmesinde **Doğrula**'yı seçin.

Yapılandırma içeri aktarıldığında doğrulamayı atlamak için aşağıdaki adımları izleyin.

1. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Yapılandırmayı içeri aktarmadan sonra doğrula** seçeneğini **Hayır** olarak ayarlayın.

Sürüm durumunu değiştirdiğinizde veya yeniden temellendirdiğinizde doğrulamayı atlamak için aşağıdaki adımları izleyin.

1. **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırmalar** seçeneğine git.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Yapılandırma durumu değişiminde ve yeniden temellendirilmesinde doğrulamayı atla** seçeneğini **Evet** olarak ayarlayın.

ER tutarlılık denetimi denetlemelerini gruplandırmak için aşağıdaki kategorileri kullanır:

- **Yürütülebilirlik**: Çalışma zamanında oluşabilecek kritik sorunları algılayan incelemeler. Bu sorunlar çoğunlukla bir **Hata** düzeyindedir. 
- **Performans**: Yapılandırılmış ER bileşenlerinin verimsiz şekilde yürütülmesine neden olabilecek sorunları tespit eden denetlemeler. Bu sorunlar çoğunlukla bir **Uyarı** düzeyindedir.
- **Veri bütünlüğü**: Veri kaybına veya çalışma zamanı sorunlarına neden olabilecek sorunları algılayan denetlemeler. Bu sorunlar çoğunlukla bir **Uyarı** düzeyindedir.

## <a name="list-of-inspections"></a>Denetlemeler listesi

Aşağıdaki tabloda, ER tarafından sağlanan denetlemeler hakkında genel bilgiler sağlanmıştır. Bu denetlemeler hakkında daha fazla bilgi edinmek için, ilk sütundaki bağlantıları bu konunun ilgili kısımlarına gitmek üzere kullanın. Bu bölümler, ER'nin denetleme sağladığı bileşen türlerini ve sorunları önlemek için ER bileşenlerini nasıl yeniden yapılandıracağınızı açıklamaktadır.

<table>
<thead>
<tr>
<th>Kuruluş adı</th>
<th>Kategori</th>
<th>Raf</th>
<th>İleti</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href='#i1'>Tür dönüştürme</a></td>
<td>Yürütülebilirlik</td>
<td>Hata</td>
<td>
<p>&lt;type&gt; türündeki ifade &lt;type&gt; türündeki alana dönüştürülemiyor.</p>
<p><b>Çalışma zamanı hatası:</b> Tür için özel durum</p>
</td>
</tr>
<tr>
<td><a href='#i2'>Tür uyumluluğu</a></td>
<td>Yürütülebilirlik</td>
<td>Hata</td>
<td>
<p>Yapılandırılan ifade, &lt;type&gt; türündeki geçerli biçim öğesi tarafından desteklenen veri türlerinin kapsamı dışındaki &lt;type&gt; veri türü değerini döndürdüğünden, söz konusu ifade geçerli biçim öğesini veri kaynağına bağlamak için kullanılamaz.</p>
<p><b>Çalışma zamanı hatası:</b> Özel durum türü</p>
</td>
</tr>
<tr>
<td><a href='#i3'>Eksik yapılandırma öğesi</a></td>
<td>Yürütülebilirlik</td>
<td>Hata</td>
<td>
<p>Yol bulunamadı: &lt;path&gt;.</p>
<p><b>Çalışma zamanı hatası:</b> &lt;path&gt; yapılandırma öğesi bulunamadı</p>
</td>
</tr>
<tr>
<td><a href='#i4'>FILTER işlevi içeren bir ifadenin yürütülebilirliği</a></td>
<td>Yürütülebilirlik</td>
<td>Hata</td>
<td>
<p>FİLTRE işlevinin liste ifadesi sorgulanabilir değil.</p>
<p><b>Çalışma zamanı hatası:</b> Filtreleme desteklenmiyor. Bu konuda daha fazla ayrıntı öğrenmek için yapılandırmayı doğrulayın.</p>
</td>
</tr>
<tr>
<td rowspan='2'><a href='#i5'>GROUPBY veri kaynağının yürütülebilirliği</a></td>
<td>Yürütülebilirlik</td>
<td>Hata</td>
<td>&lt;path&gt; yolu sorgulamayı desteklemiyor.</td>
</tr>
<tr>
<td>Yürütülebilirlik</td>
<td>Hata</td>
<td>
<p>Gruplandırma ölçütü işlevi, sorguyla yürütülemez.</p>
<p><b>Çalışma zamanı hatası:</b> Gruplandırma ölçütü işlevi, sorguyla yürütülemez.</p>
</td>
</tr>
<tr>
<td><a href='#i6'>JOIN veri kaynağının yürütülebilirliği</a></td>
<td>Yürütülebilirlik</td>
<td>Hata</td>
<td>
<p>Sorguda filtre olmayan bir liste &lt;path&gt; birleştirilemiyor.</p>
<p><b>Çalışma zamanı hatası:</b> Birleştirilmiş veri kaynağı işlevi, filtre ifadesi olmalıdır, hesaplanan alan hatalı olarak çağrılmıştır.</p>
</td>
</tr>
<tr>
<td><a href='#i7'>FILTER ile WHERE işlevinin tercih edilirliği</a></td>
<td>Performans</td>
<td>Uyarı</td>
<td>İfade için FILTER işlevinin kullanılması, performans açısından WHERE işlevinin kullanılmasından daha tercih edilir bir durumdur. Otomatik olarak değiştirmek için Düzelt'i seçin.</td>
</tr>
<tr>
<td><a href='#i8'>ALLITEMSQUERY ile ALLITEMS işlevinin tercih edilirliği</a></td>
<td>Performans</td>
<td>Uyarı</td>
<td>İfade için ALLITEMSQUERY işlevinin kullanılması, performans açısından ALLITEMS işlevinin kullanılmasından daha tercih edilir bir durumdur. Otomatik olarak değiştirmek için Düzelt'i seçin.</td>
</tr>
<tr>
<td><a href='#i9'>Boş liste durumlarının dikkate alınması</a></td>
<td>Yürütülebilirlik</td>
<td>Uyarı</td>
<td>
<p>Liste &lt;path&gt; boş liste durumu için herhangi bir denetime sahip değildir; çalışma zamanında hataya neden olabilir. Boş liste durumu için denetim ekleyin.</p>
<p><b>Çalışma zamanı hatası:</b> Liste &lt;path&gt; konumunda boş</p>
<p><b><a href='#i9a'>Olası sorun</a>:</b> Satır bir kez doldurulurken veri kaynağı birden fazla kayıttan doldurulur</p>
</td>
</tr>
<tr>
<td><a href='#i10'>FILTER işlevi içeren bir ifadenin yürütülebilirliği (önbelleğe alma)</a></td>
<td>Yürütülebilirlik</td>
<td>Hata</td>
<td>
<p>FILTER işlevi, seçili veri kaynağı türüne uygulanamaz. Tablo kayıtları türündeki bir veri kaynağı, yalnızca önbelleğe alınmamışsa ve el ile iç içe geçirilen veri kaynakları yoksa uygulanabilir.</p>
<p><b>Çalışma zamanı hatası:</b> Filtreleme desteklenmiyor. Bu konuda daha fazla ayrıntı öğrenmek için yapılandırmayı doğrulayın.</p>
</td>
</tr>
<tr>
<td><a href='#i11'>Eksik bağlama</a></td>
<td>Yürütülebilirlik</td>
<td>Uyarı</td>
<td>
<p>&lt;path&gt; yolunda modelin eşlemesinin kullanılmasında herhangi bir veri kaynağına bağ yok.</p>
<p><b>Çalışma zamanı hatası:</b> &lt;path&gt; yolu bağlı değil</p>
</td>
</tr>
<tr>
<td><a href='#i12'>Bağlanmamış şablon</a></td>
<td>Veri bütünlüğü</td>
<td>Uyarı</td>
<td>&lt;name&gt; dosyası hiçbir dosya bileşenine bağlı değil ve konfigürasyon sürümünün durumu değiştirildikten sonra kaldırılacak.</td>
</tr>
<tr>
<td><a href='#i13'>Eşitlenmemiş biçim</a></td>
<td>Veri bütünlüğü</td>
<td>Uyarı</td>
<td>&lt;component name&gt; tanımlı adı, &lt;sheet name&gt; Excel sayfasında bulunmuyor</td>
</tr>
<tr>
<td><a href='#i14'>Eşitlenmemiş biçim</a></td>
<td>Veri bütünlüğü</td>
<td>Uyarı</td>
<td>
<p>Word şablon dosyasında &lt;etiketli Word içerik denetimi&gt; etiketi yok</p>
<p><b>Çalışma zamanı hatası:</b>Word şablon dosyasında &lt;etiketli Word içerik denetimi&gt; etiketi yok.</p>
</td>
</tr>
<tr>
<td><a href='#i15'>Varsayılan eşleme yok</a></td>
<td>Veri bütünlüğü</td>
<td>Hata</td>
<td>
<p>&lt;Virgülle ayrılmış yapılandırma adları&gt; yapılandırmalarındaki &lt;model adı (kök tanımlayıcı)&gt; veri modeli için birden fazla model eşlemesi var. Yapılandırmalardan birini varsayılan olarak ayarlayın</p>
<p><b>Çalışma zamanı hatası:</b> &lt;Virgülle ayrılmış yapılandırma adları&gt; yapılandırmalarındaki &lt;model adı (kök tanımlayıcı)&gt; veri modeli için birden fazla model eşlemesi var. Yapılandırmalardan birini varsayılan olarak ayarlayın.</p>
</td>
</tr>
<tr>
<td><a href='#i16'>Üst bilgi veya alt bilgi bileşenlerinin tutarsız ayarı</a></td>
<td>Veri bütünlüğü</td>
<td>Hata</td>
<td>
<p>Üst bilgiler/alt bilgiler( &lt;bileşen türü: üst bilgi veya alt bilgi&gt;) tutarsız</p>
<p><b>Çalışma Zamanı:</b>Yapılandırılan ER biçiminin taslak sürümü yürütülürse, son yapılandırılan bileşen çalışma zamanında kullanılır.</p>
</td>
</tr>
<tr>
<td><a href='#i17'>Sayfa bileşeninin tutarsız ayarı</a></td>
<td>Veri bütünlüğü</td>
<td>Hata</td>
<td>Çoğaltma olmaksızın ikiden fazla aralık bileşeni var. Lütfen gereksiz bileşenleri kaldırın.</td>
</tr>
<tr>
<td><a href='#i18'>ORDERBY işlevi içeren bir ifadenin yürütülebilirliği</a></td>
<td>Yürütülebilirlik</td>
<td>Hata</td>
<td>
<p>ORDERBY işlevinin liste ifadesi sorgulanabilir değil.</p>
<p><b>Çalışma zamanı hatası:</b> Sıralama desteklenmiyor. Bu konuda daha fazla ayrıntı öğrenmek için yapılandırmayı doğrulayın.</p>
</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a>Tür dönüştürme

ER; veri modeli alanı veri türünün, söz konusu alanın bağı olarak yapılandırılmış ifadenin veri türüyle uyumlu olup olmadığını denetler. Veri türleri uyumsuzsa ER model eşleme tasarımcısında bir doğrulama hatası oluşur. Aldığınız iletide, ER'nin A türündeki ifadeyi B türündeki alana dönüştüremediği belirtilir.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER veri modelini ve ER model eşleme bileşenlerini eşzamanlı olarak yapılandırmaya başlayın.
2. Veri modeli ağacında **X** adlı bir alan ekleyin ve veri türü olarak **Tamsayı**'yı seçin.

    ![X alanı ve Tamsayı veri türü, Veri modeli sayfasındaki veri modeli ağacına eklenir.](./media/er-components-inspections-01.png)

3. Model eşleme tasarımcısında **veri kaynakları** bölmesinde **Hesaplanan alan** türünün bir veri kaynağını ekleyin.
4. Yeni veri kaynağını **Y** olarak adlandırın ve `INTVALUE(100)` ifadesini içerecek şekilde yapılandırın.
5. **X**'i **Y**'ye bağlayın.
6. Veri modeli tasarımcısında, **X** alanının veri türünü **Tamsayı**'dan **Int64** olarak değiştirin.
7. **Model eşleme tasarımcısı** sayfasında, düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin.

    ![Model eşleme tasarımcısı sayfasında düzenlenebilir model eşleme bileşenini doğrulama.](./media/er-components-inspections-01.gif)

8. **Yapılandırmalar** sayfasında seçili ER yapılandırmasının model eşleme bileşenini denetlemek için **Doğrula**'yı seçin.

    ![Yapılandırmalar sayfasında model eşleme bileşenini denetleme.](./media/er-components-inspections-01a.png)

9. Doğrulama hatasının oluştuğunu göreceksiniz. Bu iletide şu belirtilir: **Y** veri kaynağının döndürdüğü `INTVALUE(100)` ifadesinin **Tamsayı** türündeki değeri, **Int64** türündeki **X** veri modeli alanında depolanamaz.

Aşağıdaki çizimde, uyarıyı yok sayıp model eşlemesini kullanmak üzere yapılandırılmış bir biçimi çalıştırmak için **Çalıştır**'ı seçerseniz oluşacak çalışma zamanı hatası gösterilir.

![Biçim tasarımcısı sayfasındaki çalışma zamanı hataları.](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

Veri modeli alanının veri türünü değiştirerek veri modeli yapısını güncelleştirin. Böylece veri türü, söz konusu alanın bağlanması için yapılandırılan ifadenin veri türüyle eşleşir. Önceki örnek için, **X** alanının veri türünün tekrar **Tamsayı** olarak değiştirilmesi gerekir.

#### <a name="option-2"></a>Seçenek 2

Veri modeli alanına bağlı veri kaynağının ifadesini değiştirerek model eşlemeyi güncelleştirin. Önceki örnek için, **Y** veri kaynağı ifadesinin `INT64VALUE(100)` olarak değiştirilmesi gerekir.

## <a name="type-compatibility"></a><a id="i2"></a>Tür uyumluluğu

ER; biçim öğesi veri türünün, söz konusu biçim öğesinin bağı olarak yapılandırılmış ifadenin veri türüyle uyumlu olup olmadığını denetler. Veri türleri uyumsuzsa ER İşlemleri tasarımcısında bir doğrulama hatası oluşur. Aldığınız iletide yapılandırılan ifade, B veri türündeki geçerli biçim öğesi tarafından desteklenen veri türlerinin kapsamı dışındaki A veri türü değerini döndürdüğünden, söz konusu ifadenin geçerli biçim öğesini veri kaynağına bağlamak için kullanılamayacağı belirtilir.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER veri modelini ve ER biçim bileşenlerini eşzamanlı olarak yapılandırmaya başlayın.
2. Veri modeli ağacında **X** adlı bir alan ekleyin ve veri türü olarak **Tamsayı**'yı seçin.
3. Biçim yapısı ağacında, **Sayısal** türde bir biçim öğesi ekleyin.
4. Yeni biçim öğesini **Y** olarak adlandırın. **Sayısal tür** alanında, veri türü olarak **Tamsayı**'yı seçin.
5. **X**'i **Y**'ye bağlayın.
6. Biçim yapısı ağacında, **Y** biçim öğesinin veri türünü **Tamsayı** değerinden **Int64** değerine değiştirin.
7. **Biçim tasarımcısı** sayfasında, düzenlenebilir biçim bileşenini denetlemek için **Doğrula**'yı seçin.

    ![Biçim tasarımcısı sayfasında tür uyumluluğunu doğrulama.](./media/er-components-inspections-02.gif)

8. Doğrulama hatasının oluştuğunu göreceksiniz. Bu iletide, yapılandırılan ifadenin yalnızca **Int64** değerlerini kabul edebileceği belirtilri. Bu nedenle, **Tamsayı** türünün **X** veri modeli alanının değeri **Y** biçim öğesine girilemez.

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

**Sayısal** biçim öğesi veri türünü değiştirerek biçim yapısını güncelleştirin. Böylece veri türü, söz konusu öğenin bağlanması için yapılandırdığınız ifadenin veri türüyle eşleşir. Önceki örnek için, **X** biçim öğesinin **Sayısal tür** değerinin tekrar **Tamsayı** olarak değiştirilmesi gerekir.

#### <a name="option-2"></a>Seçenek 2

İfadeyi `model.X` değerinden `INT64VALUE(model.X)` değerine değiştirerek **X** biçim öğesinin biçim eşlemesini güncelleştirin.

## <a name="missing-configuration-element"></a><a id="i3"></a>Eksik yapılandırma öğesi

ER; bağlama ifadelerinin yalnızca düzenlenebilir ER bileşeninde yapılandırılmış veri kaynaklarını içerip içermediğini denetler. Düzenlenebilir ER bileşeninde bulunmayan bir veri kaynağı içeren her bağlama için ER İşlemler tasarımcısında veya ER model eşleme tasarımcısında bir doğrulama hatası oluşur.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER veri modelini ve ER model eşleme bileşenlerini eşzamanlı olarak yapılandırmaya başlayın.
2. Veri modeli ağacında **X** adlı bir alan ekleyin ve veri türü olarak **Tamsayı**'yı seçin.

    ![Veri modeli sayfasında X alanı ve Tamsayı veri türü ile veri modeli ağacı.](./media/er-components-inspections-01.png)

3. Model eşleme tasarımcısında **veri kaynakları** bölmesinde **Hesaplanan alan** türünün bir veri kaynağını ekleyin.
4. Yeni veri kaynağını **Y** olarak adlandırın ve `INTVALUE(100)` ifadesini içerecek şekilde yapılandırın.
5. **X**'i **Y**'ye bağlayın.
6. Model eşleme tasarımcısındaki **veri kaynakları** bölmesinde **Y** veri kaynağını silin.
7. **Model eşleme tasarımcısı** sayfasında, düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin.

    ![Model eşleme tasarımcısı sayfasında düzenlenebilir ER modeli eşleme bileşenini denetleme.](./media/er-components-inspections-03.gif)

8. Doğrulama hatasının oluştuğunu göreceksiniz. Bu iletide, **X** veri modeli alanı bağlamasının **Y** veri kaynağına başvuran yolu içerdiği ancak bu veri kaynağının bulunamadığı belirtilir.

### <a name="automatic-resolution"></a>Otomatik çözüm

Eksik veri kaynağı bağlamasını kaldırarak bu sorunu otomatik olarak düzeltmek için **Bağlamayı kaldır**'ı seçin.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

Var olmayan **Y** veri kaynağına başvurmayı durdurmak için **X** veri modelinin bağlamasını kaldırın.

#### <a name="option-2"></a>Seçenek 2

Model eşleme tasarımcısındaki **veri kaynakları** bölmesinde **Y** veri kaynağını tekrar ekleyin.

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a>FILTER işlevi içeren bir ifadenin yürütülebilirliği

Yerleşik [FILTER](er-functions-list-filter.md) ER işlevi, gerekli verileri kayıt listesi olarak almak için tek bir SQL çağrısı yaparak uygulama tablolarına, görünümlere ve veri varlıklarına erişmek için kullanılır. **Kayıt listesi** türündeki bir veri kaynağı, bu işlevin bağımsız değişkeni olarak kullanılır ve çağrı için uygulama kaynağını belirtir. ER, `FILTER` işlevinde başvurulan veri kaynağına doğrudan SQL sorgusu oluşturulup oluşturulamayacağını denetler. Doğrudan sorgu oluşturulamazsa ER model eşleme tasarımcısında bir doğrulama hatası oluşur. Aldığınız iletide, `FILTER` işlevini içeren ER ifadesinin çalışma zamanında çalıştırılamadığı belirtilir.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER model eşleme bileşenini yapılandırmaya başlayın.
2. **Dynamics 365 for Operations \\ Tablo kayıtları** türünde bir veri kaynağı ekleyin.
3. Yeni veri kaynağını **Vendor** olarak adlandırın. **Tablo** alanında, bu veri kaynağının VendTable tablosunu isteyeceğini belirtmek için **VendTable** seçeneğini belirleyin.
4. **Hesaplanan alan** türünde bir veri kaynağı ekleyin.
5. Yeni veri kaynağını **FilteredVendor** olarak adlandırın ve `FILTER(Vendor, Vendor.AccountNum="US-101")` ifadesini içerecek şekilde yapılandırın.
6. **Model eşleme tasarımcısı** sayfasında düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin ve **Vendor** veri kaynağındaki `FILTER(Vendor, Vendor.AccountNum="US-101")` ifadesinin sorgulanabildiğini doğrulayın.
7. Kırpılan satıcı hesap numarasını almak için **Hesaplanan alan** türünde iç içe bir alan ekleyerek **Vendor** veri kaynağını değiştirin.
8. Yeni iç içe alanı **$AccNumber** olarak adlandırın ve `TRIM(Vendor.AccountNum)` ifadesini içerecek şekilde yapılandırın.
9. **Model eşleme tasarımcısı** sayfasında düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin ve **Vendor** veri kaynağındaki `FILTER(Vendor, Vendor.AccountNum="US-101")` ifadesinin sorgulanabildiğini doğrulayın.

    ![FILTER işlevini içeren ifadenin Model eşleme tasarımcısı sayfasında sorgulanabildiğini doğrulama.](./media/er-components-inspections-04.gif)

10. **Vendor** veri kaynağı, **FilteredVendor** veri kaynağı ifadesinin doğrudan SQL deyimine çevrilmesine izin vermeyen **Hesaplanan alan** türünde iç içe alan içerdiğinden doğrulama hatası oluşur.

Aşağıdaki çizimde, uyarıyı yok sayıp model eşlemesini kullanmak üzere yapılandırılmış bir biçimi çalıştırmak için **Çalıştır**'ı seçerseniz oluşacak çalışma zamanı hatası gösterilir.

![Biçim tasarımcısı sayfasında düzenlenebilir biçimi çalıştırdığınızda oluşan çalışma zamanı hataları.](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

**Vendor** veri kaynağına, **Hesaplanan alan** türünde iç içe geçmiş bir alan eklemek yerine, **FilteredVendor** veri kaynağına **$AccNumber** iç içe alanını ekleyin ve bunu `TRIM(FilteredVendor.AccountNum)` ifadesini içerecek şekilde yapılandırın. Bu şekilde, `FILTER(Vendor, Vendor.AccountNum="US-101")` ifadesi SQL düzeyinde çalıştırılabilir ve daha sonra **$AccNumber** iç içe alanını hesaplayabilir.

#### <a name="option-2"></a>Seçenek 2

**FilteredVendor** veri kaynağı ifadesini, `FILTER(Vendor, Vendor.AccountNum="US-101")` yerine `WHERE(Vendor, Vendor.AccountNum="US-101")` olacak şekilde değiştirin. Büyük bir veri hacmi bulunan bir tablo (işlem tablosu) için ifadeyi değiştirmenizi önermeyiz çünkü bu durumda tüm kayıtlar getirilir ve gerekli kayıtların seçilmesi işlemi bellekte yapılır. Bu nedenle, bu yaklaşım düşük performansa neden olabilir. Daha fazla bilgi için bkz. [WHERE ER işlevi](er-functions-list-where.md).

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a>GROUPBY veri kaynağının yürütülebilirliği

**GROUPBY** veri kaynağı, genellikle her grup üzerinde bir veya daha fazla toplama yapmak amacıyla sorgu sonucunu kayıt gruplarına böler. Her bir **GROUPBY** veri kaynağı, veritabanı düzeyinde veya bellekte çalışacak şekilde yapılandırılabilir. Bir **GROUPBY** veri kaynağı veritabanı düzeyinde çalışacak şekilde yapılandırıldığında ER, veri kaynağında başvurulan veri kaynağına doğrudan bir SQL sorgusu oluşturulup oluşturulamayacağını denetler. Doğrudan sorgu oluşturulamazsa ER model eşleme tasarımcısında bir doğrulama hatası oluşur. Aldığınız iletide, yapılandırılan **GROUPBY** veri kaynağının çalışma zamanında çalıştırılamayacağı belirtilir.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER model eşleme bileşenini yapılandırmaya başlayın.
2. **Dynamics 365 for Operations \\ Tablo kayıtları** türünde bir veri kaynağı ekleyin.
3. Yeni veri kaynağını **Trans** olarak adlandırın. **Tablo** alanında, bu veri kaynağının **VendTrans** tablosunu isteyeceğini belirtmek için VendTrans'ı seçin.
4. **Gruplandırma ölçütü** türünde bir veri kaynağı ekleyin.
5. Yeni veri kaynağını **GroupedTrans** olarak adlandırın ve aşağıdaki şekilde yapılandırın:

    - Gruplandırılması gereken kayıtların kaynağı olarak **Trans** veri kaynağını seçin.
    - **Yürütme konumu** alanında, bu veri kaynağını veritabanı düzeyinde çalıştırmak istediğinizi belirtmek için **Sorgu**'yu seçin.

    !["Gruplama Ölçütü" parametrelerini düzenle sayfasında veri kaynağını yapılandırma.](./media/er-components-inspections-05a.gif)

6. **Model eşleme tasarımcısı** sayfasında düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin ve yapılandırılan **GroupedTrans** veri kaynağının sorgulanabildiğini doğrulayın.
7. Kırpılan satıcı hesap numarasını almak için **Hesaplanan alan** türünde iç içe bir alan ekleyerek **Trans** veri kaynağını değiştirin.
8. Yeni veri kaynağını **$AccNumber** olarak adlandırın ve `TRIM(Trans.AccountNum)` ifadesini içerecek şekilde yapılandırın.

    ![Model eşleme tasarımcı sayfasında veri kaynağını yapılandırma.](./media/er-components-inspections-05a.png)

9. **Model eşleme tasarımcısı** sayfasında düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin ve yapılandırılan **GroupedTrans** veri kaynağının sorgulanabildiğini doğrulayın.

    ![ER model eşleme bileşenini doğrulama ve GroupedTrans veri kaynağının Model eşleme tasarımsıcı sayfasında sorgulanabildiğini doğrulama.](./media/er-components-inspections-05b.png)

10. **Trans** veri kaynağı, **GroupedTrans** veri kaynağı çağrısının doğrudan SQL deyimine çevrilmesine izin vermeyen **Hesaplanan alan** türünde iç içe alan içerdiğinden doğrulama hatası oluşur.

Aşağıdaki çizimde, uyarıyı yok sayıp model eşlemesini kullanmak üzere yapılandırılmış bir biçimi çalıştırmak için **Çalıştır**'ı seçerseniz oluşacak çalışma zamanı hatası gösterilir.

![Biçim tasarımcısı sayfasında uyarı yok sayıldığında oluşan çalışma zamanı hataları.](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

**Trans** veri kaynağına, **Hesaplanan alan** türünde iç içe geçmiş bir alan eklemek yerine, **GroupedTrans** veri kaynağının **GroupedTrans.lines** öğesi için **$AccNumber** iç içe alanını ekleyin ve bunu `TRIM(GroupedTrans.lines.AccountNum)` ifadesini içerecek şekilde yapılandırın. Bu şekilde, **GroupedTrans** veri kaynağı SQL düzeyinde çalıştırılabilir ve daha sonra **$AccNumber** iç içe alanını hesaplayabilir.

#### <a name="option-2"></a>Seçenek 2

**GroupedTrans** veri kaynağı için **Yürütme konumu** alanının değerini **Sorgu** yerine **Bellek içi** olarak değiştirin. Büyük bir veri hacmi bulunan bir tablo (işlem tablosu) için değeri değiştirmenizi önermeyiz çünkü bu durumda tüm kayıtlar getirilir ve gruplandırma ile toplama bellekte yapılır. Bu nedenle, bu yaklaşım düşük performansa neden olabilir.

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a>JOIN veri kaynağının yürütülebilirliği

[JOIN](er-join-data-sources.md) veri kaynağı birleştirme, ilgili alanlara göre iki veya daha fazla veri tabanı tablosuna ait kayıtları birleştirir. Her bir **JOIN** veri kaynağı, veritabanı düzeyinde veya bellekte çalışacak şekilde yapılandırılabilir. Bir **JOIN** veri kaynağı veritabanı düzeyinde çalışacak şekilde yapılandırıldığında ER, veri kaynağında başvurulan veri kaynaklarına doğrudan bir SQL sorgusu oluşturulup oluşturulamayacağını denetler. Başvurulan veri kaynaklarından en az birine doğrudan SQL sorgusu oluşturulamazsa ER model eşleme tasarımcısında bir doğrulama hatası oluşur. Aldığınız iletide, yapılandırılan **JOIN** veri kaynağının çalışma zamanında çalıştırılamayacağı belirtilir.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER model eşleme bileşenini yapılandırmaya başlayın.
2. **Dynamics 365 for Operations \\ Tablo kayıtları** türünde bir veri kaynağı ekleyin.
3. Yeni veri kaynağını **Vendor** olarak adlandırın. **Tablo** alanında, bu veri kaynağının VendTable tablosunu isteyeceğini belirtmek için **VendTable** seçeneğini belirleyin.
4. **Dynamics 365 for Operations \\ Tablo kayıtları** türünde bir veri kaynağı ekleyin.
5. Yeni veri kaynağını **Trans** olarak adlandırın. **Tablo** alanında, bu veri kaynağının **VendTrans** tablosunu isteyeceğini belirtmek için VendTrans'ı seçin.
6. **Vendor** veri kaynağının iç içe alanı olarak **Hesaplanan alan** türünde bir veri kaynağı ekleyin.
7. Yeni veri kaynağını **FilteredTrans** olarak adlandırın ve `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` ifadesini içerecek şekilde yapılandırın.
8. **Birleştirme** türünde bir veri kaynağı ekleyin.
9. Yeni veri kaynağını **JoinedList** olarak adlandırın ve aşağıdaki şekilde yapılandırın:

    1. **Vendor** veri kaynağını birleştirilecek ilk kayıt kümesi olarak ekleyin.
    2. **Vendor.FilteredTrans** veri kaynağını birleştirilecek ikinci kayıt kümesi olarak ekleyin. Tür olarak **INNER** türünü seçin.
    3. **Yürütme** alanında, bu veri kaynağını veritabanı düzeyinde çalıştırmak istediğinizi belirtmek için **Sorgu**'yu seçin.

    ![Birleştirme tasarımcısı sayfasında veri kaynağını yapılandırma.](./media/er-components-inspections-06a.gif)

10. **Model eşleme tasarımcısı** sayfasında düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin ve yapılandırılan **JoinedList** veri kaynağının sorgulanabildiğini doğrulayın.
11. **Vendor.FilteredTrans** veri kaynağı ifadesini, `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` yerine `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` olacak şekilde değiştirin.
12. **Model eşleme tasarımcısı** sayfasında düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin ve yapılandırılan **JoinedList** veri kaynağının sorgulanabildiğini doğrulayın.

    ![Düzenlenebilir model eşleme bileşenini doğrulama ve JoinedList veri kaynağının Model eşleme tasarımcısı sayfasında sorgulanabildiğini doğrulama.](./media/er-components-inspections-06b.png)

13. **Vendor.FilteredTrans** veri kaynağı ifadesi doğrudan SQL çağrısına çevrilemediği için doğrulama hatası oluştuğuna dikkat edin. Ek olarak, doğrudan SQL çağrısı **JoinedList** veri kaynağı için çağrının doğrudan SQL deyimine çevrilmesine izin vermez.

    ![Model eşleme tasarımcısı sayfasında JoinedList veri kaynağı doğrulamasının başarısız olmasından kaynaklanan çalışma zamanı hataları.](./media/er-components-inspections-06c.png)

Aşağıdaki çizimde, uyarıyı yok sayıp model eşlemesini kullanmak üzere yapılandırılmış bir biçimi çalıştırmak için **Çalıştır**'ı seçerseniz oluşacak çalışma zamanı hatası gösterilir.

![Biçim tasarımcısı sayfasında düzenlenebilir biçimi çalıştırma.](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

Uyarıda tavsiye edilen şekilde, **Vendor.FilteredTrans** veri kaynağı ifadesini `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` yerine tekrar `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` olarak değiştirin.

![Model eşleme tasarımcısı sayfasında güncelleştirilmiş veri kaynağı ifadesi.](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a>Seçenek 2

**JoinedList** veri kaynağı için **Yürütme** alanının değerini **Sorgu** yerine **Bellek içi** olarak değiştirin. Büyük bir veri hacmi bulunan bir tablo (işlem tablosu) için değeri değiştirmenizi önermeyiz çünkü bu durumda tüm kayıtlar getirilir ve birleştirme bellekte gerçekleşir. Bu nedenle, bu yaklaşım düşük performansa neden olabilir. Bu riski size bildiren bir doğrulama uyarısı gösterilir.

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a>FILTER ile WHERE işlevinin tercih edilirliği

Yerleşik [FILTER](er-functions-list-filter.md) ER işlevi, gerekli verileri kayıt listesi olarak almak için tek bir SQL çağrısı yaparak uygulama tablolarına, görünümlere ve veri varlıklarına erişmek için kullanılır. [WHERE](er-functions-list-where.md) işlevi, belirli bir kaynaktaki tüm kayıtları getirir ve kayıt seçimi işlemini bellekte gerçekleştirir. **Kayıt listesi** türündeki bir veri kaynağı, her iki işlevin de bağımsız değişkeni olarak kullanılır ve kayıt alma işlemi için bir kaynak belirtir. ER, **WHERE** işlevinde başvurulan veri kaynağına doğrudan SQL çağrısı oluşturulup oluşturulamayacağını denetler. Doğrudan çağrı oluşturulamazsa ER model eşleme tasarımcısında bir doğrulama uyarısı oluşur. Aldığınız iletide, verimliliği artırmaya yardımcı olmak için **WHERE** işlevi yerine **FILTER** işlevini kullanmanız önerilir.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER model eşleme bileşenini yapılandırmaya başlayın.
2. **Dynamics 365 for Operations \\ Tablo kayıtları** türünde bir veri kaynağı ekleyin.
3. Yeni veri kaynağını **Trans** olarak adlandırın. **Tablo** alanında, bu veri kaynağının **VendTrans** tablosunu isteyeceğini belirtmek için VendTrans'ı seçin.
4. **Vendor** veri kaynağının iç içe alanı olarak **Hesaplanan alan** türünde bir veri kaynağı ekleyin.
5. Yeni veri kaynağını **FilteredTrans** olarak adlandırın ve `WHERE(Trans, Trans.AccountNum="US-101")` ifadesini içerecek şekilde yapılandırın.
6. **Dynamics 365 for Operations \\ Tablo kayıtları** türünde bir veri kaynağı ekleyin.
7. Yeni veri kaynağını **Vendor** olarak adlandırın. **Tablo** alanında, bu veri kaynağının VendTable tablosunu isteyeceğini belirtmek için **VendTable** seçeneğini belirleyin.
8. **Hesaplanan alan** türünde bir veri kaynağı ekleyin.
9. Yeni veri kaynağını **FilteredVendor** olarak adlandırın ve `WHERE(Vendor, Vendor.AccountNum="US-101")` ifadesini içerecek şekilde yapılandırın.
10. **Model eşleme tasarımcısı** sayfasında, düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin.

    ![Model eşleme tasarımcısı sayfasında düzenlenebilir model eşleme bileşenini denetleme.](./media/er-components-inspections-07a.png)

11. Doğrulama uyarılarında, **FilteredVendor** ve **FilteredTrans** veri kaynakları için **WHERE** işlevi yerine **FILTER** işlevini kullanmanızın önerildiğine dikkat edin.

    ![Model eşleme tasarımcısı sayfasında WHERE işlevi yerine FILTER işlevinin kullanılması için öneri.](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu denetim türünün **Uyarılar** sekmesindeki ızgarada gösterilen tüm veri kaynakları ifadelerinde **WHERE** işlevini **FILTER** işlevi ile otomatik olarak değiştirmek için **Düzelt**'i seçin.

Alternatif olarak, ızgarada tek bir uyarı satırını seçebilir ve ardından **Seçilenleri düzelt**'i seçebilirsiniz. Bu durumda, ifade yalnızca seçilen uyarıda belirtilen veri kaynağında otomatik olarak değiştirilir.

![Model eşleme tasarımcısı sayfasında WHERE işlevini FILTER işleviyle otomatik olarak değiştirmek için Düzelt'i seçme.](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a>El ile çözüm

**WHERE** işlevini **FILTER** işleviyle değiştirerek, doğrulama ızgarasındaki tüm veri kaynaklarının ifadelerini el ile ayarlayabilirsiniz.

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a>ALLITEMSQUERY ile ALLITEMS işlevinin tercih edilirliği

Yerleşik [ALLITEMS](er-functions-list-allitems.md)ve [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ER işlevleri, belirtilen yolla eşleşen tüm öğelerin temsil edildiği bir kayıt listesinden oluşan düzleştirilmiş **Kayıt listesi** değerini döndürür. ER, **ALLITEMS** işlevinde başvurulan veri kaynağına doğrudan SQL çağrısı oluşturulup oluşturulamayacağını denetler. Doğrudan çağrı oluşturulamazsa ER model eşleme tasarımcısında bir doğrulama uyarısı oluşur. Aldığınız iletide, verimliliği artırmaya yardımcı olmak için **ALLITEMS** işlevi yerine **ALLITEMSQUERY** işlevini kullanmanız önerilir.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER model eşleme bileşenini yapılandırmaya başlayın.
2. **Dynamics 365 for Operations \\ Tablo kayıtları** türünde bir veri kaynağı ekleyin.
3. Yeni veri kaynağını **Vendor** olarak adlandırın. **Tablo** alanında, bu veri kaynağının VendTable tablosunu isteyeceğini belirtmek için **VendTable** seçeneğini belirleyin.
4. Birden fazla satıcıyla ilgili kayıtları almak için **Hesaplanan alan** türünde bir veri kaynağı ekleyin.
5. Yeni veri kaynağını **FilteredVendor** olarak adlandırın ve `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))` ifadesini içerecek şekilde yapılandırın.
6. Filtrelenen tüm satıcıların hareketlerini almak için **Hesaplanan alan** türünde bir veri kaynağı ekleyin.
7. Yeni veri kaynağını **FilteredVendorTrans** olarak adlandırın ve `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')` ifadesini içerecek şekilde yapılandırın.
8. **Model eşleme tasarımcısı** sayfasında, düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin.

    ![Model eşleme tasarımcısı sayfasında düzenlenebilir model eşleme bileşenini denetleme.](./media/er-components-inspections-08a.png)

9. Doğrulama uyarısının oluştuğunu göreceksiniz. Bu iletide, **FilteredVendorTrans** veri kaynağı için **ALLITEMS** işlevi yerine **ALLITEMSQUERY** işlevini kullanmanız önerilir.

    ![Model eşleme tasarımcısı sayfasında ALLITEMS işlevi yerine ALLITEMSQUERY işlevinin kullanılması için öneri.](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu denetim türünün **Uyarılar** sekmesindeki ızgarada gösterilen tüm veri kaynakları ifadelerinde **ALLITEMS** işlevini **ALLITEMSQUERY** işlevi ile otomatik olarak değiştirmek için **Düzelt**'i seçin.

Alternatif olarak, ızgarada tek bir uyarı satırını seçebilir ve ardından **Seçilenleri düzelt**'i seçebilirsiniz. Bu durumda, ifade yalnızca seçilen uyarıda belirtilen veri kaynağında otomatik olarak değiştirilir.

![Model eşleme tasarımcısı sayfasında Seçilenleri düzelt'i seçme.](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a>El ile çözüm

**ALLITEMS** işlevini **ALLITEMSQUERY** işleviyle değiştirerek, doğrulama ızgarasında belirtilen tüm veri kaynaklarının ifadelerini el ile ayarlayabilirsiniz.

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a>Boş liste durumlarının dikkate alınması

**Kayıt listesi** türünde bir veri kaynağının alan değerini almak için ER biçim veya model eşleme bileşenini yapılandırabilirsiniz. ER, var olmayan bir kayıt alanından değer getirildiğinde çalışma zamanı hatalarını önlemek için, çağrılan veri kaynağının kayıt içermediği (boş olduğu) durumların tasarım tarafından dikkate alınıp alınmadığını denetler.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER veri modeli, ER model eşleme ve ER biçim bileşenlerini eşzamanlı olarak yapılandırmaya başlayın.
2. Veri modeli ağacında, **Root3** adlı bir kök öğe ekleyin.
3. **Kayıt listesi** türünde iç içe bir öğe ekleyerek **Root3** öğesini değiştirin.
4. Yeni iç içe öğeyi **Vendor** olarak adlandırın.
5. **Vendor** öğesini aşağıdaki şekilde değiştirin:

    - **Dize** türünde iç içe bir alan ekleyin ve bu alanı **Name** olarak adlandırın.
    - **Dize** türünde iç içe bir alan ekleyin ve bu alanı **AccountNumber** olarak adlandırın.

    ![Veri modeli sayfasında iç içe alanlar ekleme.](./media/er-components-inspections-09a.png)

6. Model eşleme tasarımcısında **veri kaynakları** bölmesinde **Dynamics 365 for Operations\\Tablo kayıtları** türünün veri kaynağını ekleyin.
7. Yeni veri kaynağını **Vendor** olarak adlandırın. **Tablo** alanında, bu veri kaynağının VendTable tablosunu isteyeceğini belirtmek için **VendTable** seçeneğini belirleyin.
8. Çalışma zamanı iletişim kutusunda bir satıcı hesabı aramak için **Genel \\ Kullanıcı girişi parametresi** türünde bir veri kaynağı ekleyin.
9. Yeni veri kaynağını **RequestedAccountNum** olarak adlandırın. **Etiket** alanına **Satıcı hesap numarası**'nı girin. **İşlemler veri türü adı** alanında, **Açıklama** varsayılan değerini boş bırakın.
10. Sorgulanan satıcıyı filtrelemek için **Hesaplanan alan** türünde bir veri kaynağı ekleyin.
11. Yeni veri kaynağını **FilteredVendor** olarak adlandırın ve `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)` ifadesini içerecek şekilde yapılandırın.
12. Veri modeli öğelerini yapılandırılan veri kaynaklarına aşağıdaki şekilde bağlayın:

    - **FilteredVendor** öğesini **Vendor** öğesine bağlayın.
    - **FilteredVendor.AccountNum** öğesini **Vendor.AccountNumber** öğesine bağlayın.
    - **FilteredVendor.'name()'** öğesini **Vendor.Name** öğesine bağlayın.

    ![Model eşleme tasarımcısı sayfasında veri modeli öğelerini yapılandırma.](./media/er-components-inspections-09b.png)

13. Biçim yapısı ağacında, satıcı ayrıntılarını içeren bir giden belgeyi XML biçiminde oluşturmak için aşağıdaki öğeleri ekleyin:

    1. **Statement** kök XML öğesini ekleyin.
    2. **Statement** XML öğesi için, iç içe geçmiş **Party** XML öğesini ekleyin.
    3. **Party** XML öğesi için, aşağıdaki iç içe XML özniteliklerini ekleyin:

        - Kuruluş adı
        - AccountNum

14. Biçim öğelerini sağlanan veri kaynaklarına aşağıdaki şekilde bağlayın:

    - **Statement\\Party\\Name** biçim öğesini **model.Vendor.Name** veri kaynağı alanına bağlayın.
    - **Statement\\Party\\AccountNum** biçim öğesini **model.Vendor.AccountNumber** veri kaynağı alanına bağlayın.

15. **Biçim tasarımcısı** sayfasında, düzenlenebilir biçim bileşenini denetlemek için **Doğrula**'yı seçin.

    ![Biçim tasarımcısı sayfasında veri kaynaklarına bağladığınız biçim öğelerini doğrulama.](./media/er-components-inspections-09c.png)

16. Doğrulama hatasının oluştuğunu göreceksiniz. Bu iletide, `model.Vendor` listesi boşsa çalışma zamanında yapılandırılmış **Statement\\Party\\Name** ve **Statement\\Party\\AccountNum** biçim bileşenleri için bir hata oluşabileceği belirtilir.

    ![Yapılandırılan biçim bileşenleri için olası bir hata hakkındaki doğrulama hatası.](./media/er-components-inspections-09d.png)

Aşağıdaki çizimde, uyarıyı yok sayıp biçimi çalıştırmak için **Çalıştır**'ı seçer ve var olmayan bir satıcının hesap numarasını seçerseniz oluşacak çalışma zamanı hatası gösterilir. İstenen satıcı var olmadığından `model.Vendor` listesi boş olacaktır (kayıt içermeyecektir).

![Biçim eşleme çalışırken oluşan çalışma zamanı hataları.](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a>Otomatik çözüm

**Uyarılar** sekmesindeki ızgarada seçili satır için **Bağlamayı Kaldır**'ı seçebilirsiniz. **Yol** sütununda işaret edilen bağ, biçim öğelerinden otomatik olarak kaldırılır.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

**Statement\\Party\\Name** biçim öğesini `model.Vendor` veri kaynağı öğesine bağlayabilirsiniz. Çalışma zamanında bu bağ, önce `model.Vendor` veri kaynağını çağırır. `model.Vendor` boş bir kayıt listesi döndürürse iç içe geçmiş biçim bileşenleri çalıştırılmaz. Bu nedenle, bu biçim yapılandırması için herhangi bir doğrulama uyarısı oluşmaz.

![Biçim tasarımcısı sayfasında biçim öğesini veri kaynağı öğesine bağlama.](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a>Seçenek 2

**Statement\\Party\\Name** biçim bileşenini bağlamasını `model.Vendor.Name` öğesinden `FIRSTORNULL(model.Vendor).Name` olarak değiştirin. Güncelleştirilmiş bağ, **Kayıt listesi** türündeki `model.Vendor` veri kaynağının ilk kaydını koşullu olarak **Kayıt** türündeki yeni bir veri kaynağına dönüştürür. Bu yeni veri kaynağı aynı alan kümesini içerir.

- `model.Vendor` veri kaynağında en az bir kayıt varsa söz konusu kaydın alanları `model.Vendor` veri kaynağının ilk kaydındaki alanların değerleriyle doldurulur. Bu durumda, güncelleştirilen bağlama satıcı adını döndürür.
- Aksi durumda, kaydın oluşturulan her alanı söz konusu alan veri türünün varsayılan değeriyle doldurulur. Bu durumda, **Dize** veri türünün varsayılan değeri olan boş dize döndürülür.

Bu nedenle, **Statement\\Party\\Name** biçim bileşeni `FIRSTORNULL(model.Vendor).Name` ifadesine bağlandığında doğrulama uyarıları oluşmaz.

![Biçim tasarımcısı sayfasında değiştirilen bağlama doğrulama uyarıların çözer.](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a>Seçenek 3

**Kayıt listesi** türündeki `model.Vendor` veri kaynağı kayıt döndürmediğinde oluşturulan belgeye girilen veriyi açıkça belirtmek istiyorsanız (bu örnekte **Yok** metni), **Statement\\Party\\Name** biçim öğesinin bağlamasını `model.Vendor.Name` ifadesinden `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")` ifadesine değiştirin. Şu ifadeyi de kullanabilirsiniz: `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.

### <a name="additional-consideration"></a><a id="i9a"></a>Dikkate alınması gereken ek hususlar

Denetleme de başka bir olası sorun hakkında daha uyarı alırsınız. Varsayılan olarak, **Statement\\Party\\Name** ve **Statement\\Party\\AccountNum** biçim öğelerini **Kayıt listesi** türündeki `model.Vendor` veri kaynağının uygun alanlarına bağlarken, bu bağlar çalıştırılır ve liste boş değilse `model.Vendor` veri kaynağının ilk kaydındaki uygun alanların değerlerini alır.

**Statement\\Party** biçim öğesini `model.Vendor` veri kaynağına bağlamadığınız için biçim yürütme sırasında **Statement\\Party** öğesi `model.Vendor` veri kaynağının her kaydı için tekrarlanmaz. Bunun yerine, kayıt listesi birden fazla kayıt içeriyorsa oluşturulan belge listenin yalnızca ilk kaydındaki bilgilerle doldurulur. Bu nedenle, biçimin oluşturulan belgeyi `model.Vendor` veri kaynağındaki tüm satıcılar hakkındaki bilgilerle doldurması amaçlanıyorsa sorun oluşabilir. Bu sorunu gidermek için **Statement\\Party** öğesini `model.Vendor` veri kaynağına bağlayın.

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a>FILTER işlevi içeren bir ifadenin yürütülebilirliği (önbelleğe alma)

[FILTER](er-functions-list-filter.md) ve [ALLITEMSQUERY](er-functions-list-allitemsquery.md) dahil pek çok ER işlevi, gerekli verileri kayıt listesi olarak almak için tek bir SQL çağrısı yaparak uygulama tablolarına, görünümlere ve veri varlıklarına erişmek için kullanılır. **Kayıt listesi** türündeki bir veri kaynağı, bu işlevlerden her birinin bağımsız değişkeni olarak kullanılır ve çağrı için uygulama kaynağını belirtir. ER, bu işlevlerden birinde başvurulan veri kaynağına doğrudan SQL çağrısı oluşturulup oluşturulamayacağını denetler. Veri kaynağı [önbelleğe alınmış](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace) olarak işaretlendiğinden doğrudan çağrı oluşturulamazsa ER model eşleme tasarımcısında bir doğrulama hatası oluşur. Aldığınız iletide, bu işlevlerden birini içeren ER ifadesinin çalışma zamanında çalıştırılamadığı belirtilir.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER model eşleme bileşenini yapılandırmaya başlayın.
2. **Dynamics 365 for Operations \\ Tablo kayıtları** türünde bir veri kaynağı ekleyin.
3. Yeni veri kaynağını **Vendor** olarak adlandırın. **Tablo** alanında, bu veri kaynağının VendTable tablosunu isteyeceğini belirtmek için **VendTable** seçeneğini belirleyin.
4. Çalışma zamanı iletişim kutusunda bir satıcı hesabı aramak için **Genel \\ Kullanıcı girişi parametresi** türünde bir veri kaynağı ekleyin.
5. Yeni veri kaynağını **RequestedAccountNum** olarak adlandırın. **Etiket** alanına **Satıcı hesap numarası**'nı girin. **İşlemler veri türü adı** alanında, **Açıklama** varsayılan değerini boş bırakın.
6. Sorgulanan satıcıyı filtrelemek için **Hesaplanan alan** türünde bir veri kaynağı ekleyin.
7. Yeni veri kaynağını **FilteredVendor** olarak adlandırın ve `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)` ifadesini içerecek şekilde yapılandırın.
8. Yapılandırılan **Vendor** veri kaynağını önbelleğe alınmış olarak işaretleyin.

    ![Model eşleme tasarımcısı sayfasında model eşleme bileşenini yapılandırma.](./media/er-components-inspections-10a.gif)

9. **Model eşleme tasarımcısı** sayfasında, düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin.

    ![Model eşleme tasarımcısı sayfasında ön belleğe alınan Satıcı veri kaynağına uygulanan FILTER işlevini doğrulama.](./media/er-components-inspections-10a.png)

10. Doğrulama hatasının oluştuğunu göreceksiniz. İletide, **FILTER** işlevinin önbelleğe alınan **Vendor** veri kaynağına uygulanamayacağı belirtilir.

Aşağıdaki çizimde, uyarıyı yok sayıp biçimi çalıştırmak için **Çalıştır**'ı seçerseniz oluşacak çalışma zamanı hatası gösterilir.

![Biçim tasarımcısı sayfasında biçim eşleme çalıştırması sırasında oluşan çalışma zamanı hatası.](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

**Vendor** veri kaynağından **Önbellek** işaretini kaldırın. **FilteredVendor** veri kaynağı yürütülebilir hale gelir ancak **FilteredVendor** veri kaynağı her çağrıldığında VendTable tablosunda başvurulan **Vendor** veri kaynağına erişilecektir.

#### <a name="option-2"></a>Seçenek 2

**FilteredVendor** veri kaynağı ifadesini, `FILTER(Vendor, Vendor.AccountNum="US-101")` yerine `WHERE(Vendor, Vendor.AccountNum="US-101")` olacak şekilde değiştirin. Bu durumda, VendTable tablosunda başvurulan **Vendor** veri kaynağına yalnızca **Vendor** veri kaynağı ilk çağrıldığında erişilir. Ancak, kayıt seçimi bellekte yapılır. Bu nedenle, bu yaklaşım düşük performansa neden olabilir.

## <a name="missing-binding"></a><a id="i11"></a>Eksik bağlama

Bir ER biçimi bileşenini yapılandırdığınızda ER biçimi için varsayılan veri kaynağı olarak temel ER veri modeli sunulur. Yapılandırılmış ER biçimi çalıştırıldığında, temel model için [varsayılan model eşlemesi](er-country-dependent-model-mapping.md) veri modelini uygulama verileriyle doldurmak için kullanılır. Bir biçim öğesini, düzenlenebilir biçim için varsayılan model eşlemesi olarak seçilmiş olan model eşleştirmesindeki herhangi bir veri kaynağıyla ilişkili olmayan bir veri modeli öğesine bağlarsanız, ER biçim tasarımcısı bir uyarı görüntüler. Çalıştırılan biçim bağlı öğeyi uygulama verileriyle dolduramayacağından, bu bağlama türü çalışma zamanında çalıştırılamaz. Bu nedenle, çalışma zamanında hata oluşur.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER veri modeli, ER model eşleme ve ER biçim bileşenlerini eşzamanlı olarak yapılandırmaya başlayın.
2. Veri modeli ağacında, **Root3** adlı bir kök öğe ekleyin.
3. **Kayıt listesi** türünde yeni bir iç içe bir öğe ekleyerek **Root3** öğesini değiştirin.
4. Yeni iç içe öğeyi **Vendor** olarak adlandırın.
5. **Vendor** öğesini aşağıdaki şekilde değiştirin:

    - **Dize** türünde iç içe bir alan ekleyin ve bu alanı **Name** olarak adlandırın.
    - **Dize** türünde iç içe bir alan ekleyin ve bu alanı **AccountNumber** olarak adlandırın.

    ![Veri modeli sayfasında Satıcı öğesine iç içe alanlar ekleme.](./media/er-components-inspections-11a.png)

6. Model eşleme tasarımcısında **veri kaynakları** bölmesinde **Dynamics 365 for Operations\\Tablo kayıtları** türünün veri kaynağını ekleyin.
7. Yeni veri kaynağını **Vendor** olarak adlandırın. **Tablo** alanında, bu veri kaynağının VendTable tablosunu isteyeceğini belirtmek için **VendTable** seçeneğini belirleyin.
8. Çalışma zamanı iletişim kutusunda bir satıcı hesabı hakkında sorgu oluşturmak için **Genel \\ Kullanıcı girişi parametresi** türünde bir veri kaynağı ekleyin.
9. Yeni veri kaynağını **RequestedAccountNum** olarak adlandırın. **Etiket** alanına **Satıcı hesap numarası**'nı girin. **İşlemler veri türü adı** alanında, **Açıklama** varsayılan değerini boş bırakın.
10. Sorgulanan satıcıyı filtrelemek için **Hesaplanan alan** türünde bir veri kaynağı ekleyin.
11. Yeni veri kaynağını **FilteredVendor** olarak adlandırın ve `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)` ifadesini içerecek şekilde yapılandırın.
12. Veri modeli öğelerini yapılandırılan veri kaynaklarına aşağıdaki şekilde bağlayın:

    - **FilteredVendor** öğesini **Vendor** öğesine bağlayın.
    - **FilteredVendor.AccountNum** öğesini **Vendor.AccountNumber** öğesine bağlayın.

    > [!NOTE]
    > **Vendor.Name** veri modeli alanı bağlanmamış olarak kalır.

    ![Yapılandırılan veri kaynaklarına bağlı veri modeli öğeleri ve Model eşleme tasarımcısı sayfasındaki bağlanmamış olarak kalan veri modeli öğesi.](./media/er-components-inspections-11b.png)

13. Biçim yapısı ağacında, sorgu oluşturulan satıcıların ayrıntılarını içeren bir giden belgeyi XML biçiminde oluşturmak için aşağıdaki öğeleri ekleyin:

    1. **Statement** kök XML öğesini ekleyin.
    2. **Statement** XML öğesi için, iç içe geçmiş **Party** XML öğesini ekleyin.
    3. **Party** XML öğesi için, aşağıdaki iç içe XML özniteliklerini ekleyin:

        - Kuruluş adı
        - AccountNum

14. Biçim öğelerini sağlanan veri kaynaklarına aşağıdaki gibi bağlayın:

    - **Statement\\Party** biçim öğesini `model.Vendor` veri kaynağı öğesine bağlayın.
    - **Statement\\Party\\Name** biçim öğesini **model.Vendor.Name** veri kaynağı alanına bağlayın.
    - **Statement\\Party\\AccountNum** biçim öğesini **model.Vendor.AccountNumber** veri kaynağı alanına bağlayın.

15. **Biçim tasarımcısı** sayfasında, düzenlenebilir biçim bileşenini denetlemek için **Doğrula**'yı seçin.

    ![Biçim tasarımcısı sayfasında ER biçimi bileşenini doğrulama.](./media/er-components-inspections-11c.png)

16. Doğrulama uyarısının oluştuğunu göreceksiniz. Bu iletide, **model.Vendor.Name** veri kaynağı alanının, biçim tarafından kullanılmak üzere yapılandırılan model eşlemesindeki hiçbir veri kaynağına bağlı olmadığı belirtilir. Bu nedenle, **Statement\\Party\\Name** biçim öğesi çalışma zamanında doldurulamayabilir ve çalışma zamanı hatası oluşabilir.

    ![Biçim tasarımcısı sayfasında ER biçimi bileşenini doğrulama.](./media/er-components-inspections-11d.png)

Aşağıdaki çizimde, uyarıyı yok sayıp biçimi çalıştırmak için **Çalıştır**'ı seçerseniz oluşacak çalışma zamanı hatası gösterilir.

![Biçim tasarımcısı sayfasında düzenlenebilir biçimi çalıştırma.](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

**model.Vendor.Name** veri kaynağı alanı için bağlama ekleyerek, yapılandırılan model eşlemesini değiştirin.

#### <a name="option-2"></a>Seçenek 2

**Statement\\Party\\Name** biçim öğesi için bağı kaldırarak, yapılandırılan biçimi değiştirin.

## <a name="not-linked-template"></a><a id="i12"></a>Bağlanmamış şablon

Bir ER biçimi bileşenini giden belge oluşturmak için şablon kullanacak şekilde [el ile](er-fillable-excel.md#manual-entry) yapılandırdığınızda **Excel\\Dosya** bileşenini el ile eklemeniz, gerekli şablonu düzenlenebilir bileşeninin eki olarak eklemeniz ve eklenen **Excel\\Dosya** bileşeninde eki seçmeniz gerekir. Bu şekilde, eklenen öğenin çalışma zamanında seçili şablonu dolduracağını belirtirsiniz. **Taslak** [durumundaki](general-electronic-reporting.md#component-versioning) bir biçim bileşeni sürümünü yapılandırdığınızda, düzenlenebilir bileşene birkaç şablon ekleyebilirsiniz ve ER biçimini çalıştırmak için **Excel\\Dosya** öğesinde her bir şablonu seçebilirsiniz. Bu şekilde çalışma zamanında farklı şablonların nasıl doldurulduğunu görebilirsiniz. Herhangi bir **Excel\\Dosya** öğesi içinde seçili olmayan şablonlarınız varsa ER biçim tasarımcısı, düzenlenebilir ER biçim bileşeni sürümünün durumu **Taslak** iken **Tamamlandı** olarak değiştirildiğinde bu şablonların düzenlenebilir ER biçimi bileşeni sürümünden silineceği hakkında sizi uyarır.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER biçim eşleme bileşenini yapılandırmaya başlayın.
2. Biçim yapısı ağacında, **Excel\\Dosya** öğesini ekleyin.
3. Yeni eklediğiniz **Excel\\File** için ek olarak **A.xlsx** adında bir Excel çalışma kitabı dosyası ekleyin. ER biçim şablonlarının depolanmasını belirtmek için [ER parametrelerinde](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) yapılandırılan belge türünü kullanın.
4. **Excel\\File** için ek olarak **B.xlsx** adında başka bir Excel çalışma kitabı dosyası ekleyin. A çalışma kitabı dosyası için kullanılan belge türünü kullanın.
5. **Excel\\Dosya** öğesinde, A çalışma kitabı dosyasını seçin.
6. **Biçim tasarımcısı** sayfasında, düzenlenebilir biçim bileşenini denetlemek için **Doğrula**'yı seçin.

    ![Biçim tasarımcısı sayfasındaki çalışma kitabı dosyasının düzenlenebilir biçim bileşenini doğrulama.](./media/er-components-inspections-12a.gif)

7. Doğrulama uyarısının oluştuğunu göreceksiniz. Bu iletide, B.xlsx çalışma kitabı dosyasının hiçbir bileşene bağlanmadığı ve yapılandırma sürümünün durumu değiştirildikten sonra kaldırılacağı belirtilir.

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

**Excel\\Dosya** öğesine bağlı olmayan tüm şablonları kaldırarak, yapılandırılan biçimi değiştirin.

## <a name="not-synced-format"></a><a id="i13"></a>Eşitlenmemiş biçim

Bir ER biçimi bileşenini giden belge oluşturmak için bir Excel şablonu kullanacak şekilde [yapılandırdığınızda](er-fillable-excel.md) **Excel\\Dosya** bileşenini el ile ekleyebilir, gerekli şablonu düzenlenebilir bileşeninin eki olarak ekleyebilir ve eklenen **Excel\\Dosya** bileşeninde eki seçebilirsiniz. Bu şekilde, eklenen öğenin çalışma zamanında seçili şablonu dolduracağını belirtirsiniz. Eklenen Excel şablonu dışarıda tasarlandığından, düzenlenebilir ER biçimi eklenmiş şablonda bulunmayan Excel adları içerebilir. ER biçim tasarımcısı, eklenen Excel şablonunda bulunmayan adlara başvuran ER biçim öğelerinin özellikleri arasındaki tutarsızlıklar hakkında sizi uyarır.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER biçim eşleme bileşenini yapılandırmaya başlayın.
2. Biçim yapısı ağacında, **Excel\\Dosya** **Rapor** öğesini ekleyin.
3. Yeni eklediğiniz **Excel\\File** için ek olarak **A.xlsx** adında bir Excel çalışma kitabı dosyası ekleyin. ER biçim şablonlarının depolanmasını belirtmek için [ER parametrelerinde](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) yapılandırılan belge türünü kullanın.

    > [!IMPORTANT]
    > Eklenen Excel çalışma kitabının **ReportTitle** adını içermediğinden emin olun.

4. **Rapor** öğesinin iç içe öğesi olarak **Excel\\Hücre** **Başlık** öğesini ekleyin. **Excel aralığı** alanına **ReportTitle** girin.
5. **Biçim tasarımcısı** sayfasında, düzenlenebilir biçim bileşenini denetlemek için **Doğrula**'yı seçin.

    ![Biçim tasarımcısı sayfasındaki iç içe öğeleri ve alanları doğrulama.](./media/er-components-inspections-13a.png)

6. Doğrulama uyarısının oluştuğunu göreceksiniz. Bu iletide, kullandığınız Excel şablonunun **Sheet1** sayfasında **ReportTitle** adının bulunmadığı belirtilir.

    ![Excel şablonunun Sheet1 sayfasında ReportTitle adının bulunmadığına dair doğrulama uyarısı.](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

Şablonda bulunmayan Excel adlarına başvuran tüm öğeleri kaldırarak, yapılandırılan biçimi değiştirin.

#### <a name="option-2"></a>Seçenek 2

Bir Excel şablonunu içeri aktararak düzenlenebilir ER biçimini [güncelleştirin](er-fillable-excel.md#template-import). Düzenlenebilir ER biçiminin yapısı, içeri aktarılan Excel şablonunun yapısıyla [eşitlenecektir](modify-electronic-reporting-format-reapply-excel-template.md).

### <a name="additional-consideration"></a>Dikkate alınması gereken ek hususlar

Biçim yapısının [İş belgesi yönetiminin](er-business-document-management.md) şablon düzenleyicisindeki ER şablonu ile nasıl eşitleneceğini öğrenmek için [İş belgesi şablonunun yapısını güncelleştirme](er-bdm-update-structure.md) konusuna bakın.

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a>Word şablon biçimiyle eşitlenmedi

Bir ER biçimi bileşenini giden belge oluşturmak için bir Word şablonu kullanacak şekilde [yapılandırdığınızda](er-fillable-excel.md) **Excel\\Dosya** bileşenini el ile ekleyebilir, gerekli Word şablonunu düzenlenebilir bileşeninin eki olarak ekleyebilir ve eklenen **Excel\\Dosya** bileşeninde eki seçebilirsiniz.

> [!NOTE]
> Word belgesi eklendiğinde, ER biçim tasarımcısı düzenlenebilir öğeyi **Word\\Dosya** olarak sunar.

Bu şekilde, eklenen öğenin çalışma zamanında seçili şablonu dolduracağını belirtirsiniz. Eklenen Word şablonu dışarıda tasarlandığından, düzenlenebilir ER biçimi eklenmiş şablonda bulunmayan Word içerik denetimlerine referanslar içerebilir. ER biçim tasarımcısı, eklenen Word şablonunda bulunmayan içerik denetimlerine referans veren ER biçim öğelerinin özellikleri arasındaki tutarsızlıklar hakkında sizi uyarır.

Bu sorunun nasıl meydana gelebileceğini gösteren bir örnek için, [Özet bölümünü gizlemek için düzenlenebilir biçimi yapılandırma](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control) bölümüne bakın.

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

**Kaldırılan** formülü doğrulama uyarısında belirtilen biçim öğesinden silerek, yapılandırılmış biçimi değiştirin.

#### <a name="option-2"></a>Seçenek 2

Gerekli etiketi ilgili Word içerik denetimine [ekleyerek](er-design-configuration-word-suppress-controls.md#tag-control) kullanılan Word şablonunu değiştirin.

## <a name="no-default-mapping"></a><a id="i15"></a>Varsayılan eşleme yok

[Eksik bağlama](#i11) incelemesi yapıldığında, incelenen biçim bağlamaları ilgili model eşleme bileşeninin bağlamalarıyla değerlendirilir. Finance örneğiniz için [birkaç](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER model eşleme yapılandırması içe aktarabileceğinizden ve her bir yapılandırma uygun model eşleme bileşenini içerebileceğinden, yapılandırmaların biri varsayılan yapılandırma olarak seçilmelidir. Aksi durumda, incelenen ER biçimi çalıştırmayı, düzenlemeyi veya doğrulamayı denediğinizde, bir özel durum ortaya çıkar ve şu iletiyi alırsınız: "\<configuration names separated by comma\> yapılandırmalarında  \<model name (root descriptor)\> veri modeli için birden fazla model eşlemesi var. Yapılandırmalardan birini varsayılan olarak ayarlayın."

Bu sorunun nasıl meydana gelebileceği ve nasıl düzeltilebileceği hakkında bir örnek için, bkz. [Tek bir model kökü için çeşitli türetilmiş eşleştirmeleri yönetme](er-multiple-model-mappings.md).

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a>Üst bilgi veya alt bilgi bileşenlerinin tutarsız ayarı

Bir ER biçim bileşenini, giden belge oluşturmak üzere Excel şablonu kullanacak şekilde [yapılandırdığınızda](er-fillable-excel.md), **Excel\\başlık** bileşenini çalışma sayfasının en üstündeki başlıkları doldurmak üzere Excel çalışma kitabına ekleyebilirsiniz. Ayrıca, çalışma sayfasının alt kısmında alt bilgileri doldurmak üzere **Excel\\alt bilgi** bileşenini ekleyebilirsiniz. Eklediğiniz her **Excel\\üst bilgi** veya **Excel\\Alt bilgi** bileşeni için, bileşenin çalıştırıldığı sayfaları belirtmek üzere **üst bilgi/alt bilgi görünümü** özelliğini ayarlamanız gerekir. Tek bir **sayfa** bileşeni için birkaç **Excel\\üst bilgi** veya **Excel\\alt bilgi** bileşeni yapılandırabileceğiniz ve Excel çalışma sayfasında farklı türde sayfalar için farklı üst bilgiler veya alt bilgiler oluşturabileceğiniz için, **üst bilgi/alt bilgi görünümü** özelliğinin belirli bir değeri için tek bir **Excel\\üst bilgi** veya **Excel\\alt bilgi** bileşeni yapılandırmalısınız. **Üst bilgi/alt bilgi görünümü** özelliğinin belirli bir değeri için birden fazla **Excel\\üst bilgi** veya **Excel\\alt bilgi** bileşeni yapılandırılırsa, doğrulama hatası oluşur ve şu hata iletisini alırsınız: "Üst bilgiler/alt bilgiler ( &lt;bileşen türü: üst bilgi veya alt bilgi &gt;) tutarsız."

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

Tutarsız **Excel\\Üst bilgi** veya **Excel\\Alt bilgi** bileşenlerinden birini silerek yapılandırılmış biçimi değiştirin.

#### <a name="option-2"></a>Seçenek 2

Tutarsız **Excel\\üst bilgi** veya **Excel\\Alt bilgi** bileşenlerinden birinin **üst bilgi/alt bilgi görünümü** özelliğinin değerini değiştirin.

## <a name="inconsistent-setting-of-page-component"></a><a id="i17"></a>Sayfa bileşeninin tutarsız ayarı

Giden belgesi oluşturmak için bir Excel şablonu kullanmak üzere ER biçim bileşeni [yapılandırdığınızda](er-fillable-excel.md) ER formüllerini kullanarak oluşturulan bir belgeyi sayfalandırmak için **Excel\\Sayfa** bileşeni ekleyebilirsiniz. Eklediğiniz her **Excel\\Sayfa** bileşeni için birçok iç içe [Aralık](er-fillable-excel.md#range-component) bileşeni ekleyebilir ve yine de aşağıdaki [yapı](er-fillable-excel.md#page-component-structure) ile uyumlu kalabilirsiniz:

- İlk iç içe **Aralık** bileşeni, **Yineleme yönü** özelliği **Yineleme yok** olarak ayarlanacak şekilde yapılandırılabilir. Bu aralık, oluşturulan belgelerde sayfa üst bilgileri oluşturmak için kullanılır.
- **Yineleme yönü** özelliğinin **Dikey** olarak ayarlandığı durumda diğer birçok iç içe **Aralık** bileşenini ekleyebilirsiniz. Bu aralıklar, oluşturulan belgeleri doldurmak için kullanılır.
- Son iç içe **Aralık** bileşeni, **Yineleme yönü** özelliği **Yineleme yok** olarak ayarlanacak şekilde yapılandırılabilir. Bu aralık, oluşturulan belgelerde sayfa alt bilgileri oluşturmak ve gerekli sayfa sonlarını eklemek için kullanılır.

Bu yapıyı tasarım zamanında ER biçim tasarımcısında ER biçimi için izlemezseniz doğrulama hatası oluşur ve şu hata iletisini alırsınız: "Çoğaltma olmaksızın ikiden fazla aralık bileşeni var. Lütfen gereksiz bileşenleri kaldırın."

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

Tüm tutarsız **Excel\\Aralık** bileşenleri için **Yineleme yönü** özelliğini değiştirerek yapılandırılmış biçimi değiştirin.

## <a name="executability-of-an-expression-with-orderby-function"></a><a id="i18"></a>ORDERBY işlevi içeren bir ifadenin yürütülebilirliği

Yerleşik [ORDERBY](er-functions-list-orderby.md) ER işlevi, işlevin bağımsız değişkeni olarak belirtilen **[Kayıt listesi](er-formula-supported-data-types-composite.md#record-list)** türünün ER veri kaynağı kayıtlarını sıralamak için kullanılır.

`ORDERBY` işlevinin bağımsız değişkenleri, sıralanmış verileri kayıt listesi olarak almak için tek bir veritabanı çağrısı yaparak uygulama tabloları, görünümleri ve veri varlıklarının kayıtlarını sıralamak için [belirtilebilir](er-functions-list-orderby.md#syntax-2). **Kayıt listesi** türündeki bir veri kaynağı, işlevin bağımsız değişkeni olarak kullanılır ve çağrı için uygulama kaynağını belirtir.

ER, `ORDERBY` işlevinde başvurulan veri kaynağına doğrudan veritabanı sorgusu oluşturulup oluşturulamayacağını denetler. Doğrudan sorgu oluşturulamazsa ER model eşleme tasarımcısında bir doğrulama hatası oluşur. Aldığınız iletide, `ORDERBY` işlevini içeren ER ifadesinin çalışma zamanında çalıştırılamadığı belirtilir.

Aşağıdaki adımlarda bu sorunun nasıl oluşabileceği gösterilmektedir.

1. ER model eşleme bileşenini yapılandırmaya başlayın.
2. **Dynamics 365 for Operations \\ Tablo kayıtları** türünde bir veri kaynağı ekleyin.
3. Yeni veri kaynağını **Vendor** olarak adlandırın. **Tablo** alanında, bu veri kaynağının **VendTable** tablosunu isteyeceğini belirtmek için **VendTable** seçeneğini belirleyin.
4. **Hesaplanan alan** türünde bir veri kaynağı ekleyin.
5. Yeni veri kaynağını **OrderedVendors** olarak adlandırın ve `ORDERBY("Query", Vendor, Vendor.AccountNum)` ifadesini içerecek şekilde yapılandırın.
 
    ![Model eşleme tasarımcı sayfasında veri kaynaklarını yapılandırma.](./media/er-components-inspections-18-1.png)

6. **Model eşleme tasarımcısı** sayfasında düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin ve **OrderedVendors** veri kaynağındaki ifadenin sorgulanabildiğini doğrulayın.
7. Kırpılan satıcı hesap numarasını almak için **Hesaplanan alan** türünde iç içe bir alan ekleyerek **Vendor** veri kaynağını değiştirin.
8. Yeni iç içe alanı **$AccNumber** olarak adlandırın ve `TRIM(Vendor.AccountNum)` ifadesini içerecek şekilde yapılandırın.
9. **Model eşleme tasarımcısı** sayfasında düzenlenebilir model eşleme bileşenini denetlemek için **Doğrula**'yı seçin ve **Vendor** veri kaynağındaki ifadenin sorgulanabildiğini doğrulayın.

    ![Vendor veri kaynağındaki ifadenin Model eşleme tasarımcısı sayfasında sorgulanabildiğini doğrulama.](./media/er-components-inspections-18-2.png)

10. **Vendor** veri kaynağı, **OrderedVendors** veri kaynağı ifadesinin doğrudan veritabanı deyimine çevrilmesine izin vermeyen **Hesaplanan alan** türünde iç içe alan içerdiğinden doğrulama hatası oluşur. Doğrulama hatasını yoksayıp bu model eşlemesini çalıştırmak için **Çalıştır**'ı seçerseniz çalışma zamanında aynı hata oluşur.

### <a name="automatic-resolution"></a>Otomatik çözüm

Bu sorunu otomatik olarak düzeltme seçeneği bulunmaz.

### <a name="manual-resolution"></a>El ile çözüm

#### <a name="option-1"></a>Seçenek 1

**Vendor** veri kaynağına, **Hesaplanan alan** türünde iç içe geçmiş bir alan eklemek yerine, **FilteredVendors** veri kaynağına **$AccNumber** iç içe alanını ekleyin ve bu alanı `TRIM(FilteredVendor.AccountNum)` ifadesini içerecek şekilde yapılandırın. Bu şekilde, `ORDERBY("Query", Vendor, Vendor.AccountNum)` ifadesi veritabanı düzeyinde çalıştırılabilir ve **$AccNumber** iç içe alanının hesaplanması daha sonra yapılabilir.

#### <a name="option-2"></a>Seçenek 2

**FilteredVendors** veri kaynağı ifadesini, `ORDERBY("Query", Vendor, Vendor.AccountNum)` yerine `ORDERBY("InMemory", Vendor, Vendor.AccountNum)` olacak şekilde değiştirin. Büyük bir veri hacmi bulunan bir tablo (işlem tablosu) için ifadeyi değiştirmenizi önermeyiz çünkü bu durumda tüm kayıtlar getirilir ve gerekli kayıtların sıralanması işlemi bellekte yapılır. Bu nedenle, bu yaklaşım düşük performansa neden olabilir.

## <a name="additional-resources"></a>Ek kaynaklar

[ALLITEMS ER işlevi](er-functions-list-allitems.md)

[ALLITEMSQUERY ER işlevi](er-functions-list-allitemsquery.md)

[INT64VALUE ER işlevi](er-functions-conversion-int64value.md)

[INTVALUE ER işlevi](er-functions-conversion-intvalue.md)

[FILTER ER işlevi](er-functions-list-filter.md)

[WHERE ER işlevi](er-functions-list-where.md)

[ER model eşlemelerinde birden çok uygulama tablosundan veri almak için JOIN veri kaynaklarını kullanma](er-join-data-sources.md)

[Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme](trace-execution-er-troubleshoot-perf.md)

[İş belgesi yönetimine genel bakış](er-business-document-management.md)

[Oluşturulan raporlarda Word içerik denetimlerini gizleme](er-design-configuration-word-suppress-controls.md)

[Tek bir model kökü için türetilmiş birkaç eşlemeyi yönetme](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
