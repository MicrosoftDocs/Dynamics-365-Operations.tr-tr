---
title: Mağaza stok yönetimi
description: Bu konuda, stoku yönetmek için kullanabileceğiniz belge türleri açıklanmaktadır.
author: rubencdelgado
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a3e6450c358d12dc62c2ffa20e7ff529be86bbe5
ms.sourcegitcommit: e789b881440f5e789f214eeb0ab088995b182c5d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2020
ms.locfileid: "3379271"
---
# <a name="store-inventory-management"></a>Mağaza stok yönetimi

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce uygulamasında stokla çalışırken ve satış noktası (POS) uygulamasını kullandığınızda POS'un bazı stok boyutları ve bazı stok maddesi türleri için sınırlı destek sağladığını bilmeniz önemlidir. POS uygulaması, Dynamics 365 Supply Chain Management uygulamasındaki madde yapılandırma seçenekleriyle kullanılabilen tüm madde yapılandırma özelliklerini desteklemez.

POS çözümü, şu anda aşağıdaki ürün boyutlarını ve madde yapılandırmalarını desteklememektedir:

- Ürün boyutu ve ürün reçetesi (BOM) maddelerini yapılandırma (BOM çerçevesinin bazı bileşenlerini kullanan perakende paket ürünleri hariç)
- Fiili ağırlık maddeleri
- Ürün boyutu denetimli maddelerin sürümü

POS uygulaması şu anda POS içindeki aşağıdaki izleme boyutlarını desteklemez:

- Toplu iş izleme boyutu
- Sahip boyutu

POS, aşağıdaki boyutlar için sınırlı destek sağlar. Başka bir deyişle POS, ambar veya mağaza kurulumunun yapılandırmasına bağlı olarak bu boyutlardan bazılarını stok işlemlerine otomatik olarak girebilir. POS, bir satış hareketi Commerce Headquarters'a el ile girilirse desteklendikleri gibi tam olarak boyutları desteklemez. 

