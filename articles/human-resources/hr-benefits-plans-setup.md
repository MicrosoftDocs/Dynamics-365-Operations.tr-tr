---
title: Bir kazanç planı oluştur
description: Dynamics 365 Human Resources'da Kazanç planlarını ayarlama
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanListPage, BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 97c3acf1294b7a8c2496f23a32918152f50a9e5e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010878"
---
# <a name="create-a-benefits-plan"></a>Bir kazanç planı oluştur

[!include [banner](includes/preview-feature.md)]

Bu makalede, Dynamics 365 Human Resources'de kazanç planlarının nasıl ayarlanacağı gösterilmektedir.

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. **Yeni**'yi seçin.

3. **Genel** sekmesinde, aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | Plan | PLanın benzersiz tanımlayıcısı. |
   | Tanım | Planın açıklaması. |
   | Plan türü | Yeni bir plan oluşturduğunuzda, plan türünü belirtmeniz gerekir. Plan tipi belirli avantaj tiplerinin üst düzey gruplandırmasıdır. Her plan türü bir çalışanın o tipte birden çok plana kaydolabileceğini belirtir, ilgili kişilerin lehdar veya bağımlı olup olmadığını belirtir ve karşılama seçeneklerini tanımlar. Sosyal haklar tekliflerinizin gereksinimlerini karşılamak için yeni özel plan türleri oluşturabilirsiniz. Başlıca kazanç planı türleri şunlardır: <ul><li>401K</li><li>ADD</li><li>Dişle ilgili</li><li>Fitness</li><li>FSA</li><li>Yaşam</li><li>LTD</li><li>Tıbbi</li><li>PTO</li><li>STD</li><li>Görüş</li></ul> |
   | Plan türü kodu | Plan türünün plan türü kodu. |
   | Program | Plana isteğe bağlı olarak atanacak bir program belirtir. |
   | Ürün demeti | Plana isteğe bağlı olarak atanacak bir ürün demeti belirtir. |
   | Ana | Planın atandığı ürün demetinde master plan olup olmadığını belirtir. |
   | Durum | Kazanç planının geçerli durumunu belirtir. Varsayılan değer Etkin'dir. Durumu etkin değil olarak değiştirirseniz, plan kayıt sırasında seçim olarak kullanılamaz. |
   | Geçerlilik başlangıç tarihi ve saati | Planın başladığı tarih ve saati Geçerli değer varsayılan sistem tarihidir. |
   | Geçerlilik bitiş tarihi ve saati | Planın bitiş tarihi ve saati (durum, devre dışı olarak ayarlı). Varsayılan değer 12/31/2154'dir ve hiçbir zaman bunu belirtir. |

