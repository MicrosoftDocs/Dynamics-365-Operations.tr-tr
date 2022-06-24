---
title: Elektronik iletiler işleviyle çalışma
description: Bu makalede, Elektronik iletiler (EM) işlevinin nasıl kullanılacağı hakkında bilgiler sağlanmaktadır.
author: liza-golub
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b61c119a06e1a7281d3adb67e043d2f7002cbea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880715"
---
# <a name="work-with-the-electronic-messages-functionality"></a>Elektronik mesajlar işlevselliği ile çalışmak

[!include [banner](../includes/banner.md)]

Mesaj düzeyinde çalışıyorsanız, **Elektronik mesajlar** sayfası (**Vergi** \> **Sorgular ve raporlar** \> **Elektronik mesajlar** \> **Elektronik mesajlar**) daha yararlıdır. Veri koleksiyonu veya ileti öğesi düzeyinde çalışıyorsanız **Elektronik mesaj öğeleri** sayfası (**Vergi** \> **Sorgular ve raporlar** \> **Elektronik iletiler** \> **Elektronik ileti öğeleri**) daha yararlıdır.

## <a name="electronic-messages"></a>Elektronik iletiler

**Elektronik mesajlar** sayfası, rolünüze dayalı olarak kullanabileceğiniz işlemleri sunar. Güvenlik rolleri bu işlemenin kurulumundaki işlemler ile ilişkilendirilmiştir. Kullanabileceğiniz her işleme için sayfa size bunlarla ilişkili elektronik mesajlar ve bilgiler gösterir.

**Mesajlar** FastTab'i, seçilen işleme için elektronik mesajlar gösterir. Seçilen mesajın ve önceden tanımlanmış işlemenin durumuna bağlı olarak, kılavuzun üstündeki düğmeleri kullanarak bazı eylemleri gerçekleştirebilirsiniz:

- **Yeni** - Bu düğme, **Mesaj oluştur** türünün eylemleri ile ilişkilendirilmiştir.
- **Sil** - Bu düğme, **Silmeye izin ver** onay kutusu seçili mesajın geçerli durumu için seçiliyse kullanılabilir olur.
- **Veri topla** - Bu düğme, **Kayıtları doldur** türü eylemleriyle ilişkilendirilmiştir.
- **Rapor oluştur** - Bu düğme, **Elektronik raporlama dışa aktarma mesajı** nın eylemleri ile ilişkilendirilmiştir.
- **Rapor gönder** - Bu düğme, **Web hizmeti** türünün eylemleri ile ilişkilendirilmiştir.
- **Yanıt içe aktar** - Bu düğme, **Elektronik raporlama içe aktarma** türünün eylemleriyle ilişkilendirilmiştir.
- **Güncelleştirme durumu** - Bu düğme, **Mesaj düzeyi kullanıcı işleme** türünün eylemleri ile ilişkilendirilmiştir.
- **Mesaj öğeleri** - **Elektronik mesaj öğeleri** sayfasını açın.

**Eylem günlüğü** FastTab'i, seçilen mesaj için yürütülmüş olan tüm eylemler hakkında bilgileri gösterir. Bir eylem bir hataya sebep olursa, hata hakkındaki bilgi kılavuzdaki ilgili satıra eklenir. Hata hakkındaki bilgiyi görüntülemek için kılavuzdaki satırı seçin ve sonra sayfanın sağ üst köşesindeki **Ek** düğmesini seçin (ataş simgesi).

**Mesaj ek alanları** FastTab'i işleme kurulumunda mesajlar için tanımlanmış tüm ek alanları gösterir. Hızlı sekme ayrıca bu ek alanların değerlerini de gösterir.

**Mesaj öğeleri** FastTab'i, seçilen mesaj ile ilişkili tüm mesaj öğelerini gösterir. Seçilen mesajın öğesinin durumuna bağlı olarak, kılavuzun üstündeki düğmeleri kullanarak bazı eylemleri gerçekleştirebilirsiniz:

