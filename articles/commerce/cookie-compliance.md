---
title: Çerez uyumluluğu
description: Bu konu, tanımlama bilgisi uyumu ve Microsoft Dynamics 365 Commerce'in içerdiği varsayılan ilkelerin dikkate alınması konularını açıklamaktadır.
author: BrianShook
ms.date: 05/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8eb610eb819dee09a30368257e36dc88f855e985
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2021
ms.locfileid: "6088399"
---
# <a name="cookie-compliance"></a>Çerez uyumluluğu

[!include [banner](includes/banner.md)]

Bu konu, tanımlama bilgisi uyumu ve Microsoft Dynamics 365 Commerce'in içerdiği varsayılan ilkelerin dikkate alınması konularını açıklamaktadır.

E-ticaret müşterilerini etkileyen izleme teknolojileri kullanıldığında, gizlilik önemli bir etkendir. Avrupa Birliği (AB) içindeki genel veri koruma düzenlemesi (GDPR) gibi gizlilik uyumluluk standartları nedeniyle, günümüzde etkin olan tüm siteler için elektronik gizlilik yönergeleri dikkate alınmalıdır. Birçok e-ticaret sitesine varsayılan olarak genel erişim sağlandığından, e-ticaret sitenizin uyumluluk standartlarını incelemeniz önemlidir.

Microsoft'un çerez uyumluluğu için kullandığı temel ilkeler hakkında daha fazla bilgi için [Microsoft Güven Merkezi](https://www.microsoft.com/trust-center)'ni ziyaret edin. Aynı zamanda, uyumluluk ve gizlilik alanları hakkında daha fazla bilgi edinebilirsiniz.

Aşağıdaki tabloda, Dynamics 365 Commerce siteleri tarafından yerleştirilen tanımlama bilgilerine ilişkin geçerli başvuru listesi gösterilmektedir.

| Tanımlama bilgisi adı                               | Kullanım                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Cookies                             | Çoklu oturum açma (SSO) için Microsoft Azure Active Directory (Azure AD) kimlik doğrulama bilgilerini depolar. Şifreli kullanıcı asıl bilgisini depolar (adı, soyadı, eposta). |
| &#95;msdyn365___cart&#95;                           | Sepet örneğine eklenen ürünlerin listesini almak için kullanılan alışveriş sepeti kodunu depolar. |
| &#95;msdyn365___ucc&#95;                            | Tanımlama bilgisi uyumluluk onayı izleme.                          |
| ai_session                                  | Uygulamanın belirli sayfalarını ve özelliklerini içeren kaç kullanıcı etkinliği oturumu olduğunu saptar. |
| ai_user                                     | Uygulamayı ve özelliklerini kaç kişinin kullanmış olduğunu saptar. Kullanıcılar anonim kimlikler kullanılarak sayılır. |
| b2cru                                       | Yeniden yönlendirme URL'sini dinamik olarak depolar.                              |
| JSESSIONID                                  | Adyen ödeme bağlayıcısı tarafından kullanıcı oturumunu depolamak için kullanılır.       |
| OpenIdConnect.nonce.&#42;                       | Kimlik Doğrulama                                               |
| x-ms-cpim-cache:.&#42;                          | İstek durumunu korumak için kullanılır.                      |
| x-ms-cpim-csrf                              | CRSF koruması için kullanılan siteler arası istek sahteciliği (CRSF) belirteci.     |
| x-ms-cpim-dc                                | İstekleri uygun üretim kimlik doğrulama sunucusu örneğine yönlendirmek için kullanılır. |
| x-ms-cpim-rc.&#42;                              | İstekleri uygun üretim kimlik doğrulama sunucusu örneğine yönlendirmek için kullanılır. |
| x-ms-cpim-slice                             | İstekleri uygun üretim kimlik doğrulama sunucusu örneğine yönlendirmek için kullanılır. |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | SSO oturumunu sürdürmek için kullanılır.                        |
| x-ms-cpim-trans                             | Geçerli hareket dahil olmak üzere hareketleri izlemek için kullanılır (işletme tüketici arası (B2C) sitede kimlik doğrulaması yapan açık sekme sayısı). |
| \_msdyn365___muid_                            | Ortam için Deneme etkinleştirilirse kullanılır; deneme amacıyla userId olarak kullanılır. |
| \_msdyn365___exp_                             | Ortam için Deneme etkinleştirilirse kullanılır; performans yük dengelemesini ölçmek için kullanılır.         |
| d365mkt                                       | Mağaza konumu önerileri için kullanıcının IP adresini izlemek üzere konum tabanlı algılama, **Site Ayarları> Genel > Konum tabanlı mağaza algılamayı etkinleştir**'deki Commerce site oluşturucusunda etkinleştirilmişse kullanın.      |

