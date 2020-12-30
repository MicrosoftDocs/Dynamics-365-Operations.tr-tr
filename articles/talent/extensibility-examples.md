---
title: Power Apps ve Power Automate ile Talent'i genişletme
description: Bu konu, Microsoft Power Apps ve Microsoft Power Automate kullanan Microsoft Dynamics 365 Talent - Attract için bazı örnek genişletilebilirlik senaryolarını açıklar.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529646"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Power Apps ve Power Automate ile Talent'i genişletme

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu, Microsoft Power Apps ve Microsoft Power Automate kullanan Microsoft Dynamics 365 Talent: Attract için bazı örnek genişletilebilirlik senaryolarını açıklar. Her bir örnek ile ilişkilendirilmiş çözüm paketini Power Apps ortamınıza içe aktarabilirsiniz. Daha sonra paketleri kılavuz veya başlangıç noktası olarak kullanarak, kuruluşunuza uygun olan senaryoları gerçekleştirmek için kullanabilirsiniz.

> [!IMPORTANT]
> Bu makalede açıklanan şablonları ve uygulamayı "olduğu gibi" kullanmak istiyorsanız, uygulamanıza spesifik olan tüm senaryoları kapsadıklarından emin olmak için test ettiğinizden emin olun.


## <a name="prerequisites"></a>Önkoşullar

- Paketleri almak için kullanıcıların **Ortam Yapıcı** izni olması gerekir.
- Uygulamaları içe veya dışa aktarmak için kullanıcıların bir Power Apps Plan 2 lisansı veya Power Apps Plan 2 deneme lisansına sahip olmaları gerekir.

## <a name="power-automate--form-connect"></a>Power Automate – Form Bağlantısı

**Power Automate – Form Bağlantısı** şablonu, Microsoft Forms'tan veri okumak ve bunları bir Common Data Service varlığı içinde depolamak için kullanılabilir.

Bu şablon, diğer senaryolar için kullanılabilecek şekilde genişletilebilir. Burada bazı örnekler verilmiştir:

- Aday değerlendirmeleri yakalama.
- Kurs anketlerinden sonuçları yakala.
- İnsan kaynakları (İK) yöneticileri için bir görüşme soruları kütüphanesi derleyin.
- Bir adayın görüşme sürecini değerlendirmesini yakalayın

Microsoft Dynamics 365: Attract'ta, adayların bilgilerini girdiği aday portalındaki formları kullanabilirsiniz. Ayrıca formları bir iş şablonuna etkinlikler olarak da katıştırabilirsiniz.

Bir aday bir form gönderdiğinde, Microsoft Power Automate, form gönderimini yakalar, veriyi okur ve Common Data Service varlığı içinde depolar.

**Power Automate – Form Bağlantısı** şablonunu ve Özel Varlık Yapısını indirmek için Microsoft İndirme Merkezi'nde [Power Automate – Form Bağlantısı](https://go.microsoft.com/fwlink/?linkid=2081988)'na gidin.

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePoint Tümleştirmesi

**Power Automate – SharePoint Tümleştirmesi** şablonu, Microsoft SharePoint listesinden veri okumak, listeleri herhangi bir Common Data Service varlığı için alan değerleriyle karşılaştırmak ve karşılaştırmanın sonuçlarını bir bildirim e-postası olarak göndermek için kullanılabilir. 

Bir kuruluş, acil olarak ihtiyaç duydukları bir yetenek kümesine sahip olabilir. Bu yetenekler, SharePoint içinde bir SharePoint listesi olarak depolanabilir. Bir aday, bir gerekli yetenekler kümesinin listelendiği herhangi bir işe başvurduğunda, adayın yetenekleri ve SharePoint içinde depolanmış yetenekler arasında önemli bir eşleşme varsa bir e-posta bildirimi gönderilir. Bu, acil olarak ihtiyaç duyulan pozisyonların daha hızlı doldurulmasına yardımcı olur çünkü bildirimler işe alanların kuruluş içinden adaylara ulaşmalarına yardım eder.

Bu şablon, SharePoint tümleştirmesi içeren herhangi bir senaryoda kullanılmak üzere genişletilebilir.

**Power Automate – SharePoint Tümleştirmesi** şablonunu indirmek için Microsoft İndirme Merkezi'nde [Power Automate – SharePoint Tümleştirmesi](https://go.microsoft.com/fwlink/?linkid=2082109) bağlantısına gidin.

## <a name="referral-app"></a>Başvuru Uygulaması

Paylaşılan bir yetenek havuzuna aday eklemek için referans uygulamasını kullanabilirsiniz. Başvuran, adayı gönderirken **FirstName**, **LastName**, **Email** ve **Linkedln URL** girebilir. Aday kaynak meta verileri daha sonra başvuran bilgileri ile doldurulur.

Bu uygulamayı, referanslar göndermek için çalışan self servisi'ne (ESS) katıştırabilir veya bunu şirket portalında köprü olarak kullanıp tek başına çalışan bir uygulama olarak kullanabilirsiniz.

**Referans uygulamasını** karşıdan yüklemek için Microsoft İndirme Merkezi'nde [Dynamics 365 Talent genişletilebilirlik çözümü: Referans Uygulaması](https://www.microsoft.com/download/details.aspx?id=58497) bağlantısına gidin. Bu uygulamayı içe aktarabilir ve başka işlevler eklemek için özelleştirebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Kiracılar ve ortamlar arasında uygulamaları geçirmek](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
