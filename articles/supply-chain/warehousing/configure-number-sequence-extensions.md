---
title: Ambar akışları için numara serilerini yapılandırma
description: Bu konu plaka kodları, dalga etiketi kodları, konteyner kodları ve konşimento kodları için numara serisi uzantıları sağlayan işlevlere genel bir bakış sağlar.
author: GarmMSFT
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSNumberSequenceExt
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: e9ba06908b9e82763557e98715e495cfaf649753
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574725"
---
# <a name="configure-number-sequences-for-warehouse-flows"></a>Ambar akışları için numara serilerini yapılandırma

[!include [banner](../includes/banner.md)]

*Numara serisi uzantıları* özelliği numara serilerini ayarlamak için yeni bir yapılandırma sayfası ekler. GS1 önekleri ve denetim basamakları (modül 10) dahil GS1-düzenlenmiş kimlikleri için esnek yapılandırmaya olanak tanır ve varolan numara serilerinde uzunluk sınırını zorunlu kılar.

Denetim hanesi hesaplanmadığından ve şirketin GS1 önekinin el ile güncelleştirilmesi gerektiğinden, standart numara serisi segmentleri GS1 uygulaması için uygun değildir.

Bu özellik aşağıdaki işlevleri ekler:

- Konşimento (BOL) kodları önceden oluşturulabilir.
- Seri sevkiyat konteyner kodu (SSCC) numaraları için benzersiz bir numara serisi oluşturulabilir.
- BOL ve SSCC numaraları için GS1 uyumlu numara serileri oluşturulabilir. Özellik plaka kodları, konteyner kodları, dalga etiketi kodları ve BOL kodları için kullanıma hazır destek ekler.
- Plaka kodu numaralarının yapılandırması esnektir. Örneğin, baştaki sıfırlar (00) gibi, uygulama tanımlayıcıları (AI) dahil edebilir veya hariç tutabilirsiniz.

Bu işlev, kolilerin etiketlenmesini desteklemeyi ve sistem tarafından oluşturulan yeni numaraları düzenlemeyi daha etkili bir hale getirir.

## <a name="turn-on-the-number-sequence-extensions-feature"></a>Numara serisi uzantıları özelliğini açma

Özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Numara serisi uzantıları*

## <a name="set-up-the-feature"></a>Özelliği ayarlama

Sisteminizde numara serisi uzantıları ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
1. **Genel** sekmesinde, **GS1 şirket öneki** alanına şirketinizin GS1 önekini girin. Bu değer, GS1 önekinin bir segment olarak dahil edildiği tüm numara serilerini etkileyecektir.
1. Dalga etiketleri için BOL numaraları oluşturmak istiyorsanız **Raporlar** sekmesinde **Dalga etiketleri yazdırılırken BOL numarası oluştur** onay kutusunu seçin.

    > [!NOTE]
    > Bu onay kutusu yalnızca [dalga etiketi yazdırma işlevi ](configure-wave-label-printing.md) etkinse kullanılabilir.

1. **Ambar yönetimi** \> **Kurulum** \> **Numarası serisi uzantıları**'na gidin
1. Eylem Bölmesinde **Varsayılan ayar oluştur**'u seçin. GS1 uyumlu bir BOL numarası serisi ve üç tür SSCC numara serisi oluşturulur. Tüm bu numara serileri şirketinizin GS1 önekinin uzunluğu dikkate alır.

    Bu varsayılan numara serilerini özelleştirme ve/veya yeni seriler ekleme hakkında daha fazla bilgi için, sonraki bölüme bakın. Ayrıca, ihtiyacınız yoksa bu dizilerinden herhangi birini kaldırabilirsiniz.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne geri dönün.
1. **Numara serileri** sekmesinde, plaka kodlarınız, dalga etiketi kodlarınız, konteyner kodlarınız (bu durumda, uygun **SSCC-18 numara** serisini seçin) ve/veya BOL kodlarınız (bu durumda, **BOL** serisini seçin) için numaralar oluşturmak üzere ilgili numara serisi uzantısını seçin. Varsayılan olarak, numara serisi uzantıları yalnızca bu dört kimlik türü için desteklenir.

Bu numara serilerinden biri için daha sonra yeni bir numara oluşturulduğunda, yeni mantık kullanılacaktır.

