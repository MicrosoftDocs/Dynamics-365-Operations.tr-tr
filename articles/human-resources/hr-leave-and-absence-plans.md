---
title: İzin ve devamsızlık planı oluşturma
description: Dynamics 365 Human Resources'ta farklı izin tipleri için izin planlarını içinde oluşturun.
author: andreabichsel
manager: tfehr
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 90a3d624dac6c78dfbf2479c5ac7eab76dd4b542
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115960"
---
# <a name="create-a-leave-and-absence-plan"></a>İzin ve devamsızlık planı oluşturma

Sunduğunuz her izin türü için Dynamics 365 Human Resources'ta izin ve devamsızlık planlarını tanımlayın. İzin ve devamsızlık planları, yıllık, aylık veya yarı aylık gibi farklı frekanslarda tahakkuk edebilir. Planlar ayrıca tahakkukun belirli bir tarihte tek bir defa oluşacağı bir türde de tanımlanabilir. Örneğin, yıllık olarak değişken tatiller veren bir plan oluşturabilirsiniz.

Katmanlı izin planları, çalışanların bir organizasyonla harcadıkları sürenin miktarına göre faydalar almasına olanak tanır. Katmanlı planlar ek kazanç saatlerinde otomatik kaydı etkinleştirir.

Çalışanların yalnızca tahakkuk etmiş oldukları kazanç saatlerini kullanmasını sağlamak için maksimum yürütme tutarlarını veya minimum bakiyelerini belirtebilirsiniz.

Örneğin, katmanlı bir planla, yeni çalışanlara 80 saatlik ödeme zamanı (PTO) kazanabilecek bir avantaj verebilirsiniz. Daha sonra 60 aylık hizmetin 120 saatini sağlayabilirsiniz.

Ayrıca, yalnızca Yöneticiler için olan kazanç saatleri gibi, pozisyonlara dayalı olarak izin verebilirsiniz.

## <a name="create-a-leave-plan"></a>İzin planı oluştur

1. **İzin ve devamsızlık planları** sayfasında, **Yeni plan oluştur** üzerine tıklayın.

2. **Ayrıntılar** altında, planınız için **adı**, **başlangıç tarihini**, **açıklamasını** ve **ayrılma türünü** girin.

**Tek bir izin ve devamsızlık planı için birden fazla izin türü yapılandır** özelliği etkinse, izin türleri **Ayrıntılar** yerine **Tahakkuk planı** altında yapılandırılır. Tahakkuk çizelgesi tablosundaki her kayıt için, bir izin türü tanımlayabilirsiniz. Ayrıca, bu özellik etkinleştirildiğinde, tümleştirmeler veya varlıklar kullanmanız gereken başka senaryolar için yeni veri varlıkları kullanmanız gerekir. 

Yeni varlıklar şunlardır:

- İzin ve devamsızlık banka hareketi V2
- İzin ve devamsızlık kaydı V2
- İzin ve devamsızlık planı katmanı V2
- İzin ve devamsızlık planı V2
- İzin süresi isteği V2

 > [!IMPORTANT]
   > Bu özelliği etkinleştirdikten sonra kapatabilirsiniz.

