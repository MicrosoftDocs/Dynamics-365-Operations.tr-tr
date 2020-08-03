---
title: Kazanç yönetimi parametrelerini ayarlama
description: Microsoft Dynamics 365 Human Resources'Ta sosyal haklar yönetimiyle ilgili parametreleri yapılandırın.
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85bbe5d3b422f2f29f1d1fe8ee269b407da691c2
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599368"
---
# <a name="set-benefits-management-parameters"></a>Kazanç yönetimi parametrelerini ayarlama

Microsoft Dynamics 365 Human Resources'ta çıkış planları kurmadan önce, kazançlar yönetimi parametrelerini yapılandırmanız gerekir. Bu parametreler varsayılan değerleri, neden kodları ve diğer seçenekleri ayarlar.

## <a name="configure-general-parameters"></a>Genel parametrelerini yapılandırma

1. **Kazanç yönetimi** çalışma alanında, **Kurulum** altında **İnsan Kaynakları Paylaşılan Parametreleri**'ni seçin.

2. **Genel** sekmesinde, aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Ülke/bölge** | **Ülke/bölge** alanı, posta kodlarının/durumlarının görüntülenme düzenini belirler. Seçili ülke, aşağı açılan listede ilk olarak görüntülenir. |
   | **Kayıt nedeni kodu** | Açık kayıt işleme sırasında çalışan planları oluşturulduğunda kullanılacak varsayılan neden kodunu seçin. |
   | **İptal nedeni kodu** | Bir çalışan avantajı planı iptal edildiğinde kullanılacak neden kodu. İptal işlemi sırasında bir iletişim kutusunda görüntülenir. Gerekirse, kullanıcılar bunu **iptal nedeni kodu** ile değiştirebilir. |
   | **Neden kodunu yeniden aç** | Bir çalışan avantajı planı yeniden açıldığında kullanılacak neden kodu. İptal işlemi sırasında bir iletişim kutusunda görüntülenir. Gerekirse, kullanıcılar bunu **Yeniden açma neden kodu** ile değiştirebilir. | 
   | **Yaşam olayı neden kodu** | Ömür olayı oluştuğunda kullanılacak neden kodu. |
   | **Oran değişikliği neden kodu** | Güncelleştirme oranı değişimi sürecinde bir çalışan avantajı planının iptal edilmesi ve yeniden açma işlemi sırasında kullanılacak neden kodu. Güncelleştirme oranı değişimi işlemi oran ile hangi kayıtların değiştiğini gösterir. |
   | **Kazanç yıllık maaş** | Bir personel için **Kazanç yıllık maaş** tutarını ayarlamanıza olanak tanır. Human Resources, karşılama tutarlarını belirlerken yıllık sabit ücret tutarı yerine **Kazançlar yıllık maaş** alanını kullanacaktır. |
   | **Yeni işe alınan kişi uygun** | Yeni işe alımların uygun olduğunu belirtir. |
   | **Yeni işe alma kaydı dönemi** | Yeni işe alma kaydına izin verildiği zaman dilimi.</br></br>**Not**: Bu ayar, plan uygunluğu kuralında ayarladığınız tüm yeni işe alma dönemini geçersiz kılar. |
   | **Varsayılan ödeme sıklığı** | Yeni çalışanlar eklendiğinde kullanılacak varsayılan ödeme sıklığı. |
   | **Yaşam olayları etkin** | Yaşam olaylarını etkinleştirir. |
   | **Eski kazanç formlarını gizle** | Eski kazanç formlarını gizlemenizi sağlar. |

3. **Kaydet**'i seçin.

## <a name="configure-employee-self-service-parameters"></a>Personel self servisi parametrelerini yapılandırma

1. **Kazanç yönetimi** çalışma alanında, **Kurulum** altında **İnsan Kaynakları Parametreleri**'ni seçin.

2. **Personel self servisi** sekmesinde, aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Kazanç doğrulaması** | Kendi kendine faydaların kullanıma alma sırasında kullanılacak doğrulama metni. |
   | **Görevlileri otomatik olarak seç** | Plan seçeneklerine uygunluğuna göre otomatik olarak bağımlılar ve lehdarlar oluşturulup oluşturulmayacağını belirtir. |

3. **Kaydet**'i seçin.
