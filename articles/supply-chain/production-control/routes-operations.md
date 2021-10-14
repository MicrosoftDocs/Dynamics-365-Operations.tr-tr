---
title: Rotalar ve operasyonlar
description: Bu konu rotalar ve operasyonlar hakkında bilgi sağlar.
author: johanhoffmann
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable, ProdRouteJob, ProdRouteTrans, ProdRouteOverview, ProdRouteJobOverview, ProdRouteJobListPagePreviewPane, RouteTable, RouteVersionFeasibility, ProdRouteJobCurrent, RouteGroup, RouteProductionOrder, EngChgCaseRouteTablePart, EcoResProductProdTypeFormulaNoActiveRouteFormPart,
ms.author: johanho
audience: Application User
ms.reviewer: kamaybac
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b31f949304dfc9cf8723c29c1354c35ff41dbe17
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566707"
---
# <a name="routes-and-operations"></a>Rotalar ve operasyonlar

[!include [banner](../includes/banner.md)]

Bu konu rotalar ve operasyonlar hakkında bilgi sağlar. Rota, bir ürün veya ürün çeşidini üretme sürecini tanımlar. Üretim sürecindeki her adımı (operasyonu) ve bu adımların gerçekleştirilmesi gereken sırayı açıklar. Rota her adım için gerekli operasyon kaynaklarını, gerekli hazırlık süresini ve çalışma süresini, maliyetin nasıl hesaplanacağını tanımlar.

## <a name="overview"></a>Özet

Rota, bir ürünü veya ürün çeşidini üretmek için gereken operasyonların sırasını açıklar. Rota gerekli operasyon kaynaklarını, operasyonu hazırlayıp gerçekleştirmek için gereken süreyi ve maliyetin nasıl hesaplanacağını da tanımlar. Birden fazla ürün üretmek için aynı rotayı kullanabilirsiniz veya her ürün ya da ürün çeşidi için birer benzersiz rota tanımlayabilirsiniz. Hatta aynı ürün için birden fazla rotanız bile olabilir. Bu durumda, kullanılan rota, üretilmesi gereken miktar gibi etkenlere bağlı olarak değişir. Supply Chain Management'ta rotanın tanımı, birlikte üretim sürecini açıklayan dört ayrı öğeden oluşur:

- **Rota** – üretim sürecinin yapısını tanımlar. Diğer bir deyişle, operasyonların sırasını tanımlar.
- **Operasyon** – rotadaki adlandırılmış bir adımı tanımlar (örneğin **Montaj**). Aynı operasyon birden çok rotada yapılabilir ve bunların farklı operasyon numaraları olabilir.
- **Operasyon ilişkisi** – bir operasyonun hazırlık süresi ve çalışma süresi, maliyet kategorileri, tüketim parametreleri ve kaynak gereksinimleri gibi operasyonel özelliklerini tanımlar. Operasyon ilişkisi, bir operasyonun operasyonel özelliklerinin, içinde o operasyonun kullanıldığı veya ürünlerin üretilmekte olduğu rotaya göre değişmesini sağlar.
- **Rota sürümü** – bir ürünü veya ürün çeşidini üretmek için kullanılan rotayı tanımlar. Rota sürümleri rotaların farklı ürünlerde yeniden kullanılabilmesini veya zamanla değişebilmesini sağlar. Sürümler aynı ürünü üretmek için farklı rotaların kullanılabilmesini de sağlar. Bu durumda, kullanılan rota, lokasyon veya üretilmesi gereken miktar gibi etkenlere bağlı olarak değişir.

## <a name="routes"></a>Rotalar
Rota, bir ürünü veya ürün çeşidini üretmek için kullanılan operasyonların sırasını açıklar. Her operasyona bir operasyon numarası ve bir ardıl operasyon atanır. Operasyonların sırası bir veya birden fazla başlangıç noktası ve tek bir bitiş noktası olan yönlü bir grafikle temsil edilebilen bir rota ağı oluşturur. Supply Chain Management'ta rotalar yapı türüne göre ayrılır. İki tür, basit rotalar ve rota ağlarıdır. Üretim denetim parametrelerinde yalnızca basit rotalar veya daha karmaşık rota ağları kullanılıp kullanılamayacağını belirtebilirsiniz.

