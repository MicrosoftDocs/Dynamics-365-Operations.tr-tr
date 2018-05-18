---
title: "Mali dönem kapatma çalışma alanı"
description: "Bu makale, Mali dönem kapanış çalışma alanı ve bununla ilişkili yapılandırma hakkında genel bir bakış sağlar."
author: twheeloc
manager: AnnBe
ms.date: 11/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b999fd3c26304b81f24389a83faf73e1658c39b3
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="financial-period-close-workspace"></a>Mali dönem kapatma çalışma alanı

[!include [banner](../includes/banner.md)]

Bu makale, Mali dönem kapanış çalışma alanı ve bununla ilişkili yapılandırma hakkında genel bir bakış sağlar.

Mali dönem kapatma çalışma alanı

**Mali dönem kapaması** çalışma alanı, şirketler, bölgeler ve kişiler arasında finansal kapama işlemlerinizi takip etmenizi sağlar. **Mali dönem kapaması** çalışma alanınızın görünümüne bağlı olarak, bir kapama zamanlaması için tüm görevleri ve durumlar ya da sadece size atanmış olan görevleri görürsünüz. 

Önce çalışma alanının üstünden bir kapanış zaman çizelgesi seçmelisiniz. Çalışma alanında gösterilen tüm veriler daha sonra seçilen kapanış zaman çizelgesi ile filtrelenir.

### <a name="summary-tiles"></a>Özet kutucukları

**Özet** kutucuğu, işleme genel bir bakış ve kapanış işlemini yolunda tutmanıza yardımcı olacak göstergeler sağlar. Süresi dolmuş görevleri, bugün için kalan görevleri, bugün süresi dolan ancak bağımlılıklar yüzünden engellenmiş görevleri ve işlemin tüm kalan görevlerini görebilirsiniz. Bu bilgi, seçilen kapma zamanlama çizelgesine dahil tüm şirketler için geçerlidir.

### <a name="tasks-and-status-section"></a>Görevler ve durum bölümü

**Görev ve durum** bölümünde, genel kapanış zaman çizelgesi durumu, çeşitli şekillerde bölünmüştür: şirkete göre durum, bölgeye göre durum ve sorumlu kişiye göre durum. Kapanış zaman çizelgesi içindeki tüm görevlerin, yalnızca bugün süresi dolan görevleri veya süreleri dolmuş görevleri, kart listesinin üstündeki filtreyi değiştirerek durumunu görebilirsiniz. Belirli bir şirketin durumunu görüntülemek için şirket filtresini de seçebilirsiniz. Her durum sekmesi, hem tamamlanmış olan yüzde hem de kalan görevlerin sayısı hakkında bir çözümleme verir. Karta veya **Ayrıntıları görüntüle** eylemi üzerine tıklayarak ayrıntılı görev listesini, seçili karta göre filtreleyin. 

Son sekme, ayrıntılı görev listesi içindir. Liste, görev listesinin tamamını gösterir ve yalnızca ilgilendiğiniz görevleri göstermek üzere filtrelenebilir. Görev listesini çeşitli şekillerde filtrelenebilir. Görev filtresini örneğin, son tarih, ilişkili şirket ve ilişkili alanı göre uygulayabilirsiniz. Tamamlanmış görevleri, görev listesinde göstermeyi veya gizlemeyi de seçebilirsiniz. 

Görevler için iki gösterge kullanılır:

-   Bir ünlem, görevin süresinin geçmiş olduğunu belirtir. Tarihi geçmiş görevler için, vade dolumu ayrıca kırmızı olarak vurgulanır.
-   Bir asma kilit simgesi, görevin henüz tamamlanmamış başka görevlere bağlı olduğunu gösterir. Bağımlılıklar tarafından engellemiş olan bir görev, tamamlandı olarak işaretlenemez. **Bağımlılık ayarla** eylemini kullanarak bir görev için bağımlılıkları ayarlayabilirsiniz.

Görev adı, Microsoft Dynamics 365 for Operations sayfasına veya kullanıcının görevi tamamlamak için gitmesi gereken başka bir web sayfasına giden bir köprüdür. Bu köprüyü **Görev bağlantısı** alanını kullanarak bir görevi oluşturduğunuzda veya düzenlediğinizde ayarlayabilirsiniz. 

