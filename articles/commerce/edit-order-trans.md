---
title: Çevrimiçi siparişi ve zaman uyumsuz müşteri siparişi hareketlerini düzenleme ve denetleme
description: Bu makalede, Microsoft Dynamics 365 Commerce'te çevrimiçi siparişin ve zaman uyumsuz müşteri siparişi hareketlerinin nasıl düzenleneceği ve denetleneceği açıklanmaktadır.
author: josaw1
ms.date: 10/21/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: dbeeff47446c1617da44f34ae56f333717f577a1
ms.sourcegitcommit: 18b7a02c497709e8d9c7b943d82f1fcc3dafa4cd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/21/2022
ms.locfileid: "9712123"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Çevrimiçi siparişi ve zaman uyumsuz müşteri siparişi hareketlerini düzenleme ve denetleme

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te çevrimiçi siparişin ve zaman uyumsuz müşteri siparişi hareketlerinin nasıl düzenleneceği ve denetleneceği açıklanmaktadır.

## <a name="overview"></a>Genel bakış

Commerce 10.0.5 sürümünden 10.0.6 sürümüne geçiş sırasında peşin hareketleri (satışlar ve iadeler gibi) ve nakit yönetimi hareketlerini (kasa devri girişi ve ödeme kaldırma gibi) düzenlemek için destek eklendi. Commerce 10.0.7 sürümünde, çevrimiçi sipariş hareketlerini ve zaman uyumsuz müşteri siparişi hareketlerini düzenleme desteği eklendi.

## <a name="edit-and-audit-order-transactions"></a>Sipariş hareketlerini düzenleme ve denetleme

Commerce headquarters'ta sipariş hareketlerini düzenlemek ve denetlemek için aşağıdaki adımları izleyin.

1. [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview)'i yükleyin.
1. **Commerce parametreleri** sayfasında, **Müşteri siparişleri** sekmesindeki **Sipariş** hızlı sekmesinde, **Sipariş eşitleme hataları kodunu tut** için bir tutma kodu belirtin.
2. Düzenleme ve denetleme zamanlamanızla çakışacak diğer sipariş eşitleme işlerini duraklatın.
3. **Mağaza mali öğeleri** çalışma alanını açın. **Çevrimiçi sipariş eşitleme hataları** ve **Müşteri siparişi eşitleme hataları** kutucukları, perakende hareketi sayfasının önceden filtrelenmiş bir görünümünü sağlar. Her biri, karşılık gelen sipariş türü için eşitlemenin başarısız olduğu hareket kayıtlarını gösterir.
4. **Çevrimiçi sipariş eşitleme hataları** sayfasını veya **Müşteri siparişi eşitleme hataları** sayfasını açın. Eşitleme hatasının ayrıntılarını görüntülemek için bir kayıt seçin. **Eşitleme durumu** hızlı sekmesinde aşağıdaki hata ayrıntıları sağlanır:

    - Beklemedeki sipariş durumu
    - Sipariş hatası ayrıntıları
    - Değiştirilme tarihi ve saati
    - Yeniden deneme sayısı

1. Hata ayrıntılarında kaydın düzeltilmesi gerektiği belirtiliyorsa **Office Eklentisi**'ni ve ardından **Seçili hareketi düzenle**'yi seçin. Seçilen hareketin ayrıntılarını gösteren bir Excel dosyası açılır.

    - Düzenlenmekte olan hareket bir çevrimiçi sipariş hareketiyse Excel dosyası aşağıdaki çalışma sayfalarını içerir:

        - **Hareket**: Bu çalışma sayfasında harekete ilişkin başlık ayrıntıları yer alır.
        - **Satış hareketi**: Bu çalışma sayfasında harekete ilişkin satır ayrıntıları yer alır.
        - **Ödeme hareketleri**: Bu çalışma sayfasında harekete ilişkin ödeme satırlarının ayrıntıları yer alır.
        - **İskonto hareketleri**: Bu çalışma sayfasında harekete ilişkin iskontoyla ilgili ayrıntılar yer alır.
        - **Vergi hareketleri**: Bu çalışma sayfasında harekete ilişkin vergiyle ilgili ayrıntılar yer alır.
        - **Masraf hareketleri**: Bu çalışma sayfasında harekete ilişkin masraflarla ilgili veriler yer alır.

    - Düzenlenmekte olan hareket bir zaman uyumsuz müşteri siparişi hareketiyse Excel dosyası aşağıdaki çalışma sayfalarını içerir:

        - **Satırlar**: Bu çalışma sayfasında hareket için başlık ve satır ayrıntıları yer alır.
        - **Ödemeler**: Bu çalışma sayfasında harekete ilişkin ödeme satırlarının ayrıntıları yer alır.
        - **İskontolar**: Bu çalışma sayfasında harekete ilişkin iskontoyla ilgili ayrıntılar yer alır.
        - **Vergiler**: Bu çalışma sayfasında harekete ilişkin vergiyle ilgili ayrıntılar yer alır.
        - **Masraflar**: Bu çalışma sayfasında harekete ilişkin masraflarla ilgili veriler yer alır.

