---
title: "Üretim yürütmede üretim parametreleri"
description: "Bu konu Üretim yürütmeden üretim parametrelerinin ayarlanmasıyla ilgili bilgiler içerir."
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a0a28ba5072d55b8133f5458f75befa752a3dcdf
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="production-parameters-in-manufacturing-execution"></a>Üretim yürütmede üretim parametreleri

[!INCLUDE [banner](../includes/banner.md)]

Bu konu Üretim yürütmeden üretim parametrelerinin ayarlanmasıyla ilgili bilgiler içerir.

**Üretim yürütme** modülü temel olarak üretim şirketleri tarafından kullanılmak üzere tasarlanmıştır. Üretim işleri veya projelerde zaman ve madde tüketimini kaydetmek için kullanılabilir. İş kayıtları için Üretim yürütmeyi kullanmaya başlamadan önce, kayıtların üretim süresi sırasında nasıl ve ne zaman deftere nakledileceğini tanımlayan çeşitli üretim parametreleri ayarlamanız gerekir. Üretim parametreleri ayarları stok yönetimini, üretim yönetimini ve maliyet hesaplamasını etkiler.

Çalışanlar üretim işleri üzerinde kayıtlar yapmaya başlamadan önce **Üretim parametreleri** sayfasındaki tüm ayarlar üzerinde dikkatlice düşünmelisiniz. **Üretim denetimi** &gt; **Kurulum** &gt; **Üretim yürütme** &gt; **Üretim emri varsayılanları** öğesine tıklayın. Şirketiniz çoklu tesis işlevini kullanıyorsa, her tesise yönelik farklı üretim parametreleri ayarlamak isteyebilirsiniz. **Üretim** modülüyle entegrasyon için parametreler **Üretim parametreleri** sayfasındaki şu sekmelerden ayarlanır:

- **Genel** – Üretim yürütmedeki üretim işlerine ilişkin parametre ayarları.
- **Başlangıç** - Üretim işlemleri başlatıldığında kullanılan parametreler.
- **Operasyonlar** – Üretim işlerine uygulanan parametreler ve üretim süreci sırasındaki operasyonlarla ilgili geribildirim.
- **Tamamlandı bildirimi** - Maddeler, üretim emrinin son operasyonunda tamamlandı olarak bildirildiğinde kullanılan parametreler.
- **Miktar doğrulaması** – Üretim emirlerindeki başlangıç ve geribildirim miktarlarını doğrulamak için kullanılan parametreler.

## <a name="types-of-production-jobs"></a>Üretim işleri tipleri
**Operasyonlar** sekmesinde, **İş kaydı** sayfasında kayıt yapılmasını gerektiren üretim işlerinin türlerini seçin.

Genellikle, çalışanlar kurulum işlerine ve işlem işlerine kayıt yaptırır. Ancak, iş planlama uygulanması durumunda, çalışanların üretim emirleri işleme konduğunda kayıt yaptırmak zorunda oldukları diğer iş türlerini de seçebilirsiniz. Örneğin, taşıma işleri için kaydı gerekli kılabilirsiniz.

> [!IMPORTANT]
> Tüm ilgili iş tiplerini seçtiğinizden emin olun. Aksi halde, işler **İş kaydı** sayfasında kayıt için görüntülenmeyebilir. Seçimleriniz **Rota grupları** sayfasında bulunan **Kurulum** sekmesindeki **İş yönetimi** sütunundaki seçimlerle eşleşmelidir (**Üretim denetimi**  &gt; **Kurulum** &gt; **Rotalar** &gt; **Rota grupları**) .

Rota grubunda **İş yönetimi** seçilirse, iş Üretim yürütmede tamamlandı olarak bildirildiğinde bu iş tipi üretim emrinde tamamlandı olarak bildirilir. **İş yönetimi** seçimi yapılan tüm iş türleri bir operasyonda tamamlandı olarak bildirildiğinde, Üretim yürütme operasyonu tamamlandı olarak raporlar.

> [!NOTE]
> Bazı iş tipleri üretim günlükleri üzerinden el ile bildirilebilir. Bu durumda, iş türü için **İş yönetimi**'ni seçin ancak Üretim yürütmedeki **Üretim parametreleri** sayfasında bulunan **Operasyonlar** sekmesinde kayıt için iş türünü seçmeyin.

## <a name="bom-consumption-and-picking-list-journals"></a>Ürün reçetesi tüketimi ve malzeme çekme listesi günlükleri
Ürün reçetesi (BOM) tüketimi için tutarlı bir ayar önemlidir çünkü bu stok yönetiminin etkili olmasını sağlar. Örneğin, ürün reçetesi tüketimi parametreleri Üretim yürütmede düzgün şekilde ayarlanmazsa, malzemeler stoktan iki kez düşülebilir veya hiç düşülmez.

**Üretim parametreleri** sayfasında, otomatik ürün reçetesi tüketimi üç aşamada ayarlanır:

