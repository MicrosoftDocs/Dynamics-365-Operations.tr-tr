---
title: Gelir kabulü kurulumu
description: Bu makalede, Gelir kabulü için kurulum seçenekleri ve bunların etkileri açıklanmaktadır.
author: kweekley
ms.date: 04/28/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: ef294af8d3a8f39a80b98aeba293267dcca1f29b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900027"
---
# <a name="revenue-recognition-setup"></a>Gelir kabulü kurulumu
[!include [banner](../includes/banner.md)]

Gerekli olan tüm kurulum için menü maddelerini içeren yeni bir **Gelir kabulü** modülü eklenmiştir. Bu makalede, kurulum seçenekleri ve bunların etkileri açıklanmaktadır.

> [!NOTE]
> Gelir kabulü özelliği artık varsayılan olarak Özellik yönetimi aracılığıyla etkinleştirilmektedir. Kuruluşunuz bu özelliği kullanmıyorsa **Özellik yönetimi** çalışma alanından kapatabilirsiniz.
>
> Paket işlevi dahil olmak üzere gelir kabulü, Commerce kanallarında (e-ticaret, POS ve çağrı merkezi) desteklenmez. Gelir kabulü için yapılandırılan maddeler, Commerce kanallarında oluşturulan siparişlere veya hareketlere eklenmemelidir.

**Gelir kabulü** modülünde aşağıdaki kurulum seçenekleri vardır:

- Gelir kabulü günlükleri
- Gelir kabulü için parametreler
- Gelir planları 
- Stok kurulumu

    - Madde grupları ve serbest bırakılan ürünler
    - Gelir planını tanımlama
    - Gelir fiyatını tanımlama
    - Stok kurulumu

        - Gelir planını tanımlama
        - Gelir fiyatını tanımlama

    - Deftere nakil profilleri
    - Ürün demetleri

        - Ürün demeti bileşenleri
        - Ürün demeti maddesi

- Proje kurulumu

## <a name="revenue-recognition-journals"></a>Gelir kabulü günlükleri

Gelir kabulü için yeni bir günlük türü kullanıma alınmıştır. Günlük gereklidir ve iki senaryoda kullanılır.

İlk senaryo, ertelenen gelir, gelir planının ayrıntılarına göre bir gelir kabulü günlüğü oluşturarak kabul edildiğinde tüm sözleşme yükümlülükleri karşılandıktan sonra gerçekleşir. Günlük, bakiyeyi ertelenen gelir genel muhasebe hesabından gelir genel muhasebe hesabına taşıyan bir muhasebe girişi içerir.

İkinci senaryo, yeniden tahsis yapıldıktan sonra bir günlük oluşturulduğunda gerçekleşir. Yeniden tahsis işlemi, bir satış siparişi satırı daha önce faturalandırılmış satış siparişine eklendiğinde veya orijinal sözleşmenin parçası olan bir satır içerecek şekilde yeni bir satış siparişi oluşturulduğunda gerçekleşir. Fatura, yeni satış siparişi satırı eklenmeden önce deftere nakledildiyse deftere nakledilen müşteri faturası için düzeltici bir muhasebe girişi oluşturulmalıdır.

Günlük, **Günlük adları** sayfasında (**Gelir kabulü \> Kurulum \> Günlük adları**) ayarlanır. Günlük türü, **Gelir kabulü** olarak ayarlanmalıdır. 

## <a name="parameters-for-revenue-recognition"></a>Gelir kabulü için parametreler

Gelir kabulü ayarları, **Genel muhasebe parametreleri** sayfasının (**Gelir kabulü \> Kurulum \> Genel muhasebe parametreleri**) **Gelir kabulü** sekmesinde yapılandırılır. Aşağıdaki ayarlar kullanılabilir:

