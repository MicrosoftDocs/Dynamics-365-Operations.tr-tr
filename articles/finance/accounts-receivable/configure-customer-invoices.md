---
title: Müşteri faturası oluşturma
description: '**Satış siparişi için müşteri faturası** kuruluşun bir müşteriye verdiği, satışla ilişkili bir faturadır.'
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f5b9866fc7afba205b84b372c6a204ec4c8f64d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772732"
---
# <a name="create-a-customer-invoice"></a>Müşteri faturası oluşturma

[!include [banner](../includes/banner.md)]

**Satış siparişi için müşteri faturası** kuruluşun bir müşteriye verdiği, satışla ilişkili bir faturadır. Bu türdeki bir satış faturası, satış satırları ve madde numaraları içeren bir satış siparişine dayanarak oluşturulur. Madde numaraları genel muhasebede belirtilir ve deftere kaydedilir. Muavin defteri günlük girişleri, bir satış siparişi için müşteri faturası için kullanılamaz Daha fazla bilgi için bkz. [Satış siparişi faturaları oluşturun](tasks/create-sales-order-invoices.md).

Bir **serbest metin faturası** satış siparişiyle ilişkili değildir. Genel muhasebe hesaplarının, serbest metin açıklamalarının ve girdiğiniz satış tutarının bulunduğu sipariş satırlarını içerir. Bu tür bir faturaya bir madde numarası giremezsiniz. Uygun satış vergisi bilgilerini girmeniz gerekir. Satış için bir ana hesap her fatura satırında belirtilir ve **serbest metin faturası** sayfasındaki **Dağıtım tutarları** üzerine tıklatarak birden çok genel muhasebe hesaplarına dağıtabilirsiniz. Ayrıca, müşteri bakiyesi gelen serbest metin faturası için kullanılan deftere nakil profili özet hesabına nakledilir.

Daha fazla bilgi için bkz.:

[Serbest metin faturaları oluştur](../accounts-receivable/create-free-text-invoice-new.md)

[Serbest metin faturası şablonu oluşturma](../accounts-receivable/create-free-text-invoice-template-new.md)

[Bir müşteriye serbest metin faturası şablonu atayın](tasks/assign-free-text-invoice-template-customer.md)

[Yinelenen serbest metin faturaları oluşturma ve deftere nakletme](tasks/post-recurring-free-text-invoices.md)


Bir **Proforma fatura** bir fatura deftere nakledilmeden önce gerçek fatura tutarlarının bir tahmini olarak hazırlanan faturadır. Satış siparişi için müşteri faturası veya bir serbest metin faturası için bir proforma fatura yazdırabilirsiniz.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Satış siparişine dayalı olan tekil müşteri faturalarını deftere nakledin veya yazdırın.
Bir satış siparişini temel alan bir fatura oluşturmak için bu işlemi kullanın. Mal veya hizmeti teslim etmeden önce müşteriye fatura kesmek isterseniz bunu yapabilirsiniz. 

Bir faturayı deftere naklettiğinizde, her maddenin **Fatura kalan tutarı** miktarı, seçili satış siparişinden faturalanan miktarların toplamı ile güncelleştirilir. Eğer tüm maddeler için **Fatura kalanı** miktarı ve **Teslimat bakiyesi** satış siparişindeki miktarı 0 (sıfır) olursa, satış siparişinin durumu **Faturalandı** olarak değiştirilir. Eğer **Fatura kalanı** miktarı 0 (sıfır) değilse, satış siparişinin durumu değiştirilmez ve buna ek faturalar girilebilir.

Satış siparişlerinin durumunu **Tüm satış siparişleri** listesi sayfasından görüntüleyebilirsiniz. **Açık müşteri faturaları** liste sayfasını deftere nakledilen faturaları görüntülemek için kullanın.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Sevk irsaliyesine ve tarihe dayalı olan tekil müşteri faturalarını deftere nakledin veya yazdırın.
Bu işlemi, satış siparişine bir veya daha fazla sevk irsaliyesinin deftere nakledildiğinde kullanın. Müşteri faturası bu sevk irsaliyelerine dayanır ve bunların miktarlarını yansıtır. Faturanın mali bilgileri, faturayı naklettiğinizde girilen bilgilere dayanır. 

Belirli bir satış siparişi için olan tüm maddeler henüz sevk edilmemiş olsa bile, o tarihe kadar sevk edilmiş sevk irsaliyesi satır maddelerine dayanan bir satış müşteri faturası oluşturabilirsiniz. Bunu, örneğin, tüzel kişiliğiniz müşteri başına, o ayda sevk ettiğiniz tüm teslimatları içeren bir fatura kesiyorsa yapabilirsiniz. Her sevk irsaliyesi, satış siparişindeki maddelerin kısmen veya tamamen sevk edildiğini temsil eder. 

