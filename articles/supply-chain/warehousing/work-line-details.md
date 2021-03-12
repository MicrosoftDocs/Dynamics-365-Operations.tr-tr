---
title: İş satırı ayrıntıları
description: Bu konu, sisteminizdeki bireysel çalışma satırlarının kapsamlı, sıralanabilir ve filtrelenebilir listesini gösteren İş satırı ayrıntıları sayfası hakkında bilgi vermektedir.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 07dbfa301e4b242f50a9c2758b11b5ad2c31b261
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998365"
---
# <a name="work-line-details"></a>İş satırı ayrıntıları

[!include [banner](../includes/banner.md)]

**İş satırı ayrıntıları sayfası**, sisteminizdeki bireysel çalışma satırlarının kapsamlı, sıralanabilir ve filtrelenebilir listesini gösterir. Bu, planlanan ve ambarda yürütülen işlerin tam bir özetini sağlar. Tüm iş satırlarını görüntüleme ve yalnızca açık iş satırlarını görüntüleme arasında kolayca geçiş yapabilirsiniz. Her bir satır için verilen ayrıntılar iş durumunu, madde kodunu, yerleşimi, iş miktarını, yükleme kodunu ve sevkiyat kodunu içerir.

## <a name="turn-on-the-work-line-details-feature"></a>İş satırı ayrıntıları özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *İş satırı ayrıntıları*

## <a name="open-and-use-the-work-line-details-page"></a>İş satırı ayrıntıları sayfasını açma ve kullanma

İş satırı ayrıntılarının listesini görüntülemek için **Ambar Yönetimi \> İş \> İş satırı ayrıntıları**'na gidin. Buradan, aşağıdaki eylemleri gerçekleştirebilirsiniz:

- Kullanılabilir herhangi bir parametre için belirli bir değeri olan satırları aramak için **Filtre** alanını kullanın. (Kullanılabilir parametreler kılavuzda sütun olarak gösterilmeyen birçok parametre içerir.)
- Kapalı satırları göstermek veya gizlemek için **Kapalı olanı göster** onay kutusunu kullanın.
- Kılavuzda çeşitli boyut sütunlarını göstermeyi veya gizlemeyi seçebileceğiniz **Boyutların görünümü** iletişim kutusunu açmak için **Boyutları görüntüle**'yi seçin.
- Listeyi bir sütundaki değerlere göre sıralamayı veya filtreyi seçebileceğiniz bir menü açmak için o sütunun başlığını seçin.
- Bir iş satırı seçin ve ardından o iş satırına ilişkin yerleşimi değiştirebileceğiniz bir iletişim kutusu açmak için **Yerleşimi değiştir**'i seçin. Belirttiğiniz yerleşim, yerleşim yönergesinin kurulumunu geçersiz kılar.
- Bir iş satırı seçin ve ardından o iş satırının miktarını kısmen veya tamamen azaltabileceğiniz bir iletişim kutusu açmak için **İş satırını iptal et**'i seçin.
- Miktarları ayarlayın.
- Herhangi bir iş satırının arkasındaki hareketleri görüntüleyin.

## <a name="try-out-the-feature"></a>Özelliği deneyin

Bu bölüm, iş satırı ayrıntılarıyla nasıl çalışılacağını gösteren üç bölümlü bir tanıtım sunmaktadır.

### <a name="make-sample-data-available"></a>Örnek verilerini kullanılabilir hale getirme

Burada belirtilen örnek kayıtları ve değerleri kullanarak bu tanıtım üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

Bir üretim sisteminde çalışırken bu tanıtımdan kılavuz olarak da yararlanabilirsiniz. Ancak, kendi değerlerinizi değiştirmeniz gerekir ve standart tanıtım verilerinin sağladığı bazı gerekli kayıt türleri kaybolabilir.

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a>Senaryo kurulumunun yeterli kullanılabilir stok içerdiğini doğrulayın

**USMF** tanıtım verileriyle çalışıyorsanız, ilgili her malzeme çekme yerleşiminde yeterli stok olmasını sağlamak için sisteminizin ayarlandığından emin olmanız gerekir. Bu tanıtım için, aşağıdaki stoka sahip olmanız beklenir:

- **Madde M9200:** 45 beher. (veya üzeri)
- **Madde M9202:** 10 beher. (veya üzeri)

Yeterli stok olduğunu doğrulamak ve gerekli ayarlamaları yapmak için bu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Konum yönergeleri**'ne gidin ve 51 kodlu ambarda satış siparişi çekme için hangi malzeme çekme yerleşimlerinin kullanıldığını belirleyin. (Daha fazla bilgi için bkz. [İş şablonları ve yerleşim yönergeleri ile ambar işini denetleme](control-warehouse-location-directives.md).)
1. İlgili yerleşimlerdeki stok düzeylerini denetleyin.
1. Stoku gerektiği gibi düzeltin. El ile hareketler oluşturabilir, stok yenilemeyi kullanarak veya başka bir akışı uygulayarak stokta düzeltme yapabilirsiniz.

