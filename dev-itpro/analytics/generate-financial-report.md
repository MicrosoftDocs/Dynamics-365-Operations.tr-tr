---
title: "Bir mali rapor oluştur"
description: "Bu konu mali rapor oluşturma hakkında bilgi sağlar."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9b0d8fd9f5ae9d99f299cc71d7caef021ad3fb9d
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="generate-a-financial-report"></a>Bir mali rapor oluştur

[!include[banner](../includes/banner.md)]


Bu konu mali rapor oluşturma hakkında bilgi sağlar. 

Bir rapor oluşturmak için rapor tanımı açın ve ardından araç çubuğundaki Oluştur düğmesini tıklatın. Rapor sırası durumu penceresini açılır ve raporunuzun sıradaki konumunu belirtir. Varsayılan olarak, oluşturulan rapor Web Görüntüleyicisi'nde açılır.
| ![Not](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Not")**Not**        |
|------------------------------------------------------------------------------------------------|
| Yalnızca erişim izni olan klasörlere ve konumlar için raporlar oluşturabilirsiniz. |

Aşağıdaki tablo, rapor oluşturmak için kullanabileceğiniz seçenekleri açıklar.

| Seçenek                                                                                | Daha fazla bilgi için |
|---------------------------------------------------------------------------------------|----------------------|
| Bir raporu veya rapor grubu otomatik olarak oluşturmak için bir zamanlama ayarlayın              |                      |
| Hesapları veya bir rapordaki verileri eksik olup olmadığını denetleyin ve raporun doğruluğunu doğrulayın |                      |

Bir rapor oluşturduğunuzda, Rapor tanımını sekmesinde belirlediğiniz seçenekleri kullanılır. Çıktı ve dağıtım sekmesi raporu paylaşmak için kolay bir yol sağlayan bir rapor kitaplığı konumu belirtmenize olanak sağlar.

## <a name="schedule-report-generation"></a>Zamanlama raporu oluşturma
Birçok şirket, iş süreçlerinin hizalamak için zamanlanmış aralıklarla çalıştırmak çekirdek raporlar kümesine sahiptir. Günlük, haftalık, aylık veya yıllık olarak düzenli olarak oluşturulması için bir rapor zamanlayabilirsiniz. Bu, tek bir rapor ya da birden çok şirket içeren raporlar grubu olabilir. Her bir raporlama ağacı tanımı içinde olanlar gibi, belirtilen her şirket için kimlik bilgilerinizi girmeniz gerekir. Kimlik bilgileri geçerli değil ise, rapor yalnızca zaman oturum açtığınız şirket gibi erişim izniniz olan bilgileri görüntüler. Çıkış bilgileri rapor grubundan ve tek tek raporlardan önce okunur.

Rapor zamanlamaları oluşturulurken ve kaydedilirken rapor zamanlamaları altındaki gezinti bölmesinde görüntülenir. Raporları düzenlemek için klasörler oluşturabilirsiniz. Zamanlama içindeki tek bir rapor çalışmıyorsa, tüm raporlar çalışmaya devam eder.
| ![Önemli](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Önemli")**Önemli**                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rapor gruplarını yaratma, değiştirme ve silme için tasarımcı veya yönetici rolüne sahip olmanız gerekir. Bir raporu çalıştırdığınızda, rapor üretmek için zamanlamayı oluşturan kullanıcının kimlik bilgileri kullanılır. |

### <a name="create-a-report-schedule"></a>Rapor zamanlaması oluştur

1.  Rapor Tasarımcısı'nda Dosya menüsünde Yeni seçeneğini tıklatın ve sonra Rapor zamanlaması seçeneğini seçin. Yeni Rapor Zamanlaması iletişim kutusu açılır.
2.  Ayarlar altında, tek bir raporu veya rapor grubunu zamanlamak için seçin. Yalnızca oturum açmış olduğunuz şirket veya yapı taşı seçimi için raporlar veya rapor grupları kullanılabilir.
3.  Rapor zamanlamasını açmak için etkin onay kutusunu seçin. Yalnızca rapor oluşturucu ya da bir yönetici rapor zamanlamasını etkinleştirebilir veya devre dışı bırakabilir.
4.  Şirketin kimlik bilgilerini girmek için izin düğmesini tıklatın. Varsayılan olarak, oturum açtığınız bir şirket için oturum açma bilgileriniz kullanılır. Raporlama ağacı tanımlarında olduğu gibi diğer şirketler dahilse, ayrı kimlik bilgilerini kullan'ı seçin ve ardından rapor zamanlamaya dahil herhangi bir şirket için kimlik bilgilerini girin. Windows kimlik doğrulaması seçebilir ya da her şirket için bir kullanıcı adı ve parola yazabilirsiniz. Bu şirketlerin kimlik bilgilerini kaydetmek için kimlik bilgileri kaydet onay kutusunu seçin ve ardından iletişim kutusunu kapatmak için Tamam'ı tıklatın.
5.  frekans altında, yineleme Başlat alanında, zaman çizelgesi başlatmak için tarih seçin. İstemci bilgisayarın geçerli sistem tarihi varsayılan olarak seçilidir.
6.  Raporu çalıştır alanında, raporun çalıştırılması gereken saati seçin. Geçerli sistem saatinden önce bir saat girerseniz, raporu sonraki zamanlanan tarihte çalışır.
7.  yineleme deseni alanınında, raporun ne sıklıkla çalıştırıldığını belirtin. Varsayılan olarak, Günlük bir aralık (gün) 1 değerine sahipse seçilir. Diğer seçenekler haftalık, aylık ve yıllıktır.
8.  yineleme aralığı alanında, oluşturulan raporun ne zamana durdurulması gerektiğini seçin.
    -   Bitiş tarihi yok – rapor zamanlaması sonsuza kadar çalışır.
    -   Yinelenme sayısını ayarlama – rapor zamanlamasını belirtilen sayıda çalışır ve sonra devre dışı bırakılır.
    -   Bitiş tarihi – rapor zamanlaması belirtilen tarihte sona erer.

9.  Araç çubuğunda Kaydet'i tıklatın. Farklı Kaydet iletişim kutusunda, benzersiz bir ad ve rapor zamanlaması için açıklama girin.

Rapor zamanlaması kopyalamak için tasarımcı veya yönetici rolüne sahip olmanız gerekir. Yönetici rapor zamanlamayı değiştirir olsa bile, rapor raporu oluşturan kullanıcının kimlik bilgilerini korur.
### <a name="copy-a-report-schedule"></a>Rapor zamanlaması kopyala

1.  Rapor Tasarımcısı'nda gezinti bölmesinde rapor zamanlamaları'nı tıklatın ve kopyalanacak bir rapor zamanlaması açın.
2.  dosya menüsünde Farklı Kaydet'i tıklatın ve Farklı Kaydet iletişim kutusuna zamanlama için yeni bir ad ve açıklama girin. Tamam'ı tıklatın ve yeni zamanlama Gezinti Bölmesi'nde görüntülenir.
3.  Yeni zamanlama içindeki alanları ve bilgileri gerektiği gibi değiştirin ve sonra araç çubuğu üzerindeki Kaydet'i tıklatın veya dosya menüsünde Kaydet'i tıklatın.

Rapor zamanlamasını silmek için rapor zamanlama sahibi olmanız veya yönetici rolünde olmanız gerekir.
### <a name="delete-a-report-schedule"></a>Rapor zamanlaması sil

1.  Rapor Tasarımcısı'nda gezinme bölmesinde Rapor Zamanlamaları seçeneğini tıklatın.
2.  Silinecek rapor zamanlamasını seçin ve sonra Sil'i tıklatın veya Sil tuşuna basın.
3.  Rapor zamanlamasını kalıcı olarak silmek için silme işlemini doğrulama iletişim kutusunda, Evet'i tıklatın. Zamanlamayı silmek için izniniz yoksa, bir ileti görüntülenir ve rapor silinmez.

### <a name="credentials-and-report-schedules"></a>Kimlik bilgileri ve rapor zamanlamaları

Raporlara dahil tüm şirketler için gereken kimlik bilgileri girmezseniz, rapor zamanlama kaydettiğinizde, aşağıdaki iletiyi alırsınız: "Bu rapor zamanlamasında yer alan şirketler için kimlik bilgilerinizi girmeniz gerekir. Kimlik bilgilerinizi girmek için izin düğmesini seçin."

Örneğin, Oğuz Şirket A için kullanıcı adı açma ve parola kullanarak oturum açar. Birden çok şirketten veri toplamak için bir raporlama ağaç tanımını kullanan bir rapor için bir zamanlama planı oluşturur. Bu rapor zamanlama kaydedildiğinde, Oğuz'un raporlama ağaç tanımında belirtilen diğer şirketler için kimlik bilgilerini girmesi istenir. Kimlik bilgileriniz zaman aşımına uğradığında, rapor zamanlamada etkilenen raporlar kimlik bilgilerini güncelleştirene kadar oluşturulmaz. Rapor sırasında izinlerin güncelleştirilmesi gerektiğini belirten bir ileti görüntülenir. Aşağıdaki senaryolardan biri oluşursa, rapor zamanlama başarısız olur (çünkü kimlik bilgileri gerektirir):
-   Yeni bir şirket, tek bir rapor için bir rapor ağacına eklendi.
-   Bir rapor rapor grubunda değiştirildi.
-   Ek bir şirket için yeni bir rapor bir rapor grubuna eklendi.

Devam etmek için izin düğmesini rapor zamanlama iletişim kutusunda tıklatın ve sonra uygun kimlik bilgilerini girin.

## <a name="missing-account-analysis-feature"></a>Hesap analiz özelliği eksik
Tüm satır tanımları, raporlama ağaç tanımları ve bir yapı taşı grubundaki rapor tanımı arasında eksik finansal hesaplar ve boyutlar için arama yapabilirsiniz. Bu kısa dönemde birkaç hesap veya yapı taşı oluşturduğunuzda veya güncellediğinizde ve tüm yeni bilgilerin raporlarınızda bulunduğunu doğrulamak istediğiniz zaman yararlıdır.

Eksik hesaplar en düşük ve en yüksek değerleri satır tanımını kullanılarak veya raporlama ağaç tanımından belirlenir ve daha sonra satır tanımı ya da raporlama ağaç tanımında olmayan, ancak mali verileri olan hesapların listesini görüntülenir. Eksik bir hesap satır tanımındaki değerlerden daha büyük veya daha küçük ise, o hesap eksik hesapları listesine dahil edilmez.
| ![İpucu](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "İpucu")**İpucu**                                             |
|----------------------------------------------------------------------------------------------------------------------------------|
| Doğrulama amacıyla, aylık raporlar oluşturmadan önce ve yeni yapı taşları oluşturduğunuzda, bu işlem çalıştırılmalıdır. |

Değer aralıkları olan raporların hesapları eksik olması olasılığı daha düşüktür. Mümkün olduğunda, aralıkları Yapı bloğu içinde oluşturuldukları sırada yeni hesaplar eklemek için kullanın. Hiçbir rapor tanımı, @ANY şirketi olarak ayarlanmamışsa, belirli bir şirkete oturum açın ve bu şirket için eksik bir hesap analizi çalıştırın.
| ![Not](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Not")**Not**                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Yeni bir şirket eklenmişse, yeni şirketi varolan tüm raporlarda raporlama ağaçlarına eklemeniz gerekir veya şirket eksik hesap analizine dahil edilmez. |

### <a name="run-missing-account-analysis"></a>Eksik hesap analizi çalıştır

1.  Rapor Tasarımcısı'nda Araçlar'ı tıklatın ve ardından Eksik Hesap Analiz'ini tıklatın.
2.  Şirket filtresi alanında, sonuçları veya seçmek filtrelemek için bir şirket seçin veya tüm kullanılabilir şirketlere ait sonuçları görüntülemek için tüm (filtre yok) seçeneğini seçin.
3.  boyut filtresi alanında, sonuçları filtrelenecek boyut seçin veya tüm kullanılabilir boyut bilgileri için boyut bilgilerini görüntülemek için tüm (filtre yok) seçeneğini seçin.
4.  grupla alanında, sonuçları sıralamak için bir seçenek belirleyin. Sonuçları etkilenen yapıtaşına göre sıralayabilir veya boyut ve değer kümelerine göre sonuçları sıralayabilirsiniz.
5.  Görüntülenen sonuçları gözden geçirin. Üst bölmede bir öğe seçtiğinizde, alt bölme istisna hakkındaki ek bilgileri görüntüler. Bu, ilgili boyutları, değerler ve raporları içerir.
6.  Etkilenen öğeyi açmak için liste bölmesinde görüntülenen ilişkili simgeyi tıklatın veya öğeyi sağ tıklatın ve açık'ı seçin. Birden çok öğe seçmek için alt bölmede öğeleri seçerken Ctrl tuşunu basılı tutun.
7.  Analize dahil edilmemesi gereken değerler, yapı taşları veya raporları döndürülürse, öğeyi sağ tıklatın ve Hariç Bırak'ı seçin veya listeden öğeyi kaldırmak için öğenin yanındaki hariç bırak onay kutusunu seçin. Liste yenilendiğinde, dışlanan öğeler dahil edilmez. Birden çok öğe seçmek için alt bölmede öğeleri seçerken Ctrl tuşunu basılı tutun. Analiz dışı bırakmak için daha önce seçtiğiniz herhangi bir sonuç da dahil olmak üzere tüm öğeleri görüntülemek için Dışarıda bırakılan yapı taşları ve değerleri göster onay kutusunu seçin ve ardından Yenile'yi tıklatın.
8.  Ele aldığınız özel durumları yenilemek için Yenile'yi tıklatın. Tüm sonuçların tam yenilemesini gerçekleştirmek içinEvet'i tıklatın veya ele alınmış maddelerin kısmi yenilemesini gerçekleştirmek için Hayır'ı tıklatın.
    | ![Not](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Not")**Not**                    |
    |------------------------------------------------------------------------------------------------------------|
    | Açıldığında, form son 15 dakika içinde açılmadığı sürece, form otomatik olarak yenilenir. |

9.  Sorunları çözülmüş olunca Tamam'ı tıklatarak iletişim kutusunu kapatın.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Eksik hesap analiz için klavye kısayolları
Eksik bir hesap analizini çalıştırdığınızda, aşağıdaki klavye kısayollarını kullanılabilir.

| Bunun için                           | Bu klavye kısayolunu kullanın |
|--------------------------------------|----------------------------|
| Şirkete göre filtre uygula                    | Alt+C                      |
| Boyuta göre filtre uygula                  | Alt+D                      |
| Grupla alanını seçin            | Alt+G                      |
| Dışlanan blokları ve değerleri göster      | Alt+S                      |
| Sonuçları yenile                      | Alt+R                      |
| Seçili yapı taşını dışla  | Alt+X                      |
| Seçilen satır tanımını dışla  | Ctrl+B                     |
| Seçili boyut değerini dışla | Ctrl+D                     |
| Seçilen rapor tanımını aç  | Ctrl+R                     |
| Seçilen satır tanımını aç     | Ctrl+O                     |

 
<a name="see-also"></a>Ayrıca bkz.
--------

[Mali raporlama](financial-reporting-intro.md)

[Rapor Tasarımcısı arayüzü](report-designer-interface.md)