Site kullanıcısı bir sitedeki herhangi bir sosyal medya bağlantısını seçerse, aşağıdaki tabloda yer alan tanımlama bilgileri de tarayıcılarında izlenir.


| Etki alanı                      | Tanımlama bilgisi               | Tanım                                                  | Kaynak                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | LinkedIn Ads Kimliği eşitleme                                      | LinkedIn Akış ve İçgörü etiketi                                |
| .linkedin.com               | li_sugr                  | Tarayıcı tanımlayıcısı                                           | IP adresi belirlenmiş bir ülkede değilse LinkedIn İçgörü etiketi |
| .linkedin.com               | BizographicsOptOut       | Üçüncü taraf izleme için geri çevirme durumunu belirler.              | LinkedIn konuk denetimleri ve sektör geri çevirme sayfaları           |
| .linkedin.com               | \_guid                    | Google Ads için tarayıcı tanımlayıcısı.                            | LinkedIn Akışı                                                |
| .linkedin.com               | li_oatml                 | Dönüştürme izlemesi, yeniden hedefleme ve analiz için üye dolaylı tanımlayıcısı. | LinkedIn Reklamlar ve İçgörü etiketi                                |
| Çeşitli birinci taraf etki alanı | li_fat_id                | Dönüştürme izlemesi, yeniden hedefleme ve analiz için üye dolaylı tanımlayıcısı. | LinkedIn Reklamlar ve İçgörü etiketi                                |
| .adsymptotic.com            | U                        | Tarayıcı tanımlayıcısı                                           | IP adresi Belirlenmiş Ülkede değilse LinkedIn İçgörü etiketi |
| .linkedin.com                | bcookie                  | Tarayıcı kimliği tanımlama bilgisi                                            | LinkedIn İstekleri                                         |
| .linkedin.com                | bscookie                 | Güvenli tarayıcı tanımlama bilgisi                                        | LinkedIn İstekleri                                         |
| .linkedin.com               | lang                     | Varsayılan yerel ayarı ve dili ayarlar.                                 | LinkedIn İstekleri                                         |
| .linkedin.com                | lidc                     | Yönlendirme için kullanılır.                                             | LinkedIn İstekleri                                         |
| .linkedin.com               | aam_uuid                 | Adobe hedef kitle yöneticisi tanımlama bilgisi                                                     | Kimlik eşitleme için ayar                                              |
| .linkedin.com               | \_ga                      | Google Analytics tanımlama bilgisi                                            | Google Analytics                                             |
| .linkedin.com               | \_gat                     | Google Analytics tanımlama bilgisi                                             | Google Analytics                                             |
| .linkedin.com               | liap                     | Google Analytics tanımlama bilgisi                                             | Google Analytics                                             |
| .linkedin.com               | lissc                    |                                                              |                                                              |
| .facebook.com               | c_user                   | Tanımlama bilgisi, oturum açmış geçerli kullanıcının kullanıcı kimliğini içerir.  |   Facebook                                                           |
| .facebook.com               | datr                     | Oturum açan kullanıcıdan bağımsız olarak Facebook'a bağlanmak için kullanılan web tarayıcısını tanımlamak için kullanılır. | Facebook                                                             |
| .facebook.com               | wd                       | Tarayıcı penceresinin boyutlarını depolar ve Facebook tarafından sayfa işlemeyi en iyi duruma getirmek için kullanılır. | Facebook                                                             |
| .facebook.com               | xs                       | Oturum numarasını gösteren iki basamaklı sayı. Değerin ikinci bölümü bir oturum gizli anahtarıdır. |  Facebook                                                            |
| .facebook.com               | fr                       | Hedeflenen reklam için kullanılan benzersiz tarayıcı ve kullanıcı kimliğini içerir. |  Facebook                                                            |
| .facebook.com               | sb                       | Facebook arkadaş önerilerini geliştirmek için kullanılır.                                |  Facebook                                                            |
| .facebook.com               | spin                     |                                                              |  Facebook                                                            |
| .twitter.com                | guest_id                 |                                                              |  Twitter                                                            |
| .twitter.com                | kdt                      |                                                              |  Twitter                                                             |
| .twitter.com                | personalization_id       | Tanımlama bilgisi, oturum açmış geçerli kullanıcının kullanıcı kimliğini içerir.  |  Twitter                                                             |
| .twitter.com                | remember_checked_on      |                                                              | Twitter                                                              |
| .twitter.com                | twid                     |                                                              |  Twitter                                                             |
| .pinterest.com              | \_auth                    | Tanımlama bilgisi, oturum açmış geçerli kullanıcının kullanıcı kimliğini içerir.  |   Pinterest                                                           |
| .pinterest.com              | \_b                       |                                                              |   Pinterest                                                           |
| .pinterest.com              | \_pinterest_pfob          |                                                              |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_referrer      | Tanımlama bilgisi, kullanıcı Pinterest düğmesini seçtiğinde sayfalar içerir.      |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_sess          | Tanımlama bilgisi, kullanıcı Pinterest düğmesini seçtiğinde sayfalar içerir.      |  Pinterest                                                            |
| .pinterest.com              | \_routing_id              |                                                              |  Pinterest                                                            |
| .pinterest.com              | bei                      |                                                              |  Pinterest                                                            |
| .pinterest.com              | cm_sub                   | Tanımlama bilgisi oluşturulduğunda bir kullanıcı kimliği ve zaman damgası içerir. |  Pinterest                                                            |
| .pinterest.com              | csrftoken                | Tanımlama bilgisi, kullanıcı Pinterest düğmesini seçtiğinde sayfalar içerir.      | Pinterest                                                             |
| .pinterest.com              | sessionFunnelEventLogged | Tanımlama bilgisi, kullanıcı Pinterest düğmesini seçtiğinde sayfalar içerir.      | Pinterest                                                             |
| .pinterest.com              | Yerel depolama            |                                                              |  Pinterest                                                            |
| .pinterest.com              | Servis Çalışanları          |                                                              |  Pinterest                                                            |


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Bir e-ticaret sitesinde site kullanıcısı tanımlama bilgisi izni 

Bir e-ticaret sitesi özelliği veya modülü gerekli olmayan bir tanımlama bilgisi kullanırsa, tanımlama bilgisi izlenmeden önce site kullanıcısının onayı alınmalıdır. Site kullanıcılarına e-ticaret sitesinde tanımlama bilgisi izni sağlamasına olanak vermek için, site yazarı sayfanın üst bilgi modülüne, izin sorulmasını ve alınmasını sağlamak amacıyla bir tanımlama bilgisi izin modülü ekleyip yapılandırmalıdır. Site kullanıcısı izni, sitenin bir sayfasında gerekli olmayan tanımlama bilgilerini kullanan bir özellik veya modülle ilgili olarak verilmelidir.

## <a name="additional-resources"></a>Ek kaynaklar

[Erişilebilirlik özellikleri ve yetenekleri](accessibility.md)

[Uyumluluğa genel bakış](compliance-overview.md)

[Gizlilik ilkesi sayfası ekleme](add-privacy-page.md)

[İzlenen içerik değişiklikleriyle ilişkili kullanıcı kimliklerini değiştirme](replace-IDs-tracked-changes.md)

[Tanımlama bilgisi izin modülü](cookie-consent-module.md) 
 
[Üst bilgi modülü](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
