---
title: Commerce deftere nakil parametreleri
description: Bu makale, Microsoft Dynamics 365 Commerce'de mali ve fiziksel hareketlerin deftere nakledilmesine özel parametreleri açıklamaktadır.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 10ea650b7c5c0cad7e1a3d7556c073aecef06036
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887126"
---
# <a name="commerce-posting-parameters"></a>Commerce deftere nakil parametreleri

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce'de mali ve fiziksel hareketlerin deftere nakledilmesine özel parametreleri açıklamaktadır. Commerce deftere nakil parametreleri, Commerce yönetim merkezinde **Retail ve Commerce \> Yönetim merkezi kurulumu \> Parametreler \> Commerce parametreleri \> Deftere nakil**'de yer almaktadır.

## <a name="periodic-discount-parameters"></a>Periyodik iskonto parametreleri

Aşağıdaki tabloda, mali ve fiziksel hareketlerin deftere nakledilmesine özel periyodik iskonto parametreleri açıklanmaktadır.

| Parametre | Açıklama |
|-----------|-------------|
| Periyodik indirimi deftere naklet | Bu seçenek, periyodik tekliflerin genel muhasebe hesaplarına nakledilip edilmeyeceğini kontrol eder. Periyodik iskontolar, karıştır ve eşle iskontoları, miktar iskontoları ve iskonto tekliflerini kapsar. Bu parametre etkinleştirildiğinde, **Periyodik iskontolar** bölümünde ek alanlar ayarlanabilir. |
| Genel muhasebe hesabı tipi | <p>Periyodik iskontoların deftere nakli için kullanılan hesap türünü seçin:</p><ul><li>**Standart** – Sistem bu sayfadaki indirimle ilgili alanları kullanmaz. Bunun yerine, Commerce yönetim merkezindeki **Deftere nakil** sayfasında tanımlanan hesapları kullanır (**Stok yönetimi \> Kurulum \> Deftere nakil \> Deftere nakil formları**).</li><li>**Periyodik** – Sistem bu sayfadaki indirimle ilgili alanlar tarafından belirtilen Commerce iskonto hesaplarını kullanır. Bu seçeneği belirlerseniz, her teklif türü için bir genel muhasebe (GL) hesabı belirtmelisiniz (iskonto, karıştır ve eşle, miktar ve eşik). Her indirimi ayarladığınızda, bir hesap tanımlayabilirsiniz. İskonto kurulumu sayfasında iskonto hesabı deftere nakli özelliği kullanıldığında, iskonto deftere naklini Commerce iskonto GL hesabından iskonto GL hesabına yeniden sınıflandırmak için ek bir borç girişi ve alacak girişi yapılır. Daha fazla bilgi için bkz. [Perakende iskontoları](retail-discounts-overview.md).</li></ul> |
| Bilgi kodu indirimini deftere naklet | Bu seçenek artık standart Commerce çözümde kullanılmaz ve kullanım dışı bırakılacaktır. |
| Siparişler için periyodik iskontoyu deftere naklet | Bu seçenek periyodik perakende iskontolarının müşteri siparişleri ve çağrı merkezi siparişleri için genel muhasebe defterine nakledilip edilmediğini denetler. |

## <a name="inventory-update-parameters"></a>Stok güncelleştirme parametreleri

Aşağıdaki tabloda, mali ve fiziksel hareketlerin deftere nakledilmesine özel stok güncelleştirme parametreleri açıklanmaktadır.

| Parametre | Açıklama |
|-----------|-------------|
| Toplu iş numaraları bulunamadığında varsayılan toplu iş kodunu kullan | Bu seçenek, toplu iş numaraları bulunmadıysa ve negatif stoka izin veriliyorsa varsayılan toplu iş kimliğinin toplu iş etkin maddeler için kullanılıp kullanılmayacağını kontrol eder. |
| Varsayılan toplu iş kodu | Maddelerle ilgili toplu iş numaraları bulunmadıysa ve **Toplu iş numaraları bulunmadığında varsayılan toplu iş kodunu kullan** parametresi etkinleştirilmişse kullanılacak toplu iş numarası. |

