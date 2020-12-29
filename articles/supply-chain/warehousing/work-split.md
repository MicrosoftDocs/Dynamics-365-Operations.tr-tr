---
title: İş bölme
description: Bu konu, iş bölme işlevi hakkında bilgi sağlar. Bu işlevsellik, büyük iş siparişlerini daha sonra birden çok ambar çalışanına atayabileceğiniz birkaç küçük iş siparişine bölmenize olanak tanır. Bu şekilde, aynı iş aynı anda birkaç ambar çalışanı tarafından çekilebilir.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e74b630e72d70829938f0f34efd624509b1ba7c3
ms.sourcegitcommit: 531be324bf706ca727d777720df899d6ddd3c2d7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4439772"
---
# <a name="work-split"></a>İş bölme

İş bölme işlevi, büyük iş kimliklerini (diğer bir şekilde, birkaç satırı olan iş emirleri) birden çok ambar çalışanına atayabileceğiniz birkaç küçük işe bölmenize olanak tanır. Bu şekilde, aynı iş oluşturma numarası aynı anda birkaç ambar çalışanı tarafından çekilebilir.

> [!IMPORTANT]
> Yalnızca *Açık* veya *Devam ediyor* durumundaki iş emirlerini bölebilirsiniz.

## <a name="turn-on-the-work-split-functionality"></a>İş bölme işlevini açma

İş bölme işlevini kullanamadan önce, özelliği ve sisteminizdeki ön koşul özelliğini açmanız gerekir. Yöneticiler özelliklerin durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.

İlk olarak, zaten açık değilse, *Kuruluş genelinde iş engelleme* özelliğini açın. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Kuruluş çapında işi engelleme*

> [!NOTE]
> Bu özellik etkinleştirildiğinde, özellik tüm tüzel kişilerde etkinleştirildikten sonra otomatik olarak bir veri yükseltmesi uygulanır.

Ardından, aşağıdaki şekilde listelenen *İş bölme* özelliğini açın:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *İş bölme*

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a>İş ayrıntıları ve Tüm iş sayfalarındaki geliştirmeler

*İş bölme* özelliği, **İş ayrıntılar** ve **Tüm işler** sayfalarının Eylem Bölmesi'ndeki **İş** sekmesine aşağıdaki iki düğmeyi ekler:

- **İşi böl**: Geçerli iş kimliğini ayrı çalışanlar tarafından işlenebilen birden çok küçük iş kimliğine böler.
- **İş bölme oturumunu iptal et**: İş bölme oturumunu iptal eder ve işi işlemeye hazır hale getirir.

![İşi böl ve İş bölme oturumunu iptal et düğmeleri](media/Work_split_buttons.png "İşi böl ve İş bölme oturumunu iptal et düğmeleri")

> [!IMPORTANT]
> Aşağıdaki koşullardan herhangi biri karşılanırsa **İşi böl** düğmesi kullanılamaz:
>
> - İş durumu, *Açık* veya *Devam ediyor*'dan farklıysa.
> - Kapsayıcı kimliği, iş kimliğiyle ilişkiliyse. (Fiziksel eylemler gerektirdiğinden, bir kapsayıcı sistematik olarak bölünemez.)
> - İş bir küme ile ilişkiliyse.
> - İş emri türü aşağıdaki türlerden farklıysa:
>
>    - Satış siparişleri
>    - Hammadde çekme
>    - Transfer sorunu
>
> - İş şu anda başka bir kullanıcı tarafından bölünmektedir. Zaten başka bir kullanıcı tarafından bölünmekte olan iş için bölme sayfasını açmaya çalışırsanız aşağıdaki hata iletisini alırsınız: "\#\#\#\# kimliğine sahip iş şu anda bölünmektedir. Birkaç dakika içinde tekrar deneyin. Bu iletiyi almaya devam ederseniz bir denetçiye başvurun."

