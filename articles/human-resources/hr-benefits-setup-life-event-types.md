---
title: Yaşam olayı türlerini yapılandırma
description: Microsoft Dynamics 365 Human Resources, çalışan kazançları kaydını güncelleştirmek için geçerli olduğu olayları tanımlamak için ömür olayı türlerini kullanır.
author: andreabichsel
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 821e11d6ee22cb560b3d23017c7c332f80d41c18
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057658"
---
# <a name="configure-life-event-types"></a>Yaşam olayı türlerini yapılandırma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources, personel kazançları kaydını güncelleştirmek için geçerli olduğu olayları tanımlamak için yaşam olayı türleri kullanır (örn. evlenme veya çocuk sahibi olma). Her ömür olayı tür kimliği yalnızca bir ömür olay türüyle ilişkilendirilebilir. Örneğin, çalışan adres değişikliği ömür olay türü ile ilişkilendirilmiş adres değişikliği adlı bir ömür olayı kodu oluşturursanız, çalışan adresi değişikliğini etiketlenmiş başka bir kimlik oluşturamazsınız ve bunu çalışan adı olay türü olan çalışanın adres değişikliğiyle ilişkilendirebilirsiniz. Ömür olayı türü bir plan türüyle ilişkilendirilmemişse, ömür olayı türü bir ömür olayını tetiklemez. Daha fazla bilgi için, bkz. [Plan türleri oluşturma](hr-benefits-setup-plan-types.md).

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

Seçilen ömür olay türüne iliştirilmiş planların listesini görebilirsiniz. Ömür olayları bir plan türüne bağlıdır ve plan tipleri bir planla ilişkilendirilir.

1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Yaşam olayı türleri**'nı seçin.

2. **Eylemler**'i seçin.

3. **İlişik planları** seçin.

## <a name="life-events"></a>Yaşam olayları

Ömür olayı türü oluştururken, aşağıdaki ömür olayları arasından seçim yapabilirsiniz:

| Yaşam olayı | Konum | Tetik |
| --- | --- | --- |
| **Medeni durum değişikliği** | Çalışan > profili > kişisel bilgiler > medeni durum| Medeni durum değişikliği |
| **İstihdam durumu değişikliği** | Çalışan > İstihdam<br>İstihdam geçmişi sayfası | Çalışma ayrıntısı zaten olan bir çalışan için farklı bir iş durumuyla yeni bir iş ayrıntısı oluşturulması bir ömür olayı tetikleyecektir.  Varolan bir iş ayrıntısını farklı bir iş durumuyla güncelleştirmek de bir ömür olayı tetikler.  |
| **Personel adres değişikliği** | Çalışan > profili > adresleri<br>Çalışan > kişisel bilgileri > Kişisel Kişiler > adresi | Adreste değişiklik. Ömür olayının tetiklenmesi için adresin birincil olması gerekir. |
| **Bakmakla yükümlü olunan kişi değişikliği** | Çalışan > Profil > kişisel bilgileri > Kişisel Kişiler<br>Personel self servisi | Kişisel irtibat ekleyerek bu irtibatı bağlı olarak belirleyin ve **Geçerlilik başlangıç tarihi**'ni belirleyin. Kişisel irtibatın bağlı kişisinin **Geçerlilik bitiş tarihi** bilgilerini güncelleştirin. Kişisel ilgili kişi ilişkisi çocuk, eşinin, yurtiçi partner veya eski eşinin olmalıdır.  |
| **Doğum veya evlat edinme (bakmakla yükümlü olunan kişi)** | Çalışan > Profil > kişisel bilgileri > Kişisel Kişiler<br>Personel self servis > Kişisel detayları düzenle > Kişisel irtibatlar | **Doğum tarihi** veya **Evlat edinilme tarihi** eklendi veya güncelleştirildi. Çocuğun **Doğum tarihi** gereklidir. |
| **Karşılama kaybı (eş / hayat arkadaşı)** | Çalışan > profil > Kişiler > Kişisel bilgileriyle > bağımlı ayrıntıları > Kapsam kaybı | Kişisel bir ilgili kişi için seçilen, **geçerlilik tarihiyle** birlikte seçili **kapsam kaybı** |
| Hayat arkadaşı istihdam değişikliği | Çalışan > Profil > Kişisel bilgiler > Kişisel irtibatlar > Bağlı ayrıntıları > Çalışıyor | Kişisel irtibat oluşturma ve **Çalışıyor**'u **Evet** olarak ayarlama. Kişisel irtibatı güncelleştirme ve **Çalışıyor** durumunu değiştirme.  |
| **İzin (Eş/hayat arkadaşı)** | Çalışan > profil > Kişiler > Kişisel bilgileriyle > bağımlı ayrıntıları > Kapsam kaybı > Devamsızlık izni | Kişisel irtibat oluşturuldu ve **İzin başlangıç tarihi** belirlendi. Kişisel irtibat **İzin** güncelleştirildi. Kişisel irtibat **İzin başlangıç tarihi** güncelleştirildi.  |
| **Karşılama değişikliği (pozisyon)** | Çalışan > konumu ataması > çalışan konumu atamaları<br>Pozisyonlar > pozisyonlar | Çalışan pozisyondaki pozisyonda yer değiştirme atama kayıtları. Çalışan pozisyonda yer değiştirme atama kayıtları. |
| **Karşılama değişikliği (maaş)** | Çalışan > Ücret > Sabit planı<br>Çalışan > Kişisel bilgiler > Kazançlar yıllık ücret | Kazançlar yönetimi > İnsan kaynakları paylaşılan parametreleri > Kazançlar > Kazançlar yıllık ücret etkinleştirilmemiş, Çalışan güncelleniyor > Ücret > Sabit plan bir ömür olayı oluşturacaktır. Kazançlar yönetimi > İnsan kaynakları paylaşılan parametreleri > Kazançlar > Kazançlar yıllık ücret etkinleştirilmiş, Çalışan güncelleniyor > Kişisel Bilgiler > Kazançlar yıllık ücret bir ömür olayı oluşturacaktır. |
| **Medicare (Personel/bakmakla yükümlü olunan kişi)** | Çalışan > profil > Kişiler > Kişisel bilgileriyle > bağımlı ayrıntıları > Kapsam kaybı > Medicare yürürlük tarihi | Kişisel irtibat için **Medicare geçerlilik** tarihi eklenmesi veya güncelleştirilmesi bu ömür olayını oluşturur. |
| **Mahkeme kararıyla destek** | Çalışan > profili > kişisel bilgiler > özel kişiler > bağımlı > mahkemeler sipariş edilen destek (QMSCO/QDRO ve yürürlülük tarihleri | Bir kişisel irtibat oluştururken, **Mahkeme kararlı destek** **Evet** olarak ayarlanırsa bir ömür olayı oluşturulur. **Mahkeme kararlı destek** veya **Mahkeme kararının bitiş tarihi**'nin güncelleştirilmesi de bir ömür olayı tetikler. |
| **Ölüm** | Çalışan > profili > kişisel bilgiler > Ölüm tarihi | Bir ölüm tarihi girildi veya güncelleştirildi. |
| **Sigorta kanıtı** | Çalışan > çalışan > sürümleri > İş geçmişi > Tarih Yöneticisi > Kazanç ayrıntıları | **Sigorta kanıtı** **Evet** olarak ayarlı. **Sigorta kanıtı doğrulama tarihi** tanımlandı. |
| **Hak sahibi** | Çalışan > Profil > kişisel bilgileri > Kişisel Kişiler | Bir kişisel ilgili kişi eklenir ve **lehdar** kutu ve **geçerlilik tarihi** doldurulur. Kişisel irtibatın **Çocuk**, **Eş**, **Hayat arkadaşı**, **Kardeş**, **Aile Bireyi**, **Diğer** veya **Ebeveyn** türünden olması gerekir |
| **Personel Medicare'i** | Çalışan > çalışan > sürümleri > İş geçmişi > Tarih Yöneticisi > Kazanç ayrıntıları | **Medicare uygunluğu** **Evet** olarak ayarlandı. **Medicare uygunluk tarihi** değiştirildi. |
| **Doğum günü** | Kazançlar yönetimi > Ömür olayı değişikliği işleme | Bu ömür olayları, **Ömür olayı değişikliği işleme**'den oluşturulur. İşlem, seçilen dönemi ve tüzel kişiliği analiz eder ve ilişkili çalışanları bulur. Son doğum gününü hesaplar ve henüz oluşturulmuşsa bir doğum günü ömür olayı oluşturur. |
| **Çalışan uygunluğu değişikliği (ABD'ye özgü değil)** | Çalışan > İstihdam<br>Çalışan > çalışan > sürümleri > İş geçmişi | Aşağıdaki durumlarda bir ömür olayı oluşturur:<br><ul><li>Eski bir iş varken yeni bir iş oluşturma ve çalışan türünün değişmesi.</li><li>Eski bir iş ayrıntısı varken yeni bir iş ayrıntısı oluşturma ve iş türü veya iş kategorisinin değişmesi.</li><li>İş kaydının güncelleştirilmesi ve farklı bir çalışan türünün belirlenmesi.</li><li>İş ayrıntısı kaydının güncelleştirilmesi ve farklı bir iş türü veya kategorisinin belirtilmesi.</li></ul> |
| **Yeni uygunluk geçersiz kılma (ABD'ye özgü değil)** | İnsan kaynakları Gelişmiş > kazançlar > planlar > kazançlar > uygunluk kuralı geçersiz kılma | Yaşam olayı işlemeyi kullanma<br>Bir çalışan için yeni bir kazanç planı uygunluğu geçersiz kılma oluşturma, bu ömür olayını tetikler.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Uygunluk kuralı geçersiz kılmayı değiştirme (ABD'ye özgü değil)** | İnsan kaynakları Gelişmiş > kazançlar > planlar > kazançlar > uygunluk kuralı geçersiz kılma | Bir kazan planı uygunluk geçersiz kılmada **Geçerlilik başlangıç tarihi** veya **Geçerlilik bitiş tarihi**'nin güncelleştirilmesi bu ömür olayını tetikler. |
| **Uygunluk kuralı geçersiz kılma son tarihi (ABD'ye özgü değil)** | Kazançlar yönetimi > Ömür olayı değişikliği işleme  | Bu ömür olayları, **Ömür olayı değişikliği işleme**'den oluşturulur. İşlem, seçilen dönemi ve tüzel kişiliği analiz eder ve ilişkili kazanç planı uygunluk geçersiz kılmaları bulur. Geçersiz kılmaların süresi dolmuşsa, ömür olayları oluşturur. |
| **Yeni kazanç planı (ABD 'ye özel değil)** | İnsan kaynakları Gelişmiş > Kazançlar > planlar > yeni | Geçerli plana uygunluk seçenekleri eklenir. Uygunluk seçenekleri eklenmiş yeni bir plan eklendi.</br></br>IK personelin bu örnekte ömür olayı uygunluk işlemi çalıştırması gerekir. |
| **Uygunluk kuralı değiştirme (ABD'ye özgü değil)** | Kazançlar yönetimi > Uygunluk kuralları | Yaşam olayı uygunluğunu işlemeyi kullanma **BenefitEligibilityRule** kayıtları aşağıdaki değerlere sahip olduğunda günlüğe kaydedilir: **UseEmplCategory**, **UseEmplStatus** veya **UseEmplType**. Yalnızca değiştirilmiş bir kural veya uygunluk ölçütü için zaten varolan ömür olayı hareketlerini güncelleştirir. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]