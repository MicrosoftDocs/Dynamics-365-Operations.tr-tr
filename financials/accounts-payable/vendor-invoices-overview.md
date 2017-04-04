---
title: "Satıcı faturaları genel bakış"
description: "Bu makalede, satıcı faturaları hakkında genel bilgiler verilmektedir. Satıcı faturaları, alınan ürün ve hizmetler için ödeme talepleridir. Satıcı faturaları, devam eden hizmetler için bir faturayı temsil edebileceği gibi, belirli madde ve hizmetler için satınalma siparişlerine de dayanabilir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: ecd32549b6067ed4c1211996e846e210f77f5013
ms.openlocfilehash: bc6fb66e9038612cc133dc89e60eb3cb75cc7943
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-invoices-overview"></a>Satıcı faturaları genel bakış

Bu makalede, satıcı faturaları hakkında genel bilgiler verilmektedir. Satıcı faturaları, alınan ürün ve hizmetler için ödeme talepleridir. Satıcı faturaları, devam eden hizmetler için bir faturayı temsil edebileceği gibi, belirli madde ve hizmetler için satınalma siparişlerine de dayanabilir. 

<a name="vendor-invoices"></a>Satıcı faturaları
---------------

Bir satınalma siparişinden bir satıcı faturası, satıcıya verilmiş satınalma siparişine göre ürünler veya hizmetler alındığında, oluşturulan bir faturadır. Satıcı faturası, bir başlık ve öğeler veya hizmetler için bir veya daha fazla satır içerir. Satıcı Fatura döngüsüne satınalma siparişine ait satıcı faturası için ürün bilgisi tamamlar. 

Bazı satıcı faturaları bir satınalma siparişine bağlı olsalar da, satıcı faturaları satınalma siparişi satırlarına karşılık gelmeyen satırlar da içerebilirler. Herhangi bir satınalma siparişi ile ilişkili olmayan satıcı faturaları da oluşturabilirsiniz. Bu satıcı faturaları bir hizmet faturası gibi fatura devam etmekte olan hizmetleri gösterebilir ve bunları eklediğinizde, bir satınalma siparişine referans göstermeniz gerekmez. 

Satıcı faturası girmek için çeşitli yollar vardır:

-   Satıcı fatura kaydına gider tahakkuk böylece bir satınalma siparişine referans yok faturaları hızla girmenizi sağlar. Satıcı Fatura onay günlüğü kullanarak, bu faturaları seçin ve tahakkuk tersine çevirmek için satıcı bakiyesi nakledin.
-   Satıcı fatura günlüğü tek adımda bir satınalma siparişine referans göstermeyen faturaları hızla girmenizi sağlar.
-   Satıcı faturası havuzu ile birlikte satıcı fatura kaydı, hızla gider tahakkuk etmek için faturaları girmenizi sağlar. Daha sonra gider hesabına karşı faturayı deftere nakletmek için ilişkili satınalma siparişlerini açabilirsiniz.
-   **Açık satıcı faturaları** ve **Bekleyen satıcı faturaları** sayfaları onaylanmış satınalma siparişlerinden satıcı faturaları oluşturmanızı sağlar.

Aşağıdaki tartışma **Açık satıcı faturaları** veya **Bekleyen satıcı faturaları** sayfalarının bir satınalma siparişinden bir satıcı faturasının nasıl oluşturulacağı hakkında daha fazla bilgi sağlar.

## <a name="understanding-invoice-line-quantities"></a>Fatura satırı miktarlarını anlama
Bir satıcı faturasını ilgili satınalma siparişinden açarsanız, fatura satırları satınalma siparişinden oluşturulur. Miktarlar varsayılan olarak ürün girişi miktarlarından alınır. Ancak, aşağıdaki varsayılan davranışların herhangi birini kullanabilirsiniz:

-   **Şimdi alma miktarı** – Kısmi sevkiyatlar için bu seçeneği kullanın. **Miktar** alanındaki varsayılan değer satınalma siparişindeki **Şimdi al** miktarı alanından alınır.
-   **Sipariş edilen miktar** – Tam sevkiyatlar için bu seçeneği kullanın. **Miktar** alanındaki varsayılan değer satınalma siparişindeki **Sipariş edilen** miktarı alanından alınır.
-   **Kayıtlı miktar** – Madde kayıt gerektiriyorsa, bu seçeneği **Madde modeli grupları** sayfasında belirtildiği gibi kullanın. **Miktar** alanındaki varsayılan değer, kaydedilen fiziksel güncelleştirme miktardır.
-   **Ürün giriş miktarı** – Sipariş için ürün girişi aldıysanız, bu seçeneği kullanın. **Miktar** alanındaki varsayılan değer,mevcut ürün girişlerinin toplam miktarından alınır.
-   **Kayıtlı miktar ve hizmetler** – Stoklu maddeleri veya stoğu olmayan maddeler için miktarlar giriş günlüklerinde kaydedilmiş ise bu seçeneği kullanın. Bu seçenek kaydettirilmiş olup olmadığını dikkate almadan hizmetleri de içerir.

