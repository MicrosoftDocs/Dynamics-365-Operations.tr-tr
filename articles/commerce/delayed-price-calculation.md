---
title: İyileştirilmiş performans için kesin fiyat ve iskonto hesaplamasını geciktirme
description: Bu makalede, Microsoft Dynamics 365 Commerce satış noktasında (POS) ve çağrı merkezinde bulunan gecikmeli fiyat hesaplama özelliği açıklanmaktadır.
author: boycezhu
ms.date: 09/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 66c7c5a61648ba0423b27b74a1c4e42bc1b22b8b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267603"
---
# <a name="delay-exact-price-and-discount-calculation-for-improved-performance"></a>İyileştirilmiş performans için kesin fiyat ve iskonto hesaplamasını geciktirme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce satış noktasında (POS) ve çağrı merkezinde bulunan gecikmeli fiyat hesaplama özelliği açıklanmaktadır.

Dynamics 365 Commerce, bir satış siparişinde veya satış teklifinde birden çok satış satırı birleştirilmesi sırasında uygulanan çok satırlı iskontolar oluşturmayı destekler. Bu iskontolar; karıştır ve eşle, eşik ve miktar iskontolarını içerir.

Siparişe yeni bir satır eklendiğinde Commerce fiyatlandırma altyapısı bu çok satırlı iskontolardan herhangi birinin uygulanıp uygulanamayacağını belirlemek için tüm sepeti değerlendirir. Bu yeniden hesaplama nedeniyle yeni satırların eklenmesi satış siparişi büyüdükçe performansı etkileyebilir.

Ancak işletmeden işletmeye (B2B) şirketlerinin ve bazı işletmeden kullanıcıya (B2C) şirketlerinin siparişleri genellikle büyük boyutludur. Bu nedenle, sepete eklenen her maddeden sonra fiyatlandırma altyapısının yeniden hesaplamasını beklemek zaman alabilir. Ayrıca büyük siparişler için sepete her ürün eklendiğinde kesin fiyatın ve iskontonun gösterilmesi genellikle çok önemli değildir. Kullanıcıların maddeleri hızlı bir şekilde ekleyebilmesi daha önemlidir. Kullanıcı talebini oluşturana veya bir sipariş kesinleşene kadar kesin fiyat ve iskonto hesaplamasını geciktirme yeteneği performansı önemli ölçüde artırabilir. Ayrıca siparişi tamamlamak için gereken süreyi de azaltabilir.

Kesin fiyat ve iskonto hesaplamasını geciktirme özelliği uzun zamandır POS'ta kullanılabilmektedir. Bu yetenek, Commerce uygulamasının 10.0.22 sürümünden itibaren çağrı merkezi için de kullanılabilir.

## <a name="enable-delayed-price-and-discount-calculation-for-pos"></a>POS için gecikmeli fiyat ve iskonto hesaplamasını etkinleştirme

POS için gecikmeli fiyat ve iskonto hesaplamasını etkinleştirmek üzere aşağıdaki adımları izleyin.

1. Commerce genel merkezinde fiziksel mağazayla ilişkili işlevsellik profiline gidin.
1. **Tutar** hızlı sekmesinde, **Birden fazla madde iskontosunu el ile hesapla** yapılandırmasını etkinleştirin.
1. Gecikmeli hesaplamanın etkinleştirilmesini istediğiniz kayıtlar için ekran düzeni tasarımcısını açın.
1. İstenen düğme grubuna **Toplamı hesapla** işlemi için bir düğme ekleyin.
1. **1070** ve **1090** işlerini çalıştırın.

Artık, bir harekete maddeler eklendiğinde kasiyer, **Toplamı hesapla** düğmesini seçmedikçe çok satırlı iskontolar hesaplanmaz. Hareket için **Toplamı hesapla** seçildikten sonra her zaman çok satırlı iskontolar hesaplanır. Sepete ek maddeler eklense bile kasiyerin düğmeyi tekrar seçmesi gerekmez. Sistem, **Toplamı hesapla** seçilinceye kadar kasiyerin ödemeyi almasına izin vermez.

## <a name="enable-delayed-price-and-discount-calculation-for-call-center"></a>Çağrı merkezi için gecikmeli fiyat ve iskonto hesaplamasını etkinleştirme

Çağrı merkezi için gecikmeli fiyat ve iskonto hesaplamasını etkinleştirmek üzere aşağıdaki adımları izleyin.

1. Commerce genel merkezinde, **Çalışma alanları \> Özellik yönetimi**'ne gidin.
1. **Ticaret siparişleri için istenmeyen fiyat hesaplamalarını engelle** özelliğini etkinleştirin. Bu özellik, gecikmeli fiyat ve iskonto hesaplama yeteneği için bir ön koşuldur.

    > [!NOTE]
    > Yeni dağıtımlar için, **Ticaret siparişleri için istenmeyen fiyat hesaplamalarını engelle** özelliği varsayılan olarak etkindir.

1. **Commerce parametreleri \> Fiyatlar ve iskontolar**'a gidin.
1. **Çeşitli** bölümünde, **Çok satırlı fiyatları ve iskontoları el ile hesapla** yapılandırmasını etkinleştirin.

Artık çağrı merkezinde bir satış siparişi veya satış teklifi oluşturulduğunda ya da düzenlendiğinde kesin fiyat ve iskonto hesaplaması ertelenir. Fiyatlandırma altyapısı yalnızca eklenen veya düzenlenen satış satırını dikkate alır ve diğer tüm satış satırlarını yok sayar. Maddenin net tutarı, fiyat hesaplamasını ve basit iskontoları (tek bir maddenin iskonto yüzdesi veya tutarı) içerir. Ancak karıştır ve eşle, eşik ve miktar iskontoları uygulanmaz. Tüm iskontoların uygulandığı kesin fiyatı görmek isteyen çağrı merkezi kullanıcıları şu üç düğmeden birini seçebilir: **Yeniden hesapla**, **Toplamlar** veya **Tamamla**.

> [!NOTE]
> Çağrı merkezi siparişlerinde uygulanacak kesin fiyat ve iskonto hesaplaması için sistem, kullanıcıya **Yeniden hesapla**, **Toplamlar** veya **Tamamla** düğmelerinden birini seçmesi gerektiğini hatırlatmak için bir uyarı iletisi görüntüler. **Tamamla** düğmesinin kullanılabildiği siparişler için çağrı merkezi kullanıcısının sipariş yakalamayı tamamlamak için **Tamamla**'yı seçmesi gerektiğinden kesin fiyat ve iskonto hesaplamasını atlayabilmesinin bir yolu yoktur. **Tamamla** düğmesinin kullanılamadığı siparişler için sipariş yakalamanın tamamlandığını gösteren herhangi bir eylem yoktur. Bu nedenle, sipariş yakalamayı tamamlamadan önce **Yeniden hesapla** veya **Toplamlar**'ı seçmekten çağrı merkezi kullanıcısı sorumludur.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
