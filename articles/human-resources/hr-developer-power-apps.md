---
title: Power Apps ve Power Automate ile Talent'i genişletme
description: Bu konu, Microsoft Power Apps ve Microsoft Power Automate kullanan Microsoft Dynamics 365 Human Resources için bazı örnek genişletilebilirlik senaryolarını açıklar.
author: negudava
manager: tfehr
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: edc2352fa53ac93c582b608b65fc624ff5dcd2a4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467085"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Power Apps ve Power Automate ile genişletme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu, Microsoft Power Apps ve Microsoft Power Automate kullanan Microsoft Dynamics 365 Human Resources için bazı örnek genişletilebilirlik senaryolarını açıklar. Her bir örnek ile ilişkilendirilmiş çözüm paketini Power Apps ortamınıza içe aktarabilirsiniz. Daha sonra paketleri kılavuz veya başlangıç noktası olarak kullanarak, kuruluşunuza uygun olan senaryoları gerçekleştirmek için kullanabilirsiniz.

> [!IMPORTANT]
> Bu konuda açıklanan şablonları ve uygulamayı "olduğu gibi" kullanmak istiyorsanız, uygulamanıza spesifik olan tüm senaryoları kapsadıklarından emin olmak için test ettiğinizden emin olun.

## <a name="prerequisites"></a>Önkoşullar

- Paketleri almak için kullanıcıların **Ortam Yapıcı** izni olması gerekir.
- Uygulamaları içe veya dışa aktarmak için kullanıcıların bir Power Apps Plan 2 lisansı veya Power Apps Plan 2 deneme lisansına sahip olmaları gerekir.

## <a name="integration-with-microsoft-365-power-automate"></a>Microsoft 365, Power Automate ile tümleştirme

**Microsoft 365 ile tümleştirme** uygulaması, Microsoft 365 üzerinden oturum açmış kullanıcılar için takım bilgisini ayıklamak için kullanılabilir. Çalışanların kimlik tiplerini çıkarmak için İnsan Kaynakları çalışanlara başvurur. Yöneticiler, çalışan kimlik tiplerinin sona erme tarihlerini denetleyebilir. Çalışan numarası tipi sona ertiğinde, bunlar da e-posta anımsatıcısı gönderebilirler. Power Automate, bu anımsatıcıyı göndermek için Power Apps ile birleşir. Anımsatıcı gönderildiğinde, onay Power Automate'tan Power Apps'e geri gönderilir. Tanımlama türleri, sürücünün lisansını, Passport 'unu ve kabul edilen diğer kod biçimlerini içerir.

Bu uygulamayı diğer senaryolar için genişletebilirsiniz. Örneğin, ekip tatil bilgisini, takvim etkinlikleri ve ekibe özel etkinlikleri göstermek için kullanılabilir.

**Microsoft 365, Power Automate ile Tümleştirme** uygulamasını indirmek için Microsoft İndirme Merkezi'nde [Microsoft 365 ile Tümleştirme bağlantısına](https://go.microsoft.com/fwlink/?linkid=2081787) gidin.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL Bağlan ve yürüt

**Power Automate – SQL Bağlan ve yürüt** şablonu, Microsoft SQL Server'a bağlanır ve SQL sorgularının çalıştırılmasını etkinleştirir.

Bu şablon SQL tablolarını okuyup güncelleştirse de, genişletebilir ve diğer senaryolar için kullanabilirsiniz. Örneğin, Dataverse içinde bir hazırlama tablosunu SQL Server'dan doldurmak ve hazırlama tablosunu SQL Server'dan kademeli şekilde eşitlemek üzere kullanılabilir.

Veri dönüşümü ve artımlı gönderimi etkinleştirmek için Gelişmiş sorgu akış ile tümleşiktir.

**Power Automate – SQL Bağlan ve yürüt** şablonunu indirmek için Microsoft İndirme Merkezi'nde [Power Automate – SQL Bağlan ve yürüt](https://go.microsoft.com/fwlink/?linkid=2081789) bağlantısına gidin.

## <a name="additional-resources"></a>Ek kaynaklar

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]