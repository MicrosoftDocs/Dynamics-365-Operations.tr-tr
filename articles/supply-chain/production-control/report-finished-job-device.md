---
title: İş kartı cihazından tamamlandı olarak bildirme
description: Bu konuda, bir iş kartı kullanıcıları bir üretim emrinden stoka bitmiş ürünleri raporlenebilecek şekilde sistemi konfigüre etme yöntemi açıklanmıştır.
author: johanhoffmann
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 2fa82c721316fb21442e1cfc00ba00ff8cb2b750
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778243"
---
# <a name="report-as-finished-from-the-job-card-device"></a>İş kartı cihazından tamamlandı olarak bildirme

[!include [banner](../includes/banner.md)]

Çalışanlar, bir üretim işi için tamamlanan miktarları bildirmek üzere, iş kartı aygıtındaki **rapor ilerleme** sayfasını kullanır. Bu konuda, çalışanların bu sayfayı kullanarak tamamlandı olarak nasıl bildirme ile ilgili çeşitli seçeneklerin nasıl ayarlanacağı ve sonraki işlemler açıklanmaktadır. Seçenekler arasında bulunanlar:

- Tamamlandı olarak bildirilen miktarların stoka eklenip eklenmeyeceğini ve nasıl ekleneceğini denetleme.
- Tamamlandı bildirimi yapılırken, toplu iş numaralarının oluşturulup oluşturulmayacağını ve nasıl uygulanacağını denetleme.
- Tamamlandı bildirimi yapılırken, seri numaralarının oluşturulup oluşturulmayacağını ve nasıl uygulanacağını denetleme.
- Bir plakaya tamamlandı bildirimi yapılıp yapılmayacağını ve nasıl yapılacağını denetleme.

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>Tamamlandı olarak rapor edilen miktarların stoğa eklenip eklenmeyeceğini denetleme

Son operasyonda tamamlandı olarak rapor edilen miktarların stoğa eklenmesi gerekip alınıp alınmayacağını denetlemek için, aşağıdaki adımları izleyin.

1. **Üretim denetimi \> Kurulum \> Üretim yürütme \> Üretim emri varsayılanları** öğesine tıklayın.
1. **Tamamlandı bildirimi** sekmesinde, **güncelleştirme tamamlandı raporu çevrimiçi** alanını aşağıdaki değerlerden birine ayarlayın:

    - **Hayır** – Son operasyonda miktar raporlandığında stoğa hiçbir miktar eklenmez. Üretim emrinin durumu hiçbir zaman değişmeyecek.
    - **Durum + Miktar** - Üretim emrinin durumu *tamamlandı bildirimi* olarak değişecektir ve miktar stoka tamamlandı olarak bildirilir.
    - **Miktar** - Miktar, envantere durumu tamamlandı bildirimi olarak değişecektir ancak üretim emri asla değişmez.
    - **Durum** - Yalnızca Üretim emrinin durumu değişir. Son operasyonda miktar raporlandığında stoğa hiçbir miktar eklenmez.

> [!NOTE]
> Tamamlandı olarak raporlandığı operasyonlar son operasyon olarak tanımlanmazsa, miktarlar stokta izlenmiyor. Ancak, ilerlemeyi görüntülemek için bu miktarlar kullanılabilir. Bunlar aynı zamanda, önceki operasyonda bildirilen rapor edilen bir eşiğe ulaşılmadan önce çalışanların sonraki operasyonu başlatıp başlatmayacağını denetleyen kurallara dahil edilebilir. Bu kuralları , **üretim emri Varsayılanları** sayfasının **miktar doğrulama** sekmesinde tanımlayabilirsiniz.

**Üretim emri Varsayılanları** sayfasıyla nasıl çalışılacağı hakkında daha fazla bilgi için [üretim yürütmesindeki üretim parametrelerine](production-parameters-manufacturing-execution.md) bakın.

## <a name="report-batch-controlled-items-as-finished"></a>Toplu denetimli maddeleri tamamlandı olarak raporla

İş kartı aygıtı toplu iş maddelerini raporlamak için üç senaryoyu destekler. Bu senaryolar, hem Gelişmiş ambar süreçleri için etkinleştirilen maddelere hem de Gelişmiş ambar işlemleri için etkinleştirilmemiş maddelere uygulanır.

