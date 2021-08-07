---
title: Adventure Works temasını yükleme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te Adventure Works temasının nasıl yükleneceği açıklanmaktadır.
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9c94dd8ead32f58a25a396376840101d9c2c9b08
ms.sourcegitcommit: 0c77dbb8547cd36fce3977ca9515fa1474efa77a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/22/2021
ms.locfileid: "6655860"
---
# <a name="install-the-adventure-works-theme"></a>Adventure Works temasını yükleme

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te Adventure Works temasının nasıl yükleneceği açıklanmaktadır. 

> [!IMPORTANT]
> Adventure Works teması ve modülleri Dynamics 365 Commerce 10.0.20 sürümü itibarıyla kullanılabilir. Microsoft AppSource'tan edinilebilir.

## <a name="prerequisites"></a>Önkoşullar

Adventure Works temasını yüklemeden önce, Retail Cloud Scale Unit (RCSU), Commerce çevrimiçi yazılım geliştirme kiti (SDK) ve Commerce modül kitaplığını içeren bir Dynamics 365 Commerce ortamınız (Commerce sürüm 10.0.20 veya üstü) olmalıdır. Commerce SDK ve modül kitaplığını yükleme hakkında bilgi için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md). 

## <a name="installation-steps"></a>Yükleme adımları

### <a name="install-the-adventure-works-theme-in-your-application"></a>Adventure Works temasını uygulamanıza yükleme

Adventure Works tema paketi **dynamics365-commerce** akışında, **@msdyn365-commerce-theme/adventureworks-theme-kit** olarak mevcuttur. Ancak, Adventure Works tema paketi bu akışın bir parçası olsa da farklı bir ad alanı altındadır. Bu nedenle, ad alanına kayıt defteri girdileri eklemek için bu adımları izlemelisiniz.

1. **.npmrc** dosyasını aşağıdaki kayıt defteri girdisini içerecek şekilde güncelleştirin (girdi zaten dahil değilse):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. **.yarnrc** dosyasını aşağıdaki kayıt defteri girdisini içerecek şekilde güncelleştirin (girdi zaten dahil değilse):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Paketi yerel ortamınıza yüklemek için komut isteminden aşağıdaki komutu çalıştırın. Bu komut, package.json dosyasını bağımlılığı içerebilecek şekilde otomatik olarak güncelleştirir.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit`

**package.json** dosyasında, tema sürümünü belirli bir sürüme güncelleştirmeniz gerekir.

> [!IMPORTANT]
> - Tema sürümü, tüm özelliklerin beklendiği gibi çalıştığından emin olmak için modül kitaplığı sürümüyle eşleşmelidir. 
> - Commerce modül kitaplığı ve SDK için minimum sürüm 10.0.20 (9.31) olmalıdır. 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>Adventure Works teması için yazı tipi dosyalarını ekleme

Adventure Works teması uygulamanıza yüklendikten sonra, bunun için gereken yazı tipi dosyalarını eklemeniz gerekir. Bu adımı tamamlamak için **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** konumundaki tüm yazı tipi dosyalarını iş ortağı uygulama ortak dizin yolu olan **\public\webfonts**'a kopyalayın.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>Adventure Works teması için kaynakları ayarlama

Bir sonraki adım, tema için gerekli varsayılan kaynağı güncelleştirmektir. Bu adımı tamamlamak için **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** altındaki global.json dosyasındaki içeriği **\src\resources\modules** altındaki ortak uygulama global.json dosyasına kopyalayın. **\src\resources** hedef dizini yoksa **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** kaynak dizininden **\src** hedef dizinine bütünüyle kopyalanabilir.

### <a name="pull-updates-and-validate-the-theme"></a>Güncelleştirmeleri çekme ve temayı doğrulama

En son SDK, modül kitaplığı ve diğer bağımlılık güncelleştirmelerini çekme hakkında bilgi için [SDK ve modül kitaplığı güncelleştirmelerinin](e-commerce-extensibility/sdk-updates.md#pull-updates) başlığının "Güncelleştirmeleri çekme" bölümüne bakın.

En son bağımlılıklar çekildikten sonra, geliştirme ortamınızda Düğüm sunucusunu başlatmak ve yeni Adventure Works temasını test etmek için **yarn start** komutunu çalıştırabilirsiniz. `?theme=adventureworks` sorgu dizesi parametresini kullanarak uygulamaya yerel olarak (örneğin, `https://localhost:4000/?theme=adventureworks`) göz atın.

## <a name="additional-resources"></a>Ek kaynaklar

[Adventure Works teması](adventure-works-theme.md)

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