Dosyalar, notlar, resimler veya URL'leri bir göreve **Ekler** eylemini kullanarak ekleyebilirsiniz. Örneğin, bir görevin parçası olarak kullanılan günlük numaralarını gösterebilir, belirli bir görev hakkında yorumlar ekleyebilir veya bir görev için yazdırılmış bir rapor dosyasını ekleyebilirsiniz. Bir ek mevcutsa, **Ek** sütununda bir simge belirir. 

**Görev tamamlandı** seçeneği, görev tamamlandıktan sonra el ile seçilmek zorundadır. Bir görev, tamamlandı olarak işaretlendiğinde, **Tamamlandı tarihi** alanı otomatik olarak geçerli tarih ve saat ile güncelleştirilir. Bağımlılık göstergeleri de uygun şekilde güncelleştirilir.

## <a name="all-financial-period-close-tasks-list-page"></a>Tüm mali dönem kapatma görevleri liste sayfası
Geçerli ve önceki dönem kapanış görevlerini **Tüm mali dönem kapanış görevleri** liste sayfasında görüntüleyebilirsiniz. Liste sayfası, kapanış işlemlerinizin tarihi analizlerini görüntülemek için en iyi şekilde kullanılır çünkü zamanlanan bitiş tarihi, gerçek tamamlanma tarihi ve görevi tamamlayan kişi hakkında bilgi içerir. Bu liste sayfasındaki bilgiyi raporlama ve denetleme amaçları için Microsoft Excel'e kolayca aktarabilirsiniz.

## <a name="financial-period-close-configuration-page"></a>Mali dönem kapatma yapılandırması sayfası
**Mali dönem kapatma** çalışma alanını kullanmadan önce mutlaka Microsoft Dynamics 365 for Finance and Operations'ta **Mali dönem kapatma yapılandırması** sayfasını kullanarak süreci yapılandırmanız gerekir. (**Genel muhasebe** &gt; **Dönem kapanışı** &gt; **Mali dönem kapatma yapılandırması** öğelerini tıklayın.)

### <a name="resources"></a>Kaynaklar

**Kaynaklar** sekmesinde, kapanış işlemleriyle ilgili kişileri belirlersiniz. Bir kapanış görevinde sorumlu olacak herhangi bir personelin, öncelikle burada atanmış olması gerekir. Personelin çalışma alanı görünümünü de belirtmeniz gerekir. Aşağıdaki seçenekler bulunur:

-   **Sadece atanan görevler** – Kullanıcı sadece kendisine atanmış olan görevleri görebilir.
-   **Tüm görevler ve durum** – Kullanıcı tüm kapanış görevlerini ve genel sürecin durumunu görebilir.

Sadece kendilerine atanan görevleri görüntüleme iznine sahip kullanıcılar görev listesine görev ekleyemez, görevleri düzenleyemez veya görev listesindeki görevleri kaldıramazlar.

### <a name="task-areas"></a>Görev alanları

Kapanış görevlerini organizasyonunuz içindeki mantıklı mülkiyet alanlarına gruplandırmak için görev alanlarını kullanırsınız. Örneğin, görev alanları olarak Borç hesapları, Alacak hesapları ve Genel muhasebe kullanılabilir.

### <a name="calendars"></a>Takvimler

Takvimler sekmesini kullanarak mali kapanış takvimlerini oluşturabilir ve düzenleyebilirsiniz. Kapatma işlemleri için çalışma günlerini tanımlayabilir ve bunu kapanış görevlerini zamanlamak için de burayı kullanabilirsiniz.  Yeni bir takvim oluşturun ve görev zamanlama için kullanılacak çalışma günlerini belirtin.  Bir takvimi uzun bir dönem için oluşturmak, örneğin bir yıl veya birden fazla yıl gibi, en iyisidir çünkü oluşturulduktan sonra düzenlenebilir.  Bir takvim oluşturduktan sonra, takvimi örneğin tatiller gibi belirli günler için güncelleştirmek için Düzenle düğmesini tıklatın.  Kapanış görevleri, Denetim değerinin Açık olarak ayarlandığı günlerde zamanlanır.  Kapanış görevleri belirli bir güne zamanlanmayacaksa, o günün Denetim değeri Kapalı olarak ayarlanmalıdır.

### <a name="templates"></a>Şablonlar

