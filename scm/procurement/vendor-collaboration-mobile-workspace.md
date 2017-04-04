---
title: "Satıcı işbirliği mobil çalışma alanı için Microsoft Dynamics 365 işlemleri uygulama için"
description: "Satıcı işbirliği mobil çalışma alanıyla satıcılarınıza onayı ve yeni ve güncelleştirilmiş satınalma siparişleri ve kişiler hakkındaki bilgileri görüntüleyin kendisine gönderilen satınalma siparişlerine güncel kalabilir."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Satıcı işbirliği mobil çalışma alanı için Microsoft Dynamics 365 işlemleri uygulama için

Satıcı işbirliği mobil çalışma alanıyla satıcılarınıza onayı ve yeni ve güncelleştirilmiş satınalma siparişleri ve kişiler hakkındaki bilgileri görüntüleyin kendisine gönderilen satınalma siparişlerine güncel kalabilir.

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
<td>Mobil platform için işlemleri hakkında Microsoft Dynamics 365 okuyun</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 işlemleri mobil platformu</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 işlemleri için</td>
<td>1611 işlemleri sürümü için Microsoft Dynamics 365 olmayan bir ortamda kullanıyorsanız ve Microsoft Dynamics işlemleri platform için 3 (Kasım 2016) güncelleştirme emin olun.</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Yüklü uygulama işlemleri için Dynamics 365 sahip mobil aygıt</span></td>
<td><span style="color: #000000;">Dynamics 365 işlemleri uygulama için mobil app deponuzdan indirin.</span></td>
</tr>
<tr class="even">
<td>Düzeltme KB 3215650</td>
<td>Dynamics 365 işlemleri için sağlanan çalışma alanlarını etkinleştirmek için düzeltmeyi yükleyin.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Düzeltme KB 3216943</span> </span></td>
<td>Satıcı işbirliği mobil çalışma alanı etkinleştirmek için düzeltmeyi yükleyin.</td>
</tr>
<tr class="even">
<td>Satıcı kullanıcı, Dynamics 365 işlemleri için satıcı işbirliği web arabiriminde erişiminiz ve bir satıcı işbirliği kullanıcı ayarlama.</td>
<td>Ayarlamak ve satıcı işbirliği web arabirimi ile çalışmak için aşağıdaki konularda açıklanan adımları izleyin.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Dış satıcılar ile çalışmak için satıcı işbirliği kullanın</a></li>
<li><a href="manage-vendor-collaboration-users.md">Satıcı iş birliği kullanıcılarını yönetme</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Satıcı iş birliğini ayarlama ve koruma</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Satıcı işbirliği Dynamics 365 işlemleri için müşteriler ile çalışmak için kullanın</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Özet
Satıcı işbirliği mobil çalışma alanı satıcıları görmek ve satınalma siparişleri, Dynamics 365 işlemleri web istemcisi yanıt böylece yeni satınalma siparişleri hakkında haberdar tutar.  

**Not:** mobil çalışma satıcı işbirliği web arabirimi, ancak bir değiştirme için bir ek olarak kullanılmalıdır.  

Satıcı işbirliği mobil çalışma alanıyla satıcılarınıza onay için gönderilen yeni satınalma siparişlerini görüntüleyebilirsiniz. Bu ürün, miktar ve istenen teslimat tarihleri gibi satınalma siparişi bilgilerini görüntüler. Fiyat bilgileri, her satıcı için yapılandırmasına bağlı olarak kullanılabilir.  

Satıcı olarak bir kullanıcı oturum açarken hangi satınalma siparişleri için yanıt veren ya da hangi satınalma siparişleri müşteri eylem hala bekleyen göreceksiniz. Başka önerilen satıcı teslim tarihi satınalma siparişindeki müşteri eylem bekleyen böylece müşteriyle henüz anlaşma yok. Satıcı aynı zamanda teyit edilen ancak henüz teslim edilmemiş satınalma siparişlerinin bir listesini görürsünüz.  

