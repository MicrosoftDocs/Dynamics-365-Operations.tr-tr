---
title: Power Apps ve Power Automate ile Talent'i genişletme
description: Bu konu, Microsoft Power Apps ve Microsoft Power Automate kullanan Microsoft Dynamics 365 Human Resources için bazı örnek genişletilebilirlik senaryolarını açıklar.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: Dynamics 365 Human Resources;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8d4185b958ed35e9d2bc764db8ea77b3a2f53c37
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029877"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Power Apps ve Power Automate ile genişletme

Bu konu, Microsoft Power Apps ve Microsoft Power Automate kullanan Microsoft Dynamics 365 Human Resources için bazı örnek genişletilebilirlik senaryolarını açıklar. Her bir örnek ile ilişkilendirilmiş çözüm paketini Power Apps ortamınıza içe aktarabilirsiniz. Daha sonra paketleri kılavuz veya başlangıç noktası olarak kullanarak, kuruluşunuza uygun olan senaryoları gerçekleştirmek için kullanabilirsiniz.

> [!IMPORTANT]
> Bu konuda açıklanan şablonları ve uygulamayı "olduğu gibi" kullanmak istiyorsanız, uygulamanıza spesifik olan tüm senaryoları kapsadıklarından emin olmak için test ettiğinizden emin olun.

## <a name="prerequisites"></a>Önkoşullar

- Paketleri almak için kullanıcıların **Ortam Yapıcı** izni olması gerekir.
- Uygulamaları içe veya dışa aktarmak için kullanıcıların bir Power Apps Plan 2 lisansı veya Power Apps Plan 2 deneme lisansına sahip olmaları gerekir.

## <a name="integration-with-office-365-power-automate"></a>Office 365, Power Automate'le Tümleştirme

**Office 365 ile tümleştirme** uygulaması, Microsoft Office 365 üzerinden oturum açmış kullanıcılar için takım bilgisini ayıklamak için kullanılabilir. Çalışanların kimlik tiplerini çıkarmak için İnsan Kaynakları çalışanlara başvurur. Yöneticiler, çalışan kimlik tiplerinin sona erme tarihlerini denetleyebilir. Çalışan numarası tipi sona ertiğinde, bunlar da e-posta anımsatıcısı gönderebilirler. Power Automate, bu anımsatıcıyı göndermek için Power Apps ile birleşir. Anımsatıcı gönderildiğinde, onay Power Automate'tan Power Apps'e geri gönderilir. Tanımlama türleri, sürücünün lisansını, Passport 'unu ve kabul edilen diğer kod biçimlerini içerir.

Bu uygulamayı diğer senaryolar için genişletebilirsiniz. Örneğin, ekip tatil bilgisini, takvim etkinlikleri ve ekibe özel etkinlikleri göstermek için kullanılabilir.

**Office 365, Power Automate ile Tümleştirme** uygulamasını indirmek için Microsoft İndirme Merkezi'nde [Office 365 ile Tümleştirme](https://go.microsoft.com/fwlink/?linkid=2081787) bağlantısına gidin.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL Bağlan ve yürüt

**Power Automate – SQL Bağlan ve yürüt** şablonu, Microsoft SQL Server'a bağlanır ve SQL sorgularının çalıştırılmasını etkinleştirir.

Bu şablon SQL tablolarını okuyup güncelleştirse de, genişletebilir ve diğer senaryolar için kullanabilirsiniz. Örneğin, Common Data Service içinde bir hazırlama tablosunu SQL Server'dan doldurmak ve hazırlama tablosunu SQL Server'dan kademeli şekilde eşitlemek üzere kullanılabilir.

Veri dönüşümü ve artımlı gönderimi etkinleştirmek için Gelişmiş sorgu akış ile tümleşiktir.

**Power Automate – SQL Bağlan ve yürüt** şablonunu indirmek için Microsoft İndirme Merkezi'nde [Power Automate – SQL Bağlan ve yürüt](https://go.microsoft.com/fwlink/?linkid=2081789) bağlantısına gidin.

## <a name="additional-resources"></a>Ek kaynaklar

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Kiracılar ve ortamlar arasında uygulamaları geçirmek](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
