---
title: Dynamics 365 Commerce'te deneme
description: Deneme, site oluşturucuda sayfa düzeni ve içerik işlemleri oluşturma, düzenleme ve yönetmeyi sağlar. Uçtan uca deneme desteği e-ticaret sayfaları ve bir sayfadaki varlıklar için sağlanır.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 85eb7a661cc66c42699797cca4fa6820941de7c0
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "4416565"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Dynamics 365 Commerce'te deneme
Dynamics 365 Commerce'te denemeyi E-ticaret sayfalarınızın verimliliği hakkındaki varsayımları doğrulamak ve verilere dayalı güvenilirlikle kararlar vermek için kullanın. Commerce, sayfalar, modüller ve parçalar üzerinde A/B testi gerçekleştirme desteği sunar ve web sitenizde önerilen değişikliklerin etkisini ölçmenize olanak tanır.

Commerce sitesi oluşturucuda **varyasyonlar** olarak bilinen sayfa ve içerik işlemlerini oluşturabilir, bunları düzenleyebilir ve yönetebilirsiniz. Commerce, denemeler ve işlem atamaları oluşturmak için kullanabileceğiniz üçüncü taraf hizmetlerle tümleşir. Commerce'ta yakalanan gerçek zamanlı olay akışları, üçüncü taraf hizmetindeki deneme sonuçlarını tanımlayan analizleri etkinleştirir. Daha sonra bu analizlerden, varsayımınızı desteklemek veya çürütmek için yararlanabilirsiniz.

## <a name="set-up-prerequisites"></a>Önkoşulları ayarlama
1. **Doğru Commerce sürümünü edinin** - Modül kitaplığınızı, çevrimiçi kanal genişletilebilirlik yazılım geliştirme kitini (SDK) ve Commerce Scale Unit'i Commerce sürüm 10.0.13 veya sonrasına yükseltin.
1. **Deneme bağlayıcısı ayarlayın** - Deneme bağlayıcısı, Commerce'ın denemelerin listesini almak ve bir denemenin kullanıcıya ne zaman gösterileceğini belirlemek için üçüncü taraf hizmetlerle bağlantı kurmasına olanak tanır. Üçüncü taraf bir bağlayıcıyı [AppSource](https://appsource.microsoft.com)'tan satın alabilirsiniz. Yayımcının sağladığı kurulum yönergelerini uygulayın. Alternatif olarak deneme iş akışını bir harici servis yapılandırmaya gerek kalmadan test etmek için Commerce'taki örnek test bağlayıcısını kullanabilirsiniz. Daha fazla bilgi için, bkz. [Bağlayıcıları yapılandırma ve etkinleştirme](e-commerce-extensibility/connectors.md). 
1. **Commerce'ta deneme özelliği bayraklarını açın** - **Site ayarları > Özellikler**'de site düzeyinde veya **Kiracı Ayarları > Özellikler**'e giderek kiracı düzeyinde deneme etkinleştirebilirsiniz.
    - Denemenin parçası olmayan başka içeriği etkilemeden veya kopyalamadan, bir sayfa içindeki modüllerin varyasyonlarını oluşturmak için **Deneme** bayrağını etkinleştirin. Bu, denemeler dışında kalan içerik güncelleştirmelerinin deneme yaşam döngüsü sırasında eşitlenmiş olarak kalmasını sağlar. Bu bayrağın devre dışı bırakılması tüm denemelerin kullanıcılara gösterilmesini durdurur ve site oluşturucu içindeki tüm düzenleme işlevlerini kaldırır.
    - Sayfa veya parça üzerinde denemeler çalıştırmak için **Sayfalar veya parçalarda deneme** bayrağını etkinleştirin. Bu, sayfa veya parçadaki tüm modüller için tüm sayfa veya parçanın tam örnek kopyasını oluşturur. Bu modu, kapsamlı içerik değişikliklerini test etmek istediğinizde veya örnekler arasında devam eden içerik değişikliklerinin eşitlenmesi bir sorun olmadığında kullanın. Bu bayrağın devre dışı bırakılması, sayfalar ve parçalar üzerinde yeni denemeler oluşturulmasını ve düzenlenmesini engeller.
    > [!NOTE]
    > **Sayfalar veya parçalarda deneme** işlevinin çalışması için **Deneme** bayrağının etkinleştirilmiş olması gerekir.
    
## <a name="experimentation-lifecycle"></a>Deneme yaşam döngüsü
Deneme ayarlama, varyasyonlar oluşturma ve deneme çalıştırma yinelemeli bir işlemdir. Aşağıdaki diyagram Commerce ve üçüncü taraf hizmetindeki deneme yaşam döngüsünü göstermektedir. 

[ ![Deneme yaşam döngüsü](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Deneme işlemindeki her adım hakkında daha fazla bilgi için aşağıdaki konulara bakın.
- [Varsayım tanımlama ve deneme için ölçümleri belirleme](experimentation-identify.md)
- [Deneme ayarlama](experimentation-setup.md)
- [Deneme bağlama ve düzenleme](experimentation-connect-edit.md)
- [Deneme önizleme ve yayımlama](experimentation-preview-publish.md)
- [Deneme çalıştırma ve izleme](experimentation-run-monitor.md)
- [Çeşit yükseltme ve deneme tamamlama](experimentation-review-complete.md)

> [!NOTE]
> Bir denemenin yaşam döngüsü içinde nerede olduğunu öğrenmek için site oluşurucunun sol gezinme bölümündeki **Denemeler**'i seçin. Hem Commerce hem de üçüncü taraf hizmetindeki her denemeyle ilgili durum ile birlikte Denemelerin listesi görüntülenir. Daha fazla bilgi için, bkz. [Bir denemenin durumunu inceleme](experimentation-status.md).

## <a name="next-step"></a>Sonraki adım
[Varsayım tanımlama ve deneme için başarı ölçümleri belirleme](experimentation-identify.md) 
