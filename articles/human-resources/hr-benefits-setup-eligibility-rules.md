---
title: Uygunluk kurallarını ve seçeneklerini yapılandırma
description: Microsoft Dynamics 365 Human Resources'un sosyal haklar yönetiminde, uygunluk kurallarını ve seçeneklerini ayarlayın.
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
ms.openlocfilehash: 448156a2428e99d8b95de547cb6f1621d49b1c7b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010925"
---
# <a name="configure-eligibility-rules-and-options"></a>Uygunluk kurallarını ve seçeneklerini yapılandırma

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources'Ta sosyal haklar yönetimi için gerekli parametreleri yapılandırdıktan sonra, kazanç planlarınızla ilişkilendireceğiniz uygunluk kuralları, demeti, dönemler ve programlar oluşturabilirsiniz.

## <a name="create-an-eligibility-rule"></a>Uygunluk kuralı oluştur

Uygunluk kuralları, hangi çalışanların her bir kazanç planına kaydolabileceği tanımlar. Uygunluk kurallarını tanımladıktan sonra, onları kazanç planlarına atarsınız. Böylece, her plana uygun olan çalışanları görmek için kayıt uygunluğunu işleyebilirsiniz. 

Açık kayıt sırasında çalışanlar kazanç planlarını seçebilir. Zaten kaydolduktan sonra uygunluk kurallarına dayalı bir kazanç planı için uygun değilse, bunlar otomatik olarak kaydedilmezler. Genellikle, plan uygunluğunu etkileyen bir ömür olayı gerçekleştiğinde, çalışan için uygun oldukları planları seçmek amacıyla bir kayıt dönemi başlatılır. 

1. **Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Uygunluk kuralları ve seçenekleri** seçin.

2. **Uygunluk kuralları** sekmesinde, uygunluk kuralı oluşturmak için **yeni**'yi seçin. Uygunluk kuralıyla ilişkili planları görmek için **ilişik planlar**'ı seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Uygunluk kuralı** | Uygunluk kuralı için benzersiz bir tanımlayıcı. |
   | **Açıklama** | Uygunluk kuralının açıklaması. |
   | **Geçerlilik başlangıç tarihi ve saati** | Uygunluk kuralının başlangıç tarihi. | 
   | **Geçerlilik bitiş tarihi ve saati** | Uygunluk kuralının bitiş tarihi. |
   | **Kullanıcı personel türü** | Kazanç uygunluğu kuralını, çalışanın çalışan tarafından mı kullanacağınızı belirtir. |
   | **Çalışan türü** | Çalışan türü, **Personel türünü kullan** **Evet** olarak ayarlanmışsa. |
   | **Personel durumu kullan** | Kazanç uygunluğu kuralında çalışanın istihdam durumu tarafından mı kullanacağınızı belirtir. |
   | **Durum** | Personel durumu, **Personel durumu kullan** **Evet** olarak ayarlanmışsa. **Personel durumu kullan** **Hayır** olarak ayarlanmışsa alan kullanılmaz. |
   | **İstihdam kategorisi kullan** | Kazanç uygunluğu kuralının parçası olarak çalışanın **İstihdam kategorisi** tarafından mı kullanacağınızı belirtir. | 
   | **İstihdam kategorisi** | **İstihdam kategorisi kullan** geçişi **Evet** olarak ayarlanmışsa, çalışanın istihdam kategorisi. |
   | **Yeni işe alma kuralı kullan** | Sosyal haklar kuralının bir parçası olarak yeni işe alma dönem değerinin kullanılacağını belirtir. |
   | **Kayıt dönemi** | Yeni işe alma kaydına izin verildiği zaman dilimi. Bunu aynı zamanda parametrelerde ayarlarsanız, parametreler ayarı da bunun üzerine öncelik kazanır. |

