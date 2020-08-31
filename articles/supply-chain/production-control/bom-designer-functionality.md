---
title: Ürün reçetesi tasarımcısı işlevi
description: Bu konu, ürün reçetesi tasarımcısı sayfasını, ürün reçeteleri (BOM) tasarlamak ve ağaç yapıları ile çalışmak için nasıl kullanabileceğinizi açıklar.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerSetup, BOMDesignerFilterDialog, BOMDesignerBOMVersion, BOMChangeLine
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c97e58f6f608efd3b964e7fad229a00e1ae603a
ms.sourcegitcommit: 59a9e840989bc9f2c7004efa3499b69c09a91b06
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677843"
---
# <a name="bom-designer-functionality"></a>Ürün reçetesi tasarımcısı işlevi

[!include [banner](../includes/banner.md)]

Bu konu, ürün reçetesi tasarımcısı sayfasını, ürün reçeteleri (BOM) tasarlamak ve ağaç yapıları ile çalışmak için nasıl kullanabileceğinizi açıklar. Farklı yapılandırmaları seçmek için Kurulum'u tıklatabilir ve ağacın satırlarında hangi bilgilerin gösterileceğini belirleyebilirsiniz.

**Çıkan ürünler** sayfasından **BOM tasarımcısı** sayfasını açtığınızda seçilen ürün için etkin olan ve onaylanmış malzeme listesi (BOM) hiyerarşisi, ürün için varsayılan sipariş sitesi ve gerçek tarih görüntülenir.  

Görünümdeki ilk seçimi değiştirmek için **Filtre** düğmesini tıklayın. Ekran ilkesini **Seçilen/Etkin veya Seçilen** konumuna atayarak, görünümde kullanılacak bireysel BOM veya rota sürümlerini seçebilirsiniz. BOM tasarımcısında görüntülemek veya korumak için onaylanmamış ve etkin olmayan BOM sürümlerini seçebilirsiniz.  

**Not:** **Malzeme listesi** liste sayfasından BOM tasarımcısını açarsanız rota bilgileri görüntülenmez. Mevcut durumda, bir BOM veya rota sürümü seçimi, BOM ve rota sürümünün bir özelliğidir ve BOM tasarımcısının tüm modelleri için geçerli olacaktır.  

Aşağıdaki bölümlerde BOM tasarımcısının çeşitli sekmelerinde bulunan işlevler açıklanmıştır.

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>BOM tasarımcısı kullanılarak bir BOM yapısının analiz edilmesi
BOM tasarımcısı iki bölüme sahiptir:

-   BOM yapısı ağaç görünümü.
-   Ayrıntılar bölümü, seçilen veriler hakkında ayrıntılı bilgiler gösterir. Ağaç görünümünden bir düğüm seçtiğinizde, söz konusu düğümdeki FastTabs, o düğüme bağlı olarak güncelleştirilir:
    -   **BOM satır bilgileri** – Ağaç görünümünden seçilen BOM satırının ayrıntılarını gösterir.
    -   **Ürün verileri** – Ana ürünün veya seçilen düğümde kullanılan ürünün bilgilerini gösterir. Seçilen ürünü tutmak için **Çıkarılan ürünü düzenle** düğmesini tıklayın.
    -   **BOM** – Seçilen düğümle iglili BOM'un başlığını gösterir.
    -   **Rota** – Seçilen düğümle ilgili rotanın bağlığını gösterir.
    -   **Rota operasyonları** – Rota için operasyonların bir önizlemesini gösterir. Belirli bir operasyona atanmış bir BOM satırı seçildiğinde operasyon, **Operasyonlarda gerekli bileşen** olarak işaretlenir.

## <a name="selecting-a-bom-and-route"></a>Bir BOM ve rota seçimi
BOM ve rotaya uygulanan filtre, BOM tasarımcısının başlığında görüntülenir. **Filtre** iletişim kutusunu kullanarak filtreyi değiştirebilirsiniz. Aşağıdaki tabloda bu iletişim kutusunun alanları açıklanmıştır.

<table>
<thead>
<tr class="header">
<th>Alan</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ürün boyutları</td>
<td>Seçilen bitmiş ürün bir ana ürün ise, etkin ürün boyutlarını ana bölüm için tanımlayabilirsiniz. <strong>Note:</strong> Ana ürün olmayan bir ürün için ürün reçetesi tasarımcısını açarsanız, <strong>Filtre</strong> iletişim kutusunda hiçbir ürün boyutu seçilemez.</td>
</tr>
<tr class="even">
<td>Tesis</td>
<td>BOM ağacının görüntülendiği siteyi değiştirin. Varsayılan site, nihai ürünün varsayılan stok sahasıdır.</td>
</tr>
<tr class="odd">
<td>İlkeyi göster</td>
<td>Mevcut BOM yapısı ve mevcut rota için geçerli olan sürüm görüntüleme ilkesini seçin:
<ul>
<li>İlke, <strong>Etkin veya Seçilen/Etkin</strong> olarak ayarlandığında bu tarih için geçerli BOM veya rota sürümü bulunur.</li>
<li>İlke, <strong>Seçilen/Etkin veya Seçilen</strong> konumuna ayarlandığında <strong>BOM</strong> &gt; <strong>BOM sürümleri</strong> veya <strong>Rota</strong> &gt; <strong>Rota sürümleri</strong> seçeneklerini tıklayarak bir BOM sürümünü veya rota sürümünü seçebilirsiniz.</li>
</ul></td>
</tr>
<tr class="even">
<td>Sürüm tarihi</td>
<td>Ürün reçetesi ve rota için versiyon tarihini girin. Sürüm, belirli bir tarihte hangi BOM sürümünün kullanılacağını BOM sürümü kurulumundaki sürüm tarihlerine göre belirleyerek tanımlar.</td>
</tr>
<tr class="odd">
<td>Başlangıç miktarı</td>
<td>Sürümleri, tutarlar içinden bir özel tutar seçerek filtreleyin. Bir değer ayarlarsanız farklı BOM ve rota sürümleri seçilebilir.</td>
</tr>
<tr class="even">
<td>Yalnızca geçerli olanları göster</td>
<td>Seçim kutusunu işaretlediğinizde ağaç yapısında sadece geçerli tarihlere sahip olan BOM satırları görüntülenecektir. BOM satırı için geçerlilik tarihlerini görebileceğiniz <strong>BOM satırını düzenle</strong> sayfasını açmak için BOM satırını sağ tıklayın veya çift tıklayın.</td>
</tr>
</tbody>
</table>

