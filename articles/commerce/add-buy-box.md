---
title: Satın alma kutusu modülü
description: Bu konu satın alma kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 13d044a150651dd18c3a09c4db6a783fe8f42287
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025473"
---
# <a name="buy-box-module"></a>Satın alma kutusu modülü


[!include [banner](includes/banner.md)]

Bu konu satın alma kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Terim *satın alma kutusu* genellikle, ürün satın alma işlemi yapmak için gereken en önemli bilgileri barındıran, ürün Ayrıntıları sayfasının "manşet" alanını belirtir. (Sayfanın ilk yüklendiği sırada "manşet" olan alan görünür, böylece görmek için kullanıcıların aşağı kaydırılması gerekmez.)

Satın alma kutusu modülü, Ürün Ayrıntıları sayfasının satın alma kutusu alanında gösterilen tüm modülleri barındırmak için kullanılan özel bir konteynerdir.

Ürün Ayrıntıları sayfasının URL'SI ürün kodunu içerir. Bir satınalma kutusu modülünü işlemek için gereken tüm bilgiler bu ürün kimliğinden türetilir. Bir ürün kodu sağlanmazsa, satın alma kutusu modülü sayfada doğru olarak işlenmez. Bu nedenle, satın alma kutusu modülü yalnızca ürün içeriği olan sayfalarda kullanılabilir. Ürün bağlamı bulunmayan bir sayfada (örneğin, giriş sayfası veya pazarlama sayfası) kullanmak için, ek özelleştirmeler yapmanız gerekir.

## <a name="buy-box-module-properties-and-slots"></a>Satın alma kutusu modülü özelliklerini ve yuvaları 

Ürün Ayrıntıları sayfasında, satınalma kutusu iki bölgeye ayrılmıştır: soldaki ortam bölgesi ve sağda bulunan bir içerik bölgesi. Varsayılan olarak, ortam bölgesi sütunu genişliğinin içerik bölgesi sütunu genişliğine oranı 2:1'dir. Mobil cihazlarda iki bölge yığılır, böylece diğer bölgenin altında bir alan görünür. Temalar, sütun genişlikleri ve yığınlama derecesini özelleştirmek için kullanılabilir.

Satınalma kutusu modülü bir ürünün başlığını, açıklamasını, fiyatını ve derecelendirmelerini işler. Ayrıca müşteriler boyut, stil ve renk gibi farklı ürün özniteliklerine sahip ürün çeşitlerini da seçmenizi sağlar. Bir ürün çeşidi seçildiğinde, satınalma kutusundaki diğer Özellikler (örneğin, ürün açıklaması ve görüntüler) değişken bilgilerini yansıtacak şekilde güncelleştirilir. 

Müşterilerin satın alınacak maddelerin miktarını belirtebilmesi için bir miktar seçici sağlanır. Satın alınabilecek maksimum miktar, Tesis ayarlarında tanımlanabilir.
 
Müşteriler, satınalma kutusunda, alışveriş sepetine ürün ekleme, istek listesine ürün ekleme ve malzeme çekme yerleşimi seçme gibi eylemleri gerçekleştirebilirler. Bu eylemler bir ürün veya ürün çeşidi için gerçekleştirilebilir. Bir ürünü bir istek listesine listesine eklemek için müşterinin oturum açmış olması gerekir.

Temalar, satın alma kutusu ürün özelliklerini ve eylem denetimlerini kaldırmak veya değiştirmek için kullanılabilir. 

## <a name="module-properties"></a>Modül özellikleri

- **Başlık etiketi** – bu özellik, ürün başlığının başlık etiketini tanımlar. Satın al kutusu sayfanın en üstünde ise, erişilebilirlik standartlarını karşılamak için bu özelliğin **H1** olarak ayarlanması gerekir. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Satınalma kutusu modülünde kullanılabilen modüller

