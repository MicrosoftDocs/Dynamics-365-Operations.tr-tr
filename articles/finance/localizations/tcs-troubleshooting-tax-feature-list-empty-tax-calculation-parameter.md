---
title: Vergi hesaplama parametrelerinde boş vergi özelliği listesi
description: Bu konu, Vergi hesaplama parametreleri sayfasındaki vergi özellikleri listesinin boş olduğu bir sorunun nasıl giderileceğini açıklamaktadır.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 5b87499042c9c4bfe76e182b170adf4f1cfeac4b
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388574"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Vergi hesaplama parametrelerinde boş vergi özelliği listesi

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="symptom"></a>Belirti

Microsoft Dynamics 365 Finance'te kullanabilmeniz için, Regulatory Configuration Service (RCS) içinde bir özellik yayımladınız. Ancak, Finance'i açtığınızda ve **Vergi** \> **Kurulum** \> **Vergi yapılandırması** \> **Vergi hesaplama parametrelerine** gidip **Özellik kurulum adı** alanına gittiğinizde değerler listesi boş.

## <a name="reason"></a>Neden

Bu sorun genellikle Finance ortamınız ve RCS ortamınızın aynı kiracı altında olmadığı için oluşur.

### <a name="rcs-tenant"></a>RCS kiracısı

RCS kiracınızın kimliğini bulmak için bu adımları izleyin.

1. Tam RCS URL'sini kopyalayın. Örneğin, URL şu şekilde olabilir: `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`.
2. InPrivate tarayıcı penceresini açın, RCS YRL'sini Adres çubuğuna yapıştırın ve **Enter** tuşunu seçin. RCS kiracı kimliğini bulabileceğiniz oturum açma sayfasına yönlendirilirsiniz. Örneğin, oturum açma sayfasının URL'si `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d` ise, kiracı kimliği, `https://login.microsoftonline.com/` kısmından sonra beliren bilgi veya **d335a570-a05b-4bc5-8eb3-c42c65f9560d** öğesidir.

### <a name="finance-environment-tenant-id"></a>Finance ortamı kiracı kimliği

Finance ortamınızın kiracı kimliğini bulmak için, RCS kiracısını bulmak amacıyla izlediğiniz adımların aynısını izleyin. Ancak, tam RCS URL'si yerine, Finance ortamınızın tam URL'sini kopyalayın ve yapıştırın.

## <a name="resolution"></a>Çözüm

İki kiracının kodu farklıysa, bu konuda açıklanan sorunla karşılaşırız. Aynı değillerse, ilişkisiz bir konuyla karşılaşıyoruz. Bu durumda, Microsoft Destek ile bağlantı kurmamız önerilir.

### <a name="solution-1"></a>Çözüm 1

RCS ortamınızı, Finance ortamınızın oturum açtığı aynı kiracıda imzalayın. Sonra vergi özelliğini oluşturun ve yayımlayın.

### <a name="solution-2"></a>Çözüm 2

Vergi özelliğini RCS'deki Finance kiracısı ile paylaşın.

1. RCS'de, **Genelleştirme özellikleri** \> **Vergi Hesaplama**'ya gidin.
2. Paylaşılacak özelliği seçin ve sonra **Kuruluşlar** sekmesinde **Paylaş**'ı seçin.
3. **Kuruluş etki alanı adı** alanına bir ad girin. Örneğin **contoso.onmicrosoft.com** yazın.
4. **Paylaş**'ı seçin.

![Harici kuruluş açılır listesi iletişim kutusuyla paylaşın.](media/ShareTaxFeature.png)
