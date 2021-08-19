---
title: Paylaşılan parametrelerini yapılandırma
description: Konum kayıtları gibi şirketler arasında paylaşılan kayıtlar için paylaşılan parametreleri ayarlamanız gerekir. Bu makalede, tüzel kişilikler arasında İnsan kaynakları parametrelerinin nasıl ayarlandığı açıklanmaktadır.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66f57c9613ba04ebb3748699105469586c27d66131c062d1af286b24199c4be7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723659"
---
# <a name="configure-shared-parameters"></a>Paylaşılan parametrelerini yapılandırma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Konum kayıtları gibi şirketler arasında paylaşılan kayıtlar için paylaşılan parametreleri ayarlamanız gerekir. Bu makalede, tüzel kişilikler arasında İnsan kaynakları parametrelerinin nasıl ayarlandığı açıklanmaktadır.

Bazı kayıt türleri konum kayıtları gibi şirketler arasında paylaşılır. Bu kayıtlar için paylaşılan parametreleri ayarlamanız gerekir. Örneğin, **İnsan Kaynakları parametreleri paylaşılan** sayfasını tüzel kişilikler arasında İnsan Kaynakları parametreleri ayarlamak için kullanırsınız. 

**İnsan Kaynakları paylaşılan parametreleri** sayfasında, parametreler kendi işlevselliğine dayalı alanlar halinde gruplandırılır. 

### <a name="settings"></a>Ayarlar
**kimlik** sekmesinde sayfada listelenen kimlik numaralarını temsil eden kimlik türleri seçmelisiniz. Çalışanlar için kimlik bilgilerini girmeden önce kimlik tiplerini ayarlamanız gerekir. Sosyal Güvenlik numarası, Ulusal kimlik numarası, yabancı kimlik numarası ve kişisel kimlik kodu hakkında bilgiler **kimlik türü** sayfasında saklanır. Yeni bir kimlik türü tanımlamak veya mevcut türlerin listesini gözden geçirmek için **Personel yönetimi** &gt; **Bağlantılar sekmesi** &gt; **Kurulum** &gt; **Kimlik türleri**'ne tıklayın. Basit bir kod ve açıklama girebilirsiniz. 

**Numara sıraları** sekmesinde, aşağıdaki kayıtlar için kullanılan numara serilerini seçebilirsiniz: Personel numarası, pozisyon, kullanıcı isteği kimliği, I-9 belgesi, başvuran, tartışma, yararı kimliği ve personel eylem (Bu kayıt türü etkinleştirilmişse). Numara serisi referanslarını ve kodlarını tanımlamak için **Numara serisi** listesi sayfasını kullanın. Bu sayfayı bulmak için sayfa arama özelliğini kullanın. 

**pozisyonlar** sekmesinde, varsayılan olarak atama için kullanılabilir olan yeni pozisyonlar olup olmadığını gösterin:

- **Her zaman** – Pozisyonlar oluşturulurken çalışanları yeni pozisyonlara atayamazsınız. Pozisyonlar oluşturulurken, **Pozisyon** sayfasının **Genel** sekmesindeki **Atama için kullanılabilir** tarih ve saat, oluşturma tarihi ve saatine otomatik olarak ayarlanır.
- **Hiçbir zaman** – pozisyonlar oluşturduğunuzda yeni konumlara çalışanları atayamazsınız. Bu seçeneği seçerseniz, her yeni pozisyon kullanılabilir hale geldiğinde **Pozisyon** sayfasını açmanız gerekir. Daha sonra, **Genel** sekmesinde, çalışan atamasını etkinleştirmek üzere **Atama için kullanılabilir** tarihini girin.

**Gelişmiş erişim** sekmesinde, bazı bilgilere veya bağlantılara erişimi kısıtlayabilirsiniz:

- **Çalışan bilgilerine erişimi kısıtla** – Kullanıcıların yalnızca erişebileceği tüzel kişilikler için çalışan bilgilerini ve söz konusu tüzel kişiliklerde istihdam edilen çalışanlarla ilgili bilgilieri görüntüleyebilmeleri için bu özelliği etkinleştirin.

    Bu özellik etkinleştirildikten sonra, görünümü sınırlanması gereken her kullanıcıya uygun izinleri ayarlamak için aşağıdaki adımları izlemeniz gerekir:

    1. **Kullanıcılar** sayfasında bir kullanıcı seçin.
    1. Kullanıcı için bir rol seçin. **Kuruluşları ata** seçeneği kullanılabilir.
    1. **Kuruluşlar ata**'yı seçin.
    1. Yeni sayfasında, **Belirli kuruluşlara özel olarak erişim ver** seçeneğini belirleyin ve sonra da kullanıcının erişebileceği kuruluşları seçin.
    1. Sistem Kullanıcı rolü de dahil olmak üzere, kullanıcının sahip olduğu her rol için 2 ile 4 arasındaki adımları yineleyin.

    > [!NOTE]
    > Bir kullanıcının erişimi olan şirketler, tüm Kullanıcı rolleri arasında eşleşmelidir.

- **Şirketler arası ücret görünümünü etkinleştir** – Çalışanlar için ücret, yasal iş tüzel kişiliği bazında atanır. Bazen bir çalışan aynı anda çoklu tüzel kişilikler içinde çalışabilir. Bu özellik etkinleştirildiğinde, geçerli varlıkları değiştirmenizi gerektirmeden, her tüzel kişilikle ilgili ücret Çalışan Self-Servisi ve yönetici self servisinde görünür. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
