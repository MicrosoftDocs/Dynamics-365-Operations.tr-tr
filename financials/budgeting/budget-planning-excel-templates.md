---
title: "Excel&quot;de bütçe planlama şablonları"
description: "Bu konu bütçe planlamalarında kullanılabilecek Microsoft Excel şablonlarının nasıl oluşturulacağını açıklar."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2ae8255a84f36af624e915e85bc769a8ca37fa7e
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="budget-planning-templates-for-excel"></a>Excel'de bütçe planlama şablonları

[!include[banner](../includes/banner.md)]


Bu konu bütçe planlamalarında kullanılabilecek Microsoft Excel şablonlarının nasıl oluşturulacağını açıklar.

Bu konu, standart demo veri kümesi ve Yönetici kullanıcı oturum açma kullanarak bütçe planlamalarında kullanılacak Excel şablonlarının nasıl oluşturulacağını gösterir. Bütçe planlama hakkında daha fazla bilgi için bkz: [Bütçe planlamaya genel bakış.](budget-planning-overview-configuration.md) Ayrıca [Bütçe planlama 101](budget-plan.md) eğitime de temel modül yapılandırması ve kullanım prensipleri için göz atabilirsiniz.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Bütçe planlama belge şablonu kullanarak bir çalışma sayfası oluşturun
Bütçe planlama belgeleri bir veya daha fazla düzen kullanılarak görüntülenebilir ve düzenlenebilir. Her düzen, bir Excel çalışma sayfasında bütçe planını görüntülemek ve düzenlemek için ilişkili bir bütçe planlama belgesi şablonuna sahip olabilir. Bu konuda, bir bütçe plan belgesi şablonu, varsayılan düzen yapılandırması kullanılarak oluşturulacaktır. **Bütçe planları listesini** (**Bütçeleme**&gt; **Bütçe planları**) açın. Yeni bir bütçe plan belgesi oluşturmak için **Yeni** üzerine tıklayın. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Satır eklemek için **Ekle** seçeneğini kullanın. Bütçe planı belge düzeni yapılandırmasını görüntülemek için **Düzenler** üzerine tıklayın. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Düzen yapılandırmasını gözden geçirebilir ve gerektiği gibi ayarlayabilirsiniz. **Şablon** &gt; **Oluştur** üzerine giderek bu düzen için bir Excel dosyası oluşturun. Şablon oluşturulduktan sonra, **Şablon** &gt; **Görüntüle** üzerine giderek açın ve bütçe planı belge şablonunu görüntüleyin. Excel dosyasını yerel sürücünüze kaydedebilirsiniz. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Bütçe planı belgesi düzeni, bir Excel şablonu onunla ilişkilendirilen sonra düzenlenemez. Düzeni değiştirmek için ilişkili Excel şablon dosyasını silin ve onu yeniden oluşturun. Bu, düzendeki ve çalışma sayfasındaki alanları eşit tutmak için gereklidir. 

Excel şablonu bütçe planı belgesi düzenindeki **Çalışma Sayfasında kullanılabilir** sütunu Evet olarak ayarlanmış tüm öğeleri içerecektir. Excel şablonunda çakışan öğelere izin verilmez. Örneğin, eğer düzen İstek Q1, İstek Q2, İstek Q3 ve İstek Q4 sütunlarını içeriyorsa ve toplam istek sütunu, tüm 4 çeyreklik sütunların toplamını temsil ediyorsa, yalnızca çeyrek sütunları veya toplam sütun Excel şablonunda kullanılmaya açıktır. Excel şablonu çakışan sütunları güncelleştirme boyunca güncelleştiremez çünkü tablo içerisindeki verilerin tarihi geçebilir ve hatalı olabilirler.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Excel kullanarak bütçe planı verisini düzenleme ve görüntüleme ile ilgili potansiyel sorunları önlemek için, Dynamics 365 for Operations ve Microsoft Dynamics Office Add-in Data Connector için aynı kullanıcı oturum açmış olmalıdır.

## <a name="add-a-header-to-budget-plan-document-template"></a>Bütçe planı belge şablonuna bir başlık ekleyin
Başlık bilgisi eklemek için, Excel dosyasındaki üst satırı seçin ve boş satırlar ekleyin. **Veri Bağlayıcısı** içerisinde **Tasarım** üzerine tıklayarak Excel dosyasına başlıklar ekleyin.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

**Tasarım** sekmesinde, ** **tıklayın **Ekle** alanlar üzerine ve sonra varlık veri kaynağı olarak **BudgetPlanHeader** seçin.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

İmleci Excel dosyası üzerinde istenilen konuma getirin. Seçilen konuma alan etiketi eklemek için **Etiket ekle** üzerine tıklayın. Seçilen yere değer alanı eklemek için **Değer Ekle** seçeneğini işaretleyin. Tasarımcıyı kapatmak için **Kapat** üzerine tıklayın.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Bütçe planı belge şablonu tablosuna bir hesaplanmış sütun ekleyin
--------------------------------------------------------------

Daha sonra, hesaplanmış sütunlar, oluşturulmuş bütçe planı belge şablonuna eklenir. Bir **Toplam istek** sütunu, İstek Q1: İstek Q4 sütunlarını toplar ve bir **Ayarlama** sütunu, **Toplam İstek** sütununu önceden belirlenmiş bir faktör ile yeniden hesaplar.

