---
title: Operasyonel İçgörüler ayarlama
description: Bu makalede, Operasyonel İçgörüler özelliğinin Microsoft Dynamics 365 Commerce içinde nasıl ayarlanacağı ve kullanılacağı açıklanır.
author: ashishMSFT
ms.date: 12/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: ca0d31e403275d6131fa6d53f0a7b46a7ddb651d
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832144"
---
# <a name="set-up-operational-insights"></a>Operasyonel İçgörüler ayarlama

[!include [banner](../includes/banner.md)]

Bu makalede, Operasyonel İçgörüler özelliğinin Microsoft Dynamics 365 Commerce içinde nasıl ayarlanacağı ve kullanılacağı açıklanır.

Operasyonel İçgörüler, müşterilere müşteri sahipliğindeki Application Insights hesabına doğrudan telemetri göndererek hizmet durumu ve işletme işlevlerine daha iyi görünürlük sağlamak için tasarlanmış bir Dynamics 365 Commerce özelliğidir.

Commerce Headquarters'taki ortamlarınızla ilgili Operasyonel İçgörüler etkinleştirerek, hem Commerce Scale Unit (CSU) hem de satış noktası (POS) cihazlarından alınan olayların bir listesini toplayabilirsiniz. Bu olaylar, sistemlerinizin nasıl çalıştığını daha iyi anlamanıza yardımcı olabilir ve önemli teknik ve iş ölçümlerini izlemenize olanak tanır.

Bu telemetrinin her zaman toplanmasını istemiyor olsanız da, belirli ortamlar için toplamayı hızlıca etkinleştirdiğinizde veya devre dışı bırakacağınız avantajdan yararlanabilirsiniz. Bu şekilde, telemetri geliştirme veya üretim sırasında sorun gidermenize veya hata ayıklamanıza yardımcı olabilir.

## <a name="access-logs-in-application-insights"></a>Application Insights'ta erişim günlükleri

Commerce CSU ve POS bileşenlerinin Application Insights aracılığıyla tanılama olay günlüklerine erişmek için, bu bölümdeki yordamları tamamlayın.

### <a name="minimum-version-requirements-for-csu"></a>CSU için minimum sürüm gereksinimleri

CSU aşağıdaki en düşük sürüm gereksinimlerine sahiptir:

- 10.0.23 (perakende sunucusu sürüm 9.33.22062.15 ve üstü)
- 10.0.24 (perakende sunucusu sürüm 9.34.22062.14 ve üstü)
- 10.0.25 (perakende sunucusu sürüm 9.35.22062.13 ve üstü)
- 10.0.26 ve sonrası (tüm sürümler)

### <a name="enable-diagnostic-events-in-application-insights"></a>Application Insights içinde tanılama olaylarını etkinleştir

> [!IMPORTANT]
> Daha önce Operasyonel İçgörüler'in bir önizleme sürümü kullandıysanız, Operasyonel İçgörüler'i etkinleştirmek için aşağıdaki yordamı kullanmanız gerekir. Böylece, olaylara güvenilir ve güvenli erişim sağlanmasına devam edebilirsiniz.

