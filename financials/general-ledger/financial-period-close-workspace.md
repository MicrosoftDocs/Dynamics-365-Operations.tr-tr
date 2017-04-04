---
title: "Mali dönem kapatma çalışma alanı"
description: "Bu makale, Mali dönem kapanış çalışma alanı ve bununla ilişkili yapılandırma hakkında genel bir bakış sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ba0d709d123f56edb2a5287376c06c1f41181b1c
ms.lasthandoff: 03/31/2017


---

# <a name="financial-period-close-workspace"></a>Mali dönem kapatma çalışma alanı

Bu makale, Mali dönem kapanış çalışma alanı ve bununla ilişkili yapılandırma hakkında genel bir bakış sağlar.

Mali dönem kapatma çalışma alanı

**Yakın mali dönem** çalışma alanı şirketler, alanlar ve kişiler arasında mali kapanış işlemlerinizi izlemenize olanak sağlar. Görünümünüzü bağlı olarak **yakın mali dönem** çalışma alanı, ya da tüm görevleri ve kapanış tablosu veya yalnızca size atanan görevler için durumlarını göreceksiniz. 

İlk çalışma alanının üstünde bir kapanış tablosu seçmelisiniz. Çalışma alanında gösterilen tüm verilerin seçilen kapanış zamanlamaya göre sonra filtre.

### <a name="summary-tiles"></a>Özet kutucukları

**Özet** kutucukları sürece genel bakış sağlarken, göstergeler kapatma sürecini izlemenize yardımcı olur. Geçmiş Bugün, bugün dolan ancak bağımlılıkları nedeniyle engellenen görevler ve işlemin kalan tüm görevler için kalan görevler vadesi geçmiş olan görevleri görebilirsiniz. Seçili kapanış tablosu içinde bulunan tüm şirketler için bu bilgiler sağlar.

### <a name="tasks-and-status-section"></a>Görevler ve durum bölümü

İçinde **görevler ve durum** bölümünde, genel durumunu kapatma zamanlaması bölünmüş çeşitli şekillerde: Şirket, alana göre durumu ve sorumlu kişinin durumuna göre durumu. Kapanış tüm görevleri, bugün, son yalnızca görevleri zamanlamak için durumunu görüntüleyebilirsiniz veya görevleri vadesi geçmiş olan kart listenin üstündeki filtre değiştirerek. Şirket Filtresi, belirli bir şirkete durumunu görüntülemek için de seçebilirsiniz. Her durum sekmesi tamamlanan yüzdesi ve kalan görevlerin sayısını tarafından bir çözümlemesini verir. Kart'ı tıklatın veya **ayrıntıları görüntüle** tarafından seçilen kart ayrıntılı görev listesine filtre uygulamak için eylem. 

Son sekme için ayrıntılı görev listesi kullanılır. Bu liste yalnızca ilgilendiğiniz görevleri gösterir böylece süzülebilir ve tam görev listesini gösterir. Görev listesi, çeşitli şekillerde filtre uygulayabilirsiniz. Örneğin, son tarih, ilişkili şirket ve ilişkili alanı görev göre filtre uygulayabilirsiniz. Tamamlanmış görevleri görev listesinde gizlemek veya göstermek için de seçebilirsiniz. 

Görevler için iki gösterge kullanılır:

-   Ünlem işareti simgesi görev vadesi geçmiş olduğunu gösterir. Vadesi geçmiş görevler için son tarih de kırmızıyla vurgulanır.
-   Bir asma kilit simgesi görev henüz tamamlanmış değil diğer görevlere bağlı olduğunu gösterir. Bağımlılıklar tarafından engellenmiş olan bir görevi tamamlandı olarak işaretlenemez. Görev bağımlılıklarını kullanarak ayarlayabilirsiniz **bağımlılık ayarlamak** eylem.

Görev kullanıcı işi tamamlamak için nereye gitmeniz gerekir Microsoft Dynamics 365 işlemler sayfasına veya başka bir Web sayfası için köprü adıdır. Bu köprü kullanarak ayarlayabilirsiniz **görev bağlantısı** düzenlemek veya bir görev oluşturduğunuzda, alan. 

