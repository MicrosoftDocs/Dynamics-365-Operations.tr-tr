---
title: "İş planlaması için Gantt şeması"
description: "Üretim planlayıcıları Gantt şemalarını kullanarak üretim planlarını denetleyebilir ve en iyi duruma getirebilirler."
author: johanhoffmann
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5a4b0450cc76c8d9307b9b21b78a170afcc298e4
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="gantt-chart-for-job-scheduling"></a>İş planlaması için Gantt şeması

[!include[banner](../includes/banner.md)]

Gantt grafiği üretim planlayıcılarını üretim planını denetleme ve en iyi duruma getirme konusunda desteklemek için tasarlanmıştır. Gantt grafiği işlem akışını saydam hale getirir ve üretim planını malzeme veya kaynak eksikliklerini göz önünde bulundurarak kolaylıkla düzenlemeyi sağlar. Planlayıcıların kullanılabilir kaynaklardan en iyi şekilde yararlanmasına, ilerlemedeki işi en aza indirmesine ve üretim emirleri için çıkış sürelerini optimize etmesine yardımcı olur..

Gantt grafiği belirli bir zaman aralığındaki planlanmış faaliyetlerin görsel temsilidir. Faaliyetler kapasite takvimi tarafından kapasitesi olan kaynaklar üzerinden planlanır. Gantt şemasında aşağıdaki türde faaliyetler görüntülenebilir.

-   Planlanmış iş olan üretim emirlerinden gelen işler.
-   Planlı üretim emirlerinden gelen işler.
-   Saat tahmini türündeki iş planlama projesi faaliyetleri.

