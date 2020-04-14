---
title: Görev ayrımını ayarlamak
description: Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 712cc90bef4f3ad56291e99edd9f963ae88add48
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143524"
---
# <a name="set-up-segregation-of-duties"></a>Görev ayrımını ayarlamak

[!include [banner](../../includes/banner.md)]

Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz. Bu kavram, görev ayrımı adını taşır. Örneğin, malların giriş kabul etmek ve satıcının ödemesini işlemek için aynı kişi istemeyebilirsiniz. Görevlerin ayrılması dolandırıcılık riskini azaltır, hataları ve düzensizlikleri tespit etmenizi kolaylaştırır. Görev ayrımlarını ayrıca dahili denetim kurallarının uygulanması için de kullanabilirsiniz. Bir kural yaratmak için aşağıdaki yordamı takip edin. Bu yordamı tamamlamak için sistem yöneticisi olmanız gerekir. Bu yöntemi oluşturmak için kullanılan demo verisi şirketi DAT'dir. 

1. **Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Görev ayrımı > Görev ayırma kuralları**'na gidin.
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

