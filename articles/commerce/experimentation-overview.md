---
title: Dynamics 365 Commerce'te deneme
description: Deneme, site oluşturucuda sayfa düzeni ve içerik işlemleri oluşturma, düzenleme ve yönetmeyi sağlar. Uçtan uca deneme desteği e-ticaret sayfaları ve bir sayfadaki varlıklar için sağlanır.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: overview
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1ef877072ba7ffe1b0326cf8d526b512b5ab30b8
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946226"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Dynamics 365 Commerce'te deneme
Dynamics 365 Commerce'te denemeyi E-ticaret sayfalarınızın verimliliği hakkındaki varsayımları doğrulamak ve verilere dayalı güvenilirlikle kararlar vermek için kullanın. Commerce, sayfalar, modüller ve parçalar üzerinde A/B testi gerçekleştirme desteği sunar ve web sitenizde önerilen değişikliklerin etkisini ölçmenize olanak tanır.

Commerce sitesi oluşturucuda **varyasyonlar** olarak bilinen sayfa ve içerik işlemlerini oluşturabilir, bunları düzenleyebilir ve yönetebilirsiniz. Commerce, denemeler ve işlem atamaları oluşturmak için kullanabileceğiniz üçüncü taraf hizmetlerle tümleşir. Commerce'ta yakalanan gerçek zamanlı olay akışları, üçüncü taraf hizmetindeki deneme sonuçlarını tanımlayan analizleri etkinleştirir. Daha sonra bu analizlerden, varsayımınızı desteklemek veya çürütmek için yararlanabilirsiniz.

## <a name="set-up-prerequisites"></a>Önkoşulları ayarlama

1. **Doğru Commerce sürümünü edinin** - Modül kitaplığınızı, çevrimiçi kanal genişletilebilirlik yazılım geliştirme kitini (SDK) ve Commerce Scale Unit'i Commerce sürüm 10.0.13 veya sonrasına yükseltin.
1. **Deneme bağlayıcısı ayarlayın** - Deneme bağlayıcısı, Commerce'ın denemelerin listesini almak ve bir denemenin kullanıcıya ne zaman gösterileceğini belirlemek için üçüncü taraf hizmetlerle bağlantı kurmasına olanak tanır. Üçüncü taraf bir bağlayıcıyı [AppSource](https://appsource.microsoft.com)'tan satın alabilirsiniz. Yayımcının sağladığı kurulum yönergelerini uygulayın. Alternatif olarak deneme iş akışını bir harici servis yapılandırmaya gerek kalmadan test etmek için Commerce'taki örnek test bağlayıcısını kullanabilirsiniz. Daha fazla bilgi için, bkz. [Bağlayıcıları yapılandırma ve etkinleştirme](e-commerce-extensibility/connectors.md). 
1. **Commerce'ta deneme özelliği bayrağını açma** - **Site ayarları \> Özellikler**'de site düzeyinde veya **Kiracı Ayarları \> Özellikler**'e giderek kiracı düzeyinde deneme etkinleştirebilirsiniz. Modül varyasyonlarını oluşturmaya başlamak için **Deneme** bayrağını açın. Bu bayrağın devre dışı bırakılması tüm denemelerin kullanıcılara gösterilmesini durdurur ve site oluşturucu içindeki tüm düzenleme işlevlerini kaldırır.
    
## <a name="experimentation-lifecycle"></a>Deneme yaşam döngüsü

Deneme ayarlama, varyasyonlar oluşturma ve deneme çalıştırma yinelemeli bir işlemdir. Aşağıdaki diyagram Commerce ve üçüncü taraf hizmetindeki deneme yaşam döngüsünü göstermektedir. 

[ ![Deneme yaşam döngüsü.](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Deneme işlemindeki her adım hakkında daha fazla bilgi için aşağıdaki makalelere bakın.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
