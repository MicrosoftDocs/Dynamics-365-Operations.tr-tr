---
title: Human Resouces ile servise alma için hazırlanma
description: Bu sayfa, Dynamics 365 Human Resources ile servise alma hakkında rehberlik sağlar.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 196d843ce3ccacc203896439b8c66f168c75bdc945c9b2cd5f9bdd46a2cc3ddd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744906"
---
# <a name="prepare-for-human-resources-go-live"></a>Human Resouces ile servise alma için hazırlanma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics Lifecycle Services (LCS) kullanarak bir Dynamics 365 Human Resources projesiyle servise almaya nasıl hazırlanılacağını açıklamaktadır. 

Bu grafik, servise alma sürecinin aşamalarını gösterir. 

![Servise alma süreci.](./media/hr-admin-go-live-prepare-process.png)

Aşağıdaki tabloda, süreçteki tüm adımlar, beklenen süre ve eylemden sorumlu olan kişiler listelenmiştir.

| Aşama | Eylem | Süre/Zaman | Kim | Notlar |
| --- | --- | --- | --- |--- |
| 1 | LCS'de servise alma tarihini güncelleştirme | En az 2-3 ay önceden | İş ortağı/müşteri | Aşama tarihleri sürekli olarak güncel tutulmalıdır. |
| 2 | Denetim listesini tamamlama ve gönderme | Kullanıcı kabul sınamaları (UAT) tamamlandıktan sonra | İş ortağı/müşteri | [FastTrack servise alma değerlendirmesinde](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment) sağlanan yönergeleri izleyin. |
| 3 | Proje değerlendirmesi (FastTrack) | FastTrack mimarı* | Mimar denetim listesi alındıktan sonra değerlendirmesini sunar ve sorular netleşinceye ve varsa risk azaltıcı etkenler uygulanıncaya kadar inceleme işlemine devam eder. |
| 4 | Proje Atölyesi (FastTrack) | FastTrack mimarı* | |
| 5 | Veri paketini içe aktarma | Projeye bağlıdır | İş ortağı/müşteri | [Veri yönetimine genel bakış](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md) yönergelerini izleyin.|
| 6 | Üretime hazır | Önceki adımların tümü tamamlandıktan sonra | İş ortağı/müşteri | İş ortağı/müşteri, üretim ortamının kontrolünü alabilir.|
| 7 | Kesin bitiş faaliyetleri | Projeye bağlıdır | İş ortağı/müşteri | |
| 8 | Servise alma | Projeye bağlıdır | Müşteri | |

> [!IMPORTANT]
> * Adım 3 ve 4 yalnızca FastTrack'e uygun müşteriler için tamamlanır.

## <a name="completing-the-lcs-methodology"></a>LCS yöntemini tamamlama

Her uygulama projesindeki önemli aşamalardan biri üretim ortamının kesin bitişidir. Bir adımı tamamlama sürecinde iki bölüm vardır: 

- Sığdırma-boşluk analizi veya Kullanıcı kabul sınaması (UAT) gibi gerçek çalışmayı yapın. 
- İlgili adımı LCS metodolojisinde tamamlandı olarak işaretleyin. 

Uygulamada ilerlerken metodolojide adımları tamamlamak iyi bir harekettir. Son dakikaya kadar beklemeyin. İyi bir uygulamaya sahip olmak, müşterinin yararınadır. 

## <a name="uat-for-your-solution"></a>Çözümünüz için UAT

UAT aşamasında uyguladığınız tüm iş süreçlerini ve yaptığınız tüm özelleştirmeleri uygulama projesindeki bir korumalı alan ortamında sınamanız gerekir. Başarılı bir servise alma deneyimi için, UAT aşamasını tamamlarken aşağıdakileri göz önünde bulundurmalısınız: 

