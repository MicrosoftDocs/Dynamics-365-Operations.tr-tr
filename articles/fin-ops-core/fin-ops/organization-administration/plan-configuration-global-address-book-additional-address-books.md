---
title: Genel adres defteri ve diğer adres defterleri için planlama
description: Bu konuda, genel adres defteri ve diğer ek adres defterlerini kurup yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktalar ve almanız gereken kararlar açıklanmaktadır.
author: msftbrking
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7d83d6536d85100ef6a91e909be5a8e57e423371
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693942"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a>Genel adres defteri ve diğer adres defterleri için planlama

[!include [banner](../includes/banner.md)]

Bu konuda, genel adres defteri ve diğer ek adres defterlerini kurup yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktalar ve almanız gereken kararlar açıklanmaktadır. Kararlardan bazılarında, üretimin diğer alanları için verilen kararları (örneğin organizasyon hiyerarşisini) onaylamanız gerekir.

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
