---
title: Mali raporlar oluştur
description: Bu makalede, mali rapor oluşturma hakkında bilgiler sağlanmaktadır.
author: jinniew
ms.date: 02/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 59ec6978d83f5c51309bc7d90d47366774cb2880
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898841"
---
# <a name="generate-financial-reports"></a>Mali raporlar oluştur

[!include [banner](../includes/banner.md)]

Bu makalede, mali rapor oluşturma hakkında bilgiler sağlanmaktadır.

Rapor oluşturmak için rapor tanımını açın ve araç çubuğunda **Oluştur**'u seçin. **Rapor Kuyruğu Durumu** sayfası açılır ve raporunuzun kuyruktaki konumunu gösterir.

Rapor oluşturma işlemi sürerken, **Rapor Kuyruk Durumu** sayfasında aşağıdaki rapor kuyruk durumu göstergeleri görüntülenebilir.

| Çalıştırma Durumu          | İl | Açıklama|
|-----------------|--------|--------------------|
| Sıraya alma        | Geçici |Rapor tanımı, rapor oluşturma sırasına yerleştirilmeden önce doğrulanır.                    |
| Kuyruğa eklendi          | Geçici | Rapor, rapor oluşturma kuyruğuna girer ve işlenmeyi bekler.                      |
| İşleniyor      | Geçici | Bu durum genellikle **Kuyruğa alınmış** durumunu izler ve işlem tamamlandığında genellikle **Son** durumuna geçiş yapar.       |
| Son işlem yapılıyor | Geçici | Bu durum **İşleniyor** durumunu takip eder ve tüm rapor verilerinin toplandığını ancak hesaplama ve yuvarlama gibi türev eylemlerin gerçekleştirilmekte olduğunu gösterir.            |
| İptal ediliyor      | Geçici | Rapor kullanıcının isteğiyle iptal edildi. Bu durum, **Kuyruğa alındı** veya **İşleniyor** durumundaki bir rapor için kullanıcı tarafından istenen bir iptalin sonucunda oluşur. Sistem çok uzun olmadıkça ve başka bir durumda bunu sonuçlandırmak zorunda olmadığı sürece sistem raporu **İptal edildi** durumuna geçirmeye çalışır. |
| İptal Edildi        | Son | Raporun işlenmesi sona erdi ancak kullanıcı tarafından istenen bir durdurma nedeniyle tamamlanmadı.            |
| Tamamlandı       | Son | Rapor zaten kullanımda.                      |
| Başarısız          | Son | Rapor işlemeyi tamamladı ancak başarısız oldu ve kullanılmamalı. |

Varsayılan olarak, oluşturulan rapor Web Görüntüleyici'de açılır. Rapor oluşturma için aşağıdaki seçenekler kullanılabilir:

- Otomatik olarak rapor veya rapor grubu oluşturmak için bir plan ayarlayın
- Hesapları veya bir rapordaki verileri eksik olup olmadığını denetleyin ve raporun doğruluğunu doğrulayın

Bir rapor oluşturduğunuzda, Rapor tanımını sekmesinde belirlediğiniz seçenekleri kullanılır.

## <a name="generate-a-financial-report"></a>Bir mali rapor oluştur

Mali rapor oluşturmak için **Genel kayıt defteri** \> **Sorgular ve raporlar** \> **Mali raporlar**'a gidin.

- Oluşturmak için bir rapor seçip **Oluştur**'u seçin.
- **Rapor tarihi** alanını doldurup **Tamam**'ı seçin.

Rapor oluşturulduktan sonra raporu **Raporlar** bölümünden görüntüleyebilirsiniz.

Raporu **Görüntülemeyi** veya **Silmeyi** seçebilirsiniz.

**Rapor tasarımcısını** kullanarak rapor oluşturmak için rapor tanımını açın ve ardından araç çubuğundaki **Oluştur** düğmesini seçin. **Rapor Kuyruğu Durumu** sayfası açılır ve raporunuzun kuyruktaki konumunu gösterir. Varsayılan olarak, oluşturulan rapor Web Görüntüleyici'de açılır.

## <a name="report-groups"></a>Rapor grupları

Rapor grupları aynı anda birden fazla rapor oluşturmak için etkili bir yoldur. Örneğin, ay sonunda kullanıcılarınızın her ay için sekiz rapor oluşturduğunu bildiğinizi varsayalım. Bir rapor grubu oluşturun ve gruptaki sekiz raporun her biri için **Oluştur**'u seçmek yerine, rapor grubu için **Oluştur**'u seçebilirsiniz böylece sekiz rapor tek bir adımda oluşturulacaktır. Seçili rapor grubundaki raporlar oluşturulduğunda, tek tek raporları görüntülemek için **mali raporlara** **(Genel kayıt defteri > Sorgular ve raporlar > finansal raporlar**) gidebilirsiniz. Rapor grubu ayarlamak için aşağıdaki adımları tamamlayın.

