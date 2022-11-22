---
title: Dynamics 365 Commerce'te ön ödemeler
description: Bu makalede, Microsoft Dynamics 365 Commerce'de ön ödeme hareketlerinin işlemesi hakkında bir genel bakış sağlanmaktadır.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-06-28
ms.openlocfilehash: 8262470f83481ef8840857a52948c0833d8b278e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780378"
---
# <a name="prepayments-in-dynamics-365-commerce"></a>Dynamics 365 Commerce'te ön ödemeler

[!include[banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'de ön ödeme hareketlerinin işlemesi hakkında bir genel bakış sağlanmaktadır.

Dynamics 365 Commerce Alacak hesapları veya Commerce'da kullanılan aşağıdaki ödeme türleri için ön ödeme hareketlerini işler:

- **Müşteri hesabı depozito ödemesi** – Müşteri satış noktasında (POS) depozito öder. Commerce, depozito ödemesini bir ön ödeme hareketi olarak işler. Hareketi deftere naklettiğinizde, Commerce Headquarters 'daki **Günlük fişi** sayfasında bir ödeme günlüğü oluşturulup deftere nakledilir. **Ödeme** sekmesindeki **Ön ödeme günlüğü fişi** onay kutusu otomatik olarak ödeme günlüğü için seçilir. Ön ödeme ve hedef bölgeyle ilgili olan vergi dahil daha fazla bilgi için bkz. [Globalleştirme kaynakları - Ülke/bölgeye özel yardım içeriği](/dynamics365/fin-ops-core/dev-itpro/lcs-solutions/country-region?context=%2Fdynamics365%2Fcontext%2Ffinance#countryregion-specific-help-content).
- **Depozito içeren müşteri siparişi** – Müşteri, POS'ta bir müşteri siparişi oluşturur. Müşteri, Commerce Headquarters 'daki **Müşteri siparişleri** sayfasında yapılandırılan varsayılan depozito yüzdesine göre sipariş için depozito ödeyebilir (**Commerce parametreleri \> Müşteri siparişleri**). Commerce, depozito ödemesini müşteri siparişi için bir ön ödeme hareketi olarak işler. Hareketi deftere naklettiğinizde, **Günlük fişi** sayfasında bir ödeme günlüğü oluşturulup deftere nakledilir. **Ödeme** sekmesindeki **Ön ödeme günlüğü fişi** onay kutusu otomatik olarak ödeme günlüğü için seçilir. Ödeme kapatılır ve sipariş teslim alındığında veya teslim edildiğinde müşteri faturası otomatik olarak düzenlenir.
- **Çağrı Merkezi satış siparişi** - Çağrı merkezi müşteri hizmetleri temsilcisi müşteri adına bir satış siparişi oluşturur ve ödeme alındığı sırasında **ön ödeme** özniteliği **Evet** olarak ayarlanır.

Commerce, bir ön ödemeyi işlemek için aşağıdaki görevleri gerçekleştirir:

- **Müşteri hesabı depozito ödemesini işleme** – Müşterinin yaptığı bir depozito ödemesi, verileri eşitleyen bir hizmet kullanılarak Commerce'a aktarılır. Commerce, ödeme için bir perakende ödeme hareketi oluşturur. Perakende hareketini deftere naklettiğinizde, bir nakit günlüğü veya müşteri ödeme günlüğü deftere nakledilir. Commerce Headquarters'daki **Günlük fişi** sayfasının **Ödeme** sekmesindeki **Ön ödeme günlüğü fişi** onay kutusu otomatik olarak ödeme günlüğü için seçilir. Ödeme tutarı negatifse ön ödemeler işlenemez.
- **Bir depozito içeren müşteri siparişi veya satış siparişini işleme** – Bir müşteri, Commerce Data Exchange: Gerçek Zamanlı Hizmet kullanarak bir müşteri siparişi için gerekli bir depozito öder. Commerce, müşterinin kullandığı ödeme yöntemine bağlı olarak bir müşteri ödeme günlüğü ya da bir nakit günlüğü oluşturur. Commerce Headquarters'da **Günlük fişi** sayfasının **Ödeme** sekmesindeki **Ön ödeme günlüğü fişi** onay kutusu otomatik olarak ödeme günlüğü için seçilir. Bir müşteri kısmi ödemeler yapmak için birden çok ödeme yöntemi kullanırsa Commerce, kullanılan ödeme yöntemine göre her kısmi ödemeyi işler.

Kredi kartları ve temelinde kredi kartı ödeme yöntemleri bulunan dijital cüzdanlar için Commerce başarılı bir yetkilendirme yaptıktan sonra bir "Yakala" isteği gönderir. (Satış siparişi faturalanmadan önce fonlar yakalanır.)

Bir müşteri siparişini iptal ederseniz, ön ödeme tutarı iade edilir ve depozito tutarı için bir iade ödeme günlüğü deftere nakledilir. İade edilen tutar, iade ödemesini deftere naklederken belirttiğiniz ödeme yöntemine göre hesaplanır ve deftere nakledilir. Commerce, Commerce Headquarters'daki **Commerce parametreleri** sayfasında ayarladığınız yüzdeye göre bir iptal masrafı uygulayabilir.

Bir müşteri siparişini iade ederseniz, bir iade emri ve geri ödeme günlüğü oluşturulur. İade siparişini deftere naklettiğinizde Commerce, müşterinin orijinal hareket için kullandığı ödeme yöntemine bağlı olarak bir müşteri ödeme günlüğü ya da bir nakit günlüğü oluşturur.
