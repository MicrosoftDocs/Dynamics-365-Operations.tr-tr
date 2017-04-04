---
title: "Projeye kaynak oluşturma"
description: "Bu konuda, proje resourcing hakkında bilgi sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: c29c95fc6abd13e668c44d3ccf437bb0e879e46b
ms.lasthandoff: 03/31/2017


---

# <a name="project-resourcing"></a>Projeye kaynak oluşturma

Bu konuda, proje resourcing hakkında bilgi sağlar.

Bir proje yöneticileri ve proje planlama aşaması sırasında kaynak yöneticileri için kaynak ayırma, burada onlar gerekir belirlemek ve bir proje üzerinde çalışmak için doğru kaynak ayırmak iştir. İşlemler için Microsoft Dynamics 365 içinde yetenekleri projeler resourcing, geçici bir özel Nişan ya da Nişan parçası için ayrılmış kaynaklar olarak kabul edilen rolleri tanımlamanıza olanak sağlar. Bu tür kaynak oluşturma, proje yöneticileri ve kaynak yöneticilerinin aşağıdaki görevleri yerine getirmesini sağlar:

-   Kaynakları eşleştirmeyi kolaylaştırmak için gerekli olan yetkinliklere sahip bir rol tanımlamak.
-   Roller üzerinde korunan kaynaklara dayalı bir ilk Nişan zamanlama tanımlamak için kullanın.
-   Bir proje için atanan rolleri ve kaynakları temel alarak maliyetleri tahmin etmek ve başlangıç bütçesini belirlemek.
-   Roller her Nişan için gerekli olan kaynak ayırmaları sayısını tahmin etmek için kullanın.
-   Tüm proje yaşam döngüsü için gereken kaynak sayısını tahmin etmek.
-   İlk kaynak atamalarını kullanarak iş kırılım yapısı (WBS) taslağı hazırlamak.

