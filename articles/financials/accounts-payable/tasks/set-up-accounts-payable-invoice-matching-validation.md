---
title: Borç hesapları fatura eşleştirme doğrulaması ayarlayın
description: Bu kayıtta USMF demo şirketi kullanılmaktadır.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a26a057b524f162e4b288b88e8c30f7c5db7a45
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552057"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Borç hesapları fatura eşleştirme doğrulaması ayarlayın

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu kayıtta USMF demo şirketi kullanılmaktadır. Bu adımları borç hesapları yöneticisi veya muhasebe müdürü rolü gerçekleştirir. Başlamadan önce Fatura eşleştirme yapılandırma anahtarının seçildiğinden emin olun. Tüzel kişilik navlun vb. gibi masrafları giderleri kullanarak takip ediyorsa, Masraflar yapılandırma anahtarının seçili olduğundan emin olun.  Borç hesapları faturası eşleştirme, satıcı faturasını, satın alma siparişini ve ürün alındı bilgilerini eşleştirme işlemidir. Bu belgelerin aralarındaki farklara eşleştirme uyuşmazlıkları denir. Eşleştirme uyuşmazlıkları, belirtilen toleranslarla karşılaştırılır. Bir eşleştirme uyuşmazlığı tolerans yüzdesini veya tutarını aşarsa, Satıcı faturası formunda ve Fatura eşleştirme ayrıntıları formunda eşleşme farkı simgeleri görüntülenir.

1. Borç hesapları > Kurulum > Borç hesapları parametreleri'ne gidin.
2. Fatura doğrulama sekmesine tıklayın.
3. Fatura eşleştirmesi doğrulamasını etkinleştir onay kutusunu işaretleyin veya kutunun işaretini kaldırın.
    * Fatura eşleşme uyuşmazlıkları bulunan bir faturanın deftere nakledilebilmesi için onay gerekip gerekmediğini belirtin. Bu ayar Uyarıyla izin ver yapıldıysa, fatura eşleştirmedeki bir uyuşmazlık toleransı aştığı zaman görsel bir gösterge çıkar. Ancak yine de faturayı deftere nakledebilirsiniz. Fatura eşleştirme doğrulamasıyla birlikte iş akışları kullanmak istiyorsanız, bir kereden fazla onaylamak zorunda kalmamak için, Uyuşmazlıkları olan faturayı deftere naklet alanının Uyarıyla izin ver olarak ayarlandığından emin olun.  
    * Fatura başlığı durumunu otomatik olarak güncelleştir alanında, fatura veri girişi sırasında sistem tarafından otomatik eşleştirme yapılıp yapılmayacağını belirtin. Veri giriş performansında sorunlar yaşamadığınız sürece, önerilen ayar Evet'tir. Otomatik güncelleştirmeleri devre dışı bırakmak, fatura verileri girilirken fatura eşleştirme doğrulaması atlanacağı için daha hızlı sistem performansı sağlayabilir. Bu ayar Hayır yapılırsa, veri giriş görevlisinin, fatura eşleştirme doğrulaması sonuçlarını görmek için fatura eşleştirme durumunu el ile güncelleştirmesi gerekir.  
4. Fatura toplamları eşleştirme bölümünün genişletilmiş görünümüne geçin.
5. Gerçek fatura toplamlarını beklenen toplamlarla eşleştirmek için, Fatura toplamlarını eşleştir onay kutusunu işaretleyin veya kutunun işaretini kaldırın.
    * Fatura eşleştirmesindeki bir uyuşmazlık toleransı aştığı zaman simge görüntülenip görüntülenmeyeceğini belirtin. Toleransı aşan uyuşmazlık pozitif olduğunda veya pozitif ya da negatif olduğunda simge görüntülenmesini seçebilirsiniz.  
    * Örneğin, tolerans yüzde 5 ve satınalma siparişindeki toplam fatura tutarı 100,00 olsun. Bu nedenle, faturadaki toplam fatura tutarı 105,00'i aştığı takdirde bir fiyat eşleşme simgesi görüntülenir. Büyükse veya düşükse toleransı'nı seçerseniz, simge, fatura tutarının 95,00'ten az olması durumunda da görüntülenir.  
6. Fatura toplamları tolerans yüzdesi alanına bir sayı girin.
7. Fiyat ve miktar eşleştirme bölümünün genişletilmiş görünümüne geçin.
    * Satır eşleştirme ilkesinde, birlikte çalıştığınız tüzel kişilik için varsayılan ilke olarak kullanılacak değeri seçin. "Gerekli değil", tekil fatura satırı fiyatlarının satınalma siparişi fiyatıyla veya fatura miktarlarının sevk irsaliyesi miktarlarıyla eşleştirilmesinde doğrulama yapmak gerekmediği anlamına gelir. "İki Yönlü Eşleştirme", fatura satırlarının doğrulanması gerekmediği, ancak satınalma siparişi ve tedarikçi fatura belgelerinin doğrulamaya dahil edileceği anlamına gelir. Ürün girişi, eşleştirme doğrulamalarında dikkate alınmaz. "Üç Yönlü Eşleştirme", fatura net birim fiyatının satınalma siparişi net birim fiyatıyla karşılaştırılacağı ve eşleşen ürün girişi miktarının fatura miktarıyla karşılaştırılacağı anlamına gelir.  
    * Satır eşleştirme ilkesi olarak İki yönlü eşleştirme veya Üç yönlü eşleştirme kullanıyorsanız, Madde fiyat toleransı sayfasında tüzel kişiliğiniz, maddeler ve satıcılar için fiyat toleransı yüzdeleri ayarlayabilirsiniz. Satıcı faturaları, satınalma siparişlerindeki bilgilerle karşılaştırılırken, ilgili fiyat toleransı yüzdesi aranır.  
8. Satır eşleştirme ilkesi alanında bir seçenek belirtin.
    * Bir madde, satıcı, satıcı ve madde birleşimi veya satınalma siparişi satırı için uygulanacak eşleştirmede farklı bir düzeye izin vermek için alanında Eşleştirme ilkesini geçersiz kılmaya izin ver alanında bir değer seçin. Eşleştirme ilkesi sayfasında belirli bir satıcı, madde veya satıcı ve madde birleşimi için tüzel kişilik satır eşleştirme ilkesinin üzerine yazılabilir.  
    * Faturalardaki satır maddelerinin fiyat toplamlarını eşleştirmek için, Fiyat toplamlarını eşleştir alanında bir değer seçin. Satıcı aynı satınalma siparişi satırı için birden fazla fatura gönderdiği zaman bu eşleştirme türü yararlı olur. Faturadaki her bir satırın net tutarıyla ilgili fiyat bilgilerini ve tüm bekleyen ve önceden nakledilmiş fatura satırlarını, karşılık gelen satınalma siparişi satırının net tutarıyla karşılaştırabilirsiniz.  
9. Fiyat toplamlarını eşleştir alanında bir seçenek belirtin.
10. Satınalma fiyatı toplam toleransı alanına bir sayı girin.
11. Masraf eşleştirme bölümünün genişletilmiş görünümüne geçin.
12. Gerçek masrafları satınalma siparişi bilgilerine göre beklenen masraflarla eşleştirmek için, Giderleri eşleştir onay kutusunu işaretleyin.
13. Sayfayı kapatın.

