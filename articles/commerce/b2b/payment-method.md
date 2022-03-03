---
title: B2B e-ticaret siteleri için müşteri hesabı ödeme yöntemini yapılandırma
description: Bu konuda, Microsoft Dynamics 365 Commerce'de müşteri hesabı ödeme yönteminin nasıl yapılandırılacağı açıklanmıştır. Ayrıca, alacak limitlerinin işletmeler arası (B2B) e-ticaret sitelerinde açık hesap ödeme yakalamasını nasıl etkilediğini de açıklar.
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0366f7b51ac138cc7305f98d5607c554440e6d34
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323367"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>B2B e-ticaret siteleri için müşteri hesabı ödeme yöntemini yapılandırma

[!include [banner](../../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'de müşteri hesabı ödeme yönteminin nasıl yapılandırılacağı açıklanmıştır. Ayrıca, alacak limitlerinin işletmeler arası (B2B) e-ticaret sitelerinde açık hesap ödeme yakalamasını nasıl etkilediğini de açıklar.

Perakendeciler, e-ticaret kanalında sattıkları ürünler ve hizmetler karşılığında çeşitli türlerde ödemeler kabul edebilirler. Perakendecinin kabul edeceği ödeme türlerinin her biri, sistem ayarlandığında Dynamics 365 Commerce'te yapılandırılmalıdır. Müşteri hesabı (veya "açık hesap") ödeme yöntemi, B2B e-ticaret sitelerinde desteklenmelidir. 

## <a name="prerequisites"></a>Önkoşullar

1. Müşteri hesabı ödeme yöntemini Commerce Headquarters'a ekleyin.
2. Müşteri hesabı ödeme yöntemini e-ticaret kanalıyla ilişkilendirin.
3. Commerce Headquarters'da **Perakende ve Ticaret \> Müşteriler \> Tüm müşteriler \> Ödeme varsayılanları** bölümünde müşteri için **Açık hesaba izin ver**' özelliğinin etkinleştirildiğinden emin olun.

    > [!NOTE]
    > Tüm müşterilerin açık hesap ödeme yöntemi etkinleştirilmiş olmasına izin verilmesi gerekiyorsa, B2B sitesiyle ilişkilendirilmiş kanalın varsayılan müşterisi için **Açık hesaba izin ver** özelliğini **Evet** olarak ayarlayabilirsiniz. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Commerce site oluşturucusunda müşteri hesabı ödeme yöntemini etkinleştirme 

Commerce site oluşturucuda müşteri hesabı ödeme yöntemini etkinleştirmek için aşağıdaki adımları izleyin.

1. **Site Ayarları \> Uzantılar**'a gidin.
1. **Müşteri hesabı ödemelerini etkinleştir** özelliğini **B2B müşterileri için etkin** olarak ayarlayın. 
1. **kaydet ve yayınla** yı seçin.

> [!NOTE]
> Yeni site ayarları yalnızca app.settings.json dosyası güncelleştirildikten sonra etkinleşir. Daha fazla bilgi için bkz. [SDK ve Modül kitaplığı güncelleştirmeleri](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>B2B e-ticaret siteleri için ödeme sayfasında müşteri hesabı ödeme yöntemini etkinleştirme

B2B e-ticaret sitesinin ödeme sayfasında müşteri hesabı ödeme yöntemini etkinleştirmek için şu adımları izleyin.

1. Commerce site oluşturucusunda, B2B e-ticaret sitesinin ödeme modüllerini içeren ödeme sayfasını veya parçasını bulun ve düzenleyin.
1. **Ödeme bölümü kapsayıcısı** alanında, **Modül Ekle**'yi seçin ve **Müşteri hesabı ödemesi** modülü ekleyin.
1. Üç noktayı (**...**) seçip gerektiği gibi **Yukarı Taşı** veya **Aşağı Taşı**'yı seçerek **Müşteri hesabı ödemesi** modülunu konumlandırın.
1. **Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Müşteri hesabı ödeme yönteminin etkinleştirildiğini ve yayınlandığını onaylayın

Müşteri hesabı ödeme yönteminin etkinleştirildiğini onaylamak için şu adımları izleyin.

1. E-ticaret sitesinde oturum açın.
1. Sepete ürün ekleyin.
1. Ödeme sayfasına gidin. Yeni **Müşteri Hesabı** ödeme yöntemini görürsünüz.

## <a name="work-with-credit-limits"></a>Alacak limitleriyle çalışma

B2B sitesinde müşteri hesabı ödemeleriyle ilgili özellikler etkinleştirildiğinde kuruluşlar, genellikle sipariş yakalama işlemi sırasında alacak limitleri ve alacak limiti bakiyeleri hakkındaki bilgileri göstermek ister. Bir müşterinin alacak limiti, Commerce Headquarters'daki müşteri kaydının **Alacak ve tahsilatlar** hızlı sekmesinin **Alacak limiti** özelliği tarafından tanımlanır. Ancak, B2B senaryolarında, bir müşterinin verdiği siparişin genellikle müşterinin ait olduğu kuruluşun hesabına faturalandırılması gerekir. Bu nedenle, müşteri kaydının **Fatura ve teslimat** hızlı sekmesindeki **Fatura hesabı** özelliğini kuruluşun müşteri hesabı kimliğine ayarlamanız gerekir. Böylece, müşteri B2B sitesine sipariş verdiğinde sipariş kuruluşa faturalanacaktır. B2B sitesi ayrıca, müşteri kaydında tanımlanan alacak limiti yerine kuruluşun alacak limitini kullanır.

B2B web sitesinde gösterilen alacak limiti hesaplaması ve bakiyesi Commerce Headquarters'da **Alacak limiti türü** özelliğinin ayarına bağlıdır. Bu özelliğin konumu, **Özellik Yönetimi** çalışma alanında **Alacak yönetimi** özelliğinin etkinleştirilmiş olup olmadığına bağlı olarak farklılık gösterir:

- **Alacak yönetimi** özelliği etkinleştirilmişse, özellik **Alacak limitleri** hızlı sekmesinde **Alacak ve tahsilarlar \> Ayar \> Alacak ve tahsilatlar paranmetreleri \> Alacak** bölümünde bulunur. 
- **Alacak yönetimi** özelliği devre dışı bırakılmışsa, özellik **Alacak hesapları \> Ayar \> Alacak hesapları parametreleri \> Alacak derecelendirmesi** konumunda **Alacak derecelendirmesi** altında bulunur.

**Alacak limiti türü** özelliğinin desteklediği değerler şunlardır. **Yok**, **Bakiye**, **Bakiye + sevk irsaliyesi veya ürün makbuzu** ve **Bakiye + Tümü**. Bu değerler hakkında daha fazla bilgi için bkz. [Alacak limiti türü değerleri](/dynamics365/supply-chain/sales-marketing/credit-limits-customers).

> [!NOTE]
> Açık satış siparişlerinin bakiye hesaplamasına katkıda bulunmaması için **Kredi limiti türü** özelliğini **Bakiye + sevk irsaliyesi veya ürün makbuzu** olarak ayarlamanız önerilir. Daha sonra, müşterileriniz gelecekte sipariş verdiğinde, bu siparişlerin geçerli bakiyelerini etkileyeceği konusunda endişelenmeye gerek yoktur.

Açık hesap siparişini etkileyen başka bir özellik müşteri kaydının **Alacak ve tahsilatlar** hızlı sekmesinde bulunan **Zorunlu alacak limiti** özelliğidir. Alacak limitinin hiçbir müşteri için kontrol edilmemesi gerektiği belirtmek için **Alacak limiti türü** özelliği **Yok** olarak ayarlanmış olsa bile bu özelliği belirli müşteriler için **Evet** olarak ayarlayıp sistemi bu müşterilerin alacak limitini kontrol etmeye zorlayabilirsiniz.

Şu anda, **Zorunlu alacak limiti** özelliğinin etkinleştirildiği B2B sitelerinde ek işlevler bulunur. Özellik bir müşteri kaydında etkinleştirilmişse, müşteri bir sipariş verdiğinde, B2B sitesi müşterinin kalan alacak bakiyesinden daha fazla ödeme yapmak için açık hesap ödeme yöntemini kullanmasını engeller. Örneğin, müşterinin kalan alacak bakiyesi $1.000 ancak siparişin $1.200 olması durumunda, müşteri açık hesap yöntemini kullanarak yalnızca $1.000 ödeme yapabilir. Bakiyeyi ödemek için başka bir ödeme yöntemi kullanması gerekir. Bir müşteri kaydında **Zorunlu kredi limiti** özelliği devre dışı bırakılmışsa, müşteri açık hesap ödeme yöntemini kullanarak herhangi bir tutar ödeyebilir. Ancak, müşteri sipariş verebilse bile, sistem alacak limitini aştıklarında bu siparişlerin karşılanmalarına izin vermez. Açık hesap ödemeleri için uygun olan tüm müşteriler için alacak limitini denetlemeniz gerekiyorsa **Kredi limiti türü**  özelliğini **Bakiye + sevk irasliyesi veya ürün makbuzu** ve **Zorunlu kredi limiti** özelliğini **Hayır** olarak ayarlamanız önerilir.

**Alacak ve tahsilatlar** modülünde yeni kredi yönetimi özellikleri bulunmaktadır. Bu özellikleri açmak için **Özellik yönetimi** çalışma alanında **Alacak yönetimi** özelliğini etkinleştirin. Yeni özelliklerden biri, satış siparişlerinin engelleme kurallarına dayalı olarak beklemeye alınmasına olanak tanır. Daha sonra alacak yöneticisi siparişleri serbest bırakabilir veya daha fazla incelenmeleri için reddedebilir. Ancak, satış siparişlerinde genellikle bir ön ödeme olduğundan ve **Alacak yönetimi** özelliği ön ödeme senaryolarını tamamaen desteklemediğinden satış siparişlerini beklemeye alma özelliği Commerce siparişlerine uygulanamaz. 

**Alacak yönetimi** özelliğinin etkinleştirilmiş olup olmamasına bakılmaksızın, sipariş karşılama sırasında bir müşteri bakiyesi alacak limitinin üstüne çıktığında satış siparişleri beklemeya alınma durumuna gitmez. Bunun yerine, Commerce **Alacak limitleri** hızlı sekmesindeki **Alacak limiti aşıldığında ileti** alanındaki değere bağlı olarak bir uyarı iletisi veya bir hata iletisi oluşturur.

Commerce satış siparişlerinin beklemeye alınmasını engelleyen **Alacak yönetimi dışında tut** özelliği satış siparişi başlığında bulunur (**Perakende ve ticaret \> Müşteriler \> Tüm satış siparişleri**). Bu özellik Commerce satış siparişleri için **Evet** (varsayılan değer) olarak ayarlanırsa, siparişler alacak yönetiminin beklemede iş akışı dışında bırakılır. Bu özellik **Alacak yönetimi dışında bırak** olarak adlandırılsa da, sipariş karşılama sırasında tanımlanan alacak limiti kullanılmaya devam edilir. Siparişler yalnızca beklemeye gitmez.

Engelleme kurallarını temel alan Commerce satış siparişlerini beklemeye alma özelliği gelecekteki Commerce sürümleri için planlanmaktadır. Desteklenene kadar, Commerce satış siparişlerinin yeni alacak yönetimi akışlarına gitmesini zorunlu kılmanız gerekiyorsa Visual Studio çözümünüzde aşağıdaki XML dosyalarını özelleştirebilirsiniz. Dosyalarda, mantığı **CredManExcludeSalesOrder** bayrağı **Hayır** olarak ayarlanacak şekilde değiştirin. Bu şekilde, **Alacak yönetimi dışında tut** özelliği Commerce satış siparişleri için varsayılan olarak **Hayır** olarak ayarlanır.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

**CredManExcludeSalesOrder** bayrağı **Hayır** olarak ayarlanırsa ve B2B müşterisi satış noktası (POS) uygulamasını kullanarak mağazalardan satın alım işlemi yapabiliyorsa peşin hareketlerini deftere nakletme başarısız olabilir. Örneğin, nakit ödeme türünde bir engelleme kuralı vardır ve B2B müşterisi nakit kullanarak mağazada bazı maddeler satın almıştır. Bu durumda, elde edilen satış siparişi beklemeye alınacağından başarılı şekilde faturalanamaz. Bu nedenle, deftere nakil işlemi başarısız olur. Bu nedenle, bu özelleştirmeyi uyguladıktan sonra uçtan uca test etmenizi öneririz.

## <a name="additional-resources"></a>Ek kaynaklar

[B2B e-ticaret sitesi ayarlama](set-up-b2b-site.md)

[Müşteri hiyerarşileri kullanarak B2B iş ortaklarını yönetme](partners-customer-hierarchies.md)

[B2B e-ticaret sitelerindeki iş ortağı kullanıcılarını yönetme](manage-b2b-users.md)

[B2B e-ticaret siteleri için ürün miktarı sınırlarını ayarlama](quantity-limits.md)

[SDK ve Modül kitaplığı güncelleştirmeleri](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
