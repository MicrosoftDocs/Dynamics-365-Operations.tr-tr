---
title: Perakende mağazalarındaki mali mutabakat
description: Bu makalede, Microsoft Dynamics 365 Commerce için Retail mağazalarda finansal mutabakat açıklanmaktadır.
author: anpurush
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 19c0f6edd7756a611a234a162418ef5826bd5cc2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860256"
---
# <a name="financial-reconciliation-in-retail-stores"></a>Perakende mağazalarındaki mali mutabakat

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce Sürüm 10.0.10 ve öncesi, perakende mağazalarında satış noktası işlemleri için sağlanan işlevsellik ve Mağaza yöneticilerinin günlük işlem operasyonları gerçekleştirmesini sağlayan işlevler (POS) istemcisi. Örneğin, ödeme bildirimleri, kör vardiyaları, vardiya hareketlerine mutabakat yapabilir ve vardiyaları kapatabilir. Ancak, POS 'un, finans bilgilerini Ticaret merkezinde deftere nakletmek için kullanılabilecek mali bilgileri son haline getirmeleri için bir yeteneği yoktur. Genellikle, mağaza yöneticileri bu görevin tamamlanmasından sorumludur. Bir vardiya üzerinde oturumu kapatmadan önce bilgileri gözden geçirmeleri, gerekli düzeltmeleri yapmanız ve o vardiya için toplamları sonuçlandırmak zorunda kalırlar. Son toplamların Ticaret merkezinde mali modüllerde deftere nakledilmesi gerekir.

Ek olarak, Ticaret sürüm 10.0.10 ve önceki sürümlerde, mağaza yöneticileri Ticaret merkezindeki ekstre satırları için gözden geçirebilir ve bazı ayarlamalar yapabilirler. Ancak, bu beceri sınırlıdır ve Mağaza yöneticilerinin nadiren Commerce Headquarters istemcisine erişimi vardır. Ayrıca, finansal perakende ekstresi incelemesi ve ayarlaması yalnızca, ekstreler Commerce Headquarters 'da oluşturulduğunda yapılabilir. Ancak, bu işlem genellikle gecelik bir işlemdir. Bu nedenle, Commerce headquarters finansal perakende raporları oluşturulurken, Mağaza yöneticilerinin vardiya oturumu kapatmasını beklemesi gerekir.

Commerce sürüm 10.0.11 ve sonrasında, mağaza yöneticileri POS istemcisindeki vardiyalarını gözden geçirebilir, düzeltebilir ve son haline geçirebilir. Bu veriler daha sonra Commerce Headquarters 'da finansal perakende raporları oluşturmak ve nakletmek için kullanılır.

> [!NOTE]
> Retail mağazalardaki mali mutabakatlarla ilgili işlevler yalnızca iç besleme tabanlı sipariş oluşturma açıksa çalışır. Daha fazla bilgi için bkz. [Perakende mağaza hareketleri için akış tabanlı sipariş oluşturma](trickle-feed.md).

## <a name="set-up-financial-reconciliation"></a>Finansal mutabakatı ayarlama

Mali mutabakat işlevini kullanmak için bu adımları izleyin.

1. **Özellik Yönetimi** çalışma alanında, **perakende satış tabloları-Yavaş besleme** özelliğini açın.
1. İlgili mağazanın POS işlevsellik profilinde, **Mağaza 'da finansal mutabakatı Etkinleştir** seçeneğini **Evet** olarak ayarlayın .

## <a name="more-information-about-financial-reconciliation"></a>Mali mutabakat hakkında daha fazla bilgi

Mali mutabakat işlevi açık olduğunda, Commerce Headquarters'da bulunan **perakende mağazalar** sayfasının **Ekstre/Kapanış** hızlı sekmesinde tanımlanan parametrelerden bazıları Kanal veritabanıyla eşitlenir. Aynı Hesaplama ölçütü kümesi ve perakende beyannameleri için kullanılan tutar eşikleri zorlanır.

**Vardiya kapatma** işlemi çağrıldığında, sistem, sistem tarafından hesaplanan tutarların ve bildirilen tutarların eşleştiğini doğrular. Farklılar farklıysa ve fark tanımlanan eşikleri aşıyorsa, kullanıcıya sorulur ve gerekli ayarlamaları yapabilirler.

Her ödeme için ayarlamalar yapılabilir. Bir ödeme seçildiğinde, Kullanıcı farklı hareket türleriyle ilgili toplamları görüntüleyebilir ve belirli bir hareket türü için toplamları düzenleyebilirler. Düzenleme sırasında, sistem orijinal hesaplanan tutarı ve bu hareket türü için geçersiz kılınan tutarı gösterir. Kullanıcı ayrıca, düzenleme işleminin bir parçası olarak notları yakalayabilir. Notlar, denetleme amacıyla kullanılabilir.

Kullanıcılar doğrulama istemlerini ve iletileri yoksayabilir ve SHIFT 'i kapatmaya devam edebilir. Ancak, bir Kullanıcı doğrulama istemlerini dikkate almaz, aynı sorunlar ortaya çıkar ve giriş Commerce Headquarters 'da finansal raporları deftere naklederken sabit kalır.

POS'ta **vardiya kapatma** işlemi, çevrimdışı veritabanındaki tüm hareketlerin kanal veritabanıyla eşitlenmiş olduğunu da doğrular. Herhangi bir hareket eşitlenmemişse, Kullanıcı bir uyarı iletisi alır, çünkü bu durum sistem tutarlarının hatalı şekilde hesaplanmasına neden olabilir. Bu durumda, Kullanıcı **vardiya kapatma** işlemini sonlandırabilir ve çevrimdışı hareketleri kanal veritabanıyla eşitlemeyi deneyebilir. Alternatif olarak, Kullanıcı, sistem tarafından hesaplanan tutarları eşitlenmemiş hareketler için hesaba göre el ile belirleyebilir ve böylece doğru mali numaralar kümesi sonlandırılır ve deftere nakledilir. 

Trickle besleme ekstre deftere nakli kullanıldığında, hareketlerin deftere nakledilmesi mali hareketlerin deftere nakledilmesinde ayrılırsa, eksik çevrimdışı hareketler için sistem tarafından hesaplanan tutarları ayarlamayı seçebilirsiniz. Bu şekilde, mali hareketlerin her zaman hesap yaptıklarından ve eksik hareketlerden bağımsız olarak doğru şekilde deftere nakledilmesinden emin olursunuz. Çevrimdışı hareketler, kanal veritabanı ve Commerce Headquarters ile eşitlenebilir ve daha sonra mali deftere nakillerinden ayrı olarak nakledilebilir.

Bir vardiya için mali mutabakat ayrıntıları, P-iş kullanılarak Commerce Headquarters ile eşitlenir.

Commerce Headquarters 'daki mali tablolar ekstre satırlarındaki ayrıntıları göstermek için toplamları hesaplamaz. Bunun yerine, POS istemcisindeki son tutarlar mali satış ekstrelerini oluşturmak ve nakletmek için kullanılır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]