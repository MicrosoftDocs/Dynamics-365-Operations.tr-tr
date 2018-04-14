---
title: "Satınalma siparişlerini onaylama ve doğrulama"
description: "Bu makalede oluşturulduktan sonra bir satınalma siparişinin (PO) geçtiği durumlar ve değişiklik yönetiminin etkinleştirilmesinin PO'lara etkisi tanımlanır."
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Retail
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1c7209c91f3821a77e9b127d767c78df403ff6cc
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="approve-and-confirm-purchase-orders"></a>Satınalma siparişlerini onaylama ve doğrulama

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [retail name](../includes/retail-name.md)]

Bu makalede oluşturulduktan sonra bir satınalma siparişinin (PO) geçtiği durumlar ve değişiklik yönetiminin etkinleştirilmesinin PO'lara etkisi tanımlanır.

Satınalma siparişi (PO) oluşturulduktan sonra bir onay işleminden geçmelidir. Satıcı siparişi onayladıktan sonra PO **Teyit Edildi** durumuna ayarlanır.

## <a name="approval-of-purchase-orders"></a>Satınalma siparişlerinin onayı
PO'lar oluşturulduklarında **Onaylandı** durumuna sahip bir değişiklik yönetimini kullanmazlar ancak ilk oluşturulduklarında **Taslak** durumuna sahip değişiklik yönetimini kullanırlar. Master planlamadan planlı sipariş olarak kesinleştirilerek oluşturulan bir PO değişiklik yönetimi ayarlarına bakılmaksızın her zaman **Onaylandı** durumuna ayarlanır. Bir PO yalnızca **Onaylandı** durumuna ulaştığında stok hareketlerini oluşturur. Bu nedenle bu stok sipariş kabul edilene kadar rezervasyon veya işaretleme için kullanılabilir görünmez.  

PO'lar için değişiklik yönetimini **Tedarik ve kaynak atama parametreleri** sayfasındaki **Değişiklik yönetimini etkinleştir** seçeneğine ayarlayarak etkinleştirin. Değişiklik yönetimi etkinleştirildiğinde PO'lar tamamlandıktan sonra onay iş akışından geçmelidir. Microsoft Dynamics 365 for Finance and Operations onay işlemini göstermek için bir akışı tanımlayabileceğiniz bir iş akışı işlemi düzenleyicisine sahiptir. Bu iş akışı otomatik onaya ilişkin kuralları, belli PO'lara kimlerin atanacağını belirleyen kuralları ve uzun süredir onay için bekleyen bir iş akışını ilerletmek için kuralları içerebilir. Değişiklik yönetimi işlemini tüm satıcılar veya belirli satıcılar için etkinleştirebilirsiniz. İşlemi PO'lar için geçersiz kılacak şekilde de ayarlayabilirsiniz.  

Değişiklik yönetimi etkinleştirildiğinde PO'lar **Sonlandırıldı** ile **Taslak** arasında altı onay durumundan geçer. Sipariş onaylandıktan sonra değiştirmek isteyen kullanıcılar **Değişiklik iste** eylemini kullanmalıdır.

| Onay durumu | Açıklama                                                                      | İstenen değişiklik etkinleştirilir |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Taslak           | PO bir taslaktır ve PO iş akışında onaya gönderilmemiştir.     | Hayır                        |
| İncelemede       | PO, PO iş akışında onaya gönderilmiştir. Onay bekliyor.       | Hayır                        |
| Reddedildi        | PO onay işlemi sırasında reddedildi.                                 | Hayır                        |
| Onaylandı        | PO onaylandı.                                                             | Evet                       |
| Onaylandı       | PO teyit edildi. PO onaylanana kadar teyit edilemez.        | Evet                       |
| Sonlandırıldı       | PO son halini aldı. Şimdi mali olarak kapatılır ve artık değiştirilemez. | Hayır                        |

## <a name="confirming-purchase-orders"></a>Satınalma siparişlerini teyit etme
Onay durumu **Onaylandı** olan PO'lar teyit edilmeden önce ek adımlardan geçebilir. Örneğin, satıcıya fiyatları, iskontoları veya teslim tarihlerini sormak için bir satınalma sorgusu göndermeniz gerekebilir. Bu durumda, PO'yu **Satınalma sorgusu** eylemini kullanarak **Harici incelemede** durumuna ayarlayabilirsiniz.  

