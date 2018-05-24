---
title: "Microsoft Dynamics 365 for Talent'ta önizleme özelliklerine erişme"
description: "Bu konu önizleme özelliklerini bir yöneticinin nasıl etkinleştirebileceğini tanımlar ve önizleme için etkin olan özellikleri listeler."
author: rschloma
manager: AnnBe
ms.date: 04/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2e5dd8f852ac1a6c2997a50a60f03db6adfd218c
ms.openlocfilehash: 5500bfc1cdd1949d301ae82fad5506dfdbeb59f3
ms.contentlocale: tr-tr
ms.lasthandoff: 05/01/2018

---

# <a name="access-preview-features-in-dynamics-365-for-talent"></a>Microsoft Dynamics 365 for Talent'ta önizleme özelliklerine erişme 

[!include[banner](../includes/banner.md)]

Sürekli olarak kullanıma sunduğumuz ürün özelliklerinin bir parçası olarak, müşterilerimizin yeni özellikleri mümkün olan en kısa sürede deneyimlemesini istiyoruz. Yöneticiler önizleme özelliklerini kendi ortamlarında görebilir ve kullanabilir. Bu özellikler neredeyse genel kullanıma sunulmak üzere hazır durumdadır ve kapsamlı bir sınamadan geçirilmiştir. Bu özellikleri genel kullanım için yayımlamadan önce müşterilerimizden son kez geribildirim almak istiyoruz.

Bu konu önizleme özelliklerini bir yöneticinin nasıl etkinleştirebileceğini tanımlar ve önizleme için kullanılabilir olan özellikleri listeler. Bu liste özellikler genel kullanım için yayımladıkça ve yeni özellikler önizleme için yayımlandıkça güncelleştirilecektir. Yeni özellikler önizleme için yayımlandığında bildirim gönderilmeyecektir. Kullanıcılar özellikleri görmeye başlayacaktır.

## <a name="enable-or-disable-preview-features"></a>Önizleme özelliklerini etkinleştirme veya devre dışı bırakma

Önizleme özelliklerini etkinleştirmek veya devre dışı bırakmak için Microsoft Dynamics 365 for Talent yönetim merkezindeki **Önizleme özellikleri** ayarını kullanabilirsiniz. Varsayılan olarak, bu ayar kapalıdır. Önizleme özelliklerini devre dışı bırakma veya etkinleştirme ortama özgü bir eylemdir.

> [!IMPORTANT]
> **Önizleme özellikleri** ayarını açarak, kuruluşunuzda bulunan bu ortamdaki tüm kullanıcılar için önizleme özelliklerini etkinleştirirsiniz. Ayarı kapattığınızda, önizleme özelliklerini devre dışı bırakırsınız ve kullanıcılarınız bu özelliklere erişemez. Önizleme özellikleri Talent'ta sınırlı şekilde desteklenir. Daha az gizlilik ve güvenlik önemi kullanabilirler ve Talent hizmet düzeyi sözleşmene dahil değildirler. Kişisel verileri (diğer bir deyişle, sizi tanımlamaya yardımcı olabilecek tüm bilgileri) işlemek ya da yasa veya düzenlemelerle uyumluluk gereksinimlerine tabi olan diğer verileri işlemek için önizleme özelliklerini kullanmamanız gerekir.

### <a name="enable-or-disable-preview-features-for-your-organization"></a>Kuruluşunuz için önizleme özellikleri devre dışı bırakma veya etkinleştirme

#### <a name="attract"></a>Attract

1. Microsoft Dynamics 365 for Talent: Attract'ta oturum açın.
2. Sağ üst köşedeki **Kurulum** menüsünden (çark simgesi) **Yönetici ayarları**'nı seçin.
3. **Özellik yönetimi** sekmesinde **Önizleme özellikleri** yanındaki seçeneği seçin. Seçildiğinde mavi renge dönecektir.
4. Yeni özellikleri görmek için tarayıcınızı yenileyin. (Zaten oturum açmış kullanıcılar özellikleri daha sonra yeniden oturum açtıklarında görürler veya özellikleri hemen görmek için tarayıcıyı yenileyebilirler.)

#### <a name="core-hr"></a>Temel İK

1. Talent'ta oturum açın. Kalan adımları tamamlayabileceğiniz temel İnsan kaynakları çalışma alanı açılır. 
2. **Sistem yönetimi \> Bağlantılar Sistem parametreleri**'ni seçin.
3. **Sistem Parametreleri sayfasında**, **Önizleme özellikleri** sekmesinde **Önizleme modunu tüm kullanıcılar için etkinleştir** seçeneğini **Evet** olarak seçip önizleme özelliklerinin kullanılabilir olmasını sağlayın.

> [!NOTE]
> Önizleme özelliklerini devre dışı bırakmak için aynı temel adımları kullanın. Önizleme özelliklerini devre dışı bıraktığınızda, kullanıcılar bu özelliklere erişemez ve özelliklerle ilişkilendirilmiş işlemlerde hatalar meydana gelebilir.

## <a name="features-that-are-currently-in-preview"></a>Şu anda önizlemede olan özellikler

### <a name="attract"></a>Attract

