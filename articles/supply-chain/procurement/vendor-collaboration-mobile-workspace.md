---
title: Satıcı işbirliği mobil çalışma alanı
description: Bu konu, Satıcı işbirliği mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı satıcılarınızın, onay için onlara gönderilen satınalma siparişleri hakkında güncel kalmasını sağlar. Ayrıca yeni ve güncelleştirilmiş satınalma siparişleri ve kişiler hakkında bilgileri görebilirler.
author: RichardLuan
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: riluan
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 5cd8a2b2db7147aca6bdc29ba15d99a619ddb4f8
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020848"
---
# <a name="vendor-collaboration-mobile-workspace"></a>Satıcı işbirliği mobil çalışma alanı

[!include [banner](../includes/banner.md)]

Bu konu, **Satıcı işbirliği** mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı satıcılarınızın, onay için onlara gönderilen satınalma siparişleri hakkında güncel kalmasını sağlar. Ayrıca yeni ve güncelleştirilmiş satınalma siparişleri ve kişiler hakkında bilgileri görebilirler.

Bu mobil çalışma alanı, Finance and Operations mobil uygulaması ile kullanılmak üzere tasarlanmıştır.

## <a name="overview"></a>Özet 
**Satıcı işbirliği** mobil çalışma alanı, satıcıları web istemcisinde satınalma siparişlerini görüp yanıtlayabilmeleri için yeni satınalma siparişleri hakkında bilgilendirir. 

>[!NOTE]
> Mobil çalışma alanı, satıcı işbirliği web arabirimi yerine değil, ona bir katkı olarak kullanılmalıdır. 

Satıcılarınız **Satıcı işbirliği** mobil çalışma alanını kullanarak kendilerine onay için gönderilen yeni satınalma siparişlerini görüntüleyebilir. Bu çalışma alanı ürünler, miktarlar ve istenen teslimat tarihleri gibi satınalma siparişi bilgilerini görüntüler. Fiyat bilgileri, her satıcının yapılandırmasına bağlı olarak da kullanılabilir. 

Bir kullanıcı satıcı olarak oturum açtığı zaman hangi satınalma siparişlerinin yanıtlandığını ve hangi satınalma siparişlerinin müşteri eylemi beklediğini görür. Örneğin, satıcı başka bir teslim tarihi önerdiğinden ve müşteriyle bu tarih üzerinde henüz anlaşılmadığından satınalma siparişi müşteri eylemi bekliyor olabilir. Satıcı onaylanmış ancak henüz teslim edilmemiş satınalma siparişlerinin bir listesini de görür. 

Satıcı bir satınalma siparişini yanıtlamak için web istemcisinde satıcı işbirliği web arabirimini kullanmak zorundadır. Burası aynı zamanda satıcının, belge ekleri, satır başına teslimat adresi ve satıcı ile ilişkili masraflar gibi sipariş hakkında daha fazla bilgi alabileceği yerdir. 

Özel bir güvenlik rolüne sahip satıcılar, satıcı hesabı için kaydedilen iletişim görevlilerini görüntüleyebilir. Aynı güvenlik rolü, satıcının gönderilmiş kullanıcı isteklerinin durumunu görüntülemesini sağlar. 

Web istemcisindeki satıcı işbirliği web arabirimi yeni ilgili kişi oluşturmak ve yeni kullanıcı istekleri göndermek için kullanılmalıdır. 

**Satıcı işbirliği** mobil çalışma alanı satıcının bu görevleri gerçekleştirmesini sağlar:

-   Satıcıya gönderilen yeni satınalma siparişlerini görüntüleme.
-   Satıcının yanıtladığı ve müşteriden eylem bekleyen satınalma siparişlerini görüntüleme.
-   Onaylanmış ama tamamen teslim alınmamış durumdaki satınalma siparişlerini görüntüleme.
-   Satıcı hesabı için kaydedilen ilgili kişi bilgilerini görüntüleme. (Bu görev bir ek güvenlik rolü gerektirir.)
-   Satıcı tarafından gönderilen kullanıcı isteğinin bilgilerini görüntüleme ve isteğin durumunu izleme. (Bu görev bir ek güvenlik rolü gerektirir.)

