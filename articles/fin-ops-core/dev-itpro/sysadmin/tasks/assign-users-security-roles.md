---
title: Kullanıcıları güvenlik rollerine atama
description: Finance and Operations uygulamalarına erişmek için kullanıcıların güvenlik rolleri atanmış olmalıdır.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0744f45ac91dfb9b5aae35091e3675202c9144f9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143582"
---
# <a name="assign-users-to-security-roles"></a>Kullanıcıları güvenlik rollerine atama

[!include [banner](../../includes/banner.md)]

Ortak yetenekler dışında herhangi bir şey kullanmak için, kullanıcıların güvenlik rollerine atanması gerekir. Bu yordam sistem yöneticilerinin kullanıcıları iş verilerine dayalı olarak rollere otomatik olarak nasıl atayabileceklerini açıklar. 

## <a name="automatically-assign-users-to-roles"></a>Kullanıcıları rollere otomatik olarak ata
1. **Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Kullanıcılara roller atayın**'a gidin.
2. Ağaçta, 'Muhasebe yöneticisi' seçin. Kuralı yapılandırmak istediğiniz rolü seçin. Bu örnekte, Muhasebe yöneticisi'ni seçin. 
3. İletişim kutusunu açmak için **Kural ekle**'ye tıklayın.
4. **Sorgu seçin**listesinde, istenen kaydı bulun ve seçin. Bu kuralda kullanılacak sorguyu seçin.  
5. **Üyelik kuralı adı** listesinde, seçili satırdaki bağlantıya tıklayın.
6. **Sorguyu düzenle**'ye tıklayın. Sorguyu gerektiği gibi düzenleyin.  
7. **Tamam**'a tıklayın.
8. **Otomatik rol atamayı çalıştır**'a tıklayın.
9. **Gezinti bölmesi > Modüller > Sistem yönetimi > Kullanıcılar > Kullanıcılar**'a gidin (ideal olarak ayrı bir tarayıcı sekmesinde).
10. Rol atama sorgusunun doğru olduğunu onaylamak için çeşitli kullanıcılara atanan rolleri gözden geçirin. Gerekirse ayarlayın ve yeniden çalıştırın.

## <a name="exclude-users-from-automatic-role-assignment"></a>Kullanıcıları otomatik rol atamasının dışında bırakmak
1. Sayfayı kapatın.
2. **Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Kullanıcılara roller atayın**'a gidin.
3. Ağaçta, 'Muhasebe yöneticisi' seçin. Bir rol seçin. Bu örnek için, Muhasebe yöneticisi'ni seçin.  
4. **Role atanmış kullanıcılar** menüsünde, **Kullanıcıları el ile ata/dışarıda tut**'u seçin.
5. **Kullanıcıları role atayın veya rol dışında bırakın** listesinde, seçili satırları işaretleyin. Bir kullanıcı seçin.  
6. **Eylem bölmesi**'nde, **Rol dışında bırakın**'ı seçin.
    
    Seçili kullanıcıları rolün dışında bırakmak için **Rol dışında bırakın**'ı seçin. Dışarıda bırakmaları kaldırmak için, hariç tutulma durumunu kaldırmak istediğiniz kullanıcıları seçin ve sonra **Durumu sıfırla**'ya tıklayın. Bir kullanıcının durumunu sıfırlayarak bir hariç tutmayı kaldırdığınızda, kullanıcının rolü otomatik olarak atanır. Ancak, durumunu sıfırladığınızda, kullanıcı hemen role atanmaz veya rolden hariç tutulmaz. Bunun yerine kullanıcı otomatik rol atama bir sonraki çalıştığında rolüne eklenir veya çıkartılır.  