Kapanış işleminin parçası olan görevleri belirlemek için bir mali kapanış şablonu kullanabilirsiniz. Bir kapanış görevi, her kapanış işlemini tamamlamak için bir kişiye atanmış, tekrar eden bir çalışma eforudur. Şablonda, göreceli bir vade tarihi her kapanış görevi için tanımlanmalıdır. Göreceli vade tarihi, her dönemde belirlenmiş dönem bitiş tarihinden önce veya sonra görevin vadesinin dolacağı günlerin sayısıdır. Bir vade tarihi ayrıca her göreve de atanır. Vade tarihi, saat diliminizin bağlamı kullanılarak ayarlanır ve her kullanıcı için saat dilimine dönüştürülür. 

Görevin uygulanacağı bir veya daha fazla şirkete bir görevi şablonda atayabilirsiniz. Her şirkette işi eforunu tamamlamak için farklı bir kişi atandıysa, aynı iş eforu için birden fazla görev oluşturmayı yararlı bulabilirsiniz. Her şirket için bir görev oluşturun. 

**Görev bağlantısı** menü öğesi görev eforuyla ilişkilidir ve çalışma alanındaki görev bağlantısından, ilişkili sayfaya doğrudan gitmek için kullanılabilir. Örneğin, Borç hesapları için para birimini yeniden değerleme işlemini gerçekleştirecek bir kapanış görevi, Microsoft Dynamics 365 for Finance and Operations içerisinde **Yabancı para birimi yeniden değerleme işlemi** sayfasında bağlanabilir. Ayrıca, bir harici URL'ye de bağlayabilirsiniz. 

> [!TIP]
> Bir mali dönem kapanış görevine belirli bir Yönetim Raporlayıcı raporu ilişkilendirmek istiyorsanız, rapor URL'si kullanabilirsiniz. Rapor URL'sine erişmek için raporu rapor tasarlayıcıda açın ve ardından raporu bir web tarayıcısında açmak için **Dosya** &gt; **Raporu göster** öğelerini tıklayın. Tarayıcının adres çubuğundaki URL'yi kopyalayabilir ve bunu **Görev bağlantısı** **URL** alanına yapıştırabilirsiniz. 

Görev bağımlılıklarını şablonda tanımlayabilirsiniz. Bir görev, bir ya da birden çok göreve bağlı olacak şekilde ayarlanmış ise, tüm bağımlılıkları tamamlanmış olarak işaretlenene kadar tamamlandı olarak işaretlenemez. 

Birden çok mali kapanış şablonu oluşturabilirsiniz. Daha sonra çeşitli şablonları, farklı dönem türleri için kapanış işlemlerini izlemek için kullanabilirsiniz; örneğin ay sonundan yıl sonuna veya farklı kapanış işlemleri kullanan şirketleri izlemek için. Bir şablon oluşturulduktan sonra, bunu yeni şablona kopyalayabilir ve gerekli değişiklikleri gerçekleştirebilirsiniz. Her bir kapanış zamanlamasına yalnızca bir şablon atayabilirsiniz.

### <a name="closing-schedules"></a>Kapanış planlamaları

Bir kapanış zamanlamasını, kapatılması gereken belirli bir mali döneme bir mali kapanış şablonu atamak için kullanabilirsiniz. Şablondan görevler daha sonra, belirtilen dönem için otomatik olarak oluşturulur ve yeni kapanış şablonu çalışma alanına eklenir. Yeni bir kapanış zamanlaması oluşturduğunuzda, **Dönem sonu tarihi** alanı, mali kapanış şablonu içerisinde atanmış vade dolum tarihine dayanarak, kapanış görevleri için gerçek bitiş tarihlerini belirlemek için kullanılır. 

Görev zamanlamasında kullanılan çalışma günlerini göstermek için kapanış zamanlamasına uygun takvimi atayın. Belirli bir takvimi atamazsanız, görev son tarihleri haftanın tüm günlerini kullanır. 

Kapanış zamanlaması ile ilişkilendirilecek şirketleri de tanımlamanız gerekir. Şablon görevleri birden fazla şirkete atanırsa, her ayrı görev, kapanış zamanlamasında bulunan ve şablon görevine atanmış her şirket için oluşturulur. 

Kapanış zamanlaması tamamlandıktan sonra, onun için **Kapalı** seçeneğini işaretleyin. Göre geçmişi hala **Tüm mali dönem kapanış görevleri** liste sayfasında kullanılabilir olacaktır, ancak kapanış zamanlaması, çalışma alanından kaldırılacaktır. Bir kapanış zamanlaması **Kapalı** olarak işaretlendikten sonra, buna görevler ekleyemez, görevleri düzenleyemez veya görevleri kaldıramazsınız.




