---
title: Word biçiminde raporlar oluşturmak için yeni bir ER yapılandırması tasarlama
description: Bu makalede, kullanıcıların Microsoft Word belgeleri olarak rapor oluşturmak için yeni bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceği açıklanmaktadır.
author: kfend
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.search.form:
- ERWorkspace, ERSolutionTable, EROperationDesigner
- LedgerJournalTable, LedgerJournalTransVendPaym
ms.openlocfilehash: b56b328aa2a2b53dc177a02a4d453e5dbcb8340c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273353"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>Word biçiminde raporlar oluşturmak için yeni bir ER yapılandırması tasarlama

[!include [banner](../includes/banner.md)]

Microsoft Word belgeleri olarak rapor oluşturmak için Word masaüstü uygulaması gibi bir uygulama kullanarak raporlar için bir şablon tasarlamanız gerekir. Aşağıdaki çizimde, işlenmiş satıcı ödemelerinin ayrıntılarını göstermek için oluşturulabilen denetim raporu için örnek bir şablon gösterilmektedir.

![Word masaüstü uygulamasındaki denetim raporu için örnek şablon.](./media/er-design-configuration-word-image1.png)

Word biçimindeki raporlar için şablon olarak Word belgesi kullanmak için yeni bir [Elektronik raporlama (ER)](general-electronic-reporting.md) [çözümü](er-quick-start1-new-solution.md) yapılandırabilirsiniz. Bu çözüm, ER biçimi bileşeni içeren bir ER [yapılandırması](general-electronic-reporting.md#Configuration) içermelidir.

> [!NOTE]
> Word biçiminde raporlar oluşturmak için yeni bir ER biçimi yapılandırması oluşturduğunuzda **Yapılandırma oluştur** açılır iletişim kutusunda biçim türü olarak **Word** seçeneğini belirlemeniz ve **Biçim türü** alanını boş bırakmanız gerekir.

![Yapılandırmalar sayfasında özel biçim yapılandırması oluşturma.](./media/er-design-configuration-word-image2.gif)

Çözümün ER biçimi bileşeni, **Excel\\File** biçim öğesini içermeli ve söz konusu biçim öğesi çalıştırma zamanında oluşturulan raporlar için şablon olarak kullanılacak Word belgesine bağlanmalıdır. ER biçim bileşenini yapılandırmak için ER biçim tasarımcısında oluşturulan ER yapılandırmasının taslak sürümünü açmanız gerekir. Ardından **Excel\\File** öğesini ekleyin, Word şablonunuzu düzenlenebilir ER biçimine ekleyin ve söz konusu şablonu eklediğiniz **Excel\\File** öğesine bağlayın.

> [!NOTE]
> Şablonu eklediğinizde, ER biçimleri şablonlarını depolamak için ER parametrelerinde daha önce [yapılandırılmış](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) olan [belge türünü](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) kullanmanız gerekir.

![Biçim tasarımcısı sayfasına şablon ekleme.](./media/er-design-configuration-word-image3.gif)

Çalıştırma zamanında oluşturulan raporlara girilecek verilerin yapısını belirtmek için **Excel\\File** öğesine **Excel\\Range** ve **Excel\\Cell** iç içe öğelerini ekleyebilirsiniz. Ardından, çalıştırma zamanında oluşturulan raporlara girilecek asıl verileri belirtmek için bu öğeleri düzenlenebilir ER biçiminin veri kaynaklarına bağlamanız gerekir.

![Biçim tasarımcısı sayfasına iç içe öğeler ekleme.](./media/er-design-configuration-word-image4.gif)

Tasarım aşamasında değişikliklerini ER biçimine kaydettiğinizde hiyerarşik biçim yapısı, ekli Word şablonunda **Rapor** adlı [özel XML bölümü](/visualstudio/vsto/custom-xml-parts-overview) olarak saklanır. Değiştirilen şablona erişmeniz, Finance'ten indirmeniz, yerel olarak depolamanız ve Word masaüstü uygulamasında açmanız gerekir. Aşağıdaki çizimde, **Rapor** özel XML bölümünü içeren denetim raporu için yerel olarak depolanan örnek şablon gösterilmektedir.

![Word masaüstü uygulamasında örnek rapor şablonunun önizlemesini görüntüleme.](./media/er-design-configuration-word-image5.gif)

**Excel\\Range** ve **Excel\\Cell** bağlamaları çalıştırma zamanında çalıştırıldığında, söz konusu bağlamanın sunduğu veriler, oluşturulan Word belgesine **Rapor** özel XML bölümünün ayrı bir alanı olarak gelir. Özel XML bölümünün alanlarındaki değerleri oluşturulmuş bir belgeye girmek için, Word şablonunuza uygun Word [içerik denetimlerini](/office/client-developer/word/content-controls-in-word) eklemeniz gerekir ve bunlar çalışma zamanında doldurulacak veriler için yer tutucu görevi görür. İçerik denetimlerinin nasıl doldurulacağını belirtmek içinc her içerik denetimini **Rapor** özel XML bölümünün uygun alanıyla eşleştirin.

![Word masaüstü uygulamasında içerik denetimleri ekleme ve eşleme.](./media/er-design-configuration-word-image6.gif)

Ardından, düzenlenebilir ER biçiminin özgün Word şablonunu **Rapor** özel XML bölümünün alanlarıyla eşleştirilen Word içerik denetimlerini içeren değiştirilmiş şablonla değiştirmeniz gerekir.

![Biçim tasarımcısı sayfasındaki şablonu değiştirme.](./media/er-design-configuration-word-image7.gif)

Yapılandırılmış ER biçimini çalıştırdığınızda, ekli Word şablonu yeni bir rapor oluşturmak için kullanılır. Asıl veriler, Word raporunda **Rapor** adlı özel XML bölümü olarak depolanır. Oluşturulan rapor açıldığında, Word içerik denetimleri **Rapor** özel XML bölümünden alınan verilerle doldurulur.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

**Soru:** Şirket adresi içeren bir Word belgesini yazdırmak için bir ER biçimi yapılandırdım. Bu ER biçiminin Word şablonunda, şirket adresini göstermek için zengin metin içerik denetimi ekledim. Finance'te, şirket adresini çok satırlı metin olarak girdim ve girdiğim her satır için satır başı eklemek üzere **Gir**'i seçtim. Bu nedenle, şirket adresinin oluşturulan belgelerde çok satırlı metin olarak görünmesini bekliyorum. Ancak adres, satır başı yerine özel semboller içeren tek satırlık bir metin olarak görünüyor. Ayarlarımdaki sorun nedir?

**Yanıt:** Zengin metin içerik denetimi kullanmak yerine, düz metin içerik denetimini kullanmanız ve denetim özelliklerinde **Satır başlarına izin ver (birden fazla paragraf)** onay kutusunu seçin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Word biçiminde raporlar oluşturmak için Excel şablonlarıyla ER yapılandırmalarını yeniden kullanma](./tasks/er-design-configuration-word-2016-11.md)
- [Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
