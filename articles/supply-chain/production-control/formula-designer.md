---
title: "Formül tasarımcısı"
description: "Bu konu, formül tasarımcısının, bir ağaç görünümündeki formülleri analiz etmek ve korumak için nasıl kullanılacağını açıklar."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a4cfd017fe10bbda6eda0e3a9a045e0832b08753
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="formula-designer"></a>Formül tasarımcısı

[!INCLUDE [banner](../includes/banner.md)]

Bu konu, formül tasarımcısının, bir ağaç görünümündeki formülleri analiz etmek ve korumak için nasıl kullanılacağını açıklar.

**Formül tasarımcısı** sayfasını **Serbest bırakılmış ürünler** sayfasından açtığınızda, sol bölmedeki ağaç, serbest bırakılmış ürünün içeriğindeki ortak ürünlerin ve hiyerarşinin listesini gösterir. Bunun yapısı, seçili madde için etkin ve onaylanmış olan formüllerin hiyerarşisinden ve içeriklerinden, maddenin varsayılan sipariş tesisinden ve gerçek tarihinden üretilir.

Farklı yapılandırmaları seçmek için **Kurulum**'u tıklatın ve ağacın satırlarında hangi bilgilerin gösterileceğini belirleyebilirsiniz.

Görünümdeki ilk seçimi değiştirmek için **Filtre** düğmesini tıklayın. Ekran ilkesini **Seçilen/Etkin** veya **Seçilen** konumuna ayarlarsanız, görünümde kullanılacak bireysel formül veya rota sürümlerini seçebilirsiniz. Formül tasarımcısında görüntülemek veya korumak için onaylanmamış ve etkin olmayan formül sürümlerini seçebilirsiniz.  

> [!NOTE]
> **Malzeme listesi** liste sayfasından **Formül tasarımcısını** sayfasını açarsanız rota bilgileri gösterilmez. Şu anda, bir formül veya rota sürümünün seçimi, formül tasarımcısının tüm örneklerine uygulanır.  

Aşağıdaki bölümlerde BOM tasarımcısının içinde bulunan işlevler açıklanmıştır.

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a>Formül tasarımcısını kullanarak bir formül yapısını analiz et
Formül tasarımcısı iki bölüme sahiptir:

-   Formül yapısı ağaç görünümü.
-   Ayrıntılar bölümü, seçilen veriler hakkında ayrıntılı bilgiler gösterir. Ağaç görünümünden bir düğüm seçtiğinizde, söz konusu düğümdeki FastTabs, o düğüme bağlı olarak güncelleştirilir:
    -   **Formül satır bilgileri** – Ağaç görünümünden seçilen formül satırının ayrıntılarını görüntüleyin.
    -   **Ürün verileri** – Ana ürünün veya seçilen düğümde kullanılan ürünün bilgilerini görüntüleyin. Seçilen ürünü tutmak için **Çıkarılan ürünü düzenle** düğmesini tıklayın.
    -   **Formül** – Seçilen düğümle ilgili formülün başlığını görüntüleyin.
    -   **Rota** – Seçilen düğümle ilgili rotanın bağlığını görüntüleyin.
    -   **Rota operasyonları** – Rota için operasyonların bir önizlemesini görüntüleyin. Belirli bir operasyona atanmış bir ürün reçetesi (BOM) satırı seçildiğinde operasyon, **Operasyonlarda gerekli bileşen** olarak işaretlenir.

## <a name="select-a-formula-and-route"></a>Bir formül veya rota seçin
Formül ve rotaya uygulanan filtre, formül tasarımcısının başlığında gösterilir. **Filtre** iletişim kutusunu kullanarak filtreyi değiştirebilirsiniz. Aşağıdaki tabloda bu iletişim kutusunun alanları açıklanmıştır.

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
<td>Seçilen bitmiş ürün bir ana ürün ise, etkin ürün boyutlarını ana bölüm için tanımlayabilirsiniz. Ana ürün olmayan bir ürün için formül tasarımcısını açarsanız, <strong>Filtre</strong> iletişim kutusunda hiçbir ürün boyutu seçilemez.</p></td>
</tr>
<tr class="even">
<td>Tesis</td>
<td>İçerik ağacının gösterildiği siteyi değiştirin. Varsayılan site, nihai ürünün varsayılan stok sahasıdır.</td>
</tr>
<tr class="odd">
<td>İlkeyi göster</td>
<td><p>Geçerli formül yapısı ve geçerli rota için geçerli olan versiyon görüntüleme ilkesini seçin:</p>
<ul>
<li>Prensip <strong>Etkin</strong> veya <strong>Seçili/Etkin</strong> olarak ayarlanırsa, bu tarih için geçerli formül veya rota versiyonu bulunur.</li>
<li>İlke, <strong>Seçilen/Etkin</strong> veya <strong>Seçilen</strong> konumuna ayarlandığında formül sürüü veya rota sürümünü, <strong>Formül</strong> &gt; <strong>Formül sürümleri</strong> veya <strong>Rota</strong> &gt; <strong>Rota sürümleri</strong> seçeneklerini tıklayarak seçebilirsiniz.</li>
</ul></td>
</tr>
<tr class="even">
<td>Sürüm tarihi</td>
<td>Formül ve rota için versiyon tarihini girin. Sürüm hangi formül sürümünün belirli bir tarih için kullanılacağını, formül sürümü kurulumdaki sürüm tarihine dayanarak tanımlar.</td>
</tr>
<tr class="odd">
<td>Başlangıç miktarı</td>
<td>Belirli bir &quot;başlangıç&quot; miktarı seçerek sürümleri filtreleyin. Bir değer ayarlarsanız farklı formül ve rota sürümleri seçilebilir.</td>
</tr>
<tr class="even">
<td>Yalnızca geçerli olanları göster</td>
<td>Seçim kutusunu işaretlediğinizde ağaç yapısında sadece geçerli tarihlere sahip olan formül satırları görüntülenecektir. Formül satırı için geçerlilik tarihlerini görebileceğiniz <strong>Formül satırını düzenle</strong> sayfasını açmak için Formül satırını sağ tıklayın veya çift tıklayın.</td>
</tr>
</tbody>
</table>