### <a name="simple-routes"></a>Basit rotalar

Basit rota sıralıdır ve rotanın yalnızca bir başlangıç noktası vardır.  

[![Basit rota.](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Üretim denetim parametrelerinde yalnızca basit rotaları etkinleştirirseniz, rotayı tanımladığınız zaman Supply Chain Management operasyon numaralarını otomatik olarak üretir (10, 20, 30 vb.).

### <a name="route-networks"></a>Rota ağları

Üretim denetim parametrelerinde daha karmaşık rota ağlarını etkinleştirirseniz, birden çok başlangıç noktasının ve paralel işleyen operasyonların bulunduğu rotalar tanımlayabilirsiniz.  

[![Rota ağı.](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

> [!NOTE]
> - Her operasyonun tek bir ardıl operasyonu olabilir ve tüm rota tek bir operasyonla bitmek zorundadır.
> - Birden fazla operasyonun paralel olarak çalışacak aynı ardıl operasyonu olacağının garanti etmez (örneğin önceki şekilde görülen 30 ve 40 operasyonları). Kaynakların kullanılabilirliği ve kapasitesi nedeniyle operasyonların zamanlanma yöntemine kısıtlamalar getirilebilir.
> - Operasyon numarası olarak 0 (sıfır) kullanamazsınız. Bu numara rezervedir ve rotadaki son operasyonun ardıl operasyonu olmadığını belirtmek için kullanılır.

### <a name="parallel-operations"></a>Paralel operasyonlar

Bazen, bir operasyonu gerçekleştirmek için farklı özelliklere sahip birden fazla operasyon kaynağı kombinasyonu gerekir. Örneğin, bir montaj operasyonu için bir makine, bir alet ve operasyonu denetlemek üzere her iki makine için bir işçi gerekebilir. Bu örnek, bir operasyonun birincil operasyon olarak ve diğerlerinin ikincil olarak belirlendiği paralel operasyonlarla modellenebilir.  

[![Birincil ve ikincil operasyonları olan rota.](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Genellikle birincil operasyon darboğaz kaynağını temsil eder ve ikincil operasyonlar için çalışma süresini belirler. Bununla birlikte, sınırlı kapasite içeren zaman planlamasında hem birincil operasyon hem de ikincil operasyonlar için planlanan kaynaklar aynı anda mevcut ve boş kapasiteli olmalıdır.  

Hem birincil operasyonun hem de ikincil operasyonların operasyon numarası aynı olmalıdır (önceki şekilde 30).  

Önceki örnekte birincil operasyonun (30) kaynak gereksinimi makine, ikincil operasyonların (30' ve 30'') kaynak gereksinimleri alet ve çalışandır. Yüzde ellilik bir yük, planlanan çalışanın iki makineyi aynı anda denetleyebilmesini garantilemeye yardımcı olur.

### <a name="approval-of-routes"></a>Rotaların onaylanması

Bir rotanın planlama veya üretim sürecinde kullanılabilmesi için onaylanması gerekir. Onay, rota tasarımının tamamlandığını gösterir. Piyasaya sürülen bir ürünün veya ürün çeşidinin birden fazla onaylanmış rotası olabilir. Rota onayı genellikle ilgili ilk rota sürümü onaylandığında gerçekleşir. Bununla birlikte, bazı iş senaryolarında, rotanın ve rota sürümünün onayları farklı süreç sahiplerini içerebilecek ayrı faaliyetlerdir.  

Her rota ayrı olarak onaylanabilir veya onayı kaldırılabilir. Bununla birlikte bir rotanın onayı kaldırıldığında ilgili tüm rota sürümlerinin onayının da kaldırılacağını unutmayın. Üretim denetim parametrelerinde rotaların onayının kaldırılıp kaldırılamayacağını ve onaylanmış rotaların değiştirilip değiştirilemeyeceğini belirtebilirsiniz.  

Her rotanın onaylayanının kaydedildiği bir günlük tutmanız gerekiyorsa, rota onayı için elektronik imzalar isteyebilirsiniz. Bu durumda kullanıcılar bir [elektronik imza](../../fin-ops-core/fin-ops/organization-administration/electronic-signature-overview.md) kullanarak kimliklerini onaylatmak zorundadır.

## <a name="operations"></a>Operations
Operasyon üretim sürecindeki bir adıma karşılık gelir. Her operasyonun bir kodu ve basit bir açıklaması vardır. Aşağıdaki tablolarda, bir atölyeye ait tipik operasyon örnekleri gösterilmektedir.

| Operasyon  | Açıklama        |
|------------|--------------------|
| BoruKesim    | Boru kesme       |
| TIGkaynak    | TIG kaynak        |
| JigMontaj    | Jig montajı       |
| Denetleme | Kalite inceleme |

Operasyonun hazırlık süresi ve çalışma süresi, kaynak gereksinimleri, maliyet bilgileri ve tüketim hesaplama gibi operasyonel özellikleri operasyon ilişkisinde belirtilir. (Operasyon ilişkileri hakkında daha fazla bilgi için sonraki bölüme bakın.)

## <a name="operation-relations"></a>Operasyon ilişkileri
Operasyon ilişkisinde bir operasyonun şu operasyonel özellikleri tutulur:

- Maliyet kategorileri
- Tüketim parametreleri
- İşlem süreleri
- İşlem miktarları
- Kaynak gereksinimleri
- Notlar ve yönergeler

Aynı operasyon için birden fazla operasyon ilişkisi tanımlayabilirsiniz. Ancak, her operasyon ilişkisi belirli bir operasyona özgüdür ve belirli bir madde grubuyla ilgili bir rotaya, serbest bırakılan bir ürüne veya bir serbest bırakılan ürünler grubuna özgü özellikleri saklar. Bu nedenle, farklı operasyonel özellikleri olan birden fazla rotada aynı operasyon kullanılabilir. Ayrıca, kullanılan rotadan ve üretilen üründen bağımsız olarak, aynı operasyonel özellikleri taşıyan standart operasyonlar kullanırsanız ana verilerinizi daha kolay yönetebilirsiniz. Operasyon ilişkisinin kapsamı, aşağıdaki tabloda gösterildiği gibi, **Madde kodu**, **Madde ilişkisi**, **Rota kodu** ve **Rota ilişkisi** özellikleriyle tanımlanır.

| Madde kodu | Madde ilişkisi         | Rota kodu | Rota ilişkisi   | Operasyon ilişkisinin kapsamı                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tablo     | &lt;Madde Kodu&gt;       | Rota      | &lt;Rota kodu&gt; | **Madde numarası**=&lt;madde kodu&gt; olan serbest bırakılan ürünü üretmek için **Rota numarası**=&lt;rota kodu&gt; olan rotada kullanılan bir operasyonun operasyonel özellikleri.                                                                                                                        |
| Tablo     | &lt;Madde Kodu&gt;       | Tümü        |                  | **Madde numarası**=&lt;madde kodu&gt; olan serbest bırakılan ürünü üretmek için kullanılan bir operasyonun varsayılan operasyonel özellikleri. Diğer bir deyişle, serbest bırakılan ürüne ilişkin rotaya özgü bir operasyon ilişkisi yoksa bu operasyonel özellikler uygulanır.                                     |
| Grup     | &lt;Madde grubu kodu&gt; | Rota      | &lt;Rota kodu&gt; | Kodu &lt;madde grubu kodu&gt;, olan madde grubuyla ilişkili serbest bırakılan ürünleri üretmek için **Rota numarası**=&lt;rota kodu&gt; olan kotada kullanılan bir operasyonun operasyonel özellikleri (serbest bırakılan ürün için rotaya özgü bir operasyon ilişkisi olmadığı sürece).                         |
| Grup     | &lt;Madde grubu kodu&gt; | Tümü        |                  | Numarası &lt;madde grubu kodu&gt; olan madde grubuyla ilişkili serbest bırakılan ürünleri üretmek için kullanılan bir operasyonun varsayılan operasyonel özellikleri (daha spesifik bir operasyon ilişkisi olmadığı sürece).                                                                                                  |
| Tümü       |                       | Rota      | &lt;Rota kodu&gt; | **Rota numarası**=&lt;rota kodu&gt; olan rotada kullanılan operasyonun varsayılan operasyonel özellikleri. Diğer bir deyişle, bu rota için serbest bırakılan ürüne veya ilişkili madde grubuna özgü bir operasyon ilişkisi yoksa bu operasyonel özellikler uygulanır. |
| Tümü       |                       | Tümü        |                  | Bir operasyonun varsayılan operasyonel özellikleri. Daha spesifik bir operasyon ilişkisi yoksa bu operasyonel özellikler uygulanır.                                                                                                                                                                |

Bir operasyon ilişkisinin bir tesise özgü olduğunu da belirtebilirsiniz. Bu şekilde, bir operasyonun operasyonel özellikleri, operasyonun yapıldığı lokasyona (yani tesise) göre değişebilir. Yapılandırılmış ürünlerde, her ürün yapılandırması için farklı operasyonel özellikler de belirtebilirsiniz.  

Operasyon ilişkileri, rotaları tanımlarken size çok esneklik sağlar. Ayrıca, varsayılan özellikleri tanımlayabilmek, yönetmeniz gereken ana veri miktarını azaltmaya yardımcı olur. Ancak, bu esneklik, bir operasyon ilişkisini değiştirdiğiniz bağlamı bilmeniz gerektiği anlamına gelir.  

> [!NOTE]
> Operasyonel özellikler rota başına her operasyon için operasyon ilişkilerinde depolandığından, aynı operasyonun (örneğin Montaj) tüm tekrarlarında aynı hazırlık süresi, çalışma süresi, kaynak gereksinimleri vb. kullanılır. Bu nedenle, bir operasyon aynı rotada iki kez uygulanıyorsa ama farklı çalışma süreleri varsa iki ayrı operasyon oluşturmanız gerekir (Montaj1, Montaj2 gibi).

### <a name="modifying-product-specific-routes"></a>Ürüne özgü rotalarda değişiklik

**Serbest bırakılan ürün ayrıntıları** sayfasından **Rota** sayfasını açtığınız zaman, seçili serbest bırakılan ürünle ilişkili rota sürümleri gösterilir. Bu bağlamda Supply Chain Management, her operasyon için, rota sürümüyle en iyi eşleşen operasyon ilişkisinden operasyonel özellikleri gösterir. Operasyon ilişkisindeki **Madde kodu** ve **Rota kodu** özelliklerini içeren operasyonlar listesini göreceksiniz. Bu sayede, hangi operasyon ilişkisinin gösterildiğini belirleyebilirsiniz.  

**Rota** sayfasında, operasyonun çalışma süresi veya maliyet kategorileri gibi operasyonel özelliklerinde değişiklik yapabilirsiniz. Değişiklikleriniz, geçerli rota sürümünde gösterilen rotaya ve serbest bırakılan ürüne özgü operasyon ilişkisinde depolanır. Gösterilen operasyon ilişkisi rotaya ve serbest bırakılan ürüne özgü değilse, değişiklikleriniz depolanmadan önce sistem o operasyon ilişkisinin bir kopyasını oluşturur. Bu kopya o rota ve serbest bırakılan ürüne *özgüdür*. Bu sayede, yaptığınız değişiklikler diğer rotaları veya serbest bırakılan ürünleri etkilemez. **Rota** sayfasında değişiklik yapılmakta olan operasyonun hangisi olduğunu doğrulamak için **Madde kodu** ve **Rota kodu** alanlarına bakın.  

Rotaya ve serbest bırakılan ürüne özgü bir operasyonu **İlişkiyi kopyala ve düzenle** işleviyle kendiniz oluşturabilirsiniz.  

> [!NOTE]
> **Rota** sayfasındaki bir rotaya yeni bir operasyon eklerseniz yalnızca mevcut serbest bırakılan ürün için bir operasyon ilişkisi oluşturulur. Bu nedenle, rota başka serbest bırakılan ürünleri üretmek için de kullanıldığı zaman o serbest bırakılan ürünler için geçerli bir operasyon ilişkisi olmaz rota artık o serbest bırakılan ürünler için kullanılamaz.

### <a name="maintaining-operation-relations-per-route"></a>Rotanın operasyon ilişkilerini yönetme

**Rotalar** liste sayfasında **Rota ayrıntıları** sayfasını açtığınız zaman, seçili rotaya ilişkin tüm operasyon ilişkilerinin listesi gösterilir. Bu nedenle, hangi operasyonel özelliklerin hangi ürünler için kullanıldığını kolayca doğrulayabilirsiniz. Hem varsayılan özellik değerlerinde hem de ürüne özgü özellik değerlerinde değişiklik yapabilirsiniz.  

**Rota ayrıntıları** sayfasında yeni bir operasyon ilişkisi eklerseniz, **Rota kodu** alanı ayarı otomatik olarak **Rota** yapılır ve **Rota ilişkisi** alanı ayarı geçerli rotanın rota numarasına getirilir.

### <a name="maintaining-operation-relations-per-operation"></a>Operasyonun özgü operasyon ilişkilerini yönetme

**Operasyonlar** sayfasından **Operasyon ilişkileri** sayfasını açabilirsiniz. Bu sayfada, belirli bir operasyonun tüm operasyon ilişkilerinde değişiklik yapabilirsiniz. Varsayılan değerler içeren operasyon ilişkilerini bile değiştirebilirsiniz.  

İşletmeniz standart operasyonlar kullanıyorsa ve operasyonel parametreler tüm ürün ve süreçlerde aynıysa, **Operasyon ilişkileri** sayfasında bu operasyonların varsayılan operasyonel özelliklerini yönetmek için uygun bir yol belirtilir.

### <a name="applying-operation-relations"></a>Operasyon ilişkilerini uygulama

Bazı durumlarda, Supply Chain Management'ın bir operasyonun operasyonel özelliklerini bulması gerekir. Örneğin, bir satınalma siparişi oluşturulduğunda, her operasyonun operasyonel özellikleri operasyon ilişkilerinden üretim rotasına kopyalanmalıdır. Böyle durumlarda, Supply Chain Management ilgili operasyon ilişkilerini en spesifik kombinasyondan en az spesifik kombinasyona doğru arar.  

Supply Chain Management serbest bırakılan bir ürün için en uygun operasyon ilişkisini ararken, serbest bırakılan ürünün madde koduyla eşleşen bir operasyon ilişkisi, madde grubu koduyla eşleşen bir operasyon ilişkisine tercih edilir. Buna karşılık, madde grubu koduyla eşleşen bir operasyon ilişkisi, varsayılan operasyon ilişkisine tercih edilir. Arama aşağıdaki sıraya göre yapılır:

1.  **Madde kodu**=**Tablo** ve **Madde ilişkisi**=&lt;madde kodu&gt;
2.  **Madde kodu**=**Grup** ve **Madde ilişkisi**=&lt;madde grubu kodu&gt;
3.  **Madde kodu**=**Tümü**
4.  **Rota kodu**=**Rota** ve **Rota ilişkisi**=&lt;rota kodu&gt;
5.  **Rota kodu**=**Tümü**
6.  **Yapılandırma**=&lt;yapılandırma kodu&gt;
7.  **Yapılandırma**=
8.  **Tesis**=&lt;Tesis kodu&gt;
9.  **Tesis**=

Bu nedenle, bir operasyon her rota için yalnızca bir kez kullanılmalıdır. Operasyon aynı rotada birden çok kez gerçekleşirse, o operasyonun tüm tekrarları aynı operasyon ilişkisini taşıyamaz ve her tekrar için farklı özelliklere (örneğin çalışma süreleri) sahip olamazsınız.

## <a name="route-versions"></a>Rota sürümleri

Rota sürümleri ürünlerin üretimindeki varyasyonları karşılamak veya üretim süreci üzerinde daha fazla kontrol sağlamak için kullanılır. Bu sürümler belirli bir serbest bırakılan ürün veya serbest bırakılan ürün çeşidi üretilirken kullanılması gereken rotayı tanımlar. Serbest bırakılan bir üründe hangi rotanın kullanılacağını tanımlamak için aşağıdaki kısıtlamaları kullanabilirsiniz:

- Ürün boyutları (boyut, renk, stil veya yapılandırma)
- Üretim miktarı
- Üretim tesisi
- Üretim tarihi

Ürünü belirli bir tesiste, miktarda veya bir süre içinde üretirken, varsayılan rota sürümü olarak belirli bir rota sürümü belirleyebilirsiniz. Bununla birlikte, belirli bir serbest bırakılan ürün ve belirli bir kısıtlama grubu için yalnızca bir adet etkin rotaya izin verildiğini unutmayın.  

Üretim denetim parametrelerinde, bir rota sürümünün geçerlilik süresinin her zaman belirtilmesini zorunlu kılabilirsiniz.

### <a name="approval-of-route-versions"></a>Rota sürümlerini onaylama

Bir rota sürümünün planlama veya üretim sürecinde kullanılabilmesi için onaylanması gerekir. Bir rota sürümünü onaylarken ilgili rotayı da onaylayabilirsiniz. Bununla birlikte, bir rota sürümünün ancak ilgili rotanın da onaylanması durumunda onaylanabileceğini unutmayın.

### <a name="activating-the-default-route-version"></a>Varsayılan rota sürümünü etkinleştirme

Bir rota sürümünü etkinleştirdiğinizde, onu ana planlamanın kullanacağı varsayılan rota sürümü olarak ya da üretim emirleri oluşturmak için kullanılacak şekilde belirtirsiniz. Belirli bir kısıtlama grubu için yalnızca bir etkin rota sürümü kullanabilirsiniz (örneğin, dönem, tesis veya miktar). Etkinleştirmeye çalıştığınız sürüm zaten etkin olan bir sürümle çakışırsa, bir hata iletisi alırsınız. Bu durumda belirsiz bir etkinleştirmeyi önlemek için, çakışan sürümü devre dışı bırakmanız veya rotanın sürümündeki kısıtlamaları (genellikle dönemi) değiştirmeniz gerekir.

### <a name="electronic-signatures"></a>Elektronik imzalar

Her rota sürümünü kimin onayladığının ve etkinleştirdiğinin kaydedildiği bir günlük tutmanız gerekiyorsa, bu görevler için elektronik imzalar isteyebilirsiniz. Böylece rota sürümlerini onaylayan ve etkinleştiren kullanıcıların [elektronik imza](../../fin-ops-core/fin-ops/organization-administration/electronic-signature-overview.md) kullanarak kimliklerini doğrulamaları gerekir.

### <a name="product-change-that-uses-case-management"></a>Servis talebi yönetiminin kullanıldığı ürün değişikliği

Yeni veya değiştirilmiş rotaları ve rota sürümlerini onaylamak ve etkinleştirmek için yapılan ürün değişikliği servis talebi, rota sürümü kısıtlamalarını genel bir açıdan görmenin kolay bir yoludur. Ayrıca, tek bir işlemde belirli bir değişiklikle ilgili tüm rotaları onaylayıp etkinleştirebilir ve sonuçları ürün değişikliği servis talebinde belgeleyebilirsiniz.

## <a name="maintaining-routes"></a>Rotaları yönetme

İş gereksinimlerinize bağlı olarak, işlem tanımlarınızı korumak için gereken iş yükünü azaltabilirsiniz.

### <a name="making-routes-independent-of-resources"></a>Kaynaklardan bağımsız rota yapma

Birçok sistemde, bir operasyonu gerçekleştirmesi gereken operasyon kaynaklarının veya kaynak grubunun rotada belirtilmesi gerekir. Bununla birlikte, Supply Chain Management'ta bir operasyon kaynağının operasyona uygun olması için karşılaması gereken bir dizi gereksinimi tanımlayabilirsiniz. Bu nedenle, kullanılması gereken belirli operasyon kaynaklarının veya kaynak grubunun, operasyon fiilen planlanana kadar belirlenmesine gerek yoktur. Bu işlevsellik, özellikle, aynı operasyonu gerçekleştirebilecek birçok çalışan veya makineye sahip olduğunuzda yararlıdır.  

Örneğin bir operasyon için 20 tonluk **Damgalama** kapasiteli **Makine** tipinde bir operasyon kaynağı gerektiğini belirtiyorsunuz. Planlama altyapısı, operasyon planlanırken bu gereksinimleri belirli bir operasyon kaynağına veya kaynak grubuna bağlar. İşlemi belirli bir makineye bağlamak yerine yalnızca bu gereksinimleri belirtebildiğiniz için daha fazla esneklik elde edersiniz. Ayrıca, kaynaklar taşınırken veya yeni kaynaklar eklenirken yönetim daha kolay hale gelir.  

Çeşitli kaynak gereksinimi türleri ve bunların nasıl kullanılacağı hakkında daha fazla bilgi için bkz. Operasyon kaynağı gereksinimleri ve [Kaynak yetenekleri](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Rotaları tesisler arasında paylaştırma

Aynı ürünü birden fazla üretim tesisinde üretiyorsanız ve ürünün üretilmesi için gereken adımlar tüm tesislerde aynı ise, genellikle tüm üretim tesislerinde kullanılmak üzere paylaşılan bir rota tasarlayabilirsiniz. Paylaşılan bir rota oluştururken rotada tesis belirtmeyin. Ancak yine de, paylaşılan rotayı her bir sitedeki ürünle ilişkilendiren bir rota sürümü oluşturmanız gerekir.  

Ayrıca, rotadaki her operasyon için kaynak gereksinimlerinin belirli operasyon kaynakları veya kaynak grupları için değil, bunun yerine gerekli kaynakların özellikleri açısından ifade edildiğinden emin olmanız gerekir. Planlama altyapısı, bunun üzerine, üretimin planlandığı tesisten uygun operasyon kaynaklarını atayabilir. Örneğin, çalışma süresinde küçük farklılıklar varsa veya belirli bir operasyon için hazırlık süresi tesise özgüyse, bu tesis için bir ek operasyon ilişkisi ekleyerek bu bilgileri belirtebilirsiniz.  

Paylaşılan rotaların avantajlarından tam olarak yararlanabilmek için, ilgili ürün reçetelerinde (BOM) kaynak tüketimini de kullanmanız gerekir. Ürün reçetesi satırındaki kaynak tüketimi için bayrağı belirlediğinizde, ambar ve ham maddelerin tüketilmesi gereken lokasyon, operasyonun üzerinde planlandığı operasyon kaynaklarından çıkarsanır. Dolayısıyla, üretim fiilen planlanıncaya kadar ambar ve lokasyonun belirlenmesi gerekmez. Bu şekilde, ürün reçetesini hem rota hem de ürünün üretildiği fiziksel lokasyondan bağımsız kılabilirsiniz.

### <a name="standard-operation-relations"></a>Standart operasyon ilişkileri

İşletmeniz tüm üretim sürecinde standartlaştırılmış operasyonlar kullanıyorsa ve hazırlık süresi, çalışma süresi, tüketim hesaplaması, maliyet hesaplaması vb. özelliklerde çok az değişiklik varsa veya hiç değişiklik yoksa, tüm operasyonlar için varsayılan operasyon ilişkileri oluşturmanız yararlı olabilir. Bu durumda, herhangi bir rotaya veya serbest bırakılan ürüne özgü operasyon ilişkileri oluşturmaktan kaçının.  

Ayrıca, beceri ve yetenek türünde kaynak gereksinimleri belirliyorsanız ve rotalarınızı tesisten bağımsız yaparsanız, iş süreçlerinizin sürekli yönetimini minimumda tutmaya yardımcı olabilirsiniz.  

Bu yaklaşımı kullandığınız zaman, **Operasyon ilişkileri** sayfası, çalışma süreleri ve diğer özelliklerin yönetimi için birincil hedefiniz haline gelir.

### <a name="resource-specific-process-times"></a>Kaynağa özgü işlem süreleri

Bir operasyonun kaynak gereksinimlerinin bir parçası olarak bir operasyon kaynağı veya kaynak grubu belirtmezseniz, geçerli kaynaklar farklı hızlarda çalışabilir. Bu nedenle, bir operasyonu yürütmek için gereken süre değişebilir. Bu sorunu gidermek amacıyla, işlem süresinin nasıl hesaplanacağını belirtmek için, operasyon ilişkisindeki **Formül** alanını kullanabilirsiniz. Aşağıdaki seçenekler bulunur:

- **Standart** – (Varsayılan seçenek) Hesaplama, yalnızca operasyon ilişkisindeki alanları kullanır ve belirtilen çalışma süresini sipariş miktarıyla çarpar.
- **Kapasite** – Hesaplamaya, operasyon kaynağındaki **Kapasite** alanı dahil edilir. Bu nedenle, süre kaynağa bağlıdır. Operasyon kaynağında belirtilen değer saat başına kapasitedir. **İşlem süresi** **Sipariş miktarı** bölü **Kapasite** olarak hesaplanır.
- **Parti** – Parti kapasitesi, operasyon ilişkisinden alınan bilgilerle hesaplanır. Parti sayısı ve dolayısıyla işlem süresi sipariş miktarına göre hesaplanabilir.
- **Kaynak parti** – Bu seçenek temelde **Parti** seçeneğiyle aynıdır. Ancak, hesaplamaya, operasyon kaynağındaki **Parti kapasitesi** alanı dahil edilir. Bu nedenle, süre kaynağa bağlıdır.

### <a name="set-up-route-groups"></a>Rota gruplarını ayarla

Rota gruplarını ve rota veya iş türü için kurulumunu **Üretim denetimi > Kurulum > Rotalar > Rota grupları** altında tanımlayabilirsiniz. Her bir rota grubundaki Rota/iş türü için, aşağıdaki seçenekleri seçebilir veya temizleyebilirsiniz:

- **Etkinleştirme** - Seçilen iş türü için hesaplamaları ve planlamayı etkinleştirmek ve iş planlamasını çalıştırdığınızda geribildirim almak için bu seçeneği seçin. Bu seçeneği iş türünü etkinleştirmek ve daha sonra, bu iş türü için seçeneklerin geri kalanını seçmek için seçmeniz gerekir. Etkinleştirme seçilmezse, bu iş türü etkinleştirilmeyecektir, diğer seçeneklerin ne olduğundan bağımsız olarak. 
- **İş yönetimi** - İş planlamasını çalıştırdığınızda iş türünü iş yönetimine dahil etmek için bu seçeneği seçin. 
- **Çalışma süresi** İşlem kaynakları için tanımlanan çalışma süresi takvimine göre iş türünü planlamak için bu seçeneği seçin, aksi taktirde Miladi takvim kullanılır. Çalışma zamanı, Miladi takvime göre veya tanımlanmış çalışma takvimine göre planlanabilir. Bu seçeneği seçerseniz, planlama tanımlanmış çalışma süresi takvimini temel alır. Ayrıca, iş türünün işi, işin başlangıç tarihi olarak tanımlanan tarihte gece yarısından itibaren planlanır.
- **Kapasite** - İş planlamasını çalıştırdığınızda iş türü için kapasite rezerve etmek için bu seçeneği seçin. Bu seçeneği seçerseniz, seçili iş türü için iş planlama çalıştırıldığında kapasite rezerve edilir. Bu, işlem kaynaklarını her rota grubunda hangi iş türlerinin kullandığının özetini verir. Örneğin, kurutma kaynaklarının darboğazda kaynaklar olması durumunda, bu kaynaklar darboğaz olarak belirtilmelidir. Kuyruk süresi iş türlerine atanan kurutma işlemleri kurutma kaynaklarını rezerve edecektir. 

İş türlerinin her biri için, önce etkinleştirmeniz veya devre dışı bırakmanız gerekir. Devre dışı bırakıldığında, diğer kurulumdan hiçbiri (İş yönetimi, çalışma zamanı ve kapasite) dikkate alınmayacaktır, çünkü iş türü etkin olmayacaktır. 

İş türleri arasında Çakışma'yı bulabilirsiniz. Çakışma, farklı işlerin aynı anda gerçekleştirilmesine izin verir. İşler çakıştığında, kaynaklar kullanılabilir ancak belirli işler için rezerve edilemez.
Bu nedenle, Etkinleştirme Çakışma için seçildiğinde, ayarların geri kalanı (İş yönetimi, Çalışma zamanı ve Kapasite), rota grubunda herhangi bir etki yapmaz. 

> [!NOTE]
> Sürüm yükselttiğinizde, aşağıdaki hatayla karşılaşabilirsiniz: **"CRL Hatası zamanlama altyapısı çağrılırken oluştu**. Bu hatayla karşılaşırsanız, **Rota grupları** sayfasına gidin ve **Çakışma**'yı etkinleştirdiğiniz tüm rotalar için **İş yönetimi**, **Çalışma süresi** ve **Kapasite** seçeneklerini temizleyin. 

## <a name="additional-resources"></a>Ek kaynaklar

- [Ürün reçeteleri ve formüller](bill-of-material-bom.md)

- [Üretim rotasında kullanılan maliyet kategorileri](../cost-management/cost-categories-used-production-routings.md)

- [Kaynak yetenekleri](resource-capabilities.md)

- [Elektronik imzalara genel bakış](../../fin-ops-core/fin-ops/organization-administration/electronic-signature-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]