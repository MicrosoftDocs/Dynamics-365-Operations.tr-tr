---
title: "Microsoft Dynamics 365 for Operations uygulaması için satıcı işbirliği mobil çalışma alanı"
description: "Satıcı işbirliği mobil çalışma alanıyla, tedarikçileriniz onay için onlara gönderilen satınalma siparişlerini güncelleyebilir, yeni ve güncellenmiş satınalma siparişleri ve kişilerle ilgili bilgileri görüntüleyebilir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d5157e6f4b10b6158aa08279a9f68dae676f5666
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Microsoft Dynamics 365 for Operations uygulaması için satıcı işbirliği mobil çalışma alanı

[!include[banner](../includes/banner.md)]


Satıcı işbirliği mobil çalışma alanıyla, tedarikçileriniz onay için onlara gönderilen satınalma siparişlerini güncelleyebilir, yeni ve güncellenmiş satınalma siparişleri ve kişilerle ilgili bilgileri görüntüleyebilir.

<a name="prerequisites"></a>Önkoşullar
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Önkoşul</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 for Operations mobil platformu hakkında bilgi alın</td>
<td><a href="https://ax.help.dynamics.com/en/wiki/mobile-development-handbook/">Dynamics 365 for Operations mobil platformu</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Microsoft Dynamics 365 for Operations sürüm 1611 ve Microsoft Dynamics for Operations platform güncelleştirmesi 3 (Kasım 2016) güncelleştirmelerine sahip bir ortam kullandığınıza emin olun.</td>
</tr>
<tr class="odd">
<td><span style="color: #000000">Dynamics 365 for Operations yüklü mobil cihaz</span></td>
<td><span style="color: #000000">Dynamics 365 for Operations uygulamasını mobil uygulama mağazanızdan indirin.</span></td>
</tr>
<tr class="even">
<td>Düzeltme KB 4013633</td>
<td>Dynamics 365 for Operations içerisinde sağlanan çalışma alanlarını etkinleştirmek için düzeltmeyi yükleyin.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000"><span style="color: #000000">Düzeltme KB 3216943</span> </span></td>
<td>Satıcı işbirliği mobil çalışma alanını etkinleştirmek için düzeltmeyi yükleyin.</td>
</tr>
<tr class="even">
<td>Satıcı kullanıcısının, Dynamics 365 for Operations'taki satıcı işbirliği web arabirimine erişmesi ve bir satıcı işbirliği kullanıcısı ayarlaması gerekir.</td>
<td>Satıcı işbirliği web arabirimini ayarlamak ve bu arabirimle çalışmak için aşağıdaki konularda açıklanan adımları izleyin.
<ul>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-external-vendors/">Harici satıcılarla çalışmak için satıcı işbirliğini kullanma</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/manage-vendor-collaboration-users/">Satıcı iş birliği kullanıcılarını yönetme</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/set-up-and-maintain-vendor-collaboration/">Satıcı iş birliğini ayarlama ve koruma</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-customers-in-dynamics-365-for-operations/">Dynamics 365 for Operations'ta müşterilerle çalışmak için satıcı işbirliğini kullanma</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Özet
Satıcı işbirliği mobil çalışma alanı, satıcıları Dynamics 365 for Operations web istemcisinde satınalma siparişlerini görüp yanıtlayabilmeleri için yeni satınalma siparişleri hakkında bilgilendirir. 

**Not:** Mobil çalışma alanı, satıcı işbirliği web arabirimi yerine değil, ona bir katkı olarak kullanılmalıdır. 

Satıcı işbirliği mobil çalışma alanıyla, satıcılarınız onay için gönderilen yeni satınalma siparişlerini görüntüleyebilir. Bu çalışma alanı, ürünler, miktar ve istenen teslimat tarihleri gibi satınalma siparişi bilgilerini görüntüler. Fiyat bilgileri, her satıcının yapılandırmasına bağlı olarak kullanılabilir. 

Bir kullanıcı satıcı olarak oturum açtığı zaman hangi satınalma siparişlerinin yanıtlandığını veya hangi satınalma siparişlerinin müşteri eylemi beklediğini görür. Satıcı başka bir teslim tarihi önermiş olabilir ve müşteriyle bu tarih üzerinde henüz anlaşılmadığı için satınalma siparişi müşteri eylemi bekliyordur. Satıcı onaylanmış ancak henüz teslim edilmemiş satınalma siparişlerinin bir listesini de görür. 