> [!NOTE]
> Plaka kimlikleri için bir numara serisi uzantısı seçmezseniz, plaka kodları oluşturmak için geçerli kurallar kullanılacaktır. Aksi takdirde, seçtiğiniz numara seriniz kullanılır. Diğer kodlar, onlar için bir numara serisi uzantısı uygulanıncaya kadar düz numara serisini kullanır.

## <a name="create-and-edit-number-sequences"></a>Numara serileri oluşturma ve düzenleme

Önceki bölümde, varsayılan numara serisi kümesi oluşturdunuz. Bu bölümde, her numara serisinin nasıl tanımlandığı açıklanmaktadır. Ayrıca, özel serilerin nasıl oluşturulacağı ve varsayılan veya özel serilerin nasıl düzenleneceği de açıklanmıştır.

Numara serileri oluşturmak ve düzenlemek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi** \> **Kurulum** \> **Numarası serisi uzantıları**'na gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Numara serisi uzantısı** alanında, yeni seri için bir ad girin. **Açıklama** alanına bir açıklama girin.
1. **Segmentler** hızlı sekmesinde segment ekleyerek, silerek ve düzenleyerek numaralandırma biçiminizi birleştirmek için araç çubuğundaki düğmeleri kullanın. Her satırın **Segment** alanında, o segmentin amacını ve içeriğini tanımlamak için bir segment türü atayın. Aşağıdaki tabloda, kullanılabilecek segment türleri açıklanmıştır.

    | Segment türü | Tanım |
    |---|---|
    | Sabit | Bu segment türü, serideki her oluşturulan numara için aynı sabit metni ekler. **Değer** alanında, gerekli metni girin. **Uzunluk** alanı otomatik olarak **Değer** alanına girdiğiniz metnin uzunluğuna güncelleştirilir. |
    | Numara serisi | **Değer** alanına, oluşturulan seride gösterilmesi gereken her karakter için bir sayı işareti (*\#*) girin. Numara serisinin kendisi daha uzun numaralar oluşturabilir ancak yalnızca en sağdaki karakterler gösterilecektir. **Uzunluk** alanı otomatik olarak **Değer** alanına girdiğiniz sayı işareti sayısına güncelleştirilir.<p>SSCC-18 numaraları için GS1 gereksinimlere uymak amacıyla bu segmentin uzunluğunun GS1 öneki uzunluğundan 16 eksik olduğundan emin olun.</p> |
    | GS1 öneki | Bu segment türü **Ambar yönetimi parametreleri** sayfasının **GS1 şirket öneki** alanında ayarlanan değeri ekler. **Değer** alanı, **Ambar yönetimi parametreleri sayfasında** ayarlanan değeri gösterir ve **Uzunluk** alanında değerin kaç karakter olduğu gösterilir. Hem **Değer** hem de **Uzunluk** alanı salt okunurdur. |
    | Uygulama tanımlayıcısı | **Değer** alanına, bu numara serisi türü içim ilgili GS1 ilkesinde belirtildiği şekilde bir uygulama tanımlayıcısı girin. Örneğin, SSCC için *00* veya BOL için *420* girin. **Uzunluk** alanı otomatik olarak **Değer** alanına girdiğiniz tanımlayıcının uzunluğuna güncelleştirilir. |
    | Sevk türü | Açıkça tanımlanlabilecek maddeler için bu segment türü, ilgili birim seri grubundan (**Birim seri grupları** sayfasından) bir alan değeri ekler. (Bu davranış, plaka kodları için varolan mantığı eşleştirir.) Çoklu stok tutma birimleri (STB) içeren plakalar için bu segment türü varsayılan olarak *0* (sıfır) değerini ekler. Bu segment türü için, **Değer** alanı her zaman *P* olarak ayarlanır ve **Uzunluk** alanı her zaman *1* olarak ayarlanır.|
    | Denetleme basamağı | Bu segment türü, modül 10 hesaplaması olan bir denetleme basamağı ekler. (Bu davranış, plaka kodları için varolan mantığı eşleştirir.) Bu segment türü için **Değer** alanı her zaman bir şapka işareti (*^*) olarak ayarlanır ve **Uzunluk** alanı her zaman *1* olarak ayarlanır. |

1. Nihai numara biçiminizin bir örneğini görüntülemek için, **Segmentler** hızlı sekmesinin alt kısmındaki **Biçim** alanını inceleyin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]