---
title: Ürün girişi ve satın alma siparişleri karşılaştırması
description: Bu makalede ürünleri teslim alınmış olarak kaydetmeye yönelik çeşitli seçenekler açıklanmıştır.
author: GalynaFedorova
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, VendPackingSlipJournalListPage, VendPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93113
ms.assetid: d4ec3e86-fce2-4546-911b-e0acf64c8887
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53925426b5df6000617b0d8cee757a551fb89c95
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904057"
---
# <a name="product-receipt-against-purchase-orders"></a>Ürün girişi ve satın alma siparişleri karşılaştırması

[!include [banner](../includes/banner.md)]

Bu makalede ürünleri teslim alınmış olarak kaydetmeye yönelik çeşitli seçenekler açıklanmıştır.

Ürün girişi satınalma siparişi (PO) satırlarının daha sonra faturalama için işlem görmesi amacıyla sipariş edilen ürünlerin alındığını kaydetme işlemidir. Bazı durumlarda, ürünler alınmadan ek bilgilerin tedarikçilerden alındığı ön kayıt işleminden geçen ürünler kaydedilir. Ürünler geldiğinde ilk olarak **Kayıtlı** şeklinde işaretlenir. Ürünler son olarak **Alındı** şeklinde işaretlenmeden önce kalite yönetimi gibi ek işlemlerden geçebilirler.

## <a name="preregistration-asn"></a>Ön kayıt (ASN)
Tedarikçiler sevk edilecek ürünler hakkındaki bilgileri paylaşabilirler. Bu durumda ürünler alınmadan önce bu bilgileri kaydetmek için ürünlerin ön kaydını yapabilirsiniz. Ürünlerin ön kaydını yaparak madde kaydı ve girişi sırasında iş tutarını düşün. Tedarikçiler Ön Sevkiyat Bildirimi (ASN) aracılığıyla ürün bilgilerini elektronik olarak sağlayabilir ve daha sonra bunlar otomatik olarak sisteme kaydedilir. ASN'deki bilgiler sevk edilecek ürünlerin miktarı ve sevk edilecekleri tarihi içerir. ASN toplu iş veya seri numaraları gibi bilgileri de içerebilir. ASN'nin kaydı **Taşıma yönetimi** modülünde yapılır.

## <a name="registration"></a>Kayıt
Ürün giriş kaydı genellikle bir ambardaki giriş noktalarında gerçekleşir. Bu el tipi bir cihaz kullanılarak veya varış günlükleri aracılığıyla gerçekleştirilir. Alternatif olarak **Satınalma siparişi** sayfasındaki **Kayıt** eylemini kullanarak ürünü el ile kaydedebilirsiniz. Her iki durumda da ürünler **Kayıtlı** olarak işaretlenmiştir. Ürünlerin henüz **Alındı** olarak işaretlenmediğini unutmayın.  

Stokta yerine koymadan önce ambarda alınan ürünler kalite incelemesinden geçebilirler. Kalite emirleri veya karantina emirleri kalite incelemesini gerçekleştirmek için kullanılabilir. Kalite emirleri kullanılıyorsa ürünleri incelenirken rezervasyon aracılığıyla geçici olarak engellemek için işlemi yapılandırabilirsiniz. Karantina emirleri kullanılıyorsa ürünler inceleme için diğer ambara taşınır. Bu ambar karantina ambarı olarak bilinir. Her iki inceleme işleminde kalite beklentilerine uyumlu olmamaları veya kalite incelemesinin bir ürün örneğinin bozucu testini içermesi nedeniyle malların bazıları hurdaya çıkabilir.

## <a name="product-receipt"></a>Ürün girişi
Çoğu zaman **Satınalma siparişleri** sayfasındaki **Ürün girişi** eylemi ürünleri PO'da **Alındı** olarak işaretlemek için kullanılır. Alındı olarak muhasebeleştirilen miktar için **Ürün girişi naklediliyor** sayfası çeşitli seçeneklere sahiptir. Örneğin **Kalite** alanını **Sipariş edilen miktar** veya **Hemen teslim alma miktarı** olarak ayarlayabilirsiniz. Alternatif olarak bir ambar varış işlemi kullanılmışsa bu alanı genellikle **Kayıtlı miktar** olarak ayarlarsınız. Eksik teslimat ve fazla teslimat gibi uyuşmazlıkları açıklamak için miktarları **Alındı** olarak işaretlenecek her bir sipariş satırı üzerinden değiştirebilirsiniz. Ürün girişi sırasında genellikle tedarikçiden alınan sevk irsaliyesine referans olacak bir ürün giriş tanımlayıcısı belirtmeniz gerekir. Bu tanımlayıcı, alınanlara ve muhasebesi yapılmış stok veya gidere göre tedarikçi sevk irsaliyelerinin kontrol edilmesi veya denetlenmesini etkinleştirdiğinden muhasebeye ihtiyaç duyar.  

