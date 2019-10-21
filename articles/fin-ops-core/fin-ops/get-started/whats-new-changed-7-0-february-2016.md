---
title: Dynamics AX 7.0'daki yenilikler ve değişiklikler (Şubat 2016)
description: Bu makale Microsoft Dynamics AX 7.0'da yeni veya değişen özellikler açıklanmaktadır. Bu sürüm, platform ve uygulama özellikleri içerir ve Şubat 2016'da yayımlanmıştır.
author: sericks007
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57e88285c29d13001d5c5586ec4ad8674973f256
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180461"
---
# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a>Dynamics AX 7.0'daki yenilikler ve değişiklikler (Şubat 2016)

[!include [banner](../includes/banner.md)]

Bu makale Microsoft Dynamics AX 7.0'da yeni veya değişen özellikler açıklanmaktadır. Bu sürüm, platform ve uygulama özellikleri içerir ve Şubat 2016'da yayımlanmıştır.

## <a name="cost-management"></a>Maliyet yönetimi

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Stoka bakiyesi, süren iş (WIP) stok bakiyesi ve seçili mali yıl için stok girişi ve çıkışının ne olduğu hakkında genel bir bakış edinin.</td>
<td>Geçerli değil</td>
<td><strong>Maliyet yönetimi</strong> çalışma alanı seçili mali dönem için stok ekstresinin veya süren iş (WIP) stok ekstresinin sunulduğu bir bölüm içerir. Ekstre, varsayılan olarak her 24 saatte bir güncelleştirilen bir veri kümesi önbelleğini temel alır. Veri kümesi önbelleği, kullanıcıların el ile gerçek zamanlı raporlama için güncelleştirebileceği şekilde yapılandırılabilir. <strong>Maliyet yönetimi</strong> çalışma alanı içindeki <strong>Veri yenileme durumu kartı</strong> önbelleğin en son ne zaman güncelleştirildiğini gösterir.</td>
<td>Maliyet denetleyicileri stok veya süren iş stok ekstresi bakiyesinin zamanla arttığını mı azaldığını mı öğrenmek isterler. Çalışma olaylarını ekstrede sınıflandırarak, maliyet denetleyicisi stokun nasıl aktığı konusuna genel bir bakış elde edebilir. Stok veya süren iş stoğu standart maliyetler tarafından değerlendirilirse, kayıtlı toplam fark da görülebilir.</td>
</tr>
<tr>
<td><strong>Maliyet yönetimi</strong> modülünü kullanın.</td>
<td>Geçerli değil</td>
<td>Maliyet yönetimi bir etki alanı olarak sunulur. Maliyet ile ilgili yapılandırma ve içgörü Stok yönetimi, Üretim kontrolü ve Borç hesaplarına dağılmıştır.</td>
<td>Maliyet yönetimi ile ilgili tüm görevler bir modül içinde merkezileştirildiği için, maliyet denetleyicilerinin sistemi korumaları daha kolay olacaktır.</td>
</tr>
<tr>
<td>Stok muhasebesi ve üretim muhasebesi ile ilgili deftere nakil tiplerini güncelleştirildi.</td>
<td><strong>InventPosting</strong>, <strong>Resource</strong>, <strong>ResourceGroup</strong> ve <strong>ProductionGroup</strong> formları içindeki etiketler her zaman gerçekte kullanılan <strong>LedgerPostingType</strong> etiketi ile hizalanmış değildirler. Etiketlerde kullanılan terminolojiyi anlamak kolay değildir.</td>
<td>Etiketler, <strong>InventPosting</strong>, <strong>Kaynak</strong>, <strong>ResourceGroup</strong> ve <strong>ProductionGroup</strong> üzerindeki etiketlerin <strong>LedgerPostingType</strong> gerçek etiketleri ile uyumlu olması için güncelleştirilmiştir. Ayrıca tüm etiketler operasyonel olaylar ile eşleşebilmeleri için yeniden adlandırılmıştır. Gerçek deftere nakil mantığının değişmediğini unutmayın.</td>
<td>Bu deftere nakil türünü kullanan çalışma olayları ile yeni etiketler birbiriyle ilişkilendirildiğinden, sistemi yapılandırmak daha kolaydır.</td>
</tr>
<tr>
<td>Satınalma fiyatı, maliyet veya satış fiyatını Microsoft Excel'den maliyet sürümüne içeri veya dışarı aktarın.</td>
<td>Veri modeli InventDim kimliği gerektirdiğinden, fiyatları veya maliyetleri maliyetlendirme sürümüne doğru şekilde alamazsınız.</td>
<td>Veri varlıklarının sunulması, bir alma/verme özelliğini uygulamayı mümkün kılar. Bu özellik kullanıcıların fiyatları bir maliyetlendirme sürümüne içeri almalarına veya dışarı aktarmalarını sağlar.
<ul>
<li>Satınalma bölümünden elde edilen bir sonraki yılın Satınalma fiyatlarının tam listesini içeri alma.</li>
<li>Merkezden gelen maliyetleri ya da standart fiyatları bir operasyondaki bir ya da birden fazla satış şirketine itin.</li>
</ul></td>
<td>Bu maliyet denetleyicilerine özellikle de bundan sonra mali yıl için önceden belirlenmiş maliyetleri korumak zorunda olduklarında büyük ölçüde vakit kazanmalarını sağlar.</td>
</tr>
<tr>
<td>Bir maliyet nesnesinin stok bakiyesi ve ortalama birim maliyetine hızlı bir genel bakış atın.</td>
<td>Kullanıcı, eldeki formu açmak ve maliyet nesnesini yansıtan stok boyutlarını seçmek zorundadır. Bu nedenle, kullanıcının belirli bir ürün için hangi stok boyutlarının mali stok için işaretlendiğini bilmesi gerekir.</td>
<td>Yeni bir <strong>Maliyet nesnesi</strong> sayfası kullanıma sunulmuştur. Varsayılan olarak, bu sayfa ürünle ilgili tüm maliyet nesneleri gösterir. Bu sayfa geçerli stok miktarını, değerini ve maliyet nesnesi başına düşen ortalama birim maliyetini gösterir.</td>
<td>Bu karmaşıklığın bir kısmını kaldırır ve maliyet denetleyicisinin işini kolaylaştırır.</td>
</tr>
<tr>
<td>Stok denetimi sırasında yeni <strong>Maliyet girişleri</strong> sayfasını kullanın.</td>
<td>Aynı hareketler fiziksel veya mali olabileceğinden dolayı, kayıtlı stok hareketleri ve ilgili kapatmaların üzerinde stok denetimi gerçekleştirmek karmaşık olabilir.</td>
<td><strong>Maliyet girişleri</strong> sayfası stok hareketlerini görüntülemek için yeni bir yol sunar.
<ul>
<li>Hareketler tarih sırasına göre gösterilir.</li>
<li>Sadece maliyetlere katkıda bulunan hareketler dahil edilir.</li>
<li>Fiziksel maliyet veya finansal maliyet kavramı yoktur.</li>
<li>Fiziksel miktar veya finansal miktar kavramı yoktur.</li>
<li>Maliyetleri artımlı olarak eklenir.</li>
</ul></td>
<td>Bu, maliyet denetleyicilerinin stok işlem düzeyinde denetim gerçekleştirmeleri gerektikleri zaman önemli miktarda zaman kazandırabilir.</td>
</tr>
<tr>
<td>Belirli bir ürün için birikmiş maliyetlerin özet görünümünü görüntülemek amacıyla yeni <strong>Üretim süren iş raporu</strong> iletişim kutusunu kullanın.</td>
<td>Geçerli değil</td>
<td>Süren iş raporu belirli bir üretim emrinin özetlenmiş süren iş bakiyesini, uygun maliyet sınıflandırmaları içinde gruplandırılmış şekilde gösterir. Bir grafik, işlem deftere nakillerinin süren iş bakiyesini nasıl etkilediğini kronolojik olarak gösterir.</td>
<td>Bu, belirli bir üretim emrindeki mevcut süren iş bakiyesinin ne olduğunu veya emirde ne kadar malzeme tüketildiğini bilmeleri gerektikleri zaman, maliyet denetçilerine bir hayli zaman kazandırır.</td>
</tr>
<tr>
<td>Üretim siparişlerinde yeni sunulan maliyet karşılaştırma görüntüleme özelliğini kullanın. Bu özellik, bir üretim emriyle ilişkili maliyetleri karşılaştırmayı kolaylaştırır.</td>
<td>Kullanıcı yalnızca tahmini maliyetleri ve gerçekleşmiş maliyetleri karşılaştırabilir. Karşılaştırma en alt düzeyde yapılabilir.</td>
<td>Maliyet karşılaştırma özelliği maliyet denetleyicilerinin aşağıdaki verileri karşılaştırmalarını sağlar:
<ul>
<li>Etkin maliyet, tahmini maliyet kıyaslaması = Planlama farkı</li>
<li>Tahmini maliyet, gerçekleşmiş maliyet kıyaslaması = Üretim farkı</li>
<li>Planlama farkı + Üretim farkı = Toplam fark</li>
</ul>
Bu özellik, üretilen maddeye atanan maliyetlendirme yöntemlerinden bağımsız olarak çalışır. Varsayılan olarak, grafik maliyet grubu türünde maliyet karşılaştırmasını gösterir. Grafik, kullanıcıların daha ayrıntılı düzeylere inmesine izin verir.</td>
<td>Bu, maliyet denetleyicilerinin veya üretim yöneticilerinin üretim farklarının nereden geldiklerini ve neden kaynaklandıklarını görmelerini sağlar.</td>
</tr>
</tbody>
</table>

## <a name="developer"></a>Geliştirici

