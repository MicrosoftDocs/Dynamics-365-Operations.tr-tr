---
title: Görev ayrımını ayarlamak
description: Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c1521d6bbbe12964fef0942fcc4943f12a4360a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562509"
---
# <a name="set-up-segregation-of-duties"></a>Görev ayrımını ayarlamak

[!include [banner](../../includes/banner.md)]

Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz. Bu kavram, görev ayrımı adını taşır. Örneğin, aynı kişinin malların girişini kabul etmesini ve satıcıya ödemeyi işlemesini isteyebilirsiniz. Görevlerin ayrılması dolandırıcılık riskini azaltır, hataları ve düzensizlikleri tespit etmenizi kolaylaştırır. Görev ayrımlarını ayrıca dahili denetim kurallarının uygulanması için de kullanabilirsiniz. Bir kural yaratmak için aşağıdaki yordamı takip edin. Bu yordamı tamamlamak için sistem yöneticisi olmanız gerekir.

1. **Sistem yönetimi** > **Güvenlik** > **Görev ayrımı** > **Görev ayrımı kuralları**'na gidin.
2. **Yeni**'ye tıklayın.
3. **Ad** alanına kural için bir değer girin.
4. **İlk görev** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, istenen kaydı bulun ve seçin. Kural tarafından denetlenen ilk görevi seçin.
6. **İkinci görev** alanında, aramayı açmak için açılır menü düğmesine tıklayın. 
7. Listede, istenen kaydı bulun ve seçin. Kural tarafından denetlenen ikinci görevi seçin.
10. **Önem derecesi** alanında bir seçenek belirleyin. Aynı kullanıcının veya rolün her iki görevi de gerçekleştirdiğinde oluşacak riskin önemini seçin.  
11. **Güvenlik riski** alanına bir değer girin. Güvenlik riski için bir açıklama girin.  
12. **Güvenlik azaltma** alanına bir değer girin. Güvenlik riskini ortadan kaldırmak için yapılacaklar eylemler için bir açıklama girin. Örneğin, işlemi daha ayrıntılı inceleyerek, aylık yönetim incelemesi yapılmasını veya kaynakların diğer departmanlarla paylaşılmasını sağlayarak riski azaltabilirsiniz.     
13. **Kaydet**'e tıklayın.

> [!IMPORTANT] 
> Görev ayrımı kurallarına uygunluk, kural oluşturduğunuzda doğrulanmaz. Mevcut roller için çakışma oluşturan bir kural oluşturabilirsiniz. Mevcut kullanıcı rolü atamaları yeni kuralla çakışıyor da olabilir. Bir kuralı oluşturduktan veya değiştirdikten sonra uyumluluğu doğrulamanız gerekir. Daha fazla bilgi için bkz. [Görev ayrımındaki çakışmaları tanımlama ve çözümleme](identify-resolve-conflicts-segregation-duties.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]