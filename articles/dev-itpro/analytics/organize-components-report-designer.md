---
title: Rapor tasarımcısında rapor bileşenlerini düzenlemek
description: Yapı taşları tasarlayıp rapor oluşturduktan sonra bu nesneleri düzenlemeniz kullanıcıların bunları bulmasını kolaylaştırmaya yardımcı olur. Bu makalede varolan raporların, yapı taşlarının ve nesnelerin rapor tasarımcısında nasıl düzenleneceği açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3f2b34cccfd84a9e4bb76e7a1da64e5cefa9982e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "323951"
---
# <a name="organize-report-components-in-report-designer"></a>Rapor tasarımcısında rapor bileşenlerini düzenlemek

[!include [banner](../includes/banner.md)]

Yapı taşları tasarlayıp rapor oluşturduktan sonra bu nesneleri düzenlemeniz kullanıcıların bunları bulmasını kolaylaştırmaya yardımcı olur. Bu makalede varolan raporların, yapı taşlarının ve nesnelerin rapor tasarımcısında nasıl düzenleneceği açıklanmaktadır.

Klasörleri, raporları, yapı taşlarını ve diğer nesneleri rapor tasarımcısında dosyalarınızı düzenlemenize yardımcı olması için yeniden adlandırabilirsiniz. Yeniden adlandırdığınız nesne türüne bağlı olarak, o nesneyle ilişkileri güncelleştirmek gerekebilir.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Rapor Tasarımcısı'nda bir klasörü veya yapı taşını yeniden adlandırma
Rapor Tasarımcısı'nda, klasörler, rapor tanımları, satır tanımları, sütun tanımları ve raporlama ağacı tanımlarını yeniden adlandırabilirsiniz.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Rapor Tasarımcısı'nda bir klasörü veya yapı taşını yeniden adlandırma

1. Rapor Tasarımcısı'nda, yeniden adlandırılacak klasörü veya nesneyi bulmak için gezinti bölmesini kullanın.
2. Klasöre veya nesneye sağ tıklayın ve ardından **Yeniden Adlandır**'a tıklayın. Gezinti bölmesindeki **Ad** alanı kullanılabilir hale gelir.
3. Yeni bir ad yazın ve ardından Enter'a basın.
4. Yapı taşı satır tanımı, sütun tanımı veya raporlama ağacı tanımıysa yapı taşıyla ilişkili diğer yapı taşlarını güncelleştirmeniz gerekir. 3. adımda yeniden adlandırdığınız yapı taşına sağ tıklayın, **İlişkiler**'i seçin ve ardından güncelleştirmek için listeden bir madde seçin.
5. Tüm ilişkili maddeler güncelleştirilene kadar 4. adımı tekrarlayın.

## <a name="create-and-manage-report-groups"></a>Rapor grupları oluşturma ve yönetme
Aynı anda birden fazla rapor oluşturmak için rapor tanımlarını gruplandırabilirsiniz. Rapor gruplarını değiştirmek, silmek ve oluşturmak için, tasarımcı veya yönetici rolüne sahip olmanız gerekir. Oluşturan rolüne sahip kullanıcılar rapor grupları oluşturabilir ve aynı zamanda rapor gruplarına ilişkin kullanıcı rapor tanımları ayarını değiştirebilir.

### <a name="create-a-report-group"></a>Rapor grubu oluşturma

1. Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.
2. **Dosya** menüsünde, **Yeni** &gt; **Rapor Grubu Tanımı**'na tıklayarak görüntüleyici penceresinde yeni bir rapor grubu açın. Alternatif olarak, araç çubuğundaki **Rapor Grubu** düğmesine ![Rapor Grubu](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Rapor Grubu") tıklayın.
3. **Rapor Grubu** sekmesine tıklayın. Bu raporun oluşturulması için tek rapor tanımlarındaki bilgileri geçersiz kılmak üzere, **Tek rapor tanımlarındaki şirket, ayrıntı ve tarih ayarlarını geçersiz kıl** onay kutusunu işaretleyin. Şirket adı, ayrıntı düzeyi, geçici ayar ve tarih bilgileri otomatik olarak girilir, ancak güncelleştirmeler yapabilirsiniz.
4. Raporlama para birimlerini gösteren birden fazla rapor oluşturmak için **Tüm raporlama para birimlerini ekle** onay kutusunu seçin. Böylece raporu görüntülediğinizde, Web Görüntüleyici'deki **Para Birimi** düğmesine tıklayarak birden fazla görünüme erişebilirsiniz.
5. Rapor grubuna eklemek üzere raporları seçmek için **Gruptaki raporlar** alanında **Ekle**'ye tıklayın. **Ekle** iletişim kutusunda birden fazla rapor seçmek için, raporları seçerken Ctrl tuşunu basılı tutun. Rapor seçme işlemini tamamladığınızda **Tamam** öğesine tıklayın.
6. Yeni rapor grubu kaydetmek için **Dosya** &gt; **Kaydet**'e tıklayın.

### <a name="modify-a-report-group"></a>Bir rapor grubu değiştirin

1. Rapor Tasarımcısı'nda gezinme bölmesinde **Rapor Grupları** seçeneğine tıklayın.
2. Değiştirilecek rapor grubuna çift tıklayın.
3. **Rapor Grubu** sekmesinde, istediğiniz değişiklikleri yapın.
4. Değiştirilen rapor grubunu kaydetmek için **Dosya** menüsünde **Kaydet**'e tıklayın veya araç çubuğunda **Kaydet** düğmesine ![Kaydet](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Kaydet")  tıklayın.