| Ne yapabilirsiniz? | Dynamics AX 2012 | Dynamics AX 7.0 | Bu neden önemlidir? |
|------------------|------------------|-----------------|------------------------|
| Birçok aygıt üzerinden erişilebilir web tabanlı çözümleri bulutta oluşturun. | Uygun değil | Dynamics AX'in geçerli sürümü yeni bir web tabanlı istemci ve istemci çerçevesini dayanır. | Son kullanıcılarınıza yeni nesil çözümler sağlayabilirsiniz. |
| Çözümlerinizi geliştirmek için Microsoft Visual Studio'yu kullanın. | Microsoft MorphX ana geliştirme ortamı olmakla birlikte, bazı geliştirme Visual Studio'da gerçekleşir. | Visual Studio, tek geliştirme ortamıdır. | Bilinen Dynamics AX 2012 kavramlarını korur ve Visual Studio çerçevesi ve kipleri ile sorunsuz şekilde uyum sağlar. Diğer .NET dilleri ve projeleri ile de standart birlikte çalışabilirliği sağlar. |
| Ortak Ara Dil'in (CIL) tüm özellikleri için derleyin. | X++ p-kod'a derlenir. | Yeni X ++ derleyicisi tüm özellikler için CIL oluşturur. CIL diğer .NET tabanlı diller tarafından kullanılan aynı ara dilidir. | CIL daha hızlıdır, verimli bir şekilde dinamik bağlantı kitaplıkları (DLL'ler) ile yönetilen sınıflarda referans yapabilir ve .NET'in geniş araç tabanında çalışabilir. |
| İş Zekası (BI) raporlarını ve görsel öğelerini Microsoft Dynamics AX istemcisinde gömün. | Uygun değil | Son derece sezgisel ve akıcı görsel öğeler oluşturun. | BI temel alarak karar verme içgörüleri sağlar. |
| Microsoft Office'le Tümleştir. | Uygun değil | Yeni yeteneklere Excel Veri Bağlayıcısı uygulaması **Çalışma Kitabı Tasarımcısı** sayfası, API dışa aktarma ve Belge yönetimi dahildir. | Son kullanıcılarınız için üretkenlik çözümleri oluşturabilirsiniz. |
| Derleme, sınama ve dağıtımı otomatikleştirin. | Kısmen uygun | Geliştirici topolojisini, Geliştirici ve VM Derleme'sini kullanarak dağıtın. Keşfedilecek VM Derlemesini otomatik olarak yapılandırın, Visual Studio Online (VSO) üzerinden modülleri oluşturun ve testleri çalıştırın. C\## ve X++ modül derlemesi ve referansları destekleniyor. | Bu, sınama ve doğrulama için maliyeti ve çabayı azaltarak geliştirici verimliliğini artırır. |
| Üst katman oluşturma ve uzantılar ile özelleştirin. | Uzantılar mevcut değildir. | Dynamics AX'in geçerli sürümünün yeni bir özelleştirme modeli vardır. | Microsoft veya üçüncü taraf Microsoft iş ortakları tarafından sevk edilmiş olan model öğelerinin kaynak kodu ve meta verilerini özelleştirebilirsiniz. |
| Yeni denetimleri ve kullanıcı arabirimi öğelerini X++ ve modern web çerçevesi kullanarak oluşturun. | Özel denetimler Microsoft ActiveX ve Windows Presentation Foundation (WPF) gibi dış çerçeveleri temel alır. | Geçerli sürümde denetimleri oluşturmak daha kolaydır. X++ framework uygulama davranışı ve iş mantığı için kullanılabilir ve bir HTML/JavaScript tabanlı istemci modern görseller sağlar. | Denetimleriniz, Dynamics AX kullanıma hazır (OOB) denetimleri gibi görünmek ve davranmak üzere tasarlanabilir. |
| Yeni araçları kullanarak değerlendirme yapın performansı ayarlayın. | PerfSDK, Beri genişletme araç seti, Trace Parser WEb app ve PerfTimer kullanılamaz. | PerfSDK, Veri Genişletme Araç Seti, Trace Parser Web app ve PerfTimer yenidir. | Yazılım Geliştirme Seti (SDK), tüm önemli iş süreçlerini tek kullanıcı ve (varsa) çok kullanıcılı test çalışmasına test ve performans için doğrulama sağlar. Veri genişletme Toolkit, ana veri ve işlem verilerinin doğru şekilde genişletilmiş olması gereken tüm performans testlerini doğru olarak genişletmenizi sağlar. İzleme Ayrıştırıcısı, tek kullanıcılı performans testini veya çok kullanıcılı çalışmayı doğrulamanızı sağlar. PerfTimer, herhangi bir sorgunun veya herhangi bir özel yöntem çağrısının bir performans sorununa neden olup olmadığını görmenizi sağlar. Bu nedenle, bir izleme almanıza ve her şeyi ayrıntılı analiz etmenize gerek kalmaz. |
| Güncelleştirilebilir görünümü OData kullanarak ortaya çıkarın. | Uygun değil | Dynamics AX'in geçerli sürümü, Dynamics AX verilerine erişimi geniş bir istemci yelpazesinde, tutarlı bir şekilde sağlayan bir ortak OData hizmet bitiş noktasını tanıtır. | Çözümleriniz RESTful hizmetler ile etkileşimde bulunabilir, keşfedilebilir bir şekilde veri paylaşabilir ve HTTP Protokolü Yığını'ı kullanarak geniş tümleştirmeyi etkinleştirebilir. |
| İş mantığı yazmak ve tümleştirme senaryolarını desteklemek için business connector'dan yararlanın. | Business connector, yönetilen koddan X++ koduna çağrılabilir. Business connector'ı tümleştirme senaryoları için değil, yalnızca C\# içinde iş mantığı yazmak için kullanmanızı öneririz. | Business connector artık desteklenmemektedir. Geliştirme gereksinimi X++ yönetilen kod için derlenmiş olduğundan sağlanır. Bu nedenle, birlikte çalışma daha kolay olur. Tümleştirme senaryoları OData kullanılarak gerçekleştirilir. | Gelecekte business connector'u kullanamazsınız. |
| Ölçek (diğer bir deyişle, ondalık basamak sayısı) gerçek veritabanı alanlarında ve genişletilmiş veri türlerinde (EDTs) seçin. | Ölçek 16 varsayılan ölçektir ve geliştirici tarafından değiştirilemez. | EDTs ve alanlar artık tekil alana ve EDT'ye uygulanabilecek bir ölçek özelliğine sahiptir. Varsayılan 6 olarak ayarlanmıştır, 16 değil. | Daha küçük bir ölçek kullanıldığında NCCI tablolarının (SQL bellek desteği) performans ile kat ve kat daha hızlıdır. Ölçeği tekil alanlarınızın ihtiyaç duyduğu şekilde değiştirin. |

## <a name="financial-management"></a>Mali yönetim

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Hesap yapılarını Microsoft Excel'e dışa aktar.</td>
<td>Uygun değil</td>
<td>Şimdi bir hesap yapısı seçip, Excel'e aktarabilirsiniz.</td>
<td>Birçok müşteri daha kolay filtreleme için hesabı yapılarını Excel'e aktarma özelliğini talep etmişlerdir.</td>
</tr>
<tr>
<td>Defterler ve tek bir sayfada bir hesap yapısı ile ilişkili gelişmiş kural yapılarını görüntüleyin.</td>
<td> Kullanılan genel muhasebe ve hesap yapısını görmek için kullanıcının birden fazla form arasında gezinmesi gereklidir.</td>
<td>Bilgi kutuları hesap yapısı sayfasına eklenmiştir.</td>
<td>Hesap yapıları tanımlandığında ve düzenlendiğinde, önemli bilgilere erişmek daha kolaydır.</td>
</tr>
<tr>
<td>Bir hesap planı ile ilişkilendirilmiş olan defterleri tek bir sayfada görüntüleyin.</td>
<td>Kullanıcı, her şirkete gidip, genel muhasebeye atanan hesap planını görmek için genel muhasebe formunu açmalıdır.</td>
<td>Bilgi kutuları <strong>Hesap planı</strong> sayfasına eklenmiştir.</td>
<td> Hesap planı tanımlandığında ve atandığında, önemli bilgilere erişmek daha kolaydır.</td>
</tr>
<tr>
<td><strong>Mizan</strong> listesi sayfasında, kapanış sayfa ayarlamalarını ve kapanış hareketlerini ayrı sütunlarda görüntüleyin.</td>
<td>Kullanıcı her iki hareket türünü tek bir sütunda görür.</td>
<td>Ek bir parametre <strong>Mizan</strong> listesi sayfasına eklenmiştir.</td>
<td>Bu daha kısa veri analizine izin verir ve ayrıca bazı ülkelerde/bölgelerde yasal raporlama için gereklidir.</td>
</tr>
<tr>
<td>Yeni <strong>Global genel günlük</strong> sayfasını kullanın.</td>
<td>Uygun değil</td>
<td>Genel günlükleri girmek için yeni <strong>Global genel günlük</strong> sayfası. Bu sayfa için ayrıcalıklar <strong>Muhasebeci</strong> rolüne eklenir.</td>
<td>Formdan çıkmadan veya şirket bağlamını değiştirmeden paylaşılan hizmet muhasebecisinin yevmiye defterlerini şirketler arasında girmesini olanaklı hale getirir.</td>
</tr> 
<tr>
<td>Yeni <strong>Muhasebe kaynağı gezgini </strong>sayfasını kullanın.</td>
<td>Dynamics AX 2012 R3 CU10'dan kullanılabilir.</td>
<td><strong>Mizan</strong> listesi sayfası ve <strong>Fiş hareketleri</strong> sayfasından gitmek için yeni <strong>Muhasebe kaynağı gezgini</strong> sayfası ve eylemler.</td>
<td>Genel muhasebede bir mizan veya muhasebe girişi için veya ad-hoc analizleri için kaynak hakkında en ayrıntılı bilgilerin görüntülenmesini mümkün kılar.</td>
</tr>
<tr>
<td>İlave nakil katmanlarını ekleyin.</td>
<td>İlave nakil katmanlarını ekleyerek bir geliştirici deneyimi elde edilmiştir.</td>
<td>Artık on nakil katmanı kullanılabilir.</td>
<td>Müşterilerin çoğu ilave nakil katmanları ekler.</td>
</tr>
<tr>
<td>İlgili fiş seçeneğini kullanın.</td>
<td>Uygun değil</td>
<td>İlgili fiş seçeneği şirketlerarası hareketleri naklederken kullanıcıların mahsup şirketinde fişi görüntülemelerini sağlar. Kullanıcılar ilgili fişlerden ayrıntılara tıklayabilir ve mahsup şirketi fişine hızla atlayabilirler.</td>
<td>Kullanıcılar şirketlerarası hareketleri naklederken mahsup şirketine nakledilen fişi görüntüleyemez veya izleyemezdi.</td>
</tr>
<tr>
<td>Toplu mali dönem kapatma</td>
<td>Uygun değil</td>
<td>Kullanıcılar birden fazla şirket için aynı anda modül erişimini güncelleştirebilir ve dönem durumunu değiştirebilirler.</td>
<td>Özellikten önce kullanıcılar oturum açtıkları şirketi değiştirmeli, genel muhasebe defteri takvim formuna gitmeli ve modül erişimini ve dönem durumunu el ile güncelleştirmeliydi.</td>
</tr>
<tr>
<td>Oanda tarafından güçlendirilen döviz kurlarına sahiptir.</td>
<td>Oranları Oanda'dan içe aktarmak için döviz kurları sağlayıcısını yapılandırarak bir geliştirici deneyimi elde edilmiştir.</td>
<td>Kullanıcıların Oanda için anahtarı varsa döviz kuru sağlayıcısını yapılandırırken bunu girebilirler.</td>
<td>Kullanıcılar, planlanmış bir temel üzerinden içe aktarılan Oanda tarafından güçlendirilmiş döviz kurlarına sahip olarak temel işlevlerden yararlanabilirler.</td>
</tr>
<tr>
<td>Mali raporları (Yönetim Raporlayıcısı) boyutlar, öznitelikler, tarihler ve senaryolara göre filtreleyin.</td>
<td> Management Reporter raporlarının tüm filtrelemesi, rapor tasarımı tarafından yönetilir. Örneğin, görüntüleme ayrıcalıklarına sahip bir kullanıcı farklı bir tarihe ait raporu görüntülemek isterse, bir rapor tasarımcısının değişikliği yapması gerekir.</td>
<td>Rapor seçenekleri eklenerek, bir kullanıcı rapor görüntülerken farklı filtrelerin uygulanabilmesi sağlanmıştır. Bu filtrelere göre yeni bir rapor oluşturulur.</td>
<td>Finansal raporların tüketicileri, rapor tasarımları için güncelleştirmeye gerek kalmadan boyutlar, tarihler, öznitelikler ve senaryolar için farklı filtreler uygulayabilirler.</td>
</tr>
<tr>
<td>Finansal raporları (Management Reporter) Microsoft Dynamics AX istemcisi içinde görüntüleyin.</td>
<td>Management Reporter raporlarını görüntülemek için ayrı bir web istemcisi kullanılırdı.</td>
<td>Tüm finansal raporlara Dynamics AX istemcisinde erişilebilir. Kullanıcı görüntülemek için bir raporu seçer ve rapor istemci uygulamasında görüntülenir.</td>
<td>Artık farklı bir istemci/uygulamaya erişmek zorunda kalmadan mali raporları görüntüleyebilirsiniz.</td>
</tr>
<tr>
<td>Finansal raporları (Management Reporter) Microsoft Dynamics AX istemcisinden yazdırın.</td>
<td>Bir raporu yazdırmak için tarayıcının yazdırma seçenekleri kullanılır ve yalnızca kullanıcının ekran üzerinde görebildiği yazdırılır.</td>
<td>Kullanıcı Dynamics AX istemcisi içindeki mali raporda Yazdırma seçeneğini kullanarak ayrıntı düzeyini ve sayfa ayarını seçebilir.</td>
<td>Raporlar bir web sayfasını yazdırmak yerine kullanıcıların beklediği şekilde yazdırılır.</td>
</tr><tr>
<td>Power BI "Finansal performansı izle" içeriği kullanarak mali verileri çözümleyin.</td>
<td>Uygun değil</td>
<td>PowerBI.com üzerinde <strong>Veri Al</strong> ve sonra <strong>Dynamics AX – finansal performans</strong> içerik paketini seçin. Dynamics AX bitiş noktası URL'sini verilerinizin panoda yansıtılması için girin.</td>
<td>Kuruluşlar üç veya dört tıklatma ile önemli finansal verileri içeren bir Power BI Pano'su dağıtabilirler. İçerik organizasyon tarafından kişiselleştirilebilir.</td>
</tr>
<tr>
<td>Mali dönem kapanış işlemlerini izleme.</td>
<td>Uygun değil</td>
<td>Kapanış şablonları ve zamanlamaları, Mali dönem kapatma yapılandırması kullanılarak oluşturulabilir. <strong>Mali dönem kapanışı</strong> çalışma alanını kullanarak şirketler arasında kapatma zamanlamalarının ilerlemesini izleyin.</td>
<td>Bu çalışma alanı, aktivitelerin tanımlanması, zamanlanması ve iletişiminin kurulması için el ile sistemleri ortadan kaldırır. Bu nedenle, kapatmak için gerekli gün sayısı azalır.</td>
</tr>
<tr>
<td><strong>Genel muhasebe bütçeleri ve tahminleri</strong> çalışma alanını ve ek sorgu formlarını kullanarak bütçe ile fiili değerlerin karşılaştırmalarını izleyin ve muhasebe tahminleri oluşturun.</td>
<td>Uygun değil</td>
<td> Çalışma alanına Dynamix AX panosundan erişilebilir. Birçok yeni sorgulama sayfalarına bağlantılar içerir: <strong>Gerçek tutar-bütçe karşılaştırma özeti</strong>, <strong>Bütçe denetimi istatistik özeti</strong>, <strong>Bütçe kayıt girişleri</strong>, ve <strong>Bütçe planları</strong>.</td>
<td>Yeni sorgu sayfaları, bütçe bilgilerine kolay erişim sağlar. Çalışma alanı, tüm bütçe bakım ve izleme görevlerini, bütçe yöneticileri veya muhasebe yöneticilerinin kolay kullanabilecekleri tek bir yerde birleştirir.</td>
</tr>
<tr>
<td>Tahminler ve bütçe planları için düzenler oluşturun.</td>
<td><strong>Bütçe planı</strong> belgesi, mali boyutların kombinasyonları için geçerli tarihler ve tutarlara sahip satırlar listesi olarak görüntülenir. Kullanıcı, bütçe planını bir PivotTable içerisinde görüntülemek için Excel şablonları oluşturmak ve kullanmak zorundadır.</td>
<td>Bütçe planları ve tahminleri için sınırsız sayıda düzen mevcuttur. Seçili mali boyutları, kullanıcı tanımlı sütunları ve diğer satır niteliklerini (örneğin: yorumlar, projeleri ve varlıkları) düzen içinde birleştirebilirsiniz. Kullanıcılar bütçe planı belge düzenini kolayca değiştirebilirler ve herhangi bir seçili düzeni kullanarak verileri düzenleyebilirler. Bütçe planlamanın yapılandırması, senaryo kısıtlamalarını ortadan kaldırarak ve bütçe planı belgesinin her aşamasında hangi verinin görüntülenebilir ve düzenlenebilir olduğunu tanımlayarak basitleştirilmiştir.</td>
<td>Hem Excel hem de Dynamics AX istemcisi kullanarak bütçe planlarını oluşturmada ve düzenlemede esneklik sağlar. Bütçe plan düzen kurulumu kullanarak Excel çalışma kitapları için şablonlar oluşturulabilir.</td>
</tr>
<tr>
<td><strong>Satıcı Fatura hareketleri</strong> raporunu, vadesi geçmiş günleri içeren <strong>Ayrıntılı vade günü listesi</strong> raporundan gelen verileri kullanarak yazdırın.</td>
<td>İki farklı rapor yazdırmanız gerekir: <strong>Ayrıntılı vade günü listesi</strong> ve <strong>Satıcı Fatura hareketleri</strong>.</td>
<td>İki rapor üzerindeki <strong>Satıcı Fatura hareketleri</strong> raporuna birleştirilmiştir. <strong>Ayrıntılı vade günü listesi</strong> raporu kaldırıldı.</td>
<td>Bu, iki ayrı fakat birbiriyle ilgili raporu yazdırma gereksinimini ortadan kaldırır.</td>
</tr>
<tr>
<td>Mevzuat raporlarını doğrudan PDF formatında oluşturun.</td>
<td>Önce Mevzuat raporunu bir biçimde oluşturmanız ve sonra PDF formatında dışa aktarmanız gerekir.</td>
<td>Mevzuat raporlar için varsayılan biçim, PDF biçimidir.</td>
<td>Hem bilgisayar ekranı hem kağıda yazdırılan kopyada birleşik bir görüntü deneyimi sağlar.</td>
</tr>
<tr>
<td>Satış vergisi kapatma işlemi bir toplu işlem olarak çalıştırmak.</td>
<td>Uygun değil</td>
<td><strong>Satış vergisi kapatma dönemi</strong> sayfası üzerinde, kapatma işleminin toplu modda çalıştırılması gerektiğini belirtebilirsiniz.</td>
<td>Birçok vergi hareketleri olan dönemler için kapatma işlemi zaman kaybı olabilir ve işlemi bir toplu işlem olarak arka planda çalıştırmak daha yararlı olabilir.</td>
</tr>
</tbody>
</table>

## <a name="foundation"></a>Vakıf

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td>İstemciye her zaman ve her yerden erişin.</td>
<td>AX 2012 masaüstü istemcisi tam bir dizi formlar sağlar, ancak yalnızca Microsoft Windows üzerinde çalışan bilgisayarlarda kullanılabilir ve kurulum gerektirir. Terminal Sunucusu genellikle masaüstü istemcisi ile bir geniş alan ağı (WAN) üzerinden erişim sağlamak için kullanılır. Enterprise Portal web istemcisi, azaltılmış formlar sağlar.</td>
<td>Bu iki AX 2012 istemcisi, masaüstü istemcisinin işlevselliğini, Kurumsal Portal istemcisinin erişimi ile birleştiren, standartlara dayalı bir web istemcisi ile değiştirilmiştir.</td>
<td>Bu da geliştirme çabalarının iki farklı kullanıcı arabirimi arasına ayrılmasını engeller. Standart bir web arabirimi kullanarak, terminal sunucusu gereksinimini ortadan kaldırır.</td>
</tr>
<tr>
<td>Yeni bir Görev Kaydedici'si kullanarak üretken olun.</td>
<td>AX 2012 Görev Kaydedici'si, bir uygulama nesne sunucusu (AOS) bilgisayara ve yükseltilmiş yetkilere doğrudan erişime ihtiyaç duyar ve hiçbir düzenleme seçeneği sunmaz.</td>
<td>Yeni Görev Kaydedici doğrudan web istemcisinde kullanılabilir. Görev Kaydedici'ye erişim yönetici ayrıcalıkları gerektirmez. Kaydedilmiş adımlar kaydettiğiniz esnada canlı olarak izlenebilir, yeni düzenleme seçenekleri sunulmuştur ve görev kaydedici, varolan iş süreci modelleyici (BPM) senaryolarının yanı sıra daha fazla senaryo destekler.</td>
<td>Yeni Görev Kaydedici, kolaylaştırılmış bir deneyim sunar ve Dynamics AX üzerinde yeni yetenekler sağlar. Bu yeteneklerin bazıları şimdi kullanılabilir ve daha fazlası takip edecektir.</td>
</tr>
<tr>
<td>Çalışma alanları ile kullanıcıların bekleyen işlerini daha iyi anlamalarına yardımcı olur.</td>
<td>Rol merkezleri işletme veya kuruluştaki kullanıcının iş işlevine ait bilgilere genel bakış sağlar.</td>
<td>Çalışma alanları, Dynamics AX'te görevlere ve belirli sayfalara gitmenin ilk yolu olan rol merkezlerini değiştirme amaçlı yeni bir kavramdır. Bunlar bir iş faaliyetine tek sayfalık bir genel bakış sağlarlar ve kullanıcıların mevcut durumu, yaklaşan iş yükünü ve işlem veya kullanıcının performansını anlamalarına yardım ederler. Çalışma alanları AX 2012 rol merkezlerinden daha ayrıntılıdır ve bir kullanıcı birden çok çalışma alanı erişimine sahip olabilir.</td>
<td>Çalışma alanları, kullanıcı üretkenliğini artırma amaçlıdır. Geliştiriciler üründe desteklenen her önemli "faaliyet" için bir çalışma alanı oluşturmalıdır. Eski AX 2012 rol merkezleri genel olarak Dynamics AX'in geçerli sürümünde birden çok çalışma alanı ile değiştirilir.</td>
</tr>
<tr>
<td>Formları tarayıcı görünüm penceresi veya cihaz boyutuna duyarlı hale getirin.</td>
<td>AX 2012'de form içeriği sütunlar kullanılarak kesin bir şekilde düzenlenmiş ve genel form yüksekliği/genişliği form üzerindeki denetimlere göre büyük ölçüde tespit edilmiştir.</td>
<td>En son Dynamics AX'te web'e geçişle birlikte bir formun boyutları şu anda tarayıcı görünüm penceresi boyutunu veya cihazı temel alır. Görünüm penceresi boyutundaki değişikliklere daha iyi yanıt vermek için denetimler ve düzen parametreleri değiştirilmiş veya eklenmiştir.</td>
<td>Tarayıcı veya cihazın mevcut yüksekliğini/genişliğini en uygun şekilde kullanmak için form içeriğinin daha duyarlı olması gerekir. Duyarlılığa ulaşmak için formun modellendiği yöntemin değiştirilmesi gerekebilir.</td>
</tr>
<tr>
<td>Gelişmiş bir form geliştirme deneyimi için modelleri kullanın.</td>
<td>Form stiline dayalı AX 2012'de form şablonları form geliştirme için başlangıç noktaları olarak kullanılıyordu. İsteğe bağlı eklenti Form Stili Denetleyicisi bir formun ilgili şablondan nasıl nakledildiğine dair bilgi verir.</td>
<td>Dynamics AX'in geçerli sürümünde, form modelleri eklenmiştir. Form desenleri form şablonlarının birleşimini gösterir ve Form Stili Denetleyicisi geliştirme deneyimine sıkı bir şekilde tümleştirilmiştir. Desenler artık grup ve sekme sayfası düzeyinde kullanılabilen ek modellerle form düzeyinde (AX 2012 gibi) tanımlanmıştır.</td>
<td>Modellere uygun formlar, daha tutarlı bir arayüz, daha basit bir geliştirme deneyimi, daha kolay form güncelleştirme yolu ve form düzeni duyarlılığında artan güven dahil birçok yarar sağlar.</td>
</tr>
</tbody>
</table>

## <a name="help"></a>Yardım

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Yardım</strong>'a tıklayarak destekli yordamsal Yardım (görev kılavuzları) ve kavramsal konulara erişin.</td>
<td>AX 2012 Yardım sistemi, yerel web sunucusunda depolanmış olan HTML konulara yönlendirir. Müşteriler ve ortaklar kendi yardımlarını oluşturabilirler.</td>
<td>Dynamics AX'in mevcut sürümündeki yardım sistemi, Microsoft Dynamics Lifecycle Services (LCS) BPM içinde depolanan görev kılavuzlarını görüntüler. Yardım sistemi aynı zamanda Microsoft belgeler sitesinde de konular görüntüler. Daha fazla bilgi için bkz. <a href="help-overview.md" data-raw-source="[Dynamics AX Help - Getting Started](help-overview.md)">Dynamics AX Yardımı - Başlarken</a> ve <a href="new-task-guides-available-february-2016.md" data-raw-source="[New task guides available (February 2016)](new-task-guides-available-february-2016.md)">Mevcut yeni görev kılavuzları (Şubat 2016)</a>.</td>
<td>Görev kılavuzları, size bir görevin veya iş işlemin adımları boyunca yol gösteren destekli, etkileşimli bir deneyim sağlar. Microsoft'un sağladığı görev kılavuzlarını indirebilir ve özelleştirebilirsiniz. Konu, ürün belgelerini oluşturmak, teslim etmek ve güncelleştirmek için daha hızlı ve esnek bir yol sağlar. Bu nedenle, en son teknik bilgilerin erişimine sahip olmanızı garanti etmeye yardımcı olur.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>İnsan sermayesi yönetimi

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Kurs tamamlandığında, derse katılanlara yetenekleri ve sertifikaları aktarın.</td>
<td>Bu el ile gerçekleşen bir işlemdir.</td>
<td>Kurs tamamlandığında, katılımcının kayıtlarını yeni beceriler ve sertifikalar ile bir güncelleştirmek üzere yeni bir seçenek kullanılabilir duruma gelir.</td>
<td>Personel kayıtlarını güncelleştirmek için yeni ve etkili bir yol sağlar.</td>
</tr>
<tr>
<td>İstihdamı hızlıca doğrulayın.</td>
<td>Bu el ile gerçekleşen bir işlemdir.</td>
<td>İnsan kaynakları bölümünüz İstihdami bir çalışma alanı veya çalışan sayfasını kullanarak hızlıca doğrulayabilir.</td>
<td>İnsan kaynakları departmanınızın artık başlangıç tarihi, yönetici, pozisyondaki geçen ay sayısı ve ücret verisini doğrulamak için çok sayıda sayfaya erişimi yoktur.</td>
</tr>
<tr>
<td>Çalışanların sistemdeki bilgiyi görüntülemelerine, güncelleştirmelerine ve silmelerine olanak verin.</td>
<td>Kullanılabilir, ancak sınırlı görüntüleme ve güncelleştirme özellikleriyle.</td>
<td>Bu özellik etkinleştirilmiştir ve çalışanların ve yüklenicilerin çok çeşitli kişisel verileri görüntülemelerini sağlar. İsteğe bağlı olarak, bilgiler oluşturulduğunda, güncelleştirildiğinde veya silindiğinde bir iş akışı kullanılabilir.</td>
<td>Bu ister adres veya kişisel bilgileri güncelleştirme, bir işe başvurma, bir anket doldurma veya kendi fotoğraflarını güncelleştirme olsun, çalışanların kendi bilgileri üzerinde kontrol sahibi olmalarını sağlar. Bir iş akışı etkin olduğunda, iş süreçlerinize dayalı olarak, bilgiler bir onaylayıcı tarafından gözden geçirilebilir veya otomatik olarak onaylanabilir.</td>
</tr>
<tr>
<td>Yöneticilerin çalışan bilgilerini görüntülemelerine veya düzenlemelerine olanak sağlayın.</td>
<td>Kullanılabilir, ancak sınırlı görüntüleme ve güncelleştirme özellikleriyle.</td>
<td>Yapılandırma ayarları ve güvenliğe bağlı olarak, yöneticileri çalışan bilgilerini görebilir veya düzenleyebilirler.</td>
<td>Böylece yöneticilerin kaynak bulma, performans ve çalışan geliştirme konusunda daha iyi kararlar verebilmeleri için önemli çalışan verilerine erişimlerini sağlar.</td>
</tr>
<tr>
<td>Yönetici self-servis işlevselliğinden yararlanın.</td>
<td>Uygun değil</td>
<td>Yöneticiler artık yeni işe alım (çalışanlar ve yükleniciler), transferler ve işten çıkarma (istihdamın sona ermesi) için talepte bulunabilirler. Ayrıca yöneticiler yeni bir pozisyon, pozisyon süresinin uzatma veya pozisyon değişikliği talebinde bulunabilirler.</td>
<td>Bu senaryolar daha önce yalnızca İnsan Kaynaklarına uygulanıyordu. Bu senaryoları etkinleştirmek bir kuruluştaki yöneticilere güçlü araçlar sağlar. İsteğe bağlı iş akışları, gözden geçirme ve onayların doğru düzeyini sağlamak üzere etkinleştirilebilir.</td>
</tr>
<tr>
<td>Maaş işlemesinin sonuçlarına erişin.</td>
<td>Sonuçlar yalnızca işleme sırasında elde edilebilir.</td>
<td>Artık, işlemi çalıştırdıktan sonra herhangi bir noktada Maaş işleme sonuçlarına erişilebilir.</td>
<td>Bu, işlemin ve işleminin sonucunun mükemmel şekilde denetlenmesini sağlar. Ayrıca veriler güncelleştirilmeden önce çalışan kayıtlarına detaylı bir görünüm de sağlar.</td>
</tr>
<tr>
<td>Kazanç işlemesinin sonuçlarına erişin.</td>
<td>Sonuçlar yalnızca işleme sırasında elde edilebilir.</td>
<td>Artık, işlemi çalıştırdıktan sonra herhangi bir noktada kazanç işleme sonuçlarına erişilebilir.</td>
<td>Kazanç kaydı ve maliyet değişiklikleri tarafından güncellenen verilere detaylı bir bakış olanağı sağlar.</td>
</tr>
<tr>
<td>"Etkili Tarih" zaman çizelgesinin değişikliklerini görüntülemek.</td>
<td>Uygun değil</td>
<td>Bu karşılaştırma aracı; çalışanlar, pozisyonlar ve işler için kullanılabilir. Kaydın bir sürümünden diğerine olan değişimlerin kapsamlı bir görünümünü sağlar.</td>
<td>Çalışanlarda, pozisyonlarda ve iş kayıtlarında zaman içerisinde oluşmuş değişiklikleri görüntülerken zaman kazandırır. Bir kaydın iki sürümü veya zaman içerisindeki tüm sürümleri arasında hızlıca kıyaslama yapmanızı sağlar.</td>
</tr>
<tr>
<td>Çalışanları şirkete göre görüntüleyin.</td>
<td>Bu filtreleme yoluyla gerçekleştirilen, el ile yapılan bir işlemdir.</td>
<td>Çalışan ve yüklenici listeleri otomatik olarak oturum açtığınız şirkete göre filtrelenir.</td>
<td>Giriş yapılmış şirkette çalışanlara göre çalışanların filtrelenmiş bir görünümünü sağlar. Tüm çalışanların ve yüklenicilerin filtrelenmemiş görünümü için çalışan listesi kullanılabilir durumda kalır. Dynamics AX'ın geçerli sürümünde, sistem şirket listesinde seçili çalışana göre değişmez.</td>
</tr>
<tr>
<td>Kursun katılımcı listesini güncelleştirin</td>
<td>Uygun değil</td>
<td>Kurs katılımcıları katılımcı listesinden çıkartılabilir.</td>
<td>Yanlışlıkla kayıt edilen kurs katılımcılarını güncelleştirmek için kolay bir yol sağlar.</td>
</tr>
<tr>
<td>Bir gruptaki ücret olaylarını yönet</td>
<td>Uygun değil</td>
<td>Bu özellik, çalışanların maaş değişikliklerini işlemeyi basitleştirir.</td>
<td>Maaş çalışma alanı ve ilgili sayfaları aracılığıyla, çalışan kayıtlarını güncelleştirmek için basit, modern bir süreç sağlar.</td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a>Stok yönetimi

Yeni özellik eklenmemiştir.

## <a name="localization"></a>Yerelleştirme

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Çeşitli ülkelerdeki/bölgelerdeki yasal gereksinimleri karşılamak üzere elektronik belgeler oluşturun ve yapılandırın.</td>
<td>Elektronik belgeler, X++'da sabit kodlanmıştır veya Genişletilebilir Stil Sayfası Dil Dönüşümleri'dir (XSLT). Herhangi bir biçim ayarlaması geliştirme çabalarını gerektirir. Veri ve biçimlendirmeye erişimi yalıtılmış değildir. Ayarlanmış bir biçim dağıtımı, varolan biçimi geçersiz kılacak yeni bir Microsoft Dynamics AX düzeltme paketi gerektirir. Her biçimin özel değişiklikleri el ile yeni bir Microsoft Dynamics AX düzeltme paketi için kaynak kodu bağlantı noktalar gerekir.</td>
<td>Elektronik Raporlama (ER) elektronik belgeler oluşturmak ve yapılandırmak için bir geliştirici yerine bir işletme kullanıcısını hedefleyen yeni bir araçtır. ER etki alanına özel ve veri kaynakları olarak Microsoft Dynamics AX veritabanından bağımsız belge biçimleri için veri modelleri oluşturmanıza olanak sağlar. Bir işletme kullanıcısı, bu etki alanına özgü veri modelleri temel alan biçimler yapılandırabilir (örneğin; ödemeler, Intrastat raporları veya vergi raporları). Kullanıcı, Excel'e benzer basit görsel araçlar kullanarak biçimleri yapılandırır. ER şu anda elektronik belgelerin oluşturulması için metin, XML ve Excel biçimlerini destekler. Bu belgeler eşzamanlı olarak oluşturulabilir ve zip dosyalarına paketlenir. Veri modelleri ve biçimleri sürüm oluşturmayı destekler. Biçim sürümlerinin etkin oldukları dönemleri olabilir. Her biçim sürümü veya veri modeli ayrı bir yapılandırma içerisinde depolanır ve ortaklara ve müşterilere LCS aracılığıyla dağıtılır. Ortaklar ve müşteriler Microsoft veri modellerini ve biçimlerini özelleştirebilirler veya kendileri oluşturabilirler. ER ortak ve müşteri yapılandırma değişikliklerini, Microsoft yapılandırmalarına delta olarak kaydeder, bu da Microsoft yapılandırmalarının yeni sürümlerine yükseltmeyi basitleştirir. Ortaklar LCS kullanarak veri modellerini ve biçim yapılandırmalarını da diğer ortaklar ve müşteriler ile paylaşabilirler ve onlar da bunları daha fazla paylaşabilir ve özelleştirebilir. Delta özelleştirme ve kolay yükseltme tüm özelleştirme zincirinde desteklenir.</td>
<td>ER elektronik belge biçimlerinin çeşitli ülkelerdeki/bölgelerdeki yasal gereksinimleri karşılayacak şekilde oluşturulmasını, bakımını ve sürdürülmesini kolaylaştırır. ER elektronik belge biçimlerini değiştirme veya oluşturma işlemini daha hızlı ve kolay hale getirir. Bu değişiklikler, geliştiriciler yerine iş kullanıcıları tarafından yapılabilir. ER, Microsoft veya diğer ortaklar tarafından yayımlanan biçimlerin yeni sürümlerine yükseltmeyi ortaklar ve müşteriler için daha hızlı ve kolay hale getirir. ER Microsoft ve iş ortaklarının diğer ortakları ve müşterilerine elektronik belge yapılandırmalarını dağıtmaları için (LCS üzerinden) ortak bir yol sağlar. ER ayrıca ortaklar ve müşteriler için özelleştirme, yükseltme ve elektronik belge biçimleri için belirli iş gereksinimlerine dağıtmayı kolaylaştırır.</td>
</tr>
<tr>
<td>(MEX) Meksika katma değer vergisi (KDV) Mevzuat raporları oluşturun.</td>
<td>Gerçekleşmemiş KDV özelliğini kullanarak <strong>Satış ve Satınalma KDV</strong>'si raporları oluşturmanız gerekir, bu sayede kullanıcılar gerçekleştirilmiş ve gerçekleştirilmemiş bölümlere ait hareketleri durumlarına göre tanımlayabilirler.</td>
<td><strong>Satış ve Satınalma KDV</strong> raporları değiştirildi ve artık koşullu vergi özelliğini yalnızca belirli ödeme dönemlerinde gerçekleşmiş ve gerçekleşmemiş satış vergisi kodlarının tanımını kullanarak göz önünde bulundururlar.</td>
<td>Kullanıcıların bu raporları doğru şekilde oluşturabilmeleri için önce satış vergisi kodlarındaki yapılandırma değişiklikleri gereklidir. Koşullu bir satış vergisi özelliği gereklidir ve kullanıcının hareketleri ilgili bölüm alanında tanımlayabilmeleri için gerçekleşmiş ve gerçekleşmemiş ayrı kapatma dönemlerini yapılandırması gerekir.</td>
</tr>
<tr>
<td>(JPN) Japon sabit kıymet hızlandırılmış amortisman bildirimi belgesini yönetme.</td>
<td>Uygun değil</td>
<td>Önemli Beyanname bilgileri daha iyi bakım için tek bir belge içinde merkezi olarak depolanır.</td>
<td>Belge uyumluluğu ve yönetim kolaylığı, denetimler ve diğer incelemeler sırasında gerçekleşebilecek sorunlarını azaltmaya yardımcı olur.</td>
</tr>
<tr>
<td>(JPN) Banka hesabındaki JBA karakterleri doğrulayın.</td>
<td>Uygun değil</td>
<td>Kana ad alanlarının yalnızca JBA banka biçimi tarafından izin verilen karakterler içerdiğini doğrulayabilirsiniz.</td>
<td>Bu da, kullanıcılara geçersiz karakterler nedeniyle ödeme dosyasının oluşturulması sırasında kesintilerin azaltılmasında yardımcı olur.</td>
</tr>
<tr>
<td>(JPN) Japon sabit kıymet kuruş farkını mali yılın sonunda yakalayın.</td>
<td>Uygun değil</td>
<td><strong>Sabit kıymet parametreleri</strong> sayfası üzerinde, mali döneminin veya mali yılın sonunda yakalamayı seçebilirsiniz.</td>
<td>Bu, yerel uygulamalarla eşleştirmek için daha fazla esneklik sağlar.</td>
</tr>
<tr>
<td>(JPN) Japon şirket vergi beyannamesine eklenen Tablo 16 serisini, ana türde sabit kıymet miktarı üzerinde oluşturun.</td>
<td>Uygun değil</td>
<td>Sabit bir kıymetın değer modelleri üzerinde, ana türe göre özetlemeyi seçebilirsiniz. Varsayılan olarak, bu işlev yeni oluşturulan sabit kıymetler için kullanılır.</td>
<td>Binlerce sabit kıymete sahip büyük şirketler için, bu özetle raporlar, oluşturulan raporun büyüklüğünü önemli ölçüde kısaltır.</td>
</tr>
<tr>
<td>(JPN) Japon sabit kıymetler için, gelecek mali yıldaki özel amortisman rezervini tahsis etmeye başlayın.</td>
<td>Uygun değil</td>
<td>Uygun olağandışı amortisman profili bulunan sabit kıymet değer modelleri üzerinde, sonraki mali dönem veya sonraki mali yıl için tahsis etme başlatmasını seçebilirsiniz.</td>
<td>Bu, yerel uygulamalarla eşleştirmek için daha fazla esneklik sağlar.</td>
</tr>
<tr>
<td>(JPN) Yeniden düzenlenen vergi oranlarını içeren Japon tüketim vergisi raporu oluşturun.</td>
<td>Tüketim vergisi raporu yüzde 5'lik bir vergi oranı için kullanılabilir.</td>
<td>Tüketim vergisi raporu, yeniden düzenlenen vergi oranı için bir bölüm içerir (örneğin, yüzde 8).</td>
<td>Düzen, hükümet tarafından yeni tanıtıldı.</td>
</tr>
<tr>
<td>(AB) AB satış listesi için yuvarlama ayarlarını yapılandırın.</td>
<td>Çeşitli ülkeler/bölgeler için AB satış listesi raporlamasına ait yuvarlama ayarları X++'da veya Genişletilebilen Biçim Tablosu Dil Dönüştürmelerinde (XSLT'ler) sabit kodlanmıştır.</td>
<td>Yuvarlama ayarları Dış ticaret parametrelerine eklenir. Yuvarlama hassasiyetini, yuvarlama yöntemini, çıktı hassasiyetini ve yuvarlama hassasiyetinden daha küçük tutarlar için davranışı yapılandırabilirsiniz.</td>
<td>Bu AB satış listesi raporlaması yapılandırmasını birleştirir ve basitleştirir. Yuvarlama ayarları artık geliştirme çabalarını gerektirmez.</td>
</tr>
<tr>
<td>(AB) Ters gider uygulanabilirlik kurallarını yapılandırın.</td>
<td>Ters gider uygulanabilirlik kuralları yurtiçi ters gideri senaryosu için sabit kodlanmıştır. Uygulanabilirlik eşiği madde grubu bazında ayarlanabilir. İşlevsellik yalnızca İngiltere için kullanılabilir.</td>
<td>Ters gider uygulanabilirlik kurallarını belge türü bazında (satınalma/satış siparişleri, satıcı faturası, serbest metin faturası vb.) ve maddeler, madde grupları ve satınalma/satış kategorilerini birleştiren ters gider grubu bazında yapılandırabilirsiniz. Uygulanabilirlik kuralları tarih etkilidir. Satış vergi gruplarında ters gidere uygulanabilecek şekilde tek tek satış vergi kodlarını işaretleyebilirsiniz. Satış faturası raporu uygulanan ters giderin ayrıntılarını göstermek üzere ayarlanır. İşlevsellik tüm Avrupa ülkeleri/bölgelerinde kullanılabilir.</td>
<td>Bu değişiklik ters gider uygulanabilirlik kuralları yapılandırmasını birleştirir ve yurtiçi ters gider düzenlemelerinin Avrupa ülkeleri/bölgeleri tarafından benimsenmesini destekler.</td>
</tr>
<tr>
<td>(DE) Almanca denetim dosyası oluştur - GDPdUGoBD</td>
<td>Kullanıcılar Alman denetçiler ve makamları tarafından kabul edilen bir biçimde dışa aktarılacak mali verileri içeren tablo tanımlarını ayarlayabilir.</td>
<td>Özellik bir elektronik raporlama yapılandırması olarak uygulanmıştır. İşlevsellik Almanya ve Avusturya'da kullanılabilir.</td>
<td>Bu değişiklik, kullanıcılara veri biçimlendirme ve dönüşümler için daha fazla olasılık verir ve ayrıca kolay yapılandırma alışverişi, sürüm oluşturma gibi elektronik raporlama yapılandırma yaşam döngüsü yönetiminden gelen tüm kazançları sağlar.</td>
</tr>
<tr>
<td>(FR) Grup hesap toplamlarıyla birlikte bakiye listesi raporu</td>
<td>Grup hesap toplamlarıyla birlikte bakiye listesi raporu SSRS raporu olarak uygulanır (LedgerAccountSum_FR).</td>
<td>Grup hesap toplamlarıyla birlikte bakiye listesi raporu mali raporlar klasöründe yerelleştirilmiş LCS Varlık kitaplığından erişilebilen Yönetim Raporlayıcısı raporu olarak uygulanır.</td>
<td>Bu, kullanıcıların Yönetim Raporundaki mali raporları kullanarak özelleştirmelerde tüm kazançları ve özgürlük elde etmelerini sağlar.</td>
</tr>
<tr>
<td>(AB) Ödeme ihbarı, Ödemeler için katılım notu ve Denetim raporları.</td>
<td>Tüm bu raporlar ve SSRS raporları uygulanır.</td>
<td>Bu raporlar Microsoft Excel'de kullanılacak Açık XML şablonları olarak uygulanmıştır.</td>
<td>Elektronik ödeme yapılandırmaları ödeme dosyası biçimi ayarı ve şablonlarını içerir. Bu, kullanıcıların Elektronik raporlamayı kullanarak rapor özelleştirmelerinde tüm kazançları ve özgürlük elde etmelerini sağlar.</td>
</tr>
<tr>
<td>(AB) Intrastat için yuvarlama ayarlarını yapılandırın.</td>
<td>Çeşitli ülkeler/bölgeler için Intrastat raporlamasına ait yuvarlama ayarları X++'da veya Genişletilebilen Biçim Tablosu Dil Dönüştürmelerinde (XSLT'ler) sabit kodlanmıştır.</td>
<td>Yuvarlama ayarları dış ticaret parametrelerine eklenir. Yuvarlama hassasiyetini, yuvarlama yöntemini, çıktı hassasiyetini ve yuvarlama hassasiyetinden daha küçük tutarlar için davranışı yapılandırabilirsiniz.</td>
<td>Bu Intrastat raporlama yapılandırmasını birleştirir ve basitleştirir. Yuvarlama ayarları artık geliştirme çabalarını gerektirmez.</td>
</tr>
<tr>
<td>(AB) Kategori hiyerarşilerinde Intrastat emtia kodlarını ayarlayın.</td>
u<td>Intrastat emtia kodları ayrı bir listedir. Emtia Kodu türü kategori hiyerarşisi varsa, bu emtia kodları Perakende HQent ve satış kategorilerinde varsayılan olarak alınabilir.</td>
<td>Intrastat emtia kodlarının ayrı listesi Emtia kodu türü ürün hiyerarşisi ile birleştirilir.</td>
<td>Bu, emtia kodlarının serbest bırakılan ürünlere atanması yaklaşımını ve satış ve satınalma belgelerindeki kategorileri birleştirir.</td>
</tr>
<tr>
<td>(AB) Birim dönüştürme ayarını kullanarak Intrastat için ilave birimlerdeki miktarı raporlayın.</td>
<td>Intrastat emtia kodu ilave birimleri tanımlamak için bir metin alanına sahiptir ve<strong> Ürün</strong> kartı ilave birimlerin miktarını kilogram cinsinden tanımlayan bir alana sahiptir.</td>
<td>Intrastat emtia kodu için ilave birimler, Birimler listesinden seçilir. İlave birimlerin miktarı birim dönüştürme ayarları aracılığıyla hesaplanır.</td>
<td>Bu hareket birimlerinden ilave birimlere kadar yeniden hesaplama yaklaşımını birleştirir.</td>
</tr>
<tr>
<td>(AB) Varsayılan taşıma yöntemini teslimat yöntemine atayın.</td>
<td>Uygun değil</td>
<td>Varsayılan taşıma yöntemi için bir alan teslimat Yöntemine eklenir.</td>
<td>Bu Intrastat raporlama hazırlığını basitleştirir.</td>
</tr>
<tr>
<td>(AB) Intrastat'da raporlanmayacak serbest bırakılan ürünü işaretleyin.</td>
<td>Uygun değil</td>
<td>Intrastat raporlamadan maddeyi dışarıda bırakma seçeneği serbest bırakılan ürüne eklemektir.</td>
<td>Bu Intrastat raporlama hazırlığını basitleştirir.</td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a>İmalat