Satıcı bir satınalma siparişini yanıtlamak için Dynamics 365 for Operations web istemcisinde satıcı işbirliği web arabirimini kullanmak zorundadır. Burası aynı zamanda satıcının, belge ekleri, satır başına teslimat adresi ve satıcı ile ilişkili masraflar gibi sipariş hakkında daha fazla bilgi alacağı yerdir. 

Özel bir güvenlik rolüyle, satıcı, satıcı hesabı için kaydedilen iletişim görevlilerini görüntüleyebilir. Aynı güvenlik rolüyle, satıcı gönderilmiş kullanıcı isteklerinin durumunu görüntüleyebilir. 

Yeni kişiler oluşturma ve yeni kullanıcı istekleri gönderme işlemleri Dynamics 365 for Operations web istemcisindeki satıcı işbirliği arabiriminde yapılmalıdır. 

Mobil çalışma alanıyla satıcınız şunları yapabilir:

-   Satıcıya gönderilen yeni satınalma siparişlerini görüntüleme.
-   Satıcının yanıtladığı ve müşteriden eylem bekleyen satınalma siparişlerini görüntüleme.
-   Onaylanmış ama tamamen teslim alınmamış durumdaki satınalma siparişlerini görüntüleme.
-   Satıcı hesabı için kayıtlı ilgili kişi bilgilerini görüntüleme (ek güvenlik rolü gerektirir).
-   Satıcı tarafından gönderilen kullanıcı isteğinin bilgilerini görüntüleme ve durumunu izleme (ek güvenlik rolü gerektirir).

## <a name="get-started"></a>Başlayın
Mobil cihazınızda kullanmaya başlamak için:

1.  Mobil uygulama mağazanızda, Microsoft Dynamics 365 for Operations uygulamasını indirin ve yükleyin.
2.  Cihazınızda uygulamayı başlatın.
3.  Dynamics 365 URL'nizi girin.
4.  Oturum açılacak şirketi girin. Örneğin **USMF** yazın.
5.  İlk defa oturum açtığınızda, Microsoft Dynamics 365 for Operations hesabınızın kullanıcı adı ve parolasını girmeniz için uyarılırsınız.

Uygulamada oturum açtığınızda görünür çalışma alanı yoktur. Çalışma alanları, mobil app üzerinde görüntülemek için önce istediğiniz çalışma işlemlerini Dynamics 365 for Operations uygulaması için yayımlamanız gerekir. Çalışma alanını yayımlamak için sistem yönetim iznine gereksiniminiz vardır.