4. **Ek ölçütler** altında, aşağıdaki seçenekleri seçin ve gerekli bilgileri ekleyin:

   | Seçenek | Tanım |
   | --- | --- |
   | **Uygun yaş** | Uygunluk kuralını karşılamak için gerekli yaş veya Aralık aralıklarını belirtir. |
   | **Uygun departman** | Uygunluk kuralını karşılamak için çalışanın içinde olması gereken Departmanı veya departmanları belirtir. |
   | **Uygun istihdam türü** | Uygunluk kuralını karşılamak için çalışanın içinde olması gereken istihdam türü veya türleri belirtir. Örneğin, tam saat veya parça zaman. |
   | **Uygun iş** | Uygunluk kuralına uyan işi veya işleri belirtir. İşler pozisyonlarla ilişkilendirilir ve pozisyonlar çalışanlar tarafından doldurulur. |
   | **Uygun iş görevi** | Uygunluk kuralına uyan işlevi veya işlevleri belirtir. Örneğin, satış çalışanları veya teknisyenler. |
   | **Uygun iş türü** | Uygunluk kuralına uyan türü veya türleri belirtir. Örneğin, bir büro memuru veya yönetici. |
   | **Uygun tüzel kişilik** | Uygunluk kuralı için geçerli olan yasal varlığı veya yasal varlıkları belirtir. Örneğin, Contoso eğlence sistemi USA. |
   | **Uygun ücret bölgesi** | Uygunluk kuralına uyan çalışan konumunu belirtir. Örneğin, merkez ABD |
   | **Uygun pozisyon** | Uygunluk kuralına uyan pozisyon veya pozisyonları belirtir. Örneğin, İK Yardımcısı veya İK müdürü. |
   | **Uygun pozisyon türü** | Uygunluk kuralına uyan pozisyon veya pozisyonları belirtir. Örneğin, tam zaman. |
   | **Uygun durum** | Uygunluk kuralına uyan iller veya eyaletleri belirtir. Örneğin, Kuzey Dakota ABD veya İngiliz Columbia, Kanada. |
   | **Uygun istihdam koşulları** | Uygunluk kuralına uyan istihdam şartları belirtir. Örneğin, grupta veya grup sözleşmeniz. |
   | **Uygun sendika** | Uygunluk kuralına uyan işçi sendikası üyelikleri belirtir. Örneğin, Amerika Forklift sürücüleri. </br></br>Birleşim tabanlı uygunluk kuralı kullanırken, çalışanın birleşim kaydı bitiş tarihine sahip olmalıdır. Boş bırakamazsınız. |
   | **Uygun Posta kodu** | Uygunluk kuralına uyan ZIP/posta kodu belirtir. Örneğin, 58104. |

5. **Ek ayrıntılı** bilgi için aşağıdaki ek ayrıntıları görüntüleyebilirsiniz:

   | Alan | Tanım |
   | --- | --- |
   | **Uygun kullanıcı alanı** | Müşteri tanımlı alanlara dayalı olarak ek uygunluk kurallarını belirtir. |
   | **Uygunluk türü** | **Ek ölçütler** altında seçtiğiniz ölçüt kategorisini belirtir. |
   | **Uygunluk referansı** | **Ek ölçütler** altında seçtiğiniz değerleri belirtir. |
   | **Açıklama** | **Ek ölçütler** altında seçtiğiniz açıklama. |

6. **Kaydet**'i seçin.

## <a name="configure-bundles"></a>Ürün demetlerini yapılandırma

Bir dizi ilgili kazanç planları kümesidir. Bir çalışanın, başka bir kazanç planına bağımlı olabilecek belirli bir avantaj planına kayıt yapmak için seçmesi gereken kazanç planlarını gruplamak için kazançlar demeti kullanabilirsiniz. Bir ürün demetini kullanmak isteyebileceğiniz durumlarda örnekler şunlardır:

- İlişkili bir sistem durumu tasarruf hesabı (HSA) içeren yüksek kesinti yapılabilen sağlık sigortası içeren bir sistem durumu planı paketi.

- Bir bağımlı ömür planıyla birlikte gelen zorunlu çalışan ömür sigortası planı olan bir ömür sigortası planı. Bu, çalışanın çalışan kapsamı için kaydolmadan bağımlı ömür kapsamını seçmemesini sağlar.

1. **Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Uygunluk kuralları ve seçenekleri** seçin.