| Ne yapabilirsiniz? | Dynamics AX 2012 |
|------------------|------------------|
| **Üretim Katı Yönetimi** çalışma alanından açılan ayrı bir sayfadan, üretim siparişleri için malzeme kullanılabilirliğinin kontrolünü gerçekleştirin. | Uygun değil |
| Yeni **İş kartı aygıtı** sayfasını kullanılarak üretim işleriyle ilgili ilerlemeyi başlatın ve raporlayın. | **İş kaydı** formu öncelikle büyük terminal ekranları hedeflemektedir ve kullanıcı arayüzü genellikle fare tıklatmaları ile erişilir. |

## <a name="master-planning-and-forecasting"></a>Master planlama ve tahmin

| Ne yapabilirsiniz? | Dynamics AX 2012 | Dynamics AX 7.0 | Bu neden önemlidir? |
|------------------|------------------|-----------------|------------------------|
| Satış siparişi veya üretim emri planlanan tarihte teslimata hazır değil ise kullanıcıyı uyarın. | Master planlama tarafından oluşturulan uyarılar *Vadeli işlem iletileri* adını taşır. *Vadeli işlemler*, teslimat ve ödeme ileri bir tarihte gerçekleşecek olsa da (*teslimat tarihi*), iki taraf arasında bir kıymetin bugünkü fiyatı üzerinden (*vadeli işlem fiyatı*) alım ya da satım yapmayı öngören bir sözleşmedir. | *Vadeli işlem iletileri* ve *vadeli işlem tarihleri* sırasıyla *hesaplanan gecikmeler* ve *gecikmeli tarihler* olarak adlandırılmıştır. | AX 2012'de kullanılan terminoloji tutarsızdı ve yanlış çevirilere sebep oluyordu. |
| Master planlama çalışması, acil planlı siparişler ve gecikmelere sebep olan planlı siparişler durumları hakkında hızlı içgörüler kazanın. | Bu bilgi mevcuttur, ancak birden fazla form üzerinde dağılmıştır. | **Master planlama** çalışma alanı, son master planlamanın ne zaman tamamlandığı, hata oluşup oluşmadığı, acil planlı siparişlerin neler olduğu ve hangi planlı siparişlerin gecikmelere neden olduğuna dair bilgileri bir bakışta sunar. | Çalışma alanının sağladığı genel bakıştan yararlanırsınız. İlgili bilgiler, master planlamaya kılavuz olmak ve üretkenliği artırmaya yardımcı olmak için bir araya getirilmiştir. |
| Talep tahminleri güncelleştirmek için Excel kullanın. | Uygun değil | Talep tahminleri girdiğinizde, güncelleştirmeler yaptığınızda ve talep tahminlerini sildiğinizde Excel ile entegrasyonun avantajlarından yararlanırsınız. | Bu da verimliliği ve üretkenliği artırmanıza yardımcı olur. |
| Gelecekteki talebi tahmin edin ve geçmiş hareket verilerini temel alan talep tahminleri oluşturun. | Microsoft Dynamics AX 2012 R3 içinde, Microsoft SQL Server Analiz Servisi içindeki tahmin modelleri talep tahmin öngörüleri oluşturmakta kullanılır. | Microsoft Azure makine öğrenme bulut hizmetinin genişleme yeteneği ve gücünü kullanarak gelecekteki talebi tahmin edin. Müşteri gereksinimlerini karşılamak için makine öğrenme tahmin modellerini kullanmak ve genişletmek kolaydır. Hizmet en iyi eşleşme modeli seçimi yapar ve tahmin doğruluk hesaplamak için kullanılabilecek anahtar performans göstergeleri (APG) sunar. | Makine öğrenme tekniklerini kullanarak daha doğru tahminler üretin. |
| Sipariş tarihi ve miktarını master planlama çalışmasının ilgili eylemlerinin görsel genel bakışına dayanarak iyileştirin. | Genel eylemleri grafik görünümü kullanılabilir durumdadır, ancak tüm ilgili eylemleri gösterir. Eylemleri uygulandığında, bunlar hemen görünümden kaybolacaktır. | Eylemler grafiği daha iyi bir genel bakış sağlar. Bu yalnızca uygulanan ve doğrudan ilgili eylemleri göstermenize izin verecek seçenekleri içerir. Eylemleri uygulandığında, soluk görünürler ancak hala gösterilirler. Bu nedenle, genel bakış korunur. Ek bilgiler, verileri tek bir sayfada görüntülemek için eylemler grafiğine eklenir. | Yalnızca ilgili eylemler üzerinde odaklandığınız için verimlilikte geliştirmeden faydalanırsınız. |

