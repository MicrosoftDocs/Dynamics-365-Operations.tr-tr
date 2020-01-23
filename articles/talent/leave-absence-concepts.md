---
title: İzin ve devamsızlık konseptleri
description: Bu konu, izin ve devamsızlık kavramlarını ve izin sürelerinin nasıl belirlediğini açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 03e2557e29194f17a9a586470ced5b352408b07c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898654"
---
# <a name="leave-and-absence-concepts"></a>İzin ve devamsızlık konseptleri

Bu konuda açıklanan kavramlar ve terimler, bir personele nasıl izin verileceğini ve personelin zaman bakiyelerinin nasıl hesapladığını belirlemenizde yardımcı olabilir. İzin ve devamsızlık yönetimi hakkında daha fazla bilgi için bkz. [İzin ve devamsızlık yönetimi](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).

## <a name="leave-plan-details"></a>İzin planı ayrıntıları

### <a name="start-date"></a>Başlangıç tarihi

Başlangıç tarihi, tahakkuk işleme başladığındaki tarihtir. Başlangıç tarihi ayrıca, ileriye taşıma tutarlarını hesaplamakta kullanılan yıl dönümü tarihidir.

## <a name="accruals"></a>Tahakkuklar

Tahakkuklar, bir personele ne zaman ve ne sıklıkta izin verileceğini belirler. Tahakkukların ne zaman verileceğine dair ilkeler ve dağılım hakkındaki ilkeler **Tahakkuklar** bölümünde, izin ve devamsızlık planını ayarlarken tanımlanır.

### <a name="accrual-frequency"></a>Tahakkuk sıklığı

Tahakkuk sıklığı, iznin ne sıklıkta tahakkuk edileceğini veya verileceğini tanımlar. Aşağıdaki seçenekler kullanılabilir durumdadır:

- Günlük
- Haftalık
- İki haftalık
- Yarım aylık
- Aylık
- Üç aylık
- Yarı yıllık
- Yıllık
- Hiçbiri

### <a name="accrual-period-basis"></a>Tahakkuk dönemi esası

Tahakkuk dönemi esası, tahakkuk dönemlerini hesaplamakta kullanılan tarihi belirler. Aşağıdaki seçenekler kullanılabilir durumdadır:

- **Plan başlangıç tarihi**
- **Personel belirli tarihi** - Bu seçenek seçili olduğunda, değer, tahakkuk dönemlerini hesaplamakta kullanılan ilk tarih değerinin kaynağını belirler. Aşağıdaki seçenekler kullanılabilir durumdadır:

    - Özel
    - Yıldönümü tarihi
    - Orijinal işe alma tarihi
    - Kıdem tarihi
    - Çalışanın ayarlanan başlama tarihi
    - Çalışanın başlama tarihi

### <a name="accrual-award-date"></a>Fiili ikramiye tarihi

Tahakkuk verme tarihi, bir personele izin verileceği tarihi belirler. Aşağıdaki seçenekler kullanılabilir durumdadır:

- **Tahakkuk dönemi bitiş tarihi** - Personele, verilme döneminin son gününde izin verilecektir.

    Doğru değeri tahakkuk etmek için tahakkuk işleminin dönemin tamamını içermesi gerekir. Örneğin, tahakkuk dönemi 1 Ocak 2018 ile 31 Ocak 2018 arasındadır. Bu durumda, Ocak'ın dahil edilmesi için tahakkukun 1 Şubat 2018 için yürütülmesi gerekir.

- **Tahakkuk dönemi başlangıç tarihi** - Personele, verilme döneminin ilk gününde izin verilecektir.

### <a name="accrual-policy-on-enrollment"></a>Tahakkuk ilkesi kaydı

Kayıttaki tahakkuk ilkesi, tahakkukun bir personel, tahakkuk döneminin ortasında kayıt yaptığında nasıl hesaplanacağını tanımlar. Aşağıdaki seçenekler kullanılabilir durumdadır:

- **Dağıtılmış** - Kayıt tarihi ve başlangıç tarihi arasındaki tarih aralığı, farkı gün olarak belirlemek için kullanılır. Fark, tahakkuklar işlendiğine uygulanır.
- **Tam tahakkuk** - Tam tahakkuk tutarı, katmana dayalı olarak ilk tahakkuk işlemesi sırasında verilir.
- **Tahakkuk yok** - Bir sonraki tahakkuk dönemine kadar hiç tahakkuk verilmez.

### <a name="accrual-policy-on-unenrollment"></a>Tahakkuk ilkesi kayıt sildirme

Kayıt sildirmedeki tahakkuk ilkesi, tahakkukun bir personel, tahakkuk döneminin ortasında kayıt sildirme yaptığında nasıl hesaplanacağını tanımlar. Aşağıdaki seçenekler kullanılabilir durumdadır:

- **Dağıtılmış** - Kayıt tarihi ve başlangıç tarihi arasındaki tarih aralığı, farkı gün olarak belirlemek için kullanılır. Fark, tahakkuklar işlendiğine uygulanır.
- **Tam tahakkuk** - Tam tahakkuk tutarı, katmana dayalı olarak ilk tahakkuk işlemesi sırasında verilir.
- **Tahakkuk yok** - Bir sonraki tahakkuk dönemine kadar hiç tahakkuk verilmez.

## <a name="accrual-schedule"></a>Tahakkuk planı

Tahakkuk planı, bir personelin izin nasıl tahakkuk ettiğini belirler ve hangi tutarın personel tarafından tahakkuk edeceğini ve ileri taşınacağını belirler. Katmanlar, iznin farklı düzeylere dayanarak verilmesi için oluşturulabilir.

### <a name="months-of-service"></a>Hizmetteki ay sayısı

**Hizmet ayı** değeri, personelin tahakkuk hakkı kazanabilmesi için çalışması gereken minimum ay sayısını belirtir. Personel için minimum gerekli değilse, değeri **0** olarak ayarlayın.

### <a name="hours-worked"></a>Çalışılan saatler

**Çalışılan saatler** değeri, personelin tahakkuk hakkı kazanabilmesi için tahakkuk başına çalışması gereken minimum saat sayısını belirtir. Personel için minimum gerekli değilse, değeri **0** olarak ayarlayın.

### <a name="accrual-amount"></a>Tahakkuk tutarı

Tahakkuk tutarı saat veya gün cinsinden çalışanların tahakkuk numarasıdır dönem başına düşen. Dönem, tahakkuk sıklığını temel alır.

### <a name="minimum-balance"></a>Minimum bakiye

Bir negatif değer, minimum bakiye için kullanılabilir, eğer personel kullanılabilir sahip olduğundan daha fazla izin talep ederse.

### <a name="maximum-carry-forward"></a>Maksimum ileriye taşıma

Tahakkuk işlemi, başlangıç tarihinin yıl dönümündeki maksimum ileri taşıma bakiyesini aşan izin bakiyelerini ayarlar.

### <a name="grant-amount"></a>Tutar ver

Tutar ver, izin planına ilk kaydolduklarında personele verilen saat veya günün ilk sayısıdır. Tutar, her bir tahakkuk dönemi için tahakkuk edilmez.

## <a name="enrollments-and-balances"></a>Kayıtlar ve bakiyeler

### <a name="enrollment-date"></a>Kayıt tarihi

Kayıt tarihi, bir personelin izin tahakkuk etmeye başlayabileceği tarihi belirtir. Örneğin, bir personel bir tatil planına 15 Haziran 2018 tarihinde kaydolduysa, 15 Haziran 2018 tarhinden önce herhangi bir süre tahakkuk edemez.

### <a name="current-balance"></a>Mevcut bakiye

Tahakkuk bakiyesi, izin talepleri için kullanılabilir izin tutarıdır. Bu tutar tahakkukları, onaylanmış talepleri ve geçerli tarih üzerinden ayarlamaları içerir.

### <a name="current-balance-examples"></a>Geçerli bakiye örnekleri

#### <a name="annual-plan"></a>Yıllık plan

**Plan kurulumu**

