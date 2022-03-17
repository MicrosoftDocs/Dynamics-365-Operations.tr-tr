---
title: Lifecycle Services'de mikro hizmetler için eklentiyi yükleme
description: Bu konu, Microsoft Dynamics Lifecycle Services (LCS) içindeki Elektronik Faturalama eklentisinin nasıl yükleneceğini açıklamaktadır.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a575f3e26489607dc2143ba05c941240969a0feb
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371847"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Lifecycle Services'de mikro hizmetler için eklentiyi yükleme

[!include [banner](../includes/banner.md)]

Elektronik Faturalama hizmetindeki kimlik doğrulaması, Microsoft Dynamics Lifecycle Services (LCS) ortamınıza yönelik eklentiyi yükleyerek Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management'ın ortamınızı hizmetler platformuna kaydetmenizi gerektirir.

Ortamı kaydetmek için şu adımları izleyin.

1. LCS hesabınızda oturum açın.
2. Proje panonuzda, bir LCS projesi seçin.
2. Projedeki **Ortamlar** panosunda dağıtılan ortamınızı seçin. Seçtiğiniz ortamın çalışıyor olması gerekir.
3. **Power Platform Tümleştirme** sekmesinde, **Ortam eklentileri** bölümünde, **Yeni eklenti yükle**'yi seçin.
4. **Elektronik Faturalama**'yı seçin.
5. **AAD uygulama kodu** alanına şunu girin: **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Bu değer sabit bir değerdir. Yalnızca bir genel benzersiz tanımlayıcı (GUID) girdiğinizden emin olun. Boşluk, virgül, nokta veya tırnak işareti gibi başka semboller eklemeyin.
6. **AAD kiracı kimliği** alanında, Azure abonelik hesabınızın kiracı kimliğini girin. Belirttiğiniz Azure Active Directory (Azure AD) kiracısı, Regulatory Configuration Service (RCS) için kullanılan kiracıyla aynı olmalıdır.
7. Hüküm ve koşulları inceleyin ve ardından onay kutusunu seçin.
8. **Yükle**'yi seçin. Birkaç dakika sonra, durum **Yükleniyor** yerine **Yüklü** olarak değişmelidir. Bu değişikliği görmek için sayfayı yenilemeniz gerekebilir.

Elektronik faturalama artık kullanıma hazır.

> [!NOTE]
> Şirketler genellikle birkaç Finance veya Supply Chain Management ortamına sahiptir. Bu ortamlarda üretim ortamları, Kullanıcı Kabul Testi (UAT) ortamları ve geliştirme (korumalı alan) ortamları sayılabilir. Elektronik faturalamaya bağlamak istediğiniz tüm ortamlar için yukarıdaki prosedürü tamamlamanız gerekir.