[![Proje yaşam döngüsü](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Hasılatını planlama projesi olarak planlanmış kaynaklar aracılığıyla kaynakları ile değiştirilebilir. Proje Yöneticisi de dönün ve herhangi bir proje aşamaları sırasında resourcing rezervasyonları güncelleştirin.

## <a name="set-up-project-resources"></a>Proje kaynaklarını ayarlama
Bir takvim ayarlamanız ve bunu bir personel veya çalışanla ilişkilendirmeniz gerekir. Takvimi, proje ve proje için ayrılmış olan kaynakların çalışma zamanını planlamak için kullanılır. Takvim ayarlama işlemi sırasında, proje yöneticileri kaynak eşitlemeyi kaynak optimizasyonunun bir parçası olarak gerçekleştirebilirler. Takvim planına bağlı olarak, kaynaklara kısıtlamalar getirilebilir. Temel bir takvim ayarlamak **takvimleri** sayfa. 

Bir alt projenin kaynak olarak ayarladığınızda, kaynakları ayarlama şirketteki iş arkadaşlarına arasından seçim yapabilirsiniz veya kuruluşunuzdaki diğer şirketlerden çalışanları seçebilirsiniz. Bu şirketlerarası kaynaklardır. İşçi, şirketinizdeki bir proje kaynağı olarak ayarlamak ve nasıl bir şirketlerarası proje kaynağı ayarlarken aşağıdaki yordamlar açıklanmaktadır.

### <a name="set-up-a-worker-as-a-project-resource"></a>Bir çalışanı proje kaynağı olarak ayarlama

1.  Üzerinde **çalışanları** sayfa içinde **çalışanları** listesinde, proje kaynağı olarak eklediğiniz alt seçin ve alt kaydı açın.
2.  Eylem bölmesinde tıklatın **proje**&gt;**Kurulum**&gt;**Proje Kurulumu**.
3.  Bir takvim seçin ve ardından sayfayı kapatın.

Bir kaynak için ön atama türü olarak varsayılan projeleri de belirtebilirsiniz. Ön atamalar, kaynak yöneticisi veya proje yöneticisi, kaynağın hangi projede çalışacağını önceden bildiğinde kullanılır. Ön atamalar için bir proje sponsoru veya müşterinin talebi de temel alınabilir. Bir projeyi önceden atamak için **Projeleri ata** sayfasındaki **Projeler** sekmesinde bulunan **Kalan projeler** listesinden ilgili projeyi seçin.

### <a name="set-up-an-intercompany-resource"></a>Şirketlerarası bir kaynak ayarladıysanız

İşçi şirketlerarası bir kaynak olarak ayarladığınızda, ödünç verme şirket ve ödünç şirket Kurulumu tamamlamalısınız. 

**Ödünç verme şirkette:**

1.  Ödünç verme şirket seçilir ve "bir alt projenin kaynak olarak ayarlayın." Yukarıdaki yordamı tamamlayın işlemleri için Dynamics 365 içinde doğrulayın
2.  Git ** genel muhasebe **&gt; ** deftere nakil kurulumu **&gt;**Şirketlerarası muhasebe**. Click **New**.
3.  İçinde ** yasal Varlık Kimliği ** alanında, ödünç verme şirketi seçin. Kalan alanları uygun şekilde doldurun ve **kaydetmek**.
4.  Git ** proje yönetimi ve muhasebe **&gt; ** Kur **&gt;**fiyatları ** &gt;**Transfer fiyatı**.** **
5.  Üzerinde ** Transfer fiyatı ** formunda,'ı **yeni**hem de ** tüzel ödünç ** alanında, ilgili şirketi seçin.
6.  Sadece ödünç şirket içinde bu bölümün başında oluşturulan kaynak ödünç vermek isterseniz, **kaynak** alanında, oluşturduğunuz kaynak adını seçin. Tüm kaynakları şirkette ödünç şirkete kullanılabilmesini istiyorsanız, bırakın ** kaynak ** alanı boş.
7.  Git ** proje yönetimi ve muhasebe **&gt; ** Kur **&gt;**proje yönetimi ve muhasebe parametreleri**ve ** şirketlerarası ** sekmesinde, ayarlamak ** etkinleştirmek şirketlerarası kaynak planlama ve zaman çizelgelerini ** alanı **Evet**.

**Ödünç şirket:**

1.  Git **proje yönetimi ve muhasebe**&gt;**proje kaynakları**&gt;**kaynaklar listesi**.
2.  Arama Filtresi alanında ödünç verme şirket adı ödünç şirket için kaynak listesinde bulunduğunu doğrulamak önceki yordamda oluşturduğunuz kaynak adını girin.

## <a name="manage-resource-competencies"></a>Kaynak yetkinliklerini yönetme
Kaynak yetkinlikleri, kaynak yönetiminin önemli bir parçasıdır. Yetkinlikler, doğru yetenek, sertifika ve proje deneyimi açısından uygun dengeye sahip kaynakların belirlenmesinde temel olarak kullanılabilir. Bu bilgiyi her kaynak için ayarlamanız ve düzenli olarak güncellemeniz gerekir. Bu şekilde, proje kaynak ataması sırasında belirli kaynak yetkinlikleri eşleştiğinde becerileri en üst seviyeye çıkarabilirsiniz. [![Becerileri, sertifikaları, eğitim ve Proje deneyimi örnekleri](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Aşağıdaki yordamlar bir kaynak için bazı yetkinliklerin nasıl ayarlanacağını açıklar. 

Bir çalışan için yetkinlikleri ayarlamak üzere, İnsan kaynaklarındaki **Çalışanlar** liste sayfasını veya Proje yönetimi ve muhasebedeki **Kaynaklar** listesi sayfasını kullanabilirsiniz. Aşağıdaki yordamlarda, **çalışanları** İnsan Kaynakları'ndaki liste sayfası kullanılır.

### <a name="set-up-competencies-certificates"></a>Yetkinlikleri ayarlama: Sertifikalar

1.  **Çalışanlar** listesi sayfasında, sertifika bilgisi ekleyeceğiniz çalışanın satırını seçin.
2.  Eylem Bölmesinde, **Çalışanlar** sekmesindeki **Yetkinlikler** gurubunda **Sertifikalar**'a tıklayın.
3.  **Yeni**'ye tıklayın.
4.  **Sertifika türü** alanında **PMP**'yi seçin.
5.  **Başlangıç tarihi** alanında, **1/10/2015** tarihini seçin.
6.  **Kaydet**'e tıklayıp sayfayı kapatın.

### <a name="set-up-competencies-skills"></a>Yetenekleri ayarlama: Beceriler

1.  **Çalışanlar** listesi sayfasında, önceki yordamda kullanmış olduğunuz çalışanın hala seçili olduğundan emin olun. Ardından Eylem Bölmesinde, **Çalışanlar** sekmesindeki **Yetkinlikler** gurubunda **Beceriler**'e tıklayın.
2.  **Yeni**'ye tıklayın.
3.  **Beceri** alanında **Proje yönetimi**'ni seçin.
4.  **Düzey** alanında **5 Uzman**'ı seçin.
5.  **Düzey tarihi** alanında **14/1/2014** tarihini seçin.
6.  **Deneyim yıl sayısı** alanına **10** girin.
7.  **Kaydet**'e tıklayıp sayfayı kapatın.

## <a name="create-a-new-project"></a>Yeni proje oluştur
1.  ' I **proje yönetimi ve muhasebe**&gt;**çalışma**&gt;**proje yönetimi**.
2.  **Yeni proje**'ye tıklayın ve şu değerleri girin:
    -   **Proje türü** - zaman ve malzeme
    -   **Proje adı** -XYZ yükseltme Phase 2
    -   **Proje grubu** -TM\_Süren iş
    -   **Proje Sözleşme kimliği** -00000002
3.  **Proje oluştur**'a tıklayın.

### <a name="assign-a-resource-to-a-project"></a>Projeye kaynak atama

1.  ' I **İnsan Kaynakları**&gt;**çalışanları**&gt;**çalışanları**.
2.  **Çalışanlar** listesinde, daha önce yetkinlikleri ayarladığınız çalışanın kaydını seçin ve çalışan kaydını açın.
3.  Eylem Bölmesinde, **Proje** sekmesindeki **Ayar** gurubunda **Projeleri ata**'ya tıklayın.
4.  **Kaynak doğrulama proje atamaları** sayfasında, **Projeler** sekmesine tıklayın.
5.  İçinde **Seçilen projeler için proje eklemek**, XYZ yükseltme Phase 2 proje üzerinde filtre
6.  **Kalan projeler** bölmesinde, bir proje seçin ve ardından **Seçilen projeler** bölmesine eklemek için oka tıklayın.
7.  Sayfayı kapatın.

Gerekirse, kaynak için kategoriler de atayabilirsiniz. Kategori türü Maliyet veya Gelir'dir. Bu kuruluş tarafından belirlenir. Kaynağın atanan kategori yok ise, Dynamics 365 işlemleri için varsayılan kategori için maliyet ve gelir saat fiyatları yukarı bakar.

### <a name="set-up-project-resource-and-role-characteristics"></a>Proje kaynağını ve rol özelliklerini ayarlama

Proje yöneticisi, bir proje için gerekli olan rolleri oluşturmak için proje kaynak oluşturma işlevini kullanabilir. Roller, teyit edilen kaynaklar hala bilinmeyen kaynaklar madde rezerve ederken olduğunda kullanılabilir. Proje aşamaları planlama devam edebilmesi için rolleri geçici olarak planlanmış kaynaklar olarak rezerve edilebilir. 

[![Bir rol örneği](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Senaryo:** Contoso, onaylanmış bir proje tüzüğü olan bir Zaman ve malzeme projesini tamamlamak üzere işe alınmıştır. Yardımcı proje müdürü, projenin amacını doldurmaya devam etmektedir. Kaynak Yöneticisi şu anda yeni bir proje üzerinde çalışmak için ayrılmış belirli kaynakları tanımlamak için kullanılır. Proje destekleyicisi, kritik Proje yapısı gereği istenen rollerinden biri Kıdemli proje yöneticisidir. Kaynak Yöneticisi, yeni kaynak alma ve çırak proje yöneticisi proje planlama sırasında kaynak bilgilerini gerektiren durumlarda sistemde rolünü tanımlayabilirsiniz. 

Aşağıdaki adımlar nasıl Kaynak Yöneticisi Kıdemli proje yöneticisi rolünü kurmadan ve kaynak özellikleri bu ilişkilendirmeyi gösterir. Daha sonra, rol istenen kaynak yetkinlikleriyle eşleşen kullanılabilir kaynakları aramak için kullanılabilir.

1.  ' I **proje yönetimi ve muhasebe**&gt;**Kurulum**&gt;**kaynakları**&gt;**rolleri Kurulumu**.
2.  **Yeni**'ye tıklayın ve şu değerleri girin:
    -   **Rol Kimliği** -Kıdemli Proje Yöneticisi
    -   **Açıklama** -Kıdemli Proje Yöneticisi
3.  **Oluştur**'a tıklayın.
4.  **Kıdemli Proje Yöneticisi** rolünü seçip **Özellikleri yapılandır**'a tıklayın.
5.  **Özelliklerin türü** alanında, **Beceri**'yi seçin.
6.  **Kullanılabilir özellikler** alanına, aradığınız beceriyi girin.
7.  **Özellik türü** alanında **Sertifika**'yı seçin.
8.  **Kullanılabilir özellikler** alanına, aradığınız sertifika türünü girin.
9.  **Tamam**'a tıklayıp sayfayı kapatın.

### <a name="assign-a-project-resource-to-a-project"></a>Projeye proje kaynağı atama

1.  ' I **proje yönetimi ve muhasebe**&gt;**ortak**&gt;**projeleri**&gt;**tüm projeleri**ve açık **XYZ yükseltme Phase 2** proje.
2.  **Proje ekibi ve planlama** sekmesinde **Ekle**'ye tıklayın.
3.  **Rol** alanında **Ekip üyesi**'ni seçin.
4.  **Takvimden rezerve et**'e tıklayın.
5.  **Kaynak kullanılabilirliği** sayfasında, **Görünüm ayarları**'na tıklayın.
6.  **Görünüm ayarlarını ayarla** sayfasına şu değerleri girin:
    -   **Tarih aralığını görüntüleme biçimini** - gün
    -   **Kullanılabilirlik açıklamaları görüntülemek** - Evet
    -   **Kalan kapasite görüntü** - Evet
7.  Kaynak listesinde, bir kaynak seçin.
8.  ' I **sabit kitap**&gt;**tam kapasite**.
9.  Sayfayı kapatın.

### <a name="assign-a-resource-to-a-default-role"></a>Varsayılan bir role kaynak atama

Proje veya kaynak yöneticilerine yardımcı olmak için inebilir aşağı bir proje için ayrılmış kaynakları üzerinde daha fazla. Varsayılan bir rolü mevcut bir kaynakla veya yeni edinilen bir kaynakla ilişkilendirebilirsiniz. Daniel işe alındığında, örneğin, yaptığı iş analisti rolü doldurmak için beceri ve deneyimi vardı. Kaynak Yöneticisi, bu rolü Daniel'ın varsayılan rol olarak atanmış. Bu nedenle, kaynak yöneticisi Daniel projeler üzerinde çalışmak kullanılabilir olan iş analistleri havuzu eklendi. 

Kaynak ayırma sırasında proje yöneticileri proje üzerinde çalışmak kullanılabilen rol kaynakları filtre uygulayabilirsiniz. Bu bilgiyi, kaynak karşılama sırasında çok ölçütlü karar analizi gerçekleştirirken bir ölçüt olarak kullanabilirler. Ayrıca, söz konusu proje için belirli becerileri, eğitimi ve deneyimi olan kaynakları aramak için filtre uygulamak amacıyla diğer kaynak özelliklerini ekleyebilirler. 

**Senaryo:** onaylanmış bir proje başladı ve Kıdemli proje yöneticisi rolü proje planlama aşaması sırasında planlı bir kaynak olarak ayrıldı. Kaynak yöneticisi, Kıdemli proje yöneticisi rolünü yerine getirecek bir kaynak edinmiştir.

1.  ' I **proje yönetimi ve muhasebe**&gt;**proje kaynakları**&gt;**kaynaklar listesi**.
2.  **Kaynak** listesinden, **Daniel Goldschmidt**'i seçin.
3.  ' I **proje kaynak**&gt;**koru**&gt;**Kaynak rolü**.
4.  **Yeni**'ye tıklayın ve şu değerleri girin:
    -   **Etkili** - (geçerli tarihi)
    -   **Sona erme** - asla
    -   **Rol** -Kıdemli Proje Yöneticisi
5.  **Kaydet**'e tıklayıp sayfayı kapatın.
6.  **Yetkinlikler** sekmesinde, **ProjectMgmt** becerisini ve **PMP** sertifikasını ekleyin.

## <a name="set-up-role-based-pricing"></a>Rol tabanlı fiyatlandırmayı ayarlama
Tüm satış, maliyet ve transfer fiyatları roller için ayarlanabilir.

1.  ' I **proje yönetimi ve muhasebe**&gt;**Kurulum**&gt;**fiyatları**&gt;**satış fiyatı (saat)**.
2.  Click **New**.
3.  Bir yürürlük tarihi girin.
4.  **Rol** sütunundan bir rol seçin.
5.  **Fiyatlandırma** sütununa, seçilen kaynak rolü için bir fiyat girin.

## <a name="form-a-project-team"></a>Proje ekibi oluşturmak
Bir projede önceden ayarlanmış olan rolleri kullanmak için bir proje yöneticisi rolleri proje ile ilişkilendirmeniz gerekir. Bir proje için birden çok rol atanabilir ve Dynamics 365 işlemleri için bu rolleri Karışıklığı önlemek için rezervasyon sırasında otomatik olarak etiketler. Proje Yöneticisi üç yazılım mühendisleri, yazılım mühendisi, 1 olan üç yazılım mühendisi rol gerektiriyorsa, örneğin, yazılım mühendisi 2 ve yazılım mühendisi olarak etiketlerine 3 otomatik olarak oluşturulur. Rol için rol özellikleri önceden ayarlanmışsa, kaynak arama sırasında filtre olarak uygulanır. Aramayı daha detaylı hale getirmek için ek özellikler eklenebilir. 

Kaynak kullanılabilirliğinin daha iyi görüntülenebilmesi için görüntüleme ayarları özelleştirilebilir. Saatlik, günlük, haftalık, aylık, üç aylık ve yıllık kullanılabilirliği gösterme seçenekleri vardır. Ayrıca, kullanılabilir ve kalan kaynak kapasitesini görüntüleme seçeneği de bulunur. Bu seçenek, faaliyetler veya kaynak kullanılabilirliği için kullanılabilir zamanı tahmin etmeniz gerektiğinde yararlıdır. 

Proje Yöneticisi rolü sayfasında seçebilir ve gereksinimi karşılayan kullanılabilir bir kaynak ise, rolü doldurmak için bir kaynak ayırmak için seçin. Not kaynakları planlama aşamasında bu noktada ayrılmış olması gerekmez. Bir ÇÇY oluşturduğunuzda, proje için Ekip kaynakları rolleri yerine kullanabilirsiniz. Roller ekip kaynakları ÇÇY değiştirilirse, kaynak Kurulumu proje ekibi listeleme ve zamanlama otomatik olarak güncelleştirir. 

[![Rolleri hem fiili kaynakları içeren proje takım listeleme](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Proje yöneticisinin bir proje için bir kaynağı rezerve etmek için kullanabileceği **Kalan kapasite**, **Tam kapasite**, **Kapasite yüzdesi** ve **Saatleri belirtme** gibi çeşitli seçenekleri vardır. Kaynak atamalarını değiştirirseniz, bu rezerve etme seçenekleri herhangi bir zamanda iptal edilebilir. İki tür rezervasyon desteklenir:

-   **Sabit bir kitap** – kaynak ayırma onaylanması ve belirtilen süre için Nişan üzerinde çalışmak üzere onaylanmış.
-   **Yumuşak kitap** – kaynak ayırmaları belirtilen süre için Nişan üzerinde çalışmak üzere ayarlı kesin.

Aşağıdaki yordamda bir proje ekibinin nasıl oluşturulacağı açıklanmaktadır.

### <a name="create-a-project-team"></a>Proje ekibi oluşturma

1.  **Tüm projeler** liste sayfasında bir proje seçin ve ardından **Düzenle**'ye tıklayın.
2.  Üzerinde **proje ekibi ve iş planlama çizelgeleme** No **zamanlama bitiş tarihi** alanına, zamanlama başlangıç tarihi artı bir ay. Zamanlama Başlangıç tarihi, örneğin, 24 Haziran 2017 dir (24/06/2017) girin **24/07/2017**.
3.  Click **Add**.
4.  **Projeye roller ekle** bölmesindeki **Rol **alanında **Kıdemli Proje Yöneticisi**'ni seçin.
5.  **Gerekli yetkinlikler**'e tıklayın.
6.  **Özelliklerini seçin** sayfasında, Kıdemli proje yöneticisi rolü için önceden ayarlamış olduğunuz özellikler varsayılan olarak seçilir. **Tamam** düğmesine tıklayın.
7.  **Projeye roller ekle** sayfasındaki **Kaynak sayısı** alanına **1** girin.
8.  **Kaynak** alanında, arama gerekli yetkinliklere sahip tüm kaynakları gösterir. **Daniel Goldschmidt**'i seçin ve **Oluştur**'a tıklayın.
9.  **Proje** sayfasında **Ekle**'ye tıklayın.
10. **Projeye roller ekle** bölmesindeki **Rol **alanında **Ekip üyesi**'ni seçin. **Kaynak sayısı** alanına **5** girin.
11. **Oluştur**'a tıklayın.
12. **Projeler** sayfasında **Kaynağı karşıla**'ya tıklayın.

## <a name="resource-capacity-synchronization"></a>Kaynak kapasitesi eşitleme
Kaynak eşitleme işlemleri, takvim ve temel takvim bilgilerini, proje kaynak planlamasına doğru çekilmesinin sağlanmasına yardımcı olur. Takvim değiştirilse, işlemler proje kaynak planlama için gerekli güncelleştirmeleri yapar. İşlemler, takvim kaynak bilgileri önceden eşitlendiği için performansın artmasına da yardımcı olur. Bu durumda, kaynak planlama bilgilerindeki güncelleştirmeler daha hızlı gerçekleşir. İşlemleri tek tek planlamak yerine toplu iş olarak planlamanızı öneririz. Aksi halde, birisinin bilgiler son eşitlendiğinde dahil edilen tarihleri unutma riski vardır. Dahil olan tarihler kullanılmazsa, tarih eşitleme sırasında boşluklar oluşabilir.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Takvim eşitleme](./media/projectresourcing04-1024x471.jpg)

**Synchronize resource capacity roll-ups**

Eşitleme işlemi, tüm kaynak takvim bilgilerini eşitlemek üzere tasarlanmıştır. Bu bilgiler, projenin Kaynak takvimi kapasite tablosundaki değişikliklerle ilgili temel takvim bilgilerini içerir. Yeni kaynaklar Project'te eklediyseniz, eşitleme güncelleştirilmiş Takvim bilgilerini kullanılabilir olduğundan emin olun yardımcı olur. Eşitleme herhangi bir zamanda yapılabilir. 

Toplu iş kullanmanızı öneririz. Eşitleme kapasite rezervasyonunda seçenekler bulunmaktadır.

-   ' I **proje yönetimi ve muhasebe**&gt;**Periyodik**&gt;**kapasite eşitleme**&gt;**kaynaklar kapasite toplamalar eşitleme**.

| Seçenek | Açıklama                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evet    | Tüm kaynak verilerini takvimle ve temel takvim bilgileriyle eşitleyin ve proje kaynak kapasitesi takvimindeki tüm bilgileri değiştirin.                                                  |
| Hayır     | Tarih aralığı kodu ve belirtilen başlangıç ve bitiş tarihlerini temel alarak kaynak verilerini eşitleyin. Bu seçenek, mevcut verileri kaldırmaz ve yalnızca yeni eklenen kaynaklarla ilgili bilgileri güncelleştirir. |

[![Eşitleme işlemi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>WBS şablonlarında rolleri ayarlama
Proje yöneticileri, yeni projeler için WBS oluştururken uygulayabilecekleri WBS şablonlarını ayarlayabilirler. Bunlar bir şablon oluşturduğunuzda, proje yöneticilerinin rolleri ekleyebilirsiniz. Bir ÇÇY template.* * için rol atamak için aşağıdaki yordamı kullanın **

1.  ' I **proje yönetimi ve muhasebe**&gt;**Kurulum**&gt;**projeleri**&gt;**çalışma çözümleme yapısı şablonları**.
2.  Seçilen İKY şablonu için **Ayrıntıları** tıklayın.
3.  Listeden bir görev seçin ve **Rol** alanında, göreve atamak için bir rol seçin.

### <a name="work-with-a-wbs"></a>İKY ile çalışma

Yeni bir İKY oluşturabilir veya mevcut bir İKY şablonundan İKY kopyalayabilirsiniz. Proje Yöneticisi, İKY'deki yeni görevlere roller atayarak kaynakları kolayca yönetebilir. Roller, bir kaynak edinildikten veya görevde çalışmak üzere onaylı bir kaynak tanımlandıktan sonra değiştirilebilir. Bu esneklik, proje yöneticilerinin aşağıdaki görevleri gerçekleştirmesine olanak sağlar:

-   İKY iş paketleri için gereken kaynak sayısını belirlemek.
-   Proje maliyetlerini tahmin etmek.
-   Ön bütçe belirlemek.
-   Roller ve kaynakları temel alarak faaliyet süresini tahmin etmek.
-   Kullanılabilir proje bilgilerine dayanarak bazı proje yönetim planları geliştirmek.

Kaynak oluşturma işlevinin daha etkin kullanılması için İKY'ye ek seçenekler eklenmiştir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Seçenek</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kaynak atamaları</td>
<td>İKY'deki görevler için atanan kaynakları, tarihleri, saat sayısını ve rezervasyon türünü görüntüleyin.</td>
</tr>
<tr class="even">
<td>Takımı otomatik olarak oluştur</td>
<td>Görevle ilişkili rolleri kullanarak planlanmış kaynakları otomatik olarak ekleyin. Dynamics 365 işlemleri için rollere göre birden çok ölçüt karar çözümlemesi kullanarak planlanmış kaynaklar otomatik olarak önerir. İKY'deki görevler için roller ve çalışma (saat) ayarlandıktan ve yapı serbest bırakıldıktan sonra, <strong>Ekibi otomatik oluştur</strong>'a tıklayın. Gereken sayıda planlanmış kaynak İKY'ye ve <strong>Proje ve ekip planlama</strong> sekmesine eklenir.</td>
</tr>
<tr class="odd">
<td>Kaynak (açılan liste)</td>
<td><strong>Kaynak atamayı başlat </strong>sayfasında, belirtilen süreye göre kesin rezervasyon veya geçici rezervasyon yapmak için kaynakları seçebilirsiniz. Kaynak faaliyetlerini görmek ve süresini ayarlamak için görüntüleme ayarlarını düzenleyebilirsiniz. Aşağıdaki seçenekleri kullanarak, kaynakları seçebilir ve iş paketi düzeyinde atayabilirsiniz:
<ul>
<li><strong>Kabul et</strong> – Bir göreve atanan kaynakla ilgili değişiklikleri onaylar.</li>
<li><strong>İptal et</strong> – Bir göreve atanan kaynakla ilgili değişiklikleri iptal eder.</li>
<li><strong>Otomatik olarak ata</strong> – bu seçenek, seçili görev için eşleşen bir rol kullanılabilir staffed kaynakla seçer.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  ' I **proje yönetimi ve muhasebe**&gt;**projeleri**&gt;**tüm projeleri**.
2.  Listeden **XYZ Yükseltme Aşaması 2** projesini seçin.
3.  ' I **Plan**&gt;**etkinlikleri**&gt;**çalışma çözümleme yapısı**.
4.  İKY'ye aşağıdaki düzey bir faaliyetlerini eklemek için **Yeni**'ye tıklayın:
    -   Başlatma
    -   Planlama
    -   Yürütme
    -   İzleme ve Denetim
    -   Kapalı

5.  Tarihleri ve çaba ayarlayın (saat) aşağıda gösterildiği gibi ekran görüntüsü. [![Çaba ve tarihleri ayarlama](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
6.  **Başlatma** görev satırını seçin, ardından **Rol** alanında **Kıdemli Proje Yöneticisi**'ni seçin.
7.  **Yayımla**'ya tıklayın.
8.  Aynı satırda, **Kaynak** alanında **Daniel Goldschmidt**'i seçin.
9.  **Kabul et**'e tıklayın
10. **Planlama** görev satırını seçin ve ardından **Rol** alanında **İş analisti**'ni seçin.
11. **Yayımla**'ya ve ardından **Ekibi otomatik oluştur**'a tıklayın.
12. Görüntülenen iletişim kutusunda **Evet**'e tıklayın.
13. **Kaynak** alanında, değerin **İş analisti 1** olduğunu doğrulayın.
14. **İş analisti 1** kaynağı için aramayı açın ve **Kaynak atama formunu aç**'a tıklayın.
15. Görev için bir çalışan seçin.
16. ' I **yumuşak Ata**&gt;**tam kapasite**.
17. **Kaydet**'e tıklayıp sayfayı kapatın. 

> [!NOTE] 
> Kaynak sayısı 1'den kaldığı için belirtilen kaynak 2, şimdi olduğunu belirten bir uyarı almıyorum.
18. **İş kırılım yapısı **sayfasında, İKY'deki kaynak atamasını doğrulayın ve **Kaydet**'e tıklayın.

## <a name="resource-fulfillment-for-planned-resources"></a>Planlanmış kaynaklar için kaynak karşılama
Proje yöneticisi, bir proje için gerekli kaynak rollerini planlayabilir. Kaynak yöneticisi **Kaynak karşılama** sayfasında planlanan bu kaynakları istek olarak görür ve gerçek kaynakları atayabilir.

1.  ' I **proje yönetimi ve muhasebe**&gt;**projeleri**&gt;**tüm projeleri**.
2.  Listeden **XYZ Yükseltme Aşaması 2** projesini seçin.
3.  **Proje**'ye tıklayın.
4.  **Düzenle**'yi tıklatın.
5.  Üzerinde **proje ekibi ve iş planlama çizelgeleme** sekmesinde ** **'ı **Ekle**.
6.  **Rolleri ekle** iletişim kutusunda **Yazılım geliştiricisi** rolünü seçin.
7.  **Oluştur**'a tıklayın.
8.  Proje sayfasını kapatın.
9.  ' I **proje yönetimi ve muhasebe**&gt;**proje kaynakları**&gt;**kaynak Karşılama**.
10. **XYZ Yükseltme projesi Aşama 2** projesi için **Yazılım geliştirici 1**'i seçin.
11. Bir çalışan seçip **Ata** öğesine tıklayın.
12. **XYZ Yükseltme projesi Aşama 2** projesi için **Yazılım geliştirici 1** satırının kaldırıldığından emin olun.
13. **Proje ekibi ve planlama** sekmesinde, **XYZ Yükseltme Aşama2** projesi için, adım 11'de seçtiniz çalışanın **Yazılım geliştiricisi** olarak eklendiğini kontrol edin.

## <a name="requests-for-project-resources"></a>Proje kaynakları için istekleri
Proje kaynak planlama işlevselliği yalnızca yöneliyorlar veya projelerin ekip kaynakları dağıtmak için kaynak yöneticilerini destekler. Bu işlevselliği etkinleştirmek için aşağıdaki görevleri tamamlamak veya onların tamamlandığını doğrulayın.

-   Numara sıralarını ayarlayın.
-   Proje yönetimi ve muhasebe iş akışları ayarlayın.
-   Kaynak isteği iş akışı sağlar.

Doğrulanan veya yukarıdaki görevleri tamamlandı sonra gerektiğinde aşağıdaki görevleri tamamlayabilirsiniz.

-   Bir kaynak isteği yumuşak ayrıldı staffed kaynağı oluşturun.
-   Kaynak isteklerini izleyebilir.
-   Kaynak isteklerini yerine getirmek.
-   Staffed kaynak ÇÇY isteyin.
-   Staffed kaynak isteği olmayan bir proje defteri kaynakları.

## <a name="monitor-project-teams"></a>Monitör proje ekipleri
1.  ' I **proje yönetimi ve muhasebe**&gt;**projeleri**&gt;**tüm projeleri**.
2.  Projeler listesinde **XYZ Yükseltme Aşama 2** projesi için **Proje kimliği** bağlantısına tıklayın.
3.  **Proje ekibi ve planlama ** hızlı sekmesinde, listelenen proje kaynaklarının doğru olduğunu kontrol edin.



