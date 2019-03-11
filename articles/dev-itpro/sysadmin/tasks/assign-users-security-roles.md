---
title: Kullanıcıları güvenlik rollerine atama
description: Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a erişmek için kullanıcıların güvenlik rolleri atanmış olmalıdır.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "349964"
---
# <a name="assign-users-to-security-roles"></a>Kullanıcıları güvenlik rollerine atama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a erişmek için kullanıcıların güvenlik rolleri atanmış olmalıdır. Bu yordam sistem yöneticilerinin kullanıcıları iş verilerine dayalı olarak rollere otomatik olarak nasıl atayabileceklerini açıklar. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


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

