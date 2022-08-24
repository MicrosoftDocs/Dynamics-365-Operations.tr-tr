---
title: SharePoint kanalı yapılandırma
description: Bu makalede, Microsoft SharePoint kanalının gelen elektronik faturaları işleyecek şekilde nasıl yapılandırılacağı açıklanmaktadır.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 92eaa357c6d72cc637d4ce353702e5d41ecf4338
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272319"
---
# <a name="configure-a-sharepoint-channel"></a>SharePoint kanalı yapılandırma

[!include [banner](../includes/banner.md)]

Bir Microsoft SharePoint kanalının gelen belgeleri işlemek üzere konfigüre edilmeyle ilgili önkoşulu olarak, [SharePoint bağlantısı yapılandırma](e-invoicing-create-sharepoint-connection.md) bölümünde açıklanan adımları tamamlayın.

Böylece, SharePoint klasörlerinizde depolanan dosyalardan elektronik satıcı faturalarını içe aktarmak için SharePoint kanalını kullanabilirsiniz.

1. SharePoint sitenizde aşağıdaki klasörleri oluşturun:

    - **Ana klasör** – Hizmetin dosyaları işlemek için kullanacağını kaynak klasör.
    - **Arşiv klasörü** – İşlenen dosyaların depolanacağı klasör.
    - **Hata klasörü** – İşlem başarısız olursa, sistemin dosyaları taşıyacağı klasör.

2. Regulatory Configuration Services'te (RCS), oluşturduğunuz Elektronik faturalama özelliğini seçin. **Taslak** durumunda olan sürümü seçtiğinizden emin olun.
3. **Kurulumlar** sekmesinde, **Ekle**'yi seçin.
4. **Özellik kurulumu oluştur** açılan iletişim kutusunda, **Yeni** alan grubunda, **Özel kurulum** seçeneğini belirleyin.
5. **Kurulum türü** alan grubunda, **Veri kanalı** seçeneğini belirleyin.
6. **Veri kanalı seç** alanında, **SharePoint klasörü**'nü seçin.
7. **Oluştur**'u seçin.
8. Oluşturduğunuz satırı seçin ve sonra **Düzenle**'yi seçin.
9. **Veri kanalı** sekmesinde, **Parametreler** bölümünde aşağıdaki gerekli alanları ayarlayın.

    | Alan                 | Açıklama |
    |-----------------------|-------------|
    | Veri kanalı          | Veri kanalını tanımlamak için benzersiz bir ad girin. Ad en fazla 10 karakter uzunluğunda olabilir. İletişim işlemi sırasında, uygulanabilirlik kurallarında ve bağlı uygulamalarda başvurulacak. |
    | SharePoint adresi    | SharePoint URL'sini girin. Örneğin `<domain>.sharepoint.com` yazın. |
    | Uygulama kodu        | SharePoint kullanıcı hesabının kimliğini içeren Azure Key Vault gizli dizisini girin. Bu gizli dizi, Key Vault'ta oluşturulmalı ve hizmet ortamınızda kurulmalıdır. Değer, [SharePoint bağlantısı yapılandırma](e-invoicing-create-sharepoint-connection.md)'dan alınan **Uygulama (istemci) kimliğidir**. |
    | Uygulama gizli anahtarı    | SharePoint kullanıcı hesabının parolasını içeren Key Vault gizli dizisinin adını girin. Değer, [SharePoint bağlantısı yapılandırma](e-invoicing-create-sharepoint-connection.md)'dan alınan **Uygulama Kaydı gizli dizisidir**. |
    | Site adı             | SharePoint sitesinin adını girin. |
    | Belge kitaplığı adı | SharePoint belge kitaplığının adını girin. |
    | Zaman aşımı               | Sistemin yanıt beklemesi için bekleyeceği, milisaniye (ms) cinsinden en fazla süreyi girin. Varsayılan değer 10.000 ms'dir (10 saniye). |
    | Ana klasör           | Dosya alma kaynağını veya hizmetin dosyaları işlemesi gereken klasörü belirtin. |
    | Arşiv klasörü        | İşlenen dosyaların depolanacağı klasörü belirtin. |
    | Hata klasörü          | Sistemin işlem başarısız olduğunda dosyaları taşımak için kullanacağı klasörü belirtin. |
    | Maksimum dosya boyutu         | İşlenen tek bir dosyanın en büyük boyutunu bayt olarak girin. Varsayılan değer 20.000.000 bayttır. |
    | Maksimum dosya sayısı      | Tek bir eylem için işlenecek maksimum dosya sayısını girin. Dosyaların sayısını sınırlandırmak istemiyorsanız, değeri **0** (sıfır) olarak ayarlayın. |
    | Dosya filtresi           | Dosya adına göre filtrelemek için bir dize girin. Bu alan isteğe bağlıdır. **\*smth\*.ext** gibi basit maskeler desteklenir, her bir yıldız işareti (\*) sıfırı veya herhangi bir karakterin birden fazla tekrarlanmasını temsil eder. Örneğin, kanalı PDF dosyaları okuyacak şekilde yapılandırmak için **\*.pdf** girin. |
    | Özel dosya adı      | İstemciden özel dosya adını girin. |

10. **Uygulanabilirlik kuralları** sekmesinde, ölçütleri gerektiği şekilde inceleyip güncelleştirin. **Kanal** alanının değeri önceki adımdaki **Veri kanalı** alanına girdiğiniz değere eşit olmalıdır.
11. **Kaydet**'i seçip sayfayı kapatın.
