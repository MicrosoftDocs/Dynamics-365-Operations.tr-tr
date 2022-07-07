---
title: Müşteriler için kredi limitleri
description: Bu makalede, Dynamics 365 Supply Chain Management'ta kredi limitlerinin nasıl çalıştığına genel bir bakış sağlanmıştır.
author: Henrikan
ms.date: 09/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4a98b90491093f55ce6974b9b11ff326c0c2f5c
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015335"
---
# <a name="credit-limits-for-customers"></a>Müşteriler için kredi limitleri

[!include [banner](../includes/banner.md)]

Bir kredi limiti ayarlamak, müşterilerinize sunacağınız maksimum kredi tutarını belirlemenizi sağlar. Bir kredi limiti belirtilirse, bir kullanıcı bir belgeyi güncelleştirmeye teşebbüs ettiğinde otomatik denetlenir. Kredi limiti aşıldığında, kullanıcıya bir ileti görüntülenir. Bu makale, kredi limitlerinin nasıl çalıştığına genel bir bakış sağlar ve aşağıdaki soruları yanıtlar:

-   Kredi limitleri için hangi belgeleri ve işlemleri ı kontrol edebilirim?

-   Müşterinin kalan kredisinin nasıl hesaplanacağını nasıl yapılandırabilirim?

-   Müşterinin kalan kredisi hakkındaki bilgi nerede kullanılır?

-   Bir müşteriye kredi verilmesi için kimlik saptama kullanılıp kullanılmaması gerektiğini ve kimlik saptama gereken kredi limiti tutarını nerede belirtirim?

-   Kredi limiti aşıldığında bir uyarı veya hatanın görüntülenmesini nerede belirtirim?

-   Belirli bir müşterinin kredi limiti nasıl belirlerim?

-   Satış siparişlerinde kredi limitlerini el ile nasıl kontrol ederim?

**Kredi limitleri için hangi belgeleri ve işlemleri ı kontrol edebilirim?**

**Alacak hesapları parametreleri** formunu, kredi limitlerini kontrol etmek için hangi belgelerin gerektiğini belirtmek için kullanın. Bu formda değişiklikler yapmak için Sistem yöneticisi (-SYSADMIN-) güvenlik rolünün bir üyesi olmanız gerekir. Kredi limitlerini aşağıdaki belgeler ve işlemler için denetleyebilirsiniz:

-   Satış siparişleri için faturalar, faturalar deftere nakledilirken

-   Satış siparişleri için sevk irsaliyeleri, sevk irsaliyelerini güncelleştirirken

-   Satış siparişleri, **Satış siparişi** formuna satırlar eklediğinizde

-   Satış siparişleri, bir hizmet aracılığıyla oluşturulduklarında

-   Serbest metin faturaları, faturaları deftere naklettiğinizde

Aşağıdaki seçeneklerinden biri ayarlandığında kredi limitleri otomatik olarak denetlenir:

-   **Alacak hesapları parametreleri**, **Kredi limiti türü** alanı **Hiçbiri** dışındaki herhangi bir şeye ayarlandığında. Kredi limitleri tüm müşteriler için denetlenir.

-   **Alacak hesapları parametreleri** formunda **Kredi limiti türü** alanı **Hiçbiri** olarak ayarlandığında ancak **Zorunlu kredi limiti**, bir müşteri için **Müşteriler** formunda seçildiğinde. Kredi limitleri yalnızca belirli müşteriler için denetlenir.

Kredi limitlerini aşağıdaki belgelerde denetlemek için ek ayarları belirtmeniz gerekir.

|    Belge                                    |    Ek ayar                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    Serbest metin   faturası                         |    Kredi derecelendirme alanındaki Alacak hesapları parametreleri formunda, Serbest metin faturasında kredi limitini denetle'yi seçin.     |
|    Satış   siparişi (el ile girilmiş)            |    Alacak hesapları parametreleri formunda, Kredi derecelendirmesi alanında, satış   siparişlerinde Kredi limitlerini denetle'yi işaretleyin.           |
|    Satış   siparişi (elektronik olarak alınmış)     |    Alacak hesapları parametreleri formunda, AIF alanında, satış siparişleri için Kredi limitlerini denetle'yi işaretleyin.                     |

**Bir müşterinin kalan kredisinin nasıl hesaplanacağını nasıl yapılandırabilirim?**

Dynamics 365'i, bir müşterinin kalan kredisini aşağıdaki şekillerden birinde hesaplamak üzere yapılandırabilirsiniz:

-   Kredi limitini müşteri bakiyesiyle karşılaştır.

-   Kredi limitini müşteri bakiyesi ve sevk irsaliyesi tutarları ile karşılaştır.

-   Kredi limitini müşteri bakiyesi ve tüm açık hareket etkinliği ile karşılaştır. Bu, sevk irsaliyesi tutarlarını ve satış siparişi tutarlarını içerir.

**Alacak hesapları parametreleri** formunu, karşılaştırılacak bilgiyi belirtmek için kullanın. Bu formda değişiklikler yapmak için Sistem yöneticisi (-SYSADMIN-) güvenlik rolünün bir üyesi olmanız gerekir. **Kredi limiti türü** alanında, kredi limiti denetimlerinin gerçekleştirilip gerçekleştirilmeyeceğini seçin ve hangi hareketlerin kredi limiti denetlendiğinde dahil edileceğini seçin. Aşağıdaki seçenekler arasından seçim yapın:

-   **Hiçbiri** – Kredi limitlerini denetleme. Bu seçeneği belirli bir müşteri için **Zorunlu kredi limiti** onay kutusunu **Müşteriler** formunda seçerek geçersiz kılabilirsiniz. Bunu yaparsanız, kredi limiti müşteri bakiyesine karşı denetlenir.

-   **Bakiye** - Kredi limiti müşteri bakiyesine karşı denetlenir.

-   **Bakiye + sevk irsaliyesi veya ürün girişi** – Kredi limiti müşteri bakiyesi ve teslimatlara göre denetlenir.

-   **Bakiye + Tümü** - Kredi limiti müşteri bakiyesiyle, teslimatlarla ve açık siparişlerle karşılaştırılır.

**Müşterinin kalan kredisi hakkındaki bilgi nerede kullanılır?**

Bir müşterinin bakiyesi ve kalan kredi tutarı, yaşlandırma anlık görüntüsü oluşturduğunuzda hesaplanır ve depolanır ve **Tahsilatlar** formunda görüntülenir. **Tahsilatlar** formunda görüntülenen tutarlar, yeni bir yaşlandırma anlık görüntüsü oluşturulana kadar tüm hareket etkinliğini içermeyebilir. Daha fazla bilgi için bkz. [Alacak hesaplarında koleksiyonlar ve kredi](/dynamicsax-2012/appuser-itpro/collections-and-credit-in-accounts-receivable).

Seçilen belgelere bağlı olarak, bir müşterinin bakiyesi ve kalan kredi tutarı hakkında bilgiler, satış siparişleri, sevk irsaliyeleri ve müşteri faturaları güncelleştirildiğinde hesaplanır. Çalışmakta olduğunuz belgenin tutarı, kredi limitinin aşılmasına neden olursa, bir ileti görüntülenir.

**Bir müşteriye kredi verilmesi için kimlik saptama kullanılıp kullanılmaması gerektiğini ve kimlik saptama gereken kredi limitini nerede belirtirim?**

**Alacak hesapları parametreleri** formunu, kimlik saptama gerekip gerekmediğini ve kimlik saptama gerektiren kredi limiti tutarını belirtmek için kullanın.
Bu formda değişiklikler yapmak için Sistem yöneticisi (-SYSADMIN-) güvenlik rolünün bir üyesi olmanız gerekir.

|    Alan                                    |    Tanım                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Krediyle   birlikte kimliği gerekli kıl     |    Tüzel varlığınızın kredi verdiği müşteri   için girilmesi gereken kimlik tipini seçin. Bu alanda seçtiğiniz seçenek, Müşteriler formundaki hangi alanlarda Resmi kimlik saptama alanlarında ne zaman ve hangi bilginin gerekeceğini belirtir: Hayır – Resmi kimlik gerekmez, müşterinin kredi limitinden bağımsız olarak.     Evet – Bir müşterinin kredi limit sıfırdan büyük veya sıfıra eşitse resmi kurumlar tarafından verilen bir lisans numarası veya başka bir kimlik gereklidir.     Minimum limit – Müşterinin kredi limit bu formdaki Limit alanına girdiğiniz limitten yüksek veya eşitse resmi kurumlar tarafından verilen bir lisans numarası veya başka bir kimlik gereklidir.        |
|    Sınır                                    |    Müşteriler için resmi kurumlar tarafından verilen bir lisansın veya başka bir kimliğin gerekeceği kredi limitini girin.    Örneğin 2,000 veya daha yüksek kredi limitine sahip müşteriler için ehliyet numarası gibi bir kimlik numarası zorunlu kılmak için 2000 girin.    Bu alan yalnızca, Krediyle birlikte kimliği gerekli kıl alanında Minimum limit'i seçtiyseniz kullanılabilir.                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**Kredi limiti aşıldığında bir uyarı veya hatanın görüntülenmesini nerede belirtirim?**