Bir satınalma siparişi için yanıt vermek için Dynamics 365 işlemleri web istemcisi için kullanılabilir satıcı işbirliği web arabirimi kullanmak satıcı vardır. Satıcı belge ekleri gibi sipariş, teslimat adresi, her satır ve satıcıyla ilişkili giderleri hakkında daha fazla bilgiyi nereden budur.  

Özel güvenlik rolüyle, satıcı için bir satıcı hesabı kayıtlı kişilerin hangi kişi görüntüleyebilirsiniz. Aynı güvenlik rolüyle satıcı gönderildi herhangi kullanıcı isteğinin durumunu görüntüleyebilirsiniz.  

Yeni kişi oluşturma ve yeni kullanıcı isteklerini gönderme işlemlerini web istemcisi için Dynamics 365 kullanılabilir satıcı işbirliği arabirimi yapılmalıdır.  

Mobil çalışma alanıyla satıcınıza yapabilirsiniz:

-   Satıcıya gönderilen yeni satınalma siparişleri görüntüleyin.
-   Satıcı için yanıtladı ve müşteri eylem bekleyen görünüm satınalma siparişleri.
-   Teyit edilmiş durumda olan satınalma siparişlerini görüntüleme ve tam olarak alınmamış.
-   Satıcı hesabı için kayıtlı olduğu ilgili kişi bilgileri görüntüleyin (ek güvenlik rolü gerektirir).
-   (Ek güvenlik rolü gerektirir) satıcı tarafından gönderilen kullanıcı isteğinin durumunu izleyin ve bilgileri görüntüleyin.

## <a name="get-started"></a>Başlayın
Mobil aygıtınızda kullanmaya başlamak için:

1.  Mobil app store üzerinde karşıdan yükleyip Microsoft Dynamics 365 işlemleri uygulama için.
2.  Aygıtınızda uygulamayı başlatın.
3.  Dynamics 365 URL'nizi girin.
4.  Oturum açmak için şirket girin. Örneğin: **USMF**.
5.  İlk kez, oturum, Microsoft Dynamics 365 işlem hesabı için kullanıcı adı ve parola için uyarılırsınız. 

Çalışma alanı yok uygulamasında oturum sonra görülebilir. Çalışma alanları, mobil app üzerinde görüntülemek için önce istediğiniz çalışma işlemleri uygulama için Dynamics 365 yayımlamanız gerekir. Çalışma yayımlamak için sistem yönetim iznine ihtiyacınız var.

1.  Dynamics 365 işlemleri için başlatın.
2.  Git **Sistem Yönetimi**&gt;**Kurulum**&gt;**sistem parametreleri**.
3.  Seçin **Yönet mobil uygulama**.
4.  Çalışma alanını seçin **satıcı işbirliği** için mobil platformda yayımlanacak.
5.  Seçin **çalışma yayımlamak**.
6.  Yayımlanmış çalışma öğrenmek için aygıtınızın yenileyin.
7.  Seçin **satıcı işbirliği** çalışma alanı. Şu sayfaya çalışacaksınız.

