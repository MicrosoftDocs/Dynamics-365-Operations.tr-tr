---
title: Bakım işi türü kategorileri ve bakım işi türleri, bakım işi türü çeşitlemeleri, bakım zanaatları ve bakım denetim listeleri
description: Bu konuda, Varlık Yönetimi'nde bakım işi türü kategorileri ve bakım işi türleri, bakım işi türü çeşitlemeleri, bakım zanaatları ve bakım denetim listeleri açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetJobTypeDefaultForecast, EntAssetJobTrade, EntAssetJobTypeDefaultCopy, EntAssetChecklistVariableValueLookup, EntAssetChecklistTemplateCreate, EntAssetJobVariant, EntAssetJobTypeDefaultReference, EntAssetJobTypeDefaultChecklist, EntAssetJobTypeDefault, EntAssetJobType, EntAssetJobTypeDefaultChecklistCopy, EntAssetChecklistTemplate, EntAssetJobTypeDefaultDescription, EntAssetJobTypeLookup, EntAssetJobTypeDefaultToolCopy, EntAssetJobTypePreviewPart, EntAssetJobTypeDefaultTool, EntAssetJobTypeDefaultForecastCopy, EntAssetChecklistTemplateLookup, EntAssetJobGroup, EntAssetChecklistVariable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8bf7c53a6150a2beeca5c6e9b5ab4ea98584158d
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889087"
---
# <a name="maintenance-job-type-categories-and-maintenance-job-types-maintenance-job-type-variants-maintenance-job-trades-and-maintenance-checklists"></a>Bakım işi türü kategorileri ve bakım işi türleri, bakım işi türü çeşitlemeleri, bakım zanaatları ve bakım denetim listeleri

[!include [banner](../../includes/banner.md)]

 

Varlık türü her varlığa iliştirilir. Varlık türleri, varlıklarda gerçekleştirilen bakım işi türlerini (ve dolayısıyla bakım işlerini) tanımlar. İş emri oluşturduğunuzda bakım işi türü seçmeniz gerekir. Yalnızca varlık için kullanılan varlık türü kurulumu ile ilgili bakım işi türlerini seçebilirsiniz.

Varlıkların ve bakım işi türlerinin grafik özeti ve bunların iş emirleriyle bağlantısı için bkz. [İşlem yapılacak yerleşimler ve varlıklar](../overview/functional-locations-and-objects.md).

Bakım işi türü çeşitlemeleri, bakım işi türünde ayarlanabilir. Bakım işi türü çeşitlemeleri; boyutlar (küçük, orta veya büyük), dönemler (haftalık, iki haftada bir, bir ay veya üç ay) ve yapılandırmalar (düşük standart, esnek veya yüksek performans) gibi iş türü türevlerini tanımlar.

Bakım zanaatları; mekanik, elektrik ve hidrolik zanaatları gibi profesyonel zanaatlar hakkında bilgi sağlar. Uzmanlık gereksinimleri, bakım zanaatlarında ayarlanabilir. Tüm bakım zanaatları, tüm bakım işi türleriyle ilgili olarak kullanılabilir. İş emrinde bakım işi türü çeşitlemesi ve/veya bakım zanaatı seçimi isteğe bağlıdır.

Her bakım işi türü için bakım işi türü kurulumu çeşitlemeleri oluşturulabilir. Örneğin, **Servis** olarak adlandırılan bakım işi türünüz varsa bu bakım işi türü için şu çeşitlemeleri oluşturabilirsiniz: **Kamyonlar 30.000 km**, **Arabalar 30.000 km** ve **Kamyonetler 30.000 km**.

Bakım işi türü kategorileri, genel bakış amaçlarıyla bir grup bakım işi türü toplamak için kullanılır. Bakım işi türü kategorisi örnekleri arasında **Ayarlama**, **İnceleme**, **Onarma** ve **İzleme** olabilir.

Bakım denetim listesi şablonları ve bakım denetim listesi değişkenleri, bakım denetim listelerini ayarlamak için kullanılır. Bakım denetim listeleri, bakım işi türlerinde ayarlanır ve iş emirlerinde kullanılır.

