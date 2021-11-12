---
title: Otomatik satıcı faturalama işlemlerine genel bakış
description: Bu konu, otomatik bir işlem kullanmanın yararlarını ve satıcı fatura işlemeyi otomatikleştirme yeteneğini açıklamaktadır.
author: abruer
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2acb6d1c31f54a23a0b3c761e2147fa2dd43a161
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674964"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Otomatik satıcı faturalama işlemlerine genel bakış

[!include [banner](../includes/banner.md)]

Bu konu, otomatik bir işlem kullanmanın yararlarını ve satıcı fatura işlemeyi otomatikleştirme yeteneğini açıklamaktadır. Bu yetenek, Özellik yönetiminde etkinleştirilmiş olan özelliklerden oluşur. Bu özellikler, **Fatura günlüğü** veya **Fatura kayıt günlüğü** sayfasını kullanarak işlenen faturalara değil, yalnızca satıcı faturalarına uygulanır.

Çoğu durumda, kuruluşlar kağıt faturaların optik karakter tanıma (OCR) servis sağlayıcısı kullanılarak işlenmesi için üçüncü taraflarla birlikte çalışırlar. Servis sağlayıcı makine tarafından okunabilen fatura meta verilerini döndürür. Otomasyona yardımcı olmak amacıyla Borç hesapları otomasyon özellikleri, bu yapıları Borç hesaplarından kullanmanıza olanak tanır.

Bazı Borç hesapları satıcı faturalama işlemlerini otomatikleştirebilirsiniz. Bu işlemler içe aktarılan satıcı faturalarını iş akışı sistemine göndermeyi ve deftere nakledilen ürün giriş satırlarını bekleyen satıcı fatura satırlarına eşleştirmeyi içerir. Otomatik işlem, bir satıcı faturasının ilerlemesi hakkında bilgileri fatura her bir işlemde hareket ederken gösterir. Bu yetenek, Borç hesapları görevlileri ve yöneticilerinin satıcı faturalarını daha etkili şekilde işlemesine yardımcı olabilir. Ayrıca, bilginin el ile girildiği ve işlendiği durumlarda oluşabilecek hataları ve verimsizliği azaltmaya da yardımcı olur.

Otomasyon süreçleri, bu görevleri gerçekleştirmek için kullanılabilir:

- Otomatik olarak ön ödemeleri satıcı faturalarına uygula
- İçe aktarılan faturaları otomatik olarak iş akışı sistemine gönderme.
- Ürün girişlerini bekleyen satıcı faturası satırlarıyla eşleştirme.
- Satıcı faturası deftere nakledilmeden önce deftere nakil benzetimi yapma.
- İş akışı ve otomasyon geçmişini hızlı ve etkili şekilde görüntüleme.
- Satıcı faturası işlemeyi otomatikleştirme sonuçlarını görüntüleme ve inceleme.
- Birden fazla fatura için otomatik işlemeyi sürdürme.

## <a name="submit-imported-vendor-invoices-to-the-workflow-system"></a>İçe aktarılan satıcı faturalarını iş akışı sistemine gönderme

Temassız Borç hesapları faturalama işleminin bir parçası olarak, sistemin içe aktarılan bir faturayı iş akışı sistemine otomatik olarak göndermesini sağlayabilirsiniz. Bu işlem arka planda, belirttiğiniz bir sıklıkta (saatlik veya günlük) çalışacaktır. İçe aktarılan faturaları otomatik olarak iş akışı sistemine gönderme yeteneği, işleminizin içe aktarılan bir faturayla başlamasını gerektirir. Faturanın el ile müdahale olmadan başlangıçtan bitişe kadar işlendiğinden emin olmak için, iş akışı yapılandırmasına otomatik deftere nakil görevinin dahil edilmesi gerekir.


