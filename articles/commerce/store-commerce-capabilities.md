---
title: Store Commerce uygulaması özellikleri
description: Bu makalede, Microsoft Dynamics 365 Commerce için Store Commerce uygulamasında bulunan işlevler anlatılmaktadır.
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: 58f2ab1f913d3629de7971c8eeb2d1821161e44f
ms.sourcegitcommit: 29d9a7573bdac004726da88a9d7b2cc9c383e9ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788526"
---
# <a name="store-commerce-app-capabilities"></a>Store Commerce uygulaması özellikleri

[!include [banner](includes/banner.md)]

Store Commerce uygulaması, Microsoft Dynamics 365 Commerce için modern satış noktası (POS) deneyimidir. İşletmelerin hareketleri işleme ve stok ve sipariş yönetimi gibi arka ofis işlemlerini yönetme olanağı sağlar. Uygulama, işletmelerin bağlılık programı ve müşteri rehberliği ile müşteri ilişkilerini yönetmesini de sağlar. 

Commerce Scale Unit (CSU) ile güçlendirilmiştir, Store Commerce uygulaması tam bir çok yönlü kanallı çözüm sağlar. Örneğin, bir müşteri çevrimiçi olarak bir ürün satın alabilir ve bunu yakındaki bir mağazadan teslim alabilir, böylece herhangi bir veri kaybı olmaksızın alışveriş için sürekli yolculuk sağlanır. 

Bu makale, Store Commerce uygulama özelliklerinin genel bakışını sunar.

