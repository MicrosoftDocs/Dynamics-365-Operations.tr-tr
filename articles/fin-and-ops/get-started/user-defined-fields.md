---
title: "Özel alanlar"
description: "Bu konu Microsoft Dynamics 365 for Finance and Operations'ın bazı kullanıcılara uygulamayı işletmelerine uygun hale getirmek üzere nasıl özel alanlar oluşturma olanağı tanıdığını açıklar."
author: jasongre
manager: AnnBe
ms.date: 04/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: 83648a93f367510d7b04bbd04a9f37689ecfaa59
ms.openlocfilehash: f2aa55ae4258f5ef81456b92278415297c194d66
ms.contentlocale: tr-tr
ms.lasthandoff: 05/23/2018

---

# <a name="custom-fields"></a>Özel alanlar

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/pre-release.md)]

Microsoft Dynamics 365 for Finance and Operations çok sayıda iş sürecini yönetmek için kullanıma hazır kapsamlı bir alan kümesi sunmasına karşın bazen bir şirketin sistemde ilave bilgileri izlemesi gerekebilir. Finance and Operations bu ihtiyacı karşılamak amacıyla, özellik için gerekli izinlere sahip olmanız durumunda, uygulamayı işletmenize uygun hale getirmek üzere özel alanlar oluşturmanıza olanak tanır. 

Özel alanlar ekleme yeteneği, platform güncelleştirmesi 13 ve sonraki sürümlerde kullanılabilir.

Bu video, sayfaya özel alan eklemenin ne kadar kolay olduğunu gösteriyor: [Dynamics 365 for Finance and Operations'ta özel alanlar ekleme](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Özel alanlar oluşturma
Uygulamada izlemek istediğiniz ek bilgileri tanımladıktan sonra ilgili tabloda özel alan oluşturabilir ve bu yeni alanı sayfa üzerinde gösterebilirsiniz.   

Aşağıdaki adımlar özel alan oluşturma ve bu alanı forma yerleştirme sürecini açıklar.  

1.   Yeni alanın gerekli olduğu forma gidin. 
2.   Son hedef bir formda özel alanı görüntülemek olduğundan, özel alanları oluşturmaya giriş noktası kişiselleştirme deneyimi içinde bulunur. **Seçenekler**'i seçip kişiselleştirme araç çubuğunu açın ve daha sonra **Bu formu kişiselleştir**'i seçin. 
3.   **Ekle**'ye ve ardından **Alan**'a tıklayın.  
4.   Yeni alanı görüntülemek istediğiniz form bölgesini seçin. Seçim yaptıktan sonra **Alan ekle** iletişim kutusunda formun seçilen bölgesine eklenebilecek mevcut alanların listesi gösterilir.  
5.   İlgilendiğiniz alanın zaten listede bulunmadığından emin olun. Varsa, listeden alanı seçip **Ekle**'ye tıklayabilirsiniz.   
6.   Özel alan oluşturma işlemini başlatmak için listenin üstündeki **Yeni alan oluştur** düğmesine tıklayın. **Yeni alan oluştur** iletişim kutusu açılır. 

     **Yeni alan oluştur** düğmesini görmüyorsanız, bu özelliği kullanmak için gerekli izinlere sahip değilsinizdir.  
     
7.   **Yeni alan oluştur** iletişim kutusuna, aşağıdaki bilgileri girin.
     1.   Bu alanın eklenmesi gereken veritabanı tablosunu seçin. Açılır listede yalnızca özel alanları destekleyen tabloların görüntülendiğini unutmayın. Desteklenen tablolardaki teknik ayrıntılar için aşağıdaki bölüme bakın.  
     2.   Yeni alanın veri türünü seçin. Kullanılabilir veri türleri şunlardır: onay kutusu, tarih, tarih saat, ondalık, numara, seçim listesi ve metin.   
          - Metin veri türünü seçerseniz, bu alana girilebilecek maksimum metnin uzunluğunu da belirtebilirsiniz. 
          - Seçim listesi türünü seçerseniz, alan için geçerli değerler kümesini de seçebilirsiniz.  
     3.   Alan için bir ad, etiket ve yardım metni girin. Ad veritabanındaki fiziksel alan adına karşılık gelirken etiket ve yardım metni bu alanı kullanıcı arabiriminde temsil etmek üzere kullanılan metindir.  
8.   Bu alan bu form için oluşturmanız gereken tek alanda **Kaydet**'e tıklayın. Ek alanlar oluşturmanız gerekiyorsa **Kaydet ve yeni**'ye tıklayın ve adım 7'ye dönün. Şu anda **Tablo başına 20 özel alan** sınırı bulunduğunu unutmayın.
9.   **Yeni alan oluştur** iletişim kutusundan çıktığınızda **Alan ekle** iletişim kutusuna geri dönersiniz. Yeni eklenen özel alanlar forma eklenecek alan listesinde otomatik olarak işaretlenir.  
10.   İşaretlenen alanları formun seçilen bölgesine eklemek için **Ekle**'ye tıklayın. 
11.   **İsteğe bağlı:** Yeni alanları seçilen bölümde istenen konuma taşımak için kişiselleştirme araç çubuğundaki **Taşı** modunu etkinleştirin. Kişisel kullanım için bir formu en iyi duruma getirmek amacıyla çeşitli kişiselleştirme özelliklerinin kullanılmasıyla ilgili daha fazla bilgi edinmek için [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md) bölümüne bakın.  

## <a name="sharing-custom-fields-with-other-users"></a>Özel alanları diğer kullanıcılarla paylaşma
Özel alan oluşturup formda görüntülenmesini sağladıktan sonra, güncelleştirilen ve yeni alanı içeren bu sayfa görünümünü sistemdeki diğer kullanıcılara sunmak isteyebilirsiniz. Bunu üründeki kişiselleştirme özelliklerini kullanarak iki farklı yoldan yapabilirsiniz:

-   Önerilen yol bu işlemi bir kişiselleştirmeyi tüm kullanıcılara veya bir kullanıcı alt kümesine sunabilecek olan sistem yöneticisi aracılığıyla gerçekleştirmektir. Daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md). 