## <a name="procurement-and-sourcing"></a>Tedarik ve kaynak atama

| Ne yapabilirsiniz? | Dynamics AX 2012 | Dynamics AX 7.0 | Bu neden önemlidir? |
|------------------|------------------|-----------------|------------------------|
| **Satınalma siparişi hazırlık** çalışma alanını, hazırlanmakta olan satınalma siparişlerinin durumuna hızlı bir anlayış kazanmak için kullanın. | Desteklenmez | **Satınalma siparişi hazırlık** çalışma alanı, siparişlerin taslak olarak oluşturuldukları ve izlendikleri zamandan, iş akışı onay durumları arasında ve onaylanmaya doğru ileri bir genel bakış sağlar. | Satınalma departmanınız artık birden çok sayfadan bilgileri aramak zorunda kalmaz ve artık çalışma alanının sunduğu genel bakıştan faydalanır. |
| **Satınalma sipariş girişi ve takip** çalışma alanını, giriş bekleyen satınalma siparişleri hakkında hızlı bir anlayış kazanmak ve izlemelerini takip etmek için kullanın. | Desteklenmez | **Satınalma sipariş girişi ve takip** çalışma alanı, bekleyen girişe veya teslimata sahip, onaylanmış satınalma siparişlerine genel bir bakış sağlar. Çalışma alanı girişlerini önleyici inceleme ve tedarikçi tarafından izleme ile ilgili Yardım için bekleyen ve sonrası son giriş listeleri içerir. Çalışma alanı ek olarak ambarda varış kaydı gerçekleşen satınalma siparişlerini, irsaliyelerinin deftere naklediğinden emin olmaya yardımcı olmak için listeler. Henüz sevkedilmemiş satınalma sipariş dönüşleri de ayrıca gözden geçirilmek için kullanılabilir. | Satınalma departmanınız çalışma alanının sunduğu genel bakıştan faydalanır. İlgili bilgiler, takip için bir kılavuz olmak ve üretkenliği artırmaya yardımcı olmak için bir araya getirilmiştir. |
| Satınalma siparişlerini onay için Dynamics AX istemcisinde barındırılan bir satıcı portalına gönderin. Satıcının onaylamasına veya reddetmesine izin ver. | Desteklenmez | Satıcı portalı arayüzü, satıcıların aldıkları satınalma siparişlerinin onaylamış veya reddedilmiş olmalarına izin verir. Ayrıca satıcının bir hesaptaki tüm onaylanmış satınalma siparişleri hakkında genel bir bakış edinmesini sağlar. Satınalma aracısı, satıcıdan bir onaylama isteyen, bir satınalma siparişini gönderebilir. Satıcının Dynamics AX'te kayıtlı bir Microsoft Azure Active Directory (Azure AD) kullanıcısı olması, satıcı için bir ilgili kişi bulunması ve özel bir güvenlik rolüne sahip olması gerekmektedir, | Satınalma departmanınız, evrak işlerinin ve satınalma siparişlerinin el ile takip edilmesinin azalmasından, bunlar doğrudan sisteme aktıkları için, faydalanır. Tek bir gerçek kaynağı olması müşteri ve satıcı arasındaki yanlış anlamaları azaltır. |