İlk olarak gerekli bakım işi türü kategorilerini, bakım işi türü değişkenlerini ve bakım zanaatlarını ayarlarsınız. Ardından bakım işi türlerini oluşturursunuz. Son olarak, **Bakım işi türü varsayılanları** sayfasında ekipmanınız için gerekli olan tüm bakım işi türleri çeşitlemelerini oluşturursunuz. Bu sayfada ayrıca bakım işi türleri birleşimi için tahminler, bakım denetim listeleri ve araçlar ayarlayabilirsiniz.

> [!NOTE]
> Bir bakım işi türü yalnızca bir bakım işi türü kategorisiyle ilgili olabilir.

## <a name="create-a-maintenance-job-type-category"></a>Bakım işi türü kategorisi oluşturma

1. **Varlık yönetimi** \> **Kurulum** \> **İşler** \> **Bakım işi türü kategorileri**'ni seçin.
2. **Yeni**'yi seçin.
3. **Bakım işi türü kategorisi** alanına bakım işi türü kategorisi için bir kimlik girin.
4. **Ad** alanına, bir ad girin.

    Bakım işi türü kategorilerini bakım işi türleriyle ilişkilendirmenizin ardından **İş türleri** alanı bu bakım işi türü kategorisiyle ilgili bakım işi türü sayısını gösterir.

