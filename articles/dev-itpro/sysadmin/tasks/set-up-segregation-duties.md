---
title: Görev ayrımını ayarlamak
description: Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68e1a4419eaa11a59e1b634deb8e76a2bb9b6fdf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "318799"
---
# <a name="set-up-segregation-of-duties"></a>Görev ayrımını ayarlamak

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