## <a name="projects"></a>Projeler

| Ne yapabilirsiniz? | Dynamics AX 2012 | Dynamics AX 7.0 | Bu neden önemlidir? |
|------------------|------------------|-----------------|------------------------|
| Çalışanları projelere kaynaklar olarak rezerve edin. | Kaynaklara benzer olarak, çalışanlar, kaynaklara ek olarak projelere doğrudan rezerve edilir. | Üretim ve üretim kaynaklarının depolandığı İş Merkezi tablosu, şimdi projedeki kaynaklar olarak çalışanlar rezerve etmek için kullanılabilir. | Projeleri rezerve ettiğinizde, sadece kaynakları rezerve etmeniz yeterlidir. |

## <a name="retail-sales-marketing-and-customer-service"></a>Perakende satış, pazarlama ve müşteri hizmetleri

### <a name="retail-hq"></a>Perakende Genel Merkezi

Microsoft Azure tarafından barındırılan Perakende HQ, bir web istemcisi aracılığıyla ticaret operasyonlarının tüm yönlerine tam görünürlük merkezi yönetim sağlar.

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ticaret operasyonlarını gerçekleştirmek.</td>
<td>Kullanıcıların bu verileri yönetmek için birden fazla formlarına erişimi gerekir:
<ul>
<li>Kategori yönetimi</li>
<li>Ürün yönetimi</li>
<li>Kanal ürünü öznitelikleri</li>
<li>Sınıflamalar</li>
<li>Katalog yönetimi</li>
<li>Setler</li>
<li>Fiyatlar ve iskontolar</li>
</ul></td>
<td><strong>Kategori ve ürün Yönetimi</strong> çalışma alanı aşağıdaki işlevselliği sağlar:
<ul>
<li>Ürün çeşidi yönetimi.</li>
<li>Ürün çeşidi ömrü izleme.</li>
<li>Serbest bırakılan ürünlerin yönetimi.</li>
</ul>
<strong>Fiyat ve iskonto yönetimi çalışma alanı</strong> aşağıdaki işlevselliği sağlar:
<ul>
<li>Verilen bir kanal ve kategori için fiyat ve iskonto yönetimi.</li>
<li>Kategori fiyatı kural yönetimi.</li>
<li>Fiyat ve iskonto öncelikleri, fiyat gruplarına ve iskontolara öncelikler atamanızı sağlar, böylelikle uygulanabilecekleri sırayı kontrol edebilirsiniz.</li>
<li>Katılımcı ve katalog iskonto yönetimi.</li>
</ul>
<strong>Katalog Yönetimi</strong> çalışma alanı aşağıdaki işlevselliği sağlar:
<ul>
<li>Etkin katalogların özeti.</li>
<li>Tek bir yerde katalog ömrü izleme.</li>
</ul></td>
<td><ul>
<li>Çalışma alanları mağazacılık rolüyle ilgili eylemler ve bunların görevlerini merkezi olarak yönetme imkanı vererek çalışanların üretkenliğini ve verimliliğini artırır.</li>
<li>Fiyat ve iskonto öncelikleri özelliği, fiyatların ve iskontoların nasıl kullanıldığını üzerinde müşterilere daha fazla kontrol sağlar. Bu özellik ayrıca daha yüksek mağaza fiyatlarının standart fiyatlara üstün geldiği yeni senaryolara olanak sağlar.</li>
</ul></td>
</tr>
<tr>
<td>Perakende kanal dağıtımları ve işlemleri yönetme.</td>
<td>Kullanıcının aşağıdaki görevleri gerçekleştirmek için birden çok forma erişmesi gerekir:
<ul>
<li>Yeni kanallar ve ilgili varlıklar oluşturun ve yapılandırın.</li>
<li>Günlük mağaza aktivitelerini yönetin.</li>
<li>Microsoft Dynamics AX içinde perakende işlerini işleme, perakende bildirimleri oluşturma ve Microsoft Dynamics AX stok ve finansalları güncelleştirme.</li>
</ul>
</td>
<td><strong>Kanal dağıtımı</strong> çalışma alanı aşağıdaki görevleri gerçekleştirmenize olanak sağlar:
<ul>
<li>Yeni kanallar ve ilgili varlıkları oluşturun.</li>
<li>Perakende mağaza yapılandırmasının ilerlemesini izleyin.</li>
<li>Bir görevi tamamlamak için gereken adımları gerçekleştirin veya görevi tamamlamak için gereken bilgileri sağlayın.</li>
<li>Aygıtlar durumunu izleyin ve mağazalardaki perakende Retail Modern POS (MPOS) programım kurulumunu mağazaların içinde doğrudan doğrulayın ve karşıdan yükleyin.</li>
<li>Tüm ilgili sayfalara erişin.</li>
</ul>
<strong>Perakende mağaza yönetimi</strong> çalışma alanı aşağıdaki görevleri gerçekleştirmenize izin verir:
<ul>
<li>Çalışanları ve çalışanların satış noktası (POS) izinlerini yönetin.</li>
<li>Belirli mağaza veya mağaza grubuna ait vardiya durumunu izleme.</li>
<li>Mağazalardaki MPOS programını doğrulayın ve kurulumunu doğrudan karşıdan yükleyin.</li>
<li>İlgili sayfalara erişin ve raporlar yazdırın.</li>
</ul>
<strong>Perakende mağaza finansmanı</strong> çalışma alanı aşağıdaki görevleri gerçekleştirmenize izin verir:
<ul>
<li>Belirli bir kanal için ekstreleri oluşturun, hesaplayın ve deftere nakledin.</li>
<li>Stok güncelleştirmek, hesaplamak ve ekstreleri deftere nakletmek için toplu işleri zamanlayın.</li>
<li>Açık ekstreleri izleyin.</li>
<li>Belirli mağaza veya mağaza grubuna ait vardiya durumunu izleme.</li>
<li>Raporları yazdırın ve ilgili tüm sayfalara hızlı bir şekilde erişin.</li>
</ul></td>
<td>Çalışma verimliliğini artırmak ve onların birçok görevleri ve kanal dağıtımı, yönetimi ve finansal öğeleri saklamak için ilişkili eylemler tarafından merkezi olarak izin vererek çalışanların verimliliğini yönetin.</td>
</tr>
<tr>
<td>Perakende BT operasyonlarını yönetin</td>
<td>Kullanıcının birden fazla forma erişmesi gerekir.</td>
<td><strong>Perakende BT</strong> çalışma alanı belirli bir kanal için tek bir yerde Commerce Data Exchange sorgularını sağlar ve böylece aşağıdaki görevleri gerçekleştirebilirsiniz:
<ul>
<li>İndirme oturumları.</li>
<li>Karşıya yükleme oturumları.</li>
<li>Başarısız oturumlar izleyin ve yeniden başatın veya yeniden çalıştırın.</li>
<li>Yaklaşan işleri görüntülemek veya çalıştırın.</li>
</ul></td>
<td>Çalışma alanları perakende BT ile ilgili eylemler ve bunların görevlerini merkezi olarak yönetme imkanı vererek çalışanların üretkenliğini ve verimliliğini artırır.</td>
</tr>
<tr>
<td>Verileri, veri varlıklarını kullanarak dışarı aktarın/içeri alın.</td>
<td>AX 2012, Microsoft Dynamics Retail Management Sistemi'ni (RMS) geçişini, veri alma/verme çerçevesi aracılığıyla kullanıma hazır olarak destekler.</td>
<td>Perakende veri varlıkları için perakende ilgili tüm ana ve başvuru veri desteklemek için genişletilmiştir. Tüm Dynamics AX çözümünde veri varlıkları için geliştirilmiş destek mevcuttur.</td>
<td>Veri varlıkları müşterilerin meta veri güdümlü şekilde veri alma ve veri vermelerini sağlar. OData varlıkları da müşterilerin Dynamics AX'i üçüncü taraf programlarla tümleştirmelerini sağlar.</td>
</tr>
<tr>
<td>Dynamics Microsoft AX ve POS istemcisinden BI raporlarını kullanarak akıllı analiz gerçekleştirin.</td>
<td>25'ten fazla arka ofis raporu ve beş kanal raporu kullanılabilir.</td>
<td>30'dan fazla arka ofis raporu ve 10 kanal raporu kullanılabilir.</td>
<td>Bu raporlar daha fazla BI ile müşterilerin sürekli en yüksek performansla çalışmalarını, eğilimleri tahmin etmelerini ve görüşleri ortaya çıkarmalarını sağlar.</td>
</tr>
<tr>
<td>Perakende kanal satış verilerini çözümlemek için "Retail Channel performance izle" Power BI içeriğini kullanın.</td>
<td>Uygun değil</td>
<td>PowerBI.com üzerinde <strong>Veri Al</strong> ve sonra <strong>Dynamics AX – Retail Channel Performance</strong> içerik paketini seçin. Dynamics AX bitiş noktası URL'sini verilerinizin panoda yansıtılması için girin.</td>
<td>Kuruluşlar üç veya dört tıklatma ile önemli finansal verileri içeren bir Power BI Pano'su dağıtabilirler. İçerik organizasyon tarafından kişiselleştirilebilir. Ayrıca kullanıcılar, Power BI pano kutucuklarını kendi kişiselleştirilmiş çalışma alanlarına Dynamics AX'de ekleyebilirler ve böylece daha sonra analitik bilgileri bir bakışta görebilirler.</td>
</tr>
<tr>
<td>Müşteri izinlerini yapılandırın.</td>
<td>Uygun değil</td>
<td>Müşteriler POS işlemlerinin tüketiciler tarafından kullanılabilir olup olmadığını belirleyebilirler. Perakende Sunucusu uygulama programlama arabirimi (API) çağrıları için izinleri kullanır.</td>
<td>Tüketici düzeyinde izinler yapılandırma olanağı sağlar.</td>
</tr>
<tr>
<td>Varlık yapılandırmalarını doğrulayın ve yönetin.</td>
<td>Uygun değil</td>
<td>Yapılandırma Yöneticisi ve doğrulayıcı özelliği aşağıdaki işlevselliği sağlar:
<ul>
<li>Toplu yapılandırma verilerini karşıya yükleme</li>
<li>İş varlığı doğrulaması</li>
</ul></td>
<td>Yapılandırmayı önyükleme yeteneği sağlar ve yapılandırmanın çeşitli yapılandırma elemanları için durumunu ve bütünlüğünü doğrulama seçeneği sağlar.</td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a>Perakende Donanım İstasyonu