3. **Tahakkukları** sekmesinde tahakkukları tanımlayın. Tahakkukları, bir çalışana ne kadar hangi sıklıkta izin vereceğini belirler. Bu adımda, tahakkukları ne zaman kazanıyorsanız ve eşit olma kazandıklarının politikalarını öğrenmek için ilkeler tanımlarsınız.

   1. **Tahakkuk sıklığı** açılır kutusundan bir değer seçin:

      - Günlük
      - Haftalık
      - İki Haftalık
      - 15 günlük
      - Aylık
      - Üç Aylık
      - Yarı yıllık
      - Yıllık
      - Hiçbiri

   2. Tahakkuk dönemlerini hesaplamak için kullanılan başlangıç tarihini belirlemek için **tahakkuk dönemi esası** açılır kutusundan bir seçenek belirleyin:

      | Tahakkuk dönemi esası | Tanım |
      | --- | --- |
      | **Plan başlangıç tarihi** | Tahakkuk dönemi başlangıç tarihi, planın kullanılabilir olduğu tarihtir. |
      | **Personele özgü tarih** | Tahakkuk dönemi başlangıç tarihi bir çalışan olayına bağlıdır:</br><ul><li>Özel (her bir kayıt için bir tahakkuk tarihi temeli belirtmeniz gerekir)</li><li>Yıldönümü tarihi</li><li>Orijinal işe alma tarihi</li><li>Kıdem tarihi</li><li>Çalışanın ayarlanan başlama tarihi</li><li>Çalışanın başlama tarihi</li></ul> |

   3. **Tahakkuk ikramiye tarihi** açılır kutusunda bir seçenek belirleyin:

      - **Tahakkuk dönemi bitiş tarihi** - Personele, verilme döneminin son gününde izin verilecektir. Doğru değeri tahakkuk etmek için tahakkuk işleminin dönemin tamamını içermesi gerekir. Örneğin, tahakkuk dönemi 1 Ocak 2020 ile 31 Ocak 2020 arasında ise, 1 Şubat 2020 için tahakkuku çalıştırıp Ocak ayına dahil etmelisiniz.

      - **Tahakkuk dönemi başlangıç tarihi** - Personele, verilme döneminin ilk gününde izin verilecektir.

   4. **Kayıtta tahakkuk ilkesi** açılır kutusunda bir seçenek belirleyin. Bu değer, bir çalışan bir tahakkuk dönemi ortasına geldiğinde tahakkuk hesaplamanın nasıl hesaplanacağını tanımlar.

      - **Dağıtılmış** - Kayıt tarihi ve başlangıç tarihi arasındaki tarih aralığı, farkı gün olarak belirlemek için kullanılır. Fark, tahakkuklar işlendiğine uygulanır.

      - **Tam tahakkuk** - Tam tahakkuk tutarı, katmana dayalı olarak ilk tahakkuk işlemesi sırasında verilir.

      - **Tahakkuk yok** - Bir sonraki tahakkuk dönemine kadar hiç tahakkuk verilmez.

   5. **Kayıt silme tahakkuk ilkesi** açılır kutusunda bir seçenek belirleyin. Bu değer, bir çalışan bir tahakkuk dönemi ortasında kayıt silerken tahakkuk hesaplamanın nasıl hesaplanacağını tanımlar.

      - **Dağıtılmış** - Kayıt tarihi ve başlangıç tarihi arasındaki tarih aralığı, farkı gün olarak belirlemek için kullanılır. Fark, tahakkuklar işlendiğine uygulanır.

      - **Tam tahakkuk** - Tam tahakkuk tutarı, katmana dayalı olarak ilk tahakkuk işlemesi sırasında verilir.

      - **Tahakkuk yok** - Bir sonraki tahakkuk dönemine kadar hiç tahakkuk verilmez.

