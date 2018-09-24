---
title: "Satıcı iş akışı"
description: "Satıcı bilgilerini değiştirin ve onaylamak için iş akışını kullanın."
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Vendor
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 950a1852acf9f3e4747ce2d55738c0eb3a646897
ms.contentlocale: tr-tr
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-workflow"></a>Satıcı iş akışı

[!include [banner](../includes/banner.md)]

Satıcı iş akışı kullanıldığında belirli alanlarda yapılan değişiklikler, satıcıya eklenmeden önce onaylanmak üzere iş akışına gönderilir.

## <a name="set-up-the-vendor-workflow"></a>Satıcı iş akışının kurulumu

İş akışı özelliğini kullanmak için önce etkinleştirmeniz gerekir.

1. **Borç hesapları \> Kurulum \> Borç hesapları parametreleri**'ne gidin.
2. **Genel** sekmesinde **Satıcı onayı** hızlı sekmesinde, **Satıcı onaylarını etkinleştir** seçeneğini **Evet** olarak ayarlayın.
3. **Veri varlığı davranışı** alanında, veriler içe aktarıldığında kullanılması gereken davranışı seçin:

    - **Onay olmadan değişikliklere izin ver**: Veri varlığı, satıcı kaydını iş akışında işlemeden güncelleştirebilir.
    - **Değişiklikleri reddet**: Satıcı kaydında değişiklik yapılamaz. İş akışı için etkinleştirilen alanlarda içe aktarma başarısız olur.
    - **Değişiklik teklifleri oluştur**: İş akışı için etkinleştirilen alanlar dışında tüm alanlar değiştirilir. Bu alanlar için yeni değerler önerilen değişiklikler olarak satıcıya eklenir ve iş akışı otomatik olarak başlatılır.

4. Satıcı alanı listesinde, değişiklik yapılmadan önce onaylanması gereken her alan için onay kutusunu **Etkinleştir** öğesini seçin.
5. **Borç hesapları \> Kurulum \> Borç hesapları iş akışları**'na gidin.
6. **Yeni** öğesini seçin.
7. **Önerilen satıcı değişiklikleri iş akışı** öğesini seçin. 
8. İş akışını onay işleminizle eşleşecek şekilde ayarlayın. **Önerilen satıcı değişikliği için iş akışı onayı** iş akışı onayı öğesi, satıcıda yapılan değişiklikleri uygular.

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a>Satıcı bilgilerini değiştirme ve değişiklikleri iş akışına gönderme

İş akışı için etkinleştirilen bir alanı değiştirdiğinizde **Önerilen değişiklikler** sayfası görüntülenir. Bu sayfada, alanın orijinal değeri ve girdiğiniz yeni değer gösterilir. Değiştirdiğiniz alan orijinal değerine geri döndürülür. Ayrıca bir durum iletisi ile değişikliklerinizin gönderilmediği bilgisi verilir. 

İş akışı için etkinleştirilen bir alanı her değiştirdiğinizde bu alan, **Önerilen değişiklikler** sayfasındaki listeye eklenir. Bir alan için önerilen değeri atmak isterseniz listedeki alanın yanında bulunan **At** düğmesini kullanın. Tüm değişiklikleri atmak için sayfanın alt kısmındaki **Tüm değişiklikleri at** düğmesini kullanın. Sayfayı kapatmak için **Tamam** öğesini seçin.

En az bir önerilen değişiklik yaptıktan sonra eylem bölmesinde iki ek sekme görüntülenir: **Önerilen değişiklikler** ve **İş akışı**.

1. **Önerilen değişiklikler** sayfasını seçmek için **Önerilen değişiklikler** öğesini seçin ve değişikliklerinizi gözden geçirin.
2. Değişiklikleri iş akışına göndermek için **İş akışı \> Gönder** öğesini seçin.

    Sayfadaki durum, **Değişiklikler onay bekliyor** olarak değişir.

İş akışı, Microsoft Dynamics 365 for Finance and Operations'ta standart iş akışı işlemini takip eder. Onaylayan, **Önerilen değişiklikler** sayfasında değişiklikleri gözden geçirebildiği ve iş akışını onaylamak için **İş akışı \> Onayla** öğesini seçebildiği **Satıcı** sayfasına yönlendirilir. Tüm onaylar tamamlandıktan sonra alanlar önerdiğiniz değerler ile güncelleştirilir.

