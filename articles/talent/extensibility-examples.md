---
title: PowerApps ve Microsoft Flow kullanarak Talent'ı genişletme - Örnek senaryolar
description: Bu konu, Microsoft PowerApps ve Microsoft Flow kullanan Microsoft Dynamics 365 Talent için bazı örnek genişletilebilirlik senaryolarını açıklar.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 7bc3a18327f2d32770176eddcb7200681f0fb0da
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008071"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a>PowerApps ve Microsoft Flow kullanarak Talent'ı genişletme - Örnek senaryolar

Bu konu, Microsoft PowerApps ve Microsoft Flow kullanan Microsoft Dynamics 365 Talent için bazı örnek genişletilebilirlik senaryolarını açıklar. Her bir örnek ile ilişkilendirilmiş çözüm paketini PowerApps ortamınıza içe aktarabilirsiniz. Daha sonra paketleri kılavuz veya başlangıç noktası olarak kullanarak, kuruluşunuza uygun olan senaryoları gerçekleştirmek için kullanabilirsiniz.

> [!IMPORTANT]
> Bu konuda açıklanan şablonları ve uygulamayı "olduğu gibi" kullanmak istiyorsanız, uygulamanıza spesifik olan tüm senaryoları kapsadıklarından emin olmak için test ettiğinizden emin olun.


## <a name="prerequisites"></a>Önkoşullar

- Paketleri almak için kullanıcıların **Ortam Yapıcı** izni olması gerekir.
- Uygulamaları içe veya dışa aktarmak için kullanıcıların bir PowerApps Plan 2 lisansı veya PowerApps Plan 2 deneme lisansına sahip olmaları gerekir.

## <a name="flow--form-connect"></a>Akış - Form Bağlantısı

**Akış - Form Bağlantısı** şablonu, Microsoft Formlarından veri okumak ve bunları bir Common Data Service varlığı içinde depolamak için kullanılabilir.

Bu şablon, diğer senaryolar için kullanılabilecek şekilde genişletilebilir. Burada bazı örnekler verilmiştir:

- Aday değerlendirmeleri yakalama.
- Kurs anketlerinden sonuçları yakala.
- İnsan kaynakları (İK) yöneticileri için bir görüşme soruları kütüphanesi derleyin.
- Bir adayın görüşme sürecini değerlendirmesini yakalayın

Microsoft Dynamics 365 içinde: Attract, formları Aday portalında görüntülenebilir ve adaylar ayrıntıları doldurabilir. Formlar ayrıca bir iş şablonunda etkinlikler olarak katıştırılabilir.

Bir aday bir form gönderdiğinde, Microsoft Flow, form gönderimini yakalar, veriyi okur ve Common Data Service varlığı içinde depolar.