Satınalma siparişleri (PO'lar) ile ilgili faturalar ve PO dışı tedarik kategorisi ve stoklanmayan satırlar içeren faturalar, otomatik olarak iş akışı sistemine gönderilebilir. El ile girilen faturalar ve **Satıcı işbirliği faturalama** çalışma alanını kullanarak oluşturulan faturalar iş akışı sistemine el ile gönderilmelidir. Ön ödeme uygulaması işleminin içe aktarılan faturalar için el ile gerçekleştirilmesi gerekir. İçe aktarılan faturayı deftere nakletme işleminden önce veya sonra ön ödemeleri el ile uygulayabilirsiniz. **Satıcı faturaları** sayfasını kullanarak, deftere nakledilmemiş standart faturalara yapılacak ön ödemeleri el ile uygulayabilirsiniz. Deftere nakilden sonra, kapatılan ön ödeme **satıcılar** sayfasında (**Borç hesapları \> ortak \> satıcılar \> tüm satıcılar \> fatura sekmesi \> Uygula**) bu satıcıdan diğer faturalara el ile uygulanmak üzere kullanılabilir.

Otomasyon özelliği, içe aktarılan satıcı faturalarını iş akışı sistemine göndermek için şirkete özgü kurallar tanımlamanıza ve deftere nakledilen ürün giriş satırlarını bekleyen satıcı fatura satırlarına eşleştirmenize olanak sağlayan esnek bir çerçeve sağlar.

## <a name="match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Ürün girişlerini üç yönlü eşleştirme ilkesine sahip fatura satırlarıyla eşleştirme

Sistem, deftere nakledilen ürün girişlerini, üç yönlü eşleştirme ilkesi için tanımlanmış olan fatura satırlarına otomatik olarak eşleştirebilir. İşlem, eşlenen ürün giriş miktarı fatura miktarına eşit oluncaya kadar çalışacaktır. Bu işlemin bir parçası olarak, işlemin başarısız olması sonucuna varmadan önce, sistemin ürün girişlerini bir fatura satırıyla eşleştirmek için kaç kez deneme yapması gerektiğini belirtebilirsiniz. İşlem, saatlik ya da günlük olarak arka planda çalışacaktır. Otomatik eşleştirme sürecini, faturaları iş akışı sistemine gönderme sürecinin bir parçası olarak çalıştırabilirsiniz. Alternatif olarak, bunu bağımsız bir işlem olarak da çalıştırabilirsiniz.

## <a name="pre-validate-vendor-invoice-posting"></a>Satıcı faturası deftere naklini ön doğrulama

Deftere nakil benzetimi, satıcı faturalarının deftere nakil işlemi sırasında yapılan doğrulama adımlarını tamamlar, ancak hiçbir hesap güncelleştirilmez. Bu işlemi çalıştırmak için, **Bekleyen satıcı faturaları** sayfasında tek bir fatura veya birden fazla fatura seçebilirsiniz.

## <a name="enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Satıcı faturaları için iş akışı ve otomasyon geçmiş bilgilerini görüntüleme için geliştirilmiş deneyim

Satıcı faturası iş akışı geçmişiyle ilgili kolay okunabilir bir görünüm sağlanmıştır. Satıcı faturası iş akışı geçmişine doğrudan satıcı faturasından erişilebilir. Bu nedenle, bu bilgileri bulmak için daha az tıklama gerekir. Kuruluşunuz içeri aktarılan satıcı faturalarını iş akışına otomatik olarak gönderme özelliğini etkinleştirmişse içeri aktarılan faturalar için otomasyon geçmişi sunulur. Otomasyon geçmişi, geçerli işlem adımının yanı sıra zaten tamamlanmış olan adımları belirlemenize yardımcı olur. Bir adım başarısız olduğunda, sistem hatanın nedenini anlamanıza yardımcı olacak ayrıntılı bilgiler sağlar.

## <a name="analytics-and-metrics"></a>Analiz ve ölçümler

**Satıcı fatura girişi** çalışma alanı, otomatik işlem aracılığıyla bunu yapmamış olan satıcı faturalarına odaklanmanızı sağlar. Çalışma alanı üzerindeki kutucuklar iş akışı sistemine başarıyla gönderilmemiş, içe aktarılan veya ürün girişleriyle eşleştirilemeyen satıcı faturaları hakkındaki bilgileri listeler. Microsoft Power BI ölçümleri ayrıca, satıcı fatura otomasyonunun verimlilkleri için Borç hesapları yöneticilerine içgörü sunmak amacıyla da sağlanır.


## <a name="resume-automation-processing-for-multiple-invoices"></a>Birden fazla fatura için otomasyon işlemini sürdürme

İçeri aktarılan bir fatura otomatik işlem kullanılarak iş akışına başarılı bir şekilde gönderilmezse sistem bu faturayı diğer otomatik işlemlerden kaldırır. Borç hesapları memuru, otomatik işlem faturayı iş akışına yeniden göndermeden önce faturayı inceleyip düzenleyebilir. Bir hata nedeni birden çok fatura için aynı düzeltme ile çözülebiliyorsa otomatik işlemi **Otomatik fatura işlemeyi sürdür** sayfasından otomatik işlemi yeniden başlatabilirsiniz. 

## <a name="tracking-the-invoice-received-date-value"></a>Fatura alma tarih değerini izleme

**Fatura alma tarihi** değeri, şirketin faturayı satıcıdan aldığı tarihi gösterir. Faturanın Otomasyon işlemleri boyunca ilerleyişini izlemek için bir başlangıç noktası sağlar. Bu değer, satıcı faturası için içe aktarılan verilere dahil edilebilir. El ile oluşturulmuş faturalar için tarihi belirtebilirsiniz. Değer girilmezse, varsayılan olarak geçerli tarih kullanılır.


## <a name="tracking-the-imported-invoice-amount-and-imported-sales-tax-amount-values"></a>İçe aktarılan fatura tutarı ve içe aktarılan satış vergisi tutarı değerlerini izleme

Satıcı faturalarına ait **içe aktarılan fatura tutarı** ve **içe aktarılan satış vergisi tutarı** değerleri satıcı faturaları içe aktarma dosyasında sağlanabilir. Genellikle, bu değerler dışarıdaki bir sağlayıcı tarafından taranmış ve içe aktarma dosyasına dahil edilmiş bir faturadan alınır. Fatura borç hesaplarında işlenirken, sistem, değerleri fatura verilerine göre hesaplar. Fatura ancak içe aktarılan değerler hesaplanan değerlerle eşleşiyorsa deftere nakledilebilir. Eşleşen değerler, faturanın satıcıya ödenmesi gereken tutarı doğru şekilde yansıttığını gösterir. Kuruluşunuz içe aktarılan faturaların iş akışı sistemine otomatik olarak gönderilmesine izin verdiği takdirde, faturanın iş akışı sistemine gönderilebilmesi için, isteğe bağlı olarak içe aktarılan toplamların hesaplanan toplamlarla eşleşmesini zorunlu kılabilirsiniz.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Satıcı fatura otomasyonu - Birden fazla fatura için otomatik işlemeyi sürdürme
İçeri aktarılan bir fatura otomatik işlem aracılığıyla iş akışına başarılı bir şekilde gönderilmezse sistem bu faturayı diğer otomatik işlemlerden kaldırır. Borç hesapları memuru, otomatik işlem faturayı iş akışına yeniden göndermeden önce faturayı inceleyip düzenleyebilir. Bir hata nedeni birden çok fatura için aynı düzeltme ile çözülebiliyorsa otomatik işlemi **Otomatik fatura işlemeyi sürdür** sayfasından otomatik işlemi yeniden başlatabilirsiniz. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