- UAT işleminizin, GOLD yapılandırmanızdaki verilerin UAT işlemi başlamadan önce ortama kopyalandığı temiz ve yeni bir ortamla başlatılmasını öneririz. Yayınlanana ve ortam üretime dönüştürülene kadar üretim ortamını GOLD ortamınız olarak kullanmanızı öneririz.
- Test çalışmaları, tüm gereksinim kapsamını kapsamalıdır. 
- Taşınan verileri kullanarak test edin. Çalışanlar, işler ve pozisyonlar gibi verileri içermelidir. Ayrıca, izin ve devamsızlık tahakkukları gibi açılış bakiyelerini de dahil edin. Son olarak, geçerli kazançlar kayıtları gibi açık işlemleri dahil edin. Veri kümesi son halinde olmasa bile, tüm veri türleriyle sınamayı tamamlayın. 
- Kullanıcılara atanan doğru güvenlik rollerini (varsayılan roller ve özel roller) kullanarak test edin. 
- Çözümün şirket ve sektörlere özgü düzenleme gereksinimleriyle uyumlu olduğundan emin olun. 
- Tüm özellikleri belgeleyin ve müşterinin onayını alın. 

## <a name="mock-go-live"></a>Sahte yayınlama

Yayınlama işleminden önce, eski sistemlerinizden yeni sisteme geçiş için gereken adımları test etmek üzere sahte bir yayınlama işlemi gerçekleştirmeniz gerekir. Sahte yayınlama işleminizi korumalı alan ortamında gerçekleştirmeli ve tüm adımları kesin bitiş planınıza dahil etmelisiniz.

- Yayınlamaya kadar üretim ortamını GOLD yapılandırma ortamı olarak kullanmanızı öneririz.
- Üretim ortamını yayınlamadan önce yanlışlıkla yapılan işlemlerden veya güncelleştirmelerden korumak için güçlü bir yönetim sürecine sahip olduğundan emin olun.
- UAT veya sahte yayınlama işlemi gerçekleştirmeye hazır olduğunuzda, korumalı alan ortamını üretim ortamından yenileyin. Daha fazla bilgi için bkz. [Kurulum kopyalama](hr-admin-setup-copy-instance.md).
- Kesin bitiş planınızın her adımını korumalı alan ortamında sınayın ve ardından ortamdaki UAT komut dosyalarınızdan nokta denetimleri veya testler gerçekleştirerek korumalı alan ortamını doğrulayın.
  - Testler, yayınlama işlemi için gereken dönüşümler de dahil olmak üzere tüm veri geçişlerini içermelidir.
  - İşlem, herhangi bir eski sistemin uygulama kesin bitişini içermelidir.
  - Sahte kesin bitişteki tümleştirme kesme adımlarını veya harici sistem adımlarını ekleyin.
- Sahte kesin bitiş sırasında herhangi bir sorun bulursanız ikinci bir sahte kesin bitiş gerekebilir. Bu nedenle, proje planınızda iki sahte kesin bitiş planlamanızı öneririz.

## <a name="fasttrack-go-live-assessment"></a>FastTrack servise alma değerlendirmesi

FastTrack için uygun olan ve bir FastTrack çözümü mimarı ile çalışan müşteriler Microsoft FastTrack ile servise alma incelemesi tamamlayacaktır. Daha fazla bilgi için bkz.  [Microsoft FastTrack](/dynamics365/fasttrack/). 

Servise almadan yaklaşık sekiz hafta önce, FastTrack ekibi, bir [servise alma denetim listesi](https://go.microsoft.com/fwlink/?linkid=2146013) doldurmanızı isteyecektir.

Proje Yöneticisi veya yetkili bir proje üyesi projenin servise alma öncesi aşamasındayken servise alma denetim listesini tamamlamalıdır. Genel olarak, denetim listesi, UAT tamamlandığında veya neredeyse tamamlandığında, önerilen servise alma tarihinden dört ile altı hafta önce tamamlanır. 

Servise alma denetim listesini tamamladığınızda, bunu FastTrack çözüm mimarınıza e-posta ile gönderin. Müşteriden yetkili bir paydaşı ve uygulama ortağını e-postaya her zaman dahil edin. 

Denetim listesini gönderdikten sonra, FastTrack çözüm mimarı projeyi inceler ve projenin başarılı bir şekilde servise alınması için olası riskleri, en iyi yöntemleri ve önerileri tanımlayan bir değerlendirme sağlar. Bazı durumlarda, çözüm mimarı risk faktörlerini vurgulayabilir ve risk azaltma planı isteyebilir. 

## <a name="see-also"></a>Ayrıca bkz.

[Servise almayla ilgili SSS](hr-admin-go-live-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
