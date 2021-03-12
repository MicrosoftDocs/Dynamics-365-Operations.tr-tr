---
title: Satış ve pazarlamaya genel bakış
description: Satış akışında çeşitli veri türlerini elde etmek, depolamak ve kullanmak için Satış ve pazarlamayı kullanabilirsiniz. Bu veriler, özgün satış girişimini, gelecekteki takip eylemini ve ek satışları içerir.
author: kfend
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 92303
ms.assetid: 65ca9992-bbfa-4224-bf0e-067a25c7e6a4
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4fe08f2edbbfc9d89de00c4375c1cc938188553
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975072"
---
# <a name="sales-and-marketing-overview"></a>Satış ve pazarlamaya genel bakış

[!include [banner](../includes/banner.md)]

Satış akışında çeşitli veri türlerini elde etmek, depolamak ve kullanmak için Satış ve pazarlamayı kullanabilirsiniz. Bu veriler, özgün satış girişimini, gelecekteki takip eylemini ve ek satışları içerir.

<a name="marketing"></a>Pazarlama
---------

Potansiyel müşteriler bulup onlarla ilişkiler kurmak için pazarlama kampanyalarını ve etkinliklerini kullanın. Böylelikle, ilk etkileşimler satış ilişkileri haline gelebilir. Aşağıdaki süreç akışı, pazarlama için iş sürecini gösterir. [![Pazarlama için iş süreci](./media/marketing01.jpg)](./media/marketing01.jpg)

### <a name="relationships"></a>İlişkiler

Satış ve pazarlamada potansiyel müşterilerle yaptığınız ilk etkileşimler çeşitli durumlarda yaşanabilir. Örneğin, fuara katılırken bir müşteri adayı bulabilirsiniz veya kuruluşunuz toplu bir e-posta gönderme kampanyası yaptıktan sonra bir müşteri adayıyla olası bir iş fırsatı yakalayabilirsiniz. Bir tarafın varlığının akışını, o taraf müşteri haline gelmeden önce anlamanız çok önemlidir. Potansiyel bir müşteri, gerçek bir müşteri haline gelirken varlık ilişkilerinin akışı, aşağıdaki grafikte gösterilmiştir. [![SalesandMarketing01](./media/salesandmarketing01.jpg)](./media/salesandmarketing01.jpg)

### <a name="campaigns"></a>Kampanyalar

Kampanya, aday müşterilerin ilgili kişilerini, müşteri adaylarını, iş fırsatlarını ve kampanyaya katılmak için seçilmiş müşterileri hedefler. Supply Chain Management'ta müşteri potansiyelini en üst düzeye çıkarmak için telefonla pazarlama, postalama ve e-posta kampanyaları gibi çeşitli kampanya türleri oluşturabilirsiniz. Kampanyanız ilerledikçe ve olumlu yanıtlar aldıkça kampanyaya olumlu yanıt veren alıcılarla satış sürecine başlayabilirsiniz.

## <a name="sales"></a>Satış
Teklifler oluşturmak, yeni ve mevcut müşterilere dikey ve çapraz satış yapmak, satış siparişleri oluşturmak ve müşteriler için satış faturaları oluşturmak için satış işlevlerini kullanın. Aşağıdaki süreç akışı, satış için iş sürecini gösterir. [![Satış için iş süreci](./media/sales01.jpg)](./media/sales01.jpg)

### <a name="sales-quotations"></a>Satış teklifleri

Müşterilere sağladığınız malların veya hizmetlerin teklifini sunmak için satış teklifleri oluşturursunuz. Müşteri bir teklif isteyebilir veya potansiyel veya mevcut bir müşteriden gelen isteğe yanıt olarak siz bir teklif oluşturabilirsiniz. Müşteri satış teklifini onayladığında bunu bir satış siparişine dönüştürebilirsiniz.

### <a name="up-sellcross-sell"></a>Dikey satış/çapraz satış

Dikey satış ve çapraz satış, müşteri için bir sipariş girildiğindeki ürün satış teknikleridir. Dikey satışta mevcut ürün yerine bir başka ürün önerilir. Çapraz satışta mevcut ürüne ek olarak bir ürün önerilir. Ürün listelerini ayarladığınızda, bir ürünün ne zaman çapraz satış veya dikey satış olarak önerilmesi gerektiğini belirtmek için belirli kurallar oluşturabilirsiniz.

### <a name="sales-orders"></a>Satış siparişleri

Yeni bir satış siparişi oluştururken, oluşturmak istediğiniz satış türünü seçmelisiniz. Beş seçeneğiniz bulunur. **Not:** Satış siparişi oluşturduktan sonra, satış siparişi **Teslim edildi** durumundaysa **Öğe gereksinimleri** türü dışındaki tüm sipariş türleri değiştirilebilir.

