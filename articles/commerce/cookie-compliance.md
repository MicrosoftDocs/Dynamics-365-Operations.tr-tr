---
title: Çerez uyumluluğu
description: Bu konu, tanımlama bilgisi uyumu ve Microsoft Dynamics 365 Commerce'in içerdiği varsayılan ilkelerin dikkate alınması konularını açıklamaktadır.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10a58cf7197d2a8596107a42174b35350e72ae11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215709"
---
# <a name="cookie-compliance"></a>Çerez uyumluluğu

[!include [banner](includes/banner.md)]

Bu konu, tanımlama bilgisi uyumu ve Microsoft Dynamics 365 Commerce'in içerdiği varsayılan ilkelerin dikkate alınması konularını açıklamaktadır.

## <a name="overview"></a>Özet

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