**Veri Bağlayıcısı** içerisinde **Tasarım** üzerine tıklayarak tabloya sütunlar ekleyin. **BudgetPlanWorksheet** veri kaynağının yanındaki **Düzenle** üzerine tıklayarak sütunlar eklemeye başlayın.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Seçili alan grubu, şablonda kullanılan sütunları görüntüler. Yeni bir sütun eklemek için **Formül** üzerine tıklayın. Yeni sütuna bir ad verin ve formülü **Formül** alanına yapıştırın. Sütunu yerleştirmek için **Güncelleştir** düğmesini tıklatın.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Formülü tanımlamak için, formülü elektronik tabloda oluşturun ve sonra **Tasarım** penceresine yapıştırın. Dynamics 365 for Operations'a bağlı bir tablo genellikle "AXTable1" olarak adlandırılır. Örneğin, İstek Q1 : İstek Q4 sütunlarını elektronik sayfada özetlemk için, formül = AxTable1\[İstek Q1\]+AxTable1\[İstek Q2\]+AxTable1\[İstek Q3\]+AxTable1\[İstek Q4\].

**Ayarlama** sütununu eklemek için bu adımları tekrarlayın. Şu formülü kullanın = AxTable1\[Toplam istek\]\*$I$1 bu sütun için. Bu, hücre I1 içindeki değeri alır ve **Toplam istek** içindeki değerleri, ayarlama tutarlarını hesaplamak için çarpar.

Kaydedin ve Excel dosyasını kapatın. Dynamics 365 for Operations'a geri dönün ve **Düzenler** içerisinde **Şablon &gt; Karşıya Yükleme** üzerine tıklayarak kaydedilmiş Excel şablonunu bütçe planında kullanılmak üzere karşıya yükleyin. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

**Düzenler** kaydırıcısını kapatın. **Bütçe planı** belgesi içinde **Çalışma sayfası** üzerine tıklayarak belgeyi Excel'de görüntüleyin ve düzenleyin. Ayarlanabilir Excel şablonu, bu bütçe planı çalışma sayfasını oluşturmak için kullanıldı ve hesaplanmış sütunlar önceki adımlarda tanımlanan formüller kullanılarak güncelleştirilir. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Bütçe planı şablonlarını oluşturmak için ipuçları ve püf noktalar
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Bir bütçe planı şablonu için ek veri kaynakları ekleyebilir ve kullanabilir miyim?

Evet, **Tasarım** menüsünü, Excel şablonundaki aynı ya da diğer sayfalara ek varlıklar eklemek için kullanabilirsiniz. Örneğin, **BudgetPlanProposedProject** veri kaynağını, Excel içindeki bir bütçe planı verisi üzerinde çalışırken aynı zamanda önerilen projelerin bir listesini oluşturmak ve tutmak için ekleyebilirsiniz. Yüksek hacimli veri kaynakları dahil etmenin, Excel çalışma kitabının performansını etkileyebileceğini unutmayın. 

**Veri Bağlayıcısı** içerisindeki **Filtre** seçeneğini, istediğiniz filtreleri ek veri kaynaklarına bağlamak için kullanabilirsiniz.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Diğer kullanıcılar için Veri bağlayıcısı içindeki Tasarım seçeneğini gizleyebilir miyim?

Evet **Veri Bağlayıcısı** seçeneğini açarak **Tasarım** seçeneğini diğer kullanıcılardan gizleyin.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

**Veri bağlayıcısı seçeneklerini** genişletin ve **Tasarım etkinleştir** onay kutusunu temizleyin. Bu, **Tasarım** seçeneğini **Veri bağlayıcısından** gizleyecektir.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Kullanıcıların verilerle çalışırken veri bağlayıcısını yanlışlıkla kapatmalarını engelleyebilir miyim?

Kullanıcıların onu kapatmasını engellemek için şablonu kilitlemeyi öneririz. Kilidi açmak için **Veri bağlayıcısı** üzerine tıklayın, sağ üst köşede bir ok belirir. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Ek bir menü için oku tıklatın. **Kilidi** seçin.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Bütçe planı şablonlarımla hücre biçimlendirme, koşullu biçimlendirme ve grafikler gibi diğer Excel özelliklerini kullanabilir miyim?

Evet, Excel yeteneklerinden çoğu bütçe planı şablonlarında çalışacaktır. Salt okunur ve düzenlenebilir sütunlar arasında ayrım yapmak için renk kodlaması kullanmanızı öneririz. Koşullu biçimlendirme, bütçenin sorunlu alanlarını vurgulamak için kullanılabilir. Standart Excel formüllerini tablo üzerinde kullanarak sütun toplamları kolaylıkla sunulabilir.

Bütçe verisinin ek gruplama ve görselleştirmeleri için özet tabloları ve grafikleri oluşturabilir ve kullanabilirsiniz. **Veri** sekmesinde, **Bağlantılar** grubunda, **Tümünü Yenile** üzerine tıklayın ve daha sonra **Bağlantı Özellikleri** üzerine tıklayın. **Kullanım** sekmesini tıklatın. **Yenile** altında, **Dosya açarken veriyi yenile** onay kutusuna seçin. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)