- **Gelir kabulü günlük adı**: Gelir kabulü için oluşturulan günlüğü seçin. Günlük, gelir planından gelir kabul edildiğinde veya zaten faturalanmış bir satış siparişi için yeniden tahsis işlemi yaptığınızda gereklidir.
- **İskonto tahsisat yöntemini etkinleştir**: Serbest bırakılan her ürün için gelir fiyatında tanımlanan adil piyasa değerinin tahsisatı üzerinden gelir fiyatını belirlemek için bu seçeneği **Evet** olarak ayarlayın. Bu tahsisat, maddeler boyunca satır iskontolarının tahsisatını içerir. Bu seçenek **Hayır** olarak ayarlanırsa sistem, serbest bırakılan her ürün için gelir fiyatında tanımlanan medyan fiyatı kullanır. Bu seçenek **Hayır** olarak ayarlanırsa ancak serbest bırakılan ürünler için ayarlanan medyan fiyat yoksa gelir fiyatının tahsisatı gerçekleşmez.
- **Genel iskontoları dahil et**: Ürünlerde genel iskontolar tahsis ederek gelir fiyatını belirlemek için bu seçeneği **Evet** olarak ayarlayın. Bu seçenek **Hayır** olarak ayarlanırsa genel iskonto, gelir fiyatı tahsisatına dahil edilmez.
- **Sözleşme şartlarını devre dışı bırak**: Sözleşme başlangıç ve bitiş tarihleri tanımlı olmasa bile **Sözleşme desteğini deftere naklet** seçeneğindeki gelir türüne sahip olan ürünler serbest bırakılabilirse bu seçeneği **Evet** olarak ayarlayın. Genellikle sözleşme başlangıç ve bitiş tarihleri, **Sözleşme desteğini deftere naklet** gelir türünün maddeleri için gereklidir. Sözleşme başlangıç ve bitiş tarihleri tanımlı olmadığında deftere nakledilen gelir planının ayrıntıları, tekrar sayısı ve fatura tarihi kullanılarak hesaplanır.
- **Yeniden tahsis ederken Alacak hesapları için fatura düzeltmelerini deftere naklet**: Zaten deftere nakledilmiş faturalar için yeniden tahsis yaptığınızda deftere nakledilmiş fatura için muhasebe girişinin düzeltilmesi gerekir. Düzeltmenin nasıl yapılacağını belirtmek için bu seçeneği kullanın.

    - Düzeltme hareketinin Genel muhasebeye nakledilmesini sınırlamak için bu seçeneği **Hayır** olarak ayarlayın. Bu seçenek **Hayır** olarak ayarlandığında dahili muhasebe düzeltmesi için Alacak hesaplarında ek belge oluşturulmaz. Fatura ödendiğinde kapatma işlemi, nakit iskontolarını veya gerçekleşmiş kazanç ya da zararları deftere nakletmek için eski muhasebe girişini kullanır.
    - Alacak hesaplarında düzeltme hareketi için otomatik olarak bir ters işlem belgesi ve yeni fatura oluşturmak üzere bu seçeneği **Evet** olarak ayarlayın. Bu düzeltme, dahili muhasebe düzeltmesi olduğundan yeni belgeler müşteriye gönderilmez veya bildirilmez. Ters işlem belgesi orijinal faturayla kapatılır ve yeni düzeltilen fatura, müşteri tarafından ödenir. Üç belgenin de müşteri ekstresi gibi raporlarda gösterildiğini unutmayın.

[![Kurulum bilgileri.](./media/revenue-recognition-setup-info.png)](./media/revenue-recognition-setup-info.png)

## <a name="revenue-schedules"></a>Gelir planları

Gelirin ertelenebileceği her tekrar için bir gelir planının oluşturulması gerekir. Örneğin, kuruluşunuz altı aylık, 12 aylık, 18 aylık ve 24 aylık dönemler üzerinden destek sağlıyorsa her dönem için bir gelir planı oluşturmanız gerekir. Gelir planının kurulumu, gelir fiyatının seçtiğiniz dönem sayısı boyunca nasıl tahsis edileceğini belirler. Ayrıca fatura deftere nakledildiğinde oluşturulan gelir planı için girilen varsayılan tarihleri de belirler.

Geliri kilometre taşlarına göre kabul ederseniz kabul tarihlerinden bağımsız olarak kilometre taşlarının sayısı için bir gelir kabulü planı oluşturmanızı öneririz. Planları oluşturduktan sonra bunları, beklenen kilometre taşı tarihlerini yansıtacak şekilde düzenleyebilirsiniz. Bu kayıtları, kilometre taşlarının karşılandığı ve gelirin kabul edilebileceği bildirilinceye kadar beklemeye alabilirsiniz.

Gelir planları, **Gelir planları** sayfasında (**Gelir kabulü \> Kurulum \> Gelir planları**) oluşturulur.

[![Gelir planları.](./media/revenue-recognition-revenue-schedules.png)](./media/revenue-recognition-revenue-schedules.png)

