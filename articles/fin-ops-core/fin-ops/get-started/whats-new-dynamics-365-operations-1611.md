---
title: Dynamics 365 for Operations sürüm 1611'deki yenilikler veya değişiklikler (Kasım 2016)
description: Bu makalede, Dynamics 365 for Operations 1611 sürümündeki yeni veya değişen özellikler açıklanmaktadır.
author: sericks007
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 221294
ms.assetid: 357931ed-f843-4bf5-bc85-0da3de0619ec
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a6e9454baa33e37fe62db2b7bd39ff00891ff855
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905038"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-version-1611-november-2016"></a>Dynamics 365 for Operations sürüm 1611'deki yenilikler veya değişiklikler (Kasım 2016)

[!include [banner](../includes/banner.md)]

Bu makalede, Dynamics 365 for Operations 1611 sürümündeki yeni veya değişen özellikler açıklanmaktadır.

## <a name="cost-accounting"></a>Maliyet muhasebesi

<table>
<thead>
<tr>
<th>Yapabilecekleriniz</th>
<th>Bunun önemi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Maliyet öğesi boyutlarını tanımlayın ve maliyet öğesi boyut üyelerini içe aktarın.</td>
<td>Maliyet öğeleri, Maliyet muhasebesinde maliyetleri sınıflandırmak ve maliyetlerin akışını belgelemek için kullanılır. Birincil maliyet öğeleri, ana hesapları doğrudan Operations'dan almak için bir Microsoft Dynamics 365 for Operations veri bağlayıcısı kullanarak veya ana hesapları başka bir kaynak sistem türünden Microsoft Excel aracılığıyla aldığınız genel bir veri bağlayıcı kullanarak içe aktarılır. Ana hesaplar Maliyet muhasebesine içe aktarıldıktan sonra maliyet öğesi boyut üyeleri olarak kullanılır. İkincil maliyet öğeleri kullanıcı tarafından tanımlanır ve maliyetlerin akışını belgelemek üzere tahsisatlarda kullanılır.</td>
</tr>
<tr>
<td>Maliyet öğesi boyutlarını eşleyin.</td>
<td>Tüzel kişiliklerinizdeki ana hesaplar yasal muhasebe gereksinimleri gereği paylaşılamıyorsa kuruluşunuzun bütünsel bir görünümünü elde etmek için bu hesapları Maliyet muhasebesine içe aktardıktan sonra eşleyebilirsiniz.</td>
</tr>
<tr>
<td>Maliyet nesnesi boyutlarını tanımlayın ve maliyet nesnesi boyut üyelerini içe aktarın.</td>
<td>Maliyet nesneleri, maliyetlerin atandığı nesne türleridir. Maliyet nesneleri genellikle ürünleri, projeleri, kaynakları, departmanları, maliyet merkezlerini ve coğrafi bölgeleri içerir. Mali boyutları ve değerleri Operations'dan almak için bir Microsoft Dynamics 365 for Operations veri bağlayıcısı veya boyutları ve değerleri başka bir kaynak sistem türünden Excel aracılığıyla alabileceğiniz genel bir veri bağlayıcı kullanabilirsiniz. Örneğin, nesne boyutu olarak Maliyet merkezi mali boyutunu kullanırsanız içe aktarılan tüm maliyet merkezleri maliyet nesnesinin boyut üyeleridir.</td>
</tr>
<tr>
<td>İstatistiksel boyutları tanımlayın veya içe aktarın.</td>
<td>İstatistiksel boyut üyeleri makine saatleri, personel sayısı ve metrekare gibi parasal olmayan birimler cinsinden ölçülür. Bunlar raporlarda veya tahsisatların ve dağıtımların temeli olarak kullanılır.</td>
</tr>
<tr>
<td>İstatistiksel ölçü sağlayıcısı şablonları oluşturun.</td>
<td>İstatistiksel ölçü sağlayıcısı şablonu, Dynamics 365 for Operations verilerini istatistiksel ölçülere dönüştürmek için kullanılır. Şablon daha sonra belirli bir istatistiksel boyut üyesi ile ilişkilendirilir. Şablonlar yalnızca mali boyutlarla ilişkilendirilmiş tabloları gösterecek şekilde önceden filtrelenir.</td>
</tr>
<tr>
<td>Maliyet muhasebesi genel muhasebe defterleri oluşturun.</td>
<td>Maliyet muhasebesi genel muhasebe defteri kendi takvimini ve para birimini kullanan belirsiz bir defterdir. Tüm maliyet hareketlerinin işlenmesinde önemli bir rol oynar. Örneğin, bir maliyet muhasebesi genel muhasebe defteri, maliyetleri kendi maliyet öğelerine göre sınıflandırır ve maliyetleri kendi nesne boyutlarına göre toplar. Çeşitli açılardan yönetim raporlaması yapmak için ihtiyaç duyduğunuz sayıda maliyet muhasebesi genel muhasebe defteri oluşturabilirsiniz.</td>
</tr>
<tr>
<td>Maliyet kontrol birimleri oluşturun.</td>
<td>Maliyet kontrol birimleri, maliyet yapısını oluşturur ve bir maliyet muhasebesi genel muhasebe defterindeki maliyetlerin akışını tanımlar. Bunlar, defterdeki maliyet nesnesi boyutlarını temsil etmek üzere maliyet nesnesi boyutları ile ilişkilendirilmelidir.</td>
</tr>
<tr>
<td>Genel muhasebe girişlerini işleyin.</td>
<td>Fiili performansı ölçmek için verilere ihtiyacınız vardır. Veriler, maliyet muhasebesi genel muhasebe defteri için tanımladığınız bağlayıcılar kullanılarak içe aktarılır. Genel muhasebe girişlerini işlediğinizde veriler artımlı olarak içe aktarılır.</td>
</tr>
<tr>
<td>Bütçe girişlerini işleyin.</td>
<td>Bütçelenmiş performansı ölçmek için verilere ihtiyacınız vardır. Veriler, maliyet muhasebesi genel muhasebe defteri için tanımladığınız bağlayıcılar kullanılarak içe aktarılır. Bütçe girişlerini işlediğinizde, veriler artımlı olarak içe aktarılır.</td>
</tr>
<tr>
<td>Maliyet davranış ilkeleri oluşturun ve uygulayın.</td>
<td>Maliyetleri sabit, değişken veya yarı değişken olarak sınıflandırmak için bir maliyet davranış ilkesi kullanırsınız. İlke kural tabanlıdır ve belirli bir tarihte yürürlüğe girer. Varsayılan olarak, siz bir maliyet davranış ilkesi uygulayana ve kuralın etkilerini hesaplayana kadar tüm maliyetler sınıflandırılmamış olarak işaretlenir. Hesaplamadan sonra tüm maliyetler sınıflandırılır.</td>
</tr>
<tr>
<td>Maliyetleri izleyin.</td>
<td>Maliyet ilkelerinin etkisini anlamanıza yardımcı olmak için, Maliyet muhasebesi maliyetleri kaynak değerlere ve oluşturuldukları geçerli kurallara kadar izlemenize olanak tanır. Bu işlev, maliyetlerin oluştuğu zaman, oluşan maliyet türleri ve uygulanan maliyet davranış kuralları hakkında tam izlenebilirlik sağlar.</td>
</tr>
<tr>
<td>Boyut hiyerarşileri tanımlayın.</td>
<td>Kategorilere ayırma veya sınıflandırma amacıyla boyut hiyerarşileri oluşturabilirsiniz. Örneğin, bir maliyet öğesi boyutunu ve bunun üyelerini temel alan bir kümeleme hiyerarşisi tanımlayabilirsiniz. Alternatif olarak, bir maliyet nesnesi boyutunu ve bunun üyelerini temel alan bir sınıflandırma hiyerarşisi tanımlayabilirsiniz. Raporlama yapıları aşağıdaki durumlarda kullanılır:
<ul>
<li>Tahsisatları, maliyet oranlarını ve maliyet yuvarlama kurallarını tanımladığınızda.</li>
<li>Ekstreleri çalışma alanını kullanarak görüntülediğinizde.</li>
<li>Toplanan verileri görüntülemek için erişim tanımladığınızda.</li>
<li>Verileri Excel'de görüntülediğinizde.</li>
</ul></td>
</tr>
<tr>
<td>Çalışma alanında görüntülenebilen ekstreler oluşturun.</td>
<td>Sapmaların yanı sıra, fiili ve bütçelenmiş maliyetlere hızlı bir genel bakış almak için çalışma alanını kullanın. Verilere döneme veya maliyet düzeyine göre filtre uygulayabilirsiniz. Çalışma alanı, maliyet kontrolünden sorumlu yöneticiler için tasarlanmıştır. Çalışma alanı, boyut hiyerarşileri için tanımlanmış erişim kurallarına uyar.</td>
</tr>
<tr>
<td>Excel kullanarak rapor oluşturun.
<blockquote>[!NOTE] Microsoft Excel 2016 çalıştırmanız lazım.</blockquote>
</td>
<td>Maliyet muhasebesi verilerini veri varlıkları üzerinden doğrudan Excel'e dışa aktarabilir ve raporları oluşturmak için Microsoft PivotTable'ı kullanabilirsiniz.</td>
</tr>
</tbody>
</table>

## <a name="expense-management"></a>Gider yönetimi

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| İşten çıkarılan personelin kredi kartı hareketlerini yeniden atayın. | Bazen, bir personel işten çıkarıldığında, harcanması gereken etkin kredi kartı hareketleri içe aktarılırsa bu personelin Active Directory Domain Services (AD DS) hesabı devre dışı bırakılır. Önceden, gider girişi için bir temsilci atayabilir veya kredi kartı hareketlerini bir gider raporuna ekleyebilirdiniz. Artık ilişkili personelin işten çıkarıldığı her türlü kredi kartı hareketi için personeli yeniden atamak üzere, **Kredi kartı hareketleri** sayfasını kullanabilirsiniz. Kredi kartı hareketini yeniden atadıktan sonra, hareket bir gider raporu için seçilebilir ve gider raporu geri ödemeleri için uygulanan normal işlemlerle ödenebilir. |
| Bekleyen ve eski personel için gider kredi kartı bilgilerini değiştirin. | Bekleyen çalışanlar ve eski çalışanlar için gider yönetimi kredi kartı bilgilerini değiştirebilirsiniz. Önceden, gider kredi kartı bilgilerini yalnızca çalışan etkin bir personelse değiştirebilirdiniz. |
| Gider raporunu kopyalayın. | Artık aynı gider raporunda yeni bir gider oluşturduğunuzda mevcut bir gideri kopyalayabilirsiniz. Gider raporunu ve kredi kartı harici tüm ilişkili giderleri yeni bir gider raporuna kopyalayabilirsiniz. Yine de tanımlanan gider ilkelerine ve kategorilerine göre, tüm gerekli dökümleri gerçekleştirmeniz ve gerekli girişleri eklemeniz gerekir. Kredi kartı hareketlerini gider raporuna eklemek için mutabakata varılmamış gider eklemeyi seçebilirsiniz. |
| Giderleri toplu düzenleyin. | Bazı kredi kartı hareketleri bir gider kategorisine eşlenmemiş veya içe aktarıldıklarında hatalı olarak eşlenmiş olabilir. Bu durumda, personelin ilişkili gider kategorisini el ile değiştirmesi gerekir. Artık mutabakat sağlanmamış giderleri yönetirken, seçili giderler için gider kategorisini toplu düzenleyebilirsiniz. Ayrıca belirli bir gider raporu için seçili giderleri yönetirken, projeyi ve ek bilgileri de toplu düzenleyebilirsiniz. |
| Kredi kartı hareketleri için döviz kurunu değiştirin. | Kredi kartı hareketi için kullanılan fiili döviz kuru, sistemde ayarlanan döviz kurundan farklı olabilir. Önceden, personel Gider yönetimine içe aktarılan kredi kartı hareketleri için döviz kurunu değiştiremiyordu. Artık, **Gider yönetimi parametreleri** sayfasından bir parametre ayarlayarak kredi kartı hareketleri için döviz kurunun değiştirilebilmesine izin verebilirsiniz. |
| Giderler için yolsuzlukla mücadele onayını ayarlayın. | Kuruluşun bazı çalışanları kamu görevlileriyle çalışabilir ve bu işlerin bir parçası olarak ortaya çıkan bazı giderler rüşvet olarak algılanabilir. Gider yönetiminde, yemek ve hediyeler gibi seçili gider kategorileri için artık gösterilen bir yolsuzlukla mücadele onayı ayarlayabilirsiniz. Personel, yolsuzlukla mücadele onayı için ayarlanan giderlerin kuruluşunuzun ilkeleri tarafından tanımlanan ölçütleri karşılayıp karşılamadığını seçmelidir. |
| Belirli gider kategorileri için giderlerin el ile girilmesini önleyin. | Gider kategorisi kategorinin değiştirilemediği bir kredi kartı hareketini temsil etmek üzere ayarlanabilir. Kredi kartının geç ödenmesinden doğan ücret buna bir örnektir. Artık, giderlerin yalnızca içe aktarma yoluyla oluşturulmasına izin veren bir gider kategorisi ayarlayabilirsiniz. Bu özellik, personelin kategori için el ile bir gider oluşturmasını önler. Ayrıca içe aktarılan ve bu kategoriyi kullanan hareketler için kategorinin değiştirilmesine de izin vermez. |
| Girişi birden fazla gidere ekleyin. | Gider yönetimine yüklenen bir giriş birden fazla giderle ilgili olabilir. Önceden, birden fazla giderle ilgili olan bir girişin her gider için bir kere yüklenmesi gerekiyordu. Artık, bir girişi yüklenmiş ve aynı gider raporunda başka bir gidere eklenmiş olan bir gidere ekleyebilirsiniz. Ayrıca bir girişi gider raporunun başlığına yüklerseniz girişi eklemek üzere bir veya daha fazla satır seçebilirsiniz. |
| İleri tarihli giderler oluşturun. | Gider raporunu kopyaladığınızda, örneğin bir giderin hareket tarihi, ileri tarihli olabilir. Önceki sürümler ileri tarihli giderlere izin vermez. Artık, ileri tarihi olan giderler oluşturabilir ve kaydedebilirsiniz. Ancak ileri tarihli bir gider gönderemezsiniz. |
| Eyalet/il için gider vergilerini yapılandırın. | Bazı ülkelerde/bölgelerde, farklı eyaletlerde/illerde oluşan giderler farklı satış vergisi oranlarına tabi olabilir. Artık gider vergisi yapılandırmalarını yalnızca ülke/bölge düzeyinde değil, eyalet/il düzeyinde ayarlayabilirsiniz. **Vergi yapılandırması** sayfasında **Eyalet/İl** alanını boş bırakırsanız satış vergisi grubu belirtilen ülkedeki/bölgedeki tüm eyaletler/iller için uygulanır. |
| Gider kredi kartı türlerini ayarlayın. | Önceden, Gider yönetiminde kullanılabilecek Visa, MasterCard veya AMEX gibi yeni kredi kartı türleri oluşturabileceğiniz bir sayfa yoktu. Artık, Gider yönetiminde kullanmak üzere kredi kartı türleri oluşturabilirsiniz. Sayfa, **Hesaplamalar ve kodlar** bölümündeki **Kurulum** alanında yer alır. |
| Gider raporları için çok düzeyli onay iş akışı tanımlayın. | Gider raporları için yeni bir iş akışı çok düzeyli onay işlemini destekler. Personel gider raporunu oluşturduğunda, ara onaylayanları ve son onaylayanları girer. Daha sonra, iş akışı gider raporunu öncelikle ara onaylayanlara yönlendirir. Gider raporu bu düzeyde onaylandıktan sonra, iş akışı raporu son onay için son onaylayanlara yönlendirir. |
| Gider raporuna eklenmemiş giderler oluşturun ve yönetin. | Artık, kullanıcı önce bir gider raporu oluşturmak zorunda kalmadan (örneğin girişleri ekleyerek veya döküm alarak veya konuk atayarak) giderleri oluşturabilir ve yönetebilir. Bir veya daha fazla gider seçilip yeni bir gider raporuna eklenebilir ve onay için gönderilebilir. Giderlerin yönetilebildiği yeni bir sayfa **Gider yönetimi** &gt; **Giderlerim** &gt; **Giderler** yolunda bulunabilir. |