- **Sil** - Bu düğme, **Silmeye izin ver** onay kutusu seçili mesaj öğesinin geçerli durumu için seçiliyse kullanılabilir olur.
- **Güncelleştirme durumu** - Bu düğme, **Kullanıcı işleme** türünün eylemleri ile ilişkilendirilmiştir.
- **Orijinal belge** - Seçilen mesaj öğesi için orijinal belgeyi gösteren bir sayfa açın.

Bir ileti için halihazırda oluşturulan ve alınan raporlar bu iletiye eklenmiştir. Hata hakkındaki ekleri görüntülemek için iletiyi seçin ve sonra sayfanın sağ üst köşesinde bulunan **Ek** düğmesini seçin (ataş simgesi).

![Ek düğmesi](media/attachment-icon.png)

**Ekler** sayfası, seçilen mesaj ile ilişkili tüm ekleri gösterir. Bir dosyayı görüntülemek için soldaki listeden seçin ve sonra Eylem Panosunda **Aç** öğesini seçin.

![Aç düğmesi](media/open-button.png)

Bir mesaj için önceden çalıştırılmış belirli bir eylemle ilişkili ekleri gözden geçirebilirsiniz. **Elektronik iletiler** sayfasında, **İletiler** hızlı sekmesinde iletiyi seçin. **Eylem günlüğü** hızlı sekmesinde, eylemi seçin ve sonra sayfanın sağ üst köşesinde **Ek** düğmesini (ataş simgesi) seçin.

Tüm işlemi veya belirli bir eylemi Eylem Panosunda **İşlemeyi yürüt** seçeneğini işaretleyerek çalıştırabilirsiniz.

## <a name="electronic-message-items"></a>Elektronik ileti maddeleri

**Elektronik ileti öğeleri** sayfası, tüm ileti öğelerini ve her bir ileti öğesi için çalıştırılmış eylemleri sunar. Ayrıca, sayfa ileti öğeleri için tanımlanmış ek alanları ve bu ek alanların değerlerini de gösterir.

Aşağıdaki tablo, **Mesaj öğeleri** sekmesindeki alnları açıklar.

<table>
<thead>
<tr>
<th>Alan</th>
<th>Tanım</th>
</tr>
</thead>
<tbody>
<tr>
<td>İşleniyor</td>
<td>Mesaj öğesini oluşturmak için kullanılmış olan işlemin adı.</td>
</tr>
<tr>
<td>İleti maddesi</td>
<td>Mesaj öğesinin kimlik kodu. Bu kimlik kodu otomatik olarak, <b>Genel muhasebe parametreleri</b> sayfasında tanımlanmış olan <b>İleti öğesi</b> numara serisine göre atanır.</td>
</tr>
<tr>
<td>İleti maddesi tarihi</td>
<td>Mesaj öğesinin oluşturulduğu tarih.</td>
</tr>
<tr>
<td>İleti maddesi türü</td>
<td>Mesaj öğesinin türü. Çeşitli mesaj öğesi türleri aynı işlem için ayarlanabilir (örneğin, <b>Gelen faturalar</b> ve <b>Giden faturalar</b>). Bu alan bir fatura İleti öğeleri tablosuna bir fatura eklendiğinde otomatik olarak ayarlanabilir.</td>
</tr>
<tr>
<td>İleti maddesi durumu</td>
<td><p>Mesaj öğesinin gerçek durumu. Kullanılabilir durumlar, mesaj öğesinin türüne göre farklılık gösterir. Burada bazı örnekler verilmiştir:</p>
<ul>
<li><b>Doldurulan</b> - Bir kayıt Mesaj öğeleri tablosuna eklendi.</li>
<li><b>Değerlendirilen</b> - Ek öznitelikler mesaj öğesi için hesaplandı.</li>
<li><b>Bildirilen</b> - Mesaj öğesi rapora başarıyla eklendi.</li>
<li><b>Dışarıda bırakılan</b> - Bu durum bazı ileti öğelerini rapor dışa aktarılmadan önce dışarıda bırakmanız gerektiğinde faydalı olabilir.</li>
</ul>
</td>
</tr>
<tr>
<td>İletim tarihi</td>
<td>Oluşturulan bir raporu otomatik olarak sistem dışına aktaran bir işleme için mesaj öğesinin aktarıldığı tarih.</td>
</tr>
<tr>
<td>Belge numarası</td>
<td>Bu alan otomatik olarak, kayıtları doldur eyleminin kurulumuna dayalı olarak ayarlanır. Bu alan bir fatura İleti öğeleri tablosuna bir fatura eklendiğinde otomatik olarak ayarlanabilir.</td>
</tr>
<tr>
<td>Hesap numarası</td>
<td>Bir müşteri veya satıcının hesap numarası (veya başka bir alan değeri, Kayıtları doldur eyleminde tanımlanmış olan alana dayanarak). Bu alan bir fatura İleti öğeleri tablosuna bir fatura eklendiğinde otomatik olarak ayarlanabilir.</td>
</tr>
<tr>
<td>İleti</td>
<td>Mesajın numarası. Bu numara otomatik olarak, <b>Genel muhasebe parametreleri</b> sayfasında tanımlanmış olan <b>İleti</b> numara serisine göre atanır.</td>
</tr>
<tr>
<td>İleti durumu</td>
<td>Elektronik mesajın gerçek durumu.</td>
</tr>
<tr>
<td>Sonraki eylem</td>
<td>Mesaj öğesinin geçerli durumu için başlatılabilecek sonraki eylemler.</td>
</tr>
</tbody>
</table>

