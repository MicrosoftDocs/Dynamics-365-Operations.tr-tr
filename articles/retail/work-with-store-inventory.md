---
title: Mağaza stok yönetimi
description: Bu konuda, stoku yönetmek için kullanabileceğiniz belge türleri açıklanmaktadır.
author: rubencdelgado
manager: AnnBe
ms.date: 04/23/2019
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
ms.openlocfilehash: 551a8408aa730bc1916f1c57b7cfd773966ce8bf
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606815"
---
# <a name="store-inventory-management"></a>Mağaza stok yönetimi

[!include [banner](includes/banner.md)]

Dynamics 365 for Retail içine stok ile çalışırken ve POS uygulamasını kullanırken, POS'un stok boyutları ve çeşitli stok öğesi türleri için sınırlı destek sağladığını dikkate almak önemlidir.

POS çözümü aşağıdaki öğe yapılandırmalarını desteklemez:

- Ürün reçetesi öğeleri (ürün reçetesi çerçevesinin bazı bileşenlerini kullanan paket ürünler hariç)
- Fiili ağırlık maddeleri
- Toplu iş kontrollü maddeler

POS uygulaması şu anda POS içindeki aşağıdaki izleme boyutlarını desteklemez:

- Toplu iş izleme boyutu
- Sahip boyutu

POS çözümü, aşağıdaki boyutlar için sınırlı destek sağlar. Sınırlı destek, POS'un bu boyutlardan bazılarını stok hareketlerine otomatik olarak ambar/mağaza kurulum yapılandırmasına varsayılana dönebileceğini belirtir. POS, bir satış hareketi ERP'ye el ile girilirse desteklendikleri gibi tam olarak boyutları desteklemez. 

- **Ambar Konumu** - Mağaza ambar yönetim işlemini kullanmak üzere yapılandırılmadığında kullanıcılar bir mağaza ambarına alınan maddeler için teslim alma ambar konumunu yönetme özelliğine sahip olmaz. Bu maddeler için mağaza ambarında tanımlanan varsayılan bir teslim alma yerleşimi kullanılacaktır. Ambar yönetimi işlemi mağaza için etkinleştirilmişse, kullanıcıdan tüm giriş için bir teslim alma konumu seçmesini isteyen sınırlı destek tetiklenir. Mağazadan satılan maddeler, mağaza ambar kurulumunda tanımlandığı şekilde, her zaman varsayılan perakende konumundan satılır. Ambar iadesi yönetimi yerleşimi, mağaza ambarındaki varsayılan iade konumu tanımı aracılığıyla veya iade konumu ilkesinde tanımlandığı şekilde iade neden koduna dayalı olarak denetlenebilir.
- **Plaka** - Plakalar yalnızca **Ambar yönetimi sürecini kullan** madde ve mağaza ambarında etkinleştirilmişse uygulanır. POS'ta, stok ambar yönetimi işleminin etkinleştirildiği bir mağaza ambarına teslim alınırsa ve maddeyi teslim almak için seçilen yerleşim plaka kontrolü gerektiren bir yerleşim profiline bağlıysa, POS uygulaması bir plakayı teslim alma satırına sistematik olarak uygular. POS'taki kullanıcıların bu palka verilerini değiştirme veya yönetme yetkisi yoktur. Plakaların tam yönetimi gerekiyorsa, mağazanın bu maddelerin girişini yönetmek için WMS mobil uygulamasını veya arka ofis ERP istemcisini kullanması önerilir.
- **Seri numarası** - POS uygulaması, serileştirilmiş maddelerle POS'ta oluşturulan siparişler için bir hareket satış satırına kaydedilecek tek seri numarası için sınırlı destek sağlar. Bu seri numarası zaten stokta bulunan kayıtlı seri numaraları ile doğrulanamaz. Bir satış siparişi çağrı merkezi kanalında oluşturulursa veya ERP aracılığıyla karşılanırsa ve çoklu seri numaraları ERP'de karşılama işlemi sırasında tek bir satış satırına kaydedilirse, bu seri numaralar bu siparişler için POS'ta bir iada işlenmesi durumunda uygulanmaz veya doğrulanmaz.
- **Stok durumu** - Ambar yönetimi sürecini kullanan ve stok durumu gerektiren maddeler için, bu durum alanı POS uygulaması aracılığıyla ayarlanamaz veya değiştirilemez. Mağaza ambar yapılandırmasında tanımlanan varsayılan stok durumu, maddeler stoğa alındığında kullanılır.

> [!NOTE]
> Tüm kuruluşların POS aracılığıyla madde yapılandırmalarını üretime dağıtmadan önce geliştirme veya test ortamlarında test etmeleri gerekir. Öğelerinizi (eğer uygunsa) sıradan nakit ve taşıma satış hareketleri gerçekleştirerek ve müşteri siparişleri oluşturarak POS üzerinde maddeleriniz ile test edin. Testin, test ortamınızda tam bildirim deftere nakil işlemini çalıştırmayı içermesi ve sorun olmadığını doğrulaması gerekir.
>
> Maddeleri POS uygulamasında desteklenmeyen bir şekilde, doğru biçimde test etmeden yapılandırmak, bildirim deftere nakil işleminizin, sorunları kolay bir düzeltme şekli olmadan üretimde başarısız olmasına neden olabilir. Uygulamadaki ortak veya müşteri özelleştirmeleri, isteğe bağlı olarak bu deftere nakil işlemlerinin başarıyla tamamlanmış kabul edilebilir. Özelleştirmeler gerekli değilse, kuruluşun ürünlerinizin ürün yapılandırmasının, standart POS uygulaması/sipariş oluşturma/bildirim deftere nakletme işlemi tarafından desteklenmiş bir şekilde yapıldığından emin olması gerekir.