## <a name="financial-management"></a>Mali yönetim

<table>
<thead>
<tr>
<th>Yapabilecekleriniz</th>
<th>Bunun önemi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sabit kıymet değerlemelerini tek bir "defter" kavramıyla izleyin.</td>
<td>Önceden, sabit kıymet değerlerini izlemek için, değer modelleri ve amortisman defterleri olmak üzere iki ayrı değerleme türü kullanılıyordu. Geçerli sürümde, bu iki kavram defterler adı verilen tek bir değerleme kavramında birleştirildi. Defterler, değer modellerinin ve amortisman defterlerinin tüm işlevlerine sahiptir. Örneğin genel muhasebeye nakli devre dışı bırakabilirsiniz. Genel muhasebeye nakledilen defterler genellikle kurumsal mali raporlama amacıyla kullanılır. Genel muhasebeye nakledilmeyen defterler vergi raporlama amacıyla kullanılabilir.</td>
</tr>
<tr>
<td>Birden fazla tüzel kişilik için Genel muhasebe yıl sonu kapanışı gerçekleştirin.</td>
<td>Yıl sonu kapanışı işlemini hızlandırmak için artık yıl sonu kapanışını paylaşılan bir yıl sonu kapanış sayfasından birden fazla tüzel kişilik için çalıştırabilirsiniz. Bir yıldan sonrakine aktarılacak ayarlara sahip tüzel kişilik grupları tanımlanabilir. Yıl sonu kapanış işleminde başka kullanılabilirlik geliştirmeleri de yapılmıştır.</td>
</tr>
<tr>
<td>Genel muhasebe yabancı para birimi yeniden değerleme işlemi geliştirmelerinden yararlanın.</td>
<td>Yabancı para birimi yeniden değerleme işlemi için Genel muhasebe işlemine aşağıdaki geliştirmeler yapılmıştır:
<ul>
<li>Ana hesaba bir döviz kuru türü eklenmiştir. Şimdi bu döviz kuru türü, para birimi değerleme işlemi sırasında döviz kurunu belirlemek için kullanılır. Döviz kuru türü tanımlanmadıysa işlem genel muhasebede tanımlanan döviz kuru türünü kullanmaya devam eder.</li>
<li>Şimdi değerleme işlemini çalıştırmak için bir ana hesap ve para birimi aralığı seçmek daha kolaydır.</li>
<li>Birden fazla tüzel kişilik için yeniden değerleme çalıştırılabilir.</li>
<li>Şimdi sistem, Alacak hesapları (AR) ve Borç hesapları (AP) yeniden değerleme işlemlerinde olduğu gibi, gerçekleştirilen her yeniden değerleme işleminin geçmişini tutar.</li>
<li>Artık işlemi çalıştırdığınızda, yeniden değerlemenin sonuçlarını önizleyebilirsiniz. Önizleme, işlemin çalıştırıldığı tüm tüzel kişilikler için olan sonuçları gösterir. Daha sonra tüm tüzel kişilikleri veya bunların bir alt kümesini önizlemeden deftere nakledebilirsiniz. Önizlemede sonuçları Excel'e de dışa aktarabilirsiniz.</li>
</ul></td>
</tr>
<tr>
<td>Ek deftere nakil katmanları için hareketleri görüntüleyin.</td>
<td>Artık, <strong>Mizan</strong> liste sayfasında ve <strong>Boyut ekstresi</strong> raporunda, Genel muhasebeye eklenmiş olan ek deftere nakil katmanlarını seçebilirsiniz. Ek deftere nakil katmanlarını seçtiğinizde, bu deftere nakil katmanlarında yapılan düzeltmeler liste sayfasında veya rapordaki bakiyelere dahil edilir.</td>
</tr>
<tr>
<td>Nasıl yapılır belgelerini mali dönem kapatma şablonuna ekleyin.</td>
<td>Önceden, belgeleri bir görev tamamlandıktan sonra ekleyebiliyordunuz. Örneğin, oluşturulan bir raporu ekleyebilirdiniz. Artık, şablona bir nasıl yapılır belgesi de ekleyebilirsiniz. Bu nasıl yapılır belgesi daha sonra, mali dönem takvimindeki her göreve kopyalanır ve görev sahibinin görevin nasıl tamamlanacağına ilişkin yönergeleri görüntülemesi sağlanır.</td>
</tr>
<tr>
<td>Şirketlerarası muhasebe kurulumunu paylaşılan bir sayfadan tanımlayın.</td>
<td><strong>Şirketlerarası muhasebe kurulumu sayfası</strong> artık paylaşılmaktadır, böylece bir kuruluş birbiriyle işlem gerçekleştirebilen tüm tüzel kişilik çiftlerini tanımlayabilir. Artık bir hareketi ayrıca kaynak tüzel kişiliğe girebilir ancak hedef tüzel kişiliğe giremezsiniz. İki tüzel kişilik de şirketlerarası bir hareket başlatabiliyorsa karşılıklı çift tanımlanmalıdır. Bu nedenle, hedef tüzel kişilik de kaynak tüzel kişilik olarak ayarlanır.</td>
</tr>
<tr>
<td>Bütçe planları için gerekçe belgelerini gönderin.</td>
<td>İstenen tüm bütçe tutarları için tamamlayıcı belge olarak bir gerekçe şablonu oluşturabilirsiniz. Kullanıcılar şablonun ayrıntılarını doldurabilir ve şablonu bütçe planına ekleyebilir. Böylece, şablon onay işlemi sırasında kullanılabilir.</td>
</tr>
<tr>
<td>Bütçe kayıt girişleri için gelişmiş kuralları etkinleştirin.</td>
<td>Gelişmiş kurallar Genel muhasebede yapılandırılırsa bu kurallar bütçe kayıtlarındaki yeni girişler ve transferler için kullanılabilir.</td>
</tr>
<tr>
<td>Ön ödeme faturalandırma etkinliğinin gelişmiş görünürlüğünden yararlanın.</td>
<td>Yeni bir <strong>Açık ön ödemeler</strong> liste sayfası ön ödeme faturalandırma etkinliğinin durumuna ait bir anlık görüntü sunar. Sayfa, AP departmanına faturalandırılması gereken kalan ön ödeme değerlerine sahip satınalma siparişleri, ödenmesi gereken faturalandırılmış değerler ve standart faturalara uygulanması gereken ödenmiş fatura değerleri hakkında bilgiler sağlar. Ayrıca, ödenmiş ön ödeme faturalarının standart faturalara otomatik olarak uygulanmasına yönelik geliştirmeler, faturalandırma memurlarının veri girişini daha etkin bir şekilde yapmasına yardımcı olur.</td>
</tr>
<tr>
<td><strong>Satıcı iş birliği faturalama</strong> çalışma alanını kullanın.</td>
<td><strong>Satıcı iş birliği</strong> alanındaki yeni <strong>Faturalama</strong> çalışma alanı harici satıcıların kendi fatura bilgilerine güvenle erişmesini sağlar. Örneğin, satıcılar bir faturanın ödenip ödenmediğini görebilir ve kendi faturalarını gönderebilir. Bu değişiklik, harici satıcılarla daha verimli ve zamanında iletişimi teşvik eder. Bu nedenle, faturalama memurları fazla kesintiye uğramaz.</td>
</tr>
<tr>
<td>Fatura girişi sırasında tüzel kişilikleri değiştirin.</td>
<td>Geliştirmeler birden fazla tüzel kişilik için fatura girmesi gereken faturalama memurlarının tüzel kişiliği hızlı bir şekilde değiştirmelerine olanak tanır. Geçerli tüzel kişiliğin oturumunu kapatıp farklı bir tüzel kişilikte oturum açmak zorunda olmadıkları için bu özellik faturalama memurlarına zaman kazandırır. Hem <strong>Genel fatura günlüğü</strong> sayfası hem de <strong>Satıcı faturaları</strong> sayfası kullanıcıların veri girişi sırasında tüzel kişiliği değiştirmesine olanak tanır.</td>
</tr>
<tr>
<td>İç Gelir Servisi (IRS) 1099 Birleştirilmiş Federal/Eyalet dosyalama programı için elektronik dosya desteği</td>
<td><strong>ABD</strong> konfigürasyon anahtarı etkinleştirildiğinde, 1099 elektronik dosyalama işlemi Birleştirilmiş Federal/Eyalet dosyalama programına ilişkin IRS düzenlemelerine uyumlu ek işlevler sunar. IRS bu programı, katılımcı eyaletlere bilgi dönüşlerini elektronik olarak yönlendirebilmek için kurmuştur.</td>
</tr>
<tr>
<td>Kapatma geliştirmeleri</td>
<td>Geliştirmeler, ödeme memurlarının birden fazla deftere nakledilmemiş ödemenin aynı fatura için kapatılmasına izin vermesini sağlayarak, memurların kapatmaları daha etkin biçimde gerçekleştirmesine yardımcı olur.</td>
</tr>
<tr>
<td>Şirketler arası görünüm</td>
<td>Merkezi ödeme memurları artık şirketler arasında vadesi geçen faturaları görüntüleyebilir. <strong>Satıcı ödemeleri</strong> ve <strong>Müşteri ödemeleri</strong> çalışma alanları şimdi merkezi ödeme kurumsal hiyerarşisinin bir parçası olan şirketler arasında görüntüleme ve filtreleme yapmanın bir yolunu sunarak vadesi geçmiş faturalar için daha iyi görünürlük ve denetim sağlar.</td>
</tr>
<tr>
<td><strong>Banka yönetimi</strong> çalışma alanını kullanın.</td>
<td>Yeni bir <strong>Banka yönetimi</strong> çalışma alanı, tüzel kişiliklerinizin banka hesaplarını ve bakiyelerini izlemeye yardımcı olur. Cari bilançolar ve beklemedeki bakiyeler tüm hesaplar için hemen kullanılabilir ve bakiyelerden ayrıntılı hareket fişlerine geri ayrıntılandırma yapabilirsiniz. Ayrıca her banka hesabının geçmiş bakiye verilerini veya şirketteki tüm banka hesaplarının bir özetini kısa ve uzun dönem görünümlerinde görebilirsiniz. Her banka hesabı için son mutabakat tarihi bildirildiğinden, banka hesabı mutabakatı hakkında daha iyi öngörüler elde edebilirsiniz. Ayrıca, işlemde olan mutabakatlar için de bir gösterge bulunur.</td>
</tr>
<tr>
<td>Tüm tüzel kişiliklerin elektronik banka ekstrelerini tek bir adımda içe aktarın.</td>
<td>Artık, tüm tüzel kişiliklerin elektronik banka ekstrelerini tek bir adımda içe aktarabilirsiniz. Banka ekstresi dosyaları çok sayıda banka hesabına ve tüzel kişiliğe ait ekstreleri içerebilir ve zip dosyaları da çok sayıda banka ekstresi dosyası içerebilir. Tek bir içe aktarma işlemi kullanarak, tüm tüzel kişiliklerdeki bildirilen tüm banka hesapları için mutabakat başlatabilirsiniz. Bu özellik, şirketler ve çok sayıda ekstre içe aktarma işlemi arasında geçiş yapmak zorunda kalmayacağınız için zaman kazanabilirsiniz. Ayrıca, her şirkette içe aktarılan tüm ekstreler için eşleşen kuralları otomatik olarak çalıştırabilirsiniz.</td>
</tr>
<tr>
<td>Değerleme izleme</td>
<td>Tek bir sabit kıymet farklı muhasebe standartları için çok sayıda değerlemeye sahip olabilir ve isteğe bağlı olarak ilişkili hareketleri genel muhasebeye nakledebilir. Önceden, bu değerlemeler değer modelleri veya amortisman defterleri kullanarak izleniyordu. Artık defterler olarak bilinen bu değerlemeleri günlükler, sorgular ve raporlardan oluşan tek bir ortak kümeyi kullanarak izleyebilirsiniz. Birleştirilmiş deneyim uygulamayı basitleştirir ve dönemsel işlemlerin gerektirdiği arabirimlerin sayısını azaltır.</td>
</tr>
<tr>
<td>Şirketler arası amortisman çalıştırmaları geliştirmelerinden yararlanın.</td>
<td>Artık, tüm tüzel kişiliklerin kıymetleri için bir amortisman çalıştırmasını tek bir sayfadan başlatabilirsiniz. Ayrıca günlükler oluşturulduktan sonra bunları otomatik olarak nakledebilirsiniz. Günlükleri oluşturma ve nakletme işlemlerini toplu işlemeye gönderebilir ve amortismanın arka planda çalışmasını sağlayabilirsiniz. Bu geliştirmelerle, her şirket için ayrı ayrı amortisman çalıştırması başlatmak zorunda kalmayacağınız için verimsizlikler azalır. Bu geliştirme sabit kıymetlerinizin merkezi yönetimini de iyileştirir.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>İnsan sermayesi yönetimi

