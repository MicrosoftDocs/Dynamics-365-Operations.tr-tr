---
title: "Sahtekarlık uyarıları ayarla"
description: "Bu konu, siparişler işlendiğinde, müşteri hizmetleri temsilcilerini sahte olması olası bilgilere karşı uyarmak için kuralların nasıl ayarlanacağını açıklar. Siparişleri otomatik olarak veya el ile beklemeye almak için kullanılacak belirli kodlar tanımlayabilirsiniz."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f57cdb44d5ed3b078478cf47b74d1a79ba10323c
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fraud-alerts"></a>Sahtekarlık uyarılarını ayarlama

[!include [banner](includes/banner.md)]

Bu konuda, potansiyel sahte satış siparişlerini daha fazla incelenmek üzere beklemeye almak için nasıl ölçütler ve kurallar ayarlayacağınız açıklanmaktadır. Sahtekarlık inceleme işlevi, bir satış siparişindeki bilgilerin geçerliliğini belirlemek için kullanılır. Satış siparişindeki bilgiler kuruluşun sahtekarlık ölçütlerine ve kurallarına göre şüpheli görünüyorsa, sipariş yönetici tarafından incelenmek üzere beklemeye alınabilir.

> [!NOTE]
> Bu özellik yalnızca Retail Çağrı Merkezi kanalı satış siparişi işleme işlemlerinde kullanılabilir. 

Çağrı Merkezi kanalı tanımlandığında, **Sipariş Tamamlamayı Etkinleştir** **Evet** olarak ayarlanmalıdır. Sipariş tamamlama etkinleştirildiğinde, kullanıcılar sipariş özetini görüntüleyebilir ve siparişi tamamlamak için **Gönder**'e tıklayabilir. Kullanıcılara ayrıca satış siparişini sahtekarlık incelemesine el ile gönderme seçeneği de sunulur. Bir Çağrı Merkezi kullanıcısı tarafından girilen satıl siparişleri, gönderme sırasında sahtekarlık denetimi kuralları ve ölçütlerine göre işlenir.

Siparişin sahtekarlık incelemesi için beklemeye alınıp alınmayacağını belirlemek üzere sistemin başvuracağı iki tür sahtekarlık ölçütü bulunur:

-   **Statik kurallar**, kara listeye alınan bir telefon numarası veya daha önce sahtekarlık hareketleri için kullanıldığı bilinen e-posta adresi gibi statik bir değer kullanır. **Statik Sahtekarlık Verisi** sayfasında, sahtekarlık bilgileri el ile veya veri aktarma yoluyla eklenebilir ve puanlar sahtekarlık bilgilerine iliştirilir. Sahtekarlık denetimi açık olduğunda, girilen her satış siparişi statik veriyle karşılaştırılır. Veriler müşterinin faturalama veya sevkiyat adresinde bulunursa veya veri satış satırındaki teslimat adresinde bulunursa, tüm benzersiz eşleşmelerin puanları toplanır.  
-   **Dinamik kurallar** değişkenlerden ve bu değişkenler için tanımlanan koşullardan oluşur. Dinamik kurallarla, statik kurallarında tanımlanmayan başka ölçütler denetlenebilir. Daha karmaşık "VE/VEYA" ifadeleri, kural ölçütüyle olumlu eşleşme olup olmadığını ve satış siparişinin gönderilip gönderilmeyeceğini belirlemek üzere birden fazla koşulu değerlendirmek amacıyla kullanılabilir. Örneğin, bir kullanıcı belirli bir müşteri grubu değerine bağlı olan ve belirli bir ürünü sipariş eden müşterilerin tüm siparişlerini sahtekarlık incelemesine sokmak isterse, müşteriyi doğrulama ve ürünleri doğrulama koşulları **Kurallar** sayfasında "VE" koşuluyla birlikte tanımlanabilir. Sipariş, yalnızca her iki koşulun da doğru olması ve kurala atanan puan değerinin siparişin toplam sahtekarlık puanını Çağrı Merkezi parametrelerinde tanımlanan minimum sahtekarlık puanı üzerine çıkarması durumunda sahtekarlık incelemesine alınır.

Bir çağrı merkezi kullanıcısı bir siparişi el ile sahtekarlık inceleme kuyruğuna yerleştirebilir. Siparişi giren kullanıcı siparişi veren müşterinin şüpheli olabileceğini düşünmesi ve sipariş işlenmeden önce bir başkası tarafından geçerliliğinin incelenmesini istemesi durumunda, siparişi giren kullanıcı **Satış Siparişi Özeti** sayfasındaki **Beklemeye alınanlar** açılır menüsünden **El İle Sahtekarlık İncelemesine alma** seçeneğini seçebilir (bu, **Tamamla** sipariş işlevi çağrıldıktan sonra görüntülenir). Kullanıcıdan, inceleyecek olan kişiye bağlam sağlaması için siparişin neden sahte olabileceğini düşündüğüne ilişkin açıklama girmesi istenecektir.

El ile sahtekarlık nedeniyle tutma yoluyla veya sistematik sahtekarlık puanı hesaplaması tarafından beklemeye alınan tüm siparişler **Sipariş Tutma** sayfasında görüntülenir; bu sayfada sipariş gözden geçirilip iptal edilebilir veya işleme devam edilmesi için serbest bırakılabilir.

> [!NOTE]
> Birden fazla kuralın veya fazla karmaşık kuralların kullanılması, satış siparişleri gönderilirken sistem performansının düşmesine neden olur. Sahtekarlık uyarısı özelliği, büyük hacimli statik sahtekarlık verilerini ve çok fazla etkin kuralı işlemek üzere optimize edilmemiştir. Her kuralın, çağrı merkezi satış siparişi girişindeki gönder işlevi sırasında değerlendirildiğini unutmamanız önemlidir. Kurallar satış siparişi başlıklarında ve tüm sipariş satırlarında değerlendirilir. Ne kadar fazla ve ne kadar karmaşık kural olursa, işlem o kadar uzun sürecektir. Siparişinizde çok sayıda satır maddesi ve çok sayıda etkin kurak ile statik veri girişi varsa, sistematik veri inceleme ve doğrulama işlemi ile sahtekarlık puanını hesaplama işlevinin performans üzerindeki etkisi o kadar büyük olur.  Bu özelliği kullanan kuruluşların, kurallarda veya statik sahtekarlık ölçütünde değişiklik yapmadan önce daima sipariş gönderme işlemi süresinin kabul edilebilir olduğunu üretim ortamında test etmesi ve onaylaması gerekir.

