---
title: "Rapor tasarımcısında rapor bileşenlerini düzenlemek"
description: "Yapı taşları tasarlayıp rapor oluşturduktan sonra bu nesneleri düzenlemeniz kullanıcıların bunları bulmasını kolaylaştırmaya yardımcı olur. Bu makalede varolan raporların, yapı taşlarının ve nesnelerin rapor tasarımcısında nasıl düzenleneceği açıklanmaktadır."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a8739f426c401aacbab56179bad429a231060f57
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="organize-report-components-in-report-designer"></a>Rapor tasarımcısında rapor bileşenlerini düzenlemek

[!include[banner](../includes/banner.md)]


Yapı taşları tasarlayıp rapor oluşturduktan sonra bu nesneleri düzenlemeniz kullanıcıların bunları bulmasını kolaylaştırmaya yardımcı olur. Bu makalede varolan raporların, yapı taşlarının ve nesnelerin rapor tasarımcısında nasıl düzenleneceği açıklanmaktadır.

Klasörleri, raporları, yapı taşlarını ve diğer nesneleri rapor tasarımcısında dosyalarınızı düzenlemenize yardımcı olması için yeniden adlandırabilirsiniz. Yeniden adlandırdığınız nesne türüne bağlı olarak, o nesneyle ilişkileri güncelleştirmek gerekebilir.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Rapor Tasarımcısı'nda bir klasörü veya yapı taşını yeniden adlandırma
Rapor Tasarımcısı'nda, klasörleri, rapor tanımlarını, satır tanımlarını, sütun tanımları ve raporlama ağaç tanımlarını yeniden adlandırabilirsiniz. **Not:** Bir yapı taşını yeniden adlandırdığınızda bu yapı taşını kullanan tüm raporlama tanımlarını güncelleştirmeniz gerekir. Aksi halde, yeni bir rapor oluşturulamaz.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Rapor Tasarımcısı'nda bir klasörü veya yapı taşını yeniden adlandırma

1.  Rapor Tasarımcısı'nda, klasörü veya yeniden adlandırılacak nesneyi bulmak için gezinti bölmesini kullanın.
2.  Klasör veya nesneyi sağ tıklatın ve ardından **Yeniden adlandır** seçeneğini tıklatın. Gezinti bölmesinde **Ad** alanı kullanılabilir hale gelir.
3.  Yeni bir ad yazın ve sonra Enter tuşuna basın.
4.  Yapı taşı bir satır tanımı, sütun tanımı veya raporlama ağacı tanımı ise, bununla ilişkili diğer yapı taşlarını güncelleştirmeniz gerekir. 3. adımda yeniden adlandırdığınız yapı taşına sağ tıklayın, **İlişkiler** seçeneğini seçin ve sonra güncelleştirmek için listeden bir öğe seçin.
5.  Tüm ilişkili öğeleri güncelleştirilene kadar 4. adımı tekrarlayın.

## <a name="create-and-manage-report-groups"></a>Rapor gruplarını oluşturmak ve yönetmek
Aynı anda birden çok rapor oluşturmak için rapor tanımlarını gruplandırabilirsiniz. Rapor gruplarını oluşturma, değiştirme, silme ve oluşturma için tasarımcı veya yönetici rolüne sahip olmanız gerekir. Oluşturucu rolüne sahip kullanıcılar rapor grupları oluşturabilir ve ayrıca rapor grupları için kullanıcı rapor tanımlarını değiştirebilir.

### <a name="create-a-report-group"></a>Rapor grubu oluşturma

1.  Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.
2.  **Dosya** menüsünde, **Yeni** &gt; **Rapor Grubu Tanımı**'na tıklayarak görüntüleyici penceresinde yeni bir rapor grubu açın. Alternatif olarak, araç çubuğundaki **Rapor Grubu** düğmesine ![Rapor Grubu](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Rapor Grubu") tıklayın.
3.  **Rapor Grubu** sekmesini tıklatın. Bu raporun oluşturulması için ayrı ayrı rapor tanımlarındaki bilgileri geçersiz kılmak için **Tek tek rapor tanımlarından şirket, ayrıntı ve tarih ayarlarını geçersiz kıl** onay kutusunu seçin. Şirket adı, ayrıntı düzeyi, geçici ayar ve tarih bilgileri otomatik olarak girilir ancak güncelleştirmeleri yapabilirsiniz.
4.  Raporlama para birimlerini gösteren birden çok rapor oluşturmak için **Tüm raporlama para birimlerini dahil et** onay kutusunu seçin. Bundan sonra, raporu görüntülediğinizde Web Görüntüleyicisi üzerinde **Para** düğmesine tıklayarak birden çok görünüme erişebilirsiniz.
5.  **Grup içindeki raporlar** alanında, **Ekle** öğesine tıklayarak raporları rapor grubuna eklemek için seçin. **Ekle** iletişim kutusunda birden fazla rapor seçmek için raporları seçerken Ctrl tuşunu basılı tutun. Rapor seçme işlemini tamamladığınızda **Tamam** öğesine tıklayın.
6.  Yeni rapor grubu kaydetmek için **Dosya** &gt; **Kaydet**'e tıklayın.

### <a name="modify-a-report-group"></a>Bir rapor grubu değiştirin