- **Ortam Galerisi** – bu modül, ürün ayrıntıları sayfasındaki bir ürünün görüntülerini sergilemesinde kullanılır. Bir ile birçok görüntüyü destekleyebilir. Küçük resimleri de destekler. Küçük resimler yatay (görüntünün altında bir satır olarak) veya dikey olarak (görüntünün yanında bir sütun olarak) düzenlenebilir. Ortam Galerisi modülü, satın alma kutusu modülündeki **ortam** yuvasına eklenebilir. Şu anda yalnızca resimleri desteklemektedir. 
- **Mağaza seçici** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir. Kullanıcıların yakındaki mağazaları bulabilmesi için bir konum girmesini sağlar. Mağaza seçici modülü Bing Haritalar Coğrafi kodlama uygulama programlama arayüzü (API) ile tümleştirilmiştir ve bu sayede konumu bir enlem ve boylama dönüştürür. Bir Bing Haritalar API anahtarı gereklidir ve Dynamics 365 Retail içinde Retail paylaşılan parametreler sayfasına eklenmelidir. Bu modül iki özelliği destekler, **Arama yarıçapı** ve **Hizmet koşulları bağlantısı**. **Arama yarıçapı** özelliği, depolar için, mil olarak arama yarıçapını tanımlar. Herhangi bir değer belirtilmezse, varsayılan arama yarıçapı olan 50 mil değeri kullanılır. Bing Haritalar veya herhangi bir harici hizmet kullanılırsa, **Hizmet koşulları bağlantısı** özelliği, hizmet koşullarına bir bağlantı sağlamak için kullanılabilir. Bing Haritalar hizmeti için bir hizmet koşulları bağlantısı gereklidir. 

## <a name="buy-box-module-settings"></a>Satın alma kutusu modülü ayarları

Satın al kutusu modülü **Site Ayarları \> Uzantılar** üzerinden yapılandırılabilecek üç ayara sahiptir:

- **Maksimum miktar** - Bu özellik, alışveriş sepetine eklenebilecek maksimum madde sayısını belirtmekte kullanılır. Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.
- **Stok denetimi** – değer **doğru** olarak ayarlandığında, yalnızca satın alma kutusu modülü stokta olduğundan emin olduktan sonra alışveriş sepetine bir madde eklenir. Bu stok denetimi hem maddenin sevk edileceği senaryolar için, hem de mağazada yer alacak senaryolar için gerçekleştirilir. Değer **yanlış** olarak ayarlandığında, bir madde alışveriş sepetine eklenmeden önce hiçbir stok denetimi yapılmaz ve sipariş yerleştirilir.
- **Stok tamponu** – Bu özellik, stok için bir tampon numarası belirtmek için kullanılır. Gerçek zamanlı olarak sürdürülür ve birçok müşteri sipariş yerleştirirken, doğru stok sayımının korunması zor olabilir. Bir stok denetimi yapıldığında, stok tampon tutardan azsa, ürün Stokta tükenmiş olarak kabul edilir. Bu nedenle, stok sayımı tam olarak eşitlenmemesi için çeşitli kanallarda hızlı şekilde satış gerçekleştiğinde, stokta olmayan bir maddenin satılması için daha az risk vardır.

## <a name="commerce-scale-unit-interaction"></a>Ticari ölçek birim etkileşimi

Satın alma kutusu modülü, ürün bilgilerini Commerce Scale Unit API'leri kullanarak alır. Ürün Ayrıntıları sayfasındaki ürün kimliği tüm bilgileri almak için kullanılır.

## <a name="add-a-buy-box-module-to-a-page"></a>Sayfaya satınalma kutusu modülü ekleme

Bir yeni sayfaya satın alma kutusu modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Satınalma kutusu parçası** olarak adlandırılan bir parça oluşturun ve buna satınalma kutusu birimi ekleyin.
1. Ortam Galerisi modülünü, satın alma kutusu modülündeki **ortam** yuvasına ekleyin.
1. Satın alma kutusu modülünde **Mağaza seçici** içinde, bir seçici modülü ekleyin.
1. Sayfayı giriş yapın ve yayımlayın.
1. Ürün Ayrıntıları sayfası için bir şablon oluşturun ve bunu **PDP şablonu** olarak adlandırın.
1. Varsayılan sayfa ekleyin.
1. Varsayılan sayfanın **ana** yuvasına bir satın alma parçası ekleyin.
1. Şablonu kaydedin, düzenlemeyi bitirin ve sonra yayınlayın.
1. **PDF sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz şablonunu kullanın.
1. Yeni sayfanın **ana** yuvasına bir satın alma parçası ekleyin.
1. Sayfayı kaydet ve önizleyin. **?productid=&lt;Product ID&gt;** sorgu dizesi parametresini önizleme sayfasının URL 'sine ekleyin. Bu şekilde, ürün bağlamı Önizleme sayfasını yüklemek ve oluşturmak için kullanılır.
1. Sayfayı kaydedin, düzenlemeyi bitirin ve yayımlayın. Ürün Ayrıntıları sayfasında bir satınalma kutusu görünmelidir.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
