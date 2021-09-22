---
title: MPOS ve Cloud POS için genişletilmiş oturum açma işlevini ayarlama
description: Bu konu Bulut POS ve Retail Modern POS (MPOS) için genişletilmiş oturum açma seçeneğini ayarlamada kullanabileceğiniz seçenekleri ele alır.
author: boycezhu
ms.date: 09/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0cc3d3a3cadbc614e82b8cc7ae0b78406247cece
ms.sourcegitcommit: efcb853a68a77037cca23582d9f6f96ea573727a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7478683"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a>MPOS ve Cloud POS için genişletilmiş oturum açma işlevini ayarlama

[!include [banner](includes/banner.md)]

Bu konu Bulut POS ve Retail Modern POS (MPOS) için genişletilmiş oturum açma seçeneğini ayarlamada kullanabileceğiniz seçenekleri ele alır.

## <a name="setting-up-extended-logon"></a>Genişletilmiş oturum açma ayarlaması

Barkod maskeleri ayarını **Retail ve Commerce** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **İşlevsellik profilleri**'nde bulabilirsiniz. **İşlevler** Hızlı Sekmesi genişletilmiş oturum açma ile ilgili aşağıdaki seçenekleri içerir.

### <a name="staff-bar-code-logon"></a>Personel barkod oturum açma işlemi

**Personel barkodla oturum açma** seçeneği etkinleştirilmişse, kendi satış noktası (POS) kimlik bilgilerine bir genişletilmiş oturum açma atanmış çalışanlar bir barkod kullanarak oturum açabilir.

### <a name="staff-bar-code-logon-requires-password"></a>Personelin barkodla oturum açması parola gerektirir

**Personel barkodla oturum açma parola gerektiriyor** seçeneği etkinleştirilmişse, personel barkodla oturum açma yalnızca mevcut genişletilmiş oturum açmaya atanan çalışanı seçer. Bu seçenek etkinleştirildiğinde, çalışanların gene de parolalarını girmesi gerekir.

### <a name="staff-card-logon"></a>Personel kart oturum açma işlemi

**Personel kartla oturum açma** seçeneği etkinleştirilmişse, kendi POS kimlik bilgilerine bir genişletilmiş oturum açma atanmış çalışanlar bir manyetik bant kullanarak oturum açabilir.

### <a name="staff-card-logon-requires-password"></a>Personelin kartla oturum açması parola gerektirir

**Personel kartla oturum açma parola gerektiriyor** seçeneği etkinleştirilmişse, personel kartla oturum açma yalnızca mevcut genişletilmiş oturum açmaya atanan çalışanı seçer. Bu seçenek etkinleştirildiğinde, çalışanların gene de parolalarını girmesi gerekir.

## <a name="assigning-an-extended-logon"></a>Genişletilmiş oturum açma ataması

Varsayılan olarak, yalnızca yöneticiler çalışanlara genişletilmiş oturum açma atayabilir. Genişletilmiş oturum atamak için POS içinde **Genişletilmiş oturum açma**'ya gidin. Daha sonra, çalışanın operatör kimliğini arama alanına girerek çalışanı arayın. Çalışanı seçip **Ata** öğesine tıklayın. Bir sonraki sayfada, çalışana atamak için genişletilmiş oturum açma kartını geçirin veya taratın. Kart geçirme veya tarama başarıyla okunursa, **Tamam** düğmesi kullanılabilir olur. O çalışan için genişletilmiş oturum açmayı kaydetmek için **Tamam** düğmesine tıklayın.

## <a name="deleting-an-extended-logon"></a>Genişletilmiş oturum açmanın silinmesi

Bir çalışana atanan genişletilmiş oturum açmayı silmek için, **Genişletilmiş oturum açma** işlemini kullanarak o çalışanı arayın. Çalışanı seçip **Atamayı Kaldır** öğesine tıklayın. Bu çalışan ile ilişkili olan tüm genişletilmiş oturum açma kimlik bilgileri kaldırılır.

## <a name="extending-extended-logon"></a>Genişletilmiş oturum açmanın genişletilmesi

Genişletilmiş oturum açmada yalnızca beş önemli karakterin kullanıma hazır benzersiz tanımlayıcı olmasına izin verilir. Örneğin, "1234567" ve "1234578" kimliklerine sahip iki kart yapılandırırsanız her ikisi de "12345" olarak kabul edilir. Daha fazla karakteri desteklemek için bir uzantı oluşturabilirsiniz. Ayrıntılı yönergeler için [MPOS ve Bulut POS için Genişletilmiş oturum açma işlevini genişletme](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/) bölümüne bakın.

Oturum açma hizmeti, avuç içi tarayıcılar gibi ek genişletilmiş oturum açma cihazları desteklenecek şekilde genişletilebilir. Daha fazla bilgi için, POS genişletilebilirlik belgelerine bakın.

## <a name="using-extended-logon"></a>Genişletilmiş oturum açmanın kullanılması

Genişletilmiş oturum açma yapılandırıldığında ve bir çalışana barkod ya da manyetik bant atandığında, o çalışanın sadece POS oturum açma sayfası ekrana geldiğinde çalışanın kartını geçirmesi veya taratması gerekir. Oturum açma işlemine devam edebilmesi için önce bir parola da gerekliyse, çalışandan parolasını girmesi istenir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
