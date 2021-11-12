---
title: Satıcı işbirliğini ayarlama ve koruma
description: Bu konuda, Dynamics 365 Supply Chain Management'ta satıcı işbirliğinin nasıl ayarlanacağını açıklanmaktadır. Ayrıca, yeni satıcı işbirliği kullanıcılarının nasıl alınacağını ve bu kullanıcılar için güvenlik rollerini yönetmeyi da açıklamaktadır.
author: Henrikan
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b635255fffa6fd3c6612cd248dc692df204aa76d
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/19/2021
ms.locfileid: "7652113"
---
# <a name="set-up-and-maintain-vendor-collaboration"></a>Satıcı işbirliğini ayarlama ve koruma

[!include [banner](../includes/banner.md)]

Satıcı iş birliği arabirimi; satınalma siparişleri, faturalar ve harici satıcı kullanıcılarına konsinye stok hakkında kısıtlı bilgi kümesi sağlar. Bu arabirimden, bir satıcı ayrıca teklif taleplerini (RFQ'ler) yanıtlayabilir ve temel şirket bilgilerini görüntüleyebilir ve düzenleyebilir.

Bu konuda, Dynamics 365 Supply Chain Management'ta satıcı işbirliğinin nasıl ayarlanacağını açıklanmaktadır. Ayrıca, yeni satıcı işbirliği kullanıcılarının nasıl alınacağına dair bir iş akışı ayarlama ve bu kullanıcılar için güvenlik rollerini yönetmeyi da açıklamaktadır.

> [!NOTE]
> Satıcı işbirliğiyle ilgili güvenlik rollerinin kurulumu hakkındaki bilgiler yalnızca Finance and Operations'ın geçerli sürümü için geçerlidir. Microsoft Dynamics AX 7.0 (Şubat 2016) ve Microsoft Dynamics AX uygulaması 7.0.1 (Mayıs 2016) sürümünde, **Satıcı portalı** modülünü kullanarak satıcılarla iş birliği yapabilirsiniz. Microsoft Dynamics AX'deki satıcı portalı ile ilgili kullanıcı izinleri hakkında bilgi için bkz. [Satıcı portalı kullanıcı güvenliği](configure-security-vendor-portal-users.md).

## <a name="set-up-vendor-collaboration-security-roles"></a>Satıcı güvenlik rollerini ayarlama

Yeterli izni olan bir tedarik uzmanı veya satıcı, ilgili kişi kaydında **Satıcı kullanıcısı sağla** işlevini etkinleştirerek bir ilgili kişinin bir kullanıcı olarak sağlanmasını isteyebilir. Sağlama işlemi sırasında, yeni harici kullanıcı için kullanıcı izinleri seçilir ve yeni satıcı kullanıcı isteği gönderilir. Satıcı kullanıcı isteğinde seçim için kullanılabilen kullanıcı izinlerini doğru şekilde ayarlamanız önemlidir. Aksi durumda, satıcılara Supply Chain Management içinde erişimleri olmayan bilgilere erişim izni verilebilir.

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a>İlgili kişi için yeni kullanıcı isteği kullanıldığında seçim için kullanılabilen güvenlik rollerini ayarla

1. **Sistem yönetimi** &gt; **Güvenlik** &gt; **Harici roller**'i seçin.
2. **Yeni**'yi seçin ve sonra bir güvenlik rolü ve **Satıcı** tarafı rolü seçin.

Supply Chain Management'ta sağlanan **Satıcı yönetici (harici)** ve **Satıcı (dış)** rollerini eklemek isteyebilirsiniz. Alternatif olarak, şirketinizin oluşturmuş olduğu güvenlik rollerini de kullanabilirsiniz.

**Satıcı yönetici (dış)** rolünün yalnızca satıcılar yeni ilgili kişiler oluşturacaksa, yeni kullanıcılar için satıcı işbirliği kullanıcı isteklerini, kullanıcı bilgilerinde yapılan değişiklikleri teslim etmek ve bu istekleri iş akışı yoluyla işlemek için kullanılabilir yapmalısınız.

Satıcı ilgili kişilerini ve kullanıcılarını el ile ayarlamayı planlıyorsanız, yalnızca **Satıcı (dış) rolü** kullanılabilir hale getirebilirsiniz. Bu rol daha sonra bir satıcı kullanıcı isteği aracılığıyla talep edilebilecek tek rol olacaktır.

> [!NOTE]
> **SystemUser** rolü, yeni bir kullanıcı hesabını el ile oluşturduğunuzda otomatik olarak verilir. Bu nedenle, bu rolü kaldırmalı ve **SystemExternalUser** rolünü atamalısınız. Yeni kullanıcı hesapları, yeni bir kullanıcı sağlamak üzere bir satıcı kullanıcı isteği tarafından başlatılan iş akışı aracılığıyla oluşturulduysa, satıcı işbirliği için ayarlamış olduğunuz bir veya daha fazla rolden ve **SystemExternalUser** rolünün atanması sağlanır.

#### <a name="vendor-admin-external-security-role"></a>Satıcı yönetici (harici) güvenlik rolü

**Satıcı yönetici (harici)** rolü, satıcı ilgili kişi bilgilerini içeren harici satıcılar için ve yeni satıcı işbirliği kullanıcıları sağlamak için istekler oluşturmak amacıyla kullanılabilir. Bu güvenlik rolüne sahip harici kullanıcılar aşağıdaki görevleri gerçekleştirebilir:

- Kişinin başlığı, e-posta adresi ve telefon numarası gibi ilgili kişi bilgilerini görüntüleyin ve değiştirin.
- İlgili kişi oldukları satıcı hesaplarına yeni veya varolan ilgili kişi ekleyin.
- Oluşturdukları tüm ilgili kişileri silin.
- İlgili kişi ve satıcı hesabı arasındaki ilişkilendirmeyi etkinleştirin veya devre dışı bırakın. İlgili kişi ve satıcı hesabı arasındaki ilişki devre dışında etkinleştirildiğinde, ilgili kişi yeni satınalma siparişlerinde veya diğer belgelerde referans alınamaz.
- Satıcı hesabına özgü satıcı işbirliği arabirimindeki belgelere ilgili kişinin erişimini reddedin veya izin verin. İlgili kişi ve satıcı hesabı arasındaki ilişki devre etkinleştirildikten sonra, satıcı hesabına özgü belgelere erişim her zaman reddedilir.
- **Kullanıcı sağla** eylemini kullanarak ilgili kişi için yeni bir kullanıcı hesabı isteyin.
- İlgili kişinin kullanıcı hesabının devre dışı bırakılmasını isteyin.
- Güvenlik rolleri eklemek veya kaldırmak için ilgili kişinin kullanıcı hesabının değiştirilmesini isteyin.
- RFQ'ları görüntüleme.

#### <a name="vendor-external-security-role"></a>Satıcı (harici) güvenlik rolü

**Satıcı (harici) rolü**, satınalma siparişleriyle çalışacak harici satıcılar için kullanılabilir. Bu güvenlik rolüne sahip harici kullanıcılar aşağıdaki görevleri gerçekleştirebilir:

- Satınalma siparişleri hakkındaki bilgileri yanıtlama ve görüntüleme.
- Satıcı işbirliği faturalarını koru.
- Konsinye stoğu görüntüle.
- RFQ'ları görüntüleyin ve yanıtlayın.
- Satıcı bilgilerini görüntüleme.

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a>Olası satıcılar oluşturulurken kullanılan güvenlik rollerini ayarlayın

Olası bir satıcı kayıt isteğiyle başlatılan satıcıların yerleşik satıcısı olması için, bir harici güvenlik rolü ayarlamanız gerekir. Bu rol, sağlama işlemi sırasında **Kullanıcı isteği iş akışı (platform)** türünün iş akışı tarafından denetlenen yeni kullanıcılara atanacak. Daha fazla bilgi için, bu konunun ilerleyen kısımlarında bulunan [Satıcı işbirliği kullanıcı istekleri bölümünü işlemek üzere iş akışlarını ayarla](#set-up-workflows-to-process-vendor-collaboration-user-requests) konusuna bakın.

Olası satıcıların nasıl kullanılacağı hakkında bilgi için, bkz. [Satıcıları ekleme](vendor-onboarding.md).

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a>Yeni bir olası satıcı kullanıcı talebi gönderildiğinde kullanılan güvenlik rolünü ayarlama

1. **Sistem yönetimi** >  **Güvenlik** > **Harici roller**'i seçin.
2. **Yeni**'yi seçin ve sonra bir güvenlik rolü ve **Olası satıcı** tarafı rolü seçin.

Supply Chain Management'ta sağlanan **Satıcı adayı (harici)** rolünü eklemeniz gerekir.

Güvenlik rolü, yalnızca yeni satıcı kayıt sihirbazına erişim verecektir.

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a>Satıcı işbirliği kullanıcı isteklerini işleyecek iş akışlarını ayarla

İlgili tüm görevlerin tamamlandığından ve uygun onayların verildiğinden emin olmak için, satıcı işbirliği kullanıcı taleplerini işleyecek iş akışları ayarlamanız gerekir.

Satıcı işbirliği kullanıcı istekleri, **Satıcı yönetici (harici)** güvenlik rolüne veya benzer izinlere sahip harici satıcılar tarafından veya şirketinizdeki satın alma uzmanları tarafından gönderilir. Bunlar, satıcı ekleme işlemi sırasında olası satıcı kayıt isteklerinden de oluşturulabilir.

Üç tip istek vardır:

- Yeni bir kullanıcı sağlama istekleri
- Varolan bir kullanıcıyı devre dışı bırakma istekleri
- Varolan bir kullanıcının güvenlik rollerini değiştirme istekleri

Satıcı işbirliği kullanıcı istekleri hakkında daha fazla bilgi için bkz. [Satıcı iş birliği kullanıcılarını yönetme](manage-vendor-collaboration-users.md).

Üç tür satıcı işbirliği kullanıcı isteğini işlemek için iki veya daha fazla iş akışı oluşturmanız gerekir. Yeni iş akışları, **Kullanıcı iş akışları** sayfasında oluşturulur.

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a>Yeni kullanıcıları sağlama ve güvenlik rollerini değiştirme için iş akışı örneği

Yeni kullanıcılar oluşturmak ve güvenlik rollerini değiştirmek amacıyla satıcı kullanıcı isteklerini işlemek için iş akışının başına dallanma koşulu koyabilirsiniz. Bu şekilde, isteğin yeni bir kullanıcı oluşturma veya var olan bir kullanıcıyı değiştirme olmasına bağlı olarak, iş akışının farklı bir dalı kullanılır.

Bu dallanmayı ayarlamak için **Kullanıcı İsteği İş Akışı (Platform)** türünün yeni iş akışı oluşturun. Bu iş akışının dalları aşağıdaki öğeleri içerebilir.

#### <a name="branch-to-provision-new-users"></a>Yeni kullanıcıları sağlamak için dallanma

1. Yeni kullanıcıların satıcı işbirliği bilgilerine erişim izni verilmesini onaylamaktan sorumlu kişiye onay görevi atayın.
2. Azure portalında yeni Microsoft Azure Active Directory (Azure AD) kullanıcı hesaplarını istemeye sorumlu kişiye bir görev atayın. Bu adım için önceden tanımlanmış **Azure B2B Kullanıcı daveti gönder** görevini kullanın. B2B kullanıcıları, otomatik olarak Azure AD'ye aktarılabilir. Önceden tanımlanmış **Azure AD B2B kullanıcısı sağlama**'yı kullanın. Daha fazla bilgi için, bkz. [B2B kullanıcılarını Azure AD'ye aktarma](../../fin-ops-core/dev-itpro/sysadmin/implement-b2b.md).
3. Azure'a yükleme yapan kişiye onay görevi atayın. Bir hesap başarıyla oluşturulmazsa, bu kişi görevi reddeder ve iş akışını sonlandırır. Bu onay görevi, B2B uygulama programlama arabirimi (API) aracılığıyla otomatik olarak Azure'a yeni kullanıcı hesapları veren adımı eklediyseniz atlanabilir.
4. Yeni bir kullanıcı sağlayan otomatik bir görev ekleyin. Bu adım için önceden tanımlanmış **Otomatikleştirilmiş kullanıcı sağlama** görevini kullanın.
5. Yeni kullanıcıyı uyaran bir görev ekleyin. Yeni kullanıcıyı, Supply Chain Management için bir URL içeren bir karşılama e-postası göndermek isteyebilirsiniz. Bu e-posta, **E-posta iletileri** sayfasında oluşturduğunuz bir şablonu kullanabilir ve sonra **Kullanıcı iş akışı parametreleri** sayfasında seçeneğini belirleyebilirsiniz. Şablon, **%portalURL%** etiketi içerebilir. Hoş geldiniz e-postası oluşturulduğunda, bu etiket Supply Chain Management kiracısı URL'siyle değiştirilecektir.

    > [!NOTE]
    > Bu iş akışı, kullanıcı ekleme gerektiren birden çok senaryoda kullanılabilir. Örneğin, olası satıcılar veya ilgili kişiler satıcı işbirliği hesabı gerektiriyorsa kullanılabilir. Bu nedenle, e-postayı çoklu amaçlar için kullanılabilecek bir genel ifade olarak ifade etmelisiniz.

#### <a name="branch-to-modify-security-roles"></a>Güvenlik rollerini değiştiren dal

1. Güvenlik rollerdeki değişiklikleri onaylamaktan sorumlu kişiye onay görevi atayın.
2. İlgili güvenlik rollerini ekleyen veya kaldıran otomatik bir görev ekleyin. Bu adım için **Otomatikleştirilmiş kullanıcı sağlama** görevini kullanın.

### <a name="example-of-a-workflow-for-inactivating-a-user"></a>Kullanıcıyı geçersiz kılma ile ilgili iş akışı örneği

**Devre dışı olan kullanıcı isteği iş akışı platform** türünde bir iş akışı oluşturun ve aşağıdaki görevleri ekleyin.

1. Kullanıcıları devre dışı bırakmayla ilgili istekleri kabul etmekten sorumlu kişiye onay görevi atayın. Bu onay adımını otomatikleştirmek için koşullar ekleyebilirsiniz.
2. Kullanıcıyı geçersiz kılan otomatik bir görev ekleyin. Bu adım için **Otomatikleştirilmiş kullanıcı devre dışı bırakma** görevini kullanın.
3. Gerekli olan tüm temizleme görevlerini ekleyin. Örneğin, hesabı Azure portalında dizinden kaldıran bir görev ekleyebilirsiniz.

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a>Belirli bir satıcı için satıcı iş birliğini etkinleştirme

Satıcı işbirliği kullanan birisi için bir kullanıcı hesabı oluşturmadan önce satıcıyı, satıcı iş birliğini kullanabilecek şekilde ayarlamanız gerekir. **Satıcılar** sayfasındaki **Genel** sekmesinde **İş birliğini etkinleştirme** alanını seçin. Aşağıdaki seçenekler bulunur:

- **Etkin (SS otomatik olarak onaylanır)** – Satınalma siparişleri satıcılar değişiklik istemeden kabul ettiğinde otomatik olarak onaylanır.
- **Etkin (PO otomatik olarak onaylanmaz)**- Satınalma isteklerinin satıcı kabul ettikten sonra kuruluşunuz tarafından el ile onaylanması gerekir.

> [!NOTE]
> Şirketinizdeki satın alma uzmanları da bu görevi tamamlayabilir.

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a>Yeni satıcı işbirliği kullanıcıları sağlama sorunlarını giderme

Yeni satıcı iş birliği kullanıcıları, **Satıcı kullanıcısı sağla** türünden olan satıcı işbirliği kullanıcı taleplerini işleyecek şekilde ayarladığınız iş akışı aracılığıyla sağlanır.

Yeni bir satıcı işbirliği kullanıcısının e-posta adresi kiracı olarak Azure'da kayıtlı bir etki alanına aitse (bir yönetilen etki alanı hesabındaysa), e-posta adresinin varolan bir Azure AD hesabı olması gerekir. Aksi takdirde, sağlama işlemi tamamlanamaz.

Azure AD hesap yönetimi için iş akışında **Azure B2B kullanıcı daveti gönder** görevinde kullanılan işlemle ilgili daha fazla bilgi edinmek için bkz. [Azure Active Directory B2B iş birliği](/azure/active-directory/external-identities/what-is-b2b).

## <a name="additional-resources"></a>Ek kaynaklar

[Harici satıcılarla satıcı işbirliği](vendor-collaboration-work-external-vendors.md)

Satıcı ekleme işlemine dair kısa bir video izleyin: [Yeni satıcı ekleme](https://www.youtube.com/watch?v=0KUc3AGaTKk&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