4. **Konfigürasyon** sekmesinde, oluşturmakta olduğunuz planın türüne bağlı olarak aşağıdaki alanlar için değer belirtin:

   | Plan türü | Alan | Tanım |
   | --- | --- | --- |
   | Tıp (tıp, dental, vizyon, HMO) | COBRA | Planın COBRA (Konsolide Çok maddeli bütçe mutabakat Yasası) uygun olup olmayacağını belirtir. |
   | Tıp (tıp, dental, vizyon, HMO) | HIPAA | Planın HIPAA (sağlık sigortası taşınabilirlik ve Sorumluluk Yasası) uygun olup olmayacağını belirtir. |
   | <ul><li>Tıp (tıp, dental, vizyon, HMO)</li><li>Diğer (PTE, Fitness)</li><li>Diğer</li><li>Uzun süreli engellilik</li><li>ADD (temel ömür, gönüllü kullanım ömrü)</li><li>Tasarruf (örneğin, 401(k))</li><li>FSA</li></ul> | Vergi öncesinde uygun | Vergiler uygulanmadan önce plana katkıların yapılıp yapılmayacağını belirtir. |
   | <ul><li>Tıp (tıp, dental, vizyon, HMO)</li><li>Diğer (PTE, Fitness)</li><li>Uzun süreli engellilik</li><li>ADD (temel ömür, gönüllü kullanım ömrü)</li><li>Tasarruf (örneğin, 401(k))</li><li>FSA</li></ul> | Uygun vergiyi deftere naklet | Vergiler uygulandıktan sonra plana katkıların yapılıp yapılmayacağını belirtir. |
   | <ul><li>Tıp (tıp, dental, vizyon, HMO)</li><li>Diğer (PTE, Fitness)</li><li>Uzun süreli engellilik</li><li>ADD (temel ömür, gönüllü kullanım ömrü)</li><li>Tasarruf (örneğin, 401(k))</li><li>FSA</li></ul> | Katkıda bulunan | Plana kimlerin katkıda bulunduğunu, çalışanı, işvereni veya her ikisini belirtir. |
   | <ul><li>Uzun süreli engellilik</li><li>ADD (temel ömür, gönüllü kullanım ömrü)</li></ul> | Minimum karşılama | Plan için gerekli olan minimum sigorta kapsamı tutarı. |
   | <ul><li>Uzun süreli engellilik</li><li>ADD (temel ömür, gönüllü kullanım ömrü)</li></ul> | Maksimum karşılama | Plan için gerekli olan maksimum sigorta kapsamı tutarı. |
   | <ul><li>Uzun süreli engellilik</li><li>ADD (temel ömür, gönüllü kullanım ömrü)</li></ul> | Kapsam artışlarını kullan | Kapsam tutarının geçerli bir artan tutarla eşleşmediğini doğrulamak için doğrulama yapılıp yapılmayacağını belirtir. |
   | <ul><li>Uzun süreli engellilik</li><li>ADD (temel ömür, gönüllü kullanım ömrü)</li></ul> | Artışlı tutar | Plan için artımlı sigorta kapsamı tutarı. Örneğin, artan tutar 1.000 ise, bir çalışanın sigorta $200.500 olamaz, $201.000 veya $200.000'e yuvarlama yapmaları gerekir. |
   | <ul><li>Uzun süreli engellilik</li><li>ADD (temel ömür, gönüllü kullanım ömrü)</li></ul> | Artışlı yön | Karşılama tutarı artışlı tutar değerini karşılamıyorken yukarı veya aşağı yuvarlama yönünü belirtir. |
   | ADD (temel ömür, gönüllü kullanım ömrü) | Sigorta kanıtı | Bir çalışanın aşırı sayıda kanıt sağlayıp sağlamaması gerektiğini belirtir. |
   | ADD (temel ömür, gönüllü kullanım ömrü) | Tutar | Muhasebe para birimi cinsinden tutar. Bu alan yalnızca Sigortalanabilirlik kanıtı onay kutusunun etkin olması durumunda kullanılabilir. |
   | <ul><li>Tasarruf (örneğin, 401(k))</li><li>FSA</li></ul> | Minimum yıllık katkı | Plan için gerekli olan minimum katkı tutarı. |
   | <ul><li>Tasarruf (örneğin, 401(k))</li><li>FSA</li></ul> | Maksimum yıllık katkı | Plan için gerekli olan maksimum katkı tutarı. |
   | Tasarruf (örneğin, 401(k)) | İşverenin maksimum yıllık tutarı | Bir işverenin, bir kazanç döneminde bir çalışan tasarruf planına göre katkıda bulunmasına izin verilen maksimum tutar. Bu alanı kullanmak için işveren eşleştirmesi onay kutusunu seçmeniz gerekir. |
   | Tasarruf (örneğin, 401(k)) | İşveren eşleşmesi | Personel tasarruf planına işverenin katkıda bulunup bluunmadığını belirtir. |
   | Tasarruf (örneğin, 401(k)) | İşveren eşleştirme yüzdesi | İşverenin eşleşmesi gereken bir çalışan katkısı yüzdesi. |
   | Tasarruf (örneğin, 401(k)) | İşveren kapasite eşleşmesi | İşverenin eşleşmesi için maksimum yüzde. Örneğin, bir işveren çalışanın ödemesine kadar %6'ya kadar olan çalışan katkılarına %100 uyacaksa, işverenin eşleşme şapkası %6'dır. |

5. **Kurulum** sekmesinde, aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | Kaydolmaya izin ver/devam et | Uygunluğu, uygunluk gereksinimlerini karşılıyorsa, çalışanların plana kaydolabileceği kayıt olup olmayacağını belirtir.</br></br>Bu Hayır olarak ayarlanmışsa, uygunluğu gerçekleştirdiğinizde planlama çalışanlar tarafından kullanılamaz. |
   | Önceki yıldan otomatik olarak kaydet | Uygun bir personelin önceki yıl boyunca kayıtlıysa plana otomatik olarak kaydedilip kaydedilmeyeceğini belirtir. |
   | Varsayılan olarak otomatik kaydet | Varsayılan olarak kayıt planının görünüp görünmeyeceğini belirtir. Plan zorunlu olmadığı için, çalışanın varsayılan seçimi değiştirebilmesini sağlayacak. |
   | Yeni kayıtlara kapatıldı | Planın yalnızca önceki yılın planında kayıtlı olan çalışanlarla sınırlandırılıp kısıtlanmayacağını belirtir. |
   | Zorunlu plan | Plandaki çalışanların otomatik olarak kaydedilip kaydedilmeyeceğini belirtir. Çalışanlar kayıt seçimini değiştiremez. |
   | Başlangıç tarihi | Planın şirkette oluşturulduğu tarih. |
   | Satıcı hesabı (kazanç tedarikçisi) | Şirketin, plan için prim ödediği satıcı. |
   | Ad (kazanç tedarikçisi) | Satıcının adı. |
   | Satıcı refernsı (kazanç tedarikçisi) | Planla ilgili olarak Satıcının referansı. Örneğin, şirketin grup planı numarası. |
   | Alternatif referans (kazanç tedarikçisi) | Planla ilgili olarak Satıcının alternatif referansı. Örneğin, şirketin hesap numarası. |
   | Para birimi (Kazanç tedarikçisi) | Primye prim ödemesi için kullanılan para birimi. |
   | Gider hesabı (kazanç tedarikçisi) | Plan primleri için gider hesabı olarak kullanılan genel muhasebe hesabı. |
   | Satıcı hesabı (kazanç yöneticisi) | Şirketin, planı yönetmesi için ödeme yaptığı satıcı. Planı kendi kendine uygulanıyorsa bu alanı boş bırakın. |
   | Ad (kazanç Yöneticisi) | Kazanç yöneticisi satıcısının adı. |
   | Satıcı referansı (kazanç yöneticisi) | Planla ilgili olarak Satıcının yönetici referansı. |
   | Alternatif referans (kazanç yöneticisi) | Planla ilgili olarak Satıcının alternatif yönetici referansı. |
   | Para birimi (kazanç Yöneticisi) | Kazanç yöneticisini ödemesi için kullanılan para birimi. |
   | Gider hesabı (kazanç yöneticisi) | Planın yönetimiyle ilişkili maliyetler için gider hesabı olarak kullanılan genel muhasebe hesabı. |