- Üretim başlangıcında. Bu aşamayı **Başlangıç** sekmesinden ayarlayın.
- Bir İşlem tamamlandığında üretim sürecinde. Bu aşamayı **Operasyonlar** sekmesinden ayarlayın.
- Bir üretim emri tamamlandı olarak bildirildiğinde. Bu aşamayı **Tamamlandı bildirimi** sekmesinden ayarlayın.

Her aşama için **Otomatik ürün reçetesi tüketimi** alanı, bir üretim emriyle ilgili malzeme çekme için üç yöntemden birini seçmenize olanak sağlar:

- **Otomatik tüketim kuralı** – Bu seçenek, **Üretim** modülünde ürün reçetesi için tanımlanmış bir seçenek ile birlikte kullanılır. **Üretim denetimi** &gt; **Ortak** &gt; **Üretim emirleri** &gt; **Tüm üretim emirleri**'ni tıklayın. **Tüm üretim emirleri** sayfasında, listeden bir üretim emri seçin ve ardından Eylem Panosunda **Ürün reçetesi**'ne tıklayın. **Ürün reçetesi** sayfasında **Kurulum** sekmesindeki **Otomatik tüketim kuralı** alanında, aşağıdaki seçeneklerden birini seçin:

  - **Başlangıç**
  - **Son**
  - **El ile**
  - Boş (Hiçbir seçenek belirtilmez.)
  - **Yerleşimde kullanılabilir**

    Üretim yürütmede, **Başlangıç** sekmesindeki **Otomatik ürün reçetesi tüketimi** alanında **Otomatik tüketim kuralı** seçilirse, ürün reçetesinde **Başlangıç** olarak ayarlanan tüm malzemeler operasyon başlatıldığında, stoktan düşülür. **Yerleşimde kullanılabilir** seçeneği, gelişmiş ambar işlemleri için etkinleştirilen ürünler için kullanılır. Bu otomatik tüketim kuralını seçerseniz, malzeme ham madde çekme için ambar işi tamamlandığında tüketilir. Malzeme ayrıca bu tüketim kuralını kullanan bir ürün reçetesi satırı ambara serbest bırakıldığında ve malzeme üretim giriş konumunda kullanılabilir olduğunda da tüketilir.

    > [!NOTE]
    > **Otomatik tüketim kuralı** alanı Üretim yürütme içerisinde **Başlat** sekmesinde ayarlanmışsa, aynı kuralı ya **Operasyonlar** sekmesinde ya da **Tamamlandı olarak raporla** sekmesinde seçmelisiniz. Bu gereksinim, malzemelerin, **Sonlandır**'ı tüketim kuralı olarak üretim emrinde kullanan ürün reçetelerinden eksiltilmesini garanti etmeye yardımcı olur. **Operasyonlar** sekmesinde veya **Tamamlandı bildirimi** sekmesinde aynı otomatik tüketim kuralı seçilmezse, malzemelerin stoktan iki kez düşülebilir.

- **Her zaman** – Bir aşama için bu seçeneği belirlediğinizde, malzemeler her zaman bu aşamada stoktan düşülür. Örneğin, üretim için malzemeler üretim emri başlatıldığında düşülür. Bu ayar **Operasyonlar** ve **Tamamlandı bildirimi** sekmelerinde **Hiçbir zaman** seçeneğinin seçili olmasını gerektirir. Bu gereksinim maddelerin stoktan iki kez düşülmesini önler.
- **Hiçbir zaman** – Bir aşama için bu seçeneği belirlediğinizde, bu aşamada ürün reçetesi tüketimi gerçekleşmez. Örneğin, her üç sekmede de **Hiçbir zaman** seçilirse (**Başlangıç**, **Operasyonlar** ve **Tamamlandı bildirimi**), malzemelerin stoktan el ile düşülmesi gerekir.

> [!IMPORTANT]
> Üretim parametreleri ayarlarınızı dikkatli şekilde değerlendirin ve **Üretim parametreleri** sayfasının çeşitli sekmelerinde seçilen parametrelerin birbiriyle çakışmadığından emin olun.

Aşağıdaki örnekler çeşitli ürün reçetesi tüketim kuralını destekleyen parametre ayarlarını göstermektedir. Parametreler Üretim yürütmedeki **Üretim parametreleri** sayfasından ayarlanır.

### <a name="example-1-backflushing-on-operations"></a>Örnek 1 : Operasyonlarda malzeme çekme

Maddeler bir operasyonda tamamlandı olarak bildirildiğinde ürün reçetesi madde tüketimi ve malzeme çekme listesi günlüklerinin oluşturulması gerekiyorsa aşağıdaki ayarları kullanın.

