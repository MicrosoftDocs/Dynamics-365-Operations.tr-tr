---
title: Mağaza stok yönetimi
description: Bu konuda, stoku yönetmek için kullanabileceğiniz belge türleri açıklanmaktadır.
author: rubencdelgado
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c4891f9dcb031f4cb8dfb91f3fe1a301aad9838e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793885"
---
# <a name="commerce-inventory-management"></a>Commerce stok yönetimi

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce'te stokla çalıştığınızda ve bir Commerce Scale Unit'e (CSU) bağlı Commerce uygulamalarından herhangi birini kullandığınızda, CSU'daki sipariş işleme mantığının bazı stok boyutları ve bazı stok madde türleri için sınırlı destek sağladığını bilmek önemlidir. Commerce uygulamaları, Dynamics 365 Supply Chain Management'taki madde yapılandırma seçenekleri aracılığıyla kullanılabilen tüm madde yapılandırma özelliklerini desteklemez.

CSU'da çalışan Commerce uygulamaları aşağıdaki ürün boyutlarını ve madde yapılandırmalarını desteklemez:

- Ürün boyutu ve ürün reçetesi (BOM) maddelerini yapılandırma (BOM çerçevesinin bazı bileşenlerini kullanan perakende paket ürünleri hariç)
- Fiili ağırlık maddeleri
- Ürün boyutu denetimli maddelerin sürümü

CSU üzerinde çalışan Commerce uygulamaları aşağıdaki izleme boyutlarını desteklemez:
- Sahip boyutu

- Satış noktası (POS) uygulaması aşağıdaki boyutlar için sınırlı destek sunabilir. POS, ambar veya mağaza kurulumunun konfigürasyonunu temel alarak stok hareketlerindeki boyutların bir kısmını otomatik olarak girebilir. Ancak POS, bir satış hareketi Commerce Headquars'a el ile girilirse, boyutları desteklenme biçiminde tam olarak desteklemez. 

