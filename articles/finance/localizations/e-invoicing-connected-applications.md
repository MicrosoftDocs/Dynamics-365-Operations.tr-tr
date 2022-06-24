---
title: Bağlı uygulamalar
description: Bu makalede, Elektronik faturalamada bağlı uygulamaların nasıl ayarlanacağı açıklanmaktadır.
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
ms.openlocfilehash: 7a0a9c19009c49b80ca8c182c31592c1a713a2aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906301"
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
6. **Tür** alanında **Dynamics 365 Finance**'i seçin.
7. **Uygulama** alanına, bağlanacak ortamın URL'sini girin.
8. **Kiracı** alanında, ortamın kiracısını girin.
9. **Kaydet**'i seçin.
10. Eylem bölmesinde, ortamla bağlantıyı test etmek için **Bağlantıyı denetle**'yi seçin. Ardından sayfayı kapatın.

## <a name="link-connected-applications-to-environments"></a>Bağlı uygulamaları ortamlara bağlama

1. **Ortam kurulumu** sayfasında, bir ortama bağlı bir uygulama atamak için **Yeni**'yi seçin.
2. **Bağlı uygulama** alanından, bağlı bir uygulama seçin.
3. **Hizmet ortamı** alanında, bir hizmet ortamı seçin.
4. **Kaydet**'i seçip sayfayı kapatın.
