---
title: Üretim yapılarını serbest bırakma
description: Bu konu, ürünleri mühendislik sürümleriyle birlikte serbest bırakmanın yanı sıra tüm ürün yapılarını nasıl serbest bırakabileceğinizi açıklar. Bu şekilde, mühendislikle ilgili ürün verilerinin farklı tüzel kişiliklerde kolayca yeniden kullanılabilmesini sağlayabilirsiniz.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 68f091cca9c3c2baa03813553127ee41abe6d522
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/29/2020
ms.locfileid: "4439753"
---
# <a name="release-product-structures"></a>Üretim yapılarını serbest bırakma

[!include [banner](../includes/banner.md)]

Mühendislikle ilgili ürün verilerinin farklı tüzel kişilerde kolayca yeniden kullanılabilmesini sağlamak için ürünleri mühendislik sürümleriyle birlikte serbest bırakmanın yanı sıra tüm ürün yapılarını da serbest bırakabilirsiniz. Bu nedenle, tek bir serbest bırakma eyleminde üst öğe ile birlikte çok düzeyli ürün reçetesi yapılarını serbest bırakabilirsiniz. Bu durumda, ürün reçetesi ve alt düzey ürünler de serbest bırakılır.

Mühendislik ürünleri, mühendislik şirketleri tarafından, tasarlanırken kalite gereksinimlerini karşılayacak şekilde oluşturulur ve bakımları yapılır. Bir ürün üreten her operasyonel şirket aynı ürün ve temel ürün reçetesine ihtiyaç duyar. Üretim tesisine bağlı olarak rota yerel olarak oluşturulabilir. Bu durumda, ürünle birlikte bir rotayı serbest bırakamazsınız. Ürünleri üretmeyen ancak satan tüzel kişilikler için, ürün reçetesi gerekli olmayabilir.

İşlemi daha verimli hale getirmek için mühendislikle ilgili tüm veriler aynı anda diğer operasyonel şirketlere de yayınlanabilir. Bu veriler ürün yapısını içerir. Yayınlama işlemi sırasında, ürün verilerinin hangi bölümünün yayınlanması gerektiğini seçebilirsiniz.

Mühendislik şirketleri ve operasyonel şirketler hakkında daha fazla bilgi için [Mühendislik şirketleri ve veri sahipliği kuralları](engineering-org-data-ownership-rules.md)'na bakın.

Hem standart ürünleri hem de mühendislik ürünlerini ürün yapısıyla birlikte serbest bırakabileceğinizi unutmayın. Bu işlem sırasında, tüm ürün yapısıyla birlikte ürünün serbest bırakıldığı şirketten alınan ürün reçetesi ve rota serbest bırakılır.