Bir veya daha fazla sayıda hayalet görüntü içeren formülleri İncelemek veya düzenlemek, için formül tasarımcısını kullanıyorsanız birinci ürünle bağlantılı rota tipik olarak tüm formül hiyerarşisini kaplayacak şekilde genişler. Görünümü basitleştirmek için ekrandaki üst seviye rotaya **Görünüm** &gt; **Rotayı kilitle** seçeneklerini tıklayarak kilitleyebilirsiniz. Rotanın kilidini açmak için **Görünüm** &gt; **Rotanın kilidini aç** seçeneklerini tıklayın.

## <a name="add-and-edit-formulas-and-formula-lines"></a>Formüller ve formül satırları ekleyin ve düzenleyin
Formül satırlarını veya formülü değiştirmek için **BOM satırları** veya **Formül** işlevlerini kullanın. Ağaç görünümden bir düğüm seçtiğinizde düğümün türü, kullanılabilecek işlevleri belirleyecektir.

| İşlev                            | Açıklama                                                                                               | Düğüm türü ve koşullar |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| BOM satırları &gt; Düzenle                 | Formül satırı özelliklerini düzenleyebileceğiniz bir iletişim kutusu açın.                                         | Bu işlev bir formül satırı düğümü seçildiğinde kullanılabilir. |
| BOM satırları &gt; Sil               | Bir formül satırını seçili formülden silin.                                                          | Bu işlev, bir formül satır düğümü seçildiğinde ve formül düzenleme için kilitlenmediğinde kullanılabilir. |
| BOM satırları &gt; Satırdan önce ekle      | Seçilen formül satırından önce bir ürün çeşidini seçebileceğiniz bir iletişim kutusunu açın.     | Bu işlev bir formül satırı düğümü seçildiğinde kullanılabilir. |
| BOM satırları &gt; Bileşen BOM'una ekle | Seçilen formülün sonuna eklemek üzere bir ürün çeşidi seçebileceğiniz bir iletişim kutusunu açın.   | Bu işlev seçilen düğümün bir seçilen formül içerdiği durumlarda kullanılabilir. Bu işlev kullanılabilir değilse, seçilen ürün çeşidi için bir formül sürümü eksik olabilir. Bu durumda seçilen düğümün eksik sürümünü oluşturmak için **Formül** &gt; **Sürüm oluştur** düğmelerini tıklayın. |
| BOM satırları &gt; Satırdan sonra ekle       | Seçilen formül satırından sonra bir ürün çeşidini seçebileceğiniz bir iletişim kutusunu açın.      | Bu işlev bir formül satırı düğümü seçildiğinde kullanılabilir. |
| Formül &gt; Sürüm oluştur         | Seçili düğümün ürün çeşidi için yeni bir formül sürümü veya formül oluşturun.                     | Bu işlev, seçilen formül satır düğümünün **BOM** veya **Formül** türünde bir üretime sahip olan bir ürünle ilişkilendirilmesi durumunda kullanılabilir. |
| Formül &gt; Hesaplama            | Seçilen ürün çeşidi için maliyet veya satış fiyatı hesaplaması yürütebileceğiniz bir iletişim kutusunu açın. | Bu işlev seçilen düğümün bir formül sürümüyle ilişkili olduğu durumlarda kullanılabilir. |
| Formül &gt; Denetle                  | Seçili formülü doğrulayın ve denetleyin.                                                                  | Bu işlev seçilen düğümün bir formül sürümüyle ilişkili olduğu durumlarda kullanılabilir. |

## <a name="configuring-the-tree-view"></a>Ağaç görünümünün yapılandırılması
Formül tasarımcısının ağaç görünümünde gösterilen bilgileri özelleştirmek için **Kurulum** öğesini tıklayın.


| Alan grubu |                                                                          Açıklama                                                                          |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Ürün reçetesi     | Ağaç görünümünde gösterilen kriterleri seçmek için seçim kutularını kullanın. Formül tasarımcısı seçili ölçütleri her iki sekmenin altında gösterir. |
|    Rota    |                                           Rotalar için gösterilen kriterleri seçmek için seçim kutularını kullanın.                                           |


