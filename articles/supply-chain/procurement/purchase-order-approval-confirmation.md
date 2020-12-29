---
title: Satınalma siparişlerini onaylama
description: Bu konuda, oluşturulduktan sonra bir satınalma siparişinin geçtiği durumlar ve satınalma siparişlerinde değişiklik yönetiminin etkinleştirilmesinin etkisi açıklanmaktadır.
author: mkirknel
manager: tfehr
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchOrderInReview, PurchOrderApproved, PurchOrderInDraft, PurchOrderAssignedToMe, VendPurchOrderJournalListPage, PurchTableWorkflowDropDialog, VendPurchOrderJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3879079e233a881ea0adc1f5e2ba39ab70b372d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439618"
---
# <a name="approve-and-confirm-purchase-orders"></a>Satınalma siparişlerini onaylama

[!include [banner](../includes/banner.md)]

Bu konuda, oluşturulduktan sonra bir satınalma siparişinin (PO) geçtiği durumlar ve PO'larda değişiklik yönetiminin etkinleştirilmesinin etkisi açıklanmaktadır.

Satınalma siparişi (PO) oluşturulduktan sonra bir onay işleminden geçmelidir. Satıcı siparişi onayladıktan sonra PO **Teyit Edildi** durumuna ayarlanır.

## <a name="approval-of-purchase-orders"></a>Satınalma siparişlerinin onayı
SAS'lar oluşturulduklarında **Onaylandı** durumuna sahip bir değişiklik yönetimini kullanmazlar ancak ilk oluşturulduklarında **Taslak** durumuna sahip değişiklik yönetimini kullanırlar. Master planlamadan planlı sipariş olarak kesinleştirilerek oluşturulan bir PO değişiklik yönetimi ayarlarına bakılmaksızın her zaman **Onaylandı** durumuna ayarlanır. Bir PO yalnızca **Onaylandı** durumuna ulaştığında stok hareketlerini oluşturur. Bu nedenle bu stok sipariş kabul edilene kadar rezervasyon veya işaretleme için kullanılabilir görünmez.

PO'lar için değişiklik yönetimini **Tedarik ve kaynak atama parametreleri** sayfasındaki **Değişiklik yönetimini etkinleştir** seçeneğine ayarlayarak etkinleştirin. Değişiklik yönetimi etkinleştirildiğinde PO'lar tamamlandıktan sonra onay iş akışından geçmelidir. Supply Chain Management onay işlemini göstermek için bir akışı tanımlayabileceğiniz bir iş akışı işlemi düzenleyicisine sahiptir. Bu iş akışı otomatik onaya ilişkin kuralları, belli PO'lara kimlerin atanacağını belirleyen kuralları ve uzun süredir onay için bekleyen bir iş akışını ilerletmek için kuralları içerebilir. Değişiklik yönetimi işlemini tüm satıcılar veya belirli satıcılar için etkinleştirebilirsiniz. İşlemi PO'lar için geçersiz kılacak şekilde de ayarlayabilirsiniz.

Değişiklik yönetimi etkinleştirildiğinde PO'lar **Sonlandırıldı** ile **Taslak** arasında altı onay durumundan geçer. Sipariş onaylandıktan sonra değiştirmek isteyen kullanıcılar **Değişiklik iste** eylemini kullanmalıdır.

| Onay durumu | Tanım                                                                      | İstenen değişiklik etkinleştirilir |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Taslak           | SAS bir taslaktır ve SAS iş akışında onaya gönderilmemiştir.     | Hayır                        |
| İncelemede       | PO, PO iş akışında onaya gönderilmiştir. Onay bekliyor.       | Hayır                        |
| Reddedildi        | PO onay işlemi sırasında reddedildi.                                 | Hayır                        |
| Onaylandı        | PO onaylandı.                                                             | Evet                       |
| Onaylı       | PO teyit edildi. SAS onaylanana kadar teyit edilemez.        | Evet                       |
| Sonuçlandırılmış       | PO son halini aldı. Şimdi mali olarak kapalıdır ve artık değiştirilemez. | Hayır                        |

## <a name="confirming-purchase-orders"></a>Satınalma siparişlerini teyit etme
Onay durumu **Onaylandı** olan PO'lar teyit edilmeden önce ek adımlardan geçebilir. Örneğin, satıcıya fiyatları, iskontoları veya teslim tarihlerini sormak için bir satınalma sorgusu göndermeniz gerekebilir. Bu durumda, PO'yu **Satınalma sorgusu** eylemini kullanarak **Harici incelemede** durumuna ayarlayabilirsiniz.

Satıcı portalını kullanmaya ayarlanmış satıcılar portaldaki siparişleri gözden geçirebilir ve bunları onaylayabilir veya reddedebilir. Bu gözden geçirme işlemi sırasında PO **Harici incelemede** durumundadır. Satıcı portalı, satıcıdan gelen bir teyit Supply Chain Management'daki siparişi otomatik olarak teyit edecek şekilde yapılandırılabilir. Alternatif olarak, satıcıdan teyit aldıktan sonra bir PO'yu el ile teyit edebilirsiniz. Satıcı PO'yu reddederse reddetme eylemi, reddetme nedeni ve değişiklik önerileri ile birlikte alınır. Bu durumda PO **Harici incelemede** durumunda kalır.

Fiili teyit işlenmeden önce sipariş için bir proforma teyidi oluşturma seçeneği de bulunmaktadır. Bu seçenek yalnızca satıcı ile paylaşabileceğiniz bir rapor oluşturur. Herhangi bir günlük bilgisi oluşturmaz.

