---
title: Kazanca uygunluk kurallarını ve ilkelerini tanımlama
description: Bu konuda, kazanç uygunluk kuralları ve ilkelerinin nasıl oluşturulacağı ve ardından kuralların Kazançlara nasıl atanacağı açıklanmaktadır.
author: twheeloc
ms.date: 08/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 4781a00ae63bb2d27df0610a1886cc43e52798f9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861203"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Kazanca uygunluk kurallarını ve ilkelerini tanımlama


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, kazanç uygunluk kuralları ve ilkelerinin nasıl oluşturulacağı ve ardından kuralların kazançlara nasıl atanacağı açıklanmaktadır.  

## <a name="create-benefit-eligibility-policy-rule-type"></a>Kazanç uygunluk ilkesi kural türü yaratın

1. **İnsan kaynakları > Kazançlar > Uygunluk > Kazanç uygunluğu ilkesi kural türleri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Kural adı** alanına bir değer girin.
4. **Açıklama** alanında bir değer girin.
5. **Sorgu adı** alanında, açılır menü düğmesini seçerek aramayı açın.
6. Listeden, seçilen satırdaki bağlantıyı seçin.
7. **Kaydet**'i seçin.
8. Sayfayı kapatın.

## <a name="benefit-eligibility-policy"></a>Kazanç uygunluğu ilkesi

1. **İnsan kaynakları > Kazançlar > Uygunluk > Kazanç uygunluk ilkeleri**'ni seçin.
2. Varolan bir kazanç ilkesi seçin.
3. Listeden, seçilen satırdaki bağlantıyı seçin.
4. **İlke kuruluşları** bölümlerinin genişletilmiş görünümüne geçin. İlkeye dahil etmek istediğiniz kuruluşları ekleyebilir veya kaldırabilirsiniz.
5. **İlke kuralları** bölümünü genişletin veya daraltın.
6. Listede, daha önce oluşturduğunuz ilke kuralını bulun.
7. **İlke kuralı oluştur**'u seçin.
8. **Geçerlilik tarihi** alanına, ilkenin yürürlüğe girmesini istediğiniz tarihi girin.
    * Geçerlilik bitiş tarihleri ayarlamak, ilke kurallarında gelecekte değişiklikler yapmanıza olanak tanır, böylece bu değişikliklerin etkili olmasını istediğinizde ilkeye geri dönmenize gerek yoktur.  
9. Gerekirse, **Koşul ekle** alanına where yan tümcesi ekleyin.
    * Örneğin, kuralın yalnızca Satış Yöneticileri için geçerli olmasını istiyorsanız where yan tümcesini oluşturabilirsiniz: Where konum açıklaması Satış Yöneticisi'ne eşittir. Kuralda birden çok where deyimlerini birlikte ekleyebilirsiniz.  
10. **Tamam**'ı seçin.
11. Sayfayı kapatın.

## <a name="assign-rule-to-benefit"></a>Kuralı, kazanca atayın

1. **İnsan kaynakları > Kazançlar > Kazançlar**'a gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listeden, seçilen satırdaki bağlantıyı seçin.
4. **Uygunluk kuralları** bölümünü genişletin veya daraltın.
5. **Düzenle** öğesini seçin.
6. **Uygunluk** alanında, kuralı seçin.
7. **Kural türü** alanında, daha önce oluşturduğunuz kuralı seçin.
9. Listeden, seçilen satırdaki bağlantıyı seçin.
10. **Kaydet**'i seçin.
11. Formu kapatın.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
