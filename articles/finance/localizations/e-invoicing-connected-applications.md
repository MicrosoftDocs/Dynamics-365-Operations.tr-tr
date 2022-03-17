---
title: Bağlı uygulamalar
description: Bu konu, Elektronik faturalamada bağlı uygulamaları kurmayı açıklamaktadır.
author: dkalyuzh
ms.date: 02/07/2022
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
ms.openlocfilehash: 59b67589139c0ce332716acf998825c6a024bded
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371740"
---
# <a name="connected-applications"></a>Bağlı uygulamalar

[!include [banner](../includes/banner.md)]

Bağlı uygulamalar, Regulatory Configuration Service (RCS) üzerinden ulaşmak istediğiniz Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management örnekleridir. Bağlı uygulamalar sayesinde, Finance ve Supply Chain Management'ta Genelleştirme özelliğinin bir kısmını, Elektronik faturalamayı çalışır hale getirmek için konfigüre edebilirsiniz.

Genelleştirme özelliğini dağıttığınızda, Finance veya Supply Chain Management uygulamanıza uygun kurulum bilgileri doğrudan RCS'den uygun bağlı uygulamaya yayımlanabilir.

RCS'de Finance veya Supply Chain Management parametrelerinin kullanılabilirliği, Kullanıcı Kabulü Testi (UAT) ve üretim ortamları gibi birkaç uygulama ortamınız olduğunda ve aynı parametreleri farklı ortamlara dağıtarak kurulumu tutarlı tutmak istediğinizde yararlıdır.

## <a name="create-a-connected-application"></a>Bağlı bir uygulama oluşturma

1. RCS hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Ortam** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
3. **Ortam kurulumu** sayfasındaki Eylem Bölmesi'nde **Bağlı uygulamalar**'ı seçin.
4. Yeni bir bağlı uygulama oluşturmak için **Yeni**'yi seçin.
5. **Ad** alanına bağlanacak uygulamanın adını girin.
6. **Tür** alanında, **Dynamics 365 Finance**'ü seçin.
7. **Uygulama** alanına, bağlanacak ortamın URL'sini girin.
8. **Kiracı** alanında, ortamın kiracısını girin.
9. **Kaydet**'i seçin.
10. Eylem bölmesinde, ortamla bağlantıyı test etmek için **Bağlantıyı denetle**'yi seçin. Ardından sayfayı kapatın.

## <a name="link-connected-applications-to-environments"></a>Bağlı uygulamaları ortamlara bağlama

1. **Ortam kurulumu** sayfasında, bir ortama bağlı bir uygulama atamak için **Yeni**'yi seçin.
2. **Bağlı uygulama** alanından, bağlı bir uygulama seçin.
3. **Hizmet ortamı** alanında, bir hizmet ortamı seçin.
4. **Kaydet**'i seçip sayfayı kapatın.
