---
title: "Sipariş işleme seçeneklerini ayarlamak"
description: "Bu konuda, çağrı merkezleri için siparişlerin Microsoft Dynamics 365 for Operations - Perakende&quot;yi kullanarak nasıl işleneceği hakkında bilgi verilmektedir."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eb62073fdfa50576d2c613594f3d85cbc0b322f6
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-order-processing-options"></a>Sipariş işleme seçeneklerini ayarlamak

[!include[banner](includes/banner.md)]


Bu konuda, çağrı merkezleri için siparişlerin Microsoft Dynamics 365 for Operations - Perakende'yi kullanarak nasıl işleneceği hakkında bilgi verilmektedir. 

Microsoft Dynamics 365 for Operations'ta perakende ve ticaret, çevrimiçi mağazalar, fiziksel mağazalar ve çağrı merkezleri gibi birden fazla perakende kanalını destekler. Çağrı merkezlerinde, çalışanlar telefonda Müşteri Siparişlerini alır ve satış siparişleri oluşturur. Bu konu, bir çağrı merkezi oluşturmak ve çağrı Merkezi seçeneklerini yapılandırmayı açıklar. Her bir çağrı merkezinin kendi kullanıcıları, ödeme yöntemleri, fiyat grupları, mali boyutları ve teslimat modları olabilir. Çağrı merkezi oluşturduğunuzda, bu seçenekleri yapılandırabilirsiniz. **Önemli:** çağrı merkezi iş akışlarının geçerli Dynamics AX kullanıcısı satış siparişleri oluştururken kullanılabilmesi için, kullanıcı çağrı merkezine çağrı merkezi kullanıcısı olarak atanmalıdır. **çağrı merkezi** sayfasını çağrı merkezlerine özgü özellikler gruplarını etkinleştirmek veya devre dışı bırakmak için kullanabilirsiniz. Aşağıdaki özellik grupları etkinleştirilebilir:

-   **Sipariş tamamlama** – Bu grup ödemelerle ve **satış sipariş** sayfasındaki sipariş tamamlamayla ilgili özellikleri içerir.
-   **Yönlendirilen satış** – Bu grup kaynak kodlar, komut dosyaları ve katalog talepleriyle ilgili özellikleri içerir.

Bu özellikleri çağrı Merkezi ayarlarında etkinleştirdiğinizde **satış sipariş** sayfasında çağrı merkezi ile ilişkili olan kullanıcılar için kullanılabilir. Bu özelliklerin çoğu kullanılabilmesi için önce ek kurulum gerektirir. Görüntüler ve komut dosyaları, belirli çağrı merkezi için yönlendirilmiş satış ayarının bir parçası olarak etkinleştirilir. Bu özellik etkinleştirilirse, komut dosyalarını ve ürün resimleri **satış sipariş** sayfasının bilgi kutusu bölmesinde görüntülenir. Bir ürün için ayarlanan varsayılan resim gösterilir. Komut dosyaları, bir madde, katalog, müşteri veya madde bağlamında bir katalog için yapılandırılabilir. Çağrı merkezi siparişleri belirli bir sipariş satırı için fiyatın nasıl elde edildiği hakkında ek ayrıntıları gösterebilir. Örneğin, siparişler hangi iskontoların uygulandığını görüntüler. Bu işlevselliği **Alacak hesapları** &gt; **Kurulum** &gt; **Alacak hesapları parametreleri** &gt; **Fiyatlar** &gt; **Fiyat ayrıntıları**'nda ekinleştirebilirsiniz. **Fiyat ayrıntıları** sayfasına**satış sipariş satırı** açılan listesinden erişebilirsiniz. Sipariş olay izlemeyi denetim amacıyla, siparişin yaşam döngüsü sırasında bir siparişte alınan eylemleri gözden geçirmek veya belirli bir kullanıcının eylemlerini izlemek için kullanabilirsiniz. Örneğin, eylemi bir kullanıcı her satış siparişi oluşturduğunda, bir siparişi beklemeye aldığında, bir masrafı geçersiz kıldığında veya bir sipariş satırını güncellediğinde kaydedebilirsiniz. Sipariş olaylarını, eylemleri belirli kullanıcıları, kullanıcı gruplarını veya tüm kullanıcılar için belirli bir dönemde izlemek için ayarlayabilirsiniz. O belge için Eylem Bölmesinden **sipariş olayları** sayfasını açarak bir belge üzerinde gerçekleştirilen eylemleri görüntüleyebilirsiniz. Sipariş olaylarını **Satış ve pazarlama** &gt; **Kurulum** &gt; **Olaylar** &gt; **Sipariş olayları**'nda yapılandırabilirsiniz. Zamanında bir müşterinin siparişi sevk edilemez olduğunda, bir şirket sipariş durumunu açıklamak ve müşteriye siparişi iptal etmek için bir şans vermek için müşteriye otomatik olarak bildirim e-posta iletileri gönderebilir. Gecikme belirtilen bir eşiği geçerse, sipariş otomatik olarak iptal edilebilir. En çok üç e-posta iletileri belirtilen aralıklarla gönderilebilir:

1.  **İlk iptal bildirimi** – müşteri siparişi iptal edebilir.
2.  **İkinci iptal bildirimi** – müşteri siparişi iptal edebilir.
3.  **Son iptal bildirimi** – sistem siparişi iptal eder ve müşteriye iptal bilgisi verilir.

Tek tek müşterileri ve ürünleri otomatik bildirim ve iptal işleminden muaf tutabilirsiniz. Sipariş için bir öğe eklediğinizde, bir kenar boşluğu uyarı tetiklenir. Uyarı öğenin fiyat marjı ve madde kârlılık hakkında önemli bilgiler içerir. Satış siparişi için bir öğe eklediğinizde, fiyat geçersiz kılmanın uygun olup olmadığına karar vermek için bu bilgileri kullanabilirsiniz. Örneğin, maliyetin yüzde 40 veya daha fazla üzerindeki eşiğin bir madde için kabul edilir, ancak maliyetin yüzde 20 ila 39 üzerinde olan eşiğin sorgulanabilir olduğunu belirtmek için ticari marjlar için eşikler belirleyebilirsiniz. Bu durumda, yüzde 39 ile 20 arasında eşiği olan herhangi bir öğe bir uyarı tetikler. Maliyetin yüzde 20'sinden az eşiği olan bir öğe satılamaz ve öğe fiyatı ayarlanamaz. Marj uyarılarını **Alacak hesapları** &gt; **Kurulum** &gt; **Alacak hesapları parametreleri** &gt; **Marj uyarıları**'nda yapılandırabilirsiniz. Varsayılan kurallarına göre satış vergisi atama ayarladığınızda, adres öğeleri için eşleşen bir öncelik belirleyebilirsiniz. Örneğin, bir satış vergisi grubunu ZIP kodu veya posta kodu ile eşleşmenin bir satış vergisi grubu eyaletle eşleşmeden daha yüksek bir öncelik olduğunu belirtebilirsiniz. Yeni müşteri adres kayıtları girerken, satış vergisi grubu müşterinin adresinin varsayılan kurallarla eşleşmesine ve tanımladığınız öncelik eşlemesine bağlı olarak otomatik olarak atanır. Bu işlevi **genel muhasebe parametreleri** sayfasında yapılandırabilirsiniz.