**Ek alanlar** sekmesi, seçilen mesaj öğesi için ek alanları ve bunların değerlerini gösterir.

### <a name="run-processing"></a>İşlemeyi başlat

Eylem Panosunda **İşlemeyi yürüt** öğesini seçerek ileti öğeleri için işlemeyi çalıştırın. Belirli bir eylemi yürütmek için **İşlemeyi çalıştır** iletişim kutusunda, **Eylemi seç** seçeneğini **Evet** olarak ayarlayın ve sonra bir eylem seçin. Tüm işlemeyi çalıştırmak için **Eylem seç** seçeneğini **Hayır** olarak ayarlayın.

### <a name="generate-report"></a>Rapor oluştur

Eylem bölmesinde, **Rapor oluştur**'u seçin. Bu düğme, **Elektronik raporlama dışa aktarma** türünün eylemleri ile ilişkilendirilmiştir.

### <a name="update-status"></a>Durumu güncelleştir

**Durumu güncelleştir** öğesini Eylem Panosu üzerinde seçerek bir veya birden fazla ileti öğesinin durumunu güncelleştirin. **Durumu güncelleştir** iletişim kutusunda, güncelleştirilerek mesaj öğelerini seçmek için **Dahil edilecek kayıtlar** FastTab'i kullanın. Seçim kriterini doğru tanımladığınızdan emin olun çünkü mesaj öğesi durumları bu kriterler, seçilen eylemin başlangıç durumu ve belirttiğiniz **Yeni durum** değeri doğrultusunda güncelleştirilecektir. Bir durum güncelleştirmesi tamamlandıktan sonra, hangi öğelerin güncelleştirildiğini belirlemek güç olacaktır. Bu nedenle, durum güncelleştirmesini geri almak zor olacaktır.

### <a name="electronic-messages"></a>Elektronik iletiler

Seçilen ileti öğesi ile ilişkili bir elektronik iletiyi görüntülemek için Eylem Panosunda **Elektronik iletiler** öğesini seçin.

Belirli bir ileti öğesine ilişkin özel dosyaları da gözden geçirebilirsiniz. İleti öğesinin **İleti** alanını seçin veya Eylem Panosunda **Elektronik iletiler** öğesini seçin. **Elektronik ileti** sayfasında, dosyalarının gözden geçileceği iletiyi seçin ve sayfanın sağ üst köşesindeki **Ek** düğmesini (ataş simgesi) seçin.

**Ekler** sayfası, ileti ile ilişkili tüm ekleri gösterir. Bir dosyayı görüntülemek için soldaki listeden seçin ve sonra Eylem Panosunda **Aç** öğesini seçin.

### <a name="original-document"></a>Özgün belge

Seçilen ileti öğesi için orijinal belgeyi açmak için Eylem Panosunda **Orijinal belge** öğesini seçin.
