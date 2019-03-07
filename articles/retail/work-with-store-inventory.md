---
title: Mağaza stok yönetimi
description: Bu konuda, stoku yönetmek için kullanabileceğiniz belge türleri açıklanmaktadır.
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
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
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "339246"
---
# <a name="store-inventory-management"></a>Mağaza stok yönetimi

[!include [banner](includes/banner.md)]

Bu konuda, stoku yönetmek için kullanabileceğiniz belge türleri açıklanmaktadır.

Kuruluşunuzun stoğunu yönetmek için aşağıdaki belge türlerini kullanabilirsiniz.

Dynamics 365 for Retail içine stok ile çalışırken ve POS uygulamasını kullanırken, POS'un stok boyutları ve çeşitli stok öğesi türleri için sınırlı destek sağladığını dikkate almak önemlidir.  

POS çözümü aşağıdaki öğe yapılandırmalarını desteklemez:
- Ürün reçetesi öğeleri (ürün reçetesi çerçevesinin bazı bileşenlerini kullanan paket ürünler hariç)
- Fiili ağırlık maddeleri
- Toplu iş kontrollü maddeler

POS uygulaması şu anda POS içindeki aşağıdaki izleme boyutlarını desteklemez:
- Toplu iş izleme boyutu
- Sahip boyutu

POS çözümü, aşağıdaki boyutlar için sınırlı destek sağlar. Sınırlı destek, POS'un bu boyutlardan bazılarını stok hareketlerine otomatik olarak ambar/mağaza kurulum yapılandırmasına varsayılana dönebileceğini belirtir. POS, bir satış hareketi ERP'ye el ile girilirse desteklendikleri gibi tam olarak boyutları desteklemez. 

- Yer
- Plaka (yalnızca **Ambar yönetimi sürecini kullan** madde ve mağaza ambarında etkinleştirilmişse uygulanır)
- Seri numarası
- Stok durumu

> [!NOTE]
> Tüm kuruluşların POS aracılığıyla madde yapılandırmalarını üretime dağıtmadan önce geliştirme veya test ortamlarında test etmeleri gerekir. Öğelerinizi (eğer uygunsa) sıradan nakit ve taşıma satış hareketleri gerçekleştirerek ve müşteri siparişleri oluşturarak POS üzerinde maddeleriniz ile test edin. Testin, test ortamınızda tam bildirim deftere nakil işlemini çalıştırmayı içermesi ve sorun olmadığını doğrulaması gerekir.
> Maddeleri POS uygulamasında desteklenmeyen bir şekilde, doğru biçimde test etmeden yapılandırmak, bildirim deftere nakil işleminizin, sorunları kolay bir düzeltme şekli olmadan üretimde başarısız olmasına neden olabilir. Uygulamadaki ortak veya müşteri özelleştirmeleri, isteğe bağlı olarak bu deftere nakil işlemlerinin başarıyla tamamlanmış kabul edilebilir. Özelleştirmeler gerekli değilse, kuruluşun ürünlerinizin ürün yapılandırmasının, standart POS uygulaması/sipariş oluşturma/bildirim deftere nakletme işlemi tarafından desteklenmiş bir şekilde yapıldığından emin olması gerekir.

## <a name="purchase-orders"></a>Satın alma siparişleri

Satınalma siparişleri merkez ofiste oluşturulur. Satınalma siparişi başlığına bir perakende ambarı dahil edilirse, sipariş, Microsoft Dynamics 365 for Retail'de Modern POS (MPOS) veya Cloud POS kullanılarak mağazadan teslim alınabilir. Mağazada teslim alınan miktarlar girildikten sonra ek değişiklikler için yerel olarak kaydedilebilir. Alternatif olarak, miktarlar ayrılıp merkez ofise gönderilebilir. Merkez ofiste, mağazada alınan miktarlar Dynamics 365 for Retail'da, satınalma siparişindeki **Şimdi Al** alanında görüntülenir.

## <a name="transfer-orders"></a>Transfer emirleri

Transfer emri belirli bir mağazanın maddelerin sevk edilebileceği bir konum olduğunu belirtebilir. Bu durumda, transfer emri MPOS'ta veya Cloud POS'ta bir malzeme çekme isteği olarak mağazada görünür. Talep edilen miktarlar çekildikten sonra taahhüt edilip merkez ofise gönderilir. Merkez ofiste, mağazada alınan miktarlar Dynamics 365 for Retail'da, aktarma siparişindeki **Şimdi sevk et** çekilmesi görüntülenir. Transfer emri belirli bir mağazanın maddelerin sevk edilebileceği bir konum olduğunu belirtebilir. Bu durumda, transfer emri MPOS'ta veya Cloud POS'ta teslim alma isteği olarak mağazada görünür. Mağazada teslim alınan miktarlar girildikten sonra ek değişiklikler için yerel olarak kaydedilebilir. Alternatif olarak, miktarlar ayrılıp merkez ofise gönderilebilir. Merkez ofiste, mağazada alınan miktarlar Dynamics 365 for Retail'da, aktarma siparişindeki **Şimdi Al** alanında görüntülenir.

## <a name="stock-counts"></a>Stok sayımları

Stok sayımları zamanlanmış veya zamanlanmamış olabilir. Planlı stok sayımları sayılması gereken maddeleri belirten merkez ofiste başlatılır. Merkez ofis mağazada alınabilecek bir sayım belgesi oluşturur ve fiili eldeki stok miktarları burada MPOS'a veya Cloud POS'a girilir. Mağazada planlanmamış stok sayımları başlatılır ve fiili eldeki stok miktarları MPOS'ta veya Cloud POS'te güncelleştirilir. Planlı stok sayımlarından farklı olarak, planlanmamış stok sayımlarında önceden tanımlanmış bir madde listesi yoktur. Her iki türün birinden bir stok sayımı tamamlandığında, özen ve merkez ofise gönderilir. Merkez ofiste sayım doğrulanır ve nakledilir.

## <a name="inventory-lookup"></a>Stok arama

Çok sayıda mağaza ve ambar için geçerli eldeki ürün miktarı, Stok arama sayfasından görüntülenebilir. Geçerli eldeki miktara ek olarak, gelecekte karşılanabilir (ATP) miktarlar, her bir mağaza için görüntülenebilir. Bunu yapmak için, ATP'sini görüntülemek istediğiniz mağazayı seçin ve **Mağaza kullanılabilirliğini göster** üzerine tıklayın.
