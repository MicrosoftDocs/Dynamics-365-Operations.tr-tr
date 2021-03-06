---
title: İzin ve devamsızlık yönetimi
description: Bu konu İzin ve devamsızlık yönetim modülü hakkında bir genel bakış sağlar.
author: andreabichsel
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3376a9aec5c0003e9cc7c076c4d221a697df61ce
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462855"
---
# <a name="leave-and-absence-management"></a>İzin ve devamsızlık yönetimi

**İzin ve devamsızlık yönetim** modülü devamsızlık yönetimini tanımlamak için esnek bir çerçeve sunar. İzin ve devamsızlık planları, personelin boş zamanın nasıl atanacağını belirlemek için oluşturulabilir. Çalışanlar bir plana kaydedildikten sonra, yöneticilerine onay için izin istekleri gönderebilirler. İzin izleme, hem birinci seviye yöneticilerin hem de İnsan Kaynakları (İK) yöneticilerinin kimin izinli olduğunu ve her bir personelin en kadar süresi kaldığını izleme olanağı sağlar.  

İzin ve devamsızlık yönetimi aşağıdaki özellikleri sağlar: 

- **İzin ve devamsızlık türlerini tanımlama.**

    İzin türleri, bir personelin bildirebileceği çeşitli türde devamsızlıkları tanımlayabilir. Bu türler kullanıcı tanımlı olduğu için kuruluşunuza göre ayarlanabilmektedir. Bazı tipik izin türleri ücretli izin (PTO), izin, kısa süreli iş görmezlik, jüri görevi (bu türdeki izin türü Amerika Birleşik Devletleri'ne özeldir) ve cenazeye katılma gibi türleri içerir. 

- **İşinize uygun düzenlenmiş İzin ve devamsızlık planlarını tanımlayın**

    İzin ve devamsızlık planları, tahakkukun belirli sıklıklarda gerçekleşmesi üzerine tanımlanabilir, örneğin yıllık, aylık ve ayda iki kez gibi. Planlar ayrıca tahakkukun belirli bir tarihte tek bir defa oluşacağı bir türde de tanımlanabilir. 

    İzin planları genellikle katmanlar içerir; bazı çalışan grupları, kuruluşta bulundukları süreye dayanarak ek kazançlar sağlar. Bu kullanıcı tanımlı katmanlar ek kazanç saatlerine otomatik kaydı etkinleştirir; tanımlanmış oldukları tarih kriterine dayalı olarak. İzin planları, çalışanların tahakkuk edildikleri kazanç saatlerinden fazlasını kullanmalarını önlemek için bir maksimum devretme miktarı veya minimum bakiye olarak da zorunlu kılınabilir. 

    Tipik izin planları, yeni çalışanlara 80 saatlik PTO, 60 aylık hizmetten sonra ise 120 saat PTO verecek şekilde dahildir. Ek planlar kayan tatiller veya yalnızca üst düzey yönetici kazanç saatleri gibi konuma dayalı kazançlar gibi faydalar sağlayabilir.

- **Çalışanları izin ve devamsızlık planlarına tek tek veya iş kriterine dayalı olarak toplu olarak atayın.**

    İşle ilişkili çeşitli filtreler bir grup çalışanı bir izin planına atamak için kullanılabilir. İK yöneticileri bir personeli, kaydedilmiş olduğu izin ve devamsızlık planını görmek için görüntüleyebilirler. Alternatif olarak İK yöneticileri tüm planları ve ilişkili personel kayıtlarını görebilirler.

- **İzin ve devamsızlık planlarını askıya al.**

    İzin ve devamsızlık planları, ek tahakkukları önlemek için askıya alınabilmektedir. Tahakkuklar, bir personelin çalışması sona ererse askıya alınabilir.  

- **Hak veya izinleri ayarlama.**

    Bir personel çalışana özel tarihi kullanarak personelin varsayılan plan teklifini değiştirerek daha yüksek bir plan katmanına kaydedilebilirler. Personeller plan kaydı sırasında izin ve devamsızlık bakiyelerine ek el ile ayarlama alabilirler veya İK, istediği zaman el ile ayarlama yapabilmektedir. 

- **İzin isteklerine ek iş akışı uygulama.**

     Bir iş akışı, kuruluşun gereksinimlerini karşılamak için izin isteklerine uygulanmak üzere özelleştirilebilir ve uygulanabilir.  

- **Personel izin bakiyelerini izleme.**

    Çalışanlar, yöneticileri ve İK izin ve devamsızlık bakiyelerini görüntüleyebilir. İK, etkileşimli raporları türe göre plan kaydını ve izin bakiyelerini izlemek üzere kullanabilir. 

- **İzne ayrılma istekleri gönderme.**

    Personeller kullanılabilir saatlerine karşılık izin istekleri gönderebilir. İstekler basit bir tek günlük istek veya çoklu izin ve devamsızlık türlerini içeren çoklu gün isteklerinden oluşabilir. Bir iş akışı etkinleştirilmemişse, istekler otomatik olarak onaylanır. Bir iş akışı etkinleştirilmişse, iş akışının yapılandırmasına bağlı olarak onay otomatik olabilir veya onay gerektirebilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]