2. **Ürün demetleri** sekmesinde, bir paket oluşturmak için **yeni**'yi seçin. Ürün paketiyle ilişkili planları görmek için **ilişik planlar**'ı seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Ürün demeti** | Ürün demeyinin benzersiz tanımlayıcısı |
   | **Açıklama** | Ürün demeti açıklaması. |
   | **Ana** | Paketteki planlardan birinin Master plan olarak işaretlenip işaretlenmemesi gerektiğini gösterir. Ana plan açık kayıt sırasında, kazançlar Yöneticisi çalışanın sosyal haklarının koşullarını onaylayabilmesi için başlangıçta seçilen kümenin bir parçası olarak seçilmelidir. |
   | **Geçerlilik başlangıç tarihi ve saati** | Ürün demetinin etkin olduğu tarih ve saat. |
   | **Geçerlilik bitişi** | Ürün demetinin bitiş tarihi. Varsayılan 12/31/2154'dir ve hiçbir zamanı belirtir. |

4. **Kaydet**'i seçin.

## <a name="configure-periods"></a>Dönemlerini yapılandırma

Dönemler, kazançların etkili olduğu ve çalışanların ne zaman kayıt yapmasına izin verileceğini tanımlar. Yararları korumak için istediğiniz sayıda dönem oluşturabilir, açık kayıt ve kazanç tedarik dönemleri oluşturabilirsiniz. Kazanç planı yıllar takvim yılını izleyebilir veya izleyemeyebilir. 

1. **Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Uygunluk kuralları ve seçenekleri** seçin.

2. **Dönemler** sekmesinde, bir dönem oluşturmak için **yeni**'yi seçin. Geçerli tüm etkin kazanç planlarını avantaj dönemine bağlayan bir işlemi çalıştırmak için, ilgili **Plan Ekle**'yi seçin. Ürün paketiyle ilişkili planları görmek için **ilişik planlar**'ı seçin. 

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Dönem** | Dönemi için benzersiz bir tanımlayıcı. |
   | **Geçerlilik başlangıç tarihi ve saati** | Sosyal haklar döneminin etkin olduğu başlangıç tarihi ve saati. |
   | **Geçerlilik bitiş tarihi ve saati** | Sosyal haklar döneminin devre dışı olduğu tarihi ve saati. |
   | **Kayıt başlangıcı** | Açık kayıt için başlangıç tarihi. Açık kayıt, bir çalışanın self servis avantajlarında avantajlara sahip olması halinde olabilir. |
   | **Kayıt bitişi** | Açık kayıt için bitiş tarihi. |
   | **Aç** | Dönemin, sistem tarihi ve geçerlilik başlangıç ve bitiş tarihleri ile saatleri temel alınarak açık olup olmadığını gösterir. | 
   | **Önceki dönem** | Seçilen kazançlar döneminin önündeki kazançlar dönemini belirtir. Bu bilgiler, önceki bir yıldan planlar, kapsam seçenekleri ve görevlendirilenleri atamak için kazanç uygunluğu kaydı sırasında kullanılır. |
 
4. **Kaydet**'i seçin.

## <a name="use-a-flex-credit-program"></a>Esnek kredi programı kullanma

Çalışanları, önceden belirlenmiş esnek kredi sayısına göre sosyal haklar kaydetmek için, esnek kredi programlarını kullanabilirsiniz. Çalışanlar esnek kredileri nasıl tahsis etmek için seçim yapabilir. Örneğin, bir çalışanın eşinin sağlık durumu planı kapsamında olması durumunda, diğer avantajlara doğru, sistem durumu kapsamında kullanılmasını istedikleri kredileri kullanmak isteyebilir.

1. **Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Uygunluk kuralları ve seçenekleri** seçin.

2. **Dönemler** sekmesinde, **esnek kredi programlarını** seçin.

