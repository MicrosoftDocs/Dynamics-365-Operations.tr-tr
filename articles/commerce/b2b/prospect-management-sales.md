---
title: Dynamics 365 Sales kullanarak B2B e-ticaret web sitelerindeki iş ortağı kullanıcılarını yönetme
description: Bu makalede, Dynamics 365 Commerce işletmeler arası (B2B) e-ticaret web siteleri için iş ortağı onaylarını yönetmek üzere Microsoft Dynamics 365 Sales uygulamasının nasıl kullanılacağı açıklanmaktadır.
author: shajain
ms.date: 2/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ac4aa15f2c6e7f557105254c2c8ce743a9466985
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878633"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Dynamics 365 Sales kullanarak B2B e-ticaret web sitelerindeki iş ortağı kullanıcılarını yönetme

[!include [banner](../../includes/banner.md)]

Bu makalede, Dynamics 365 Commerce işletmeler arası (B2B) e-ticaret web siteleri için iş ortağı onaylarını yönetmek üzere Microsoft Dynamics 365 Sales uygulamasının nasıl kullanılacağı açıklanmaktadır. Dynamics 365 Sales çözümüne zaten yatırım yapmış olan kuruluşlar, B2B e-ticaret iş ortağı onay işlemi için müşteri adayı ve fırsat kavramlarını kullanabilir.

B2B iş ortağı onay işlemi hakkında temel bilgiler için [B2B e-ticaret web sitelerinde iş ortağı kullanıcılarını yönetme](manage-b2b-users.md) konusuna bakın.

Potansiyel iş ortakları, B2B sitesindeki bir bağlantı aracılığıyla bir ekleme isteği göndererek B2B e-ticaret web sitesine ekleme işlemini başlatabilir. İstek gönderildikten ve ilgili işler (**P-0001**, **Sipariş ve kanal isteklerini eşitle**) Commerce headquarters'da çalıştırıldıktan sonra ekleme isteği Commerce Headquarters'daki **Tüm aday müşteriler** sayfasına kaydedilir. Böylece iş ortağı aday müşteri onay süreci Sales'de tamamlanabilir.

Sales ve Commerce arasındaki tümleştirme etkinleştirildikten sonra, Commerce'da iş ortağı aday müşterisi oluşturulması Sales'de *müşteri adayı* oluşturulmasına neden olur.

Aşağıda, iş ortağı aday müşterisi için Sales'de müşteri adayı oluşturma sayfasının örneği gösterilmektedir.

![Dynamics 365 Sales'de müşteri adayı oluşturma sayfası.](../media/LeadInSales.png)

Örnekte **İlgili kişi** bölümünde ekleme isteğini gönderen kişi ve **Şirket** bölümünde kuruluş gösterilirmektedir. **Zaman çizelgesi** bölümündeki bir not, müşteri adayının ikili yazma alt yapısı tarafından oluşturulduğunu gösterir. Çift yazma altyapısı tarafından oluşturulduğundan bu müşteri **Açık aday müşterilerim** açılır listesinde görünmez. Bunun yerine, **tüm Commerce B2B müşteri adayları** adılı yeni bir görünüm altında görüntülenir.

Sales'deki standart müşteri adayı uygun bulma işlemine göre, bir kullanıcı müşteri adayını "uygun bulduğunda" bir *fırsat* kaydı, *ilgili kişi* kaydı ve *hesap* kaydı oluşturulur. Çift yazma alt yapısı, ilgili kişi ve hesap kayıtlarını Commerce'a yazmak için kullanılır. İlgili kişi, *kişi* türünde müşteri olarak oluşturulur ve şirket *kuruluş* türünde müşteri olarak oluşturulur. Kullanıcı fırsat için **Kazanıldı Olarak Kapat**'ı seçerse aday müşteri Commerce'da onaylanır. Aday müşterinin onaylanması müşteri hiyerarşisinin oluşturulmasına neden olur.

Tüm kalan iş süreçleri Commerce'da gerçekleşir. Bu işlemler arasında iş ortağına e-posta gönderme, kullanıcılar için alacak limiti yönetimi tanımlama ve B2B sitesine daha fazla kullanıcı ekleme bulunur. Bununla birlikte, bir kullanıcı müşteri adayını uygun bulmak yerine müşteri adayını uygun değil olarak belirlerse veya fırsatı kaybedildi olarak işaretlerse aday müşteri Commerce'da reddedildi olarak işaretlenir ve istek sahibine eklemeyi reddetme e-postası gönderilir.

## <a name="enable-integration-between-sales-and-commerce"></a>Sales ve Commerce arasında tümleştirmeyi etkinleştirme

Sales ve Commerce arasındaki tümleştirme çift yazma altyapısına dayanır. Bu nedenle, bir sistemde oluşturulan müşterilerin diğer sisteme yazılması için çift yazma etkin ve çalışıyor olmalıdır. Çift yazma altyapısı hakkında daha fazla bilgi için bkz. [Çift yazmaya genel bakış](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview).

Çift yazma kurulumu tamamlandıktan sonra, uygulama iş ortağı [Microsoft AppSource](https://appsource.microsoft.com/)'a gidip [Çift yazma Commerce çözümleri](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview) adındaki çözümü arayabilir. Standart yükleme sihirbazını kullanarak paketi yükleyin ve bir B2B sitesinde aday müşteri oluşturarak test edin. Aday müşteri oluşturulduktan sonra isteğin Commerce'ta **Tüm aday müşteriler** bölümünde görüntülendiğini ve ardından aday müşterinin Sales'de müşteri adayı olarak gösterildiğini doğrulayın.

## <a name="additional-resources"></a>Ek kaynaklar

[B2B e-ticaret web sitelerindeki iş ortağı kullanıcılarını yönetme](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
