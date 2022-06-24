---
title: İşlem kayıt uygunluğu
description: Bu makalede, kayıt uygunluk işleminin nasıl çalıştırıldığı açıklanır.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c01d7a6f456514fc9da1889ccaff5af1ae7c0f52
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877757"
---
# <a name="process-enrollment-eligibility"></a>İşlem kayıt uygunluğu


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, kayıt uygunluk işleminin nasıl çalıştırıldığı açıklanır.

1. **Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, kayıt **uygunluk işlemini** seçin.

2. **Kazanç kaydı uygunluk işlemini çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Kayıt dönemi** | Kayıt uygunluğunu işleyecek kayıt dönemi. |
   | **Tüzel kişilik** | Yasal varlık işleyecek kayıt dönemi. |
   | **Çalışan** | Çalışan işleyecek kayıt dönemi. Bu alanı boş bırakırsanız, kayıt uygunluğu tüm çalışanlar için işlem görür. |
   | **Kazanç planı** | Kazanç planı işleyecek kayıt dönemi.

3. İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:

   1. İşlem bilgilerini girin.

   2. Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.

   3. İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.

   4. **Tamam**'ı seçin. İşlem, ayarladığınız parametrelerle çalışacaktır.

4. **Tamam**'ı seçin.

## <a name="view-process-results"></a>İşlem Sonuçlarını Görüntüleme

Bu makalede, uygunluk işlemi sonuçlarının nasıl görüntüleneceği açıklanmaktadır.

1.  **Kazanç yönetimi** çalışma alanında, **İşleme** altında, **İşlem sonuçları**'nı seçin.

2.  **İşlem sonuçları** sayfasında, aşağıdaki alanlar belirtilir:

   | Alan | Tanım |
   | --- | --- |
   | **İşlem Kodu** | Çalışan, Tüzel kişilik ve işlem çalıştırma birleşiminin benzersiz kodu. |
   | **İşlem türü** | Çalıştırılmış olan işlemi tanımlar. Örnek: Kayıt. |
   | **Zaman damgası** | Uygunluk işleminin çalıştırıldığı zaman. |
   | **Tüzel kişilik** | Kayıt işlemi sırasında belirtilen tüzel kişilik. |
   | **Çalışan** | İşlenmiş olan çalışan. |
   | **Plan | Kaydın denendiği Kazanç planı. |
   | **Uygunluk kuralı** | İşlenmiş olan uygunluk kuralı. Uygunluk çalıştırılmadan önce hata oluştuysa, bu boş olacaktır. Örnek: Bir çalışan için ücret tanımlanmadıysa, uygunluk işlemi çalışmaz ve bu alan boş bırakılır. |
   | **Sonuç durumu** | Bu, Uygun veya Uygun Değil olacaktır. Çalışan uygunluk kuralı kriterini karşılamıyorsa, çalışanın ödeme sıklığı veya sabit ücret gibi gerekli bilgileri eksikse veya kazanç planında çalışanın kaydedilmesini engelleyen eksik bilgi varsa sonuç durumu Uygun Değil olur. |
   | **Sonuç iletisi** | Bir çalışanın kazanç planı için neden uygun olmadığını veya uygunluk kuralının geçilip geçilmediğini gösterir. |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