**Alacak hesaplar parametreleri** formunu, kredi limiti aşılırsa bir hata mesajı veya uyarı görüntülenip görüntülenmeyeceğini belirtmek için kullanın. Bu uyarı veya hata, bir kullanıcı bilgi girdiğinde veya deftere naklettiğinde veya belgeler bir elektronik servis tarafından işlendiğinde görüntülenir. Bu formda değişiklikler yapmak için Sistem yöneticisi (-SYSADMIN-) güvenlik rolünün bir üyesi olmanız gerekir.

|    Alan                                                               |    Tanım                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Kredi limiti aşıldığında ileti (Kredi derecelendirme alanında)     |    Kredi limitleri aşıldığında iletilerin kullanıcılara nasıl görüntüleneceğini seçin. Aşağıdaki seçeneklerden birini seçin: Hata – Bir hata iletisi görüntülenir. Bu genellikle geçerli işlemi durdurur ve işlemin devam edebilmesi için sorunun çözümlenmesi gerekir.     Uyarı – Bir uyarı iletisi görüntülenir fakat işlem devam edebilir.                     |
|    Kredi limiti aşıldığında ileti (AIF alanında)               |    Kredi sınırlarının aşılması hakkında iletilerin bir kayda nasıl teslim edileceğini seçin. Aşağıdaki seçeneklerden birini seçin: Hata – Özel durumlar formunda bir hata iletisi görüntülenir ve hata çözülene kadar belge işlenmez.     Uyarı – Özel durumlar formunda bir uyarı iletisi görüntülenir fakat işlem devam edebilir.        |

**Belirli bir müşterinin kredi limiti tutarını nasıl belirtirim?**

**Müşteriler** formunu, belirli bir müşteri için kredi limiti tutarını belirtmek için kullanın. Bu formda değişiklik yapmak için Müşteri ana bakım görevine atanmış (CustCustomersMaintain) olan bir güvenlik rolünün bir üyesi olmalısınız

1.  **Alacak hesapları** \> **Müşteriler** \> **Tüm müşteriler**'e tıklayın. Müşteri hesabına çift tıklayın.

2.  **Müşteriler** formunda, Eylem Panosunda **Düzenle**'yi tıklatın.

3.  **Kredi limiti** alanında para birimi tutarını girin. Bu değer sıfırdan (0) büyük olmalıdır ve kredi limiti tutarı olarak kullanılacaktır.

4.  Gerekirse, bir lisans numarası veya diğer resmi kurum tarafından verilmiş kimliği **Resmi kimlik** alanına girin.

> [!NOTE]
> **Alacak hesapları parametreleri** formunda, kredi limiti türü genellikle seçilmiştir. Ancak, kredi limiti türü **Hiçbir** olarak ayarlanmışsa, müşterinin kredi limitini, müşterinin bakiyesiyle kıyaslamak için **Zorunlu kredi limiti** onay kutusunu **Müşteriler** formunda seçmelisiniz. Kredi limiti türleri hakkında daha fazla bilgi için bu makaledeki "Hangi belgeler ve işlemler için kredi limitini denetleyebilirim?" bölümüne bakın. 

**Satış siparişlerinde kredi limitlerini el ile nasıl kontrol ederim?**

Bazen bir müşterinin kredi limitini el ile kontrol etmeniz gerekebilir. Örneğin, bir satış siparişi girmeye başlamadan önce bir müşterinin kredi limiti el ile denetleyebilirsiniz. Kredi limitlerini el ile denetlemek için **Satış siparişleri** formunu kullanabilirsiniz. Bu formda değişiklik yapmak için Satış siparişi bakım görevine atanmış (SalesOrderMaintain) olan bir güvenlik rolünün bir üyesi olmalısınız

1.  **Satış ve pazarlama** \> **Satış siparişleri** \> **Tüm satış siparişleri**'ne tıklayın. Bir satış siparişine çift tıklayın.

2.  **Satış siparişi** formunda, Eylem Panosunda, **Yönet** sekmesinde, **Kredi limitini denetle**'ye tıklayın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]