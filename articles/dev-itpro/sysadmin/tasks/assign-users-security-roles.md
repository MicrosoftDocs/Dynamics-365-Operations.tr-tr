--- 
title: "Kullanıcıları güvenlik rollerine atama"
description: "Microsoft Dynamics 365 for Finance and Operations, Enterprise edition erişimi sağlamak için kullanıcıların güvenlik rollerine atanmış olmaları gerekir."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 551048af26f46d334c562d1968963aed262a5e03
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="assign-users-to-security-roles"></a>Kullanıcıları güvenlik rollerine atama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Microsoft Dynamics 365 for Finance and Operations, Enterprise edition erişimi sağlamak için kullanıcıların güvenlik rollerine atanmış olmaları gerekir. Bu yordam sistem yöneticilerinin kullanıcıları iş verilerine dayalı olarak rollere otomatik olarak nasıl atayabileceklerini açıklar. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="automatically-assign-users-to-roles"></a>Kullanıcıları rollere otomatik olarak ata
1. Sistem Yönetimi > Güvenlik > Kullanıcılara roller atayın'a gidin.
2. Ağaçta, 'Muhasebe yöneticisi' seçin.
    * Kuralı yapılandırmak istediğiniz rolü seçin. Bu örnekte, Muhasebe yöneticisi'ni seçin.  
3. İletişim kutusunu açmak için Kural ekle'yi tıklatın.
4. Listede, istenen kaydı bulun ve seçin.
    * Bu kuralda kullanılacak sorguyu seçin.  
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Sorguyu düzenle'ye tıklayın.
    * Sorguyu gerektiği gibi düzenleyin.  
7. Tamam'a tıklayın.

## <a name="exclude-users-from-automatic-role-assignment"></a>Kullanıcıları otomatik rol atamasının dışında bırakmak
1. Sayfayı kapatın.
2. Sistem Yönetimi > Güvenlik > Kullanıcılara roller atayın'a gidin.
3. Ağaçta, 'Muhasebe yöneticisi' seçin.
    * Bir rol seçin. Bu örnek için, Muhasebe yöneticisi'ni seçin.  
4. Kullanıcıları el ile ata / dışarıda tut seçeneğini tıklatın.
5. Listede, seçili satırı işaretleyin.
    * Bir kullanıcı seçin.  
6. Rol dışında tut seçeneğini tıklatın.
    * Seçili kullanıcıları, rolün dışında bırakmak için, Rolün dışında bırak'ı tıklayın. Dışarıda bırakmaları kaldırmak için, hariç tutulma durumunu kaldırmak istediğiniz kullanıcıları seçin ve sonra Durum sıfırla'ya basın. Bir kullanıcının durumunu sıfırlayarak bir hariç tutmayı kaldırdığınızda, kullanıcının rolü otomatik olarak atanır. Ancak, durumunu sıfırladığınızda, kullanıcı hemen role atanmaz veya rolden hariç tutulmaz. Bunun yerine kullanıcı otomatik rol atama bir sonraki çalıştığında rolüne eklenir veya çıkartılır.  


