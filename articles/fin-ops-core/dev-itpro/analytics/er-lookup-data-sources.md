---
title: ER uygulamasına özgü parametreleri kullanmak için Arama veri kaynaklarını yapılandırma
description: Bu makalede, Elektronik raporlama (ER) biçimlerindeki Arama veri kaynaklarını ER uygulamasına özgü parametreleri kullanacak şekilde nasıl yapılandıracağınız açıklanmaktadır.
author: NickSelin
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 193f185e0b7a7183f98bf9aff3fd3e1c4589fb58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892551"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>ER uygulamasına özgü parametreleri kullanmak için Arama veri kaynaklarını yapılandırma 

[!include[banner](../includes/banner.md)]

[Elektronik raporlama (ER)](general-electronic-reporting.md) uygulamasına özgü parametreler özelliği, veri filtrelemelerini bir dizi soyut kurala göre ER biçiminde yapılandırmanıza olanak tanır. Bu kurallar kümesi, bir ER biçiminde mevcut olan **Arama** türündeki veri kaynaklarını kullanmak için yapılandırılabilir. Daha sonra, karşılık gelen ER biçiminin **Arama** veri kaynağı ayarlarına ve geçerli tüzel kişilik verilerine dayanılarak otomatik olarak oluşturulan kullanıcı arabirimini (UI) kullanarak ER bileşenleri tasarımcılarının ötesinde gerçek kurallar belirleyebilirsiniz. Sonuç olarak, bu ER biçimi yürütüldüğünde, belirtilen kurallara, ER biçiminin **Arama** veri kaynağı tarafından erişilir.

> [!NOTE]
> Gerçek kuralları yapılandırmak için hangi uygulama verilerinin kullanılacağını belirtmek için düzenlenebilir ER biçiminin yapılandırılmış veri kaynaklarını kullanın.

ER biçiminize **Arama** türünde veri kaynağı getirmek için [ER İşlemleri tasarımcısını](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) kullanın. Veri kaynağı, aşağıdakileri içerecek ve soyut kurallarınızın nasıl göründüğünü açıklayacak şekilde yapılandırılmalıdır:

   - Değeri tek bir kural belirtmek için sağlanan belirli bir veri türünün parametre kümesi.
   - Kural diğerleri arasında en uygun olarak kabul edildiğinde tek bir kural tarafından döndürülen belirli veri türünün değer türü.

Yapılandırılmış herhangi bir kural tarafından döndürülen değerin türüne bağlı olarak aşağıdaki **Arama** veri kaynağı türlerini yapılandırabilirsiniz:

   - Model numaralandırma değeri döndürülmesi gerektiğinde **Veri modeli\Arama** türünü kullanın.
   - Bir uygulama numaralandırma değeri veya bir uygulama [genişletilmiş veri türü](../extensibility/extensible-edts.md) değeri döndürülmesi gerektiğinde **Dynamics 365 Operations\Arama** türünü kullanın.
   - Biçim numaralandırma değeri döndürülmesi gerektiğinde **Biçim numaralandırması\Arama** türünü kullanın.

Aşağıdaki şekilde, bir biçim numaralandırmasının örnek ER biçiminde nasıl yapılandırılabileceği gösterilmektedir.

   ![Yapılandırılan arama veri kaynağı için temel olarak bir biçim numaralandırması gösterme.](./media/er-lookup-data-sources-img1.gif)

Aşağıdaki şekil, oluşturulmuş bir raporun farklı bir bölümünde farklı türde vergiler bildirmek için yapılandırılan biçim bileşenlerini gösterir.

   ![Farklı vergi türlerini ayrı olarak raporlamak için kullanılan biçim bölümleri gösterme.](./media/er-lookup-data-sources-img2.png)

Aşağıdaki şekil, ER İşlemleri tasarımcısının **Biçim numaralandırması\Arama** türündeki veri kaynağının eklenmesine nasıl olanak tanıdığını gösterir.  Eklenen veri kaynağı, `List of taxation levels` biçim numaralandırmasının döndürülen değeri olarak yapılandırılır.

   ![Biçim numaralandırması\Arama türünde bir ER veri kaynağı ekleme.](./media/er-lookup-data-sources-img3.gif)

Aşağıdaki şekil, eklenen veri kaynağının **Model** veri kaynağının **Model.Data.Tax** kayıt listesinin **Kod** alanını her yapılandırılan kuralda belirtilmesi gereken bir parametre olarak kullanmak üzere nasıl yapılandırıldığını göstermektedir.

![Biçim numaralandırması\Arama türündeki eklenen veri kaynağının parametrelerini yapılandırma.](./media/er-lookup-data-sources-img4.gif)

Eklenen `Model.Data.Tax` veri kaynağı, **TaxTable** uygulama tablosunun kayıtlarına erişerek, yapılandırılan her kural için bir vergi kodu belirtmek üzere yapılandırılmıştır.

   ![Biçim numaralandırması\Arama türündeki tek şirket arama veri kaynağını gözden geçirme.](./media/er-lookup-data-sources-img5.gif)

Seçilen ER biçiminin arama kurallarını, yapılandırılan veri kaynağının yapısı ile otomatik olarak uyumlu hale gelen kullanıcı arabirimini kullanarak ayarlayabilirsiniz. Şu anda, bu kullanıcı arabirimi her kural için döndürülen değeri `List of taxation levels` biçim numaralandırma değeri ve parametre olarak da vergi kodu belirtmenizi gerektirir.

   ![Yapılandırılan veri kaynağı için kuralları ayarlama.](./media/er-lookup-data-sources-img6.gif)

