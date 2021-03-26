---
title: Peşin ve nakit yönetimi hareketlerini düzenleme ve denetleme
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta peşin ve nakit yönetimi hareketlerinin nasıl düzenleneceği ve denetleneceği açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 296dbf03ed65c1994562149a2c4b8fccd9073f0d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221931"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a>Peşin ve nakit yönetimi hareketlerini düzenleme ve denetleme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'ta peşin ve nakit yönetimi hareketlerinin nasıl düzenleneceği ve denetleneceği açıklanmaktadır.

## <a name="overview"></a>Genel bakış

Dynamics 365 Commerce müşterileri hem birinci taraf satış noktası (POS) uygulamasını hem de üçüncü taraf POS uygulamalarını kullanır. Birinci taraf uygulamasının kullanıldığı durumlarda mağaza hareketleri bir toplu işlem aracılığıyla kanallardan Commerce genel merkezine çekilir. Üçüncü taraf uygulamalarının kullanıldığı durumlarda hareketler tümleştirme yoluyla Commerce genel merkezine çekilir. Her iki durumda da hareketler Commerce genel merkezine çekildikten sonra bir tutarlılık denetimi işlemi gerçekleştirilmelidir. Bu işlem, hareketler üzerinde birden fazla doğrulama çalıştırır ve yalnızca başarılı şekilde doğrulanmış hareketler Commerce genel merkezinde deftere nakledilebilmeleri için ekstreye çekilir.

Commerce hareketleri çeşitli nedenlerle doğrulamada başarısız olabilir. Tümleştirme kodundaki veya POS uygulamasındaki bir hata tutarsız verilere neden olabilir. Alternatif olarak, bir kullanıcı hatası tutarsız verilere neden olabilir. Örneğin kullanıcı, bir ürünü kanala eşitlendikten sonra silebilir veya o dönem için hareketleri deftere nakletmeden bir mali dönemi kapatabilir. Bu hareketler bayrakla işaretlenmiş ve ekstrelerden hariç tutulmuş olsalar da müşterinin günlük satışları mali öğelere nakletme sürecinde kesintiye neden olabilir. Commerce uygulamasında, doğrulamada başarısız olan hareketleri düzenlerken denetimi tüm değişiklikler için sürdürmeye devam edebilirsiniz.

## <a name="edit-transactions"></a>Hareketleri düzenleme

Commerce 10.0.5 sürümünde yalnızca satış ve iadeler gibi peşin hareketler düzenlenebilir. Müşteri siparişleri ve çevrimiçi siparişler düzenlenemez. Commerce 10.0.6 ve sonraki sürümlerinde nakit yönetimi hareketleri de düzenlenebilir.

Commerce genel merkezinde hareketleri düzenlemek için aşağıdaki adımları izleyin.

1. [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview)'ni yükleyin.
1. Commerce genel merkezinde, **Mağaza mali öğeleri** çalışma alanını açın. **Hareket doğrulama hataları** kutucuğu, bir veya daha fazla doğrulama kuralının başarısız olduğu hareket sayfasının ön filtre uygulanmış görünümünü sunar.
1. Hareket sayfasını açın, doğrulamada başarısız olan kaydı seçin, **Office Eklentisi**'ni ve ardından **Seçili hareketi düzenle**'yi seçin. Seçilen hareketin ayrıntılarını gösteren bir Excel dosyası açılır. Bu dosya aşağıdaki çalışma sayfalarını içerir:

    - **Satırlar**: Bu çalışma sayfasında hareket için başlık ile ürün satırları ve hareketle ilgili veriler bulunur.
    - **Ödemeler**: Bu çalışma sayfasında harekete ilişkin ödeme satırlarının ayrıntıları yer alır.
    - **İskontolar**: Bu çalışma sayfasında harekete ilişkin iskontoyla ilgili ayrıntılar yer alır.
    - **Vergiler**: Bu çalışma sayfasında harekete ilişkin vergiyle ilgili ayrıntılar yer alır.
    - **Masraflar**: Bu çalışma sayfasında harekete ilişkin masraflarla ilgili veriler yer alır.

1. Excel dosyasında, uygun alanları değiştirin ve ardından Dynamics Excel Eklentisi'nin yayımlama işlevini kullanarak verileri Commerce genel merkezine geri yükleyin. Veriler yayımlandıktan sonra değişiklikler sisteme yansıtılır. Yayımlama sırasında, kullanıcıların yaptığı değişiklikler için doğrulama yapılmaz.
1. Başlık düzeyindeki değişiklikler için **Perakende hareketi** başlığındaki **Denetim kaydını görüntüle**'yi seçip uygun hareket sayfasındaki ilgili bölümü veya kaydı seçerek değişikliklerle ilgili eksiksiz bir denetim kaydı görüntüleyebilirsiniz. Örneğin, satış satırlarıyla ilgili tüm değişiklikler **Satış hareketleri** sayfasında ve ödemelerle ilgili tüm değişiklikler de **Ödeme hareketleri** sayfasında gösterilir. Değişiklikler için aşağıdaki denetim ayrıntıları korunur:

    - Değiştirilme tarihi ve saati
    - Alan
    - Eski değer
    - Yeni değer
    - Değiştiren

1. Değişikliklerinizi yapıp yayınladıktan sonra bu değişikliklerin tutarlı ve geçerli olduğunu doğrulamak için **Mağaza hareketlerini doğrula** toplu işini çalıştırın.

