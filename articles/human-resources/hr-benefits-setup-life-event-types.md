---
title: Yaşam olayı türlerini yapılandırma
description: Microsoft Dynamics 365 Human Resources, çalışan kazançları kaydını güncelleştirmek için olayları tanımlamak üzere yaşam olayı türlerini kullanır.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df523dd4da11e24c7b601c8f34aef24ad6cb3b18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337098"
---
# <a name="configure-life-event-types"></a>Yaşam olayı türlerini yapılandırma

Dynamics 365 Human Resources, personel yan haklar kaydını güncelleştirmek için geçerli olduğu olayları tanımlamak için **Yaşam olayı türleri** kullanır (örn. evlenme veya çocuk sahibi olma). Her ömür olayı tür kimliği yalnızca bir ömür olay türüyle ilişkilendirilebilir. Örneğin, **Personel adres değişikliği** yaşam olayı türü ile ilişkilendirilmiş **Adres değişikliği** adlı bir **Yaşam olayı kimliği** oluşturursanız **Personel adresi değişikliği** olarak etiketlenmiş başka bir kimlik oluşturamazsınız ve bunu **Personel adres değişikliği** adlı yaşam olayı türüyle ilişkilendiremezsiniz. Ömür olayı türü bir plan türüyle ilişkilendirilmemişse, ömür olayı türü bir ömür olayını tetiklemez. Daha fazla bilgi için, bkz. [Plan türleri oluşturma](hr-benefits-setup-plan-types.md).

## <a name="create-a-life-event-type"></a>Ömür olayı türü oluştur

1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Yaşam olayı türleri**'nı seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Yaşam olayı tür kodu** | Ömür olayı türü benzersiz tanımlayıcısı. |
   | **Tanım** | Yşaam olayı türünün açıklaması |
   | **Yaşam olayı türü** | Bir çalışanın sosyal haklar kaydını güncelleştirmek için bir Catalyst. Ömür olaylarının listesi için, bkz. aşağıdaki [ömür olayları](hr-benefits-setup-payment-frequencies.md?life-events). |

4. **Kaydet**'i seçin.

## <a name="view-attached-plans"></a>İliştirilmiş planları görüntüle

Seçilen **Yaşam olayı türü**'ne iliştirilmiş planların listesini görebilirsiniz. Ömür olayları bir plan türüne bağlıdır ve plan tipleri bir planla ilişkilendirilir.

1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Yaşam olayı türleri**'nı seçin.

2. **Eylemler**'i seçin.

3. **İlişik planları** seçin.

## <a name="life-events"></a>Yaşam olayları

Ömür olayı türü oluştururken, aşağıdaki ömür olayları arasından seçim yapabilirsiniz:

| Yaşam olayı | Konum | Tetik |
| --- | --- | --- |
| **Medeni durum değişikliği** | **Çalışan > profili > kişisel bilgiler > medeni durum**| Medeni durum değişikliği |
| **İstihdam durumu değişikliği** |**Çalışan > İstihdam > İstihdam geçmişi sayfası** | Çalışma ayrıntısı zaten olan bir çalışan için farklı bir iş durumuyla yeni bir iş ayrıntısı oluşturulması bir ömür olayı tetikleyecektir.  Varolan bir iş ayrıntısını farklı bir iş durumuyla güncelleştirmek de bir ömür olayı tetikler.  |
| **Personel adres değişikliği** |**Çalışan > profili > adresleri**</li><li>**Çalışan > kişisel bilgileri > Kişisel Kişiler > adresi**</li></ul> | Adreste değişiklik. Yaşam olayının tetiklenmesi için adresin **Birincil** olması gerekir. |
| **Bakmakla yükümlü olunan kişi değişikliği** |<br><ul><li>**Çalışan > Profil > Kişisel bilgiler > Kişisel ilgili kişiler**/li><li>**Personel self servisi**</li></ul> | Kişisel irtibat ekleyerek bu irtibatı bağlı olarak belirleyin ve **Geçerlilik başlangıç tarihi**'ni belirleyin. Kişisel irtibatın bağlı kişisinin **Geçerlilik bitiş tarihi** bilgilerini güncelleştirin. Kişisel ilgili kişi ilişkisi çocuk, eşinin, yurtiçi partner veya eski eşinin olmalıdır.  |
| **Doğum veya evlat edinme (bakmakla yükümlü olunan kişi)** |<br><ul><li>**Çalışan > Profil > kişisel bilgileri > Kişisel Kişiler**</li><li>**Personel self servis > Kişisel detayları düzenle > Kişisel irtibatlar**</li></ul>| **Doğum tarihi** veya **Evlat edinilme tarihi** eklendi veya güncelleştirildi. Çocuğun **Doğum tarihi** gereklidir. |
| **Karşılama kaybı (eş / hayat arkadaşı)** | Çalışan > profil > Kişiler > Kişisel bilgileriyle > bağımlı ayrıntıları > Kapsam kaybı | Kişisel bir ilgili kişi için seçilen, **geçerlilik tarihiyle** birlikte seçili **kapsam kaybı** |
| Hayat arkadaşı istihdam değişikliği | **Çalışan > Profil > Kişisel bilgiler > Kişisel irtibatlar > Bağlı ayrıntıları > Çalışıyor** | Kişisel irtibat oluşturma ve **Çalışıyor**'u **Evet** olarak ayarlama. Kişisel irtibatı güncelleştirme ve **Çalışıyor** durumunu değiştirme.  |
| **İzin (Eş/hayat arkadaşı)** | **Çalışan > profil > Kişiler > Kişisel bilgileriyle > bağımlı ayrıntıları > Kapsam kaybı > Devamsızlık izni** | Kişisel irtibat oluşturuldu ve **İzin başlangıç tarihi** belirlendi. Kişisel irtibat **İzin** güncelleştirildi. Kişisel irtibat **İzin başlangıç tarihi** güncelleştirildi.  |
| **Karşılama değişikliği (pozisyon)** |<br><ul><li>**Çalışan > konumu ataması > çalışan konumu atamaları**</li><li>**Pozisyonlar > pozisyonlar**</li></ul>| Çalışan pozisyondaki pozisyonda yer değiştirme atama kayıtları. Çalışan pozisyonda yer değiştirme atama kayıtları. |
| **Karşılama değişikliği (maaş)** |<br><ul><li>**Çalışan > Ücret > Sabit planı**</li><li>**Çalışan > Kişisel bilgiler > Kazançlar yıllık ücret**</li></ul>| **Yan haklar yönetimi > Human Resources paylaşılan parametreleri > Yan haklar > Yan haklar yıllık ücret** etkinleştirilmemiş, **Çalışan > Ücret > Sabit plan** bir yaşam olayı oluşturacaktır. **Kazançlar yönetimi > İnsan kaynakları paylaşılan parametreleri > Kazançlar > Kazançlar yıllık ücret** etkinleştirilmiş, **Çalışan > Kişisel Bilgiler > Kazançlar yıllık ücret** bir yaşam olayı oluşturacaktır. |
| **Medicare (Personel/bakmakla yükümlü olunan kişi)** | **Çalışan > profil > Kişiler > Kişisel bilgileriyle > bağımlı ayrıntıları > Kapsam kaybı > Medicare yürürlük tarihi** | Kişisel irtibat için **Medicare geçerlilik** tarihi eklenmesi veya güncelleştirilmesi bu ömür olayını oluşturur. |
| **Mahkeme kararıyla destek** | **Çalışan > Profil > Kişisel bilgiler > Kişisel ilgili kişiler > Bağımlı > Mahkeme kararlı destek** (QMSCO/QDRO) ve geçerlilik tarihleri | Bir kişisel irtibat oluştururken, **Mahkeme kararlı destek** **Evet** olarak ayarlanırsa bir ömür olayı oluşturulur. **Mahkeme kararlı destek** veya **Mahkeme kararının bitiş tarihi**'nin güncelleştirilmesi de bir ömür olayı tetikler. |
| **Ölüm** | **Çalışan > profili > kişisel bilgiler > Ölüm tarihi** | **Ölüm tarihi** girildi veya güncelleştirildi. |
| **Sigorta kanıtı** | **Çalışan > çalışan > sürümleri > İş geçmişi > Tarih Yöneticisi > Kazanç ayrıntıları** | **Sigorta kanıtı** **Evet** olarak ayarlı. **Sigorta kanıtı doğrulama tarihi** tanımlandı. |
| **Hak sahibi** | **Çalışan > Profil > kişisel bilgileri > Kişisel Kişiler** | Kişisel ilgili kişi eklenir ve **Lehtar** ve **Geçerlilik tarihi** alanları doldurulur. Kişisel irtibatın **Çocuk**, **Eş**, **Hayat arkadaşı**, **Kardeş**, **Aile Bireyi**, **Diğer** veya **Ebeveyn** türünden olması gerekir |
| **Personel Medicare'i** | **Çalışan > çalışan > sürümleri > İş geçmişi > Tarih Yöneticisi > Kazanç ayrıntıları** | **Medicare uygunluğu** **Evet** olarak ayarlandı. **Medicare uygunluk tarihi** değiştirildi. |
| **Doğum günü** | **Kazançlar yönetimi > Ömür olayı değişikliği işleme** | Bu ömür olayları, **Ömür olayı değişikliği işleme**'den oluşturulur. İşlem, seçilen dönemi ve tüzel kişiliği analiz eder ve ilişkili çalışanları bulur. Son doğum gününü hesaplar ve henüz oluşturulmuşsa bir doğum günü ömür olayı oluşturur. |
| **Çalışan uygunluğu değişikliği (ABD'ye özgü değil)** |<br><ul><li>**Çalışan > İstihdam**</li><li>**Çalışan > çalışan > sürümleri > İş geçmişi**</li></ul>| Aşağıdaki durumlarda bir ömür olayı oluşturur:<br><ul><li>Eski bir iş varken yeni bir iş oluşturma ve çalışan türünün değişmesi.</li><li>Eski bir iş ayrıntısı varken yeni bir iş ayrıntısı oluşturma ve iş türü veya iş kategorisinin değişmesi.</li><li>İş kaydının güncelleştirilmesi ve farklı bir çalışan türünün belirlenmesi.</li><li>İş ayrıntısı kaydının güncelleştirilmesi ve farklı bir iş türü veya kategorisinin belirtilmesi.</li></ul> |
| **Yeni uygunluk geçersiz kılma (ABD'ye özgü değil)** | **İnsan kaynakları Gelişmiş > kazançlar > planlar > kazançlar > uygunluk kuralı geçersiz kılma** | Yaşam olayı işlemeyi kullanma<br>Bir çalışan için yeni bir kazanç planı uygunluğu geçersiz kılma oluşturma, bu ömür olayını tetikler.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Uygunluk kuralı geçersiz kılmayı değiştirme (ABD'ye özgü değil)** | **İnsan kaynakları Gelişmiş > kazançlar > planlar > kazançlar > uygunluk kuralı geçersiz kılma** | Bir kazan planı uygunluk geçersiz kılmada **Geçerlilik başlangıç tarihi** veya **Geçerlilik bitiş tarihi**'nin güncelleştirilmesi bu ömür olayını tetikler. |
| **Uygunluk kuralı geçersiz kılma son tarihi (ABD'ye özgü değil)** | Kazançlar yönetimi > Ömür olayı değişikliği işleme  | Bu ömür olayları, **Ömür olayı değişikliği işleme**'den oluşturulur. İşlem, seçilen dönemi ve tüzel kişiliği analiz eder ve ilişkili kazanç planı uygunluk geçersiz kılmaları bulur. Geçersiz kılmaların süresi dolmuşsa, ömür olayları oluşturur. |
| **Yeni kazanç planı (ABD 'ye özel değil)** | **İnsan kaynakları Gelişmiş > Kazançlar > planlar > yeni** | Geçerli plana uygunluk seçenekleri eklenir. Uygunluk seçenekleri eklenmiş yeni bir plan eklendi.</br></br>IK personelin bu örnekte ömür olayı uygunluk işlemi çalıştırması gerekir. |
| **Uygunluk kuralı değiştirme (ABD'ye özgü değil)** | **Kazançlar yönetimi > Uygunluk kuralları** | Yaşam olayı uygunluğunu işlemeyi kullanma **BenefitEligibilityRule** kayıtları aşağıdaki değerlere sahip olduğunda günlüğe kaydedilir: **UseEmplCategory**, **UseEmplStatus** veya **UseEmplType**. Yalnızca değiştirilmiş bir kural veya uygunluk ölçütü için zaten varolan ömür olayı hareketlerini güncelleştirir. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
