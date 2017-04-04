---
title: "Satıcı iş birliği kullanıcılarını yönetme"
description: "Bu konu, yeni satıcı iş birliği kullanıcıları hazırlama talebinde bulunma ve yeni satıcı iş birliği kişileri ekleme konularını ele alır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 380f1bcdf7109dc12fd898199033eac7710d863c
ms.lasthandoff: 03/31/2017


---

# <a name="manage-vendor-collaboration-users"></a>Satıcı iş birliği kullanıcılarını yönetme

Bu konu, yeni satıcı iş birliği kullanıcıları hazırlama talebinde bulunma ve yeni satıcı iş birliği kişileri ekleme konularını ele alır. 

Microsoft Dynamics 365 for Operations'taki satıcı iş birliği arabirimi; satınalma siparişleri, faturalar ve harici satıcılara konsinye stok hakkında bilgi sağlar. **Satıcı yöneticisi (harici)** güvenlik rolü ya da benzer izinlerle harici satıcı olarak çalışıyorsanız yeni kullanıcıların sağlandığı yeni satıcı iş birliği kişileri ve talepleri oluşturabilirsiniz. Tedarik profesyoneli olarak çalışıyorsanız da bu görevleri gerçekleştirebilirsiniz. Bu konuda, bu rol Dynamics 365 for Operations kurulumuna sahip bir şirkette çalışan tedarik profesyoneli anlamına gelir. Harici satıcı iseniz satıcı işbirliği kullanma hakkında daha fazla bilgi için bkz: [satıcı müşteriler ile](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Profesyonel bir tedarik iseniz satıcı işbirliği kullanma hakkında daha fazla bilgi için bkz: [dış satıcılar için satıcı işbirliği](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Yeni satıcı iş birliği kişileri ekleme
Bir kullanıcının satıcı iş birliğine erişimi olmasını istiyorsanız ilk olarak satıcı iş birliği ilgili kişisi olarak eklenmesi gerekir. Şirketinizdeki satıcı iş birliğini kullanmayan çalışanlar için de kişi eklemek isteyebilirsiniz. Örneğin, diğer tedarik bilgisi türleri için iletişim noktası olabilirler. Yeni kişiler eklenen **tüm kişiler** nereden erişildiğine sayfası, **satıcı işbirliği**&gt;**kişiler** menü. Yeni bir ilgili kişi eklemek için:

