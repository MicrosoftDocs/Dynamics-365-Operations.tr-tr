---
title: Yaşam olayı türlerini yapılandırma
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 93c4285a1918cb625a01b4523195cacdee1170b4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010922"
---
# <a name="configure-life-event-types"></a>Yaşam olayı türlerini yapılandırma

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources, çalışan kazançları kaydını güncelleştirmek için geçerli olduğu olayları tanımlamak için ömür olayı türleri kullanır. Örneğin, evliliğe veya çocuğa sahip olun. Her ömür olayı tür kimliği yalnızca bir ömür olay türüyle ilişkilendirilebilir. Örneğin, çalışan adres değişikliği ömür olay türü ile ilişkilendirilmiş adres değişikliği adlı bir ömür olayı kodu oluşturursanız, çalışan adresi değişikliğini etiketlenmiş başka bir kimlik oluşturamazsınız ve bunu çalışan adı olay türü olan çalışanın adres değişikliğiyle ilişkilendirebilirsiniz. 

Ömür olayı türleri oluşturduktan sonra, onları plan türleriyle ilişkilendirmeniz gerekir. Daha fazla bilgi için, bkz. [Plan türleri oluşturma](hr-benefits-setup-plan-types.md).

   > [!NOTE]
   > Ömür olayı türleri oluşturduktan sonra, onları plan türleriyle ilişkilendirmeniz gerekir. Daha fazla bilgi için, bkz. [Plan türleri oluşturma](hr-benefits-setup-life-event-types.md).

## <a name="create-a-life-event-type"></a>Ömür olayı türü oluştur

