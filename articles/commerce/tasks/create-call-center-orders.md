---
title: " Çağrı merkezi siparişleri oluşturma"
description: Bu makale, bir çağrı merkezi kullanıcısının Microsoft Dynamics 365 Commerce'te bir müşteriyi aradığı, yeni bir sipariş oluşturduğu, bir ürün aradığı ve müşteriden ödeme tahsil ettiği örnek bir yordam için kılavuzluk sağlar.
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228523"
---
# <a name="create-call-center-orders"></a> Çağrı merkezi siparişleri oluşturma

[!include [banner](../includes/banner.md)]

Bu makale, bir çağrı merkezi kullanıcısının Microsoft Dynamics 365 Commerce'te bir müşteriyi aradığı, yeni bir sipariş oluşturduğu, bir ürün aradığı ve müşteriden ödeme tahsil ettiği örnek bir yordam için kılavuzluk sağlar. Yordam, USRT demo veri şirketini kullanır ve satış siparişi memurlarına yöneliktir. 

## <a name="prerequisites"></a>Ön Koşullar

Bu yordamı tamamlayan kullanıcının bir çağrı merkezi kullanıcısı olarak ayarlanması gerekir. Fabrikam yarım yıllık kataloğu, isteğe bağlı olarak, üzerinde en az bir kaynak kodla yayımlanabilir.

### <a name="add-yourself-as-a-call-center-user"></a>Kendinizi arama merkezi kullanıcısı olarak ekleme

Kendinizi bir arama merkezi kullanıcısı olarak eklemek için, aşağıdaki adımları izleyin.

1. Commerce headquarters'da, **Perakende ve Ticaret \> Kanallar \> Çağrı merkezleri \> Tüm çağrı merkezleri**'ne gidin.
1. **Kullanıcılar** alanında, **Kanal kullanıcıları**'nı seçin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Kullanıcı kimliği** alanında kullanıcı kimliğinizi girin.
1. **Ad** alanında, kullanıcı adınızı girin. Kullanıcı adı kullanıcı kimliğiyle aynı olabilir.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Perakende ve ticaret \> Kanallar \> Çağrı merkezleri \> Tüm çağrı merkezleri**'ne geri dönün.
1. Çağrı merkezinin perakende kanal kodunu seçin.
1. **Sipariş tamamlamayı etkinleştir** seçeneğinin **Evet** olarak ayarlandığını doğrulayın. Seçenek görünmüyorsa, bu adımı atlayabilirsiniz.

## <a name="complete-the-example-call-center-procedure"></a>Çağrı merkezi yordamını tamamlama

Çağrı merkezi yordamını tamamlamak için aşağıdaki adımları izleyin.

1. **Perakende ve Ticaret \> Müşteriler \> Müşteri hizmetlerine gidin**.
1. **Müşteri arama** sekmesinde, müşteri aramak için arama ölçütü girin. Bu örnek yordam için **Karen** yazın.
1. **Ara**'yı seçin. **Müşteri arama** iletişim kutusu görünür ve arama sonuçlarını listeler.
1. Müşteri hesap numarası **2001** olan **Karen Berg** için müşteri kaydını seçin ve ardından **Seç**'i seçin.
1. Eylem Bölmesinde **Yeni satış siparişi**'ni seçin.
1. Sağda, **Başlık** sekmesini seçin.
1. **Teslimat** hızlı sekmesindeki **Teslimat yöntemi** alanında **99 Standart**'ı seçin.

    ![Teslimat şeklini seçme.](../media/Select_Mode_of_Delivery.png)

1. Sağda, **Satırlar** sekmesini seçin.
1. **Satış siparişi satırları** bölümünde, yeni satış satırının yeni satırında, **Madde numarası** alanına, aranacak madde numarasını girin. Bu örnek yordamda, **81327** girin ve satış siparişine eklenecek ürünü açılır listeden seçin.
1. **Miktar** alanına satış miktarını girin.
1. **Kaynak kodu** alanında, katalog için kaynak kodunu seçin. Hiçbir etkin kaynak kodu yoksa bu adımı atlayabilirsiniz.
1. Eylem Bölmesinde, müşteri ödemesini yakalamak için **Tamamla**'yı seçin. Bu eylem, vadesi geçmiş toplam tutarı gösteren **Satış siparişi özeti** iletişim kutusunu açar. Eylem ayrıca, sevkiyat ve ambalaj gibi herhangi bir masrafın hesaplamasını da tetikler ve bunları **Satış siparişi özeti** iletişim kutusunda gösterir.

    ![Tamamla düğmesi.](../media/Complete_button.png)

1. **Satış siparişi özeti** iletişim kutusunda, **Ödemeler** hızlı sekmesinde, ödemeleri yakalamak için **Ekle**'yi seçin.

    ![Satış siparişi özeti iletişim kutusu.](../media/order_summary.png)

1. **Müşteri ödeme bilgilerini gir** iletişim kutusunda, **Ödeme yöntemi** alanında, ödeme yöntemini seçin. Bu örnek yordam için **Nakit** seçin.
1. **Ödeme tutarı** alanına, ödeme tutarını girin. Bu örnek için, **Satış siparişi özeti** iletişim kutusunda gösterilen sipariş bakiyesine eşit olan **120,00** değerini girin. Bu tutarı girerek siparişi tamamen ödenmiş olarak tamamlayabilirsiniz.
1. **Tamam**'ı seçin.
1. **Gönder**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Teslimat şekline göre işlem tabanlı e-postaları özelleştirme](../customize-email-delivery-mode.md)

[Satış noktasında teslimat şeklini değiştirme](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
