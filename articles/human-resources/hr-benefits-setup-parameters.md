---
title: Tüm şirketler için Kazanç yönetimi ve Personel self servisi parametrelerini ayarlama
description: Microsoft Dynamics 365 Human Resources uygulamasında Kazanç yönetimi ve Personel self servisi için parametreleri yapılandırın.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1bae79e47c3fa695ac239320eeee17b1a480f18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337083"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a>Tüm şirketler için Kazanç yönetimi ve Personel self servisi parametrelerini ayarlama



Microsoft Dynamics 365 Human Resources'ta kazanç planları kurmadan önce, kazançlar yönetimi parametrelerini yapılandırmanız gerekir. Bu parametreler varsayılan değerleri, neden kodları ve diğer seçenekleri ayarlar. 

## <a name="configure-general-parameters"></a>Genel parametrelerini yapılandırma

1. **Kazanç yönetimi** çalışma alanında, **Kurulum** altında **İnsan Kaynakları Paylaşılan Parametreleri**'ni seçin.

2. **Kazanç yönetimi** sekmesinde, aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Ülke/bölge** | **Ülke/bölge** alanı, posta kodlarının/durumlarının görüntülenme düzenini belirler. Seçili ülke, aşağı açılan listede ilk olarak görüntülenir. |
   | **Kayıt nedeni kodu** | Açık kayıt işleme sırasında çalışan planları oluşturulduğunda kullanılacak varsayılan neden kodunu seçin. |
   | **İptal nedeni kodu** | Bir çalışan avantajı planı iptal edildiğinde kullanılacak neden kodu. İptal işlemi sırasında bir iletişim kutusunda görüntülenir. Gerekirse, kullanıcılar bunu **iptal nedeni kodu** ile değiştirebilir. |
   | **Neden kodunu yeniden aç** | Bir çalışan avantajı planı yeniden açıldığında kullanılacak neden kodu. İptal işlemi sırasında bir iletişim kutusunda görüntülenir. Gerekirse, kullanıcılar bunu **Yeniden açma neden kodu** ile değiştirebilir. | 
   | **Yaşam olayı neden kodu** | Ömür olayı oluştuğunda kullanılacak neden kodu. |
   | **Oran değişikliği neden kodu** | Güncelleştirme oranı değişimi sürecinde bir çalışan avantajı planının iptal edilmesi ve yeniden açma işlemi sırasında kullanılacak neden kodu. Güncelleştirme oranı değişimi işlemi oran ile hangi kayıtların değiştiğini gösterir. |
   | **Kazanç yıllık maaş** | Bir personel için **Kazanç yıllık maaş** tutarını ayarlamanıza olanak tanır. İnsan Kaynakları, karşılama tutarlarını belirlerken yıllık sabit ücret tutarı yerine **Kazançlar yıllık maaş** alanını kullanacaktır. |
   | **Yeni işe alınan kişi uygun** | Yeni işe alımların uygun olduğunu belirtir. |
   | **Yeni işe alma kaydı dönemi** | Yeni işe alma kaydına izin verildiği zaman dilimi.</br></br>**Not**: Bu ayar, plan uygunluğu kuralında ayarladığınız tüm yeni işe alma dönemini geçersiz kılar. |
   | **Varsayılan ödeme sıklığı** | Yeni çalışanlar eklendiğinde kullanılacak varsayılan ödeme sıklığı. |
   | **Yaşam olayları etkin** | Yaşam olaylarını etkinleştirir. |
   | **Eski kazanç formlarını gizle** | Eski kazanç formlarını gizlemenizi sağlar. |
   | **Kazanç doğrulaması** | Kendi kendine faydaların kullanıma alma sırasında kullanılacak doğrulama metni. |
   | **Görevlileri otomatik olarak seç** | Plan seçeneklerine uygunluğuna göre otomatik olarak bağımlılar ve lehdarlar oluşturulup oluşturulmayacağını belirtir. |

3. **Kaydet**'i seçin.

## <a name="configure-employee-self-service-parameters"></a>Personel self servisi parametrelerini yapılandırma

1. **Kazanç yönetimi** çalışma alanında, **Kurulum** altında **İnsan Kaynakları Parametreleri**'ni seçin.

2. **Kazanç yönetimi** sekmesinde, aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Kazanç doğrulaması** | Self servis kazançların kullanıma alınması sırasında kullanılacak doğrulama metni. |
   | **Görevlileri otomatik olarak seç** | Plan seçeneklerine uygunluğuna göre otomatik olarak bağımlılar ve lehdarlar oluşturulup oluşturulmayacağını belirtir. |

3. **Kaydet**'i seçin.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
