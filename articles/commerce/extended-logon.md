---
title: Genişletilmiş oturum açma yeteneğini ayarlama ve kullanma
description: Bu makalede, Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasının genişletilmiş oturum açma yeteneğinin nasıl ayarlanacağı ve kullanılacağı açıklanmaktadır.
author: boycezhu
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.industry: Retail
ms.search.form: RetailFunctionalityProfile
ms.openlocfilehash: e2fc39b1b7fb34f49c061dcc324c28cf5a89277c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283708"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>Genişletilmiş oturum açma yeteneğini ayarlama ve kullanma

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasının genişletilmiş oturum açma yeteneğinin nasıl ayarlanacağı ve kullanılacağı açıklanmaktadır.

Bulut POS (CPOS) ve Modern POS (MPOS), perakende mağaza çalışanlarının bir manyetik bant okuyucu (MSR) kullanarak barkod taramasıyla veya kart kaydırmasıyla POS uygulamasında oturum açmasına olanak tanıyan genişletilmiş bir oturum açma yeteneği sağlar.

## <a name="set-up-extended-logon"></a>Genişletilmiş oturum açmayı ayarlama

Perakende mağazasında POS kayıtlarında genişletilmiş oturum açma için aşağıdaki adımları izleyin.

1. Commerce Headquarters'ta **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> İşlevsellik profilleri**'ne gidin. 
2. Sol gezinti bölmesinde, perakende mağazasıyla ilişkili işlevsellik profilini seçin.
3. **İşlevler** hızlı sekmesinde, **Ek oturum açma kimlik doğrulama seçenekleri** altında aşağıdaki seçenekleri uygun şekilde **Evet** veya **Hayır** olarak ayarlayın:

    - **Personel barkod oturum açma işlemi**: Çalışanlarınızın bir barkod tarayarak POS'ta oturum açmasını istiyorsanız bu seçeneği **Evet** olarak ayarlayın. 
    - **Personelin barkodla oturum açması parola gerektirir**: Çalışanlarınızın bir barkod tarayarak POS'ta oturum açarken bir parola girmelerini istiyorsanız bu seçeneği **Evet** olarak ayarlayın.
    - **Personel kart oturum açma işlemi**: Çalışanlarınızın bir kartı kaydırarak POS'ta oturum açmasını istiyorsanız bu seçeneği **Evet** olarak ayarlayın.
    - **Personelin kartla oturum açması parola gerektirir**: Çalışanlarınızın bir kartı okutarak POS'ta oturum açarken parola girmelerini istiyorsanız bu seçeneği **Evet** olarak ayarlayın.

Barkod veya kart, bir çalışana atanabilecek kimlik bilgileriyle ilişkilendirilir. Kimlik bilgilerinin en az altı karakter olması gerekir. İlk beş karakteri içeren dize benzersiz olmalıdır ve çalışanı aramak için kullanılan bir *kimlik numarası* olarak kabul edilir. Kalan karakterler güvenlik doğrulaması için kullanılır. Örneğin, kimlik bilgileri 12345DGYDEYTDW ve 12345EWUTBDAJH olan iki kartınız var. Bu iki kart aynı kimlik numarasına (12345) sahip olduğundan her ikisi de çalışanlara başarıyla atanamaz.

## <a name="assign-extended-logon"></a>Genişletilmiş oturum açma yeteneği atama

Varsayılan olarak, yalnızca yöneticiler çalışanlara genişletilmiş oturum açma atayabilir. Genişletilmiş oturum atamak için POS içinde **Genişletilmiş oturum açma**'ya gidin. Daha sonra, çalışanın operatör kimliğini arama alanına girerek çalışanı arayın. Çalışanı seçip **Ata** öğesine tıklayın. Bir sonraki sayfada, çalışana atamak için genişletilmiş oturum açma kartını geçirin veya taratın. Kart geçirme veya tarama başarıyla okunursa, **Tamam** düğmesi kullanılabilir olur. O çalışan için genişletilmiş oturum açmayı kaydetmek için **Tamam** düğmesine tıklayın.

## <a name="delete-extended-logon"></a>Genişletilmiş oturum açma yeteneği silme

Bir çalışana atanan genişletilmiş oturum açmayı silmek için, **Genişletilmiş oturum açma** işlemini kullanarak o çalışanı arayın. Çalışanı seçip **Atamayı Kaldır** öğesine tıklayın. Bu çalışan ile ilişkili olan tüm genişletilmiş oturum açma kimlik bilgileri kaldırılır.

## <a name="use-extended-logon"></a>Genişletilmiş oturum açma yeteneğini kullanma

Genişletilmiş oturum açma yapılandırıldıktan ve bir çalışana bir barkod veya manyetik bant atandıktan sonra çalışanın yalnızca POS oturum açma sayfası gösterilirken kartını kaydırması veya taraması gerekir. Oturum açma işlemine devam edebilmesi için ayrıca bir parola gerekiyorsa çalışandan parolasını girmesi istenir.

## <a name="extend-extended-logon"></a>Genişletilmiş oturum açma işlemini genişletme

Genişletilmiş oturum açma yeteneğinin kullanıma hazır uygulaması kimlik bilgilerinin en az altı karakter uzunluğunda olmasını ve ilk beş karakterin (kimlik numarası) benzersiz olmasını gerektirir. Başlangıçta, geliştiricilerin belirli bir uygulamanın gereksinimlerini karşılayabilmeleri için özelleştirebilecekleri bir örnek olarak tasarlanmıştı. (Örneğin, daha fazla karakteri destekleyecek veya farklı güvenlik doğrulama kuralları kullanacak şekilde özelleştirilebilir.) Genişletilmiş oturum açma yeteneğinde uzantıların nasıl oluşturulacağı hakkında ayrıntılı bilgi için bkz. [MPOS ve Bulut POS için Genişletilmiş oturum açma işlevini genişletme](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/).

Oturum açma hizmeti, avuç içi tarayıcılar gibi ek genişletilmiş oturum açma cihazları desteklenecek şekilde de genişletilebilir. Daha fazla bilgi için bkz. [POS genişletilebilirlik belgeleri](dev-itpro/pos-extension/pos-extension-overview.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
