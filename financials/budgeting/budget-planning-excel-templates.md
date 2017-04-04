---
title: "Excel için bütçe planlama şablonları"
description: "Bu konuda bütçe planlarıyla kullanılabilmesi için Microsoft Excel şablonlarının nasıl oluşturulacağı açıklanmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>Excel için bütçe planlama şablonları

Bu konuda bütçe planlarıyla kullanılabilmesi için Microsoft Excel şablonlarının nasıl oluşturulacağı açıklanmaktadır.

Bu konuda bütçe planlarıyla standart demo veri kümesi ve yönetici kullanıcı oturum açma kullanarak kullanılacak Excel şablonlarının nasıl oluşturulacağı gösterilir. Bütçe planlama hakkında daha fazla bilgi için bkz: [bütçe planlamaya genel bakış.](budget-planning-overview-configuration.md) Takip edebilirsiniz [bütçe planlama 101](budget-plan.md) temel modül yapılandırma ve kullanım ilkelerini öğrenmek için öğretici.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Bütçe plan belge düzenini kullanan bir çalışma sayfası oluşturmak
Bütçe plan belgeler görüntülenebilir ve bir veya daha fazla düzenleri kullanılarak düzenlenebilir. İlgili bütçe planı belge şablonu görüntülemek ve bir Excel çalışma sayfasındaki bütçe planı verileri düzenlemek için her düzeni olabilir. Bu konuda, varolan bir düzeni yapılandırma'yı kullanarak bir bütçe planı belge şablonu oluşturulur. Açık **bütçe planları listesi** (**bütçeleme**&gt;**bütçe planları**). ' I **yeni** yeni bir bütçe planı belge oluşturmak için. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Kullanım **Ekle** satır satır eklemek için seçenek. ' I **düzenleri** bütçe planı belge düzeni yapılandırmasını görüntülemek için. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Düzen yapılandırmasını gözden geçirin ve gerektiği gibi ayarlayın. Git **şablon**&gt;**Generate** bu düzen için bir Excel dosyası oluşturmak için. Şablon oluşturulduktan sonra Git **şablon**&gt;**Görünüm** açın ve belge şablonu bütçe planı gözden geçirmek için. Excel dosyayı yerel sürücünüze kaydedebilirsiniz. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Bütçe plan belge düzeni Excel şablonu onunla ilişkilendirilen sonra düzenlenemez. Düzeni değiştirmek için ilişkili Excel şablon dosyasını silmek ve onu yeniden. Bu alanların düzenini korumak için gereklidir ve çalışma eşitlenir. 

Excel şablonu bütçe planı belge düzeninden tüm öğeleri içerecek nerede **çalışma sayfasında kullanılabilir** sütununda True olarak ayarlanır. Çakışan öğeler Excel şablon içinde izin verilmez. Düzen isteği S1, S2 isteği, istek Q3 ve isteği S4 sütunlar ve 4 üç aylık tüm sütunların toplamını temsil eder bir toplam istek sütun içeriyorsa, örneğin, üç aylık sütunlar veya toplam sütun yalnızca Excel şablon kullanılmak üzere kullanılabilir. Tablosundaki veriler güncelliğini yitirmiş veya hatalı olabilir çünkü Excel dosyasını güncelleştirme sırasında çakışan sütunları güncelleştiremiyor.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Excel kullanarak bütçe planı veri görüntüleme ve düzenleme ile ilgili olası sorunları önlemek için aynı kullanıcı iki Dynamics 365 işlemleri ve Microsoft Dynamics Office eklenti veri bağlayıcısı için oturum.

## <a name="add-a-header-to-budget-plan-document-template"></a>Bütçe planı belge şablonu için bir başlık ekleme
Başlık bilgilerini eklemek için Excel dosyasında en üst satırı seçin ve boş satır ekleyin. ' I **tasarım** içinde **Veri Bağlayıcısı** üstbilgi alanları Excel dosyasına eklemek için.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

İçinde **tasarım** sekmesinde ** **'ı **Ekle** alanları seçin ve **BudgetPlanHeader** varlık veri kaynağı olarak.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Excel dosyayı istediğiniz konuma imleci üzerine gelin. ' I **Etiket Ekle** seçili konuma alan etiketi eklemek için. Seçin **değer Ekle** seçilen yere değer alanı eklemek için. ' I **yapılan** tasarımcıyı kapatın.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Bütçe plan belge şablonu tablosu için hesaplanan sütun ekleme
--------------------------------------------------------------

Sonraki, hesaplanmış sütunları oluşturulan bütçe planı belge şablonuna eklenir. A **toplam istek** isteği S1 özetleyen sütun: İstek 4 sütun ve bir **ayarlama** yeniden hesaplar sütun, **toplam istek** sütun tarafından önceden tanımlanmış bir faktör.

