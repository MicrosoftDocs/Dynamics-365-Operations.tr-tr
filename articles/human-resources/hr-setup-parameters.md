---
title: Human Resources parametrelerini yapılandırma
description: Bu makalede, Dynamics 365 Human Resources'da şirkete özgü İK parametrelerinin nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 13a25d3f1f72d8053ed3951b036522cfa3a15959
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065659"
---
# <a name="configure-human-resources-parameters"></a>Human Resources parametrelerini yapılandırma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Human Resources parametrelerinin ayarları şirketler arasında paylaşılır ancak diğer parametrelerin ayarları şirkete özeldir. Bu makalede, şirkete özgü Human Resources parametrelerinin nasıl ayarlanacağı açıklanmaktadır.

İki sayfa Human Resources parametrelerini ayarlamak için kullanılır. Şirketler arasında paylaşılan parametreler için **İnsan Kaynakları paylaşılan parametreleri** sayfasını kullanırsınız. Şirkete özel parametreler için **İnsan kaynakları parametreleri** sayfasını kullanırsınız.

![Human Resources parametrelerini yapılandır'a gidin.](./media/hr-employee-self-service-human-resources-parameters.png)

**İnsan Kaynakları parametreleri** sayfasında ayarlar altı sekmeye ayrılır:

- **Genel**
- **İşe alım** (bu sekme Dynamics 365 Human Resources'a dahil değildir)
- **Maaş**
- **Numara serileri**
- **FMLA**
- **Personel self servisi**
- **Yönetici self servisi**
- **Kazanç yönetimi**
- **İzin ve devamsızlık**
- **Ödeme yöntemleri**

Her sekme, tek bir şirketle ilgili bilgileri içerir.

## <a name="general"></a>Genel

**genel** sekmesindeki ayarlar, Devamsızlık, yaralanma ve hastalık ve yeni işe alma hakkında bilgi görünümünü belirler. Bu sekmedeki ayarlar, çalışırken görünen bazı varsayılan girdileri de tanımlar. Özellikle, bu sekme şunları sağlar:

- Açık devamsızlık hareketlerine uygulanacak rengi seçme.
- Raporlar için kullanılacak stil sayfasını belirtme.
- Eğitim kursları ve devamsızlık kaydı arasındaki tümleştirmeyi etkinleştirme.
- Bu tümleştirmeyi denetlemek için kullanılan devamsızlık kodunu seçme.
- Yaralanma ve hastalık durumlarının ne kadar süreyle saklanılacağını belirtme.
- Yeni bir çalışan işe alındığında gösterilen varsayılan kimlik numarasını belirtme.
- Hizmet yıllarını hesaplamak için kullanılacak tarihi belirtin. 

![Genel sekmesi.](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>İşe alma

**İşe Alım** sekmesindeki ayarlar, başvuru sahiplerine otomatik olarak gönderilen yazışmalar için kullanılan belge türlerini tanımlar. Talep edilmemiş başvurular için kullanılan işe alım projesini de belirtebilirsiniz.

**İşe alma projesi eskimesi** için tanımlanan dönem,işe alma **İşe alma yönetimi** çalışma alanındaki **Eskiyen projeler** kutucuğuna dahil edilen işe alma projesini belirleyen işe alma projeleri belirler. Uygulama son başvuru tarihi uyarısı için tanımlanan dönem **işe alma** çalışma alanındaki **son başvuru tarihi yaklaşan** döşemesindeki son başvuru tarihi yaklaşan işe alma projeleri görüntülemek için kullanılan uygulama son uyarısı için kullanılır.

İşe alma hakkında daha fazla bilgi için bkz. [İş adaylarını işe alma](hr-personnel-recruit.md).

## <a name="compensation"></a>Maaş

Dynamics 365 Finance'te **Ücret** sekmesindeki ayarlar, kullanıcının bir sabit veya değişken ücret planı bilgilerini kaydetmek istediklerini onaylamaları gerekip gerekmediğini tanımlar. **Kaydetme doğrulamasını etkinleştir**'i işaretlerseniz kullanıcılar ücretle ilgili bir sayfayı kapatmak istediklerinde kaydı kaydetmek isteyip istemediklerini soran bir ileti alır. Ücret yönetimindeki bazı sayfalar kullanıcıların bilgileri silmesine izin vermez. Kullanıcılardan bilgilerinin kaydedilmesini istediklerini doğrulamalarını isteyerek, kaydedilen daha sonra silinemez bilgi miktarını sınırlama olanağınız olabilir. **Kaydetme doğrulamasını etkinleştir** seçimini kaldırırsanız kayıtlar, büyük olasılıkla kullanıcı hazır olmadan önce hemen kaydedilir. Performans yönetimi'ni kullanıyorsanız **Ücret** sekmesi performansı değerlendirirken tazminat planlarına atanan model yerine bir değerlendirme modeli kullanmayı seçmenizi sağlar.

Human Resources'da, ücret planlarına erişimi kısıtlamayı ve varsayılan bir para birimi ayarlamayı seçmek için **Ücret** sekmesini kullanabilirsiniz.

> [!NOTE]
> Birleştirilmiş altyapıda **İnsan kaynakları parametreleri** sayfasının **Ücret** sekmesindeki varsayılan **Para birimi** parametresi kaldırıldı. İleriye dönük olarak mevcut finans ve operasyonlar işlevleriyle ilgili çakışma olmamasını ve tekrarlanan öğe oluşmasını önlemek için para birimi, **Kayıt defteri para birimi** parametresini ele alınır. Kayıt defteri para birimi işlevlerinin nasıl kullanılacağı hakkında daha fazla bilgi için bkz. [Kayıt defterleri yapılandırma](/general-ledger/configure-ledger#configuring-currencies-for-the-ledger.md). 

Ücret hakkında daha fazla bilgi için bkz. [Ücret planlarına genel bakış](hr-compensation-overview.md).

## <a name="number-sequences"></a>Numara serileri

**Numara serisi** sekmesindeki ayarlar, Human Resources'daki öğelere otomatik olarak kimlik atamak için kullanılan sıraları belirler. Örneğin:

- Başvurular
- Devamsızlık kayıtları
- Ücret işlemi sonuçları
- Servis talebi numaraları
- Kurslar
- Kurs konu başlıkları

Numara serisi referanslarını ve kodlarını korumak için **Numara serileri** listesi sayfasını kullanın (**Kuruluş yönetimi > Numara serileri > Numara serileri**'ni seçin).

Daha fazla bilgi için bkz. [Numara serilerine genel bakış](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

> [!NOTE]
> Çalışılan saat sayısı 1250'yi aşamaz ve 12 ay İstihdam uzunluğunu aşamaz. Bu en büyük değerler Amerika Birleşik Devletleri'nde federal yasalara uygundur.

![Numara serileri sekmesi.](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

FMLA sekmesinde FMLA uygunluk gereksinimlerini ve FMLA destek hakkı saatlerini ayarlarsınız. Daha fazla bilgi için bkz. [İzin ve devamsızlık parametreleri yapılandırma](hr-leave-and-absence-parameters.md).

![FMLA sekmesi.](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Personel self servisi

**Personel self servisi** sekmesindeki ayarlar, **Personel self servisi**'nin personele nasıl görüneceğine etki eder. Bu sekmede aşağıdaki görevleri tamamlayabilirsiniz:

- **Personel self servisi** çalışma alanı için ad girme
- Yöneticinin çalışanlar için hangi bilgileri girebileceğini seçme
- Çalışanlar için yararlı bağlantılar ekleme
- Çalışanların iletişim bilgilerini eklemelerini veya düzenlemelerini kısıtlama. Daha fazla bilgi için bkz. [Kişisel bilgileri düzenlemeyi kısıtlama](hr-employee-self-service-restrict-editing.md).

**Personel self servisi**'ni ayarlama hakkında daha fazla bilgi için bkz. [Personel ve Yönetici self servisi'ne genel bakış](hr-employee-manager-self-service-overview.md).

![Personel self servisi sekmesi.](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Yönetici self servis

**Yönetici self servisi** sekmesindeki ayarlar, yöneticilerin **Yönetici self servisinde** neler gördüğünü etkiler. Bu sekmede aşağıdaki seçenekleri yapılandırabilirsiniz:

- Süresi dolan kayıtlar için aralık
- Bilgi yöneticileri süresi dolan kayıtları görüntüleyebilir
- Yöneticilerin genişletilmiş raporlar için açık pozisyonları görüntüleyip görüntüleyemeyeceği
- Çıkış yapan çalışanların görünümleri
- Yöneticiler için yararlı bağlantılar

**Yönetici self servisi**'ni ayarlama hakkında daha fazla bilgi için bkz. [Personel ve Yönetici self servisi'ne genel bakış](hr-employee-manager-self-service-overview.md).

![Yönetici self servisi sekmesi.](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Kazanç yönetimi

**Kazanç yönetimi** sekmesinde, Kazanç yönetimi için e-posta seçeneklerini yapılandırabilirsiniz. Kazanç yönetimini ayarlama ve kullanma hakkında bilgi için bkz. [Kazanç yönetimine genel bakış](hr-benefits-management-overview.md).

![Kazanç yönetimi sekmesi.](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>İzin ve devamsızlık

İzin ve devamsızlığı ayarlama ve kullanma hakkında daha fazla bilgi için bkz. [İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Ödeme yöntemleri

**Ödeme yöntemleri** sekmesinde, kuruluşunuz tarafından desteklenen ödeme yöntemlerini seçebilirsiniz. Ücretleri yapılandırma hakkında daha fazla bilgi için bkz. [Ücret planlarına genel bakış](hr-compensation-overview.md).

![Ödeme yöntemleri sekmesi.](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
