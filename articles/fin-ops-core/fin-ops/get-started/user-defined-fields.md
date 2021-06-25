---
title: Özel alanlar oluşturma ve bunlarla çalışma
description: Bu konu uygulamayı işletmenize uygun hale getirmek için kullanıcı arabiriminden nasıl özel alanlar oluşturabileceğinizi açıklar.
author: jasongre
ms.date: 05/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: b15b25ac172e8ab942e950c9e8c4aff1e26c9291
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193867"
---
# <a name="create-and-work-with-custom-fields"></a>Özel alanlar oluşturma ve bunlarla çalışma

[!include [banner](../includes/banner.md)]

Çok sayıda iş sürecini yönetmek için kullanıma hazır kapsamlı bir alan kümesi olmasına karşın bazen bir şirketin sistemde ek bilgileri izlemesi gerekebilir. Bu alanları geliştirici araçlarında uzantı olarak eklemek için programlayıcılar kullanılabilir, özel alanlar özelliği alanların doğrudan kullanıcı arabiriminden eklenmesine olanak tanır ve web tarayıcınızı kullanarak uygulamanızı işletmenize uygun hale getirmenize olanak tanır.

*Yalnızca özel izinlere sahip kullanıcıların bu özelliğe erişimi vardır.*

Bu videoda bir sayfaya özel alan eklemenin ne kadar kolay olduğu gösterilmektedir: [Özel alanlar ekleme](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Özel alanlar oluşturma

Uygulamada izlemek istediğiniz ek bilgileri tanımladıktan sonra ilgili tabloda özel alan oluşturabilir ve bu yeni alanı sayfa üzerinde gösterebilirsiniz.

Aşağıdaki adımlar özel alan oluşturma ve bu alanı forma yerleştirme sürecini açıklar.

1. Yeni alanın gerekli olduğu forma gidin.
2. Son hedef bir formda özel alanı görüntülemek olduğundan, özel alanları oluşturmaya giriş noktası kişiselleştirme deneyimi içinde bulunur. **Seçenekler**'i seçip kişiselleştirme araç çubuğunu açın ve daha sonra **Bu formu kişiselleştir**'i seçin.
3. **Ekle**'ye ve ardından **Alan**'a tıklayın.
4. Yeni alanı görüntülemek istediğiniz form bölgesini seçin. Seçim yaptıktan sonra **Alan ekle** iletişim kutusunda formun seçilen bölgesine eklenebilecek mevcut alanların listesi gösterilir.
5. İlgilendiğiniz alanın zaten listede bulunmadığından emin olun. Varsa, listeden alanı seçip **Ekle**'ye tıklayabilirsiniz.
6. Özel alan oluşturma işlemini başlatmak için listenin üstündeki **Yeni alan oluştur** düğmesine tıklayın. **Yeni alan oluştur** iletişim kutusu açılır.

    **Yeni alan oluştur** düğmesini görmüyorsanız, bu özelliği kullanmak için gerekli izinlere sahip değilsinizdir.

7. **Yeni alan oluştur** iletişim kutusuna, aşağıdaki bilgileri girin.
   
    1. Bu alanın eklenmesi gereken veritabanı tablosunu seçin. Açılır listede yalnızca özel alanları destekleyen tabloların görüntülendiğini unutmayın. Desteklenen tablolardaki teknik ayrıntılar için aşağıdaki bölüme bakın.

    2. Yeni alanın veri türünü seçin. Kullanılabilir veri türleri şunlardır: onay kutusu, tarih, tarih saat, ondalık, numara, seçim listesi ve metin.

        - Metin veri türünü seçerseniz, bu alana girilebilecek maksimum metnin uzunluğunu da belirtebilirsiniz.
        - Seçim listesi türünü seçerseniz, alan için geçerli değerler kümesini de seçebilirsiniz.

    3. Alan için bir ad, etiket ve yardım metni girin. Ad veritabanındaki fiziksel alan adına karşılık gelirken etiket ve yardım metni bu alanı kullanıcı arabiriminde temsil etmek üzere kullanılan metindir.

8. Bu alan bu form için oluşturmanız gereken tek alanda **Kaydet**'e tıklayın. Ek alanlar oluşturmanız gerekiyorsa **Kaydet ve yeni**'ye tıklayın ve adım 7'ye dönün. Şu anda **Tablo başına 20 özel alan** sınırı bulunduğunu unutmayın.
9. **Yeni alan oluştur** iletişim kutusundan çıktığınızda **Alan ekle** iletişim kutusuna geri dönersiniz. Yeni eklenen özel alanlar forma eklenecek alan listesinde otomatik olarak işaretlenir.
10. İşaretlenen alanları formun seçilen bölgesine eklemek için **Ekle**'ye tıklayın.
11. **İsteğe bağlı:** Yeni alanları seçilen bölümde istenen konuma taşımak için kişiselleştirme araç çubuğundaki **Taşı** modunu etkinleştirin. Kişisel kullanım için bir formu en iyi duruma getirmek amacıyla çeşitli kişiselleştirme özelliklerinin kullanılmasıyla ilgili daha fazla bilgi edinmek için [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md) bölümüne bakın.

> [!WARNING]
> Sayfaya eklenen özel bir alana değer girme yeteneği, özel alanla ilişkili tablonun düzenlenebilir veya salt okunur olmasına bağlıdır. Yalnızca ilişkili tablosu okunduğunda, herhangi bir özel alan da dahil olmak üzere bu tabloya bağlı tüm alanlar da salt okunur olacaktır.


## <a name="sharing-custom-fields-with-other-users"></a>Özel alanları diğer kullanıcılarla paylaşma

Özel alan oluşturup sayfada görüntülenmesini sağladıktan sonra, güncelleştirilen ve yeni alanı içeren bu sayfa görünümünü sistemdeki diğer kullanıcılara sunmak isteyebilirsiniz. Bunu üründeki kişiselleştirme özelliklerini kullanarak iki farklı yoldan yapabilirsiniz:

- Önerilen yol, sayfaya eklenen özel alanla birlikte uygun kullanıcı kümesine **[kaydedilmiş bir görünümü](saved-views.md) yayımlamaktır**. Kaydedilen görünümler özelliği etkinleştirilmemişse, sistem yöneticisi kişiselleştirme formundan istediğiniz kullanıcılara kişiselleştirmeyi uygulayabilir. Daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).
- Alternatif olarak, değişikliklerinizi (*kişiselleştirmeler* denir) dışa aktarabilir, bir veya daha fazla kullanıcıya gönderebilir ve bu kullanıcıların değişikliklerini içe aktarmalarını isteyebilirsiniz. Kişiselleştirme araç çubuğundaki **Yönet** seçeneği kişiselleştirmeleri dışa ve içe aktarmanıza olanak tanır.