Yeni bir iş engelleme nedeni, *İşi böl*, iş kimliği bölme işleminin devam etmekte olduğunu gösterir. Bir kullanıcı işi çalıştırmaya çalışırsa hem **İşi böl** sayfasında hem de ambar uygulamasında gösterilir. Engelleme nedenleri kullanıldığında, iş kimliğindeki **Engellenen dalga** alanının adı **Engellendi** olarak değiştirilir.

## <a name="initiate-a-work-split"></a>İş bölme işlemi başlatma

Özellik, kullanıcıların iş satırlarını iş kimliğinden ayırmasına olanak tanıyan yeni bir **İşi böl** sayfası ekler. Sayfa ilk açıldığında, *Açık* iş durumu olan ve bölünebilecek satırlar gösterilir. Eylem Bölmesi'nde, seçili işi işlemek için **İşi böl**'ü seçin.

İşi bölmek için aşağıdaki adımları izleyin.

1. Aşağıdaki iş sayfalarından birini açın:

    - **İş Ayrıntıları** (**Ambar yönetimi \> İş \> İş ayrıntıları**)
    - **Tüm iş** (**Ambar yönetimi \> İş \> Tüm iş**)

1. Kılavuzda, bölünecek bir iş kimliği seçin. **İş emri türü** alanı, aşağıdaki değerlerden birine ayarlanmalıdır:

    - Satış siparişleri
    - Hammadde çekme
    - Transfer sorunu

1. Eylem Bölmesinde **İş** sekmesindeki **İş** grubunda **İşi böl**'ü seçin.

    **İşi böl** sayfası görüntülenir ve açık ve bölünebilecek iş satırlarını gösterir. Varsayılan olarak, yalnızca kullanılabilir iş satırları gösterilir. İş kimliği için tüm satırları görüntülemek için (örneğin, *Yerine koyma* iş türüne sahip satırlar), kılavuzun üzerindeki **Tüm satırları göster** onay kutusunu seçin.

    Aşağıdaki ileti gösterilir: "Kullanıcılar, siz bölmeyi bitirip bu sayfayı kapatana kadar işin satırlarını işleyemez."

    Geçerli işin **İş engelleme nedeni** alanı *İşi böl* olarak ayarlanır ve iş engellenir.

    ![Engelleme nedeni](media/Blocking_reason.png "Engelleme nedeni")

1. Geçerli iş kimliğinden kaldırılacak satırları seçin ve yeni bir iş kimliği ekleyin. Aşağıdaki olaylar gerçekleşir:

    - İşi böldüğünüzde, seçili satır veya özgün iş kimliğindeki satırlar iptal edilir ve ardından yeni bir iş kimliğine kopyalanır.
    - Var olan iş şablonu yapısı ve yerine koyma konumu (ve ayrıca gelecekteki malzeme çekme/yerine koyma çiftleri) korunur. Aşağıdaki iş kimliği alanlarının değerleri özgün işten yeni işe kopyalanır:

        - Yük kodu
        - Sevkiyat Kodu
        - İş siparişi türü
        - Sipariş numarası
        - Tesis
        - Ambar
        - İş önceliği
        - İş havuzu kodu
        - Dalga kodu
        - İş oluşturma numarası

    - Aşağıdaki alanlar yeni iş kimliğine kopyalanır:

        - **İş Kimliği**: Uygun numara dizisinden yeni bir iş kimliği oluşturulur.
        - **İş durumu**: Bu alanı *Açık* konumuna ayarlayın.
        - **Kilitleyen**: Bu alan başlangıçta boş olarak ayarlanır.
        - **Hedef plaka kimliği**: Bu alan boş bırakılır.
        - **Oluşturulma tarihi ve saati**: Bu alan mevcut tarih ve saate ayarlanır.
        - **Engellenen dalga/dondurulmuş**: Bu alan, özgün iş kimliği ve yeni iş kimliği için yeniden hesaplanır.

1. Eylem bölmesinde **İşi böl**'ü seçin.