Bir veya daha fazla sayıda hayalet görüntü içeren BOM'ları İncelemek veya düzenlemek, için BOM tasarımcısını kullanıyorsanız birinci ürünle bağlantılı rota tipik olarak tüm BOM hiyerarşisini kaplayacak şekilde genişler. Görünümü basitleştirmek için ekrandaki üst seviye rotaya **Görünüm** &gt; **Rotayı kilitle** seçeneklerini tıklayarak kilitleyebilirsiniz. Rotanın kilidini açmak için **Görünüm** &gt; **Rotanın kilidini aç** seçeneklerini tıklayın.

## <a name="adding-and-editing-boms-and-bom-lines"></a>BOM'ların ve BOM satırlarının eklenmesi ve düzenlenmesi
BOM satırlarını veya BOM'u değiştirmek için **BOM satırlarını** veya **BOM** işlevlerini kullanın. Ağaç görünümden bir düğüm seçtiğinizde düğümün türü, kullanılabilecek işlevleri belirleyecektir.

| İşlev                            | Açıklama                                                                                               | Düğüm türü ve koşullar                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BOM satırları &gt; Düzenle                 | BOM satırı özelliklerini düzenleyebileceğiniz bir iletişim kutusu açın.                                             | Bu işlev bir BOM satır düğümü seçildiğinde kullanılabilir.                                                                                                                                                                                                                                   |
| BOM satırları &gt; Sil               | Seçilen BOM'dan bir BOM satırını silin.                                                                  | Bu işlev, bir BOM satır düğümü seçildiğinde ve BOM düzenleme için kilitlenmediğinde kullanılabilir.                                                                                                                                                                                             |
| BOM satırları &gt; Satırdan önce ekle      | Seçilen BOM satırından önce bir ürün çeşidini seçebileceğiniz bir iletişim kutusunu açın.         | Bu işlev bir BOM satır düğümü seçildiğinde kullanılabilir.                                                                                                                                                                                                                                   |
| BOM satırları &gt; Bileşen BOM'una ekle | Seçilen BOM'un sonuna eklemek üzere bir ürün çeşidi seçebileceğiniz bir iletişim kutusunu açın.       | Bu işlev seçilen düğümün bir seçilen BOM içerdiği durumlarda kullanılabilir. Bu işlev kullanılabilir değilse, seçilen ürün çeşidi için bir BOM sürümü eksik olabilir. Bu durumda seçilen düğümün eksik sürümünü oluşturmak için **BOM** &gt; **Sürüm oluştur** düğmelerini tıklayın. |
| BOM satırları &gt; Satırdan sonra ekle       | Seçilen BOM satırından sonra bir ürün çeşidini seçebileceğiniz bir iletişim kutusunu açın.          | Bu işlev bir BOM satır düğümü seçildiğinde kullanılabilir.                                                                                                                                                                                                                                   |
| BOM &gt; Sürüm oluştur             | Seçili düğümün ürün çeşidi için yeni bir BOM sürümü veya BOM oluşturun.                             | Bu işlev, seçilen BOM satır düğümünün **BOM** veya **Formül** türünde bir üretime sahip olan bir ürünle ilişkilendirilmesi durumunda kullanılabilir.                                                                                                                                                  |
| Ürün reçetesi &gt; Hesaplama                | Seçilen ürün çeşidi için maliyet veya satış fiyatı hesaplaması yürütebileceğiniz bir iletişim kutusunu açın. | Bu işlev seçilen düğümün bir BOM sürümüyle ilişkili olduğu durumlarda kullanılabilir.                                                                                                                                                                                                         |
| BOM &gt; Kontrol                      | Seçili BOM'u doğrulayın ve kontrol edin.                                                                      | Bu işlev seçilen düğümün bir BOM sürümüyle ilişkili olduğu durumlarda kullanılabilir.                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>Ağaç görünümünün yapılandırılması
BOM tasarımcısının ağaç görünümünde gösterilen bilgileri özelleştirmek için **Kurulum** öğesini tıklayın.

| Alan grubu | Açıklama                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ürün reçetesi         | Ağaç görünümünde gösterilen kriterleri seçmek için seçim kutularını kullanın. BOM tasarımcısı her iki sekmenin altında seçilen kriterleri gösterir. |
| Rota       | Rotalar için gösterilen kriterleri seçmek için seçim kutularını kullanın.                                                                                    |