Faturayı deftere naklettiğinizde, her madde için **Faturan kalan** miktarı, seçili sevk irsaliyelerinden sevk edilmiş miktarların toplamı ile güncelleştirilir. Eğer tüm maddeler için **Fatura kalanı** miktarı ve **Teslimat bakiyesi** satış siparişindeki miktarı 0 (sıfır) olursa, satış siparişinin durumu **Faturalandı** olarak değiştirilir. Eğer **Fatura kalanı** miktarı 0 (sıfır) değilse, satış siparişinin durumu değiştirilmez ve buna ek faturalar girilebilir. 

Stok hareketleri fatura numarasıyla güncelleştirilir ve satış siparişindeki **Satır durumu** alanı **Faturalandı** olarak değiştirilir. 

Satış siparişlerinin durumunu **Tüm satış siparişleri** listesi sayfasından görüntüleyin.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Satış siparişlerini veya sevk irsaliyelerini deftere nakletmek için konsolide edin.
Bu işlemi, bir veya daha fazla satış siparişi faturalanmaya hazır durumda olduğunda ve bunları tek bir faturada birleştirmek istediğinizde kullanın. 

**Satış siparişi** liste sayfasında birden fazla fatura seçebilirsiniz ve sonra **Faturalar oluştur**'u kullanarak bunları birleştirebilirsiniz. **Sipariş özeti** ayarını, **Faturayı deftere nakletme** sayfasında siparişi numarasına göre özetlemek için (tek bir satış siparişi için birden çok sevk irsaliyesi olduğunda) veya fatura hesabına göre (tek bir fatura hesabı için birden fazla satış siparişi bulunduğunda) değiştirebilirsiniz. **Yerleştir** düğmesini kullanıp satış siparişlerini **Sipariş özeti** ayarlarına dayanarak tek bir faturada bir araya getirin.