<table>
<thead>
<tr>
<th>Yapabilecekleriniz</th>
<th>Bunun önemi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Performans günlüğü oluşturun.</td>
<td>Gözden geçirmenizi tamamlamadan önce, genellikle, gözden geçirme dönemi boyunca bir personel olarak başarınıza katkıda bulunan etkinlikler veya olaylar hakkında bilgi toplarsınız. Bu etkinlikleri ve olayları belgelemek için performans günlüğünüze bir giriş ekleyebilirsiniz. Ayrıca, gözden geçirene daha fazla bilgi sunmak için bu etkinlikleri ve olayları bir hedef veya performans gözden geçirmesine de bağlayabilirsiniz.</td>
</tr>
<tr>
<td>Daha ayrıntılı hedefler oluşturun.</td>
<td>Ayarladığınız hedeflerin içerikleri üzerinde daha fazla denetime sahipsiniz. Hedefler için ölçümler oluşturabilir, performans günlüğü girişlerini ölçümlere bağlayabilir ve belge ekleyip görüntüleyebilirsiniz. Hedefleri şablonlar olarak saklayabilir ve hızlı kurulum için yeniden kullanabilirsiniz.</td>
</tr>
<tr>
<td>Daha ayrıntılı performans gözden geçirmeleri oluşturun.</td>
<td>Önceden tartışmalar olarak bilinen performans gözden geçirmeleri artık, sürekli geri bildirimi ve daha resmi gözden geçirmeleri destekleyecek kadar esnektir. Etkin hedefleri alabilir ve bunlar hakkında yorumlar gönderebilir ve uzmanlıklarınızın gözden geçirilmesi için bölümler ekleyebilirsiniz. Gözden geçirme ile ilgili ölçümleri, performans günlüğü girişlerini, ekleri ve kapatmaları ekleyip görüntüleyebileceğiniz ek bölümler sağlanmıştır.</td>
</tr>
<tr>
<td>Ek pozisyon hiyerarşilerini iş akışlarıyla ilişkilendirin.</td>
<td>İş akışını bir pozisyon hiyerarşisiyle ilişkilendirebilirsiniz. Ayrıca iş gereksinimlerinize uyması için onay işlemini en iyi hale getirecek şekilde iş akışı adımlarını değiştirebilirsiniz. Böylece, kuruluşunuzun kullandığı çeşitli raporlama ilişkilerine uyan etkin bir onay yapısı tanımlayabilirsiniz.</td>
</tr>
<tr>
<td>Personel self servisinde kişisel kimlik numaralarını (PIN) girmek için iş akışı desteği.</td>
<td>İnsan kaynaklarının (İK) iş akışı becerileri genişletilmiştir ve artık PIN desteğini de içermektedir. Personel, verimliliği artırmak için PIN'lerini ekleyebilir ve düzenleyebilir. Ancak, İK çalışanları bu bilgileri personelin kaydına eklemeden önce doğru ve eksiksiz olduklarından emin olmak için gözden geçirebilir.</td>
</tr>
<tr>
<td>Hedef şablonları oluşturun ve bunları yeni hedefler eklemek için kullanın.</td>
<td>Şirketteki pek çok personel tarafından paylaşılan hedefler için hedef şablonları oluşturabilirsiniz. Personel bir şablondan kendi hedeflerini ekleyebilir, yöneticiler ekipleri için bir şablondan hedef ekleyebilir ve İK ekibi üyeleri de şirketteki personel için hedefler ekleyebilir.</td>
</tr>
<tr>
<td>Hedef grupları oluşturun ve bunları yeni hedefler eklemek için kullanın.</td>
<td>Hedef şablonlarını bir gruba ekleyebilir ve bir personel, ekip, pozisyon, departman veya şirket için bir veya daha fazla hedef oluşturmak için grubu kullanabilirsiniz.</td>
</tr>
<tr>
<td>Gözden geçirme süreci üzerinde daha fazla denetim sahibi olun.</td>
<td>Gözden geçirme sürecini denetlemek için bir iş akışı kullanabilirsiniz. Gözden geçirme şablonları oluşturabilir ve bunları gözden geçirmeler oluşturmak için kullanabilirsiniz. Ayrıca bir gözden geçirmeye derecelendirme de ekleyebilirsiniz.</td>
</tr>
<tr>
<td>Gözden geçirmenin zaman dilimini tanımlamak için gözden geçirme dönemlerini kullanın.</td>
<td>Performans gözden geçirmesi için bir zaman dilimi tanımlayabilirsiniz. Gözden geçirmenin başlangıç ve bitiş tarihleri otomatik olarak girilir. Bununla birlikte, bu varsayılan tarihleri gerektiği şekilde değiştirebilirsiniz.</td>
</tr>
<tr>
<td>İnsan kaynakları için beş yeni Power BI içerik paketine erişim</td>
<td>Yeni içerik paketi, insan kaynakları kuruluşunun ve insan kaynakları yöneticilerinin aşağıdakileri analiz etmesine olanak tanır:
<p>İş gücü ölçümleri</p>
<ul>
<li>Nüfus niteliklerini yaş, cinsiyet ve Medeni durum dökümüne</li>
<li>Yıpranma oranlarını yıllar arasında karşılaştırma ve personellerin kuruluştan ayrılma sebeplerinin bir listesini görüntüleme</li>
<li>Açık pozisyonların listesini görüntülemek ve açıktan kapanan pozisyonların karşılaştırması</li>
</ul>
<p>Ücret ve kazançlar</p>
<ul>
<li>Saatlik ve Ücretli Çalışanlar Karşılaştır</li>
<li>Kullanılabilir kazançlara kaydedilmiş çalışanlar sayısını görüntüle</li>
<li>Çalışan iş türüne göre görüntüle</li>
</ul>
<p>İşe Alma</p>
<ul>
<li>Başvuran sayısına, nereden geldiklerine ve hangi pozisyona başvurduklarına dayanarak başvuranları analiz edin.</li>
</ul>
<p>Kurumsal eğitim</p>
<ul>
<li>Konuma göre kurs kaydı</li>
<li>Duruma göre kurs katılımcıları</li>
<li>Kurslar için kaydedilen çalışanların listesi</li>
</ul>
<p>Personel uzmanlıkları ve gelişim</p>
<ul>
<li>Çalışanlar tarafından sahip olunan yetenekler listesi</li>
<li>Ekip üyesine göre yetenek tiplerinin dökümü</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="localizations"></a>Yerelleştirmeler