## <a name="prerequisites"></a>Önkoşullar
Önkoşullar, kuruluşunuza dağıtılan Microsoft Dynamics 365 sürümüne bağlı olarak farklılık gösterir.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Supply Chain Management kullanıyorsanız önkoşullar
Supply Chain Management, kuruluşunuza dağıtıldıysa sistem yöneticisinin **Satıcı işbirliği** mobil çalışma alanını yayımlaması gerekir. Yönergeler için bkz: [Bir mobil çalışma alanı yayımlama](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Microsoft Dynamics 365 for Operations sürüm 1611'i Platform güncelleştirmesi 3 veya daha sonrasıyla kullanıyorsanız önkoşullar
Kuruluşunuza Platform güncelleştirmesi 3 veya üzeri ile Microsoft Dynamics 365 for Operations 1611 sürümü dağıtılmışsa, sistem yöneticisinin aşağıdaki ön koşulları yerine getirmesi gerekir. 

<table>
<thead>
<tr class="header">
<th>Önkoşul</th>
<th>Rol</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Platform Güncelleştirmesi 3 kullanıyorsanız, KB 3216943 uygulanmalıdır.</td>
<td>Sistem yöneticisi</td>
<td>Platform Güncelleştirmesi 3 kullanıyorsanız, KB 3216943 gerekli bir ikili güncelleştirmedir. Bu KB'yi uygulamak için sistem yöneticinizin bu adımları izlemesi gerekir.
<ol>
<li>Microsoft Dynamics Lifecycle Services (LCS) içerisinden KB 3216943 indirin.</li>
<li>Dağıtılabilir bir paket olarak teslim edilen ikili güncelleştirmeyi yükleyin. Dağıtılabilir paket uygulama hakkında bilgi için bkz. <a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Dağıtılabilir paket uygulama</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>KB 4013633 uygulanmış olmalıdır.</td>
<td>Sistem yöneticisi</td>
<td>KB 4013633, <strong>Eldeki stok</strong> mobil çalışma alanını içeren bir X++ güncelleştirmesi veya meta veri düzeltmesidir. KB 4013633 uygulamak için sistem yöneticiniz bu adımları atması gerekir.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Meta veri düzeltmesini LCS'den indirme</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Meta veri düzeltmesini kurun</a>.</li><li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Şunu içeren bir dağıtılabilir paket oluşturun:</a> <strong>SCMMobile</strong> modeli ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Dağıtılabilir paketi uygulayın</a>.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Satıcı işbirliği</strong> mobil çalışma alanının yayımlanmış olması gerekir.</td><td>Sistem yöneticisi</td>
<td>Bkz. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</td>
</tr>
<tr class="even">
<td>Satıcı kullanıcısının, web istemcisindeki satıcı işbirliği web arabirimine erişmesi ve bir satıcı işbirliği kullanıcısı ayarlaması gerekir.</td><td>Satın alma uzmanları ve sistem yöneticisi</td>
<td>Satıcı işbirliği web arabirimini ayarlamak ve bu arabirimle çalışmak için aşağıdaki konularda açıklanan adımları izleyin.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Harici satıcılarla çalışmak için satıcı işbirliğini kullanma</a></li>
<li><a href="manage-vendor-collaboration-users.md">Satıcı iş birliği kullanıcılarını yönetme</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Satıcı işbirliğini ayarlama ve koruma</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Supply Chain Management'ta müşterilerle çalışmak için satıcı işbirliğini kullanma</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobil uygulamayı indirin ve yükleyin

Finance and Operations mobil uygulamasını indirip yükleyin:

-   [Android telefonlar için](https://go.microsoft.com/fwlink/?linkid=850662)
-   [İPhone'lar için](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobil uygulamaya oturum açın
1.  Mobil cihazınızda uygulamayı başlatın.
2.  Microsoft Dynamics 365 URL'nizi girin.
4.  İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir. Kimlik bilgilerinizi girin.
5.  Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir. Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.

    [![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="use-the-vendor-collaboration-mobile-workspace"></a>Satıcı işbirliği mobil çalışma alanını kullanma
**Satıcı işbirliği** çalışma alanını seçtiğinizde aşağıdaki seçenekleri göreceksiniz.

![Satıcı işbirliği mobil çalışma alanı](./media/vendor-collaboration-mobile-app.png)

**Satıcı işbirliği** çalışma alanı aşağıdaki sayfaları içerir.

### <a name="contacts"></a>İlgili kişiler
**Kişiler** sayfası satıcı hesabı için ayarlanan tüm kişileri görmenize olanak sağlar. İlgili kişinin adını, birincil e-posta adresini ve varsa ilgili kişinin diğer adını gösterir. Bu sayfa, ilgili kişinin kullanıcı hesabının etkin olup olmadığını da gösterir. İlgili kişi seçtiğinizde, kişinin ilgili kişisi olduğu tüzel kişilik gibi ayrıntıları görürsünüz. İlgili kişi telefon numarası veya diğer e-posta adresi gibi bilgileri de görebilirsiniz.

### <a name="user-requests"></a>Kullanıcı talepleri
**Kullanıcı istekleri** sayfası, satıcı işbirliği web arabirimi üzerinden gönderdiğiniz tüm kullanıcı isteklerini görmenizi sağlar. Aynı zamanda, bu isteklerin durumunu da izleyebilirsiniz. Bir kullanıcı isteğini seçtiğinizde, neyin istendiğini görebilir, kullanıcı ekleyebilir veya devre dışı bırakabilir, güvenliği değiştirebilir ve kullanıcı için hangi güvenlik rollerinin istendiğini görebilirsiniz.

### <a name="purchase-orders-ready-for-review"></a>İncelemeye hazır satınalma siparişleri
**İncelemeye hazır satınalma siparişleri** sayfası, müşteri tarafından gönderilen ve yanıtlanmamış tüm satınalma siparişlerini görmenizi sağlar. Sipariş hakkında, hangi ürünlerin istendiği ve bu ürünlerin ne zaman teslim edileceği gibi seçili bilgileri görüntüleyebilirsiniz. Fiyat bilgileri, satıcının yapılandırmasına bağlı olarak da kullanılabilir.

Satınalma siparişinde notlar veya ekler olup olmadığını da görebilirsiniz. Bununla birlikte, notları ve ekleri açmak için, web istemcisindeki satıcı işbirliği web arabirimi kullanmanız gerekir. Tüm satırları ayrıntılarıyla görmek için **Satınalma siparişi satırı**'nı seçin. Her satır için bir gösterge notlar veya ekler olup olmadığını veya başlıkta gösterilenden farklı bir teslimat adresi olup olmadığını gösterir.

Satınalma siparişini yanıtlamak için web istemcisindeki satıcı işbirliği web arabirimini kullanmalısınız.

### <a name="awaiting-customer-action"></a>Müşteri eylemi bekleniyor
**Müşteri eylemi bekleniyor** sayfası, sizin veya şirketinizde satıcı işbirliğine erişimi olan bir başka kişinin yanıtladığı satınalma siparişlerini bulmanıza olanak sağlar. Satınalma siparişleri bu listede ancak müşterinin, satınalma siparişinde aşağıdaki eylemlerden birini gerçekleştirmesi gerekiyorsa görünür.

-   Satınalma siparişi reddedilirse müşterinin orijinal siparişi güncelleştirmesi veya iptal etmesi ve yeniden göndermesi gerekir. Satınalma siparişi yeniden gönderildikten sonra **Müşteri eylemi bekleniyor** sayfasında görünmez.
-   Satınalma siparişi değişikliklerle kabul edildiyse, müşterinin orijinal siparişi güncelleştirip ve yeniden incelemeye göndermesi veya istenen değişikliklere göre güncelleştirip hemen onaylaması gerekir. Her iki durumda da, satınalma siparişi **Müşteri eylemi bekleniyor** sayfasından kalkar.
-   Satınalma siparişi kabul edildiyse ancak **Müşteri eylemi bekleniyor** sayfasında görünüyorsa, kabul işlemiden sonra otomatik olarak onaylanmamıştır. Bir satınalma temsilcisinin siparişin durumunu **Onaylandı**'ya çevirmesini bekliyordur. Genellikle, satıcı siparişi kabul ettiği andan itibaren, satınalma siparişi, müşteri ve satıcı arasında bir anlaşma olarak görülür. Bu nedenle, durumu **Onaylandı** olarak güncelleştirmek genellikle bir formalitedir.

Bir satınalma siparişi seçtiğinizde, yanıt hakkında ek ayrıntılar görüntülenir. Satır ayrıntılarını görebilir ve her satır için yanıt verebilirsiniz. Satır durumu, aşağıdaki yanıtlardan hangisinin verildiğini gösterir:

-   Kabul Edildi
-   Reddedildi
-   Değişikliklerle kabul edildi
-   Değiştirildi/Değiştir
-   Plan halinde böl/Plan satırı

**Teslim** alanı satırların teslim edilip edilmeyeceğini belirtmek için **Evet** veya **Hayır** olarak ayarlanır. Bir satır aşağıdaki nedenlerle teslim edilemeyebilir:

- Satır reddedildi.
- Bir değiştirme yapıldı ve orijinal satırın alınan siparişteki gibi teslim edilmesi beklenmiyor.
- Satır birden çok zamanlama satırına bölündü ve orijinal satırın alınan siparişte istendiği gibi teslim edilmesi beklenmiyor.

Sipariş satırı yanıtında yaptığınız değişiklikler gösterilir. Ancak, yüklenen notlar ve ekler gösterilmez. Notları ve ekleri görüntülemek için, web istemcisindeki satıcı işbirliği web arabirimini kullanmanız gerekir.

### <a name="open-confirmed-orders"></a>Açık onaylanmış siparişler
Satın alma siparişi müşteri tarafından onaylandığında, (yani satınalma siparişinin durumu **Onaylandı** olarak değiştirildiğinde), açık onaylanmış siparişte görünür. Sipariş müşteri tarafından alındı şeklinde kaydedilene kadar bu listede kalır.