4. **Tahakkuk çizelgesi** sekmesinde, tahakkuk planını tanımlayın. Tahakkuk çizelgesi şunları belirler:

   - Bir çalışan nasıl zaman tahakkuk eder
   - Çalışanın tahakkuk yaptığı tutarlar
   - İletilecek tutarlar

   Katmanlar, iznin farklı düzeylere dayanarak verilmesi için oluşturulabilir.

   Saatlik çalışanı olan kuruluşlar, kuruluştaki kıdem yerine çalışılan saatlere dayanarak izin verebilirler. Çalışılan saatler verisi genellikle bir zaman ve katılım sisteminde depolanır. Zaman ve katılımcı sisteminden çalışılan normal ve fazla mesai saatlerini içe aktarabilir ve bunları bir çalışanın Ödülü için temel olarak kullanabilirsiniz.
   
    1. **Tahakkuk türü** açılır kutusunda bir seçenek belirleyin:

      - **Servis ayları** - Tahakkuk planının servis ayları için matrah.

      - **Çalışılan saat** - Tahakkuk planını çalışılan saatlere dayandırın. Çalışılan saatlerin tahakkukları hakkında daha fazla bilgi için bkz. [Çalışılan saatlere bağlı tahakkuk süresi](hr-leave-and-absence-plans.md?accrue-time-off-based-on-hours-worked).

      Tahakkuk bakiyeleri hakkında daha fazla bilgi için bkz. [Çalışılan saatlere bağlı tahakkuk süresi](hr-leave-and-absence-plans.md?enrollments-and-balances).

    2. Tahakkuk çizelgesi tablosuna değerleri girin:

      - **Hizmet ayı** - Personelin tahakkuk hakkı kazanabilmesi için çalışması gereken minimum ay sayısını belirtir. En azından bir minimum gereksinim duymuyorsanız, değeri 0 olarak ayarlayın.

      - **Çalışılan saatler** - Personelin tahakkuk hakkı kazanabilmesi için tahakkuk başına çalışması gereken minimum saat sayısını belirtir. En azından bir minimum gereksinim duymuyorsanız, değeri 0 olarak ayarlayın.

      - **Tahakkuk tutarı** - Saat veya gün cinsinden çalışanların tahakkuk numarasıdır dönem başına düşen. Dönem, tahakkuk sıklığını temel alır.

      - **Minimum bakiye** - Bir negatif değer, minimum bakiye için kullanılabilir, eğer personel kullanılabilir sahip olduğundan daha fazla izin talep ederse.

      - **Maksimum iletme** - Tahakkuk işlemi, başlangıç tarihinin yıl dönümündeki maksimum ileri taşıma bakiyesini aşan izin bakiyelerini ayarlar.

      - **Verilen tutar** - İzin planına ilk kaydolduklarında personele verilen saat veya günün ilk sayısıdır. Tutar, her bir tahakkuk dönemi için tahakkuk edilmez.
      
**Tek bir izin ve devamsızlık planı için birden fazla izin türü yapılandır** özelliği etkinse **İzin türü**'nden bir seçenek belirleyin. 

   > [!IMPORTANT]
   > Bu özelliği etkinleştirdikten sonra kapatabilirsiniz.

**Tam zamanlı eşdeğerini kullan** özelliği etkinde, Human Resources bir çalışanın tahakkukunu eşit şekilde dağıtmak üzere pozisyon için tanımlanan tam zamanlı eşedeğeri (FTE) kullanır. Örneğin, FTE .5 ise ve tahakkuk tutarı 10 ise, çalışan 5'i tahakkuk eder. Bu özelliği yalnızca birden fazla izin türünü etkinleştirirseniz kullanabilirsiniz.  

5. **Kaydet**'i seçin.

## <a name="accrue-time-off-based-on-hours-worked"></a>Çalışılan saatlere göre tahakkuk eden süre

Saatlik çalışanı olan kuruluşlar, kuruluştaki kıdem yerine çalışılan saatlere dayanarak izin verebilirler. Çalışılan saatler verisi genellikle bir zaman ve katılım sisteminde depolanır. Zaman ve katılımcı sisteminden çalışılan normal ve fazla mesai saatlerini içe aktarabilir ve bunları bir çalışanın Ödülü için temel olarak kullanabilirsiniz.

Çalışılan saatler tahakkuk türü olarak seçildiğinde, tahakkuk için kullanılacak iki saat türü vardır: normal ve fazla mesai. Çalışılan saatler planları için tahakkuk işleme, tahakkuk sıklığını, tahakkuk dönemi tabanı ile kullanarak tahakkuk edilecek saatleri belirlemek için kullanır.

### <a name="annual-accrual-frequency"></a>Yıllık tahakkuk sıklığı

| Tahakkuk verilme tarihi    | Çalışılan saatler katmanı    | Tahakkuk tutarı        | Çalışan saatlerin tarihi   | Çalışılan gerçek saatler| İkramiye               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/12/2018            | 2080                 | 144                   | 1/1/2018-31/12/2018  | 2085                | 144                 |        
| 31/12/2018            | 2080                 | 144                   | 1/1/2018-31/12/2018  | 2000                | 0                 |


### <a name="monthly-accrual-frequency"></a>Aylık tahakkuk sıklığı

