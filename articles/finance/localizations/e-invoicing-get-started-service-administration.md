---
title: Elektronik faturalama eklentisi hizmet yönetimini kullanmaya başlama
description: Bu konu, elektronik faturalama eklentisini kullanmaya nasıl başlayacağınızı açıklar.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104448"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a>Elektronik faturalama eklentisi hizmet yönetimini kullanmaya başlama

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki prosedürleri tamamlamadan önce, aşağıdaki önkoşulların yerine getirilmesi gerekir:

- Microsoft Dynamics Lifecycle Services (LCS) hesabınıza erişiminiz olmalıdır.
- Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management'ın 10.0.13 veya sonraki sürümünü içeren bir LCS projeniz olmalıdır. Ayrıca, bu uygulamaların aşağıdaki Azure coğrafyalarından birinde dağıtılması gerekir:

    - Doğu ABD
    - Batı ABD
    - Kuzey AB
    - Batı AB

- Dynamics 365 Regulatory Configuration Services (RCS) hesabınıza erişiminiz olmalıdır.
- Özellik yönetiminde RCS hesabınız için Globalleştirme özelliğini etkinleştirmeniz gerekir. Daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).
- Azure'da bir anahtar kasası ve depolama hesabı oluşturmanız gerekir. Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a>Lifecycle Services'de mikro hizmetler için eklentiyi yükleme

1. LCS hesabınızda oturum açın.
2. **Önizleme özelliği yönetimi** kutucuğunu seçin.
3. **Genel Önizleme Özellikleri** bölümünde, **e-Faturalama hizmeti**'ni seçin.
4. **Önizleme özelliği etkin** seçeneğinin **Evet** olarak ayarlanmış olduğundan emin olun.

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a>Elektronik faturalama eklentisiyle RCS entegrasyonu için parametreleri ayarlama

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
5. **LCS Ortam Kimliği** alanına LCS abonelik hesabınızın kimliğini girin.
6. **Kaydet**'i seçip sayfayı kapatın.

## <a name="create-key-vault-secret"></a>Key Vault gizli dizisini oluşturma

1. RCS hesabınızda oturum açın.
2. **Globalleştirme özelliği** çalışma alanında **Ortam** bölmesinde **e-faturalama** kutucuğunu seçin.
3. **Ortam kurulumları** sayfasında, Eylem Bölmesi'nde **Hizmet ortamı**'nı ve ardından **Anahtar kasası parametreleri**'ni seçin.
4. Yeni bir anahtar kasası gizli dizisi oluşturmak için **Yeni**'yi seçin.
5. **Ad** alanına anahtar kasası gizli dizisi adını girin. **Açıklama** alanına bir açıklama girin.
6. **Anahtar Kasası URI**'si alanına, gizli dizi Azure Key Vault'tan yapıştırın.
7. **Kaydet**'i seçin.

## <a name="create-storage-account-secret"></a>Depolama hesabı gizli dizisi oluşturma

1. **Anahtar kasası parametreleri** sayfasında, **Sertifikalar** bölümünde **Ekle**'yi seçin.
2. **Ad** alanına depolama hesabı gizli dizisinin adını girin. **Açıklama** alanına bir açıklama girin.
3. **Tür** alanında **Sertifika**'yı seçin.
4. **Kaydet**'i seçip sayfayı kapatın.

## <a name="create-an-electronic-invoicing-add-on-environment"></a>Elektronik faturalama eklentisi ortamı oluşturma

1. RCS hesabınızda oturum açın.
2. **Globalleştirme özelliği** çalışma alanında **Ortam** bölmesinde **e-faturalama** kutucuğunu seçin.

## <a name="create-a-service-environment"></a>Hizmet ortamı oluşturma

1. **Ortam kurulumları** sayfasındaki Eylem bölmesinde **Hizmet ortamı**'nı seçin.
2. Yeni hizmet ortamı oluşturmak için **Yeni**'yi seçin.
3. **Ad** alanına E-faturalama ortamının adını girin. **Açıklama** alanına bir açıklama girin.
4. **Depolama SAS belirteci gizli dizisi** alanında, depolama hesabına erişimin kimliğini doğrulamak için kullanılması gereken sertifikanın adını seçin.
5. **Kullanıcılar** bölümünde, ortam üzerinden elektronik fatura göndermesine ve ayrıca depolama hesabına bağlanmasına izin verilen bir kullanıcı eklemek için **Ekle**'yi seçin.
6. **Kullanıcı Kimliği** alanına,kullanıcının diğer adını girin. **E-posta** alanına kullanıcının e-posta adresini girin.
7. **Kaydet**'i seçin.
8. Ülke/bölgenize özgü faturalarınız dijital imzaları uygulamak için bir sertifika zinciri gerektiriyorsa, Eylem bölmesinde **Anahtar kasası parametreleri**'ni seçin, ardından **Sertifikalar zinciri**'ni seçin ve şu adımları izleyin:

    1. Bir sertifika zinciri oluşturmak için **Yeni**'yi seçin.
    2. **Ad** alanına sertifika zinciri adını girin. **Açıklama** alanına bir açıklama girin.
    3. **Sertifikalar** bölümünde, zincire sertifika eklemek için **Ekle**'yi seçin.
    4. Sertifikanın zincirdeki konumunu değiştirmek için **Yukarı** veya **Aşağı** düğmesini kullanın.
    5. **Kaydet**'i seçip sayfayı kapatın.
    6. Sayfayı kapatın.
9. **Hizmet ortamı** sayfasında, Eylem Bölmesi'nde, ortamı bulutta yayınlamak için **Yayınla**'yı seçin. **Durum** alanının değeri **Yayınlandı** olarak değiştirilir.

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

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a>Finance ve Supply Chain Management'ta Elektronik faturalama eklentisi tümleştirmesini ayarlama

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Elektronik faturalama eklenti tümleştirme özelliğini açma

1. Finance veya Supply Chain Management kurulumunuzda oturum açın.
2. **Özellik yönetimi** çalışma alanında, **Elektronik faturalama eklentisini tümleştirme** özelliğini arayın. Bu özellik sayfada görünmüyorsa **Güncelleştirmeleri denetle**'yi seçin.
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

3. **Ortam** alanına Elektronik faturalama eklentissi ortamının adını girin.
4. **Kaydet**'i seçip sayfayı kapatın.