- **El ile atanan toplu iş numaraları:** Çalışanlar özel bir toplu iş numarası girin. Bu toplu iş numarası, sistemde bilinmeyen bir harici kaynaktan gelebilir.
- **Önceden tanımlı toplu iş numaraları:** Çalışanlar, üretim emri iş kartı aygıtında serbest bırakılmadan önce sistemin otomatik olarak oluşturduğu toplu iş numaraları listesinde bir toplu iş numarası seçer.
- **Sabit toplu iş numaraları:** Çalışanlar toplu iş numarası girmez veya seçmez. Bunun yerine, sistem üretim emrine serbest bırakılmadan önce bir toplu iş numarası atar.


### <a name="enable-the-feature-on-your-system"></a>Sisteminizde özelliği etkinleştirme

İş kartı aygıtlarınızın tamamlandı bildirimi sırasında bir toplu iş numarası kabul etmesini sağlamak için, [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanarak aşağıdaki özellikleri (Bu sırada) açmanız gerekir:

1. İş Kartı Cihazındaki Rapor ilerlemesi iletişim kutusu için geliştirilmiş kullanıcı deneyimi.
1. İş Kartı Cihazında iş sona erdi bildirimi yaparken toplu iş ve seri numaralarını girmek için etkinleştirin

### <a name="configure-products-that-require-batch-number-reporting"></a>Toplu numara bildirimi gerektiren ürünleri yapılandırma

Bir ürünün, kullanılabilir olan toplu iş denetimli senaryolarından herhangi birini desteklemesini sağlamak için şu adımları izleyin:

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Yapılandırmak istediğiniz ürünü seçin.
1. **Stoğu Yönet** hızlı sekmesinde, **toplu iş numarası grubu** alanında, senaryonuzu destekleyecek izleme numara grubunu seçin.

> [!NOTE]
> Varsayılan olarak, toplu denetlenen bir ürüne toplu iş numarası grubu atanmamışsa, iş kartı aygıtı tamamlandı bildirimi sırasında toplu iş numarası için el ile giriş sağlar.

Aşağıdaki bölümler, toplu iş öğelerinde raporlama için üç senaryonun her birini desteklemek üzere izleme numarası gruplarının nasıl ayarlanacağını açıklar.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Çalışanlarınızın el ile bir toplu iş numarası atayabilmesine olanak veren bir izleme numarası grubu ayarla

El ile atanan toplu iş numaralarına izin vermek için, bir izleme numarası grubu ayarlamak üzere aşağıdaki adımları izleyin.

1. **Stok Yönetimi \> Kurulum \> Boyut \> zleme numara gruplarına** gidin.
1. Ayarlanacak izleme grubu grubunu oluşturun veya seçin.
1. **Genel** hızlı sekmesinde, **Manuel** seçeneğini **Evet** olarak ayarlayın.

    ![El ile toplu iş numaraları için izleme numarası grubu.](media/tracking-number-group-manual.png "El ile toplu iş numaraları için izleme numarası grubu")

1. İstediğiniz şekilde diğer değerleri ayarlayın, sonra da bu senaryoyu kullanmak istediğiniz serbest bırakılan Ürünler için toplu iş numarası grubu olarak bu izleme numara grubunu seçin.

Bu senaryoyu kullandığınızda, iş kartı aygıtında **durumu raporla** sayfasının sağladığı **toplu iş numarası** alanı çalışanların herhangi bir değer girebildiği bir metin kutusudur.

![El ile toplu iş numarası için alan bulunan ilerleme raporu sayfası.](media/job-card-device-batch-manual.png "El ile toplu iş numarası için alan bulunan ilerleme durumu sayfasını raporla")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Önceden tanımlanmış toplu iş numaralarının listesini sağlayan bir izleme numarası grubu ayarla

Önceden tanımlanmış toplu iş numaraları listesi sağlamak için bir izleme numarası grubu ayarlamak üzere aşağıdaki adımları izleyin.

1. **Stok Yönetimi \> Kurulum > Boyut \> İzleme numara gruplarına** gidin.
1. Ayarlanacak izleme grubu grubunu oluşturun veya seçin.
1. **Genel** hızlı sekmesinde, **Yalnızca envanter işlemleri için** seçeneğini **Evet** olarak ayarlayın.
1. Miktar bazında toplu iş numaralarını, girdiğiniz değere göre, **Her miktarda** ayırmak için kullanın. Örneğin, on parça için bir üretim emri, **Her miktar** alanı *2* olarak ayarlanmıştır. Bu durumda üretim emrine oluşturulurken beş toplu iş numarası atanacaktır.

    ![Ön tanımlı toplu iş numaraları için izleme numarası grubu.](media/tracking-number-group-predefined.png "Ön tanımlı toplu iş numaraları için izleme numarası grubu")

1. İstediğiniz şekilde diğer değerleri ayarlayın, sonra da bu senaryoyu kullanmak istediğiniz serbest bırakılan Ürünler için toplu iş numarası grubu olarak bu izleme numara grubunu seçin.

Bu senaryoyu kullandığınızda, iş kartı aygıtında **durumu raporla** sayfasının sağladığı **toplu iş numarası** alanı çalışanların önceden tanımlanan değer girebildiği bir açılır listedir.

![Önceden tanımlanan toplu iş numaraları listesi için alan bulunan ilerleme raporu sayfası.](media/job-card-device-batch-predefined.png "Önceden tanımlanan toplu iş numaraları listesi için alan bulunan ilerleme durumu sayfasını raporla")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Otomatik olarak toplu iş numarası atayabilmesine olanak veren bir izleme numarası grubu ayarla

Toplu iş numaralarının çalışan girişi olmadan otomatik olarak atanması gerekiyorsa, bir izleme numarası grubu ayarlamak için aşağıdaki adımları izleyin.

1. **Stok Yönetimi \> Kurulum \> Boyut \> zleme numara gruplarına** gidin.
1. Ayarlanacak izleme grubu grubunu oluşturun veya seçin.
1. **Genel** hızlı sekmesinde, **Yalnızca envanter işlemleri için** seçeneğini **Hayır** olarak ayarlayın.
1. **Manuel** seçeneğini **Hayır** olarak ayarlayın.

    ![Sabit toplu iş numaraları için izleme numarası grubu.](media/tracking-number-group-fixed.png "Sabit toplu iş numaraları için izleme numarası grubu")

1. İstediğiniz şekilde diğer değerleri ayarlayın, sonra da bu senaryoyu kullanmak istediğiniz serbest bırakılan Ürünler için toplu iş numarası grubu olarak bu izleme numara grubunu seçin.

Bu senaryoyu kullandığınızda, iş kartı aygıtında **durumu raporla** sayfasının sağladığı **toplu iş numarası** alanı bir değer gösterir ancak çalışanlar düzenleymez.

![Sabit toplu iş numarası ile ilerleme raporu sayfası.](media/job-card-device-batch-fixed.png "Sabit toplu iş numarası ile ilerleme durumu sayfasını raporla")

## <a name="report-serial-controlled-items-as-finished"></a>Seri denetimli kalemleri tamamlandı olarak bildirme

İş kartı cihazı seri denetimli kalemleri bildirmek için üç senaryoyu destekler. Bu senaryolar, hem Gelişmiş ambar süreçleri için etkinleştirilen maddelere hem de Gelişmiş ambar işlemleri için etkinleştirilmemiş maddelere uygulanır.

- **El ile atanan seri numaralar:** Çalışanlar özel bir seri numarası girin. Bu seri numarası, sistemde bilinmeyen bir harici kaynaktan gelebilir.
- **Önceden tanımlı seri numaraları:** Çalışanlar, üretim emri iş kartı cihazında serbest bırakılmadan önce sistemin otomatik olarak oluşturduğu seri numaraları listesinde bir seri numarası seçer.
- **Sabit seri numaraları:** Çalışanlar seri numarası girmez veya seçmez. Bunun yerine, sistem üretim emrine serbest bırakılmadan önce bir seri numarası atar.

### <a name="enable-the-feature-on-your-system"></a>Sisteminizde özelliği etkinleştirme

İş kartı aygıtlarınızın tamamlandı bildirimi sırasında bir seri numarası kabul etmesini sağlamak için, [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanarak aşağıdaki özellikleri (Bu sırada) açmanız gerekir:

1. İş Kartı Cihazındaki Rapor ilerlemesi iletişim kutusu için geliştirilmiş kullanıcı deneyimi.
1. İş Kartı Cihazında iş sona erdi bildirimi yaparken toplu iş ve seri numaralarını girmek için etkinleştirin

### <a name="configure-products-that-require-serial-number-reporting"></a>Seri numarası bildirimi gerektiren ürünleri yapılandırma

Bir ürünün, kullanılabilir olan seri denetimli senaryolarından herhangi birini desteklemesini sağlamak için şu adımları izleyin:

Her Senaryoyu etkinleştirmek için şu adımları izleyin.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Yapılandırmak istediğiniz ürünü seçin.
1. **Stoku Yönet** hızlı sekmesinde, **Seri numarası grubu** alanında, senaryonuzu destekleyecek izleme numara grubunu seçin.

> [!NOTE]
> Varsayılan olarak, seri denetimli bir ürüne seri numarası grubu atanmamışsa, iş kartı cihazı tamamlandı bildirimi sırasında seri numarası için el ile giriş sağlar.

Aşağıdaki bölümler, seri denetimli öğelerde bildirim için üç senaryonun her birini desteklemek üzere izleme numarası gruplarının nasıl ayarlanacağını açıklar.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-serial-number"></a>Çalışanlarınızın el ile bir seri numarası atayabilmesine olanak veren bir izleme numarası grubu ayarlama

El ile atanan seri numaralarına izin vermek için, bir izleme numarası grubu ayarlamak üzere aşağıdaki adımları izleyin.

1. **Stok Yönetimi \> Kurulum \> Boyut \> zleme numara gruplarına** gidin.
1. Ayarlanacak izleme grubu grubunu oluşturun veya seçin.
1. **Genel** hızlı sekmesinde, **Manuel** seçeneğini **Evet** olarak ayarlayın.

    ![Numara gruplarını izleme sayfası, seri numaraları.](media/tracking-number-group-manual-serial.png "Numara gruplarını izleme sayfası, seri numaraları")

1. İstediğiniz şekilde diğer değerleri ayarlayın, sonra da bu senaryoyu kullanmak istediğiniz serbest bırakılan ürünler için seri numarası grubu olarak bu izleme numara grubunu seçin.

Bu senaryoyu kullandığınızda, iş kartı cihazında **İlerlemeyi bildir** sayfasının sağladığı **Seri numarası** alanı çalışanların seri numarası için herhangi bir değer girebildiği bir metin kutusudur. Değer girerken, seri numarası listesine eklenir. Bu listede, çalışanlar aşağıdakileri yapabilir:

- Bir seri numarasını ıskartaya ayrılmış olarak işaretlemek için uygun satır için **Iskartaya ayır** düğmesini seçin. Çalışanın **Hata nedeni** sağlaması istenir.
- Bir seri numarasını silmek için uygun satır için **Sil** düğmesini seçin.

![El ile seri numarası için alan bulunan ilerleme raporu sayfası.](media/job-card-device-serial-manual.png "El ile seri numarası için alan bulunan ilerleme durumunu bildirme sayfası")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-serial-numbers"></a>Önceden tanımlanmış seri numaralarının listesini sağlayan bir izleme numarası grubu ayarlama

Önceden tanımlanmış seri numaraları listesi sağlamak için bir izleme numarası grubu ayarlamak üzere aşağıdaki adımları izleyin.

1. **Stok Yönetimi \> Kurulum \> Boyut \> zleme numara gruplarına** gidin.
1. Ayarlanacak izleme grubu grubunu oluşturun veya seçin.
1. **Genel** hızlı sekmesinde, **Yalnızca envanter işlemleri için** seçeneğini **Evet** olarak ayarlayın.
1. Miktar başına seri numaralarını ayırmak için **Miktar başına** alanını kullanın.

    ![Ön tanımlı seri numaraları için izleme numarası grubu.](media/tracking-number-group-predefined-sn.png "Ön tanımlı seri numaraları için izleme numarası grubu")

1. İstediğiniz şekilde diğer değerleri ayarlayın, sonra da bu senaryoyu kullanmak istediğiniz serbest bırakılan ürünler için seri numarası grubu olarak bu izleme numara grubunu seçin.

Bu senaryoyu kullandığınızda, iş kartı cihazında **Durumu bildir** sayfasının sağladığı **Seri numarası** alanı çalışanların önceden tanımlanan değer girebildiği bir açılır listedir.

![Önceden tanımlanan seri numaraları listesi için alan bulunan ilerleme raporu sayfası.](media/job-card-device-serial-predefined.png "Önceden tanımlanan seri numaraları listesi için alan bulunan ilerleme durumunu bildirme sayfası")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-serial-numbers"></a>Otomatik olarak seri numarası atayabilmesine olanak veren bir izleme numarası grubu ayarlama

Seri numarasının çalışan girişi olmadan otomatik olarak atanması gerekiyorsa, bir izleme numarası grubu ayarlamak için aşağıdaki adımları izleyin.

1. **Stok Yönetimi \> Kurulum \> Boyut \> zleme numara gruplarına** gidin.
1. Ayarlanacak izleme grubu grubunu oluşturun veya seçin.
1. **Genel** hızlı sekmesinde, **Yalnızca envanter işlemleri için** seçeneğini **Hayır** olarak ayarlayın.
1. **Manuel** seçeneğini **Hayır** olarak ayarlayın.

    ![Sabit seri numaraları için izleme numarası grubu.](media/tracking-number-group-fixed-sn.png "Sabit seri numaraları için izleme numarası grubu")

1. İstediğiniz şekilde diğer değerleri ayarlayın, sonra da bu senaryoyu kullanmak istediğiniz serbest bırakılan ürünler için seri numarası grubu olarak bu izleme numara grubunu seçin.

Bu senaryoyu kullandığınızda, iş kartı cihazında **Durumu bildir** sayfasının sağladığı **Seri numarası** alanı bir değer gösterir ancak çalışanlar düzenleyemez. Bu senaryo yalnızca seri numarası denetimli bir kalemin bir parçasının miktarı için üretim emri oluşturulduğunda geçerlidir.

![Sabit seri numarası bulunan ilerleme raporu sayfası.](media/job-card-device-serial-fixed.png "Sabit seri numaraları ile ilerleme durumunu bildirme sayfası")

## <a name="report-as-finished-to-a-license-plate"></a>Lisans plakasına tamamlandı olarak raporlama

Gelişmiş ambar işlemleri, bu amaçla ayarlanmış ambar yerleşimlerinde bulunan stoğu izlemek için, lisans levhası boyutunu kullanabilir. Bu durumda, bir çalışanın tamamlandığı miktarları raporladığında, lisans levhası numarası gereklidir.

### <a name="enable-license-plate-reporting-and-label-printing"></a>Raporlama ve Plaka etiketi yazdırmayı etkinleştirme

Bu bölümde anlatılan özellikleri kullanmak için, [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanarak aşağıdaki özellikleri (Bu sırada) açmanız gerekir:

1. İş Kartı Cihazına eklenme işi tamamlandı bildirimi için plaka (Supply Chain Management sürüm 10.0.21'den itibaren bu özellik varsayılan olarak etkindir.)
1. İş kartı cihazında tamamlandı olarak bildirme sırasında otomatik plaka numarası oluşturmayı etkinleştirin
1. İş Kartı Cihazından etiket yazdır

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a>Lisans plakasına tamamlandı olarak raporlamayı ayarla

Çalışanların varolan bir lisans plağı 'nı yeniden kullanması veya miktarları tamamlandı olarak raporlarına yeni bir lisans plağı oluşturup oluşturmayacağını denetlemek için aşağıdaki adımları izleyin.

1. **Üretim denetimi \> Ayarlar \> Üretim yürütme \> Cihazlar için iş kartını konfigüre et**'e gidin.
2. Her aygıt için aşağıdaki seçenekleri belirleyin:

    - **Lisans levhasını oluştur** - Her tamamlandı bildirimi oluşturmak için bu seçeneği **Evet** olarak ayarlayın. Her bir rapor tamamlandı bildirimi için mevcut bir lisans kalıbının kullanılması gerekiyorsa **Hayır** olarak ayarlayın.
    - **Etiket Yazdır** - bir çalışan bir çalışma tamamlandı bildirimi yapmak için bu seçeneği **Evet** olarak ayarlayın. Etiket gerekmiyorsa **Hayır** olarak ayarlayın. 

![Cihazlar için iş kartını yapılandırma sayfası.](media/config-job-card-raf.png "Cihazlar için iş kartını yapılandırma sayfası")

> [!NOTE]
> Etiekt yapılandırmak içni **Ambar Yönetimi \> Kurulum \> Belge yönlendirme \> Belge yönlendirme**'ye gidin. Daha fazla bilgi için, bkz [Lisans plaka etiket yazdırmayı etkinleştir](../warehousing/tasks/license-plate-label-printing.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]