> [NOT] Ayarlanan aralıklarda oluşturulmaları için planlanan raporlarınız varsa bu ayarları geçersiz kılarak hemen bir rapor oluşturabilirsiniz.

### <a name="generate-a-report-group-report"></a>Rapor grubu raporu oluşturma

1. Rapor Tasarımcısı'ndaki gezinti bölmesinde **Rapor Grupları**'na tıklayın.
2. Oluşturmak için rapor grubunu açın.
3. Rapor oluşturmak için **Rapor Oluştur** düğmesine ![Rapor Oluştur](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Rapor Oluştur") tıklayın.

### <a name="delete-a-report-group"></a>Bir rapor grubunu silme

1. Rapor Tasarımcısı'ndaki gezinti bölmesinde **Rapor Grupları**'na tıklayın.
2. Silinecek rapor grubuna sağ tıklayın ve ardından **Sil**'i seçin.
3. Bir onay mesajı göründüğünde, **Evet**'e tıklayın.

## <a name="report-group-tab-controls"></a>Rapor Grubu sekmesi kontrolleri
Aşağıdaki tabloda **Rapor Grubu** sekmesindeki kontroller açıklanmaktadır.

<table>
<thead>
<tr>
<th>Kontrol</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tek rapor tanımlarındaki şirket, ayrıntı ve tarih ayarlarını geçersiz kıl</td>
<td>Yalnızca bu raporların oluşturulması için bu rapor grubundaki raporların tek rapor tanımlarını geçersiz kılmak üzere bu onay kutusunu seçin.</td>
</tr>
<tr>
<td>Şirket adı</td>
<td>Raporlar için kullanmak üzere şirketi seçin.</td>
</tr>
<tr>
<td>Ayrıntı düzeyi</td>
<td>Raporların içerdiği ayrıntı düzeyini belirtin.
<ul>
<li><strong>Mali</strong>: Üst düzey özet rapor. Bir raporlama ağacı aracılığıyla eklenen hesaplar ve boyutlar hariç, hesaplar ve boyutlarda ayrıntıya inemezsiniz.</li>
<li><strong>Finans &amp; Hesap</strong> - Üst düzey bir özet ve hesap ayrıntıları içeren bir rapor.</li>
<li><strong>Finans, Hesap &amp; İşlem</strong> - Üst düzey bir özet ve işlem ayrıntıları içeren bir rapor.</li>
</ul></td>
</tr>
<tr>
<td>Geçici</td>
<td>Raporların içerdiği faaliyet türlerini belirtin.
<ul>
<li><strong>Yalnızca deftere nakledilmiş faaliyet</strong>: Yalnızca mali verilerinize nakledilen hareketleri ve bakiyeleri ekleyin.</li>
<li><strong>Deftere nakledilmiş ve nakledilmemiş faaliyet</strong>: Mali verilerinize girilip nakledilen tüm hareketleri ve bakiyeleri ekleyin.</li>
<li><strong>Deftere nakledilmemiş faaliyet</strong>: Yalnızca mali verilerinize girilmiş ancak henüz nakledilmemiş hareketleri ekleyin.</li>
</ul></td>
</tr>
<tr>
<td>Tüm raporlama para birimlerini ekle</td>
<td>Microsoft Dynamics ERP sisteminizde yapılandırılan tüm ek raporlama para birimleri burada belirtilir. Belirtilen para birimlerinde ek raporlar oluşturmak için bu onay kutusunu seçin. Bu raporları Web Görüntüleyici'de görüntülemek için <strong>Para Birimi</strong> düğmesine tıklayın ve ardından bir para birimi seçin.</td>
</tr>
<tr>
<td>Tarih bilgileri rapor tanımına kaydedilmedi</td>
<td><ul>
<li>Esas dönem</li>
<li>Esas yıl</li>
<li>Kapsanan dönemler</li>
</ul>
Rapor tanımıyla yalnızca varsayılan esas dönem ayarları kaydedilir.</td>
</tr>
<tr>
<td>Tarih bilgileri rapor tanımına kaydedildi</td>
<td><ul>
<li>Rapor tarihi</li>
<li>Varsayılan esas dönem</li>
</ul></td>
</tr>
<tr>
<td>Gruptaki raporlar</td>
<td>Rapor grubuna rapor ekleyin, bunları kaldırın ve yeniden sıralayın.
<ul>
<li>Rapor grubuna rapor tanımları eklemek için, açmak üzere rapor grubuna çift tıklayın ve ardından <strong>Ekle</strong>'ye tıklayın. Rapor grubuna eklenecek raporları seçin ve ardından <strong>Tamam</strong>'a tıklayın.</li>
<li>Bir raporu rapor grubundan kaldırmak için, raporu seçin ve ardından <strong>Kaldır</strong>'a tıklayın.</li>
<li>Raporların oluşturulduğu sırayı değiştirmek için, listeden bir rapor seçin ve ardından <strong>Yukarı taşı</strong>'ya veya <strong>Aşağı taşı</strong>'ya tıklayın.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Ek kaynaklar

[Mali raporlama](financial-reporting-intro.md)
