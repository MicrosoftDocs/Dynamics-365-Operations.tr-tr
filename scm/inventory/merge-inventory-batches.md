---
title: "Stok toplu işlerini birleştir"
description: "Bu makalede iki veya daha fazla stok toplu işinin birleştirilmiş bir toplu iş ile nasıl konsolide edileceği hakkında bilgiler verilmiştir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventBatchJournalListPage, InventBatchJournalMerge
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 39782
ms.assetid: 07c5e98b-10fd-4f5c-b471-41d2150f47b0
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 5abf8cf272924669cec6987a96f6565fffa54642
ms.lasthandoff: 03/31/2017


---

# <a name="merge-inventory-batches"></a>Stok toplu işlerini birleştir

[!include[banner](../includes/banner.md)]


Bu makalede iki veya daha fazla stok toplu işinin birleştirilmiş bir toplu iş ile nasıl konsolide edileceği hakkında bilgiler verilmiştir. 

Toplu işleri birleştirdiğinizde, hesaplamalar, birleştirilmiş toplu iştin özellikleri ve toplu iş özniteliklerini en iyi duruma getirmenize yardımcı olur. Kaynak toplu işleri seçtikten sonra, birleştirilen toplu işi deftere nakletmeden önce gözden geçirilebilir ve değiştirebilirsiniz. Ayrıca, toplu iş birleştirme işlemini onay için bir stok günlüğüne transfer edebilirsiniz. Stok ardından doğrudan bu stok günlüğünden rezerve edilebilir veya deftere nakledilebilir. Birleştirilmiş bir toplu işi deftere naklettiğinizde, stok, kaynak toplu işler ve birleştirilmiş toplu iş için ayarlanır.

## <a name="are-there-any-prerequisites"></a>Herhangi bir önkoşul var mı?
Evet, birleştirme toplu iş araçlarını kullanmadan önce ayarlamanız gereken bazı şeyler vardır. Aşağıdaki tablo bu önkoşulları açıklar.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sayfa</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Günlük adları, stok</td>
<td>Stok günlüklerinde toplu iş birleştirmelerini deftere naklettiğinizde varsayılan olarak kullanılan bir günlük adı oluşturmanız gerekir. İsteğe bağlıdır, ancak önerilir: Toplu iş birleştirmesi stok günlüğüne aktarıldığında rezervasyonların otomatik olarak yapılmasını belirtebilirsiniz. Aksi takdirde, toplu iş birleştirme ayrıntıları ayarlandıktan ve günlük deftere nakledildikten sonra eldeki stokun değiştirilme riski vardır. Günlük adı için otomatik rezervasyonları etkinleştirmek üzere <strong><strong>Rezervasyon</strong> </strong>alanında <strong>Otomatik</strong> öğesini seçin.</td>
</tr>
<tr class="even">
<td>Stok ve ambar yönetim parametreleri</td>
<td>Stok günlüğü için varsayılan günlük adını belirtmeniz gerekir.</td>
</tr>
<tr class="odd">
<td>Serbest bırakılan ürünler</td>
<td>Madde için önerilen ayarlar şunlardır:
<ul>
<li>Birleştirilmiş toplu işlerin toplu iş numaralarını otomatik olarak oluşturmak için, serbest bırakılan ürünü bir toplu iş numarası grubuna atamanız gerekir. Birleştirilmiş bir toplu iş oluşturduğunuzda toplu iş numarasını el ile de girebilirsiniz veya mevcut bir toplu iş numarasını seçersiniz. Mevcut bir toplu iş numarası seçerseniz, seçilen toplu işin herhangi bir stok hareketine dahil edilmemiş olduğundan emin olun.</li>
<li>Serbest bırakılan ürün için raf ömrü veya son kullanma tarihi kullanıyorsanız, birleştirilmiş bir toplu işin tarihleri <strong>Toplu iş birleştirme tarihi</strong> hesaplaması alanında yapılan seçime göre hesaplanır. Aşağıdaki seçenekler bulunur:
<ul>
<li><strong>En erken</strong> – Hesaplama, toplu iş birleştirmede seçilen kaynak toplu iş için belirtilen en erken tarihe dayalı yapılır.</li>
<li><strong>En geç</strong> – Hesaplama, toplu iş birleştirmede seçilen kaynak toplu iş için belirtilen en geç tarihe dayalı yapılır.</li>
<li><strong>El ile</strong> – Hesaplama yapılmaz. Bir tarih tüm kaynak toplu işlerde aynıysa, bir tarih önerilir. Bu tarihi değiştirebilirsiniz. Bir tarih kaynak toplu işlerde aynı değilse, bu tarihi el ile girebilirsiniz.</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>Parti numarası grubu</td>
<td>İsteğe bağlı: Birleştirilmiş bir toplu iş oluşturduğunuzda bir toplu iş numarası oluşturmak için serbest bırakılan ürüne bir toplu iş numarası grubu atamanız gerekir. Aksi durumda, bir toplu iş numarasını el ile girebilirsiniz.</td>
</tr>
</tbody>
</table>

