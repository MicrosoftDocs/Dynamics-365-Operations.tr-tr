---
title: Lifecycle Services'te mikro hizmetler eklentisini yükleme
description: Bu makalede, Microsoft Dynamics Lifecycle Services'daki (LCS) Elektronik Faturalama eklentisinin nasıl yükleneceği açıklanmaktadır.
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 938b00192acc0ff5534239f2f280792471181fad
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710821"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Lifecycle Services'de mikro hizmetler için eklentiyi yükleme

[!include [banner](../includes/banner.md)]

Elektronik Faturalama hizmetindeki kimlik doğrulaması, Microsoft Dynamics Lifecycle Services (LCS) ortamınıza yönelik eklentiyi yükleyerek Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management ortamınızı hizmetler platformuna kaydetmenizi gerektirir.

Ortamı kaydetmek için şu adımları izleyin.

1. LCS hesabınızda oturum açın.
2. Proje panonuzda, bir LCS projesi seçin.
2. Projedeki **Ortamlar** panosunda dağıtılan ortamınızı seçin. Seçtiğiniz ortamın çalışıyor olması gerekir.
3. **Power Platform Tümleştirme** sekmesinde, **Ortam eklentileri** bölümünde, **Yeni eklenti yükle**'yi seçin.
4. **Elektronik Faturalama**'yı seçin.
5. **AAD uygulaması kodu** alanına **091c98b0-a1c9-4b02-b62c-7753395ccabe** sabit değerini girin. Bu değer her zaman sabittir. Yalnızca bir genel benzersiz tanımlayıcı (GUID) girdiğinizden emin olun. Boşluk, virgül, nokta veya tırnak işareti gibi başka semboller eklemeyin.
6. **AAD kiracı kimliği** alanında, Azure abonelik hesabınızın kiracı kimliğini girin. Belirttiğiniz Azure Active Directory (Azure AD) kiracısı, Regulatory Configuration Service (RCS) için kullanılan kiracıyla aynı olmalıdır.
7. Hüküm ve koşulları inceleyin ve ardından onay kutusunu seçin.
8. **Yükle**'yi seçin. Birkaç dakika sonra, durum **Yükleniyor** yerine **Yüklü** olarak değişmelidir. Bu değişikliği görmek için sayfayı yenilemeniz gerekebilir.

Elektronik faturalama artık kullanıma hazır.

> [!NOTE]
> Şirketler genellikle birkaç Finance veya Supply Chain Management ortamına sahiptir. Bu ortamlarda üretim ortamları, Kullanıcı Kabul Testi (UAT) ortamları ve geliştirme (korumalı alan) ortamları sayılabilir. Elektronik faturalamaya bağlamak istediğiniz tüm ortamlar için yukarıdaki prosedürü tamamlamanız gerekir.