1.  Dynamics 365 for Operations'ı başlatın.
2.  **Sistem yönetimi** &gt; **Kurulum** &gt; **sistem parametreleri**ne gidin.
3.  **Mobil uygulamayı yönet** seçeneğini işaretleyin.
4.  Mobil platformda yayımlanacak **Satıcı işbirliği** çalışma alanını seçin.
5.  **Çalışma alanını yayımla** seçeneğini işaretleyin.
6.  Yayımlanmış çalışma alanlarını görmek için cihazınızı yenileyin.
7.  **Satıcı işbirliği** çalışma alanını seçin. Aşağıdaki sayfayı görürsünüz.

    [![satıcı-işbirliği-mobil-uygulaması](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>İlgili kişiler
**Kişiler** sayfası satıcı hesabı için ayarlanan tüm kişileri görmenize olanak sağlar. İlgili kişinin adını, birincil e-posta adresini ve varsa kullanıcı diğer adlarını gösterir. İlgili kişinin kullanıcı hesabının etkin olup olmadığını da gösterir. Bir kişiyi seçtiğinizde, kişinin ayrıntılarını (hangi tüzel kişilerin ilgili kişisi olduğu ve telefon numarası veya farklı bir e-posta adresi gibi iletişim bilgilerini vb.) görürsünüz.

## <a name="user-requests"></a>Kullanıcı talepleri
**Kullanıcı istekleri** sayfası, satıcı işbirliği web arabirimi üzerinden gönderdiğiniz tüm kullanıcı isteklerini görmenizi ve durumlarını izlemenizi sağlar. Bir kullanıcı isteğini seçtiğinizde, neyin istendiğini görebilir, kullanıcı ekleyebilir veya devre dışı bırakabilir, güvenliği değiştirebilir ve kullanıcı için hangi güvenlik rollerinin istendiğini görebilirsiniz.

## <a name="purchase-orders-ready-for-review"></a>İncelemeye hazır satınalma siparişleri
**İncelemeye hazır satınalma siparişleri** sayfası, müşteri tarafından gönderilen ve yanıtlanmamış tüm satınalma siparişlerini görmenizi sağlar. Sipariş hakkında, hangi ürünlerin istendiği ve ne zaman teslim edileceği gibi seçili bilgileri görüntüleyebilirsiniz. Fiyat bilgileri ancak bu satıcı için yapılandırılmışsa mevcuttur. Satınalma siparişinde notlar veya ekler olup olmadığını görebilirsiniz. Ekleri açmak için web istemcisindeki satıcı işbirliğini kullanmanız gerekir. Tüm satırları ayrıntılarıyla görmek için **Satınalma siparişi satırı**'nı seçin. Her satır için bir göstergenin notlar veya ekler olup olmadığını veya başlıkta gösterilenden farklı bir teslimat adresi olup olmadığını göstereceğine dikkat edin. Satınalma siparişini yanıtlamak için satıcı işbirliği web istemcisini kullanmalısınız.

## <a name="awaiting-customer-action"></a>Müşteri eylemi bekleniyor
**Müşteri eylemi bekleniyor** sayfası, sizin veya şirketinizde satıcı işbirliğine de erişimi olan bir başka kişinin yanıtladığı satınalma siparişlerini bulmanıza olanak sağlar. Satınalma siparişleri bu listede ancak müşterinin, satınalma siparişinde aşağıdaki eylemlerden birini gerçekleştirmesi gerekiyorsa görünür.

-   Satınalma siparişi reddedilirse müşterinin gönderilen siparişi güncelleştirip yeniden göndermesi veya siparişi iptal edip yeniden göndermesi gerekir. Satınalma siparişi yeniden gönderildikten sonra **Müşteri eylemi bekleniyor** sayfasında görünmez.
-   Satınalma siparişi değişikliklerle kabul edildiyse, müşterinin orijinal siparişi güncelleştirip ve yeniden incelemeye göndermesi veya değişikliklere göre güncelleştirip hemen onaylaması gerekir. Her iki durumda da, satınalma siparişi **Müşteri eylemi bekleniyor** sayfasından kalkar.
-   Satınalma siparişi kabul edildiyse ve **Müşteri eylemi bekleniyor** sayfasında görünüyorsa, kabul işlemiden sonra otomatik olarak onaylanmamıştır. Bir satınalma temsilcisinin siparişin durumunu Onaylandı'ya çevirmesini bekliyordur. Genellikle, satıcı siparişi kabul ettiği andan itibaren, satınalma siparişi, müşteri ve satıcı arasında bir anlaşma olarak görülür. Satınalma siparişinin durumunu Onaylandı yapmak formalite gereğidir.

Satınalma siparişi seçilince, yanıt hakkında ek ayrıntılar görüntülenir. Satır ayrıntılarını görebilir ve her satır için yanıt verebilirsiniz. Satır durumu, aşağıdaki yanıtlardan hangisinin verildiğini gösterir.

-   Kabul Edildi
-   Reddedildi
-   Değişikliklerle kabul edildi
-   Değiştirildi/Değiştir
-   Plan halinde böl/Plan satırı

Satırların teslim edilmeyeceğini göstermek için kullanılan bir göstergenin **Teslim ediliyor**= evet/hayır gösterdiğine dikkat edin. Bunun nedeni, satırın reddedilmesi veya orijinal satırların teslim edilmesinin beklenmediği yerlerde ikame edilmesinin veya birden fazla plan satırına bölünmüş bir satırın ve orijinal satırın alınan siparişte talep edildiği şekilde teslim edilmesinin beklenmemesinden kaynaklanmış olabilir. Sipariş satırı yanıtındaki değişiklikler görüntülenir (satıcı işbirliği web arabirimini kullanarak görebileceğiniz, karşıya yüklenmiş notlar ve ekler dışında).

## <a name="open-confirmed-orders"></a>Onaylanan siparişleri açma
Satın alma siparişi müşteri tarafından onaylandığında, yani satınalma siparişinin durumu Onaylandı olarak değiştirildiğinde, açık onaylanmış siparişte görünür. Sipariş müşteri tarafından Teslim alındı şeklinde kaydedilene kadar bu listede kalır.