**Gelir planı** ve **Açıklama** alanlarına açıklayıcı değerler girin. Aşağıdaki ek ayarlar, fatura deftere nakledildiğinde gelir planını oluşturmak için kullanılır.

- **Tekrarlar**: Gelir ertelemesi için ay veya tekrar sayısını girin.
- **Otomatik bekleme**: Fatura deftere nakledildiğinde tüm gelir planı satırlarının otomatik olarak beklemeye alınması gerekirse bu onay kutusunu seçin. Satırın ertelenen gelirinin kabul edilebilmesi için bekleme, planın her satırından el ile kaldırılmalıdır.
- **Otomatik sözleşme şartları**: Sözleşme başlangıç ve bitiş tarihlerinin otomatik olarak ayarlanması gerekirse bu onay kutusunu seçin. Bu tarihler otomatik olarak yalnızca **Sözleşme desteğini deftere naklet** gelir türündeki serbest bırakılan ürünler için ayarlanır. Sözleşme başlangıç tarihi otomatik olarak satış siparişi satırının talep edilen sevk tarihi olarak ayarlanır ve sözleşme bitiş tarihi de otomatik olarak başlangıç tarihi artı gelir planının kurulumunda tanımlanan ay veya tekrar sayısı olarak ayarlanır. Örneğin, satış siparişi satırındaki ürünün bir yıllık garantisi vardır. Varsayılan gelir planı **12M**'dir (12 ay) ve bu gelir planı için **Otomatik sözleşme şartları** onay kutusu seçilmiştir. Satış siparişi satırındaki talep edilen sevk tarihi 16 Aralık 2019 ise varsayılan sözleşme başlangıç tarihi 16 Aralık 2019 ve varsayılan sözleşme bitiş tarihi 15 Aralık 2020'dir.
- **Kabul esası**: Kabul esası, gelir fiyatının tekrarlar boyunca nasıl tahsis edileceğini belirler.

    - **Güne göre aylık**: Tutar, her takvim ayındaki gerçek gün sayısına göre tahsis edilir.
    - **Aylık**: Tutar, tekrarlarda tanımlanan ay sayısı boyunca eşit olarak tahsis edilir.
    - **Tekrarlar**: Tutar, tekrarlar boyunca eşit olarak tahsis edilir ancak kabul yöntemi olarak **Gerçek başlangıç tarihi** seçeneğini belirlerseniz fazladan bir dönem içerebilir.
    - **Güne göre mali dönem**: Tutar, her mali dönemdeki gerçek gün sayısına göre tahsis edilir. 

         - **Güne göre aylık** ve **Güne göre mali dönem** sonuçları, mali dönemler takvim aylarını takip ettiğinde aynı olur. Tek özel durum, kabul yönteminin **Ay/dönem sonu** olarak ayarlanması ve bir satış siparişi satırında **Sözleşme başlangıç tarihi** ve **Bitiş tarihi** alanlarının boş bırakılmasıdır.

- **Kabul yöntemi**: Kabul yöntemi, fatura için gelir planında ayarlanan tarihleri belirler.

    - **Gerçek başlangıç tarihi**: Plan, sözleşme başlangıç tarihini (sözleşme desteğini deftere naklet \[PCS\] maddeleri için) veya fatura tarihini (temel ve temel olmayan maddeler için) kullanarak oluşturulur.
    - **Ayın/dönemin ilk günü**: İlk plan satırındaki tarih, sözleşme başlangıç tarihidir (veya fatura tarihi). Ancak sonraki tüm plan satırları, ayın veya mali dönemin ilk günü için oluşturulur.
    - **Ay ortasından bölme**: İlk plan satırındaki tarih, fatura tarihine bağlıdır. Fatura, ayın ilk on beş gününde deftere nakledilirse gelir planı, ayın ilk günü kullanılarak oluşturulur. Fatura, ayın on altıncı gününde veya sonrasında deftere nakledilirse gelir planı, bir sonraki ayın ilk günü kullanılarak oluşturulur.

        - **Ay ortasından bölme** kabul esası **Güne göre mali dönem** olarak ayarlanmışsa seçilemez.

    - **Sonraki ayın/dönemin ilk günü**: Planın başladığı tarih, sonraki ayın veya mali dönemin ilk günüdür.
    - **Ay/dönem sonu**: İlk plan satırındaki tarih, sözleşme başlangıç tarihidir (veya fatura tarihi). Ancak sonraki tüm plan satırları, ayın veya mali dönemin son günü için oluşturulur. 