Aşağıdaki şekil, **Hesaplanan alan** türündeki `Model.Data.Summary.LevelByLookup` veri kaynağının gerekli parametreleri sağlayan yapılandırılmış **Arama** veri kaynağını çağırmak üzere nasıl yapılandırılabileceği gösterilmiştir. Bu çağrıyı çalışma zamanında işlemek için ER, sağlanan koşulları sağlayan ilk kuralı bulmak üzere tanımlanan dizideki yapılandırılan kurallar listesinden geçer. Bu örnekte, sağlanan vergi koduyla eşleşen kodu içeren kural verilmektedir. Sonuç olarak, en uygun kural bulunur ve bulunan kural için yapılandırılan numaralandırma değeri bu veri kaynağı tarafından döndürülür.

> [!NOTE]
> Uygulanabilir bir kural bulunamazsa özel durum oluşur. Bu özel durumların oluşmasını önlemek için, yapılandırılmamış bir değer olduğunda veya değer olmadığında durumları işlemek üzere kurallar listesinin sonunda ek kurallar oluşturun. **\*Boş değil**\* ve **\*Boş**\* seçeneklerini uygun şekilde kullanın.  
>
> ![Yapılandırılan Arama veri kaynağını çağırmak için bir veri kaynağı ekleme.](./media/er-lookup-data-sources-img7.png)

Düzenlenebilir arama veri kaynağı için **Şirketler arası** seçeneğini **Evet** olarak ayarlarken bu veri kaynağının parametre kümesine yeni bir gerekli **Şirket** parametresi eklersiniz. Arama veri kaynağı çağrıldığında, çalıştırma zamanında **Şirket** parametresinin değeri belirtilmelidir. Şirket kodu çalıştırma zamanında belirtildiğinde, bu şirket için yapılandırılan kurallar en uygun kuralı bulmak için kullanılır ve ilgili değer döndürülür. Aşağıdaki şekilde bunu nasıl yapabileceğiniz ve düzenlenebilir veri kaynağının parametre kümesinin nasıl değiştirileceği gösterilmektedir.

   ![Biçim numaralandırması\Arama türündeki şirketler arası arama veri kaynağını gözden geçirme.](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> Düzenlenebilir ER biçiminin bu arama veri kaynağı için kural kümesini yapılandırmak üzere her şirketi ayrı olarak seçin. Şirketler arası arama, arama ayarının tamamlanmadığı şirketin koduyla çağrıldığında, çalışma zamanında bir özel durum oluşur.
>
> Bu veri kaynağının kapsamındaki her şirketin verilerine erişmek için, ER biçimini şirketler arası **Arama** veri kaynağıyla çalıştıran kullanıcıya izin verdiğinizden emin olun. Aksi durumda, çalışma zamanında özel durum oluşturulur.

Sürüm 10.0.19'dan başlayarak, **Arama** veri kaynaklarının genişletilmiş özellikleri kullanılabilir. Düzenlenebilir arama veri kaynağı için **Genişletilmiş** seçeneğini **Evet** olarak ayarladığınızda, yapılandırılan arama veri kaynağı yapılandırılmış kurallar kümesini çözümlemek için ek yetenekler sunan yapılandırılmış veri kaynağına dönüştürülür. Aşağıdaki şekilde bu dönüşüm gösterilmiştir.

   ![Biçim numaralandırması\Arama türündeki yapılandırılmış arama veri kaynağını gözden geçirme.](./media/er-lookup-data-sources-img9.gif)

- **Arama** alt öğesi, sağlanan parametreler kümesini temel alan yapılandırılabilir kurallar kümesinden en uygun kuralı bulmak için bir işlev olarak tasarlanmıştır.
- **IsLookupResultSet** alt öğesi, temel numaralandırma veri kaynağının sağlanan değerini kabul eden bir işlev olarak tasarlanmıştır ve kural kümesi sağlanan numaralandırma değerinin döndürülen değer olarak yapılandırıldığı en az bir kural içerdiğinde **True** *Boole* değerini döndürür. Sağlanan numaralandırma değerini döndürmek üzere yapılandırılmış kural olmadığında bu işlev **False** *Boole* değerini döndürür.
- **Ayar** alt öğesi, bir kayıt listesinin kayıtları olarak yapılandırılan kurallar kümesini döndüren bir işlev olarak tasarlanmıştır. Döndürülen değerler ve yapılandırılan kuralların parametre kümesi, her döndürülen kayıtta ilgili veri türlerindeki alanlar olarak sunulur:

    - Döndürülen değer **Arama sonucu** alanı olarak sunulur.
    - Yapılandırılan parametreler, parametrelerin adlarına sahip alanlar (bu örnekte **Kod** alanı) olarak sunulur.

**Arama** veri kaynağını yapılandırma hakkında daha fazla bilgi için bkz. [Tüzel kişi başına belirtilen parametreleri kullanmak üzere ER biçimlerini yapılandırma](er-app-specific-parameters-configure-format.md). Arama kurallarının nasıl ayarlanacağını öğrenmek için bkz. [Tüzel kişilik için ER biçiminin parametrelerini ayarlama](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Ek kaynaklar

[ER biçimlerini her tüzel kişilik için belirtilen parametreleri kullanmak üzere yapılandırma](er-app-specific-parameters-configure-format.md)

[Her tüzel kişilik için ER biçiminin parametrelerini ayarlama](er-app-specific-parameters-set-up.md)