| Satış siparişi türü  | Açıklama                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Günlük           | Bu türü satış siparişi için bir taslak olarak kullanın. Bu türün stok miktarları üzerinde etkisi yoktur ve madde hareketleri oluşturmaz.                                                                                                                                                                    |
| Abonelik      | Bu türü tekrarlayan siparişler için kullanın. Sipariş faturalandırıldığında, sipariş durumu otomatik olarak açık sipariş olarak ayarlanır. Faturalanan teslim edilmiş miktar ve kalan teslimatlar güncelleştirildi. Ambar yönetimi işlevlerini kullanıyorsanız, bu satış siparişi türünü kullanamazsınız. |
| Satış siparişi       | Müşteri bir sipariş verdiğinde veya siparişi teyit ettiğinde bu türü kullanın.                                                                                                                                                                                                                                        |
| İade edilen sipariş    | Müşteri maddeyi iade ettiğinde bu türü kullanın. Otomatik olarak bir iade madde numarası (RMA numarası) atanır.                                                                                                                                                                                            |
| Madde gereksinimleri | Proje aracılığıyla bir madde satışı yaptığınızda, bu tür otomatik olarak oluşturulur.                                                                                                                                                                                                                       |

### <a name="sales-agreements"></a>Satış anlaşması

Satış anlaşması, müşterinin özel fiyatlar ve iskontolar karşılığında bir ürünü, belirli miktarda veya belirli bir zaman aralığında belirli bir tutarda almasını sağlayan bir sözleşmedir. Satış anlaşmasındaki fiyatlar ve iskontolar, mevcut her türlü ticaret anlaşmasında belirtilen fiyatları ve iskontoları geçersiz kılar. Satış anlaşması tanımlanmış bir dönem için geçerlidir. Satış için **Satış siparişi** sayfasında belirtilmiş talep edilen sevk tarihi, geçerli dönem içerisinde olmalıdır. Satış anlaşması varsayılan olarak, bekleme durumundadır. Satış anlaşması ancak **Yürürlükte** durumuna ayarlandığında sipariş verebilirsiniz.

### <a name="backorders"></a>Karşılanamayan siparişler

Siparişleri girip doğrularken, satışın tamamlanabilmesi için karşılanamayan siparişleri ve özel durumları yönetmeniz gerekebilir. Sipariş bakiyeleri ya bir satıcıdan henüz teslim edilmemiş satınalma siparişleridir ya da müşteriye henüz teslim edilmemiş satış siparişleridir. Karşılanamayan siparişlerin takip edilmesi önemlidir. Örneğin bir satıcıdan gelen ürünler gecikirse müşteriye yapılacak teslimat tarihini değiştirilmeniz ve ardından müşteriyi gecikmeyle ilgili bilgilendirmeniz gerekebilir. Maddeye, müşteriye veya satıcıya göre sipariş bakiyelerini görüntüleyebilirsiniz.

#### <a name="viewing-backorders-by-item"></a>Karşılanamayan siparişleri maddeye göre görüntüleme

Karşılanamayan siparişleri madde bazında görüntülediğinizde, belirli bir madde için hareketlerin gelecekte beklenen akışını takip edebilirsiniz. Örneğin aşağıdaki bilgileri kontrol edebilirsiniz:

-   Bir madde için verilen satış siparişlerinin sayısı
-   Satıcılardan gelecek madde teslimatlarının hala eksik olup olmadığı
-   Tüm satış siparişlerini zamanında teslim edebilmeniz için daha çok maddenin sipariş edilmesi gerekip gerekmediği

Bu denetimi yaparak, madde teslimatının zamanlaması hakkında müşterilerin isteklerini yanıtlayabilirsiniz. Aynı zamanda karşılanamayan satış siparişlerini önceliklendirebilir ve eldeki maddeleri siparişler arasında bölebilirsiniz.

#### <a name="viewing-backorders-by-customer"></a>Müşteriye göre karşılanamayan siparişleri görüntüleme

Müşteriye göre satış siparişini görüntülediğinizde, müşterinin karşılanamayan siparişlerinin durumunu görebilirsiniz. Bu denetim, gecikmiş maddeleri bekleyen müşterilere yanıt vermeniz gerektiğinde faydalıdır.

#### <a name="viewing-backorders-by-vendor"></a>Karşılanamayan siparişleri satıcıya göre görüntüleme

Karşılanamayan siparişleri satıcıya göre görüntülediğinizde, eksik teslimatları ve beklenen teslimat tarihlerini takip edebilirsiniz. Bu denetim aynı zamanda, ürünler satıcılardan geldiğinde ve satış siparişlerinin teslimat için çekilmesi gerektiğinde karşılanamayan siparişleri önceliklendirmenize yardımcı olur.

