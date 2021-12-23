---
title: Warehouse Management mobil uygulaması için adım başlıklarını ve yönergeleri özelleştirme
description: Bu konuda, Warehouse Management mobil uygulaması için ayarladığınız her bir görev akışının tüm adımları için özel yönergelerin nasıl oluşturulacağı ve gösterileceği açıklanmaktadır.
author: Mirzaab
ms.date: 08/11/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-11
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ffd433427b2c5011740a7ee54c93713689945df3
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902259"
---
# <a name="customize-step-titles-and-instructions-for-the-warehouse-management-mobile-app"></a>Warehouse Management mobil uygulaması için adım başlıklarını ve yönergeleri özelleştirme

> [!IMPORTANT]
> Bu konuda açıklanan özellikler yalnızca yeni Warehouse Management mobil uygulaması için geçerlidir. Artık kullanımdan kaldırılan eski ambar uygulamasını etkilemezler.

Bu konuda, Warehouse Management mobil uygulaması için ayarladığınız tüm görev akışlarının her bir adımı için özel yönergelerin nasıl oluşturulacağı ve gösterileceği açıklanmaktadır. Ambar çalışanları iyi yazılmış yönergeler aldıklarında önceden eğitime ihtiyaç duymadan yeni akışları hemen kullanmaya başlayabilirler. Bu özellik aşağıdaki avantajları sağlar:

- **Her görev adımı için basit yönergeler izlemelerini sağlayarak çalışanları işe daha hızlı alıştırın.** Akışın her adımı, ön saflardaki çalışanların görevi anlamasını sağlayan yönergeler sağlar.
- **Kendi süreçlerinizle eşleşen yönergeler sağlayın.** İş ve ambar süreçlerinizle eşleşecek kendi yönergelerinizi yazın. Örneğin, terminolojiyi fiziksel alanınıza ve yerel kısaltmalara uygun hale getirebilirsiniz.

## <a name="turn-on-the-warehouse-app-step-instructions-feature"></a>Ambar uygulaması adım yönergeleri özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Ambar uygulaması adım yönergeleri*

## <a name="step-titles-and-step-instructions-in-the-app"></a>Uygulamadaki adım başlıkları ve adım yönergeleri

Warehouse Management mobil uygulamasında yer alan bir görev akışındaki her adım bir adım kimliği ile tanımlanır. Ek olarak, her adımın bir başlığı, simgesi ve yönergesi vardır. (Daha fazla bilgi için bkz. [Warehouse Management mobil uygulaması için adım simgeleri ve başlıklar atama](step-icons-titles.md).)

### <a name="step-titles"></a>Adım başlıkları

*Adım başlığı*, bir çalışanın bir adım sırasında ne yapması gerektiğini belirten kısa bir açıklamadır. Aşağıdaki resimde gösterildiği gibi ekranın üst kısmında büyük bir metin olarak görüntülenir.

![Warehouse Management mobil uygulamasında adım başlığı örneği](media/wma-step-title.png "Warehouse Management mobil uygulamasında adım başlığı örneği")

> [!TIP]
> Metin boyutunun büyük olması nedeniyle adım başlıklarını mümkün olduğunca kısa tutmaya çalışmalısınız. Aksi takdirde, metin kesilebilir. Bununla birlikte, uzun başlıklar için çalışanlar tam metni gösteren bir iletişim kutusu açmak üzere başlığı basılı tutabilirler.

### <a name="step-instructions"></a>Adım yönergeleri

*Adım yönergesi*, bir çalışanın bir adım sırasında ne yapması gerektiği hakkında daha fazla bilgi sağlayan daha uzun bir açıklamadır. Aşağıdaki resimde gösterildiği gibi bir açılır iletişim kutusunda görüntülenir.

![Warehouse Management mobil uygulamasında adım yönergesi örneği](media/wma-step-instructions.png "Warehouse Management mobil uygulamasında adım yönergesi örneği")

Adım açıldığında adım yönergesi otomatik olarak gösterilir. Çalışanlar, açılır iletişim kutusunun dışında herhangi bir yere dokunarak adım yönergesini kapatabilir. Ek olarak iletişim kutusu, çalışanların aynı görevi bir sonraki sefer gerçekleştirdiklerinde yönergenin görüntülenmesini önlemek için seçebilecekleri bir **Bir daha gösterme** onay kutusu içerir.

## <a name="load-the-default-setup"></a>Varsayılan kurulumu yükleme

Sisteminiz, *Ambar uygulaması adım yönergeleri* özelliğini ilk açtığınızda özelleştirilebilir adım başlıkları veya yönergeler içermez. Bu nedenle, yapmanız gereken ilk şey varsayılan kurulumu yüklemektir. Varsayılan kurulum, desteklenen her dilde kullanılabilir tüm adım kimlikleri için metinler sağlar. Varsayılan kurulumu yüklemek için şu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz adımları**'na gidin.
1. Eylem Bölmesinde **Varsayılan ayar oluştur**'u seçin. Sayfa, standart adımlarla doldurulur.

## <a name="customize-step-titles-and-instructions"></a>Adım başlıklarını ve yönergeleri özelleştirme

