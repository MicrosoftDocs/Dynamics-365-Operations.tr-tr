---
title: B2B e-ticaret web siteleri için fatura yönetimi
description: Bu makale Microsoft Dynamics 365 Commerce işletmeler arası (B2B) e-ticaret web sitelerinin fatura yönetimi yeteneklerini açıklar.
author: ShalabhjainMSFT
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: c1f3533eb711bf87fe226f5c61678b6939f35e13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274441"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>B2B e-ticaret web siteleri için fatura yönetimi

[!include [banner](../../includes/banner.md)]

Bu makale Microsoft Dynamics 365 Commerce işletmeler arası (B2B) e-ticaret web sitelerinin fatura yönetimi yeteneklerini açıklar.

B2B hareketlerini kullanan şirketler için Müşteri alacağına karşılık sipariş kabul etmek ve arından siparişi karşıladıktan sonra müşterilere fatura göndermek yaygın bir uygulamadır. Müşteriler için ödeme koşulları tanımlanır ve müşterilerin zamanında veya zamanından önce ödeme yapmasını teşvik etmek için bazı iskontolar yapılabilir. Ödemelerin zamanında alınma olasılığını artırmaya yardımcı olmak için, B2B e-ticaret web siteleri müşterilerin tüm faturalarını görüntülemesine olanak tanır. Müşteri ödenmiş, ödenmemiş ve kısmen ödenmiş faturaları vade tarihleriyle birlikte görüntülemek için faturalara kolayca filtre uygulayabilir.

![B2B web sitesindeki faturalar sayfası.](../media/ViewInvoices.png)

> [!NOTE]
> Oturum açmış bir kullanıcı yalnızca kendi faturalarını görüntüleyebilir ve ödeyebilir. Commerce Headquarters'da müşteri kaydının **fatura ve teslimat** hızlı sekmesindeki **Fatura hesabı** açılır menüsünde bir kuruluş hesabı yapılandırılırsa kullanıcı kuruluş hesabıyla ilgili faturaları görüntüleyebilir ve ödeyebilir.

B2B web sitesinin **Faturalar** sayfasında, kullanıcı ödenmemiş veya kısmen ödenmiş bir fatura seçebilir ve **Faturayı öde** seçeneğini kullanabilir. Seçilen fatura alışveriş sepetine eklenir ve kullanıcı ödeme işlemiyle devam edebilir. Böylece kullanıcı, faturanın tam tutarının mı yoksa kısmi bir tutarın mı ödeneceğine karar verebilir. Kullanıcı faturaları ödemek için açık hesap ödeme yöntemini kullanamaz.

> [!NOTE]
> Faturalar yalnızca sepette bir madde yoksa alışveriş sepetine eklenebilir. Aynı şekilde, maddeler yalnızca septte fatura yoksa sepete eklenebilir. Microsoft, gelecekteki Commerce sürümlerinde bu kısıtlamayı kaldırmayı planlamaktadır.

![B2B web sitesindeki sepet sayfası.](../media/PayInvoice.png)

**Faturalar** sayfasında, kullanıcı faturanın yanındaki **Fatura iste** seçeneğini de belirleyebilir. Böylece kullanıcı, fatura ayrıntılarının kayıtlı e-posta adresine gönderilmesini isteyebilir.

![Fatura iste iletişim kutusu.](../media/RequestInvoice2.png)

Kullanıcı bir fatura istediğinde, istek **Hesabım** sayfasının **B2B İstekleri** bölümüne taşınır. Daha sonra, **P-0001** ve **Siparişleri ve kanal isteklerini eşitle** işleri Commerce Headquarters da çalıştırdıktan sonra, fatura e-postası tetiklenir ve B2B isteğinin durumu tamamlandı olarak işaretlenir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