-   Alternatif olarak, değişikliklerinizi (*kişiselleştirmeler* denir) dışa aktarabilir, bir veya daha fazla kullanıcıya gönderebilir ve bu kullanıcıların değişikliklerini içe aktarmalarını isteyebilirsiniz. Kişiselleştirme araç çubuğundaki **Yönet** seçeneği kişiselleştirmeleri dışa ve içe aktarmanıza olanak tanır.

## <a name="managing-custom-fields"></a>Özel alanları yönetme

Sistemdeki tüm özel alanların yönetimi Sistem yönetimi modülündeki **Özel alanlar** sayfası aracılığıyla gerçekleştirilebilir.  Bu sayfa kullanıcılara aşağıdakiler dahil birçok özelliğe erişime olanağı tanır: 
-   Sistemdeki tüm özel alanların listesini görüntüleme.
-   Varolan özel alanlarını sınırlı düzenleme.
-   Özel alanları silme.
-   Özel alanları veri varlıklarında görüntüleme.
-   Özel alanların etiketleri ve yardım metninin çevirisini sağlama.

### <a name="viewing-all-custom-fields"></a>Tüm özel alanları görüntüleme
**Özel alanlar** sayfası sistemde tanımlanan tüm özel alanların görülmesini sağlar. İlgilendiğiniz tabloyu seçmeniz yeterlidir; sayfa bu tabloyla ilişkili özel alanların listesini gösterecek şekilde güncelleştirilir. Listeden bir özal alan seçmek bu alanla ilgili tüm ayrıntıları görmenize olanak tanır.

### <a name="editing-custom-fields"></a>Özel alanları düzenleme
Özel alan oluşturulduktan sonra, **Özel alanlar** sayfasında özel alanla ilgili yalnızca bazı bilgi parçaları değiştirilebilir.   

Şu öznitelikleri *değiştirebilirsiniz*: 
-   Etiket 
-   Yardım metni
-   Uzunluk, Metin alanları için

Şu öznitelikleri *düzenleyemezsiniz*: 
-   Alan adı
-   Veri tipi

Ek olarak, özel alanlar için geçerli değerler kümesi olan seçim listesi alanları yeniden sıralanabilir ve yeni değerler eklenebilir; ancak seçim listesi alanındaki mevcut değerler kaldırılamaz. Değişikliklerin kaydedilebilmesi için belirli bir tabloya ilişkin alanları düzenlemeyi tamamladıktan sonra **Değişiklikleri uygula**'ya tıklamayı unutmayın. 

