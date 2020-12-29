---
title: Müşteri sipairşleri için Çoklu malzeme çekme teslimat şekillerini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce'ta bir mağazada malzeme çekme amacıyla müşteri siparişleri oluşturmanıza olanak sağlayan işlevleri açıklamaktadır.
author: hhainesms
manager: annbe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 768b20ecc8d15353258c9b3af69b897957d3de60
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595004"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Müşteri sipairşleri için Çoklu malzeme çekme teslimat şekillerini etkinleştirme

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Microsoft Dynamics 365 Commerce sürüm 10.0.16 ve sonraki sürümlerde kuruluşlar, alışverişçiler veya satış kişilerin bir mağazada çekilecek bir sipariş oluştururken aralarından seçim yapabildikleri çoklu teslimat modlarını tanımlayabilir. Böylece kuruluşlar alışverişçilere çoklu malzeme çekme seçeneği sağlayabilir. Örneğin, birçok perakende satış şimdi, siparişleri için mağaza içi malzeme çekme veya perde çekme seçimini alışverişçileri sunmaktadır. Commerce, bu farklı malzeme çekme teslim modlarının konfigürasyonunun yapılandırmasını destekler. Kullanıcılar daha sonra desteklenen herhangi bir ticaret kanalında (e-ticaret, çağrı merkezi veya mağaza) müşteri siparişleri oluştururken faydalanabilir.

## <a name="enable-and-configure-pickup-delivery-modes"></a>Malzeme çekme teslimat şekillerini etkinleştirme ve yapılandırma

Bu işlevi kullanmak için Commerce Headquarter 'da **özellik yönetimi** çalışma alanında **çoklu malzeme çekme teslim modları desteğini** açın . Özellik etkinleştirildikten sonra ek konfigürasyon gereklidir.

Commerce 10.0.15 ve önceki sürümlerde kuruluşlar, belirlenen malzeme çekme teslimat modu olarak yalnızca bir teslimat modu tanımlayabilir. Bu tanım **Commerce parametreler** sayfasında gerçekleştirilir. Sürüm 10.0.16 ve sonrasında, **Çoklu malzeme teslim modları desteğini** etkinleştirdiğinizde daha önce **ticaret parametreleri** sayfasında malzeme çekme teslim modu olarak tanımlanan teslimat modu, Malzeme çekme teslim modları için yeni konfigürasyona otomatik olarak kopyalanır.

![Ticaret parametreleri sayfasındaki malzeme çekme teslimat şekilleri](media/multiplepickupparameter.png)

**Çoklu malzeme çekme teslim modları desteğini** açtıktan sonra, **ticaret parametreleri** sayfasının **müşteri siparişleri** sekmesindeki **teslimat modları** hızlı sekmesinde teslimat kılavuzunun **malzeme çekme modunda** Çoklu malzeme çekme teslimat modları tanımlayabilirsiniz.

**Teslimat modu**, **teslim alanlarının elektronik modu** ve **Sevk emirleri için yalnızca taşıyıcı modu seçeneklerini göster** seçeneği bu hızlı sekmeye yeniden konumlandırıldı.

Ek malzeme çekme teslimat modlarını konfigüre etmeden önce teslimat modlarını tanımlamanız gerekir. Commerce Headquarters 'daki teslimat modları sayfasında, **malzeme çekme teslim modları** olarak kabul edilmesi gereken teslimat şekillerini ekleyin. Tüm konfigürasyonunun tamamlandığından emin olun. Örneğin, Teslimat modunun uygun kanallara ve maddelere bağlı olduğundan emin olun. Bitirdiğinizde, Teslimat modu, kanallar ve maddeler arasındaki ilişkileri oluşturmak için **işlem teslimat modları** işini çalıştırın. İşin çalışması bittiğinde, Commerce Headquarters 'da **dağıtım çizelgesi** sayfasını açın ve ilgili Commerce Channel veritabanlarının yeni teslimat modu konfigürasyonınızla güncelleştirilmesini sağlamak için **1120** dağıtım işini çalıştırın.

![Yol kenarı malzeme çekme için teslim konfigürasyonu moduna örnek](media/pickupmodes.png)

Ek malzeme çekme teslimat modlarını tanımladıktan sonra, bunları **Commerce parametreleri** sayfasındaki **teslimatın teslim modu** kılavuzuna ekleyin . Sonra ilgili Commerce kanal veritabanlarını konfigürasyon değişikliğiyle güncelleştirmek için uygun dağıtım işlerini çalıştırın.

> [!NOTE]
> **Çoklu malzeme çekme teslim modları desteğini** açtığınızda, teslimat kılavuzunun **malzeme çekme moduna** kopyalanan varolan malzeme çekme teslimat modundan ayrı olarak, oluşturduğunuz her ek malzeme çekme teslim modu konfigürasyonu için yeni teslimat modları konfigüre etmelisiniz. Teslimat kılavuzunun **Pickup (teslimat) şekillerini** eklediğinizde , Commerce etkin açık satış satırlarının bunları kullanıp kullanmadığını doğrular. Herhangi bir açık satış satırı bulunursa, bir hata iletisi alırsınız. Bunları kullanan tüm açık satış satırları kapatılıncaya kadar teslimat modları malzeme çekme teslim modları olarak kabul edilmez (Faturalandı veya iptal edildi).