| Ne yapabilirsiniz? | Dynamics AX 2012 | Dynamics AX 7.0 | Bu neden önemlidir? |
|------------------|------------------|-----------------|------------------------|
| POS aygıtları, yazıcılar, nakit çekmeceleri veya ödeme aygıtları gibi çevre aygıtlarına bağlanmak için etkinleştirin. | MPOS donanım profili, kullanılan aygıtlarını belirtmek için kullanılır. | Eklenen bir donanım profili bir istasyondan diğerine daha fazla donanımı destekler. Yeni bir donanım istasyonu profili her bir donanım istasyonu için benzersiz bir terminal kimliği, elektronik fon transferi (EFT) hareketleri işlendiği zaman destekler. EFT desteği donanım istasyonu içine, MPOS'un EFT ödeme işlemine katılımını azaltmak için birleştirilir. | Bu uygulamalar için daha fazla esneklik sağlar. Ayrıca, gelişmiş güvenlik ve kredi kartı verileri sınırlı erişim sağlar. |

### <a name="retail-server-and-data-management"></a>Perakende Sunucu ve veri yönetimi

Perakende sunucu ve veri yönetimi, tüketicilerin ve işletmelerin çevrimiçi, mağaza içi ve çağrı merkezi kanalları için mağazalar arası bir omni-kanal alışveriş deneyimi sağlar.

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td>CRT hizmetlerini kullanarak kanalı için iş verilerini depolayan bir commerce runtime (CRT) veritabanına bağlanın.</td>
<td>OData V3 desteklenir.</td>
<td>OData V4 desteklenir.</td>
<td>Bu, müşterilerin OData standartları ile güncel kalmalarına yardımcı olur. Ayrıca satışları mağaza içi, mobil ve çevrimiçi kanallar arası tümleşik duruma getirerek sağlam bir omni-kanal deneyimi oluşturur.</td>
</tr>
<tr>
<td>Perakende hizmetleri barındırılabilir hizmetler seti olarak destekler.</td>
<td>Perakende sunucusu üzerinden E-ticaret API desteklenmiyor.</td>
<td>E-ticaret API'si artık çevrimiçi senaryoları desteklemek için perakende sunucusu üzerinden kullanıma sunulmuştur.</td>
<td>Bu üçüncü taraf çevrimiçi mağazalar ile kullanılabilen, barındırılan ve ölçeklenebilir e-ticaret hizmetleri sağlar.</td>
</tr>
<tr>
<td>Microsoft Dynamics AX arka ofis ve kanallar arasında Commerce Data Exchange kullanarak veri taşıyın.</td>
<td>Commerce Data Exchange, çevrimiçi mağazalar ve fiziksel mağazalar gibi Microsoft Dynamics AX ve perakende kanalları arasında veri aktarımı sağlayan bir sistemdir. Daha fazla bilgi için bkz. <a href="https://technet.microsoft.com/library/dn741440.aspx">Commerce Data Exchange [AX 2012]</a>.</td>
<td>Microsoft Dynamics AX 2012 CU8 ile fonksiyonel eşlilik vardır. Ancak, aşağıdaki ayrıntıları unutmayın:
<ul>
<li>Commerce Data Exchange bulut için yeniden yaratıldı.</li>
<li>Zaman uyumsuz hizmet, kanal veritabanına doğrudan veritabanı erişimi kullanır.</li>
<li>Commerce Data Exchange: Gerçek zamanlı servis bir Microsoft Dynamics AX özel hizmet olarak barındırılır.</li>
<li>MPOS çevrimdışı veritabanları ve perakende sunucu arasında eşitlemeyi yönetir.</li>
</ul></td>
<td>Commerce Data Exchange bulut platformu için yeniden yaratıldı. Çevrimiçi mağazalar ve fiziksel mağazalar gibi Microsoft Dynamics AX ve perakende kanalları arasında veri aktarımını yönetmeye devam eder.</td>
</tr>
<tr>
<td>Tak ve Kullan, ödeme SDK'sını kullanarak yarı tümleşik kanal-arası ödeme işlemesini destekler.</td>
<td>AX 2012 aşağıdaki işlevselliği sağlar:
<ul>
<li>Tüm kanallar için destek: POS, e-ticaret ve çağrı merkezi.</li>
<li>Kart mevcut ve kart mevcut değil desteği.</li>
<li>Ödeme kabul etmek için sayfa.</li>
<li>Örnek kod olarak Perakende SDK'sı içinde LS5300 ve MX925 için çevrebirim desteği.</li>
</ul></td>
<td>Dynamics AX'in geçerli sürümü, mevcut Microsoft Dynamics AX perakende 2012 kredi/banka kartı özelliklerinin tümünü ve dört yeni geliştirmeyi destekler.</td>
<td>Müşterinin ödemeler için kredi/banka kartı hareketlerini işlemesine olanak sağlar.</td>
</tr>
<tr>
<td>Bir Microsoft hesabı kullanarak cihazları etkinleştirme (Microsoft Azure Active Directory (Azure AD)).</td>
<td>Uygun değil</td>
<td>Aşağıdaki işlevsellik sağlanır:
<ul>
<li>Bulut için Azure AD tabanlı etkinleştirme tarafından geliştirilmiş güvenlik.</li>
<li>Belirteç yönetimi için gelişmiş güvenlik.</li>
<li>Geliştirilmiş güvenilirlik, sorun giderme ve etkinleştirme sırasında hata iletileri</li>
<li>Etkinleştirmeyle ilgili basitleştirilmiş BT yönetim görevleri.</li>
<li>Yenilenmiş tehdit modeli ve giderilmiş güvenlik sorunları.</li>
</ul></td>
<td>Aşağıdaki yararları sağlar:
<ul>
<li>Azure AD ve aygıt simgesi/kimliği (belirteç, kullanıcıya özgü app depolama kullanan RS çağrıları) ile geliştirilmiş güvenlik.</li>
<li>MPOS'un (Tuğla aygıt) uzaktan yetkisiz kullanımını durdurur.</li>
<li>PCI uyum amacıyla MPOS aygıtlarını izler.</li>
<li>Bir iş tüzel kişiliği (register) ile fiziksel aygıtlar, aygıt belirteci kullanarak eşleştirir.</li>
<li>Pürüzsüz MPOS işlevler (numara serileri ve donanım profilleri) için ayarları MPOS'un ilk temas noktası olarak başlatır.</li>
<li>Yönetim merkezlerinden cihaz bilgilerini bildirir.</li>
</ul></td>
</tr>
<tr>
<td>Medya galerisi aracılığıyla zengin ortam içeriklerini ve yazarlığı yönetir.</td>
<td>Uygun değil</td>
<td><ul>
<li>Hem dışarıda barındırılan hem de Perakende'de barındırılan görüntüler için ortam galerisinden resmi karşıya yükleme, görüntüleme, yönetme ve silmeyi destekler.</li>
<li>Varlık sayfalarından resim karşıya yükleme ve görüntüleme desteği (<strong>Ürünler</strong>, <strong>Kataloglar</strong>, vb.) resim galerisinden bağlayarak ve görüntüyü masaüstünden karşıya yükleyerek.</li>
<li>Küçük resim, özel boyut ve özgün boyut için resimleri en iyi duruma getirme.</li>
<li>Toplu ilişkilendirme için şablon ve arka plan işleri kullanarak varlıkları toplu olarak bağlama.</li>
<li>Microsoft Excel entegrasyonu, adlandırma kuralların ve önceden tanımlanmış yolların öznitelik grup kısıtlamalarını geçersiz kılar.</li>
<li>Örneğin perakende'de barındırılan çalışan veya müşteri resimleri gibi kişisel olarak tanımlanabilen bilgiler (PII) için çevrimdışı resimler ve güvenli resimleri destekler.</li>
</ul></td>
<td><ul>
<li>Böylece harici olarak barındırılan görsellerin sorunlarına parmak basar ve git gel yapmanızı önleyerek tek bir yerden yönetmenizi sağlar.</li>
<li>Karşıya yüklenen ve dışarıda barındırılan görüntüler için Medya Galerisi aracılığıyla güçlü bir içerik yönetimi sağlar ve ayrıca görüntüleri bulmak için filtreleme sağlar.</li>
<li>Ürünler ve kataloglar gibi dışarıda barındırılan görüntüler ve varlıklar arasında kolayca toplu ilişkiler oluşturmanıza olanak sağlar.</li>
<li>Görüntüler için Perakende'de barındırılan depolamayı ve Excel entegrasyonu ile kolay güncelleştirmeleri destekler.</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a>Müşteri toplulukları için zengin deneyim