Genel dönemleri ve her dönemde kabul edilen yüzdeleri görüntülemek için **Gelir planı ayrıntıları** düğmesini seçin. Varsayılan olarak **Kabul etme yüzdesi** değeri, dönem sayısı boyunca eşit olarak bölünür. Kabul esası **Aylık** olarak ayarlanırsa kabul yüzdesi değiştirilebilir. Kabul yüzdesini değiştirdiğinizde bir uyarı iletisi toplamın yüzde 100'e eşit olmadığını belirtir. Bu iletiyi alırsanız satırları düzenlemeye devam edebilirsiniz. Ancak sayfayı kapatmadan önce toplam yüzde 100'e eşit olmalıdır.

[![Gelir planı ayrıntıları.](./media/revenue-schedule-details-2nd-scrn.png)](./media/revenue-schedule-details-2nd-scrn.png)

## <a name="inventory-setup"></a>Stok kurulumu

Satış siparişlerindeki serbest bırakılan ürünler için gelir kabul edebilirsiniz ancak belgeye eklenen madde yoksa satış siparişlerindeki satış kategorileriyle veya serbest metin faturalarıyla kabul edemezsiniz. Serbest bırakılan ürünleri ayarlarken yaptığınız seçimler maddenin gelirinin nasıl kabul edileceğini belirler. Örneğin seçimler, gelir fiyatının tahsis edilip edilmediğini ve gelirin, bir gelir planı kullanılarak ertelenip ertelenmediğini belirler.

Kurulum, **Madde grubu** sayfasının (**Gelir kabulü \> Kurulum \> Stok ve ürün kurulumu \> Madde grubu**) **Gelir kabulü** hızlı sekmesinde başlatılabilir. Bu sayfa, çeşitli kurulum alanları içerir. Bu alanlar yalnızca sistemde oluşturulan yeni serbest bırakılan ürünlerin varsayılan değerlerini ayarlamak için kullanılır. Yeni ürünler oluşturulduğunda, burada ayarladığınız değerler madde grubu için varsayılan olarak girilir. **Serbest bırakılan ürünler** sayfasındaki (**Gelir kabulü \> Kurulum \> Stok ve ürün kurulumu \> Serbest bırakılan ürünler**) serbest bırakılan ürünlerin varsayılan değerlerini geçersiz kılabilirsiniz. Serbest bırakılan ürünler için ayarlanan varsayılan değerler daha sonra satış siparişine taşınır.

## <a name="item-groups-and-released-products"></a>Madde grupları ve serbest bırakılan ürünler

### <a name="define-the-revenue-schedule"></a>Gelir planını tanımlama

Satış siparişi satırındaki gelir, serbest bırakılan ürün için bir gelir planı tanımlanırsa ve satış siparişi satırında varsayılan olarak kullanılırsa ertelenir. Ayarın ürün için varsayılan olarak kullanılması gerektiği durumda gelir planını **Madde grubu** sayfasının (**Gelir kabulü \> Kurulum \> Stok ve ürün kurulumu \> Madde grubu**) **Gelir kabulü** hızlı sekmesinde tanımlayabilirsiniz. Ayrıca serbest bırakılan ürünün ayarını da **Serbest bırakılan ürünler** sayfasının (**Gelir kabulü \> Kurulum \> Stok kurulumu \> Serbest bırakılan ürünler**) **Gelir kabulü** hızlı sekmesinde tanımlayabilirsiniz.

**Gelir planı** alanında, gelirin ertelenmesi gereken dönemi temsil eden gelir planını seçin. Gelir planı, satış siparişi satırına otomatik olarak girilir ve satış siparişi faturası deftere nakledildiğinde plan ayrıntıları oluşturulur.

### <a name="define-the-revenue-price"></a>Gelir fiyatını tanımlama

Madde grupları ve serbest bırakılan ürünler, medyan fiyat yöntemi veya iskonto tahsisat yöntemi kullanılarak ayarlanabilir. İki yöntem için de **Serbest bırakılan ürünler** sayfasında çeşitli ayarlar gerekir:

