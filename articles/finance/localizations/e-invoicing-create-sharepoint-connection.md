---
title: SharePoint bağlantısını yapılandırma
description: Bu makalede, Elektronik faturalamanın Microsoft SharePoint sitesine erişebilmesi için bağlantının nasıl yapılandırılacağı açıklanmaktadır.
author: gionoder
ms.date: 12/15/2021
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
ms.openlocfilehash: a2762178686d1f29c457b6de2a9b052fd048484b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284002"
---
# <a name="configure-a-sharepoint-connection"></a>SharePoint bağlantısını yapılandırma

[!include [banner](../includes/banner.md)]

Elektronik faturalama hizmeti, Microsoft SharePoint klasörlerinden dosyaları okuyabilir ve dosyaları SharePoint'e yükleyebilir. Elektronik faturalamanın belirli bir SharePoint sitesine erişebilmesini sağlamak için, elektronik faturalama hizmetine site kimlik bilgilerini sağlamanız gerekir. Ek olarak, kimlik bilgilerinin güvenli şekilde depolanmasını sağlamak için bunları doğrudan sağlamadığınızdan emin olun. Bunun yerine, bunları bir Azure Key Vault içinde depolayın ve bir Azure Key Vault gizli dizisi sağlayın.

## <a name="grant-access-to-a-sharepoint-folder"></a>Bir SharePoint klasörüne erişim sağlama

1. Kiracıda, Regulatory Configuration Service'in (RCS) yüklendiği yerde bir uygulama kaydı oluşturun.

    1. [Azure portalında](https://portal.azure.com/) adresinden oturum açın.
    2. **Uygulama kayıtları**'na gidin.
    3. **Yeni kayıt** öğesini seçin.
    4. **Elektronik Faturalama için SharePoint Uygulaması** gibi bir ad girin ve kayıt işlemini tamamlayın
    5. Yeni uygulama kaydını seçin.
    6. **Kimlik doğrulama** sekmesinde **Ortak istemci akışlarına izin ver** seçeneğini etkinleştirin.
    4. **Sertifikalar ve gizli diziler** sekmesinde, bir gizli anahtar oluşturmak için **Yeni gizli anahtar**'ı seçin.
    5. Oluşturulan gizli dizi değerini kopyalayın.

    Aşağıdaki yönergeleri izleyin:

    - Farklı hizmetler için aynı uygulama kaydını kullanmayın.
    - [Parola ilkesi önerilerine](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide) uyun.
    - Farklı parolalardan oluşan bir döngü belirleyin. Döngü sırasında, uygulama kaydı için yeni bir gizli anahtar oluşturun, Key Vault'u güncelleştirin ve eski gizli diziyi silin.

2. **Uygulama Kaydı gizli dizisi** ve **Uygulama (istemci) kimliği** değerlerini, elektronik faturalama ortamınızın kurulumunda anahtar kasaya iki yeni parola olarak kaydedin.
3. Oluşturduğunuz gizli dizileri, RCS'de Elektronik faturalama ortamınızın kurulumunda Key Vault parametrelerine ekleyin.
4. Azure portalında, SharePoint'e erişim izni verin. Bu adımın kiracı yöneticisi tarafından tamamlanması gerekir.

    1. Oluşturduğunuz uygulama kaydını seçin.
    2. **API izinleri** sekmesinde, **İzin ekle**'yi seçin.
    3. **Microsoft Graph (Uygulama izinleri)** \> **Sites.Selected**'ı seçin.
    4. **\<user&nbsp;name\> için yönetici izni ver**'i seçin.
    5. İzinlerin verildiğinden emin olmak için **Durum** alanını gözden geçirin.

        ![API izinleri sekmesinde izinler verildi.](media/configured-permissions.jpg)

    6. [Graph Gezgini - Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer)'ı açın ve oturum açın.
    7. Sol bölmede, **Örnek sorgular** sekmesinde, **SharePoint Siteleri** altında, **sitenin göreli yoluna göre SharePoint sitesini al** öğesini seçin.
    8. **\{host-name\}** ve **\{server-relative-path\}** parametrelerini doldurun. Örneğin, **\{host-name\}** için `<domain>.sharepoint.com` ve **\{server-relative-path\}** için `sites/<siteName>` öğesini doldurun.

        > [!NOTE]
        > Varsayılan web sitesi için, **\{server-relative-path\}** parametresini boş bırakın.

    9. **Sorguyu çalıştır**'ı seçin ve sonucu kaydedin.
    10. Aşağıdaki sorguyu konfigüre edin.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        Bu sorgude, **\{site-id\}**, önceki sorgu yanıtından alınan **kimlik** düğümünün değeridir.

        İstek gövdesi aşağıdadır.

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        İstek gövdesinde, **\{app-id\}** **Uygulama (istemci) kimliği** değeridir ve **\{app-name\}** ise **Uygulama adı** değeridir.

        ![POST sorgusu.](media/app-id-query.jpg)

    11. **İzinleri değiştir** sekmesinde, **İzinler panelini aç**'ı seçin ve sonra **Siteler** \> **Sites.FullControl.All** \> **Onay**'ı seçin.
    12. **Sorguyu çalıştır**'ı seçin.

Elektronik faturalama servisi artık SharePoint sitenize erişebilir.