Perakende, sürükleyici mobil deneyimleri her yerde, her zaman ve herhangi bir aygıt üzerinde sunar. Bu işlev tüm kanallarda geliştirilmiş alışveriş ve mağaza deneyimleri sağlar.

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ürünleri arayın, göz atın ya da tarayın, ürünleri bir sepete ekleyin, ödeme kabul edin ve sezgisel ve kolay dokunmatik, zengin ve derinlikli kullanıcı deneyimi kullanarak MPOS üzerinde çıkış alın.</td>
<td>AX 2012 aşağıdaki özellikleri sağlar:
<ul>
<li>Satışlar, iadeler ve iptaller gerçekleştirin.</li>
<li>Müşteri siparişlerini oluşturun, değiştirin ve seçin.</li>
<li>Shift ve çekmece işlemleri gerçekleştirin.</li>
<li>Siparişleri alın ve çekin ve stok sayımları gerçekleştirin.</li>
<li>Mağaza içi raporları görüntüleyin.</li>
</ul></td>
<td>AX 2012 MPOS ile işlevsel eşlik sağlanır. Bu, aşağıdaki işlevleri kapsar:
<ul>
<li>Mağazalar/kanallar arasında müşteri arama.</li>
<li>Gerçek zamanlı Hizmete erişmeden müşteri siparişleri oluşturma yeteneği.</li>
<li>Geliştirilmiş aygıt etkinleştirme iş akışları, durum ve hata iletileri.</li>
<li>Öncesi sonrası tetikler ve özelleştirme geliştirmek için faaliyet desteği gibi genişletilebilme geliştirmeleri.</li>
</ul></td>
<td>Satış ekibi, mobil aygıtları mağazanın herhangi bir yerinde kullanarak satış hareketlerini ve müşteri siparişleri işleyebilir ve günlük işlemleri ve stok yönetimini gerçekleştirebilir.</td>
</tr>
<tr>
<td>POS'u, Bulut POS üzerinden bir web uygulaması olarak başlatın.</td>
<td>Uygun değil</td>
<td>MPOS ile işlevsel eşlik sağlanır. Bu, aşağıdaki işlevleri kapsar:
<ul>
<li>AAD kullanılarak cihaz etkinleştirme</li>
<li>Esnek düzen tasarımı</li>
<li>Edge, Internet Explorer ve Chrome tarayıcılar için destek.</li>
</ul></td>
<td>MPOS ile uyumlu işleve sahip bir web uygulama POS'u sağlar ve dağıtım masrafı olmadan platformlar ve tarayıcılar arasında kullanılabilir.</td>
</tr>
<tr>
<td>Bir omni-kanal e-Ticaret web sitesi oluşturmak için içerik yönetim sistemleri ile bütünleştirin.</td>
<td>Microsoft SharePoint ve üçüncü taraf mağaza ön tarafları desteklenir.</td>
<td>Üçüncü taraf mağaza ön taraflarına destek veren bir e-Ticaret platformu sağlanır. Bu platform aşağıdaki özellikleri içerir:
<ul>
<li>Zengin bir tüketici API'si.</li>
<li>Tüm üçüncü taraf açık kimlik sağlayıcılar için kimlik tümleştirme.</li>
<li>Ödeme entegrasyonu.</li>
</ul></td>
<td>Müşteriler artık istedikleri içerik yönetim sistemini kullanma esnekliğine sahipler.</td>
</tr>
<tr>
<td>Posta siparişi kataloglar yoluyla müşterileri hedefleyin ve çağrı merkezi kullanarak hızlı sipariş girişi, yardımlı satış ve yerine getirme işlemleri ile daha verimli hale getirin.</td>
<td><ul>
<li>Çağrı Merkezi kanalı</li>
<li>Posta siparişi katalogları</li>
<li>Hızlı sipariş girişi ve yardımlı satışı</li>
<li>Geliştirilmiş sipariş karşılama</li>
<li>Müşteri hizmeti</li>
<li>Tümleşik fiyatlandırma ve promosyonlar/iskontolar</li>
</ul></td>
<td>Fiyat geçersiz kılmaları dışında, AX 2012 Çağrı Merkezi çözümü ile özellik eşliği mevcuttur.</td>
<td>Çağrı merkezleri, çalışanlarının telefon üzerinden müşterilerden sipariş almalarını ve satış siparişleri oluşturmalarını sağlar perakende kanal türüdür.</td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a>Ticaretle ilgili temel bilgiler

Perakende ve ticaret odaklı yapılandırma seçeneği, perakendeye özgü dağıtımları kolaylaştırmaya yardımcı olur.