| Plan başlangıç tarihi | Kayıt tarihi | Tahakkuk sıklığı | Tahakkuk dönemi esası | Fiili ikramiye tarihi    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 01/01/2018        | 01/01/2018        | Yıllık            | Plan başlangıç tarihi      | Tahakkuk döneminin sonu |

Tahakkuklar 1 Ocak 2019 (01/01/2019) tarihinde işlenir, böylece dönemin tamamı dahil edilir.

**Sonuçlar**

| Tahakkuk tutarı | Minimum bakiye | Maksimum ileriye taşıma | Talep tutarı | Geçerli bakiye (01/01/2019 itibariyle) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Geçerli bakiye (160) = Tahakkuk tutarı (200) - Talep tutarı (40)

#### <a name="semimonthly-plan"></a>Yarım aylık plan

**Plan kurulumu**

| Plan başlangıç tarihi | Kayıt tarihi | Tahakkuk sıklığı | Tahakkuk dönemi esası | Fiili ikramiye tarihi    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 01/01/2018        | 01/02/2018        | Yarım aylık       | Plan başlangıç tarihi      | Tahakkuk döneminin sonu |

Tahakkuklar 1 Mayıs 2018 (01/05/2018) tarihinde işlenir, böylece dönemin tamamı dahil edilir.

**Sonuçlar**

| Tahakkuk tutarı | Minimum bakiye | Maksimum ileriye taşıma | Talep tutarı | Geçerli bakiye (01/01/2019 itibariyle) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Geçerli bakiye (22) = Tahakkuk tutarı (5 × 6) - Talep tutarı (8)

#### <a name="monthly-plan"></a>Aylık plan

**Plan kurulumu**

| Plan başlangıç tarihi | Kayıt tarihi | Tahakkuk sıklığı | Tahakkuk dönemi esası | Fiili ikramiye tarihi    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 01/01/2018        | 01/02/2018        | Yarım aylık       | Plan başlangıç tarihi      | Tahakkuk döneminin sonu |

Tahakkuklar 1 Mayıs 2018 (01/05/2018) tarihinde işlenir, böylece dönemin tamamı dahil edilir.

**Sonuçlar**

| Tahakkuk tutarı | Minimum bakiye | Maksimum ileriye taşıma | Talep tutarı | Geçerli bakiye (01/01/2019 itibariyle) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Geçerli bakiye (7) = Tahakkuk tutarı (5 × 3) - Talep tutarı (8)

### <a name="forecasted-balance"></a>Tahmin edilen bakiye

*Tahmin edilen bakiye*, gelecekteki bir tarihte kullanılabilir olan iznin tutarıdır. Tahakkuk ve ileriye taşıma ayarlamaları, bu tarihe kadar tahmin edilir.

Aşağıdaki formül kullanılır:

Pazartesi tahmin edilen bakiye = Geçerli bakiye – Talepler + Tahakkuklar – İleriye taşıma ayarlaması

### <a name="forecasted-balance-examples"></a>Tahmin edilen bakiye örnekleri

#### <a name="annual-plan"></a>Yıllık plan

**Plan kurulumu**

| Plan başlangıç tarihi | Kayıt tarihi | Tahakkuk sıklığı | Tahakkuk dönemi esası | Fiili ikramiye tarihi    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 01/01/2018        | 01/01/2018        | Yıllık            | Plan başlangıç tarihi      | Tahakkuk döneminin sonu |

Tahakkuklar 15 Şubat 2019 (15/02/2019) tarihinde işlenir, böylece dönemin tamamı dahil edilir.

**Sonuçlar**

| Tahakkuk tutarı | Minimum bakiye | Maksimum ileriye taşıma | Mevcut bakiye | Tahmin edilen bakiye (15/02/2019 itibariyle) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Tahmin edilen bakiye (40) = Tahakkuk tutarı (20) + Geçerli bakiye (40) – İleriye taşıma ayarlaması (20)

#### <a name="semimonthly-plan"></a>Yarım aylık plan

**Plan kurulumu**

