---
title: Ödemeye hazır
description: Bu konu, Dynamics 365 Human Resources'ta bir personeli ödemeye hazır işaretlemeyi gösterir.
author: marcelbf
ms.date: 08/25/2021
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
ms.openlocfilehash: 825aa327cc1530675fad57be6fc1b4313f0cf998
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068982"
---
# <a name="ready-to-pay"></a>Ödemeye hazır


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!NOTE]
> Bir personeli ödemeye hazır olarak işaretlemek istiyorsanız önce özellik yönetiminde **(Önizleme) bordro tümleştirmesi** işlevini etkinleştirmeniz gerekir. Önizleme özelliklerini etkinleştirmeyle ilgili daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

Bu özellik, insan kaynakları uzmanlarının hangi personelin bordro işlemeye hazır olduğunu ve üçüncü taraf bordro sağlayıcısı tarafından kullanılmadan önce hangilerinin eylem gerektirdiğini anlamalarını sağlar.

## <a name="mark-employee-as-ready-to-pay"></a>Personeli ödemeye hazır olarak işaretleme

Personel bilgilerini toplamak ve doğrulamak zaman alıcı ve hata yapma olasılığı yüksek olabilir. Dynamics 365 Human Resources, insan kaynakları profesyonellerinin personel bilgilerini gözden geçirmeleri ve kolayca güncellemeleri için bir yol sağlayarak bordro işlemeye hazırlanmak için harcanan süreyi azaltmaya yardımcı olur.

Bir personeli ödemeye hazır olarak işaretlemek için:

1. **Maaş yönetimi**'ni açın. Çalışma alanında iki kutucuk vardır: 
    - **Çalışanlar ödemeye hazır**
    - **Ödemeye hazır olmayan personel**
    ![Maaş yönetimi çalışma alanı.](./media/hr-ready-to-pay-1-workspace.png)

2. **Ödeme yapmaya hazır olmayan personel** kutucuğunu seçin.

3. Doğrulanacak personeli seçin. **Bordro sekmesinde** **Ödemeye hazır** grubunda **Doğrula**'yı seçin.
    ![Personeli doğrulayın.](./media/hr-ready-to-pay-2-validate.png)

4. Sonuçları gözden geçirmek için **Bordro sekmesinde** **Ödemeye hazır** grubunda **Sonuçlar**'ı seçin.

## <a name="validation"></a>Doğrulama

Bir personeli ödemeye hazır olarak işaretlemeden önce personelin profil, eksiksizlik açısından doğrulanır.

![Sonuçları doğrulayın.](./media/hr-ready-to-pay-3-results.png)

| Doğrulama | Ayrıntılı |
| --- | --- |
| **Adres amacı parametresi** | **Bordro adresleri amacını kullan** parametresinin seçili olduğunu onaylar. |
| **Bordro adresi** | Çalışan profilinde **Bordro ikamet konumu** veya **Bordro iş konumu** amacına sahip en az bir adres bulunduğunu ve amaç başına yalnızca bir adres olduğunu onaylar. |
| **İstihdam** | Çalışanın en az bir istihdamı (mevcut, önceki veya gelecekteki) olduğunu onaylar. |
| **Kimlik numarası** | **İnsan kaynakları parametreleri** sayfasında **Bordro işlemede kimlik türlerini kullan** alanının **Evet** olduğunu ve parametrede belirtilen kimlik türünün çalışan profilinde doldurulup doldurulmadığını onaylar. |
| **Ad ve soyadı** | **Ad** ve **Soyadı** alanlarının doldurulduğunu onaylar.|
| **Pozisyon numarası** | Çalışanın atanmış bir pozisyonu olduğunu onaylar. |
| **Doğum tarihi** | **Doğum günü** alanının doldurulduğunu onaylar. |
| **Maaş** | Çalışanın bir sabit ücret planına kayıtlı olduğunu onaylar. |

Bu doğrulamalardan biri başarısız olursa personeli ödemeye hazır olarak işaretleyemezsiniz.

**Ödemeye hazır** alanı **Hayır** ise bu, çalışan profilinin tamamlandığından emin olmak için bir eylem gerçekleştirmeniz gerektiğinin bir göstergesidir. Bu, herhangi bir veri varlığında verilerin açığa çıkmasını durdurmaz. 

## <a name="process-automation"></a>İşlem Otomasyonu

[Süreç Otomasyonu](/dynamics365/fin-ops-core/dev-itpro/sysadmin/process-automation)'nu kullanarak tüm personelin doğrulamasını otomatik hale getirebilirsiniz. **Ücret yönetimi** çalışma alanında **Bağlantılar** \> **Parametreler** \> **Süreç Otomasyonları**'na gidin.

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