Kullanarak dosyaları, notlar, görüntüleri ve URL'leri göreve ekleyebilirsiniz **ek** eylem. Örneğin, bir görevin parçası olarak kullanılan günlük numaralarının göstermek, belirli bir görev hakkında açıklamalar eklemek veya yazdırılan rapor dosyası için bir görev eklemek. Bir simge görünür **ek** bir ek varsa, görev için sütun. 

**Görevi tamamlamak** seçeneğini el ile seçilmesi gerekir görev tamamlandıktan sonra. Görev tamamlandı olarak işaretlendiğinde **tamamlanan tarihi** alan geçerli tarih ve saati otomatik olarak güncelleştirilir. Bağımlılık göstergeler uygun şekilde güncelleştirilir.

## <a name="all-financial-period-close-tasks-list-page"></a>Tüm mali dönem kapatma görevleri liste sayfası
Tüm geçerli ve önceki dönem Kapat görevleri görüntüleyebilirsiniz **tüm mali dönem görevleri Kapat** listesi sayfası. Bu liste sayfası zamanlanmış hakkında bilgi içerdiği için en iyi, kapatma işleminin geçmiş çözümleme amacıyla kullanılır son tarih, gerçek tamamlanma tarihi ve kişinin görev tamamlandı. Bu liste sayfasında bilgileri raporlama ve denetim amacıyla kolayca Microsoft Excel'e verebilirsiniz.

## <a name="financial-period-close-configuration-page"></a>Mali dönem kapatma yapılandırması sayfası
Kullanabilmeniz için önce **yakın mali dönem** çalışma alanı kullanarak Microsoft Dynamics 365 işlemleri için de işlem yapılandırmalısınız **mali dönem kapatma yapılandırma** sayfa. (Tıklayın **genel muhasebe**&gt;**dönemi kapatmak**&gt;**mali dönem kapatma yapılandırma**.)

### <a name="resources"></a>Kaynaklar

Üzerinde **kaynakları** sekmesi, kapanış süreçlerle ilgili kişilerin belirleyin. Kapanış görev için sorumlu olacak bir çalışan ilk buraya atanmış olması gerekir. Çalışma alanı çalışanın görünümünü de belirtmeniz gerekir. Aşağıdaki seçenekler bulunur:

-   **Sadece atanan görevler** – Kullanıcı sadece kendisine atanmış olan görevleri görebilir.
-   **Tüm görevler ve durum** – Kullanıcı tüm kapanış görevlerini ve genel sürecin durumunu görebilir.

Sadece kendilerine atanan görevleri görüntüleme iznine sahip kullanıcılar görev listesine görev ekleyemez, görevleri düzenleyemez veya görev listesindeki görevleri kaldıramazlar.

### <a name="task-areas"></a>Görev alanları

Kapanış görevlerini organizasyonunuz içindeki mantıklı mülkiyet alanlarına gruplandırmak için görev alanlarını kullanırsınız. Örneğin, görev alanları olarak Borç hesapları, Alacak hesapları ve Genel muhasebe kullanılabilir.

### <a name="calendars"></a>Takvimler

Oluşturabilir ve kapanış mali takvimleri takvimler sekmesini kullanarak düzenleyebilirsiniz.  Burada, kapatma işlemleri için çalışma günlerini tanımlayacak ve kapanış görevleri zamanlamak için kullanılan budur.  Yeni bir takvim oluşturun ve görev zamanlamak için kullanılacak çalışma günleri gösterir.  Oluşturulduktan sonra düzenlenebilir beri uzun süre için bir yıl veya birden fazla yıl gibi bir takvim oluşturmak en iyisidir.  Takvim oluşturduktan sonra tatiller gibi belirli günler için takviminizi güncelleştirmek için Düzenle düğmesini tıklatın.  Denetim değeri açık olarak ayarlandığında günlerde görevleri kapatmaya planlanır.  Kapanış görevleri belirli bir tarihte zamanlama olmamalı, o gün kapalı olarak ayarlamak denetim değeri olması gerekir.

### <a name="templates"></a>Şablonlar