1. Rapor tasarımcısında **rapor gruplarını** seçin. 
2. Rapor grubuna dahil etmek için varolan rapor tanımlarını seçin. 
3. Gruba eklenecek raporlardan Şirket, ayrıntı ve tarih ayarlarını geçersiz kıl seçeneğini belirleyin.
   Her rapor için **şirket**, **dönem**, **yıl** ve **ayrıntı düzeyini** ayarlamayı öneririz. 
4. Rapor grubunu kaydedin.

## <a name="schedule-report-generation"></a> Rapor oluşturmayı planlama
Birçok şirket iş süreçleriyle uyum sağlamak üzere planlı aralıklarda çalıştırılan temel bir rapor kümesine sahiptir. Bir raporun örneğin günlük, haftalık, aylık veya yıllık olarak oluşturulmasını planlayabilirsiniz. Bu, tek bir rapor ya da birden fazla şirketi içeren bir rapor grubu olabilir. Bir raporlama ağacı tanımındakiler gibi belirtilen şirketlerin her biri için kimlik bilgilerinizi girmeniz gerekir. Kimlik bilgileri geçerli değilse rapor yalnızca erişime izniniz bulunan o anda oturum açtığınız şirket gibi bilgileri görüntüler. Çıkış bilgileri önce rapor grubundan ve ardından tek raporlardan okunur.

Rapor planları oluşturulup kaydedildikçe Rapor Planları'nın altındaki gezinti bölmesinde görüntülenir. Raporları düzenlemek için klasörler oluşturabilirsiniz. Bir plandaki tek bir rapor çalışmıyorsa tüm diğer raporlar çalışmaya devam eder.

> [!IMPORTANT]
> Rapor planlarını oluşturmak, değiştirmek ve silmek için, tasarımcı veya yönetici rolüne sahip olmanız gerekir. Bir rapor çalıştırıldığında, raporu oluşturmak için planı oluşturan kullanıcının kimlik bilgileri kullanılır.

### <a name="create-a-report-schedule"></a>Rapor planı oluşturma

1. Rapor Tasarımcısı'ndaki **Dosya** menüsünde, **Yeni**'yi seçin ve ardından **Rapor planı**'nı seçin. **Yeni Rapor Planı** iletişim kutusu açılır.
2. **Ayarlar**'ın altında, planlamak için tek bir rapor veya bir rapor grubu seçin. Yalnızca şirkete ait raporlar veya rapor grupları ya da o anda oturum açtığınız yapı taşı seçimi kullanılabilir.
3. Rapor planını açmak için **Etkin** onay kutusunu işaretleyin. Bir rapor planını yalnızca raporu oluşturan ya da yönetici etkinleştirebilir veya devre dışı bırakabilir.
4. Şirket kimlik bilgilerini girmek için **İzinler** düğmesini seçin. Varsayılan olarak, oturum açtığınız şirket için oturum açma bilgileriniz kullanılır. Raporlama ağacı tanımlarında olduğu gibi diğer şirketler dahil edilirse **Ayrı kimlik bilgileri kullan**'ı seçin ve ardından rapor planına dahil edilen her türlü diğer şirketin kimlik bilgilerini girin. Her şirket için **Windows Kimlik Doğrulaması**'nı seçebilir ya da bir kullanıcı adı ve parola yazabilirsiniz. Bu şirketlere ait kimlik bilgilerini kaydetmek için **Kimlik bilgilerini kaydet** onay kutusunu seçin ve ardından iletişim kutusunu kapatmak için **Tamam**'ı seçin.
5. **Sıklık**'ın altındaki **Yinelenmeyi başlat** alanında planın başlayacağı tarihi seçin. Varsayılan olarak, istemci bilgisayarın geçerli sistem tarihi seçilir.
6. **Raporu şurada çalıştır:** alanında, raporun çalıştırılması gereken saati seçin. Geçerli sistem saatinden önce olan bir saati girerseniz rapor sonraki planlı tarihte çalıştırılır.
7. **Yinelenme modeli** alanında, raporun ne sıklıkta çalıştırılacağını belirtin. Varsayılan olarak, **Günlük** 1 aralık (gün) değeriyle birlikte seçilir. Diğer seçenekler haftalık, aylık ve yıllıktır.
8. Yinelenme aralığı alanında, raporun oluşturulmasının ne zaman durdurulacağını seçin.

    - **Bitiş tarihi yok**: Rapor planı süresiz olarak çalışır.
    - **Tekrar sayısını ayarla**: Rapor planı belirtilen sefer kadar çalışır ve ardından devre dışı bırakılır.
    - **Şu tarihte sonlandır**: Rapor planı belirtilen tarihte sona erer.

