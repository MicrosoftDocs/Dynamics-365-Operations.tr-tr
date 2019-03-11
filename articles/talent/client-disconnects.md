---
title: Talent istemcisi bağlantısı kesiliyor
description: Bu konu, müşteri ortamından bilinmediği sebeple bağlantısı kesilirse ne yapılacağını açıklar.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4f96b986059c179268f8a96ea7e7725831a93524
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "306551"
---
# <a name="talent-client-disconnects"></a>Talent istemcisi bağlantısı kesiliyor

[!include [banner](includes/banner.md)]

**Ortam ayrıntıları** 

Bu sorun her ortamda ortaya çıkabilir.
 
**Belirti** 

Müşteri ortamından bilinmediği sebeple bağlantısı kesilirse. Müşteri, aşağıdaki hata iletilerinden birini alır:

- Bağlantınızı kaybettik. Çalışmaya devam etmek için Kapat'ı tıklatın.
- Ağ bağlantınız kesilmiş olabilir, yeniden denemek için Yeniden Dene'ye tıklayın.

**Kırmızı bayrak**

Bu sorun genellikle kullanıcılar uygulama aşamasındayken, üretim ve test ortamları arasında bilgi kıyaslaması yaptıklarında ve oturumlar arası geçiş yaptıklarını unuttuklarında gerçekleşir. Kullanıcılar bu aşamadayken, büyük olasılıkla bu sorunla karşılaşacaklardır.

**Stok çıkışı** 

**Tarayıcı türleri:** Google Chrome, Internet Explorer ve Microsoft Edge

Microsoft Dynamics 365 for Talent platformu, kullanıcılar aynı anda, aynı kullanıcı ve aynı tarayıcı türünden iki farklı oturum açtıklarında kullanıcıların bağlantısını keser. (Örneğin, kullanıcı A, hem ortam 1 hem de ortam 2'yi Chrome içerisinde görüntülüyor.) Kullanıcının farklı tarayıcı pencereleri veya sekmeler açması fark oluşturmaz. Aynı kullanıcı kimlik bilgiler, hem ortam 1 hem de ortam 2 için aynı tarayıcı türünde aynı anda oturum açmakta kullanılırsa, Talent oturumlardan birinin bağlantısını keser.

**Çözüm**

Bir tarayıcı türü için yalnızca bir ortamın açık olduğundan emin olun. Kullanıcılar, aynı ortama birden fazla oturumu açabilirler (aynı tarayıcı içinde birden fazla sekmede).

İki ortam arasında aynı zamanda geçiş yapmak isteyen kullanıcılar, her bir ortamı farklı bir tarayıcı türünde açmalıdırlar. (Örneğin, kullanıcı A ortam 1'i Chrome'da ve ortam 2'yi Microsoft Edge'de görüntüleyebilir.)
