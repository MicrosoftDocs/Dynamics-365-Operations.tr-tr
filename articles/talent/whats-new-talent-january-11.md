---
title: Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (11 Ocak 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent - Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d49a4aca368e3de10ae37b56c6d286d78f7f369a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462847"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a>Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (11 Ocak 2019)

**Derleme 8.1.2100**

Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes"></a>Değişiklikler

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>Bırakma taleplerini kullanılabilir bakiye tahminine göre doğrula
Bu sürümde yapılan değişiklikleri, çalışanların gelecekteki izin sürelerini mevcut bakiyelerinden çıkartmadan talep etmelerine olanak sağlar. Standart iş akışları gelecekte yapılacak istekler için kullanılacaktır. Daha fazla bilgi için [Çalışılan saatlere dayanarak zaman tahakkuk](leave-accrue-hours-worked.md) okuyun.

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>ESS ve Kişiler içinde tahmin edilen izin bakiyesini görüntüleyin
Bu özellik, gelecekteki izin bakiyelerinin İK, yöneticiler ve çalışanlar tarafından görüntülenmesine izin verir. Çalışanlar, gelecekteki bakiyelere **Çalışan Self Servis** çalışma alanında görebilirler ve İK aynı bilgiye **Kişiler** çalışma alanından sahiptir.

### <a name="notifications-for-changing-leave-balances"></a>İzin bakiyelerini değiştirmek için bildirimler
İzin bakiyeleri çalışanın geçerli bakiyesini görüntüler. Gelecekteki bakiyeler, **Çalışan Self Servisi** ve **Kişiler** çalışma alanında, tahmin edilen bakiyeyi hesaplamak için bir "başlangıç tarihi" girilerek kullanılabilir.

Aşağıdaki alanlarda tahmin edilen bakiyeleri görüntülemek için gezinti eklendi:
  - **Çalışan Self Servisi** çalışma alanında **İzin süresi** kartı.
  - **İzin ve devamsızlık** kartında, **Yönetici Self Servisi** çalışma alanında.
  - **Kişiler** çalışma alanında **İzin ve devamsızlık**.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>Değişken ücret planları için ondalıklara izin ver (Nakit planları)
Değişken nakit ödülleri ve planları şimdi ondalık tutarlar ve geçersiz kılmalar için ek esnekliğe sahiptir.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>Değişken ücret kayıtları üzerindeki tarihler, plan kaydedildikten sonra değiştirilemiyor
Bu değişiklik, plan kaydedildikten sonra planın bitiş tarihinin güncelleştirilmesine izin verir (genişletilmiş veya süresi dolmuş). Planları başlangıç ve bitiş tarihlerinden bağımsız olarak hala etkinleştirebilir veya devre dışı bırakabilirsiniz.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>Bordro bilgisi Bordro yöneticisi güvenlik rolü atandığında kullanılabilir
Bordro Yöneticisi rolü, talep işlemi sırasında bordro bilgisine erişim sahibi olmak üzere güncelleştirildi.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Çalışan Self-Servis | Konum hiyerarşisini açılan kutusundan ana düğüm alamıyor
Pozisyon hiyerarşisini yeni bir çalışma alanına eklerken ve kuruluş yapısı içinde gezinirken ortaya çıkan bir hatayı gidermek için değişiklikler yapıldı.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>Personel numara serisi kullanımda olduğunda yeni doğrulama iletisi
Bir çalışanı işe aldığınızda ve bir sonraki personel numarası kullanımda olduğunda sorunu açıklığa kavuşturmak için bir değişiklik yapıldı.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>Çalışan Self Servisi çalışma başlangıç sayfası olarak seçili
**Çalışan self servisi** çalışma alanı, bir kullanıcı için başlangıç sayfası olarak seçildi ve bu kullanıcı bir çalışan rolüne atanmış olmadığında, sistem varsayılan panoya yönlendirir.

### <a name="termination-reason-code-updates-position-assignment-record"></a>İşten çıkarma kodu, pozisyon atama kaydını güncelleştirir
Sonlandırma neden kodu şimdi pozisyon atamasını, bir çalışanı işten çıkarırken ve pozisyonu sonlandırırken güncelleştirilir. 