**Akış - Form Bağlantısı** şablonunu ve Özel Varlık Yapısını indirmek için [Akış - Form Bağlantısı](https://go.microsoft.com/fwlink/?linkid=2081988)'na, Microsoft Download Center üzerinden gidin.

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a>PowerApps'e aktarılan parametreleri başlat ve ayıkla

**PowerApps'e aktarılan parametreleri başlat ve ayıkla** şablonu Attract'e özel olan PowerApps senaryosuna bir başlangıç noktası olarak kullanılabilir. Attract'e aktarılan tüm varsayılan parametreleri içerir, örnein **İş Başvurusu**, **Aday Kimlik Kodu** ve **JobID** gibi.

Bu şablon, aday değerlendirme formunu çağırmak için kullanılabilir, böylece işe alan yönetici adayın doldurduğu değerlendirmeyi görüntüleyebilir.

PowerApps kullanılarak oluşturulan uygulamalar Attract içindeki bir iş şablonuna katıştırılabilir.

**PowerApps'e aktarılan parametreleri başlat ve ayıkla** şablonu ve Özel Varlık Yapısını indirmek için [PowerApps'e aktarılan parametreleri başlat ve ayıkla](https://go.microsoft.com/fwlink/?linkid=2081991)'ya Microsoft Download  Center üzerinden gidin.

## <a name="integration-with-office-365"></a>Office 365'le Tümleştirme

**Office 365 ile tümleştirme** uygulaması, Microsoft Office 365 üzerinden oturum açmış kullanıcılar için takım bilgisini ayıklamak için kullanılabilir. Talent içindeki çalışanların işe başlama ve işten çıkma ayrıntılarını ve istisna kayıtlarına referans gösterir. İşe başlama ve işten çıkma ayrıntıları özel Common Data Service varlıklarında depolanır. Varsayım, bu ayrıntıların bir üçüncü parti sistemden tümleştirme aracılığıyla doldurulduğudur.

Bu uygulama, diğer senaryolar için kullanılabilecek şekilde genişletilebilir. Örneğin, ekip tatil bilgisini, takvim etkinlikleri ve ekibe özel etkinlikleri göstermek için kullanılabilir.

**Office 365 ile tümleştirme** uygulamasını ve Özel Varlık Yapısını indirmek için [Office 365 ile tümleştirme'ye](https://go.microsoft.com/fwlink/?linkid=2081787) Microsoft Download Center'a gidin.

## <a name="flow--email-notification"></a>Akış - E-posta Bildirimi

**Akış - E-posta Bildirimi** şablonu, e-posta bildirimi senaryoları için kullanılabilir. İşe alma sürecinin herhangi bir aşamasında işe alma ekibinin reddettiği adaylara bildirim e-postaları gönderilmesini tetiklemekte kullanılabilir.

Bu şablon, adaylık aşamasında işe alma süreci boyunca değişiklikleri takip etmek için ve işe alma ekibi ve adaya bildirimler göndermek için genişletilebilir.

Genel olarak, Common Data Service içinde depolanan varlıklar, akışlar Core HR, Attract veya Onboard içinde gerçekleşen etkinlikler için bildirimler göndermek üzere ayarlanabilir.

**Akış - E-posta Bildirimi** şablonunu indirmek için [Akış - E-posta bildirimi](https://go.microsoft.com/fwlink/?linkid=2082103)'ne Microsoft Download Center'dan gidin.

## <a name="flow--sql-connect-and-execute"></a>Akış - SQL Bağlan ve yürüt

**Akış - SQL Bağlan ve yürüt** şablonu, Microsoft SQL Server'e bağlanır ve SQL sorgularının yürütülmesini etkinleştirir.

Bu şablon, SQL tablolarını okumak ve güncelleştirmek üzere tasarlanmış olsa da, diğer senaryolar için kullanılmak üzere genişletilebilir. Örneğin, Common Data Service içinde bir hazırlama tablosunu SQL Server'dan doldurmak ve hazırlama tablosunu SQL Server'dan kademeli şekilde eşitlemek üzere kullanılabilir.

**Akış - SQL Bağlan ve yürüt** şablonunu indirmek için [Akış - SQL Bağlan ve yürüt](https://go.microsoft.com/fwlink/?linkid=2081789)'na, Microsoft Download Center üzerinden gidin.

## <a name="flow--sharepoint-integration"></a>Akış - SharePoint Tümleştirmesi

**Akış - SharePoint Tümleştirmesi** şablonu, Microsoft SharePoint listesinden veri okumak, listeleri herhangi bir Common Data Service varlığı için alan değerleriyle karşılaştırmak ve karşılaştırmanın sonuçlarını bir bildirim e-postası olarak gönderir. 

Bir kuruluş, acil olarak ihtiyaç duydukları bir yetenek kümesine sahip olabilir. Bu yetenekler, SharePoint içinde bir SharePoint listesi olarak depolanabilir. Bir aday, bir gerekli yetenekler kümesinin listelendiği herhangi bir işe başvurduğunda, adayın yetenekleri ve SharePoint içinde depolanmış yetenekler arasında önemli bir eşleşme varsa bir e-posta bildirimi gönderilir. Bu şekilde, acil olarak ihtiyaç duyulan pozisyonlar daha hızlı doldurulur çünkü bildirimler işe alanların adaylara kuruluş içinden ulaşmasına olanak sağlar.

Bu şablon, SharePoint tümleştirmesi içeren herhangi bir senaryoda kullanılmak üzere genişletilebilir.

**Akış - SharePoint Tümleştirmesi** şablonunu indirmek için [Akış - SharePoint Tümleştirmesi](https://go.microsoft.com/fwlink/?linkid=2082109)'ne Microsoft Download Center'dan gidin.

## <a name="referral-app"></a>Başvuru Uygulaması
Paylaşılan bir yetenek havuzuna aday eklemek için referans uygulamasını kullanabilirsiniz. Başvuran, adayı gönderirken **FirstName**, **LastName**, **Email** ve **Linkedln URL'sini** girebilir. Aday kaynak meta verileri daha sonra başvuran bilgileri ile doldurulur.

Bu uygulamayı, referanslar göndermek için çalışan self servisi'ne (ESS) katıştırabilir veya bunu şirket portalında köprü olarak kullanıp tek başına çalışan bir uygulama olarak kullanabilirsiniz.

**Referans uygulamasını** karşıdan yüklemek için [Dynamics 365 Talent genişletilebilirlik çözümü: Referans uygulaması](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) gidip Microsoft Yükleme Merkezi'nden indirin. Bu uygulamayı içe aktarabilir ve başka işlevler eklemek için özelleştirebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Kiracılar ve ortamlar arasında uygulamaları geçirmek](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