## <a name="when-might-i-want-to-merge-batches-of-inventory"></a>Stoktaki toplu işleri ne zaman birleştirmeyi düşünmeliyim?
Burada, toplu işleri birleştirmenin ne zaman yararlı olduğuna yönelik bazı senaryo örnekleri verilmiştir:

-   Sammy, çalıştığı ambarda yürürken, aynı maddeden düşük miktarlarda birkaç toplu işin bulunduğu fark ediyor. Yeni birkaç sevkiyat beklemektedir ve artık miktarları yeni bir toplu işte birleştirerek biraz alan açabileceğini görür.
-   Sammy, stok almaktadır ve mevcut toplu işin toplu iş öznitelik değerini geliştirmek yeni toplu işi daha önce aldığı bir toplu işle birleştirmek istiyor.

## <a name="can-i-merge-batches-across-sites-and-legal-entities"></a>Toplu işleri tesisler ve tüzel kişilikler genelinde birleştirebilir miyim?
Hayır, yalnızca tek tüzel kişilikte aynı tesise ve ambar depolama boyutuna sahip toplu işleri birleştirebilirsiniz. Ancak, birleştirilmiş toplu iş için farklı bir konum ve palet kimliği belirtebilirsiniz.

## <a name="can-i-merge-partial-quantities"></a>Kısmi miktarları birleştirebilir miyim?
Hayır, sadece toplu işin tam miktarını birleştirebilirsiniz. Toplu iş birleştirme özelliği bir stok özelliği olarak tasarlanmıştır, bir üretim özelliği değildir.

## <a name="what-if-the-batches-have-different-batch-attribute-values"></a>Toplu işler farklı toplu iş öznitelik değerlerine sahipse ne olur?
Kaynak toplu işlemi, birleştirilmiş bir toplu işlemde birleştirmek için seçtiğinizde Microsoft Dynamics 365 for Operations tüm toplu işlerin aynı özelliklere ya da özniteliklere sahip olup olmadığını doğrular. Bir öznitelik değeri aynı olduğunda, birleştirilmiş toplu iş için bir değer önerilir. Bu değeri değiştirebilirsiniz. Aynı olmayan öznitelik değerleri birleştirilmiş toplu iş için boş bırakılır ve bu değerleri el ile girebilirsiniz. Öznitelik değerinin toplu iş özniteliği türü bir tamsayı ya da kesirli bir değerse ve değerler tüm kaynak toplu işler için aynı değilse, değer, ağırlıklı ortalama hesaplaması kullanılarak hesaplanır. Hesaplanan değer yakın olan sayıya yuvarlanır. Değer bir kaynak toplu iş için boşsa, toplu iş ve miktarı hesaplamaya dahil edilmez. **Örnek** Aşağıdaki örnek, birleştirilmiş bir toplu iş için ağırlıklı ortalama hesaplamayı göstermektedir. Kaynak toplu işlerin ikisinde tamsayı olan bir toplu iş öznitelik türü için boş bir değer vardır. Aşağıdaki öznitelik kaynak toplu işlere atanır.

