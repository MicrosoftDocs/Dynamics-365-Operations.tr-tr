---
title: Bir kazanç planı oluştur
description: Dynamics 365 Human Resources'da Kazanç planlarını ayarlama
author: andreabichsel
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitPlanListPage, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d95fce78102ebed52a9a2df0855767c3fd97f574
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052229"
---
# <a name="create-a-benefit-plan"></a>Kazanç planı oluşturma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources'de kazanç planlarının nasıl ayarlanacağı gösterilmektedir.

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. **Yeni**'yi seçin.

3. **Genel** sekmesinde, aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Plan** | PLanın benzersiz tanımlayıcısı. |
   | **Tanım** | Planın açıklaması. |
   | **Plan türü** | Yeni bir plan oluşturduğunuzda, plan türünü belirtmeniz gerekir. Plan tipi belirli avantaj tiplerinin üst düzey gruplandırmasıdır. Her plan türü bir çalışanın o tipte birden çok plana kaydolabileceğini belirtir, ilgili kişilerin lehdar veya bağımlı olup olmadığını belirtir ve karşılama seçeneklerini tanımlar. Sosyal haklar tekliflerinizin gereksinimlerini karşılamak için yeni özel plan türleri oluşturabilirsiniz. Başlıca kazanç planı türleri şunlardır: <ul><li>401K</li><li>ADD</li><li>Dişle ilgili</li><li>Fitness</li><li>FSA</li><li>Yaşam</li><li>LTD</li><li>Tıbbi</li><li>PTO</li><li>STD</li><li>Görüş</li></ul> |
   | **Plan türü kodu** | Plan türünün plan türü kodu. |
   | **Program** | Plana isteğe bağlı olarak atanacak bir program belirtir. |
   | **Ürün demeti** | Plana isteğe bağlı olarak atanacak bir ürün demeti belirtir. |
   | **Ana** | Planın atandığı ürün demetinde master plan olup olmadığını belirtir. |
   | **Geçerlilik başlangıç tarihi ve saati** | Planın başladığı tarih ve saati Geçerli değer varsayılan sistem tarihidir. |
   | **Geçerlilik bitiş tarihi ve saati** | Planın bittiği tarih ve saat. Varsayılan değer 12/31/2154'dir ve hiçbir zaman bunu belirtir. |

4. **Konfigürasyon** sekmesinde, oluşturmakta olduğunuz planın türüne bağlı olarak aşağıdaki alanlar için değer belirtin:

   | Plan türü | Alan | Tanım |
   | --- | --- | --- |
   | Tıp (tıp, dental, vizyon, HMO) | COBRA | Planın COBRA (Konsolide Çok maddeli bütçe mutabakat Yasası) uygun olup olmayacağını belirtir. |
   | Tıp (tıp, dental, vizyon, HMO) | HIPAA | Planın HIPAA (sağlık sigortası taşınabilirlik ve Sorumluluk Yasası) uygun olup olmayacağını belirtir. |
   | Tıp (tıp, dental, vizyon, HMO)<br><br>Diğer (PTE, Fitness)<br><br>Diğer<br><br>Uzun süreli engellilik<br><br>ADD (temel ömür, gönüllü kullanım ömrü)<br><br>Tasarruf (örneğin, 401(k))<br><br>FSA | Vergi öncesinde uygun | Vergiler uygulanmadan önce plana katkıların yapılıp yapılmayacağını belirtir. |
   | Tıp (tıp, dental, vizyon, HMO)<br><br>Diğer (PTE, Fitness)<br><br>Uzun süreli engellilik<br><br>ADD (temel ömür, gönüllü kullanım ömrü)<br><br>Tasarruf (örneğin, 401(k))<br><br>FSA | Uygun vergiyi deftere naklet | Vergiler uygulandıktan sonra plana katkıların yapılıp yapılmayacağını belirtir. |
   | Tıp (tıp, dental, vizyon, HMO)<br><br>Diğer (PTE, Fitness)<br><br>Uzun süreli engellilik<br><br>ADD (temel ömür, gönüllü kullanım ömrü)<br><br>Tasarruf (örneğin, 401(k))<br><br>FSA | Katkıda bulunan | Plana kimlerin katkıda bulunduğunu, çalışanı, işvereni veya her ikisini belirtir. |
   | Uzun süreli engellilik<br><br>ADD (temel ömür, gönüllü kullanım ömrü) | Minimum karşılama | Plan için gerekli olan minimum sigorta kapsamı tutarı. |
   | Uzun süreli engellilik<br><br>ADD (temel ömür, gönüllü kullanım ömrü) | Maksimum karşılama | Plan için gerekli olan maksimum sigorta kapsamı tutarı. |
   | Uzun süreli engellilik<br><br>ADD (temel ömür, gönüllü kullanım ömrü) | Kapsam artışlarını kullan | Kapsam tutarının geçerli bir artan tutarla eşleşmediğini doğrulamak için doğrulama yapılıp yapılmayacağını belirtir. |
   | Uzun süreli engellilik<br><br>ADD (temel ömür, gönüllü kullanım ömrü) | Artışlı tutar | Plan için artımlı sigorta kapsamı tutarı. Örneğin, artan tutar 1.000 ise, bir çalışanın sigorta $200.500 olamaz, $201.000 veya $200.000'e yuvarlama yapmaları gerekir. |
   | Uzun süreli engellilik<br><br>ADD (temel ömür, gönüllü kullanım ömrü) | Artışlı yön | Karşılama tutarı artışlı tutar değerini karşılamıyorken yukarı veya aşağı yuvarlama yönünü belirtir. |
   | ADD (temel ömür, gönüllü kullanım ömrü) | Sigorta kanıtı | Bir çalışanın aşırı sayıda kanıt sağlayıp sağlamaması gerektiğini belirtir. |
   | ADD (temel ömür, gönüllü kullanım ömrü) | Tutar | Muhasebe para birimi cinsinden tutar. Bu alan yalnızca Sigortalanabilirlik kanıtı onay kutusunun etkin olması durumunda kullanılabilir. |
   | Tasarruf (örneğin, 401(k))<br><br>FSA | Minimum yıllık katkı | Plan için gerekli olan minimum katkı tutarı. |
   | Tasarruf (örneğin, 401(k))<br><br>FSA | Maksimum yıllık katkı | Plan için gerekli olan maksimum katkı tutarı. |
   | Tasarruf (örneğin, 401(k)) | İşverenin maksimum yıllık tutarı | Bir işverenin, bir kazanç döneminde bir çalışan tasarruf planına göre katkıda bulunmasına izin verilen maksimum tutar. Bu alanı kullanmak için işveren eşleştirmesi onay kutusunu seçmeniz gerekir. |
   | Tasarruf (örneğin, 401(k)) | İşveren eşleşmesi | Personel tasarruf planına işverenin katkıda bulunup bluunmadığını belirtir. |
   | Tasarruf (örneğin, 401(k)) | İşveren eşleştirme yüzdesi | İşverenin eşleşmesi gereken bir çalışan katkısı yüzdesi. |
   | Tasarruf (örneğin, 401(k)) | İşveren kapasite eşleşmesi | İşverenin eşleşmesi için maksimum yüzde. Örneğin, bir işveren çalışanın ödemesine kadar %6'ya kadar olan çalışan katkılarına %100 uyacaksa, işverenin eşleşme şapkası %6'dır. |