- **İş şablonları** – Artık işe alım süreci şablonları oluşturabilirsiniz. Kullanıcılar belirli bir proje için işe alma sürecini zaten özelleştirebiliyordu. Ancak, şimdi süreç için şablonlar oluşturabilir ve belirli bir iş oluşturulduğunda uygun şablonu seçebilirsiniz. Bu nedenle, bu özellik iş kurulumu sürecini kolaylaştırmaya yardımcı olur.
- **Kariyer sitesi** – Kariyer sitesinin geçerli sürümü yalnızca tüm açık işleri listeler. Bununla birlikte, gelecekte siteye daha fazla özellik eklenecektir. İşler dahili veya harici olarak işaretlenebilir. Sitede oturum açan dahili kullanıcılar hem dahili hem de harici işleri görür. Ancak, dahili olmayan veya oturum açmamış olan kullanıcılar yalnızca harici işleri görebilir.
- **İş ilanı** – Artık işleri kariyer sitesinde yayınlayabilirsiniz.
- **LinkedIn iş ilanı** – Artık işleri LinkedIn'de yayınlayabilirsiniz.

    > [!NOTE]
    > Yayınlanan işler yalnızca bir veya daha fazla LinkedIn iş listeme ürününe abone olan müşteriler tarafından görülebilir. Aksi takdirde, müşteriler yalnızca özellikle aradıkları bir işi görebilirler. İşler LinkedIn'de yayınlandığında bir gecikme olur. Bir işin Attract'tan yayınladıktan sonra görünür olması birkaç saat alabilir.

- **Aday başvurusu** – Hem harici hem de dahili adaylar artık doğrudan kariyer sitesindeki iş sayfasından başvuruda bulunabilir.
- **Değerlendirmeler** – Yapılandırılabilir işe alım işleminin bir parçası olarak, belirli bir iş için veya bir iş şablonu kullanıldığında, kullanıcılar yeni **Değerlendirme** faaliyet türüne erişebilir. Talent'taki Project: "Gauge" uygulamasını kullanarak adaylara gönderebilecekleri temel değerlendirmeler oluşturabilirler. Project: "Gauge" genel önizlemeye sunulmuştur. Gelecekte ek sağlayıcılar eklenecektir.
- **Project: "Gauge"** – Proje: "Gauge" Talent'ta yer alan ve kullanıcılara basit değerlendirmeler veya anketler oluşturma olanağı sunan bir uygulamadır.
- **Teklif yönetimi** – Kullanıcılar artık yer tutucular içeren şablonlardan teklif mektupları oluşturabilir. Adaylar Teklif aşamasında ilerlediğinde, işe alanlar ve işe alım müdürleri aday için şablonlar aracılığıyla bir resmi teklif hazırlamak, teklifi dahili onaylayana gönderme ve son olarak teklifi imzalanmak üzere adaya göndermek için Teklif aracını kullanabilirler. Zaman içinde Teklif aracına birçok yeni özellik eklenecektir ve önizleme için yayımlamaya hazır olduğumuzda önizleme özelliği bu özelliklerle güncelleştirilecektir.

### <a name="core-hr"></a>Temel İK

- **Açık Kayıt** – Açık kayıt kazançları çalışanlara kazançlarını seçmeleri için kolay, self-servis deneyimi sunar. İnsan Kaynakları (İK) yöneticileri kuruluşları için kazanç açık kayıt sürecini ve çalışanlara yönelik kayıt deneyimini, kolay izlenebilen kılavuzlu çözümleri kullanarak yapılandırabilir.

## <a name="feedback"></a>Geribildirim

Geribildirimin pozitif veya negatif olmasına bakılmaksızın, önizleme özellikleri kullanımınıza ilişkin düşüncelerinizi öğrenmek istiyoruz. Bu özellikleri veya diğer yeni özellikleri kullandıkça aşağıdaki sitelerden bize düzenli olarak geribildirim göndermenizi rica ediyoruz.

- [Topluluk](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – Bu, kullanıcıların olayları tartışabileceği, sorular sorabileceği ve topluluktan yardım alabileceği yararlı bir kaynaktır.
- Ürün fikirlerini önermek için aşağıdaki siteleri kullanın. Üründe görmek istediğiniz özellikleri ve mevcut özellikler için yapılması gerektiğini düşündüğünüz herhangi bir değişikliği bize bildirin.

    - [Fikirleri Çekmek](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Temel İK](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

Kişisel verilerinizi (sizi tanımlamaya yardımcı olabilecek bilgiler) geribildiriminize veya ürün incelemesi gönderimlerinize eklemeyin. Toplanan bilgiler daha ayrıntılı incelenebilir ve yürürlükteki gizlilik yasaları kapsamında talepleri yanıtlamak için kullanılmayacaktır. Bu programlar altında ayrı olarak toplanan kişisel veriler [Microsoft Gizlilik Bildirimi](https://privacy.microsoft.com/en-us/privacystatement)'ne tabidir.

> [!TIP]
> Bu konuyu işaretleyin ve yayımladığımızda yeni önizleme özelliklerinden haberdar olmak için sık sık kontrol edin.