1.  **Yeni**'ye tıklayın.
2.  İlgili kişi ayrıntılarını girin.
3.  Şirketinizde temsil ettikleri tüzel kişiliği ve iş birliği yapacakları şirkette birlikte çalışacakları tüzel kişiliği seçin. Seçerek bunu bir **benim şirket tüzel**/**müşteri şirkete tüzel** çifti.
4.  **Oluştur**'a tıklayın.

Yalnızca kendi oluşturduğunuz ilgili kişileri silebilirsiniz.

## <a name="vendor-collaboration-user-requests"></a>Satıcı işbirliği kullanıcısı istekleri
Satıcı iş birliği kullanıcısı istekleri bir tedarik profesyoneli veya harici satıcı yöneticisi tarafından yapılabilir.

-   Harici satıcı iseniz, gelen istekleri gönderme **tüm kişiler** sayfa içinde **satıcı işbirliği** modülü.
-   Tedarik profesyoneli iseniz **İlgili kişileri görüntüle** sayfasından istekleri gönderirsiniz. Satıcı kayıt üzerinde bunun için **Kurulum** eylem bölmesinde, select bölümünde **kişiler**&gt;**kişileri görüntülemek**.

Kullanıcıyı hazırlamak, devre dışı bırakmak veya güvenlik rollerini değiştirmek için de istek gönderebilirsiniz. Harici satıcı yöneticisi iseniz kullanıcı istekleri göndermek istediğiniz satıcı hesaplarında ilgili kişi olarak kayıtlı olmanız gerekir ve bu satıcı hesapları için satıcı iş birliği arabirimine erişiminiz olmalıdır.  

İstek gönderildiğinde **Satıcı işbirliği** modülündeki **Satıcı işbirliği kullanıcısı istekleri** ve **Tedarik ve kaynak atama** modülündeki **Satıcı işbirliği kullanıcısı isteği** listelerine eklenir. (Tedarik ve kaynak atama modülüne harici kullanıcılar erişemez.)

### <a name="provision-a-user"></a>Kullanıcıyı hazırlama

Yeni bir kullanıcı hazırlanması için istekte bulunmadan önce ilgili kişinin bir veya daha fazla satıcı hesabında kayıtlı olması gerekir. Yeni bir satıcı iş birliği kullanıcısı isteği oluşturmak için:

1.  Üzerinde **tüm kişiler** sayfasında,'ı **provizyon satıcı kullanıcı**.
2.  Kullanıcının e-posta adresini girin. Bu adres kullanıcı tarafından Dynamics 365 for Operations'ta oturum açmak için kullanılır. E-posta adresi, Microsoft Azure'da kiracı olarak kayıtlı bir etki alanına aitse hazırlama işleminin başarıyla tamamlanması için e-posta adresi mevcut bir Azure Active Directory (ADD) hesabı olmalıdır. E-posta adresi Microsoft Azure'da kayıtlı bir etki alanına ait değilse hazırlama işleminin bir parçası olarak EKLE hesabı oluşturulur ve yeni kullanıcı bir davet e-postası alır. Tüketici e-posta adresleri ile etki alanları gibi @hotmail.com, @gmail.com, veya @comcast.netDynamics 365 işlemleri kullanıcı için kaydetmek için kullanılamaz.
3.  Kullanıcının erişimi olması gereken tüm tüzel kişilikler için **Satıcı işbirliği erişimine izin verildi** seçeneğini **Evet** olarak ayarlayın.
4.  **Kullanıcı rolleri ata** bölümünde, yeni kullanıcının sahip olması gereken güvenlik rolleri için **Ata** onay kutusunu işaretleyin.
5.  **Gönder**'e tıklayın.

Satıcı Kullanıcı isteği gönderildiğinde, **satıcı işbirliği erişim izin** ayarlanırsa **Evet** iş akışı başlatıldığında seçili satıcı hesabı ve bir kullanıcı istemek için. İş akışının bir parçası olarak, Dynamics 365 for Operations'ta yeni bir kullanıcı oluşturulur ve güvenlik rolleri atanır. Buna ek olarak, Azure portalı ile etkileşim başlatan ve yeni veya mevcut bir AAD hesabını Dynamics 365 for Operations kullanıcı hesabı ile ilişkilendiren bir Azure B2B hizmeti etkinleştirilir.

### <a name="inactivate-a-user"></a>Kullanıcıyı devre dışı bırakma

İlgili kullanıcının satıcı iş birliğine olan erişimini kaldırmanın iki yolu bulunmaktadır:

-   Satıcının **İlgili kişiler** sayfasındaki **Satıcı işbirliği erişimine izin verildi** seçeneğini ilgili kişi için **Hayır** olarak ayarlayın. Bu, ilgili kişinin bağlantıda olduğu her bir tüzel kişilik için tek tek yapılabilir. Bu seçenek yalnızca tedarik profesyonelleri tarafından kullanılabilir.
-   Tüm kullanıcı hesabını **Satıcı kullanıcısını devre dışı bırak** isteği göndererek devre dışı bırakın.

Bir kullanıcı devre dışı bırakılan olmadığını istemek için:

1.  Üzerinde **tüm kişiler** sayfasında,'ı **Yinele****satıcı kullanıcı**.
2.  **İş gerekçesi** alanına bir yorum yazın.
3.  **Gönder**'e tıklayın.

### <a name="modify-security-roles"></a>Güvenlik rollerini ayarlama

**Satıcı kullanıcı rolleri bakımını** sayfa aynı olup **provizyon satıcı kullanıcı** sayfa dışında güvenlik rollerinin listesini düzenlenebilir.  

Bir kullanıcı için güvenlik rolleri değiştirilir istemek için:

1.  Üzerinde **tüm kişiler** sayfasında,'ı **koru****satıcı kullanıcı rolleri**.
2.  **İş gerekçesi** alanına bir yorum yazın.
3.  **Kullanıcı rollerini koru** bölümünde, atamak istediğiniz güvenlik rollerini seçin veya kaldırmak istediklerinizin seçimini kaldırın.
4.  Click **Submit**.