## <a name="additional-settings-that-change-the-posting-behavior"></a>Deftere nakil davranışını değiştiren ek ayarlar
Aşağıdaki alanlar deftere nakil işleminin davranışını değiştirir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Alan</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Miktar</td>
<td>Belgenin deftere naklinde temel alınacak miktarları seçin. Kullanılabilecek seçenekler, hangi türde bir belgeyi naklettiğinize göre, örneğin sevk irsaliyesi veya fatura gibi, değişmektedir.
<ul>
<li><strong>Şimdi teslim et</strong>: <strong>Şimdi teslim et</strong> alanına girilen tüm miktarları seçin. Bu seçeneği kısmi bir siparişi onaylamak veya teslim etmek için kullanın.</li>
<li><strong>Çekilen</strong>: Çekilen tüm miktarları seçin.</li>
<li><strong>Tümü</strong> – Geçerli belge türü ile henüz güncelleştirilmeyen satış siparişlerindeki tüm miktarları seçmek için kullanılır.</li>
<li><strong>Sevk irsaliyesi</strong>: Sevk irsaliyesiyle güncelleştirilen tüm miktarları seçin.</li>
<li><strong>Çekilen miktar ve stoklanmayan ürünler</strong> – Çekilen tüm miktarları ve stoklanmamış tüm ürün miktarlarını seçin.</li>
</ul></td>
</tr>
<tr class="even">
<td>Deftere nakletme</td>
<td><ul>
<li>Satış siparişini günlüğe girmek için bu seçeneği belirleyin.</li>
<li>Proforma satış siparişi yazdırmak için bu seçeneği kaldırın. <strong>Not:</strong> Ödeme planı için anlaşma yaptıysanız, ödeme planı proforma satış siparişinde gösterilmez. Ödeme planları yalnızca fiili satış emirlerinde gösterilir.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Geç seçim</td>
<td>Seçili sorguyu daha sonra uygulamak için bu seçeneği belirleyin. Bu seçenek, toplu işler için kullanılır. Toplu iş çalıştırıldığında, sorgu çalıştırılır.</td>
</tr>
<tr class="even">
<td>Miktarı azalt</td>
<td>Belge deftere nakledildiğinde, teslim edilen miktarın kullanılabilir stoğa eşit olması için teslim edilen miktarı otomatik olarak azaltmak için bu seçeneği seçin.</td>
</tr>
<tr class="odd">
<td>Yazdır</td>
<td>Belgelerin ne zaman yazdırılacağını seçin:
<ul>
<li><strong>Cari</strong> - Belgeleri her bir faturayı güncelleştirildikten sonra yazdırın.</li>
<li><strong>Sonra</strong>: Tüm faturalar güncelleştirildikten sonra belgeleri yazdırın.</li>
</ul>
<strong>Not:</strong> <strong>Yazdır alanı</strong> yalnızca, <strong>Faturayı yazdır</strong>, <strong>Onayı yazdır</strong>, <strong>Malzeme çekme listesini yazdır</strong> veya <strong>Sevk irsaliyesi yazdır</strong> seçeneğini seçerseniz kullanılabilir. Örneğin, <strong>Form sıralaması</strong> sayfasında, sistemi bilgileri fatura hesabına göre sıralayacak şekilde ayarlarsınız. Fatura hesabı tarafından sıralanan toplu işteki belgeleri yazdırmak için <strong>Sonra</strong>'yı seçebilirsiniz. Aksi halde, belgeler işleme tamamlanmadan önce yazdırılır ve belgeler <strong>Form sıralama</strong> sayfasında belirtilen sırada sıralanmaz.</td>
</tr>
<tr class="even">
<td>Faturayı yazdır</td>
<td>Faturayı yazdırmak için bu seçeneği seçin. Bu seçenek devre dışı bırakılırsa, yazdırma olmadan bir faturayı deftere nakledebilirsiniz.</td>
</tr>
<tr class="odd">
<td>E-posta gönder</td>
<td>Fatura deftere nakledildikten sonra satış siparişinin faturasını müşteriye e-posta eki göndermek için bu seçeneği seçin. Ekler PDF ve XML dosyaları olarak gönderilir. Bu seçenek yalnızca <strong>Elektronik fatura parametreleri </strong>sayfasındaki <strong>CFD etkinleştir (elektronik faturalar)</strong>'ı seçtiğinizde kullanılabilir. <strong>Not:</strong> (MEX) Bu denetim yalnızca birincil adresi Meksika'daki tüzel kişilikler için kullanılabilir.</td>
</tr>
<tr class="even">
<td>Yazdırma yönetimi hedefini kullan</td>
<td>Bu seçeneği <strong>Yazdırma Yönetimi Kurulumu</strong> sayfasında hareket, belge veya modülü üzerinde belirtilen yazdırma ayarlarını kullanmak için seçin.</td>
</tr>
<tr class="odd">
<td>Kredi limitini denetle</td>
<td>Kredi limiti denetimi gerçekleştirilirken analiz edilmesi gereken bilgileri seçin.
<ul>
<li><strong>Yok</strong>: Kredi limiti kontrolü için bir gereksinim mevcut değildir.</li>
<li><strong>Bakiye</strong> - Kredi limiti müşteri bakiyesine karşı denetlenir.</li>
<li><strong>Bakiye + sevk irsaliyesi veya ürün girişi</strong>: Kredi limiti müşteri bakiyesi ve teslimatlara göre denetlenir.</li>
<li><strong>Bakiye + Tümü</strong> - Kredi limiti müşteri bakiyesiyle, teslimatlarla ve açık siparişlerle karşılaştırılır.</li>
</ul></td>
</tr>
<tr class="even">
<td>Alacak düzeltme</td>
<td>Alacak dekontunu fiş hareketlerinde borç olarak görüntülemek için bu seçeneği belirleyin.</td>
</tr>
<tr class="odd">
<td>Kalan alacak miktarı</td>
<td>Borç dekontunu deftere naklediyorsanız, kalan miktarı siparişte bırakmak için bu seçeneği seçin. Bu seçenek işaretlenmezse kalan miktar 0 (sıfır) olarak ayarlanır.</td>
</tr>
<tr class="even">
<td>Özet güncelleştirme kapsamı</td>
<td>Birden fazla satış siparişinin nasıl özetlenmesi gerektiğini seçin:
<ul>
<li><strong>Hiçbiri</strong> - Satış siparişlerini özetleme. Örneğin, her satış siparişi için ayrı bir fatura oluşturulur.</li>
<li><strong>Fatura hesabı</strong>: Seçilen tüm siparişleri <strong>Özet güncelleştirme parametreleri</strong> sayfasında ayarlanmış olan ölçüte göre özetleyin.</li>
<li><strong>Sipariş</strong>: Seçilen aralıktaki siparişlerin tek bir sipariş olarak özetler. Siparişler, <strong>Özet güncelleştirme parametreleri</strong> sayfasında ayarlanan ölçütlere göre özetlenir. Bu seçenek işaretlerseniz, <strong>Satış siparişi</strong> alanında bir değer işaretlemeniz gerekir.</li>
<li><strong>Otomatik özet</strong>: Eğer özet güncelleştirmeleri <strong>Özet güncelleştirme</strong> sayfasında belirtildiyse, <strong>Özet güncelleştirme parametreleri</strong> sayfasında belirlenen kriterlere dayanarak tüm siparişleri özetleyin. Eğer Özet güncelleştirmeleri belirlemezseniz, sipariş ayrı olarak deftere nakledilir.</li>
<li><strong>Sevk irsaliyesi</strong>: Seçilen aralıktaki siparişleri sevk irsaliyesi başına bir fatura şeklinde özetler. Bu seçenek yalnızca, <strong>Miktar</strong> alanında <strong>Sevk irsaliyesi</strong> seçiliyse kullanılabilir.</li>
</ul></td>
</tr>
</tbody>
</table>





