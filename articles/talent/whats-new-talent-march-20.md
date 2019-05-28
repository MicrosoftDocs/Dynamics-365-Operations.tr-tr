---
title: Dynamics 365 for Talent'daki yenilikler veya değişiklikler (20 Mart 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d69294b64c841c5486d694b129cf6c0f26fd93fd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519320"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-20-2019"></a>Dynamics 365 for Talent'daki yenilikler veya değişiklikler (20 Mart 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

### <a name="setting-the-audience-on-activities"></a>Etkinliklerdeki izleyicileri ayarlamak
Sistemdeki etkinlikleri şimdi kitlesi tanımlanabilir. Süreçle ilgili etkinlikler (görüşme, zamanlama, geri bildirim ve EEO gibi), Tüm adaylar, Dahili adaylar ve Harici adaylara gönderilmek üzere ayarlanabilir. Özel etkinlikler, örneğin Microsoft Forms, YouTube videoları ve web içeriği Tüm adaylara, Dahili adaylara, Harici adaylara veya işe alma ekibine aktarılabilir.  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>Kariyer sitesi iş keşfedilebilirliği: Arama Motoru Optimizasyonu
Bu özellik, arama motoru gezginlerinin Attract kariyer sitesindeki iş ilanlarına erişmesine ve endekslemesine olanak sağlar. Bu, popüler arama motorları kullanarak Attract kariyer sitesine verilmiş iş ilanlarını bulmalarına yardımcı olur.

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>Kimlik bilgilerini unutan adaylara oturum açma ipucunu göster
Bir aday bir link açarken kaydedilen veya kendilerine e-postayla gönderilen sosyal kimlik bilgilerini unuttuysa, sağlayıcı adı ve kullanıcı (karıştırılmış) içeren bir ipucu görürler. Bu, iş başvurularına erişmek için doğru kimlik bilgilerini kullanmalarına yardımcı olur.

### <a name="help-internal-candidates-explore-internal-jobs"></a>Dahili adayların dahili işleri keşfetmelerine yardımcı ol
Harici adayların bir işin işe alanı veya işe alım yöneticisinin adını görebildiği bir sorun düzeltilmiştir. Şimdi yalnızca dahili adaylar bir iş için işe alım ekibinin üyelerini görebilir. Dahili adayların yalnızca dahili işleri görüntülemesi ve başvurması daha kolaydır. Bir aday, bağlantıya bir yalnızca dahili işi görüntülemek veya başvurmak için erişmeye çalışırsa, Azure Active Directory kimlik bilgileri ile kimlik doğrulaması yapmaya zorlanırlar. Dahili adayların ayrıca işe alma ekibi üyeleriyle iletişim kurarak iş hakkında bilgi isteme ve ilgilerini belirtme olanakları vardır. Bu yeterlilik, yalnızca dahili adaylar için tüm işler için kullanılabilir. Daha fazla bilgi için [Attract'taki kariyer sitesi işlevi](./career-site.md).

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>Gelecekteki bir pozisyon için başvuran yüksek bir değer atamak için gümüş madalyalıları belirleyin
İşe alanlar ve işe alım yöneticileri çoğu zaman pozisyon için uygun olan ancak pozisyon zaten doldurulduğu için teklif yapılamayan bir aday olan adayların listesini tutarlar. Bu tür adaylar, gümüş madalyalılar olarak adlandırılır ve benzer bir pozisyon bir daha açıldığında işe alma sürecini hızlandırabilecekleri için değerlidirler. Attract şimdi işe alımcıların ve işe alma yöneticilerinin aday listesinde, aday Teklif aşamasına ulaştıysa gümüş madalyalı olarak adanmasına izin verir. Gümüş madalyalı ataması, bir iş için başvuran listesinde ve ayrıca bu adaylar, herhangi bir işe alımcı veya işe alım yöneticisinin havuzunda olduğunda aday havuzu görünümünde görüntülenecektir. Ek olarak, atama, bir adayın yetenek havuzu profilinin parçası olarak iş geçmişinde de görüntülenecektir. Bu özelliği, bir yöneticinin [Yönetim Merkezinde Özellik Yönetimi](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature)'ni kullanarak açmasıyla önizleyebilirsiniz.

### <a name="add-applicants-to-talent-pools"></a>Yetenek havuzlarına başvuranlar ekle
Şimdi, Başvuranlar listesinde yeni bir eylemi yüzeye çıkararak başvuranları bir beceri havuzuna eklemek daha da kolaydır. **Yetenek havuzuna ekle** simgesini seçerek, işe alımcı veya işe alma müdürü, kendi yetenek havuzu listesi arasından seçim yapabilir ve bir işteki Başvuranlar listesinden yetenek havuzlarına doğrudan başvuran ekleyebilir.

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>Belirli bir işe başvurmak için özgeçmiş gerekli olup olmadığını yapılandır
Müşteri geribildirimine dayanarak, işe alımcılar artık karşıya yüklenmiş bir dosya biçiminde bir özgeçmişin belirli bir işe başvururken gerekli olup olmadığını yapılandırabilirler. Bu yapılandırma, Başvuru etkinliğinin parçasıdır, işe alma sürecinde erişilebilirdir. Etkin olduğunda, her potansiyel başvuran bu pozisyona başvurduklarında bir özgeçmiş karşıya yüklemeleri konusunda bildirim alırlar. Bir özgeçmiş karşıya yüklenene kadar başvuru tamamlandı olarak kabul edilmez. Bu, başvuran havuzunda, her başvuranın, işe alımcıların onları değerlendirmesine olanak tanıyacak kadar bilgi sağlamış olduğundan emin olarak, gürültüyü önler.

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>Adaylar, bir işe LinkedIn profillerini kullanarak başvurabilirler
Güncelleştirilmiş profillerine LinkedIn'de halihazırda sahip olan adaylar bu profili kullanarak tek bir tıkla işlere başvurabilirler.

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>Bir aday profilinin sistemde nereden geldiğini ve adaylarınızın başvurdukları işleri nerede keşfettiklerini izleyin
Şimdi belirli bir adayın profilinin Attract içinde nereden geldiğini, profilin kaynağına adayların ayrıntılarına bir başvurunun veya yetenek havuzu profilinin **Profil** sayfasından görebilirsiniz. Benzer şekilde, herhangi bir başvuranın, işi **Başvuru etkinliği** içerisindeki başvuru etkinlik akışında sağlanan başvuru kaynağına bakarak da öğrenebilirsiniz. Bu bilgi, ayrıca yetenek havuzu profilindeki iş geçmişinde de mevcuttur. İşe alanlar veya işe alım yöneticileri adayları el ile eklediklerinde, başvurunun veya aday profilinin kaynağını belirtmeleri de istenir. Bir aday ilk kez başvurduğunda, profil kaynakları, başvurunun kaynağı ile aynı olacaktır. Bu özelliği, bir yöneticinin [Yönetim Merkezinde Özellik Yönetimi](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature)'ni kullanarak açmasıyla önizleyebilirsiniz. Varolan adayların ve başvuranların herhangi bir kaynak bilgisine sahip olmayacağını unutmayın. Ancak, işe alanlar bu bilgiyi el ile ekleyebilirler.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içerir.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2195 için geçerlidir

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>Attract tümleştirmesi, Başvurular için yinelenen kayıt hatası veriyor
Bu güncelleştirmede, yinelenen kayıtlarla ilgili bir sorun giderilmiştir. Bu sorun, **Personel yönetimi** çalışma alanını açarken ortaya çıkmaktadır.

### <a name="unable-to-close-form-when-editing-name-sequence"></a>Ad sırası düzenlenirken form kapatılamıyor
Çalışan formundaki ad sırasını düzenlerken ortaya çıkan bir hatayı düzeltmek için değişiklikler yapıldı.

## <a name="coming-soon"></a>Çok yakında

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Gelişmiş ücret güvenliği (sabit ve değişken)
Pek çok kuruluşta, ücret ve kazanç yöneticilerinin yalnızca belirli ücret kayıtlarına erişimi olabilir. Bunlar yöneticiler veya bölgesel çalışanlar için olabilir. Bu değişiklik ile IK, yönetimini değiştirebilir ve ücret planlarını kuruluş içindeki farklı personel grupları için korur. Planlar ve planlarla ilişkili personel verilerine, örneğin maaş veya ikramiye kayıtlarına erişimi belirleyen sabit ve değişken planlara güvenlik rolleri atayabilirsiniz. Yalnıza erişime sahip olan roller, bu çalışanlar için ücreti işleyebilirler.

###  <a name="email-support-for-alerts"></a>Uyarılar için e-posta desteği
Platform güncelleştirmesi 24 ile kullanıcılar otomatik olarak, bir etkinlik tarafından tetiklendiğinde e-posta bildirimlerini ilgili kişilere gönderen uyarı kuralları oluşturabilirler.

### <a name="duplicate-employee-check-interface-changes"></a>Yinelenen personel denetimi: Arabirim değişikliği
Bu değişiklikle, isim alanlarını girdiğinizde yinelenenler tespit edilir ve yinelenenlerin sayısını görüntüleyen bir durum gösterilir. Sağlanan bağlantıyı tespit edilen eşleşmeyi kullanıp kullanmamak üzere yeni bir sayfa açmak için seçebilirsiniz. Yinelenenler formu, veri girişini kesintiye uğratmayı önlemek için otomatik olarak açılmaz.


