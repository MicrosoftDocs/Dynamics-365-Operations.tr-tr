---
title: İstemcinin bağlantısı kesiliyor
description: Bu konuda, müşterinin ortamla bağlantısının kesilmesi durumunda neler yapılması gerektiği açıklanmaktadır.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f99731d4d0658ed6f06b9e6915237532601a0a1d
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413523"
---
# <a name="client-disconnects"></a>İstemcinin bağlantısı kesiliyor

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Ortam ayrıntıları** 

Bu sorun her ortamda ortaya çıkabilir.
 
**Belirti** 

Müşteri ortamından bilinmediği sebeple bağlantısı kesilirse. Müşteri, aşağıdaki hata iletilerinden birini alır:

- Bağlantınızı kaybettik. Çalışmaya devam etmek için Kapat'ı tıklatın.
- Ağ bağlantınız kesilmiş olabilir, yeniden denemek için Yeniden Dene'ye tıklayın.

**Kırmızı bayrak**

Bu sorun genellikle kullanıcılar uygulama aşamasındayken, üretim ve test ortamları arasında bilgi kıyaslaması yaptıklarında ve oturumlar arası geçiş yaptıklarını unuttuklarında gerçekleşir. Kullanıcılar bu aşamadayken, büyük olasılıkla bu sorunla karşılaşacaklardır.

**Çıkış** 

**Tarayıcı türleri:** Google Chrome, Internet Explorer ve Microsoft Edge

Microsoft Dynamics 365 Human Resources kullanıcılar aynı anda, aynı kullanıcı ve aynı tarayıcı türünden iki farklı oturum açtıklarında kullanıcıların bağlantısını keser. (Örneğin, kullanıcı A, hem ortam 1 hem de ortam 2'yi Chrome içerisinde görüntülüyor.) Kullanıcının farklı tarayıcı pencereleri veya sekmeler açması fark oluşturmaz. Aynı kullanıcı kimlik bilgiler, hem ortam 1 hem de ortam 2 için aynı tarayıcı türünde aynı anda oturum açmakta kullanılırsa, İnsan Kaynakları oturumlardan birinin bağlantısını keser.

**Çözüm**

Bir tarayıcı türü için yalnızca bir ortamın açık olduğundan emin olun. Kullanıcılar, aynı ortama birden fazla oturumu açabilirler (aynı tarayıcı içinde birden fazla sekmede).

İki ortam arasında aynı zamanda geçiş yapmak isteyen kullanıcılar, her bir ortamı farklı bir tarayıcı türünde açmalıdırlar. (Örneğin, kullanıcı A ortam 1'i Chrome'da ve ortam 2'yi Microsoft Edge'de görüntüleyebilir.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
