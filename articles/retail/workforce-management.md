---
title: "İş Gücü yönetimine genel bakış"
description: "Bu konu, İşgücü yönetimi (WFM) hizmetini, alışıldık satış noktası (POS) istemcileri, Modern POS ve Bulut POS istemcilerinin avantajını nasıl kullanabileceğinizi ve böylece mağaza yöneticilerinin iş güçlerini nasıl kolayca yönetebileceklerini açıklar."
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a>İş Gücü yönetimine genel bakış

[!include[banner](includes/banner.md)]
    
İşgücü yönetimi (WFM) hizmetini, alışıldık satış noktası (POS) istemcileri, Modern POS ve Bulut POS istemcilerinin avantajını kullanabilirsiniz ve böylece mağaza yöneticileri iş güçlerini kolayca yönetebilirler. WFM servisi uzantı çerçevesini ilgili paketleri POS içinde indirmek için kullanır. Bu paketler POS kapatıldığında ve yeniden açıldığında yüklenir. Bu nedenle, Microsoft WFM için yeni özellikler yayınladığında, POS uygulamasının kapatılması ve yeniden açılması gerekir.

Bu servisi kullanarak, mağaza yöneticileri mağazaları için haftalık çalışma planlamalarını kolayca oluşturabilirler. Mağaza çalışanları daha sonra hızlı bir şekilde kendi zamanlama planlar, iş arkadaşlarınınkini görebilir. Bu şekilde, kimin onlarla vardiya sırasında çalışacağının bilgisini edinebilirler. Mağaza çalışanları devamsızlık, vardiya değişimi ve vardiya teklifi için talepler de oluşturabilirler. Tüm bu istekler tanımlanan bir iş akışını tetikler.

Bir vardiya sırasında mağaza çalışanları POS istemcilerinde bulunan giriş ve çıkış saatinin avantajından yararlanabilir. Veri daha sonra merkeze (HQ) bordro işlemesi için gönderilir. Giriş ve çıkış saati özelliği POS'un mevcut bir özelliğidir. Kurulum ve desteklenen senaryolar hakkında daha fazla bilgi için bkz [Giriş ve çıkış saati](retail-time-attendance.md).

## <a name="supported-scenarios"></a>Desteklenen senaryolar
Bu bölüm, desteklenen senaryolar hakkında daha fazla bilgi sağlar.

- **Planları oluştur ve yayınla** – WFM hizmeti, HQ içinde yapılandırılmış POS izinlerini, bir çalışanın mağaza ayrıcalıklarına sahip olup olmadığını belirlemek için kullanır. Yalnızca mağaza yöneticileri Zaman çizelgesi yönetim operasyonunu kullanarak zaman çizelgelerini oluşturabilir ve yayınlayabilir. Bir çalışanın vardiyasını başka bir çalışana kopyalayıp yapıştırarak hızlıca bir zamanlama oluşturabilirler. Önceki bir haftanın zaman çizelgesini geçerli haftaya da içe aktararak bir zaman çizelgesi oluşturabilirler.

    Bir zaman çizelgesi yayımlanmamışsa, bir taslak durumundadır ve yayımlanmış bir zaman çizelgesinden farklı görünür. Mağaza yöneticileri bir zaman çizelgesini **Yayımla** düğmesi üzerine tıklayarak herhangi bir hafta için yayımlayabilirler. Zaman çizelgesi bir hafta için yayımlandıktan sonra, herhangi bir değişiklik otomatik yayımlanır. Değişiklik örnekleri arasında çalışma vardiyalarının eklenmesi veya silinmesi, devamsızlıklar veya vardiyaların ve devamsızlıkların düzenlenmesi vardır. Mağaza çalışanları, yalnızca çeşitli haftalar için yayımlanan planları görebilirler.
    
- **İstekleri oluştur ve onayla** – Mağaza çalışanları üç tipte talep oluşturabilir:

    - Devamsızlık isteği
    - Vardiya değiştirme isteği
    - Vardiya teklifi isteği

    Bu istekler Zaman çizelgesi talepleri operasyonu kullanılarak oluşturulabilir. Her bir istek tanılanmış bir iş akışını izler ve çalışanlar taleplerinin geçerli durumunu kolayca görebilirler.
    
    Devamsızlık talepleri, mağaza yöneticisine onay için otomatik olarak gönderilir. Birden fazla mağaza yöneticisi varsa, tüm yöneticiler bir talebi görüntüleyebilir ancak yalnızca bir yönetici onaylayabilir veya reddedebilir. Devamsızlık türleri perakende HQ içerisinde **Perakende** modülü içindeki **Devamsızlık ve ayrılma türleri** sayfası kullanılarak yapılandırılır. Mağaza yöneticisi bir talebi onayladıktan veya reddettikten sonra bu, Zaman çizelgesi talebi operasyonu için **Geçmiş** sekmesine taşınır.
    
    Bir vardiya değişimi veya vardiya teklifi talebi önce talebin gönderildiği çalışana gider. Mağaza yöneticisi talebi yalnızca bu çalışan onayladıktan sonra görebilir. Bu nedenle, çalışan vardiya değişimini veya vardiya teklifi talebini reddederse, yönetici bunu görüntüleyemez. Talebi oluşturan çalışan, yönetici bunu onaylamadan veya reddetmeden önce iptal edebilir.

- **Etkin mağaza çalışanlarını zamanlama çizelgesi görünümünde göster** – Bir çalışan bir mağazaya, örneğin onu bir mağazanın personel adres defteri kullanarak eklendiğinde, çalışan WFM servisi içinde zamanlama için kullanılabilir olur. **İşgücü yönetimi için çalışan verisini işleme** adlı yinelenen bir toplu iş HQ'da çalıştırılır. Bu iş, mağaza çalışanının Ortak Veri Hizmeti'ne (CDS) gönderilecek ilişkilendirmelerini hazırlar.

    Aynı işlem, bir çalışan bir mağazadan çıkarıldığında da kullanılır. Ancak, çıkarılan çalışan halen geçmiş, geçerli ve gelecek haftalarda, etkin bir vardiya veya devamsızlık söz konusu çalışana atanmışsa gösterilir. Bu nedenle, bu vardiya ve devamsızlıklar silinene kadar çıkarılan çalışan bu haftalar için gösterilmeye devam edecektir.

