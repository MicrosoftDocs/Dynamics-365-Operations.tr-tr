---
title: Microsoft Dynamics 365 Talent önizleme özelliklerine erişme
description: Bu konu Microsoft Dynamics 365 Talent içindeki önizleme özelliklerini bir yöneticinin nasıl etkinleştirebileceğini tanımlar ve önizleme için etkin olan özellikleri listeler.
author: tracykeya
manager: AnnBe
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 0f9a83aeea3942d3c56d32956f79490c91565e9e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551622"
---
# <a name="access-preview-features-in-microsoft-dynamics-365-talent"></a>Microsoft Dynamics 365 Talent önizleme özelliklerine erişme

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 Talent için sürekli olarak kullanıma sunduğumuz insan sermayesi yönetim döngüsü (HCM) özelliklerinin bir parçası olarak, müşterilerimizin yeni özellikleri mümkün olan en kısa sürede deneyimlemesini istiyoruz. Yöneticiler önizleme özelliklerini kendi ortamlarında görebilir ve kullanabilir. Bu özellikler neredeyse genel kullanıma sunulmak üzere hazır durumdadır ve kapsamlı bir sınamadan geçirilmiştir. Bu özellikleri genel kullanım için yayımlamadan önce müşterilerimizden son kez geribildirim almak istiyoruz.