Satıcı portalını kullanmaya ayarlanmış satıcılar portaldaki siparişleri gözden geçirebilir ve bunları onaylayabilir veya reddedebilir. Bu gözden geçirme işlemi sırasında PO **Harici incelemede** durumundadır. Satıcı portalı, satıcıdan gelen bir teyit Finance and Operations'daki siparişi otomatik olarak teyit edecek şekilde yapılandırılabilir. Alternatif olarak, satıcıdan teyit aldıktan sonra bir PO'yu el ile teyit edebilirsiniz. Satıcı PO'yu reddederse reddetme eylemi, reddetme nedeni ve değişiklik önerileri ile birlikte alınır. Bu durumda PO **Harici incelemede** durumunda kalır.  

Fiili teyit işlenmeden önce sipariş için bir proforma teyidi oluşturma seçeneği de bulunmaktadır. Bu seçenek yalnızca satıcı ile paylaşabileceğiniz bir rapor oluşturur. Herhangi bir günlük bilgisi oluşturmaz.  

Satıcı siparişi kabul ettikten sonra bir sonraki adım PO'yu taahhüt edilmiş olarak kaydetmektir. Bu adımı **Teyit** eylemini veya **Teyit Et** eylemini kullanarak tamamlayabilirsiniz. Bu eylemler siparişin onay durumunu **Teyit Edildi** olarak ayarlar. Bir siparişin teyidi iki ek işlem başlatır:

-   Sistemde teyit edilenin tam bir kopyasını depolamak için bir günlük oluşturulur. Bazı durumlarda, siparişlerin değiştirilmesi gerekir ve güncelleştirilmiş sipariş teyit edildikten sonra ek günlükler oluşturulur. Bu günlükler teyit edilen siparişlerin çeşitli sürümlerinin geçmişini görüntülemenizi sağlar.
-   Muhasebe dağılımları oluşturulur ve bu işlevler etkinleştirilirse sipariş kontrolleri ve bütçe kontrolleri gerçekleşir. Kontrol başarısız olursa yeniden teyit edilmeden önce PO'da değişiklik yapılması gerektiğini bildiren bir hata mesajı alırsınız.

Bir satıcı satınalma için ödeme sağlanacağına dair bir tür güvence isteyebilir. Bu teminatı borç hesapları işlemlerinde sağlamak için çeşitli yöntemler bulunmaktadır. Örneğin, **Ön ödeme** eylemi PO için fon rezerve eder ve bu ön ödeme PO'ya kaydedilir.

## <a name="changing-purchase-orders"></a>Satınalma siparişlerinin değiştirilmesi
Bazı durumlarda **Onaylandı** veya **Teyit Edildi** onay durumlarına ulaşıldıktan sonra PO'yu değiştirmeniz gerekebilir.  

PO değişiklik yönetimi işlemi kullanılarak oluşturulmuşsa siparişi tekrar çağırarak veya sipariş zaten onaylanmışsa **Değişiklik iste** eylemini kullanarak değişiklikleri yapabilirsiniz. Bu durumda onay durumu tekrar **Taslak** durumuna dönüşür ve sonra siparişi değiştirebilirsiniz. Değişiklikler yapıldıktan sonra PO'yu yeniden onaya gönderebilirsiniz. Yeniden onaylama gerektiren değişiklik türlerini **Satınalma ilkeleri** sayfasındaki **Satınalma emirleri için yeniden onaylama kuralı** ilke kuralını kullanarak yapılandırabilirsiniz.  

Bir PO satırı için sipariş edilen miktarın bir parçası teslim edilmişse sipariş edilen miktarı değiştiremezsiniz. Ancak satırdaki **Teslimat bakiyesi** miktarını değiştirebilirsiniz. Daha sonra satırları iptal etmek ve sonraki işlemi önlemek için **Sonlandır** eylemini kullanın. 

Bir sipariş teyit edildikten sonra artık onu silemezsiniz. Ancak, miktarın alınmaması veya faturalanmaması koşuluyla siparişteki toplam miktarı veya kalan miktarı iptal edebilirsiniz.

<a name="see-also"></a>Ayrıca bkz.
--------

[Satınalma siparişine genel bakış](purchase-order-overview.md)

[Satınalma siparişi oluşturma](purchase-order-creation.md)

[Ürün girişine karşılık satınalma siparişleri](product-receipt-against-purchase-orders.md)

[Satıcı faturalarına genel bakış](../../financials/accounts-payable/vendor-invoices-overview.md)




