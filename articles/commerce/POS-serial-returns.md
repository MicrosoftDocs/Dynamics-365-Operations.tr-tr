---
title: POS'ta seri numarası denetimli ürünleri iade etme
description: Bu konu, serileştirilmiş maddeleri Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasında iade sürecinin bir parçası olarak doğrulamaya yönelik özellikleri açıklamaktadır.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 179d66e19c7fa81d587ea920b1c71468ec070177d7e7e68e45c2b58da2f9f5af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716360"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>POS'ta seri numarası denetimli ürünleri iade etme

[!include [banner](includes/banner.md)]

Bu konu, serileştirilmiş maddeleri Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasında iade sürecinin bir parçası olarak doğrulamaya yönelik özellikleri açıklamaktadır.

> [!NOTE]
> Commerce sürüm 10.0.20 ve sonrasında, **POS'ta birleşik iade işleme deneyimi** olarak adlandırılan yeni bir özellik mevcuttur. POS'ta iade siparişi işleme sırasında seri numara doğrulamasını kullanmak için bu özelliği etkinleştirmelisiniz. Bu özellik etkinleştirildiğinde sağladığı diğer özellikler hakkında bilgi için, bkz. [POS'ta iade oluşturma](POS-returns.md).
>
> Özellik, etkinleştirildikten sonra kapatılamaz.

## <a name="options-for-validating-serialized-returns"></a>Serileştirilmiş iadeleri doğrulama seçenekleri

**POS'ta birleşik iade işleme deneyimi** özelliği açık olduğunda, kuruluşlar POS üzerinden seri numarası denetimli maddelerin iadesinde doğrulama gerçekleştirebilir. Döndürülen seri numarası, satılan orijinal seri numarasından farklıysa bu özellik kullanıcıları uyarabilir. Commerce sürüm 10.0.20 ve sonrasında kullanıcıların aldığı ileti yalnızca bir uyarı iletisidir. Kullanıcılar, başlangıçta satılan seri numarasından farklı bir seri numarasına sahip bir iade işlemine devam edebilir.

**POS'ta birleşik iade işleme deneyimi** özelliği etkinleştirildikten sonra bir kuruluşun seri numarası doğrulamasını yapılandırmak için Commerce genel merkezinde **Retail ve Commerce \> Genel merkez kurulumu \> Parametreler \> Commerce parametreleri** bölümüne gidin. **Stok** sekmesinde, **Mağaza stoku işlemleri** hızlı sekmesinde, **POS iadelerinde seri numaralarını doğrulama** seçeneğini **Evet** olarak ayarlayın.

## <a name="process-returns-for-serialized-items-in-pos"></a>POS'ta serileştirilmiş maddelerin iadesi

**POS iadelerinde seri numaraların doğrulamasını etkinleştir** seçeneği **Evet** olarak ayarlanmışsa, POS aracılığıyla seri numarası denetimli bir madde iade edildiğinde kullanıcı, **İade edilebilir ürünler** sayfasındaki ayrıntılar bölmesine iade satırına ait seri numarasını girebilir. Girilen seri numarası, satış hareketi için satılan orijinal seri numarasıyla eşleşmiyorsa, kullanıcı bir uyarı iletisi alır. Ancak, uygulama kullanıcının iadeyi deftere nakletmeye devam etmesini engellemez.

> [!NOTE]
> POS, yalnızca orijinal sipariş edilen miktarın birden fazla olmadığı iade satırlarında seri numaralarının doğrulanmasını destekler. Orijinal satış siparişi satırı, POS dışı bir kanalda oluşturulmuşsa ve belirli bir satış satırındaki serileştirilmiş madde için sipariş edilen miktar birden büyükse, madde POS üzerinden doğru şekilde iade edilemez.

## <a name="additional-resources"></a>Ek kaynaklar

[POS'ta iade oluşturma](POS-returns.md)
