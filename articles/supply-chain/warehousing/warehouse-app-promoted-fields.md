---
title: Warehouse Management mobil uygulamasında tanıtılan alanların adımlarını yapılandırma
description: Bu makalede, Warehouse Management mobil uygulaması için görev akışlarındaki addımlar için belirli bilgileri nasıl tanıtıp vurgulayacağınız açıklanır.
author: Mirzaab
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8ecca2d00b8753a405faa8d4c67c3cbb1eef6907
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218989"
---
# <a name="configure-promoted-fields-for-steps-in-the-warehouse-management-mobile-app"></a>Warehouse Management mobil uygulamasında tanıtılan alanların adımlarını yapılandırma

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Bu makalede açıklanan özellikler yalnızca yeni Warehouse Management mobil uygulaması için geçerlidir. Artık kullanımdan kaldırılan eski ambar uygulamasını etkilemezler.

Bu makalede, Warehouse Management mobil uygulaması için görev akışlarındaki addımlar için belirli bilgileri nasıl tanıtıp vurgulayacağınız açıklanır. Bu özellik, çalışanların bir akışla çalışırken en önemli alanlar üzerinde ilgilenmesini sağlamaya yardımcı olabilir. Her bir işlemdeki her adım için, yöneticiler hangi alanların tanıtılacağını ve hangi alanların vurgulanacağını seçebilir.

## <a name="enable-promoted-fields-in-your-system"></a>Sisteminizdeki tanıtılan alanları etkinleştir

Tanıtılan alanları ayarlamadan önce, gerekli özellikleri etkinleştirmek ve Warehouse Management mobil uygulamasında gerekli alan adlarını oluşturmak için aşağıdaki yordamı tamamlamanız gerekir.

1. **Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.
1. Sistem için *Ambar uygulaması adım yönergeleri* özelliğinin açık olduğundan emin olun. Supply Chain Management sürüm 10.0.29 itibariyle, bu özellik varsayılan olarak açıktır. *Ambar uygulaması adım yönergeleri* özelliği hakkında daha fazla bilgi için , [Warehouse Management mobil uygulaması ile ilgili adım başlıklarını ve yönergeleri özelleştirme](mobile-app-titles-instructions.md) konusuna bakın. Bu özellik, *Ambar uygulaması tanıtılan alanlar* özelliği için bir önkoşuldur.
1. Özelliği, aşağıdaki şekilde etkinleştirin:

    - **Modül:** *Ambar yönetimi*
    - **Özellik adı:** *Ambar uygulaması tanıtılan alanlar*

    Bu özellik, bu makalede açıklanan özelliktir.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Ambar uygulaması alan adları**'na gidip **Varsayılan kurulum oluştur**'u seçerek Warehouse Management mobil uygulamasında alan adlarını güncelleştirin. - Daha fazla bilgi için bkz. [Ambar Yönetimi mobil uygulaması için alanları yapılandırma](configure-app-field-names-priorities-warehouse.md).
1. Warehouse Management mobil uygulamasını kullandığınız her yasal varlık (şirket) için önceki adımı yineleyin.

## <a name="configure-promoted-fields-from-a-menu-specific-override"></a>Menüye özel bir geçersiz kılmadan tanıtılan alanları konfigüre etme

Tanıtılan alanları ayarlamak için aşağıdaki yordamı kullanın.

1. İlgili menü için, [Warehouse Management mobil uygulaması için adım başlıklarını ve talimatlarını özelleştirme](mobile-app-titles-instructions.md) bölümünde açıklandığı şekilde ilgili menü ve adımlar için menüye özel geçersiz kılma oluşturun.
1. Düzenlemek istediğiniz **Adım Kimliği** ve **Menü öğesi adı** değerlerinin birleşimini bulun ve **Adım Kimliği** sütunundaki değeri seçin.
1. Görüntülenen sayfada, **Tanıtılan alanları seç** hızlı sekmesinde, araç çubuğundaki **Alanları seç**'i belirleyin.
1. **Tanıtılan alanlar** iletişim kutusunda, tanıtmak istediğiniz alanları seçin. Ayrıca, seçili alanlardan en fazla ikiye kadar vurgulayabilirsiniz. Vurgulanan alanlar, Warehouse Management mobil uygulamasında kalın olarak gösterilir. Alanları seçerken, bazı ekranların yalnızca en üstteki bir veya iki yükseltilen alanı görüntüleyecek kadar büyük olabileceğini göz önünde bulundurun. Bu ayarların nasıl kullanılacağını gösteren bir örnek için, bu makalenin ilerleyen kısımlarında yer alan senaryoya bakın.

    > [!NOTE]
    > **Kullanılabilir alanlar** listesi, menü öğesi için görünebilecek alanlarla sınırlıdır. Ancak, başka etkenler (madde oluşturma gibi) bir alanın Warehouse Management mobil uygulamasında gerçekten görünüp görünmeyeceğini belirler. Tanıtılan alanları konfigüre etmişseniz, Warehouse Management mobil uygulamasının ana sayfasında yalnızca seçilen alanlar görünür. Ancak, çalışanlar ayrıntılar sayfasına dokunarak kalan alanları görüntülemeye devam edebilir.