1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Yaşam olayı türleri**'nı seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | Yaşam olayı tür kodu | Ömür olayı türü benzersiz tanımlayıcısı. |
   | Tanım | Yşaam olayı türünün açıklaması |
   | Yaşam olayı türü | Bir çalışanın sosyal haklar kaydını güncelleştirmek için bir Catalyst. Ömür olaylarının listesi için, bkz. aşağıdaki [ömür olayları](hr-benefits-setup-payment-frequencies.md?life-events). |

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
| Medeni durum değişikliği | Çalışan > profili > kişisel bilgiler > medeni durum| Medeni durum değişikliği |
| İstihdam durumu değişikliği | <ul><li>Çalışan > İstihdam</li><li>İstihdam geçmişi sayfası</li></ul> | İstihdam durum değişikliği |
| Personel adres değişikliği | <ul><li>Çalışan > profili > adresleri </li><li>Çalışan > kişisel bilgileri > Kişisel Kişiler > adresi</li></ul> Eklenen, düzenlenen veya silinen adres |
| Bakmakla yükümlü olunan kişi değişikliği | <ul><li>Çalışan > profil > Kişiler > Kişisel bilgileriyle > bir bağımlı ekleme veya silme</li><li>Personel self servisi</li></ul> | Bağımlı olarak eklendi veya silindi. Kişisel ilgili kişi ilişkisi çocuk, eşinin, yurtiçi partner veya eski eşinin olmalıdır. **Geçerli başlangıç** tarihinin güncelleştirilmesi ömür olayını tetikler. Bu tarihi güncelleştirmezseniz, hiçbir ömür olayı tetiklenemez. |
| Doğum veya evlat edinme (bakmakla yükümlü olunan kişi) | <ul><li>Çalışan > profil > Kişiler > Kişisel bilgileriyle > bağımlı ayrıntıları</li><li>Personel self servisi</li></ul> | **Benimseme tarihi** alanı dolduruldu. Alt öğenin Doğum tarihi gereklidir. |
| Karşılama kaybı (eş / hayat arkadaşı) | Çalışan > profil > Kişiler > Kişisel bilgileriyle > bağımlı ayrıntıları > Kapsam kaybı | Kişisel bir ilgili kişi için seçilen, **geçerlilik tarihiyle** birlikte seçili **kapsam kaybı** |
| Hayat arkadaşı istihdam değişikliği | Çalışan > profil > Kişiler > Kişisel bilgileriyle > bağımlı ayrıntıları > İşe alındı. | <ul><li>Bağımlı Ayrıntılar kaydı oluşturuldu ve **özel ilgili kişi istihdam** kutusu = Evet</li><li>**Özel ilgili kişi istihdam** kutusu değiştirildi (Evet veya Hayır)</li></ul> |
| İzin (Eş/hayat arkadaşı) | Çalışan > profil > Kişiler > Kişisel bilgileriyle > bağımlı ayrıntıları > Kapsam kaybı > Devamsızlık izni | <ul><li>Bağımlı Ayrıntılar kaydı oluşturuldu ve **EhrLOAEffectiveDate** doldurulmuş</li><li>**personPrivateDetails.EhrIsLOA** değiştirildi (Evet veya Hayır)</li><li>**personPrivateDetails.Ehrloaefekttivedate** değiştirildi</li></ul> |
| Karşılama değişikliği (pozisyon) | <ul><li>Çalışan > konumu ataması > çalışan konumu atamaları</li><li>Pozisyonlar > pozisyonlar</li></ul> | <ul><li>Çalışan pozisyondaki pozisyonda yer değiştirme atama kayıtları</li><li>Çalışan pozisyonda yer değiştirme atama kayıtları</li></ul> |
| Karşılama değişikliği (maaş) | Çalışan > Ücret > Sabit planı | Maaş değiştirdiğinizde maaş otomatik olarak yeniden hesaplama yıllık |
| Medicare (Personel/bakmakla yükümlü olunan kişi) | Çalışan > profil > Kişiler > Kişisel bilgileriyle > bağımlı ayrıntıları > Kapsam kaybı > Medicare yürürlük tarihi | Özel bir ilgili kişi geçerlilik tarihi girdiğinde otomatik olarak tetiklenmez. |
| Mahkeme kararıyla destek | Çalışan > profili > kişisel bilgiler > özel kişiler > bağımlı > mahkemeler sipariş edilen destek (QMSCO/QDRO ve yürürlülük tarihleri | Hiçbir otomatik güncelleştirmeyi tetiklemez. Etkili olmaz; bir ömür olayı kaydeder. |
| Ölüm | Çalışan > profili > kişisel bilgiler > Ölüm tarihi | Bir ölüm tarihi girildi |
| Sigorta kanıtı | <ul><li>Çalışan > çalışan > sürümleri > İş geçmişi > Tarih Yöneticisi > Kazanç ayrıntıları</li><li> Çalışan > İstihdam > kazanç ayrıntıları > doğrulama tarihi</li></ul> | <ul><li>Bir çalışan bir doğrulama tarihine giriyor</li><li>Bir çalışan, beliret EvidenceOfInsurability alanını **Evet** olarak ayarlar</li></ul> |
| Lehtar | Çalışan > Profil > kişisel bilgileri > Kişisel Kişiler | Bir kişisel ilgili kişi eklenir ve **lehdar** kutu ve **geçerlilik tarihi** doldurulur. Kişisel ilgili kişi **çocuk**, **eşinin**, **DomesticPartner**, **kardeş**, **FamilyContact**, **othercontact**, **Ebeveyn**, **BeneficiaryEstate**, **BeneficiaryOrg** veya **BeneficiaryTrust** olmalıdır. |
| Personel Medicare'i | Çalışan > çalışan > sürümleri > İş geçmişi > Tarih Yöneticisi > Kazanç ayrıntıları | <ul><li>**EhrMedicareEligibilityDate** değiştirildi</li><li>**MedicareEligibile** **Evet** olarak ayarlanır</li></ul> |
| Doğum günü | Çalışan > profil > Kişiler > Kişisel bilgileriyle > bağımlı ayrıntıları > Doğum tarihi | Doğum tarihi eklendi veya güncelleştirildi (ömür olayı değişikliği işleminden sonra değil). Örnek: bir çocuk için **özel ilgili kişi uygunluğu seçenekleri** Kurulum > Kazançlar > özel ilgili kişi uygunluğu seçeneklerinde Yaş: > 26 olarak ayarlandıysa ve İK personeli, bağımlı kişi 26 olsuktan sonra Yaşam etkinlik değişikliği işlemini çalıştırırsa bağımlı öğenin artık kapsama uygun olmadığını bildiren bir ileti görüntülenir. |
| Çalışan uygunluğu değişikliği (ABD'ye özgü değil) | <ul><li>Çalışan > İstihdam</li><li>Çalışan > çalışan > sürümleri > İş geçmişi</li></ul> | <ul><li>Çalışan türü, İş kategorisi veya beş Kullanıcı tanımlı uygunluk alanları değişikliği</li><li>**HcmEmploymentDetail.EhrEmploymentType** değişiklikleri (yeniden işe alma ve işten çıkarma gibi *yeni* iş kayıtları için işlenmediği, yalnızca *değiştirilmiş* istihdam ayrıntısı kayıtları için işlenir)</li></ul> |
| Yeni uygunluk geçersiz kılma (ABD'ye özgü değil) | İnsan kaynakları Gelişmiş > kazançlar > planlar > kazançlar > uygunluk kuralı geçersiz kılma | Yaşam olayı işlemeyi kullanma | EhrBenefitEligibilityRuleOverride.ValidFrom |
| Uygunluk kuralı geçersiz kılmayı değiştirme (ABD'ye özgü değil) | İnsan kaynakları Gelişmiş > kazançlar > planlar > kazançlar > uygunluk kuralı geçersiz kılma | Yaşam olayı işlemeyi kullanma (yalnızca uygunluk kuralı geçersiz kılmada yapılan değişiklikleri **ValidFrom** ve **ValidTo** alanlarında yakalar) |
| Uygunluk kuralı geçersiz kılma son tarihi (ABD'ye özgü değil) | İnsan kaynakları Gelişmiş > kazançlar > planlar > kazançlar > uygunluk kuralı geçersiz kılma | Yaşam olayı değişikliğini işlemeyi kullanma Örneğin, bir planın uygunluk kuralını geçersiz kılma sona erme tarihi 17:00 veya aşağıdaki günlerde bugün olacak şekilde 17:00 zaman aşımına uğradı ve sonra da ömür olayı değişikliği işlemeyi çalıştırdıktan sonra, uygunluk kuralının geçersiz kılındığını bildiren bir ileti görüntülenir. |
| Yeni kazanç planı (ABD 'ye özel değil) | İnsan kaynakları Gelişmiş > Kazançlar > planlar > yeni | <ul><li>Geçerli plana uygunluk seçenekleri eklenir</li><li>Uygunluk seçenekleri eklenmiş yeni bir plan eklendi</li></ul></br></br>IK personelin bu örnekte ömür olayı uygunluk işlemi çalıştırması gerekir. |
| Uygunluk kuralı değiştirme (ABD'ye özgü değil) | İnsan kaynakları Gelişmiş > kazançlar > Kurallar/seçenekler > uygunluk kuralları | Yaşam olayı uygunluğunu işlemeyi kullanma **EhrBenefitEligibilityRule** kayıtları aşağıdaki değerlere sahip olduğunda günlüğe kaydedilir: **UseEmplCategory**, **UseEmplStatus** veya **UseEmplType**. Yalnızca değiştirilmiş bir kural veya uygunluk ölçütü için zaten varolan ömür olayı hareketlerini güncelleştirir. |