- **Gelir kabulü etkin**: Serbest bırakılan ürünü gelir tahsisatı hesaplamasına eklemek için bu seçeneği **Evet** olarak ayarlayın. Bu seçenek **Hayır** olarak ayarlanırsa ve medyan fiyat tanımlıysa, serbest bırakılan ürün medyan fiyatı kullanır. Medyan fiyat tanımlı değilse, geliri veya ertelenen geliri deftere nakletmek için satış siparişi satırındaki birim fiyat kullanılır.
- **Gelir türü**: Serbest bırakılan ürünü tanımlayan gelir türünü seçin:

    - **Temel**: Madde, kuruluşun birincil gelir kaynağıdır. Bu değer, varsayılan ayardır.
    - **Temel Olmayan**: Madde, kuruluşun birincil gelir kaynağı değildir. Medyan fiyat ayarları kullanıldığında fiyat, medyan fiyattan "çıkarılır" ve ardından tahsis edilir. Örneğin, temel maddenin gelir için kabul edilmesi gereken bir sabit fiyatı vardır. İskonto varsa iskontonun temel madde gelirinden çıkarılması gerekir ancak bu **yalnızca** en fazla sabit fiyat tutarı kadar olabilir. İskontonun geri kalanı, temel olmayan maddelerin gelirinden çıkarılır. Alternatif olarak iskonto, temel madde gelirinden çıkarılamayabilir.
    - **Sözleşme desteğini deftere naklet**: Madde, müşteriye yapılan satışa dahil olan diğer öğeleri destekler. Gelir fiyatı, satışa dahil olan temel ve temel olmayan ürünlere dağıtılır. Kuruluma bağlı olarak, PCS maddeleri için satış siparişi satırında sözleşme başlangıç ve bitiş tarihlerinin tanımlanması gerekmeyebilir.

- **Çıkarmadan hariç tut**: Maddenin medyan fiyatının tanımlanan minimum yüzdenin altında veya maksimum yüzdenin üstünde ayarlanamayacağını belirtmek için bu seçeneği **Evet** olarak ayarlayın. Gelir fiyatları, satış siparişine dahil olan başka bir serbest bırakılan ürünün gelir fiyatından türetilir. Bu seçenek **Hayır** olarak ayarlanırsa maddenin medyan fiyatı ayarlanabilir veya çıkarılabilir. Medyan fiyat olarak ayarlanan birden fazla madde satarsanız en az bir serbest bırakılan ürün için **Çıkarmadan hariç tut** seçeneğinin **Hayır** olarak ayarlanması gerektiğini unutmayın. Bu şekilde, gelir fiyatındaki farklılıkların tahsis edilebileceği en az bir madde vardır.
- **Medyan fiyat**: Maddenin gelir fiyatının belirttiğiniz minimum toleransın altında veya maksimum toleransın üstünde olması durumunda medyan fiyata eşit olacak şekilde ayarlanması gerektiğini ve **Çıkarmadan hariç tut** seçeneğinin **Hayır** olarak ayarlandığı ürünlere sahip satırlar için çıkarılan tutarın tahsis edilmesi gerektiğini belirtmek için bu seçeneği **Evet** olarak ayarlayın.

    - **Maksimum tolerans**: Medyan fiyatın üzerinde izin verilen yüzdeyi girin.
    - **Minimum tolerans**: Medyan fiyatın altında izin verilen yüzdeyi girin.

