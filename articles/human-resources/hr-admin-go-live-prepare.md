---
title: Human Resouces ile servise alma için hazırlanma
description: Bu sayfa, Dynamics 365 Human Resources ile servise alma hakkında rehberlik sağlar.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59d7274c3b40e78209d90960c4514321b736876a
ms.sourcegitcommit: d66fd72342931fad25a696b251c05781280d36c4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/14/2020
ms.locfileid: "4011443"
---
# <a name="prepare-for-human-resources-go-live"></a>Human Resouces ile servise alma için hazırlanma

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics Lifecycle Services (LCS) kullanarak bir Dynamics 365 Human Resources projesiyle servise almaya nasıl hazırlanılacağını açıklamaktadır. 

Bu grafik, servise alma sürecinin aşamalarını gösterir. 

![Servise alma süreci](./media/hr-admin-go-live-prepare-process.png)

Aşağıdaki tabloda, süreçteki tüm adımlar, beklenen süre ve eylemden sorumlu olan kişiler listelenmiştir.

| Aşama | Eylem | Süre/Zaman | Kim | Notlar |
| --- | --- | --- | --- |--- |
| 1 | LCS'de servise alma tarihini güncelleştirme | En az 2-3 ay önceden | İş ortağı/müşteri | Aşama tarihleri sürekli olarak güncel tutulmalıdır. |
| 2 | Denetim listesini tamamlama ve gönderme | Kullanıcı kabul sınamaları (UAT) tamamlandıktan sonra | İş ortağı/müşteri | [FastTrack servise alma değerlendirmesinde](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment) sağlanan yönergeleri izleyin. |
| 3 | Proje değerlendirmesi (FastTrack) | FastTrack mimarı* | Mimar denetim listesi alındıktan sonra değerlendirmesini sunar ve sorular netleşinceye ve varsa risk azaltıcı etkenler uygulanıncaya kadar inceleme işlemine devam eder. |
| 4 | Proje Atölyesi (FastTrack) | FastTrack mimarı* | |
| 5 | Veri paketini içe aktarma | Projeye bağlıdır | İş ortağı/müşteri | [Veri yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages) yönergelerini izleyin.|
| 6 | Üretime hazır | Önceki adımların tümü tamamlandıktan sonra | İş ortağı/müşteri | İş ortağı/müşteri, üretim ortamının kontrolünü alabilir.|
| 7 | Kesin bitiş faaliyetleri | Projeye bağlıdır | İş ortağı/müşteri | |
| 8 | Servise alma | Projeye bağlıdır | Müşteri | |

> [!IMPORTANT]
> * Adım 3 ve 4 yalnızca FastTrack'e uygun müşteriler için tamamlanır.

## <a name="completing-the-lcs-methodology"></a>LCS yöntemini tamamlama

Her uygulama projesindeki önemli aşamalardan biri üretim ortamının kesin bitişidir. 

Üretim ortamının canlı operasyonlar için kullanılmasını sağlamaya yardımcı olmak amacıyla, Microsoft, LCS yöntemlerindeki gerekli faaliyetler tamamlandıktan sonra, yalnızca uygulama **çalışma** aşamasına yaklaştığında üretim örneğini sağlar. Aboneliğinizdeki ortamlar hakkında daha fazla bilgi için,  [Dynamics 365 Lisans Kılavuzu](https://go.microsoft.com/fwlink/?LinkId=866544)'na bakın. 

Üretim ortamını istemek için kullanılan  **Yapılandır** düğmesinin kullanılabilmesi için, müşteriler LCS metodolojisinde **analiz** , **tasarım ve geliştirme** ve **test** aşamalarını tamamlamalıdır. LCS'de bir aşamayı tamamlamak için, öncelikle bu aşamada gereken her adımı tamamlamalısınız. Bir aşamadaki tüm adımlar tamamlandığında, tüm aşamayı tamamlayabilirsiniz. Daha sonra değişiklik yapmanız gerekiyorsa, bir aşamayı istediğiniz zaman yeniden açabilirsiniz. Daha fazla bilgi için bkz.  [Finance and Operations uygulamaları müşterileri için Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs). 

Bir adımı tamamlama sürecinde iki bölüm vardır: 

- Sığdırma-boşluk analizi veya Kullanıcı kabul sınaması (UAT) gibi gerçek çalışmayı yapın. 
- İlgili adımı LCS metodolojisinde tamamlandı olarak işaretleyin. 

Uygulamada ilerlerken metodolojide adımları tamamlamak iyi bir harekettir. Son dakikaya kadar beklemeyin. Üretim ortamını alabilmeniz için tüm adımları tıklatıp geçmeyin. İyi bir uygulamaya sahip olmak, müşterinin yararınadır. 

## <a name="uat-for-your-solution"></a>Çözümünüz için UAT

UAT aşamasında uyguladığınız tüm iş süreçlerini ve yaptığınız tüm özelleştirmeleri uygulama projesindeki bir korumalı alan ortamında sınamanız gerekir. Başarılı bir servise alma deneyimi için, UAT aşamasını tamamlarken aşağıdakileri göz önünde bulundurmalısınız: 

- Test çalışmaları, tüm gereksinim kapsamını kapsamalıdır. 
- Taşınan verileri kullanarak test edin. Bu veriler çalışanlar, işler ve pozisyonlar gibi ana verileri içermelidir. Ayrıca, izin ve devamsızlık tahakkukları gibi açılış bakiyelerini de dahil edin. Son olarak, geçerli kazançlar kayıtları gibi açık işlemleri dahil edin. Veri kümesi son halinde olmasa bile, tüm veri türleriyle sınamayı tamamlayın. 
- Kullanıcılara atanan doğru güvenlik rollerini (varsayılan roller ve özel roller) kullanarak test edin. 
- Çözümün şirket ve sektörlere özgü düzenleme gereksinimleriyle uyumlu olduğundan emin olun. 
- Tüm özellikleri belgeleyin ve müşterinin onayını alın. 

## <a name="fasttrack-go-live-assessment"></a>FastTrack servise alma değerlendirmesi

FastTrack için uygun olan ve bir FastTrack çözümü mimarı ile çalışan müşteriler Microsoft FastTrack ile servise alma incelemesi tamamlayacaktır. Daha fazla bilgi için bkz.  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). 

Servise almadan yaklaşık sekiz hafta önce, FastTrack ekibi, bir [servise alma denetim listesi](https://go.microsoft.com/fwlink/?linkid=2146013) doldurmanızı isteyecektir.

Proje Yöneticisi veya yetkili bir proje üyesi projenin servise alma öncesi aşamasındayken servise alma denetim listesini tamamlamalıdır. Genel olarak, denetim listesi, UAT tamamlandığında veya neredeyse tamamlandığında, önerilen servise alma tarihinden dört ile altı hafta önce tamamlanır. 

Servise alma denetim listesini tamamladığınızda, bunu FastTrack çözüm mimarınıza e-posta ile gönderin. Müşteriden yetkili bir paydaşı ve uygulama ortağını e-postaya her zaman dahil edin. 

Denetim listesini gönderdikten sonra, FastTrack çözüm mimarı projeyi inceler ve projenin başarılı bir şekilde servise alınması için olası riskleri, en iyi yöntemleri ve önerileri tanımlayan bir değerlendirme sağlar. Bazı durumlarda, çözüm mimarı risk faktörlerini vurgulayabilir ve risk azaltma planı isteyebilir. 

## <a name="see-also"></a>Ayrıca bkz.

[Servise almayla ilgili SSS](hr-admin-go-live-faq.md)