![Bakım işi türü kategorileri sayfası](media/01-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type-variant"></a>Bakım işi türü çeşidi oluşturma

1. **Varlık yönetimi** \> **Kurulum** \> **İşler** \> **Bakım işi türü çeşitleri**'ni seçin.
2. **Yeni**'yi seçin.
3. **Bakım işi türü çeşidi** alanına bakım işi türü çeşidi için bir kimlik girin.
4. **Açıklama** alanına bir açıklama girin.
5. **Bakım işi türleri** hızlı sekmesinde bakım işi türü eklemek için **Ekle**'yi seçin.
6. **Bakım işi türü** alanında bakım işi türünü seçin.
7. Bakım işi türü çeşidine daha fazla bakım işi türü eklemek için 5. ve 6. adımları tekrarlayın.

    **Ayrıntılar** hızlı sekmesinde **İş türleri** alanı bu bakım işi türü çeşidine eklenen bakım işi türlerinin sayısını gösterir.

![Bakım işi türü varyantları sayfası](media/02-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-trade"></a>Bakım zanaatı oluşturma

1. **Varlık yönetimi** \> **Kurulum** \> **İşler** \> **Bakım zanaatı**'nı seçin.
2. **Yeni**'yi seçin.
3. **Ticaret** alanına bakım zanaatı için bir kimlik girin.
4. **Açıklama** alanına bir açıklama girin.
5. **Yetenekler** hızlı sekmesinde, bakım zanaatıyla ilgili olması gereken yeni bir yetenek eklemek için **Ekle**'yi seçin.
6. **Yetenek** alanında yeteneği seçin.
7. **Düzey** alanında düzeyi seçin.
8. Bakım zanaatına daha fazla yetenek eklemek için 5. ile 7. adımlar arasını tekrarlayın.

    **Ayrıntılar** hızlı sekmesinde **Yetenekler** alanı bu bakım zanaatına eklenen yeteneklerin sayısını gösterir.

9. **Sertifikalar** hızlı sekmesinde bakım zanaatına sertifika eklemek için **Ekle**'yi seçin.
10. **Sertifika türü** alanında sertifikayı seçin.
11. Bakım zanaatına daha fazla sertifika eklemek için 9. ve 10. adımları tekrarlayın.

    **Ayrıntılar** hızlı sekmesinde **Sertifikalar** alanı bu bakım zanaatına eklenen sertifikaların sayısını gösterir.

![Bakım işi zanaat sayfası](media/03-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-variable"></a>Bakım denetim listesi değişkeni oluşturma

Bakım işi türü varsayılanında bakım denetim listesi satırları oluşturduğunuzda bir bakım denetim listesi türü seçmeniz gerekir. **Değişken** bir bakım denetim listesi türüdür. İş emri satırıyla ilgili bakım denetim listesi satırında bir aralıkta olası bir sonucu tanımlamak için kullanılır. Değişken, tam bir ölçüm yapmak zorunda kalmadan önceden tanımlanmış sonuç kümesi oluşturmanıza olanak sağlar.

**1. Örnek:** Yağ düzeyini üç değer tanımlayarak ölçebilirsiniz: **Düzey çok yüksek**, **Düzey çok düşük** ve **Düzey aralık içinde**. Her değer için değer sonucunun **Başarılı**, **Başarısız** veya **Hiçbiri** olduğunu tanımlarsınız.

**2. Örnek:** Aşınmayı değerlendirmek için ekipman parçasının görsel incelemesini yaparsınız.

1. **Varlık yönetimi** \> **Kurulum** \> **Bakım denetim listeleri** \> **Bakım denetim listesi değişkenleri**'ni seçin.
2. **Yeni**'yi seçin.
3. **Değişken** alanına bakım denetim listesi değişkeni için bir kimlik girin.
4. **Ad** alanına, bir ad girin.
5. **Genel** hızlı sekmesinde bir değişkene satır eklemek için **Ekle**'yi seçin.

    Sıralı satır numarası **Satır numarası** alanına otomatik olarak girilir. Satırları eklemenizin ardından gerektiğinde satır numaralarını değiştirebilirsiniz. Satırı seçip **Aşağı ok** tuşuna bastığınızda sıradaki sonraki numara, sonraki satıra otomatik olarak girilir.

6. **Değer** alanına bir değer açıklaması girin.
7. **Sonuç** alanında satır için bir sonuç seçin.

![Bakım denetim listesi değişkenleri sayfası](media/04-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-template"></a>Bakım denetim listesi şablonu oluşturma

Bakım denetim listesi şablonları bir çalışanın iş emrini doğru şekilde tamamlamak için gerçekleştirmesi gereken ortak görev kümesi olarak kullanılabilir. Şablonlara, bakım işi türü varsayılanındaki bakım denetim listesi satırlarından başvurulur. Şablonlara birden çok bakım işi türü varsayılan satırı boyunca başvurulabilir. Bu nedenle bir ortak bakım denetim listesi görev kümesini kolayca yeniden kullanabilirsiniz. Bakım denetim listesi şablon örneklerine genel güvenlik yönergeleri ve özel bir pompada veya konveyör kayışının benzer modellerinde denetlenmesi gereken madde ve koşulların listesi dahildir.

1. **Varlık yönetimi** \> **Kurulum** \> **Bakım denetim listeleri** \> **Bakım denetim listesi şablonları**'nı seçin.
2. **Yeni**'yi seçin.

    Şablon kimliği, **Bakım denetim listesi şablonu** alanına otomatik olarak girilir.

3. **Ad** alanına bakım denetim listesi şablonu için bir ad girin.
4. **Bakım denetim listesi satırları** hızlı sekmesinde şablon satırı eklemek için **Ekle**'yi seçin.

    Sıralı satır numarası **Satır numarası** alanına otomatik olarak girilir. Satırları eklemenizin ardından gerektiğinde satır numaralarını değiştirebilirsiniz. Satırı seçip **Aşağı ok** tuşuna bastığınızda sıradaki sonraki numara, sonraki satıra otomatik olarak girilir.

5. **Tür** alanında bakım denetim listesi satırı için bir tür seçin. Her bakım denetim listesi türü için **Satır ayrıntıları** hızlı sekmesi, ilgili alanları gösterir. Aşağıdaki değerler kullanılabilir:

    - **Metin**: Satır, ne yapılacağını açıklayan metne sahiptir. Bir çalışanın bir şeyleri denetlemesini veya incelemesini istiyor ancak belirli (ölçülebilir) bir sonuç beklemiyorsanız bu bakım denetim listesi türünü kullanın. Bu türü seçmenizin ardından **Ad** alanına bir ad veya başlık girin. **Yönergeler** alanına nelerin yapılması gerektiğine dair bir açıklama girin. Adım bakım denetim listesi için zorunluysa **Zorunlu** seçeneğini **Evet** olarak ayarlayın.
    - **Başlık**: Satır, altında görüntülenen bakım denetim listesi satırlarını gruplamak için başlık olarak kullanılır. Bu tür, belirli alanlara bölünebilen birkaç bakım denetim listesi satırı varsa yararlıdır. Başlıklar, birçok bakım denetim listesi satırı bulunan bir bakım denetim listesini tamamlayacak çalışan için genel bakış sağlar. Bu türü seçmenizin ardından **Ad** alanına açıklayıcı bir ad girin.
    - **Şablon**: Satır, var olan bir şablona referans oluşturmak için kullanılır. Bu türü seçmenizin ardından **Ad** alanına şablon için bir ad girin. **Şablon** alanında şablonu seçin.
    - **Değişken**: Satır, bir aralıkta olası bir sonucu tanımlamak için kullanılır. Bakım denetim listesi değişkenleri ayarlama hakkında bilgi için [Bakım denetim listesi değişkeni oluşturma](#create-a-maintenance-checklist-variable) bölümüne bakın. Bu türü seçmenizin ardından **Ad** alanına değişken için açıklayıcı bir ad girin. **Değişken** alanında değişkeni seçin. **Yönergeler** alanına nelerin yapılması gerektiğine dair bir açıklama girin. Adım bakım denetim listesi için zorunluysa **Zorunlu** seçeneğini **Evet** olarak ayarlayın.
    - **Ölçüm**: Satır, belirli bir ölçümü kaydetmek için kullanılır. Önceden tanımlanmış bir sayaçla ilgili olması gereken ölçümü ayarlayabilirsiniz. Bu türü seçmenizin ardından **Ad** alanına şablon için bir ad girin. Bu adım bakım denetim listesi için zorunluysa **Zorunlu** seçeneğini **Evet** olarak ayarlayın. Ölçüm satırını sayaç kaydı olarak kullanmak isterseniz **Sayaç** alanında sayacı seçin. İlgili **Birim** alanı daha sonra otomatik olarak güncelleştirilir. Sayaç seçtiyseniz **Değer** alanında güncelleştirme yöntemini seçin. **Minimum değer** ve **Maksimum değer** alanlarına izin verilen değer aralığını girin. **Yönergeler** alanına nelerin yapılması gerektiğine dair bir açıklama girin.

        > [!NOTE]
        > Sayaç kurulumu bulunmayan **Ölçüm** türünün satırları, Varlık Yönetimi'nde otomatik takip olmayan bağımsız ölçüm kaydı olarak kabul edilir. Benzer şekilde, iş emriyle ilgili varlıkta seçili sayaç türü yoksa bakım denetim listesi görevi bağımsız ölçüm olarak kabul edilir. Sayaç değeri birçok kez değiştirilebilir. Bu, [iş emri yaşam döngüsü durumu](work-order-lifecycle-states.md) **Bakım denetim listesini işle** seçeneğinin **Evet** olarak ayarlandığı durum için değiştirilene kadar yayımlanmaz.

    **Ayrıntılar** hızlı sekmesinde **Denetimler** alanı, şablonunuzdaki denetim listesi satırlarının toplam sayısını gösterir. Bu sayı, şablonunuzda başvurduğunuz var olan şablondaki iç içe satırları içerir.

![Bakım denetim listesi şablonları sayfası](media/05-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type"></a>Bakım işi türü oluşturma

1. **Varlık yönetimi** \> **Kurulum** \> **İşler** \> **Bakım işi türleri**'ni seçin.
2. **Yeni**'yi seçin.
3. **Bakım işi türü** alanına bakım işi türü için bir kimlik girin.
4. **Ad** alanına, bir ad girin.

    **Ayrıntılar** hızlı sekmesi, bu bakım işi türünde oluşturulan iş türü çeşitleri, yetenekler, sertifikalar, izleyen işler ve varlık türlerinin sayısının özetini gösterir. **Kurulum satırları** alanı, bu bakım işi türünde ayarlanan bakım işi türü varsayılan satırı sayısını gösterir. **Varlıklar** alanı, şu anda bu bakım işi türünü kullanan etkin varlıkların sayısını gösterir.

5. **Genel** hızlı sekmesinde **Bakım işi türü kategorisi** alanında bakım işi türü kategorisi seçin.
6. İş gerçekleştirilmeden önce bakım işi türü için ekipman bakım molası gerekirse **Bakım kesinti süresi faaliyetleri** seçeneğini **Evet** olarak ayarlayın.
7. **Açıklama** hızlı sekmesinde bakım işi türünün açıklamasını girin.
8. **Bakım işi türü çeşitleri** hızlı sekmesinde bakım işi türüne çeşitler ekleyebilirsiniz.
9. **Gerekli yetenekler** ve **Gerekli sertifikalar** hızlı sekmelerinde bakım işi türüne yetenek ve sertifika gereksinimleri ekleyebilirsiniz.
10. Sonraki adımda belirli bakım işi türünün gerçekleştirilmesi gerekiyorsa bunu **İlerleyen işler** hızlı sekmesine ekleyin. Ayrıca bakım işi türüyle ilgili bakım işi türü çeşidini ve ticareti de ayarlayabilirsiniz. İlerleyen işin bu bakım işi türünü kullanan işin başlamasından belirli bir gün sayısından önce veya sonra başlaması gerekirse **Gün sayısı kadar geciktir** alanına gün sayısını girin. Pozitif sayılar ilgili işin başlangıcından sonraki günleri ve negatif sayılar ilgili işin planlı başlangıcından önceki günleri temsil eder. Örneğin, **5** girerseniz ilerleyen iş bakım işi türüyle ilgili işin başlangıcından beş gün sonra başlar. **-3** girerseniz ilerleyen iş bakım işi türüyle ilgili işin planlı başlangıcından üç gün önce başlar.

    > [!NOTE]
    > Bir bakım işi türü satırından fazla eklerseniz satır sırası, gerçekleştirilmesi gereken düzeni gösterir. Sıra, listenin en üstünden başlar.

11. **Varlık türleri** hızlı sekmesinde bakım işi türüne varlık türleri ekleyebilirsiniz.

![Bakım işi türleri sayfası](media/06-setup-for-work-orders.png)

## <a name="create-maintenance-job-type-default-lines-and-related-forecasts-maintenance-checklists-tools-description-and-attachments"></a>Bakım işi türü varsayılan sıraları ve ilgili tahminler, bakım denetim listeleri, araçlar, açıklama ve ekler oluşturma

1. **Varlık yönetimi** \> **Kurulum** \> **İşler** \> **Bakım işi türü varsayılanları**'nı seçin.

    veya

    **Varlık yönetimi** \> **Kurulum** \> **İşler** \> **Bakım işi türleri**'ni, bakım işi türünü ve ardından **Bakım işi türü varsayılanları**'nı seçin.

2. **Yeni**'yi seçin.
3. **İşlem yapılacak yerleşim**, **Varlık türü**, **Üretici**, **Model** ve **Varlık** alanlarında bakım işi türü varsayılanının nasıl özel olması gerektiğine bağlı olarak uygun değerleri seçin.
4. **Bakım işi türü** alanında otomatik olarak seçilmediyse bir bakım işi türü seçin.
5. **Bakım işi türü çeşidi** ve **Ticaret** alanlarında gerektiğinde bakım işi türü çeşidi ve bakım zanaatı seçin.
6. **Tahmin**'i seçin.
7. **Bakım işi türü varsayılan tahmini** sayfasında saatlere, maddelere ve giderlere dair tahminler yapabilirsiniz. İlgili sekmelerde **Ekle**'yi seçin ve bakım işi türü için gerekli tahminleri oluşturmak üzere seçimler yapın.
8. **Madde tahmini** sekmesinde madde satırında gösterilmesi gereken stok boyutlarını seçebilirsiniz. **Stok** \> **Boyutlar**'ı ve gösterilecek boyutları seçin, **Kurulumu kaydet** seçeneğini **Evet** olarak ayarlayın ve ardından **Tamam**'ı seçin.
9. **Madde tahmini** sekmesinde varlıklar, bakım işi türü varsayılanı, yedek parçalar ve iş emirleriyle ilgili olarak Varlık Yönetimi'nde seçilen satırdaki maddenin nerede kullanıldığına dair genel bakış edinmek için **Maddenin kullanıldığı yer**'i seçin. 

    **Bakım tahmini toplamları** hızlı sekmesi, tahmin toplamlarının özetini gösterir. Bu özet, toplam saat sayısını ve oluşturulan tahmin satırlarını içerir.

    > [!NOTE]
    > Tahmin kurulumunu başka bakım işi türünden kopyalamak için **Tahmin kopyala**'yı ve ardından kurulumun kopyalanacağı bakım işi türünü seçin.

11. Değişikliklerinizi kaydetmek için **Kaydet**'i seçin.
12. **Bakım işi türü varsayılanları** sayfasına dönmek için **Bakım işi türü varsayılan tahmini** sayfasını kapatın.
13. **Bakım denetim listesi**'ni seçin.
14. **Bakım işi türü varsayılanları denetim listesi** sayfasında seçilen bakım işi türü varsayılanına bakım denetim listesi satırları ekleyebilirsiniz. **Bakım denetimi satırları** hızlı sekmesinde bakım denetim listesi satırı eklemek için **Yeni**'yi seçin.

    Satır numaraları, bakım denetim listesi satırlarının sırasını belirtecek şekilde **Satır numarası** alanına otomatik olarak girilir. Gerektiğinde satır numaralarını düzenleyebilirsiniz. İlk bakım denetim listesi satırını oluşturmanızın ardından satırı seçin ve ardından bunun altına bir satır eklemek için **Aşağı ok** tuşuna basın. Alternatif olarak, bir bakım denetim listesi satırı ve ardından **Yeni**'yi seçebilirsiniz. Bu durumda, seçilen bakım denetim listesi satırının üstüne yeni bir satır eklenir.

15. **Tür** alanında satır türünü seçin ve ardından bakım denetim listesi türüyle ilgili bilgileri ekleyin. Kullanılabilir türlere ve ilgili alanlara dair açıklama için [Bakım denetim listesi şablonu oluşturma](#create-a-maintenance-checklist-template) bölümüne bakın.

    > [!NOTE]
    > Bakım denetim listesi kurulumunu başka bakım işi türünden kopyalamak için **Bakım denetim listesi kopyala**'yı ve ardından kurulumun kopyalanacağı bakım işi türünü seçin.
    >
    > Var olan bakım denetim listesinden kolayca şablon oluşturabilirsiniz. Ardından şablonu birden çok bakım denetim listesi boyunca yeniden kullanabilirsiniz. Yeni şablon, etkin bakım denetim listesinin tam bir kopyası olur. **Şablon oluştur**'u seçin ve ardından şablon için bir ad girin. Var olan bakım denetim listesini yeni şablona başvuran tek bir satırla değiştirmek için **Değiştir** seçeneğini **Evet** olarak ayarlayın. **Bakım denetim listesi şablonları** ayrıntıları sayfasında şablonun içeriğini görüntüleyebilirsiniz.

16. Değişikliklerinizi kaydetmek için **Kaydet**'i seçin.
17. **Bakım işi türü varsayılanları** sayfasına dönün.
18. **Araçlar**'ı seçin.
19. **Bakım işi türü varsayılan araçları** sayfasında bakım işi türü için kullanılması gereken araçları (kaynaklar) ekleyebilirsiniz. **Yeni**'yi ve ardından **Kaynak** alanında aracı seçin.

    > [!NOTE]
    > Araç kurulumunu başka bakım işi türünden kopyalamak için **Araçları kopyala**'yı ve ardından kurulumun kopyalanacağı bakım işi türünü seçin.

20. Değişikliklerinizi kaydetmek için **Kaydet**'i seçin.
21. **Bakım işi türü varsayılanları** sayfasına dönün.
22. **İş açıklaması**'nı seçin.
23. **İş açıklaması** sayfasında **Düzenle**'yi seçin ve ardından gerektiğinde, seçilen bakım işi türü varsayılanıyla ilgili bir açıklama ekleyin.
24. Açıklamayı kaydetmek için **Kaydet**'i seçin.

    Buraya iş açıklaması eklerseniz bu, **Bakım işi türleri** sayfasında bakım işi türü için ayarlanan açıklamayı geçersiz kılar. Buraya bir iş açıklaması eklemezseniz bakım işi türü için ayarlanan bir açıklama kullanılır. Açıklamalar, bakım işi türü veya bakım işi türü varsayılanı kullanan iş emirlerine otomatik olarak aktarılır.

25. **Bakım işi türü varsayılanları** sayfasına dönün.
26. Seçilen bakım işi türü varsayılan satırında ekleri ayarlamak için **Belge ekle**'yi seçin. Bakım işi türü varsayılan satırında ayarlanan ekler, bu bakım işi türü varsayılan satırını kullanan iş emri satırlarına otomatik olarak eklenir.
27. **Yeni**'yi ve ardından belge türünü seçin.
28. Belgeyi veya dosyayı karşıya yükleyin.
29. **Ekler** sayfasında alanları ayarlayın. Ek kurulumunda standart belge kurulumu işlevi kullanılır.
30. Eki kaydetmek için **Kaydet**'i seçin.

    > [!NOTE]
    > Bakım işi türü varsayılan satırındaki ekler yalnızca eklerin belge türleri **Varlık yönetimi parametreleri** sayfasının (**Varlık yönetimi** \> **Kurulum** \> **Varlık yönetimi parametreleri**) **Belge türleri** sekmesinde seçilirse iş emri raporuyla birlikte yazdırılır. Ek örnekleri arasında belirli bir işin nasıl tamamlanacağını açıklayan kılavuzlar veya (bakım işi türü varsayılan satırları için bakım denetim listesi işlevini kullanmıyorsanız) önceden tanımlanan bakım denetim listesi vardır.

    **Bakım işi türü varsayılanları** sayfasında her satır, tahmin edilen saat sayısını ve ayrıca maddeler, giderler, bakım denetim listeleri ve araçlar için oluşturulan satırların sayısını gösterir. **Varlıklar** alanı, bakım işi türü varsayılan satırıyla ilgili etkin varlıkların sayısını gösterir.

31. Bakım işi türü varsayılanını başka bakım işi türü varsayılanına kopyalamak için başka kuruluma kopyalamak üzere bakım işi türü varsayılanını, **Kurulumu kopyala**'yı ve ardından kopyalanacak bakım işi türü varsayılanını seçin.
32. Şu anda bakım işi türü varsayılan satırını kullanan varlıkların, bakım planlarının veya bakım sıralarının listesini görüntülemek için satırı ve ardından **Kullanan**'ı seçin.

![Bakım işi türü varsayılanları sayfası](media/07-setup-for-work-orders.png)

Sistem, iş emri satırında kullanılması gereken kullanılabilir bakım işi türü varsayılanını seçtiğinde seçim varlığa ve ilgili varlık türü kurulumuna bağlıdır. Varlık Yönetimi, olası eşleşmeyi denetlemek için varlık türüyle ilgili bakım işi türüyle ilgili tüm bakım işi türü varsayılan kayıtlarını tarar. Her zaman ilk önce en belirgin birleşimi denetler. Diğer bir deyişle, Varlık Yönetimi en belirgin birleşimi bulmak için önce **Ticaret** alanı için olası eşleşmeyi denetler. Eşleşme bulamazsa **Bakım işi** alanı için eşleşmeleri denetler. Eşleşme bulunmazsa eşleşme için **Bakım işi türü** alanını ve devamını denetler (**Ticaret**, ardından **Bakım işi türü çeşidi**, ardından **Bakım işi türü**, ardından **Varlık**, ardından **Model**, ardından **Üretici** ve ardından **Varlık türü**). Eşleşme bulunmazsa yalnızca bakım işi türünün seçildiği varsayılan kaydı kullanılır.

Proje faaliyeti kimliği, oluşturduğunuz her bakım işi türü varsayılan satırıyla otomatik olarak ilgilidir. Proje faaliyeti, **Varlık yönetimi parametreleri** sayfasının **Varlıklar** sekmesindeki **Bakım tahmini projesi** alanında seçilen tahmin projesinde oluşturulur. Proje faaliyetinin amacı, iş emirleriyle ilgili olarak saatler, maddeler ve giderlere dair tahminleri yönetmektir. Bakım işi türü tahminleri iş emri satırına otomatik olarak transfer edilir ve tahmin projesinden iş emri satırı için oluşturulan iş emri projesine kopyalanırlar. Proje faaliyetinin amacı, iş emirleriyle ilgili olarak tahminleri yönetmektir.

Düzenli aralıklarla bakım işi türü varsayılan referanslarını güncelleştirmek için toplu iş ayarlayabilir veya işi el ile çalıştırabilirsiniz. Toplu iş oluşturmak veya el ile güncelleştirme çalıştırmak için **Varlık yönetimi** \> **Periyodik** \> **Önleyici bakım** \> **Bakım işi türü varsayılan referanslarını güncelleştir**'i seçin.

## <a name="overview-of-maintenance-job-types-that-are-related-to-assets"></a>Varlıklarla ilgili bakım işi türlerine genel bakış

Gerekli bakım işi türü varsayılan birleşimlerini oluşturmanızın ardından belirli bir varlıkla ilgili geçerli bakım işi türü varsayılanına genel bakış edinmek için **Tüm varlıklar** sayfasını kullanabilirsiniz. Genel bakış, varlık için seçilen varlık türünde kullanılabilen tüm bakım işi türü varsayılan birleşimlerini gösterir. Bu birleşimler, bakım işi türü çeşitlerinin ve bakım zanaatlarının çeşitlemelerine sahip birleşimleri içerir.

1. **Varlık yönetimi** \> **Genel** \> **Varlıklar** \> **Tüm varlıklar** veya **Etkin varlıklar**'ı seçin.
2. Listede bakım işi türü birleşimlerinin özetini görmek için varlığı seçin.
3. Eylem Bölmesinde **Genel** sekmesindeki **İlgili bilgiler** grubunda **Bakım işi türleri**'ni seçin.

    **Varlık bakım işi türleri** sayfasının sol bölmesi, seçilen varlıkla ilgili tüm bakım işi türü birleşimlerinin listesini gösterir.

4. Bakım denetim listeleri, tahminler ve araçlar için ilgili kurulumu görmek üzere bir bakım işi türü birleşimi seçin. **Bakım işi türü varsayılanları** hızlı sekmesindeki **Ayrıntılar** bölümü, seçilen bakım işi türü birleşimiyle ilgili bakım denetim listeleri, tahmin edilen saatler, maddeler ve daha fazlasının sayısını gösterir.
5. Seçilen bakım işi türünün ayrıntılarını görüntülemek için **Bakım işi türleri**'ni seçin.

![Varlık bakım işi türleri sayfası](media/08-setup-for-work-orders.png)

## <a name="automatic-update-of-maintenance-job-type-forecasts"></a>Bakım işi türü tahminlerinin otomatik güncelleştirmesi

Varlık Yönetimi'nde, diğer modüllerde güncelleştirilen saat maliyetleri, madde maliyetleri ve giderler için bakım işi türü tahminlerindeki değişiklikleri otomatik olarak güncelleştirebilirsiniz. Bu şekilde, bakım işi türü tahminlerinizin her zaman en son maliyet fiyatlarını kullanmasını sağlamaya yardımcı olursunuz.

1. **Varlık yönetimi** \> **Periyodik** \> **Tahmin** \> **Bakım işi türü tahminini güncelleştir**'i seçin.
2. **Bakım işi türü tahminini güncelleştir** iletişim kutusunda **Eklenecek kayıtlar** hızlı sekmesinde gerektiğinde belirli bakım işi türleri için seçimler ekleyebilirsiniz. **Filtre**'yi seçin ve ardından seçim yapmak için **Seç**'i belirleyin.
3. **Arka planda çalıştır** hızlı sekmesinde gerektiğinde otomatik güncelleştirmeyi toplu iş olarak ayarlayabilirsiniz.
4. Tahmin güncelleştirmesini başlatmak için **Tamam**'ı seçin.
