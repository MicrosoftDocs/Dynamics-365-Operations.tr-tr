---
title: Genel adres defteri ve diğer adres defterleri için planlama
description: Bu makalede, planlama sürecinde değerlendirmeniz gereken noktalar ve almanız gereken kararlar açıklanmaktadır.
author: msftbrking
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288c96d8c877f5e3b3101080294b2f6cdeb39882
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863173"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a>Genel adres defteri ve diğer adres defterleri için planlama

[!include [banner](../includes/banner.md)]

Bu makalede, genel adres defteri ve diğer ek adres defterlerini kurup yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktalar ve almanız gereken kararlar açıklanmaktadır. Kararlardan bazılarında, üretimin diğer alanları için verilen kararları (örneğin organizasyon hiyerarşisini) onaylamanız gerekir.

## <a name="global-address-book"></a>Genel adres defteri

Genel Adres Defteri ile çalışmaya başlamadan önce onun için varsayılan değerleri belirlemeniz gerekir. Bu varsayılan değerler, daha sonra oluşturacağınız tüm ek adres defterleri için kullanılır.

**Kararlar**

- **Kişi** türü için tarafların kayıtları hangi sıralama ile görüntülenmesi gerekir. Örneğin bir sıralama, soyad, ikinci ad ve isimden oluşur.
- Taraf kayıtları adres defterinden, rol kayıtları silindiğinde silinmeli midir? Örneğin, bir müşteri kaydı silinirse, taraf kaydı da silinmelidir?
- Yeni bir kayıt oluşturulduğunda, genel adres defteri içinde yinelenen bir kayıt bulunursa, kullanıcılara bildirisin mi?
- Veri evrensel numaralandırma sistemi (DUNS) numarası bir taraf kaydının bilgilerine dahil edilsin mi?
- Eğer DUNS numarası taraf kaydına dahil edildiyse, numaranın benzersiz olması kontrol edilmeli midir?
- Genel Adres Defteri içinde bir taraf kayıt oluşturulduğunda, varsayılan taraf türü, kişi veya kuruluş olmasını istiyor musunuz?
- Hangi kullanıcı rolleri, özel adreslere ve parti kayıtlarının iletişim bilgilerine erişebilir?

## <a name="additional-address-books"></a>Ek adres defterleri

Genel Adres Defteri'ni oluşturduktan sonra her iş kolu veya kuruluşunuzdaki her şirket için bir ayrı bir adres defterini, gerektiği gibi oluşturabilirsiniz. Örneğin, Fabrikam birden fazla şirket ve birden çok iş kolları olan uluslararası bir kuruluştur. Fabrikam, her iş kolu için bir adres defteri oluşturmayı planlar. Pnömatik Araçlar iş gibi birden fazla yerde ortaya çıkan iş kolları için Fabrikam her konum için bir adres defteri oluşturma planı yapar. Chris, Fabrikam'ın BT yöneticisi, aşağıdaki gerekli olan adres defterleri listesini oluşturmuştur. Bu liste aynı zamanda da her adres defterinin içermesi gereken taraf kayıtlarını açıklar.

- **Kamu sektörü sözleşmeleri (PubSC)** – Fabrikam'ın elinde bulunan kamu sektörü sözleşmelere dahil tüm taraflar için taraf kayıtları.
- **Özel sektör sözleşmeleri (PriSC)** – Fabrikam'ın elinde bulunan özel sektör sözleşmelerine dahil tüm taraflar için taraf kayıtları.
- **Elektronik Araçlar (ET)** – Elektronik araçların veya başka şekilde Fabrikam için Fabrikam-Japonya şirketinden sağlanan veya satın alınanlarla etkileşime giren, alımına veya satımına dahil olan tüm taraflar için taraf kayıtları.
- **Pnömatik Araçlar (PTJPN)** – Pnömatik araçların veya başka şekilde Fabrikam için Fabrikam-Japonya şirketinden sağlanan veya satın alınanlarla etkileşime giren, alımına veya satımına dahil olan tüm taraflar için taraf kayıtları.
- **Pnömatik Araçlar (PTUSA)** – Pnömatik araçların veya başka şekilde Fabrikam için Fabrikam-ABD şirketinden sağlanan veya satın alınanlarla etkileşime giren, alımına veya satımına dahil olan tüm taraflar için taraf kayıtları.

**Karar:**

- Kaç tane ek adres defteri oluşturacaksınız?


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]