Bir ürünün nasıl serbest bırakılabildiğini öğrenmek için bkz. [Bir mühendislik ürününü yerel şirkete serbest bırakma](engineering-scenarios.md#release)

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>Ürün yapısını serbest bırakma işlemi kullanıldığında bir ürünün serbest bırakılan verileri

Mühendislik ürünlerinin serbest bırakılmasına aşağıdaki veriler dahildir:

- **Ürün verileri**: Serbest bırakılan yeni bir ürün oluşturulur.
- **Mühendislik sürümü verileri**: Mühendislik sürümü ve verileri oluşturulur veya güncelleştirilir. Aynı mühendislik sürümünü bir operasyonel şirkete tekrar serbest bırakırsanız mühendislik verilerinin üzerine yazılacağını unutmayın.
- **Mühendislik öznitelikleri**: Mühendislik öznitelikleri ve değerleri oluşturulur veya güncelleştirilir.
- **Mühendislik ürün reçetesi**: Mühendislik ürün reçetesi ve satırları oluşturulabilir veya güncelleştirilebilir. Veri sahipliği hakkında daha fazla bilgi için bkz. [Veri sahipleri](product-owner.md).
- **Mühendislik rotaları**: Mühendislik rotaları ve bu rotaların işlemleri oluşturulabilir veya güncelleştirilebilir. Veri sahipliği hakkında daha fazla bilgi için bkz. [Veri sahipleri](product-owner.md).
- **Mühendislik belgeleri**: Mühendislik versiyonuna bağlı mühendislik belgeleri oluşturulur veya güncelleştirilir.

Sisteminizde mühendislik değişikliği yönetimini açtığınızda, ürün yapısını serbest bırakma işlevi kullanılabilir. Buna ek olarak, standart ürünler serbest bırakıldığında ürün ve rotalarını içerecektir.

## <a name="product-acceptance"></a>Ürün kabulü

**Ürün kabulü**, serbest bırakma işlemini etkileyen önemli bir parametredir. **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik değişikliği yönetimi parametreleri**'ne giderek her şirket için bu parametreyi ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Mühendislik değişikliği yönetimi parametreleri](engineering-parameters.md).

### <a name="automatic-product-acceptance"></a>Otomatik ürün kabulü

Mühendislik ürünlerinin her serbest bırakılması, mühendislik şirketinden biri kişi serbest bırakmak üzere bir ürün seçtiğinde başlar. **Ürün kabulü** parametresi, *Otomatik* olarak ayarlandığında, mühendislik şirketindeki kullanıcı hangi ürün verilerinin operasyonel şirketlere otomatik olarak serbest bırakılacağına karar verir. Ürün daha sonra serbest bırakma sihirbazında seçilen şirketlere otomatik olarak serbest bırakılır.

### <a name="manual-product-acceptance"></a>El ile ürün kabulü

Mühendislik ürünlerinin her serbest bırakılması, mühendislik şirketinden biri kişi serbest bırakmak üzere bir ürün seçtiğinde başlar. **Ürün kabulü** parametresi, *El ile* olarak ayarlandığında, mühendislik şirketindeki kullanıcı hangi ürün verilerinin operasyonel şirketlere serbest bırakılacağına karar verir. Her operasyonel şirketten bir kullanıcı, daha sonra ürün verilerini gözden geçirir ve serbest bırakmayı kabul edip etmeyeceğine karar verir. Operasyonel şirketteki kullanıcı, veriler alındığı zaman aşağıdaki seçenekleri ayarlayabilir:

- Ürünler (güncelleştirmeler) operasyonel şirket için alakalı değilse kullanıcı, serbest bırakmayı kabul etmemeyi seçebilir.
- Kullanıcı yeni ürünler için madde şablonunu değiştirebilir.
- Kullanıcı, ürünün ürün reçeteleri ve/veya rotalarıyla birlikte serbest bırakılıp bırakılmayacağını ve onaylı ve etkin olarak serbest bırakılıp bırakılmayacağını seçebilir.
- Kullanıcı ürünlerin geçerlilik tarihlerini değiştirebilir.

Bir ürünün nasıl kabul edildiğiyle ilgili örnek için bkz. [Ürünü yerel şirkette serbest bırakmadan önce inceleme ve kabul etme](engineering-scenarios.md#accept).

> [!NOTE]
> Standart ürünlerde, herhangi bir tüzel kişilikten herhangi başka bir tüzel kişiliğe serbest bırakabilirsiniz. Mühendislik ürünlerinde, serbest bırakabileceğiniz tek tüzel kişilik mühendislik şirketidir.

## <a name="release-policies"></a>Serbest bırakma ilkeleri

Tüm operasyonel şirketler aynı ürün verilerine ihtiyaç duymaz. Genel olarak, mühendislik ürünleri üreten operasyonel şirketler bir ürün reçetesi gerektirirken, sadece mühendislik ürünleri satan operasyonel şirketler ürün reçetesi gerektirmez. Ürünlerin serbest bırakılması için kullanılan parametreleri oluşturmak için serbest bırakma ilkelerini kullanabilirsiniz.

Mühendislik ürünleri için serbest bırakma ilkesi mühendislik ürün kategorisinde atanır ve alan zorunludur. Standart ürünlerde ilke, paylaşılan ürüne atanır ve alan isteğe bağlıdır.

Mühendislik ürünü kategorileri hakkında daha fazla bilgi için bkz. [Mühendislik sürümleri ve mühendislik ürünü kategorileri](engineering-versions-product-category.md).

Serbest bırakma işlemi sırasında ayarları etkileyebilirsiniz.

## <a name="create-and-manage-product-release-policies"></a>Ürün serbest bırakma ilkelerini oluşturma ve yönetme

Ürün serbest bırakma ilkeleriyle çalışmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Ürün serbest bırakma ilkeleri**'ne gidin. Ardından şu adımlardan birini izleyin.

- Yeni ilke oluşturmak için Eylem bölmesinden **Yeni**'yi seçin ve sonra alanları aşağıdaki alt bölümlerde açıklandığı gibi ayarlayın.
- Mevcut ilkeyi düzenlemek için liste bölmesinden ilkeyi seçin ve Eylem bölmesinden **Düzenle**'yi seçin ve sonra alanları aşağıdaki alt kısımlarda açıklandığı gibi ayarlayın.
- Var olan bir ilkeyi silmek için liste bölmesinden seçin, Eylem Bölmesinde **Düzenle**'yi seçin ve ardından **Genel** hızlı sekmesinde **Etkin** seçeneğini *Hayır* olarak ayarlayın. Eylem Bölmesi'nde **Sil**'i seçin.

### <a name="header"></a>Üst bilgi

Ürün serbest bırakma ilkesinin üst bilgisinde aşağıdaki alanları ayarlayın.

| Alan | Tanım |
|---|---|
| Kuruluş adı | İlke için bir ad girin. |
| Tanım | İlke için açıklama girin. |

### <a name="general-fasttab"></a>Genel FastTab

Ürün serbest bırakma ilkesinin **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın.

| Alan | Tanım |
|---|---|
| Ürün türü | İlkenin *Madde* veya *Hizmet* türündeki ürünler için geçerli olup olmadığını seçin. Kaydı kaydettikten sonra bu ayarı değiştiremezseniz. |
| Şablonları uygula | İlke kullanıldığında ürün serbest bırakma şablonlarının uygulanıp uygulanmayacağını ve nasıl uygulanacağını belirtmek için aşağıdaki seçeneklerden birini belirleyin:<ul><li>**Her zaman**: Serbest bırakılan ürüne yönelik bir şablon her zaman kullanılmalıdır. Bu seçeneği belirlerseniz serbest bırakma işlemi yaptığınız her şirket için kullanılan şablonu belirtmek üzere **Tüm ürünler** hızlı sekmesini kullanın. **Tüm ürünler** hızlı sekmesinde listelenen her şirket için bir şablon belirtmezseniz ilkeyi kaydetmeye çalıştığınızda bir hata alırsınız.</li><li>**İsteğe bağlı**: **Tüm ürünler** hızlı sekmesinde listelenen bir şirket için serbest bırakılan bir şablon belirtilirse, bu şablon o şirkete serbest bırakma işlemi uyguladığınızda kullanılır. Aksi takdirde hiçbir şablon kullanılmaz. Bu seçeneği belirlerseniz, tüm şirketlere şablon atamadan ilkeyi kaydedebilirsiniz. (Hiçbir uyarı gösterilmez.)</li><li>**Hiçbir zaman**: **Tüm ürünler** hızlı sekmesinde listelenen şirketler için bir şablon belirtilse bile, serbest bırakma işlemi yaptığınız şirketler için hiçbir serbest bırakılan şablon kullanılmaz. Şablon sütunları kullanılamaz.</li></ul> |
| Active | Serbest bırakma ilkelerinizin korunmasına yardımcı olmak için bu seçeneği kullanın. Bunu, kullandığınız tüm serbest bırakma ilkeleri için *Evet* olarak ayarlayın. Kullanılmadığında etkin olmayan bir serbest bırakma ilkesini işaretlemek için *Hayır* olarak ayarlayın. Mühendislik ürünü kategorisine atanan bir serbest bırakma ilkesini devre dışı bırakamayacağınızı ve yalnızca etkin olmayan serbest bırakma ilkelerini silebileceğinizi unutmayın. |

### <a name="all-products-fasttab"></a>Tüm ürünler hızlı sekmesi

**Tüm ürünler** hızlı sekmesinde, bu ilkeyi kullanarak serbest bırakma işlemi yapmak istediğiniz her operasyonel şirket için bir satır ekleyin. İhtiyacınız olan satırları eklemek ve kaldırmak için **Tüm ürünler** hızlı sekmesindeki düğmeleri kullanın. Eklediğiniz her satır için aşağıdaki alanları ayarlayın.

> [!NOTE]
> **Tüm ürünler** hızlı sekmesindeki ayarlar hem mühendislik ürünleri hem de standart ürünler için geçerlidir.

| Alan | Tanım |
|---|---|
| Şirket hesapları kodu | Satırın geçerli olduğu şirketi seçin. Ürünler bu şirkete serbest bırakıldığında satırdaki parametreler geçerli olacaktır. |
| Şablon serbest bırakılan ürün | Ürün için bir şablon ekleyin. |
| Ürün reçetesi onayını kopyala | Ürün reçetesi onay durumunu alıcı şirkete kopyalamak için bu onay kutusunu seçin. |
| Ürün reçetesi etkinleştirmesini kopyala | Ürün reçetesi etkinleştirme durumunu alıcı şirkete kopyalamak için bu onay kutusunu seçin. |
| Rota onayını kopyala | Rota onay durumunu alıcı şirkete kopyalamak için bu onay kutusunu seçin.|
| Rota etkinleştirmesini kopyala | Rota etkinleştirme durumunu alıcı şirkete kopyalamak için bu onay kutusunu seçin. |

### <a name="option-parameters-for-engineering-products-fasttab"></a>Mühendislik ürünleri için seçenek parametreleri hızlı sekmesi

**Tüm ürünler** hızlı sekmesinde her satır eklediğinizde, **Şirket hesapları kimliği** değeri ile eşleşen bir satır da **Mühendislik ürünleri için seçenek parametreleri** hızlı sekmesinde oluşturulur. Daha sonra, **Tüm ürünler** hızlı sekmesinden bir satır kaldırırsanız eşleşen **Şirket hesapları kimliği** değerine sahip satır da **Mühendislik ürünleri için seçenek parametreleri** hızlı sekmesinden kaldırılır.

**Mühendislik ürünleri için seçenek parametreleri**'nde gösterilen her satır için aşağıdaki alanları ayarlayın.

> [!NOTE]
> **Mühendislik ürünleri için seçenek parametreleri** hızlı sekmesindeki ayarlar yalnızca mühendislik ürünleri için geçerlidir.

| Alan | Tanım |
|---|---|
| Şablon Ürün Reçetesi | Ürün reçetesi olan bir ürün serbest bırakıldığında, belirtilen şablon ürün reçetesinin satırları eklenir. Bu alan, yerel dilde paketleme veya yönergeler gibi yerel bileşenler eklemek için yararlıdır. |
| Şablon rota | Rotası olan bir ürün serbest bırakıldığında, belirtilen şablonun satırları eklenir. |
| Geçerliliği kopyalama | Ürünleri serbest bıraktığınızda geçerlilik tarihlerinin mühendislik şirketinden operasyonel şirkete kopyalanıp kopyalanmayacağını seçin. |
| Serbest bırakma teklifine otomatik olarak ekle | Mühendislik değişikliği emrine göre otomatik olarak serbest bırakılması gereken ürünler için bu onay kutusunu seçin. Bu şekilde, bu serbest bırakma ilkesini kullanan mühendislik ürünü kategorilerine ait ürünler, bu seçeneğin ayarlandığı operasyonel şirketlere otomatik olarak serbest bırakılabilir. (Daha fazla bilgi için bkz. [Mühendislik ürünlerindeki değişiklikleri yönetme](engineering-change-management.md).)

### <a name="review-each-product-when-you-release-it"></a>Her ürünü serbest bıraktığınızda inceleme

Ürün reçeceleri veya rotaları olan mühendislik ürünleri serbest bırakıldığında, parametreler serbest bırakma ilkesinde belirtildiği gibi varsayılan değerlere ayarlanır. Bir kullanıcı olarak, ürün yapısını serbest bırakma işlemini kullandığınızda serbest bırakan tarafta bu davranışı etkileyebilirsiniz.

Mühendislik ürünlerini serbest bırakmak için **Serbest bırakılan ürünler** sayfasında, serbest bırakılacak ürünleri seçin ve serbest bırakma sihirbazını açarak **Ürün yapısını serbest bırak**'ı seçin. **Serbest bırakılacak mühendislik ürünlerini seçin** sayfasında ürünler gösterilir. Tek bir ürün seçin ve ardından ürünün serbest bırakma ayrıntılarını incelemek için **Serbest bırakma ayrıntıları**'nı seçin.

**Serbest bırakma ayrıntıları** sayfasında, **Ürün reçetesini teslim al**, **Ürün reçetesi onayını kopyala**, **Ürün reçetesi etkinleştirmeyi kopyala**, **Ürün reçetesini teslim al**, **Rota onayını kopyala** ve **Rota etkinleştirmeyi kopyala** alanlarının değerini değiştirebilirsiniz. Push-pull senaryosunda, ürün reçetesi ve rota serbest bırakılırsa alıcı taraftaki aynı alanların değerini değiştirebilirsiniz.

## <a name="product-owners-and-product-releases"></a>Ürün sahipleri ve ürün serbest bırakmaları

Ürün sahipleri hangi tüzel kişiliklerin ürünlerine ihtiyaç duyduğunu bildikleri için bir ürün yalnızca ürünün ürün sahibi grubunun üyeleri tarafından serbest bırakılabilir. Diğer kullanıcılar sahip olmadıkları ürünleri serbest bırakamaz.

Bu davranış, yalnızca bir ürün doğrudan serbest bırakılması için seçildiğinde geçerlidir. Bir ürün reçetesi üzerinden başka bir ürün yapısının bir parçası olan ürünler, ürünün sahibi olmayan kullanıcılar ana ürünün sahibi olmaları koşuluyla, bu kişiler tarafından serbest *bırakılabilir*.

Örneğin, X ürünü *Tasarım dolapları* ürün sahibi grubuna atanır. X ürünü, *Tasarım hoparlörleri* ürün sahibi grubuna atanmış, Y ürününün ürün reçetesinin de bir parçasıdır. *Tasarım hoparlörleri* ürün sahibi grubundaki bir kullanıcı, Y ürününü ve ürün reçetesini serbest bıraktığında, X ürünü, Y ürünü ile birlikte serbest bırakılacaktır.

Daha fazla bilgi için bkz. [Ürün sahipleri](product-owner.md).