3. Uygulanacak esnek kredi programını seçin. Alanlar şu bilgileri kapsar:

   | Alan | Tanım |
   | --- | --- |
   | Kazanç kredisi kodu | Esnek kredi programının benzersiz tanımlayıcısı. |
   | Tanım | Esnek kredi programı açıklaması. | 
   | Başlangıç tarihi | Esnek kredi programının etkin olacağı tarih. |
   | Bitiş tarihi | Esnek kredi programının son tarihi. Esnek kredi programının zamanlanan bir sona erme tarihi olmadığını belirtmek için varsayılan değeri (12/31/2154) boş bırakabilirsiniz. |
   | Toplam Kredi Değeri | Her çalışanın avantajları için kullanması gerekecektir kullanılan alacak sayısı. |
   | Eşit Dağıtma Kuralı | Esnek kredi dönemi ortasında bir çalışan işe alındığında, esnek krediler için kullanılacak kural. </br></br><ul><li>**Hiçbiri** – esnek kredi programı başlatıldıktan sonra işe alındığında çalışan esnek kredi almaz.</li><li>**Tam kredi** – çalışan, işe alındıklarında bağımsız olarak, tüm esnek kredi tutarını alır.</li><li>**Eşit dağıt** – çalışan, başlangıç tarihlerine göre eşit miktarda esnek kredi alır.</li></ul> |
   | Esnek Kredi Eşit Dağıtma Formülü | Esnek kredi programının kazanç dönemi ortasında bir çalışan işe alındığında, esnek krediler için kullanılacak kural. Kat, istihdam başlangıç tarihine dayanır. Bu alan yalnızca **eşit dağıtma kural**ı alanında **eşit dağıt** seçeneği seçildiğinde kullanılır. </br></br><ul><li>**Günlük** – bir çalışanın gün düzeyine alacağı esnek kredi sayısı. Esnek kredi toplam sayısı dönem içindeki gün sayısına bölünür. Örneğin, bir avantaj dönemi 400 gün ise, sistem günde alınan esnek kredi sayısını hesaplamak üzere, toplam esnek kredi sayısını 400 ile bölecektir.</li><li>**Geçerli ay** - Bir çalışanın geçerli aya yuvarlanmış, ay düzeyine aldığı esnek kredi sayısı. Esnek kredi toplam sayısı dönem içindeki ay sayısına bölünür. Örneğin, bir avantaj dönemi 15 ay ise, sistem ayda alınan esnek kredi sayısını hesaplamak üzere, toplam esnek kredi sayısını 15 ile bölecektir.</li><li>**Sonraki ay** - Bir çalışanın sonraki aya yuvarlanmış, ay düzeyine aldığı esnek kredi sayısı. Esnek kredi toplam sayısı dönem içindeki ay sayısına bölünür. Örneğin, bir avantaj dönemi 15 ay ise, sistem ayda alınan esnek kredi sayısını hesaplamak üzere, toplam esnek kredi sayısını 15 ile bölecektir.</li></ul> |
   
   Her bir kazanç planının her bir avantaj dönemine göre yalnızca bir esnek kredi programına kaydedildiğinizden emin olun. Aksi durumda, sistem, esnek jenerik vermek için hangi esnek kredi programını kullanacağınızı bilmeyecek ve sorunlarla karşılaşacaksınız. 

## <a name="configure-programs"></a>Programları konfigüre et

Programlar, ortak uygunluk kuralları kümesini paylaşan bir dizi kazanç planındaysa. Her bir plan için, programın tamamı yerine uygunluk kuralları tanımlayabilirsiniz. Örneğin, contoso Kanada FTE programı veya contoso Avrupa Executive-seviye programı. 

1. **Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Uygunluk kuralları ve seçenekleri** seçin.

2. **Programlar** sekmesinde, bir program oluşturmak için **yeni**'yi seçin. Uygunluk kuralı gereksinimlerini karşılamayan çalışanlara özel durumlar yapmak için **uygunluk kuralı geçersiz kılma**'yi seçin. Programla ilişkili planları görmek için **ilişik planlar**'ı seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Program** | Program için benzersiz tanımlayıcı. |
   | **Açıklama** | Programın bir açıklaması | 
   | **Geçerlilik başlangıç tarihi ve saati** | Programın etkin olduğu tarih ve saat. |
   | **Geçerlilik bitiş tarihi ve saati** | Programın süresinin dolduğu olduğu tarih ve saat. Varsayılan 12/31/2154'dir ve hiçbir zamanı belirtir. |
   | **Karşılama bekleme dönemi** | Kazanç programı için, bir çalışanın tedarik başlangıcından önce beklemesi gereken dönem. |
   | **Kesinti bekleme dönemi** | Kazanç programı için kesintiler başlamadan önce bir çalışanın beklemesi gereken dönem. |
   | **Uygunluk kuralları** | Kazançlar programına uygulanacak uygunluk kurallarını seçin. Uygunluk kurallarını bu sayfadaki **uygunluk kuralları** sekmesinde tanımlarsınız. |
   
4. **Kaydet**'i seçin.
