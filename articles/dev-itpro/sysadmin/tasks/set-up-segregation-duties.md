--- 
title: "Görev ayrımını ayarlamak"
description: "Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz."
author: maertenm
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 2ab30f4326b627406f9a39d6c3203b181b67d68f
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-segregation-of-duties"></a>Görev ayrımını ayarlamak

[!include[task guide banner](../../includes/task-guide-banner.md)]

Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz. Bu kavram, görev ayrımı adını taşır. Örneğin, malların giriş kabul etmek ve satıcının ödemesini işlemek için aynı kişi istemeyebilirsiniz. Görevlerin ayrılması dolandırıcılık riskini azaltır, hataları ve düzensizlikleri tespit etmenizi kolaylaştırır. Görev ayrımlarını ayrıca dahili denetim kurallarının uygulanması için de kullanabilirsiniz. Bir kural yaratmak için aşağıdaki yordamı takip edin. Bu yordamı tamamlamak için sistem yöneticisi olmanız gerekir. Bu yöntemi oluşturmak için kullanılan demo verisi şirketi DAT'dir. 

1. Sistem Yönetimi > Güvenlik > Görev ayrımı > Görev ayrımı kuralları seçeneğine gidin.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
    * Kural için bir isim girin.  
4. Birinci görev alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, istenen kaydı bulun ve seçin.
    * Kural tarafından denetlenen ilk görevi seçin.  
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. İkinci görev alanında, aramayı açmak için açılır menü düğmesine tıklayın.
8. Listede, istenen kaydı bulun ve seçin.
    * Kural tarafından denetlenen ikinci görevi seçin.  
9. Listede, seçili satırdaki bağlantıya tıklayın.
10. Önem alanında, bir seçenek seçin.
    * Aynı kullanıcının veya rolün her iki görevi de gerçekleştirdiğinde oluşacak riskin önemini seçin.  
11. Güvenlik riski alanına bir değer yazın.
    * Güvenlik riski için bir açıklama girin.  
12. Risk azaltma alanına bir değer yazın.
    * Güvenlik riskini ortadan kaldırmak için yapılacaklar eylemler için bir açıklama girin. Örneğin, işlemi daha ayrıntılı inceleyerek, aylık yönetim incelemesi yapılmasını veya kaynakların diğer departmanlarla paylaşılmasını sağlayarak riski azaltabilirsiniz.  
13. Kaydet'e tıklayın.