### <a name="invoices"></a>Faturalar

Satış süreci sırasında üç tür fatura oluşturabilirsiniz:

-   Müşteri faturası
-   Serbest metin faturası
-   Proforma fatura

#### <a name="customer-invoice"></a>Müşteri faturası

Müşteri faturası, kuruluşun bir satışla bağlantılı olarak müşteriye verdiği faturadır. Bu tür müşteri faturası, bir başlık ve bir veya daha fazla madde veya hizmet satırı içeren satış siparişini temel alarak oluşturulur. Müşteri faturası, satış siparişi, sevk irsaliyesi ve satış faturası döngüsünü tamamlar.  

Tek müşteri faturasını, bir satış siparişi veya sevk irsaliyesi ve tarihini temel alarak deftere nakledebilir ve yazdırabilirsiniz. Ayrıca sevk irsaliyelerini ve tarihlerini temel alarak birden fazla müşteri faturasını birlikte deftere nakledebilir ve yazdırabilirsiniz. Tek bir müşteri faturasını satış siparişini kullanarak deftere naklettiğinizde, her maddenin **Faturalanan bakiye** miktarı, seçili satış siparişinden faturalanan miktarların toplamı ile güncelleştirilir.  

Tüm maddeler satış siparişindeki **Faturalanan bakiye** ve **Teslimat bakiye** miktarı, 0 (sıfır) olursa, satış siparişinin durumu **Faturalandı** olarak değiştirilir. Her iki alanın miktarı da sıfır değilse, satış siparişinin durumu değişmez ve siparişe ek faturalar ekleyebilirsiniz. Sevk irsaliyesini temel alarak bir veya daha fazla müşteri faturasını deftere nakletmeyi ve yazdırmayı planlıyorsanız, her bir satış siparişi için en azından bir sevk irsaliyesini daha önceden deftere nakletmiş olmanız gerekir. Müşteri faturası sevk irsaliyelerine dayanır ve bunlarda listelenen miktarları yansıtır.  

Belirli bir satış siparişi için olan tüm maddeler henüz sevk edilmemiş olsa bile, o tarihe kadar sevk edilmiş sevk irsaliyesi satır maddelerine dayanan bir satış müşteri faturası oluşturabilirsiniz. Bunu, örneğin, işletmeniz müşteri başına, o ayda sevk ettiğiniz tüm teslimatları kapsayacak şekilde tek bir fatura kesiyorsa, yapabilirsiniz. Her sevk irsaliyesi, satış siparişindeki maddelerin kısmen veya tamamen sevk edildiğini temsil eder.  

Faturayı deftere naklettiğinizde, her madde için **Faturan kalan** miktarı, seçili sevk irsaliyelerinden sevk edilmiş miktarların toplamı ile güncelleştirilir. Tüm maddeler satış siparişindeki **Fatura kalan tutarı** ve **Teslimat bakiye** miktarı, 0 (sıfır) olursa, satış siparişinin durumu **Faturalandı** olarak değiştirilir. Miktar sıfır değilse, satış siparişinin durumu değişmez ve siparişe ek faturalar ekleyebilirsiniz. Stok hareketleri fatura numarasıyla güncelleştirilir ve satış sipariş satırındaki durum **Faturalandı** olarak değiştirilir.

#### <a name="free-text-invoice"></a>Serbest metin faturası

Serbest metin faturası satış siparişiyle ilişkili bir fatura değildir. Genel muhasebe hesaplarını, serbest metin açıklamalarını ve satış tutarının bulunduğu sipariş satırlarını içerir. Bu tür bir faturaya bir madde numarası giremezsiniz ve uygun satış vergisi bilgilerini girmeniz gerekir. Satış için ana bir hesap her fatura satırında belirtilir. Müşteri bakiyesi, serbest metin faturası için kullanılan deftere nakil profili özet hesabına nakledilir.

#### <a name="pro-forma-invoice"></a>Proforma fatura

Proforma fatura, fatura deftere nakledilmeden önce gerçek fatura tutarının bir tahmini olarak hazırlanan faturadır. Müşteri faturası veya serbest metin faturası için bir proforma fatura yazdırabilirsiniz.

### <a name="additional-resources"></a>Ek kaynaklar

#### <a name="blogs"></a>Bloglar

[Dynamics 365 for Finance and Operations'ta satış nasıl işler?](https://financefunction.tech/2018/05/15/how-sales-work-in-dynamics-365-for-finance-and-operations) başlıklı yazıda satış sürecine ilişkin bir genel bakış bulabilirsiniz.