## <a name="managing-custom-fields"></a>Özel alanları yönetme

Sistemdeki tüm özel alanların yönetimi Sistem yönetimi modülündeki **Özel alanlar** sayfası aracılığıyla gerçekleştirilebilir. Bu sayfa kullanıcılara aşağıdakiler dahil birçok özelliğe erişime olanağı tanır:

- Sistemdeki tüm özel alanların listesini görüntüleme.
- Var olan özel alanlarını sınırlı düzenleme.
- Özel alanları silme.
- Özel alanları veri varlıklarında görüntüleme.
- Özel alanların etiketleri ve yardım metninin çevirisini sağlama.

### <a name="viewing-all-custom-fields"></a>Tüm özel alanları görüntüleme

**Özel alanlar** sayfası sistemde tanımlanan tüm özel alanların görülmesini sağlar. İlgilendiğiniz tabloyu seçmeniz yeterlidir; sayfa bu tabloyla ilişkili özel alanların listesini gösterecek şekilde güncelleştirilir. Listeden bir özal alan seçmek bu alanla ilgili tüm ayrıntıları görmenize olanak tanır.

### <a name="editing-custom-fields"></a>Özel alanları düzenleme

Özel alan oluşturulduktan sonra, **Özel alanlar** sayfasında özel alanla ilgili yalnızca bazı bilgi parçaları değiştirilebilir.

Şu öznitelikleri *değiştirebilirsiniz*:

- Etiket
- Yardım metni
- Uzunluk, Metin alanları için

Şu öznitelikleri *düzenleyemezsiniz*:

- Alan adı
- Veri tipi

Ek olarak, özel alanlar için geçerli değerler kümesi olan seçim listesi alanları yeniden sıralanabilir ve yeni değerler eklenebilir; ancak seçim listesi alanındaki mevcut değerler kaldırılamaz. Değişikliklerin kaydedilebilmesi için belirli bir tabloya ilişkin alanları düzenlemeyi tamamladıktan sonra **Değişiklikleri uygula**'ya tıklamayı unutmayın.

### <a name="exposing-custom-fields-on-data-entities"></a>Özel alanları veri varlıklarında görüntüleme

Ayrıca özel alanların veri varlıklarında görünür olmasını sağlamak önemli olabilir. Veri varlıkları [Office tümleştirmesine genel bakış](../../dev-itpro/office-integration/office-integration.md) özelliğinde ve veri içe aktarma/dışa aktarma senaryolarında kullanılır.