## <a name="platform"></a>Platform

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Çok kanallı | Dynamics 365 Commerce, arka ofis, mağaza içi, çağrı merkezi ve dijital deneyimleri birleştiren kapsamlı bir çok kanallı çözüm sunar. | [Genel bakış](index.md) | [Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| Gözetimsiz Commerce | Commerce Scale Unit, gözetimsiz Commerce altyapısını barındırır. Gözetimsiz Commerce altyapısı, tüm ticaret iş mantığı için merkezi bir nokta olarak hizmet verir ve eksiksiz bir çok kanallı çözümünü destekler. | <p>[Mimari genel bakış](commerce-architecture.md)</p><p>[Gözetimsiz mimari](dev-itpro/retail-server-architecture.md)</p> | [Teknik sohbet](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce headquarters | Commerce headquarters, işletme için gerekli ürünlerin, çalışanların, iş süreçlerinin, fiyatlandırma ve diğer işlevlerin yapılandırılmasını sağlayan, arka ofis yeteneklerini sağlar. | [Mimari genel bakış](commerce-architecture.md) | |
| Satış noktası (POS) | Store Commerce uygulaması, Dynamics 365 Commerce için POS deneyimidir. Satış temsilcileri, kasiyerlerin ve yöneticilerin üstün müşteri hizmetleri sağlamasına yardımcı olan özellik zengin ve kapsamlı POS yetenekleri sunar. Ek olarak, perakendecilere birçok dağıtım seçeneği sağlar, performansın artırılmasına yardımcı olur ve gelişmiş uygulama yaşam döngüsü yönetimi (ALM) sunar. | [Store Commerce Uygulaması](dev-itpro/store-commerce.md) | <p>[Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[Görüntü](https://youtu.be/7B332XH_zfs)</p><p>[MPOS'u Store Commerce'e geçirme](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| Bulut dağıtımı | Yük dağıtımı ve coğrafi yakınlık için birden fazla Commerce Scale Unit örneği dağıtılabilir. | [Bulut dağıtımı](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| Şirket içi dağıtım | Commerce müşterilerinin bir yerel iş verileri dağıtımını kullanarak bir Dynamics 365 ortamının daha fazla sahipliği ve yönetimi olabilir. | [Şirket içi dağıtım](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>Aygıt yönetimi

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Birden çok form faktörü | Store Commerce uygulaması, bilgisayarlar, tabletler ve mobil aygıtlar gibi çoklu aygıt formu faktörlerinde desteklenir. Hızlı kullanıcı arabirimi (UI) düzenin otomatik olarak yeniden boyutlandırılıp ekran boyutuna ayarlamasına olanak tanır. | [Görsel konfigürasyonlar](pos-screen-layouts.md) |  |
| Platformlar arası | Store Commerce uygulaması Web, Windows, iOS ve Android platformlarında desteklenir. | [Platformlar](dev-itpro/hybridapp.md) | |
| Markalama | Ekran tasarımcısı, iş gereksinimlerinizi karşılayacak şekilde ekran düzenlerini özelleştirmenizi sağlar. Ek olarak, temalar, düzenler, renkler ve görüntüler çalışan rollerine göre oluşturulabilir ve böylece, marka tutarlılığı ve kullanım kolaylığı için kullanıcılar arasında paylaşılabilir. | [Görsel konfigürasyonlar](pos-screen-layouts.md) | [Görüntü](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| Topoloji | Farklı yerleşik topolojiler, ağ kullanılabilirliğine göre desteklenir. | <p>[Topoloji](dev-itpro/retail-modern-pos-architecture.md)</p><p>[Bilgi grafikleri](dev-itpro/retail-in-store-topology.md)</p> | |
| Çoklu aygıt yönetimi | Mağazalar arasında birden fazla aygıt, Commerce Headquarters'tan kolayca yönetilebilir. | [Etkinleştirme](set-up-activation-accounts-validate-devices-hq.md) | [Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>Personel yönetimi

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Oturum açma | Her mağaza çalışanının adanmış bir oturumu olabilir. Oturum açma türleri, kullanıcı adı, barkod, manyetik şerit okuyucu (MSR), biyometri ve Azure Active Directory (Azure AD) içerir. | <p>[Azure AD](aad-pos-logon.md)</p><p>[Genişletilmiş oturum açma](extended-logon.md)</p> | |
| İzinler | Çeşitli izin düzeyleri, örneğin, sipariş oluşturma izni ve siparişleri düzenleme izinleri gibi çalışanlar için desteklenir. | [İzinler](tasks/create-pos-permission-groups.md) | |
| Saat ve işe devam yönetimi | Katılım, zaman saati işlevi kullanılarak yönetilebilir. Katılım verileri, Dynamics 365 Human Resources uygulaması kullanılarak bordro içinde işlenebilir. | [Zaman yönetimi](retail-time-attendance.md) | |
| Satış komisyonu | Temsilcisine göre izlenen satışlar komisyonları veya diğer teşvikleri hesaplamak için de kullanılabilir. | [Komisyon](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>Ticaret

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Ürün çeşidi yönetimi | Ticari ürün yöneticileri ürünleri belirli bir kanalda ve belirli bir dönemde satışa açık olacak şekilde sıralayabilir. | [Sınıflamalar](assortments.md) | |
| Kataloglar | Ticari ürün yöneticileri, kataloğa özel fiyatlandırmayla sunmak istediğiniz ürünleri tanımlamak için katalogları yönetebilir. | [Kataloglar](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| Ürün ve kategori yönetimi | Commerce Headquarters'ta, ticari ürün yöneticileri çeşitleri, nitelikleri, ölçü birimi vb. sahip ürünler oluşturabilir. Ayrıca, ürünleri düzenlemek üzere bir kategori hiyerarşisi tanımlayabilirler. | [Ürün](retail-hierarchies.md) | |
| Paketler | Ticari ürün yöneticileri ürünleri bir paket veya kit olarak satılacak şekilde gruplandırabilir. | [Setler](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| Bilgi kodları | Bilgi kodlarını ürün satışları, ürün iadeleri veya müşterileri seçme gibi çeşitli POS işlemleri sırasında kasiyerden bilgileri girmesinin istenmesi için kullanın. | [Bilgi kodları](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| Bağlı maddeler | Bir madde harekete eklendiğinde, bağlantılı maddeleri yukarı satılmaya yönelik ürünler kullanın. | [Bağlı maddeler](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| Garantiler | Genişletilmiş garantiler ürünlerle birlikte satılabilir. | [Garanti](extended-warranty.md) | |
| Etiket yazdırma | Toplu iş numarası, seri numarası ve son kullanma tarihi gibi ürün bilgilerini içeren etiketler oluşturulabilir. | [Etiket yazdırma](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>Yardımlı satış

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Ürüne göz atma | Kategoriye göre ürünlere göz atın. | [Ürün hiyerarşisi](retail-hierarchies.md) | |
| Ürün arama | Marka, fiyat ve malzeme gibi ürün niteliklerini kullanarak ürünleri ada göre arayın ve aramaları daraltın. Bu yetenek Azure Bilişsel Arama tarafından desteklenir. | [Bulut destekli arama](cloud-powered-search-overview.md) | |
| Ürün ayrıntıları sayfası | Zengin ürün ayrıntıları sayfaları arasında resimler, bir açıklama, ürün özellikleri ve önerilen ürünler bulunabilir. Öneriler, Öneriler Servisi tarafından desteklenir. | | |
| Ürün karşılaştırma | Birden fazla ürünü karşılaştırın ve müşterilerin bir hareketi bir harekete eklemesini sağlamak için çoklu ürün karşılaştırması yapın. | | |
| Sonsuz koridor | Diğer mağazalarda kolayca stok arayabilir ve sipariş oluşturabilirsiniz. | [Stok arama](pos-inventory-lookup-operation.md) | <p>[Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Görüntü](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Öneriler | Öneriler servisini kullanarak, ürünlerde üst satış ve çapraz satış gerçekleştirin. Bu hizmet, öneriler, satınalma eğilimleri ve yeni ulaşan, benzer görünme ve en iyi satış gibi özelliklere dayalı olarak öneri önermek için patentli teknolojiyi kullanır. Bu öneriler ürün ayrıntıları sayfalarında, **Müşteri ayrıntıları** sayfasında ve **Hareketler** sayfasında bulunur. | [Öneriler](product-recommendations.md) | [Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>Müşteri ilişkisi

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Müşteri yönetimi | Müşteri hesapları oluşturun, düzenleyin ve yönetin. Gerçek zamanlı işlemeyi önlemek için müşteri hesapları zaman uyumsuz modda yönetilebilir. | [Yönetim](customer-mgmt-stores.md) | |
| Müşteri öznitelikleri | Müşteri öznitelikleri çerçevesi, müşteri ile ilgili ek verilerin iş gereksinimlerine göre yakalanmasına olanak tanır. | [Öznitelikler](dev-itpro/customer-attributes.md) | |
| Müşteri ayrıntıları sayfası | Zengin müşteri ayrıntıları sayfası, müşterinin tüm kanallardaki etkileşimleri için bir çok kanallı görünümünü sağlar. Bu etkileşimler satınalmalar, istek listeleri ve bağlılık programı puanları içerir. | | |
| Bulut destekli müşteri arama | Müşterileri ada, telefon numarasına, e-posta adresine, bağlılık programı kartına, adrese vb. arayın. | [Bulut destekli arama](pos-search-improvements.md#customer-search) | |
| Bağlılık programı ve ödüller | Müşteriler bağlılık programlarına katılabilir ve kanallarda bağlılık programı puanları kazanılabilir ve kullanmaya çalışabilir. | [Bağlılık](set-up-customer-loyalty-program.md) | [Görüntü](https://www.microsoft.com/en-us/videoplayer/embed/RE5c2wW) |
| Müşteri rehberliği | Bir istemci defteri kullanarak önemli müşterileri yönetin ve müşteri profilindeki etkinlikleri ve notları izleyin. Dynamics 365 Customer Insights tümleştirmesi, çalışanların her müşteri için bir sonraki en iyi eylem hakkında ipucu alması için ipuçlarını depolamasına izin verir. | [Müşteri rehberliği](clienteling-overview.md#activities-and-notes) | [Görüntü](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSP) |

## <a name="pricing-and-discounts"></a>Fiyatlandırma ve iskontolar

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Ticari sözleşmeler | Fiyatlandırma yöneticileri, belirli müşterilerle ilgili uzun süreli anlaşmalar temelinde özel fiyatlar tanımlamak için ticari sözleşmeleri kullanabilir. | [Fiyatlandırma](price-management.md)| [Görüntü](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| Satış sözleşmeleri | Fiyatlandırma yöneticileri, işletmeler arası (B2B) ticari senaryolardaki sözleşmeye dayalı fiyatları tanımlamak için satış anlaşmalarını kullanabilir. | [Fiyatlandırma](price-management.md) | |
| Fiyat ayarlamaları | Fiyatlandırma yöneticileri, fiyat ayarlama özelliğini kullanarak zaman içinde ürünleri için fiyat indirimleri oluşturabilir, izleyebilir ve yönetebilir. | [Fiyat ayarlamaları](price-adjustments-discounts.md) | |
| İskontolar | Fiyatlandırma yöneticileri, çeşitli promosyonlar için çeşitli türlerde indirimler ayarlayabilir. Bu iskontolar; basit iskontolar, miktar iskontoları, eşik iskontoları, karıştırma ve eşleştirme iskontoları, ödeme temelli iskontolar ve sevkiyat iskontolarını içerebilir. | [İskontolar](retail-discounts-overview.md) | |
| Kuponlar | Fiyatlandırma yöneticileri kupon kodları veya barkodlar ayarlayabilir, bunları iskontolara bağlayabilir ve müşterilere dağıtabilir. Satış temsilcileri, satış işlemlerine kuponlar ekleyebilir veya bunları kaldırabilir. | [Kuponlar](coupons.md) | |
| Fiyat grupları | Fiyatlandırma yöneticileri fiyat grubu yeteneğini, kanallar, kataloglar, üyelikler veya bağlılık programlarına dayalı olarak bağlamsal fiyatlar tanımlamak için kullanabilirler. | [Fiyatlandırma](price-management.md) | |
| Mevcut promosyonlar | Satış temsilcileri, mağazadaki ürünlerin kullanılabilir promosyonları, bir harekete eklenen ürünler vb. kolayca arama yapabilir. | [Fiyatlandırma işlevleri](pos-pricing-functions.md) | |
| Fiyat denetimleri | Satış temsilcileri depodaki ürünlerin etkin satış fiyatlarını hızlı bir şekilde denetleyebilir. | [Fiyatlandırma işlevleri](pos-pricing-functions.md) | |
| Fiyat geçersiz kılmaları | Gerekli izinlere sahip satış temsilcileri, sistem tarafından konfigüre edilmiş veya hesaplanan fiyatları geçersiz kılabilir. | [Fiyatlandırma işlevleri](pos-pricing-functions.md) | |
| El ile iskontolar | Gerekli izinlere sahip satış temsilcileri, satış hareketi veya satış satırlarına el ile iskonto uygulayabilir. | [Fiyatlandırma işlevleri](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>Elektronik ödemeler

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Alacak ve borç | Store Commerce uygulaması ana kredi ve ATM kartı ödemelerini, bir Adyen Ödeme Ağ Geçidi ve PayPal aracılığıyla yapılan sipariş ile destekler. Ödemeler SDK'sı, bağımsız yazılım satıcısı (ISV) tümleştirmeleriyle desteklenen harici ağ geçidi bağlantılarına olanak tanır. | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[PayPal](paypal.md)</p><p>[Ödemeler](payment-methods.md)</p> | <p>[Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| Dijital cüzdan desteği | Store Commerce uygulaması, normal kredi ve ATM kartları yaptığı gibi banka kimlik numarası (BIN) aralıklarını kullanmayan Dijital Cüzdan ile yapılan ödeme yöntemleri ile ödemeleri destekler. Ödeme yöntemleri, Adyen gibi Dijital Cüzdan ödemeleriyle eşleştirilebilir. | [Cüzdan](wallets.md) | |
| Hediye kartı desteği | Banka kimlik numarası Dynamics 365 hediye kartı, Saklı Değer Çözümleri (SVS) ve Givex hediye kartları. Hediye kartları satın alınabilir ve bir siparişte kullanılabilir. | [Hediye kartları](dev-itpro/gift-card.md) | [Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| Sahtekarlık koruması | Dynamics 365 Fraud Protection, sahte etkinlikleri önlemenize ve sahtekarlık için fark edilmemiş yerleri belirlemenize yardımcı olur. | [Fraud Protection](dev-itpro/dfp.md) | [Görüntü](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>Vergiler ve ödemeler

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Vergiler | Store Commerce uygulaması, farklı türlerdeki dolaylı vergileri destekler, örneğin satış vergisi, katma değer vergisi (KDV), ürün ve hizmet vergisi, birim tabanlı ücretler ve stopaj vergisi gibi. | [Vergiler](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| Masraflar | Ücretler, satır düzeyinde, başlık düzeyinde otomatik giderler olarak, kanal tarafından vs. olarak konfigüre edilebilir. | [Masraflar](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>Sipariş işleme ve sipariş karşılama

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Sipariş oluşturma | Bir sipariş, sevkiyat veya yakın bir mağazada malzeme çekme için oluşturulabilir. Malzeme çekme için zaman yuvaları sağlanabilir. | [Genel bakış](customer-orders-overview.md) | |
| Sipariş düzeltme | Sipariş değiştirilebilir, iade edilebilir, iptal edilebilir, vb. | <p>[İptal](customer-orders-overview.md#cancel-a-customer-order)</p><p>[İadeler](pos-returns.md)</p> | |
| Arama | Siparişe özel bilgiler kullanarak siparişleri arayın ve filtre uygulayın. | [Arama](enhancedorderrecall.md) | |
| Sipariş öznitelikleri | Sipariş özniteliği çerçevesi, sipariş ile ilgili ek bilgilerin iş gereksinimlerine göre yakalanmasına olanak tanır. | [Öznitelikler](dev-itpro/order-attributes.md) | |
| Doğrudan teslim | Maddeler bir satıcı tarafından müşteri adresine doğrudan teslim edilmek üzere işaretlenebilir. Doğrudan teslime aracısız sevkiyat da denir. | [Doğrudan teslim](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| Teklif | Mağaza çalışanları müşteriler için teklifler oluşturabilir ve özel bir fiyat, el ile iskonto ve teklif geçerlilik tarihi belirleyebilir. | [Teklif](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| Sipariş karşılama | Mağazalar sipariş çekebilir, paketleyebilir ve sevk edebilir. Sevk irsaliyesi, sevkiyat için hazır paketlere eklenebilir. | [Sipariş karşılama](order-fulfillment-overview.md) | <p>[Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021)</p> <p>[Görüntü](https://www.microsoft.com/videoplayer/embed/RE5bRXE)</p>|
| Dağıtılmış sipariş yönetimi | Store Commerce uygulaması, iş stratejilerinin işletme niteliği, müşteri türü, sipariş kaynağı ve bir siparişin teslimat yöntemi temel alınarak yapılandırılabileceği akıllı sipariş karşılama optimizasyonunu destekler. | [DOM](dom.md) | [Görüntü](https://www.microsoft.com/en-us/videoplayer/embed/RE5bRYl)|

## <a name="inventory-management"></a>Stok Yönetimi

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Merkezi alım | Kullanılabilir stoğun dağıtım merkezinden birden fazla mağazaya veya ambara dağılımını kolaylaştırın. | [Merkezi alım](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Çapraz sevk | Gelen satınalma siparişlerindeki stok dağılımını birden fazla mağazaya veya ambara dağıtma. | [Çapraz sevk](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Gelen stok | Bir satıcıdan satınalma siparişi aracılığıyla veya başka bir ambardan transfer emri aracılığıyla stok alın. Bir gelen satınalma siparişi veya transfer emri talebi oluşturun. | [Gelen](pos-inbound-inventory-operation.md) | <p>[Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Görüntü](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Giden stok | Stoku transfer emri aracılığıyla başka bir ambara sevk edin ve giden transfer emri talebi oluşturun. | [Giden](pos-outbound-inventory-operation.md) | <p>[Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Görüntü](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Stok arama | Mağazaların ve ambarlardaki ürünlerin eldeki stoklarını denetleyin ve gelecekteki tarihlerde bulunan taahhüde (ATP) stoğu denetleyin. | [Stok arama](pos-inventory-lookup-operation.md) | <p>[Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Görüntü](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Stok düzeltmesi | Satış, giriş veya yeniden sayım kullanmadan belirli iş gereksinimlerini karşılamak için stoku bir mağaza ambarına veya dışına ayarlayın. | [Stok düzeltmesi](work-with-store-inventory.md) | <p>[Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Görüntü](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Stok sayımları | Fiziksel envanteri sayma ve sistem defter saklama stokunu bununla eşleşecek şekilde ayarlama. | [Sayım](work-with-store-inventory.md) | <p>[Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Görüntü](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)<p> |
| Stok hareketi | Stoku mağaza yerleşimleri arasında taşıma. | [Hareket](work-with-store-inventory.md) | <p>[Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Görüntü](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |

## <a name="financials"></a>Finansal değerler

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Nakit yönetimi | Store Commerce uygulaması, depodaki nakit ve diğer belirtilen ödeme yönetimini destekler. Ek olarak, mağazada vardiya mutabakatı gelişmiş nakit yönetimi özellikleri için etkinleştirilebilir. | [Nakit](cash-mgmt.md) | |
| Finansal ekstreler ve mutabakat | Bir mağazanın nakit ve hareket hareketleri, Commerce headquarters'ta ekstre deftere nakil işlemleri aracılığıyla kaydedilir. | [Raporlar](retail-statements.md) | |
| Gelir ve gider hareketleri | Mağazada küçük nakit hareketlerini işleyin ve kaybedilen para, lobinizdeki kahve mağazasının geliri ve halı temizleme hizmetleri gibi geleneksel yöntemlerle gelmeyen gelirleri kaydedin. | [Raporlar](retail-statements.md) | |
| Fatura ödemeleri | Faturalara göre ödemeleri yakalayın. | [Fatura](payinvoice.md) | |

## <a name="employee-productivity"></a>Çalışan verimliliği

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Görev yönetimi | Görev listeleri ve görevler oluşturun ve bunları mağazalara ve çalışanlara atayın. Mağazalardaki görevlerin durumunu izleyin. Microsoft Teams ile sorunsuz tümleştirme sağlanmıştır. | <p>[Görev Yönetimi](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [Görüntü](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>Donanım ve çevre bileşenleri

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Çevre birimleri bağlama | Yazıcılar, nakit çekmeceleri, tarayıcılar ve ödeme aygıtlarını bir POS terminaline bağlayın. | [Çevre birimleri](retail-peripherals-overview.md) ||
| Çevre birimleri paylaşma | Makbuz yazıcıları, nakit çekmecesi ve ödeme aygıtları, birçok terminalde paylaşılan bir donanım istasyonuna bağlanarak paylaşılabilir. | <p>[Donanım istasyonu](retail-peripherals-overview.md) ||
| POS ve çevre birim simülatörü | Çevre birimi benzeticisi fiziksel POS çevre birimi cihazlarını gerektiren senaryoların test edilmesini özellikle destekler. Ayrıca, POS istemcisi dağıtımı gerektirmeden fiziksel çevre birimi cihazlarının uyumluluğunu test etmek için kullanılabilecek bir POS simülatörü içerir. | [Simülatör](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>Girişler

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Girişler yazdır | Satış girişleri, kredi kartı girişleri, hediye makbuzları ve faturalar gibi çeşitli tiplerde yapılan girişler varsayılan olarak veya kullanıma alma sırasında kasiyer onayı alındıktan sonra yazdırılabilir. Günlükten de yeniden yazdırılabilir. | [Yazdırma](receipt-templates-printing.md) | |
| E-posta girişleri | Teslim alma işlemi tamamlandıktan sonra giriş, POS'tan e-postayla gönderilebilir. | [E-posta](email-receipts.md) | |
| Tasarım girişleri | Mağaza girişleri, satıcıya ve hareket türüne uygun veri ve mizanpajları gösterecek şekilde özelleştirilebilir. Ayrıca, girişler perakende için gerekli özel verileri gösterecek şekilde genişletilebilir. | [Tasarım](receipt-templates-printing.md) | |

## <a name="offline-support"></a>Çevrimdışı destek

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Sorunsuz çevrimdışı | İnternet bağlantısı sınırlı olduğunda veya olmadığında bile hareketleri işlemenize olanak tanıyan sorunsuz çevrimdışı. Veri dışlama, çevrimdışı veritabanlarının veri boyutunu azaltmanıza ve performansı en üst düzeye çıkarmanıza yardımcı olur. | [Çevrimdışı](pos-operations.md) | |
| Performans tabanlı anahtarlama | Performans düşüşü algılandığında çevrimdışı duruma geç. | [Çevrimdışı](dev-itpro/implementation-considerations-offline.md) | [Görüntü](https://youtu.be/sQU-2pgHToI) |
| Çevrimdışı pano | **Çevrimdışı durum** panosu, her bir aygıt için verilerin çevrimdışı durumunu, hatalarını ve ayrıntılarını gösterir. Bu nedenle birçok aygıtın durumunu yönetmek kolaydır. | [Çevrimdışı](dev-itpro/implementation-considerations-offline.md) | [Görüntü](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>Genişletilebilirlik

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Commerce headquarters | Commerce headquarters çözümleri, iş süreçleri ekleyerek veya değiştirerek özelleştirilebilir. Commerce headquarters özel işlevler eklemek için meta verilerin kullanımını ve kod güdümlü genişletme modelini destekler. Harici çözümlerle kolayca tümleştirilebilir. | [Genel bakış](dev-itpro/extend-customer-cdx-package.md) | [Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| Gözetimsiz commerce | Genişletilebilir Çok yönlü kanal API çerçevesi iş mantığını özelleştirmek ve eklemek için kullanılabilir. İstek işleyicileri, ön tetikleyici ve tetikleyici sonrası uzantı desenleri olan API'ler. | [CSU](dev-itpro/retail-server-customer-consumer-api.md) | [Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Commerce SDK | Commerce SDK, Dynamics 365 Commerce işlevselliğini genişletmek veya özelleştirmek için gerekli olan kod, kod örnekleri, şablonlar ve araçlar içerir. SDK, uzantı bileşenlerine bağlı olarak, GitHub'da farklı depolarda (repos) yayımlanır. | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Satış noktası | Store Commerce uygulaması, Commerce SDK'nın POS genişletme özelliği kullanılarak bağımsız olarak genişletilebilir. Çerçeve, kullanıcı deneyiminin (UX), iş akışlarının ve iş mantığının özelleştirilmesini destekler. | [POS](dev-itpro/pos-extension/pos-extension-overview.md) | [Teknik sohbet](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>Raporlama

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Satış raporları | Personel, kasa, ödeme türü, iade, ürün ve benzerine göre satış raporlarına mağaza yöneticileri erişebilir. Yöneticiler bu raporları görüntüleyebilir ve komisyon tahsis etmek ve ürün eğilimlerini tanımlamak için bunları kullanabilir. | | |

## <a name="diagnostics"></a>Tanılamalar

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Operasyonel içgörüleri | Mağazaya özel servis sağlık güvenilirliği ve performans ölçümleri müşterinin Application Insights aboneliğinde kullanılabilir. Gelişmiş uyarı ve izleme özellikleri kullanılabilir. | | |
| Durum denetimi | Bir POS'a bağlı olan çevre birimlerinin kullanılabilirliği, sağlık denetimi işlemi çalıştırılarak doğrulanabilir. Böylece, bireysel çevrebirim sorunları düzeltilebilir ve doğrulanabilir. | [Durum denetimi](pos-healthcheck.md) | [Görüntü](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>Globalleştirme

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Çoklu piyasa desteği | Mali tümleştirme, GST, gelişmiş faturalama ve ön ödemeler gibi pazara özgü özellikler kullanıma hazır desteklenir. Bu özellikler; Avrupa, Amerika, Rusya, Asya, Suudi Arabistan ve birçok piyasayı kapsar. | [Globalleştirme](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>Uyumluluk

| Yetenek | Açıklama | Belgeler | Ek içerik |
|---|---|---|---|
| Microsoft standartları | Store Commerce uygulaması, güvenlik, gizlilik, erişilebilirlik, genel veri koruma düzenlemesi (GDPR), Avrupa Birliği (AB) veri sınırı vb. için Microsoft standartlarını karşılar. | | |