> [!IMPORTANT]
> **Commerce parametreleri** sayfasında birden fazla malzeme çekme teslimat modu tanımladıktan sonra, **Çoklu malzeme çekme teslim modları için destek** özelliği zorunlu hale gelir ve artık kapatılamaz. Bu özelliği kapatmanız gerekiyorsa, Teslimat kılavuzunun **malzeme çekme modundan** biri dışında tüm malzeme çekme teslimat modunu kaldırın . Yalnızca tek bir malzeme çekme teslimat modu tanımlandığında, özellik zorunlu olarak kabul edilir ve kapatılabilir.

### <a name="e-commerce-site-configurations"></a>E-ticaret sitesi yapılandırmaları

**Çoklu malzeme çekme teslim modları desteği** etkinleştirildiğinde, e-ticaret sayfalarındaki aşağıdaki modüller konfigüre edilen yeni malzeme çekme teslim modlarını gösterir:

- Satın alma kutusu
- Mağaza seçici
- Alışveriş sepeti
- Çekme bilgileri
- Sipariş onayı
- Sipariş ayrıntıları

Malzeme çekme teslimat modlarını kullanılabilir hale getirmek için e-ticaret sayfalarında ek adım gerekmez.

## <a name="work-with-multiple-pickup-delivery-modes"></a>Çoklu malzeme çekme teslimat şekilleriyle çalışma

Bir kanal için birden fazla malzeme çekme teslimat modu olduğunda, alacak ürünleri satın alırken müşteriler tarafından geliştirilmiş bir deneyim sağlanır. 

- E-ticaret kanallarında, alışverişçiler kullanılabilir tüm geçerli malzeme çekme teslim modunu seçebilir. Örneğin, bir satıcı iki malzeme çekme teslimat modunu tanımlar (mağaza içi malzeme çekme ve perde çekme), her ikisi de **Teslimat kılavuzunun malzeme çekme modunda** konfigüre edilir ve her ikisi de sipariş karşılama kanalı ve bir alışverişçinin Şu anda satın aldığı ürün için geçerlidir. Bu durumda, alışverişçinin tercih edilen malzeme çekme teslimat modunu seçebilir. Ardından, seçilen malzeme çekme teslimat modu, sipariş Commerce Headquarters 'da oluşturulduğunda satış sipariş satırıyla bağlantılı teslimat şeklini alır.

    ![E-ticaret'te malzeme çekme seçeneği seçme](media/pickupecommerce.png)

- Mağaza kanallarında, malzeme çekme için bir müşteri siparişi satış noktası (POS) uygulaması aracılığıyla oluşturulduysa, varsa satış ilişkilendirmelerinin kullanılabilir malzeme çekme teslim modları arasında seçim yapılması istenir. Kanal ve madde için yalnızca bir adet geçerli malzeme çekme teslim modu varsa satış ilişkilendirmelerinin bunu seçmesi istenmez. Bunun yerine, kullanılabilir malzeme çekme teslim modu otomatik olarak sipariş satırlarına uygulanır.

    ![POS uygulamasında malzeme çekme seçeneği seçme](media/pickuppos.png)

- Arama Merkezi kanallarında, kullanıcılar malzeme çekme emirleri oluştururken çağrı merkezi kanalına bağlı tüm tanımlanmış malzeme çekme teslim modunu el ile seçebilir. Daha sonra sistem, seçili malzeme çekme teslim modunun, kendisine bağlanan madde sipariş edildiğinde kullanılabileceğini doğrular. Arama Merkezi kanallarında bir malzeme çekme teslimat modu seçildiğinde, satış siparişi satırlarının geçerli bir mağaza ambarına bağlanması gerekir. Bir mağaza ambar bir arama merkezi satış satırında tanımlanırsa, o satış satırında bir malzeme çekme teslimat modu ayarlanamaz.
- Satış çalışanları , malzeme çekme amacıyla siparişler veya sipariş satırlarının listesini almak için POS uygulamasındaki **sipariş geri çekme** veya **sipariş karşılama** işlemini kullanabilir. Bir satış ilişkilendirmekte, geçerli mağazada çekilecek tüm siparişleri göstermek için önceden tanımlanmış bir arama filtresi kullanılıyorsa, arama sonuçlarının herhangi bir malzeme çekme teslimat modunu kullanan tüm uygun siparişleri içermesini sağlamak için sorgular değiştirilir. POS kullanıcıları belirli bir malzeme çekme teslimat moduna sipariş listesini daraltmak için varolan filtreleri de kullanabilirler. Örneğin, yalnızca yol kenarı yan malzeme çekme için siparişleri görüntüleyebilir.

    ![Bir geri çekme siparişleri listesine uygulanan malzeme çekme teslimat modları için filtre](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Dağıtılmış sipariş yönetimi için dikkate alınacaklar

[Commerce'deki dağıtılmış sipariş yönetimi (DOM)](https://docs.microsoft.com/dynamics365/commerce/dom) özellikleri mağaza malzeme çekme için işaretlenen tüm satış satırlarını dikkate almaz. Konfigüre edilmiş malzeme çekme teslimat modlarıyla bağlantılı satış satırlarının DOM mantığını atlayıp yeni bir karşılama ambarına yeniden tahsis edilmemesini sağlamak için bu özellikler güncelleştirilmiştir.