## <a name="aggregation-parameters"></a>Toplam parametreleri

Aşağıdaki tabloda, mali ve fiziksel hareketlerin deftere nakledilmesine özel toplam parametreleri açıklanmaktadır.

| Parametre | Açıklama |
|-----------|-------------|
| Kasaya para nakli | Ekstre deftere nakli sırasında tüm hareketleri toplamak ve her bir bırakma için ayrı bir satır yerine deftere nakil için günlükte tek bir satır oluşturmak üzere bu parametreyi etkinleştirin. |
| Bankaya para nakli | Ekstre deftere nakli sırasında tüm hareketleri toplamak ve her bir bırakma için ayrı bir satır yerine deftere nakil için günlükte tek bir satır oluşturmak üzere bu parametreyi etkinleştirin. |
| Satış hareketleri | Hareketleri, hareket tablosu deftere nakil işleminin bir parçası olarak konsolide etmek için bu parametreyi etkinleştirin. Bu parametreyi etkinleştirmenizi öneririz. Daha önce **Fiş hareketleri** adını taşırdı. |
| İadeleri toplama | Bu seçenek belirlendiğinde her iade hareketi perakende ekstresine nakledildiğinde ayrı bir satış siparişi olarak nakledilir. |

## <a name="batch-processing-parameters"></a>Toplu işleme parametreleri

Aşağıdaki tabloda, mali ve fiziksel hareketlerin deftere nakledilmesine özel toplu işleme parametreleri açıklanmaktadır.

| Parametre | Açıklama |
|-----------|-------------|
| Paralel ekstreler için maksimum sayı | Bu alan, çoklu ekstreleri deftere nakletmek için kullanılan toplu iş görevlerinin sayısını tanımlar. |
| Ekstre başına sipariş işleme için maksimum iş parçacığı sayısı | Bu alan, tek bir ekstre için satış siparişleri oluşturmak ve faturalamak üzere ekstre deftere nakli toplu işi tarafından kullanılan maksimum iş parçacığı sayısını gösterir. Ekstre deftere nakil işlemi tarafından kullanılacak toplam iş parçacığı sayısı, bu parametredeki değer **Paralel ekstre deftere nakil maksimum sayısı** parametresindeki değerle çarpılarak hesaplanır. Bu parametrenin değeri çok yüksek ise, ekstre deftere nakil işleminin performansını olumsuz etkileyebilir. |
| Toplama dahil edilen maksimum hareket satırı | Bu alan, yenisi oluşturulmadan önce tek bir toplam harekete dahil edilecek hareket satırlarının sayısını tanımlar. Toplu hareketler müşteri, iş tarihi veya mali boyutlar gibi farklı toplama ölçütleri temel alınarak oluşturulur. Tek bir hareketindeki satırlar, farklı toplu hareketler arasında bölünmez. Bu nedenle, toplu hareketteki satırların sayısı, farklı ürünlerin sayısı gibi etkenlere bağlı olarak biraz daha yüksek veya düşük olabilir. |
| Mağaza hareketlerini doğrulamak için maksimum iş parçacığı sayısı | Bu alan, hareketleri doğrulamak için kullanılabilecek maksimum iş parçacığı sayısını belirler. Hareketlerinin doğrulanması, hareketler ekstrelerden çekilmeden önce gerçekleşmesi gereken bir adımdır. Kuruluş hediye kartları kullanmıyorsa bile **Commerce parametreleri** sayfasının **Deftere nakil** sekmesindeki **Hediye kartı** hızlı sekmesinde bir hediye kartı ürünü belirlemeniz gerekir. |

Aşağıdaki tabloda, önceki tabloda yer alan parametreler için önerilen değerler listeler. Bu değerler test edilmeli ve dağıtım yapılandırmasına ve kullanılabilir altyapıya göre uyarlanmalıdır. Önerilen değerleri aşan değerler, diğer toplu işlemeyi olumsuz etkileyebilir ve doğrulanmalıdır.