## <a name="purchase-orders"></a>Satın alma siparişleri

Satınalma siparişleri merkez ofiste oluşturulur. Satınalma siparişi başlığına bir perakende ambarı dahil edilirse, sipariş Microsoft Dynamics 365 for Retail'de **Malzeme çekme/Teslim alma** işlemi aracılığıyla Modern POS (MPOS) veya Cloud POS kullanılarak mağazada teslim alınabilir. Mağazada teslim alınan miktarlar satınalma siparişi belgesi için POS'ta **Şimdi Teslim Al** alanına girildiğinde, bunlar yerel olarak kaydedilebilir veya kabul edilebilir. Bu verilerin yerel olarak kaydedilmesi, stoktaki stok üzerinde herhangi bir etkiye sahip değildir. Yalnızca kullanıcının girişi HQ'ya göndermeye hazır olmaması ve önceden girilen **Şimdi Teslim Al** verilerini geçici olarak saklamak için bir yola gereksinim duyması durumunda kaydetme işlemi yapılmalıdır. Böylece, şimdi teslim al verileri kullanıcının kanal veritabanına yerel olarak kaydedilir. Belge **Kaydet** seçeneği kullanılarak işlendikten sonra **Şimdi Teslim Al** verileri HQ'ya gönderilir ve satınalma siparişi girişi deftere nakledilir. 

## <a name="transfer-orders"></a>Transfer emirleri

Transfer emri, belirli bir mağazanın maddelerin sevk edileceği yer veya stoğun teslim alınma konumu olduğunu belirtebilir. POS kullanıcısı bir transfer emri için sevkiyat ambarı ise, POS 'tan **Şimdi Sevket** miktarlarını girebilir. Sevkiyat mağazası tarafından girilen veriler yerel olarak kaydedilebilir veya kabul edilebilir. Yerel olarak kaydedildiğinde, HQ içindeki transfer emri belgesinde herhangi bir güncelleştirme yapılmaz. Yalnızca kullanıcının sevkiyatı HQ'ya nakletmeye hazır olmaması ve önceden girilen **Şimdi Sevket** verilerini geçici olarak saklamak için bir yola gereksinim duyması durumunda kaydetme işlemi yapılmalıdır. Mağaza sevkiyatı onaylanmaya hazır olduktan sonra, **Kaydet** seçeneği seçilmelidir. Böylece, HQ'daki transfer emrinin sevkiyatı deftere nakledikir ve teslim alma ambarı artık teslim alabilir. 

POS kullanıcısı bir transfer emri için teslim alma ambarı ise, POS'tan **Şimdi Teslim Al** miktarlarını girebilir. Teslim alma mağazası tarafından girilen veriler yerel olarak kaydedilebilir veya kabul edilebilir. Yalnızca kullanıcının girişi HQ'ya göndermeye hazır olmaması ve önceden girilen **Şimdi Teslim Al** verilerini geçici olarak saklamak için bir yola gereksinim duyması durumunda kaydetme işlemi yapılmalıdır. Böylece, şimdi teslim al verileri kullanıcının kanal veritabanına yerel olarak kaydedilir. Belge **Kaydet** seçeneği kullanılarak işlendikten sonra **Şimdi Teslim Al** verileri HQ'ya gönderilir ve transfer emri girişi deftere nakledilir. Teslim alma mağazasının yalnızca sevk edilen miktarlara eşit veya bundan küçük olan teslim alma miktarlarını kaydedebildiğini unutmamanız gerekir. Bir transfer emrindeki daha önce sevk edilmemiş miktarları teslim alma girişimi hatalara neden olur ve giriş HQ'da onaylanmaz.

## <a name="stock-counts"></a>Stok sayımları

Stok sayımları zamanlanmış veya zamanlanmamış olabilir. Planlı stok sayımları sayılması gereken maddeleri belirten merkez ofiste başlatılır. Merkez ofis mağazada alınabilecek bir sayım belgesi oluşturur ve fiili eldeki stok miktarları burada MPOS'a veya Cloud POS'a girilir. Mağazada planlanmamış stok sayımları başlatılır ve fiili eldeki stok miktarları MPOS'ta veya Cloud POS'te güncelleştirilir. Planlı stok sayımlarından farklı olarak, planlanmamış stok sayımlarında önceden tanımlanmış bir madde listesi yoktur. Her iki türün birinden bir stok sayımı tamamlandığında, özen ve merkez ofise gönderilir. Merkez ofiste sayım doğrulanır ve ayrı bir adım olarak deftere nakledilir.

## <a name="inventory-lookup"></a>Stok arama

Çok sayıda mağaza ve ambar için geçerli eldeki ürün miktarı, **Stok arama** sayfasından görüntülenebilir. Geçerli eldeki miktara ek olarak, gelecekte karşılanabilir (ATP) miktarlar, her bir mağaza için görüntülenebilir. Bunu yapmak için, ATP'sini görüntülemek istediğiniz mağazayı seçin ve **Mağaza kullanılabilirliğini göster** üzerine tıklayın.