### <a name="exposing-custom-fields-on-data-entities"></a>Özel alanları veri varlıklarında görüntüleme
Ayrıca özel alanların veri varlıklarında görünür olmasını sağlamak önemli olabilir. Veri varlıkları [Office'te Aç](../../dev-itpro/office-integration/office-integration.md) özelliğinde ve veri içe aktarma/dışa aktarma senaryolarında kullanılır.  

Bir veri varlığında özel alanın görünür olmasını sağlamak için aşağıdaki adımları izleyin: 
1.   **Özel alanlar** formunda özel alanı seçin. 
2.   İlgili varlıklar kümesini görmek için **Varlıklar** bölümünü genişletin.  
3.   **Düzenle** düğmesine basın.
4.   Bu alanda görünmesi gereken her varlık için seçilecek **Etkin** alanını değiştirin.  
5.   Seçimlerini kaydetmek için **Değişiklikleri uygula**'ya tıklayın.  

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Diğer dillerde görüntülenecek özel alanlara izin verme
Özel alanlara farklı dilleri kullanan kullanıcılar tarafından erişilmesi gerekebileceğinden, **Özel alanlar** sayfası bir özel alanın etiketinin ve yardım metninin diğer dillere çevrilmesine olanak tanıyan bir mekanizma sunar.  

Aşağıdaki adımlar özel alanlaron diğer dillere çevrilmesi işlemini açıklar: 
1.   **Özel alanlar** sayfasında özel alanı seçin. 
2.   Eylem Bölmesinde **Çeviriler**düğmesini seçin. Bu alan için mevcut çevirileri içeren bir açılır menü açılır.
3.   **Dil** açılır menüsü çevirisi zaten sağlanmış olan dilleri gösterir. 
     1.   Mevcut bir çeviriyi düzenlemek isterseniz, menüden istediğiniz dili seçip etiket ve yardım metni değerlerini değiştirin.  
     2.   Aksi halde, **Dil ekle** düğmesine tıklayın, menüden istediğiniz dili seçin ve etiket ve yardım metni için çevrilmiş değerleri sağlayın.  
4.   İşlemi tamamladığınızda **Tamam** düğmesini tıklayın.  

### <a name="deleting-custom-fields"></a>Özel alanları silme
Bazı ender durumlarda, bir özel alanın artık gerekli olmadığına karar verebilirsiniz. Bu durumda, sistem yöneticisi bu alanı **Özel alanlar** sayfasından silmeyi seçebilir. Bunu yapmak için doğru alanın seçili olduğundan emin olun, **Sil**'e tıklayın, silme işlemini onaylamak için **Evet**'i seçin ve son olarak **Değişiklikleri uygula**'ya tıklayın. 

> [!Note]
> Bu eylem geri alınamaz ve alanla ilişkili verilerin veritabanından tamamen silinmesine neden olur. 

## <a name="appendix"></a>Ek 
### <a name="who-can-create-custom-fields"></a>Özel alanları kimler oluşturabilir?
Sistemi korumak amacıyla, varsayılan olarak yalnızca sistem yöneticileri özel alanlar oluşturabilir. Ancak, kuruluşun gerekli gördüğü kullanıcılara sistem yöneticisi tarafından **Çalışma zamanında özelleştirme yetkili kullanıcısı** güvenlik rolü kullanılarak özel alanlar oluşturma hakkı verilebilir. Bu güvenlik rolüne sahip olmayan kullanıcılar özel alanlar oluşturamaz ancak sistemdeki diğer kullanıcılar tarafından eklenen özel alanları görebilir ve bunlarla etkileşimde bulunabilir.    

### <a name="what-tables-support-custom-fields"></a>Hangi tablolar özel alanları destekler?
Performans ve teknik nedenlerle, şu anda yalnızca aşağıdaki koşulları karşılayan tablolara özel alanlar eklenebilir.

- Tablo şu gruplardan biri olarak etiketlenmelidir: 
     -   Grup
     -   WorksheetHeader
     -   Ana
     -   Çeşitli
     -   Parametre
     -   Referans
     -   TransactionHeader
- Tablo başka bir tabloya genişletilemez.
- Tablo bir sistem tablosu olarak işaretlenemez.
- Tablo geçici bir tablo olamaz.