9. **Kaydet**'i seçin. **Farklı Kaydet** iletişim kutusunda, rapor planı için benzersiz bir ad ve açıklama girin.

Bir rapor planını kopyalamak için, tasarımcı veya yönetici rolüne sahip olmanız gerekir. Rapor planını bir yönetici değiştirse bile rapor, raporu oluşturan kullanıcının kimlik bilgilerini korur.

### <a name="copy-a-report-schedule"></a>Bir rapor planını kopyalama

1. Rapor Tasarımcısı'ndaki gezinti bölmesinde **Rapor Planları**'nı seçin ve kopyalamak için bir rapor planı açın.
2. **Dosya** menüsünde, **Farklı Kaydet**'i seçin ve ardından **Farklı Kaydet** iletişim kutusunda plan için yeni bir ad ve açıklama girin. **Tamam**'ı seçtiğinizde yeni plan gezinti bölmesinde görüntülenir.
3. Yeni planda, alanları ve bilgileri gerektiği gibi değiştirin ve ardından araç çubuğundaki **Kaydet**'i ya da **Dosya** menüsündeki **Kaydet**'i seçin.

Bir rapor planını silmek için, rapor planının sahibi olmanız ya da yönetici rolüne sahip olmanız gerekir.

### <a name="delete-a-report-schedule"></a>Bir rapor planını silme

1. Rapor Tasarımcısı'ndaki gezinti bölmesinde **Rapor Planları**'nı seçin.
2. Silinecek rapor planını seçin ve ardından **Sil**'i seçin veya **Sil** tuşuna basın.
3. Silme doğrulama iletişim kutusunda, rapor planını kalıcı olarak silmek için **Evet**'i seçin. Planı silmek için izniniz yoksa bir ileti görüntülenir ve rapor silinmez.

### <a name="credentials-and-report-schedules"></a>Kimlik bilgileri ve rapor planları

Raporlarda yer alan tüm şirketler için gerekli olan kimlik bilgilerini girmezseniz rapor planını kaydettiğinizde şu iletiyi alırsınız: "Bu rapor planında bulunan şirketlere ait kimlik bilgilerinizi girmeniz gerekir. Kimlik bilgilerinizi girmek için İzinler düğmesini seçin."

Örneğin bir kullanıcı, kullanıcı adını ve parolasını kullanarak A Şirketinde oturum açıyor. Kullanıcı, birden fazla şirketten veri toplamak için bir raporlama ağacı tanımı kullanılan bir rapor için plan oluşturuyor. Bu rapor planı kaydedildiğinde, kullanıcıdan raporlama ağacı tanımında belirtilen diğer şirketlere ait kimlik bilgilerini girmesi isteniyor. Kimlik bilgilerinizin süresi dolduğunda, rapor planındaki etkilenen raporlar kimlik bilgileri güncelleştirilene kadar oluşturulmaz. Rapor kuyruğunda izinlerin güncelleştirilmesi gerektiğini belirtmek için bir ileti görüntülenir. Aşağıdaki senaryoların biri meydana gelirse rapor planı gerçekleştirilemez (bu senaryolar kimlik bilgileri gerektirdiğinden):

- Yeni bir şirket tek bir rapor için bir rapor ağacı eklemiştir.
- Bir rapor grubundaki bir rapor değiştirilmiştir.
- Rapor grubuna ek bir şirket için yeni bir rapor eklenmiştir.

Devam etmek için, **Rapor Planları** iletişim kutusundaki **İzinler** düğmesini seçin ve ardından ilgili kimlik bilgilerini girin.

## <a name="missing-account-analysis-feature"></a> Eksik hesap analizi özelliği
Bir yapı taşı grubundaki tüm satır tanımları, raporlama ağacı tanımları ve rapor tanımları çapında eksik olabilecek mali hesapları ve boyutları arayabilirsiniz. Bu kısa dönemde birkaç hesap veya yapı taşı oluşturduğunuzda veya güncellediğinizde ve tüm yeni bilgilerin raporlarınızda bulunduğunu doğrulamak istediğiniz zaman yararlıdır.

Eksik hesaplar en düşük ve en yüksek değerleri satır tanımını kullanılarak veya raporlama ağaç tanımından belirlenir ve daha sonra satır tanımı ya da raporlama ağaç tanımında olmayan, ancak mali verileri olan hesapların listesini görüntülenir. Eksik bir hesap satır tanımındaki değerlerden büyükse veya küçükse söz konusu hesap eksik hesaplar listesine eklenmez.