Gantt grafiği iki farklı görünümde açılabilir: **Sipariş görünümü** ve **Kaynak görünümü**[](https://authoring.help.dynamics.com/en/?post_type=incsub_wiki&p=1665154&preview=true). **Sipariş görünümünde**, faaliyetler üretim emirleri altında gruplandırılır. Örneğin, aynı siparişlere ait işlerin genel görünümünü korumak istiyorsanız bu faydalı olabilir. **Kaynak görünümünde** tüm işler ayrı kaynakların altında gruplanır. Bu görünüm, planı kaynak düzeyinde (örneğin bir makine veya makine grubu) optimize ederken faydalı olabilir. Aşağıdaki örnekte verilen Gantt grafikleri şu temel öğelerle birlikte **Sipariş görünümü** ve **Kaynak görünümünü** gösterir:

1.  Gantt grafiği faaliyeti
2.  Malzeme eksikliği simgesi
3.  Malzeme kullanılabilirliği simgesi
4.  Sipariş teslim tarihi simgesi
5.  Kapasite çubuğu

## <a name="order-view"></a>Sipariş görünümü

[![Sipariş görünümü](./media/orderview.png)](./media/orderview.png)

## <a name="resource-view"></a>Kaynak görünümü
[![Kaynak görünümü](./media/resview.png)](./media/resview.png)

## <a name="activities"></a>Faaliyetler
Faaliyetler çubuklar şeklinde görünür ve zaman ölçeği ızgarasında planlanan başlangıç ve bitiş zamanıyla organize edilir; çubukların uzunluğu faaliyeti tamamlamak için gereken süreyle orantılıdır. Faaliyetler zaman dilimine göre gösterilir. Bir başlangıç ve bitiş tarihi ile örneğin gün veya saat gibi bir zaman birimi seçtiğiniz menüdeki zaman ölçeğini ayarlayabilirsiniz. Zaman ölçeğini ayarlayarak, faaliyetleri yönetmek istediğiniz zaman aralığına odaklanabilirsiniz. 

Daha iyi bir genel görünümün almak için, faaliyetlerin rengini denetleyebileceğiniz farklı renk seçenekleri bulunur. Faaliyetler için ayrı renkler yapılandırabilir, uygulama için kullanılan genel renk olan tema rengini kullanabilir veya üretim emirleri için renk koduna göre kontrol edilen renk ayarlayabilirsiniz. 

Faaliyetlerin zaman aralığında arka plan gölgesi bulunur. Beyaz gölgeli dönemler faaliyet için kaynakta tanımlanmış kapasite bulunan zaman aralığını gösterirken, gri gölgeli dönemler tanımlanan kapasite bulunmayan zaman aralıklarını gösterir. 

Grafiğin sol tarafında faaliyetle ilgili ek bilgiler bulunur. Örneğin faaliyetin planlandığı kaynak ve üretim emri numarası. Aynı siparişe ait işler arasındaki bağlantı ok ile gösterilir. 

Faaliyet iletişim kutusundan, bir faaliyet hakkında daha fazla bilgi alabilirsiniz. İletişim kutusunu açmak için faaliyete çift tıklayın veya **Bilgiler** menüsünü seçin. Faaliyet iletişim kutusunda, planlanan başlangıç ve bitiş tarihi ile faaliyetin hangi malzemeleri tüketmesinin planladığına ilişkin zaman bilgisini görebilirsiniz. 

Faaliyetleri Gruplandırma düzeylerinde gruplandırılabilir. Gruplandırma düzeyleri hiyerarşiktir ve faaliyetler için mantıksal bir gruplandırma yapmak üzere kullanılabilir. Örneğin, üretim faaliyetlerinin Tesis, Üretim birimleri, Kaynak grupları ve Kaynaklara göre gruplandırıldığı bir düzeniniz varsa, Gruplandırma düzeylerini faaliyetleri bu düzene göre gruplandırmak için kullanabilirsiniz. Gruplandırma düzeyleri tek tek gruplandırma düzeyi veya grafikteki tüm düzeyler için menüdeki **Tümünü Genişlet** ve **Tümünü Daralt** düğmeleri kullanılarak genişletilebilir ve daraltılabilir. Ayrıca, gruplandırma düzeylerini grafik açıldığı zaman genişletilecek veya daraltılacak şekilde yapılandırabilirsiniz.

### <a name="material-availability"></a>Malzeme kullanılabilirliği

Gantt grafiği ayrı faaliyetler için malzeme durumu hakkında planlayıcıya ayrıntılı bilgi sağlamak için ayarlanabilir. Örneğin, bu malzemenin gecikmesi ve üretim planını etkilemesi durumunda yararlı olabilir. Bu durumda, malzeme sorunları Gantt grafiğinde vurgulanarak planlayıcının sonuçları anlamasına ve gerekli ayarlamaları yapmasına yardımcı olur. 

İşin planlanan başlama tarihi iş tarafından tüketilen malzemenin kullanılabilirlik tarihinden daha sonraysa, iş malzeme eksikliği simgesiyle birlikte gösterilir. Malzeme kullanılabilirlik tarihi dinamik master plandaki ilişkilendirme bilgileri temel alınarak hesaplanır. Örneğin malzeme eksikliği simgesi, işin planlanan başlama tarihinden daha sonra olan bir girişi bulunan satın alma siparişine karşı ilişkilendirilen bir malzeme tüketen bir iş için görüntülenir.

### <a name="indicator-of-material-availability-date"></a>Malzeme kullanılabilirlik tarihi göstergesi

Grafiği malzeme eksikliği olan işleri göstermek üzere ayarlarsanız, iş için malzeme kullanılabilirlik tarihini gösteren bir simge de gösterilir. Simge yalnızca malzeme kullanılabilirlik tarihinin grafiğin tanımlanan zaman aralığında olması durumunda gösterilir. Malzeme kullanılabilirlik tarihi tanımlanan zaman aralığının dışındaysa, iş iletişim kutusundaki malzeme listesinden daha ayrıntılı malzeme kullanılabilirlik bilgileri alınabilir. Listede aynı zamanda iş için geç olan malzemeleri gösteren bir simge de bulunur. Malzeme kullanılabilirlik tarihini başlangıç tarihi olarak kullanarak işi yeniden planlayabilirsiniz.

### <a name="indicator-of-order-delivery-date"></a>Siparişi teslim tarihi göstergesi

Bu simge bir üretim emri için teslimat tarihini belirtir. Simge sadece Sipariş görünümünde görülebilir.

### <a name="capacity-bar"></a>Kapasite çubuğu

Grafiği bir kaynak kapasitesi çubuğu gösterecek şekilde yapılandırabilirsiniz. Bu çubuk, grafiğin tanımlanan zaman aralığındaki bir faaliyet için kaynak kapasitesi genel görünümünü sağlar. Kapasite çubuğu kaynak ayrılmamış dönemler için gösterilmez. Kaynağın kapasite için ayrıldığı dönemlerde, kapasite çubuğu düz çubuk olarak gösterilir. Kaynağın kapasitesi üzerinde ayrılmış olduğu dönemlerde çubuk daha kalın ve kırmızı renkte gösterilir. Örneğin, iki iş çakışıyorsa, kapasite çubuğu çakışmanın olduğu zaman aralığı için kapasite üzerinde ayırma belirtecektir. Kapasite çubuğu bir iş planladığınızda otomatik olarak güncelleştirilir. Kapasite çubuğunu **Kapasite çubuğunu göster** menüsünden etkinleştirebilirsiniz. Yalnızca **Kaynak görünümünde** görünür. Kaynaktaki yük kapasitesi hakkında daha ayrıntılı görünüm almak için menüden veya seçilen faaliyetin bağlam menüsünden açabileceğiniz **Yük kapasitesi** grafiğini kullanın.

## <a name="job-scheduling-in-the-gantt-chart"></a>Gantt grafiğinde iş planlama
Gantt grafiği üretim planında ayarlama yapmak için farklı seçenekler sunar. Gantt grafiğinde, faaliyetleri sürükle bırak etkileşimi olarak veya bir plan menüsünden yeniden planlayabilirsiniz. Planlama işleminde kaynak kapasitesini, kaynak yeteneklerini ve hesap için malzeme kısıtlamalarını dikkate alabilirsiniz.

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a>Bir işi sürükle bırak etkileşimi olarak planlama

İşi belirlenen zaman aralığı içinde bir sürükle bırak etkileşimi olarak yeniden planlayabilirsiniz. İşi yalnızca aynı kaynakta planlayabilir ve bir kerede yalnızca tek bir iş planlayabilirsiniz.

### <a name="schedule-a-job-from-the-menu"></a>Menüden iş planlama

**İşleri planla** menüsünden, bir planlama yönü ve planlama tarihi saatini temek alarak grafikte bir veya daha fazla seçili işi planlayabilirsiniz. Üç farklı planlama yönü vardır.

-   İş planlama çizelgeleme tarihinden ileriye doğru
-   İş planlama çizelgeleme tarihinden geriye doğru
-   Malzeme kullanılabilirlik tarihinden sonrası

Bir işin Gannt grafiğinin belirlenen zaman aralığı dışında planlamak mümkün değildir. Bunu yaparsanız, iş planlanmamış olarak kalır ve "İş yüklenen zaman dönemi içinde planlanamadı" hata iletisini alırsınız.

### <a name="schedule-previous-jobs"></a>Önceki işleri planla

Aynı üretim emrine ait olan işler gibi bir faaliyetler ağında, önceki işi ağda seçilen bir işle ilişkili planlamak için **Önceki işleri planla** işlevini kullanabilirsiniz. Aşağıdaki örnekte vurgulanan faaliyet seçili iştir. Diyagram, önceki iş zamanlanmadan önce ve önceki iş zamanlandıktan sonrayı gösterir. 

[![Önceki işi planla](./media/schprevjob3.png)](./media/schprevjob3.png)

### <a name="schedule-next-jobs"></a>Sonraki işleri planla

Faaliyet ağındaki seçili bir işle ilgili olan sonraki işleri planlamak için **Sonraki işleri planla** işlevini kullanabilirsiniz. Aşağıdaki örnekte vurgulanan faaliyet seçili iştir. Diyagram, sonraki iş zamanlanmadan önce ve sonraki iş zamanlandıktan sonrayı gösterir. 

[![Sonraki işi planla](./media/schnxtjob.png)](./media/schnxtjob.png)

### <a name="schedule-around-job"></a>İşe göre planla

Faaliyet ağındaki seçili bir işle ilgili olan önceki ve sonraki işleri planlamak için **İşe göre planla** işlevini kullanabilirsiniz. Aşağıdaki örnekte vurgulanan faaliyet seçili iştir. Diyagram, iş zamanlanmadan önce ve iş zamanlandıktan sonrayı gösterir. 

[![İşe göre planla](./media/scharoundjob1.png)](./media/scharoundjob1.png)

### <a name="arrange-jobs"></a>İşleri düzenle

Aynı kaynak üzerindeki seçili faaliyetleri düzenlemek için **Düzenle** işlevini kullanabilirsiniz. Bu faaliyetler aynı faaliyet ağında olabileceği gibi farklı ağlara da ait olabilir. Düzenleme işlevini kullandığınızda seçili eylemler arasındaki zaman boşlukları ortadan kaldırılacaktır. Bu işlevi kaynakların kapasite kullanımını optimize etmek için kullanabilirsiniz. Diyagram, iş zamanlanmadan önce ve iş zamanlandıktan sonrayı gösterir. 

[![İşi düzenle](./media/arrangejobs1.png)](./media/arrangejobs1.png)

### <a name="reassign-activities-from-one-resource-to-another"></a>Faaliyetleri bir kaynaktan diğerine atama

Bir işi bir kaynaktan başka bir kaynağa atayabilirsiniz. Bu, bir makine kullanım dışı veya kapasitesi üzerinde dolu olduğunda ve işi yapabilecek başka bir kaynak bulmanız gerektiğinde yararlı olabilir.

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a>Bir faaliyeti sürükle bırak etkileşimi olarak yeniden atama

**Kaynak** görünümünde, bir faaliyeti Gannt grafiğindeki başka bir kaynağa sürükle bırak etkileşimi olarak yeniden atayabilirsiniz. Bunu, faaliyetin planlandığı satırı seçerek yapabilirsiniz. Satırı seçtikten sonra satırı farkı bir kaynak gruplandırma düzeyi altında gruplandırılan bir kaynağa sürükleyebilirsiniz.

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a>Faaliyeti İşleri planla menüsünden yeniden atama

Bir işi **İşi planla** menüsünden açılan **İşi planla** iletişim kutusundan yeniden atayabilirsiniz. Bu menüden, bir işi yalnızca daha önce Gantt grafiğine yüklenmiş olan bir kaynağa yeniden atayabilirsiniz. Yalnızca tek bir iş seçerseniz, kaynak için açılan liste uygulanabilir kaynaklara göre sıralanır. Birden fazla iş seçerseniz, kaynak listesindeki uygulanabilir kaynaklarla ilgili bilgi olmayacaktır.

## <a name="load-additional-resources-to-the-gantt-chart"></a>Gantt grafiğine ek kaynaklar yükleme
**Kaynak görünümünde**, Gantt grafiğine ek kaynaklar yükleme seçeneğiniz bulunur. Kapasitesi üzerinde rezerve edilen veya arızalı bir makine üzerinde planlanan bir iş için alternatif bir kaynak bulmak istediğinizde yararlı olabilir. **Ek kaynaklar yükle** sayfasında, listenin açıldığı tarihte tarihleri geçerli olan kaynakların listesini elde edersiniz. Gantt grafiğinde seçilen işle ilgili uygulanabilir kaynaklar önce listelenir. Birden fazla işi seçmiş olmanız durumunda, liste açılmadan önce, uygun kaynaklarla ilgili bir gösterge gösterilmez. **Ek kaynaklar yükle** sayfasında, seçiminizi onayladığınızda Gantt grafiğine yüklenecek bir veya daha fazla kaynak seçebilirsiniz. Seçilen kaynakta Gantt grafiğinin zaman aralığında planlamış iş yoksa, kaynak Gantt grafiğindeki faaliyet listesinin alt kısmındaki bir kaynak gruplandırma düzeyi altına yerleştirilir.

### <a name="access-the-gantt-chart"></a>Gantt grafiğine erişme

Gantt grafiği aşağıdaki sayfalardan açılabilir.

| **Sayfa**                                                                                     | **Açıklama**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Üretim emri listesi ve ayrıntıları**                                                         | **Üretim emri listesi ve ayrıntıları** sayfasında, Gantt grafiğini bir veya daha fazla seçili siparişten açabilirsiniz. Grafiği **Gantt grafiği** menü öğesinden açmak seçili üretim emirleriyle ilgili tüm işleri yükler, ancak aynı kaynaklar üzerinde planlanan diğer üretim emirlerindeki işler de yüklenir. Grafiği **Gantt grafiği - Hızlı görünüm** menü öğesinden açmak yalnızca seçili üretim emirleriyle ilişkili işleri yükler. Bu görünümde, işleri planlamak mümkün değildir. |
| **Kaynak**                                                                                 | **Kaynak** sayfasında, Gantt grafiğini **Gantt grafiği** menü öğesinden açabilirsiniz. Seçildiğinde, seçili bir zaman aralığı için kaynak üzerinde planlanmış olan tüm işler grafiğe yüklenir.                                                                                                                                                                                                                                                                                                   |
| **Kaynak grubu**                                                                           | **Kaynak grubu** sayfasında, Gantt grafiğini **Gantt grafiği** menü öğesinden açabilirsiniz. Seçildiğinde, kaynak grubundaki kaynaklar üzerinde planlanmış olan tüm işler seçilen zaman aralığında gösterilir.                                                                                                                                                                                                                                                                                    |
| **Gantt grafikleri**                                                                             | **Gantt grafikleri** sayfasında, Gantt grafiklerini kaynaklara ve kaynak gruplarına göre yapılandırabilirsiniz. Örneğin, üretim faaliyetlerini belirli kaynak veya kaynak grubu kümeleri için denetlemek istiyorsanız, **Gantt grafikleri** sayfasındaki kaynaklar için ayrı yapılandırmalar yapabilirsiniz. Daha sonra her yapılandırmadaki Gantt grafiğini açabilirsiniz.                                                                                                                                                    |
| **Saat tahminleri** (proje)                                                                 | **Saat tahmini** türündeki proje faaliyetleri kaynaklar üzerinde planlanan iş olabilir. **Planlama** menüsündeki **Saat tahmini** sayfasında, işin saat tahmini türündeki planlanan proje faaliyetlerini görmek için bir siparişteki Gantt grafiğini açabilirsiniz.                                                                                                                                                                                                                                                             |
| **Tamamlanacak iş** (**Üretim katı yönetimi** çalışma alanındaki liste)                      | **Üretim katı yönetimindeki tamamlanacak iş listesi** çalışma alanı, çalışma alanında seçili kaynaklar için yürütülmekte olan üretim ve toplu iş emirlerindeki işleri gösterir. **Gantt grafiği** menü öğesinde Gantt grafiğini açabilirsiniz; listede seçili tüm işler grafiğe yüklenecektir.                                                                                                                                                                                |
| **Serbest bırakılacak üretim emirleri** (**Üretim katı yönetimi** çalışma alanından açılan) | Serbest bırakılacak üretim emirleri sayfası **Üretim katı yönetimi** çalışma alanından açılır. Bu sayfa, serbest bırakma işlemi bekleyen planlanmış üretim ve toplu iş emirlerini gösterir. Bu sayfada, seçili üretim emirleri için Gantt grafiğini açabilirsiniz.                                                                                                                                                                                                                                                        |
## <a name="see-also"></a>Ayrıca bkz.  
[Ürün ve toplu siparişler için Gantt şemasıyla görsel planlama (Video)](https://youtu.be/BtbuShkGj4I)

[Üretim için görsel planlama (demo kod)](https://mbs.microsoft.com/customersource/northamerica/365Enterprise/learning/documentation/how-to-articles/365finoptvisschep)