- **Ambar Yerleşimi**: Kullanıcılar, yeni POS işlemleri [Gelen işlem](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ve [Giden işlem](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)'i kullandıklarında gelen maddelerin alınacağı veya giden transfer emirli maddelerin sevk edileceği bir depo stok yerleşimini seçebilirler. Eski **Malzeme çekme ve teslim alma** işlemini kullanırlarsa giden transferlerin giriş ve sevkiyatları için sınırlı yerleşim yönetimi desteği alabilirler. Bu destek yalnızca madde ve mağaza ambarı için **Ambar yönetimi sürecini kullan** seçeneği etkinleştirilmişse kullanılabilir. Şu anda bir stok yerleşimi, **Stok sayımı** işlemi veya **Stok arama** işlemi ile kullanılamaz.

- **Plaka**: Plakalar yalnızca **Ambar yönetimi sürecini kullan** seçeneği madde ve mağaza ambarında etkinleştirilmişse uygulanır. POS'ta stok, **Gelen işlem** veya ambar yönetimi işlemi etkinleştirilmişse **Malzeme çekme ve teslim alma** işlemi kullanılarak bir mağaza ambarına alınırsa ve maddeyi teslim almak için seçilen yerleşim, plaka denetimi gerektiren bir yerleşim profiline bağlıysa POS uygulaması, bir plakayı teslim alma satırına sistematik olarak uygular. POS kullanıcıları bu plaka verilerini değiştiremez veya yönetemez. Plakaların tam yönetimi gerekiyorsa mağazanın bu maddelerin girişini yönetmek için [ambarlama uygulaması](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/install-configure-warehousing-app) veya arka ofis istemcisi kullanmasını öneririz.

- **Seri numarası**: POS uygulaması, POS'ta oluşturulan ve serileştirilmiş maddeler içeren siparişlerin bir satış hareketi satırına kaydedilmesi için sınırlı destek sağlar. Bu seri numarası, zaten stokta bulunan kayıtlı seri numaraları ile doğrulanamaz. Bir satış siparişi, çağrı merkezi kanalında oluşturulursa veya kurumsal kaynak planlama (ERP) aracılığıyla karşılanırsa ve çoklu seri numaraları ERP'de karşılama işlemi sırasında tek bir satış satırına kaydedilirse POS'ta sipariş için iade işlemi gerçekleştiğinde bu seri numaraları uygulanamaz veya doğrulanamaz. **Gelen işlem** işlemi kullanılarak stok girişi yapıldığında kullanıcılar [alınan seri numaralarını kaydedebilir veya onaylayabilir](https://docs.microsoft.com/dynamics365/commerce/pos-serialized-items).

- **Toplu İş Kimliği**: Toplu iş denetimli bir madde satılırsa, POS uygulaması ekstre deftere nakli sırasında sınırlı destek sağlar ancak POS kullanıcıları POS uygulamasını kullanırken satılan veya seçilen toplu iş kimliği tanımlayamaz.

- **Stok durumu**: Ambar yönetimi sürecini kullanan ve stok durumu gerektiren maddeler için bu durum alanı POS uygulaması aracılığıyla ayarlanamaz veya değiştirilemez. Mağaza ambar yapılandırmasında tanımlanan varsayılan stok durumu, maddeler stoka alındığında kullanılır.

> [!NOTE]
> Tüm kuruluşların, bu madde yapılandırmalarını üretim ortamlarına dağıtmadan önce geliştirme veya test ortamlarındaki Commerce uygulamaları üzerinden madde yapılandırmalarını test etmesi gerekir. POS'ta düzenli peşin satış işlemleri gerçekleştirmek ve tam olarak desteklendiklerini doğrulamak için POS, çağrı merkezi veya e-ticaret aracılığıyla müşteri siparişleri (varsa) oluşturmak için maddelerinizi kullanarak test edin. POS uygulamasının bunları destekleyebildiğinden emin olmak için yeni madde yapılandırmalarını dağıtmadan önce POS karşılama ve stok işlemlerini de (stok girişi ve sipariş karşılama işlemleri gibi) test etmelisiniz. Test işlemi, test ortamınızda tam bir ekstre/sipariş deftere nakil işlemi çalıştırmayı ve bu maddeler için siparişler oluşturulduğunda ve Commerce Headquarters'a deftere nakledildiğinde deftere nakil sorunu oluşmadığını doğrulamayı içermelidir.
>
> Maddeler Commerce uygulamaları tarafından desteklenmeyen bir şekilde yapılandırılırsa ve uygun test yapılmazsa, kolayca düzeltilemeyen veya hiç düzeltilemeyen veri hataları oluşabilir.

## <a name="purchase-orders"></a>Satın alma siparişleri

Satınalma siparişleri Commerce Headquarters'da oluşturulur. Mağaza ambarı satınalma siparişi başlığına veya satınalma siparişi satırlarına dahil edilmişse satırlar POS'ta, [Gelen işlem](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) işlemi kullanılarak mağazadan teslim alınabilir. 

## <a name="transfer-orders"></a>Transfer emirleri

Transfer emirleri, Commerce Headquarters'da veya POS'ta [Gelen işlem](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) veya [Giden işlem](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) işlemi aracılığıyla oluşturulabilir. Stokun başka bir ambar veya mağaza yerleşiminden mağazaya gönderilmesi için bir transfer emri isteği oluşturmak üzere **Gelen işlem** POS işlemini kullanın. Stokun, mağazadan başka bir ambar veya mağaza yerleşimine gönderilmesi için bir transfer emri isteği oluşturmak üzere **Giden işlem** POS işlemini kullanın. Mağaza için bir transfer emri oluşturulduktan sonra bu mağaza, POS'taki **Gelen işlem** işlemi aracılığıyla oluşturulan transfer emri için stok girişini yönetebilir. Mağaza, stoku başka bir yerleşime gönderiyorsa söz konusu mağazanın giden sevkiyat işlemini yönetmek için POS'taki **Giden işlem** işlemi kullanılır.

## <a name="stock-counts"></a>Stok sayımları

Stok sayımları zamanlanmış veya zamanlanmamış olabilir. Planlı stok sayımları, mağazanın ambarına bağlı bir Sayma günlüğü belgesi oluşturularak Commerce Headquarters aracılığıyla oluşturulur. Bu günlük, sayılması gereken maddeleri belirtir. Daha sonra mağaza, bu önceden tanımlanmış sayım günlüklerine erişebilir ve POS'taki **Stok sayımı** işlemini kullanarak bunlar üzerinde işlem yapabilir. Mağaza kullanıcıları POS'ta **Stok sayımı** işlemini kullandıklarında gerektiği gibi planlanmamış bir stok sayımı başlatırlar. Planlı stok sayımlarından farklı olarak planlanmamış stok sayımlarında önceden tanımlanmış bir madde listesi yoktur. POS'ta, her iki türün birinden bir stok sayımı tamamlandığında kabul edilir ve merkez ofise gönderilir. Merkez ofiste bu sayı onaylanmalı ve ayrı bir adım olarak Commerce Headquarters'da deftere nakledilmelidir.

## <a name="inventory-lookup"></a>Stok arama

Çok sayıda mağaza ve ambar için geçerli olan eldeki ürün miktarı, **Stok arama** sayfasından görüntülenebilir. Geçerli eldeki miktara ek olarak gelecekte karşılanabilir (ATP) miktarlar, her bir mağaza için tek tek görüntülenebilir. ATP miktarlarını görmek için mağaza seçin ve ardından **Mağaza kullanılabilirliğini göster**'i seçin. Kullanılabilir yapılandırma seçenekleri hakkında bilgi için bkz. [Perakende kanalları için stok kullanılabilirliğini hesaplama](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).


[!INCLUDE[footer-include](../includes/footer-banner.md)]