[![Satıcı işbirliği mobile app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>İlgili kişiler
**Kişiler** sayfası satıcı hesabı için ayarlanan tüm kişileri görmek olanak sağlar. Bu kişinin adı, birincil e-posta ve kullanıcı diğer adı, varsa gösterir. İlgili kişinin kullanıcı hesabı etkin olup olmadığını gösterir. Bir kişiyi seçtiğinizde, hangi gibi tüzel kişi için kişidir kişi ayrıntılarını görmek ve telefon numarası veya farklı bir e-posta adresi gibi bilgileri başvurun.

## <a name="user-requests"></a>Kullanıcı talepleri
**Kullanıcı istekleri** sayfasında gördüğünüz tüm kullanıcı istekleri satıcı işbirliği web arabirimi göndermiş olması ve durumunu izleyin sağlar. Kullanıcı isteği seçtiğinizde, istendi bakın, eklemek veya kullanıcı devre dışı, güvenliğini değiştirmek ve hangi güvenlik rolleri kullanıcı için talep edilen bakın.

## <a name="purchase-orders-ready-for-review"></a>Satınalma siparişleri gözden geçirmeye hazır
**Satınalma siparişleri gözden geçirme için hazır** müşteri tarafından gönderilen ve yanıtlanmamış tüm satınalma siparişleri görmek için sayfa sağlar. Hangi ürünleri istediği zaman ve teslim etmek sipariş, ilgili seçilen bilgileri görüntüleyebilirsiniz. Fiyat bilgilerini yalnızca bu satıcı için yapılandırılmışsa kullanılabilir.  

Satınalma siparişi notları veya ekleri olup olmadığını görebilirsiniz. Ekleri açmak için web istemcisinde satıcı işbirliği kullanmanız gerekir. Seçin **satınalma siparişi satırı** ayrıntıları içeren tüm satırları görmek için. Her satır için bir gösterge notları veya ekleri olup olmadığını veya başlığında gösterilen daha farklı bir teslimat adresi olup olmadığını göstereceğini unutmayın.  

Satınalma siparişi için yanıt vermek için satıcı işbirliği web istemcisini kullanmalısınız.

## <a name="awaiting-customer-action"></a>Müşteri eylemi bekleniyor
**Müşteri eylem bekleyen** bulduğunuz sayfa sağlar satınalma siz veya satıcı işbirliği erişimi olan şirketinizdeki biri yanıtlandı siparişleri. Müşteri satınalma siparişinde aşağıdaki eylemlerden birini gerçekleştirmeniz gerekiyorsa, satınalma siparişleri yalnızca bu listede görünür.

-   Satınalma siparişi reddedilirse müşteri ya da gönderilen sipariş güncelleştirmek ve yeniden gönderme gerekli veya siparişi iptal etme ve yeniden gönderin. Satınalma siparişi yeniden gönderildiğinde dan kaybolur **müşteri eylem bekleyen** sayfa.
-   Satınalma siparişi ile değişiklikleri onayladığınızda müşteri orijinal siparişi güncelleştirin ve yeniden gözden geçirilmek üzere göndermek veya göre değişir güncelleştirmek ve hemen onaylamak gerekir. Her iki durumda da, gelen satınalma siparişi kaybolur **müşteri eylem bekleyen** sayfa.
-   Satınalma siparişini kabul edildi ve görünür **müşteri eylem bekleyen** sayfa, öyledir çünkü kabul tamamlandığında satınalma siparişine otomatik olarak onaylanmadı. Onaylı için sırasını değiştirmek bir satınalma aracısı için bekliyor. Satıcı Sipariş kabul ettiği sürece genellikle, satınalma siparişi olarak müşteri ve satıcı arasındaki anlaşmanın kabul. Satınalma siparişi onaylı duruma taşıyor bir formality olurdu.

Satınalma siparişi'ni seçerek, yanıt hakkında ek ayrıntılar görüntülenir. Satır ayrıntılarını ve her satır için yanıt görebilirsiniz. Hangi aşağıdaki yanıtlar verildi satır durumu gösterir.

-   Kabul Edildi
-   Reddedildi
-   Değişikliklerle kabul edildi
-   Yerine ikame
-   Zamanlama/zamanlama Satırı Böl

Bir gösterge gösterir Not **dağıtma**= Evet/Hayır, hangi satırları değil teslim olduğunu belirtmek için kullanılır. Bu, satır reddedildi veya burada orijinal satırların teslim beklenmez ya da birden çok zamanlama satıra bölünmüş bir çizgi yerine ve özgün satır alınan sırada istenen şekilde teslim edilecek beklenmiyor olmamasından kaynaklanabilir.  

Sipariş satırı yanıtı değişiklikleri karşıya yüklenen notlar ve satıcı işbirliği web arabirimini kullanarak görebilirsiniz ekleri dışında görüntülenir.

## <a name="open-confirmed-orders"></a>Teyit edilen siparişleri Aç
Satınalma siparişi müşteri tarafından onaylandığında satınalma siparişi başka bir deyişle, onaylı duruma açık teyit edilen sırada görünür değiştirilir. Müşteri tarafından alınan olarak kayıtlı olduğu kadar bu listede kalır.


