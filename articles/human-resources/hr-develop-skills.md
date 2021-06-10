---
title: Yetenekleri konfigüre et
description: Çalışanlarınızın yeteneklerini Dynamics 365 Human Resources'ta izleyebilirsiniz. Ayrıca, belirli bir iş için gereken yetenekleri de belirtebilirsiniz.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076571"
---
# <a name="configure-skills"></a>Yetenekleri konfigüre et

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Çalışanlarınızın yeteneklerini Dynamics 365 Human Resources'ta izleyebilirsiniz. Ayrıca, belirli bir iş için gereken yetenekleri de belirtebilirsiniz.

İzleyebileceğiniz yetenek örnekleri verilmiştir:

- Gözetime yönelik – Diğerlerinin çalışmasını denetleme yeteneği.
- Liderlik – Çalışanları ve iş alanlarını yönetme yeteneği.
- Planlama - İleriyi görebilme, vizyon deyimleri oluşturma ve bunları değerlendirme yeteneği.
- HTML – HTML kodu yazabilme yeteneği.

Yetenek tiplerini ve derecelendirme modellerini henüz ayarlamadıysanız, yetenek oluşturmadan önce bir miktar eklemeniz gerekir.

Aşağıdaki kişiler bir çalışan için yetenek girebilecek:

- Çalışanlar self servise kendileri için yetenekler girebilecek. Bu yetenekler için yönetici onayı gereklidir.
- Yöneticiler, çalışanları için yetenekler girebilirler. Bu becerileri otomatik olarak onaylayan bir iş akışı oluşturabilirsiniz.

## <a name="create-a-skill-type"></a>Beceri türü oluşturma

Yetenek tipleri yönetim veya satışlar gibi bireysel yeteneklerin altında kalan kategorilerlerdir.

1. **Çalışan geliştirme** çalışma alanında, **Bağlantılar**'ı seçin.

2. **Yetki kurulumu** altında **Yetenek tipleri**'ni seçin.

3. **Yeni**'yi seçin.

4. Ardından aşağıdaki alanları tamamlayın:

   - **Beceri türü**: Beceri türü için bir ad girin.
   - **Açıklama**: Beceri türü için bir açıklama girin.

5. **Kaydet**'i seçin.

## <a name="create-a-rating-model"></a>Derecelendirme modeli oluşturma

Değerlendirme modelleri bir kişinin gerçek yetenek düzeyini, elde etmek için çalışmaları gereken düzeyi veya iş için gerekli olan yetenek düzeyini değerlendirmenize yardımcı olur. Derecelendirme modelindeki her düzeye bir faktör atanır.

1. **Çalışan geliştirme** çalışma alanında, **Bağlantılar**'ı seçin.

2. **Yetki kurulumu** altında, **değerlendirme modelleri**'ni seçin.

3. **Yeni**'yi seçin.

4. Ardından aşağıdaki alanları tamamlayın:

   - **Derecelendirme**: değerlendirme modeli için **yetenekler** gibi bir ad girin.
   - **Açıklama**: **Yetenek derecelendirmeleri** gibi bir değerlendirme modeli açıklaması girin.

5. **Düzeyler** bölümünde, **Yeni**'yi seçin. Eklemek istediğiniz her düzey için, aşağıdaki alanları tamamlayın:

   - **Düzey**: Düzey için bir ad girin.
   - **Açıklama**: Düzey için bir açıklama girin.
   - **Faktör**: 0-9 bir faktör değeri girin. Faktörlr, farklı değerlendirme modelleri kullanılan yetenek skorlarını normalleştirmeye yardımcı olur. Her düzey benzersiz bir etmenle sahip olmalıdır. Faktör değerleri yüksek düzeyler bir derecelendirme modelinde daha fazla ağırlık taşır.

   Gerektiğinde düzeyler eklemeye devam edin. Bir derecelendirme modeli için en fazla 10 düzey girebilirsiniz.

6. **Kaydet**'i seçin.

## <a name="create-a-skill"></a>Beceri oluşturma

Bir kişiye veya işe bir yetenek atayabilmek, bir yetenek eşleme araması ya da bir yetenek profili oluşturabilmek için, **Yetenekler** sayfasında yeteneklerle ilgili bilgileri girmeniz gerekir. Her bir yetenek için yetenek türünü ve değerlendirme modelini seçebilirsiniz.

1. **Çalışan geliştirme** çalışma alanında, **Bağlantılar**'ı seçin.

2. **Yetki kurulumu** altında **Yetenekler**'i seçin.

3. **Yeni**'yi seçin.

4. Ardından aşağıdaki alanları tamamlayın:

   - **Beceri**: Beceri için bir ad girin.
   - **Açıklama**: Beceri için bir açıklama girin.
   - **Derecelendirme**: Bu beceri için kullanmak istediğiniz derecelendirme modelini seçin.
   - **Yetenek türü**: Yetenek tipleri listesinden seçim yapın.

5. **Kaydet**'i seçin.

## <a name="see-also"></a>Ayrıca bkz.

[Yetenekleri girin](hr-develop-enter-skills.md)<br>
[Becerileri eşleştirme](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]