| Parametre | Önerilen değer | Ayrıntılar |
|-----------|-------------------|---------|
| Paralel ekstre deftere nakil işlemi için maksimum sayı | <p>Bu parametreyi **Ekstre** işini çalıştıran toplu iş grubu için kullanılabilen toplu iş görevlerinin sayısına ayarlayın.</p><p>**Genel kural:** Uygulama Nesne Sunucusu (AOS) sanal sunucu sayısını, AOS sanal sunucusu başına kullanılabilen toplu iş görevlerinin sayısıyla çarpın.</p> | **Perakende ekstreleri - İç besleme** özelliği etkinleştirildiğinde bu parametre geçerli değildir. |
| Ekstre başına sipariş işleme için maksimum iş parçacığı sayısı | Değerleri **4**'te test etmeye başlayın. Genellikle, değer **8**'i geçmemelidir. | Bu parametre, satış siparişleri oluşturmak ve deftere nakletmek için kullanılan iş parçacığı sayısını belirtir. Ekstre başına deftere nakil için kullanılabilen iş parçacığı sayısını temsil eder. |
| Toplama dahil edilen maksimum hareket satırı | Değerleri **1000**'te test etmeye başlayın. Commerce yönetim merkezi yapılandırmasına bağlı olarak, daha küçük siparişler performans için daha yararlı olabilir. | Bu parametre, ekstre deftere nakli sırasında her satış siparişine dahil edilecek satır sayısını belirler. Bu sayıya ulaşıldıktan sonra satırlar yeni bir siparişe bölünür. Satış satırı sayısı, belirttiğiniz sayıya tam olarak eşdeğer olmaz çünkü bölünme işlemi satış siparişi düzeyinde gerçekleşir. Yine de numara, ayarlanan sayıya yakın olacaktır. Bu parametre, adlandırılmış müşterisi olmayan perakende hareketleri için satış siparişleri oluşturmak için kullanılır. |
| Mağaza hareketlerini doğrulamak için maksimum iş parçacığı sayısı | Bu parametreyi **4** olarak ayarlamanızı ve yalnızca kabul edilebilir performansa sahip değilseniz artırmanızı öneririz. Bu işlemin kullandığı iş parçacığı sayısı, toplu iş sunucusu tarafından kullanılabilen işlemci sayısını aşamaz. İş parçacığı sayısı çok yüksekse, başka toplu işlemler de etkilenebilir. | Bu parametre, belirli bir mağaza için aynı anda doğrulanabilecek işlem sayısını denetler. |

> [!NOTE]
> Ekstre deftere nakilleriyle ilgili olan ve mağazalar ile **Ticaret parametreleri** sayfasında tanımlanan tüm ayarların ve parametreler, geliştirilmiş ekstre deftere nakil özelliğine uygulanabilir.

## <a name="invoice-parameters"></a>Fatura parametreleri

Aşağıdaki tabloda, mali ve fiziksel hareketlerin deftere nakledilmesine özel fatura parametreleri açıklanmaktadır.

| Parametre | Açıklama |
|-----------|-------------|
| Günlük adı | Satış siparişi ödemeleriyle ilgili müşteri ödeme günlükleri oluşturulduğunda kullanılan ödeme günlüğü adı. Bu ayar, satış noktası (POS), arama merkezi ve e-ticaret kanalı siparişleri için deftere nakledilen tüm sipariş ödemelerine uygulanır. |
| Hesap adı | Ödeme hesabının adı. |
| Ödeme yöntemindeki boyutları önceliklendir | Bu işaret etkinleştirildiğinde ödeme günlükleri, mağazadan alınan boyutlar yerine ödeme yönteminden alınan boyutları önceliklendirir. |
| Vergi hesaplama davranışı | Bu parametre, ekstre deftere nakli sırasında oluşturulan satış siparişlerinin faturalandığı davranışı belirtir:<ul><li>**Yeniden hesapla** – Vergileri yeniden hesaplar.</li><li> **Yeniden hesaplama** – POS'ta hesaplanan vergi tutarlarını kullanır.</li></ul> |
| Günlük adı | Para iadesi için bir müşteri ödeme günlüğü oluşturulduğunda kullanılan günlük adı. Bu ayar, POS, arama merkezi ve e-ticaret kanalı siparişleri için deftere nakledilen tüm sipariş ödemelerine uygulanır. |