1.  Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.
2.  Rapor grubunu değiştirmek için çift tıklatın.
3.  **Rapor Grubu** sekmesinde istediğiniz değişiklikleri yapın.
4.  Değiştirilen rapor grubunu kaydetmek için **Dosya** menüsünde **Kaydet**'e tıklayın veya araç çubuğunda **Kaydet** düğmesine ![Kaydet](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Kaydet")  tıklayın.

**Not:** Belirli aralıklarla oluşturulacak zamanlanmış raporlarınız varsa, bu ayarları geçersiz kılabilir ve hemen bir rapor üretebilirsiniz.

### <a name="generate-a-report-group-report"></a>Bir rapor grup raporu oluştur

1.  Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.
2.  Oluşturmak için rapor grubunu açın.
3.  Rapor oluşturmak için **Rapor Oluştur** düğmesine ![Rapor Oluştur](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Rapor Oluştur") tıklayın.

### <a name="delete-a-report-group"></a>Bir rapor grubu silme

1.  Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.
2.  Silinecek rapor grubuna sağ tıklayın ve sonra **Sil**'i seçin.
3.  Onay iletisi göründüğünde **Evet**'e tıklayın.

## <a name="report-group-tab-controls"></a>Rapor Grubu sekmesi denetimleri
Aşağıdaki tablo **Rapor Grubu** sekmesindeki denetimlerle ilgili açıklamalar sağlar.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kontrol</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Şirket, ayrıntı ve tek tek rapor tanımları tarih ayarlarını geçersiz kıl</td>
<td>Yalnızca bu raporları oluşturmak için bu rapor grubu raporlarda tek tek rapor tanımları geçersiz kılmak için bu onay kutusunu seçin.</td>
</tr>
<tr class="even">
<td>Şirket adı</td>
<td>Raporlar için kullanılacak bir şirket seçin.</td>
</tr>
<tr class="odd">
<td>Ayrıntı düzeyi</td>
<td>Raporların içereceği ayrıntı düzeyini belirtin.
<ul>
<li><strong>Finansal</strong>− Yüksek düzeyde özet raporu. Raporlama ağacıyla eklenen hesaplar ve boyutlar dışında, hesaplarda ve boyutlarda ayrıntıya gidemezsiniz.</li>
<li><strong>Finans &amp; Hesap</strong> - Üst düzey bir özet ve hesap ayrıntıları içeren bir rapor.</li>
<li><strong>Finans, Hesap &amp; İşlem</strong> - Üst düzey bir özet ve işlem ayrıntıları içeren bir rapor.</li>
</ul></td>
</tr>
<tr class="even">
<td>Provizyon</td>
<td>Raporların içereceği etkinlik türünü belirtin.
<ul>
<li><strong>Yalnızca nakledilen etkinlik</strong> − Yalnızca finansal verilere nakledilen hareketleri ve bakiyeleri içerir.</li>
<li><strong> Nakledilen ve nakledilmeyen etkinlik</strong> − Finansal verilere girilen ve nakledilen hareketlerin ve bakiyelerin tümünü içerir.</li>
<li><strong>Yalnızca nakledilmeyen etkinlik</strong> − Yalnızca finansal verilere girilen ama henüz nakledilmeyen hareketleri içerir.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tüm raporlama para birimlerini dahil et</td>
<td>Microsoft Dynamics ERP sisteminizde yapılandırılan tüm ilave raporlama para birimleri burada listelenir. Belirtilen para birimlerinde ek rapor oluşturmak için bu onay kutusunu seçin. Bu raporları Web Görüntüleyicisi'nde görüntülemek için <strong>Para Birimi</strong> düğmesine tıklayın ve bir para birimi seçin.</td>
</tr>
<tr class="even">
<td>Rapor tanımı ile kaydedilmemiş tarih bilgileri</td>
<td><ul>
<li>Esas dönem</li>
<li>Esas yıl</li>
<li>Kapsanan dönem</li>
</ul>
Yalnızca varsayılan esas dönem ayarları rapor tanımı ile kaydedilir.</td>
</tr>
<tr class="odd">
<td>Rapor tanımı ile kaydedilmiş tarih bilgileri</td>
<td><ul>
<li>Rapor tarihi</li>
<li>Varsayılan esas dönem</li>
</ul></td>
</tr>
<tr class="even">
<td>Grupta raporlar</td>
<td>Rapor grubunda raporları ekleyin, kaldırın ve yeniden sıralayın.
<ul>
<li>Rapor tanımlarını rapor grubuna eklemek için rapor grubunu çift tıklatarak açın ve ardından <strong>Ekle</strong>'yi tıklatın. Rapor grubuna eklenecek raporları seçin ve sonra <strong>Tamam</strong>'ı seçin.</li>
<li>Bir raporu rapor grubundan kaldırmak için onu seçin ve sonra<strong>Kaldır</strong>'ı tıklatın.</li>
<li>Raporların üretilme sırasını değiştirmek için listeden bir rapor seçin ve sonra <strong>Yukarı taşı</strong> veya <strong>Aşağıya taşı</strong>'ya tıklayın.</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Ayrıca bkz.
--------

[Mali raporlama](financial-reporting-intro.md)




