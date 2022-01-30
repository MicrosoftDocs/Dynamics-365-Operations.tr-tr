---
title: RCS'de ER yapılandırmaları oluşturma ve bunları Genel depoya yükleme
description: Bu konuda, Microsoft Regulatory Configuration Services (RCS) içinde Elektronik raporlama (ER) yapılandırmasının nasıl oluşturulacağı ve Genel depoya nasıl yükleneceği açıklanmaktadır.
author: JaneA07
ms.date: 01/11/2021
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
ms.openlocfilehash: eb04362d6d7261af56d2940b085fbc8d43c9d662
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/12/2022
ms.locfileid: "7965101"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>Regulatory Configuration Services (RCS) içinde ER yapılandırmaları oluşturma ve bunları Genel depoya yükleme

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) yapılandırmalarını tasarlamak ve kuruluşunuzda kullanılabilmeleri için yayımlamak üzere Microsoft Regulatory Configuration Services'ı (RCS) kullanabilirsiniz.

Aşağıdaki yordamlarda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının bir RCS örneğinde yapılandırılmış ER yapılandırmasının türetilmiş bir sürümünü nasıl oluşturabileceği ve sonra türetilmiş yapılandırmayı Genel depoya nasıl yükleyebileceği açıklanmaktadır. 

Bu yordamları tamamlamadan önce aşağıdaki önkoşulları tamamlamanız gerekir:

- Kuruluşunuz için bir RCS ortamına erişiminiz olmalı.
- Etkin bir konfigürasyon sağlayıcısı oluşturun ve bunu etkin yapın. Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Ayrıca, kuruluşunuz için bir RCS ortamının sağlandığından da emin olmalısınız. Kuruluşunuz için sağlanmış bir RCS örneğiniz yoksa, aşağıdaki adımları kullanarak bunu yapabilirsiniz:

1. Finance ve Operations uygulamasında, **Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **İlgili bağlantılar / Harici bağlantılar**'da , **Regulatory services – Konfigürasyon**'u seçin ve bir tane sağlamak üzere **Kaydolmak** için yönergeleri izleyin.

Kuruluşunuz için zaten bir RCS ortamı sağlanmışsa **oturum açma** seçeneğini belirleyerek bu URL'ye erişmek için sayfa URL'sini kullanın.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>RCS'de yapılandırmanın türetilmiş bir sürümünü oluşturma

> [!NOTE]
> RCS'yi ilk defa kullanıyorsanız, türetmeniz için kullanılabilecek herhangi bir konfigürasyonunuz olmayacaktır. Global depodan bir konfigürasyon almanız gerekir. Daha fazla bilgi için bkz. [Yapılandırma hizmeti Genel deposundan ER yapılandırmalarını indirme](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

1. RCS'de **oturum açın** ve **Elektronik raporlama** çalışma alanını seçin.
2. Etkin olarak ayarlanmış, kuruluşunuz için etkin bir yapılandırma sağlayıcınız olduğunu doğrulayın (bkz. ön koşullar). 
3. **Raporlama yapılandırmaları**'nı seçin.
4. Yeni bir sürüm türetmek istediğiniz yapılandırmayı seçin. Aramanızı daraltmak için ağacın üzerindeki filtre alanını kullanabilirsiniz.
5. **Yapılandırma oluştur** \> **İsimden Türet**'i seçin.
6. Ad ve açıklama girin ve ardından "Taslak" durumlu yeni bir türetilmiş sürüm oluşturmak için **Yapılandırma oluştur**'u seçin.
7. Yeni türetilmiş konfigürasyonu seçin ve gerekirse konfigürasyon formatında ek değişiklikler yapın. 
8. Değişiklikleriniz tamamlandıktan sonra, konfigürasyonda depoda yayımlayabilmek için **Değişiklik durumu**'nu **Tamamlanmış** olarak ayarlamanız gerekir. **Tamam**'ı seçin.

![RCS'de yeni yapılandırma sürümü.](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> Yapılandırma durumu değiştirildiğinde bağlı uygulamalarla ilgili bir doğrulama hata mesajı alabilirsiniz. Doğrulamayı kapatmak için **Yapılandırmalar** sekmesindeki Eylem Bölmesi'nde, **Kullanıcı parametreleri**'ni seçin ve ardından **Yapılandırmanın durum değişikliği ve yeniden temellendirmede doğrulamayı atla** seçeneğini **Evet** olarak ayarlayın 

## <a name="upload-a-configuration-to-the-global-repository"></a>Genel depoya bir yapılandırma yükleme

Kuruluşunuzla, yeni veya türetilmiş bir yapılandırmayı paylaşmak için yapılandırmayı Genel depoya aşağıdaki adımları izleyerek yükleyebilirsiniz:

1. Yapılandırmanın tamamlanmış sürümünü ve ardından **Depoya yükle**'yi seçin.
2. **Genel (Microsoft)** seçeneğini ve ardından **Yükle**'yi seçin.

    ![Depo seçeneklerine yükleme.](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. Onay iletisi kutusunda **Evet**'i seçin. 
4. Sürümün açıklamasını gerektiği gibi güncelleştirin ve ardından **Tamam**'ı seçin. Ayrıca, sürümü bağlı bir uygulamaya veya bir GIT deposuna da yükleyebilirsiniz.  

Yapılandırmanın durumu **Paylaşılan** olarak güncelleştirilir ve yapılandırma Genel depoya yüklenir. Karşıya yüklediğiniz yapılandırmanın taslak sürümü de oluşturulur ve sonraki değişiklikler gerekliyse kullanılabilir.

Konfigürasyon genel depoya yüklendikten sonra, aşağıdaki yollarla bunlarla çalışabilirsiniz:

- Dynamics 365 örneğinize aktarın. Daha fazla bilgi için bkz. [(ER) Yapılandırmaları RCS'den içe aktarma](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- Üçüncü tarafla veya harici bir kuruluşla paylaşmak için bkz. [RCS, Elektronik raporlama (ER) yapılandırmalarını harici kuruluşlarla paylaşma](rcs-global-repo-share-configuration.md)

    ![Genel depodaki Türetilmiş Intrastat Contoso yapılandırma sürümü.](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a>Genel depodan bir yapılandırma silme
Kuruluşunuzun oluşturmuş olduğu bir yapılandırmayı silmek için aşağıdaki adımları tamamlayın.

1. **Elektronik raporlama** çalışma alanında, yapılandırma sağlayıcınızın **Etkin** olduğunu doğrulayın. Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
2. Etkin yapılandırma sağlayıcınızda, **Depo**'yu seçin.
3. Havuz türünü **Genel** olarak seçin ve **Aç**'ı seçin.
4. **Filtre** hızlı sekmesinde, **Filtre** işlevini kullanarak silmek istediğiniz yapılandırmayı bulun.
5. **Sürüm** hızlı sekmesinde, silmek istediğiniz yapılandırmayla ilgili sürümü seçin ve **Sil**'i seçin:

    ![Genel depodan bir yapılandırma silme.](media/RCS_Delete_from_GlobalRepo.JPG)

6. Onay iletisi kutusunda **Evet**'i seçin.

    ![Yapılandırma sürümü onay iletisini silme.](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
Yapılandırma sürümü silindi ve onay iletisi gösteriliyor. 

> [!NOTE]
> Yapılandırmalar yalnızca kendilerini oluşturan Yapılandırma sağlayıcısı tarafından silinebilir. Yapılandırma başka bir kuruluşla paylaşılıyorsa, silmeden önce bu yapılandırmanın paylaşımdan kaldırılması gerekir.
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