<table>
<thead>
<tr>
<th>Yapabilecekleriniz</th>
<th>Bunun önemi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Yerelleştirmelerin kullanılabildiği ülkelere 18 ülke eklenmiştir:
<ul>
<li>Avusturya</li>
<li>Belçika</li>
<li>Brezilya</li>
<li>Çin</li>
<li>Çek Cumhuriyeti</li>
<li>Estonya</li>
<li>Finlandiya</li>
<li>Macaristan</li>
<li>İtalya</li>
<li>Letonya</li>
<li>Litvanya</li>
<li>Norveç</li>
<li>Polonya</li>
<li>Suudi Arabistan</li>
<li>İspanya</li>
<li>İsveç</li>
<li>İsviçre</li>
<li>Tayland</li>
</ul>
<p>Aşağıdaki ülkeler Perakende yerelleştirmesi de gerektirmektedir: Bu ülkeler için Perakende yerelleştirmesi tamamlanmamıştır ve H1 CY2017 için planlanmaktadır:</p>
<ul>
<li>Brezilya</li>
<li>Çek Cumhuriyeti</li>
<li>Estonya</li>
<li>Macaristan</li>
<li>Letonya</li>
<li>Litvanya</li>
<li>Malezya</li>
<li>Polonya</li>
<li>İsveç</li>
</ul>
</td>
<td>Dynamics 365 for Operations 18 ek ülkede kullanılabilir. Yerelleştirmeyi daha kolay ve daha yapılandırılabilir hale getirmek için yaptığımız çalışmaların bir parçası olarak, mevzuat elektronik raporlama özellikleri Elektronik raporlama (ER) yapılandırmalarına, bazı mevzuat Microsoft SQL Server Reporting Services (SSRS) raporları da Excel şablonları kullanan ER yapılandırmalarına dönüştürülmüştür. Bu dönüştürülmüş özellikler, bu tabloda daha sonra ayrıca ele alınmıştır.</td>
</tr>
<tr>
<td>Japonya: 26 numaralı formu ve ekli tablolarını yazdırırken sabit kıymetleri gruplandırın.</td>
<td>26 numaralı form, kurumun iş yaptığı tüm şehirlere gönderilmelidir. 26 numaralı formu yazdırmanızı kolaylaştırmak için, sabit kıymetler otomatik olarak gruplandırılabilir ve konuma göre sıralanabilir.</td>
</tr>
<tr>
<td>Japonya: Hızlandırılmış ve ek amortisman tutarları için profile bakın.</td>
<td>Profil, hızlandırılmış ve ek amortisman tutarlarına ilişkin doğru bir tahmin sağlayabilir.</td>
</tr>
<tr>
<td>Japonya: Stopaj vergisini aşamalı olarak hesaplayın.</td>
<td>Japon hükümeti stopaj vergisini ödeme tutarına göre aşamalı olarak hesaplamanızı gerektirir.</td>
</tr>
<tr>
<td>Japonya: Belirli büyük kurumsal binalar için posta kodu dosyasını içe aktarın.</td>
<td>Yetkililerin belirli büyük kurumsal binalar için verdiği posta kodu dosyası sisteme içe aktarılabilir. Adres daha sonra posta kodlarından çıkarılabilir.</td>
</tr>
<tr>
<td>Japonya: Sabit kıymetler için bir boşta kalma süresi yapılandırın.</td>
<td>Boşta kalma süreleri kullanıcının belirli bir dönemde sabit kıymet amortismanını duraklatmasına olanak tanır. Bu işlev, düzenleme uyarınca gereklidir.</td>
</tr>
<tr>
<td>Avrupa: Kayıt Kodu çerçevesini kullanarak bir tarafın adresi için bir katma değer vergisi (KDV) kayıt numarası yapılandırın.</td>
<td>Kayıt Kodu çerçevesini ve yeni bir <strong>KDV Kodu</strong> kayıt kategorisi kullanarak bir tarafın adresi için bir KDV kayıt numarası yapılandırabilirsiniz.</td>
</tr>
<tr>
<td>Finlandiya: Kayıt Kodu çerçevesini kullanarak bir tarafın adresi için bir gümrük müşteri numarası yapılandırın.</td>
<td>Kayıt Kodu çerçevesi ve yeni bir <strong>Gümrük müşteri kodu</strong> kayıt kategorisi kullanarak bir tarafın adresi için bir gümrük müşteri numarası yapılandırabilirsiniz.</td>
</tr>
<tr>
<td>Fransa: Müşteri faturalarını Fransa'ya özel bir düzenle yazdırın.</td>
<td>Müşteri fatura çıktısı Fransa'ya özgü gereksinimlere uygun hale getirilmiştir.</td>
</tr>
<tr>
<td>Fransa: Belgeleri mali döneme göre kronolojik olarak numaralandırmaya zorlayın.</td>
<td>Müşteri faturalarındaki numaralandırmayla ilgili Fransa'ya özgü gereksinimleri karşılamak amacıyla müşteri faturalarının numara sıralarını mali döneme göre ayarlayabilirsiniz.</td>
</tr>
<tr>
<td>Avusturya yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>Avusturya için AB Satış listesi XML biçimi</li>
<li>Avusturya için Intrastat biçimi</li>
<li>Avusturya için ISO20022 Alacak transferi ödeme biçimi</li>
<li>Avusturya için ISO20022 Otomatik ödeme biçimi</li>
<li>Avusturya EDIFACT PAYMUL biçimi</li>
<li>Avusturya için KDV beyannamesi</li>
</ul>
</td>
</tr>
<tr>
<td>Belçika yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>Belçika için BLWI biçimi</li>
<li>Belçika için AB Satış listesi XML biçimi</li>
<li>Belçika için sabit kıymetler raporu</li>
<li>Belçika için Intervat biçimi</li>
<li>Belçika için Intrastat biçimi</li>
<li>Belçika için fatura cirosu raporu</li>
<li>Belçika için genel muhasebe hareketi dışa aktarma biçimi</li>
<li>Belçika için SWIFT satıcı ödemesi biçimi</li>
<li>Belçika için CODA banka ekstresi içe aktarma biçimi</li>
<li>Belçika için ISO20022 Alacak transferi ödeme biçimi</li>
<li>Belçika için ISO20022 Otomatik ödeme biçimi</li>
</ul>
</td>
</tr>
<tr>
<td>Brezilya yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>Brezilya için GIA SP</li>
<li>Brezilya için GIA-ST</li>
</ul>
</td>
</tr>
<tr>
<td>Çek Cumhuriyeti yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>Çek Cumhuriyeti için AB Satış listesi XML biçimi</li>
<li>Çek Cumhuriyeti için Intrastat biçimi</li>
<li>Çek Cumhuriyeti için KDV beyannamesi</li>
</ul>
</td>
</tr>
<tr>
<td>Çin yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>Çin için Müşteri yaşlandırma raporu biçimi</li>
<li>Çin için müşteri borç tutarı analiz raporu biçimi</li>
<li>Çin için Satıcı yaşlandırma raporu biçimi</li>
<li>Çin için satıcı borç tutarı analiz raporu biçimi</li>
<li>Çin için alacak ödemesi yaşlandırma analizi biçimi</li>
<li>Çin için müşteri bakiye raporu biçimi</li>
<li>Çin için genel muhasebe hesabı bakiye raporu biçimi</li>
<li>Çin için satıcı bakiye raporu biçimi</li>
<li>Çin için GBT dosyası</li>
<li>Altın vergisi dışa aktarma dosyası biçimi</li>
<li>Çin için üretim tüketim farkı rapor biçimi</li>
</ul>
</td>
</tr>
<tr>
<td>Estonya yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>Estonya için AB Satış listesi XML biçimi</li>
<li>Estonya için Intrastat biçimi</li>
<li>Estonya için stok yeniden sınıflandırma bildirimi</li>
<li>Estonya için ISO20022 Alacak transferi ödeme biçimi</li>
<li>Estonya için müşteri satıcı bakiyesi bildirim raporu</li>
<li>Estonya için KDV beyannamesi</li>
</ul>
</td>
</tr>
<tr>
<td>Finlandiya yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>Finlandiya için AB Satış listesi TXT biçimi</li>
<li>Finlandiya için Intrastat biçimi</li>
<li>Finlandiya için ISO20022 Alacak transferi ödeme biçimi</li>
</ul>
</td>
</tr>
<tr>
<td>Macaristan yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>Macaristan için AB Satış listesi XML biçimi</li>
<li>Macaristan için Intrastat biçimi</li>
<li>Macaristan için Intrastat basitleştirilmiş biçimi</li>
<li>Macaristan için Fatura listesi dışa aktarma biçimi</li>
<li>Macaristan için KDV beyannamesi</li>
<li>Macaristan için KDV beyannamesi dökümü</li>
<li>Macaristan için stok ekstresi</li>
<li>Macaristan için MultiCash ödeme biçimi</li>
</ul>
</td>
</tr>
<tr>
<td>İtalya yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>İtalya için Intrastat biçimi</li>
<li>İtalya için proje faturası biçimi</li>
<li>İtalya için satış faturası biçimi</li>
<li>İtalya için ISO20022 Alacak transferi ödeme biçimi</li>
<li>İtalya için ISO20022 Otomatik ödeme biçimi</li>
<li>İtalya için RIBA koleksiyonu havale biçimi</li>
<li>İtalya için yurtiçi vergi hareketleri raporu</li>
<li>İtalya için blok listesi raporu</li>
<li>İtalya için Modello770 raporu</li>
<li>İtalya için yıllık vergi iletişimi raporu</li>
</ul>
</td>
</tr>
<tr>
<td>Letonya yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>Nakit tahsilat fişi kullanım raporu (LV)</li>
<li>Letonya için AB satış listesi XML biçimi</li>
<li>Letonya için AB Satış listesi düzeltmeleri XML biçimi</li>
<li>Letonya için Intrastat (A) biçimi</li>
<li>Letonya için Intrastat (B) biçimi</li>
<li>Letonya için stok sayım listesi</li>
<li>Letonya için stok sayım ekstresi</li>
<li>Letonya için stok hareketi</li>
<li>Letonya için dahili transfer teslimat notu</li>
<li>Letonya için stok yeniden sınıflandırma belgesi</li>
<li>Letonya için ISO20022 Alacak transferi ödeme biçimi</li>
<li>Letonya için KDV beyannamesi</li>
</ul>
</td>
</tr>
<tr>
<td>Litvanya yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>Litvanya için AB Satış listesi XML biçimi</li>
<li>Litvanya için Intrastat biçimi</li>
<li>Litvanya için stok ekstresi</li>
<li>Litvanya için ISO20022 Alacak transferi ödeme biçimi</li>
<li>Litvanya için müşteri satıcı mutabakatlar arası raporu</li>
<li>Litvanya için KDV beyannamesi</li>
</ul>
</td>
</tr>
<tr>
<td>Norveç yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>Norveç için tahsilat mektubu biçimi</li>
<li>Norveç için AutoGiro ödeme biçimi</li>
<li>Norveç için AvtaleGiro müşteri ödemesi biçimi</li>
<li>Norveç için eFaktura müşteri ödemesi biçimi</li>
<li>Norveç için ISO20022 Alacak transferi ödeme biçimi</li>
<li>Norveç için NETS ödeme biçimi</li>
</ul>
</td>
</tr>
<tr>
<td>Polonya yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>Polonya için Intrastat biçimi</li>
<li>Polonya için ambar belgeleri</li>
<li>Polonya için stok yeniden sınıflandırma belgesi</li>
<li>Polonya için MultiCash ödeme biçimi</li>
<li>Polonya için MultiCash yurtdışı ödeme biçimi</li>
<li>Polonya için müşteri satıcı bakiyesi onay raporu</li>
</ul>
</td>
</tr>
<tr>
<td>Suudi Arabistan yerelleştirmesi: ER yapılandırmaları</td>
<td>Suudi Arabistan için Bank LC Misc. Masraf Tahsisatı biçimi</td>
</tr>
<tr>
<td>İspanya yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>İspanya için AB Satış listesi TXT biçimi</li>
<li>İspanya için Intrastat biçimi</li>
<li>İspanya için proje faturası biçimi</li>
<li>İspanya için satış faturası biçimi</li>
<li>İspanya için ISO20022 Alacak transferi ödeme biçimi</li>
<li>İspanya için ISO20022 Otomatik ödeme biçimi</li>
<li>İspanya KDV kaydı defteri biçimi</li>
<li>İspanya KDV kaydı defter özeti biçimi</li>
<li>İspanya için ASCII'ye Beyanname 347 dışa aktarma</li>
<li>İspanya için Beyanname 347 raporu</li>
</ul>
</td>
</tr>
<tr>
<td>İsveç yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>İsveç için Intrastat biçimi</li>
<li>İsveç için Bankgirot Autogiro müşteri ödemesi biçimi</li>
<li>İsveç için Bankgirot satıcı ödemeleri biçimi</li>
<li>İsveç için SWIFT satıcı ödemesi biçimi</li>
<li>İsveç için SIE dışa aktarma biçimi</li>
<li>İsveç için ISO20022 Alacak transferi ödeme biçimi</li>
</ul>
</td>
</tr>
<tr>
<td>İsviçre yerelleştirmesi: ER yapılandırmaları</td>
<td>
<ul>
<li>İsviçre için DebitDirect ödeme biçimi</li>
<li>İsviçre için LSV otomatik ödeme biçimi</li>
<li>İsviçre için ISO20022 Alacak transferi ödeme biçimi</li>
<li>İsviçre için ISO20022 Otomatik ödeme biçimi</li>
<li>İsviçre için ESR banka ekstresi içe aktarma biçimi</li>
</ul>
</td>
</tr>
<tr>
<td>Almanya – Satıcı ödemelerini DTAZV biçiminde dışa aktar</td>
<td>Almanya, yabancı bir bankada bulunan bir hesaba giden Almanya'dan sınır ötesi ödemeleri veya yerel bir bankaya giden yabancı para birimindeki demeleri temsil eden bir kredi transferi (satıcı ödemesi) iletisi ile DTAZV yabancı biçim belirtimi gerektirmektedir.</td>
</tr>
</tbody>
</table>