Herhangi bir sayıda dilde bir adım başlığını ve/veya yönergesini özelleştirmek için şu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz adımları**'na gidin.

    **Mobil cihaz adımları** sayfası, sisteminiz için kullanılabilen tüm adımları listeler. Her adım kimliği, herhangi bir sayıda mobil cihaz menü öğesi arasında paylaşılabilir. Birden fazla menü öğesi arasında bir adım kimliği paylaşılıyorsa tüm bu menü öğeleri için aynı başlık ve yönerge gösterilir. Ancak belirli menü öğeleri için başlığı ve yönergeyi özelleştirmek üzere geçersiz kılmalar oluşturabilirsiniz. (Daha fazla bilgi edinmek için sonraki bölüme bakın.)

    Izgara aşağıdaki sütunları içerir:

    - **Menü öğesi adı**: Bu sütunun boş olduğu satırlar, herhangi bir geçersiz kılma tanımlanmamış tüm mobil cihaz menü öğeleri için geçerli olan varsayılan adım başlığını ve yönergeyi kullanır. Bu sütunun bir menü öğesinin adına ayarlandığı satırlar yalnızca belirtilen menü öğesi için geçerli olan geçersiz kılmalara sahiptir.
    - **Adım Kimliği**: Adımın benzersiz kimliği.
    - **Giriş için başlık**: Uygulama yeni bilgi istediğinde gösterilen başlık. Genellikle, sayfadaki alanlar boştur (yani alanların önceden ayarlanmış değerleri yoktur).
    - **Onay için başlık**: Uygulama, sistemde zaten kayıtlı olan bir değerin onayını istediğinde gösterilen başlık. Genellikle, sayfadaki alanlar önceden ayarlanmış değerlere sahiptir.

1. Düzenlemek istediğiniz **Adım Kimliği** ve **Menü öğesi adı** değerlerinin birleşimini bulun ve **Adım Kimliği** sütunundaki değeri seçin. Açılan sayfa, seçilen adımın başlığı ve yönergesi için kullanılabilen tüm çevirileri listeler.
1. Metni herhangi bir dil için özelleştirmek üzere aşağıdaki adımlardan birini izleyin. Her iki seçenek de kullanılabilir diller için metinleri düzenlemenize izin verir. Ancak yalnızca ilk seçenek yeni diller için metinler eklemenize izin verirken yalnızca ikinci seçenek, seçili dilin kullanılabilir tüm menüye özel geçersiz kılmaları için metinleri görüntülemenize ve düzenlemenize izin verir.

    - Araç çubuğunda, desteklenen herhangi bir dil için metin ekleyebileceğiniz veya düzenleyebileceğiniz bir iletişim kutusu açmak üzere **Ekle**'yi seçin. **Referans dil** alanını, değerlerini görüntülemek istediğiniz dile ayarlayın. Değerler sol sütunda gösterilir. **Çevirilerin dili** alanını, eklemek veya özelleştirmek istediğiniz dile ayarlayın. Sağ sütunda, **Giriş için başlık**, **Giriş için yönerge**, **Onay için başlık** ve **Onay için yönerge** alanlarının değerlerini gerektiği şekilde düzenleyin. Daha sonra **Tamam**'ı seçin.
    - Izgarada, **Dil** alanının düzenlemek istediğiniz dile ayarlandığı satırı bulun ve seçin. Araç çubuğunda, seçilen dilin kullanılabilir tüm geçersiz kılmaları için **Bu adımın &lt;dil&gt; çevirilerini görüntüle**'yi seçerek metinleri düzenleyebileceğiniz bir iletişim kutusunu açın. İletişim kutusu, hem standart metinler (**Menü öğesi adı** alanı boş olduğunda) hem de her geçersiz kılma metni (**Menü öğesi adı** alanı, geçersiz kılmanın geçerli olduğu menü öğesinin adına ayarlandığında) için satırları olan bir ızgara içerir. **Giriş için başlık**, **Giriş için yönerge**, **Onay için başlık** ve **Onay için yönerge** alanlarının değerlerini gerektiği şekilde düzenleyin. Daha sonra **Tamam**'ı seçin.

1. Gerekli her dil için gerekli her başlığı ve yönergeyi tanımlayana kadar çalışmaya devam edin.

## <a name="add-menu-specific-overrides"></a>Menüye özel geçersiz kılmalar ekleme

Önceki bölümde belirtildiği gibi, her adım kimliği için istediğiniz sayıda menüye özel geçersiz kılma oluşturabilirsiniz. Bu özelliği, belirli bir menü öğesinin yerel iş sürecinize daha iyi uyması için yönergeyi düzenlemek ve değiştirmek üzere kullanabilirsiniz. Örneğin, satış için malzeme çekme işleminde şirketiniz, çalışanlara genellikle basılı bir belgede iş kimlikleri sağlıyorsa çalışanların bir iş kimliğini tarayarak başlaması gerektiğine dair bir ipucu sağlayabilirsiniz.

Her geçersiz kılma, belirli bir mobil cihaz menü öğesi için geçerlidir ve herhangi bir sayıda çeviri içerebilir. Menü öğesi için geçersiz kılma yoksa menü öğesi standart metinleri kullanır. Bir dil için geçersiz kılma çevirisi tanımlanmadıysa diğer diller için geçersiz kılmanın tanımlandığı menü öğeleri için bile standart metinler kullanılır.

Yeni bir geçersiz kılma oluşturmak ve yapılandırmak için şu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz adımları**'na gidin.
1. Izgarada, geçersiz kılma oluşturulacak satırı bulun ve seçin.
1. Eylem Panosunda, **Adım yapılandırması ekle**'yi seçin.
1. **Adım yapılandırması ekle** açılır iletişim kutusunda, **Menü öğesi** alanını geçersiz kılmanızın geçerli olduğu mobil cihaz menü öğesinin adına ayarlayın. Daha sonra **Tamam**'ı seçin.
1. Görüntülenen sayfa, yeni geçersiz kılma için kullanılabilen tüm metinleri gösterir. Başlangıçta yalnızca bir dil oluşturulur. Diğer tüm diller, bu dilleri buraya eklemediğiniz sürece standart metinleri kullanmaya devam eder. Metinleri düzenleyin ve önceki bölümde açıklandığı üzere gerektiği gibi yeni diller ekleyin.