Serbest bırakılan ürünün ayarlarını yapılandırmayı tamamladıktan sonra **Gelir fiyatları** sayfasında (**Gelir kabulü \> Kurulum \> Stok kurulumu \> Serbest bırakılan ürünler**'e gidin ve ardından Eylem Bölmesi'ndeki **Satış** sekmesinin **Gelir kabulü** grubunda **Gelir fiyatları**'nı seçin) adil değer fiyatını veya (medyan fiyat yöntemini kullanıyorsanız) medyan fiyatı girerek gelir fiyatını el ile tanımlamanız gerekir.

[![Gelir fiyatları.](./media/revenue-recognition-revenue-prices.png)](./media/revenue-recognition-revenue-prices.png)

Bu sayfada el ile tanımlanan gelir fiyatı, tanımlanan ölçütlere göre her satış siparişindeki gelir fiyatı tahsisatını belirlemek için kullanılır. Her ölçüt, tahsisat işleminde kullanılması gereken gelir fiyatını belirlemek için satış siparişi satırıyla eşleştirilir.

- **Madde kodu** ve **Madde ilişkisi**: Gelir fiyatı tek bir ürün veya ürün grubu için tanımlanabilir. **Madde kodu** alanında **Tablo**'yu seçerseniz **Madde ilişkisi** alanında serbest bırakılan ürünü seçin. **Madde kodu** alanında **Grup**'u seçerseniz **Madde ilişkisi** alanında madde grubunu seçin.
- **Hesap kodu** ve **Hesap/Grup numarası**: Gelir fiyatı tüm müşteriler, tek bir müşteri veya müşteri grubu için tanımlanabilir. **Hesap kodu** alanında **Tümü**'nü seçerseniz fiyat tüm müşteriler için kullanılır. **Hesap kodu** alanında **Tablo**'yu seçerseniz **Hesap/Grup numarası** alanında müşteriyi seçin. **Hesap kodu** alanında **Grup**'u seçerseniz **Hesap/Grup numarası** alanında müşteri grubunu seçin.
- **Para Birimi**: Satış siparişi girdiğiniz her para birimi için ayrı bir gelir fiyatı girmeniz gerekir. Örneğin, şu anda ABD doları, Kanada doları ve avro ile satış yapıyorsanız üç para biriminde de bir gelir fiyatı tanımlamanız gerekir. Gelir fiyatı, muhasebe para birimi gibi bir para biriminden kullandığınız diğer bir hareket para birimine çevrilmez.
- **Tutar veya listenin yüzdesi**: Gelir fiyatının, tutar olarak mı yoksa liste fiyatının yüzdesi olarak mı ayarlanacağını belirtin. **Listenin yüzdesi**'ni seçerseniz kullanıcılar, medyan fiyatı tutar yerine liste fiyatının yüzdesi olarak girebilir. **Listenin yüzdesi** değeri yalnızca PCS maddeleri olarak ayarlanan serbest bırakılan ürünler için kullanılır.
- **Gelir tahsisatı fiyatı**: **Tutar veya listenin yüzdesi** alanında seçtiğiniz değere bağlı olarak satış siparişindeki öğelerden tahsis etmek için kullanılan gelir fiyatını temsil edecek şekilde bir tutar veya yüzde girin.
- **Başlangıç tarihi** ve **Bitiş tarihi**: Gelir fiyatının etkin olacağı tarih aralığını girin. Bu alanlar isteğe bağlıdır.

**Genel muhasebe parametreleri** sayfasındaki **İskonto tahsisat yöntemini etkinleştir** seçeneği **Evet** olarak ve serbest bırakılan ürün için **Gelir türü** alanı **Sözleşme desteğini deftere naklet** olarak ayarlanırsa serbest bırakılan ürün tarafından desteklenen maddeleri de belirtmeniz gerekir. Bu kurulum, **Kurulum esası** sayfasında (**Gelir kabulü \> Kurulum \> Stok kurulumu \> Serbest bırakılan ürünler**'e gidin ve ardından Eylem Bölmesi'ndeki **Satış** sekmesinin **Gelir kabulü** grubunda **Kurulum esası**'nı seçin) yapılır.

**Kurulum esası** sayfasında, maddenin desteklediği her madde grubu için bir kayıt ekleyin. Gelir tahsisatı gerçekleştiğinde gelir fiyatı, PCS öğesinin temel ve temel olmayan kısımlarına dağıtılır.

### <a name="posting-profiles"></a>Deftere nakil profilleri

Üç ek deftere nakil türü, geliri erteleme özelliğini destekler. Bu deftere nakil türleri, **Deftere nakil** sayfasının (**Gelir kabulü \> Kurulum \> Stok ve ürün kurulumu \> Deftere nakil**) **Satış siparişi** sekmesinde ayarlanır.

- **Ertelenen gelir**: Ertelenen gelire (gelir yerine) nakledilen gelir fiyatı için ana hesabı girin. Satış siparişi satırında bir gelir planı varsa gelir fiyatı ertelenir.
- **Satılan malların ertelenen maliyeti**: Gelir de ertelenirse satılan malların ertelenen maliyetine nakledilen satılan malların maliyet tutarı için ana hesabı girin.
- **Kısmi fatura geliri kliringi**: Satış siparişi kısmen faturalandığında veya yeniden tahsis gerçekleştiğinde kullanılan kliring hesabı için ana hesabı girin. Bu hesaptaki bakiye, satış siparişleri tamamen faturalandığında 0 (sıfır) olur.

### <a name="bundles"></a>Ürün demetleri

Ürün demeti maddeleri, bileşenler içerecek şekilde ayarlanan benzersiz serbest bırakılan ürünlerdir. Bu kurulum, ürün reçetesi (BOM) işlevini kullanarak gerçekleştirilir. Satış siparişine bir ürün demeti maddesi girildiğinde gelir fiyatlarını ve gelir planlarını belirlemek için bağımsız bileşenler kullanılır. Ancak müşteri için satış siparişi ve fatura gibi yazılı belgeler ürün demeti maddesini yansıtır.

#### <a name="bundle-components"></a>Ürün demeti bileşenleri

Ürün demetine dahil edilen bileşenler, **Serbest bırakılan ürünler** sayfasında (**Gelir kabulü \> Kurulum \> Stok ve ürün kurulumu \> Serbest bırakılan ürünler**) ayarlanmalıdır. Bu bileşenler, serbest bırakılan ürünlerdir ve bir ürün reçetesine eklenen ürünlerle aynı şekilde ayarlanmalıdır. Örneğin, serbest bırakılan bir ürün, **Madde** veya **Servis** türünde olabilir ancak **Stoğu tutulan ürün** seçeneği **Evet** olarak ayarlanan bir madde model grubuna atanması gerekir. Daha fazla bilgi için ürün reçetesi maddelerinin kurulum belgelerine bakın.

Ayrıca bileşenler, satış siparişinde ayrı ayrı satılabilen ürünlerde olduğu gibi gelir kabulü için de ayarlanmalıdır. Örneğin, her bileşen için doğru gelir fiyatının tanımlandığından ve fiyat esasının PCS maddeleri için ayarlandığından emin olun.

#### <a name="bundle-items"></a>Ürün demeti maddeleri

Bir ürün demeti maddesi ayarladığınızda **Serbest bırakılan ürünler** sayfasında (**Gelir kabulü \> Kurulum \> Stok ve ürün kurulumu \> Serbest bırakılan ürünler**) iki alan ayarlamanız gerekir.

- **Üretim türü** alanında **Mühendis** hızlı sekmesinde madde, ürün reçetesi maddesi olarak ayarlanmalıdır.
- **Ürün demeti** alanında **Genel** hızlı sekmesinde madde, ürün demeti maddesi olarak işaretlenmelidir.

Sonrasında bileşenler, **Ürün reçetesi sürümleri** sayfasında (**Gelir kabulü \> Kurulum \> Stok ve ürün kurulumu \> Serbest bırakılan ürünler**'e gidin ve ardından Eylem Bölmesi'ndeki **Mühendis** sekmesinde **Ürün reçetesi** grubunda **Ürün reçetesi sürümleri**'ni seçin) ürün demeti/ürün reçetesi üst maddesine atanmalıdır. Daha fazla bilgi için ürün reçetelerinin kurulum belgelerine bakın.

[![Serbest bırakılan ürünler, ürün reçetesi planları.](./media/revenue-recognition-bom-scheduleds.jpg)](./media/revenue-recognition-bom-scheduleds.jpg)

Ürün demeti üst maddesi ve ürün demeti bileşenleri tahsis edilecek şekilde ayarlanırsa ürün demeti gelir fiyatı, gelir katkısı yüzdelerine göre bileşenlere dağıtılır.

## <a name="project-setup"></a>Proje kurulumu

Gelir kabulü ayrıca Zaman ve malzeme projesi üzerinden oluşturulan satış siparişleri için de kullanılabilir. Projelerden kaynaklanan satış siparişleri için ana hesapları yalnızca proje faturalarını deftere nakletmek üzere kullanılan proje deftere nakil profillerinde tanımlamanız gerekir. Ana hesaplar, **Genel muhasebeye nakil ayarı** sayfasında (**Gelir kabulü \> Kurulum \> Proje kurulumu \> Genel muhasebeye nakil ayarı**) tanımlanır.

- **Ertelenen fatura geliri** (**Gelir hesapları** altında): Ertelenen gelire (gelir yerine) nakledilen gelir fiyatı için ana hesabı girin. Satış siparişi satırında bir gelir planı varsa gelir fiyatı ertelenir.
- **Ertelenen maliyet** (**Maliyet hesapları** altında): Gelir de ertelenirse satılan malların ertelenen maliyetine nakledilen satılan malların maliyet tutarı için ana hesabı girin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
