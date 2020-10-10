---
title: RCS'de ER yapılandırmaları oluşturma ve bunları Genel depoya yükleme
description: Bu konuda, Microsoft Regulatory Configuration Services (RCS) içinde Elektronik raporlama (ER) yapılandırmasının nasıl oluşturulacağı ve Genel depoya nasıl yükleneceği açıklanmaktadır.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 5b2b8f35b9931f8fd1824c20e9045da68af33ad5
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834245"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Regulatory Configuration Services (RCS) içinde ER yapılandırmaları oluşturma ve bunları Genel depoya yükleme

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) yapılandırmalarını tasarlamak ve kuruluşunuzda kullanılabilmeleri için yayımlamak üzere Microsoft Regulatory Configuration Services'ı (RCS) kullanabilirsiniz.

Aşağıdaki yordamlarda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının bir RCS örneğinde yapılandırılmış ER yapılandırmasının türetilmiş bir sürümünü nasıl oluşturabileceği ve sonra türetilmiş yapılandırmayı Genel depoya nasıl yükleyebileceği açıklanmaktadır. 

Bu yordamları tamamlamadan önce aşağıdaki önkoşulları tamamlamanız gerekir:

- RCS örneğine erişin.
- Etkin bir yapılandırma sağlayıcısı oluşturun. Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Ayrıca, şirketiniz için bir RCS ortamının sağlandığından da emin olmalısınız.

1. Finance and Operations uygulamasında, **Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** bölümüne gidin.
2. Şirketiniz için hiçbir RCS ortamı sağlanmamışsa **Regulatory services - Harici yapılandırma**'yı seçin ve ardından bir ortam sağlamak için yönergeleri izleyin.

Şirketiniz için zaten bir RCS ortamı sağlanmışsa oturum açma seçeneğini belirleyerek bu URL'ye erişmek için sayfa URL'sini kullanın.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>RCS'de yapılandırmanın türetilmiş bir sürümünü oluşturma

1. **Elektronik raporlama** çalışma alanında, kuruluşunuz için etkin bir yapılandırma sağlayıcınız olduğunu doğrulayın. 
2. **Raporlama yapılandırmaları**'nı seçin.
3. Yeni bir sürüm türetmek istediğiniz yapılandırmayı seçin. Aramanızı daraltmak için ağacın üzerindeki filtre alanını kullanabilirsiniz.
4. **Yapılandırma oluştur** \> **İsimden Türet**'i seçin.
5. Ad ve açıklama girin ve ardından yeni bir türetilmiş sürüm oluşturmak için **Yapılandırma oluştur**'u seçin.
6. Yeni türetilen yapılandırmayı seçin, sürümün bir tanımını ekleyin ve ardından **Tamam**'ı seçin. Yapılacak yapılandırmanın durumu **Tamamlandı** olarak değişir.

![RCS'de yeni yapılandırma sürümü](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Yapılandırma durumu değiştirildiğinde bağlı uygulamalarla ilgili bir doğrulama hata mesajı alabilirsiniz. Doğrulamayı kapatmak için **Yapılandırmalar** sekmesindeki Eylem Bölmesi'nde, **Kullanıcı parametreleri**'ni seçin ve ardından **Yapılandırmanın durum değişikliği ve yeniden temellendirmede doğrulamayı atla** seçeneğini **Evet** olarak ayarlayın 

## <a name="upload-a-configuration-to-the-global-repository"></a>Genel depoya bir yapılandırma yükleme

Kuruluşunuzla, yeni veya türetilmiş bir yapılandırmayı paylaşmak için yapılandırmayı Genel depoya yükleyebilirsiniz.

1. Yapılandırmanın tamamlanmış sürümünü ve ardından **Depoya yükle**'yi seçin.
2. **Genel (Microsoft)** seçeneğini ve ardından **Yükle**'yi seçin.

    ![Depo seçeneklerine yükleme](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Onay iletisi kutusunda **Evet**'i seçin. 
4. Sürümün açıklamasını gerektiği gibi güncelleştirin ve ardından **Tamam**'ı seçin. 

Yapılandırmanın durumu **Paylaş** olarak güncelleştirilir ve yapılandırma Genel depoya yüklenir. Oradan, aşağıdaki yollarla çalışabilirsiniz:

- Dynamics 365 örneğinize aktarın. Daha fazla bilgi için bkz. [(ER) Yapılandırmaları RCS'den içe aktarma](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Üçüncü tarafla veya harici bir kuruluşla paylaşmak için bkz. [RCS, Elektronik raporlama (ER) yapılandırmalarını harici kuruluşlarla paylaşma](rcs-global-repo-share-configuration.md)

    ![Genel depodaki Türetilmiş Intrastat Contoso yapılandırma sürümü](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Genel depodan bir yapılandırma silme
Kuruluşunuzun oluşturmuş olduğu bir yapılandırmayı silmek için aşağıdaki adımları tamamlayın.

1. **Elektronik raporlama** çalışma alanında, yapılandırma sağlayıcınızın **Etkin** olduğunu doğrulayın. Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Etkin yapılandırma sağlayıcınızda, **Depo**'yu seçin.
3. Havuz türünü **Genel** olarak seçin ve **Aç**'ı seçin.
4. **Filtre** hızlı sekmesinde, **Filtre** işlevini kullanarak silmek istediğiniz yapılandırmayı bulun.
5. **Sürüm** hızlı sekmesinde, silmek istediğiniz yapılandırmayla ilgili sürümü seçin ve **Sil**'i seçin:

    ![Genel depodan bir yapılandırma silme](media/RCS_Delete_from_GlobalRepo.JPG)

6. Onay iletisi kutusunda **Evet**'i seçin.

    ![Yapılandırma sürümü onay iletisini silme](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Yapılandırma sürümü silindi ve onay iletisi gösteriliyor. 

> [!NOTE]
> Yapılandırmalar yalnızca kendilerini oluşturan Yapılandırma sağlayıcısı tarafından silinebilir. Yapılandırma başka bir kuruluşla paylaşılıyorsa, silmeden önce bu yapılandırmanın paylaşımdan kaldırılması gerekir.
 
