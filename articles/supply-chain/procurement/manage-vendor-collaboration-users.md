---
title: Satıcı iş birliği kullanıcılarını yönetme
description: Bu konu, yeni satıcı iş birliği kullanıcıları hazırlama talebinde bulunma ve yeni satıcı iş birliği kişileri ekleme konularını ele alır.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ff0d11bf2c42f7ae63e3db5f31f3ffea2c28f693
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578140"
---
# <a name="manage-vendor-collaboration-users"></a>Satıcı iş birliği kullanıcılarını yönetme

[!include [banner](../includes/banner.md)]

Bu konu, yeni satıcı iş birliği kullanıcıları hazırlama talebinde bulunma ve yeni satıcı iş birliği kişileri ekleme konularını ele alır. 

Dynamics 365 Supply Chain Management'taki satıcı iş birliği arabirimi; satınalma siparişleri, faturalar ve harici satıcılara konsinye stok hakkında bilgi sağlar. **Satıcı yöneticisi (harici)** güvenlik rolü ya da benzer izinlerle harici satıcı olarak çalışıyorsanız yeni kullanıcıların sağlandığı yeni satıcı iş birliği kişileri ve talepleri oluşturabilirsiniz. Tedarik profesyoneli olarak çalışıyorsanız da bu görevleri gerçekleştirebilirsiniz. Bu konuda bu rol, Supply Chain Management kurulumuna sahip bir şirkette çalışan tedarik profesyoneli anlamına gelir. Harici satıcıysanız satıcı iş birliğini kullanma hakkında daha fazla bilgi için bkz. [Müşterilerle satıcı iş birliği](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Tedarik uzmanıysanız satıcı iş birliğini kullanma hakkında daha fazla bilgi için bkz. [Harici satıcılarla satıcı iş birliği](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Yeni satıcı iş birliği kişileri ekleme
Bir kullanıcının satıcı iş birliğine erişimi olmasını istiyorsanız ilk olarak satıcı iş birliği ilgili kişisi olarak eklenmesi gerekir. Şirketinizdeki satıcı iş birliğini kullanmayan çalışanlar için de kişi eklemek isteyebilirsiniz. Örneğin, diğer tedarik bilgisi türleri için iletişim noktası olabilirler. Yeni kişiler, **Satıcı iş birliği** &gt; **Kişiler** menüsünden erişilebilen **Tüm kişiler** sayfasından eklenir. Yeni bir ilgili kişi eklemek için:

1.  **Yeni**'ye tıklayın.
2.  İlgili kişi ayrıntılarını girin.
3.  Şirketinizde temsil ettikleri tüzel kişiliği ve iş birliği yapacakları şirkette birlikte çalışacakları tüzel kişiliği seçin. Bunun için, **Benim şirketimdeki tüzel kişilik**/**Müşterinin şirketindeki tüzel kişilik**  çiftini seçmelisiniz.
4.  **Oluştur**'a tıklayın.

Yalnızca kendi oluşturduğunuz ilgili kişileri silebilirsiniz.

## <a name="vendor-collaboration-user-requests"></a>Satıcı iş birliği kullanıcısı istekleri
Satıcı iş birliği kullanıcısı istekleri bir tedarik profesyoneli veya harici satıcı yöneticisi tarafından yapılabilir.

-   Harici satıcı iseniz **Satıcı iş birliği** modülündeki **Tüm kişiler** sayfasından istekleri gönderirsiniz.
-   Tedarik profesyoneli iseniz **İlgili kişileri görüntüle** sayfasından istekleri gönderirsiniz. Bunu yapmak için satıcı kaydının Eylem Bölmesi'ndeki **Kurulum** bölümünde **Kişiler** &gt; **İlgili kişileri görüntüle**'yi seçin.

Kullanıcıyı hazırlamak, devre dışı bırakmak veya güvenlik rollerini değiştirmek için de istek gönderebilirsiniz. Harici satıcı yöneticisi iseniz kullanıcı istekleri göndermek istediğiniz satıcı hesaplarında ilgili kişi olarak kayıtlı olmanız gerekir ve bu satıcı hesapları için satıcı iş birliği arabirimine erişiminiz olmalıdır.  

İstek gönderildiğinde **Satıcı iş birliği** modülündeki **Satıcı iş birliği kullanıcısı istekleri** ve **Tedarik ve kaynak atama** modülündeki **Satıcı iş birliği kullanıcısı isteği** listelerine eklenir. (Tedarik ve kaynak atama modülüne harici kullanıcılar erişemez.)

### <a name="provision-a-user"></a>Kullanıcıyı hazırlama

Yeni bir kullanıcı hazırlanması için istekte bulunmadan önce ilgili kişinin bir veya daha fazla satıcı hesabında kayıtlı olması gerekir. Yeni bir satıcı iş birliği kullanıcısı isteği oluşturmak için:

1. **Tüm kişiler** sayfasındaki **Provizyon satıcı kullanıcısı**'na tıklayın.
2. Kullanıcının e-posta adresini girin. Bu adres, kullanıcı tarafından Supply Chain Management'ta oturum açmak için kullanılır. E-posta adresi, Microsoft Azure'da kiracı olarak kayıtlı bir etki alanına aitse hazırlama işleminin başarıyla tamamlanması için e-posta adresi mevcut bir Azure Active Directory (AAD) hesabı olmalıdır. E-posta adresi Microsoft Azure'da kayıtlı bir etki alanına ait değilse hazırlama işleminin bir parçası olarak AAD hesabı oluşturulur ve yeni kullanıcı bir davet e-postası alır. Kullanıcı kaydı için @hotmail.com, @gmail.com veya @comcast.net gibi etki alanları olan tüketici e-posta adresleri kullanılamaz.
3. Kullanıcının erişimi olması gereken tüm tüzel kişilikler için **Satıcı iş birliği erişimine izin verildi** seçeneğini **Evet** olarak ayarlayın.
4. **Kullanıcı rolleri ata** bölümünde, yeni kullanıcının sahip olması gereken güvenlik rolleri için **Ata** onay kutusunu işaretleyin.
5. **Gönder**'e tıklayın.

Satıcı kullanıcısı talebi gönderildiğinde, **Satıcı iş birliği erişimine izin verildi** alanı seçilen satıcı hesabı için **Evet** olarak ayarlanır ve kullanıcı talebi iş akışı başlatılır. İş akışının bir parçası olarak, yeni bir kullanıcı oluşturulur ve güvenlik rolleri atanır. Buna ek olarak, Azure portalı ile etkileşim başlatan ve yeni veya mevcut bir AAD hesabını Supply Chain Management kullanıcı hesabı ile ilişkilendiren bir Azure B2B hizmeti etkinleştirilir. Daha fazla bilgi için bkz. [Azure AD B2B iş birliği nedir?](/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).

### <a name="inactivate-a-user"></a>Kullanıcıyı devre dışı bırakma

İlgili kullanıcının satıcı iş birliğine olan erişimini kaldırmanın iki yolu bulunmaktadır:

-   Satıcının **İlgili kişiler** sayfasındaki **Satıcı iş birliği erişimine izin verildi** seçeneğini ilgili kişi için **Hayır** olarak ayarlayın. Bu, ilgili kişinin bağlantıda olduğu her bir tüzel kişilik için tek tek yapılabilir. Bu seçenek yalnızca tedarik profesyonelleri tarafından kullanılabilir.
-   Tüm kullanıcı hesabını **Satıcı kullanıcısını devre dışı bırak** isteği göndererek devre dışı bırakın.

Bir kullanıcının devre dışı bırakılmasını talep etmek için:

1.   **Tüm kişiler** sayfasındaki **Satıcı kullanıcısını** **devre dışı bırak**'a tıklayın.
2.  **İş gerekçesi** alanına bir yorum yazın.
3.  **Gönder**'e tıklayın.

### <a name="modify-security-roles"></a>Güvenlik rollerini ayarlama

**Satıcı kullanıcısı rollerini koru** sayfası, güvenlik rolleri listesinin düzenlenebilmesi dışında **Provizyon satıcı kullanıcısı** sayfası ile aynıdır.  

İlgili kullanıcının güvenlik rollerinin değiştirilmesini talep etmek için:

1.  **Tüm kişiler** sayfasındaki **Satıcı kullanıcısı** **rollerini koru**'ya tıklayın.
2.  **İş gerekçesi** alanına bir yorum yazın.
3.  **Kullanıcı rollerini koru** bölümünde, atamak istediğiniz güvenlik rollerini seçin veya kaldırmak istediklerinizin seçimini kaldırın.
4.  **Gönder**'i tıklatın.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]