---
title: Elektronik faturalama hizmet yönetimini kullanmaya başlama
description: Bu konu, elektronik faturalamayı kullanmaya nasıl başlayacağınızı açıklar.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840160"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Elektronik faturalama hizmet yönetimini kullanmaya başlama

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki prosedürleri tamamlamadan önce, aşağıdaki önkoşulların yerine getirilmesi gerekir:

- Microsoft Dynamics Lifecycle Services (LCS) hesabınıza erişiminiz olmalıdır.
- Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management'ın 10.0.17 veya sonraki sürümünü içeren bir LCS projeniz olmalıdır. Ayrıca, bu uygulamaların aşağıdaki Azure coğrafyalarından birinde dağıtılması gerekir:

    - Doğu ABD
    - Batı ABD
    - Kuzey AB
    - Batı AB

- Dynamics 365 Regulatory Configuration Services (RCS) hesabınıza erişiminiz olmalıdır.
- Özellik yönetiminde RCS hesabınız için Globalleştirme özelliğini etkinleştirmeniz gerekir. Daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).
- Azure'da bir anahtar kasası ve depolama hesabı oluşturmanız gerekir. Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Lifecycle Services'de mikro hizmetler için eklentiyi yükleme

1. LCS hesabınızda oturum açın.
2. **Önizleme özelliği yönetimi** kutucuğunu seçin.
3. **Genel Önizleme Özellikleri** bölümünde, **e-Faturalama hizmeti**'ni seçin.
4. **Önizleme özelliği etkin** seçeneğinin **Evet** olarak ayarlanmış olduğundan emin olun.
5. LCS panonuzda, LCS dağıtım projenizi seçin. LCS projesi çalışıyor olmalıdır.
7. **Ortam eklentileri** sekmesinde, **Yeni eklenti yükle**'yi seçin.
8. **E-faturalama hizmetlerini** seçin.
9. **AAD uygulama kodu** alanına şunu girin: **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Bu sabit bir değerdir.
10. **AAD kiracı kimliği** alanında, Azure abonelik hesabınızın kiracı kimliğini girin.
11. Hüküm ve koşulları inceleyin ve ardından onay kutusunu seçin.
12. **Yükle**'yi seçin.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Elektronik faturalamayla RCS entegrasyonu için parametreleri ayarlama

1. RCS hesabınızda oturum açın.
2. **İlgili bağlantılar** içinde, **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri**'ni seçin.
3. **e-Faturalama hizmeti** sekmesinde, **Hizmet uç noktası URI**'si alanına, aşağıdaki tabloda gösterildiği gibi Azure coğrafyanız için uygun hizmet uç noktasını girin.

    | Veri merkezi Azure coğrafyası | Hizmet uç noktası URI'si                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Doğu ABD                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | Batı ABD                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Kuzey AB                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Batı AB                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. **Uygulama Kimliği** alanının **0cdb527f-a8d1-4bf8-9436-b352c68682b2** olarak ayarlı olduğunu doğrulayın. Bu değer sabit bir değerdir.
5. **LCS Ortam Kimliği** alanına LCS ortamınızın kimliğini girin.
6. **Kaydet**'i seçip sayfayı kapatın.

## <a name="create-key-vault-references"></a>Key Vault başvuruları oluşturma

1. RCS hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Ortam** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
3. **Ortam kurulumları** sayfasında, Eylem Bölmesi'nde **Hizmet ortamı**'nı ve ardından **Anahtar kasası parametreleri**'ni seçin.
4. Key Vault başvurusu oluşturmak için **Yeni**'yi seçin.
5. **Ad** alanına Key Vault başvurusunun adını girin. **Açıklama** alanına bir açıklama girin.
6. **Key Vault URI** alanına, key vault gizli dizisini Azure Key Vault'tan yapıştırın. Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).
7. **Kaydet**'i seçin.

## <a name="create-storage-account-secret"></a>Depolama hesabı gizli dizisi oluşturma

1. **Ortam kurulumları** sayfasında, Eylem Bölmesi'nde **Hizmet ortamı** > **Key Vault parametreleri**'ni seçin.
2. Bir **Key Vault başvurusu** seçin ve **Sertifikalar** bölümünde **Ekle**'yi seçin.
3. **Ad** alanına depolama hesabı gizli dizisinin adını girin. Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).
4. **Açıklama** alanına bir açıklama girin.
5. **Tür** alanında **Gizli Dizi**'yi seçin.
6. **Kaydet**'i seçip sayfayı kapatın.

## <a name="create-a-digital-certificate-secret"></a>Dijital sertifika gizli dizisi oluşturma

1. **Ortam kurulumları** sayfasında, Eylem Bölmesi'nde **Hizmet ortamı**'nı ve ardından **Key Vault parametreleri**'ni seçin.
2. Bir **Key Vault başvurusu** seçin ve ardından **Sertifikalar** bölümünde **Ekle**'yi seçin.
3. **Ad** alanına dijital sertifika gizli dizisinin adını girin. Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).
4. **Açıklama** alanına bir açıklama girin.
5. **Tür** alanında **Sertifika**'yı seçin.
6. **Kaydet**'i seçip sayfayı kapatın.