1. Excel dosyasında, **Beklemedeki sipariş durumu** alanına **Düzenleme** yazın ve ardından değişikliği yayımlayın. Bu şekilde, toplu iş modunda çalışan **Siparişi eşitle** işinin işlem sırasında bu kaydı atlamasını engellersiniz.
1. Excel dosyasında, uygun alanları değiştirin ve ardından Dynamics Excel Eklentisi'nin yayımlama işlevini kullanarak verileri Commerce headquarters'a geri yükleyin. Veriler yayımlandıktan sonra değişiklikler sisteme yansıtılır. Yayımlama sırasında, kullanıcıların yaptığı değişiklikler için doğrulama yapılmaz.
    > [!NOTE]
    > Düzenlemeniz gereken alanı bulamıyorsanız eksik alanı çalışma sayfasına eklemek için aşağıdaki adımları izleyin.
    >   1. Veri Bağlayıcı'da **Tasarla**'yı seçin.
    >   1. Alan eklemek istediğiniz tablonun yanındaki kalem simgesini seçin.
    >   1. **Mevcut alanlar** bölümünde alanı seçin ve ardından **Ekle** seçeneğini belirleyin.
    >   1. İhtiyacınız kadar alan ekleyin ve ardından **Güncelleştir**'i seçin.
    >   1. Güncelleştirme tamamlandığında değerleri güncelleştirmek için **Yenile**'yi seçmeniz gerekebilir.

3. Başlık düzeyindeki değişiklikler için **Perakende hareketi** başlığındaki **Denetim kaydını görüntüle**'yi seçip uygun hareket sayfasındaki ilgili bölümü veya kaydı seçerek değişikliklerle ilgili eksiksiz bir denetim kaydı görüntüleyebilirsiniz. Örneğin, satış satırlarıyla ilgili tüm değişiklikler **Satış hareketleri** sayfasında ve ödemelerle ilgili tüm değişiklikler de **Ödeme hareketleri** sayfasında gösterilir. Değişiklikler için aşağıdaki denetim ayrıntıları korunur:

    - Değiştirilme tarihi ve saati
    - Alan
    - Eski değer
    - Yeni değer
    - Değiştiren

1. Değişikliklerinizi yapıp yayımladıktan sonra eşitleme sürecini hemen başlatmak için **Siparişi eşitle**'yi seçin. Alternatif olarak, toplu işlem modunda çalışan eşitleme işleminin hareketi işlemesini bekleyebilirsiniz.

Varsayılan olarak, siparişler başarıyla eşitlendikten sonra Commerce parametrelerinde tanımlanan tutma koduna göre bir tutma durumuna alınır. Siparişlerin karşılanması veya diğer işlemler için daha fazla işlenebilmesi için siparişler üzerindeki tutma kaldırılmalıdır.

## <a name="additional-resources"></a>Ek kaynaklar

[Peşin ve nakit yönetimi hareketlerini düzenleme ve denetleme](edit-cash-trans.md)

[Perakende hareketlerinin mali boyutlarını düzenleme](edit-financial-dim.md)

[Perakende hareketlerini düzenlemek için bir Excel çalışma kitabı oluşturma](create-excel-edit.md)

[Perakende hareketlerini düzenlemek için Excel çalışma kitabına alanlar ekleme](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
