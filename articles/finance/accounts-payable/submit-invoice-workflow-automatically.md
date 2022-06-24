---
title: Faturaları iş akışı sistemine gönderme ve ürün giriş satırlarını eşleştirme
description: Bu makalede, satıcı faturalarını iş akışı sistemine gönderme ve deftere nakledilen ürün giriş satırlarını satıcı faturalarına otomatik olarak eşleştirme işlemi açıklanmaktadır.
author: abruer
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 960a08eb5e98cac034bbd41335b616ff41bf6fd4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861632"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>Faturaları iş akışı sistemine gönderme ve ürün giriş satırlarını eşleştirme

[!include [banner](../includes/banner.md)]

Bu makalede, satıcı faturalarını iş akışı sistemine gönderme ve deftere nakledilen ürün giriş satırlarını satıcı faturalarına otomatik olarak eşleştirme işlemi açıklanmaktadır.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>İçe aktarılan satıcı faturalarını iş akışı sistemine gönderme ve deftere nakledilen ürün giriş satırlarını bekleyen satıcı fatura satırlarına eşleştirme

Temassız Borç hesapları faturalama işleminin bir parçası olarak, içe aktarılan bir faturanın iş akışı sistemine otomatik olarak gönderilmesini sağlayabilirsiniz. İçe aktarılan faturaları iş akışı sistemine gönderme işlemini **Borç hesapları parametreleri** sayfasındaki (**Borç hesapları \> Kurulum \> Borç hesapları parametreleri**) **Satıcı faturası otomasyonu** sekmesinde yapılandırabilirsiniz. İş akışına gönder işlemi arka planda, belirttiğiniz bir sıklıkta (saatlik veya günlük) çalışacaktır.

Faturaları otomatik olarak iş akışı sistemine gönderirken içe aktarılan bir faturayla başlamanız gerekir. Faturanın el ile müdahale olmadan başlangıçtan bitişe kadar işlendiğinden emin olmak için, iş akışı yapılandırmasına otomatik deftere nakil görevi eklemeniz gerekir. Satınalma siparişleri (PO'lar) ile ilgili faturalar ve PO dışı tedarik kategorisi ve stoklanmayan satırlar içeren faturalar, otomatik olarak iş akışı sistemine gönderilebilir. El ile girilen faturalar iş akışı sistemine el ile gönderilmelidir.

İş akışındaki **Gönderen** değeri, **İşlem otomasyonu** sayfasındaki **Satıcı faturalarını iş akışına gönder** arka plan görevi için girilen kullanıcı kimliğidir. Bu kullanıcı kimliğine sahip kullanıcı, gerektiğinde faturayı iş akışı sisteminden geri çekebilecektir.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Ürün girişlerini üç yönlü eşleştirme ilkesine sahip fatura satırlarıyla eşleştirme

Temassız Borç hesapları faturalama işleminin bir parçası olarak, nakledilen ürün girişleri fatura satırlarıyla otomatik olarak eşleştirilebilir. Bu görev için üç yönlü eşleştirme ilkesi tanımlanmalıdır. Bu özellik, **Satıcı fatura otomasyonu** özelliği **Özellik yönetimi** sayfasında etkinleştirilmişse kullanılabilir.

Eşleme işlemi, eşlenen ürün giriş miktarı fatura miktarına eşit oluncaya kadar çalışacaktır. Ancak, tek bir fatura satırı için birden çok ürün girişi varsa, tam miktar eşleşmesi elde etmek için işlemi birkaç kez çalıştırmanız gerekir. İşlemin başarısız olması sonucuna varmadan önce, sistemin ürün girişlerini bir fatura satırıyla eşleştirmek için kaç kez deneme yapması gerektiğini belirtebilirsiniz. İşlem, saatlik ya da günlük olarak arka planda çalışacaktır. 

Otomatik eşleştirme sürecini, faturaları iş akışı sistemine gönderme sürecinin bir parçası olarak çalıştırabilirsiniz. Alternatif olarak, bunu bağımsız bir işlem olarak da çalıştırabilirsiniz. Ürün girişlerini fatura satırlarıyla eşleştir ayarları **Borç hesapları parametreleri** sayfasının **Satıcı fatura otomasyonu** sekmesinde (**Borç hesapları \> Kurulum \> Borç hesapları parametreleri**) yapılandırılır.

Eşleşen giriş miktarının fatura miktarından az olduğu üç yönlü eşleştirme ilkesine sahip fatura satırları otomatik ürün girişine eşleştir işlemine dahil edilir.

Otomatik iş akışına gönderme işleminin parçası olmayan faturaların **Son eşleşme** durumunu görüntülemek için faturayı **Satıcı faturaları** sayfasından açın. Faturayı görüntülediğinizde, eşleşen doğrulama bilgileri güncelleştirilir. **Son eşleşme** durumu, **Fatura eşleştirmeyi doğrula** arka plan görevi kullanılarak otomatik olarak güncelleştirilebilir. **İşlem otomasyonları** sayfasının (**Sistem yönetimi\> Kurulum\> İşlem otomasyonları**) **Arka plan işlemleri** sekmesindeki **Son eşleşme** durumunu otomatik olarak güncelleştirme işlemini yapılandırabilirsiniz.

Aşağıdaki koşullardan biri karşılanırsa, fatura satırı otomatik olarak işlemeden dışlanır:

- Fatura satırının **Otomatik giriş eşleştirme durumu** değeri **Başarısız oldu** olur.
- Fatura kullanılıyor.
- Fatura iş akışı sisteminde.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
