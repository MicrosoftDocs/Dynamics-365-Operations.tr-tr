---
title: Ödemeye hazır
description: Bu konu, Dynamics 365 Human Resources'ta bir personeli ödemeye hazır işaretlemeyi gösterir.
author: marcelbf
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 70b3f31db459fe021caf08fe09b2e44a597294d1992ee16a69efd8745941a4bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732429"
---
# <a name="ready-to-pay"></a>Ödemeye hazır

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

> [!NOTE]
> Bir personeli ödemeye hazır olarak işaretlemek istiyorsanız önce özellik yönetiminde **(Önizleme) bordro tümleştirmesi** işlevini etkinleştirmeniz gerekir. Önizleme özelliklerini etkinleştirmeyle ilgili daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

Bu özellik, insan kaynakları uzmanlarının hangi personelin bordro işlemeye hazır olduğunu ve üçüncü taraf bordro sağlayıcısı tarafından kullanılmadan önce hangilerinin eylem gerektirdiğini anlamalarını sağlar.

## <a name="mark-employee-as-ready-to-pay"></a>Personeli ödemeye hazır olarak işaretleme

Personel bilgilerini toplamak ve doğrulamak zaman alıcı ve hata yapma olasılığı yüksek olabilir. Dynamics 365 Human Resources, insan kaynakları profesyonellerinin personel bilgilerini gözden geçirmeleri ve kolayca güncellemeleri için bir yol sağlayarak bordro işlemeye hazırlanmak için harcanan süreyi azaltmaya yardımcı olur.

Bir personeli ödemeye hazır olarak işaretlemek için:

1. **Maaş yönetimi**'ni açın. Çalışma alanında iki kutucuk vardır 
    - **Çalışanlar ödemeye hazır**
    - **Ödemeye hazır olmayan personel**
    ![Maaş yönetimi çalışma alanı.](./media/hr-ready-to-pay-1-workspace.png)

2. **Ödeme yapmaya hazır olmayan personel** kutucuğunu seçin.

3. Doğrulanacak personeli seçin. **Bordro sekmesinde** **Ödemeye hazır** grubunda **Doğrula**'yı seçin.
    ![Personeli doğrulayın.](./media/hr-ready-to-pay-2-validate.png)

4. Sonuçları gözden geçirmek için **Bordro sekmesinde** **Ödemeye hazır** grubunda **Sonuçlar**'ı seçin.

## <a name="validation"></a>Doğrulama

Bir personeli ödemeye hazır olarak işaretlemeden önce, sistem, profil eksiksiz olduğunda temel bir doğrulama yapacaktır.

![Sonuçları doğrulayın.](./media/hr-ready-to-pay-3-results.png)

Aşağıdaki tablo, gerçekleştirilen doğrulamaların her biri hakkında bilgi sağlar. 

| Doğrulama | Ayrıntılı |
| --- | --- |
| Adres amacı parametresi | **Bordro adresleri amacını kullan** parametresinin açık olup olmadığını doğrular. |
| Bordro adresi | Çalışan profilinde "Bordro ikamet yeri" veya "Bordro iş yeri" amacına sahip en az bir adres olup olmadığını ve amaç başına yalnızca bir adres olup olmadığını doğrular. |
| İstihdam | Çalışanın en az bir istihdamı (mevcut, önceki veya gelecekteki) olup olmadığını doğrulayın. |
| Kimlik numarası | "Bordro işlemede kimlik türlerini kullan" parametresinin evet olup olmadığını ve parametrede belirtilen kimlik türünün çalışan profilinde doldurulup doldurulmadiğini doğrular. |
| Ad ve soyadı | **Ad** ve **Soyadı** alanlarının doldurulup doldurulmadığını denetleyerek çalışan profilinin geçerli olup olmadığını doğrular.|
| Pozisyon numarası | Çalışanın atanmış bir pozisyonu olup olmadığını doğrulayın. |
| Doğum tarihi | Çalışan profilinin geçerli olup olmadığını doğrular ve **Doğum Günü** alanının doldurulup doldurulduğunu denetler. |
| Maaş | Çalışanın sabit bir ücret planına kayıtlı olup olmadığını doğrulayın. |

Bu doğrulamalardan biri başarısız olursa personeli ödemeye hazır olarak işaretleyemezsiniz.

**Ödemeye hazır** alanı **Hayır** ise bu, çalışan profilinin tamamlandığından emin olmak için bir eylem gerçekleştirmeniz gerektiğinin bir göstergesidir. Bu, herhangi bir veri varlığında verilerin açığa çıkmasını durdurmaz. 

## <a name="known-issues"></a>Bilinen sorunlar

- Özellik yönetiminde **Kolaylaştırılmış personel girişi** özelliğini devre dışı bırakmalısınız. Bu özelliği kullanırsanız maaş yönetimi çalışma alanındaki kutucuklar düzgün çalışmaz.
- Çalışan formunda, **Bordro sekmesi**, **Ödemeye hazır** grubu herhangi bir kullanıcı rolü için kullanılabilir. 

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