| Öznitelik | Minimum | Artış | Maksimum |
|-----------|---------|-----------|---------|
| Derece     | 3       | 3         | 30      |

Kaynak toplu işlerde **Derece toplu iş** özniteliği için aşağıdaki öznitelik değerleri vardır.

| Toplu İş | Miktar | Öznitelik | Öznitelik değeri |
|-------|----------|-----------|-----------------|
| B1    | 10       | Derece     | Boşluk           |
| B2    | 15       | Derece     | 15              |
| B3    | 20       | Derece     | 20              |
| B4    | 25       | Derece     | Boşluk           |
| B5    | 30       | Derece     | 25              |

Bu toplu işleri kaynak toplu işler olarak eklediğinizde, birleştirilmiş toplu işe aşağıdaki değerler atanır.

| Toplu İş | Miktar | Öznitelik | Öznitelik değeri |
|-------|----------|-----------|-----------------|
| B6    | 100      | Derece     | 21              |

Değerler ve B1 ile B4 toplu işlerinin miktarları ağırlıklı ortalama hesaplamasına dahil edilmez. Bu nedenle, birleştirilmiş toplu iş değeri burada gösterildiği gibi hesaplanır.

| Değer | Miktar (ağırlık)                              | Göreli ağırlık | Göreli ağırlık × Değer                                               |
|-------|------------------------------------------------|-----------------|-----------------------------------------------------------------------|
| 15    | 15                                             | 0.230769231     | 3.461538462                                                           |
| 20    | 20                                             | 0.307692308     | 6.153846154                                                           |
| 25    | 30                                             | 0.461538462     | 11.53846154                                                           |
|       | **Toplam:** 65 (ağırlıklarının toplamıdır) |                 | **Toplam:** 21.5384615 (21'e (en yakın kademe) yuvarlanır) |

## <a name="what-if-the-batches-have-different-batch-dates"></a>Toplu işler farklı toplu iş tarihlerine sahipse ne olur?
Toplu işler farklı toplu iş tarihlerine sahipse, tarihlerden bazıları **Toplu iş birleştirme** sayfasının **Birleştirilen toplu iş** FastTab'indeki **Toplu iş tarihleri** grubundaki değerlere dayalı olarak hesaplanır. Sistem, **Toplu iş tarihleri** grubundaki alanlar için değerleri hesaplar. Bu değerlere üretim tarihi, bitiş tarihi, raf öneri tarihi ve son kullanım tarihi dahildir. Tarihler, **Serbest bırakılan ürün ayrıntıları** sayfasının **Ürün verileri** alanı grubundaki madde için ayarlara dayalı olarak hesaplanır. Değerleri değiştirebilir veya el ile girebilirsiniz. Tüm diğer tarihler için hiçbir hesaplama yapılmaz. Aynı ilke toplu iş öznitelik değerleri için de kullanılır. Bir tarih kaynak toplu işlerin tümü için aynıysa, birleştirilmiş toplu iş için bu tarih önerilir. Tarih tüm kaynak toplu işler için aynı değilse, tarih alanı birleştirilmiş toplu işte boş kalır ve el ile girebilirsiniz.

## <a name="what-if-the-dimensions-are-different-on-the-batches-that-i-want-to-merge"></a>Birleştirmek istediğim toplu işlerde boyutlar farklıysa ne olur?
Burada ürün boyutları, izleme boyutları ve depolama boyutlarının nasıl işleneceği açıklanmıştır:

-   **Ürün boyutları** – Seçilen ürünün tüm ürün boyutları aynı olmalıdır. Toplu işleri ürün boyutları genelinde birleştiremezsiniz.
-   **İzleme boyutları** – Ürün için bir toplu iş numarası grubu belirtilirse otomatik olarak yeni bir toplu iş numarası oluşturulur. Toplu iş numarası grubu bir ürüne atanmamışsa, mevcut bir toplu işi seçebilir veya numarayı el ile girebilirsiniz. Seri numaraları kaynak toplu işten birleştiren toplu işin stok günlüğü satırlarına aktarılır.
-   **Depolama boyutları** – Tesis ve ambar depolama boyutları tüm kaynak toplu işler ve birleştirilen toplu iş için aynı olmalıdır. Ancak, birleştirilmiş toplu iş için yeni bir konum ve palet kimliği belirtebilirsiniz.

## <a name="how-does-posting-work"></a>Deftere nakil nasıl işler?
Deftere nakil işleri, günlükler için bir onay işlemi mi kullandığınıza bağlı olarak iki şekilde çalışır. Toplu iş birleştirmeyi onaylanıp deftere nakledilebileceği bir günlüğe aktarmak için **Günlüğe transfer et** ve **Toplu iş birleştirmeyi deftere naklet** eylemlerini kullanabilir veya toplu iş birleştirmeyi doğrudan deftere nakledebilirsiniz. İki eylem arasındaki en önemli fark, bir günlüğe aktarma işleminin toplu iş birleştirmeyi deftere nakletmemesidir. Mevcut bir toplu iş seçili değilse, her iki işlem de yeni bir toplu iş oluşturur; tüm toplu iş ayrıntılarını ve öznitelik değerlerini güncelleştirin ve bir stok günlüğü oluşturun.

-   **Günlüğe transfer et** – Toplu iş birleştirme ayrıntılarını yeni bir stok günlüğüne transfer eder. Otomatik rezervasyonlar ayarlarsanız, kaynak toplu iş miktarları rezerve edilir. Toplu iş birleştirme işleminin ayrıntıları değiştirilemez. Toplu iş birleştirme işlemini değiştirmek için günlüğü silmeniz gerekir. Günlük, başka bir çalışanın daha sonra gerçekleştirmesi gereken bir görev olarak kullanılabilir. Toplu iş miktarının günlük satırına rezervasyonu güvenlik altına alınır. Bu atama işlemi bir kalite planlayıcısının veya bir depo yöneticisinin kendi çalışanları için görevler oluşturmasına izin verir.
-   **Toplu iş birleştirmeyi deftere naklet** – Toplu iş birleştirmeyi doğrudan deftere nakleder. Bu eylem, fiziksel birleştirme gerçekleştikten sonra gerçekleştirilebilir.

Toplu iş birleştirme stok günlüğünü Tüm toplu iş birleştirmeler listesi sayfasında **Tüm toplu iş birleştirmeleri** liste sayfasından onaylayabilirsiniz. **Günlük** &gt; **Deftere naklet** düğmelerine tıklayın. Günlük deftere nakledildikten sonra birleştirilen toplu iş ayrıntılarını değiştiremezsiniz. Toplu iş birleştirmesini bir stok günlüğüne transfer ettikten sonra, yalnızca günlüğün silinmesi durumunda ayrıntıları değiştirebilirsiniz.

## <a name="after-i-merged-a-catchweight-item-why-cant-i-see-the-catchweight-information-in-the-inventory-journal"></a>Fiili ağırlık maddesini birleştirdikten sonra neden stok günlüğünde fiili ağırlık bilgilerini göremiyorum?
Fiili ağırlık maddelerinin toplu işlerini tüm diğer öğeler gibi birleştirebilirsiniz. Ancak, fiili ağırlık bilgileri stok günlüğünde görüntülenmez. Toplu iş birleştirmeyi stok günlüğüne transfer etmeden önce fiili ağırlık bilgilerini doğrulamanız önerilir.




