---
title: Kazanca uygunluk kurallarını ve ilkelerini tanımlama
description: Bu makale, size yeni kazanç uygunluk kuralları ve ilkeleri oluşturmayı ve daha sonra kuralları kazançlara atamayı gösterir.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: df517e1ab72634cb434411fab3bd92bf34c7e609
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805958"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Kazanca uygunluk kurallarını ve ilkelerini tanımlama

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, size yeni kazanç uygunluk kuralları ve ilkeleri oluşturmayı ve daha sonra kuralları kazançlara atamayı gösterir.  

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