6. **Filtreler** sekmesinde gerektiği şekilde filtreleyin. Aşağıdaki alanlara göre filtre uygulayabilirsiniz:

   - İş birimi
   - Departman
   - Tüzel kişilik
   - Konum
   - Bölme

7. **Uygunluk kuralları** sekmesinde, aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | Satır numarası | Uygunluk kuralı satır numarası. |
   | Uygunluk kuralı | Kazanç planına uygulanacak uygunluk kuralı. Bu uygunluk kuralı ilgili eylem türüne uygulanır ve belirtilen tedarik bekleme dönemiyle ve kesintiler ile ilişkilendirilir. |
   | Eylem türü | Uygunluk kuralının uygulanacağı eylem: Sosyal haklar kaydolma veya sosyal işlem süresi sonu. |
   | Karşılama bekleme dönemi | Bekleme süreleri formundan alınan bir değer. Kapsam bekleme dönemi bir çalışanın, uygunluk kuralı ve eylem türündeki ölçütleri temel alarak kazanç kapsamını veya kullanım süresi sonunu beklediği gün veya ay sayısını bekler. |
   | Kesinti bekleme dönemi | Bekleme süreleri formundan alınan bir değer. Kesinti bekleme dönemi bir çalışanın, uygunluk kuralı ve eylem türündeki ölçütleri temel alarak maaşından kazanç kesintilerini beklediği gün veya ay sayısını bekler. |

8. **Kaydet**'i seçin.

## <a name="view-enrolled-workers"></a>Kayıtlı çalışanları görüntüle

Seçilen kazanç planına atanan kayıtlı çalışanları görüntüle

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. **Kayıtlı çalışanlar**'ı seçin.

## <a name="attach-coverage-options"></a>Karşılama seçenekleri ekle

Seçili kazançlar planına karşılama seçenekleri ekleyebilirsiniz. Kapsama seçenekleri eklenmesi, tedarik seçeneği için kuru ve kesinti kurulumunu birlikte getirir.  Örnek: tıbbi bir plan için Kullanıcı bir aile kapsamı seçeneği seçer.  Daha sonra, ilişkili plan (Kur ayarla kurulumu) ve ilişkili plana ait kesinti için (Kurulum Kurda ayarlanır) aile hızını seçmek gerekecektir. Bu, seçilen bir tedarik için işveren ve çalışan için maliyet sağlar. Daha sonra, bir çalışan + 1 kapsmaı veya çalışan kapsamı için işlemi tekrarlayabilirsiniz.

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. **Tedarik seçeneklerini İliştir**'i seçin.

## <a name="override-eligibility-rules"></a>Uygunluk kurallarını geçersiz kıl

Uygunluk kurallarına özel durumlar olarak bir plana çalışan ekleyebilirsiniz. Eklediğiniz her çalışan sosyal haklar planı için uygun olacak.

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. **Uygunluk kurallarını geçersiz kıl**'ı seçin.

## <a name="view-attached-periods"></a>Ekli dönemlerini görüntüle

Kullanılabilir kazançlar dönemlerinin bir listesini görebilirsiniz.

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. **Dönem** seçin.

## <a name="view-plan-information"></a>Plan bilgilerini görüntüle

Çalışanların sosyal haklar seçimlerini sağlayacak şekilde plana ilişkin bir açıklama sağlayabilirsiniz. Buraya girdiğiniz plan bilgileri, kapsam seçenekleri listesindeki planda vurgulama sırasında, çalışan self servis 'da görüntülenir.

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. **Plan bilgilerini** seçin .

## <a name="view-flex-credit-programs"></a>Esnek kredi programlarını görüntüle

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. **Esnek kredi programları**'nı seçin.