PO'lar stok olarak tasarlanmamış ancak gider olarak kabul edilen ürünler için oluşturulabilir. Bu kategori ürünlerin stok modeli gruplarına göre **Stoklanmayan** olarak işaretlendiği sipariş satırlarını ve tedarik kategorilerini kullanan satırları içerir. Bu durumda, maddeler varış kaydı ve ambara giriş işleminden geçmeyebilirler. Bunun yerine, PO'da girişi doğrudan kaydetmek için **Ürün girişi** eylemi kullanılır ve giriş kaydedilen miktara değil sipariş edilen miktara göredir.  

**Yani sabit kıymet** seçeneğinin etkinleştirildiği PO satırları oluşturabilirsiniz. Bu seçenek satınalmanın stok yerine sabit bir kıymet olarak kabul edilmesi gerektiğini gösterir. Bu durumda, yapılandırılmış sabit kıymet belirleme kuralları, ürünün veya kategorinin satın alınmasının belirli eşikleri aşıp aşmadığını belirler ve bu nedenle bir kıymet olarak hesaba katılmalı ve sabit kıymet yönetiminden geçmelidir. Satınalmalar mevcut sabit kıymete yönelik de yapılabilir. Bu durumda, tutar uygun olarak ayarlanır.  

Tüm bu siparişler üzerinden birden çok siparişi ve işlem girişini seçebilirsiniz. Bu yaklaşım çok sık kullanılmaz ancak bir tedarikçinin tek bir yük halinde konsolide edilmiş sevk irsaliyeleri varsa onu kullanmak isteyebilirsiniz. Satınalmaya ürün girişi sırasında özet güncelleştirmeler yapmak için bir işlev bulunmaktadır. Özet güncelleştirmeler birden fazla PO için tedarikçiden tek bir sevk irsaliyesi nakletmenizi sağlar.  

PO'lar **Doğrudan teslim** seçeneğinin belirlendiği bir satış siparişinden oluşturulabilir. Doğrudan teslim kullanıldığında ürünler hiçbir zaman ambarınıza ulaşmaz ancak doğrudan tedarikçiden müşteriye sevk edilir. Bu durumda giriş genellikle doğrudan PO üzerinden kaydedilir. Giriş, örneğin tedarikçi ile tümleştirilen elektronik veri alışverişi (EDI) aracılığıyla otomatik olarak yapılabilir. Alternatif olarak PO, şirketlerarası bir PO ise Supply Chain Management, sevkiyat gerçekleştiğinde girişi şirketlerarası satış siparişinde otomatikleştirir. Doğrudan teslim kullanıldığında, fiziksel olarak ambara ulaşmasalar dahi ürünler hala stok olarak hesaba katılır. Bu nedenle ürün girişi PO'da kaydedildiğinde satış siparişi bir sevk irsaliyesi ile otomatik olarak güncelleştirilir, böylece stoktaki toplam değişiklik 0 (sıfır) olur. Doğrudan teslim senaryolarında ön kayda gerek duymamalısınız. Ambar yönetimi için etkinleştirilmiş ambarlar kullanıyorsanız yerine sanal bir ambar belirterek plaka kaydı gereksinimi içinde gezinebilirsiniz. Bu ambarı üründe **Doğrudan teslim ambarı** alanında belirtin. 

Ürün girişi SAS'de işlendikten sonra faturanın sipariş için işlenebildiğini göstermek için SAS durumu **Alındı** olarak ayarlanır. **Ürün girişi günlükleri** sayfasını kullanarak halihazırda alınan ürünlerle ilgili ayrıntıları inceleyebilirsiniz.  

Bu sayfaya **Satınalma siparişi** sayfasındaki **Giriş** eylem grubu üzerinden erişebilirsiniz. Günlüklerdeki bilgiler miktarlar, tarihler ve boyutlarla ilgili ayrıntıları içerir.

## <a name="additional-resources"></a>Ek kaynaklar

[Satın alma siparişine genel bakış](purchase-order-overview.md)

[Satınalma siparişleri oluşturma](purchase-order-creation.md)

[Satınalma siparişlerini onaylama](purchase-order-approval-confirmation.md)

[Satıcı faturalarına genel bakış](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]