| Sekme                | Alan                          | Ayar                             |
|--------------------|--------------------------------|-------------------------------------|
| Başlat              | Başlatmayı çevrimiçi olarak güncelleştir           | **Durum** veya **Durum + miktar** |
| Başlat              | Otomatik ürün reçetesi tüketimi      | **Hiçbir Zaman**                           |
| Operations         | Otomatik ürün reçetesi tüketimi      | **Her zaman**                          |
| Tamamlandı bildirimi | Otomatik ürün reçetesi tüketimi      | **Hiçbir Zaman**                           |
| Tamamlandı bildirimi | Tamamlanan raporu çevrimiçi olarak güncelleştir | **Durum + miktar**               |

### <a name="example-2-backflushing-on-production"></a>Örnek 2: Üretimde malzeme çekme

Maddeler üretim emrinde tamamlandı olarak bildirildiğinde ürün reçetesi madde tüketimi ve malzeme çekme listesi günlüklerinin oluşturulması gerekiyorsa aşağıdaki ayarları kullanın.

| Sekme                | Alan                          | Ayar                             |
|--------------------|--------------------------------|-------------------------------------|
| Başlat              | Başlatmayı çevrimiçi olarak güncelleştir           | **Durum** veya **Durum + miktar** |
| Başlat              | Otomatik ürün reçetesi tüketimi      | **Hiçbir Zaman**                           |
| Operations         | Otomatik ürün reçetesi tüketimi      | **Hiçbir Zaman**                           |
| Tamamlandı bildirimi | Otomatik ürün reçetesi tüketimi      | **Her zaman**                          |
| Tamamlandı bildirimi | Tamamlanan raporu çevrimiçi olarak güncelleştir | **Durum + miktar**               |

### <a name="example-3-flushing-principle"></a>Örnek 3: Otomatik tüketim kuralı

Ürün reçetesi maddeleri için ayarlanan otomatik tüketim kuralı ayarına göre ürün reçetesi madde tüketimi ve malzeme çekme listesi günlüklerinin oluşturulması gerekiyorsa aşağıdaki ayarları kullanın.

| Sekme                | Alan                          | Ayar                |
|--------------------|--------------------------------|------------------------|
| Başlat              | Başlatmayı çevrimiçi olarak güncelleştir           | **Durum + miktar**  |
| Başlat              | Otomatik ürün reçetesi tüketimi      | **Otomatik tüketim kuralı** |
| Operations         | Otomatik ürün reçetesi tüketimi      | **Otomatik tüketim kuralı** |
| Tamamlandı bildirimi | Otomatik ürün reçetesi tüketimi      | **Hiçbir Zaman**              |
| Tamamlandı bildirimi | Tamamlanan raporu çevrimiçi olarak güncelleştir | **Durum + miktar**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>Örnek 4: Bir üretim emrinin başlatılması sırasında malzemelerin düşülmesi

Bir üretim başlatıldığında ürün reçetesi madde tüketimi ve malzeme çekme listesi günlüklerinin oluşturulması gerekiyorsa aşağıdaki ayarları kullanın.

| Sekme                | Alan                          | Ayar                             |
|--------------------|--------------------------------|-------------------------------------|
| Başlat              | Başlatmayı çevrimiçi olarak güncelleştir           | **Durum + miktar**               |
| Başlat              | Otomatik ürün reçetesi tüketimi      | **Her zaman**                          |
| Operations         | Otomatik ürün reçetesi tüketimi      | **Hiçbir Zaman**                           |
| Tamamlandı bildirimi | Otomatik ürün reçetesi tüketimi      | **Hiçbir Zaman**                           |
| Tamamlandı bildirimi | Tamamlanan raporu çevrimiçi olarak güncelleştir | **Durum** veya **Durum + miktar** |

Bu bölümde daha önce açıklanan seçimleri temel alarak, malzeme çekme listesi günlükleri üretim emri işleminin çeşitli aşamalarında nakledilir:

- Bir operasyon başlatıldığında
- Bir operasyonda miktar geribildirimi bildirildiğinde
- Üretim emrinde maddeler tamamlandı olarak bildirildiğinde

### <a name="example-5-manual-bom-consumption"></a>Örnek 5: El ile ürün reçetesi tüketimi

Malzemelerin stoktan her zaman el ile düşülmesi gerekiyorsa aşağıdaki ayarları kullanabilirsiniz. Bu durumda, malzeme çekme listesi günlüğü deftere nakledilmez.


|        Sekme         |             Alan              |         Ayar         |
|--------------------|--------------------------------|-------------------------|
|       Başlat        |      Başlatmayı çevrimiçi olarak güncelleştir      | <strong>Durum</strong> |
|       Başlat        |   Otomatik ürün reçetesi tüketimi    | <strong>Hiçbir Zaman</strong>  |
|     Operations     |   Otomatik ürün reçetesi tüketimi    | <strong>Hiçbir Zaman</strong>  |
| Tamamlandı bildirimi |   Otomatik ürün reçetesi tüketimi    | <strong>Hiçbir Zaman</strong>  |
| Tamamlandı bildirimi | Tamamlanan raporu çevrimiçi olarak güncelleştir | <strong>Durum</strong> |