- **Ambar Yerleşimi**: Kullanıcılar, yeni POS işlemleri [Gelen işlem](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ve [Giden işlem](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)'i kullandıklarında gelen maddelerin alınacağı veya giden transfer emirli maddelerin sevk edileceği bir depo stok yerleşimini seçebilirler. Eski **Malzeme çekme ve teslim alma** işlemini kullanırlarsa giden transferlerin giriş ve sevkiyatları için sınırlı yerleşim yönetimi desteği alabilirler. Bu destek yalnızca madde ve mağaza ambarı için **Ambar yönetimi sürecini kullan** seçeneği etkinleştirilmişse kullanılabilir. Şu anda bir stok yerleşimi, **Stok sayımı** işlemi veya **Stok arama** işlemi ile kullanılamaz.
- **Plaka**: Plakalar yalnızca **Ambar yönetimi sürecini kullan** seçeneği madde ve mağaza ambarında etkinleştirilmişse uygulanır. POS'ta stok, **Gelen işlem** veya ambar yönetimi işlemi etkinleştirilmişse **Malzeme çekme ve teslim alma** işlemi kullanılarak bir mağaza ambarına alınırsa ve maddeyi teslim almak için seçilen yerleşim, plaka denetimi gerektiren bir yerleşim profiline bağlıysa POS uygulaması, bir plakayı teslim alma satırına sistematik olarak uygular. POS kullanıcıları bu plaka verilerini değiştiremez veya yönetemez. Plakaların tam yönetimi gerekiyorsa mağazanın bu maddelerin girişini yönetmek için [ambarlama uygulaması](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/install-configure-warehousing-app) veya arka ofis istemcisi kullanmasını öneririz.
- **Seri numarası**: POS uygulaması, POS'ta oluşturulan ve serileştirilmiş maddeler içeren siparişlerin bir satış hareketi satırına kaydedilmesi için sınırlı destek sağlar. Bu seri numarası, zaten stokta bulunan kayıtlı seri numaraları ile doğrulanamaz. Bir satış siparişi, çağrı merkezi kanalında oluşturulursa veya kurumsal kaynak planlama (ERP) aracılığıyla karşılanırsa ve çoklu seri numaraları ERP'de karşılama işlemi sırasında tek bir satış satırına kaydedilirse POS'ta sipariş için iade işlemi gerçekleştiğinde bu seri numaraları uygulanamaz veya doğrulanamaz. **Gelen işlem** işlemi kullanılarak stok girişi yapıldığında kullanıcılar [alınan seri numaralarını kaydedebilir veya onaylayabilir](https://docs.microsoft.com/dynamics365/commerce/pos-serialized-items).
- **Stok durumu**: Ambar yönetimi sürecini kullanan ve stok durumu gerektiren maddeler için bu durum alanı POS uygulaması aracılığıyla ayarlanamaz veya değiştirilemez. Mağaza ambar yapılandırmasında tanımlanan varsayılan stok durumu, maddeler stoka alındığında kullanılır.

> [!NOTE]
> Tüm kuruluşların POS aracılığıyla madde yapılandırmalarını üretim ortamlarına dağıtmadan önce geliştirme veya test ortamlarında test etmeleri gerekir. Düzenli nakit satış hareketleri yapmak ve POS üzerinden müşteri siparişleri (varsa) oluşturmak için maddelerinizi, kullanarak test edin. POS uygulamasının bunları destekleyebildiğinden emin olmak için yeni madde yapılandırmalarını dağıtmadan önce POS karşılama ve stok işlemlerini de (stok girişi ve sipariş karşılama işlemleri gibi) test etmelisiniz. Testin, tam bildirim deftere nakil işlemini test ortamınızda çalıştırmayı içermesi ve bu maddelerin siparişleri Commerce Headquarters'da oluşturulduğunda ve yayımlandığında sorun olmadığını doğrulaması gerekir.
>
> Maddeler, POS uygulamasının desteklemeyeceği şekilde yapılandırılırsa ve uygun test yapılmazsa sipariş oluşturma işlemi sırasında, kolayca düzeltilmeyen veya standart ürün desteği kapsamında olmayan veri hataları ortaya çıkabilir.

## <a name="purchase-orders"></a>Satın alma siparişleri

Satınalma siparişleri Commerce Headquarters'da oluşturulur. Mağaza ambarı satınalma siparişi başlığına veya satınalma siparişi satırlarına dahil edilmişse satırlar POS'ta, [Gelen işlem](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) işlemi kullanılarak mağazadan teslim alınabilir. 

## <a name="transfer-orders"></a>Transfer emirleri

Transfer emirleri, Commerce Headquarters'da veya POS'ta [Gelen işlem](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) veya [Giden işlem](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) işlemi aracılığıyla oluşturulabilir. Stokun başka bir ambar veya mağaza yerleşiminden mağazaya gönderilmesi için bir transfer emri isteği oluşturmak üzere **Gelen işlem** POS işlemini kullanın. Stokun, mağazadan başka bir ambar veya mağaza yerleşimine gönderilmesi için bir transfer emri isteği oluşturmak üzere **Giden işlem** POS işlemini kullanın. Mağaza için bir transfer emri oluşturulduktan sonra bu mağaza, POS'taki **Gelen işlem** işlemi aracılığıyla oluşturulan transfer emri için stok girişini yönetebilir. Mağaza, stoku başka bir yerleşime gönderiyorsa söz konusu mağazanın giden sevkiyat işlemini yönetmek için POS'taki **Giden işlem** işlemi kullanılır.

## <a name="stock-counts"></a>Stok sayımları

Stok sayımları zamanlanmış veya zamanlanmamış olabilir. Planlı stok sayımları, mağazanın ambarına bağlı bir Sayma günlüğü belgesi oluşturularak Commerce Headquarters aracılığıyla oluşturulur. Bu günlük, sayılması gereken maddeleri belirtir. Daha sonra mağaza, bu önceden tanımlanmış sayım günlüklerine erişebilir ve POS'taki **Stok sayımı** işlemini kullanarak bunlar üzerinde işlem yapabilir. Mağaza kullanıcıları POS'ta **Stok sayımı** işlemini kullandıklarında gerektiği gibi planlanmamış bir stok sayımı başlatırlar. Planlı stok sayımlarından farklı olarak planlanmamış stok sayımlarında önceden tanımlanmış bir madde listesi yoktur. POS'ta, her iki türün birinden bir stok sayımı tamamlandığında kabul edilir ve merkez ofise gönderilir. Merkez ofiste bu sayı onaylanmalı ve ayrı bir adım olarak Commerce Headquarters'da deftere nakledilmelidir.

## <a name="inventory-lookup"></a>Stok arama

Çok sayıda mağaza ve ambar için geçerli olan eldeki ürün miktarı, **Stok arama** sayfasından görüntülenebilir. Geçerli eldeki miktara ek olarak gelecekte karşılanabilir (ATP) miktarlar, her bir mağaza için tek tek görüntülenebilir. ATP miktarlarını görmek için mağaza seçin ve ardından **Mağaza kullanılabilirliğini göster**'i seçin. Kullanılabilir yapılandırma seçenekleri hakkında bilgi için bkz. [Perakende kanalları için stok kullanılabilirliğini hesaplama](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).
