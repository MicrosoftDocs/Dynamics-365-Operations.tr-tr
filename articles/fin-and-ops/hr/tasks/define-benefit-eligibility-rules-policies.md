---
title: Kazanç uygunluk kurallarını ve ilkelerini tanımlama
description: Bu kayıt, size yeni kazanç uygunluk kuralları ve ilkeleri oluşturmayı ve daha sonra kuralları kazançlara atamayı gösterir.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d35266c95cfbf3473a14fec47a1c748229dd25
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510612"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Kazanç uygunluk kurallarını ve ilkelerini tanımlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu kayıt, size yeni kazanç uygunluk kuralları ve ilkeleri oluşturmayı ve daha sonra kuralları kazançlara atamayı gösterir.  

Bu kaydı oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Kazanç uygunluk ilkesi kural türü yaratın
1. İnsan Kaynakları > Kazançlar > Uygunluk > Kazanç uygunluk ilkesi ve kural türleri'ne tıklayın.
2. Yeni'ye tıklayın.
3. Kural adı alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Sorgu adı alanında, açılır menü düğmesine tıklayarak aramayı açın.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Kaydet'e tıklayın.
8. Sayfayı kapatın.

## <a name="benefit-eligibility-policy"></a>Kazanç uygunluğu ilkesi
1. İnsan Kaynakları > Kazançlar > Uygunluk > Kazanç uygunluk ilkeleri'ne tıklayın.
2. Varolan bir kazanç ilkesi seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. İlke kuruluşu bölümlerinin genişletimesini değiştirin.  Burada ilkesine dahil etmek istediğiniz kuruluşları ekleyebilir ve kaldırabilirsiniz.
5. İlke kuralları bölümünü genişletin veya daraltın.
6. Daha önce oluşturduğunuz ilke kuralını listede bulun.
7. İlke kuralı oluştur'a tıklayın.
8. Etkin tarih alanında, ilkenin etkin hale gelmesini istediğiniz tarihi girin.
    * Etkili ve bitiş tarihlerini girmek, ilke kurallarında gelecekte değişiklik yapmanıza ve bu değişikliklerin etkin olmasını istediğiniz zamanda bu ilkeye geri dönmenize olan gereksinimi kaldırır.  
9. 
    * Kuralın sadece Satış Yöneticilerine uygulanmasını istiyorsanız, Nerede yan tümcesini şunun olacağı şekilde oluşturursunuz: Pozisyon tanımının Satış Yöneticisine eşit olduğunda.  Birden çok Nerede ifadesini Ve/veya ifadeleri ile birlikte kullanabilirsiniz.  
10. Tamam'a tıklayın.
11. Sayfayı kapatın.
12. Sayfayı kapatın.

## <a name="assign-rule-to-benefit"></a>Kuralı, kazanca atayın
1. İnsan kaynakları > Kazançlar > Kazançlar seçeneğine gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Uygunluk kuralları bölümünü genişletin veya daraltın.
5. Düzenle'yi tıklatın.
6. Uygunluk alanında listeden Kurala göre'yi seçin.
7. Kural türü alanında, aramayı açmak için açılır menü düğmesini tıklatın.
8. Listede, önceden oluşturduğunuz kuralı bulun ve seçin.
9. Listede, seçili satırdaki bağlantıya tıklayın.
10. Kaydet'e tıklayın.
11. Formu kapatın.