Bu konu önizleme özelliklerini nasıl etkinleştirebileceğinizi tanımlar ve önizleme için kullanılabilir olan özellikleri listeler. Bu liste özellikler genel kullanım için yayımladıkça ve yeni özellikler önizleme için yayımlandıkça güncelleştirilecektir. Yeni özellikler önizleme için yayımlandığında bildirim gönderilmeyecektir. Kullanıcılar özellikleri görmeye başlayacaktır. Talent içindeki yeni özellikler hakkında daha fazla bilgi için bkz. [Dynamics 365 Talent içinde neler yeni veya değişti](./whats-new.md) ve [Dynamics 365 ve Power Platform Sürüm Notları](https://docs.microsoft.com/business-applications-release-notes).

## <a name="enable-or-disable-preview-features"></a>Önizleme özelliklerini etkinleştirme veya devre dışı bırakma

Önizleme özelliklerine erişmek için, önce ortamınızda etkinleştirmeniz gerekir. Önizleme özelliklerini devre dışı bırakma veya etkinleştirme ortama özgüdür.

> [!IMPORTANT]
> **Önizleme özellikleri** ayarını açtığınızda, kuruluşunuzda bulunan bu ortamdaki tüm kullanıcılar için önizleme özelliklerini etkinleştirirsiniz. Ayarı kapattığınızda, önizleme özelliklerini devre dışı bırakırsınız ve kullanıcılarınız bu özelliklere erişemez. Önizleme özellikleri Talent'ta sınırlı şekilde desteklenir. Daha az gizlilik ve güvenlik önemi kullanabilirler ve Talent hizmet düzeyi sözleşmene (SLA) dahil değildirler. Kişisel verileri (diğer bir deyişle, sizi tanımlamaya yardımcı olabilecek tüm bilgileri) işlemek ya da yasa veya düzenlemelerle uyumluluk gereksinimlerine tabi olan diğer verileri işlemek için önizleme özelliklerini kullanmamanız gerekir.

### <a name="attract"></a>Attract

1. Microsoft Dynamics 365 Talent: Attract'ta oturum açın.
2. Sağ üst köşedeki **Kurulum** menüsünden (çark simgesi) **Yönetici merkezi**'ni seçin.
3. **Özellik yönetimi** sekmesinde **Önizleme özellikleri** yanındaki seçeneği seçin. Seçildiğinde mavi renge dönecektir ve **Açık** ibaresini görüntüleyecektir.

    ![Attract içinde önizleme özelliklerini etkinleştirme](./media/attract-enable-preview-features.png)

4. Bireysel önizleme özellikleri seçimini seçin veya iptal edin. Hiçbir şey yapmazsanız, varolan tüm önizleme özellikleri etkinleştirilir.
5. Yeni özellikleri görmek için tarayıcınızı yenileyin. Zaten oturum açmış kullanıcılar özellikleri daha sonra yeniden oturum açtıklarında görürler veya özellikleri hemen görmek için tarayıcıyı yenileyebilirler.

> [!NOTE]
> Bazı önizleme özellikleri için ek konfigürasyon gerekebilir. Kurulum işleminin tamamlanması için önizleme özelliğinin yanındaki bağlantıları izleyin.

### <a name="core-hr"></a>Temel İK

1. Talent'ta oturum açın.
2. **Sistem yönetimi**'ni ve sonra **Bağlantılar** sekmesini seçin.
3. **Sistem yönetimi** sayfasında, **Kurulum** altında **Sistem parametreleri**'ni seçin.
4. **Sistem parametreleri** sayfasında **Önizleme özellikleri** sekmesini seçin.
5. **Tüm kullanıcılar için önizleme modunu etkinleştir** seçeneğini **Evet** olarak ayarlayarak önizleme özelliğini kullanılabilir kılın.

    ![Core HR içinde önizleme özelliklerini etkinleştirme](./media/corehr-enable-preview-features.png)

> [!NOTE]
> Önizleme özelliklerini devre dışı bırakmak için aynı adımları kullanın ama **Tüm kullanıcılar için önizleme modunu etkinleştir** seçeneğini **Hayır** olarak ayarlayın. Önizleme özelliklerini devre dışı bıraktığınızda, kullanıcılar bu özelliklere erişemez ve özelliklerle ilişkilendirilmiş işlemlerde hatalar meydana gelebilir.

### <a name="onboard"></a>İşe al

Şu anda Microsoft Dynamics 365 Talent: Onboard için önizleme özelliği yoktur.

## <a name="features-that-are-currently-in-preview"></a>Şu anda önizlemede olan özellikler

### <a name="attract"></a>Attract

- [Aday önerisi](./intelligent-recommendations.md#candidate-recommendations) - Özgeçmiş veya tam profili olan ondan fazla aday veya müşteri adayı varsa, bu durumdaki her iş için, işin gerekliliklerine en yakın adaylar veya müşteri adayları, işin sayfasındaki **Dikkate alınacak adaylar** bölümünde görüntülenir.
- [İş önerisi](./intelligent-recommendations.md#job-recommendations) – Kariyer sitenizde 10'dan fazla iş nakledilmişse, Attract, aday müşteri adayları için iş önerileri sağlar.
- [Broadbean tümleştirmesi](./posting-jobs-external.md#post-jobs-to-broadbean) – İşleri Attract'ten harici bir iş ilanı sitesi olan Broadbean'a aktarabilirsiniz. Bu önizleme özelliğini etkinleştirdikten sonra, Broadbean Kullanıcı adı, istemci kimliği ve şifreleme belirtecinizi girerek kurulumu tamamlamanız gerekir.
- [Analitikler](./analytic-reports.md) - Analitik Merkezinde, işe alma ekipleri tek bir iş için temel ölçümleri görebilirler, ayrıca tüm işlerdeki toplanmış ölçümleri de görebilirler.
- [EEO](./activities-attract.md) – Yeni aktivite türleri, adaydan Eşit Çalışma Fırsatı (EEO) ve Federal Sözleşme Ofsi Uyumluluk Programı (OFCCP) verilerini toplaması için önceden tanımlanmış bir form kullanımını etkinleştirin. Önceden tanımlı form düzenlenemiyor.
- [Aday önerisi](./intelligent-recommendations.md#prospect-recommendations) - Attract, geçmiş başvuruları ve güncel adayları değerlendirerek işiniz için en iyi uyuma sahip adayların listesini sağlar.
- [İlgi arama](./attract-talent-pools.md#search-and-view-candidate-profiles) - Tüm aday veritabanınızı belirli yetenekler, adlar veya eğitim geçmişine dayanarak arayabilirsiniz. Attract, profilin tamamını arar ve bulunan tüm eşleşmeleri vurgular. Attract ayrıca bir aday için bir aday için mevcut olan tüm belgeleri arar ve arama sonuçlarını akıllıca sıralar.
- [Etkinlik kitlesi](./whats-new-talent-march-20.md#setting-the-audience-on-activities) - Etkinlikler (örneğin Mülakat, Toplantı veya Geri bildirim) için kitleyi **Tüm adaylar**, **Dahili adaylar** veya **Harici adaylar** olarak ayarlayabilirsiniz. Müşteri etkinlikleri, örneğin YouTube videoları, web içeriği ve Microsoft Formları'nı tüm adaylara, yalnızca dahili adaylara, yalnızca harici adaylara veya işe alma ekibine aktarabilirsiniz.
- [LinkedIn ile başvur](./career-site.md#enable-applying-for-jobs-with-linkedin-profiles) - İş adaylarının LinkedIn kullanarak başvurmaları için Attract kariyer sitenizde bir seçenek ayarlayabilirsiniz. Bu özellik, adaylarınızın kendi LinkedIn profillerini kullanmasına izin vermek yoluyla, aday profilinizi onlara otomatik olarak doldurmak için uygulama işlemini kolaylaştırır.
- [Kaynak izleme](./source-tracking.md) - Attract, aday başvurularının kaynağını izleyerek, işe alım çabalarınızı yönlendirmek için değerli bilgiler sağlayabilir. Bir adayı bir işe veya yetenek havuzuna eklerken bir başvuru kaynağı seçebilirsiniz.
- [Gümüş madalyalı](./whats-new-talent-march-20.md#designate-silver-medalists-to-assign-high-value-applicants-for-future-positions) - Bir adaya kuruluşunuza çok uygunsa ancak geçerli pozisyon için kendisine bir teklifte bulunmadıysanız, bunları gümüş madalyalı olarak tanımlayabilirsiniz. Bu özellik, bir sonraki benzer pozisyona sahip olduğunuz zamandan sonra işe alma süresinin azaltılmasına yardımcı olur.

### <a name="core-hr"></a>Temel İK

- [Konum hiyerarşisi verisini doğrula](./whats-new-talent-may-13-2019.md#new-page-to-validate-position-hierarchy-data) - İçe aktarılan herhangi bir döngüsel referans için yönetim hiyerarşisini doğrulayabilirsiniz.
- [İzin türlerinde neden kodları belirtin](./whats-new-talent-may-13-2019.md#specify-reason-codes-on-leave-types) - İzin türleri için neden kodları belirtebilirsiniz.
- [İzin taleplerinde sebep kodları gerektir](./whats-new-talent-may-13-2019.md#require-reason-codes-for-specific-leave-types-on-time-off-requests) - İzin türleri için sebep kodları gerektirmenin yanı sıra, izin talepleri için de sebep kodları gerektirebilirsiniz.
- [İK için izin ve devamsızlık listesi sağlayın](./whats-new-talent-may-13-2019.md#provide-a-leave-and-absence-transaction-list-for-hr) - İzin bakiyelerine içgörü sağlamak için izin ve devamsızlık listesini görüntüleyebilirsiniz.

### <a name="onboard"></a>İşe al

Şu anda Onboard için önizleme özelliği yoktur.

## <a name="feedback"></a>Bildirim

Bu önizleme özelliklerinden herhangi biriyle ilgili deneyiminizden haberdar olmak istiyoruz. Bu özellikleri veya diğer yeni özellikleri kullandıkça aşağıdaki sitelerden bize düzenli olarak geribildirim göndermenizi rica ediyoruz:

- [Topluluk](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Bu, kullanıcıların olayları tartışabileceği, sorular sorabileceği ve topluluktan yardım alabileceği yararlı bir kaynaktır.
- Üründe görmek istediğiniz özellikleri ve mevcut özellikler için yapmamız gerektiğini düşündüğünüz herhangi bir değişikliği bize bildirin. Aşağıdaki sitelerde ürün fikirleri önerin:

    - [Attract fikirleri](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Core HR fikirleri](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    - [Onboard fikirleri](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

Kişisel verilerinizi (sizi tanımlamaya yardımcı olabilecek bilgiler) geribildiriminize veya ürün incelemesi gönderimlerinize eklemediğinizden emin olun. Toplanan bilgiler daha ayrıntılı incelenebilir ve yürürlükteki gizlilik yasaları kapsamında talepleri yanıtlamak için kullanılamaz. Bu programlar altında ayrı olarak toplanan kişisel veriler [Microsoft Gizlilik Bildirimi](https://privacy.microsoft.com/privacystatement)'ne tabidir.

> [!TIP]
> Bu konuyu işaretleyin ve yayımladığımızda yeni önizleme özelliklerinden haberdar olmak için sık sık kontrol edin.

## <a name="see-also"></a>Ayrıca bkz.

- [Talent uygulamaları deneyin vey asatın alın](https://dynamics.microsoft.com/talent/overview/)
- [Yenilikler](./whats-new.md)
- [Sürüm notları](https://docs.microsoft.com/business-applications-release-notes/index)
- [Talent için destek alma](./talent-support.md)
