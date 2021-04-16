---
title: RCS'deki/Genel depodaki ER yapılandırmalarını harici kuruluşlarla paylaşma
description: Bu konuda, Microsoft Regulatory Configuration Services (RCS)/Genel depodaki Elektronik raporlama (ER) yapılandırmalarının harici kuruluşlarla doğrudan nasıl paylaşılacağı açıklanmaktadır.
author: JaneA07
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ace62319bbfa38bcf4be7157882dd0c8989e25bc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838757"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>Regulatory Configuration Services (RCS)/Genel depodaki Elektronik raporlama (ER) yapılandırmalarını harici kuruluşlarla paylaşma

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) yapılandırmalarını paylaşmak ve harici kuruluşlara yayımlamak için Microsoft Regulatory Configuration Services'ı (RCS) kullanabilirsiniz.

Aşağıdaki yordamlarda, bir RCS kullanıcısının harici kuruluşla bir RCS örneğinde yapılandırılmış bir ER yapılandırmasının sürümünü nasıl paylaşabileceği açıklanmaktadır. Bu yordamları tamamlamadan önce aşağıdaki önkoşulları tamamlamanız gerekir:

- RCS örneğine erişin.
- Etkin bir yapılandırma sağlayıcısı oluşturun. Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
- ER yapılandırmasının yeni bir sürümünü oluşturun ve yükleyin. Daha fazla bilgi için bkz. [Elektronik raporlama (ER) yapılandırmasının yeni bir sürümünü oluşturma ve yükleme](rcs-global-repo-upload.md).

Ayrıca, şirketiniz için bir RCS ortamının sağlandığından da emin olmalısınız.

1. Finance and Operations uygulamasında, **Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** bölümüne gidin.
2. Şirketiniz için hiçbir RCS ortamı sağlanmamışsa **Regulatory services - Harici yapılandırma**'yı seçin ve ardından bir ortam sağlamak için yönergeleri izleyin.

Şirketiniz için zaten bir RCS ortamı sağlanmışsa oturum açma seçeneğini belirleyerek bu URL'ye erişmek için sayfa URL'sini kullanın.

## <a name="verify-the-configuration-that-you-want-to-share"></a>Paylaşmak istediğiniz yapılandırmayı doğrulama

Paylaşmak istediğiniz yapılandırmanın Genel depoya önceden yüklenmiş olduğundan emin olmak için aşağıdaki adımları izleyin.

1. **Elektronik raporlama** çalışma alanında, yapılandırma sağlayıcınız için **Depolar**'ı seçin.

    ![Konfigürasyon sağlayıcıları](media/1_RCS_Repo_for_config_provider.JPG)

2. **Genel havuz** \> **Aç**'ı seçin.
3. Paylaşmak istediğiniz yapılandırmayı arayın. Aramanızı daraltmak için filtre alanını kullanabilirsiniz. Yapılandırmayı Genel depoda bulamazsanız [Elektronik raporlama (ER) yapılandırmasının yeni bir sürümünü oluşturma ve yükleme](rcs-global-repo-upload.md) konusundaki adımları izleyin.

## <a name="share-er-configurations-with-external-organizations"></a>ER yapılandırmalarını harici kuruluşlarla paylaşma

Yapılandırma sağlayıcınız altında bir yapılandırma oluşturulduktan sonra, **Genel yapılandırma deposu** sayfasındaki **Paylaşıldı** hızlı sekmesini kullanarak harici kuruluşlarla bunu doğrudan paylaşabilirsiniz.

1. **Elektronik raporlama** çalışma alanında, yapılandırma sağlayıcınız için **Depolar**'ı seçin.
2. **Genel havuz** \> **Aç**'ı seçin. 
3. Paylaşmak istediğiniz yapılandırmayı seçin.
4. **Paylaşıldı** hızlı sekmesinde **Kuruluş**'u seçin.

    ![Paylaşıldı hızlı sekmesi](media/1_RCS_Repo_for_Share_with_org.JPG)

5. İletişim kutusunda, harici kuruluşun etki alanı adını girin ve **Tamam**'ı seçin.

    ![Yapılandırma sürümünü harici kuruluş ile paylaş iletişim kutusu](media/1_RCS_Repo_for_Share_with_form.JPG)

Yapılandırma, harici kuruluşla paylaşılır ve Genel depodaki bu kuruluş tarafından kullanılabilir. Buradan, kuruluşun RCS örneğine veya Finance and Operations uygulama örneklerine içe aktarılabilir.

6. Daha önce harici bir kuruluşla paylaşılan bir yapılandırmanın paylaşımını kaldırmak için yapılandırmayı seçin ve **Paylaşımı kaldır**'ı, ardından **Tamam**'ı seçin


[!INCLUDE[footer-include](../../includes/footer-banner.md)]