Tüzel kişiliğiniz fatura eşleştirmesi kullanıyorsa, miktar eşleştirme sonuçlarını **Ürün alış irsaliyesi miktar eşleşmesi** sütununda görüntüleyebilirsiniz. Ayrıca **İnceleme** sekmesindeki **Eşleştirme ayrıntıları** menü komutunu miktar eşleştirmesinin sonuçlarını görüntülemek için kullanabilirsiniz.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Satınalma siparişinde olmayan bir satır ekleme
Satınalma siparişine satıcı faturası için değildi yeni bir satır ekleyebilirsiniz. Madde numarası veya tedarik kategori seçmelisiniz. Daha sonra satıra miktarları, fiyatları ve tutarları ekleyebilirsiniz. Satır, sadece fatura toplamları için eşleştirme ilkeleri içine eklenecektir.

## <a name="submitting-a-vendor-invoice-for-review"></a>Satıcı faturasını değerlendirilmek üzere gönderme
Kuruluşunuz, satıcı faturalarını gözden geçirme işlemini yönetmek için iş akışlarını kullanabilir. İş akışını gözden geçirmesi, faturası başlığı, fatura satırı veya her ikisi için de gerekli olabilir. İş akışı denetimleri başlığa veya satıra uygulanabilir, denetimi tıkladığınızda odağın nere olduğuna bağlı olarak. **Naklet** düğmesi yerine, bir **Gönder** düğmesi göreceksiniz ve bunu satıcı faturasını gözden geçirme sürecine göndermek için kullanabilirsiniz.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Satıcı faturalarını ürün girişlerine eşleştirmek
Satıcı faturaları için bilgi girebilir ve kaydedebilirsiniz ve fatura satırlarını ürün giriş satırlarıyla eşleştirebilirsiniz. Bir satır için kısmi miktarlar da eşleştirebilirsiniz. 

Belirli bir satınalma siparişinin tüm maddeleri henüz alınmamış olsa bile, o tarihe kadar alınmış ürün girişi satır maddelerine dayanarak bir satıcı faturası oluşturabilirsiniz. Örneğin, satıcınızın ayda bir o ay içinde sevk ettikleri tüm teslimatları içeren bir faturayı göndermesi durumunda bu seçeneği kullanabilirsiniz. Her ürün girişi, satınalma siparişindeki maddelerin kısmi veya tam teslimini temsil eder. 

Faturayı deftere naklettiğinizde, her maddenin **Fatura kalan tutarı** miktarı seçilen ürün girişinden alınan maddelerin toplamıyla güncelleştirilir. Eğer tüm maddeler için **Fatura kalanı** miktarı ve **Teslimat bakiyesi** satınalma siparişindeki miktarı 0 (sıfır) olursa, satınalma siparişinin durumu **Faturalandı** olarak değiştirilir. Eğer **Fatura kalanı** miktarı 0 değilse, satınalma siparişinin durumu değiştirilmez ve buna ek faturalar girilebilir.

Bu seçenek, satınalma siparişi için en az bir ürün girişinin deftere nakledildiğini varsayar. Satıcı faturası bu ürün girişlerine dayanır ve bunların miktarlarını yansıtır. Faturanın mali bilgileri, faturayı naklettiğinizde girilen bilgilere dayanır.

## <a name="working-with-multiple-invoices"></a>Birden çok fatura ile çalışma

Aynı anda birden çok fatura ile çalışabilir ve bunların tümünü aynı anda deftere nakledebilirsiniz. Birden çok fatura oluşturmanız gerekiyorsa, **Bekleyen satıcı faturaları** sayfasını kullanın. Birden çok satıcı faturalarını deftere nakletmeniz ve yazdırmanız gerekiyorsa, fatura onay günlüğü sayfası kullanın. Fatura onay günlüğünü kullanıyorsanız, bu satınalma siparişi için en az bir ürün girişinin deftere nakledilmesi gerekir ve bir faturanın bu satınalma siparişi için fatura kaydına nakledilmesi gerekir. Faturanın mali bilgileri, kayda nakledilmiş faturadan gelir.