| Plan başlangıç tarihi | Kayıt tarihi | Tahakkuk sıklığı | Tahakkuk dönemi esası | Fiili ikramiye tarihi    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 01/01/2018        | 01/02/2018        | Yarım aylık       | Plan başlangıç tarihi      | Tahakkuk döneminin sonu |

Tahakkuklar 15 Şubat 2019 (15/02/2019) tarihinde işlenir, böylece dönemin tamamı dahil edilir.

**Sonuçlar**

| Tahakkuk tutarı | Minimum bakiye | Maksimum ileriye taşıma | Mevcut bakiye | Tahmin edilen bakiye (15/02/2019 itibariyle) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Tahmin edilen bakiye (35) = Tahakkuk tutarı (5 × 3) + Geçerli bakiye (40) – İleriye taşıma ayarlaması (20)

#### <a name="monthly-plan"></a>Aylık plan

**Plan kurulumu**

| Plan başlangıç tarihi | Kayıt tarihi | Tahakkuk sıklığı | Tahakkuk dönemi esası | Fiili ikramiye tarihi    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 01/01/2018        | 01/02/2018        | Yarım aylık       | Plan başlangıç tarihi      | Tahakkuk döneminin sonu |

Tahakkuklar 15 Şubat 2019 (15/02/2019) tarihinde işlenir, böylece dönemin tamamı dahil edilir.

**Sonuçlar**

| Tahakkuk tutarı | Minimum bakiye | Maksimum ileriye taşıma | Mevcut bakiye | Tahmin edilen bakiye (15/02/2019 itibariyle) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Tahmin edilen bakiye (30) = Tahakkuk tutarı (10 × 1) + Geçerli bakiye (40) – İleriye taşıma ayarlaması (20)

### <a name="proration-balance-examples"></a>Dağılım bakiye örnekleri

#### <a name="prorated-monthly-plan"></a>Dağıtılan aylık plan

**Plan kurulumu**

| Plan başlangıç tarihi | Tahakkuk sıklığı | Tahakkuk dönemi esası |
|-----------------|-------------------|----------------------|
| 01/01/2018        | Aylık           | Plan başlangıç tarihi      |

**Sonuçlar**

| Personel            | Hizmetteki ay sayısı | Kayıt tarihi | Başlangıç tarihi | Tahakkuk tutarı | İşlem tahakkuku | Bilanço |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 01/06/2018        | 01/06/2018   | 1.00           | 01/09/2018        | 3,00    |
| Jay Norman          | 0,00              | 15/06/2018       | 15/06/2018  | 1.00           | 01/09/2018        | 2,53    |

#### <a name="full-accrual-monthly-plan"></a>Aylık tam tahakkuk planı

**Plan kurulumu**

| Plan başlangıç tarihi | Tahakkuk sıklığı | Tahakkuk dönemi esası |
|-----------------|-------------------|----------------------|
| 01/01/2018        | Aylık           | Plan başlangıç tarihi      |

**Sonuçlar**

| Personel            | Hizmetteki ay sayısı | Kayıt tarihi | Başlangıç tarihi | Tahakkuk tutarı | İşlem tahakkuku | Bilanço |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 01/06/2018        | 01/06/2018   | 1.00           | 01/09/2018        | 3,00    |
| Jay Norman          | 0,00              | 15/06/2018       | 15/06/2018  | 1.00           | 01/09/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Aylık tahakkuk planı yok

**Plan kurulumu**

| Plan başlangıç tarihi | Tahakkuk sıklığı | Tahakkuk dönemi esası |
|-----------------|-------------------|----------------------|
| 01/01/2018        | Aylık           | Plan başlangıç tarihi      |

**Sonuçlar**

| Personel            | Hizmetteki ay sayısı | Kayıt tarihi | Başlangıç tarihi | Tahakkuk tutarı | İşlem tahakkuku | Bilanço |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 01/06/2018        | 01/06/2018   | 1.00           | 01/09/2018        | 3,00    |
| Jay Norman          | 0,00              | 15/06/2018       | 15/06/2018  | 1.00           | 01/09/2018        | 2.00    |