' I **tasarım** içinde **Veri Bağlayıcısı** tabloya sütun eklemek için. ' I **düzenleme** yanında **BudgetPlanWorksheet** sütun eklemeye başlamak için veri kaynağı.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Seçili alan Grup şablonda kullanılabilir sütunları görüntüler. ' I **formül** yeni bir sütun eklemek için. Yeni sütuna ad verin, sonra formüle yapıştırmak için **formül** alan. ' I **Update** sütun eklemek için.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Formül tanımlamak için elektronik tabloda formül oluşturmak ve sonra kopyalamak **tasarım** penceresi. Dynamics 365 ilişkili tablo işlemleri için genellikle "AXTable1" olarak adlandırılır. İstek S1 özetlemek için örneğin,: İstek S4 sütunlarda formül elektronik tablo AxTable1 =\[isteği S1\]+ AxTable1\[isteği S2\]+ AxTable1\[iste Q3\]+ AxTable1\[isteği S4\].

Eklemek için bu adımları yineleyin **ayarlama** sütun. Formül kullan AxTable1 =\[toplam istek\]\*$ı $ bu sütun için 1. Bu I1 hücredeki değeri alın ve değerleri çarpmak **toplam istek** Ayarlama tutarlarını hesaplamak için sütun.

Excel dosyayı kaydedip kapatın. Ve işlemleri için dönmek için Dynamics 365 **düzenleri**,'ı **şablon &gt;karşıya** bütçe plan için kullanılmak üzere kaydedilen Excel şablonunu karşıya yüklemek için. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Kapat **düzenleri** kaydırıcıyı. İçinde **bütçe planı** 'ı tıklatın, belge **çalışma** görüntülemek ve Excel'de belge düzenlemek için. Düzeltilmiş Excel şablonu bu bütçe planı çalışma sayfası oluşturmak için kullanılan Not ve hesaplanan sütunlar önceki adımlarda tanımlanan formüller kullanılarak güncelleştirilir. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>İpuçları ve püf noktaları için bütçe planı şablonları oluşturma
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Ben ekleyebilir ve ek veri kaynakları için bir bütçe planı şablonu kullanabilirsiniz?

Evet, kullanabilirsiniz **tasarım** ek bir varlıkları aynı veya Excel şablon içindeki diğer sayfalar eklemek için menü. Örneğin, eklemek **BudgetPlanProposedProject** oluşturmak ve ne zaman bütçe ile çalışma planı verileri Excel'de aynı anda önerilen projelerin listesini güncelleştirmek için veri kaynağı. Yüksek hacimli veri kaynakları da dahil olmak üzere Excel çalışma kitabının performansı etkileyebilir unutmayın. 

Kullanabileceğiniz **filtre** seçeneğini **Veri Bağlayıcısı** ek veri kaynakları için istenen filtreleri eklemek için.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Diğer kullanıcılar için veri bağlayıcısı tasarım seçeneğinde gizleyebilirim?

Evet, açık **Veri Bağlayıcısı** seçenekleri gizlemek için **tasarım** diğer kullanıcıların seçeneği.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Genişletin **veri bağlayıcı seçeneklerini** ve temizlemek **tasarım etkinleştir** onay kutusu. Bu gizleme **tasarım** gelen seçenek **Veri Bağlayıcısı**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Kullanıcıların yanlışlıkla veri bağlayıcısı verilerle çalışırken kapatılmasını engelleyebilir miyim?

Onu kapatmadan kullanıcıları engellemek için şablon kilitleme öneririz. Kilidi açmak için tıklatın **Veri Bağlayıcısı**, üst sağ köşe bir ok görünür. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Ek bir menü için oku tıklatın. Seçin **kilit**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Bütçe plan Şablonlarım hücre biçimlendirme, renkleri, koşullu biçimlendirme ve grafikler gibi diğer Excel özelliklerini kullanabilir miyim?

Evet, standart Excel özelliklerinden en iyi bütçe planı şablonlarında çalışmaz. Renk kodlama kullanıcılar için salt okunur ve düzenlenebilir sütunlar arasında ayrım yapmak için kullanmanızı öneririz. Koşullu biçimlendirme, bütçenin sorunlu alanları vurgulamak için kullanılabilir. Sütun toplamlarını tablonun üstündeki standart Excel formülleri kullanarak kolayca sunulabilir.

Ayrıca, oluşturabilir ve ek gruplandırmalar ve bütçe verilerinin görsel öğeler için Özet Tablolar ve grafikler kullanın. Üzerinde **veri** sekmesini **bağlantıları** 'ı tıklatın, grup **Tümünü Yenile**ı **bağlantı özellikleri**. ' I **kullanım** sekme. Altında **yenileme**, select **dosyayı açarken verileri Yenile** onay kutusu. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)