> [!TIP]
> Doğrulama amacıyla, bu işlem aylık raporları oluşturmanızdan önce ve yeni yap taşları oluşturduğunuzda çalıştırılmalıdır.

Değer aralıklarına sahip raporlarda eksik hesap bulunması ihtimali daha düşüktür. Mümkün olduğunda, yeni hesapları oluşturulduklarında eklemek için yapı taşındaki aralıkları kullanın. Herhangi bir rapor tanımı @ANY şirket olarak ayarlandıysa belirli bir şirkette oturum açarak söz konusu şirket için bir eksik hesap analizi yürütebilirsiniz.

> [!NOTE]
> Yeni bir şirket eklenmişse, yeni şirketi varolan tüm raporlarda raporlama ağaçlarına eklemeniz gerekir veya şirket eksik hesap analizine dahil edilmez.

### <a name="run-missing-account-analysis"></a>Eksik hesap analizi çalıştırma

1. Rapor Tasarımcısı'nda, **Araçlar**'ı ve ardından **Eksik Hesap Analizi**'ni seçin.
2. **Şirket filtresi** alanında, sonuçları filtrelemek için bir şirket seçin veya var olan tüm şirketlere ait sonuçları görüntülemek için **Tümü (filtresiz)**'i seçin.
3. **Boyut filtresi** alanında, sonuçları filtrelemek için bir boyut seçin veya var olan tüm boyutlara ait tüm boyut bilgilerini görüntülemek için **Tümü (filtresiz)**'i seçin.
4. **Gruplandırma ölçütü** alanında, sonuçları sıralamak için bir seçenek seçin. Sonuçları etkilenen yapı taşına ya da boyut ve değer kümelerine göre sıralayabilirsiniz.
5. Görüntülenen sonuçları inceleyin. Üst bölmede bir madde seçtiğinizde, alt bölmede özel durum hakkında ek bilgiler görüntülenir. Bu, ilgili boyutlar, değerler ve raporları içerir.
6. Etkilenen maddeyi açmak için, liste bölmesinde görüntülenen ilişkili simgeyi seçin veya maddeye sağ tıklayarak **Aç**'ı seçin. Birden fazla madde seçmek için, alt bölmede maddeleri seçerken **Ctrl** tuşunu basılı tutun.
7. Analize dahil edilmemesi gereken herhangi bir değer, yapı taşı veya rapor alırsanız maddeye sağ tıklayın ve **Hariç tut**'u seçin ya da maddeyi listeden kaldırmak için maddenin yanındaki **Hariç tut** onay kutusunu işaretleyin. Liste yenilendiğinde hariç tutulan maddeler dahil edilmez. Birden fazla madde seçmek için, alt bölmede maddeleri seçerken **Ctrl** tuşunu basılı tutun. Analizden çıkarmak için daha önce seçtiğiniz her türlü sonuç dahil tüm maddeleri görüntülemek için **Hariç tutulan yapı taşlarını ve değerleri göster** onay kutusunu işaretleyin ve ardından **Yenile**'ye tıklayın.
8. Ele aldığınız özel durumları yenilemek için **Yenile**'yi seçin. Tüm sonuçları tamamen yenilemek için **Evet**'i, ele alınan maddeleri kısmen yenilemek için ise **Hayır**'ı seçin.

    > [!NOTE]
    > Form, son 15 dakikada açılmadığı sürece açıldığında otomatik olarak yenilenir.

9. Sorunlar çözüldüğünde, **Tamam**'ı seçerek iletişim kutusunu kapatın.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Eksik hesap analiz için klavye kısayolları
Eksik bir hesap analizini çalıştırdığınızda, aşağıdaki klavye kısayollarını kullanılabilir.

| Bunu yapmak için                           | Şuna basın:  |
|--------------------------------------|----------------------------|
| Şirkete göre filtrele                    | Alt+C                      |
| Boyuta göre filtrele                  | Alt+D                      |
| Gruplandırma ölçütü alanını seçin            | Alt+G                      |
| Hariç tutulan yapı taşlarını ve değerleri göster      | Alt+S                      |
| Sonuçları yenile                      | Alt+R                      |
| Seçilen yapı taşını hariç tut  | Alt+X                      |
| Seçilen satır tanımını hariç tut  | Ctrl+B                     |
| Seçilen boyut değerini hariç tut | Ctrl+D                     |
| Seçilen rapor tanımını aç  | Ctrl+R                     |
| Seçilen satır tanımını aç     | Ctrl+O                     |


## <a name="additional-resources"></a>Ek kaynaklar

[Mali raporlama](financial-reporting-intro.md)

[Rapor Tasarımcısı arabirimi](report-designer-interface.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