## <a name="statement-parameters"></a>Ekstre parametreleri

Aşağıdaki tabloda, mali ve fiziksel hareketlerin deftere nakledilmesine özel ekstre parametreleri açıklanmaktadır.

| Parametre | Açıklama |
|-----------|-------------|
| Hesaplama sırasında stoğu rezerve et | Bu parametre etkinleştirildiğinde, ekstre hesaplaması, ekstre deftere nakledilene kadar stoku geçici olarak rezerve eder. Ekstre hesaplamasının performansını artırmaya yardımcı olmak için bu parametre varsayılan olarak devre dışıdır. Güncelleştirilmiş stok bilgileri, **Deftere nakil stoku** toplu işlemi kullanılarak hesaplanabilir. Perakende mağaza hareketleri için [akış tabanlı](trickle-feed.md) sipariş oluşturma etkinleştirildiğinde **Deftere nakil** stok toplu işinin artık kullanılmadığını unutmayın. |
| Sayımın devre dışı bırakılması gerekli | Bu bayrak Commerce yönetim merkezine nakil sırasında sayımı devre dışı bırakır. |
| Hata durumunda mali boyutları yeniden hesapla | Bu parametre etkinleştirildiğinde, ekstre deftere nakli başarısız olursa ardıl ekstre deftere nakil işlemlerinde mali boyutlar yeniden değerlendirilebilir. |
| İade mağazasının mali boyutlarını kullan | Bu parametre etkinleştirildiğinde, orijinal hareketteki mali boyutlar yerine mağazanın mali boyutlarını kullanan bağlantılı iade satış siparişleri oluşturulabilir. |
| İadelerin bağlantısını kaldır | Bu parametre etkinleştirildiğinde, ekstre, görünmeyen iadeler olarak deftere nakledilmemiş satışlar için geri iadeler oluşturabilir. Bu parametre varsayılan olarak devre dışıdır ve devre dışı tutmanızı öneririz. |
| Yuvarlama farkının deftere naklini devre dışı bırakın | Bu parametre, ödemelerin işlenmesi sırasında hareket ödemesi ve brüt tutar arasındaki yuvarlama farkının deftere naklini devre dışı bırakır. |
| Müşteri havalelerini otomatik kapat | Bu parametre etkinleştirildiğinde, perakende ekstre deftere nakli sırasında deftere nakledilen müşteri havaleleri, müşterinin açık hareketlerine karşı kapatılır. |
| POS'tan nakit yönetimi mutabakatını etkinleştirin ve kullanın | Bu parametre etkinleştirildiğinde, POS'ta nakit yönetimi mutabakatı yapılır ve ekstre satırları oluşturmak için değerler perakende mali tablosu deftere nakline gönderilir. |
| Genel muhasebe fiş ayrıntısı düzeyi | Bu parametre, 'tan kaynaklanan seçili hareketler için genel muhasebe fiş öğesine dahil edilen ayrıntı düzeyini tanımlar. Hareket türleri, gelir, giderler ve iskontoları içerir. İskontolar için bu parametre yalnızca periyodik iskontonun hesap numarası ve normal iskonto için hesap numarası aynı olmadığında dikkate alınır. Ayrıntı gerekli değilse, bu aktarımlar için önerilen değer **Özet** olarak alınır. Özet düzeyinde deftere nakil tanımlandığında, **TransactionDiscountTrans.RecID** alanı doldurulmaz. Commerce 10.0.27 sürümünde bu bayrak yeniden adlandırıldı ve taşındı. Daha önce **Ayrıntı düzeyi** adını taşıyordu ve **Stok güncelleştirmesi** bölümündeydi. |