### <a name="electronic-reporting"></a>Elektronik raporlama

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| ER raporlarını verileri çeşitli biçimlerde Belge Yönetimi depolama alanından oluşturulan elektronik iletilere ekleyecek şekilde yapılandırın. | ER raporları Belge Yönetimi depolama alanından verileri oluşturulan elektronik iletilere ekleyebilir. Bu nedenle, bir iş belgesinin ekleri yasal gereksinimlere uygun olarak, o belge için oluşturulan elektronik iletilere eklenebilir. Şu anda, bu ekler oluşturulan bir XML iletisine MIME biçiminde eklenebilir. Alternatif olarak, ekler oluşturulan bir ikili iletiye Base64 biçiminde eklenebilir. |
| ER raporlarını Excel, Microsoft Word veya PDF biçiminde elektronik belgeler oluşturmak için yapılandırın. | Bir yapılandırma, ER raporlarını üç farklı biçimde elektronik belge oluşturmak üzere etkinleştirir: OpenXML çalışma sayfası (Excel), Word ve XML Forms Veri Biçimi (XFDF) (PDF). Kullanıcılar Excel, Word veya PDF belgesi gibi bir ER raporuna bir biçim şablonu ekleyerek bir biçim seçebilir. |
| ER raporlarını OpenXML çalışma sayfası biçiminde oluşturulan elektronik belgelerin sayfa üstbilgilerine ve altbilgilerine veri girmek ve sayfa sonlarını denetlemek için yapılandırın. | ER raporları, iş verilerini sayfa üstbilgilerine ve altbilgilerine girebilir ve ayrıca sayfa sonu eklenen yerleri de denetleyebilir. Bu nedenle, raporlar oluşturulan elektronik belgelerin sayfalarındaki statik üst ve alt bölümleri destekleyebilir. Ayrıca, yasal gereksinimlere uyacak şekilde bu belgelerin özel sayfalama işlemini de destekleyebilir. |
| ER raporlarının hedefini çıktıyı e-posta olarak gönderecek ve iş verileri ile ER mantığının (ifadeler) çalışma zamanında kullanılacak e-posta adresini belirlemek için kullanılabileceği şekilde yapılandırın. | Önceden, bir ER hedefi yapılandırdığınızda, çıktı alıcısının e-posta adresi tasarım zamanında tanımlanabiliyordu. Artık bir ifadeyi ER biçiminde yapılandırabilirsiniz. Bu ifade daha sonra her biçim yapılandırması ve her çıktı bileşeni (klasör veya dosya) için ayrı ayrı e-posta adresinin kaynağı olarak bir hedefte seçilebilir. Böylece bir ER raporu çalıştırılırken, oluşturulan her dosya farklı bir alıcıya gönderilebilir ve e-posta adresi ER mantığına ve iş verilerine göre tanımlanabilir. |
| ER raporlarının hedefini çıktı yeni adlandırılmış bir dosya veya mevcut bir dosyanın yeni sürümü olarak Microsoft SharePoint klasörüne gönderilecek ve iş verileri veri kümesi veya bir rapor olarak Microsoft Power BI çerçevesinde kullanılabilecek şekilde yapılandırın. | ER raporlarını yapılandırdığınızda, istenen iş verilerini Power BI çerçevesinde kullanılabilecek şekilde kolaylıkla (kodlamadan) hazırlayabilirsiniz. Bu ER raporlarını çalıştırdığınızda, Power BI çerçevesine uygun iş verilerini ve/veya zaten mevcut olan Excel raporlarını sağlayabilirsiniz. Rapor çalıştırmalarını yinelenen modda zamanlarsanız iş verilerinin Power BI tabanlı raporları güncelleştirme zamanlamasını desteklemek üzere, Dynamics 365 for Operations'dan Power BI'ya zamanlanmış olarak gönderilmesi işlemini kurabilirsiniz. |
| ER raporlarını, belgenin kalan kısmını oluşturmak için bir veri kaynağı olarak zaten oluşturulmuş elektronik belgenin bir parçası olarak kullanmak üzere yapılandırın. | Çıktıyı metin biçiminde oluşturan ER raporlarını belgenin satır sayımını gerçekleştirmek için yapılandırabilirsiniz. Daha sonra, bu bilgiler özet ayrıntılarını içeren satırları oluşturmak için belgenin diğer bölümlerinde kullanılabilir. Bu özet bilgileri (toplamlar ve rakamlar) oluşturulan elektronik belgelere verilerin daha fazla dönüştürülmesini gerektirmeden hesaplanabilir ve yazdırılabilir. Bu nedenle, bu özellik rapor yürütme performansını artırır ve yapılandırılmış ER biçiminin gelecekteki bakımını kolaylaştırır. |
| ER raporlarını, metin biçiminde oluşturulan elektronik belgelerin dosya adı uzantılarını belirtmek için yapılandırın. | ER raporlarını belirli bir uzantıya sahip bir dosya olarak kaydedilebilmesi için çıktıyı metin biçiminde oluşturmak üzere yapılandırabilirsiniz. Varsayılan .txt uzantısına ek olarak .csv ve .prn gibi uzantıları biçim belirtimine uygun şekilde yapılandırabilirsiniz. |
| ER modelinin belirli bir sürümünü temel alan yeni ER raporları oluşturun. | Önceden, yeni bir ER biçimi oluşturduğunuzda biçimin veri kaynağı konumu olarak yalnızca seçili ER modelinin en son sürümü kullanılabiliyordu. Şimdi, seçili ER modelinin kullanılabilir herhangi bir sürümünü seçebilirsiniz. Bu özellik, geçerli yılın ER raporlarını korumanıza ve paralel olarak gelecek yıl için ER modelinin yeni bir sürümünü tasarlamanıza olanak tanır. |
| Veri kaynaklarında ve biçimlerde/modellerde tek bir tıklamayla metne veya seçili yapıya göre arama yapın. Rebase çalışmalarını etkin biçimde çözün ve yapılandırmalar arasındaki çakışmaları çözün. ER raporlarını, rapor yürütme durdurulana kadar keşfedilen hatalar için birden fazla doğrulama iletisi oluşturmak için yapılandırın. | ER çerçevesindeki çok sayıda kullanıcı deneyimi (UX) iyileştirmesi, kullanıcıların ER ile daha etkin ve kolay bir şekilde çalışmasına yardımcı olur. |
| Power BI raporlarında **ER** çalışma alanını gösterin. | Kullanıcılar **ER çalışma alanı** sayfasını yeni menü öğeleri ve Power BI tabanlı raporları çalıştıran canlı kutucuklar içerecek şekilde yapılandırabilir. |

## <a name="payroll"></a>Bordro

<table>
<thead>
<tr>
<th>Yapabilecekleriniz</th>
<th>Bunun önemi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Microsoft Dynamics AX 2012 R3'teki <strong>Bordro</strong> modülünün işlevine denk işlevselliği kullanarak ödeme kayıtlarını yapılandırın ve bordroyu işleyin.</td>
<td>Şimdi, AX 2012 R3'teki özellik kümesine denk bir özelliği kullanarak ABD bordrosunu yapılandırabilir ve işleyebilirsiniz.
<ul>
<li>Ödeme döngüleri ve ödeme dönemleri, iş döngüleri ve iş dönemleri, kazanç kodları ve kazanç kodu grupları, planlar, izin türleri ve kazanç tahakkuk planları yapılandırabilirsiniz.</li>
<li>Kazançlar ve vergiler için zorunlu kesintiler ayarlayabilir ve raporlama ve analiz amacıyla pozisyonlar hakkında bordro bilgilerini kaydedebilirsiniz.</li>
<li>Maaş ve vergi hacizleri için ve ilişkili tüm yönetimsel ücretler için kesinti ayarlayabilir ve yönetebilirsiniz.</li>
</ul>
</td>
</tr>
<tr>
<td>Maaş dönemi işleminizi yeni <strong>Bordro yönetimi </strong>çalışma alanını kullanarak izleyin ve işleyin.</td>
<td>Artık bordro işlemeyi kolaylıkla izleyebilirsiniz. Bordro yöneticileri ödeme işleminin eksiksiz ve doğru olması için, dikkat gerektiren kazanç ve ödeme ekstrelerini bir bakışta görebilir. <strong>Bordro yönetimi </strong>çalışma alanı kullanıcıların tek bir çalışma alanından uçtan uca işlemleri izlemesine ve çalıştırmasına olanak tanır.</td>
</tr>
<tr>
<td>Maaş çekleri için pozitif ödeme dosyaları oluşturun.</td>
<td>Bordro ödemeleri için Nakit ve banka yönetiminde pozitif ödeme işlevinin yeni bir uzantısı bulunmaktadır. Bordroya özel, ayrı yapılandırmayı etkinleştirmek için temel işlem boyunca ayrı menü öğeleri eklenmiştir. İşlev, Microsoft Dynamics AX uygulama sürümü 7.0.1 (Mayıs 2016) ile yayımlanan temel pozitif ödeme özelliği ile aynıdır. Bu uzantı nedeniyle, bordro verileri pozitif ödeme hareketlerinizin geri kalanından tamamen ayrı tutulur. Bu yalıtım, bordroyla ilgili verilere yalnızca bordro kullanıcılarının erişip bunları görmesini garanti altına almaya yardımcı olur.</td>
</tr>
<tr>
<td>Yeni Kazanç Ekstresi Satırı veri varlığını kullanarak kazanç ekstresi satırlarını harici bir kaynaktan içe aktarın.</td>
<td>Önemli bir yeni veri varlığı, harici zaman ve kazanç hesaplama sistemleriyle tümleştirmeyi sağlar. Veri varlığı, kazanç ekstresi satırlarını içe aktarır ve kullanıcının doğrudan kazanç ekstresine girdiği aynı varsayılan mantığı gerçekleştirir. İçe aktarma işleminden sonra, satırlar uygun kazanç ekstresi belgesiyle otomatik olarak ilişkilendirilir. Uygun bir kazanç ekstresi belgesi yoksa otomatik olarak bir belge oluşturulur.</td>
</tr>
</tbody>
</table>

## <a name="planning-and-scheduling"></a>Planlama ve zaman çizelgesi planlaması

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| Satışlar ve satınalmalar için, ana üründe etkin tüm ürün boyutlarını temel alan varsayılan sipariş ayarlarını ayarlayın. Böylece, stok tutma birimi (SKU) veya kısmi SKU için varsayılan sipariş ayarlarını tanımlayabilirsiniz. | Ürün boyutu veya ürün boyutları birleşimi için geçerli olan varsayılan sipariş ayarlarını belirtebilirsiniz.<p>**Örnek**</p><p>Polo Tişört adlı bir ürün satıyorsunuz. Bu ürünün Yeşil ve Mavi olmak üzere iki rengi var. Small ve Medium boy olmak üzere iki boyu var. Polo Tişörtün etkin ürün boyutları Renk ve Ebat'tır. Ebattan bağımsız olarak tüm yeşil Polo Tişörtlerin satınalma işlemlerini engelleyebilirsiniz.</p> |

## <a name="product-master-data"></a>Ana ürün verileri

<table>
<thead>
<tr>
<th>Yapabilecekleriniz</th>
<th>Bunun önemi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tüm varsayılan sipariş ayarlarını ve siteye özel sipariş ayarlarını aynı anda, tek bir sayfadan ayarlayın.</td>
<td>Bu özellik, madde ayarları için daha iyi bir genel bakış sağlar.</td>
</tr>
<tr>
<td>Ürün çeşidi numaraları için bir terminoloji oluşturun.</td>
<td>Ürün boyutları, öznitelikleri ve ürün çeşidi numaralarınızdaki karakterler gibi öğeler ekleyebilirsiniz. Satış siparişi veya satınalma siparişi oluşturduğunuzda, belirli ürün çeşidini hızlı bir şekilde bulabilirsiniz.</td>
</tr>
<tr>
<td>Satış ve satınalma senaryolarında ürünleri ve ürün çeşitlerini arayın.</td>
<td>Satış satırı veya satınalma satırı oluşturduğunuzda, ürün boyutlarını ve Global Ticaret Madde Numaraları (GTIN) ve barkodlar hariç herhangi bir ürün numarasını kullanarak ürünlerde arama yapabilirsiniz. Bu arama, satış ve satınalma arama listesinde kullanılan mevcut "İle başlar" aramasının yerini alan bir tam metin aramasıdır. Bu özellik, benzer özelliklere sahip ürün gruplarını veya benzersiz özelliklere sahip tek bir ürünü bulmanızı sağlar. Bu özelliği etkinleştirmek için, <strong>Arama parametreleri</strong> sayfasında <strong>Ürün aramayı etkinleştir</strong> parametresini seçin.</td>
</tr>
<tr>
<td>Satış veya satınalma hareketi oluşturduğunuzda ürün çeşidini doğrudan belirtin. Alternatif olarak, geçerli boyut birleşimlerinin listesinden seçim yapabilirsiniz.</td>
<td>Bu özellik bir üretkenlik geliştirmesidir.
<p><strong>Örnek</strong></p>
<p>Polo Tişört adlı bir ürün satıyorsunuz. Bu ürünün Yeşil ve Mavi olmak üzere iki rengi var. Small ve Medium boy olmak üzere iki boyu var. Polo Tişörtün etkin ürün boyutları Renk ve Ebat'tır. Yeşil renkte ve Small ebadında bir Polo Tişört için bir satış satırı girdiğinizde, <strong>Madde numarası</strong>, <strong>Renk</strong> ve <strong>Ebat</strong> alanlarına veri girmeniz gerekmez. Satırı aşağıdaki adımlardan birini izleyerek oluşturabilirsiniz:</p>
<ul>
<li><strong>Madde numarası</strong> alanında, ürün çeşidi numarasını, renk değerini veya ebadı girin. Arama alanında, satmak istediğiniz özel çeşidi bulun ve satış satırını oluşturun.</li>
<li><strong>Madde numarası</strong> alanına madde numarasını girin. Herhangi bir ürün boyutu alanına gidin. <strong>Ürün boyutu</strong> aramasında, Polo Tişört için geçerli olan tüm yayımlanmış boyut birleşimlerini görürsünüz. Tek bir adımda, satmak istediğiniz ürün çeşidini seçebilirsiniz.</li>
</ul>
</td>
</tr>
<tr>
<td>Ürün numaralarının işlem sayfalarında görünüp görünmeyeceğini belirtin.</td>
<td>Satış siparişleri ve satınalma siparişleri gibi işlem sayfaları yalnızca <strong>Madde numarası</strong> ve <strong>Ürün adı</strong> alanlarını gösterir. <strong>Ürün numarası</strong> alanını görmek için <strong>Ürün bilgileri yönetim parametreleri</strong> altından <strong>Formlarda ürün parametrelerini göster</strong> parametresini seçin.</td>
</tr>
</tbody>
</table>