Bir veri varlığında özel alanın görünür olmasını sağlamak için aşağıdaki adımları izleyin:

1. **Özel alanlar** formunda özel alanı seçin.
2. İlgili varlıklar kümesini görmek için **Varlıklar** bölümünü genişletin.
3. **Düzenle** düğmesine basın.
4. Bu alanda görünmesi gereken her varlık için seçilecek **Etkin** alanını değiştirin.
5. Seçimlerini kaydetmek için **Değişiklikleri uygula**'ya tıklayın.

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Diğer dillerde görüntülenecek özel alanlara izin verme

Özel alanlara farklı dilleri kullanan kullanıcılar tarafından erişilmesi gerekebileceğinden, **Özel alanlar** sayfası bir özel alanın etiketinin ve yardım metninin diğer dillere çevrilmesine olanak tanıyan bir mekanizma sunar.

Aşağıdaki adımlar özel alanlaron diğer dillere çevrilmesi işlemini açıklar:

1. **Özel alanlar** sayfasında özel alanı seçin.
2. Eylem Bölmesinde **Çeviriler** düğmesini seçin. Bu alan için mevcut çevirileri içeren bir açılır menü açılır.
3. **Dil** açılır menüsü çevirisi zaten sağlanmış olan dilleri gösterir.

    Mevcut bir çeviriyi düzenlemek isterseniz, menüden istediğiniz dili seçip etiket ve yardım metni değerlerini değiştirin.

    Aksi halde, **Dil ekle** düğmesine tıklayın, menüden istediğiniz dili seçin ve etiket ve yardım metni için çevrilmiş değerleri sağlayın.

4. İşlemi tamamladığınızda **Tamam** düğmesini tıklayın.

### <a name="deleting-custom-fields"></a>Özel alanları silme

Bazı ender durumlarda, bir özel alanın artık gerekli olmadığına karar verebilirsiniz. Bu durumda, sistem yöneticisi bu alanı **Özel alanlar** sayfasından silmeyi seçebilir. Bunu yapmak için doğru alanın seçili olduğundan emin olun, **Sil**'e tıklayın, silme işlemini onaylamak için **Evet**'i seçin ve son olarak **Değişiklikleri uygula**'ya tıklayın.

> [!NOTE]
> Bu eylem geri alınamaz ve alanla ilişkili verilerin veritabanından tamamen silinmesine neden olur.

## <a name="appendix"></a>Ek

### <a name="why-cant-i-enter-a-value-in-my-custom-field"></a>Özel alanıma neden bir değer giremiyorum? 

Sayfa Düzenleme modundayken özel alana bir değer yazamıyorsanız, bunun nedeni alanın eklendiği tablonun şu anda salt okunur olması olabilir. Tablodaki tüm alanlar yalnızca yedekleme tablosu şu anda sayfada salt okunur olarak yapılandırılmışsa okunur hale gelir.   

### <a name="who-can-create-custom-fields"></a>Özel alanları kimler oluşturabilir?

Sistemi korumak amacıyla, varsayılan olarak yalnızca sistem yöneticileri özel alanlar oluşturabilir. Ancak, kuruluşun gerekli gördüğü kullanıcılara sistem yöneticisi tarafından **Çalışma zamanında özelleştirme yetkili kullanıcısı** güvenlik rolü kullanılarak özel alanlar oluşturma hakkı verilebilir. Bu güvenlik rolüne sahip olmayan kullanıcılar özel alanlar oluşturamaz ancak sistemdeki diğer kullanıcılar tarafından eklenen özel alanları görebilir ve bunlarla etkileşimde bulunabilir.

### <a name="what-tables-support-custom-fields"></a>Hangi tablolar özel alanları destekler?

Performans ve teknik nedenlerle, şu anda yalnızca aşağıdaki koşulları karşılayan tablolara özel alanlar eklenebilir.

- Tablo şu gruplardan biri olarak etiketlenmelidir:

    - Grup
    - WorksheetHeader
    - Ana
    - Çeşitli
    - Parametre
    - Referans
    - TransactionHeader

- Tablo başka bir tabloya genişletilemez.
- Tablo bir sistem tablosu olarak işaretlenemez.
- Tablo geçici bir tablo olamaz.

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a>Geliştirici araçlarındaki özel alanlara başvurabilir miyim?  

Özel alanlar yalnızca kullanıcı arabiriminden yönetilebilir ve kod tarafından başvurulamaz. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
