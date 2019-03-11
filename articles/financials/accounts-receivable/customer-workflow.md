---
title: Müşteri iş akışı
description: Bu konu müşteri iş akışıyla ilgili bilgiler sağlar. Bir müşteri için belirli alanları değiştirebilir ve müşteri için eklenmeden önce iş akışı kullanarak değişiklikleri onaylanmak üzere gönderebilirsiniz.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 1b0e1621b256e6bbb42f97134b87dd65fa146193
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "303005"
---
# <a name="customer-workflow"></a>Müşteri iş akışı

[!include [banner](../includes/banner.md)]

Müşteri iş akışı, Microsoft Dynamics 365 for Finance and Operations sürüm 8.0.4'e eklendi. Bir müşteri için belirli alanları değiştirebilir ve müşteri için eklenmeden önce iş akışı kullanarak değişiklikleri onaylanmak üzere gönderebilirsiniz.

## <a name="set-up-the-customer-workflow"></a>Müşteri iş akışı ayarlama

Müşteri iş akışı özelliğini kullanabilmek için etkinleştirmeniz gerekir.

1. **Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin.
2. Özelliği etkinleştirmek için **Genel** sekmesinde, **Müşteri onayı** hızlı sekmesinde **Müşteri onaylarını etkinleştir** seçeneğini **Evet** olarak ayarlayın.
3. **Veri varlığı davranışı** alanında, veriler içe aktarıldığında veri varlıklarının kullanması gereken davranışı seçin:

    - **Değişikliklere onay olmadan izin ver**: Varlık müşteri kaydını iş akışıyla işlemeden güncelleştirebilir.
    - **Değişiklikleri reddet**: Müşteri kaydında değişiklik yapılamaz. İş akışı için etkinleştirilen alanlar içe aktarılamaz.
    - **Değişiklik önerileri oluştur**: İş akışı için etkinleştirilenler dışındaki tüm alanlar değiştirilir. Bu alanlara ilişkin yeni değerler müşteri kaydına önerilen değişiklikler olarak eklenir ve iş akışı otomatik olarak başlatılır.

4. Müşteri alanları listesinde, değişiklik yapılmadan önce onaylanması gereken her alan için **Etkinleştir** onay kutusunu seçin.
5. **Alacak hesapları \> Kurulum \> Alacak hesapları iş akışları**'na gidin.
6. **Yeni**'yi seçin.
7. **Önerilen müşteri değişikliği iş akışı**'nı seçin. 
8. İş akışını onay sürecinizle eşleşecek şekilde ayarlayın. **Önerilen müşteri değişikliği için iş akışı onayı** iş akışı onayı öğesi müşteri için değişiklikleri uygular.

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a>Müşteri bilgilerini değiştirme ve değişiklikleri iş akışına gönderme

İş akışı için etkinleştirilen bir alanı değiştirdiğinizde **Önerilen değişiklikler** sayfası görüntülenir. Bu sayfa alanın orijinal değerini ve girdiğiniz yeni değeri gösterir. Değiştirdiğiniz alan orijinal değerine geri döndürülür. Sayfadaki durum iletisi değişikliklerinizin gönderilmediği konusunda sizi bilgilendirir.

İş akışı için etkinleştirilen bir alanı her değiştirdiğinizde, bu alan önerilen değişiklikler sayfasına eklenir. Bir alan için önerilen değişikliği atmak üzere listede alanın yanındaki **At** düğmesini kullanın. Tüm değişiklikleri atmak için sayfanın alt kısmındaki **Tüm değişiklikleri at** düğmesini kullanın. Sayfayı kapatmak için **Tamam**'ı seçin.

En az bir önerilen değişikliğiniz olduğunda, Eylem Bölmesinde iki ek menü görüntülenir: **Önerilen değişiklikler** ve **İş akışı**.

1. **Önerilen değişiklikler** sayfasını açmak için **Önerilen değişiklikler**'i seçin ve değişikliklerinizi gözden geçirin.
2. Değişiklikleri iş akışına göndermek için **İş akışı \> Gönder**'i seçin.

    Sayfadaki durum **Değişiklikler onay bekliyor** olarak değişir.

İş akışı Finance and Operations'taki standart iş akışı sürecini izler. Onaylayan **Önerilen değişiklikler** sayfasındaki değişiklikleri gözden geçirebileceği ve **İş akışı \> Onayla** öğesini seçerek iş akışını onaylayabileceği **Müşteri** sayfasına yönlendirilir. Tüm onaylar tamamlandığında, alanlar önerdiğiniz değerlerle güncelleştirilir.
