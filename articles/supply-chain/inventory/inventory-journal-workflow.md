---
title: Stok günlüğü onay iş akışları
description: Bu konuda, çeşitli fiziksel stok hareketi türleri için stok günlüklerini onaylama iş akışlarını nasıl oluşturup kullanabileceğiniz açıklanmaktadır. Stok günlüğü iş akışları yalnızca onaylanmış stok günlüklerinin hareketlere nakledilebilmesine yardımcı olur.
author: sherry-zheng
manager: tfehr
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 596182dfd7430e4d1e35ffebb795fbcf98d45e33
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247922"
---
# <a name="inventory-journal-approval-workflows"></a>Stok günlüğü onay iş akışları

[!include [banner](../includes/banner.md)]

Bu konuda, sorunlar ve girişler, stok hareketleri, ürün reçeteleri (BOM) ve fiziksel stok mutabakatı gibi çeşitli fiziksel stok hareketi türleri için stok günlüklerini onaylama iş akışlarını nasıl oluşturup kullanabileceğiniz açıklanmaktadır. Stok günlüğü iş akışları yalnızca onaylanmış stok günlüklerinin hareketlere nakledilebilmesine yardımcı olur.

> [!NOTE]
> Stok günlüğü onay iş akışları yalnızca, Stok Yönetimi modülü kullanılarak kaydedilen hareketlere uygulanır. Bunlar Ambar Yönetimi modülünden tetiklenen stok günlükleri ile çalışmaz.

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a>Stok günlüğü onay iş akışları özelliğini etkinleştirme

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Stok ve ambar yönetimi*
- **Özellik adı:** *Stok günlüğü onay iş akışı*

## <a name="create-your-inventory-journal-approval-workflows"></a>Kendi stok günlüğü onay iş akışlarınızı oluşturma

Bu özelliği ayarlamak için denetlemek istediğiniz her stok günlüğü türü için bir iş akışı oluşturmanız gerekir. Farklı stok günlüğü türlerinin farklı onay hiyerarşileri ve iş akışı adımları olabileceğinden, her stok günlüğü türü için iş akışlarını ayrı ayrı yapılandırabilirsiniz.

İş akışları sürüm kontrolünü destekler ve her birinin bir iş akışı kodu ve bir de etkin sürümü vardır. Her yeni iş akışı versiyonunu oluşturma sırasında hemen etkinleştirmeyi veya devre dışı bırakmayı seçebilirsiniz. Aynı günlük türü için farklı iş akışlarına gereksinim duyarsanız, bu günlük türü için birden fazla iş akışı oluşturun ve her birini bu türü kullanan farklı bir günlük adına atayın.

Kendi stok günlüğü onay iş akışlarınızı oluşturmak için:

1. **Stok Yönetimi \> Kurulum \> Stok yönetimi iş akışları**'na gidin.
1. Eylem Bölmesi'nde **Yeni**'yi seçin.
1. İş akışı ayarlamak istediğiniz stok günlüğü türünü seçin:
    - **Stok etiketi sayım günlüğü**
    - **Stok sahipliği değişiklik günlüğü**
    - **Stok hareketi günlüğü**
    - **Stok transfer günlüğü**
    - **Stok sayım günlüğü**
    - **Stok ürün reçetesi günlüğü**
    - **Stok düzeltme günlüğü**

    ![İş akışı oluştur iletişim kutusu](media/journal-workflow-create-workflow.png "İş akışı oluştur iletişim kutusu")

1. İş akışı düzenleyici uygulaması makinenizde başlatılır. (Bu eylemi onaylamanız istenebilir.) Gerektiğinde iş akışınızı tasarlamak için kullanın. İş akışı düzenleyicisinin kullanımıyla ilgili ayrıntılar için bkz. [İş akışı sistemine genel bakış](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).
1. İş akışı düzenleyici uygulamasını kaydedip kapattıktan sonra, bu iş akışı sürümünü etkinleştirmeyi veya devre dışı olarak tutmayı seçmeniz gerekir.

> [!NOTE]
> İş akışları, oluşturduğunuz sürümlerin listesini görüntüleyebileceğiniz ve hangisinin etkin olduğunu seçebileceğiniz anlamına gelen sürüm denetimi sağlar. Kullanılabilir sürümlerin listesini görüntülemek ve hangisini etkinleştirmek istediğinizi seçmek için **Stok yönetimi iş akışları** sayfasında listelenen bir iş akışı seçin. Eylem Bölmesinde, **İş akışı** sekmesini açın ve **Sürümler**'i seçin. Her iş akışı kodu için aynı anda yalnızca bir sürüm etkin olabilir.

## <a name="assign-approval-workflows-to-inventory-journal-names"></a>Stok günlüğü adlarına onay iş akışları atama

Sonraki adım, her stok günlüğü adına bir stok günlüğü iş akışı atamaktır. Her stok günlüğü türü için birden fazla stok günlüğü adı ayarlayabilirsiniz.

Bir stok günlüğü iş akışını bir stok günlüğü adıyla ilişkilendirmek için:

1. **Stok yönetimi \> Kurulum \>> Günlük adları \>> Stok** öğesine gidin.
1. Ayarlar sayfasını açmak için liste sütunundan bir günlük adı seçin.
1. **Genel** hızlı sekmesinde, **Onay iş akışı** seçeneğini **Evet** olarak ayarlayın. Eylemi onaylamanız istendiğinde, **Evet**'i seçin.

    ![Bir günlük adına iş akışı atama](media/journal-workflow-journal-name.png "Bir günlük adına iş akışı atama")

1. **İş akışı** açılır listesini açıp uygun iş akışını seçin. Liste, iş akışı düzenleyici uygulamasını kullanarak oluşturduğunuz her etkin iş akışını gösterir.

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a>Stok günlüğü oluşturma ve onaya gönderme

Bir stok günlüğü adını eşleşen stok günlüğü onay iş akışıyla ilişkilendirdikten sonra, bu adı kullanan yeni stok günlükleri oluşturabilir ve bu iş akışını kullanarak bu günlükleri onaya gönderebilirsiniz. Stok günlüğü iş akışında yapılandırılan onaylayanlar tarafından onaylanıncaya kadar deftere nakledilemez.

1. Gezinti bölmesinde, **Stok yönetimi \> Günlük girişleri \> Kalemler**'i genişletip bir stok günlüğü türü seçin.
1. Seçilen türde yeni bir günlük oluşturmak için **Yeni**'yi seçin.
1. **Stok günlüğü oluştur** iletişim kutusu açılır. Formu gerektiği gibi doldurun ve günlüğü kaydetmek için **Tamam**'ı seçin.
1. Günlüğü gerektiği gibi tamamlayın.
1. Kendisiyle ilişkili bir onay iş akışı olan bir stok günlüğünü oluşturduğunuzda ya da açtığınızda, Eylem Bölmesinde **İş akışı** düğmesi etkin olur. Günlüğü onaya göndermeye hazır olduğunuzda, iletişim kutusunu açmak için **İş akışı** düğmesini seçin ve sonra **Gönder**'i seçin. Onay isteği daha sonra iş akışı için yapılandırılan bildirim yöntemini kullanarak uyarılacak ilgili onaylayana yönlendirilir.

    ![Günlükleri onaya gönderme](media/journal-workflow-inventory-journal.png "Günlükleri onaya gönderme")

Onay isteğini geri çekmek için ilgili günlüğü açın, **iş akışı** düğmesini ve **Geri çek**'i seçin. Bu, iş akışını sıfırlayacaktır.

Günlüğünüz onaylandığında, deftere nakledebilirsiniz. Günlüğü deftere nakletmek için Eylem Bölmesinden **Deftere naklet**'i seçin. **Deftere naklet** düğmesi etkin değilse, günlük henüz onaylanmamış demektir.

## <a name="respond-to-an-inventory-journal-approval-request"></a>Stok günlüğü onaylama isteğini yanıtlama

Bir onaylayansanız onayınız her gerektiğinde bir ileti alırsınız (ilgili iş akışında yapılandırıldığı şekilde). Daha sonra, aşağıdakileri yaparak bir günlük onay isteğini onaylayabilir veya reddedebilirsiniz:

1. Gezinti bölmesinde, **Stok yönetimi \> Günlük girişleri \> Kalemler**'i genişletip bir stok günlüğü türü seçin.
1. İlgili günlüğü açın ve gözden geçirin.
1. Açılan iletişim kutusunu açmak için Eylem Bölmesindeki **İş akışı** düğmesini seçin. Aşağıdakilerden birini seçin:
    - **Onayla** - İsteği onaylamak için.
    - **Reddet** - isteği reddetmek için.
    - **Diğer \> Değişiklik isteği** - İstekte bulunan kişiden belirli bir şeyi değiştirmesini ve yeniden göndermesini isteyen bir ileti göndermek için.
    - **Diğer \> Devret** - Onayı başka bir kullanıcıya devretmek için.
    - **Diğer \> Geri çağır** - Onay isteğini geri çekmek için (iş akışını sıfırlar).
    - **Diğer \> İş akışı geçmişi** - Bu onay iş akışının şu ana kadarki geçmişini görüntülemek için.

## <a name="review-the-approval-history"></a>Onay geçmişini gözden geçirme

Diğer iş akışı türlerinde olduğu gibi, herhangi bir günlüğün onay iş akışı geçmişini görmek için **İş akışı geçmişi** sayfasını kullanabilirsiniz.

Bir günlüğün iş akışı geçmişini gözden geçirmek için:

1. Gezinti bölmesinde, **Stok yönetimi \> Günlük girişleri \> Kalemler**'i genişletip bir stok günlüğü türü seçin.
1. İlgili günlüğü açın.
1. Açılan iletişim kutusunu açmak için Eylem Bölmesindeki **İş akışı** düğmesini seçin. **İş akışı geçmişi**'ni seçin. Daha fazla bilgi için bkz. [İş akışı geçmişini görüntüleme](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]