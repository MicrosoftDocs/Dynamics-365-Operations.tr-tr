---
title: "Merkezi ödemeleri oluşturma"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 44d51807cd6bb64ae2c4bef58d8a445417ffa3a9
ms.openlocfilehash: 815282422a6d7b8eef7d0628cf10b715449e1d1d
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-centralized-payments"></a>Merkezi ödemeleri oluşturma



Bir tüzel kişilik adına, kuruluşunuzdaki diğer tüzel kişilikler ödemeleri işlemek hazırlamak için aşağıdaki adımları izleyin. Başlamadan önce aşağıdaki Kurulum tamamlanması gerekir:

-   Tüzel kişilikler oluşturun.
-   Genel muhasebe parametreleri ve hesap planları oluşturun.
-   Borç hesapları parametreleri ve Alacak hesapları parametreleri (merkezi ödemeler kullanan modüllere bağlı olarak) oluşturun.
-   Şirketler arası muhasebeyi oluşturun.

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Merkezi ödemeler için bir organizasyon hiyerarşisi oluşturun.
Merkezi ödemeler için mutlaka bir organizasyon hiyerarşisi oluşturmanız gerekir. Aynı organizasyon hiyerarşisi, merkezi satıcı ödemelerinin ve merkezi müşteri ödemelerinin işlenmesi için kullanılır. **Not:** Merkezi ödemeler için hiyerarşi yapısı fark etmez. Hiyerarşideki herhangi bir tüzel kişilik, hiyerarşideki başka bir tüzel kişilik adına ödemeleri işleyebilir. **Organizasyon hiyerarşileri** sayfasından yeni bir organizasyon hiyerarşisi oluşturabilirsiniz.

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Merkezi ödemeler için bir şirketler arası hesap oluşturma
Mevcut tüzel kişilikteki ödeme hareketleri diğer tüzel kişiliklerdeki faturalara karşı oluşturulursa, her bir tüzel kişilik için uygun vade sonu ve vade başlangıcı hareketleri oluşturulur. İlgili bir nakit iskontosunun ve gerçekleşmiş kar veya zarar tutarlarının nakledileceği tüzel kişiliği belirtmeniz gerekir. Başlamadan önce satıcı ve müşteri ödemelerini hangi tüzel kişiliğin işleyeceğine karar verin. Bir tüzel kişilik satıcı ödemelerini işliyor, ancak başka bir tüzel kişilik müşteri ödemelerini işliyorsa her bir tüzel kişiliğe çevirmeniz gerekir. Üzerinde **Şirketlerarası muhasebe** sayfa, bir şirketlerarası ilişki kaydı adına ödemeleri işleyecek bir tüzel kişilik için seçebilirsiniz. Üzerinde **merkezi ödemeler** sekmesinde, ödeme (veya satıcı hesabının bakiyesinde diğer hareket) bir tüzel kişilik veya fatura (veya satıcı hesabı bakiyesini artıran diğer hareket) tüzel kişilik iskontoları Nakit nakletmesini isteyip seçebilirsiniz. Bu seçim **Borç hesapları parametreleri** ve **Alacak hesapları parametreleri** sayfalarındaki **Nakit iskontosu yönetimi** alanı ile birlikte çalışır. Fazla ödemeler ve kuruş farkı toleransları için ödemenin sahibi olan tüzel kişilikteki ayar kullanılır. Eksik ödemeler ve kuruş farkı toleransları için faturanın sahibi olan tüzel kişilikteki ayar kullanılır.

## <a name="map-vendor-accounts-across-legal-entities"></a>Satıcı hesaplarını tüzel kişilikler arasında eşleştirme
Bir satıcıya bir tüzel kişilikten ödeme yapıyor ve bu satıcı için faturaları diğer tüzel kişiliklerden seçmek istiyorsanız, her bir tüzel kişilikteki tüm ilgili satıcı hesaplarının aynı adres defteri kimliğini kullandığından emin olmalısınız. Faturaları birden fazla tüzel kişilikte ödeyen bir müşteriden bir ödeme alıyorsanız, her bir tüzel kişilikteki tüm ilgili müşteri hesaplarının aynı adres defteri kimliğini kullandığından emin olmalısınız.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Merkezi ödemeler için nakil profili ayarlama
Faturaları diğer tüzel kişiliklerde kapatan bir tüzel kişilikte bir ödeme oluşturduğunuzda nakil profili kimlikleri her tüzel kişilikte mutlaka aynı olmalıdır. Ödemelerin doğru şekilde oluşturulduğundan emin olmak için, faturanın sahibi her bir tüzel kişilik için, ödemenin sahibi tüzel kişilikte kullanılan nakil profillerine uygun bir nakil profili oluşurun. Geçiş yapmak için ilk tüzel kişilik fatura ve daha sonra üzerinde **Vendor posting profiles** sayfa, yeni bir deftere nakil profili oluşturun veya varolan bir deftere nakil profili düzenleyin. Tüzel kişilik faturasının nakil profili için yaptığınız seçimleri tüzel ödeme deftere nakil profili kurulumuna eşleşmesi gerekmez.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Merkezi ödemeler için ödeme yöntemleri ayarlama
Faturaları diğer tüzel kişiliklerde kapatan bir tüzel kişilikte bir ödeme oluşturduğunuzda ödeme yöntemi kimlikleri her tüzel kişilikte mutlaka aynı olmalıdır. Ödemelerin doğru şekilde oluşturulduğundan emin olmak için, faturanın sahibi her bir tüzel kişilik için, ödemenin sahibi tüzel kişilikte kullanılan ödeme yöntemlerine uygun bir ödeme yöntemi oluşurun. Faturanın sahibi ilk tüzel kişiliğe geçtikten sonra **Ödeme yöntemleri **sayfasından yeni bir ödeme yöntemi oluşturabilir veya mevcut bir ödeme yöntemini düzenleyebilirsiniz. Faturanın sahibi tüzel kişilikteki ödeme yöntemi için yaptığınız seçimlerin, ödemenin sahibi tüzel kişilikteki ödeme yönteminin kurulumuyla eşleşmesine gerek yoktur.

## <a name="set-up-default-descriptions"></a>Varsayılan tanımlar oluşturma
Şirketler arası kapanış fişleri için varsayılan tanımlar oluşturabilirsiniz. Varsayılan tanım, şirketler arası kapanış süreci sırasında vade sonu ve vade başlangıcı hareketlerine eklenir. **Varsayılan hareketler** sayfasından hem **Şirketler arası müşteri kapatma işlemleri **hem **Şirketler arası satıcı kapatma işlemleri** için bir dil seçerek ve ardından metin girerek yeni tanımlar oluşturabilirsiniz.