| Tahakkuk verilme tarihi    | Çalışılan saatler katmanı    | Tahakkuk tutarı        | Çalışan saatlerin tarihi   | Çalışılan gerçek saatler| İkramiye               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 1/8/2018-31/8/2018   | 184                 | 12                  |        
| 31/8/2018             | 160                  | 3                     | 1/8/2018-31/8/2018   | 184                 | 3                   |

### <a name="semi-monthly-accrual-frequency"></a>Ayda iki kez tahakkuk sıklığı

| Tahakkuk verilme tarihi    | Çalışılan saatler katmanı    | Tahakkuk tutarı        | Çalışan saatlerin tarihi   | Çalışılan gerçek saatler| İkramiye               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/8/2018             | 80                   | 6                     | 16/8/2018-31/8/2018  | 81                  | 6                  |        
| 31/8/2018             | 80                   | 6                     | 16/8/2018-31/8/2018  | 75                  | 0                   |

### <a name="weekly-accrual-frequency"></a>Haftalık tahakkuk sıklığı

| Tahakkuk verilme tarihi    | Çalışılan saatler katmanı    | Tahakkuk tutarı        | Çalışan saatlerin tarihi   | Çalışılan gerçek saatler| İkramiye               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/8/2018             | 40                   | 3                     | 27/8/2018-31/8/2018  | 42                  | 3                  |        
| 31/8/2018             | 40                   | 3                     | 27/8/2018-31/8/2018  | 35                  | 0                   |

### <a name="employee-assigned-leave-plans"></a>Personel atanan izin planları

Personelin atanan izin planlarında, katman tabanı ve saatlerin türü, çalışılan saatlerin plnları gösterilir. Tahakkuk dönemlerinin gerçek çalışma saatleri de geçerli tarih itibariyle etkin planlar için görüntülenir.

### <a name="loading-data"></a>Veriler yükleniyor

Gerçek saatler, veri yönetimindeki **izin ve devamsızlık saatleri çalışılan** varlığı kullanılarak içe aktarılabilir. Çalışma saati takvimleri kullanıyorsanız, içe aktarma normal saatlerin takvim tarafından tanımlanan planlanmış saatleri aşmayacağı doğrulayacaktır. İçe aktarma ayrıca bir gündeki çalışılan saatlerin 24'ü geçmemesini de doğrular. 

Aşağıdaki bilgiler gerçek saatlerin izin tahakkuk işleminde kullanılabilmesi için içe aktarılmasında gereklidir:

- Personel numarası 
- Çalışılan tarih
- Türü
- Saatler

Tek bir tarih yalnızca bir tipi ilişkilendirilmiş olabilir.

| Personel numarası       | Çalışılan tarih           | Türü                  | Saatler                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 6/8/2018             | Normal               | 8                    |       
| 000337                | 7/8/2018             | Normal               | 8                    |
| 000337                | 7/8/2018             | Fazla mesai              | 3                    |
| 000337                | 8/8/2018             | Normal               | 8                    |
| 000337                | 7/8/2018             | Normal               | 8                    |
| 000337                | 9/8/2018             | Normal               | 8                    |

## <a name="enrollments-and-balances"></a>Kayıtlar ve bakiyeler

### <a name="enrollment-date"></a>Kayıt tarihi

Kayıt tarihi, bir personelin izin tahakkuk etmeye başlayabileceği tarihi belirtir. Örneğin, bir personel bir tatil planına 15 Haziran 2018 tarihinde kaydolduysa, 15 Haziran 2018 tarhinden önce herhangi bir süre tahakkuk edemez.

### <a name="current-balance"></a>Geçerli bakiye

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

İnsan Kaynakları aşağıdaki formülü kullanır:

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
| Jeannette Nicholson | 0,00              | 01/06/2018        | 01/06/2018   | 1.00           | 01/09/2018        | 3.00    |
| Jay Norman          | 0,00              | 15/06/2018       | 15/06/2018  | 1.00           | 01/09/2018        | 2.00    |

## <a name="see-also"></a>Ayrıca bkz.

- [İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)
- [İzin ve devamsızlık türlerini yapılandırma](hr-leave-and-absence-types.md)
- [İzin ve devamsızlık planları tahakkuk etme](hr-leave-and-absence-accrue.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]