Commerce Component tanı olaylarını etkinleştirmek için bir Application Insights hesabınız olması gerekir. Mevcut bir hesap kullanabilir veya [yeni bir hesap oluşturabilirsiniz](/azure/azure-monitor/app/create-workspace-resource#create-workspace-based-resource). Veri gizliliği nedenleriyle, üretim, korumalı alan ve geliştirme ortamları için ayrı Application Insights hesaplar kullanmanızı öneririz. Hesap oluşturduktan sonra, genel muhasebedeki **Operasyonel İçgörüler** özelliğini etkinleştirmelisiniz.

Application Insights içinde tanılama olaylarını etkinleştirmek için, aşağıdaki adımları izleyin.

1. Headquarters'ta **Özellik yönetimi** çalışma alanını açın ve **Operasyonel İçgörüler** özelliğini etkinleştirin.
1. **Sistem yönetimi \> Kurulum \> Operasyonel İçgörüler**'e gidin.
1. **Yapılandır** sekmesinde, **Commerce kanal olayları** seçeneğini **Evet** olarak ayarlayın.
1. **Ortamlar** sekmesinde, Application Insights kullanmayı planladığınız her ortam için **LCS ortam kimliği** ve **Ortam modu** değerlerini girin. Her ortamın ortam kimliğini, Microsoft Dynamics Lifecycle Services içinde ortam için **Ortam ayrıntıları** sayfasında bulabilirsiniz. Bu adım, veritabanı kopyalama işlemleri gerçekleştirilirken tanılama olaylarının yanlış bir ortama gönderilmesini engellemeye yardımcı olmak için gereklidir.
1. **Application Insights kayıt defteri** sekmesinde Application Insights **izleme anahtarı** değerini belirleyin ve her Application Insights hesabını kullanmayı planladığınız karşılık gelen **Ortam Modu** değerini girin.
1. Önceki konfigürasyonu tamamladıktan sonra, **CDX Job 1110** işini çalıştırmalısınız. Bu işin kendi zamanlaması üzerinde çalışmasını bekleyebilir veya el ile çalıştırabilirsiniz.
1. Lifecycle Services'ta **Ortam ayrıntıları \> Commerce \> Yönet**'e gidin, CSU örneği seçin ve **Yeniden başlat**'ı seçin. Her CSU için bu adımı yineleyin.
1. Application Insights kullanmayı planladığınız her ortam için önceki adımları yineleyin.

> [!NOTE]
> - Operasyonel İçgörüler'deki telemetri olayları değişebilir. Panolar veya uyarılar tanımlamak için değil, kendi kendinize analiz ve sorun giderme işlemleri yapmak için Operasyonel İçgörüler olaylarını kullanmanızı öneririz. Kendi kendine sorun giderme işlemleri dışında amaçlar için olaylar kullanırsanız, her bir CSU/POS sürümünden sonra sorgularınızı doğrulamanız ve güncelleştirmeniz önerilir.
> - Commerce sürüm 10.0.29 itibariyle, bu bölümdeki yordamlar Application Insights hesabınıza POS Operasyonel İçgörüler olaylarının akışını da etkinleştirir. Daha fazla bilgi için bkz. [POS için Operasyonel İçgörüler - Olaylar ve sorgular](https://download.microsoft.com/download/9/2/b/92be35b0-0e24-4a4d-940d-6f4db29791c0/Operational-Insights-Commerce-POS-events-queries.pdf).

#### <a name="use-the-dllhostexeconfig-file-to-control-pos-operational-insights-events"></a>POS Operasyonel İçgörüler olaylarını denetlemek için DLLHost.exe.config dosyasını kullanın

POS Operasyonel İçgörüler olaylarını denetlemek için DLLHost.exe.config dosyasını kullanmak üzere bu adımları izleyin.

1. Metün düzenleyicisinde, **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker** üzerinde **DLLHost.exe.config** dosyasını açın.
1. **diagnosticsSection** bölümünde **Microsoft.Dynamics.Retail.Diagnostics.OperationalInsights.OperationalInsightsLogger** sınıf adına sahip havuz SML öğesini kaldırın.
1. Dosyayı kaydedin.

### <a name="disable-diagnostic-events-in-application-insights"></a>Application Insights içinde tanılama olaylarını devre dışı bırakın

> [!IMPORTANT]
> Tanılama olaylarını devre dışı bırakmak ve artık bunları Application Insights'a göndermek istiyorsanız, aşağıdaki yordamı tamamlamanız gerekir. Bu özelliği Özellik yönetiminde devre dışı bırakamazsınız.

Application Insights içinde tanılama olaylarını devre dışı bırakmak için, aşağıdaki adımları izleyin.

1. Headquarters'ta **Sistem yönetimi \> Operasyonel İçgörüler**'e gidin.
1. **Yapılandır** sekmesinde, **Commerce kanal olayları** seçeneğini **Hayır** olarak ayarlayın.
1. Önceki konfigürasyonu tamamladıktan sonra, **CDX Job 1110** işini çalıştırmalısınız. Bu işin kendi zamanlaması üzerinde çalışmasını bekleyebilir veya işi el ile çalıştırabilirsiniz.
1. Lifecycle Services'ta **Ortam ayrıntıları \> Commerce \> Yönet**'e gidin, CSU örneği seçin ve **Yeniden başlat**'ı seçin. Her CSU için bu adımı yineleyin.
1. Application Insights devre dışı bırakmayı planladığınız her ortam için önceki adımları yineleyin.

Tek bir ortam için tanılama olaylarını devre dışı bırakmak için **Operasyonel İçgörüler** sayfasının **Application Insights kayıt defteri** sekmesinde izleme anahtarını silin. Daha sonra, yukarıdaki yordamın 3 ve 4 numaralı adımlarını tamamlayın.

> [!NOTE]
> Commerce sürüm 10.0.29 ve sonrasında, bu bölümdeki yordamlar Application Insights hesabınıza POS Operasyonel İçgörüler olaylarının akışını da devre dışı bırakır. 