> [!NOTE]
> Yalnızca doğrulamanın başarısız olduğu hareketleri düzenleyebilirsiniz. Doğrulamayı geçen bir hareketi düzenlemek istiyorsanız hareketin doğrulama durumunu **Hata** veya **Hiçbiri** olarak değiştirin ve ardından değişikliği yayımlayın. Ardından, hareketin başlığındaki veya diğer alt kayıtlarındaki verileri düzenleyebilir ve başlığı veya kayıtları yayımlayabilirsiniz.

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a>Ekstreye bağlı hareketleri toplu düzenleme

Commerce 10.0.6 ve sonraki sürümlerde hareketleri ekstre düzeyinde toplu düzenleme seçeneği desteklenmektedir.

Commerce genel merkezindeki bir ekstreye bağlı hareketleri toplu düzenlemek için aşağıdaki adımları izleyin.

1. **Ekstreler** sayfasını açın ve düzenlenmesi gereken hareketleri içeren ekstreyi seçin.
1. **Microsoft Office'te Aç** düğmesini seçin.
1. Düzenlenmesi gereken içeriğe bağlı olarak aşağıdaki seçeneklerden birini belirleyin:

    - **Peşin hareketleri düzenle**: Bu seçenek, ekstreye dahil edilen tüm peşin hareketleri düzenlemenize olanak tanır. Aşağıdaki Excel çalışma sayfaları kullanılabilir:

        - **Hareket**: Bu çalışma sayfası, satış hareketleriyle ilgili tüm başlık düzeyindeki bilgileri içerir.
        - **Satış hareketi**: Bu çalışma sayfası, satış hareketleriyle ilgili tüm satır düzeyindeki bilgileri içerir.
        - **Ödeme hareketleri**: Bu çalışma sayfası, satış hareketleriyle ilgili tüm ödeme satırı bilgilerini içerir.
        - **İskonto hareketleri**: Bu çalışma sayfası, satış hareketleriyle ilgili tüm iskonto satırı bilgilerini içerir.
        - **Vergi hareketleri**: Bu çalışma sayfası, satış hareketleriyle ilgili tüm vergi satırı bilgilerini içerir.
        - **Masraf hareketleri**: Bu çalışma sayfası, satış hareketleriyle ilgili tüm masraf satırı bilgilerini içerir.

    - **Nakit yönetimi hareketlerini düzenle**: Bu seçenek, ekstreye dahil edilen tüm nakit yönetimi hareketlerini düzenlemenize olanak tanır. Aşağıdaki Excel çalışma sayfaları kullanılabilir:

        - **Hareket**: Bu çalışma sayfası, nakit yönetimi hareketleriyle ilgili tüm başlık düzeyindeki bilgileri içerir.
        - **Banka ödemesi hareketleri**: Bu çalışma sayfası, tüm bankaya para nakli hareketi ayrıntılarını içerir.
        - **Kasa ödemesi hareketleri**: Bu çalışma sayfası, tüm kasaya para nakli hareketi ayrıntılarını içerir.
        - **Kasa sayımı**: Bu çalışma sayfası, tüm kasa sayımı hareketi ayrıntılarını içerir.
        - **Gelir-gider hareketi**: Bu çalışma sayfası, tüm gelir-gider hareketi satır ayrıntılarını içerir.
        - **Ödeme hareketleri**: Bu çalışma sayfası, **Fatura öde** işlemi için ödemeyle ilgili tüm bilgileri ve gelir-gider hareketini içerir.

1. Gerekli hareketleri düzenleyin.

    > [!NOTE]
    > Toplu düzenlenmiş hareketleri yayımladığınızda doğrulama yapılmaz. Tüm düzenlemelerinizin doğru olduğundan ve çalışma sayfaları arasındaki verilerin doğruluğunun korunduğundan emin olmalısınız. Örneğin, açık hareketler için mali dönemin veya stok döneminin kapatıldığı senaryoları yönetebilmek için hareket tarihini değiştirmek istiyorsanız **İş tarihi** sütunu bulunan tüm Excel çalışma sayfalarında tarihi değiştirmelisiniz. Hareketleri düzenlendikten sonra doğrulamak için **Ekstreler** sayfasındaki **Hareketleri yeniden doğrula** seçeneğini belirleyebilirsiniz. Ekstreyi deftere nakletmeden önce doğrulama işinin çalışmasının bitmesini bekleyin.

1. Toplam değer zaten oluşturulmuşsa **Toplanan hareketler** sayfasını açın ve **Satış siparişi xml'ini yeniden oluştur** seçeneğini belirleyin.

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a>Ekstreye bağlı olmayan hareketleri toplu düzenleme

Commerce 10.0.10 ve sonraki sürümleri, doğrulamada başarısız olan ancak bir ekstreye bağlı olmayan işlemleri toplu düzenleme seçeneğini destekler.

Commerce genel merkezindeki bir ekstreye bağlı olmayan hareketleri toplu düzenlemek için aşağıdaki adımları izleyin.

1. **Tüm mağazalar** sayfasını açın ve hareketlerinin düzenlenmesi gereken mağazayı seçin.
1. **Microsoft Office'te Aç** düğmesini seçin ve ardından **Peşin hareketleri düzenle**'yi seçin.
1. Gerekli hareketleri düzenleyin ve ardından yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Çevrimiçi siparişi ve zaman uyumsuz müşteri siparişi hareketlerini düzenleme ve denetleme](edit-order-trans.md)

[Perakende hareketlerinin mali boyutlarını düzenleme](edit-financial-dim.md)

[Perakende hareketlerini düzenlemek için bir Excel çalışma kitabı oluşturma](create-excel-edit.md)

[Perakende hareketlerini düzenlemek için Excel çalışma kitabına alanlar ekleme](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]