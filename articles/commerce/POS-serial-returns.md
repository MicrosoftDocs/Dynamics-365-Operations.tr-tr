---
title: POS'ta seri numarası denetimli ürünleri iade etme
description: Bu makale, serileştirilmiş maddeleri Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasında iade sürecinin bir parçası olarak doğrulamaya yönelik özellikleri açıklamaktadır.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9fa7e47b6d650370afe4b98d7eca01253bd1bc36
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268487"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>POS'ta seri numarası denetimli ürünleri iade etme

[!include [banner](includes/banner.md)]

Bu makale, serileştirilmiş maddeleri Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasında iade sürecinin bir parçası olarak doğrulamaya yönelik özellikleri açıklamaktadır.

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