İş bölünürken, aşağıdaki ileti gösterilir: "İşlem işleniyor - İşi böl". Bu ileti görünürken, ileti kutusunda **İptal**'i seçerek işlemi iptal edebilirsiniz.

**Tüm satırları göster** onay kutusu temizlenirse bölünen ve iptal edilen satır artık kılavuzda görünmez. Onay kutusu seçilirse, bu satırın **İş durumu** alanının değerinin *İptal* olarak değiştirildiğini görürsünüz.

Yeni iş kimliğinin oluşturulduğunu belirtmek için aşağıdaki bildirim gösterilir: "\#\#\#\# işi, özgün \#\#\#\# işinden bölünerek oluşturuldu."

Özgün iş kimliğindeki diğer iş satırları (*Yerine koyma* satırları gibi) iptal edilen iş satırlarını yansıtacak şekilde gerektiği gibi ayarlanır. Örneğin, özgün iş kimliğinde 15'lik bir miktar için *Yerine Koyma* satırı varsa ve toplam miktarı 10 olan *Malzeme Çekme* satırları iptal edildiyse, özgün iş kimliğindeki yeni *Yerine Koyma* miktarı artık 5 olur.

Yeni iş hemen bir kullanıcıya atanmaz. Ancak **İş ayrıntıları** sayfasının standart işlevselliğini kullanarak gerektiğinde kullanıcıya atayabilirsiniz.

> [!IMPORTANT]
> Yalnızca iki veya daha fazla kullanılabilir iş satırı içeren iş kimliklerini bölebilirsiniz. Yalnızca bir iş satırı olduğunda **İşi böl**'ü seçerseniz aşağıdaki hata iletisini alırsınız: "En az bir iş satırı ilk işte kalmalıdır." Bu durumda, hiçbir bölme işlemi gerçekleşmez.

## <a name="finish-a-work-split"></a>İş bölmeyi bitirme

İşi bölmeyi sonlandırmak için *İşi böl* engelleme nedeninin kaldırılması gerekir. Bu adımı tamamlamanın iki yolu vardır:

- İşi bölen kullanıcı, sağ üst köşedeki **Kapat** düğmesini **(X)** seçerek **İşi böl** sayfasını kapatır. Sayfa kapatıldığında, *İşi Böl* engelleme nedeni kaldırılır. Bu işin *Engellendi* durumu yeniden hesaplanacaktır ve bu işin kalan engelleme nedeni yoksa, işin engeli kaldırılacaktır.
- Herhangi bir kullanıcı iş kimliğini açar ve Eylem Bölmesi'ndeki **İş bölme oturumunu iptal et** düğmesini seçer. *İşi böl* engelleme nedeni kaldırılır ve bu işin *Engellendi* durumu, **İşi böl** sayfası kapatıldığında yeniden hesaplanır.

*İşi böl* engelleme nedeni kaldırıldıktan sonra, **Engelledi** durumunun iş kimliğinde *Hayır* olarak ayarlanmış olması koşuluyla, iş mobil cihazda çalıştırılabilir.

## <a name="user-blocking-on-the-warehouse-app"></a>Ambar uygulamasında kullanıcı engelleme

Ambar uygulamasını, bölünmekte olan bir iş kimliğine karşı malzeme çekme işini çalıştırmak için kullanmaya çalışırsanız aşağıdaki hata iletisini alırsınız: "\#\#\#\# kimlikli iş şu anda bölünmektedir." Bu iletiyi alırsanız **İptal et**'i seçin. Daha sonra diğer işleri işlemeye devam edebilirsiniz.

## <a name="other-blocked-operations"></a>Engellenen diğer işlemler

İş satırlarını, iş stok hareketlerini veya bölünen işle ilgili stok yenileme bağlantılarını değiştiren işlemler başarısız olur ve aşağıdaki hata iletisi gösterilir: "\#\#\#\# kimlikli iş şu anda bölünmektedir."