Satıcı siparişi kabul ettikten sonra bir sonraki adım PO'yu taahhüt edilmiş olarak kaydetmektir. Bu adımı **Teyit** eylemini veya **Teyit Et** eylemini kullanarak tamamlayabilirsiniz. Bu eylemler siparişin onay durumunu **Teyit Edildi** olarak ayarlar. Bir siparişin teyidi iki ek işlem başlatır:

-   Sistemde teyit edilenin tam bir kopyasını depolamak için bir günlük oluşturulur. Bazı durumlarda, siparişlerin değiştirilmesi gerekir ve güncelleştirilmiş sipariş teyit edildikten sonra ek günlükler oluşturulur. Bu günlükler teyit edilen siparişlerin çeşitli sürümlerinin geçmişini görüntülemenizi sağlar.
-   Muhasebe dağılımları oluşturulur ve bu işlevler etkinleştirilirse sipariş kontrolleri ve bütçe kontrolleri gerçekleşir. Kontrol başarısız olursa yeniden teyit edilmeden önce PO'da değişiklik yapılması gerektiğini bildiren bir hata mesajı alırsınız.

Bir satıcı satınalma için ödeme sağlanacağına dair bir tür güvence isteyebilir. Bu teminatı borç hesapları işlemlerinde sağlamak için çeşitli yöntemler bulunmaktadır. Örneğin, **Ön ödeme** eylemi PO için fon rezerve eder ve bu ön ödeme PO'ya kaydedilir.

## <a name="changing-purchase-orders"></a>Satınalma siparişlerinin değiştirilmesi
Bazı durumlarda **Onaylandı** veya **Teyit Edildi** onay durumlarına ulaşıldıktan sonra PO'yu değiştirmeniz gerekebilir.

PO değişiklik yönetimi işlemi kullanılarak oluşturulmuşsa siparişi tekrar çağırarak veya sipariş zaten onaylanmışsa **Değişiklik iste** eylemini kullanarak değişiklikleri yapabilirsiniz. Bu durumda onay durumu tekrar **Taslak** durumuna dönüşür ve sonra siparişi değiştirebilirsiniz. Değişiklikler yapıldıktan sonra SAS'ı yeniden onaya gönderebilirsiniz. Yeniden onaylama gerektiren değişiklik türlerini **Satınalma ilkeleri** sayfasındaki **Satınalma emirleri için yeniden onaylama kuralı** ilke kuralını kullanarak yapılandırabilirsiniz.

Bir satınalma satırı için sipariş edilen miktarın bir parçası teslim edilmişse, satınalma siparişi **Taslak** durumundayken sipariş edilen miktarı değiştiremezsiniz. Ancak, **Taslak** durumundaki satınalma siparişinin satırında **Teslimat kalan** miktarını değiştirebilirsiniz.

Bir sipariş teyit edildikten sonra artık onu silemezsiniz. Ancak, miktarın alınmaması veya faturalanmaması koşuluyla siparişteki toplam miktarı veya kalan miktarı iptal edebilirsiniz. Daha sonra başka işlem yapılmasını önlemek için **Sonlandır** eylemini kullanabilirsiniz. 


## <a name="canceling-purchase-orders"></a>Satınalma siparişlerini iptal etme

Bir SAS, başlıktaki **İptal** eylemi kullanılarak iptal edilebilir.

Miktar kısmen kaydedilmişse, alınmışsa veya faturalanmışsa, yalnızca kaydedilmeyen, teslim alınmayan veya faturalanmayan kalan miktarı iptal edebilirsiniz. Sipariş miktarı uygun şekilde azaltılır. Satırdaki miktar güncelleştirildiğinde satır durumu da güncelleştirilir. Örneğin, satırdaki orijinal miktar 5 olsun ve 3 tanesi teslim alınsın. Bu durumda, yalnızca ikisi iptal edilebilir. Daha sonra satır durumu **Alındı** olarak güncelleştirilir.

Sipariş satırına bir teslimat bakiyesi eklenirse ve sipariş satırındaki miktarı aşarsa, **İptal** eylemi fazla miktarı iptal etmez. Bunun yerine, satır **Açık sipariş** durumunda kalır, çünkü kalan bir miktar vardır. Örneğin, satırdaki orijinal miktar 5 ve teslimat bakiyesi 7 olsun. Sipariş iptal edilirse, beş adet iptal edilir ve stok hareketlerinde de görebileceğiniz gibi 2 adet kalır.

Bir SAS satırındaki miktarın tamamını iptal etmek için, satırdaki teslim bakiyesi miktarını iptal etmelisiniz. Satır **İptal edildi** olarak güncelleştirilecektir.

SAS, değişiklik yönetimi altındaysa, siparişin veya teslimat bakiyesinin iptal edilmesi gibi tüm değişiklikler iş akışı sistemine gönderilmeli ve işlem tamamlanmadan önce onaylanmalıdır ve stok hareketleri iptal edildi olarak güncelleştirilebilir.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Satın alma siparişine genel bakış](purchase-order-overview.md)

[Satınalma siparişleri oluşturma](purchase-order-creation.md)

[Ürün girişi ve satınalma siparişleri karşılaştırması](product-receipt-against-purchase-orders.md)

[Satıcı faturalarına genel bakış](../../finance/accounts-payable/vendor-invoices-overview.md)