### <a name="part-1-create-picking-work"></a>Bölüm 1: Malzeme çekme işi oluşturun

İş oluşturmaya başlamadan önce, ambarınızın iş isteklerine beklendiği gibi yanıt verecek şekilde ayarlandığından emin olun.

Birkaç malzeme çekme işi oluşturmak için bu adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. **Satış siparişi oluştur** iletişim kutusunu açmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını _ABD-001_ olarak ayarlayın.
    - **Genel** hızlı sekmesinde, **Ambar** alanının ayarını _51_ yapın.

1. Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişiniz açılır. **Satış siparişi satırları** kılavuzunda yeni ve boş bir satırı olur. Bu sipariş satırında aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** _M9200_
    - **Miktar:** _20_
    - **Birim:** _ea_

1. Yeni sipariş satırını seçin ve ardından **Stok** menüsünde **Rezervasyon**'u seçerek **Rezervasyon** sayfasını açın.
1. **Rezervasyon** sayfasında, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.
1. Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin. Sistem bir sevkiyat oluşturur, bunu yeni bir yüklemeye ekler ve gerekli işi oluşturur.
1. İlk sipariş için kullandığınız aynı müşteri hesabı ve ambar için ikinci bir satış siparişi oluşturun. Aşağıdaki iki sipariş satırını bu siparişe ekleyin:

    - **Satır 1:** **Madde numarası** alanını _M9200_ olarak, **Miktar** alanını _25_ olarak ve **Birim** alanını _beher_ olarak ayarlayın.
    - **Satır 2:** **Madde numarası** alanını _M9202_ olarak, **Miktar** alanını _10_ olarak ve **Birim** alanını _beher_ olarak ayarlayın.

1. Her sipariş satırı için (bir seferde bir kez) stok rezerve etmek üzere 6'dan 8'e kadar olan adımları yineleyin ve siparişi ambara serbest bırakmak için 9. adımı yineleyin.

### <a name="part-2-change-the-location-for-a-work-line"></a>Bölüm 2: Bir iş satırı için yerleşimi değiştirin

1. **Ambar yönetimi \> İş \> İş satırı ayrıntıları**'na gidin.
1. Bu tanıtım için oluşturduğunuz iş satırlarından birini bulun ve seçin.
1. **Yeni yerleşim seç** iletişim kutusunu açmak için **Yerleşimi değiştir**'i seçin.
1. **Yeni yerleşim seç** iletişim kutusunda, **Yerleşim** alanında, iş satırı için yeni bir yerleşim seçin.
1. Değişikliğinizi uygulayıp iletişim kutusunu kapatmak için **Tamam**'ı seçin.

> [!IMPORTANT]
> Yerleşim değişikliklerini, yalnızca yeni yerleşimde yeterli stok varsa (malzeme çekme için) veya yerleşim türü doğrulama (koyma için) geçerse gönderebilirsiniz.

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a>Bölüm 3: Bir iş satırının miktarını değiştirin veya bir iş satırını iptal edin

1. **Ambar yönetimi \> İş \> İş satırı ayrıntıları**'na gidin.
1. Bu tanıtım için oluşturduğunuz iş satırlarından birini bulun ve seçin. Yalnızca iş türünün _çekme_ olduğu iş satırlarının miktarlarını iptal edebileceğinize veya değiştirebileceğinize dikkat edin.
1. **İptal edilecek miktar** iletişim kutusunu açmak için **İş satırını iptal et**'i seçin.
1. **İptal edilecek miktar** iletişim kutusunda, satır için o sırada belirtilmiş olan miktardan *düşülen* miktarı belirtmek için **Miktar** alanındaki değeri değiştirin. Varsayılan olarak, **Miktar** alanı tüm miktarı gösterir.

    - Tüm miktarı iptal ederseniz, **İş durumu** değeri _İptal edildi_ olarak değiştirilecek ancak **İş miktarı** alanı orijinal değeri göstermeye devam edecektir.
    - Miktarın yalnızca bir kısmını iptal ederseniz, **İş miktarı** alanı yeni değeri gösterecek şekilde güncelleştirilir ama **İş durumu** değeri değişmez.

1. Değişikliğinizi uygulayıp iletişim kutusunu kapatmak için **Tamam**'ı seçin.

> [!IMPORTANT]
> Bir iş satırı için yalnızca miktarın bir kısmını iptal ederseniz, yük satırından kullanılmayan miktarı da silmeniz gerekir. Aksi durumda, eksik teslimat doğru şekilde ayarlanmadıkça, yükleme satırının sevk onayı verilemez.