5. **Kurulum** sekmesinde, aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Kaydolmaya izin ver/devam et** | Uygunluğu, uygunluk gereksinimlerini karşılıyorsa, çalışanların plana kaydolabileceği kayıt olup olmayacağını belirtir.</br></br>Bu Hayır olarak ayarlanmışsa, uygunluğu gerçekleştirdiğinizde planlama çalışanlar tarafından kullanılamaz. |
   | **Önceki yıldan otomatik olarak kaydet** | Uygun bir personelin önceki yıl boyunca kayıtlıysa plana otomatik olarak kaydedilip kaydedilmeyeceğini belirtir. |
   | **Varsayılan olarak otomatik kaydet** | Varsayılan olarak kayıt planının görünüp görünmeyeceğini belirtir. Plan zorunlu olmadığı için, çalışanın varsayılan seçimi değiştirebilmesini sağlayacak. |
   | **Yeni kayıtlara kapatıldı** | Planın yalnızca önceki yılın planında kayıtlı olan çalışanlarla sınırlandırılıp kısıtlanmayacağını belirtir. |
   | **Zorunlu plan** | Plandaki çalışanların otomatik olarak kaydedilip kaydedilmeyeceğini belirtir. Çalışanlar kayıt seçimini değiştiremez. |
   | **Başlangıç tarihi** | Planın şirkette oluşturulduğu tarih. |
   | **Satıcı hesabı** (Kazanç tedarikçisi) | Şirketin, plan için prim ödediği satıcı. |
   | **Ad** (Kazanç tedarikçisi) | Satıcının adı. |
   | **Satıcı referansı** (Kazanç tedarikçisi) | Planla ilgili olarak Satıcının referansı. Örneğin, şirketin grup planı numarası. |
   | **Alternatif referans** (Kazanç tedarikçisi) | Planla ilgili olarak Satıcının alternatif referansı. Örneğin, şirketin hesap numarası. |
   | **Para birimi** (Kazanç tedarikçisi) | Primye prim ödemesi için kullanılan para birimi. |
   | **Gider hesabı** (Kazanç tedarikçisi) | Plan primleri için gider hesabı olarak kullanılan genel muhasebe hesabı. |
   | **Satıcı hesabı** (Kazanç yöneticisi) | Şirketin, planı yönetmesi için ödeme yaptığı satıcı. Planı kendi kendine uygulanıyorsa bu alanı boş bırakın. |
   | **Ad** (Kazanç yöneticisi) | Kazanç yöneticisi satıcısının adı. |
   | **Satıcı referansı** (Kazanç yöneticisi) | Planla ilgili olarak Satıcının yönetici referansı. |
   | **Alternatif referans** (Kazanç yöneticisi) | Planla ilgili olarak Satıcının alternatif yönetici referansı. |
   | **Para birimi** (Kazanç yöneticisi) | Kazanç yöneticisini ödemesi için kullanılan para birimi. |
   | **Gider hesabı** (Kazanç yöneticisi) | Planın yönetimiyle ilişkili maliyetler için gider hesabı olarak kullanılan genel muhasebe hesabı. |