1. Ayarlarınızı uygulamak için **Tamam**'ı seçin. Seçtiğiniz alanlar şimdi **Tanıtılan alanları seç** hızlı sekmesinde listelenir.

## <a name="example-scenario"></a>Örnek senaryo

### <a name="enable-sample-data"></a>Örnek verileri etkinleştirme

Belirtilen örnek kayıtlarını ve değerlerini kullanarak bu senaryoda çalışmak için standart [demo verilerinin](../../fin-ops-core/fin-ops/get-started/demo-data.md) yüklü olduğu bir sistem kullanmanız gerekir. Ayrıca başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

### <a name="configure-sales-picking-with-promoted-steps-on-the-license-plate-step"></a>Lisans levhası adımındaki yükseltilen adımlarla satış çekmeyi konfigüre edin

Bu yordamda, lisans levhası adımında **Satış malzeme çekme** menü öğesi için tanıtılan ve vurgulanan alanları kuracaksınız.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz adımları**'na gidin.
1. *LicensePlateId* adlı adım kodunu bulun ve seçin.
1. Eylem Panosunda, **Adım yapılandırması ekle**'yi seçin.
1. *Satış çekme*'yi bulmak ve seçmek için açılan iletişim kutusunda **Menü öğesi** alanını kullanın.
1. **Tamam**'ı seçin.
1. Yeni oluşturduğunuz geçersiz kılma için ayrıntılar sayfası görüntülenir. **Tanıtılan alanları seç** hızlı sekmesinde, araç çubuğundaki **Alanları seç**'i belirleyin.
1. **Tanıtılan alanlar** iletişim kutusunda, tanıtmak ve vurgulamak istediğiniz alanları seçebilirsiniz. **Kullanılabilir alanlar** listesinde, aşağıdaki alanları bulun ve seçin ve bunları **Seçilen alanlar** listesine taşımak için düğmeleri kullanın:

    - Konum
    - Ürün
    - Ürün adı
    - Stok durumu

1. **Seçili alanlar** listesindeki alanların sırasını özelleştirmek için yukarı ok ve aşağı ok düğmelerini kullanın. Warehouse Management mobil uygulamasında, alanlar burada ayarladığınız sırada görünür.
1. **Yerleşim** alanını seçin ve sonra **Vurgula**'yı seçin.
1. Yapılandırmayı kaydetmek için **Tamam**'ı seçin.

### <a name="view-the-promoted-fields-in-the-warehouse-management-mobile-app"></a>Warehouse Management mobil uygulamasında tanıtılan alanları görüntüleme

Bu yordamda, Warehouse Management mobil uygulamasını açacak ve önceki yordamda vurgulanmış olan alanları görüntülemek için bu adımları inceleyeceksiniz.

1. Microsoft Dynamics 365 Supply Chain Management'ta, lisans levhası izlenen bir konumdan çekme adımı gerektirecek bir satış siparişi oluşturun. Ardından satış siparişini ambara serbest bırakın. Oluşturulan iş kimliğini not edin.
1. Warehouse Management mobil uygulamasını açın ve ambar 24'te oturum açın. (Standart demo verilerinde, kullanıcı kimliği *24* ve parola olarak *1*'i kullanarak oturum açın.)
1. **Çıkış** menüsünü seçin ve sonra **Satış malzeme çekme** menü maddesini seçin.
1. Adım 1'de oluşturulan iş kodunu girmek için ekrandaki veri giriş yönergelerini izleyin.
1. **Lisans levhası tarama** metnini içeren adımda, ayrıntılar sayfasında yaptığınız değişiklikleri görmelisiniz. Alanlar, tanıtılan alanlar için ayarladığınız sırada görünür ve **Yerleşim** alanı kalın olarak gösterilir.