## <a name="project-management-and-accounting"></a>Proje yönetimi ve muhasebe

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| Fatura tekliflerini toplu olarak deftere naklettiğinizde geç seçimi kullanın. | Proje muhasebecileri teklifler toplu işte belirtilen ölçütleri karşılıyorsa deftere nakletmek üzere fatura tekliflerini otomatik olarak seçecek bir toplu iş ayarlayabilir. Toplu iş sürekli olarak çalışabildiği ve nakletmek için teklifleri otomatik olarak seçtiğinden, bu özellik fatura deftere nakil otomasyonunu iyileştirir. |
| Power BI masaüstünde analiz oluşturun. | Projeyle ilgili ve kaynakla ilgili veriler için iş zekası (BI) içeriği Power BI masaüstünde kolaylıkla oluşturulabilir. |
| Satınalma siparişi ön ödemeleri kullanın ve bunları proje tahmin işlemine doğru şekilde ekleyin. | Proje satınalma siparişlerinde, bir miktar ödeme satıcılara serbest bırakılmadan önce ön ödemelerin işlenmesi gerekir. Şimdi, bu ön ödeme faturaları **Sabit fiyatlı** türündeki projelerin proje tahmini/kabul işleminde görünür. |
| Maliyet ve gelir tahminlerine ve madde gereksinimlerine doğrudan bir iş kırılım yapısı (WBS) görevi içinden erişin ve yönetin. | Maliyet tahminlerini, gelir tahminlerini ve belirli bir WBS görevinin madde gereksinimlerini WBS planlama görünümünde o göreve ait ayrıntılar iletişim kutusundan yönetebilirsiniz. |
| Ücret günlüklerinde bir finansman kaynağı seçin. | Proje sözleşmesi birden fazla finansman kaynağı içeriyorsa, ücretler deftere nakledildiğinde tek bir belirli finansman kaynağı seçebilirsiniz. Belirli bir finansman kaynağı seçmezseniz ücretlerin tahsisatı için sözleşmede belirtilen finansman kuralları kullanılır. |
| Proje raporlarını Excel'de açın. | Genel muhasebe güncelleştirmeleri ve bütçe güncelleştirmeleri için yeni veri varlıkları, proje raporu verilerini Excel'de açmanızı ve Excel işlevini kullanarak analiz oluşturmanızı sağlar. |
| Proje yönetimi ve muhasebe (PMA) işlevini etkinleştirmek için tek bir yapılandırma anahtarı kullanın. | Projeyle ilgili yapılandırma anahtarları, PMA işlevini etkinleştiren tek bir proje yapılandırma anahtarı ile değiştirilmiştir. |

## <a name="retail-and-commerce"></a>Perakende ve ticaret

### <a name="advanced-warehouse-management-in-a-retail-store"></a>Perakende mağazasında gelişmiş ambar yönetimi

Perakendeciler mağazalarında Gelişmiş ambar yönetimi (WHS) çözümünü kullanabilir ve bunu desteklemek için geçerli satış noktası (POS) özelliklerine gerekli güncelleştirmeleri yapabilir. El tipi çözüm işlemleri, mağazada da başka bir ambarda çalıştığı gibi çalışmalıdır. Geçerli tüm perakende mağaza stok işlemleri ve stok hareketi oluşturan veya güncelleştiren tüm POS işlemleri, WHS özellikli ambarların belirli gereksinimlerini kullanacak şekilde güncelleştirilir.

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| WHS özellikli mağazalarda kullanılabilir stoğu aramak için POS kullanın. | Stokta arama yaptığınızda, işlem daha önceki gibi çalışmalıdır. Arama, kullanılabilir miktarları ambar düzeyinde göstermelidir ve Konum, Stok durumu ve Plaka boyutlarını dikkate almamalıdır. |
| WHS özellikli bir mağazada bir transfer emrine ait ürün girişini işlemek için POS kullanın. | Transfer emirlerini WHS özellikli mağaza ve maddeler için POS'ta alabilirsiniz. Kullanıcı teslim almanın gerçekleşeceği konumları seçebilmeli ve teslim alma satırlarını otomatik olarak doldurmak için plaka kodlarını girebilmelidir. |
| WHS özellikli bir mağazada bir satınalma siparişine ait ürün girişini işlemek için POS kullanın. | Satınalma siparişlerini WHS özellikli mağaza ve maddeler için POS'ta alabilirsiniz. Kullanıcı teslim almanın gerçekleşeceği konumları seçebilmeli ve teslim alma satırlarını otomatik olarak doldurmak için plaka kodlarını girebilmelidir. |
| WHS özellikli bir mağazadan ürünlerin sevkiyatını işlemek için POS kullanın. | Transferleri WHS özellikli mağaza ve maddeler için POS'tan kaydedebilirsiniz. Kullanıcı sevk edilecek konumları seçebilmelidir, stok durumu otomatik olarak oluşturulmalıdır ve plakalar göz ardı edilmelidir. |

### <a name="enable-seamless-omni-channel-commerce"></a>Omni-kanal ticareti sorunsuz bir şekilde etkinleştirme

Sorunsuz omni-kanal ticareti fiziksel mağazalarda, çevrimiçi mağazalarda, çağrı merkezlerinde ve mobil ticaret deneyimlerinde yönetim ve sipariş işleme anlamına gelir. Bu sürümde, bu alanda aşağıdaki yatırımlar yapılmıştır:

- E-ticaret mağazaları için yayınlara yönelik geliştirmeler
- Ürün keşfine, hesap yönetimine ve çevrimiçi alışverişe olanak tanıyan, tüketiciye yönelik yeni bir mobil uygulama

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| Tüketici: Tüketiciye yönelik uygulamanın geçerli sürümü, ürün arama, kategori tarama, sepete ekleme ve konuk ödemesi özelliklerini etkinleştirir. Perakendeciler uygulamaya şirketlerinin markasını uygulayabilir ve Android ve iOS uygulama mağazalarında paket olarak sunabilir. | Perakendeciler müşterilerinin mobil cihazlarından tarama, ürün arama ve konuk olarak ürün göndermelerini sağlayan tüketiciye yönelik bir uygulamayı kolaylıkla oluşturabilir. |
| Ortak ticaret çevrimiçi mağazaları için müşteri istek listeleri | Bağımsız yazılım satıcıları (ISV'ler), kullanıcıların çevrimiçi mağazada birden fazla liste oluşturup bunları yönetmesini sağlamak için istek listesi denetimini kullanabilir ve bu listeleri POS'ta görüntüleyebilir/kullanabilir. |
| E-ticaret çevrimiçi mağazaları üzerinden zaman uyumsuz müşteri oluşturma | Artık, ISV'ler Commerce Data Exchange: Real-time Service kullanılamadığında bile müşteri hesabı oluşturabilir. |
| Retail Server'dan üçüncü taraf mağazalara kanal ürünleri yayımlayın. | Retail Server artık servisten servise kimlik doğrulamayı destekler. ISV'ler Retail Server'dan üçüncü taraf mağazalara kanal ürünü yayınından yararlanabilir. |

### <a name="extensibility"></a>Genişletilebilirlik

- Ticaret çalışma zamanı projeleri artık Perakende SDK'de mühürlenir.
- Bileşenleri oluşturulmuş Microsoft bileşen paketleri ve POS, Retail Server, Veritabanları, Ödeme ve Donanım istasyonları için ISV paketleri ile daha kolay dağıtım ve hizmet sağlama.

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| CRT/Retail Server: Perakendeciler veya ISV'ler ticaret çalışma zamanını CRT uzantı kancaları aracılığıyla genişletebilir. Satır içi kod değişiklikleri artık desteklenmez. | Sürekli tümleştirmeyi ve sürekli dağıtımı etkinleştirmek için, satır içi kod değişikliklerinden tamamen kaçınılmalıdır. Ayrıca, herhangi bir kod birleştirme ve CRT bileşenleri için dağıtım olmadan düzeltmelerin kolaylıkla düzenlenmesini desteklemek üzere. |

### <a name="personalized-product-recommendations"></a>Kişiselleştirilmiş ürün önerileri

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| Bir müşterinin satın alma geçmişi, dilek listesindeki öğeler ve diğer müşterilerin çevrimiçi ve fiziksel mağazalardan satın aldığı mallar temel alınarak ilgilenebilecekleri şeyleri belirlemek için satış noktasındaki (POS) birden çok dokunmatik noktada verilen kişiselleştirilmiş ürün önerilerini görüntüleyin. | Büyük katalogları olan perakendeciler için, kişiselleştirilmiş öneriler müşteriye ürün bulmalarında yardımcı olur ve mağazanın akıllı müşterilerle ilişki kurmasını sağlar. Müşterinin ilgi alanlarını ve satın alma alışkanlıklarını hedefleyen ürünleri sunarak , ürün önerileri perakendecilere yukarı satış konusunda yardımı olabilir ve müşteri tutmayı geliştirebilir. Retail'de, ürün önerileri bilişsel servisler ve Microsoft Azure makine öğrenimi ile sağlanır. |

### <a name="pos-task-recorder"></a>POS görev kaydedicisi

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| Perakendeciler eğitim malzemeleri, İş süreci modelleyici (BPM) diyagramları üretmek ve üretkenliği artırıp uygulamaların analizini ve tasarımını daha iyi yapmak için POS görev kaydediciyi kullanabilir. | Sürekli tümleştirmeyi ve sürekli dağıtımı etkinleştirmek için satır içi değişikliklerden tamamen kaçınılmalıdır. Ayrıca, herhangi bir kod birleştirme ve CRT bileşenleri için dağıtım olmadan düzeltmelerin kolaylıkla düzenlenmesini desteklemek üzere. |
| POS'ta gerçek zamanlı yardım. | Kasiyer/Yönetici bağlamı değiştirmeden, iş sürecinde POS'tan gerçek zamanlı yardım alabilir. |

### <a name="store-system-providing-a-seamless-on-premises-store-experience"></a>Mağaza sistemi: Sorunsuz yerinde mağaza deneyimi sağlama

Mağaza sistemi, perakendeciler için yerinde mağazada, Microsoft genel bulutu veya müşterinin kendi özel bulutu üzerinde, bir dizi mağaza işleminin yönetilmesine yardımcı olan bir dağıtım seçeneğidir. Bu sürümde, kapsam yalnızca mağaza içidir. Yavaş ve güvenilir olmayan ağ bağlantısına sahip ortamları daha iyi desteklemek için, perakendecilere kanal veritabanını ve Retail Server'ı mağazada dağıtacakları bir seçenek sunmalıyız. Perakendeciler merkez (HQ) ile bağlantı olmasa da temel iş senaryolarını çalıştırmaya devam edebilir. Mühendislik ekibi tartışmalarını, müşteri anketi sonuçlarını ve rakip analizlerini içeren çeşitli veri noktalarına göre, hedef müşterilerimiz için ideal çözüm olarak aşağıdaki kapsamı tanımladık:

- Mağaza sistemi için bir self servis paket kullanılabilir.
- Varsayılan kurulum tek kutudan dağıtımdır ancak özel dağıtıma da izin verilir.
- Kolay dağıtımı/self servisi etkinleştirin.
- Retail Server ve mağaza veritabanı Async Client hizmeti ile birlikte mağazadadır.
- Mağazadaki Retail Server, Mağaza sistemi için doğrudan genel merkezdeki Uygulama Nesne Sunucusu (AOS) ile iletişim kurar.
- Genel merkezde bağlantı olmadığında, terminaller arasında senaryoları destekleyin.
- Retail Modern POS ve Bulut POS, her zaman mağazadaki Retail Server ile iletişim kurar.
- Genel merkezde bağlantı olmadığında, Retail Modern POS'u ve Bulut POS'u destekleyin.
- Genel merkezde bağlantı olmayan, Retail Modern POS'a özel çevrimdışı bir veritabanını (her Retail Modern POS kurulumu için ayrılmış) destekleyin.
- Kimlik doğrulama yalnızca Mağaza sistemi için servisten servise yöntemini temel alır.
- Real-time Service çağrıları, İnternet bağlantısı olmadığında desteklenmez.
- Retail Modern POS'un kanal veritabanına doğrudan veritabanı üzerinden bağlantısı desteklenmez.
- Telemetriyi/izlemeyi etkinleştirin.

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| Perakendeci, Mağaza sistemi self servis yükleyicisini Dynamics AX genel merkezindeki kanal veritabanı sayfasından indirir ve yapılandırma dosyasını indirir. | Perakendeci, self servis paketi sorunsuzca indirebilir. |
| Perakendeci, Mağaza sistemini self servis yükleyici kullanarak yükler. | Perakendeci, Mağaza sistemini self servis paketini kullanarak yükleyebilir. |
| BT yöneticisi Mağaza sistemini Dynamics 365 for Operations'da (kanal veritabanı, kanal profili, mağaza ve dağıtılabilir paket) yapılandırır. | BT yöneticisi Mağaza sistemini kolaylıkla ve verimli bir şekilde yapılandırabilir. |
| Perakendeci, Retail Modern POS'u yerinde mağazada çalıştırır ve bağlantı olduğunda hediye kartı vermek gibi gerçek zamanlı işlemler yapabilir. | Perakendeci, bağlantı olduğunda Mağaza sisteminden gerçek zamanlı eylemler gerçekleştirebilir. |
| Perakendeci, bağlantı olduğunda yerinde Mağaza sisteminden genel merkeze verileri eşitleyebilir. | Perakendeci, bağlantı olduğunda Mağaza sistemine ve bu sistemden eşitleme yapabilir. |
| Perakendeci, yerinde Mağaza sistemi ve genel merkez arasındaki iletişimin güvenliğini sağlayabilir. | Perakendeci, bağlantı olduğunda Mağaza sisteminden güvenle iletişim gerçekleştirebilir. |
| BT yöneticisi ve Microsoft Operations, yerinde Mağaza sistemini (tanılama ve raporlama değişiklikleri) izleyebilir ve sistem hakkında rapor sunabilir. | BT yöneticisi ve Microsoft Operations, Mağaza sistemini güvenli bir şekilde izleyebilir ve sorunları etkin bir şekilde giderebilir. |

### <a name="universal-windows-platform-app-for-retail-modern-pos"></a>Retail Modern POS için Evrensel Windows Platformu

Şu anda, Retail Modern POS yalnızca masaüstü bilgisayarlar ve tabletler için Windows 8.1 uygulaması ve masaüstü veya tablet tarayıcıları için Bulut POS olarak kullanılabilir. Bu sürümde, Perakende Modern POS bir Evrensel Windows Platformu (UWP) uygulamasına dönüştürülür. Bu değişiklik, Retail Modern POS'un tüm Windows 10 cihazlarda (masaüstü, tablet veya telefon) çalışmasını ve Continuum özellikli cihazlarda görünümler arasında geçiş yapmasını sağlar.

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| Küçük form faktörü cihazlar için önemli POS işlevini etkinleştirin. | Perakende POS işlevi Windows 10 çalıştıran telefonlarda ve küçük form faktörü cihazlarda kullanılabilir. |

## <a name="supply-chain-management"></a>Tedarik zinciri yönetimi

### <a name="consignment-inventory"></a>Konsinye stok

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| Satıcı olarak, hammaddeleri müşterinin ambarında saklayabilirsiniz. Müşteri olarak, fiili satınalma işlemini üretim için hammadde gerekene kadar erteleyebilirsiniz. | Hammadde stoğu tutmak ciddi maliyet doğurabilir. Konsinye stok kullanarak, satıcı hammaddeleri müşterinin ambarında saklayabilir. Daha sonra, müşteri fiili satınalma işlemini üretim için hammadde gerekene kadar erteleyebilir. Hammaddeler bir konsinye stok yenileme siparişi kullanılarak sipariş edilir ve alınır. Bu stok yenileme siparişi, fiziksel hareketleri kaydeder ancak genel muhasebeyi etkilemez. Müşterinin sahip olduğu stok maddeleri ile satıcının sahip olduğu stok maddelerini birbirinden ayırmak için, Stok sahibi boyutunu kullanabilirsiniz. Stoğun sahipliğinin değişmesi hammaddelerin sahipliğinin satıcının sahip olduğu stoktan müşterinin sahip olduğu stoğa aktarılmasını sağlayan bir günlük işlemi tarafından yönetilir. Bu işlem, bir satınalma emrinin ve bir ürün girişinin oluşturulmasını tetikler.<blockquote>[!NOTE] Bu özellik, üretim için gelen hammadde konsinyesi ile sınırlıdır. Ambar yönetimi (WHS) ve Taşıma yönetimi (TMS) ile tümleştirilmemiştir.</blockquote> |
| Satıcı olarak, müşteriye aktarılan konsinye stoğun tutarı hakkında bilgi edinin. | Müşteriyi faturalandırmak için, satıcıya konsinye stoktan satın alınan hammaddeler ve satınalma tarihi hakkında bilgiler gerekir. Satıcı ayrıca, satıcı iş birliği arabirimini kullanarak müşterinin tesisindeki eldeki stoğu da izleyebilir. |
| Transfer günlüğü kullanarak satıcıya ait stoğu taşıyın. | Satıcıya ait stoğun fiziksel pozisyonunu izlemek için pozisyonu sisteme kaydedebilmeniz gerekir. Transfer günlüğü kullanarak, bir ambardaki bir konumdan aynı ambardaki başka bir konuma taşınma gibi stoğun fiziksel hareketini kaydedebilirsiniz. |
| Satıcıya ait stoğu sayım günlüğü kullanarak düzeltin. | Sistemdeki eldeki stoğu, fiili fiziksel stok ile eşit tutmak önemlidir. Satıcıya ait stok, miktar düzeltmesi ve sayım günlüğü işlemleri gibi sayım işlemleri kullanılarak artı eksi olarak düzeltilebilir. |
| Dynamics 365 for Operations içinde konsinye desteği hakkında daha fazla bilgi alın | Konsinye işlemleri desteği hakkında daha fazla bilgi için bkz. [Konsinye](../../../supply-chain/inventory/consignment.md), [Konsinyeyi ayarlama](/d365F-O/fin-ops-core/fin-ops/get-started/consignment), [Konsinye stok yenileme siparişi oluşturma (Görev kılavuzu)](../../../supply-chain/inventory/tasks/create-consignment-replenishment-order.md) ve [Üretim talebine bağlı olarak konsinye stok sahipliğini değiştirme (Görev kılavuzu)](../../../supply-chain/inventory/tasks/change-ownership-consignment.md). |

### <a name="vendor-collaboration-previously-known-as-the-vendor-portal"></a>Satıcı iş birliği (eski adıyla Satıcı portalı)

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| Satıcıların her satınalma siparişi satırına yanıt vermesini ve değişiklik önerebilmelerini sağlayın. | Bazı durumlarda, satıcılar bazı satınalma siparişi satırlarını kabul edip bazılarını reddetmek ister. Artık satıcılar satınalma sipariş satırlarını ayrı ayrı yönetebilir. Her satır reddedilebilir, kabul edilebilir veya değişikliklerle kabul edilebilir. Örneğin, satıcılar teslimat tarihini değiştirebilir, teslimatı ve miktarı bölebilir veya alternatif bir madde önerebilir. |
| Satıcıların ilgili kişi bilgilerini yönetmesini sağlayın. | Satıcılar şirketleri için ilgili kişi bilgilerini saklayabilir. Bu bilgiler adları, e-posta adreslerini ve telefon numaralarını içerir. Bu özelliğe erişim özel bir güvenlik rolü üzerinden sağlanır. |
| Satınalma siparişleri ile ilgili belgeleri satıcılarla paylaşın. | Gereksinimler hakkında bir belge gibi bir belgeyi bir satıcıyla paylaşmanız gerektiğinde belgeyi ilgili satınalma siparişine bağlamak uygundur. Satıcı, belgeyi satınalma siparişine verdiği yanıta bağlayarak notları ve ekleri müşteriyle paylaşabilir. Belge yönetimi temel destekleyici çerçevesidir ve yalnızca "harici" olarak sınıflandırılan notlar ve ekler satıcılarla paylaşılabilir. |
| Yeni satıcı kullanıcıları provizyonu. | Satıcılarınız satıcı iş birliği arabirimini kullanıyorsa yeni kişiler, satıcı iş birliğine erişim istediğinde yeni kullanıcı hesapları istemek için sorunsuz bir yönteme sahiptir. Tedarik profesyonelleri satıcı kuruluştaki bir ilgili kişi için bir kullanıcı hesabı isteği gönderebilir. Zaten satıcı iş birliği kullanıcısı olan bir satıcı ilgili kişisi de bu tür bir istek gönderebilir. Bu istek sonuç olarak Dynamics 365 for Operations'da satıcıya özel güvenlik rolleri olan yeni bir kullanıcı oluşturur. Ayrıca Microsoft Azure B2B portalını, kullanıcıya yeni bir Azure Active Directory (Azure AD) kullanıcı hesabı sağlamak için de kullanır. Satıcılar ayrıca belirli satıcı kullanıcısı hesaplarının devre dışı bırakılmasını veya güvenlik rollerinin değiştirilmesini de isteyebilir. |
| Dynamics 365 for Operations'da satıcı iş birliği desteği hakkında daha fazla bilgi edinin. | Satıcı iş birliği hakkında daha fazla bilgi için bkz. [Harici satıcılarla satıcı iş birliği](../../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md), [Müşterilerle satıcı iş birliği](../../../supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations.md), [Satıcı iş birliği kullanıcılarını yönetme](../../../supply-chain/procurement/manage-vendor-collaboration-users.md), [Satıcı iş birliğini ayarlama ve koruma](../../../supply-chain/procurement/set-up-maintain-vendor-collaboration.md) ve [Satıcı iş birliği faturalama çalışma alanı](../../../finance/accounts-payable/vendor-portal-invoicing-workspace.md). |

### <a name="intercompany-order-processing"></a>Şirketlerarası sipariş işleme

<table>
<thead>
<tr>
<th>Yapabilecekleriniz</th>
<th>Bunun önemi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Talebin nereden kaynaklanacağını ve nasıl bulunacağını doğrudan satış siparişi satırlarından tanımlayın.
<p><strong>Örnek</strong></p>
<p>Satış siparişi satırı oluşturun ve teslim türünü doğrudan teslim olarak belirtin. Birincil satıcı, satış siparişi satırına kaynak noktası olarak eklenir.</p>
</td>
<td>Sipariş alma akışı önemli ölçüde iyileştirilmiştir. Artık talebin nereden kaynaklanacağını ve nasıl bulunacağını doğrudan satış siparişi satırlarından tanımlayabilirsiniz. Artık satış siparişine tüm satırların eklenmesini beklemek zorunda değilsiniz. Satış siparişi satırlarındaki yeni seçenekler, bir satıcı belirttiğinizde teslimat türünü belirlemenize olanak tanır. Satıcıyla satış siparişi satırlarını ilişkilendirdiğinizde, teslimattan satıcıya sipariş zincirleri oluşturulur.
<ul>
<li>Satıcı dahili satınalma siparişi ve satış siparişi kullanan bir şirketlerarası satıcı veya harici satınalma siparişini kullanan harici bir satıcı olabilir.</li>
<li>Teslimat türü <strong>Doğrudan teslim</strong> veya <strong>Stok</strong> olabilir. <strong>Stok</strong> teslim türü, satıcının müşteriye sevk etmeden önce yerel stoğu tedarik etmesi gerektiğini gösterir.</li>
</ul>
</td>
</tr>
<tr>
<td>Sipariş taahhüdünü doğrudan satış siparişi satırlarından oluşturun.
<p><strong>Örnek</strong></p>
<p>Şirketlerarası satıcıdan kaynaklanan bir satış siparişi satırı oluşturun. Satırdan çıkın. Teslimat tarihleri, kaynak sağlayan şirketteki kullanılabilirliğe göre hesaplanır.</p>
</td>
<td>Yeni kaynak bilgilerini kullanan satış siparişi satırları oluşturduğunuzda, <strong>Teslimat tarihi</strong> denetimine göre hesaplanır. Örneğin, bir şirketlerarası satıcı seçildiğinde kaynak sağlayan şirketteki kullanılabilirlik hesaplanır. Bu şekilde, sipariş zincirleri satış siparişi satırları ile birlikte otomatik olarak oluşturulur. Bu işlev, teslimat tarihlerinin kaynak sağlayan şirkette görünür olmasını sağlamaya yardımcı olur. Böylece, karşılanabilir miktar (ATP) profilleri beklenen talepleri doğrudan satış siparişleri oluşturulduğunda işler.</td>
</tr>
<tr>
<td>Tüm kaynak konumlarında ürün kullanılabilirliğini inceleyin ve en iyi kaynak seçeneğini belirleyin.</td>
<td><strong>Teslimat alternatifleri</strong> sayfası yeniden tasarlanmıştır ve şimdi onaylanan tüm dahili ve harici satıcılar hakkında değerli bilgiler sunar. Bu bilgiler satıcı tedariki için kaynak seçeneklerini içerir. Teslimat modu seçtiğinizde, sistem uygun teslimat tarihlerini hesaplar. Müşteri için en iyi seçeneği sorunsuz bir şekilde seçebilir ve bu seçeneği tüm satış sipariş satırlarına uygulayabilirsiniz.</td>
</tr>
</tbody>
</table>

### <a name="warehouse-enhancements-for-high-volume-distribution-centers"></a>Yüksek hacimli dağıtım merkezleri için ambar geliştirmeleri

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| Mallar sevk istasyonunda paketlendikten sonra iş oluşturun. | Bu özellik, el ile paketleme işinden sonraki ek işlemler (paletleme, kalite incelemesi, sevkiyatların birleştirilmesi veya yükleme noktalarının değiştirilmesi vs.) olduğunda kullanışlıdır. Yeni **Sevk edilmiş konteyner çekme işlemi** iş türü ayrı iş satırları kullanarak bu görevleri modellemenizi sağlar. Şimdi paketlemeden sonraki işi oluşturmak için paketleme istasyonlarını modelleyebilirsiniz. Bu iş, paketlenmiş stoğun hareketini düzenlemek için kullanılabilir. |
| Konteynerleri paketleme istasyonunda gruplandırın. | Bu özellik, birden çok paketin paketleme istasyonunda tek bir konteyner veya plaka altında gruplandırılmasını sağlar. Örneğin, bir e-ticaret/toptan satış yapan biri 100 adet ayrı ayrı paketlenmiş ürünü tek bir konteynerde (palet veya kafes) gruplandırabilir. Bu konteyner, bir çalışanın gruplandırılmış konteynere ait tek bir barkodu (plakayı) tarayarak oluşturduğu tek bir çalışma yönergesi ile taşınabilir, aşamalandırılabilir veya yüklenebilir. Bu özellik, çok sayıda küçük ambalajlı konteynerleri taşımak için yapılan iş hareketlerini en aza indirir. Daha fazla bilgi için bkz. [Plaka birleştirme işlemi için bir mobil cihaz menü öğesi oluşturma (Görev kılavuzu)](../../../supply-chain/warehousing/tasks/create-mobile-device-license-plate-consolidation.md). |
| Paketlenmiş konteynerler için bir serbest bırakma ilkesi oluşturun. | Konteyner serbest bırakıldığında tetiklenen iş otomatik olarak veya el ile oluşturulabilir. Otomatik olduğunda iş, yerleşim yönergesi ve iş şablonu çerçevesi kullanarak konteyner kapatılırken oluşturulur. Serbest bırakma işlemi el ile yapıldığında, paketi yapan kişi işin tek bir konteyner veya konteyner grubu için oluşturulması gerektiğine karar verebilir. Bu özellik, kapalı konteynerlerin hazır olmadan paketleme istasyonundan çekilme ve taşınma riskini azaltır. Ayrıca, sistem tarafından yönlendirilmeyen gruplandırılmış serbest bırakma işlemine de izin verir. |
| Kısa alım yeniden tahsisi | Kısa alım işlemleri desteği, malları çekemeyen ve gerekli madde başka bir konumda mevcutken siparişi yerine getirmek isteyen bir iş arkadaşına yardımcı olmak amacıyla eklenmiştir. Başka bir konumda kullanılabilen malları almak için aynı konum yönergelerini kullanan otomatik yeniden tahsis işlemini kullanabilirsiniz. Alternatif olarak, el ile yeniden tahsis kullanıldığında mobil cihaz, konumların listesini kullanılabilir miktarla birlikte gösterir. Ambar çalışanı stoğun kullanılacağı konumu seçebilir. Bu iki yöntem ayrı ayrı ayarlanabilir veya ambar çalışanı menüsünde tek bir komut olarak birleştirilebilir. El ile yeniden tahsis kullanıldığında, ambar çalışanı kısa çekilen madde miktarını pek çok konumdan çekebilir. Daha fazla bilgi için bkz. [Kısa alım öğesinin yeniden tahsisini ayarlama (Görev kılavuzu)](../../../supply-chain/warehousing/tasks/set-up-short-picking-item-reallocation.md). |
| İlişkili işe sahip stoğu taşıyın. | Artık, ilişkili işe sahip stoğu taşıyabilirsiniz. Bu özellik, örneğin bir çalışan bazı giriş noktası alanlarını temizlemek ve yerine konmayı bekleyen kayıtlı paletleri başka bir giriş konumuna taşımak istiyorsa kullanışlı olabilir. Giriş noktası temizlenir ve daha fazla mal yükü alabilir ve taşınan stok yeni yerine koyma bilgileriyle güncelleştirilir. Bu özellik, ilişkilendirilmiş bir işe sahip olan stoğu taşıyarak ve stok yenileme için yer açarak malzeme çekme konumlarında alan açmak için kullanılabilir. Bu özelliği, ayrıca yükleri bir aşama konumundan bir diğerine oluşturulan yükleme işini kaybetmeden taşımak için de kullanabilirsiniz. Bu şekilde, özellik kamyonlar geldiğinde yüklenmeleri için gereken zamanı en iyi duruma getirmeye yardımcı olabilir. Satış siparişleri, transfer siparişi sorunları, transfer siparişi girişleri ve satınalma siparişleri için rezerve edilen stoğu taşıyabilirsiniz. Taşıma işlemi, satırların bölünmesine neden olacaksa önlenir. Örneğin, bir maddenin 100 parçası için bir iş satırınız varsa bu maddenin yalnızca 30 parçasını başka bir konuma taşıyamazsınız. |
| Kendileriyle ilişkilendirilmiş işe sahip plakaları birleştirin. | Kendileriyle ilişkilendirilmiş giden işe sahip plakaları birleştirebilirsiniz. Örneğin, bir çekme süreci işin pek çok parçasında bölünmüşse, aşama konumuna teslim edildikten sonra plakaların birleştirilmesine izine vermek yararlı olabilir. Plakalar yalnızca aynı konumda olduklarında, aynı yükün üyesi olduklarında ve aynı sevkiyat bilgilerine sahip olduklarında birleştirilebilir. |
| Satır düzeyinde stok yenileme ile ilişkili çekme işini dondurun. | Artık işi başlık düzeyi yerine, satır düzeyinde dondurabilirsiniz. Böylece, çalışanlar talep stok yenilemesi nedeniyle dondurulmamış çekme satırlarını gerçekleştirebilir. Böylece, büyük satış siparişleri olan bir toptancı veya büyük satış siparişleri veya stok yenileme transfer emirleri olan bir perakendeci, çekme işinin stok yenileme işine tabi olmayan tüm satırlarda başlamasına izin verebilir. Çekme ve stok yenileme işi daha sonra paralel olarak tamamlanabilir. Bu özellik, başlık düzeyinde veya satır düzeyinde dondurmayı seçmenizi sağlayacak şekilde yapılandırılabilir. İki yöntemi de kullanabilir ve her yöntem için bir iş şablonu oluşturabilirsiniz. Başlık/satır yapılandırması iş şablonlarında ayarlanır ancak bunu doğrudan oluşturulan iş üzerinden değiştirebilirsiniz. |
| Mobil cihaz kullanarak işi iptal edin. | Artık talep stok yenilemesi olarak veya olmadan, mobil cihaz kullanarak işi iptal edebilirsiniz. Önceden, zengin istemci kullanmanız gerekiyordu. Bu işlevi etkinleştirmek için, modu **Dolaylı** ve etkinlik kodu **İşi iptal et** olarak ayarlanmış bir mobil cihaz menü öğesi oluşturun. |

### <a name="warehouse-operation-enhancements"></a>Ambar işlemi geliştirmeleri

| Yapabilecekleriniz | Bunun önemi |
|-----------------|-----------------------|
| Farklı konteyner türlerini modelleyin. | Depolamayı en iyi duruma getirmek için ve diğer nedenlerle ambardaki farklı konteyner türlerini kullanabilirsiniz. Yeni Konteyner türü varlığı konteyner türlerinin fiziksel özelliklerine sahiptir. Artık plakaları belirli bir konteyner türüyle ilişkilendirebilir ve konum stoklama sınırları kullanabilirsiniz. Örneğin, bu özelliği belirli bir konumda izin verdiğiniz palet (veya diğer konteyner türleri) sayısını denetlemek için kullanabilirsiniz. Alma işlemi için varsayılan konteyner türlerini eklemek için birim sıra gruplarına konteyner türleri de eklenmiştir. Konteyner türleri gelen ve giden konum yönergeleriyle birlikte kullanılabilir. Ayrıca, elde depolanan kaç adet konteyner türü olduğunu belirlemenize yardımcı olmak için eldeki stok görünümünde de kullanılabilir. Daha fazla bilgi için [Ambar yönetimi süreçlerini sürdürmek için bir konteyner türü ile ilişkili plakalar kullanma](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/20/use-of-license-plates-associated-with-a-container-type-to-drive-warehouse-management-processes/) blog gönderisine bakın. Bu blog gönderisi, Microsoft Dynamics AX 2012 güncelleştirmesini açıklıyor olsa da aynı destek Dynamics 365 for Operations için de eklenmiştir. |
| Sevkiyatları geri alın. | Ambarda, son dakika değişikliklerini yönetebilmeniz gerekir. Örneğin, bazı mallar zarar görmüş olabilir ve bu malları sevk edemezsiniz. Alternatif olarak, bir müşteri bir siparişi iptal etmek veya değiştirmek için son anda bir istek yapabilir. Dynamics 365 for Operations şimdi sevkiyatı tersine çevirmenize izin verir. Bu nedenle, sevk irsaliyesini iptal edebilir ve daha sonra doğru miktarlarla güncelleştirebilirsiniz. Benzer şekilde, gelen akışta ürün girişlerini iptal edebilir ve güncelleştirilmiş sürümü oluşturabilirsiniz. |
| Karma maddelerin bulunduğu paletler kullanın. | Artık "karma" palet alabilir ve kaydedebilirsiniz. Karma palet, bir veya birden fazla satınalma siparişi veya satırı için tek bir palet üzerinde toplanmış farklı maddelerden oluşur. Tüm kayıtlar tek bir hedef plaka ile özetlenebilir. Bu işlem, ambar mobil cihazı üzerinden etkinleştirilir. Örneğin, karma maddelerin bulunduğu bir palet ambara ulaştığında, teslim alma memuru palet kendine ayrılan konumlara çekilmeden önce paletteki maddeleri ve miktarları belirler. Yerine koyma konumları iş şablonları ve konum yönergelerine göre tanımlanır. Yerine koyma konumları sabit yerleşimleri olan birkaç maddeye yayılmışsa bu özellik, karma palet üzerindeki farklı madde sayısı kadar iş satırı oluşturur. Bu özellik, alınan karma madde paletlerinin kaydını ve yerine koyulmasını daha hızlı ve daha esnek hale getirir. Daha fazla bilgi için [Bir plaka kullanarak karma kaynak belge satırları olan paleti alma ve kaydetme](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/13/receive-and-register-a-pallet-with-mixed-source-document-lines-using-1-license-plate-purchase-order-matching/) blog gönderisine ve [en yeni toplu güncelleştirme duyurusu](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/30/whats-new-in-cu11-for-wms-and-tms/) içindeki karma palet desteği hakkındaki bilgilere bakın. Bu blog gönderisi, AX 2012 güncelleştirmesini açıklıyor olsa da aynı destek Dynamics 365 for Operations için de eklenmiştir. |

### <a name="minor-feature-enhancements-in-supply-chain-management"></a>Tedarik zinciri yönetiminde küçük özellik geliştirmeleri

<table>
<thead>
<tr>
<th>Yapabilecekleriniz</th>
<th>Bunun önemi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Verileri içe ve dışa aktarmak için yeni veri varlıklarını kullanın.</td>
<td>Verileri şu veri varlıklarını kullanarak içe ve dışa aktarabilirsiniz:
<ul>
<li>Navlun faturası</li>
<li>Ambara ve stok durumuna göre eldeki toplam</li>
<li>Stok masrafları</li>
<li>Teklif</li>
</ul>
</td>
</tr>
<tr>
<td>Etkileşimli zamanlama senaryoları geliştirmek için gelişmiş Gantt denetimini kullanın.</td>
<td>Gelişmiş Gantt denetimi, yeni etkileşimli zamanlama senaryoları geliştirmenizi ve etkinliklerin görünümünü özelleştirmek için kullanılabilecek gelişmiş API'ler sunmanızı sağlar. Yeni API'lerden bazıları şunlardır:
<ul>
<li>Dikey sürükle ve bırak etkinlikleri</li>
<li>Ekleme/kaldırma etkinlikleri</li>
<li>Ayrılan dönemleri özet çubuğunda önizleme</li>
<li>Etkinlik kenarlıklarının rengini ve stilini değiştirme</li>
<li>Kılavuzdaki metnin rengini, stilini ve arka planını değiştirme</li>
</ul>
</td>
</tr>
<tr>
<td>Malzeme ve kaynak planlamasını daha iyi yönetin.</td>
<td>Malzeme ve kaynak planlamasında birkaç geliştirme yapılmıştır:
<ul>
<li>Çıkış marjı artık bir madde elde olduğunda işlenir.</li>
<li>Planlanan siparişleri kesinleştirdiğinizde teslimat tarihini geçersiz kılın.</li>
<li>Siparişlerin gerçekleştirilmesine, emniyet stoğundan daha yüksek öncelik verin.</li>
<li>Geçmişte planlanan siparişlerin zamanlanmasını önleyin.</li>
</ul>
</td>
</tr>
<tr>
<td>Üretim için fiili tüketimi bildirin ve stok durumunu görüntüleyin.</td>
<td>Üretim için fiili tüketimi görüntüleyebilirsiniz. Ayrıca, <strong>İş oluşturma</strong> menü öğesindeki <strong>Hareket</strong>'e eklenen yeni <strong>Stok durumunu görüntüle</strong> onay kutusu stok durumunu görüntülemenizi sağlar.</td>
</tr>
<tr>
<td>Sevkiyat taşıyıcınızın oranları hacimsel ağırlığı temel alıyorsa, hacimsel ağırlığı hesaplayın.</td>
<td>Hacimsel ağırlığa dayalı yeni bir TMS değerlendirme altyapısı eklenmiştir, böylece hacimsel ağırlığı hesaplayabilirsiniz.</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Ek kaynaklar

[Finance and Operations giriş sayfasındaki yenilikler veya değişiklikler](whats-new-changed.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]