Kapatma işleminin bir parçası olan tüm görevleri tanımlamak için bir mali Kapat şablonu kullanın. Her kapatma işleminin bir parçası tamamlamak için birey için atanmış yinelenen bir çalışmalarında bir kapanış görevdir. Şablonda, göreli bir vade tarihi her kapatma görevi için tanımlanmalıdır. Göreli vade tarihidir önceki gün sayısı veya tanımlanan dönem bitiş tarihi sonra görevi her dönemin son olacaktır. Son bir saat de her göreve atanır. Son saat saat diliminizi bağlamı kullanılarak ayarlanır ve her kullanıcı için saat dilimi dönüştürülür. 

Bu görev nerede uygulanır bir veya daha fazla şirketler için şablon içinde bir görev atayabilirsiniz. Bu çalışmalarında her şirkette tamamlamak için farklı bir kişiye atadıysanız, birden çok görevi aynı çalışmalarında için oluşturmak yararlı. Her şirket için bir görev oluşturun. 

**Görev bağlantısı** menü öğesi görevi çalışmalarında ilişkilidir ve çalışma alanında görev bağlantısından ilişkili sayfaya doğrudan gitmek için kullanılabilir. Örneğin, para birimi yeniden değerleme işlemi Borç hesapları için kapanış görevi bağlı ilişkili için **yabancı para birimi yeniden değerleme** işlemleri için Microsoft Dynamics 365 sayfasında. Ayrıca, bir harici URL'ye de bağlayabilirsiniz. 

> [! İpucu] belirli bir yönetim Reporter rapor için mali dönem kapatma görevi bağlamak istiyorsanız, rapor URL'si kullanın. Rapor URL'ye erişmek için raporu Rapor Tasarımcısı içinde açın ve sonra **dosya**&gt;**raporu görüntülemek** raporu bir web tarayıcısında açmak için. Tarayıcının adres çubuğundaki URL'yi kopyalayabilir ve bunu **Görev bağlantısı** **URL** alanına yapıştırabilirsiniz. 

Görev bağımlılıkları şablonda tanımlayabilirsiniz. Bir görev için bir veya daha fazla görevlere bağlı ayarlanmış olması durumunda bu görev bağımlılıkları tamamlanana kadar tamamlandı olarak işaretlenemez. 

Birden fazla mali Kapat şablonları oluşturabilirsiniz. Daha sonra son ay veya yıl sonu gibi farklı dönem tipleri için kapanış işlemleri izlemek için veya farklı kapanış işlemleri kullanan şirketlerde izlemek için çeşitli şablonları kullanabilirsiniz. Bir şablon oluşturulduktan sonra yeni bir şablona kopyalayabilir ve gerekli değişiklikleri yapın. Her kapatma zamanlaması için tek bir şablon atayabilirsiniz.

### <a name="closing-schedules"></a>Kapanış planlamaları

Kapanış tablosu, kapalı gerekir belirli bir mali dönem için mali Kapat şablon atamak için kullanın. Şablonu görevlerinden sonra otomatik olarak belirli bir süre için oluşturulur ve yeni bir kapanış tablosu çalışma alanına eklenir. Yeni bir kapanış tablosu oluşturduğunuzda, **dönem bitiş tarihi** alanı fiili süre belirlemek için kullanılır göreli vade göre kapanışı görevlerin tarihlerini tarih mali Kapat şablonda atanır. 

Görev planlamada kullanılacak çalışma günleri belirtmek için kapanış tablosu için uygun takvimi atayın. Belirli bir takvim tanımlamazsanız, görev son tarihleri haftanın tüm günlerinin kullanın. 

Kapanış tablosu ile ilişkili şirketler de tanımlamanız gerekir. Birden çok şirket için şablon görevi atadıysanız, kapanış zamanlama ve şablon göreve atanan her şirket için ayrı görevler oluşturulur. 

Kapanış tablosu tamamlandıktan sonra seçin **kapalı** seçenek. Görev geçmişi hala kullanılabilir durumda **tüm mali dönemi kapatmak görevleri** listesi sayfası, ancak kapanış tablosu çalışma alanından kaldırılacak. Sonra bir kapatma zamanlaması olarak işaretlenmiş olan **kapalı**, görevler ekleyebilir, görevleri düzenleme veya görevleri kaldırmak mümkün olmayacaktır.


