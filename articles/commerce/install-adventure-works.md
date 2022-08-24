---
title: Adventure Works temasını yükleme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te Adventure Works temasının nasıl yükleneceği açıklanmaktadır.
author: anupamar-ms
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: f5c195694633c96a473f0f824c1f182903082bff
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274299"
---
# <a name="install-the-adventure-works-theme"></a>Adventure Works temasını yükleme

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te Adventure Works temasının nasıl yükleneceği açıklanmaktadır. 

> [!IMPORTANT]
> Adventure Works teması ve modülleri Dynamics 365 Commerce 10.0.20 sürümü itibarıyla kullanılabilir. Microsoft AppSource'tan edinilebilir.

## <a name="prerequisites"></a>Önkoşullar

Adventure Works temasını yüklemeden önce, Retail Cloud Scale Unit (RCSU), Commerce çevrimiçi yazılım geliştirme kiti (SDK) ve Commerce modül kitaplığını içeren bir Dynamics 365 Commerce ortamınız (Commerce sürüm 10.0.20 veya üstü) olmalıdır. Commerce SDK'sı ve modül kitaplığını yükleme hakkında bilgi için bkz. [Geliştirme ortamı oluşturma](e-commerce-extensibility/setup-dev-environment.md). 

## <a name="installation-steps"></a>Yükleme adımları

### <a name="install-the-adventure-works-theme-in-your-application"></a>Adventure Works temasını uygulamanıza yükleme

Adventure Works tema paketi **dynamics365-commerce** akışında, **@msdyn365-commerce-theme/adventureworks-theme-kit** olarak mevcuttur. Ancak, Adventure Works tema paketi bu akışın bir parçası olsa da farklı bir ad alanı altındadır. Bu nedenle, ad alanına kayıt defteri girdileri eklemek için bu adımları izlemelisiniz.

1. **.npmrc** dosyasını aşağıdaki kayıt defteri girdisini içerecek şekilde güncelleştirin (girdi zaten dahil değilse):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. **.yarnrc** dosyasını aşağıdaki kayıt defteri girdisini içerecek şekilde güncelleştirin (girdi zaten dahil değilse):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Paketi yerel ortamınıza yüklemek için komut isteminden `yarn add THEME_PACKAGE@VERSION` komutunu çalıştırın; burada **THEME_PACKAGE** tema paketi (@msdyn365-commerce-theme/adventureworks-theme-kit) ve **VERSION** kullanılmakta olan modül kitaplığının sürüm numarasıdır. Tema paketinin sürümleri ile modül kitaplığının eşleşmesi önemlidir. Kullanılacak doğru modül kitaplığı sürüm numarasını bulmak için package.json dosyasını açın ve **bağımlılıklar** bölümünün altında **başlangıç paketi** değerini bulun. Aşağıdaki örnekte, package.json dosyası modül kitaplığının Dynamics 365 Commerce 10.0.22 sürümüyle eşlenen 9.32 sürümünü kullanır.  

```json
"dependencies": {
    "@msdyn365-commerce-modules/starter-pack": "9.32",
}
```

Aşağıdaki örnek, Adventure Works temasının 9.32 sürümünü eklemek için `yarn add` komutunun nasıl çalıştırılacağını gösterir. Komut, package.json dosyasını bağımlılığı içermesi için otomatik olarak güncelleştirir.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit@9.32`

Modül kitaplığı sürümünü güncelleştirme hakkında daha fazla bilgi için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md). 

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