6. **Filtreler** sekmesinde gerektiği şekilde filtreleyin. Aşağıdaki alanlara göre filtre uygulayabilirsiniz:

   - **İş birimi**
   - **Departman**
   - **Tüzel kişilik**
   - **Konum**
   - **Bölme**

7. **Uygunluk kuralları** sekmesinde, aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Satır numarası** | Uygunluk kuralı satır numarası. |
   | **Uygunluk kuralı** | Kazanç planına uygulanacak uygunluk kuralı. Bu uygunluk kuralı ilgili eylem türüne uygulanır ve belirtilen tedarik bekleme dönemiyle ve kesintiler ile ilişkilendirilir. |
   | **Eylem türü** | Uygunluk kuralının uygulanacağı eylem: Sosyal haklar kaydolma veya sosyal işlem süresi sonu. |
   | **Karşılama bekleme dönemi** | Bekleme süreleri formundan alınan bir değer. Kapsam bekleme dönemi bir çalışanın, uygunluk kuralı ve eylem türündeki ölçütleri temel alarak kazanç kapsamını veya kullanım süresi sonunu beklediği gün veya ay sayısını bekler. |
   | **Kesinti bekleme dönemi** | Bekleme süreleri formundan alınan bir değer. Kesinti bekleme dönemi bir çalışanın, uygunluk kuralı ve eylem türündeki ölçütleri temel alarak maaşından kazanç kesintilerini beklediği gün veya ay sayısını bekler. |

8. **Kaydet**'i seçin.

## <a name="view-enrolled-workers"></a>Kayıtlı çalışanları görüntüle

Seçilen kazanç planına atanan kayıtlı çalışanları görüntüle

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. Gezinme çubuğundaki **kazançlar** sekmesinde, **kayıtlı çalışanlar**'ı seçin.

## <a name="attach-coverage-options"></a>Karşılama seçenekleri ekle

Seçili kazançlar planına karşılama seçenekleri ekleyebilirsiniz. Kapsama seçenekleri eklenmesi, tedarik seçeneği için kuru ve kesinti kurulumunu birlikte getirir.  Örnek: tıbbi bir plan için Kullanıcı bir aile kapsamı seçeneği seçer.  Daha sonra, ilişkili plan (Kur ayarla kurulumu) ve ilişkili plana ait kesinti için (Kurulum Kurda ayarlanır) aile hızını seçmek gerekecektir. Bu, seçilen bir tedarik için işveren ve çalışan için maliyet sağlar. Daha sonra, bir çalışan + 1 kapsmaı veya çalışan kapsamı için işlemi tekrarlayabilirsiniz.

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. Gezinme çubuğundaki **kazançlar** sekmesinde, **Tedarik seçeneklerini iliştir**'i seçin.

## <a name="override-eligibility-rules"></a>Uygunluk kurallarını geçersiz kıl

Uygunluk kurallarına özel durumlar olarak bir plana çalışan ekleyebilirsiniz. Eklediğiniz her çalışan sosyal haklar planı için uygun olacak.

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. Gezinme çubuğundaki **kazançlar** sekmesinde, **Uygunluk kurallarını geçersiz kıl**'ı seçin.

## <a name="view-attached-periods"></a>Ekli dönemlerini görüntüle

Kullanılabilir kazançlar dönemlerinin bir listesini görebilirsiniz.

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. Gezinme çubuğunda **Dönemler** sekmesini seçin.

## <a name="view-plan-description"></a>Plan açıklamasını incele

Çalışanların sosyal haklar seçimlerini sağlayacak şekilde plana ilişkin bir açıklama sağlayabilirsiniz. Buraya girdiğiniz plan açıklaması kapsam seçenekleri listesindeki planda vurgulama sırasında, çalışan self servis 'da görüntülenir.

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. Gezinme çubuğundaki **kazançlar** sekmesinde, **Plan açıklaması**'nı seçin.

## <a name="view-flex-credit-programs"></a>Esnek kredi programlarını görüntüle

1. **Sosyal haklar** yönetimi çalışma alanında, **Planlar** altında, **kazanç planları**'nı seçin.

2. Gezinme çubuğundaki **kazançlar** sekmesinde, **Esnek kredi programları**'nı seçin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]