| Ne yapabilirsiniz? | Dynamics AX 2012 | Dynamics AX 7.0 | Bu neden önemlidir? |
|------------------|------------------|-----------------|------------------------|
| Ticaretle ilgili temel bilgiler panosunu kullanın. | Menü öğelerine bağlantılar içeren bir alan sayfası mevcuttur. | Ticaretle ilgili temel bilgiler panosu; sık kullanılan görevler, çalışma alanları, Power BI web denetimi, sık kullanılan, son sayfalar ve geçerli çalışma öğesi bağlantılarının da dahil olduğu bağlantılar sağlar. | Geliştirilmiş pano çalışanları daha verimli hale getirerek ve perakendeye özgü herhangi bir görev için esnek bir başlangıç noktası sağlayarak onları güçlendirir. |
| Hesap değişikliklerine erişmek için veri varlıklarını kullanın. | Hesap değişiklikleri dosya sisteminde bir klasörde dışa aktarılır. | Hesap değişikliklerine veri varlıkları ile erişilebilir. | Bu özellik, farklı sistemler arasında veri taşırken, daha fazla esneklik sağlar. Bu özellik aynı zamanda OData uygulamalar aracılığıyla geliştirilebilir. |
| Bulut POS ve MPOS kullanın. | Yalnızca Kurumsal POS (EPOS) desteği kullanıma hazır gelmektedir. | MPOS ve Bulut POS, EPOS istemcisinin yerini alır. e-Ticaret kanalı da Ticaretle ilgili temel bilgilere varsayılan olarak eklendi. | Bu özellik, hızla konuşlandırılabilir satış noktasında istemcilerle daha gelişmiş kullanıma hazır kanal desteğini etkinleştirir. |
| İki katmanlı mimariyi uygulamak ve korumak. | Veri içeri alma/dışarı aktarma framework'ü, AX 2012 ve üçüncü-taraf sistemler arasında veri taşıma yeteneği sağlar. | Veri varlıkları, iki katmanlı mimari desteğini geliştirmek için oluşturulur. | Veri varlıkları ve OData uygulamaları iki katmanlı senaryoların uygulamasını ve bakımını daha kolay hale getirmek için bir soyutlama katmanı sağlar. |
| Formlar basitleştirin. | Özel kod kullanıcı arayüzünü basitleştirmek için gereklidir. | Form ve menü uzantıları standartlaştırılmış arayüz basitleştirmesi sağlarlar. | Bu özellik perakendecinin gereksinimlerini temel alarak formlar üzerinde ince ayar yapmak için hızlı ve kolay bir yol sağlar. |

### <a name="pos-task-recorder"></a>POS Görev kaydedicisi

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Modern POS için görev kılavuzları ve belgeler oluşturmak ve paylaşmak.</td>
<td>Uygun değil</td>
<td>MPOS Görev Kaydedici aşağıdaki özellikleri destekler:
<ul>
<li>MPOS içinde gerçekleştirilen çeşitli görevler için görev kayıtları oluşturma.</li>
<li>İş süreci modelinde bir düğüm ile ilişkilendirilecek adımları ve ekran görüntülerini içeren bir belge oluşturur.</li>
</ul></td>
<td>Ortaklar ve bağımsız yazılım satıcıları (ISV) MPOS'u özelleştirebilir ve kendi kullanıcılarını eğitmek için destekleyici belgeler sağlayabilirler.</td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a>Genişletilebilirlik

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td>HQ, Çağrı Merkezi, e-Ticaret ve POS üzerinden genişletilebilir ve kolayca dağıtılabilir perakende bileşenlerini destekler.</td>
<td>Bileşenler perakende SDK kullanılarak genişletilebilir. Paketleme ve dağıtım özellikleri desteklenmez.</td>
<td>Genişletilebilirlik kancaları çeşitli bileşenler boyunca kod yalıtımını desteklemek ve daha iyi hizmet vereiblmek için geliştirildi. Bulunan özelliklerden bazıları şunlardır:
<ul>
<li>İş akışı, etkinlik ve işlem.</li>
<li>Ön tetikleyiciler ve son tetikleyiciler bir iş akışını kolayca genişletmenize olanak sağlar.</li>
<li>Uygulama ve işlem tetikleyicileri.</li>
</ul>
Ayrıca, bu bileşenleri MSBuild kullanarak yapılandırmanıza ve paketlemenize ve daha sonra Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla özelleştirmenizi sorunsuz şekilde dağıtmanıza izin veren bir çerçeve mevcuttur.</td>
<td>Perakendecilerin işlemin coğrafyaları ve dikeylerine dayanan çok özel gereksinimleri vardır. Kolayca genişletilebilir bir platform sunarak, dikeyler ve pazarlar arasında kullanımı etkinleştiriyoruz. Perakendenin de çok dağıtılmış bir mimarisi olduğundan, sorunsuz şekilde dağıtma özelliği verimliliğini büyük ölçüde artırır.</td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a>Yaşam Döngüsü yönetimi

Lifecycle Services (LCS) müşterilerin ve ortakların sistemin ömrü kayıttan tutun günlük işlemleri yönetmeye kadar kullanabilecekleri hizmetleri sağlar.

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Programı bulut dağıtım hizmetleri aracılığıyla yönetin.</td>
<td>Uygun değil</td>
<td>Aşağıdaki topolojilerden bulut için dağıtılabilir:
<ul>
<li>Deneme bir-kutu topoloji, perakende.</li>
<li>Perakende çoklu kutu yüksek kullanılabilirlik topolojisi.</li>
<li>Perakende SDK'sı ile geliştirici topolojisi.</li>
</ul>
Kendi kendine kurulum aracılığıyla "low-touch" istemci bileşeni mevcuttur:
<ul>
<li>Retail Modern POS.</li>
<li>Perakende Donanım İstasyonu.</li>
<li>Kendi kendine yükleme aracılığıyla özelleştirilmiş paketlerin dağıtımı ve karşıya yükleme desteği.</li>
</ul></td>
<td>Bulut Dağıtım Hizmetleri aşağıdaki yararları sağlar:
<ul>
<li>Perakende HQ bileşenleri için önemli ölçüde azaltılmış dağıtım çabası ve karmaşıklık.</li>
<li>Microsoft Azure genel bulut için yerel dağıtım.</li>
<li>Yapılandırmayı daha kolay ve sezgisel hale getirmek için iyileştirilmiş mağaza içi bileşenlerin kendi kendine yüklemeleri</li>
</ul></td>
</tr>
<tr>
<td>Sistem durumunu izleyin ve hataları ve sorunları tanımlayın.</td>
<td>Bu işlevsellik <a href="https://www.microsoft.com/download/details.aspx?id=42636">Microsoft Dynamics AX 2012 R3 CU8 Perakende için System Center 2012 Yönetim Paketi gerektirir</a>.</td>
<td>Perakende bileşenleri izleme ve tanılama şimdi LCS'deki <strong>Operasyonel Öngörüler</strong> Panosunda üzerinden kullanılabilir.</td>
<td><strong>Operasyonel Öngörüler</strong> panosu, Sistem Merkezi İşlem Yöneticisi (SCOM) altyapısını kurma ihtiyacının yerini alan bir bulut tabanlı izleme portalıdır.</td>
</tr>
<tr>
<td>Self-Servisi kullanarak perakende donanım istasyon ve aygıtları yüklemek, oluşturmak, yapılandırmak, karşıdan yüklemek.</td>
<td>Yükleme Paketleyici ve Enterprise Portal kullanarak, bir kullanıcı tanımlanmış topolojisine bağlı olarak belirli bir bilgisayarda bulunması gereken tüm bileşenleri otomatik yükleme ve yapılandırma işlemini gerçekleştirebilirsiniz.</td>
<td>Sadece iki yükleme paketi olduğundan, biri MPOS istemcisi diğeri de perakende donanım istasyon bileşeni olmak üzere, Self-Servis her düzeyde bu istemci bileşenlerini yüklemek için gerekli olan çalışma miktarını azalttı.</td>
<td>Self-Servis gereksinimlerini en aza indirmeyi ve bir kullanıcı için yükleme gerçekleştirmeyi kolaylaştırmayı amaçlar.</td>
</tr>
</tbody>
</table>

## <a name="sales"></a>Satışlar

<table>
<thead>
<tr>
<th>Ne yapabilirsiniz?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Bu neden önemlidir?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Müşterilere siparişleri taahhüt ettiğinizde teslimat alternatiflerine hızlı bir genel bakış atın.</td>
<td>Ürün kullanılabilirliği kısıtlamaları varsa ve müşterinin siparişi üzerindeki bir ya da birden fazla ürün için teslim tarihinde teslimat sağlanamıyorsa, sipariş taahhüdü görev zor olur. Sipariş İşlemcisi'nin, müşterinin talep ettiği teslimat tarihine uyulabilmesi için ve bulunurluk sağlayabilmek için dengeleme yapacak alternatifler bulabilmesi ya da müşterinin kabul edip güvenebileceği bir teslimat çözümü sunabilmek için, her biri gerekli bilginin sadece bir kısmını içeren birden fazla form açması gerekir. Özellikle, bir form siteler arasında eldeki miktarı, başka bir form şirketlerarası eldeki miktar ayarını gösterir. Üçüncü bir form, kullanıcıların her seferinde bir tesis/çeşit için en erken bulunma tarihini hesaplamalarını sağlar. Dördüncü bir form ise tedarik siparişlerini gösterir. Bu nedenle kullanıcılar tüm ilgili seçenekleri değerlendirmiş olmak yerine hemen çözüm sunan fakat yeterli olmayan bir çözüm seçmediklerine güvenemezler. Taahhüt akışı içerisinde, çok sayıda sayfayı açıp kapamak ve öngörüleri ve özellikleri birleştirmek için çok sayıda kesinti gerçekleşeceğinden, kullanıcılar kendilerini etkili hissetmezler.</td>
<td>Teslim tarihini hesaplama için mevcut algoritmaları temel alan <strong>Teslim alternatifleri </strong>sayfası, sipariş taahhüdü için yeni bir kullanıcı deneyimi sunar:
<ul>
<li>Birden çok formdaki bilgileri tek bir alanda birleştirir.</li>
<li>Kullanıcının aralarından seçim yapabileceği en hızlı teslimat (en erken kullanım tarihi) ölçütünü temel alan bir siteler/ambarlama/değişken/aktarım modu birleşimi gibi alternatif bir teslimat "hazır" paketleri sunar.</li>
<li>Bu kullanıcının, benzetim arabirimden seçeneklerini belirleyip, bunları satış siparişi satırına transfer etmesini sağlar.</li>
</ul></td>
<td>Stok optimizasyon stratejisi izlerken yüksek müşteri hizmeti sağlamayı amaçlayan şirketler, siparişleri güvenilir ve rekabetçi bir şekilde taahhüt edebilmelidirler. Sonuçta, müşterilerin kendi işletmeleri, ürünleri zamanında kullanılabilir olmasına ihtiyaç duyar. <strong>Teslim alternatifleri</strong> görev sayfası sipariş taahhüdü görevini etkileşimli en iyi alternatif sipariş teslim tarihlerini belirleyerek etkileşimli bir yerde öneren daha hızlı, daha kolay ve daha sistematik hale getirir.</td>
</tr>
</tbody>
</table>

## <a name="service-management"></a>Hizmet yönetimi

Yeni özellik eklenmemiştir.

## <a name="transportation-management"></a>Taşıma yönetimi

Yeni özellik eklenmemiştir.

## <a name="travel-and-expense"></a>Seyahat ve gider

Yeni özellik eklenmemiştir.

## <a name="warehouse-management"></a>Ambar yönetimi

| Ne yapabilirsiniz? | Dynamics AX 2012 | Dynamics AX 7.0 | Bu neden önemlidir? |
|------------------|------------------|-----------------|------------------------|
| Ambar Mobil Cihazlar portalını indirin, yükleyin ve yapılandırın. | Portalı, Microsoft Dynamics AX yükleme sürecinde standart bir kurulum ile indirebilir, yükleyebilir ve yapılandırabilirsiniz. Şirket içinde otomatik olarak dağıtım ve yapılandırma için tasarlanmıştır. | Ambar Yönetimi'nde menü öğesi yoluyla bir tek başına yükleyiciyi karşıdan yükleyebilirsiniz. Şirket içinde otomatik olarak dağıtım ve yapılandırma için tasarlanmıştır. | Mobil cihaz işlevini ayarladığınızda, Ambar Mobil Cihazlar Portalı'nı yerel olarak yükleyip yapılandırmalı ve bulutta Dynamics AX programı için bir bağlantı getirmelisiniz. |

## <a name="additional-resources"></a>Ek kaynaklar

[Yenilikler veya değişenler](whats-new-changed.md)

[Kullanılabilir yeni görev kılavuzları (Şubat 2016)](new-task-guides-available-february-2016.md)