## <a name="create-a-service-environment"></a>Hizmet ortamı oluşturma

1. RCS hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Ortam** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
3. **Ortam kurulumları** sayfasındaki Eylem bölmesinde **Hizmet ortamı**'nı seçin.
4. Yeni hizmet ortamı oluşturmak için **Yeni**'yi seçin.
5. **Ad** alanına E-faturalama ortamının adını girin. **Açıklama** alanına bir açıklama girin.
6. **Depolama SAS belirteci gizli dizisi** alanında, depolama hesabına erişimin kimliğini doğrulamak için kullanılması gereken depolama hesabı gizli dizisinin adını seçin.
7. **Kullanıcılar** bölümünde, ortam üzerinden elektronik fatura göndermesine ve ayrıca depolama hesabına bağlanmasına izin verilen bir kullanıcı eklemek için **Ekle**'yi seçin.
8. **Kullanıcı Kimliği** alanına,kullanıcının diğer adını girin. **E-posta** alanına kullanıcının e-posta adresini girin.
9. **Kaydet**'i seçin.
10. Ülke/bölgenize özgü faturalarınız dijital imzaları uygulamak için bir sertifika zinciri gerektiriyorsa, Eylem bölmesinde **Anahtar kasası parametreleri**'ni seçin, ardından **Sertifikalar zinciri**'ni seçin ve şu adımları izleyin:
    1. Bir sertifika zinciri oluşturmak için **Yeni**'yi seçin.
    2. **Ad** alanına sertifika zinciri adını girin. **Açıklama** alanına bir açıklama girin.
    3. **Sertifikalar** bölümünde, zincire sertifika eklemek için **Ekle**'yi seçin.
    4. Sertifikanın zincirdeki konumunu değiştirmek için **Yukarı** veya **Aşağı** düğmesini kullanın.
    5. **Kaydet**'i seçip sayfayı kapatın.
    6. Sayfayı kapatın.
11. **Hizmet ortamı** sayfasında, Eylem Bölmesi'nde, ortamı bulutta yayınlamak için **Yayınla**'yı seçin. **Durum** alanının değeri **Yayınlandı** olarak değiştirilir.

## <a name="create-a-connected-application"></a>Bağlı bir uygulama oluşturma

1. **Ortam kurulumları** sayfasındaki Eylem bölmesinde **Bağlı uygulamalar**'ı seçin.
2. Yeni bir bağlı uygulama oluşturmak için **Yeni**'yi seçin.
3. **Ad** alanına bağlanacak uygulamanın adını girin.
4. **Uygulama** alanına, bağlanılacak Finance ve Supply Chain Management ortamının URL'sini girin.
4. **Kiracı** alanına, Finance ve Supply Chain Management ortamının kiracısını girin.
5. **Kaydet**'i seçin.
6. Eylem bölmesinde, ortamla bağlantıyı test etmek için **Bağlantıyı denetle**'yi seçin. Ardından sayfayı kapatın.

## <a name="link-connected-applications-to-environments"></a>Bağlı uygulamaları ortamlara bağlama

1. **Ortam kurulumları** sayfasında, bir ortama bağlı bir uygulama atamak için **Yeni**'yi seçin.
2. **Bağlı uygulama** alanından, bağlı bir uygulama seçin.
3. **Hizmet ortamı** alanında, bir hizmet ortamı seçin.
4. **Kaydet**'i seçip sayfayı kapatın.

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>Finance ve Supply Chain Management uygulamalarında Elektronik faturalama kurulumu

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>Elektronik faturalama tümleştirme özelliğini açma

1. Finance veya Supply Chain Management kurulumunuzda oturum açın.
2. **Özellik yönetimi** çalışma alanında, **Elektronik faturalamayı tümleştirme** özelliğini arayın. Bu özellik sayfada görünmüyorsa **Güncelleştirmeleri denetle**'yi seçin.
3. Özelliği seçin ve **Şimdi etkinleştir** düğmesini seçin.

### <a name="set-up-the-service-endpoint-url"></a>Servis uç noktası URL'sini ayarlama

1. **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.
2. **Gönderim hizmeti** sekmesinde, **Hizmet uç noktası URL**'si alanına, aşağıdaki tabloda gösterildiği gibi Azure coğrafyanız için uygun hizmet uç noktasını girin.

    | Veri merkezi Azure coğrafyası | Hizmet uç noktası URL'si                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Doğu ABD                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | Batı ABD                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Kuzey AB                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Batı AB                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. **Ortam** alanına Elektronik faturalamada yayınlanan hizmet ortamının adını girin.
4. **Kaydet**'i seçip sayfayı kapatın.

### <a name="enable-flighting-keys"></a>Deneme anahtarlarını etkinleştir

Microsoft Dynamics 365 Finance veya Microsoft Dynamics 365 Supply Chain Management sürümleri 10.0.17 veya öncesi için deneme anahtarlarını etkinleştirin. 
1. Aşağıdaki SQL komutunu çalıştırın:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Tüm AOS işlemleri için IISreset komutu gerçekleştirin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
